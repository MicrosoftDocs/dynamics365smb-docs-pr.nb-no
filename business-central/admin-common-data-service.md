---
title: Bruke Common Data Service
description: Innføring i Common Data Service og tilhørende komponenter.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 10/01/2020
ms.openlocfilehash: 85823e93b1d239bf4e59ec6a8872cdc4a2cef9c1
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911583"
---
# <a name="integrating-with-common-data-service"></a>Integrere med Common Data Service

Forretningsapper bruker ofte data fra mer enn én kilde. [!INCLUDE[d365fin](includes/cds_long_md.md)] kombinerer data til et logisk sett som gjør det enklere å koble andre Dynamics 365-apper, for eksempel [!INCLUDE[crm_md](includes/crm_md.md)] eller din egen app som er bygget på toppen av [!INCLUDE[d365fin](includes/cds_long_md.md)], til [!INCLUDE[d365fin_md](includes/d365fin_md.md)]. Hvis du vil ha mer informasjon om [!INCLUDE[d365fin](includes/cds_long_md.md)], kan du se [Hva er Common Data Service?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)

Følgende fremgangsmåte gir en oversikt over hvordan du integrerer [!INCLUDE[d365fin](includes/cds_long_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!Note]  
> Disse oppgavene krever **Systemansvarlig**-sikkerhetsrolle i [!INCLUDE[d365fin](includes/cds_long_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1. Tilordne lisenser for [!INCLUDE[d365fin](includes/cds_long_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)]-brukere som skal bruke de integrerte appene.

2. Konfigurere en tilkobling til [!INCLUDE[d365fin](includes/cds_long_md.md)] Hvis du vil ha mer informasjon, kan du se [Koble til Common Data Service](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Synkronisere data mellom apper. Hvis du vil ha mer informasjon, kan du se [Synkronisere Business Central og Common Data Service](admin-synchronizing-business-central-and-sales.md). 

## <a name="getting-started-with-d365fin"></a>Komme i gang med [!INCLUDE[d365fin](includes/cds_long_md.md)]
Hvis du vil komme i gang med [!INCLUDE[d365fin](includes/cds_long_md.md)], trenger du en Microsoft Power Apps-konto. Hvis du ikke allerede har en Power Apps-konto, kan du få en kostnadsfritt ved å gå til [powerapps.com](https://web.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) og klikke koblingen **Komme i gang vederlagsfritt**. Hvis du vil ha mer informasjon om hvordan du kommer i gang med [!INCLUDE[d365fin](includes/cds_long_md.md)], kan du se modulen [Kom i gang med Common Data Service](https://docs.microsoft.com/learn/modules/get-started-with-powerapps-common-data-service/) i Microsft Learn.

## <a name="bi-directional-or-uni-directional-data-synchronization"></a>Toveis eller enveis datasynkronisering
Avhengig av forretningsbehovene kan du konfigurere integreringen til å synkronisere data til eller fra én Dynamics 365-forretningsapp til en annen, eller i begge retninger i nær sanntid via [!INCLUDE[d365fin](includes/cds_long_md.md)]. Hvis du for eksempel integrerer [!INCLUDE[d365fin](includes/d365fin_md.md)] med [!INCLUDE[crm_md](includes/crm_md.md)] via [!INCLUDE[d365fin](includes/cds_long_md.md)], kan en selger opprette en salgsordre i [!INCLUDE[crm_md](includes/crm_md.md)], og ordren vil bli synkronisert til [!INCLUDE[d365fin](includes/d365fin_md.md)]. I [!INCLUDE[crm_md](includes/crm_md.md)] kan selgeren i motsetning vise informasjon fra [!INCLUDE[d365fin](includes/d365fin_md.md)] om tilgjengeligheten av varen i ordren. 

## <a name="standard-and-custom-entities"></a>Standard og egendefinerteenheter
[!INCLUDE[d365fin](includes/cds_long_md.md)] lagrer data på en sikker måte i et sett med enheter. Dette er sett med poster som ligner på hvordan en tabell lagrer data i en database. [!INCLUDE[d365fin](includes/cds_long_md.md)] inneholder et grunnleggende sett med standardenheter som dekker vanlige scenarier, men du kan også opprette egendefinerte enheter som er spesifikke for organisasjonen. I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du vise standard og egendefinerte enheter som synkroniseres på siden Tilordninger for integreringstabell.

## <a name="about-the-base-cds-integration-solution"></a>Om den grunnleggende løsningen for CDS-integrering

Den grunnleggende løsningen for CDS-integrering er en viktig del av integreringen. Løsningen legger til nødvendige roller og tilgangsnivåer for brukerkontoene for integreringen, og det opprettes enheter som kreves for å tilordne [!INCLUDE[d365fin](includes/d365fin_md.md)]-firmaer til konsernet i [!INCLUDE[d365fin](includes/cds_long_md.md)]. 

Som standard vil den assisterte oppsettsveiledningen **Konfigurer [!INCLUDE[d365fin](includes/cds_long_md.md)]-tilkobling** importere løsningen. For å gjøre dette bruker oppsettveiledningen en administratorbrukerkonto du angir. Denne kontoen må være en gyldig bruker i [!INCLUDE[d365fin](includes/cds_long_md.md)] med følgende sikkerhetsrolle:

* Systemansvarlig  

Hvis du vil ha mer informasjon, kan du se [Konfigurere brukerkontoer for integrering med [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) og [Opprette brukere i Microsoft Dynamics 365 (online) og tilordne sikkerhetsroller.](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles). 

Administratorkontoen brukes bare én gang i oppsettet på grunn av konfigurasjonsendringer som den grunnleggende CDS-løsningen gjør i [!INCLUDE[d365fin](includes/cds_long_md.md)]. Når løsningen er importert, er kontoen ikke lenger nødvendig. Integrasjonen fortsetter å bruke brukerkontoen som automatisk er opprettet spesielt for integrasjonen.

I tillegg til å tilpasse [!INCLUDE[d365fin](includes/cds_long_md.md)], oppretter løsningen også følgende roller i [!INCLUDE[d365fin](includes/cds_long_md.md)] for integreringen:

* **Integrasjonsadministrator** - Gjør at brukere kan administrere forbindelsen mellom [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)]. Vanligvis bare dette bare tilordnet til den automatisk opprettede brukerkontoen for synkronisering.  
* **Integrasjonsbruker** - Gjør at brukere får tilgang til synkroniserte data. Normalt tilordnes dette til den automatisk opprettede brukerkontoen for synkronisering og andre brukere som har behov for å vise eller få tilgang til de synkroniserte dataene.

Hvis du vil ha detaljert informasjon om hver rolle, for eksempel tillatelsene og tilgangsnivåene, kan du se [Sette opp brukerkontoer for integrasjon med [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Under tilkoblingsoppsettet opprettes integreringstabelltilordninger som er nødvendige for å synkronisere data. Enheter i Common Data Service blir tilordnet til tabeller og tabell felt i Business Central via integreringstabeller. Hvis du vil ha mer informasjon, kan du se [Standard enhetstilordning for synkronisering](admin-synchronizing-business-central-and-sales.md#standard-entity-mapping-for-synchronization).

## <a name="see-also"></a>Se også
[Dataeierskapsmodeller](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Common Data Service](docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/administration-custom-cds-integration) -->



