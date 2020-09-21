---
title: Installere utvidelser for å tilpasse Dynamics 365 Business Central | Microsoft-dokumentasjon
description: Finn ut hvordan du legger til funksjoner og tilpasser Business Central ved å installere utvidelser.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 08/12/2020
ms.author: edupont
ms.openlocfilehash: 2011728e8e036442418c6a2d8b51477b45b02d1e
ms.sourcegitcommit: 43284728c34b72ad1984a516273dc80e4cdc99ab
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/04/2020
ms.locfileid: "3765924"
---
# <a name="customizing-business-central-using-extensions"></a><span data-ttu-id="8fe58-103">Tilpasse Business Central for med utvidelser</span><span class="sxs-lookup"><span data-stu-id="8fe58-103">Customizing Business Central Using Extensions</span></span>

<span data-ttu-id="8fe58-104">Du kan endre [!INCLUDE[d365fin](includes/d365fin_md.md)] ved å installere utvidelser som for eksempel legger til funksjonalitet, endrer virkemåte eller gir deg tilgang til nye elektroniske tjenester.</span><span class="sxs-lookup"><span data-stu-id="8fe58-104">You can change [!INCLUDE[d365fin](includes/d365fin_md.md)] by installing extensions that add functionality, changes behavior, or gives you access to new online services, for example.</span></span>

> [!NOTE]
> <span data-ttu-id="8fe58-105">Du må ha de rette tillatelsene for å installere utvidelser fra AppSource eller legge til utvidelser per leietaker.</span><span class="sxs-lookup"><span data-stu-id="8fe58-105">To install extensions from AppSource or add per-tenant extensions, you must have the right permissions.</span></span> <span data-ttu-id="8fe58-106">Du må enten være medlem av Adm. av D365-utv.-brukergruppen eller ha tillatelsessettet Adm. av D365-utv.</span><span class="sxs-lookup"><span data-stu-id="8fe58-106">You must either be a member of the D365 EXTENSION MGMT user group or you must have the D365 EXTENSION MGMT permission set.</span></span> <span data-ttu-id="8fe58-107">Hvis du er administrator, kan du tilordne brukergrupper og -tillatelser til andre brukere i selskapet.</span><span class="sxs-lookup"><span data-stu-id="8fe58-107">If you are an administrator, you can assign user groups and permissions to other users in your company.</span></span><br /><br />
<span data-ttu-id="8fe58-108">Hvis du vil bruke funksjonaliteten fra en utvidelse, for eksempel åpne sider, kjøre rapporter, velge handlinger og så videre, må du være tilordnet tillatelsessettene som er installert som en del av utvidelsen.</span><span class="sxs-lookup"><span data-stu-id="8fe58-108">To use the functionality that is provided by an extension, such as opening pages, running reports, selecting actions, and so on, you must be assigned the permission sets that are installed as part of the extension.</span></span>

> [!IMPORTANT]  
> <span data-ttu-id="8fe58-109">Det er ikke støtte for opplasting av per leier-utvidelser og installasjon av AppSource-utvidelser fra **Administrasjon av utvidelse**-siden for lokale installasjoner.</span><span class="sxs-lookup"><span data-stu-id="8fe58-109">The upload of per-tenant extensions and the installation of AppSource extensions is not supported through the **Extension Management** page for on-premise installations.</span></span>

<span data-ttu-id="8fe58-110">Når du starter [!INCLUDE[d365fin](includes/d365fin_md.md)] for første gang, er noen utvidelser allerede installert for deg.</span><span class="sxs-lookup"><span data-stu-id="8fe58-110">When you first launch [!INCLUDE[d365fin](includes/d365fin_md.md)], some extensions are already installed for you.</span></span> <span data-ttu-id="8fe58-111">Over tid gjøres flere utvidelser tilgjengelig for deg, og du kan deretter velge om du vil bruke utvidelsen eller ikke.</span><span class="sxs-lookup"><span data-stu-id="8fe58-111">Over time, more extensions will be made available to you, and you can then choose if you want to use the extension or not.</span></span>

