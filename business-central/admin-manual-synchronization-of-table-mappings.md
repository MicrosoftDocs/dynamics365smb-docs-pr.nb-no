---
title: Manuell synkronisering i tabelltilordninger | Microsoft Docs
description: Synkroniseringen kopierer data mellom Microsoft Dataverse-tabeller og Business Central for å holde begge systemene oppdatert.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'sales, crm, integration, sync, synchronize'
ms.date: 04/01/2021
ms.author: bholtorf
---

# Synkronisere tabelltilordninger manuelt


En integrert tabelltilordning knytter en [!INCLUDE[prod_short](includes/prod_short.md)]-tabell, for eksempel kunde, med en [!INCLUDE[prod_short](includes/cds_long_md.md)]-tabell, for eksempel en konto. Synkronisering av en integrert tabelltilordning gjør det mulig å synkronisere data i alle poster av [!INCLUDE[prod_short](includes/prod_short.md)]-tabellen og [!INCLUDE[prod_short](includes/cds_long_md.md)]-tabellen som er koblet. I tillegg, avhengig av oppsettet for tabelltilordningen, kan synkroniseringen opprette og koble nye poster i målløsningen for ukoblede poster i kilden.  

Manuell synkronising av integrerte tabelltilordninger kan være nyttig under første oppsett av en integrasjon og ved diagnostisering av synkroniseringsfeil.  

Denne artikkelen beskriver tre metoder for manuell synkronisering av integrasjonstabelltilordninger. Hver metode gir et annet synkroniseringsnivå.

## Kjøre en full synkronisering
En fullstendig synkronisering kjører alle standard integreringssynkroniseringsjobber for synkronisering av [!INCLUDE[prod_short](includes/prod_short.md)]-poster og [!INCLUDE[prod_short](includes/cds_long_md.md)]-tabeller, som definert på siden **Tilordninger for integreringstabell**. 

En fullstendig synkronisering utfører følgende operasjoner for [!INCLUDE[prod_short](includes/prod_short.md)]- eller [!INCLUDE[prod_short](includes/cds_long_md.md)]-poster som er:

* Ikke koblet, en ny samsvarende rad opprettes og kobles i den motstående løsningen.
Om og hvor det opprettes en rad, avhenger av synkroniseringsretningen. Når du for eksempel synkroniserer data fra [!INCLUDE[prod_short](includes/prod_short.md)]-kunder til [!INCLUDE[prod_short](includes/cds_long_md.md)]-kontoer, hvis en kunde ikke er koblet til en konto, legges det til en ny konto automatisk i [!INCLUDE[prod_short](includes/cds_long_md.md)] og kobles til kunden i [!INCLUDE[prod_short](includes/prod_short.md)]. Det motsatte gjelder når synkroniseringsretningen er fra [!INCLUDE[prod_short](includes/cds_long_md.md)] til [!INCLUDE[prod_short](includes/prod_short.md)]. For hver konto som ikke allerede er koblet til en kunde, opprettes en tilsvarende kunde i [!INCLUDE[prod_short](includes/prod_short.md)] og kobles til kontoen i [!INCLUDE[prod_short](includes/cds_long_md.md)].  

     > [!NOTE]  
     >  For å gjøre dette fjerner den fullstendige synkroniseringsoperasjonen alternativet **Synkroniser bare koblede poster** i integrasjonstabellen som brukes av synkroniseringsjobben. På slutten av den fullstendige synkroniseringsprosessen blir du spurt om du vil beholde dette alternativet fjernet for alle jobbene.  

* Koblet er synkroniseringsretningen (for eksempel fra [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[prod_short](includes/cds_long_md.md)] eller fra [!INCLUDE[prod_short](includes/cds_long_md.md)] til [!INCLUDE[prod_short](includes/prod_short.md)]) forhåndsbestemt av integrasjonstabelltilordningene. Hvis du vil ha mer informasjon, kan du se [Standard tabelltilordning for synkronisering](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).  

> [!IMPORTANT]  
>  Du bruker vanligvis bare fullstendig synkronisering første gang du definerer integrasjon mellom [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)] og bare én av løsningene inneholder data, som du vil kopiere til den andre løsningen. En fullstendig synkronisering kan være nyttige i et demonstrasjonsmiljø. Siden fullstendig synkronisering automatisk oppretter og kobler poster mellom løsninger, er det raskere å begynne å arbeide med synkronisering av data mellom poster. Derimot må du bare utføre en full synkronisering hvis du vil ha en rad i [!INCLUDE[prod_short](includes/prod_short.md)] for hver rad i [!INCLUDE[prod_short](includes/cds_long_md.md)] for de gitte tabelltilordningene. Hvis ikke kan det oppstå uønskede eller dupliserte poster i [!INCLUDE[prod_short](includes/prod_short.md)] eller [!INCLUDE[prod_short](includes/cds_long_md.md)].  

