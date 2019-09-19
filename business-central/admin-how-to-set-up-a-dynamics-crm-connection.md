---
title: Koble til Dynamics 365 for Sales | Microsoft Docs
description: Du kan integrere med Dynamics 365 for Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/06/2019
ms.author: bholtorf
ms.openlocfilehash: 37728cb92e4b87346cf2be0e2ddc50b5a3b5f25e
ms.sourcegitcommit: 6ef7d2fae52feff786f2e15e2863d7f5aaa762be
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/22/2019
ms.locfileid: "1917394"
---
# <a name="set-up-a-connection-to-dynamics-365-for-sales"></a>Konfigurere en kobling til Dynamics 365 for Sales
For å integrere med [!INCLUDE[crm_md](includes/crm_md.md)] må du sette opp en forbindelse mellom [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)].

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085501]

## <a name="before-you-start"></a>Før du begynner
Før du begynner å koble appene er det noen opplysninger som er nyttige å ha klar:  

* En URL-adresse til [!INCLUDE[crm_md](includes/crm_md.md)]-appen. En raskt mte å hente URL-adressen er å åpne [!INCLUDE[crm_md](includes/crm_md.md)] og kopiere URL-en, og deretter lime den inn **URL-adresse for Dynamics 365 for Sales**-feltet i [!INCLUDE[d365fin](includes/d365fin_md.md)]. [!INCLUDE[d365fin](includes/d365fin_md.md)] løser formateringen for deg.  
* Et brukernavn og passord til en brukerkonto som bare brukes for integrasjonen.  
* Brukernavnet og passordet på kontoen som har administratorrettigheter.  

> [!Note]
> Følgende trinn beskriver fremgangsmåten for den elektroniske versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="set-up-test-and-enable-a-connection-to-includecrm_mdincludescrm_mdmd"></a>Konfigurere, teste og aktivere en tilkobling til [!INCLUDE[crm_md](includes/crm_md.md)]  
For andre godkjenningstyper enn Office 365-godkjenning definerer du en tilkobling til Dynamics 365 for Sales på siden **Tilkoblingsoppsett for Microsoft Dynamics 365 for Sales**. For Office 365-godkjenning kan du også bruke den assisterte oppsettsveiledningen **Tilkoblingsoppsett for Dynamics 365 for Sales**, som hjelper deg med å angi den nødvendige informasjonen.

### <a name="to-use-an-assisted-setup-guide"></a>Slik bruker du en assistert oppsettsveiledning
Den assisterte oppsettsveiledningen **Tilkoblingsoppsett for Dynamics 365 for Sales** hjelper deg med å definere tilkoblingen og angi om du vil aktivere avanserte funksjoner, for eksempel kobling mellom poster.

1. Velg **Oppsett og utvidelser**, og velg deretter **Assistert oppsett**.
2. Velg **Tilkoblingsoppsett for Dynamics 365 for Sales** for å starte assistert oppsettsveiledning.
3. Fyll ut feltene etter behov.
4. Det finnes også avanserte innstillinger som kan forbedre sikkerheten og aktivere [!INCLUDE[crm_md](includes/crm_md.md)] flere muligheter, for eksempel ordrebehandling og visning av lagernivåer. Tabellen nedenfor beskriver avanserte innstillinger.  

