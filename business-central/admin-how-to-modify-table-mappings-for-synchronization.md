---
title: Endre tabelltilordninger for synkronisering | Microsoft Docs
description: Lær hvordan du kan endre tabelltilordninger som brukes ved synkroniseringen av data mellom Business Central og Dynamics 365 for Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: de924baa494ae00c09dcb7657c050f2d9ae3ba87
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "940270"
---
# <a name="modify-table-mappings-for-synchronization"></a>Endre tabelltilordningene for synkronisering
En integrasjonstabelltilordning kobler en tabell i [!INCLUDE[d365fin](includes/d365fin_md.md)] til en integrasjonstabell for [!INCLUDE[crm_md](includes/crm_md.md)]-enheten. For hver enhet i [!INCLUDE[crm_md](includes/crm_md.md)] som du vil synkronisere med tilhørende data i [!INCLUDE[d365fin](includes/d365fin_md.md)], må det være en tilsvarende integrasjonstabelltilordning. En integrasjonstabelltilordning inneholder flere innstillinger som du kan bruke til å kontrollere hvordan poster i en [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell og en [!INCLUDE[crm_md](includes/crm_md.md)]-enhet synkroniseres med tilsvarende integrasjonssynkroniseringsjobber.  

## <a name="filtering-records"></a>Filtrere poster  
 Hvis du ikke vil synkronisere alle postene for en bestemt [!INCLUDE[crm_md](includes/crm_md.md)]-enhet eller [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell, kan du sette opp filtre for å begrense postene som synkroniseres. Du definerer filtrene på siden **Tilordninger for integreringstabell**.  

#### <a name="to-filter-records-for-synchronization"></a>Filtrere poster for synkronisering  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Tilordninger for integreringstabell**, og velg deretter den relaterte koblingen.

2.  For å filtrere [!INCLUDE[d365fin](includes/d365fin_md.md)]-postene angir du **Tabellfilter**-feltet.  

3.  For å filtrere [!INCLUDE[crm_md](includes/crm_md.md)]-postene angir du **Integreringstabellfilter**-feltet.  

## <a name="creating-new-records"></a>Opprette nye poster  
 Som standard vil bare poster i [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] som er koblet, synkroniseres av integreringssynkroniseringsjobbene. Du kan definere tabelltilordninger slik at nye poster opprettes i målet (for eksempel [!INCLUDE[d365fin](includes/d365fin_md.md)]) for hver post i kilden (for eksempel [!INCLUDE[crm_md](includes/crm_md.md)]) som ikke allerede er koblet.  

 SELGERE – Dynamics 365 for Sales-synkroniseringsjobben bruker for eksempel tabelltilordningen SELGERE. Synkroniseringsjobben kopierer data fra brukerposter i [!INCLUDE[crm_md](includes/crm_md.md)] til selgerposter i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du setter opp tabelltilordningen til å opprette nye poster, for hver bruker i [!INCLUDE[crm_md](includes/crm_md.md)] som ikke er allerede koblet til en selger i [!INCLUDE[d365fin](includes/d365fin_md.md)], opprettes en ny selgerpost i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-create-new-records-during-synchronization"></a>Slik oppretter du nye poster under synkronisering  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Tilordninger for integreringstabell**, og velg deretter den relaterte koblingen.

2.  I tabelltilordningsoppføringen i listen fjerner du **Synkroniser bare koblede poster**-feltet.  

## <a name="using-configuration-templates-on-table-mappings"></a>Bruke konfigurasjonsmaler på tabelltilordninger
Du kan tilordne konfigurasjonsmaler til tabelltilordninger til bruk for nye poster som er opprettet i [!INCLUDE[d365fin](includes/d365fin_md.md)] eller [!INCLUDE[crm_md](includes/crm_md.md)]. For hver tabelltilordning kan du angi en konfigurasjonsmal som skal brukes for nye [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster, og en annen mal for å bruke nye [!INCLUDE[crm_md](includes/crm_md.md)]-poster.  

Hvis du installerer standard synkroniseringsoppsett, vil to konfigurasjonsmaler vanligvis bli opprettet automatisk og brukes på tabelltilordningen for [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder og [!INCLUDE[crm_md](includes/crm_md.md)]-kontoer: **CRMCUST** og **CRMACCOUNT**.  

-   **CRMCUST** brukes til å opprette og synkronisere nye kunder i [!INCLUDE[d365fin](includes/d365fin_md.md)] basert på en konto i [!INCLUDE[crm_md](includes/crm_md.md)].  

     Denne malen opprettes ved å kopiere en eksisterende konfigurasjonsmal for kunder i programmet. **CRMCUST** opprettes bare hvis det finnes en eksisterende konfigurasjonsmal og **Valutakoden** -feltet i malen er tomt. Hvis et felt i konfigurasjonsmalen inneholder en verdi, brukes verdien i stedet for verdien i det tilordnede feltet for [!INCLUDE[crm_md](includes/crm_md.md)]-kontoen. Hvis **Land/region**-feltet i en [!INCLUDE[crm_md](includes/crm_md.md)]-konto inneholder *USA*, og **Land/region**-feltet i konfigurasjonsmalen er *GB*, brukes *GB* som **Land/region** for den opprettede kunden i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   **CRMACCOUNT** oppretter og synkroniserer nye kontoer i [!INCLUDE[crm_md](includes/crm_md.md)] basert på en konto i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Angi konfigurasjonsmaler på en tabelltilordning  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Tilordninger for integreringstabell**, og velg deretter den relaterte koblingen.

2.  I tabelltilordningsposten i listen angir du **Malkode for konfigurasjon av tabell**-feltet, velger du konfigurasjonsmalen som skal brukes for nye poster i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

3.  Sett **Malkode for konfigurasjon av int.tab.**-feltet til konfigurasjonsmalen som skal brukes for nye poster i [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Se også  
[Om integrering av Dynamics 365 Business Central med Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Synkronisere Business Central og Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md)   
[Planlegge en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
