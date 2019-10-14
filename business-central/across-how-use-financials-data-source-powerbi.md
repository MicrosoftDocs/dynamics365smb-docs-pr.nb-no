---
title: Bruke Business Central i Power BI-rapporter | Microsoft Docs
description: Gjør dataene tilgjengelige som en datakilde i Power BI, og bygg kraftige rapporter om status for din bedrift.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: b57b87dd8cdc9390ed5b1b7136107639f689c192
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304999"
---
# <a name="using-include-prodlongincludesprodlongmd-as-power-bi-data-source-for-building-reports"></a><span data-ttu-id="6d243-103">Bruke [!INCLUDE [prodlong](includes/prodlong.md)] som datakilde for Power BI for å bygge rapporter</span><span class="sxs-lookup"><span data-stu-id="6d243-103">Using [!INCLUDE [prodlong](includes/prodlong.md)] as Power BI Data Source for Building Reports</span></span>

<span data-ttu-id="6d243-104">Gjør [!INCLUDE[prodlong](includes/prodlong.md)]-dataene tilgjengelige som en datakilde i Power BI, og bygg kraftige rapporter om status for din bedrift.</span><span class="sxs-lookup"><span data-stu-id="6d243-104">You can make your [!INCLUDE[prodlong](includes/prodlong.md)] data available as a data source in Power BI and build powerful reports of the state of your business.</span></span>  

<span data-ttu-id="6d243-105">Du må ha en gyldig konto med [!INCLUDE[prodshort](includes/prodshort.md)] og med Power BI.</span><span class="sxs-lookup"><span data-stu-id="6d243-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power BI.</span></span> <span data-ttu-id="6d243-106">Du må også laste ned [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span><span class="sxs-lookup"><span data-stu-id="6d243-106">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span></span> <span data-ttu-id="6d243-107">Hvis du vil ha mer informasjon, kan du se [Hurtigstart: Koble til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span><span class="sxs-lookup"><span data-stu-id="6d243-107">For more information, see [Quickstart: Connect to data in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span></span>  

## <a name="to-add-includeprodshortincludesprodshortmd-as-a-data-source-in-power-bi-desktop"></a><span data-ttu-id="6d243-108">Legge til [!INCLUDE[prodshort](includes/prodshort.md)] som en datakilde i Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="6d243-108">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power BI Desktop</span></span>

