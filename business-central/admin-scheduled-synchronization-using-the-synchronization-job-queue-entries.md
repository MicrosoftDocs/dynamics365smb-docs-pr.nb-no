---
title: Synkronisere Business Central og Dataverse
description: Lære om å synkronisere data mellom Business Central og Dataverse.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'sales, crm, integration, sync, synchronize'
---

# <a name="scheduling-a-synchronization-between-business-central-and-dataverse"></a>Planlegge en synkronisering mellom Business Central og Dataverse

Du kan synkronisere [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE[cds_long_md](includes/cds_long_md.md)] på planlagte intervaller ved å definere jobber i jobbkøen. Synkroniseringsjobbene synkroniserer data i [!INCLUDE[prod_short](includes/prod_short.md)]-poster og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-poster som er koblet. For poster som ikke allerede er koblet, avhengig av synkroniseringsretningen og regler, kan synkroniseringsjobbene opprette og koble nye poster i målsystemet.

Det finnes flere synkroniseringsjobber som er tilgjengelige som standard. Jobbene kjøres i denne rekkefølgen for å unngå å koble avhengigheter mellom tabeller. Hvis du vil ha mer informasjon, kan du se [Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).

1. CURRENCY – Common Data Service-synkroniseringsjobb.
2. VENDOR – Common Data Service-synkroniseringsjobb.
3. CONTACT – Common Data Service-synkroniseringsjobb.
4. CUSTOMER – Common Data Service-synkroniseringsjobb.
5. SALESPEOPLE – Common Data Service-synkroniseringsjobb.

Du kan vise jobbene på siden **Poster i jobbkø**. Hvis du vil ha mer informasjon, kan du se [Bruk jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).

## <a name="default-synchronization-job-queue-entries"></a>Jobbkøposter for standard synkronisering

