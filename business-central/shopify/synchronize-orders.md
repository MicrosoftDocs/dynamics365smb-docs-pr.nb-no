---
title: Synkroniser og oppfyll salgsordrer
description: Definer og kjør import og behandling av ordrer fra Shopify.
ms.date: 03/25/2024
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

Du kan åpne butikkvalutaen i innstillingene for [butikkdetaljer](https://www.shopify.com/admin/settings/general) i Shopify-administratoren. Shopify kan konfigureres til å godta forskjellige valutaer. Importerte ordrer i [!INCLUDE[prod_short](../includes/prod_short.md)] bruker butikkvaluta.

En vanlig Shopify-ordre kan omfatte kostnader i tillegg til delsummen, for eksempel leveringskostnader eller tips hvis aktivert. Disse beløpene bokføres direkte på finanskontoen du vil bruke for bestemte transaksjonstyper:

* **Leveringsgebyrkonto**
* **Solgt gavekortkonto**: finn ut mer under [Gavekort](synchronize-orders.md#gift-cards)
* **Tipskonto**  

Aktiver **Opprett ordrer automatisk** for å opprette salgsdokumenter automatisk i [!INCLUDE[prod_short](../includes/prod_short.md)] når Shopify-ordren importeres.

Hvis du vil frigi et salgsdokument automatisk, slår du på vekslebryteren **Frigi ordre automatisk**.

Hvis du ikke vil sende automatiske leveringsbekreftelser til kunder, slår du av veksleknappen **Send leveringsbekreftelse** . Det kan være nyttig å slå av bryteren hvis du selger digitale varer eller vil bruke en annen varslingsmekanisme.

Hvis du velger feltet **Shopify-ordrenr. på dok.linje**, setter [!INCLUDE [prod_short](../includes/prod_short.md)] inn salgslinjene av typen **Kommentar** med Shopify-ordrenummeret.

> [!NOTE]
> Salgsdokumentet i [!INCLUDE[prod_short](../includes/prod_short.md)] kobles til Shopify-ordren, og du kan legge til feltet **Shopify-ordrenr.** til oversikten eller kortsidene for salgsordrer, fakturaer og leveringer. Hvis du vil ha mer informasjon om å legge til et felt, kan du gå til [Start tilpasning ved å bruke tilpasningsmodus](../ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode). 

I feltet **Avgiftsområdeprioritet** prioriterer du hvordan du velger en avgiftsområdekode for adresser på ordrer. Shopify-ordren du importerte, inneholder informasjon om avgifter. Avgifter beregnes på nytt når du oppretter salgsdokumenter, så det er viktig at mva- eller avgiftsinnstillingene er riktige i [!INCLUDE[prod_short](../includes/prod_short.md)]. Hvis du vil finne ut mer om avgifter, kan du gå til [Definer avgifter for Shopify-koblingen](setup-taxes.md).

Angi hvordan du vil behandle returer og refusjoner:

* **Tom** angir at du ikke importerer og behandler returer og refusjoner.
* **Bare import** angir at du importerer informasjon, men du oppretter den tilhørende kreditnotaen manuelt.
* **Opprett kreditnota automatisk** angir at du importerer informasjon, og [!INCLUDE[prod_short](../includes/prod_short.md)] oppretter automatisk kreditnotaene. Dette alternativet krever at du aktiverer vekslebryteren **Opprett ordre automatisk**.

Angi en lokasjon for returer og finanskontoer for refusjoner for varer og andre refusjoner.

* **Ikke-etterfylte varer for refusjonskonto** angir et finanskontonummer for varer der du ikke ønsker en lagerkorrigering.
* **Refusjonskonto** angir en finanskonto for forskjellen i totalt refundert beløp og totalbeløpet for varene.

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
> Lokasjonstildeling brukes også til å synkronisere lageret. Hvis du vil ha mer informasjon, kan du gå til [Synkroniser lager med Shopify](synchronize-items.md#sync-inventory-to-shopify).
  
## Kjør ordresynkroniseringen

Fremgangsmåten nedenfor beskriver hvordan du importerer og oppdaterer ordrer.

> [!NOTE]  
> Arkiverte ordrer i Shopify kan ikke importeres. Hvis du må kontrollere ordrestatusen, åpner du ordren fra [ordresiden](https://www.shopify.com/admin/orders) i panelet **Shopify-administrator** og ser gjennom ordredetaljene.
> 
> Deaktiver alternativet **Arkiver ordren automatisk** i delen **Ordrebehandling** i innstillingene **Betaling** i **Shopify-administratorpanelet** for å sørge for at alle ordrer importeres til [!INCLUDE[prod_short](../includes/prod_short.md)]. Hvis du må importere arkiverte ordrer, bruker du handlingen **Opphev arkivering av ordrer** på siden [Ordrer](https://www.shopify.com/admin/orders) i **Shopify-administratorpanelet**. 

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

1. Den importerer ordrehoder til tabellen **Shopify-ordrer som skal importeres** når de samsvarer med visse betingelser:

   * De er ikke arkivert. Dette betyr at du kan inkludere eller ekskludere bestillinger fra synkronisering ved å arkivere eller oppheve arkivering av dem i Shopify-administratoren.
   * De ble opprettet eller endret etter siste synkronisering. Dette betyr at du kan fremtvinge ny import av en bestemt ordre hvis du endrer den, for eksempel ved å legge til **Merknader** eller **Merke**.

2. Den importerer Shopify-ordrer og tilleggsopplysninger.

   * Shopify-koblingen behandler alle poster i tabellen **Shopify-ordrer som skal importeres** som tilsvarer filterkriteriene du definerte på forespørselssiden **Synkroniser ordrene fra Shopify**. Det kan for eksempel være koder, kanal eller oppfyllelsesstatus. Hvis du ikke har angitt filtre, behandler den alle postene.
   * Når du importerer en Shopify-ordre, ber Shopify-koblingen om ytterligere informasjon fra Shopify:

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
> Du kan navigere til vinduet **Shopify-ordre**, og du ser ordrer med statusen *åpen* fra alle butikker. Hvis du vil se på fullførte ordrer, må du åpne siden **Shopify-ordrer** fra den spesifikke siden **Shopify-butikkort**.

Før salgsdokumenter opprettes i [!INCLUDE[prod_short](../includes/prod_short.md)], kan du bruke handlingen **Synkroniser ordre fra Shopify** på siden **Shopify-ordre** til å importere bestemte ordrer på nytt.

Du kan også merke en bestilling som betalt, noe som er nyttig i et B2B-scenario der betalinger behandles utenfor Shopify-kassen. Velg handlingen **Merk som betalt** på siden **Shopify-ordre**. Du kan også merke en ordre som kansellert for å starte refusjonsflyten i Shopify. Velg handlingen **Annuller ordre** på siden **Shopify-ordre**, fyll ut feltene etter behov på siden **Annuller Shopify-ordre**, og trykk på **OK**. Du må kjøre ordresynkronisering for å importere oppdateringene til [!INCLUDE[prod_short](../includes/prod_short.md)].

## Opprett salgsdokumenter i Business Central

Hvis veksleknappen **Opprett ordrer automatisk** er aktivert på **Shopify-butikkortet**, prøver [!INCLUDE[prod_short](../includes/prod_short.md)] å opprette et salgsdokument etter at ordren er importert. Hvis problemer som manglede kunde eller produkt oppstår, må du løse problemene og opprette salgsordren på nytt.

### Slik oppretter du salgsdokumenter

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikker** og velger den relaterte koblingen.
2. Velg butikken du vil synkronisere ordrer med for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Ordrer**.
4. Velg ordren du vil opprette et salgsdokument for, og velg handlingen **Opprett salgsdokumenter**.
5. Velg **Ja**.

Hvis Shopify-ordren krever oppfyllelse, opprettes en **ordre**. For oppfylte Shopify-ordrer, for eksempel ordrer som bare inneholder et gavekort, eller som allerede er håndtert i Shopify, blir det opprettet en **salgsfaktura**.

Et salgsdokument opprettes og kan håndteres ved hjelp av standard [!INCLUDE[prod_short](../includes/prod_short.md)]-funksjoner.

Hvis du vil opprette salgsdokument på nytt, kan du bruke handlingen **Opphev kobling til behandlede dokumenter** på siden **Shopify-ordre**. Vær oppmerksom på at denne handlingen ikke sletter allerede opprettede salgsdokumenter. Du må behandle det manuelt.

### Administrer manglende kunder

Hvis innstillingene forhindrer at du oppretter en kunde automatisk og det ikke finnes en samsvarende kunde, må du angi en kunde til Shopify-ordren manuelt. Du kan tilordne kunder til ordrer på flere måter:

* Tilordne **Salg til-kundenr.** og **Faktura til-kundenr.** direkte på siden **Shopify-ordrer** ved å velge en kunde fra oversikten over eksisterende kunder.
* Velg en kundemal, opprett og tildel kunden via handlingen **Opprett ny kunde** på siden **Shopify-ordrer**. Shopify-kunden må ha minst én adresse. Ordrer du oppretter via Shopify-salgsstedssalgskanalen, mangler ofte adresseopplysninger.
* Tildel en eksisterende kunde til den tilknyttede **Shopify-kunden** på siden **Shopify-kunder**, og velg deretter handlingen **Søk etter tildeling** på siden **Shopify-ordrer**.

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

For B2B-ordrer er flyten er den samme, selv om koblingen bruker feltene **Standard selskapsnr.**, **Selskapsimport fra Shopify** og **Tildelingstype for selskap** på siden **Shopify-butikkort**. Legg merke til at det ikke finnes noe **Standard selskapsnr.** i **Shopify-kundemalen**, fordi det forventes at B2B har navngitte kunder.

### Ulike behandlingsregler for ordrer

Du vil kanskje behandle ordrer annerledes basert på en regel. Det kan for eksempel være at ordrer fra en bestemt salgskanal, for eksempel salgssted, bruker standardkunden, men du vil at nettbutikken skal ha ekte informasjon om kunden.

En måte å løse dette kravet på er å opprette et ekstra Shopify-butikkort og bruke filtre på forespørselssiden **Synkroniser ordrer fra Shopify**.

Eksempel: Du har en nettbutikk og et Shopify-salgssted. For salgsstedet vil du bruke en fast kunde, men for nettbutikken vil du opprette kunder i [!INCLUDE[prod_short](../includes/prod_short.md)]. Fremgangsmåten nedenfor viser en oversikt over trinn på høyt nivå. Du kan lære mer ved å gå til de tilsvarende hjelpeartiklene.

1. Opprett en Shopify-butikk som kalles *BUTIKK*, og koble den til Shopify-kontoen.
1. Konfigurer vare-/produktsynkronisering slik at denne butikken administrerer produktinformasjon.
1. Angi at kundene skal importeres med ordrer. Koblingen skal finne kunder ved å se etter e-postadressen deres. Hvis det ikke finnes noen adresse, brukes kundemalen til å opprette en ny kunde.
1. Opprett en Shopify-butikk som kalles *SALGSSTED*, og koble den til samme Shopify-konto.
1. Kontroller at vare-/produktsynkronisering er deaktivert.
1. Velg koblingen som bruker standardkunden.
1. Opprett en gjentakende prosjektkøoppføring i rapport 30104 **Synkroniser ordrer fra Shopify**. Velg **BUTIKK** i feltet **Shopify-butikkode**, og bruk filtre til å registrere alle ordrer unntatt de som opprettes av salgskanalen for SALGSSTED. Eksempel: **<>Salgssted**
1. Opprett en gjentakende prosjektkøoppføring i rapport 30104 **Synkroniser ordrer fra Shopify**. Velg **SALGSSTED** i feltet **Shopify-butikkode**, og bruk filtre til å oppdage ordrer generert av salgskanal for SALGSSTED. Eksempel: **Salgssted**.

Hver prosjektkø importerer og behandler ordrer i de definerte filtrene og bruker reglene fra det tilsvarende Shopify-butikkortet. De oppretter for eksempel salgsstedsordrer for standardkunden.

> [!Important]
> Hvis du vil unngå konflikter under behandling av ordrer, må bruke samme prosjektkøkategori for begge prosjektkøoppføringene.

### Virkningen av ordreredigering

I Shopify:

|Rediger|Innvirkning på Shopify-ordrer som ennå ikke er behandlet i [!INCLUDE[prod_short](../includes/prod_short.md)] | Innvirkning på Shopify-ordrer som allerede er behandlet i [!INCLUDE[prod_short](../includes/prod_short.md)] |
|------|-----------|-----------|
|Endre oppfyllingslokasjonen | Oppfyllelseslokasjon er synkronisert med [!INCLUDE[prod_short](../includes/prod_short.md)]. | Oppfyllelseslokasjon er synkronisert med [!INCLUDE[prod_short](../includes/prod_short.md)].|
|Rediger en ordre og øk antall|Importert ordre vil bruke et nytt antall.| Koblingen vil oppdage endringen og merke ordren. |
|Rediger en ordre og reduser antall|Importert ordre vil bruke et nytt antall. Shopify-refusjon med beløp på 0 vil bli importert, og dette kan ikke konverteres til en kreditnota.| Koblingen vil oppdage endringen og merke ordren. |
|Rediger en ordre og fjern eksisterende vare |Fjernet vare blir ikke importert. Shopify-refusjon med beløp på 0 vil bli importert, og dette kan ikke konverteres til en kreditnota.| Koblingen vil oppdage endringen og merke ordren. |
|Rediger en ordre og legg til en ny vare | Original og tilføyde varer blir importert. | Koblingen vil oppdage endringen og merke ordren. |
|Behandle ordre: oppfyll, oppdater betalingsinformasjon | Ordrehodet blir oppdatert. |Ordrehodet blir oppdatert. Oppfyllelsen synkroniseres ikke med Shopify.|
|Annuller betalt ordre | Ordrehodet vil bli oppdatert, for å bli behandlet separat |Koblingen vil oppdage endringen og merke ordren. |
|Annuller ubetalt ordre | Fjernet vare blir ikke importert. Shopify-refusjon med beløp på 0 vil bli importert, og dette kan ikke konverteres til kreditnota. |Koblingen vil oppdage endringen og merke ordren. |

Hvis en ordre allerede er behandlet i [!INCLUDE[prod_short](../includes/prod_short.md)], vil følgende feilmelding vises i koblingen: *Ordren er allerede behandlet i Business Central, men en utgave ble mottatt fra Shopify. Endringer ble ikke overført til den behandlede ordren i Business Central. Oppdater de behandlede dokumentene slik at de samsvarer med de mottatte dataene fra Shopify. Hvis du vil fremtvinge synkroniseringen, bruker du handlingen "Synkroniser ordre fra Shopify" på kortsiden Shopify-ordre.*

Avhengig av statusen til det opprettede salgsdokumentet kan du utføre følgende handlinger:

1. Slett opprettet salgsdokument
2. Velg handlingen **Opphev kobling til behandlede dokumenter** for å tilbakestille **Behandlet**-indikatoren.
3. Velg handlingen **Synkroniser ordre fra Shopify** for å oppdatere enkeltordrer med nylige data fra Shopify.

I [!INCLUDE[prod_short](../includes/prod_short.md)]:

|Rediger|Innvirkning|
|------|-----------|
|Endre plasseringen til en annen plassering. Bokfør levering. | Ordren blir merket som fullført. Oppfyllelseslokasjon fra Shopify vil bli brukt. |
|Reduser antall. Bokfør levering. | Shopify-ordren blir merket som delvis fullført. |
|Øk antall. Bokfør levering. | Oppfyllelsen synkroniseres ikke med Shopify. Det er det samme hvis oppfyllelsen ble delt i Shopify, men behandlet som en linje i [!INCLUDE[prod_short](../includes/prod_short.md)]. |
|Legg til en ny vare. Bokfør levering. | Shopify-ordren blir merket som fullført. Nye linjer blir ikke lagt til. |

## Synkroniser leveringer til Shopify

Når en ordre som opprettes fra en Shopify-ordre, leveres, kan du synkronisere leveringene med Shopify.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Synkroniser leveringer til Shopify**, og velg deretter den relaterte koblingen.
2. Definer filtrene på leveringer etter behov. Du kan for eksempel oppdatere en levering bokført på en bestemt dato.
3. Velg **OK**.

Ordren i Shopify blir merket som fullført. Kunden får automatisk en leveringsvarsels-e-post eller en tekstmelding (SMS). Hvis en transportør og en sporingskode er angitt i leveringen, inkluderes sporingsinformasjonen i e-posten.

Du kan også bruke handlingen **Synkroniser forsendelser** på sidene Shopify-ordrer eller Shopify-butikk.

Du kan planlegge at oppgaven skal utføres på en automatisk måte. Finn ut mer under [Planlegg gjentakende oppgaver](background.md#to-schedule-recurring-tasks).

> [!Important]
> Lokasjonen, inkludert tom lokasjon, definert i den bokførte følgeseddellinjen må ha en samsvarende post på Shopify-lokasjonen. Hvis ikke sendes ikke denne linjen tilbake til Shopify. Finn ut mer på [Lokasjonstildeling](synchronize-orders.md#location-mapping).

Husk å kjøre **Synkroniser ordrer fra Shopify** for å oppdatere oppfyllingsstatusen for en ordre i [!INCLUDE[prod_short](../includes/prod_short.md)]. Koblingsfunksjonen arkiverer også fullstendig betalte og oppfylte ordrer i både Shopify og [!INCLUDE[prod_short](../includes/prod_short.md)] gitt at betingelsene er oppfylt. 

### Transportører og sporingsnettadresse

Hvis dokumentet **Bokført følgeseddel** inneholder **Transportørkode** eller **Pakkesporingsnummer**, blir denne informasjonen sendt til Shopify og til kunden i e-posten for leveringsbekreftelse.

Sporingsfirmaet fylles ut i følgende rekkefølge (fra høyest til lavest) basert på transportørposten:

1. **Shopify-sporingsselskap**
1. **Navn**
1. **Kode**

Hvis feltet for **pakkesporingsnettadresse** fylles ut for transportørposten, inneholder leveringsbekreftelse også en sporingsnettadresse.

## Returer og refusjoner

I en integrering mellom Shopify og [!INCLUDE[prod_short](../includes/prod_short.md)] er det viktig å kunne synkronisere så mye forretningsdata som mulig. Det gjør det enklere å holde finans- og lagernivåene oppdatert i [!INCLUDE[prod_short](../includes/prod_short.md)]. Dataene du kan synkronisere, omfatter returer og refusjoner som ble registrert i Shopify-administrator eller Shopify-salgssted.

Returer og refusjoner importeres sammen med tilknyttede ordrer hvis du aktiverte behandlingstypen på Shopify-butikkortet.

Returer importeres bare for informasjonsformål. Ingen behandlingslogikk er tilknyttet dem.

Finans- og, om nødvendig, lagertransaksjoner behandles via refusjoner. Refusjoner kan omfatte produkter eller bare beløp, for eksempel hvis en forhandler bestemmer seg for å kompensere for forsendelseskostnader eller andre beløp.

Du kan opprette salgskreditnotaer for refusjoner. Kreditnotaene kan ha følgende linjetyper:

|Type|Nr.|Merknad|
|-|-|-|
|Finanskonto|Solgt gavekortkonto| Bruk for refusjoner knyttet til gavekort.|
|Finanskonto|Ikke-etterfylt for refusjonskonto | Brukes til refusjoner i forbindelse med produkter som ikke ble etterfylt. |
|Element |Varenr.| Brukes til refusjoner i forbindelse med produkter som ble etterfylt. Gyldig for direkte refusjoner eller refusjoner knyttet til refusjoner. Lokasjonskoden på kredittlinjen angis på grunnlag av verdien som er valgt for returlokasjonen.|
|Finanskonto| Refusjonskonto | Brukes for andre refunderte beløp som ikke er knyttet til produkter eller gavekort. Det kan for eksempel være tips eller hvis du manuelt angav beløp for refusjon i Shopify. |

> [!Note]
> Returlokasjonene, inkludert tomme lokasjoner, som er definert i **Shopify-butikkortet**, brukes på den opprettede kreditnotaen. Systemet ignorerer de opprinnelige lokasjonene fra ordrer eller forsendelser.

## Gavekort

I Shopify-butikken kan du selge gavekort, som kan brukes til å betale for virkelige produkter.

Når du håndterer gavekort, er det viktig å angi en verdi i feltet **Solgt gavekortkonto** i vinduet **Shopify-butikkort**. Det solgte gavekortet blir synkronisert sammen med ordrer på linje. Et brukt gavekort blir også importert sammen med ordren, men nå som en transaksjon. Legg merke til at gavekortet ikke reduserer beløpet som skal faktureres.

Hvis du vil gå gjennom utstedte og brukte gavekort, velger du ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Gavekort**, og velg deretter den relaterte koblingen.

## Se også

[Kom i gang med Shopify-koblingen](get-started.md)  
