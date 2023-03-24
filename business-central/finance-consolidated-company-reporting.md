---
title: Konsolidere data fra flere selskaper
description: Dette emnet forklarer hvordan du kan konsolidere finanspostene fra to eller flere atskilte selskaper (datterselskaper) i et konsolidert selskap.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.date: 06/16/2021
ms.author: edupont
---

# Konsolidere finansielle data fra flere selskaper

Noen organisasjoner bruker [!INCLUDE [prod_short](includes/prod_short.md)] i flere konsern eller juridiske enheter. Andre bruker [!INCLUDE [prod_short](includes/prod_short.md)] i datterselskaper som må rapportere til overordnede organisasjoner. I begge tilfeller bruker regnskapsførere innebygde verktøy til å konsolidere regnskapsdataene.  

Du kan konsolidere finanspostene fra to eller flere atskilte selskaper (datterselskaper) i et konsolidert selskap. Hvert enkelt selskap som er involvert i en konsolidering, kalles et konsern. Det kombinerte selskapet kalles de konsoliderte selskapet.  

Du kan importere data til det konsoliderte selskapet fra andre selskaper i samme [!INCLUDE [prod_short](includes/prod_short.md)]-leietaker, fra leietakere eller fra filer.  

Hvis årsregnskapene i et konsern er i en annen valuta enn i det konsoliderte selskapet, må du definere valutakurser for konsolidering.  

Du kan konsolidere:  

* På tvers av selskaper med ulike kontoplaner.  
* Selskaper med ulike regnskapsår og i ulike valutaer.  
* Hele beløpet eller en prosentdel av den økonomiske informasjonen i et selskap
* Bruke ulike valutakurser i individuelle finanskontoer
* Selskaper i andre regnskaps- og forretningsstyringsprogrammer

Du definerer det konsoliderte selskapet på samme måte som du definerer andre selskaper. Kontoplanen er uavhengig av kontoplanen i de andre konsernene, og kontoplanene i de individuelle konsernene kan være forskjellige. Du setter opp en liste over selskaper som skal konsolideres, bekrefter regnskapsdataene før konsolidering, importerer fra filer eller databaser og genererer konsolideringsrapporter. Du finner mer informasjon under [Konfigurere selskapskonsolidering](finance-consolidated-company-reporting-setup.md).  

> [!TIP]
> Konsolidere økonomisk data kan være spesielt aktuelt i forbindelse med konserninterne prosesser. Hvis du vil ha mer informasjon, kan du se [Behandle konserninterne transaksjoner](intercompany-manage.md).

## Råbalanse

Hvis du har mer enn ett selskap i [!INCLUDE[prod_short](includes/prod_short.md)], kan rapporten **Konsolidert råbalanse** gi deg en samlet oversikt over den økonomiske situasjonen.  

Rapporten kombinerer finansposter fra hvert av selskapene i et nytt selskap du oppretter med de konsoliderte dataene. Dette selskapet kalles vanligvis for "det konsoliderte selskapet". Det konsoliderte selskapet er bare en beholder for de konsoliderte dataene og har ikke noen live forretningsdata. Selskapene du tar med i det konsoliderte selskapet, blir **Konserner** i rapporten. Du finner mer informasjon under [Konfigurere selskapskonsolidering](finance-consolidated-company-reporting-setup.md).  

## Konsolidere data

Prosessen med å overføre tall fra konsernene til det konsoliderte selskapet er den faktiske *konsolideringen*. Før du gjør dette, er det lurt å kontrollere om det er forskjell på de grunnleggende opplysningene for konsernene og konsoliderte selskapene. Det finnes to rapporter du kan bruke til å teste databasen og filen.

### Slik tester du dataene før konsolidering

Du kan teste dataene før du overfører dem til det konsoliderte selskapet. [!INCLUDE[prod_short](includes/prod_short.md)] ser etter forskjeller mellom informasjonen i konsernet og det konsoliderte selskapet. Dette kan for eksempel være om kontonumre eller dimensjonskoder er forskjellige. Du må korrigere feilene før du kan kjøre rapporten. Du kan teste databasen, eller hvis du importerer data fra en XML-fil, kan du teste filen.  

1. Åpne det konsoliderte selskapet.  
2. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konsern**, og velg deretter den relaterte koblingen.  
3. Gjør ett av følgende:  

    * For å teste en fil velger du **Test fil**, angir navnet på filen som skal testes, og velger deretter **Skriv ut**.  
    * Hvis du vil teste databasen, kan du velge **Test database**.  

### Kjøre konsolideringen

Når du har testet dataene, kan du overføre dem til det konsoliderte selskapet.  

1. Logg deg på det konsoliderte selskapet.  
2. I **Regnskapsfører-rollesenteret** velger du **Kjør konsolidering**.  
3. Fyll ut de obligatoriske feltene.  
4. I Filter-delen definerer du et filter for det relevante konsernet eller selskapsnavnet.  
5. Du kan også planlegge at en rapport skal kjøres på et passende tidspunkt.  