Tabellen nedenfor beskriver standard synkroniseringsjobber for [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  

| Jobbkøpost | Beskrivelse | Retning | Tilordning for integreringstabell | Standard synkroniseringsfrekvens (minutter) | Standard hvilemodustid for inaktivitet (minutter) |
|--|--|--|--|--|--|--|
| CONTACT – Common Data Service-synkroniseringsjobb | Synkroniserer [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-kontakter med [!INCLUDE[prod_short](includes/prod_short.md)]-kontakter. | Toveis | CONTACT | 30 | 720 <br>(12 timer) |
| CURRENCY – Common Data Service-synkroniseringsjobb | Synkroniserer [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-transaksjonsvalutaer med [!INCLUDE[prod_short](includes/prod_short.md)]-valutaer. | Fra [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] | CURRENCY | 30 | 720 <br> (12 timer) |
| CUSTOMER – Common Data Service-synkroniseringsjobb | Synkroniserer [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-kontoer med [!INCLUDE[prod_short](includes/prod_short.md)]-kunder. | Toveis | CUSTOMER | 30 | 720<br> (12 timer) |
| VENDOR – Common Data Service-synkroniseringsjobb | Synkroniserer [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-kontoer med [!INCLUDE[prod_short](includes/prod_short.md)]-kunder. | Toveis | VENDOR | 30 | 720<br> (12 timer) |
| SALESPEOPLE – Common Data Service-synkroniseringsjobb | Synkroniserer [!INCLUDE[prod_short](includes/prod_short.md)]-selgere med [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-brukere. | Fra [!INCLUDE[cds_long_md](includes/cds_long_md.md)] til [!INCLUDE[prod_short](includes/prod_short.md)] | SELGERE | 30 | 1440<br> (24 timer) |

## <a name="synchronization-process"></a>Synkroniseringsprosess

Hver jobbkøpost for synkronisering bruker en bestemt integrasjonstabelltilordning som angir hvilken [!INCLUDE[prod_short](includes/prod_short.md)]-tabell og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-tabell som skal synkroniseres. Tabelltilordningene inneholder også enkelte innstillinger som bestemmer hvilke poster i [!INCLUDE[prod_short](includes/prod_short.md)]-tabellen og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-tabellen som skal synkroniseres.  

For å kunne synkronisere data må [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-tabellpostene være koblet til [!INCLUDE[prod_short](includes/prod_short.md)]-poster. For eksempel må en [!INCLUDE[prod_short](includes/prod_short.md)]-kunde være koblet til en [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-konto. Du kan konfigurere koblinger manuelt før du kjører synkroniseringsjobber eller la synkroniseringsjobbene sette opp koblinger automatisk. Følgende liste beskriver hvordan dataene blir synkronisert mellom [!INCLUDE[cds_long_md](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)] når du bruker jobbkøposter for synkronisering. Hvis du vil ha mer informasjon, se [Sammenkoble og synkronisere poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md).

- Avmerkingsboksen **Synkroniser bare koblede poster** kontrollerer om det opprettes nye poster når du synkroniserer. Som standard er det merket av for dette alternativet, som betyr at bare poster som er kombinert, vil bli synkronisert. I integrasjonstabelltilordning kan du endre tabelltilordningen mellom en [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-tabell og en [!INCLUDE[prod_short](includes/prod_short.md)]-tabell, slik at integrasjonssynkroniseringsjobbene oppretter nye poster i måldatabasen for hver rad i kildedatabasen som ikke er koblet. Hvis du vil ha mer informasjon, kan du se [Opprette nye poster](admin-how-to-modify-table-mappings-for-synchronization.md#create-new-records).

    **Eksempel** Hvis du fjerner merket for **Synkroniser bare koblede poster** når du synkroniserer kunder i [!INCLUDE[prod_short](includes/prod_short.md)] med kontoer i [!INCLUDE[cds_long_md](includes/cds_long_md.md)], opprettes det en ny konto for hver kunde i [!INCLUDE[prod_short](includes/prod_short.md)], og kobling opprettes automatisk. I tillegg, fordi synkronisering i dette tilfellet er toveis, opprettes og kobles en ny kunde for hver [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-konto som ikke allerede er koblet.  

    > [!NOTE]  
    > Det finnes regler og filtre som bestemmer hvilke data som synkroniseres. Hvis du vil ha mer informasjon, kan du gå til [Synkroniseringsregler](admin-synchronizing-business-central-and-sales.md).

- Når nye poster opprettes i [!INCLUDE[prod_short](includes/prod_short.md)], bruker postene enten malen som er definert for integrasjonstabelltilordningen, eller standardmalen som er tilgjengelig for radtypen. Felt fylles ut med data fra [!INCLUDE[prod_short](includes/prod_short.md)] eller [!INCLUDE[cds_long_md](includes/cds_long_md.md)], avhengig av synkroniseringsretningen. Hvis du vil ha mer informasjon, se [Endre tabelltilordningene for synkronisering](admin-how-to-modify-table-mappings-for-synchronization.md).  

- Med etterfølgende synkroniseringer oppdateres bare poster som er endret eller lagt til etter den siste vellykkede synkroniseringsjobben, for tabellen.  

     Nye poster i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] legges til i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis data i feltene i [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-postene er endret, blir dataene kopiert til det tilsvarende feltet i [!INCLUDE[prod_short](includes/prod_short.md)].  

- Med toveis synkronisering synkroniseres jobben fra [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] og deretter fra [!INCLUDE[cds_long_md](includes/cds_long_md.md)] til [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="about-inactivity-timeouts"></a>Om tidsavbrudd for inaktivitet

Noen jobbkøoppføringer, for eksempel de som planlegger synkronisering mellom [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)], bruker feltet **Tidsavbrudd for inaktivitet** på siden for jobbkøpost for å hindre at jobbkøen kjøres unødig.  

:::image type="content" source="media/on-hold-with-inactivity-timeout.png" alt-text="Flytskjema for når jobbkøoppføringer settes på vent på grunn av uvirksomhet.":::

Når verdien i dette feltet ikke er null, og jobbkøen ikke fant noen endringer under siste kjøring, setter [!INCLUDE[prod_short](includes/prod_short.md)] jobbkøoppføringen på vent. Når dette skjer, viser **Status for jobbkø**-feltet **Avvent på grunn av inaktivitet**, og [!INCLUDE[prod_short](includes/prod_short.md)] venter på tidsrommet som er angitt i feltet **Tidsavbrudd for inaktivitet** før jobbkøoppføringen kjøres på nytt.  

Som standard vil for eksempel CURRENCY-jobbkøoppføringen, som synkroniserer valutaer i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] med valutakurser i [!INCLUDE[prod_short](includes/prod_short.md)], se etter endringer i valutakursene hvert 30. minutt. Hvis ingen endringer blir funnet, setter [!INCLUDE[prod_short](includes/prod_short.md)] CURRENCY-jobbkøoppføringen på vent i 720 minutter (tolv timer). Hvis en valutakurs endres i [!INCLUDE[prod_short](includes/prod_short.md)] mens jobbkøoppføringen er på vent, vil [!INCLUDE[prod_short](includes/prod_short.md)] automatisk aktivere jobbkøoppføringen og starte jobbkøen på nytt. 

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] vil automatisk bare aktivere jobbkøoppføringer som er satt på vent, når endringer forekommer i [!INCLUDE[prod_short](includes/prod_short.md)]. Endringer i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] vil ikke aktivere jobbkøoppføringer.

## <a name="to-view-the-synchronization-job-log"></a>Slik viser du synkroniseringsjobbloggen

1. Velg ikonet :::image type="icon" source="media/ui-search/search_small.png" border="false":::, angi **Integrasjonssynkroniseringslogg**, og velg deretter den relaterte koblingen.
2. Hvis én eller flere feil oppstod for en synkroniseringsjobb, vises antall feil i **Mislyktes**-kolonnen. Hvis du vil vise feil for prosjektet, kan du velge nummeret.  

    > [!TIP]  
    > Du kan vise alle synkroniseringsjobbfeil ved å åpne loggen for synkroniseringsjobbfeil direkte.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>Slik viser du synkroniseringsjobbloggen fra tabelltilordningene

1. Velg ikonet :::image type="icon" source="media/ui-search/search_small.png" border="false":::, angi **Tilordninger for integreringstabell**, og velg deretter den relaterte koblingen.
2. På siden **Tilordninger for integreringstabell** velger du en post, og velg deretter **Logg for synkroniseringsjobb for integrering**.  

## <a name="to-view-the-synchronization-error-log"></a>Slik viser du synkroniseringsfeilloggen

- Velg ikonet :::image type="icon" source="media/ui-search/search_small.png" border="false":::, angi **Synkroniseringsfeil ved integrasjon**, og velg deretter den relaterte koblingen.

## <a name="see-also"></a>Se også

[Synkronisere data i Business Central og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Synkronisere tabelltilordninger manuelt](admin-manual-synchronization-of-table-mappings.md)  
[Planlegge en synkronisering mellom Business Central og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Om integrering av Dynamics 365 Business Central med [!INCLUDE[cds_long_md](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
