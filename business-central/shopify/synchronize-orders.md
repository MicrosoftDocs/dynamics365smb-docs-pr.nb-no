---
title: Synkroniser og oppfyll salgsordrer
description: Definer og kjør import og behandling av salgsordre fra Shopify.
ms.date: 06/06/2023
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30110, 30111, 30112, 30113, 30114, 30115, 30121, 30122, 30123, 30128, 30129, 30150, 30151, 30145, 30147'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
---

# Synkroniser og oppfyll salgsordrer

Denne artikkelen beskriver de nødvendige innstillingene og trinnene du må fullføre for å synkronisere og oppfylle salgsordrer med Shopify i [!INCLUDE[prod_short](../includes/prod_short.md)].

## Angi importen av ordrer på Shopify-butikkortet

Angi en **valutakode** hvis nettbutikken bruker en annen valuta enn lokal valuta (LV). Den angitte valutaen må ha valutakurser konfigurert. Hvis nettbutikken bruker samme valuta som [!INCLUDE[prod_short](../includes/prod_short.md)], lar du feltet stå tomt. 

Du kan se butikkvaluta i innstillingene for [butikkdetaljer](https://www.shopify.com/admin/settings/general) i Shopify-administratoren. Shopify kan konfigureres til å godta forskjellige valutaer, men importerte ordrer til [!INCLUDE[prod_short](../includes/prod_short.md)] bruker butikkvaluta.

En vanlig Shopify-ordre kan omfatte kostnader i tillegg til delsummen, for eksempel leveringskostnader eller tips hvis aktivert. Disse beløpene bokføres direkte på finanskontoen du vil bruke for bestemte transaksjonstyper:

* **Leveringsgebyrkonto**
* **Solgt gavekortkonto**: finn ut mer under [Gavekort](synchronize-orders.md#gift-cards)
* **Tipskonto**  

Aktiver **Opprett ordrer automatisk** for å opprette salgsdokumenter automatisk i [!INCLUDE[prod_short](../includes/prod_short.md)] når Shopify-ordren importeres.

Hvis du vil frigi et salgsdokument automatisk, slår du på vekslebryteren **Frigi ordre automatisk**.

Hvis du velger feltet **Shopify-ordrenr. på dok.linje**, setter [!INCLUDE [prod_short](../includes/prod_short.md)] inn salgslinjene av typen **Kommentar** med Shopify-ordrenummeret.

>[!NOTE]
>Salgsdokumentet i [!INCLUDE[prod_short](../includes/prod_short.md)] kobles til Shopify-ordren, og du kan legge til feltet **Shopify-ordrenr.** til oversikten eller kortsidene for salgsordrer, fakturaer og levering. Hvis du vil ha mer informasjon om hvordan du legger til et felt, går du til [Slik begynner du å tilpasse en side gjennom **Tilpasning**-banneret](../ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode). 

I feltet **Avgiftsområdeprioritet** prioriterer du hvordan du velger en avgiftsområdekode for adresser på ordrer. Shopify-ordren du importerte, inneholder informasjon om avgifter. Avgifter beregnes på nytt når du oppretter salgsdokumenter, så det er viktig at mva- eller avgiftsinnstillingene er riktige i [!INCLUDE[prod_short](../includes/prod_short.md)]. Hvis du vil finne ut mer om avgifter, kan du gå til [Definer avgifter for Shopify-koblingen](setup-taxes.md).

Angi hvordan du vil behandle returer og refusjoner:

* **Tom** angir at du ikke importerer og behandler returer og refusjoner.
* **Bare import** angir at du importerer informasjon, men du oppretter den tilhørende kreditnotaen manuelt.
* **Opprett kreditnota automatisk** angir at du importerer informasjon, og [!INCLUDE[prod_short](../includes/prod_short.md)] oppretter automatisk kreditnotaene. Dette alternativet krever at du aktiverer vekslebryteren **Opprett ordre automatisk**.

Angi en lokasjon for returer og finanskontoer for refusjoner for varer og andre refusjoner.

* **Ikke-etterfylte varer for refusjonskonto** – Angir et finanskontonummer for varer der du ikke ønsker en lagerkorrigering.
* **Refusjonskonto** – Angir en finanskonto for forskjellen i totalt refundert beløp og totalbeløpet for varene.

Finn ut mer under [Returer og refusjoner](synchronize-orders.md#returns-and-refunds)

### Tildeling av leveringsmåte

**Kode for leveringsmåte** for salgsdokumenter som er importert fra Shopify, kan fylles ut automatisk. Du må konfigurere **Tildeling av leveringsmåte**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikker** og velger den relaterte koblingen.
2. Velg butikken du vil definere tildeling for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Tildeling av leveringsmåte**. Dette oppretter automatisk postene for leveringsmåter som er definert i [**Levering**](https://www.shopify.com/admin/settings/payments)-innstillingene i **Shopify-administrator**.
4. I **Navn**-feltet kan du se navnet på leveringsmåten fra Shopify.
5. Angi **leveringsmåtekoden** med den tilsvarende leveringsmåten i [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Hvis det er knyttet flere leveringsgebyrer til en ordre, går du til salg, blir bare én valgt som leveringsmåten og tildelt salgsdokumentet.

### Lokasjonstildeling

Lokasjonstilordningen er nødvendig for å fylle ut **Lokasjonskoden** for salgsdokumentlinjene som importeres fra Shopify. Dette er viktig når veksleknappen **Lokasjon obligatorisk** er aktivert på kortet **Lageroppsett**, ellers kan du ikke opprette salgsdokumenter.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikker** og velger den relaterte koblingen.
2. Velg butikken du vil konfigurere tildeling av lokasjoner for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Lokasjoner** for å åpne **Shopify-butikklokasjoner**.
4. Velg handlingen **Hent Shopify-lokasjoner** hvis du vil importere alle lokasjonene som er definert i Shopify. Du finner dem i innstillingene [**Lokasjoner**](https://www.shopify.com/admin/settings/locations) på **Shopify-administratorpanelet**. 
5. Angi **standard lokasjonskode** med tilsvarende lokasjon i [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Lokasjonstilordning er også brukt til å synkronisere lager. Hvis du vil ha mer informasjon, kan du se [Synkroniser lager til Shopify](synchronize-items.md#sync-inventory-to-shopify)
  
## Kjør ordresynkroniseringen

Fremgangsmåten nedenfor beskriver hvordan du importerer og oppdaterer ordrer.

> [!NOTE]  
> Arkiverte ordrer i Shopify kan ikke importeres. Deaktiver alternativet **Arkiver ordren automatisk** i delen **Ordrebehandling** i innstillingene **Betaling** i **Shopify-administratorpanelet** for å sørge for at alle ordrer importeres til [!INCLUDE[prod_short](../includes/prod_short.md)]. Hvis du må importere arkiverte ordrer, bruker du handlingen **Opphev arkivering av ordrer** på siden [Ordrer](https://www.shopify.com/admin/orders) i **Shopify-administratorpanelet**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikker** og velger den relaterte koblingen.
2. Velg butikken du vil importere ordrer til for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Ordrer**.
4. Velg handlingen **Synkroniser ordrer fra Shopify**.
5. Definer filtre i ordrer etter behov. Du kan for eksempel importere fullt betalte ordrer eller de med lav risikograd.

> [!NOTE]  
> Når du filtrerer etter kode, må du bruke filterkoder `@` og `*`. Hvis du for eksempel vil importere ordrer som inneholder *tag1*, bruk `@*tag1*`. `@` sikrer at resultatet skiller mellom store og små bokstaver, mens `*` finner ordrer med flere koder.

6. Velg **OK**-knappen.

Du kan eventuelt søke etter den satsvise jobben **Synkroniser ordrer fra Shopify**.

Du kan planlegge at oppgaven skal utføres automatisk. Finn ut mer under [Planlegg gjentakende oppgaver](background.md#to-schedule-recurring-tasks).

### Under panseret

Shopify-koblingen importerer ordrer i to trinn:

1.  Den importerer ordrehoder til tabellen **Shopify-ordrer som skal importeres** når de samsvarer med visse betingelser:
    
* De er ikke arkivert. Dette betyr at du kan inkludere eller ekskludere bestillinger fra synkronisering ved å arkivere eller oppheve arkivering av dem i Shopify-administratoren.
* De ble opprettet eller endret etter siste synkronisering. Dette betyr at du kan fremtvinge ny import av en bestemt ordre hvis du endrer den, for eksempel ved å legge til **Merknader** eller **Merke**.

2.  Den importerer Shopify-ordrer og tilleggsopplysninger.
* Shopify-koblingen behandler alle poster i tabellen **Shopify-ordrer som skal importeres** som tilsvarer filterkriteriene du definerte på forespørselssiden **Synkroniser ordrene fra Shopify**. Det kan for eksempel være koder, kanal eller oppfyllelsesstatus. Hvis du ikke har angitt filtre, behandler den alle postene.
* Når du importerer Shopify-ordre, ber Shopify-koblingen om ytterligere informasjon fra Shopify:

    * Ordrehode
    * Ordrelinjer
    * Informasjon om levering og oppfyllelse
    * Transaksjoner
    * Returer og refusjoner, hvis konfigurert

Siden **Shopify-ordre som skal importeres** er nyttig for feilsøking av ordreimportproblemer. Du kan vurdere tilgjengelige ordrer og ta de neste trinnene:

* Kontroller om en feil har blokkert importen av en bestemt ordre, og se detaljene om feilen. Merk av for feltet **Har feil**.
* Behandle bare bestemte ordrer. Du må fylle ut feltet **Butikkode**, velge en eller flere ordrer og deretter velge handlingen **Importer valgte ordrer**.
* Slett ordrer fra siden **Shopify-ordre som skal importeres** for å utelate dem fra synkroniseringen.

## Se gjennom importerte ordrer

Når importen er fullført, kan du utforske Shopify-ordren og finne all relatert informasjon, for eksempel betalingstransaksjonene, leveringskostnadene, risikonivået, ordreattributtene og merkene eller oppfyllelsene, hvis ordren allerede var oppfylt i Shopify. Du kan også se eventuell ordrebekreftelse som er sendt til kunden, ved å velge handlingen **Shopify-statusside**.

> [!NOTE]  
> Du kan navigere til vinduet **Shopify-ordre**, og du ser ordrer med statusen *åpen* fra alle butikker. Hvis du vil se på fullførte ordrer, må du åpne siden **Shopify-ordrer** fra det bestemte vinduet **Shopify-butikkort**.

## Opprett salgsdokumenter i Business Central

Hvis veksleknappen **Opprett ordrer automatisk** er aktivert på **Shopify-butikkortet**, prøver [!INCLUDE[prod_short](../includes/prod_short.md)] å opprette et salgsdokument etter at ordren er importert. Hvis problemer som manglede kunde eller produkt oppstår, må du løse problemene og opprette salgsordren på nytt.

### Slik oppretter du salgsdokumenter

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikker** og velger den relaterte koblingen.
2. Velg butikken du vil synkronisere ordrer med for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Ordrer**.
4. Velg ordren du vil opprette et salgsdokument for, og velg handlingen **Opprett salgsdokumenter**.
5. Velg **Ja**.

Hvis Shopify-ordren krever oppfyllelse, opprettes en **ordre**. For oppfylte Shopify-ordrer, for eksempel ordrer som bare inneholder et gavekort, eller som allerede er håndtert i Shopify, blir det opprettet en **salgsfaktura**.

Et salgsdokument er nå opprettet og kan håndteres ved hjelp av standard [!INCLUDE[prod_short](../includes/prod_short.md)]-funksjoner.

### Administrer manglende kunder

Hvis innstillingene forhindrer at du oppretter en kunde automatisk og det ikke finnes en riktig eksisterende kunde, må du angi at en kunde til Shopify-ordren manuelt. Det er noen få måter å gjøre dette på:

* Du kan tildele feltet **Salg til-kundenr.** og **Faktura til-kundenr.** direkte på siden **Shopify-ordrer** ved å velge en kunde fra oversikten over eksisterende kunder.
* Du kan velge en kundemalkode, opprette og tildele kunden via handlingen **Opprett ny kunde** på siden **Shopify-ordrer**. Legg merke til at Shopify-kunden må ha minst én adresse. Ordrer som er opprettet via Shopify-salgsstedssalgskanalen, mangler ofte adresseopplysninger.
* Du kan tildele en eksisterende kunde til den tilknyttede **Shopify-kunden** i vinduet **Shopify-kunder** og deretter velge handlingen **Søk etter tildeling** på siden **Shopify-ordrer**.

### Slik velger koblingen hvilken kunde som skal brukes

*Import ordre fra Shopify*-funksjonen prøver å velge kunder i følgende rekkefølge:

1. Hvis **Standard kundenr.** feltet er definert i **Shopify-kundemalen** for **Lever-til lands-/områdekode**, brukes deretter **Standard kundenr.** uavhengig av innstillingene i feltene **Kundeimport fra Shopify** og **Kundetildeling**. Finn ut mer under [Kundemal per land](synchronize-customers.md#customer-template-per-countryregion).
2. Hvis **Kundeimport fra Shopify** er angitt til *Ingen* og **Standard kundenr.** er definert på siden **Shopify-butikkort**, brukes **Standard kundenr.** .

Neste trinn avhenger av **Kundetildelingstype**.

* Hvis det er **Ta alltid standardkunden**, bruker tilkoblingen deretter kunden som er definert i feltet **Standard kundenr.** på siden **Shopify-butikkort**.
* Hvis det er **Via e-post/telefon**, prøver koblingen å finne eksisterende kunde med ID først, deretter med e-post og så med telefonnummer. Hvis kunden ikke blir funnet, oppretter koblingen en ny kunde.
* Hvis det er **Etter faktura til-informasjon**, prøver koblingen å finne eksisterende kunde med ID først og deretter etter faktura til-adresseinformasjon. Hvis kunden ikke blir funnet, oppretter koblingen en ny kunde.

> [!NOTE]  
> Koblingen bruker opplysninger fra faktura til-adresse og oppretter faktura til-kunde i [!INCLUDE[prod_short](../includes/prod_short.md)]. Salg til-kunden er den samme som faktura til-kunden.

### Ulike behandlingsregler for ordrer

Du vil kanskje behandle ordrer annerledes basert på en regel. Det kan for eksempel være at ordrer fra en bestemt salgskanal, for eksempel salgssted, bruker standardkunden, men du vil at nettbutikken skal ha ekte informasjon om kunden.

En måte å løse dette kravet på er å opprette et ekstra Shopify-butikkort og bruke filtre på forespørselssiden **Synkroniser ordrer fra Shopify**.

Eksempel: du har nettbutikk og et Shopify-salgssted. For salgsstedet vil du bruke en fast kunde, men for nettbutikken vil du opprette kunder i [!INCLUDE[prod_short](../includes/prod_short.md)]. Fremgangsmåten nedenfor viser en oversikt over trinn på høyt nivå. Du kan lære mer ved å gå til de tilsvarende hjelpeartiklene.

1. Opprett en Shopify-butikk som kalles *BUTIKK*, og koble den til Shopify-kontoen.
2. Konfigurer vare-/produktsynkronisering slik at denne butikken administrerer produktinformasjon.
3. Angi at kundene skal importeres med ordrer. Koblingen skal finne kunder ved å se etter e-postadressen deres. Hvis det ikke finnes noen adresse, brukes kundemalen til å opprette en ny kunde.
4. Opprett en Shopify-butikk som kalles *SALGSSTED*, og koble den til samme Shopify-konto.
6. Kontroller at vare-/produktsynkronisering er deaktivert.
7. Velg koblingen som bruker standardkunden.
8. Opprett en gjentakende prosjektkøoppføring i rapport 30104 **Synkroniser ordrer fra Shopify**. Velg **BUTIKK** i feltet **Shopify-butikkode**, og bruk filtre til å registrere alle ordrer unntatt de som opprettes av salgskanalen for SALGSSTED. Eksempel: **<>Salgssted**
9. Opprett en gjentakende prosjektkøoppføring i rapporten 30104 **Synkroniser ordrer fra Shopify**. Velg **SALGSSTED** i feltet **Shopify-butikkode**, og bruk filtre til å oppdage ordrer generert av salgskanal for SALGSSTED. Eksempel: **Salgssted**.

Hver prosjektkø importerer og behandler ordrer i de definerte filtrene og bruker reglene fra det tilsvarende Shopify-butikkortet. De oppretter for eksempel salgsstedsordrer for standardkunden.

>[!Important]
> Hvis du vil unngå konflikter under behandling av ordrer, må du huske å bruke samme prosjektkøkategori for begge prosjektkøoppføringene.

### Virkningen av ordreredigering

I Shopify:

|Rediger|Innvirkning for allerede importert ordre|Innvirkning for ordre som blir importert for første gang|
|------|-----------|-----------|
|Endre oppfyllingslokasjonen | Opprinnelig lokasjon er på linjer | Oppfyllelseslokasjon er synkronisert med [!INCLUDE[prod_short](../includes/prod_short.md)].|
|Rediger en ordre og øk antall| Ordrehodet og de supplerende tabellene blir oppdatert i [!INCLUDE[prod_short](../includes/prod_short.md)].| Importert ordre vil bruke et nytt antall|
|Rediger en ordre og reduser antall| Ordrehodet og de supplerende tabellene blir oppdatert i [!INCLUDE[prod_short](../includes/prod_short.md)].| Importert ordre vil bruke det opprinnelige antallet, feltet Antall som skal oppfylles vil inneholde en ny verdi.|
|Rediger en ordre og fjern eksisterende vare | Ordrehodet og de supplerende tabellene blir oppdatert i [!INCLUDE[prod_short](../includes/prod_short.md)].| Fjernet vare importeres fortsatt, feltet Antall som skal oppfylles inneholder null. |
|Rediger en ordre og legg til en ny vare | Ordrehodet blir oppdatert, linjer blir ikke oppdatert | Original og tilføyde varer blir importert. |
|Behandle ordre: oppfyll, oppdater betalingsinformasjon | Ordrehodet blir oppdatert, men linjer blir ikke oppdatert |Endring har ingen innvirkning på hvordan ordren importeres.|
|Annuller ordre | Ordrehodet blir oppdatert, men linjer blir ikke oppdatert |Annullert ordre importeres ikke |

Som du ser kan det i noen tilfeller være rimelig å slette redigert ordre i [!INCLUDE[prod_short](../includes/prod_short.md)] og importere den som ny.

I [!INCLUDE[prod_short](../includes/prod_short.md)]:

|Rediger|Innvirkning|
|------|-----------|
|Endre lokasjonen til en annen lokasjon, tildelt Shopify-lokasjonene. Bokfør levering. | Ordren blir merket som oppfylt. Opprinnelig lokasjon blir brukt. |
|Endre lokasjonen til en annen lokasjon, ikke tildelt Shopify-lokasjonene. Bokfør levering. | Oppfyllelsen synkroniseres ikke med Shopify. |
|Reduser antall. Bokfør levering. | Shopify-ordren blir merket som delvis fullført. |
|Øk antall. Bokfør levering. | Oppfyllelsen synkroniseres ikke med Shopify. |
|Legg til en ny vare. Bokfør levering. | Shopify-ordren blir merket som fullført. Linjene blir ikke oppdatert. |

## Synkroniser leveringer til Shopify

Når en ordre som opprettes fra en Shopify-ordre, leveres, kan du synkronisere leveringene med Shopify.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Synkroniser leveringer til Shopify**, og velg deretter den relaterte koblingen.
2. Definer filtrene på leveringer etter behov. Du kan for eksempel oppdatere en levering bokført på en bestemt dato.
3. Velg **OK**-knappen.

Ordren i Shopify blir merket som fullført. Kunden får automatisk en leveringsvarsels-e-post eller en tekstmelding (SMS). Hvis en transportør og en sporingskode er angitt i leveringen, inkluderes sporingsinformasjonen i e-posten.

Du kan også bruke handlingen **Synkroniser forsendelser** på sidene Shopify-ordrer eller Shopify-butikk.

Du kan planlegge at oppgaven skal utføres på en automatisk måte. Finn ut mer under [Planlegg gjentakende oppgaver](background.md#to-schedule-recurring-tasks).

>[!Important]
>Lokasjonen, inkludert tom lokasjon, definert i den bokførte følgeseddellinjen må ha en samsvarende post på Shopify-lokasjonen. Hvis ikke sendes ikke denne linjen tilbake til Shopify. Finn ut mer på [Lokasjonstildeling](synchronize-orders.md#location-mapping).

Husk å kjøre **Synkroniser ordrer fra Shopify** for å oppdatere oppfyllingsstatusen for en ordre i [!INCLUDE[prod_short](../includes/prod_short.md)]. Koblingsfunksjonen arkiverer også fullstendig betalte og oppfylte ordrer i både Shopify og [!INCLUDE[prod_short](../includes/prod_short.md)] gitt at betingelsene er oppfylt. 

### Transportører og sporingsnettadresse

Hvis dokumentet **Bokført følgeseddel** inneholder **Transportørkode** eller **Pakkesporingsnummer**, blir denne informasjonen sendt til Shopify og til kunden i e-posten for leveringsbekreftelse.

Sporingsfirmaet fylles ut i følgende rekkefølge (fra høyest til lavest) basert på transportørposten:

* **Shopify-sporingsselskap**
* **Navn**
* **Kode**

Hvis feltet for **pakkesporingsnettadresse** fylles ut for transportørposten, inneholder leveringsbekreftelse også en sporingsnettadresse.

## Returer og refusjoner

I en integrering mellom Shopify og [!INCLUDE[prod_short](../includes/prod_short.md)] er det viktig å kunne synkronisere så mye forretningsdata som mulig. Det gjør det enklere å holde finans- og lagernivåene oppdatert i [!INCLUDE[prod_short](../includes/prod_short.md)]. Dataene du kan synkronisere, omfatter returer og refusjoner som ble registrert i Shopify-administrator eller Shopify-salgssted.

Returer og refusjoner importeres sammen med tilknyttede ordrer hvis du aktiverte behandlingstypen på Shopify-butikkortet.

Returer importeres bare for informasjonsformål. Det finnes ingen tilknyttet behandlingslogikk.

Finans- og, om nødvendig, lagertransaksjoner behandles via refusjoner. Refusjoner kan omfatte produkter eller bare beløp, for eksempel hvis en forhandler har bestemt seg for å kompensere for forsendelseskostnader eller andre beløp.
Du kan opprette salgskreditnotaer for refusjoner. Kreditnotaene kan ha følgende linjetyper:

|Type|Nr.|Merknad|
|-|-|-|
|Finanskonto|Solgt gavekortkonto| Bruk for refusjoner knyttet til gavekort.|
|Finanskonto|Ikke-etterfylt for refusjonskonto | Brukes til refusjoner i forbindelse med produkter som ikke ble etterfylt. |
|Element |Varenr.| Brukes til refusjoner i forbindelse med produkter som ble etterfylt. Gyldig for direkte refusjoner eller refusjoner knyttet til refusjoner. Lokasjonskoden på kredittlinjen angis på grunnlag av verdien som er valgt for returlokasjonen.|
|Finanskonto| Refusjonskonto | Brukes for andre refunderte beløp som ikke er knyttet til produkter eller gavekort. Det kan for eksempel være tips eller hvis du manuelt angav beløp for refusjon i Shopify. |

>[!Note]
>Returlokasjonen, inkludert tomme lokasjoner, som er definert i **Shopify-butikkortet**, brukes på den opprettede kreditnotaen. Systemet ignorerer de opprinnelige lokasjonene fra ordrer eller forsendelser.

## Gavekort

I Shopify-butikken kan du selge gavekort, som kan brukes til å betale for virkelige produkter.

Når du håndterer gavekort, er det viktig å angi en verdi i feltet **Solgt gavekortkonto** i vinduet **Shopify-butikkort**. Det solgte gavekortet blir synkronisert sammen med ordrer på linje. Et brukt gavekort blir også importert sammen med ordren, men nå som en transaksjon. Legg merke til at gavekortet ikke reduserer beløpet som skal faktureres.

Hvis du vil gå gjennom utstedte og brukte gavekort, velger du ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Gavekort**, og velg deretter den relaterte koblingen.

## Se også

[Kom i gang med koblingen for Shopify](get-started.md)  
