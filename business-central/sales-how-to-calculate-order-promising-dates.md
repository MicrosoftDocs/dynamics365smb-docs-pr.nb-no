---
title: Beregne ordrebekreftelsesdatoer
description: Ordrebekreftelsesfunksjonen er et verktøy for beregning av når en vare tidligst kan leveres.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/29/2021
ms.author: edupont
---
# Beregne ordrebekreftelsesdatoer

Et firma må være i stand til å informere kundene om ordreleveringsdatoer. På siden **Ordrebekreftelseslinjer** kan du gjøre dette fra en salgsordre.  

[!INCLUDE[prod_short](includes/prod_short.md)] beregner forsendelses- og leveringsdatoer basert på en vares kjente og forventede tilgjengelighetsdatoer, som du deretter kan bekrefte for kunder.  

Hvis du angir en ønsket leveringsdato på en ordrelinje, brukes denne datoen som utgangspunkt for følgende beregninger:  

- ønsket leveringsdato - leveringstid = planlagt forsendelsesdato  
- planlagt forsendelsesdato - utgående lagerhåndteringstid = forsendelsesdato  

Hvis varene er tilgjengelige for plukking på forsendelsesdatoen, kan salgsprosessen fortsette. Hvis ikke varene er tilgjengelige for plukking på forsendelsesdatoen, vises en advarsel om at det er tomt på lager.  

Hvis du ikke angir en ønsket leveringsdato på ordrelinjen, eller hvis ønsket leveringsdato ikke kan innfris, beregnes datoen som varene tidligst er tilgjengelige på. Denne datoen angis deretter i feltet **Forsendelsesdato** på linjen, og datoen du planlegger å sende og levere varene til kunden på beregnes også ved hjelp av følgende beregninger.  

- forsendelsesdato + utgående lagerhåndteringstid = forsendelsesdato  
- planlagt forsendelsesdato + leveringstid = planlagt leveringsdato  

## Om ordrebekreftelse

Med funksjonen for ordrebekreftelse kan du gi løfte om at en ordre skal leveres en bestemt dato. Datoen da en vare er tilgjengelig for ordre (ATP) eller varens første mulige forsendelsesdato (CTP) beregnes, og ordrelinjer opprettes for disse datoene som du godtar. Funksjonen beregner når en vare tidligst kan leveres. Den oppretter i tillegg forslagslinjer, i tilfelle varene først må kjøpes eller produseres for datoene du godtar.

[!INCLUDE[prod_short](includes/prod_short.md)] bruker to grunnleggende begreper:  

- Tilgjengelig for ordre (ATP)  
- Første mulige forsendelsesdato (CTP)  

### Tilgjengelig for ordre (ATP)

Tilgjengelig for ordre (ATP) beregner datoer basert på reservasjonssystemet. Den utfører en tilgjengelighetskontroll for de ureserverte antallene på lager i forhold til planlagt produksjon, kjøp, overføringer og ordrereturer. Basert på denne informasjonen beregner [!INCLUDE[prod_short](includes/prod_short.md)] leveringsdatoen for kundens ordre fordi varene er tilgjengelige på lager eller i planlagte mottak.  

### Første mulige forsendelsesdato (CTP)

Første mulige forsendelsesdato (CTP) forutsetter et "Hva om"-scenario som bare gjelder for vareantall som ikke er på lager eller på planlagte ordrer. Basert på dette scenariet beregner [!INCLUDE[prod_short](includes/prod_short.md)] den tidligste datoen varen kan være tilgjengelig, hvis den skal produseres, kjøpes eller overføres.

#### Eksempel

Hvis det er ti stykker i en bestilling og seks stykker er tilgjengelige på lageret eller i planlagte ordrer, baseres beregningen av første mulige forsendelsesdato på fire stykker.

### Beregninger

Når [!INCLUDE[prod_short](includes/prod_short.md)] beregner kundens leveringsdato, utføres to oppgaver:  

- Beregner den tidligste leveringsdatoen når kunden ikke har bedt om en bestemt leveringsdato.  
- Kontrollerer om leveringsdatoen som kunden har bedt om, eller som du har lovet kunden, er realistisk.  

Hvis kunden ikke ber om en bestemt leveringsdato, brukes arbeidsdatoen som leveringsdato, og tilgjengelighet baseres deretter på denne datoen. Hvis varen er på lager, beregner [!INCLUDE[prod_short](includes/prod_short.md)] fremover i tid for å fastsette når ordren kan leveres. Dette kan gjøres med følgende formler:  

- Forsendelsesdato + Utgående lagerhåndtering = Planlagt forsendelsesdato  
- Planlagt forsendelsesdato + Leveringstid = Planlagt leveringsdato  