1. <span data-ttu-id="6d243-109">I Power BI Desktop, i den venstre navigasjonsruten, velger du **Hent Data**.</span><span class="sxs-lookup"><span data-stu-id="6d243-109">In Power BI Desktop, in the left navigation pane, choose **Get Data**.</span></span>
2. <span data-ttu-id="6d243-110">På siden **Hent Data** velger du **Online Services**, **Microsoft Dynamics 365 Business Central** og deretter **Koble til**-knappen.</span><span class="sxs-lookup"><span data-stu-id="6d243-110">On the **Get Data** page, choose **Online Services**, choose **Microsoft Dynamics 365 Business Central**, and then choose the **Connect** button.</span></span>
3. <span data-ttu-id="6d243-111">Power BI viser en veiviser som veileder deg gjennom tilkoblingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="6d243-111">Power BI displays a wizard that will guide you through the connection process.</span></span> <span data-ttu-id="6d243-112">Du blir bedt om å logge på [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="6d243-112">You will be prompted to sign into [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="6d243-113">Velg **Logg på** og kontoen du vil logge på som.</span><span class="sxs-lookup"><span data-stu-id="6d243-113">Select **Sign in** and choose the account you would like to sign in as.</span></span> <span data-ttu-id="6d243-114">Dette må være samme konto som du bruker til å logge på [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="6d243-114">This should be the same account you sign into [!INCLUDE [prodshort](includes/prodshort.md)] with.</span></span>
4. <span data-ttu-id="6d243-115">Velg **Koble til**-knappen for å fortsette.</span><span class="sxs-lookup"><span data-stu-id="6d243-115">Choose the **Connect** button to continue.</span></span> <span data-ttu-id="6d243-116">Veiviseren for Power BI viser en liste over Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]-miljøer, -selskaper og -datakilder.</span><span class="sxs-lookup"><span data-stu-id="6d243-116">The Power BI wizard shows a list of Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)] environments, companies and data sources.</span></span> <span data-ttu-id="6d243-117">Disse datakildene representerer alle webtjenester som du har publisert fra hver leier/selskap i Microsoft [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="6d243-117">These data source represent all the web services that you have published from each tenant/company in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>
5. <span data-ttu-id="6d243-118">Alternativt, opprette en ny web service URL i [!INCLUDE [prodshort](includes/prodshort.md)] ved hjelp av **Opprett datasett** på siden **Web Services** ved hjelp av **Sett opp rapportering** assistert installasjonsveiledningen eller ved å velge **Rediger i Excel** i lister.</span><span class="sxs-lookup"><span data-stu-id="6d243-118">Alternatively, create a new web service URL in [!INCLUDE [prodshort](includes/prodshort.md)] by using the **Create Data Set** action on the **Web Services** page, using the **Set Up Reporting** Assisted Setup guide, or by choosing the **Edit in Excel** action in any lists.</span></span>
6. <span data-ttu-id="6d243-119">Angi hvilke data du vil legge til datamodellen, og velg deretter **Last inn**-knappen.</span><span class="sxs-lookup"><span data-stu-id="6d243-119">Specify the data you want to add to your data model, and then choose the **Load** button.</span></span>
7. <span data-ttu-id="6d243-120">Gjenta de forrige trinnene for å legge til flere [!INCLUDE [prodshort](includes/prodshort.md)] eller andre data i Power BI-datamodellen.</span><span class="sxs-lookup"><span data-stu-id="6d243-120">Repeat the previous steps to add additional [!INCLUDE [prodshort](includes/prodshort.md)], or other data, to your Power BI data model.</span></span>

> [!NOTE]  
> <span data-ttu-id="6d243-121">Når du er koblet til [!INCLUDE [prodshort](includes/prodshort.md)], blir du ikke bedt på nytt om å logge på.</span><span class="sxs-lookup"><span data-stu-id="6d243-121">Once you have successfully connected to [!INCLUDE [prodshort](includes/prodshort.md)], you will not be prompted again to sign in.</span></span>

<span data-ttu-id="6d243-122">Når dataene er lastet inn, vil de vises i høyre navigering på siden.</span><span class="sxs-lookup"><span data-stu-id="6d243-122">Once the data is loaded it will appear in the right navigation on the page.</span></span> <span data-ttu-id="6d243-123">Nå har du koblet til [!INCLUDE [prodshort](includes/prodshort.md)]-dataene og er klar til å begynne å bygge din Power BI-rapport.</span><span class="sxs-lookup"><span data-stu-id="6d243-123">At this point, you have successfully connected to your [!INCLUDE [prodshort](includes/prodshort.md)] data and are ready to begin building your Power BI report.</span></span>  

<span data-ttu-id="6d243-124">Før du lager rapporten, anbefales det at du importerer [!INCLUDE [prodshort](includes/prodshort.md)]-teamfilen.</span><span class="sxs-lookup"><span data-stu-id="6d243-124">Before building your report, we recommend that you import the [!INCLUDE [prodshort](includes/prodshort.md)] theme file.</span></span>  <span data-ttu-id="6d243-125">Temafilen oppretter en fargepalett slik at du kan lage rapporter med samme fargestil som [!INCLUDE [prodshort](includes/prodshort.md)]-appene uten at du må definere egendefinerte farger for hver visuell effekt.</span><span class="sxs-lookup"><span data-stu-id="6d243-125">The theme file will create a color palette so that you can build reports with the same color styling as the [!INCLUDE [prodshort](includes/prodshort.md)] apps without requiring you to define custom colors for each visual.</span></span>

<span data-ttu-id="6d243-126">Hvis du vil ha mer informasjon, kan du se [Power BI-dokumentasjon](/power-bi/consumer/power-bi-consumer-landing/).</span><span class="sxs-lookup"><span data-stu-id="6d243-126">For more information, see the [Power BI documentation](/power-bi/consumer/power-bi-consumer-landing/).</span></span>

## <a name="see-also"></a><span data-ttu-id="6d243-127">Se også</span><span class="sxs-lookup"><span data-stu-id="6d243-127">See Also</span></span>

[<span data-ttu-id="6d243-128">Aktivere forretningsdata for Power BI</span><span class="sxs-lookup"><span data-stu-id="6d243-128">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
[<span data-ttu-id="6d243-129">Forretningsintelligens</span><span class="sxs-lookup"><span data-stu-id="6d243-129">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="6d243-130">Komme i gang</span><span class="sxs-lookup"><span data-stu-id="6d243-130">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="6d243-131">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="6d243-131">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="6d243-132">[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="6d243-132">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="6d243-133">Finans</span><span class="sxs-lookup"><span data-stu-id="6d243-133">Finance</span></span>](finance.md)  
[<span data-ttu-id="6d243-134">Hurtigstart: Koble til data i Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="6d243-134">Quickstart: Connect to data in Power BI Desktop</span></span>](/power-bi/desktop-quickstart-connect-to-data)  