<span data-ttu-id="8fe58-112">Microsoft tilbyr for eksempel en utvidelse som kan gi integrering med PayPal Payments Standard.</span><span class="sxs-lookup"><span data-stu-id="8fe58-112">For example, Microsoft provides an extension that provides integration with PayPal Payments Standard.</span></span> <span data-ttu-id="8fe58-113">Denne utvidelsen er installert som standard.</span><span class="sxs-lookup"><span data-stu-id="8fe58-113">This extension is installed by default.</span></span>
<span data-ttu-id="8fe58-114">Hvis en annen utvidelse gjøres tilgjengelig som gir integrasjon med en annen betalingstjenesten, kan du installere den nye utvidelsen og deretter velger hvilke av de to tjenestene du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="8fe58-114">But if another extension is made available that offers integration with another payment service, you can install the new extension and then choose which of the two services to use.</span></span>  

<span data-ttu-id="8fe58-115">Du administrerer utvidelsene på siden **Administrasjon av utvidelse**.</span><span class="sxs-lookup"><span data-stu-id="8fe58-115">You manage the extensions on the **Extension Management** page.</span></span> <span data-ttu-id="8fe58-116">Du kan gå til denne siden fra Hjem.</span><span class="sxs-lookup"><span data-stu-id="8fe58-116">You can access this page from Home.</span></span> <span data-ttu-id="8fe58-117">Du kan også velge ikonet **Søk etter en side eller rapport** ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") øverst til høyre, angi **Utvidelse**, og deretter velge den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="8fe58-117">Alternatively, choose the **Search for Page or Report** icon ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") in the top right corner, enter **Extension**, and then choose the related link.</span></span> <span data-ttu-id="8fe58-118">Hvis du vil ha mer informasjon, kan du se [Installere og avinstallere utvidelser](ui-extensions-install-uninstall.md).</span><span class="sxs-lookup"><span data-stu-id="8fe58-118">For more information, see [Installing and Uninstalling Extensions](ui-extensions-install-uninstall.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="8fe58-119">Hvis du mener at du skal ha tilgang til en utvidelse, men ikke finner funksjonaliteten, kontrollerer du siden **Administrasjon av utvidelse**. Hvis utvidelsen ikke er oppført der, kan du installere den, som beskrevet i delen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="8fe58-119">If you think you should have access to an extension but you cannot find its functionality, check the **Extension Management** page - if the extension is not listed there, you can install it as described in the following section.</span></span>  

> [!NOTE]  
> <span data-ttu-id="8fe58-120">Nye utvidelser er ikke tilgjengelige i AppSource like etter at vi har kunngjort en oppdatering.</span><span class="sxs-lookup"><span data-stu-id="8fe58-120">New extensions are not available in AppSource immediately after we announce an update.</span></span> <span data-ttu-id="8fe58-121">Du kan følge med på utvidelsene på [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).</span><span class="sxs-lookup"><span data-stu-id="8fe58-121">You can keep an eye out for the extensions at  [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).</span></span>

## <a name="see-also"></a><span data-ttu-id="8fe58-122">Se også</span><span class="sxs-lookup"><span data-stu-id="8fe58-122">See Also</span></span>

[<span data-ttu-id="8fe58-123">Utvide Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="8fe58-123">Extending Dynamics 365 Business Central</span></span>](about-develop-extensions.md)  
[<span data-ttu-id="8fe58-124">Business Central-utvidelser fra andre leverandører</span><span class="sxs-lookup"><span data-stu-id="8fe58-124">Business Central Extensions by Other Providers</span></span>](ui-extensions-other.md)  
[<span data-ttu-id="8fe58-125">Sett opp Envestnet Yodlee Bank Feeds-tjenesten</span><span class="sxs-lookup"><span data-stu-id="8fe58-125">Set Up the Envestnet Yodlee Bank Feeds Service</span></span>](bank-how-setup-bank-statement-service.md)  
[<span data-ttu-id="8fe58-126">Aktivere kundebetalinger gjennom PayPal</span><span class="sxs-lookup"><span data-stu-id="8fe58-126">Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md)  
[<span data-ttu-id="8fe58-127">Overføre forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="8fe58-127">Migrating Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="8fe58-128">Konfigurere GetAddress.io UK Postal Code-utvidelsen</span><span class="sxs-lookup"><span data-stu-id="8fe58-128">Setting Up the GetAddress.io UK Postal Code extension</span></span>](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
<span data-ttu-id="8fe58-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)]-utvidelser fra andre leverandører](ui-extensions-other.md)</span><span class="sxs-lookup"><span data-stu-id="8fe58-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)] Extensions by Other Providers](ui-extensions-other.md)</span></span>  
[<span data-ttu-id="8fe58-130">Komme i gang</span><span class="sxs-lookup"><span data-stu-id="8fe58-130">Getting Started</span></span>](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
