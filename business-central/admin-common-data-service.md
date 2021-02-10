---
title: Bruke Microsoft Dataverse
description: Innføring i Microsoft Dataverse og tilhørende komponenter.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 10/01/2020
ms.openlocfilehash: 1d740cf645739e89dddc9173583eb5fa639f6be6
ms.sourcegitcommit: edac6cbb8b19ac426f8dcbc83f0f9e308fb0d45d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/29/2020
ms.locfileid: "4817107"
---
# <a name="integrating-with-microsoft-dataverse"></a>Integrere med Microsoft Dataverse
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Forretningsapper bruker ofte data fra mer enn én kilde. [!INCLUDE[prod_short](includes/cds_long_md.md)] kombinerer data til et logisk sett som gjør det enklere å koble andre Dynamics 365-apper, for eksempel [!INCLUDE[crm_md](includes/crm_md.md)] eller din egen app som er bygget på toppen av [!INCLUDE[prod_short](includes/cds_long_md.md)], til [!INCLUDE[prod_short_md](includes/prod_short.md)]. Hvis du vil ha mer informasjon om [!INCLUDE[prod_short](includes/cds_long_md.md)], kan du se [Hva er Dataverse?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)

Følgende fremgangsmåte gir en oversikt over hvordan du integrerer [!INCLUDE[prod_short](includes/cds_long_md.md)] med [!INCLUDE[prod_short](includes/prod_short.md)].

> [!Note]  
> Disse oppgavene krever **Systemansvarlig**-sikkerhetsrolle i [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Tilordne lisenser for [!INCLUDE[prod_short](includes/cds_long_md.md)] til [!INCLUDE[prod_short](includes/prod_short.md)]-brukere som skal bruke de integrerte appene.

2. Konfigurere en tilkobling til [!INCLUDE[prod_short](includes/cds_long_md.md)] Hvis du vil ha mer informasjon, kan du se [Koble til Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Synkronisere data mellom apper. Hvis du vil ha mer informasjon, kan du se [Synkronisere Business Central og Dataverse](admin-synchronizing-business-central-and-sales.md). 

## <a name="getting-started-with-prod_short"></a>Komme i gang med [!INCLUDE[prod_short](includes/cds_long_md.md)]
Hvis du vil komme i gang med [!INCLUDE[prod_short](includes/cds_long_md.md)], trenger du en Microsoft Power Apps-konto. Hvis du ikke allerede har en Power Apps-konto, kan du få en kostnadsfritt ved å gå til [powerapps.com](https://make.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) og klikke koblingen **Komme i gang vederlagsfritt**. Hvis du vil ha mer informasjon om hvordan du kommer i gang med [!INCLUDE[prod_short](includes/cds_long_md.md)], kan du se modulen [Kom i gang med Dataverse](https://docs.microsoft.com/learn/modules/get-started-with-powerapps-common-data-service/) fra Microsoft Learn.

## <a name="bi-directional-or-uni-directional-data-synchronization"></a>Toveis eller enveis datasynkronisering
Avhengig av forretningsbehovene kan du konfigurere integreringen til å synkronisere data til eller fra én Dynamics 365-forretningsapp til en annen, eller i begge retninger i nær sanntid via [!INCLUDE[prod_short](includes/cds_long_md.md)]. Hvis du for eksempel integrerer [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE[crm_md](includes/crm_md.md)] via [!INCLUDE[prod_short](includes/cds_long_md.md)], kan en selger opprette en salgsordre i [!INCLUDE[crm_md](includes/crm_md.md)], og ordren vil bli synkronisert til [!INCLUDE[prod_short](includes/prod_short.md)]. I [!INCLUDE[crm_md](includes/crm_md.md)] kan selgeren i motsetning vise informasjon fra [!INCLUDE[prod_short](includes/prod_short.md)] om tilgjengeligheten av varen i ordren. 

## <a name="standard-and-custom-entities"></a>Standard og egendefinerteenheter
[!INCLUDE[prod_short](includes/cds_long_md.md)] lagrer data på en sikker måte i et sett med tabeller. Dette er sett med poster som ligner på hvordan en tabell lagrer data i en database. [!INCLUDE[prod_short](includes/cds_long_md.md)] inneholder et grunnleggende sett med standardtabeller som dekker vanlige scenarier, men du kan også opprette egendefinerte tabeller som er spesifikke for organisasjonen. I [!INCLUDE[prod_short](includes/prod_short.md)] kan du vise standard og egendefinerte tabeller som synkroniseres på siden Tilordninger for integreringstabell.

## <a name="about-the-business-central-base-integration-solution"></a>Om den grunnleggende integreringsløsningen for Business Central

Den grunnleggende integreringsløsningen er en viktig del av integreringen. Løsningen legger til nødvendige roller og tilgangsnivåer for brukerkontoene for integreringen, og det opprettes tabeller som kreves for å tilordne [!INCLUDE[prod_short](includes/prod_short.md)]-firmaer til konsernet i [!INCLUDE[prod_short](includes/cds_long_md.md)]. 

Som standard vil den assisterte oppsettsveiledningen **Konfigurer [!INCLUDE[prod_short](includes/cds_long_md.md)]-tilkobling** importere løsningen. For å gjøre dette bruker oppsettveiledningen en administratorbrukerkonto du angir. Denne kontoen må være en gyldig bruker i [!INCLUDE[prod_short](includes/cds_long_md.md)] med følgende sikkerhetsrolle:

* Systemansvarlig  

Hvis du vil ha mer informasjon, kan du se [Konfigurere brukerkontoer for integrering med [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) og [Opprette brukere i Microsoft Dynamics 365 (online) og tilordne sikkerhetsroller.](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles). 

Administratorkontoen brukes bare én gang i oppsettet for konfigurasjonsendringene som den grunnleggende integreringsløsningen gjør i [!INCLUDE[prod_short](includes/cds_long_md.md)]. Når løsningen er importert, er kontoen ikke lenger nødvendig. Integrasjonen fortsetter å bruke brukerkontoen som automatisk er opprettet spesielt for integrasjonen.

I tillegg til å tilpasse [!INCLUDE[prod_short](includes/cds_long_md.md)], oppretter løsningen også følgende roller i [!INCLUDE[prod_short](includes/cds_long_md.md)] for integreringen:

* **Integrasjonsadministrator** - Gjør at brukere kan administrere forbindelsen mellom [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)]. Vanligvis bare dette bare tilordnet til den automatisk opprettede brukerkontoen for synkronisering.  
* **Integrasjonsbruker** - Gjør at brukere får tilgang til synkroniserte data. Normalt tilordnes dette til den automatisk opprettede brukerkontoen for synkronisering og andre brukere som har behov for å vise eller få tilgang til de synkroniserte dataene.

Hvis du vil ha detaljert informasjon om hver rolle, for eksempel tillatelsene og tilgangsnivåene, kan du se [Sette opp brukerkontoer for integrasjon med [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Under tilkoblingsoppsettet opprettes integreringstabelltilordninger som er nødvendige for å synkronisere data. Enheter i [!INCLUDE[prod_short](includes/cds_long_md.md)] blir tilordnet til tabeller og tabell felt i Business Central via integreringstabeller. Hvis du vil ha mer informasjon, kan du se [Standard enhetstilordning for synkronisering](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

## <a name="see-also"></a>Se også
[Dataeierskapsmodeller](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Dataverse](\dynamics365\business-central\dev-itpro\administration\administration-custom-cds-integration) -->