### Kjøre en full synkronisering  
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Dataverse-tilkoblingsoppsett** og velger den relaterte koblingen.

    > [!NOTE]
    > Hvis du vil kjøre en fullstendig synkronisering for tabeller via Dynamics 365 Sales, bruker du i stedet siden **Tilkoblingsoppsett for Microsoft Dynamics 365 Sales**.

2.  Velg handlingen **Kjør full synkronisering**, og velg deretter **Ja**-knappen.  
3.  Når full synkronisering er fullført, kan du angi om du vil at planlagte synkroniseringsjobber skal kunne opprette nye poster.  

    Hvis du vil at alle synkroniseringsjobber skal kunne opprette nye poster i målet for ukoblede poster i kilden, velger du **Ja**. Dette angir feltet **Synkroniser bare koblede poster** på tabelltilordningene som brukes av synkroniseringsjobbene.  

    Hvis du vil at synkroniseringsjobber skal kjøres som før den fullstendige synkroniseringen med hensyn til å opprette nye poster, velger du **Nei**. Dette setter feltet **Synkroniser bare koblede poster** til innstillingen det hadde før fullstendig synkronisering.  

Du kan se resultatet av den fullstendige synkroniseringen på siden **Synkroniseringsjobber for integrering**. Hvis du vil ha mer informasjon, kan du se [Vise statusen for en synkronisering](admin-how-to-view-synchronization-status.md).  

## Synkronisere alle endrede poster
Du kan bruke siden **Tilkoblingsoppsett for Common Data Service** til å synkronisere endringer i data i alle integrasjonstabelltilordninger. Dette ligner på en fullstendig synkronisering. Det synkroniseres data i alle koblede poster i [!INCLUDE[prod_short](includes/prod_short.md)]-tabellene og [!INCLUDE[prod_short](includes/cds_long_md.md)]-tabellene som er definert i tabelltilordningene. Som standard synkroniseres bare data som har blitt endret siden forrige synkronisert. Synkroniseringsjobber synkroniserer tabelltilordninger i følgende rekkefølgen for å unngå å koble avhengigheter mellom tabellene:  

1.  CURRENCY  
2.  SELGERE  
3.  VENDOR  
4.  CUSTOMER  
5.  KONTAKTER  

Du kan se resultatet av synkroniseringen på siden **Synkroniseringsjobber for integrering**. Hvis du vil ha mer informasjon, kan du se [Vise statusen for en synkronisering](admin-how-to-view-synchronization-status.md).  

> [!TIP]  
>  Når du endrer integreringstabelltilordningen på forhånd, kan du opprette filtre til å styre dataene som skal sunkroniseres, eller konfigurere tilordninger for å opprette nye data i målløsningen for ukoblede poster eller rader i kilden. Hvis du vil ha mer informasjon, se [Endre tabelltilordningene for synkronisering](admin-how-to-modify-table-mappings-for-synchronization.md).

### Synkronisere data for alle tabeller  
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Microsoft Dynamics 365 Sales-tilkoblingsoppsett** og velger den relaterte koblingen.
2.  Velg **Synkroniser endrede poster**-handlingen, og velg deretter **Ja**.  

## Synkronisere individuelle tabelltilordninger
Du kan bruke siden **Tilordninger for integreringstabell** til å kjøre en synkroniseringsjobb for tabelltilordninger. Dette synkroniserer data for alle koblede poster og rader i [!INCLUDE[prod_short](includes/prod_short.md)]- og [!INCLUDE[prod_short](includes/cds_long_md.md)]-tabellene som er definert av tabelltilordningen. Som standard synkroniseres bare data som har blitt endret siden forrige synkronisert.  

### Synkronisere poster i en integrasjonstabelltilordning  
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Tilordninger for integreringstabell**, og velg deretter den relaterte koblingen.
2.  Velg **Synkroniser endrede poster**-handlingen, og velg deretter **Ja**.  

## Se også  
[Synkronisere Business Central og Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)   
[Sette opp brukerkontoer for integrasjon med Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]