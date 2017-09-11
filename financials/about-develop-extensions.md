---
title: Tilpasse Dynamics 365 for Financials | Microsoft-dokumentasjon
description: Bygg, vis og frem appen og utvidelsene dine for Dynamics 365 for Financials.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: cc355c7b4cd51412ec0b5c95398c2d7b50a13f94
ms.contentlocale: nb-no
ms.lasthandoff: 07/07/2017


---
# <a name="extending-included365finlongincludesd365finlongmdmd"></a><span data-ttu-id="54fe0-103">Utvide [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]</span><span class="sxs-lookup"><span data-stu-id="54fe0-103">Extending [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]</span></span>
<span data-ttu-id="54fe0-104">Det finnes mange fordeler med å bruke [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] som en plattform for apputviklere:</span><span class="sxs-lookup"><span data-stu-id="54fe0-104">There are plenty of benefits of using [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] as a platform for App builders:</span></span>

* <span data-ttu-id="54fe0-105">Få en rikere [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], en anerkjent Microsoft online-løsning, med din ekspertise</span><span class="sxs-lookup"><span data-stu-id="54fe0-105">Enrich [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], a proven Microsoft online solution, with your expertise</span></span>  
* <span data-ttu-id="54fe0-106">Dra nytte av Dynamics 365-merket – et merke som millioner av brukere kjenner og stoler på</span><span class="sxs-lookup"><span data-stu-id="54fe0-106">Leverage the Dynamics 365 brand – a brand that millions of users know and trust</span></span>  
* <span data-ttu-id="54fe0-107">Nå flere kunder for dine businessapper med [Microsoft AppSource](https://appsource.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="54fe0-107">Reach more customers for your business apps with [Microsoft AppSource](https://appsource.microsoft.com/)</span></span>  
* <span data-ttu-id="54fe0-108">Oppnå mer med en plattform som gir moderne opplevelse og tilbyr skala</span><span class="sxs-lookup"><span data-stu-id="54fe0-108">Achieve more with a platform that delivers a modern experience and offers scale</span></span>  
* <span data-ttu-id="54fe0-109">Sammen med intelligente businessapper som PowerApps, Flow, Power BI, Cortana Intelligence og mange flere</span><span class="sxs-lookup"><span data-stu-id="54fe0-109">Bundle with intelligent business apps such as PowerApps, Flow, Power BI, Cortana Intelligence, and many more</span></span>  

## <a name="to-bring-your-included365finincludesd365finmdmd-app-into-appsource"></a><span data-ttu-id="54fe0-110">Å få din [!INCLUDE[d365fin](includes/d365fin_md.md)]-app til AppSource:</span><span class="sxs-lookup"><span data-stu-id="54fe0-110">To bring your [!INCLUDE[d365fin](includes/d365fin_md.md)] app into AppSource:</span></span>
+ <span data-ttu-id="54fe0-111">Opprette kontoene</span><span class="sxs-lookup"><span data-stu-id="54fe0-111">Create your accounts</span></span>  
<span data-ttu-id="54fe0-112">Vi vil at du skal ha tilgang til alle nødvendige verktøy!</span><span class="sxs-lookup"><span data-stu-id="54fe0-112">We want you to have access to all the necessary tools!</span></span> <span data-ttu-id="54fe0-113">Du må ha en Microsoft-Partner nettverks-ID, en utviklerkonto og en PSBC-konto.</span><span class="sxs-lookup"><span data-stu-id="54fe0-113">You must have a Microsoft Partner Network ID, a Developer account, and a PSBC account.</span></span>
<span data-ttu-id="54fe0-114">Hvis du vil ha mer informasjon om hvordan du kan få kontoene på plass, kan du få den [Create your accounts.pdf](https://go.microsoft.com/fwlink/?linkid=841514) dokumentet fra Download Center.</span><span class="sxs-lookup"><span data-stu-id="54fe0-114">For more information about how you can get your accounts in place, get the [Create your accounts.pdf](https://go.microsoft.com/fwlink/?linkid=841514) document from the Download Center.</span></span>

+ <span data-ttu-id="54fe0-115">Engasjere oss om din appidé</span><span class="sxs-lookup"><span data-stu-id="54fe0-115">Engage with us about your app idea</span></span>  
<span data-ttu-id="54fe0-116">Del din [!INCLUDE[d365fin](includes/d365fin_md.md)]-appidé med oss på Microsoft-AppSource!</span><span class="sxs-lookup"><span data-stu-id="54fe0-116">Share your [!INCLUDE[d365fin](includes/d365fin_md.md)] app idea with us on Microsoft AppSource!</span></span> <span data-ttu-id="54fe0-117">Når du har sendt din idé, vil vi forbindes med deg og gi deg alt du trenger for å begynne å arbeide på appen.</span><span class="sxs-lookup"><span data-stu-id="54fe0-117">After submitting your idea, we will engage with you and provide you with everything you need to start working on your app.</span></span>
<span data-ttu-id="54fe0-118">Hvis du vil ha mer informasjon om alle trinnene, kan du få den [Engage with us about your app idea document.pdf](https://go.microsoft.com/fwlink/?linkid=841515) dokumentet fra Download Center.</span><span class="sxs-lookup"><span data-stu-id="54fe0-118">For more information about all the steps, get the [Engage with us about your app idea document.pdf](https://go.microsoft.com/fwlink/?linkid=841515) document from the Download Center.</span></span>

+ <span data-ttu-id="54fe0-119">Utvikle de tekniske aspektene for appen</span><span class="sxs-lookup"><span data-stu-id="54fe0-119">Develop the technical aspects of your app</span></span>    
<span data-ttu-id="54fe0-120">Når du har satt opp din egen apputviklingsmiljø, kan du utvikle appen.</span><span class="sxs-lookup"><span data-stu-id="54fe0-120">After you have set up your own app development environment, you can develop your app.</span></span>
<span data-ttu-id="54fe0-121">Hvis du vil ha mer informasjon om alt du trenger å vite om hvordan du utvikler tekniske aspekter i din [!INCLUDE[d365fin](includes/d365fin_md.md)]-app, får den [Develop the technical aspects of your app.pdf](https://go.microsoft.com/fwlink/?linkid=841516) dokumentet fra Download Center.</span><span class="sxs-lookup"><span data-stu-id="54fe0-121">For more information about everything you need to know about how to develop the technical aspects of your [!INCLUDE[d365fin](includes/d365fin_md.md)] app, get the [Develop the technical aspects of your app.pdf](https://go.microsoft.com/fwlink/?linkid=841516) document from the Download Center.</span></span>

+ <span data-ttu-id="54fe0-122">Utvikle markedsføringsaspektene for appen</span><span class="sxs-lookup"><span data-stu-id="54fe0-122">Develop the marketing aspects of your app</span></span>  
<span data-ttu-id="54fe0-123">Ganske enkelt vise din apps funksjoner og funksjonalitet vil ikke konvertere kundeemner til kjøpere.</span><span class="sxs-lookup"><span data-stu-id="54fe0-123">Simply listing your app's features and functionality will not convert prospects to buyers.</span></span> <span data-ttu-id="54fe0-124">Hvis du vil ha mer informasjon om hvordan du best å markedsføre appen på AppSource-markedsplassen, kan du få den [Develop the marketing aspects of your app.pdf](https://go.microsoft.com/fwlink/?linkid=841518) fra Download Center.</span><span class="sxs-lookup"><span data-stu-id="54fe0-124">For more information about how to best market your app in the AppSource marketplace, get the [Develop the marketing aspects of your app.pdf](https://go.microsoft.com/fwlink/?linkid=841518) from the Download Center.</span></span>

+ <span data-ttu-id="54fe0-125">Publisere appen</span><span class="sxs-lookup"><span data-stu-id="54fe0-125">Publish your app</span></span>  
<span data-ttu-id="54fe0-126">Før vi publiserer, vil vi samarbeide med deg for å sikre at din app skiller seg ut på Microsoft AppSource og din egen målside!</span><span class="sxs-lookup"><span data-stu-id="54fe0-126">Before we publish, we will collaborate with you to ensure that your app stands out on Microsoft AppSource and on your own landing page!</span></span> <span data-ttu-id="54fe0-127">Vi må validere appen for å sikre at den er godt markedsført, pålitelig og oppdatert.</span><span class="sxs-lookup"><span data-stu-id="54fe0-127">We need to validate your app to ensure it is marketed well, trustworthy, and up to date.</span></span>
<span data-ttu-id="54fe0-128">Hvis du vil ha mer informasjon om valideringsprosessen og hvordan du publiserer appen, kan du få den [Publish your app.pdf](https://go.microsoft.com/fwlink/?linkid=841517) dokumentet fra Download Center.</span><span class="sxs-lookup"><span data-stu-id="54fe0-128">For more information about the validation process and how to publish your app, get the [Publish your app.pdf](https://go.microsoft.com/fwlink/?linkid=841517) document from the Download Center.</span></span>

## <a name="need-help"></a><span data-ttu-id="54fe0-129">Trenger du hjelp?</span><span class="sxs-lookup"><span data-stu-id="54fe0-129">Need help?</span></span>
<span data-ttu-id="54fe0-130">Hvis du vil ha noen råd, kan du kontakte en appekspert fra listen nedenfor:</span><span class="sxs-lookup"><span data-stu-id="54fe0-130">If you would like some coaching, you can contact an app subject matter expert from the following list:</span></span>

* <span data-ttu-id="54fe0-131">Sky klar programvare, [http://cloud-ready-software.com](http://cloud-ready-software.com/)</span><span class="sxs-lookup"><span data-stu-id="54fe0-131">Cloud Ready Software, [http://cloud-ready-software.com](http://cloud-ready-software.com/)</span></span>  
* <span data-ttu-id="54fe0-132">Dynamics App Alliance, [http://dynamicsappalliance.com](http://dynamicsappalliance.com/)</span><span class="sxs-lookup"><span data-stu-id="54fe0-132">Dynamics App Alliance, [http://dynamicsappalliance.com](http://dynamicsappalliance.com/)</span></span>

<span data-ttu-id="54fe0-133">Partnere i denne listen:</span><span class="sxs-lookup"><span data-stu-id="54fe0-133">Partners in this list:</span></span>

* <span data-ttu-id="54fe0-134">Vises alfabetisk</span><span class="sxs-lookup"><span data-stu-id="54fe0-134">Are listed alphabetically</span></span>  
* <span data-ttu-id="54fe0-135">Hjelper eller har hjulpet et minimum av tre partnere med å hente apper til Microsoft AppSource</span><span class="sxs-lookup"><span data-stu-id="54fe0-135">Are assisting or have assisted a minimum of three partners with bringing apps into Microsoft AppSource</span></span>  
* <span data-ttu-id="54fe0-136">Har en pakket tjeneste tilgjengelig (og som finnes på nettstedet) om appveiledningen som de tilbyr</span><span class="sxs-lookup"><span data-stu-id="54fe0-136">Have a packaged service available (and listed on their website) about the app guidance that they provide</span></span>  

<span data-ttu-id="54fe0-137">Hvis du mener at du skal være oppført som en appservicepartner, må du ta kontakt med [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="54fe0-137">If you believe you should be listed as an app service partner, don't hesitate to reach out to [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span></span>

## <a name="questions"></a><span data-ttu-id="54fe0-138">Spørsmål?</span><span class="sxs-lookup"><span data-stu-id="54fe0-138">Questions?</span></span>
<span data-ttu-id="54fe0-139">Dette [FAQ](https://go.microsoft.com/fwlink/?linkid=841520) svarer til de mest vanlige spørsmålene du kan ha om apper for [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="54fe0-139">This [FAQ](https://go.microsoft.com/fwlink/?linkid=841520) responds to the most common questions you might have about apps for [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="54fe0-140">Hvis du har flere spørsmål, ta kontakt med den nærmeste Microsoft-forhandleren eller send e-post til [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="54fe0-140">If you have further questions, don't hesitate to contact your local Microsoft representative or email [d365-smb@microsoft.com](mailto:d365-smb@microsoft.com).</span></span>

## <a name="further-resources"></a><span data-ttu-id="54fe0-141">Andre ressurser</span><span class="sxs-lookup"><span data-stu-id="54fe0-141">Further Resources</span></span>
<span data-ttu-id="54fe0-142">Finner du ytterligere ressurser for programutvikling på vår [DLP-emneside](https://mbspartner.microsoft.com/BFI/Topic/76) DLP-emneside.</span><span class="sxs-lookup"><span data-stu-id="54fe0-142">Please find further resources for app development on our [DLP topic page](https://mbspartner.microsoft.com/BFI/Topic/76) DLP topic page.</span></span> <span data-ttu-id="54fe0-143">Noen utvalgte er tilgjengelige under:</span><span class="sxs-lookup"><span data-stu-id="54fe0-143">Some selected ones are available below:</span></span>
-   [<span data-ttu-id="54fe0-144">Brukerregistrering og påfølgende betaling </span><span class="sxs-lookup"><span data-stu-id="54fe0-144">User Registration and Subsequent Billing </span></span>](http://download.microsoft.com/download/3/2/0/320D0286-8810-4A8F-B7DD-523ED87D441B/FAQ on apps for Dynamics 365 for Financials.pdf)



## <a name="see-also"></a><span data-ttu-id="54fe0-145">Se også</span><span class="sxs-lookup"><span data-stu-id="54fe0-145">See Also</span></span>
<span data-ttu-id="54fe0-146">[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="54fe0-146">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="54fe0-147">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="54fe0-147">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="54fe0-148">https://appsource.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="54fe0-148">https://appsource.microsoft.com</span></span>](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365-for-financials&page=1)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