|Felt|Beskrivelse|
|-----|-----|
|**Importere Dynamics 365 for Sales-løsning**|Aktiver dette for å installere og konfigurere integreringsløsningen i [!INCLUDE[crm_md](includes/crm_md.md)]. Hvis du vil ha mer informasjon, se [Om Business Central-integrasjonsløsningen](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).|
|**Publiser webtjenesten Varetilgjengelighet**|Aktiver brukere som har [!INCLUDE[crm_md](includes/crm_md.md)], til å vise tilgjengeligheten av varer (produkter) på lageret i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dette krever [!INCLUDE[d365fin](includes/d365fin_md.md)]-brukerkontoen med tilgangsnøkkel for webtjenester. Tilordning av nøkkelen er en totrinnsprosess. I brukerkontoen i [!INCLUDE[d365fin](includes/d365fin_md.md)] må du velge **Endre webtjenestenøkkel**-handlingen. I den assisterte oppsettguiden Tilkoblingsoppsett for Dynamics 365 for Sales må du angi URL-adresse for webtjenesten OData for Dynamics 365 Business Central og angi [!INCLUDE[d365fin](includes/d365fin_md.md)]-brukerlegitimasjon for å få tilgang til tjenesten. Hvis du vil ha mer informasjon, kan du se [OData-webtjenester](/dynamics365/business-central/dev-itpro/webservices/odata-web-services.md).|
|**URL-adresse for webtjenesten OData for Dynamics 365 Business Central**|Hvis du aktiverer webtjenesten Varetilgjengelighet, angis URL-adressen for webtjenesten OData for deg.|
|**Brukernavn for webtjenesten OData for Dynamics 365 Business Central**|Navnet på [!INCLUDE[d365fin](includes/d365fin_md.md)]-brukerkontoen som [!INCLUDE[crm_md](includes/crm_md.md)] bruker til å hente informasjon om varedisposisjonen i [!INCLUDE[d365fin](includes/d365fin_md.md)] via OData-webtjenesten.|
|**Tilgangsnøkkel for webtjenesten OData for Dynamics 365 Business Central**|Tilgangsnøkkelen for brukerkontoen som [!INCLUDE[crm_md](includes/crm_md.md)] bruker til å hente informasjon om varedisposisjonen fra [!INCLUDE[d365fin](includes/d365fin_md.md)] via OData-webtjenesten. Nøkkelen tilordnes til brukeren som er valgt i feltet **Brukernavn for webtjenesten OData for Dynamics 365 Business Central**. Hvis du vil ha nøkkelen, kan du velge knappen **Oppslagsverdi** ved siden av brukernavn, velge brukeren, **Administrer** og deretter klikke på **Rediger**. På kortet velger du **Handlinger**, **Godkjenning** og deretter **Endre webtjenestenøkkel**.|
|**Aktiver ordreintegrering**|Når brukerne oppretter ordrer i [!INCLUDE[crm_md](includes/crm_md.md)] og oppfyller ordrer i [!INCLUDE[d365fin](includes/d365fin_md.md)], integreres prosessen i [!INCLUDE[crm_md](includes/crm_md.md)]. Hvis du vil ha mer informasjon, se [Aktivere ordrebehandlingsintegrering](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). Dette krever at du oppgir rettigheter til en systemansvarligbrukerkonto i [!INCLUDE[crm_md](includes/crm_md.md)]. Hvis du vil ha mer informasjon, kan du se [Håndtere ordredata](marketing-integrate-dynamicscrm.md#handling-sales-order-data).|
|**Aktiver Dynamics 365 for Sales-tilkobling**|Aktiver tilkoblingen til [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Dynamics 365 SDK-versjon**|Dette er bare relevant hvis du integrerer med en lokal versjon av [!INCLUDE[crm_md](includes/crm_md.md)]. Dette er Dynamics 365 SDK-versjonen (også kalt Xrm) du bruker til å koble [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]. Versjonen må være kompatibel med SDK-versjonen som brukes av [!INCLUDE[crm_md](includes/crm_md.md)], og er lik eller nyere enn versjonen som brukes av [!INCLUDE[crm_md](includes/crm_md.md)].|

> [!Note]
> Assistert oppsett-veiledningen **Konfigurere Dynamics 365 for Sales-tilkobling** tilordner automatisk sikkerhetsrollene **Integrasjonsadministrator** og **Integrasjonsbruker** til brukerkontoen som brukes til integrasjon. 

### <a name="to-create-or-maintain-the-connection-manually"></a>Opprette eller vedlikeholde tilkoblingen manuelt
Følgende fremgangsmåte beskriver hvordan du fyller ut feltene på siden **Tilkoblingsoppsett for Microsoft Dynamics 365 for Sales** manuelt. Dette er også siden der du kan håndtere innstillingene for integrasjonen.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Tilkoblingsoppsett for Microsoft Dynamics 365**, og velg deretter den relaterte koblingen.
2. Skriv inn følgende informasjon for tilkoblingen fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)].

|Felt|Beskrivelse|
|-----|-----|
|**URL-adresse for Dynamics 365 for Sales**|URL-adressen for forekomsten av [!INCLUDE[crm_md](includes/crm_md.md)]. Hvis du vil hente URL-adressen, åpne [!INCLUDE[crm_md](includes/crm_md.md)], koper URL-adressen fra adressefeltet i webleseren, og lim inn URL-adressen i feltet. [!INCLUDE[d365fin](includes/d365fin_md.md)] sørger for at formatet er riktig.|
|**Brukernavn** og **Passord**|Legitimasjon for brukerkontoen som er reservert for integreringen. Hvis du vil ha mer informasjon, se [Sette opp brukerkontoer for integrasjon med Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md).|
|**Aktivert**|Begynn å bruke integrasjonen. Hvis du ikke aktiverer tilkoblingen nå, lagres tilkoblingsinnstillingene, men brukerne vil ikke ha tilgang til [!INCLUDE[crm_md](includes/crm_md.md)]-data fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan gå tilbake til denne siden og aktivere tilkoblingen senere.  |
|**Dynamics 365 SDK-versjon**|Hvis du integrerer med en lokal versjon av [!INCLUDE[crm_md](includes/crm_md.md)], er dette Dynamics 365 SDK-pakken (også kalt Xrm) du bruker til å koble [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]. Versjonen du velger, må være kompatibel med SDK-versjonen som brukes av [!INCLUDE[crm_md](includes/crm_md.md)]. Denne versjonen må være lik eller nyere enn versjonen som brukes av [!INCLUDE[crm_md](includes/crm_md.md)].|

