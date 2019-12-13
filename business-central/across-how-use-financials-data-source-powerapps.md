---
title: Bruk dataene til å lage en app | Microsoft-dokumenter
description: Du kan gjøre Business Central-dataene tilgjengelige som en datakilde og angi en OData-URL-adresse til webtjenestene dine for å utvikle en forretningsapp ved hjelp av Power Apps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 11/20/2019
ms.author: edupont
ms.openlocfilehash: 9cf587dca8224e742ecbde30bcabc35697bb6f2a
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881003"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a><span data-ttu-id="21612-103">Koble til Business Central-dataene for å utvikle en forretningsapp ved hjelp av Power Apps</span><span class="sxs-lookup"><span data-stu-id="21612-103">Connecting to Your Business Central Data to Build a Business App Using Power Apps</span></span>

<span data-ttu-id="21612-104">Du kan gjøre [!INCLUDE[prodshort](includes/prodshort.md)]-data tilgjengelige som en datakilde i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="21612-104">You can make your [!INCLUDE[prodshort](includes/prodshort.md)] data available as a data source in Power Apps.</span></span>  

> [!NOTE]  
> <span data-ttu-id="21612-105">Du må ha en gyldig konto med [!INCLUDE[prodshort](includes/prodshort.md)] og med Power Apps.</span><span class="sxs-lookup"><span data-stu-id="21612-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power Apps.</span></span>  

## <a name="to-add-includeprodshortincludesprodshortmd-as-a-data-source-in-power-apps"></a><span data-ttu-id="21612-106">Legge til [!INCLUDE[prodshort](includes/prodshort.md)] som en datakilde i Power Apps</span><span class="sxs-lookup"><span data-stu-id="21612-106">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power Apps</span></span>

