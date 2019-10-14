---
title: Sette opp brukerkontoer for integrasjon med Dynamics 365 Sales | Microsoft Docs
description: Lær hvordan du definerer brukerkontoene som appene bruker til å utveksle data, og som brukes til å få tilgang til og synkronisere data i appene.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: a876df301476cb6b4af335e8ee957de26865cbaa
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307831"
---
# <a name="setting-up-user-accounts-for-integrating-with-dynamics-365-sales"></a>Sette opp brukerkontoer for integrasjon med Dynamics 365 Sales
Denne artikkelen gir en oversikt over hvordan du definerer brukerkontoene som er nødvendige for å integrere [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085500]

## <a name="setting-up-the-administrator-user-account-in-sales"></a>Sette opp administratorbrukerkontoen i Sales
Du må legge til brukerkontoen for administrator for [!INCLUDE[d365fin](includes/d365fin_md.md)] som en bruker i [!INCLUDE[crm_md](includes/crm_md.md)], og deretter forfremme brukeren til administrator i [!INCLUDE[crm_md](includes/crm_md.md)]. Brukerkontoen for administrator må også ha rollen Systemtilpasser og minst én annen ikke-administrativ brukerrolle, for eksempel Salgssjef, i [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="setting-up-the-user-account-for-the-integration"></a>Konfigurere brukerkontoen for integrasjonen
Du må opprette en dedikert brukerkonto i Office 365-abonnement som både [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] kan bruke til å synkronisere data. Denne brukerkontoen må kunne logge på [!INCLUDE[crm_md](includes/crm_md.md)], noe som betyr at denne brukeren må ha lisens for [!INCLUDE[crm_md](includes/crm_md.md)] og minst én sikkerhetsrolle tilordnet til den i [!INCLUDE[crm_md](includes/crm_md.md)], slik det er beskrevet [her](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-user-account). Hvis du vil ha mer informasjon om hvordan du oppretter brukere i [!INCLUDE[crm_md](includes/crm_md.md)], kan du se [Håndtere sikkerhet, brukere og team](http://go.microsoft.com/fwlink/?LinkID=616518). Når tilkoblingen er konfigurert, tilordner [!INCLUDE[d365fin](includes/d365fin_md.md)] brukerkontoen sikkerhetsrollene den trenger for [!INCLUDE[d365fin](includes/d365fin_md.md)], og denne kontoen kan settes til [ikke-interaktiv tilgangsmodus](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account) i [!INCLUDE[crm_md](includes/crm_md.md)]

![Assistert oppsettsveiledning viser sted for å angi brukerlegitimasjon for synkronisering](media/sync-user-setup.png "Veiviserside for assistert oppsett for visualisering viser sted for å angi brukerlegitimasjon for synkronisering")

> [!IMPORTANT]  
> Ikke bruk administratorkontoen for [!INCLUDE[crm_md](includes/crm_md.md)] til synkronisering. Når du gjør det, brytes synkroniseringen.
> I tillegg, for å unngå konstant synkronisering, endringer i data som utførtes av integreringsbrukerkontoen, synkroniseres ikke. <!--What changes would this account make?--> Når tilkoblingen er opprettet, anbefales det å angi tilgangsmodus for brukerkontoen for integrering til ikke-interaktivt modus i [!INCLUDE[crm_md](includes/crm_md.md)]. Hvis du vil ha mer informasjon, se [Opprette en ikke-interaktiv brukerkonto](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

## <a name="setting-up-accounts-sales-people"></a>Definere kontoer for selgerne
Du må opprette kontoer i [!INCLUDE[crm_md](includes/crm_md.md)] for selgerne fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. For å gjøre det enklere tilbyr Microsoft 365-administrasjonssenteret en Excel-mal du kan bruke. På siden **Aktive brukere** velger du **Mer**, og deretter klikker du på **Importer flere brukere**. Velg **Last ned en CSV-fil med bare topptekst**, og deretter angir du opplysninger for selgeren. Hvis du vil se et eksempel kan du velge **Last ned en CSV-eksempelfil med topptekst og eksempelbrukerinformasjon**. Når du har angitt informasjon om brukerne, er neste trinn i importprosessen å tilordne brukerlisensene til Dynamics 365 Customer Engagement-planen.  

Når du importerer brukere og tilordner dem lisenser for Dynamics 365 Customer Engagement, må du tilordne brukerne til rollen **Selger** i [!INCLUDE[crm_md](includes/crm_md.md)].

![Koble selgere til brukere i Dynamics 365 Sales](media/couple-salespeople.png "Visualisering av kobling av selgerne til brukere i Dynamics 365 Sales")

## <a name="minimum-permissions-for-user-accounts-in-includecrm_mdincludescrm_mdmd"></a>Minimumstillatelser for brukerkontoer i [!INCLUDE[crm_md](includes/crm_md.md)]
Når du installerer integrasjonsløsningen, konfigureres tillatelser for integrasjonsbrukerkontoen i [!INCLUDE[crm_md](includes/crm_md.md)]. Hvis disse tillatelsene endres, er det mulig at du må tilbakestille dem. Dette kan du gjøre ved å installere integrasjonsløsningen på nytt eller ved å tilbakestille tillatelsene manuelt. Følgende tabeller inneholder en oversikt over minimumstillatelsene for brukerkontoene i [!INCLUDE[crm_md](includes/crm_md.md)].

### <a name="integration-administrator"></a>Integrasjonsadministrator
Tabellen nedenfor viser minimumstillatelsene i hver fane for hver sikkerhetsrolle som kreves for administratorbrukeren.

##### <a name="customization"></a>Tilpasning
|Sikkerhetsrolle|Tilgangsnivå|Dynamics NAV 2018 og tidligere|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Modelldrevet app|Global|||Les|
|Plugin-enhet|Global|Les|Les|Les|
|Plugin-type|Global|Les|Les|Les|
|Forbindelser|Global|||Les|
|SDK-melding|Global|Les|Les|Les|
|Behandlingstrinn for SDK-melding|Global|Les|Les|Les|
|Behandlingstrinn for SDK-melding – bilde|Global|Les|Les|Les|
|System fra|Global|||Skriv|

##### <a name="custom-entities"></a>Egendefinerte enheter
|Sikkerhetsrolle|Tilgangsnivå|Dynamics NAV 2018 og tidligere|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Business Central-kontostatistikk|Global|Les|Les|Les|
|Business Central-tilkobling|Global|Opprett, Les, Skriv, Slett|Opprett, Les, Skriv, Slett|Opprett, Les, Skriv, Slett|
|Konfigurasjon av post|Global|||Skriv|

#### <a name="integration-user"></a>Integrasjonsbruker
Tabellen nedenfor viser minimumstillatelsene i hver fane for hver sikkerhetsrolle som kreves for integrasjonsbrukeren.

##### <a name="core-records"></a>Kjerneposter
|Sikkerhetsrolle|Tilgangsnivå|Dynamics NAV 2018 og tidligere|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Konto|Global|Opprett, Les, Skriv, Tilføy, Tilføy i, Tilordne|Opprett, Les, Skriv, Tilføy, Tilføy i, Tilordne|Opprett, Les, Skriv, Tilføy, Tilføy i, Tilordne|
|Handlingskort|Global||Les|Les|
|Tilkobling|Global|Les|Les|Les|
|Kontakt|Global|Opprett, Les, Skriv, Tilføy, Tilføy i|Opprett, Les, Skriv, Tilføy, Tilføy i|Opprett, Les, Skriv, Tilføy, Tilføy i|
|Merk|Global|||Opprett, Les, Skriv, Slett, Tilføy, Tilordne|
|Salgsmulighet|Global||Opprett, Les, Skriv, Tilføy, Tilføy i|Opprett, Les, Skriv, Tilføy, Tilføy i|
|Post|Global|||Opprett, Les, Tilføy i|
|Brukerenhetsgrensesnitt|Bruker|Opprett, Les, Skriv|Opprett, Les, Skriv|Opprett, Les, Skriv|

##### <a name="sales"></a>Salg
|Sikkerhetsrolle|Tilgangsnivå|Dynamics NAV 2018 og tidligere|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Fakturere|Global|Opprett, Les, Skriv, Tilføy, Tilføy i|Opprett, Les, Skriv, Tilføy, Tilføy i|Opprett, Les, Skriv, Tilføy, Tilføy i|
|Bestilling|Global|Les, Skriv, Tilføy i|Les, Skriv, Tilføy i|Les, Skriv, Tilføy, Tilføy i, Tilordne|
|Produkt|Global|Opprett, Les, Skriv, Tilføy, Tilføy i|Opprett, Les, Skriv, Tilføy, Tilføy i|Opprett, Les, Skriv, Tilføy, Tilføy i|
|Egenskap|Global|Les|Les|Les|
|Egenskapstilknytning|Global|Les|Les|Les|
|Angi element for egenskapsalternativ|Global|Les|Les|Les|
|Tilbud|Global|Les|Les|Les|

##### <a name="service"></a>Tjeneste
|Sikkerhetsrolle|Tilgangsnivå|Dynamics NAV 2018 og tidligere|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Tilfelle|Global|Les|Les|Les|

##### <a name="business-management"></a>Bedriftsadministrasjon
|Sikkerhetsrolle|Tilgangsnivå|Dynamics NAV 2018 og tidligere|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Valuta|Global|Opprett, Les, Skriv|Opprett, Les, Skriv|Opprett, Les, Skriv|
|Organisasjon|Global|Les, Skriv|Les, Skriv|Les, Skriv|
|Sikkerhetsrolle|Global|||Les|
|Bruker|Global|Opprett, Les, Skriv, Tilføy, Tilføy i|Opprett, Les, Skriv, Tilføy, Tilføy i|Opprett, Les, Skriv, Tilføy, Tilføy i|
|Brukerinnstillinger|Global|Opprett, Les, Skriv, Slett, Tilføy i|Opprett, Les, Skriv, Slett, Tilføy i|Opprett, Les, Skriv, Slett, Tilføy i|
|Handle på vegne av en annen bruker|Global|Ja|Ja|Ja|

##### <a name="customization"></a>Tilpasning
|Sikkerhetsrolle|Tilgangsnivå|Dynamics NAV 2018 og tidligere|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Felt|Global||Les|Les|
|Plugin-enhet|Global|Les|Les|Les|
|Plugin-type|Global|Les|Les|Les|
|SDK-melding|Global|Les|Les|Les|
|Behandlingstrinn for SDK-melding|Global|Les|Les|Les|
|Nettressurs|Global|Les|Les|Les|

##### <a name="custom-entities"></a>Egendefinerte enheter
|Sikkerhetsrolle|Tilgangsnivå|Dynamics NAV 2018 og tidligere|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central-kontostatistikk|Global|Opprett, Les, Skriv, Tilføy i|Opprett, Les, Skriv, Tilføy i|Opprett, Les, Skriv, Tilføy i|
|Dynamics 365 Business Central-tilkobling|Global|Les|Les|Les|

### <a name="product-availability-user"></a>Produkttilgjengelighetsbruker
Du la selgere vise lagernivåer for varene de selger, ved å gi dem tillatelsene som er beskrevet i tabellen nedenfor.

##### <a name="custom-entities"></a>Egendefinerte enheter
|Sikkerhetsrolle|Tilgangsnivå|Dynamics NAV 2018 og tidligere|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central-kontostatistikk|Global|Opprett, Les, Skriv, Tilføy i|Opprett, Les, Skriv, Tilføy i|Opprett, Les, Skriv, Tilføy i|
|Dynamics 365 Business Central-tilkobling|Global|Les|Les|Les|

## <a name="see-also"></a>Se også  
[Integrere med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
