---
title: Innføring i Microsoft Fabric og Business Central
description: 'Få en oversikt over hvordan du bruker Microsoft Fabric til å få innsikt, forretningsanalyse og KPI-er fra Business Central-data.'
author: kennienp
ms.topic: overview
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.search.form: '6316, 6317'
ms.reviewer: bholtorf
ms.date: 04/24/2024
ms.author: kepontop
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Innføring i Microsoft Fabric og Business Central

[!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] er en komplett analyseløsning med fullservicefunksjoner, inkludert dataflytting, datasjøer, datateknikk, dataintegrering, datavitenskap, sanntidsanalyse og forretningsanalyse – alt støttet av en delt plattform som gir robust datasikkerhet, -styring og -samsvar. Organisasjonen trenger ikke lenger å sy sammen individuelle analysetjenester fra flere leverandører. Bruk i stedet en effektivisert løsning som er enkel å koble til, innføre og bruke.

> [!NOTE]
> Hvis du vil ha mer informasjon om lanseringsplanen for Microsoft Fabric, kan du se [aka.ms/FabricRoadmap](https://aka.ms/FabricRoadmap)
> 
> Den regelmessige publiseringen av dette veikartet vil hjelpe deg med å holde deg informert om hvordan [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] vil dekke dine behov.

## Hvor passer [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] inn i [!INCLUDE[prod_short](includes/prod_short.md)]-analyse

[!INCLUDE[prod_short](includes/prod_short.md)] leveres med mange bruksklare rapporter og dataanalysefunksjoner, for eksempel finansrapportering, åpne i Excel og analysemodus for lister og spørringer. På toppen av dette er det enkelt å definere Power BI-rapporter som leser data fra standard og tilpassede API-er, definere målstyringer for Power BI-måleverdier og bygge inn alle disse direkte i [!INCLUDE[prod_short](includes/prod_short.md)]-klienten. Men for kunder med mer avanserte datavitenskaps- eller forretningsanalysescenarioer som krever rikere datateknikk eller dataintegrering, kan [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] være et godt alternativ. 

## OneLake

En viktig del av [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)]-tilbudet er OneLake. OneLake er en enkelt, enhetlig, logisk datasjø for hele organisasjonen. Du kan se på OneLake som OneDrive for data. Det gir deg datasjø som en tjeneste uten å måtte bygge den selv. OneLake leveres automatisk med alle [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)]-leietakere uten infrastruktur å administrere. Alle dataene, som lander i OneLake, deltar automatisk i standard datastyring som dataavstamming, databeskyttelse, sertifisering og katalogintegrering. Den bryter ned datasiloer ved å gjøre det mulig for ulike deler av organisasjonen å jobbe uavhengig samtidig som de bidrar til den samme datasjøen.

[!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)]-elementer lagrer dataene dine i OneLake i et åpent filformat. For strukturerte tabelldata er dette formatet *delta parquet*. Delta parquet-format gir alle analysemotorer i [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] tilgang til dataene fra andre analysemotorer. På denne måten gir det fleksibilitet for datautøvere til å bruke verktøyene de ønsker.


## Se også
[Bruk Power BI med Business Central](admin-powerbi.md)   

[!INCLUDE[footer-include](includes/footer-banner.md)]