1. <span data-ttu-id="21612-107">I leseren, kan du gå til [powerapps.microsoft.com](https://powerapps.microsoft.com/), og deretter logge på.</span><span class="sxs-lookup"><span data-stu-id="21612-107">In your browser, navigate to [powerapps.microsoft.com](https://powerapps.microsoft.com/), and then sign in.</span></span>
2. <span data-ttu-id="21612-108">På startsiden velger du **Apper**, **Opprett en app** og **Lerret** for å opprette en ny lerretsapp.</span><span class="sxs-lookup"><span data-stu-id="21612-108">On the Home page, choose the **Apps**, **Create an app** and **Canvas** to create a new canvas app.</span></span> <span data-ttu-id="21612-109">Denne appen blir utformet for bruk på en mobil enhet, men du kan også velge å bruke en annen mal.</span><span class="sxs-lookup"><span data-stu-id="21612-109">This app will be designed for use on a mobile device, but you can also choose to use another template.</span></span>

    <span data-ttu-id="21612-110">Neste trinn for å opprette en Power App er å velge data.</span><span class="sxs-lookup"><span data-stu-id="21612-110">The next step to create a Power App is to select your data.</span></span> <span data-ttu-id="21612-111">Velg pilikonet og deretter velge **Ny tilkobling** i øvre venstre side av siden.</span><span class="sxs-lookup"><span data-stu-id="21612-111">Choose the Arrow icon then choose the **New connection** option in the upper left side of the page.</span></span>
3. <span data-ttu-id="21612-112">Velg **Business Central** i listen over tilgjengelige tilkoblinger, og velg deretter **Opprett**-knappen.</span><span class="sxs-lookup"><span data-stu-id="21612-112">In the list of available connections, choose **Business Central**, and then choose the **Create** button.</span></span>

    <span data-ttu-id="21612-113">Power Apps vil koble til dine [!INCLUDE [prodshort](includes/prodshort.md)] med legitimasjonen du logget på med.</span><span class="sxs-lookup"><span data-stu-id="21612-113">Power Apps will connect to your [!INCLUDE [prodshort](includes/prodshort.md)] using the credentials that you are signed in with.</span></span> <span data-ttu-id="21612-114">Hvis du ikke er administrator i [!INCLUDE [prodshort](includes/prodshort.md)], må du kanskje logge på med en annen konto.</span><span class="sxs-lookup"><span data-stu-id="21612-114">If you are not an administrator of your [!INCLUDE [prodshort](includes/prodshort.md)], you may have to sign in with another account.</span></span>  

4. <span data-ttu-id="21612-115">Power Apps viser en liste over *Miljøer og selskaper* som er tilgjengelige fra [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="21612-115">Power Apps will display a list of *Environments and companies* that are available from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="21612-116">Velg miljøet og selskapet som inneholder dataene du vil koble til.</span><span class="sxs-lookup"><span data-stu-id="21612-116">Choose the environment and company that contains the data you want to connect to.</span></span> <span data-ttu-id="21612-117">Nå skal du se en liste over APIer.</span><span class="sxs-lookup"><span data-stu-id="21612-117">Next, you will be presented with a list of APIs.</span></span> <span data-ttu-id="21612-118">Velg en **API** du vil koble til.</span><span class="sxs-lookup"><span data-stu-id="21612-118">Select the **API** you want to connect to.</span></span>

<span data-ttu-id="21612-119">Disse såkalte tabellene er en del av [!INCLUDE [prodshort](includes/prodshort.md)]-API-en.</span><span class="sxs-lookup"><span data-stu-id="21612-119">These so-called tables are part of the [!INCLUDE [prodshort](includes/prodshort.md)] API.</span></span> <span data-ttu-id="21612-120">Du trenger ikke konfigurere endepunktene selv, [!INCLUDE [prodshort](includes/prodshort.md)]-koblingen for Power Apps gjør det for deg.</span><span class="sxs-lookup"><span data-stu-id="21612-120">You do not have to configure the end points yourself - the [!INCLUDE [prodshort](includes/prodshort.md)] connector for Power Apps does it for you.</span></span>  

> [!NOTE]
> <span data-ttu-id="21612-121">Hvis du vil inkludere data fra andre tabeller i [!INCLUDE [prodshort](includes/prodshort.md)] i appen, må du samarbeide med en utvikler for å definere en egendefinert API i [!INCLUDE [prodshort](includes/prodshort.md)], og deretter forbruke denne tilpassede API-en via en egendefinert kobling i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="21612-121">If you want to include data from other tables in [!INCLUDE [prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE [prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in Power Apps.</span></span> <span data-ttu-id="21612-122">Hvis du vil ha mer informasjon, kan du se [Opprette en egendefinert kobling fra grunnen av](/connectors/custom-connectors/define-blank).</span><span class="sxs-lookup"><span data-stu-id="21612-122">For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).</span></span>  

<span data-ttu-id="21612-123">Nå har du koblet til [!INCLUDE [prodshort](includes/prodshort.md)]-dataene og er klar til å begynne å bygge din PowerApp.</span><span class="sxs-lookup"><span data-stu-id="21612-123">At this point, you have successfully connected to your [!INCLUDE [prodshort](includes/prodshort.md)] data and are ready to begin building your PowerApp.</span></span> <span data-ttu-id="21612-124">Du kan legge til flere skjermbilder og koble til flere data fra [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="21612-124">You can add additional screens and connect to additional data from your [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="21612-125">Hvis du vil ha mer informasjon, kan du se [Opprette en lerretsapp fra en mal i Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive).</span><span class="sxs-lookup"><span data-stu-id="21612-125">For more information, see [Create a canvas app from a template in Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive).</span></span>  

<span data-ttu-id="21612-126">Når du har utformet og bygd appen, kan du dele den med kollegene dine.</span><span class="sxs-lookup"><span data-stu-id="21612-126">When you have designed and built your app, you can share it with your colleagues.</span></span> <span data-ttu-id="21612-127">Hvis du vil ha mer informasjon, kan du se [Lagre og publisere en lerretsapp i Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span><span class="sxs-lookup"><span data-stu-id="21612-127">For more information, see [Save and publish a canvas app in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span></span>  

> [!NOTE]
> <span data-ttu-id="21612-128">Hvis du vil koble til [!INCLUDE [prodshort](includes/prodshort.md)] lokalt, må du velge **Business Central (lokalt)**-koblingen i trinn 3.</span><span class="sxs-lookup"><span data-stu-id="21612-128">If you want to connect to [!INCLUDE [prodshort](includes/prodshort.md)] on-premises, then you must choose the **Business Central (on-premises)** connector in step 3.</span></span>  

## <a name="see-also"></a><span data-ttu-id="21612-129">Se også</span><span class="sxs-lookup"><span data-stu-id="21612-129">See Also</span></span>

[<span data-ttu-id="21612-130">Opprette en lerretsapp fra en mal i Power Apps</span><span class="sxs-lookup"><span data-stu-id="21612-130">Create a canvas app from a template in Power Apps</span></span>](/powerapps/maker/canvas-apps/get-started-test-drive)  
[<span data-ttu-id="21612-131">Komme i gang</span><span class="sxs-lookup"><span data-stu-id="21612-131">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="21612-132">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="21612-132">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="21612-133">[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="21612-133">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="21612-134">Finans</span><span class="sxs-lookup"><span data-stu-id="21612-134">Finance</span></span>](finance.md)  
[<span data-ttu-id="21612-135">Komme i gang med å utvikle tilkoblingsapper for Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="21612-135">Getting Started Developing Connect Apps for Dynamics 365 Business Central</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