> [!Note]
> Hvis du kobler en lokal versjon av [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)], og du vil konfigurere en forbindelse til en [!INCLUDE[crm_md](includes/crm_md.md)]-forekomst med en bestemt godkjenningstype, fyller du ut feltene i hurtigfanen **Detaljer for godkjenningstype**. Hvis du vil ha mer informasjon, se [Bruke tilkoblingsstrenger i XRM-verktøy for å koble til Dynamics 365](https://go.microsoft.com/fwlink/?linkid=843055). Dette trinnet er ikke nødvendig ved tilkobling av en elektronisk versjon av [!INCLUDE[d365fin](includes/d365fin_md.md)].

3. Skriv inn følgende informasjon for tilkoblingen fra [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)].

|Felt|Beskrivelse|
|-----|-----|
|**URL-adresse for webklient for Dynamics 365 Business Central**|URL-adressen for [!INCLUDE[d365fin](includes/d365fin_md.md)]-forekomsten din. Dette gjør det mulig for brukere i [!INCLUDE[crm_md](includes/crm_md.md)] å åpne tilhørende poster i [!INCLUDE[d365fin](includes/d365fin_md.md)] fra poster i [!INCLUDE[crm_md](includes/crm_md.md)], for eksempel en konto eller et produkt. [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster åpnes i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Sett dette feltet til URL-adressen til [!INCLUDE[d365fin](includes/d365fin_md.md)]-forekomsten du vil bruke.<br /><br /> For å tilbakestille feltet til standard nettadresse for [!INCLUDE[d365fin](includes/d365fin_md.md)] velger du **Tilbakestill URL-adresse for webklient**.<br /><br /> Dette feltet er aktuelt hvis [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrasjonsløsningen er installert i [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Webtjenesten Varetilgjengelighet er aktivert**|Aktiver brukere som har [!INCLUDE[crm_md](includes/crm_md.md)], til å vise tilgjengeligheten av varer (produkter) på lageret i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du aktiverer dette, må du også angi et brukernavn og en tilgangsnøkkel for [!INCLUDE[crm_md](includes/crm_md.md)] for å spørre OData-webtjeneste etter tilgjengelighet for varer (produkter). Hvis du vil ha mer informasjon, kan du se [OData-webtjenester](/dynamics365/business-central/dev-itpro/webservices/odata-web-services.md).|
|**URL-adresse for webtjenesten OData for Dynamics 365 Business Central**|Hvis du aktiverer webtjenesten Varetilgjengelighet, angis URL-adressen for webtjenesten OData for deg.|
|**Brukernavn for webtjenesten OData for Dynamics 365 Business Central**|Navnet på brukerkontoen som [!INCLUDE[crm_md](includes/crm_md.md)] bruker til å hente informasjon om varedisposisjonen fra [!INCLUDE[d365fin](includes/d365fin_md.md)] via OData-webtjenesten.|
|**Tilgangsnøkkel for webtjenesten OData for Dynamics 365 Business Central**|Tilgangsnøkkelen for brukerkontoen som [!INCLUDE[crm_md](includes/crm_md.md)] bruker til å hente informasjon om varedisposisjonen fra [!INCLUDE[d365fin](includes/d365fin_md.md)] via OData-webtjenesten. Nøkkelen tilordnes til brukeren som er valgt i feltet **Brukernavn for webtjenesten OData for Dynamics 365 Business Central**. Hvis du vil ha nøkkelen, kan du velge knappen **Oppslagsverdi** ved siden av brukernavn, velge brukeren, **Administrer** og deretter klikke på **Rediger**. På kortet velger du **Handlinger**, **Godkjenning** og deretter **Endre webtjenestenøkkel**.|

4. Angi følgende innstillinger for [!INCLUDE[crm_md](includes/crm_md.md)].

|Felt|Beskrivelse|
|-----|-----|
|**Ordreintegrasjon er aktivert**|Gjør det mulig for brukerne å sende ordrer og aktiverte tilbud i [!INCLUDE[crm_md](includes/crm_md.md)] og deretter vise og behandle dem i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dette integrerer prosessen i [!INCLUDE[crm_md](includes/crm_md.md)]. Hvis du vil ha mer informasjon, se [Aktivere ordrebehandlingsintegrering](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration).|
|**Opprett ordrer automatisk**|Opprett en ordre i [!INCLUDE[d365fin](includes/d365fin_md.md)] når en bruker oppretter og sender en i [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Behandle salgstilbud automatisk**|Behandle et tilbud i [!INCLUDE[d365fin](includes/d365fin_md.md)] når en bruker oppretter og aktiverer et i [!INCLUDE[crm_md](includes/crm_md.md)].|

5. Angi følgende avanserte innstillinger.

|Felt|Beskrivelse|
|-----|-----|
|**[!INCLUDE[d365fin](includes/d365fin_md.md)]-brukere må samordne med Dynamics 365 for Sales-brukere**|Angi om [!INCLUDE[d365fin](includes/d365fin_md.md)]-brukerkontoer må ha en samsvarende brukerkonto i [!INCLUDE[crm_md](includes/crm_md.md)]. **E-postadresse for godkjenning for Office 365** for [!INCLUDE[d365fin](includes/d365fin_md.md)]-brukeren må være den samme som **Primær-e-postadresse** til [!INCLUDE[crm_md](includes/crm_md.md)]-brukeren.<br /><br /> Hvis du angir verdien til **Ja**, vil [!INCLUDE[d365fin](includes/d365fin_md.md)]-brukere som ikke har en tilsvarende [!INCLUDE[crm_md](includes/crm_md.md)]-brukerkonto, ikke ha [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrasjonsfunksjonene i brukergrensesnittet. Tilgang til [!INCLUDE[crm_md](includes/crm_md.md)]-data direkte fra [!INCLUDE[d365fin](includes/d365fin_md.md)] er utført på vegne av [!INCLUDE[crm_md](includes/crm_md.md)]-brukerkontoen.<br /><br /> Hvis du angir verdien til **Nei**, vil alle [!INCLUDE[d365fin](includes/d365fin_md.md)]-brukere ha [!INCLUDE[crm_md](includes/crm_md.md)]-integrasjonsfunksjonene i brukergrensesnittet. Tilgang til [!INCLUDE[crm_md](includes/crm_md.md)]-data gjøres på vegne av [!INCLUDE[crm_md](includes/crm_md.md)]-tilkoblings(integrerings)bruker.|
|**Gjeldende Business Central-bruker er tilordnet til en Dynamics 365 for Sales-bruker**|Angir om brukerkontoen er tilordnet til en konto i [!INCLUDE[crm_md](includes/crm_md.md)]|

6. For å teste tilkoblingsinnstillingene kan du velge **Test tilkobling**.  

    > [!NOTE]  
    >  Hvis datakryptering ikke er aktivert i [!INCLUDE[d365fin](includes/d365fin_md.md)], får du bli spurt om du vil aktivere den. Hvis du vil aktivere datakryptering, velger du **Ja** og angir nødvendig informasjon. Ellers velger du **Nei**. Du kan aktivere datakryptering senere. Hvis du vil ha mer informasjon, kan du se [Kryptere data i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) i hjelpen for utviklere og IT-eksperter.  

7. Hvis [!INCLUDE[crm_md](includes/crm_md.md)]-synkronisering ikke allerede er satt opp, vil du bli spurt om du vil bruke standard synkroniseringsoppsett. Avhengig av om du vil beholde postene som er justert i [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)], velger du **Ja** eller **Nei**.

> [!Note]
> Tilkobling til Dynamics 365 for Sales ved hjelp av siden **Tilkoblingsoppsett for Microsoft Dynamics 365 for Sales** kan kreve at du tilordner sikkerhetsrollene Integrasjonsadministrator og Integrasjonsbruker til kontoen som brukes for integrasjon. Hvis du vil ha mer informasjon, kan du se [Tilordne en sikkerhetsrolle til en bruker](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user).


> [!Note]
> Ved tilkobling til Dynamics 365 for Sales ved hjelp av siden **Tilkoblingsoppsett for Microsoft Dynamics 365 for Sales** må du kanskje [tilordne sikkerhetsrollene **Integrasjonsadministrator** og **Integrasjonsbruker**](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user) til brukerkontoen som brukes for integrasjon.


### <a name="to-disconnect-from-includecrm_mdincludescrm_mdmd"></a>For å koble fra [!INCLUDE[crm_md](includes/crm_md.md)]  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Tilkoblingsoppsett for Microsoft Dynamics 365 for Sales**, og velg deretter den relaterte koblingen.
2. På siden **Tilkoblingsoppsett for Microsoft Dynamics 365 for Sales** fjerner du merket for **Aktivert**.  

<!--## Install the [!INCLUDE[d365fin](includes/d365fin_md.md) Integration Solution
[!INCLUDE[d365fin](includes/d365fin_md.md)] includes a solution that enables users to access coupled records, such as customers and items, from records in [!INCLUDE[crm_md](includes/crm_md.md)], such as accounts and products. The solution adds a link to the pages in [!INCLUDE[crm_md](includes/crm_md.md)] to open the coupled [!INCLUDE[d365fin](includes/d365fin_md.md)] record. The solution also displays information from [!INCLUDE[d365fin](includes/d365fin_md.md)]on certain entities in [!INCLUDE[crm_md](includes/crm_md.md)], such as accounts. Installing this solution is optional. <!--"Solution" sounds old school. Is it an app, or an add-in, or an extension?


1.  From [!INCLUDE[d365fin](includes/d365fin_md.md)] installation media \(DVD\), copy the DynamicsNAVIntegrationSolution.zip file to your computer.  

     The DynamicsNAVIntegrationSolution.zip file is located in the **CrmCustomization** folder. This file is the solution package.   

2.  In [!INCLUDE[crm_md](includes/crm_md.md)], import the DynamicsNAVIntegrationSolution.zip as a solution.  

     This step adds the **[!INCLUDE[d365fin](includes/d365fin_md.md) Connection** entity and **[!INCLUDE[d365fin](includes/d365fin_md.md) Account Statistics** entity in the system and additional items such as [!INCLUDE[d365fin](includes/d365fin_md.md)] integration security roles.  

     For more information about how to manage solutions in [!INCLUDE[crm_md](includes/crm_md.md)], [http://go.microsoft.com/fwlink/?LinkID=616519](http://go.microsoft.com/fwlink/?LinkID=616519).  

3.  Optional: Set up the **[!INCLUDE[d365fin](includes/d365fin_md.md) Connection** entity to display in the **Settings** area of [!INCLUDE[crm_md](includes/crm_md.md)].  

     This enables [!INCLUDE[crm_md](includes/crm_md.md)] users who are assigned the **[!INCLUDE[d365fin](includes/d365fin_md.md) Admin** role to modify the entity in [!INCLUDE[crm_md](includes/crm_md.md)]. For more information about how to modify entities in [!INCLUDE[crm_md](includes/crm_md.md)], see [View or edit entity information](http://go.microsoft.com/fwlink/?LinkID=616521).  

4.  Assign the **[!INCLUDE[d365fin](includes/d365fin_md.md) Integration Administrator** role to the user account for the connection to [!INCLUDE[d365fin](includes/d365fin_md.md)].  

5.  Assign the **Business Central Integration User** role to all users who will use the [!INCLUDE[d365fin](includes/d365fin_md.md)] integration solution.  

If you install the [!INCLUDE[d365fin](includes/d365fin_md.md)] integration solution after you have set up the connection to [!INCLUDE[crm_md](includes/crm_md.md)] in [!INCLUDE[d365fin](includes/d365fin_md.md)], you must modify the connection setup to point to the URL.-->

<!--of the [!INCLUDE[nav_web_md](../developer/includes/nav_web_md.md)]. For more information, see [How to: Set Up a Microsoft Dynamics 365 for Sales Connection]() -->

<!--
# View Item Availability - Support Matrix
For most versions of [!INCLUDE[d365fin](includes/d365fin_md.md) and Dynamics 365 for Sales, you can view availability figures for items across the integrated products. The following table shows which version combinations support viewing item availability.

| |Dynamics 365 for Sales version|2015/Update 1/Online|2016/Update 1/Online|Dynamics 365 for Sales|
|-|---------------------|---------------------|--------------------------|-----------------|
|**Dynamics NAV version**|
|**2016**||Not supported|Not supported|Not supported|
|**2017**||Not supported - Install from 2016|Supported|Supported|
|**Dynamics 365 for Financials**||Not supported - Install from 2016|Supported|Supported|


> [Note]
> You can obtain item availability support for combinations of Dynamics CRM 2015 and Business Central by running the DynamicsNAVIntegrationSolution.zip file on the Business Central product DVD.

For more information, see [System Requirements for Business Central](../deployment/system-requirement-business-central.md).

-->

## <a name="see-also"></a>Se også  
[Vise statusen for en synkronisering](admin-how-to-view-synchronization-status.md)  
