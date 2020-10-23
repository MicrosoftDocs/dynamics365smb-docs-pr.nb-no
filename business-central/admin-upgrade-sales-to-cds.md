---
title: Oppgradere en integrasjon med Dynamics 365 Sales
description: Lær hvordan du kan flytte Dynamics 365 Business Central-integrasjonen med Dynamics 365 Sales til den nyeste versjonen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 3bb6b26e011afc515fbd4f492f56b3090c56e860
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922370"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a>Oppgradere en integrasjon med Dynamics 365 Sales
[!INCLUDE[d365fin](includes/d365fin_md.md)] kan integreres med [!INCLUDE[d365fin](includes/cds_long_md.md)], som gjør det enkelt å koble til og synkronisere data med andre Dynamics 365-apper, for eksempel [!INCLUDE[crm_md](includes/crm_md.md)] eller til og med apper du lager selv. Hvis du integrerer for første gang, anbefales det at du gjør det via [!INCLUDE[d365fin](includes/cds_long_md.md)]. Hvis du vil ha mer informasjon, kan du se [Integrasjon med Common Data Service](admin-common-data-service.md).

Hvis du allerede har integrert [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du fortsette å synkronisere data ved hjelp av konfigurasjonen. Hvis du imidlertid oppgraderer [!INCLUDE[d365fin](includes/d365fin_md.md)] eller slår av [!INCLUDE[crm_md](includes/crm_md.md)]-integreringen, må du slå den på igjen ved å koble til via [!INCLUDE[d365fin](includes/cds_long_md.md)]. 

> [!NOTE]
> Når du kobler til på nytt via [!INCLUDE[d365fin](includes/cds_long_md.md)], brukes standard synkroniseringsinnstillinger, og eventuelle konfigurasjoner blir overskrevet. Standard tabelltilordninger vil for eksempel bli brukt.

## <a name="to-upgrade-your-connection-to-use-common-data-service"></a>Slik oppgraderer du tilkoblingen for å bruke Common Data Service
1. Åpne siden **Konfigurere Microsoft Dynamics 365-tilkobling** og velg **Aktiver** for å slå av den eksisterende tilkoblingen til [!INCLUDE[crm_md](includes/crm_md.md)].
2. Åpne siden **Tilkoblingsoppsett for Common Data Service** og velg **Aktiver** for å slå på tilkoblingen.
  
   Når du har aktivert CDS-tilkoblingen, er den grunnleggende løsningen for CDS-integrering for Business Central distribuert til Common Data Service.
3. Avinstaller løsningen for integrering av Microsoft Dynamics 365 Business Central fra Dynamics 365 Sales. Hvis du vil ha mer informasjon, kan du se [emnet om å avinstallere eller slette en løsning](/powerapps/developer/common-data-service/uninstall-delete-solution). 

4. Åpne siden **Konfigurasjon for Microsoft Dynamics 365-tilkobling**, og aktiver veksleknappen **Aktiver** for å koble til [!INCLUDE[crm_md](includes/crm_md.md)].
  
   Når du har aktivert Sales-tilkoblingen, er løsningen for Business Central-integrasjon distribuert til Sales. Dette gjør det mulig å integrere med enheter som er spesifikke for [!INCLUDE[crm_md](includes/crm_md.md)], for eksempel ordrer, tilbud og fakturaer.
5. På siden **Tilkoblingsoppsett for Sales** velger du **Bruk standard synkroniseringsoppsett** til å initialisere integrasjonstabelltilordninger for [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Se også
[Integrere med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Integrere med Common Data Service](admin-common-data-service.md)
