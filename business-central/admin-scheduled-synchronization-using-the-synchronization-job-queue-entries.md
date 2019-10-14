---
title: Synkronisere Business Central og Dynamics 365 Sales | Microsoft Docs
description: Lær om å synkronisere data mellom Business Central og Dynamics 365 Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 8b1fd4a676d1efe508e6fd2dcb37a67b3c24cdb1
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304351"
---
# <a name="scheduling-a-synchronization-between-business-central-and-dynamics-365-sales"></a>Planlegge en synkronisering mellom Business Central og Dynamics 365 Sales
Du kan synkronisere [!INCLUDE[d365fin](includes/d365fin_md.md)] med [!INCLUDE[crm_md](includes/crm_md.md)] på planlagte intervaller ved å definere jobber i jobbkøen. Synkroniseringsjobbene synkroniserer data i [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster og [!INCLUDE[crm_md](includes/crm_md.md)]-poster som har blitt koblet sammen tidligere. Eller for poster som ikke allerede er koblet, avhengig av synkroniseringsretningen og regler, kan synkroniseringsjobbene opprette og koble nye poster i målsystemet. Det finnes flere synkroniseringsjobber som er tilgjengelige som standard. Du kan vise dem på siden **Poster i jobbkø**. Hvis du vil ha mer informasjon, kan du se [Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).
<!--
> [!Note]
> For the on-premeses version of [!INCLUDE[d365fin](includes/d365fin_md.md)], the synchronization jobs are run by codeunit **5339 Integration synch Job Runner**.--> 

## <a name="synchronization-process"></a>Synkroniseringsprosess  
Hver jobbkøpost for synkronisering bruker en bestemt integrasjonstabelltilordning som angir hvilken [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell og [!INCLUDE[crm_md](includes/crm_md.md)]-enhet som skal synkroniseres. Tabelltilordningene inneholder også enkelte innstillinger som bestemmer hvilke poster i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen og [!INCLUDE[crm_md](includes/crm_md.md)]-enheten som skal synkroniseres.  

For å kunne synkronisere data må [!INCLUDE[crm_md](includes/crm_md.md)]-enhetspostene være koblet til [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster. For eksempel må en [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunde være koblet til en [!INCLUDE[crm_md](includes/crm_md.md)]-konto. Du kan konfigurere koblinger manuelt før du kjører synkroniseringsjobber eller la synkroniseringsjobbene sette opp koblinger automatisk. Følgende liste beskriver hvordan dataene blir synkronisert mellom [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)] når du bruker jobbkøposter for synkronisering. Hvis du vil ha mer informasjon, se [Sammenkoble og synkronisere poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md). 

-   Som standard synkroniseres bare poster i [!INCLUDE[d365fin](includes/d365fin_md.md)] som er koblet til poster i [!INCLUDE[crm_md](includes/crm_md.md)]. Du kan endre tabelltilordningen mellom en [!INCLUDE[crm_md](includes/crm_md.md)]-enhet og en [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell, slik at integrasjonssynkroniseringsjobbene oppretter nye poster i måldatabasen for hver post i kildedatabasen som ikke er koblet. De nye postene er også koblet til tilsvarende poster i kilden. Når du for eksempel synkroniserer kunder med [!INCLUDE[crm_md](includes/crm_md.md)]-konti, opprettes en ny postkonto for hver kunde i [!INCLUDE[d365fin](includes/d365fin_md.md)]. De nye kontoene kobles automatisk til kunder i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Fordi synkronisering i dette tilfellet er toveis, opprettes og kobles en ny kunde for hver [!INCLUDE[crm_md](includes/crm_md.md)]-konto som ikke allerede er koblet.  

    > [!NOTE]  
    > Det finnes regler og filtre som bestemmer hvilke data som synkroniseres. Hvis du vil ha mer informasjon, kan du se [Synkroniseringsregler](admin-synchronizing-business-central-and-sales.md#synchronization-rules).

-   Når nye poster opprettes i [!INCLUDE[d365fin](includes/d365fin_md.md)], bruker postene enten malen som er definert for integrasjonstabelltilordningen, eller standardmalen som er tilgjengelig for posttypen. Felt fylles ut med data fra [!INCLUDE[d365fin](includes/d365fin_md.md)] eller [!INCLUDE[crm_md](includes/crm_md.md)], avhengig av synkroniseringsretningen. Hvis du vil ha mer informasjon, se [Endre tabelltilordningene for synkronisering](admin-how-to-modify-table-mappings-for-synchronization.md).  

-   Med etterfølgende synkroniseringer oppdateres bare poster som er endret eller lagt til etter den siste vellykkede synkroniseringsjobben, for enheten.  

     Nye poster i [!INCLUDE[crm_md](includes/crm_md.md)] legges til i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis data i feltene i [!INCLUDE[crm_md](includes/crm_md.md)]-postene er endret, blir dataene kopiert til det tilsvarende feltet i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   Med toveis synkronisering synkroniseres jobben fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)] og deretter fra [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="default-synchronization-job-queue-entries"></a>Jobbkøposter for standard synkronisering  
Tabellen nedenfor beskriver standard synkroniseringsjobber.  

|Jobbkøpost|Beskrivelse|Retning|Tilordning for integreringstabell|  
|---------------------|---------------------------------------|---------------|-------------------------------|  
|KONTAKT – Dynamics 365 Sales-synkroniseringsjobb|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-kontakter med [!INCLUDE[d365fin](includes/d365fin_md.md)]-kontakter.|Toveis|CONTACT|  
|VALUTA – Dynamics 365 Sales-synkroniseringsjobb|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-transaksjonsvalutaer med [!INCLUDE[d365fin](includes/d365fin_md.md)]-valutaer.|Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|CURRENCY|  
|KUNDE – Dynamics 365 Sales-synkroniseringsjobb|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-kontoer med [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder.|Toveis|CUSTOMER|  
|KUNDEPRISGRUPPER-PRIS – Dynamics 365 Sales-synkroniseringsjobb|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-salgspriser med [!INCLUDE[d365fin](includes/d365fin_md.md)]-kundeprisgrupper.| |KUNDEPRISGRUPPER-SALGSPRISLISTER|
|VARE-PRODUKT – Dynamics 365 Sales-synkroniseringsjobb|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-produkter med [!INCLUDE[d365fin](includes/d365fin_md.md)]-varer.|Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|VARE-PRODUKT|
|BOKFØRTE SALGSFAKTURAER-FAKTURAER – Dynamics 365 Sales-synkroniseringsjobb|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-fakturaer med [!INCLUDE[d365fin](includes/d365fin_md.md)]-bokførte salgsfakturaer.|Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|FAKTURAER-BOKFØRTE SALGSFAKTURAER|
|RESSURS-PRODUKT – Dynamics 365 Sales-synkroniseringsjobb|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-produkter med [!INCLUDE[d365fin](includes/d365fin_md.md)]-ressurser.|Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|RESSURS-PRODUKT|  
|SELGERE – Dynamics 365 Sales-synkroniseringsjobb|Synkroniserer [!INCLUDE[d365fin](includes/d365fin_md.md)]-selgere med [!INCLUDE[crm_md](includes/crm_md.md)]-brukere.|Fra [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)]|SELGERE|
|SALGSPRIS-PRODUKTPRIS – Dynamics 365 Sales-synkroniseringsjobb|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-produktpriser med [!INCLUDE[d365fin](includes/d365fin_md.md)]-salgspriser.||PRODUKTPRIS-SALGSPRIS|
|MÅLEENHET – Dynamics 365 Sales-synkroniseringsjobb|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-enhetsgrupper med [!INCLUDE[d365fin](includes/d365fin_md.md)]-enheter.|Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|MÅLENHET|  
|Kundestatistikk – Dynamics 365 Sales-synkroniseringsjobb|Oppdaterer [!INCLUDE[crm_md](includes/crm_md.md)]-konti med de nyeste [!INCLUDE[d365fin](includes/d365fin_md.md)]-kundedataene. I [!INCLUDE[crm_md](includes/crm_md.md)] vises denne informasjonen i **Business Central-kontostatistikk**-hurtigvisningsskjemaet for kontoer som er koblet til [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder.<br /><br /> Disse dataene kan også oppdateres manuelt fra hver enkelt kundepost. Hvis du vil ha mer informasjon, se [Sammenkoble og synkronisere poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Merk:**  Denne jobbkøen er relevant bare hvis [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrasjonsløsningen er installert i [!INCLUDE[crm_md](includes/crm_md.md)]. Hvis du vil ha mer informasjon, se [Om Business Central-integrasjonsløsningen](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).|Ikke i bruk.|Ikke i bruk.|   

## <a name="to-view-the-synchronization-job-log"></a>Slik viser du synkroniseringsjobbloggen  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Integrasjonssynkroniseringslogg**, og velg deretter den relaterte koblingen.
2.  Hvis én eller flere feil oppstod for en synkroniseringsjobb, vises antall feil i **Mislyktes**-kolonnen. Hvis du vil vise feil for prosjektet, kan du velge nummeret.  

    > [!TIP]  
    > Du kan vise alle synkroniseringsjobbfeil ved å åpne loggen for synkroniseringsjobbfeil direkte.

## <a name="to-view-the-synchronization-job-log-from-the-table-mappings"></a>Slik viser du synkroniseringsjobbloggen fra tabelltilordningene  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Tilordninger for integreringstabell**, og velg deretter den relaterte koblingen.
2.  På siden **Tilordninger for integreringstabell** velger du en post, og velg deretter **Logg for synkroniseringsjobb for integrering**.  

## <a name="to-view-the-synchronization-error-log"></a>Slik viser du synkroniseringsfeilloggen  
* Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Synkroniseringsfeil for integrering**, og velg deretter den relaterte koblingen.

## <a name="see-also"></a>Se også  
[Synkronisere data i Business Central og Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)  
[Synkronisere tabelltilordninger manuelt](admin-manual-synchronization-of-table-mappings.md)  
[Planlegge en synkronisering mellom Business Central og Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Om integrering av Dynamics 365 Business Central med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  