[!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer deretter om beregnet leveringsdato er realistisk ved å beregne bakover i tid, for å bestemme når varen må være tilgjengelig for å overholde datoen som ble lovet. Dette kan gjøres med følgende formler:  

- Planlagt forsendelsesdato - Leveringstid = Planlagt leveringsdato  
- Planlagt forsendelsesdato - Utgående lagerhåndteringstid = Forsendelsesdato  

Leveringsdatoen brukes til å utføre tilgjengelighetskontrollen. Hvis varen er tilgjengelig på denne datoen, bekrefter [!INCLUDE[prod_short](includes/prod_short.md)] at forespurt/lovet levering kan innfris ved å angi at planlagt leveringsdato skal være lik forespurt/lovet leveringsdato. Hvis varen ikke er tilgjengelig, returneres en tom dato, og ordrebehandleren kan deretter bruke CTP-funksjonalitet.  

Basert på nye datoer og klokkeslett beregnes alle relaterte datoer i henhold til formlene som er oppført tidligere i denne delen. CTP-beregningen tar lengre tid, men den gir en nøyaktig dato for når kunden kan forvente å få varen levert. Datoene som er beregnes fra CTP, vises i feltene **Planlagt lev.dato** og **Tidligste forsendelsesdato** på siden **Ordrebekreftelseslinjer**.  

Ordrebehandleren fullfører CTP-prosessen ved å godta datoene. Dette betyr at en planleggingslinje og en reservasjonspost opprettes for varen før de beregnede datoene for å sikre at ordren blir dekket.  

I tillegg til den eksterne ordrebekreftelsen som du kan utføre på siden **Ordrebekreftelseslinjer**, kan du også bekrefte interne eller eksterne leveringsdatoer for stykklistevarer. Hvis du vil ha mer informasjon, kan du se [Vise tilgjengeligheten av varer](inventory-how-availability-overview.md).

## Slik angir du ordrebekreftelser

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Oppsett for ordrebekreftelse**, og velg deretter den relaterte koblingen.  
2. Angi et nummer og en tidsenhetskode i feltet **Iverksett (tid)**. Velg én av følgende koder.  

    |Kode|Beskrivelse|  
    |----------|-----------------|  
    |**d**|Kalenderdag|  
    |**a**|Uke|  
    |**m**|Måned|  
    |**k**|Kvartal|  
    |**å**|År|  

    "3u" betyr for eksempel at Iverksett (tid) er tre uker. Bruk "n" som prefiks til en av disse kodene for å angi nåværende periode. Hvis du for eksempel vil at Iverksett (tid) skal være nåværende måned, angir du **nm**.  
3. Angi en nummerserie i feltet **Ordrebekreftelsesnr.** ved å velge en linje fra listen på siden **Nr. serie**.  
4. Angi en ordrebekreftelsesmal i feltet **Ordrebekreftelsesmal** ved å velge en linje fra oversikten på siden **Best.forslagsmal - oversikt**.  
5. Angi et bestillingsforslag i feltet **Ordrebekreftelsesskjema** ved å velge en linje fra oversikten på siden **Best.forslagsnavn**.

### Inngående og utgående lagerhåndteringstider for ordrebekreftelse

Hvis du vil at inngående lagerhåndteringstid skal tas med i beregningen av ordrebekreftelse på bestillingslinjen, kan du angi en standard håndteringstid som skal brukes på salgs- eller kjøpsdokumenter, på siden **Lageroppsett**. Du kan også angi bestemte tidspunkter for hver lokasjon på **Lokasjonskort**-siden. 

#### Angi standard inngående og utgående lagerhåndteringstider for salgs- og kjøpsdokumenter

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lageroppsett** og velg den relaterte koblingen.  
2. På hurtigfanen **Generelt** i feltene **Inngående lagerhåndteringstid** og **Utgående lagerhåndteringstid** angir du hvor mange dager som skal tas med i beregningene av ordrebekreftelsen.  

#### Angi inngående og utgående lagerhåndteringstider på lokasjoner

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Lokasjon**, og velg deretter den relaterte koblingen.  
2.  Åpne det aktuelle lokasjonskortet.  
3.  På hurtigfanen **Lager** i feltene **Inngående lagerhåndteringstid** og **Utgående lagerhåndteringstid** angir du hvor mange dager du vil skal tas med i beregningene av ordrebekreftelsen.  

> [!NOTE]  
>  Hvis du velger **Lokasjon** i feltet **Forsendelsesadresse** i hurtigfanen **Levering og betaling** og deretter velger en lokasjon i **Lokasjonskode**-feltet når du oppretter en bestilling, bruker feltene **Utgående lagerhåndteringstid** og **Inngående lagerhåndteringstid** håndteringstiden som er angitt for lokasjonen. Det samme gjelder for salgsordrer hvis du velger en lokasjon i **Lokasjonskode**-feltet. Hvis ingen håndteringstid er angitt for lokasjonen, er feltene **Utgående lagerhåndteringstid** og **Inngående lagerhåndteringstid** tomme. Hvis du lar **Lokasjonskode**-feltet stå tomt på salgs- og kjøpsdokumenter, brukes håndteringsverdien som er angitt på **Lageroppsett**-siden, i beregningen.

## Slik gjør du en vare kritisk

Før en vare kan inkluderes i beregningen av ordrebekreftelsen, må den være merket som kritisk. Dette oppsettet sikrer at ikke-kritiske varer ikke fører til uaktuell beregning av ordrebekreftelser.   
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.  
2.  Åpne det aktuelle varekortet.  
3.  På hurtifganen **Planlegging** velger du **Kritisk**-feltet.  

## Slik beregner du en ordrebekreftelsesdato

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordre**, og velg deretter den relaterte koblingen.  
2.  Åpne den aktuelle ordren, og velg ordrelinjene du vil at programmet skal beregne.  
3.  Velg handlingen **Ordrebekreftelse** og deretter **Ordrebekreftelseslinjer**.  
4.  Velg en linje, og velg deretter ett av følgende alternativer:  

    - Velg **Tilgjengelig for ordre (ATP)** hvis du vil beregne når varen tidligst vil være tilgjengelig med hensyn til beholdning, tidsplanlagte mottak og bruttobehov.  
    - Velg **Første mulige forsendelsesdato (CTP)** hvis du vet at varen er utsolgt fra lager og du vil beregne når varen tidligst vil være tilgjengelig når du utsteder nye etterfyllingsforslag.  
5.  Velg **Godta**-knappen for å godta den tidligste leveringsdatoen som er tilgjengelig.  

## Se relatert [Microsoft-opplæring](/training/modules/promising-sales-order-delivery-dynamics-365-business-central/)

## Se også

[Salg](sales-manage-sales.md)  
[Beregne dato for kjøp](purchasing-date-calculation-for-purchases.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
