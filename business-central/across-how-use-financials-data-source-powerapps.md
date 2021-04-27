---
title: Bruk dataene til å lage en app | Microsoft-dokumenter
description: Du kan gjøre Business Central-dataene tilgjengelige som en datakilde og angi en OData-URL-adresse til webtjenestene dine for å utvikle en forretningsapp ved hjelp av Power Apps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 25607473e20bca8cec8cd65e2e808e12dda47869
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774539"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a><span data-ttu-id="2b8a4-103">Koble til Business Central-dataene for å utvikle en forretningsapp ved hjelp av Power Apps</span><span class="sxs-lookup"><span data-stu-id="2b8a4-103">Connecting to Your Business Central Data to Build a Business App Using Power Apps</span></span>

<span data-ttu-id="2b8a4-104">Du kan gjøre [!INCLUDE[prod_short](includes/prod_short.md)]-data tilgjengelige som en datakilde i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="2b8a4-104">You can make your [!INCLUDE[prod_short](includes/prod_short.md)] data available as a data source in Power Apps.</span></span>  

> [!NOTE]  
> <span data-ttu-id="2b8a4-105">Du må ha en gyldig konto med [!INCLUDE[prod_short](includes/prod_short.md)] og med Power Apps.</span><span class="sxs-lookup"><span data-stu-id="2b8a4-105">You must have a valid account with [!INCLUDE[prod_short](includes/prod_short.md)] and with Power Apps.</span></span>  

## <a name="to-add-prod_short-as-a-data-source-in-power-apps"></a><span data-ttu-id="2b8a4-106">Legge til [!INCLUDE[prod_short](includes/prod_short.md)] som en datakilde i Power Apps</span><span class="sxs-lookup"><span data-stu-id="2b8a4-106">To add [!INCLUDE[prod_short](includes/prod_short.md)] as a data source in Power Apps</span></span>

