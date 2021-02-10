---
title: Intelligent innsikt og skymigrering | Microsoft-dokumentasjon
description: Bli tilkoblet intelligent innsikt med Business Central fra din lokale løsning. Lær hvordan du migrerer til skyen.
author: bmeier94
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms. search.keywords: cloud, edge
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a186166e73d4c6dcda01bbda6ac2c88a18b2babb
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753720"
---
# <a name="intelligent-insights-with-prod_short-online"></a><span data-ttu-id="c0978-104">Intelligent innsikt med [!INCLUDE[prod_short](includes/prod_short.md)] Online</span><span class="sxs-lookup"><span data-stu-id="c0978-104">Intelligent Insights with [!INCLUDE[prod_short](includes/prod_short.md)] Online</span></span>

<span data-ttu-id="c0978-105">Som en bruker av [!INCLUDE[prod_short](includes/prod_short.md)] på nettet har du full tilgang til scenarier som er basert på den intelligente skyen, for eksempel KPI-er som er basert på maskinlæring, eller når du viser dataene i Power BI.</span><span class="sxs-lookup"><span data-stu-id="c0978-105">As a user of [!INCLUDE[prod_short](includes/prod_short.md)] online, you have full access to scenarios that are based on the intelligent cloud, such as KPIs that are based on machine learning, or when you view your data in Power BI.</span></span> <span data-ttu-id="c0978-106">Selv om [!INCLUDE[prod_short](includes/prod_short.md)] primært er en skytjeneste, kan også kunder som må kjøre deres arbeidsmengder fullstendig lokalt eller på den intelligente kanten tilkoblet skyen, gjøre dette.</span><span class="sxs-lookup"><span data-stu-id="c0978-106">However, while [!INCLUDE[prod_short](includes/prod_short.md)] is a cloud-first service, also those customers who need to run their workloads fully on-premises or on the intelligent edge connected to the cloud can do so.</span></span>  

<span data-ttu-id="c0978-107">Hvis du er interessert i [!INCLUDE[prod_short](includes/prod_short.md)], kan du registrere deg for en gratis prøveversjon på Internett, eller du kan velge å arbeide med en partner for å distribuere [!INCLUDE[prod_short](includes/prod_short.md)] lokalt på din egen maskinvare.</span><span class="sxs-lookup"><span data-stu-id="c0978-107">If you are interested in [!INCLUDE[prod_short](includes/prod_short.md)], you can sign up for a free trial online, or you can choose to work with a partner to deploy [!INCLUDE[prod_short](includes/prod_short.md)] locally to your own choice of hardware.</span></span> <span data-ttu-id="c0978-108">Du kan deretter bestemme deg for å få intelligent innsikt ved å koble til en leietaker i skyen.</span><span class="sxs-lookup"><span data-stu-id="c0978-108">You can then decide to get intelligent insights by connecting to a tenant in the cloud.</span></span> <span data-ttu-id="c0978-109">Dermed vil dataene fra de lokalt distribuerte replikeringene av [!INCLUDE[prod_short](includes/prod_short.md)] til skyen for scenarier med den intelligente skyen.</span><span class="sxs-lookup"><span data-stu-id="c0978-109">As a result, the data from your [!INCLUDE[prod_short](includes/prod_short.md)] on-premises deployment replicates to the cloud for intelligent cloud scenarios.</span></span>  

