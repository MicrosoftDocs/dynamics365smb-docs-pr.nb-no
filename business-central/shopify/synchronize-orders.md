---
title: Synkroniser og oppfyll salgsordrer
description: Definer og kjør import og behandling av salgsordre fra Shopify.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 30110, 30111, 30112, 30113, 30114, 30115, 30121, 30122, 30123, 30128, 30129,
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 70c401e072e742e508b8f623ae3242d8e647ccb6
ms.sourcegitcommit: bb6ecb20cbd82fdb5235e3cb426fc73c29c0a7ae
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802934"
---
# <a name="synchronize-and-fulfill-sales-orders"></a>Synkroniser og oppfyll salgsordrer

Denne artikkelen beskriver de nødvendige innstillingene og trinnene du må fullføre for å synkronisere og oppfylle salgsordrer med Shopify i [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="set-the-import-of-orders-on-the-shopify-shop-card"></a>Angi importen av ordrer på Shopify-butikkortet

Angi en **valutakode** hvis nettbutikken bruker en annen valuta enn lokal valuta (LV). Den angitte valutaen må ha valutakurser konfigurert. Hvis nettbutikken bruker samme valuta som [!INCLUDE[prod_short](../includes/prod_short.md)], lar du feltet stå tomt. 

Du kan se butikkvaluta i innstillingene for [butikkdetaljer](https://www.shopify.com/admin/settings/general) i Shopify-administratoren. Shopify kan konfigureres til å godta forskjellige valutaer, men importerte ordrer til [!INCLUDE[prod_short](../includes/prod_short.md)] bruker butikkvaluta.

En vanlig Shopify-ordre kan omfatte kostnader i tillegg til delsummen, for eksempel leveringskostnader eller tips hvis aktivert. Disse beløpene bokføres direkte på finanskontoen du vil bruke for bestemte transaksjonstyper:

* **Leveringskostnadskonto**
* **Solgt gavekortkonto**: finn ut mer under [Gavekort](synchronize-orders.md#gift-cards)
* **Tipskonto**  

Aktiver **Opprett ordrer automatisk** for å opprette salgsdokumenter automatisk i [!INCLUDE[prod_short](../includes/prod_short.md)] når Shopify-ordren importeres.

Salgsdokumentet i [!INCLUDE[prod_short](../includes/prod_short.md)] inneholder en kobling til Shopify-ordren. Hvis du velger feltet **Shopify-ordrenr. på dok.linje**, gjentas denne informasjonen på salgslinjene av typen *Merknad*.

I feltet **Mva-områdekode** kan du angi prioriteten for hvordan du velger mva-områdekode eller mva-bokføringsgruppe for firma basert på adresse. Den importerte Shopify-ordren inneholder informasjon om avgifter, men avgiftene blir beregnet på nytt når du oppretter salgsdokumentet, slik at det er viktig at mva.-/avgiftsinnstillingene er riktige i [!INCLUDE[prod_short](../includes/prod_short.md)]. Hvis du vil ha mer informasjon om avgifter, kan du se [Definer avgifter for Shopify-koblingen](setup-taxes.md).

### <a name="shipment-method-mapping"></a>Tildeling av leveringsmåte

**Kode for leveringsmåte** for salgsdokumenter som er importert fra Shopify, kan fylles ut automatisk. Du må konfigurere **Tildeling av leveringsmåte**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikker** og velger den relaterte koblingen.
2. Velg butikken du vil definere tildeling for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Tildeling av leveringsmåte**. Dette oppretter automatisk postene for leveringsmåter som er definert i [**Levering**](https://www.shopify.com/admin/settings/payments)-innstillingene i **Shopify-administrator**.
4. I **Navn**-feltet kan du se navnet på leveringsmåten fra Shopify.
5. Angi **leveringsmåtekoden** med den tilsvarende leveringsmåten i [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Hvis det er knyttet flere leveringsgebyrer til en ordre, går du til salg, blir bare én valgt som leveringsmåten og tildelt salgsdokumentet.

### <a name="location-mapping"></a>Lokasjonstildeling

Plasseringstildelingen er nødvendig for tre formål:

* For å synkronisere lager. Hvis du vil ha mer informasjon, kan du se [Synkroniser lager til Shopify](synchronize-items.md#sync-inventory-to-shopify)
* For å fylle inn **lokasjonskoden** for salgsdokumenter som er importert fra Shopify. Dette er viktig når veksleknappen **Lokasjon obligatorisk** er aktivert på kortet **Lageroppsett**, ellers kan du ikke opprette salgsdokumenter.
* For å oppdatere Shopify-ordren med oppfyllelsesinformasjonen basert på siden **Bokført følgeseddel**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikker** og velger den relaterte koblingen.
2. Velg butikken du vil konfigurere tildeling av lokasjoner for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Lokasjoner** for å åpne **Shopify-butikklokasjoner**.
4. Velg handlingen **Hent Shopify-lokasjoner** hvis du vil importere alle lokasjonene som er definert i Shopify. Du finner dem i innstillingene [**Lokasjoner**](https://www.shopify.com/admin/settings/locations) på **Shopify-administratorpanelet**. Merk at lokasjonen som er merket som *standard*, brukes ved import av ikke-oppfylte Shopify-ordrer.
5. Angi **standard lokasjonskode** med tilsvarende lokasjon i [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="run-the-order-synchronization"></a>Kjør ordresynkroniseringen

Fremgangsmåten nedenfor beskriver hvordan du importerer og oppdaterer ordrer.

> [!NOTE]  
> Arkiverte ordrer i Shopify kan ikke importeres. Deaktiver alternativet **Arkiver ordren automatisk** i delen **Ordrebehandling** i innstillingene **Betaling** i **Shopify-administratorpanelet** for å sørge for at alle ordrer importeres til [!INCLUDE[prod_short](../includes/prod_short.md)]. Hvis du må importere arkiverte ordrer, bruker du handlingen **Opphev arkivering av ordrer** på siden [Ordrer](https://www.shopify.com/admin/orders) i **Shopify-administratorpanelet**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikker** og velger den relaterte koblingen.
2. Velg butikken du vil importere ordrer til for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Ordrer**.
4. Velg handlingen **Synkroniser ordrer fra Shopify**.
5. Definer filtre i ordrer etter behov. Du kan for eksempel importere fullt betalte ordrer eller de med lav risikograd.
6. Velg **OK**-knappen.

Du kan eventuelt søke etter den satsvise jobben **Synkroniser ordrer fra Shopify**.

Du kan planlegge at oppgaven skal utføres på en automatisk måte. Finn ut mer under [Planlegg gjentakende oppgaver](background.md#to-schedule-recurring-tasks).

## <a name="review-imported-orders"></a>Se gjennom importerte ordrer

Når importen er fullført, kan du utforske Shopify-ordren og finne all relatert informasjon, for eksempel betalingstransaksjonene, leveringskostnadene, risikonivået, ordreattributtene og merkene eller oppfyllelsene, hvis ordren allerede var oppfylt i Shopify. Du kan også se eventuell ordrebekreftelse som er sendt til kunden, ved å velge handlingen **Shopify-statusside**.

> [!NOTE]  
> Du kan navigere til vinduet **Shopify-ordre**, og du ser ordrer med statusen *åpen* fra alle butikker. Hvis du vil se på fullførte ordrer, må du åpne siden **Shopify-ordrer** fra det bestemte vinduet **Shopify-butikkort**.

## <a name="create-sales-documents-in-business-central"></a>Opprett salgsdokumenter i Business Central

Hvis veksleknappen **Opprett ordrer automatisk** er aktivert på **Shopify-butikkortet**, prøver [!INCLUDE[prod_short](../includes/prod_short.md)] å opprette et salgsdokument når ordren er importert. Hvis problemer som manglede kunde eller produkt oppstår, må du løse problemene og opprette salgsordren på nytt.

### <a name="to-create-sales-documents"></a>Slik oppretter du salgsdokumenter

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikker** og velger den relaterte koblingen.
2. Velg butikken du vil synkronisere ordrer med for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Ordrer**.
4. Velg ordren du vil opprette et salgsdokument for, og velg handlingen **Opprett salgsdokumenter**.
5. Velg **Ja**.

Hvis Shopify-ordren krever oppfyllelse, opprettes en **ordre**. For oppfylte Shopify-ordrer, for eksempel ordrer som bare inneholder et gavekort, eller som allerede er håndtert i Shopify, blir det opprettet en **salgsfaktura**.

Et salgsdokument er nå opprettet og kan håndteres ved hjelp av standard [!INCLUDE[prod_short](../includes/prod_short.md)]-funksjoner.

### <a name="manage-missing-customers"></a>Administrer manglende kunder

Hvis innstillingene forhindrer at du oppretter en kunde automatisk og det ikke finnes en riktig eksisterende kunde, må du angi at en kunde til Shopify-ordren manuelt. Det er noen få måter å gjøre dette på:

* Du kan tildele feltet **Salg til-kundenr.** og **Faktura til-kundenr.** direkte på siden **Shopify-ordrer** ved å velge en kunde fra oversikten over eksisterende kunder.
* Du kan velge en kundemalkode, opprette og tildele kunden via handlingen **Opprett ny kunde** på siden **Shopify-ordrer**.
* Du kan tildele en eksisterende kunde til den tilknyttede **Shopify-kunden** i vinduet **Shopify-kunder** og deretter velge handlingen **Søk etter tildeling** på siden **Shopify-ordrer**.

### <a name="how-the-connector-chooses-which-customer-to-use"></a>Slik velger koblingen hvilken kunde som skal brukes

*Import ordre fra Shopify*-funksjonen prøver å velge kunder i følgende rekkefølge:

1. Hvis **Standard kundenr.** feltet er definert i **Shopify-kundemalen** for det tilsvarende landet, brukes deretter **Standard kundenr.** uavhengig av innstillingene i feltene **Kundeimport fra Shopify** og **Kundetildeling**. Finn ut mer under [Kundemal per land](synchronize-customers.md#customer-template-per-country).
2. Hvis **Kundeimport fra Shopify** er angitt til *Ingen* og **Standard kundenr.** er definert på siden **Shopify-butikkort**, brukes **Standard kundenr.** .

Neste trinn avhenger av **Kundetildelingstype**.

* Hvis det er **Ta alltid standardkunden**, bruker tilkoblingen deretter kunden som er definert i feltet **Standard kundenr.** på siden **Shopify-butikkort**.
* Hvis det er **Via e-post/telefon**, prøver koblingen å finne eksisterende kunde med ID først, deretter med e-post og så med telefonnummer. Hvis kunden ikke blir funnet, oppretter koblingen en ny kunde.
* Hvis det er **Etter faktura til-informasjon**, prøver koblingen å finne eksisterende kunde med ID først og deretter etter faktura til-adresseinformasjon. Hvis kunden ikke blir funnet, oppretter koblingen en ny kunde.

> [!NOTE]  
> Koblingen bruker opplysninger fra faktura til-adresse og oppretter faktura til-kunde i [!INCLUDE[prod_short](../includes/prod_short.md)]. Salg til-kunden er den samme som faktura til-kunden.

### <a name="impact-of-order-editing"></a>Virkningen av ordreredigering

I Shopify:

|Rediger|Innvirkning|
|------|-----------|
|Endre oppfyllingslokasjonen | Opprinnelig lokasjon blir synkronisert til [!INCLUDE[prod_short](../includes/prod_short.md)]. |
|Endre oppfyllingslokasjonen og registrer oppfyllelse i Shopify| Hvis ordren allerede er importert, oppdateres ikke linjene. Ellers vil den importerte ordren bruke oppfyllingslokasjonen. |
|Rediger en ordre og endre antall| Ordrehodet og de supplerende tabellene blir oppdatert i [!INCLUDE[prod_short](../includes/prod_short.md)]. |
|Rediger en ordre og legg til en ny vare | Ordrehodet blir oppdatert, linjer blir ikke oppdatert |

I [!INCLUDE[prod_short](../includes/prod_short.md)]:

|Rediger|Innvirkning|
|------|-----------|
|Endre lokasjonen til en annen lokasjon, tildelt Shopify-lokasjonene. Bokfør levering. | Etter at du har synkronisert oppfyllelsen, oppdateres lokasjonen i Shopify. |
|Endre lokasjonen til en annen lokasjon, ikke tildelt Shopify-lokasjonene. Bokfør levering. | Oppfyllelsen synkroniseres ikke med Shopify. |
|Endre reduksjonsantall. Bokfør levering. | Shopify-ordren blir merket som delvis fullført. |
|Legg til en ny vare. Bokfør levering. | Shopify-ordren blir merket som fullført. Linjene blir ikke oppdatert. |

## <a name="synchronize-shipments-to-shopify"></a>Synkroniser leveringer til Shopify

Når en ordre som opprettes fra en Shopify-ordre, leveres, kan du synkronisere leveringene med Shopify.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Synkroniser leveringer til Shopify**, og velg deretter den relaterte koblingen.
2. Definer filtrene på leveringer etter behov. Du kan for eksempel oppdatere en levering bokført på en bestemt dato.
3. Velg **OK**-knappen.

Ordren i Shopify blir merket som fullført. Kunden får automatisk en leveringsvarsels-e-post eller en tekstmelding (SMS). Hvis en transportør og en sporingskode er angitt i leveringen, inkluderes sporingsinformasjonen i e-posten.

Du kan også bruke handlingen **Synkroniser forsendelser** på sidene Shopify-ordrer eller Shopify-butikk.

Du kan planlegge at oppgaven skal utføres på en automatisk måte. Finn ut mer under [Planlegg gjentakende oppgaver](background.md#to-schedule-recurring-tasks).

>[Viktig] Lokasjonen, inkludert tom lokasjon, definert i den bokførte følgeseddellinjen må ha en samsvarende post på Shopify-lokasjonen. Hvis ikke sendes ikke denne linjen tilbake til Shopify. Finn ut mer på [Lokasjonstildeling](synchronize-orders.md#location-mapping).

Husk å kjøre **Synkroniser ordrer fra Shopify** for å oppdatere oppfyllingsstatusen for en ordre i [!INCLUDE[prod_short](../includes/prod_short.md)]. Koblingsfunksjonen arkiverer også fullstendig betalte og oppfylte ordrer i både Shopify og [!INCLUDE[prod_short](../includes/prod_short.md)] gitt at betingelsene er oppfylt.

### <a name="shipping-agents-and-tracking-url"></a>Transportører og sporingsnettadresse

Hvis dokumentet **Bokført følgeseddel** inneholder **Transportørkode** eller **Pakkesporingsnummer**, blir denne informasjonen sendt til Shopify og til kunden i e-posten for leveringsbekreftelse.

Sporingsfirmaet fylles ut i følgende rekkefølge (fra høyest til lavest) basert på transportørposten:

* **Shopify-sporingsselskap**
* **Navn**
* **Kode**

Hvis feltet for **pakkesporingsnettadresse** fylles ut for transportørposten, inneholder leveringsbekreftelse også en sporingsnettadresse.

## <a name="gift-cards"></a>Gavekort

I Shopify-butikken kan du selge gavekort, som kan brukes til å betale for virkelige produkter.

Når du håndterer gavekort, er det viktig å angi en verdi i feltet **Solgt gavekortkonto** i vinduet **Shopify-butikkort**. Det solgte gavekortet blir synkronisert sammen med ordrer på linje. Et brukt gavekort blir også importert sammen med ordren, men nå som en transaksjon. Legg merke til at gavekortet ikke reduserer beløpet som skal faktureres.

Hvis du vil gå gjennom utstedte og brukte gavekort, velger du ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Gavekort**, og velg deretter den relaterte koblingen.

## <a name="see-also"></a>Se også

[Kom i gang med koblingen for Shopify](get-started.md)  
