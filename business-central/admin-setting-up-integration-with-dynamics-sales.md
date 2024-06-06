---
title: Sette opp brukerkontoer for integrasjon med Microsoft Dataverse | Microsoft Docs
description: 'Lær hvordan du definerer brukerkontoene som appene bruker til å utveksle data, og som brukes til å få tilgang til og synkronisere data i appene.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 01/12/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="setting-up-user-accounts-for-integrating-with-microsoft-dataverse-via-data-sync"></a>Sette opp brukerkontoer for integrasjon med Microsoft Dataverse via datasynkronisering

Denne artikkelen gir en oversikt over hvordan du definerer brukerkontoene som er nødvendige for å integrere [!INCLUDE[prod_short](includes/cds_long_md.md)] med [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="set-up-the-administrator-user-account"></a>Sette opp administratorbrukerkontoen

Når du skal definere tilkoblingen mellom [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)], må du logge deg på [!INCLUDE[prod_short](includes/prod_short.md)] med en brukerkonto som er tildelt lisensen [!INCLUDE[prod_short](includes/prod_short.md)] Essential eller [!INCLUDE[prod_short](includes/prod_short.md)] Premium. Vi bruker denne kontoen én gang til å installere og konfigurere noen nødvendige komponenter.

> [!IMPORTANT]
> Under installasjonen blir du bedt om å oppgi legitimasjon for [!INCLUDE[prod_short](includes/cds_long_md.md)]-miljøet. Oppgi legitimasjonen for en konto som er en lisensiert bruker og tildelt til sikkerhetsrollen **Systemadministrator** i [!INCLUDE[prod_short](includes/cds_long_md.md)]-miljøet og den globale administratoren for leieren som miljøet tilhører. Denne kontoen trenger ikke lisens for [!INCLUDE[prod_short](includes/prod_short.md)] fordi den bare skal brukes til å gjøre installasjonsoppgaver i [!INCLUDE[prod_short](includes/cds_long_md.md)]-miljøet.
>
> Når tilkoblingsoppsettet er fullført, kan du fjerne denne [!INCLUDE[prod_short](includes/cds_long_md.md)]-brukeren. Integrasjonen fortsetter å bruke brukerkontoen som automatisk er opprettet spesielt for integrasjonen.

## <a name="permissions-and-security-roles-for-user-accounts-in-"></a>Tillatelser og sikkerhetsroller for brukerkontoer i [!INCLUDE[prod_short](includes/cds_long_md.md)]

Baseintegrasjonsløsningen oppretter følgende rolle i [!INCLUDE [cds_long_md](includes/cds_long_md.md)] for integreringen:

* **Business Central Dataverse-integrering** – lar deg administrere tilkoblingen mellom [!INCLUDE [prod_short](includes/prod_short.md)] og [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Vanligvis bare dette bare tilordnet til den automatisk opprettede brukerkontoen for synkronisering.

> [!NOTE]
> Bare programbrukeren som kjører integreringen, skal ha rollen **Business Central Dataverse-integrering**. Programbrukeren trenger ikke lisensene [!INCLUDE [prod_short](includes/prod_short.md)] eller [!INCLUDE [cds_long_md](includes/cds_long_md.md)].

Når du installerer den grunnleggende løsningen, konfigurerer den tillatelser for integrasjonsbrukerkontoen. Hvis disse tillatelsene endres manuelt, kan du tilbakestille dem. Velg siden **Distribuer integreringsløsning på nytt** på siden **Dataverse-tilkoblingsoppsett** for å installere baseintegreringsløsningen på nytt. Dette trinnet distribuerer sikkerhetsrollen Business Central-integrasjon.

<!--
The following tables list the minimum permissions for the user accounts in [!INCLUDE[prod_short](includes/cds_long_md.md)].

### <a name="minimum-permissions-for-the-administrator"></a>Minimum Permissions for the Administrator
The following table displays the minimum permissions on each tab for each security role that is required for the administrator user.

##### <a name="customization"></a>Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Model Driven App|Global|||Read|
|Plugin Assembly|Global|Read|Read|Read|
|Plugin Type|Global|Read|Read|Read|
|Relationship|Global|||Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Proessing Step|Global|Read|Read|Read|
|SDK Message Proessing Step Image|Global|Read|Read|Read|
|System From|Global|||Write|

##### <a name="custom-entities"></a>Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2020|
|----|----|-----|----|----|
|Business Central Account Statistics|Global|Read|Read|Read|
|Business Central Connection|Global|Create, Read, Write, Delete|Create, Read, Write, Delete|Create, Read, Write, Delete|
|Post Configuration|Global|||Write|

### <a name="minimum-permissions-for-automatically-created--integration-application-user"></a>Minimum Permissions for automatically created [!INCLUDE[prod_short](includes/prod_short.md)] Integration application user
The following table displays the minimum permissions on each tab for each security role that is required for the automatically created [!INCLUDE[prod_short](includes/prod_short.md)] Integration application user.

##### <a name="core-records"></a>Core Records
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Account|Global|Create, Read, Write, Append, Append To, Assign|Create, Read, Write, Append, Append To, Assign|Create, Read, Write, Append, Append To, Assign|
|Action Card|Global||Read|Read|
|Connection|Global|Read|Read|Read|
|Contact|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Note|Global|||Create, Read, Write, Delete Append, Assign|
|Opportunity|Global||Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Post|Global|||Create, Read, Append To|
|User Entity UI|User|Create, Read, Write|Create, Read, Write|Create, Read, Write|

##### <a name="sales"></a>Sales
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Invoice|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Order|Global|Read, Write, Append To|Read, Write, Append To|Read, Write, Append, Append To, Assign|
|Product|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Property|Global|Read|Read|Read|
|Property Association|Global|Read|Read|Read|
|Property Option Set Item|Global|Read|Read|Read|
|Quote|Global|Read|Read|Read|

##### <a name="service"></a>Service
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Case|Global|Read|Read|Read|

##### <a name="business-management"></a>Business Management
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Currency|Global|Create, Read, Write|Create, Read, Write|Create, Read, Write|
|Organization|Global|Read, Write|Read, Write|Read, Write|
|Security Role|Global|||Read|
|User|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|User Settings|Global|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|
|Act on Behalf of Another User|Global|Yes|Yes|Yes|

##### <a name="customization-1"></a>Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Field|Global||Read|Read|
|Plug-in Assembly|Global|Read|Read|Read|
|Plug-in Type|Global|Read|Read|Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Processing Step|Global|Read|Read|Read|
|Web Resource|Global|Read|Read|Read|

##### <a name="custom-entities-1"></a>Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

### <a name="product-availability-user"></a>Product Availability User
You can allow sales people to view inventory levels for the items they sell by granting them the permissions described in the following table.

##### <a name="custom-entities-2"></a>Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

-->

## <a name="see-also"></a>Se også

[Integrere med Microsoft Dataverse](admin-common-data-service.md)  
[Integrere med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
