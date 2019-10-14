---
title: Bruk dataene til å lage en app | Microsoft-dokumenter
description: Du kan gjøre Business Central-dataene tilgjengelige som en datakilde og angi en OData-URL-adresse til webtjenestene dine for å utvikle en forretningsapp ved hjelp av PowerApps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 4b8005154afb988cf25c6a04b7beeaafd199afca
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305029"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-powerapps"></a><span data-ttu-id="be78f-103">Koble til Business Central-dataene for å utvikle en forretningsapp ved hjelp av PowerApps</span><span class="sxs-lookup"><span data-stu-id="be78f-103">Connecting to Your Business Central Data to Build a Business App Using PowerApps</span></span>
<span data-ttu-id="be78f-104">Du kan gjøre [!INCLUDE[d365fin](includes/d365fin_md.md)]-data tilgjengelige som en datakilde i PowerApps.</span><span class="sxs-lookup"><span data-stu-id="be78f-104">You can make your [!INCLUDE[d365fin](includes/d365fin_md.md)] data available as a data source in PowerApps.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="be78f-105">Du må ha en gyldig konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] og med PowerApps.</span><span class="sxs-lookup"><span data-stu-id="be78f-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with PowerApps.</span></span>  

## <a name="to-add-included365finincludesd365fin_mdmd-as-a-data-source-in-powerapps"></a><span data-ttu-id="be78f-106">Legge til [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde i PowerApps</span><span class="sxs-lookup"><span data-stu-id="be78f-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in PowerApps</span></span>
1. <span data-ttu-id="be78f-107">I leseren, kan du gå til [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/), og deretter logge på.</span><span class="sxs-lookup"><span data-stu-id="be78f-107">In your browser, navigate to [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="be78f-108">På startsiden velger du **Apper**, **Opprett en app** og **Lerret** for å opprette en ny lerretsapp.</span><span class="sxs-lookup"><span data-stu-id="be78f-108">On the Home page, choose the **Apps**, **Create an app** and **Canvas** to create a new canvas app.</span></span> <span data-ttu-id="be78f-109">Denne appen blir utformet for bruk på en mobil enhet, men du kan også velge å bruke en annen mal.</span><span class="sxs-lookup"><span data-stu-id="be78f-109">This app will be designed for use on a mobile device, but you can also choose to use another template.</span></span>

    <span data-ttu-id="be78f-110">Neste trinn for å opprette en PowerApp er å velge data.</span><span class="sxs-lookup"><span data-stu-id="be78f-110">The next step to create a PowerApp is to select your data.</span></span> <span data-ttu-id="be78f-111">Velg pilikonet og deretter velge **Ny tilkobling** i øvre venstre side av siden.</span><span class="sxs-lookup"><span data-stu-id="be78f-111">Choose the Arrow icon then choose the **New connection** option in the upper left side of the page.</span></span>
3. <span data-ttu-id="be78f-112">Velg **Business Central** i listen over tilgjengelige tilkoblinger, og velg deretter **Opprett**-knappen.</span><span class="sxs-lookup"><span data-stu-id="be78f-112">In the list of available connections, choose **Business Central**, and then choose the **Create** button.</span></span>

    <span data-ttu-id="be78f-113">PowerApps kobler til [!INCLUDE [prodshort](includes/prodshort.md)] med legitimasjonen du logget på med.</span><span class="sxs-lookup"><span data-stu-id="be78f-113">PowerApps will connect to your [!INCLUDE [prodshort](includes/prodshort.md)] using the credentials that you are signed in with.</span></span> <span data-ttu-id="be78f-114">Hvis du ikke er administrator i [!INCLUDE [prodshort](includes/prodshort.md)], må du kanskje logge på med en annen konto.</span><span class="sxs-lookup"><span data-stu-id="be78f-114">If you are not an administrator of your [!INCLUDE [prodshort](includes/prodshort.md)], you may have to sign in with another account.</span></span>  

4.  <span data-ttu-id="be78f-115">PowerApps viser en liste over *Miljøer og selskaper* som er tilgjengelige fra [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="be78f-115">PowerApps will display a list of *Environments and companies* that are available from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="be78f-116">Velg miljøet og selskapet som inneholder dataene du vil koble til.</span><span class="sxs-lookup"><span data-stu-id="be78f-116">Choose the environment and company that contains the data you want to connect to.</span></span> <span data-ttu-id="be78f-117">Nå skal du se en liste over APIer.</span><span class="sxs-lookup"><span data-stu-id="be78f-117">Next, you will be presented with a list of APIs.</span></span> <span data-ttu-id="be78f-118">Velg en **API** du vil koble til.</span><span class="sxs-lookup"><span data-stu-id="be78f-118">Select the **API** you want to connect to.</span></span>

<span data-ttu-id="be78f-119">Disse såkalte tabellene er en del av [!INCLUDE [prodshort](includes/prodshort.md)]-API-en.</span><span class="sxs-lookup"><span data-stu-id="be78f-119">These so-called tables are part of the [!INCLUDE [prodshort](includes/prodshort.md)] API.</span></span> <span data-ttu-id="be78f-120">Du trenger ikke konfigurere endepunktene selv, [!INCLUDE [prodshort](includes/prodshort.md)]-koblingen for PowerApps gjør det for deg.</span><span class="sxs-lookup"><span data-stu-id="be78f-120">You do not have to configure the end points yourself - the [!INCLUDE [prodshort](includes/prodshort.md)] connector for PowerApps does it for you.</span></span>  

    If you want to include data from other tables in [!INCLUDE [prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE [prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in PowerApps. For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).  

<span data-ttu-id="be78f-121">Nå har du koblet til [!INCLUDE [prodshort](includes/prodshort.md)]-dataene og er klar til å begynne å bygge din PowerApp.</span><span class="sxs-lookup"><span data-stu-id="be78f-121">At this point, you have successfully connected to your [!INCLUDE [prodshort](includes/prodshort.md)] data and are ready to begin building your PowerApp.</span></span> <span data-ttu-id="be78f-122">Du kan legge til flere skjermbilder og koble til flere data fra [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="be78f-122">You can add additional screens and connect to additional data from your [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="be78f-123">Hvis du vil ha mer informasjon, kan du se [Opprette en lerretsapp fra en mal i PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).</span><span class="sxs-lookup"><span data-stu-id="be78f-123">For more information, see [Create a canvas app from a template in PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).</span></span>  

<span data-ttu-id="be78f-124">Når du har utformet og bygd appen, kan du dele den med kollegene dine.</span><span class="sxs-lookup"><span data-stu-id="be78f-124">When you have designed and built your app, you can share it with your colleagues.</span></span> <span data-ttu-id="be78f-125">Hvis du vil ha mer informasjon, kan du se [Lagre og publisere en lerretsapp i PowerApps](/powerapps/maker/canvas-apps/save-publish-app).</span><span class="sxs-lookup"><span data-stu-id="be78f-125">For more information, see [Save and publish a canvas app in PowerApps](/powerapps/maker/canvas-apps/save-publish-app).</span></span>  

> [!NOTE]
> <span data-ttu-id="be78f-126">Hvis du vil koble til [!INCLUDE [prodshort](includes/prodshort.md)] lokalt, må du velge **Business Central (lokalt)**-koblingen i trinn 3.</span><span class="sxs-lookup"><span data-stu-id="be78f-126">If you want to connect to [!INCLUDE [prodshort](includes/prodshort.md)] on-premises, then you must choose the **Business Central (on-premises)** connector in step 3.</span></span>  

## <a name="see-also"></a><span data-ttu-id="be78f-127">Se også</span><span class="sxs-lookup"><span data-stu-id="be78f-127">See Also</span></span>

[<span data-ttu-id="be78f-128">Opprette en lerretsapp fra en mal i PowerApps</span><span class="sxs-lookup"><span data-stu-id="be78f-128">Create a canvas app from a template in PowerApps</span></span>](/powerapps/maker/canvas-apps/get-started-test-drive)  
[<span data-ttu-id="be78f-129">Komme i gang</span><span class="sxs-lookup"><span data-stu-id="be78f-129">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="be78f-130">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="be78f-130">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="be78f-131">[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="be78f-131">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="be78f-132">Finans</span><span class="sxs-lookup"><span data-stu-id="be78f-132">Finance</span></span>](finance.md)  
[<span data-ttu-id="be78f-133">Komme i gang med å utvikle tilkoblingsapper for Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="be78f-133">Getting Started Developing Connect Apps for Dynamics 365 Business Central</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
