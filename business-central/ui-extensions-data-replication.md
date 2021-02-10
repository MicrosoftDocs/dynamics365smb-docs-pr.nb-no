---
title: Intelligente skyutvidelser i Business Central for skyoverføring | Microsoft-dokumentasjon
description: Bruk skyoverføringsutvidelsene til å overføre de lokale dataene til Business Central på nettet. Disse utvidelsene flytter de lokale dataene til skyen, slik at du kan bruke Business Central på nettet med de eksisterende dataene.
author: jenolson
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f2d8d556ca4628a66c10f323f47137cd35732a68
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757295"
---
# <a name="intelligent-cloud-extensions-for-cloud-migration"></a><span data-ttu-id="cd1c6-104">Intelligente skyutvidelser for skyoverføring</span><span class="sxs-lookup"><span data-stu-id="cd1c6-104">Intelligent Cloud Extensions for Cloud Migration</span></span>

<span data-ttu-id="cd1c6-105">Avhengig av din lokale løsning må du bruke ulike utvidelser for å koble data til lokal [!INCLUDE[prod_short](includes/prod_short.md)] for å overføre løsningen til skyen.</span><span class="sxs-lookup"><span data-stu-id="cd1c6-105">Depending on your on-premises solution, you must use different extensions to connect your data with [!INCLUDE[prod_short](includes/prod_short.md)] online for purposes of migrating your solution to the cloud.</span></span>  

<span data-ttu-id="cd1c6-106">Hvis du bruker én av de støttede lokale produktene, kan du konfigurere skymiljøet basert på en produktspesifikk utvidelse.</span><span class="sxs-lookup"><span data-stu-id="cd1c6-106">If you are using one of the supported on-premises products, you can configure your cloud environment based on a product-specific extension.</span></span> <span data-ttu-id="cd1c6-107">Når skymiljøet er konfigurert, vil du kunne overføre data fra den lokale løsningen til [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="cd1c6-107">Once your cloud environment is configured, you will be able to migrate data from your on-premises solution to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="cd1c6-108">Dette gjør at du kan dra nytte av hva skyen har å tilby bedriften din, for eksempel utvidet innsikt i din bedrift, AI, tilgang til flere enheter og tilgang når og hvor som helst.</span><span class="sxs-lookup"><span data-stu-id="cd1c6-108">This will enable you to take full advantage of what the cloud has to offer your business such as, enhanced insights into your business, artificial intelligence, multiple device access, and anytime, anywhere access.</span></span>  

<span data-ttu-id="cd1c6-109">Hvis du vil ha mer informasjon, kan du se [Overføre lokale data til Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) i administrasjonsinnholdet for [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="cd1c6-109">For more information, see [Migrating On-Premises Data to Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) in the administration content for [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

## <a name="business-central-on-premises"></a><span data-ttu-id="cd1c6-110">Business Central lokalt</span><span class="sxs-lookup"><span data-stu-id="cd1c6-110">Business Central on-premises</span></span>

<span data-ttu-id="cd1c6-111">Hvis du bruker en lokal distribusjon av [!INCLUDE[prod_short](includes/prod_short.md)], hent utvidelsen for **Intelligent skybase** og utvidelsen for **Intelligent sky for Business Central**, og kjør deretter den assisterte oppsettsveiledningen **Oppsett av skyoverføring**.</span><span class="sxs-lookup"><span data-stu-id="cd1c6-111">If you are using an on-premises deployment of [!INCLUDE[prod_short](includes/prod_short.md)], get the **Intelligent Cloud Base** extension and the **Business Central Intelligent Cloud** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

## <a name="dynamics-gp"></a><span data-ttu-id="cd1c6-112">Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="cd1c6-112">Dynamics GP</span></span>

<span data-ttu-id="cd1c6-113">Hvis du bruker Dynamics GP, hent utvidelsen for **Intelligent skybaseutvidelse** og utvidelsen for **Intelligent sky for Dynamics GP** , og kjør deretter den assisterte oppsettsveiledningen **Oppsett av skyoverføring**.</span><span class="sxs-lookup"><span data-stu-id="cd1c6-113">If you are using Dynamics GP,  get the **Intelligent Cloud Base Extension** extension and the **Dynamics GP Intelligent Cloud** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="cd1c6-114">Migrering fra Dynamics GP med den assisterte oppsettsveiledningen **Oppsett av skyoverføring** støttes for øyeblikket bare for følgende markeder: USA, Canada, Storbritannia.</span><span class="sxs-lookup"><span data-stu-id="cd1c6-114">Migrating from Dynamics GP using the **Cloud Migration Setup** assisted setup guide is currently only supported for the following markets: United States, Canada, United Kingdom.</span></span>

## <a name="dynamics-sl"></a><span data-ttu-id="cd1c6-115">Dynamics SL</span><span class="sxs-lookup"><span data-stu-id="cd1c6-115">Dynamics SL</span></span>

<span data-ttu-id="cd1c6-116">Hvis du bruker Dynamics SL, hent utvidelsen for **Intelligent skybase**, utvidelsen for **Microsoft Dynamics SL intelligent sky** og utvidelsen for **Microsoft Dynamics SL historikksmartlister**, og kjør deretter den assisterte oppsettsveiledningen **Oppsett av skyoverføring**.</span><span class="sxs-lookup"><span data-stu-id="cd1c6-116">If you are using Dynamics SL, get the **Intelligent Cloud Base** extension, the **Microsoft Dynamics SL Intelligent Cloud** extension and the **Microsoft Dynamics SL History SmartLists** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cd1c6-117">Se også</span><span class="sxs-lookup"><span data-stu-id="cd1c6-117">See Also</span></span>

[<span data-ttu-id="cd1c6-118">Intelligent innsikt</span><span class="sxs-lookup"><span data-stu-id="cd1c6-118">Intelligent Insights</span></span>](about-intelligent-cloud.md)  
[<span data-ttu-id="cd1c6-119">Intelligent skybaseutvidelse</span><span class="sxs-lookup"><span data-stu-id="cd1c6-119">Intelligent Cloud Base Extension</span></span>](ui-extensions-intelligent-cloud.md)  