<span data-ttu-id="c0978-110">Koble til den intelligente skyen fra en lokal løsning krever at systemansvarlig angir opplysninger om databasen.</span><span class="sxs-lookup"><span data-stu-id="c0978-110">Connecting to the intelligent cloud from an on-premises solution requires your administrator to specify information about your database.</span></span> <span data-ttu-id="c0978-111">Verktøyene som brukes til å koble den lokale distribusjonen til [!INCLUDE[prod_short](includes/prod_short.md)] online, er de samme som også brukes for overføring fra lokal til online.</span><span class="sxs-lookup"><span data-stu-id="c0978-111">The tools used to connect your on-premises deployment to [!INCLUDE[prod_short](includes/prod_short.md)] online are the same that are also used to migration from on-premises to online.</span></span> <span data-ttu-id="c0978-112">Hvis du vil ha mer informasjon, kan du se [Overføre lokale data til Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) i administrasjonsinnholdet for [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="c0978-112">For more information, see [Migrating On-Premises Data to Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) in the administration content for [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

## <a name="viewing-intelligent-cloud-insights-in-prod_short-online"></a><span data-ttu-id="c0978-113">Vise intelligent skyinnsikt i [!INCLUDE[prod_short](includes/prod_short.md)] Online</span><span class="sxs-lookup"><span data-stu-id="c0978-113">Viewing Intelligent Cloud Insights in [!INCLUDE[prod_short](includes/prod_short.md)] Online</span></span>

<span data-ttu-id="c0978-114">I [!INCLUDE[prod_short](includes/prod_short.md)] Online-bedriften din viser siden **Intelligent skyinnsikt** fire viktige interessepunkter for de fleste bedrifter:</span><span class="sxs-lookup"><span data-stu-id="c0978-114">In your [!INCLUDE[prod_short](includes/prod_short.md)] online company, the **Intelligent Cloud Insights** page shows four key points of interest for most businesses:</span></span>

- <span data-ttu-id="c0978-115">Kontanter til disposisjon</span><span class="sxs-lookup"><span data-stu-id="c0978-115">Cash availability</span></span>
- <span data-ttu-id="c0978-116">Salgslønnsomhet</span><span class="sxs-lookup"><span data-stu-id="c0978-116">Sales profitability</span></span>
- <span data-ttu-id="c0978-117">Resultat</span><span class="sxs-lookup"><span data-stu-id="c0978-117">Net income</span></span>
- <span data-ttu-id="c0978-118">Lagerverdi</span><span class="sxs-lookup"><span data-stu-id="c0978-118">Inventory value</span></span>

<span data-ttu-id="c0978-119">Ved siden av KPI-diagrammene kan du få innsikt i potensielle problemområder, inkludert forfalte betalinger.</span><span class="sxs-lookup"><span data-stu-id="c0978-119">Next to the KPI charts, you get insights into potential areas of concern, including overdue payments.</span></span> <span data-ttu-id="c0978-120">Velg hver innsikt for å se nærmere på dataene.</span><span class="sxs-lookup"><span data-stu-id="c0978-120">Choose each insight to drill into the data.</span></span>  

> [!div class="mx-imgBorder"]
> <span data-ttu-id="c0978-121">![Intelligent skyinnsikt](media/across-intelligent-cloud/intelligentcloudApril19.png "Viser siden Intelligent skyinnsikt i Business Central")</span><span class="sxs-lookup"><span data-stu-id="c0978-121">![Intelligent cloud insights](media/across-intelligent-cloud/intelligentcloudApril19.png "Shows the Intelligent Cloud Insights page in Business Central")</span></span>

<span data-ttu-id="c0978-122">Siden kobler også til Power BI for enda mer innsikt.</span><span class="sxs-lookup"><span data-stu-id="c0978-122">The page also connects to Power BI for even more insights.</span></span>

## <a name="viewing-intelligent-insights-on-premises"></a><span data-ttu-id="c0978-123">Vise intelligent innsikt lokalt</span><span class="sxs-lookup"><span data-stu-id="c0978-123">Viewing Intelligent Insights On-Premises</span></span>

<span data-ttu-id="c0978-124">Når Dynamics 365-videresalgspartneren din har fått den riktige lisensen for at den lokale løsningen kan kobles til skyen gjennom [!INCLUDE[prod_short](includes/prod_short.md)], kan systemansvarlig konfigurere tilkoblingen.</span><span class="sxs-lookup"><span data-stu-id="c0978-124">When your Dynamics 365 reselling partner has acquired the right license for your on-premises solution to connect to the cloud through [!INCLUDE[prod_short](includes/prod_short.md)], your administrator can set up the connection.</span></span> <span data-ttu-id="c0978-125">Når dette er gjort, kan du vise den samme innsikten fra skyen i det lokale programmet.</span><span class="sxs-lookup"><span data-stu-id="c0978-125">Once that is done, you can view the same insights from the cloud in your on-premises application.</span></span> <span data-ttu-id="c0978-126">Avhengig av den lokale løsningen kan siden **Intelligent skyinnsikt** være innebygd på hjemmesiden eller være en egen side som i [!INCLUDE[prod_short](includes/prod_short.md)] på nettet og lokalt.</span><span class="sxs-lookup"><span data-stu-id="c0978-126">Depending on the on-premises solution, the **Intelligent Cloud Insights** page can be embedded in the Home page or be a separate page as in [!INCLUDE[prod_short](includes/prod_short.md)] online and on-premises.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c0978-127">Se også</span><span class="sxs-lookup"><span data-stu-id="c0978-127">See Also</span></span>

[<span data-ttu-id="c0978-128">Velkommen til Business Central</span><span class="sxs-lookup"><span data-stu-id="c0978-128">Welcome to Business Central</span></span>](index.md)  
[<span data-ttu-id="c0978-129">Intelligente skyutvidelser for skyoverføring</span><span class="sxs-lookup"><span data-stu-id="c0978-129">Intelligent Cloud Extensions for Cloud Migration</span></span>](ui-extensions-data-replication.md)  
[<span data-ttu-id="c0978-130">Overføre lokale data til Business Central Online</span><span class="sxs-lookup"><span data-stu-id="c0978-130">Migrating On-Premises Data to Business Central Online</span></span>](/dynamics365/business-central/dev-itpro/administration/migrate-data)  
