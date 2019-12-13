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
ms.openlocfilehash: 4b6137f6d5fa057d801a1afe30480017ceadd1c8
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879085"
---
# <a name="scheduling-a-synchronization-between-business-central-and-dynamics-365-sales"></a>Planlegge en synkronisering mellom Business Central og Dynamics 365 Sales
Du kan synkronisere [!INCLUDE[d365fin](includes/d365fin_md.md)] med [!INCLUDE[crm_md](includes/crm_md.md)] på planlagte intervaller ved å definere jobber i jobbkøen. Synkroniseringsjobbene synkroniserer data i [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster og [!INCLUDE[crm_md](includes/crm_md.md)]-poster som har blitt koblet sammen tidligere. Eller for poster som ikke allerede er koblet, avhengig av synkroniseringsretningen og regler, kan synkroniseringsjobbene opprette og koble nye poster i målsystemet. Det finnes flere synkroniseringsjobber som er tilgjengelige som standard. Du kan vise dem på siden **Poster i jobbkø**. Hvis du vil ha mer informasjon, kan du se [Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).
<!--
> [!Note]
> For the on-premeses version of [!INCLUDE[d365fin](includes/d365fin_md.md)], the synchronization jobs are run by codeunit **5339 Integration synch Job Runner**.-->

## <a name="synchronization-process"></a>Synkroniseringsprosess  
Hver jobbkøpost for synkronisering bruker en bestemt integrasjonstabelltilordning som angir hvilken [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell og [!INCLUDE[crm_md](includes/crm_md.md)]-enhet som skal synkroniseres. Tabelltilordningene inneholder også enkelte innstillinger som bestemmer hvilke poster i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen og [!INCLUDE[crm_md](includes/crm_md.md)]-enheten som skal synkroniseres.  

For å kunne synkronisere data må [!INCLUDE[crm_md](includes/crm_md.md)]-enhetspostene være koblet til [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster. For eksempel må en [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunde være koblet til en [!INCLUDE[crm_md](includes/crm_md.md)]-konto. Du kan konfigurere koblinger manuelt før du kjører synkroniseringsjobber eller la synkroniseringsjobbene sette opp koblinger automatisk. Følgende liste beskriver hvordan dataene blir synkronisert mellom [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)] når du bruker jobbkøposter for synkronisering. Hvis du vil ha mer informasjon, se [Sammenkoble og synkronisere poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md).

-   Avmerkingsboksen **Synkroniser bare koblede poster** kontrollerer om det opprettes nye poster når du synkroniserer. Som standard er det merket av for dette alternativet, som betyr at bare poster som er kombinert, vil bli synkronisert. I integrasjonstabelltilordning kan du endre tabelltilordningen mellom en [!INCLUDE[crm_md](includes/crm_md.md)]-enhet og en [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell, slik at integrasjonssynkroniseringsjobbene oppretter nye poster i måldatabasen for hver post i kildedatabasen som ikke er koblet. Hvis du vil ha mer informasjon, kan du se [Opprette nye poster](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records). 
    
    **Eksempel** Hvis du fjerner merket for **Synkroniser bare koblede poster** når du synkroniserer kunder i [!INCLUDE[d365fin](includes/d365fin_md.md)] med kontoer i [!INCLUDE[crm_md](includes/crm_md.md)], opprettes det en ny konto for hver kunde i [!INCLUDE[d365fin](includes/d365fin_md.md)], og kobling opprettes automatisk. I tillegg, fordi synkronisering i dette tilfellet er toveis, opprettes og kobles en ny kunde for hver [!INCLUDE[crm_md](includes/crm_md.md)]-konto som ikke allerede er koblet.  

    > [!NOTE]  
    > Det finnes regler og filtre som bestemmer hvilke data som synkroniseres. Hvis du vil ha mer informasjon, kan du se [Synkroniseringsregler](admin-synchronizing-business-central-and-sales.md#synchronization-rules).

-   Når nye poster opprettes i [!INCLUDE[d365fin](includes/d365fin_md.md)], bruker postene enten malen som er definert for integrasjonstabelltilordningen, eller standardmalen som er tilgjengelig for posttypen. Felt fylles ut med data fra [!INCLUDE[d365fin](includes/d365fin_md.md)] eller [!INCLUDE[crm_md](includes/crm_md.md)], avhengig av synkroniseringsretningen. Hvis du vil ha mer informasjon, se [Endre tabelltilordningene for synkronisering](admin-how-to-modify-table-mappings-for-synchronization.md).  

-   Med etterfølgende synkroniseringer oppdateres bare poster som er endret eller lagt til etter den siste vellykkede synkroniseringsjobben, for enheten.  

     Nye poster i [!INCLUDE[crm_md](includes/crm_md.md)] legges til i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis data i feltene i [!INCLUDE[crm_md](includes/crm_md.md)]-postene er endret, blir dataene kopiert til det tilsvarende feltet i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   Med toveis synkronisering synkroniseres jobben fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)] og deretter fra [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="default-synchronization-job-queue-entries"></a>Jobbkøposter for standard synkronisering  
Tabellen nedenfor beskriver standard synkroniseringsjobber.  

|Jobbkøpost|Beskrivelse|Retning|Tilordning for integreringstabell|Standard synkroniseringsfrekvens (minutter)|Standard hvilemodustid for inaktivitet (minutter)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|KONTAKT – Dynamics 365 Sales-synkroniseringsjobb|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-kontakter med [!INCLUDE[d365fin](includes/d365fin_md.md)]-kontakter.|Toveis|CONTACT|30|720 <br>(12 timer)| 
|VALUTA – Dynamics 365 Sales-synkroniseringsjobb|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-transaksjonsvalutaer med [!INCLUDE[d365fin](includes/d365fin_md.md)]-valutaer.|Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|CURRENCY|30|720 <br> (12 timer)| 
|KUNDE – Dynamics 365 Sales-synkroniseringsjobb|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-kontoer med [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder.|Toveis|CUSTOMER|30|720<br> (12 timer)|
|KUNDEPRISGRUPPER-PRIS – Dynamics 365 Sales-synkroniseringsjobb|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-salgspriser med [!INCLUDE[d365fin](includes/d365fin_md.md)]-kundeprisgrupper.| |KUNDEPRISGRUPPER-SALGSPRISLISTER|30|1440<br> (24 timer)|
|VARE-PRODUKT – Dynamics 365 Sales-synkroniseringsjobb|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-produkter med [!INCLUDE[d365fin](includes/d365fin_md.md)]-varer.|Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|VARE-PRODUKT|30|1440<br> (24 timer)|
|BOKFØRTE SALGSFAKTURAER-FAKTURAER – Dynamics 365 Sales-synkroniseringsjobb|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-fakturaer med [!INCLUDE[d365fin](includes/d365fin_md.md)]-bokførte salgsfakturaer.|Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|FAKTURAER-BOKFØRTE SALGSFAKTURAER|30|1440<br> (24 timer)|
|RESSURS-PRODUKT – Dynamics 365 Sales-synkroniseringsjobb|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-produkter med [!INCLUDE[d365fin](includes/d365fin_md.md)]-ressurser.|Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|RESSURS-PRODUKT|30|720<br> (12 timer)|  
|SELGERE – Dynamics 365 Sales-synkroniseringsjobb|Synkroniserer [!INCLUDE[d365fin](includes/d365fin_md.md)]-selgere med [!INCLUDE[crm_md](includes/crm_md.md)]-brukere.|Fra [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)]|SELGERE|30|1440<br> (24 timer)|
|SALGSPRIS-PRODUKTPRIS – Dynamics 365 Sales-synkroniseringsjobb|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-produktpriser med [!INCLUDE[d365fin](includes/d365fin_md.md)]-salgspriser.||PRODUKTPRIS-SALGSPRIS|30|1440<br> (24 timer)|
|MÅLEENHET – Dynamics 365 Sales-synkroniseringsjobb|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-enhetsgrupper med [!INCLUDE[d365fin](includes/d365fin_md.md)]-enheter.|Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|MÅLENHET|30|720<br> (12 timer)|  
|Kundestatistikk – Dynamics 365 Sales-synkroniseringsjobb|Oppdaterer [!INCLUDE[crm_md](includes/crm_md.md)]-konti med de nyeste [!INCLUDE[d365fin](includes/d365fin_md.md)]-kundedataene. I [!INCLUDE[crm_md](includes/crm_md.md)] vises denne informasjonen i **Business Central-kontostatistikk**-hurtigvisningsskjemaet for kontoer som er koblet til [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder.<br /><br /> Disse dataene kan også oppdateres manuelt fra hver enkelt kundepost. Hvis du vil ha mer informasjon, se [Sammenkoble og synkronisere poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Merk:**  Denne jobbkøen er relevant bare hvis [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrasjonsløsningen er installert i [!INCLUDE[crm_md](includes/crm_md.md)]. Hvis du vil ha mer informasjon, se [Om Business Central-integrasjonsløsningen](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).|Ikke i bruk|Ikke i bruk|30|Ikke i bruk|   

## <a name="about-inactivity-timeouts"></a>Om tidsavbrudd for inaktivitet
Noen jobbkøoppføringer, for eksempel de som planlegger synkronisering mellom [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)], bruker feltet **Tidsavbrudd for inaktivitet** på postkort for jobbkø for å hindre at jobbkøen kjøres unødig.  
<br><br>

> ![Flytskjema for når jobbkøoppføringer settes på vent på grunn av uvirksomhet.](media/on-hold-with-inactivity-timeout.png)

Når verdien i dette feltet ikke er null, og jobbkøen ikke fant noen endringer under siste kjøring, setter [!INCLUDE[d365fin](includes/d365fin_md.md)] jobbkøoppføringen på vent. Når dette skjer, viser **Status for jobbkø**-feltet **Avvent på grunn av inaktivitet**, og [!INCLUDE[d365fin](includes/d365fin_md.md)] venter på tidsrommet som er angitt i feltet **Tidsavbrudd for inaktivitet** før jobbkøoppføringen kjøres på nytt. 

Som standard vil for eksempel CURRENCY-jobbkøoppføringen, som synkroniserer valutaer i [!INCLUDE[crm_md](includes/crm_md.md)] med valutakurser i [!INCLUDE[d365fin](includes/d365fin_md.md)], se etter endringer i valutakursene hvert 30. minutt. Hvis ingen endringer blir funnet, setter [!INCLUDE[d365fin](includes/d365fin_md.md)] CURRENCY-jobbkøoppføringen på vent i 720 minutter (seks timer). Hvis en valutakurs endres i [!INCLUDE[d365fin](includes/d365fin_md.md)] mens jobbkøoppføringen er på vent, vil [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisk aktivere jobbkøoppføringen og starte jobbkøen på nytt. 

> [!Note]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] vil automatisk bare aktivere jobbkøoppføringer som er satt på vent, når endringer forekommer i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Endringer i [!INCLUDE[crm_md](includes/crm_md.md)] vil ikke aktivere jobbkøoppføringer.

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
[Synkronisere data i Business Central og Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)  
[Synkronisere tabelltilordninger manuelt](admin-manual-synchronization-of-table-mappings.md)  
[Planlegge en synkronisering mellom Business Central og Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Om integrering av Dynamics 365 Business Central med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
