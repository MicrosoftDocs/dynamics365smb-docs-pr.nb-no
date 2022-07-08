---
title: Synkroniser og oppfyll salgsordrer
description: Definer og kjør import og behandling av salgsordre fra Shopify.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: ce11aa8766550e72cab2f811ef6602dba4271211
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9076308"
---
# <a name="synchronize-and-fulfill-sales-orders"></a>Synkroniser og oppfyll salgsordrer

Denne artikkelen beskriver de nødvendige innstillingene og trinnene du må utføre for å synkronisere og oppfylle salgsordrer fra Shopify i [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="set-the-import-of-orders-on-the-shopify-shop-card"></a>Angi importen av ordrer på Shopify-butikkortet

En vanlig Shopify-ordre kan ha ekstra beløp øverst, for eksempel leveringskostnader eller tips hvis aktivert. Disse beløpene bokføres direkte på finanskontoene. Velg finanskontoen som skal brukes til spesifikke transaksjoner:

- **Leveringskostnadskonto**
- **Solgt gavekortkonto** hvis du vil ha mer informasjon, kan du se [Gavekort](synchronize-orders.md#gift-cards).
- **Tipskonto**  

Aktiver **Opprett ordrer automatisk** for å opprette salgsdokumenter automatisk i [!INCLUDE[prod_short](../includes/prod_short.md)] når Shopify-ordren importeres.
Salgsdokumentet i [!INCLUDE[prod_short](../includes/prod_short.md)] inneholder en kobling til Shopify-ordren. Hvis du velger feltet **Shopify-ordrenr. på dok.linje**, gjentas denne informasjonen på salgslinjene av typen *Merknad*.

I feltet **Mva-områdekode** kan du definere prioritet for hvordan du velger mva-områdekode eller mva-bokføringsgruppe for firma basert på adresse. Dette trinnet er relevant for land med merverdiavgift, men kan brukes for mva-land. Hvis du vil ha mer informasjon, kan du se [Avgiftsmerknader](synchronize-orders.md#tax-remarks).

### <a name="shipment-method-mapping"></a>Tildeling av leveringsmåte

**Kode for leveringsmåte** for salgsdokumenter som er importert fra Shopify, kan fylles ut automatisk. Du må konfigurere **Tildeling av leveringsmåte**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikker** og velger den relaterte koblingen.
2. Velg butikken du vil definere tildeling for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Tildeling av leveringsmåte**. Postene for leveringsmåter som er definert i [**Levering**](https://www.shopify.com/admin/settings/payments)-innstillingene i **Shopify-administrator**, opprettes automatisk.
4. I **Navn**-feltet kan du se navnet på leveringsmåten fra Shopify.
5. Angi **leveringsmåtekoden** med den tilsvarende leveringsmåten i [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Hvis det er knyttet flere leveringsgebyrer til en ordre, går du til salg, blir bare én valgt som leveringsmåten og tildelt salgsdokumentet.

### <a name="payment-method-mapping"></a>Tildeling av betalingsmåte

Hvis du vil fylle ut **betalingsmåtekoden** for salgsdokumenter som er importert fra Shopify automatisk, må du konfigurere **Tilordning av betalingsmåte**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikker** og velger den relaterte koblingen.
2. Velg butikken du vil definere tildeling for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Tildeling av betalingsmåte**.
4. Skriv inn navnet på betalingsmåten fra i feltene **Gateway** og **Kredittkortfirma** fra Shopify. Posten opprettes automatisk når du importerer Shopify-ordrer.
5. Angi **betalingsmåtekoden** med den tilsvarende betalingsmåten i [!INCLUDE[prod_short](../includes/prod_short.md)].
6. Angi **prioritet** for tilfeller der kunden bruker flere betalingsmåter. Betalingsmåten med høyest prioritet blir valgt i salgsdokumentet. Hvis begge betalingsmåtene har samme prioritet, brukes betalingsmåten med høyeste beløp.

### <a name="location-mapping"></a>Lokasjonstildeling

Hvis du vil fylle ut **lokasjonskoden** for salgsdokumenter som er importert fra Shopify automatisk, må du konfigurere **Shopify-butikklokasjoner**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikker** og velger den relaterte koblingen.
2. Velg butikken du vil konfigurere tildeling av lokasjoner for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Lokasjoner** for å åpne **Shopify-butikklokasjoner**.
4. Velg handlingen **Hent Shopify-lokasjoner** hvis du vil importere alle lokasjonene som er definert i Shopify. Du finner dem i innstillingene [**Lokasjoner**](https://www.shopify.com/admin/settings/locations) på **Shopify-administratorpanelet**. Merk at lokasjonen som er merket som *standard*, brukes ved import av ikke-oppfylte Shopify-ordrer.
5. Angi **standard lokasjonskode** med tilsvarende lokasjon i [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Du må konfigurere lokasjonstildelingen hvis veksleknapp **Lokasjon obligatorisk** er aktivert på kortet **Lageroppsett**, ellers kan du ikke opprette salgsdokumenter.

## <a name="run-the-order-synchronization"></a>Kjør ordresynkroniseringen

Fremgangsmåten nedenfor beskriver hvordan du importerer og oppdaterer ordrer.

> [!NOTE]  
> Arkiverte ordrer i Shopify kan ikke importeres. Deaktiver alternativet **Arkiver ordren automatisk** i delen **Ordrebehandling** i innstillingene **Betaling** i **Shopify-administratorpanelet** for å sørge for at alle ordrer importeres til [!INCLUDE[prod_short](../includes/prod_short.md)]. Hvis du må importere arkiverte ordrer, bruker du handlingen **Opphev arkivering av ordrer** på siden [Ordrer](https://www.shopify.com/admin/orders) i Shopify-administratorpanelet.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikker** og velger den relaterte koblingen.
2. Velg butikken du vil importere ordrer til for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Ordrer**.
4. Velg handlingen **Synkroniser ordrer fra Shopify**.
5. Definer filtre i ordrer etter behov. Du kan for eksempel importere fullt betalte ordrer eller de med lav risikograd.
6. Velg **OK**-knappen.

Du kan eventuelt søke etter den satsvise jobben **Synkroniser ordrer fra Shopify**.

Du kan planlegge at oppgaven skal utføres på en automatisk måte. Hvis du vil ha mer informasjon, kan du se [Planlegg gjentakende oppgaver](background.md#to-schedule-recurring-tasks).

## <a name="review-imported-orders"></a>Se gjennom importerte ordrer

Når importen er fullført, kan du utforske Shopify-ordren og finne all relatert informasjon. Finn for eksempel betalingstransaksjoner, leveringskostnader, risikonivå eller oppfyllelse hvis ordren allerede er oppfylt i Shopify. Du kan også se eventuell ordrebekreftelse som er sendt til kunden, ved å velge handlingen **Shopify-statusside**.

> [!NOTE]  
> Du kan navigere til vinduet **Shopify-ordre**, og du ser ordrer med statusen *åpen* fra alle butikker. Hvis du vil se på fullførte ordrer, må du åpne siden **Shopify-ordrer** fra det bestemte vinduet **Shopify-butikkort**.

## <a name="create-sales-documents-in-business-central"></a>Opprett salgsdokumenter i Business Central

Hvis veksleknappen **Opprett ordrer automatisk** er aktivert på **Shopify-butikkortet**, prøver [!INCLUDE[prod_short](../includes/prod_short.md)] å opprette et salgsdokument når ordren er importert. Hvis prosessen støter på problemer, for eksempel hvis en kunde eller et produkt mangler, må du løse problemet. Deretter kan du forsøke å opprette ordren på nytt.

### <a name="to-create-sales-documents"></a>Slik oppretter du salgsdokumenter

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikker** og velger den relaterte koblingen.
2. Velg butikken du vil synkronisere ordrer med for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Ordrer**.
4. Velg ordren du vil opprette et salgsdokument for, og velg handlingen **Opprett salgsdokumenter**.
5. Velg **Ja**.

Hvis Shopify-ordren krever oppfyllelse, opprettes en **ordre**. For oppfylte Shopify-ordrer, for eksempel ordrer som bare inneholder et gavekort, eller som allerede er håndtert i Shopify, blir det opprettet en **salgsfaktura**.

Et salgsdokument er nå opprettet og kan håndteres ved hjelp av standard [!INCLUDE[prod_short](../includes/prod_short.md)]-funksjoner.

### <a name="manage-missing-customers"></a>Administrer manglende kunder

Hvis innstillingene forhindrer at du oppretter en kunde automatisk og det ikke finnes en riktig eksisterende kunde, kan du angi at en kunde til Shopify-ordre manuelt. Det er et par alternativer:

- Du kan tildele feltet **Salg til-kundenr.** direkte i **Shopify-ordren** ved å velge en kunde fra oversikten over eksisterende kunder.
- Du kan velge en kundemalkode, opprette og tildele kunden via handlingen **Opprett ny kunde** på siden **Shopify-ordrer**.
- Du kan tildele en eksisterende kunde til den tilknyttede **Shopify-kunden** i vinduet **Shopify-kunder** og deretter velge handlingen **Søk etter tildeling** på siden **Shopify-ordrer**.

### <a name="tax-remarks"></a>Avgiftsmerknader

Når den importerte Shopify-ordren inneholder informasjon om avgifter, beregnes avgiftene på nytt når du oppretter salgsdokumentet. Omberegningen gjør det viktig at mva-/avgiftsinnstillingene er riktige i [!INCLUDE[prod_short](../includes/prod_short.md)].

- Flere produktavgifter/mva-satser. Noen produktkategorier er for eksempel ansvarlig for reduserte mva-satser. Disse varene må finnes i [!INCLUDE[prod_short](../includes/prod_short.md)] og tildeles til Shopify-produkter. Hvis ikke, med automatisk oppretting av manglende varer, brukes mva-bokføringsgruppen for produkt.

- Adresseavhengige mva-satser. Bruk feltet **Prioritet for avgiftsområde** sammen med tabellen **Kundemaler** til å overskrive standard logikk som fyller ut **mva-områdekoden** i salgsdokumentet. Feltet **Mva-områdekode** angir prioriteten der funksjonen skal hente informasjon om land/område og delstat/provins. Deretter finner du tilsvarende post i Shopify-kundemalene og **mva-områdekoden**, **skyldig mva.** og **mva.-bokføringsgruppe for firma** brukes når et salgsdokument opprettes.

- Priser inkludert avgift Feltet **Priser inkludert avgift**/**Priser inkludert mva.** i det opprettede salgsdokumentet er ikke avhengig av kunden, men av **kundemalen** fra Shopify-butikkortet eller kundemalen per land.

### <a name="impact-of-edits-of-orders"></a>Virkningen av redigeringer av ordrer

|Rediger|Innvirkning|
|------|-----------|
|I Shopify endrer du oppfyllingslokasjonen | Opprinnelig lokasjon blir synkronisert til [!INCLUDE[prod_short](../includes/prod_short.md)]. |
|I Shopify redigerer du en ordre og endrer antall| Ordrehodet og de supplerende tabellene blir oppdatert i [!INCLUDE[prod_short](../includes/prod_short.md)]. |
|I Shopify redigerer du en ordre og legger til en ny vare | Ordrehodet blir oppdatert, linjer blir ikke oppdatert |
|I [!INCLUDE[prod_short](../includes/prod_short.md)] endrer du lokasjonen til en annen lokasjon, tildelt Shopify-lokasjonene. Bokfør levering. | Etter at du har synkronisert oppfyllelsen, oppdateres lokasjonen i Shopify. |
|I [!INCLUDE[prod_short](../includes/prod_short.md)] endrer du lokasjonen til en annen lokasjon, ikke tildelt Shopify-lokasjonene. Bokfør levering. | Oppfyllelsen synkroniseres ikke til Shopify. |
|I [!INCLUDE[prod_short](../includes/prod_short.md)] endrer du reduksjonsantall. Bokfør levering. | Shopify-ordren blir merket som delvis fullført. |
|I [!INCLUDE[prod_short](../includes/prod_short.md)] legger du til en ny vare. Bokfør levering. | Shopify-ordren blir merket som fullført. Linjene blir ikke oppdatert. |

## <a name="synchronize-shipments-to-shopify"></a>Synkroniser leveringer til Shopify

Når en ordre som opprettes fra en Shopify-ordre, leveres, kan du synkronisere leveringene med Shopify.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Synkroniser leveringer til Shopify**, og velg deretter den relaterte koblingen.
2. Definer filtrene på leveringer etter behov. Du kan for eksempel oppdatere en levering bokført på en bestemt dato.
3. Velg **OK**-knappen.

Ordren i Shopify blir merket som fullført. Kunden får automatisk en leveringsvarsels-e-post eller en tekstmelding (SMS). Hvis en transportør og en sporingskode er angitt i leveringen, inkluderes sporingsinformasjonen i e-posten.

> [!NOTE]  
> Husk å kjøre **Synkroniser ordrer fra Shopify** for å oppdatere oppfyllingsstatusen for ordre i [!INCLUDE[prod_short](../includes/prod_short.md)]. Koblingsfunksjonen arkiverer også fullstendig betalte og oppfylte ordrer i både Shopify og i [!INCLUDE[prod_short](../includes/prod_short.md)] gitt at betingelsene er oppfylt.

### <a name="shipping-agents-and-tracking-url"></a>Transportører og sporingsnettadresse

Hvis dokumentet **Bokført følgeseddel** inneholder **Transportørkode** eller **Pakkesporingsnummer**, blir denne informasjonen sendt til Shopify og til sluttkunden i e-posten for leveringsbekreftelse.

Sporingsfirmaet fylles ut basert på transportørposten med følgende prioriteter (fra høyest til lavest):

- **Shopify-sporingsselskap**
- **Navn**
- **Kode**

Hvis feltet for **pakkesporingsnettadresse** fylles ut for transportørposten, inneholder leveringsbekreftelse også en sporingsnettadresse.

## <a name="gift-cards"></a>Gavekort

I Shopify-butikken kan du selge gavekort, som senere kan brukes til å betale for virkelige produkter.

Når du håndterer gavekort, er det viktig å angi en verdi i feltet **Solgt gavekortkonto** i vinduet **Shopify-butikkort**. Det solgte gavekortet blir synkronisert sammen med ordrer på linje. Et brukt gavekort blir også importert sammen med ordren, men nå som en transaksjon. Legg merke til at gavekortet ikke reduserer beløpet som skal faktureres.

Hvis du vil gå gjennom utstedte og brukte gavekort, velger du ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Gavekort**, og velg deretter den relaterte koblingen.

## <a name="transactions"></a>Transaksjoner

Betalingstransaksjonene som fant sted i Shopify, synkroniseres sammen med ordrene, og kan ses fra siden *Shopify-ordrer*.

Hvis du vil se gjennom alle transaksjoner, velger du ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Transaksjoner**. Velg den relaterte koblingen.

## <a name="payouts"></a>Utbetalinger

Hvis butikken har Shopify Payments aktivert, mottar du betalinger gjennom *Shopify-utbetalinger* når en kunde betaler ved hjelp av Shopify Payments og raskere betalinger.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikker** og velger den relaterte koblingen.
2. Velg butikken du vil synkronisere utbetalinger med for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Synkroniser utbetalinger**.

Hvis du vil se gjennom alle utbetalinger, velger du ikon ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Utbetalinger**. Velg den relaterte koblingen.

## <a name="see-also"></a>Se også

[Kom i gang med koblingen for Shopify](get-started.md)  
