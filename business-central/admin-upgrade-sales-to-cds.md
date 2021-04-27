---
title: Oppgradere en integrasjon med Dynamics 365 Sales
description: Lær hvordan du kan flytte Dynamics 365 Business Central-integrasjonen med Dynamics 365 Sales til den nyeste versjonen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 4e3b79d6245a0f1b8277c94faa58c24edc66662e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777019"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a>Oppgradere en integrasjon med Dynamics 365 Sales
[!INCLUDE[prod_short](includes/prod_short.md)] kan integreres med [!INCLUDE[prod_short](includes/cds_long_md.md)], som gjør det enkelt å koble til og synkronisere data med andre Dynamics 365-apper, for eksempel [!INCLUDE[crm_md](includes/crm_md.md)] eller til og med apper du lager selv. Hvis du integrerer for første gang, anbefales det at du gjør det via [!INCLUDE[prod_short](includes/cds_long_md.md)]. Hvis du vil ha mer informasjon, kan du se [Integrasjon med Dataverse](admin-common-data-service.md).

Hvis du allerede har integrert [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[prod_short](includes/prod_short.md)], kan du fortsette å synkronisere data ved hjelp av konfigurasjonen. Hvis du imidlertid oppgraderer [!INCLUDE[prod_short](includes/prod_short.md)] eller slår av [!INCLUDE[crm_md](includes/crm_md.md)]-integreringen, må du slå den på igjen ved å koble til via [!INCLUDE[prod_short](includes/cds_long_md.md)]. 

> [!NOTE]
> Når du kobler til på nytt via [!INCLUDE[prod_short](includes/cds_long_md.md)], brukes standard synkroniseringsinnstillinger, og eventuelle konfigurasjoner blir overskrevet. Standard tabelltilordninger vil for eksempel bli brukt.

## <a name="to-upgrade-your-connection-to-use-dataverse"></a>Slik oppgraderer du tilkoblingen for å bruke Dataverse
1. Åpne siden **Tilkoblingsoppsett for Microsoft Dynamics 365**, og deaktiver vekslebryteren **Aktivert** for å koble fra [!INCLUDE[crm_md](includes/crm_md.md)].
2. Åpne siden **Tilkoblingsoppsett for Dataverse** og velg **Aktivert** for å aktivere tilkoblingen til [!INCLUDE[prod_short](includes/cds_long_md.md)].
  
   > [!NOTE]
   > Når du har aktivert tilkoblingen, er Business Central-integreringsløsningen distribuert til Dataverse.
3. Velg **Distribuer integreringsløsning på nytt** for å installere Business Central-integreringsløsningen på nytt.
4. Åpne siden **Konfigurasjon for Microsoft Dynamics 365-tilkobling**, og aktiver veksleknappen **Aktivert** for å koble til [!INCLUDE[crm_md](includes/crm_md.md)] på nytt.
  
   > [!NOTE]
   > Når du har aktivert tilkoblingen, er Business Central-integreringsløsningen distribuert til [!INCLUDE[prod_short](includes/prod_short.md)]. Dette gjør det mulig å integrere med tabeller som er spesifikke for [!INCLUDE[crm_md](includes/crm_md.md)], for eksempel ordrer, tilbud og fakturaer.
5. Velg **Distribuer integreringsløsning på nytt** for å installere Business Central-integreringsløsningen på nytt.
6. På siden **Tilkoblingsoppsett for Sales** velger du **Bruk standard synkroniseringsoppsett** til å initialisere integrasjonstabelltilordninger for [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Se også
[Integrere med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Integrere med Microsoft Dataverse](admin-common-data-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]