## Fjerne gjentatte transaksjoner

Når du har konsolidert alle selskapene, må du finne transaksjoner som er registrert mer enn én gang på tvers av flere selskaper, og deretter postere elimineringsoppføringer for å fjerne dem.

Behandle konsoliderte elimineringer i en manuell prosess.  

Slik fjerner du gjentatte transaksjoner:

1. Finn transaksjoner som potensielt må justeres, og angi finanskladdelinjer for å fjerne dem.
2. Kjør rapporten **Konsoliderte elimineringer for finans** for å vurdere resultatet av finanskladdelinjene før bokføringen.
3. Bokfør justeringstransaksjonene.

Rapporten **Konsoliderte elimineringer for finans** viser en foreløpig råbalanse der du kan simulere konsekvensene av å eliminere postene gjennom å sammenligne postene i det konsoliderte selskapet med elimineringene som er angitt i finanskladden.

For at et konsern skal kunne inngå i rapporten, må det være opprettet på siden **Konsern**, og feltet **Konsolider** må være valgt.

Hver konto skrives ut på en egen linje, i likhet med kontoplanens oppbygning. En konto skrives ikke ut hvis alle beløp på linjen er 0. Følgende opplysningene vises om hver konto:

* Kontonummer
* Kontonavn.
* Hvis du har valgt én eller flere konsernkoder i feltet **Konsernkode** på forespørselssiden, vises totalen for det konsoliderte selskapet ekskl. de valgte konsernene og elimineringene. Hvis du ikke har fylt ut feltet **Konsernkode**, vises totalen for det konsoliderte selskapet ekskl. elimineringer.
* Hvis du har valgt en konsernkode i feltet **Konsernkode** på forespørselssiden, vises totalen for de innleste postene fra konsernet. Hvis du ikke har fylt ut feltet **Konsernkode**, vises totalen for bokførte elimineringer i det konsoliderte selskapet.
* Totalen for det konsoliderte selskapet med alle konsern og alle bokførte elimineringer.
* De elimineringer som skal foretas i det konsoliderte selskapet, det vil si poster i den finanskladden som er valgt på forespørselssiden.
* Bokføringsteksten kopiert fra finanskladden.
* Det konsoliderte selskapets total etter elimineringen hvis den bokføres.

## Eksportere og importere konsoliderte data mellom databaser

Hvis data for et konsern er i en annen database, må du eksportere dataene til en fil før du kan inkludere dem i konsolideringen. Hvert selskap må eksporteres separat. Til dette formålet brukes kjørselen **Eksporter konsolidering**.  

> [!TIP]
> Bruk samme fremgangsmåte for å eksportere konsoliderte data som må sendes til Dynamics 365 Finance, for eksempel hvis det aktuelle konsernet er et datterselskap og moderselskapet bruker Dynamics 365 Finance.

Når du kjører den satsvise jobben, behandles alle postene i finanskontiene. For hver kombinasjon av valgte dimensjoner og dato legges innholdet fra postenes **Beløp**-felt sammen og eksporteres. Neste kombinasjon av valgte dimensjoner og dato med samme kontonummer blir behandlet, deretter behandles kombinasjonene for neste kontonummer og så videre.  

De eksporterte postene inneholder følgende felt: **Kontonr.**, **Bokføringsdato** og **Beløp**. Hvis dimensjonsinformasjon også ble eksportert, er dimensjonskoder og dimensjonsverdier også inkludert.  

1. For hver eksporterte linje eksporteres kontonummeret som er definert i konsernets **Kons. debetkonto**-felt, til linjen, hvis summen i **Beløp**-feltene er et debetbeløp. Hvis summen er et kreditbeløp, eksporteres det tilsvarende nummeret i **Kons. kreditkonto**-feltet til linjen.  
2. Datoen som brukes for hver eksporterte linje, er periodens sluttdato eller den nøyaktige datoen for beregningen, hvis overføringen skjer hver dag.  
3. Dimensjonsverdien som eksporteres for posten, vil være dimensjonsverdien for det konsoliderte selskapet som er definert i **Konsolideringskode**-feltet for den aktuelle dimensjonsverdien. Hvis ingen dimensjonsverdi for konsolidert selskap er angitt i **Konsolideringskode**-feltet for den aktuelle dimensjonsverdien, vil selve dimensjonsverdien bli eksportert til linjen.  
4. XML-filene inneholder også valutakursene i konsolideringsperioden. Disse kursene er inkludert i en separat del på begynnelsen av filen.  

## Se også

[Konfigurere selskapskonsolidering](finance-consolidated-company-reporting-setup.md)  
[Behandle konserninterne transaksjoner](intercompany-manage.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Eksporter forretningsdataene til Excel](about-export-data.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]