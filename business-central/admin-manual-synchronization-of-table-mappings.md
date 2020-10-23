---
title: Manuell synkronisering i tabelltilordninger | Microsoft Docs
description: Synkroniseringen kopierer data mellom Common Data Service-enheter og Business Central for å holde begge systemene oppdatert.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: ba79088bc386a856f1b3e7727f1f778ebabb7d51
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911333"
---
# <a name="manually-synchronize-table-mappings"></a>Synkronisere tabelltilordninger manuelt
En integrert tabelltilordning knytter en [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell (posttype), for eksempel kunde, med en [!INCLUDE[d365fin](includes/cds_long_md.md)]-enhet, for eksempel en konto. Synkronisering av en integrert tabelltilordning gjør det mulig å synkronisere data i alle poster av [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen og [!INCLUDE[d365fin](includes/cds_long_md.md)]-enheten som er koblet. I tillegg, avhengig av oppsettet for tabelltilordningen, kan synkroniseringen opprette og koble nye poster i målløsningen for ukoblede poster i kilden.  

Manuell synkronising av integrerte tabelltilordninger kan være nyttig under første oppsett av en integrasjon og ved diagnostisering av synkroniseringsfeil.  

Denne artikkelen beskriver tre metoder for manuell synkronisering av integrasjonstabelltilordninger. Hver metode gir et annet synkroniseringsnivå.

## <a name="run-a-full-synchronization"></a>Kjøre en full synkronisering
En fullstendig synkronisering kjører alle standard integreringssynkroniseringsjobber for synkronisering av [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster og [!INCLUDE[d365fin](includes/cds_long_md.md)]-enheter, som definert på siden **Tilordninger for integreringstabell**. 

En fullstendig synkronisering utfører følgende operasjoner for [!INCLUDE[d365fin](includes/d365fin_md.md)]- eller [!INCLUDE[d365fin](includes/cds_long_md.md)]-poster som er:

* Ikke koblet, en ny samsvarende post opprettes og kobles i den motstående løsningen.
Om og hvor det opprettes en post, avhenger av synkroniseringsretningen. Når du for eksempel synkroniserer data fra [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder til [!INCLUDE[d365fin](includes/cds_long_md.md)]-kontoer, hvis en kunde ikke er koblet til en konto, legges det til en ny konto automatisk i [!INCLUDE[d365fin](includes/cds_long_md.md)] og kobles til kunden i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det motsatte gjelder når synkroniseringsretningen er fra [!INCLUDE[d365fin](includes/cds_long_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)]. For hver konto som ikke allerede er koblet til en kunde, opprettes en tilsvarende kunde i [!INCLUDE[d365fin](includes/d365fin_md.md)] og kobles til kontoen i [!INCLUDE[d365fin](includes/cds_long_md.md)].  

     > [!NOTE]  
     >  For å gjøre dette fjerner den fullstendige synkroniseringsoperasjonen alternativet **Synkroniser bare koblede poster** i integrasjonstabellen som brukes av synkroniseringsjobben. På slutten av den fullstendige synkroniseringsprosessen blir du spurt om du vil beholde dette alternativet fjernet for alle jobbene.  

* Koblet er synkroniseringsretningen (for eksempel fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[d365fin](includes/cds_long_md.md)] eller fra [!INCLUDE[d365fin](includes/cds_long_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)]) forhåndsbestemt av integrasjonstabelltilordningene. Hvis du vil ha mer informasjon, kan du se [Standard enhetstilordning for synkronisering](admin-synchronizing-business-central-and-sales.md#standard-entity-mapping-for-synchronization).  

> [!IMPORTANT]  
>  Du bruker vanligvis bare fullstendig synkronisering første gang du definerer integrasjon mellom [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)] og bare én av løsningene inneholder data, som du vil kopiere til den andre løsningen. En fullstendig synkronisering kan være nyttige i et demonstrasjonsmiljø. Siden fullstendig synkronisering automatisk oppretter og kobler poster mellom løsninger, er det raskere å begynne å arbeide med synkronisering av data mellom poster. Derimot må du bare utføre en full synkronisering hvis du vil ha en post i [!INCLUDE[d365fin](includes/d365fin_md.md)] for hver post i [!INCLUDE[d365fin](includes/cds_long_md.md)] for de gitte tabelltilordningene. Hvis ikke kan det oppstå uønskede eller dupliserte poster i [!INCLUDE[d365fin](includes/d365fin_md.md)] eller [!INCLUDE[d365fin](includes/cds_long_md.md)].  

### <a name="to-run-a-full-synchronization"></a>Kjøre en full synkronisering  
1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Tilkoblingsoppsett for Common Data Service**, og velg deretter den relaterte koblingen.

    > [!NOTE]
    > Hvis du vil kjøre en fullstendig synkronisering for enheter via Dynamics 365 Sales, bruker du i stedet siden **Tilkoblingsoppsett for Microsoft Dynamics**.

2.  Velg handlingen **Kjør full synkronisering**, og velg deretter **Ja**-knappen.  
3.  Når full synkronisering er fullført, kan du angi om du vil at planlagte synkroniseringsjobber skal kunne opprette nye poster.  

    Hvis du vil at alle synkroniseringsjobber skal kunne opprette nye poster i målet for ukoblede poster i kilden, velger du **Ja**. Dette angir feltet **Synkroniser bare koblede poster** på tabelltilordningene som brukes av synkroniseringsjobbene.  

    Hvis du vil at synkroniseringsjobber skal kjøres som før den fullstendige synkroniseringen med hensyn til å opprette nye poster, velger du **Nei**. Dette setter feltet **Synkroniser bare koblede poster** til innstillingen det hadde før fullstendig synkronisering.  

Du kan se resultatet av den fullstendige synkroniseringen på siden **Synkroniseringsjobber for integrering**. Hvis du vil ha mer informasjon, kan du se [Vise statusen for en synkronisering](admin-how-to-view-synchronization-status.md).  

## <a name="synchronizing-all-modified-records"></a>Synkronisere alle endrede poster
Du kan bruke siden **Konfigurasjon for CDS-tilkobling** til å synkronisere endringer i data i alle integrasjonstabelltilordninger. Dette ligner på en fullstendig synkronisering. Det synkroniseres data i alle koblede poster i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellene og [!INCLUDE[d365fin](includes/cds_long_md.md)]-enhetene som er definert i tabelltilordningene. Som standard synkroniseres bare poster som har blitt endret siden forrige gang de ble synkronisert. Synkroniseringsjobber synkroniserer tabelltilordninger i følgende rekkefølgen for å unngå å koble avhengigheter mellom enhetene:  

1.  CURRENCY  
2.  SELGERE  
3.  VENDOR  
4.  CUSTOMER  
5.  KONTAKTER  

Du kan se resultatet av synkroniseringen på siden **Synkroniseringsjobber for integrering**. Hvis du vil ha mer informasjon, kan du se [Vise statusen for en synkronisering](admin-how-to-view-synchronization-status.md).  

> [!TIP]  
>  Når du endrer integreringstabelltilordningen på forhånd, kan du konfigurere synkroniseringen med filtre for å kontrollere hvilke poster som er synkronisert, eller konfigurere den for å opprette nye poster i målløsningen for ukoblede poster i kilden. Hvis du vil ha mer informasjon, se [Endre tabelltilordningene for synkronisering](admin-how-to-modify-table-mappings-for-synchronization.md).

### <a name="to-synchronize-records-for-all-tables"></a>Synkronisere poster for alle tabeller  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Tilkoblingsoppsett for Microsoft Dynamics 365 Sales**, og velg deretter den relaterte koblingen.
2.  Velg **Synkroniser endrede poster**-handlingen, og velg deretter **Ja**.  

## <a name="synchronize-individual-table-mappings"></a>Synkronisere individuelle tabelltilordninger
Du kan bruke siden **Tilordninger for integreringstabell** til å utføre en synkroniseringsjobb for spesifikke tabelltilordninger. Dette synkroniserer data i alle koblede poster i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen og [!INCLUDE[d365fin](includes/cds_long_md.md)]-enheten som er definert av tabelltilordningen. Som standard synkroniseres bare poster som har blitt endret siden forrige gang de ble synkronisert.  

Ved å endre integrasjonstabelltilordningen på forhånd kan du konfigurere synkroniseringsjobben til å opprette nye poster i målløsningen for ukoblede poster i kilden.

### <a name="to-synchronize-records-of-an-integration-table-mapping"></a>Synkronisere poster i en integrasjonstabelltilordning  
1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Tilordninger for integreringstabell**, og velg deretter den relaterte koblingen.
2.  Velg **Synkroniser endrede poster**-handlingen, og velg deretter **Ja**.  

## <a name="see-also"></a>Se også  
[Synkronisere Business Central og Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)   
[Sette opp brukerkontoer for integrasjon med Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)   