1. <span data-ttu-id="2b8a4-107">I leseren, kan du gå til [powerapps.microsoft.com](https://powerapps.microsoft.com/), og deretter logge på.</span><span class="sxs-lookup"><span data-stu-id="2b8a4-107">In your browser, navigate to [powerapps.microsoft.com](https://powerapps.microsoft.com/), and then sign in.</span></span>
2. <span data-ttu-id="2b8a4-108">På startsiden, i **Start fra data**-delen, velger du flisen **Andre data kilder**.</span><span class="sxs-lookup"><span data-stu-id="2b8a4-108">On the Home page, in the **Start from data** section, choose the **Other data sources** tile.</span></span>  

    <span data-ttu-id="2b8a4-109">Dette åpner Power Apps Studio.</span><span class="sxs-lookup"><span data-stu-id="2b8a4-109">This opens Power Apps Studio.</span></span> <span data-ttu-id="2b8a4-110">Ved første pålogging må du angi landet/området.</span><span class="sxs-lookup"><span data-stu-id="2b8a4-110">On first login, you must specify the country/region.</span></span>  
3. <span data-ttu-id="2b8a4-111">Velg **Business Central** i listen over tilgjengelige tilkoblinger, og velg deretter **Opprett**-knappen.</span><span class="sxs-lookup"><span data-stu-id="2b8a4-111">In the list of available connections, choose **Business Central**, and then choose the **Create** button.</span></span>

    <span data-ttu-id="2b8a4-112">Power Apps kobler til [!INCLUDE[prod_short](includes/prod_short.md)] med legitimasjonen du logget på med.</span><span class="sxs-lookup"><span data-stu-id="2b8a4-112">Power Apps will connect to your [!INCLUDE[prod_short](includes/prod_short.md)] using the credentials that you are signed in with.</span></span> <span data-ttu-id="2b8a4-113">Hvis du ikke er administrator i [!INCLUDE[prod_short](includes/prod_short.md)], må du kanskje logge på med en annen konto.</span><span class="sxs-lookup"><span data-stu-id="2b8a4-113">If you are not an administrator of your [!INCLUDE[prod_short](includes/prod_short.md)], you may have to sign in with another account.</span></span>  

4. <span data-ttu-id="2b8a4-114">Power Apps viser en liste over *Miljøer og selskaper* som er tilgjengelige fra [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="2b8a4-114">Power Apps will display a list of *Environments and companies* that are available from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="2b8a4-115">Velg miljøet og selskapet som inneholder dataene du vil koble til, for ekssempel *PRODUKSJON – Mitt selskap*.</span><span class="sxs-lookup"><span data-stu-id="2b8a4-115">Choose the environment and company that contains the data you want to connect to, such as *PRODUCTION - My Company*.</span></span>  

5. <span data-ttu-id="2b8a4-116">Deretter vises en liste over tabeller som vises som en del av API-et for ditt miljø.</span><span class="sxs-lookup"><span data-stu-id="2b8a4-116">Next, you will be presented with a list of tables that are exposed as part of the API for your environment.</span></span> <span data-ttu-id="2b8a4-117">Velg tabellen du vil koble til, og velg deretter **Koble til**.</span><span class="sxs-lookup"><span data-stu-id="2b8a4-117">Select the table that you want to connect to, and then choose **Connect**.</span></span>

<span data-ttu-id="2b8a4-118">Disse tabellene vises som endepunkter av [!INCLUDE[prod_short](includes/prod_short.md)]-koblingen for Power Apps.</span><span class="sxs-lookup"><span data-stu-id="2b8a4-118">These so-called tables are exposed as endpoints by the [!INCLUDE[prod_short](includes/prod_short.md)] connector for Power Apps.</span></span>  

> [!NOTE]
> <span data-ttu-id="2b8a4-119">Hvis du vil inkludere data fra andre tabeller i [!INCLUDE[prod_short](includes/prod_short.md)] i appen, må du samarbeide med en utvikler for å definere en egendefinert API i [!INCLUDE[prod_short](includes/prod_short.md)], og deretter forbruke denne tilpassede API-en via en egendefinert kobling i Power Apps.</span><span class="sxs-lookup"><span data-stu-id="2b8a4-119">If you want to include data from other tables in [!INCLUDE[prod_short](includes/prod_short.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE[prod_short](includes/prod_short.md)] and then consume that custom API through a custom connector in Power Apps.</span></span> <span data-ttu-id="2b8a4-120">Hvis du vil ha mer informasjon, kan du se [Opprette en egendefinert kobling fra grunnen av](/connectors/custom-connectors/define-blank).</span><span class="sxs-lookup"><span data-stu-id="2b8a4-120">For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).</span></span>  

<span data-ttu-id="2b8a4-121">Nå har du koblet til [!INCLUDE[prod_short](includes/prod_short.md)]-dataene og er klar til å begynne å bygge din PowerApp.</span><span class="sxs-lookup"><span data-stu-id="2b8a4-121">At this point, you have successfully connected to your [!INCLUDE[prod_short](includes/prod_short.md)] data and are ready to begin building your PowerApp.</span></span> <span data-ttu-id="2b8a4-122">Du kan legge til flere skjermbilder og koble til flere data fra [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="2b8a4-122">You can add additional screens and connect to additional data from your [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="2b8a4-123">Hvis du vil ha mer informasjon, kan du se [Opprette en lerretsapp fra et eksempel i Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).</span><span class="sxs-lookup"><span data-stu-id="2b8a4-123">For more information, see [Create a canvas app from a sample in Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).</span></span>  

<span data-ttu-id="2b8a4-124">Når du har utformet og bygd appen, kan du dele den med kollegene dine.</span><span class="sxs-lookup"><span data-stu-id="2b8a4-124">When you have designed and built your app, you can share it with your colleagues.</span></span> <span data-ttu-id="2b8a4-125">Hvis du vil ha mer informasjon, kan du se [Lagre og publisere en lerretsapp i Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span><span class="sxs-lookup"><span data-stu-id="2b8a4-125">For more information, see [Save and publish a canvas app in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span></span>  

> [!NOTE]
> <span data-ttu-id="2b8a4-126">Hvis du vil koble til [!INCLUDE[prod_short](includes/prod_short.md)] lokalt, må du velge **Business Central (lokalt)**-koblingen i trinn 3.</span><span class="sxs-lookup"><span data-stu-id="2b8a4-126">If you want to connect to [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, then you must choose the **Business Central (on-premises)** connector in step 3.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2b8a4-127">Se også</span><span class="sxs-lookup"><span data-stu-id="2b8a4-127">See Also</span></span>

[<span data-ttu-id="2b8a4-128">Opprette en lerretsapp fra en mal i Power Apps</span><span class="sxs-lookup"><span data-stu-id="2b8a4-128">Create a canvas app from a template in Power Apps</span></span>](/powerapps/maker/canvas-apps/get-started-test-drive)  
[<span data-ttu-id="2b8a4-129">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="2b8a4-129">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="2b8a4-130">[Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="2b8a4-130">[Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span></span>  
[<span data-ttu-id="2b8a4-131">Komme i gang med å utvikle tilkoblingsapper for Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="2b8a4-131">Getting Started Developing Connect Apps for Dynamics 365 Business Central</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  


[!INCLUDE[footer-include](includes/footer-banner.md)]