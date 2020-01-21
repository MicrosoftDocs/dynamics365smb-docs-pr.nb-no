---
title: Tilordne tabellene og feltene som skal synkroniseres | Microsoft Docs
description: Lær hvordan du kan tilordne tabeller og felt for å synkronisere data mellom Business Central og Dynamics 365 Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 12/18/2019
ms.author: bholtorf
ms.openlocfilehash: 371bd80c04917495ea1b35f214d10d716ed5f9ad
ms.sourcegitcommit: b570997f93d1f7141bc9539c93a67a91226660a8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/08/2020
ms.locfileid: "2943116"
---
# <a name="mapping-the-tables-and-fields-to-synchronize"></a>Tilordne tabellene og feltene som skal synkroniseres
Det grunnleggende for å synkronisere data i [!INCLUDE[d365fin](includes/d365fin_md.md)] med data i [!INCLUDE[crm_md](includes/crm_md.md)] er å tilordne tabellene og feltene som inneholder dataene, til hverandre. Tilordning skjer gjennom integrasjonstabeller. 

## <a name="mapping-integration-tables"></a>Tilordne integrasjonstabeller
En integrasjonstabell er en tabell i [!INCLUDE[d365fin](includes/d365fin_md.md)]-databasen som representerer en enhet, for eksempel en konto, i [!INCLUDE[crm_md](includes/crm_md.md)]. Integrasjonstabeller inneholder felt som samsvarer med feltene i tabellen for [!INCLUDE[crm_md](includes/crm_md.md)]-enheten. Integrasjonstabellen Konto kobler for eksempel til Kontoer-enheten i [!INCLUDE[crm_md](includes/crm_md.md)]. Det må være en integrasjonstabelltilordning for hver enhet i [!INCLUDE[crm_md](includes/crm_md.md)] som du vil synkronisere med data i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Når du oppretter tilkoblingen mellom appene, definerer [!INCLUDE[d365fin](includes/d365fin_md.md)] enkelte standard tabell- og felttilordninger. Du kan endre tabelltilordningene hvis du vil. Hvis du vil ha mer informasjon, se [Standard Sales-enhetstilordning for synkronisering](admin-synchronizing-business-central-and-sales.md#standard-sales-entity-mapping-for-synchronization). Hvis du har endret standardtilordningene og vil tilbakestille endringene, går du til siden **Konfigurasjon for Dynamics 365-tilkobling** og velger **Bruk standard synkroniseringsoppsett**.

> [!Note]
> Hvis du bruker en lokal versjon av [!INCLUDE[d365fin](includes/d365fin_md.md)], er integrasjonstabelltilordningene lagret i tabellen 5335 Tilordninger for integreringstabell, og de kan vises og endres fra side 5335 Tilordninger for integreringstabell. Avanserte tilordninger og synkroniseringsregler er definert i codeunit 5341. 

### <a name="synchronization-rules"></a>Synkroniseringsregler
En integreringstabelltilordning inneholder også regler som styrer hvordan integrasjonssynkroniseringsjobber synkroniserer poster i en [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell og en enhet i [!INCLUDE[crm_md](includes/crm_md.md)]. Hvis du vil ha mer informasjon, kan du se [Synkroniseringsregler](admin-synchronizing-business-central-and-sales.md#synchronization-rules). 

## <a name="mapping-integration-fields"></a>Tilordne integreringsfelt
Tilordning av tabeller er bare det første trinnet. Du må også tilordne feltene i tabellene. Integreringsfelttilordninger kobler felt i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller med tilsvarende felt i [!INCLUDE[crm_md](includes/crm_md.md)], og avgjør om data skal synkroniseres i hver tabell. Standard tabelltilordning som [!INCLUDE[d365fin](includes/d365fin_md.md)] sørger for, inneholder felttilordninger, men du kan endre dem hvis du vil. Hvis du vil ha mer informasjon, kan du se [Vise enhetstilordninger](admin-synchronizing-business-central-and-sales.md#tip-for-admins-viewing-entity-mappings).

> [!Note]
> Hvis du bruker en lokal versjon av [!INCLUDE[d365fin](includes/d365fin_md.md)], defineres tilordninger for integreringsfelt i tabell 5336 Tilordning for integreringsfelt.

## <a name="coupling-records"></a>Koblingsposter
Kobling kobler poster i [!INCLUDE[crm_md](includes/crm_md.md)] til poster i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Kontoer i [!INCLUDE[crm_md](includes/crm_md.md)] er for eksempel vanligvis koblet sammen med kunder i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Kobling av poster gir følgende fordeler:

* Det gjør synkronisering mulig.
* Brukere kan åpne poster i én forretningsapp fra den andre. Dette krever at løsningen for [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrasjon er installert i [!INCLUDE[crm_md](includes/crm_md.md)].

Koblinger kan settes opp automatisk ved hjelp av synkroniseringsjobber eller manuelt ved å redigere posten i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du vil ha mer informasjon, kan du se [Synkronisere data i [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)]](admin-synchronizing-business-central-and-sales.md) og [Sammenkoble og synkronisere poster manuelt](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings).

## <a name="filtering-records"></a>Filtrere poster  
Hvis du ikke vil synkronisere alle postene for en bestemt [!INCLUDE[crm_md](includes/crm_md.md)]-enhet eller [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell, kan du sette opp filtre for å begrense postene som synkroniseres. Du definerer filtrene på siden **Tilordninger for integreringstabell**.  

#### <a name="to-filter-records-for-synchronization"></a>Filtrere poster for synkronisering  
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Tilordninger for integreringstabell**, og velg deretter den relaterte koblingen.

2.  For å filtrere [!INCLUDE[d365fin](includes/d365fin_md.md)]-postene angir du **Tabellfilter**-feltet.  

3.  For å filtrere [!INCLUDE[crm_md](includes/crm_md.md)]-postene angir du **Integreringstabellfilter**-feltet.  

## <a name="creating-new-records"></a>Opprette nye poster  
 Som standard vil bare poster i [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] som er koblet, synkroniseres av integreringssynkroniseringsjobbene. Du kan definere tabelltilordninger slik at nye poster opprettes i målet (for eksempel [!INCLUDE[d365fin](includes/d365fin_md.md)]) for hver post i kilden (for eksempel [!INCLUDE[crm_md](includes/crm_md.md)]) som ikke allerede er koblet.  

 SELGERE – Dynamics 365 Sales-synkroniseringsjobben bruker for eksempel tabelltilordningen SELGERE. Synkroniseringsjobben kopierer data fra brukerposter i [!INCLUDE[crm_md](includes/crm_md.md)] til selgerposter i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du setter opp tabelltilordningen til å opprette nye poster, for hver bruker i [!INCLUDE[crm_md](includes/crm_md.md)] som ikke er allerede koblet til en selger i [!INCLUDE[d365fin](includes/d365fin_md.md)], opprettes en ny selgerpost i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-create-new-records-during-synchronization"></a>Slik oppretter du nye poster under synkronisering  
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Tilordninger for integreringstabell**, og velg deretter den relaterte koblingen.

2.  I tabelltilordningsoppføringen i listen fjerner du **Synkroniser bare koblede poster**-feltet.  

## <a name="using-configuration-templates-on-table-mappings"></a>Bruke konfigurasjonsmaler på tabelltilordninger
Du kan tilordne konfigurasjonsmaler til tabelltilordninger til bruk for nye poster som er opprettet i [!INCLUDE[d365fin](includes/d365fin_md.md)] eller [!INCLUDE[crm_md](includes/crm_md.md)]. For hver tabelltilordning kan du angi en konfigurasjonsmal som skal brukes for nye [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster, og en annen mal for å bruke nye [!INCLUDE[crm_md](includes/crm_md.md)]-poster.  

Hvis du installerer standard synkroniseringsoppsett, vil to konfigurasjonsmaler vanligvis bli opprettet automatisk og brukes på tabelltilordningen for [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder og [!INCLUDE[crm_md](includes/crm_md.md)]-kontoer: **CRMCUST** og **CRMACCOUNT**.  

-   **CRMCUST** brukes til å opprette og synkronisere nye kunder i [!INCLUDE[d365fin](includes/d365fin_md.md)] basert på en konto i [!INCLUDE[crm_md](includes/crm_md.md)].  

     Denne malen opprettes ved å kopiere en eksisterende konfigurasjonsmal for kunder i programmet. **CRMCUST** opprettes bare hvis det finnes en eksisterende konfigurasjonsmal og **Valutakoden** -feltet i malen er tomt. Hvis et felt i konfigurasjonsmalen inneholder en verdi, brukes verdien i stedet for verdien i det tilordnede feltet for [!INCLUDE[crm_md](includes/crm_md.md)]-kontoen. Hvis **Land/region**-feltet i en [!INCLUDE[crm_md](includes/crm_md.md)]-konto inneholder *USA*, og **Land/region**-feltet i konfigurasjonsmalen er *GB*, brukes *GB* som **Land/region** for den opprettede kunden i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   **CRMACCOUNT** oppretter og synkroniserer nye kontoer i [!INCLUDE[crm_md](includes/crm_md.md)] basert på en konto i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Angi konfigurasjonsmaler på en tabelltilordning  
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Tilordninger for integreringstabell**, og velg deretter den relaterte koblingen.

2.  I tabelltilordningsposten i listen angir du **Malkode for konfigurasjon av tabell**-feltet, velger du konfigurasjonsmalen som skal brukes for nye poster i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

3.  Sett **Malkode for konfigurasjon av int.tab.**-feltet til konfigurasjonsmalen som skal brukes for nye poster i [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Se også  
[Om integrering av Dynamics 365 Business Central med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Synkronisere Business Central og Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)   
[Planlegge en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
