---
title: Integrere med Dynamics 365 Sales | Microsoft Docs
description: Lær hvordan du klargjør Dynamics 365 Business Central for integrering med Dynamics 365 Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 9f56e96b86fb7462799c9a9c655010ee2fb04381
ms.sourcegitcommit: cd5d3d288feee76d058d325720135275f4c8ad85
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/08/2019
ms.locfileid: "2775310"
---
# <a name="integrating-with-dynamics-365-sales"></a>Integrere med Dynamics 365 Sales.
Selgerrollen regnes ofte som den mest synlige jobben i et konsern. Det kan imidlertid være nyttig for selgere å kunne se innover i konsernet, og se hva som skjer internt. Ved å integrere [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] kan du gi selgerne innsikt ved at de kan se informasjon i [!INCLUDE[d365fin](includes/d365fin_md.md)] når de arbeider i [!INCLUDE[crm_md](includes/crm_md.md)]. For eksempel, når du forbereder et tilbud, kan det være nyttig å vite om du har tilstrekkelig lagerbeholdning til å oppfylle ordren. Hvis du vil ha mer informasjon, kan du se [Bruke Dynamics 365 Sales fra Business Central](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> Denne fremgangsmåten beskriver hvordan du integrerer elektroniske versjoner av [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du vil ha informasjon om lokal konfigurasjon, kan du se [Klargjøre Dynamics 365 Sales for lokal integrasjon](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

<!--## Software Requirements
You must have an Office 365 subscription, and both [!INCLUDE[crm_md](includes/crm_md.md)] and [!INCLUDE[d365fin](includes/d365fin_md.md)] must be part of the same organization.  -->

## <a name="overview-of-the-integration-process"></a>Oversikt over integrasjonsprosessen
Følgende fremgangsmåte gir en oversikt over hvordan du integrerer [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!Note]  
> Disse oppgavene krever **Systemansvarlig**-sikkerhetsrolle i [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1. I administrasjonssenteret for Office 365 definerer du en brukerkonto for tilkobling til og synkronisering av data med [!INCLUDE[crm_md](includes/crm_md.md)]. Hvis du vil ha mer informasjon, kan du se [Sette opp brukerkontoer for integrasjon med Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).

2. Tilordne lisenser for [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)]-brukere som skal bruke de integrerte appene.

3. Konfigurere en tilkobling til [!INCLUDE[crm_md](includes/crm_md.md)] Hvis du vil ha mer informasjon, kan du se [Konfigurere en kobling til Dynamics 365 Sales](admin-how-to-set-up-a-dynamics-crm-connection.md).  

4. Valgfritt: Koble [!INCLUDE[d365fin](includes/d365fin_md.md)]- og [!INCLUDE[crm_md](includes/crm_md.md)]-poster. Hvis du vil ha mer informasjon, se [Sammenkoble og synkronisere poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md).

5. Synkronisere data mellom apper. Hvis du vil ha mer informasjon, kan du se [Synkronisere Business Central og Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md).  

## <a name="about-the-business-central-integration-solution"></a>Om Business Central-integrasjonsløsningen
Løsningen lar personer vise informasjon i [!INCLUDE[d365fin](includes/d365fin_md.md)] når de arbeider i [!INCLUDE[crm_md](includes/crm_md.md)]. Det kan for eksempel gi innsikt i kundestatistikk, lar brukere koble og vise poster i [!INCLUDE[d365fin](includes/d365fin_md.md)] fra [!INCLUDE[crm_md](includes/crm_md.md)] og gjør det mulig å se om produktene er tilgjengelige i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Som standard importerer assistert oppsettsveiledning for **Tilkoblingsoppsett for Dynamics 365 Sales** [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrasjonsløsningen. For å gjøre dette bruker oppsettveiledningen en administratorbrukerkonto. Denne kontoen må også være en gyldig bruker i [!INCLUDE[crm_md](includes/crm_md.md)] med følgende sikkerhetsroller:

* Systemansvarlig  
* Løsningstilpasser  

Hvis du vil ha mer informasjon, se [Sette opp brukerkontoer for integrasjon med Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md), [Opprette brukere i Microsoft Dynamics 365 (online) og tilordne sikkerhetsroller](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles) og [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md).  

Denne kontoen brukes bare én gang under oppsettet. Når løsningen er importert til [!INCLUDE[d365fin](includes/d365fin_md.md)], er kontoen ikke lenger nødvendig. Integrasjonen fortsetter å bruke brukerkontoen som er opprettet spesielt for integrasjonen.

I tillegg til å tilpasse [!INCLUDE[crm_md](includes/crm_md.md)], oppretter [!INCLUDE[d365fin](includes/d365fin_md.md)]-integreringsløsningen også følgende roller i [!INCLUDE[crm_md](includes/crm_md.md)] for integreringen:

* **Integrasjonsadministrator** - Gjør at brukere kan administrere forbindelsen mellom [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)]. Vanligvis bare tilordnet til brukerkontoen for synkronisering.  
* **Integrasjonsbruker** - Gjør at brukere får tilgang til synkroniserte data. Normalt tilordnet brukerkontoen for synkronisering og andre brukere som har behov for å vise eller få tilgang til de synkroniserte dataene.
* **Produkttilgjengelighetsbruker** - Gjør at brukere kan spørre etter produkttilgjengelig i [!INCLUDE[d365fin](includes/d365fin_md.md)] fra [!INCLUDE[crm_md](includes/crm_md.md)].

Hvis du vil ha detaljert informasjon om hver rolle, for eksempel tillatelsene og tilgangsnivåene, kan du se [Sette opp brukerkontoer for integrasjon med Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).

Nederst i oppsettveiledningen ber [!INCLUDE[d365fin](includes/d365fin_md.md)] deg om å koble selgere til brukere i [!INCLUDE[crm_md](includes/crm_md.md)]. Poster i [!INCLUDE[crm_md](includes/crm_md.md)] har vanligvis en eier (bruker) som er tilordnet dem, og hvis koblingen mellom brukeren i [!INCLUDE[crm_md](includes/crm_md.md)] og selgeren i [!INCLUDE[d365fin](includes/d365fin_md.md)] ikke finnes, vil synkroniseringen mislykkes. Du kan også gjøre dette senere ved hjelp av handlingen **Koble selgere** på siden **Tilkoblingsoppsett for Microsoft Dynamics 365**.

## <a name="see-also"></a>Se også  
[Sette opp brukerkontoer for integrasjon med Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Konfigurere en kobling til Dynamics 365 Sales](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Synkronisere Business Central og Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)  
[Klargjøre Dynamics 365 Sales for lokal integrasjon](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).
