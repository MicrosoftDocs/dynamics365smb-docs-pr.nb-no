---
title: Synkronisere Business Central og Common Data Service | Microsoft Docs
description: Lære om å synkronisere data mellom Business Central og Common Data Service.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: cce95930cde316c5e233382effb0bb241b3b79fd
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196594"
---
# <a name="scheduling-a-synchronization-between-business-central-and-common-data-service"></a>Planlegge en synkronisering mellom Business Central og Common Data Service
Du kan synkronisere [!INCLUDE[d365fin](includes/d365fin_md.md)] med [!INCLUDE[d365fin](includes/cds_long_md.md)] på planlagte intervaller ved å definere jobber i jobbkøen. Synkroniseringsjobbene synkroniserer data i [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster og [!INCLUDE[d365fin](includes/cds_long_md.md)]-poster som har blitt koblet sammen tidligere. Eller for poster som ikke allerede er koblet, avhengig av synkroniseringsretningen og regler, kan synkroniseringsjobbene opprette og koble nye poster i målsystemet. 

Det finnes flere synkroniseringsjobber som er tilgjengelige som standard. Jobbene kjøres i denne rekkefølgen for å unngå å koble avhengigheter mellom enheter. Hvis du vil ha mer informasjon, kan du se [Bruke jobbkøer til å planlegge oppgaver](/dynamics365/business-central/admin-job-queues-schedule-tasks.md).

1. CURRENCY – [!INCLUDE[d365fin](includes/cds_long_md.md)]-synkroniseringsjobb.
2. VENDOR – [!INCLUDE[d365fin](includes/cds_long_md.md)]-synkroniseringsjobb. 
3. CONTACT – [!INCLUDE[d365fin](includes/cds_long_md.md)]-synkroniseringsjobb.
4. CUSTOMER – [!INCLUDE[d365fin](includes/cds_long_md.md)]-synkroniseringsjobb.
5. SALESPEOPLE – [!INCLUDE[d365fin](includes/cds_long_md.md)]-synkroniseringsjobb.

Du kan vise jobbene på siden **Poster i jobbkø**. Hvis du vil ha mer informasjon, kan du se [Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).

### <a name="default-synchronization-job-queue-entries"></a>Jobbkøposter for standard synkronisering  
Tabellen nedenfor beskriver standard synkroniseringsjobber for [!INCLUDE[d365fin](includes/cds_long_md.md)].  

|Jobbkøpost|Beskrivelse|Retning|Tilordning for integreringstabell|Standard synkroniseringsfrekvens (minutter)|Standard hvilemodustid for inaktivitet (minutter)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|CONTACT – [!INCLUDE[d365fin](includes/cds_long_md.md)]-synkroniseringsjobb|Synkroniserer [!INCLUDE[d365fin](includes/cds_long_md.md)]-kontakter med [!INCLUDE[d365fin](includes/d365fin_md.md)]-kontakter.|Toveis|CONTACT|30|720 <br>(12 timer)| 
|CURRENCY – [!INCLUDE[d365fin](includes/cds_long_md.md)]-synkroniseringsjobb|Synkroniserer [!INCLUDE[d365fin](includes/cds_long_md.md)]-transaksjonsvalutaer med [!INCLUDE[d365fin](includes/d365fin_md.md)]-valutaer.|Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[d365fin](includes/cds_long_md.md)]|CURRENCY|30|720 <br> (12 timer)| 
|CUSTOMER – [!INCLUDE[d365fin](includes/cds_long_md.md)]-synkroniseringsjobb|Synkroniserer [!INCLUDE[d365fin](includes/cds_long_md.md)]-kontoer med [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder.|Toveis|CUSTOMER|30|720<br> (12 timer)|
|VENDOR – [!INCLUDE[d365fin](includes/cds_long_md.md)]-synkroniseringsjobb|Synkroniserer [!INCLUDE[d365fin](includes/cds_long_md.md)]-kontoer med [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder.|Toveis|VENDOR|30|720<br> (12 timer)|
|SALESPEOPLE – [!INCLUDE[d365fin](includes/cds_long_md.md)]-synkroniseringsjobb|Synkroniserer [!INCLUDE[d365fin](includes/d365fin_md.md)]-selgere med [!INCLUDE[d365fin](includes/cds_long_md.md)]-brukere.|Fra [!INCLUDE[d365fin](includes/cds_long_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)]|SELGERE|30|1440<br> (24 timer)|

## <a name="synchronization-process"></a>Synkroniseringsprosess  
Hver jobbkøpost for synkronisering bruker en bestemt integrasjonstabelltilordning som angir hvilken [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell og [!INCLUDE[d365fin](includes/cds_long_md.md)]-enhet som skal synkroniseres. Tabelltilordningene inneholder også enkelte innstillinger som bestemmer hvilke poster i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen og [!INCLUDE[d365fin](includes/cds_long_md.md)]-enheten som skal synkroniseres.  

For å kunne synkronisere data må [!INCLUDE[d365fin](includes/cds_long_md.md)]-enhetspostene være koblet til [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster. For eksempel må en [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunde være koblet til en [!INCLUDE[d365fin](includes/cds_long_md.md)]-konto. Du kan konfigurere koblinger manuelt før du kjører synkroniseringsjobber eller la synkroniseringsjobbene sette opp koblinger automatisk. Følgende liste beskriver hvordan dataene blir synkronisert mellom Common Data Service og [!INCLUDE[d365fin](includes/d365fin_md.md)] når du bruker jobbkøposter for synkronisering. Hvis du vil ha mer informasjon, se [Sammenkoble og synkronisere poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md).

-   Avmerkingsboksen **Synkroniser bare koblede poster** kontrollerer om det opprettes nye poster når du synkroniserer. Som standard er det merket av for dette alternativet, som betyr at bare poster som er kombinert, vil bli synkronisert. I integrasjonstabelltilordning kan du endre tabelltilordningen mellom en [!INCLUDE[d365fin](includes/cds_long_md.md)]-enhet og en [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell, slik at integrasjonssynkroniseringsjobbene oppretter nye poster i måldatabasen for hver post i kildedatabasen som ikke er koblet. Hvis du vil ha mer informasjon, kan du se [Opprette nye poster](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records). 
    
    **Eksempel** Hvis du fjerner merket for **Synkroniser bare koblede poster** når du synkroniserer kunder i [!INCLUDE[d365fin](includes/d365fin_md.md)] med kontoer i [!INCLUDE[d365fin](includes/cds_long_md.md)], opprettes det en ny konto for hver kunde i [!INCLUDE[d365fin](includes/d365fin_md.md)], og kobling opprettes automatisk. I tillegg, fordi synkronisering i dette tilfellet er toveis, opprettes og kobles en ny kunde for hver [!INCLUDE[d365fin](includes/cds_long_md.md)]-konto som ikke allerede er koblet.  

    > [!NOTE]  
    > Det finnes regler og filtre som bestemmer hvilke data som synkroniseres. Hvis du vil ha mer informasjon, kan du se [Synkroniseringsregler](admin-synchronizing-business-central-and-sales.md).

-   Når nye poster opprettes i [!INCLUDE[d365fin](includes/d365fin_md.md)], bruker postene enten malen som er definert for integrasjonstabelltilordningen, eller standardmalen som er tilgjengelig for posttypen. Felt fylles ut med data fra [!INCLUDE[d365fin](includes/d365fin_md.md)] eller [!INCLUDE[d365fin](includes/cds_long_md.md)], avhengig av synkroniseringsretningen. Hvis du vil ha mer informasjon, se [Endre tabelltilordningene for synkronisering](admin-how-to-modify-table-mappings-for-synchronization.md).  

-   Med etterfølgende synkroniseringer oppdateres bare poster som er endret eller lagt til etter den siste vellykkede synkroniseringsjobben, for enheten.  

     Nye poster i [!INCLUDE[d365fin](includes/cds_long_md.md)] legges til i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis data i feltene i [!INCLUDE[d365fin](includes/cds_long_md.md)]-postene er endret, blir dataene kopiert til det tilsvarende feltet i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   Med toveis synkronisering synkroniseres jobben fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[d365fin](includes/cds_long_md.md)] og deretter fra [!INCLUDE[d365fin](includes/cds_long_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="about-inactivity-timeouts"></a>Om tidsavbrudd for inaktivitet
Noen jobbkøoppføringer, for eksempel de som planlegger synkronisering mellom [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)], bruker feltet **Tidsavbrudd for inaktivitet** på postkort for jobbkø for å hindre at jobbkøen kjøres unødig.  
<br><br>

> ![Flytskjema for når jobbkøoppføringer settes på vent på grunn av uvirksomhet.](media/on-hold-with-inactivity-timeout.png)

Når verdien i dette feltet ikke er null, og jobbkøen ikke fant noen endringer under siste kjøring, setter [!INCLUDE[d365fin](includes/d365fin_md.md)] jobbkøoppføringen på vent. Når dette skjer, viser **Status for jobbkø**-feltet **Avvent på grunn av inaktivitet**, og [!INCLUDE[d365fin](includes/d365fin_md.md)] venter på tidsrommet som er angitt i feltet **Tidsavbrudd for inaktivitet** før jobbkøoppføringen kjøres på nytt. 

Som standard vil for eksempel CURRENCY-jobbkøoppføringen, som synkroniserer valutaer i [!INCLUDE[d365fin](includes/cds_long_md.md)] med valutakurser i [!INCLUDE[d365fin](includes/d365fin_md.md)], se etter endringer i valutakursene hvert 30. minutt. Hvis ingen endringer blir funnet, setter [!INCLUDE[d365fin](includes/d365fin_md.md)] CURRENCY-jobbkøoppføringen på vent i 720 minutter (seks timer). Hvis en valutakurs endres i [!INCLUDE[d365fin](includes/d365fin_md.md)] mens jobbkøoppføringen er på vent, vil [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisk aktivere jobbkøoppføringen og starte jobbkøen på nytt. 

> [!Note]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] vil automatisk bare aktivere jobbkøoppføringer som er satt på vent, når endringer forekommer i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Endringer i [!INCLUDE[d365fin](includes/cds_long_md.md)] vil ikke aktivere jobbkøoppføringer.

## <a name="to-view-the-synchronization-job-log"></a>Slik viser du synkroniseringsjobbloggen  
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Integrasjonssynkroniseringslogg**, og velg deretter den relaterte koblingen.
2.  Hvis én eller flere feil oppstod for en synkroniseringsjobb, vises antall feil i **Mislyktes**-kolonnen. Hvis du vil vise feil for prosjektet, kan du velge nummeret.  

    > [!TIP]  
    > Du kan vise alle synkroniseringsjobbfeil ved å åpne loggen for synkroniseringsjobbfeil direkte.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>Slik viser du synkroniseringsjobbloggen fra tabelltilordningene  
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Tilordninger for integreringstabell**, og velg deretter den relaterte koblingen.
2.  På siden **Tilordninger for integreringstabell** velger du en post, og velg deretter **Logg for synkroniseringsjobb for integrering**.  

## <a name="to-view-the-synchronization-error-log"></a>Slik viser du synkroniseringsfeilloggen  
* Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Integrasjonssynkroniseringsfeil**, og velg deretter den relaterte koblingen.

## <a name="see-also"></a>Se også  
[Synkronisere data i Business Central og [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Synkronisere tabelltilordninger manuelt](admin-manual-synchronization-of-table-mappings.md)  
[Planlegge en synkronisering mellom Business Central og [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Om integrering av Dynamics 365 Business Central med [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  
