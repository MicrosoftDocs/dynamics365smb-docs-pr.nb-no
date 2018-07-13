---
title: Konfigurere og publisere KPI-webtjenester for kontoskjemaer | Microsoft-dokumentasjon
description: "Dette emnet beskriver hvordan du viser kontoskjemaet KPI-data som er basert på bestemte kontoskjemaer."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 05/31/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 4bc9199b879c23115082b07a81d6da5a0b46e60d
ms.openlocfilehash: c15f9c77479780566f8b1e464193b43a20c3315d
ms.contentlocale: nb-no
ms.lasthandoff: 05/31/2018

---
# <a name="set-up-and-publish-kpi-web-services-based-on-account-schedules"></a><span data-ttu-id="a1da6-103">Konfigurere og publisere KPI-webtjenester basert på kontoskjemaer</span><span class="sxs-lookup"><span data-stu-id="a1da6-103">Set Up and Publish KPI Web Services Based on Account Schedules</span></span>
<span data-ttu-id="a1da6-104">I vinduet **Oppsett av KPI-webtjeneste for kontoskjema** definerer du hvordan du vil vise kontoskjemaets KPI-data og hvilke bestemte kontoplaner KPI-ene skal baseres på.</span><span class="sxs-lookup"><span data-stu-id="a1da6-104">In the **Account Schedule KPI Web Service Setup** window, you set up how to show the account-schedule KPI data and which specific account schedules to base the KPIs on.</span></span> <span data-ttu-id="a1da6-105">Når du velger **Publiser webtjeneste**, legges kontoskjemaets angitte KPI-data til i listen over publiserte webtjenester i vinduet over publiserte webtjenester i vinduet **Webtjenester**.</span><span class="sxs-lookup"><span data-stu-id="a1da6-105">When you choose the **Publish Web Service** button, the specified account-schedule KPI data is added to the list of published web services in the **Web Services** window.</span></span>  

## <a name="to-set-up-and-publish-a-kpi-web-service-that-is-based-on-account-schedules"></a><span data-ttu-id="a1da6-106">Slik konfigurerer og publiserer du en KPI-webtjeneste som er basert på kontoskjemaer</span><span class="sxs-lookup"><span data-stu-id="a1da6-106">To set up and publish a KPI web service that is based on account schedules</span></span>  
1.  <span data-ttu-id="a1da6-107">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Oppsett av KPI-webtjeneste for kontoskjema**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a1da6-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedule KPI Web Service Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a1da6-108">I hurtigfanen **Generelt** fyller du ut feltene som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a1da6-108">On the **General** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="a1da6-109">Felt</span><span class="sxs-lookup"><span data-stu-id="a1da6-109">Field</span></span>|<span data-ttu-id="a1da6-110">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a1da6-110">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="a1da6-111">**Startdato for prognoseberegnede verdier**</span><span class="sxs-lookup"><span data-stu-id="a1da6-111">**Forecasted Values Start**</span></span>|<span data-ttu-id="a1da6-112">Angi på hvilket tidspunkt prognoseberegnede verdier vises på kontoskjemaets KPI-grafikk.</span><span class="sxs-lookup"><span data-stu-id="a1da6-112">Specify at what point in time forecasted values are shown on the account-schedule KPI graphic.</span></span><br /><br /> <span data-ttu-id="a1da6-113">Prognoserverdiene hentes fra finansbudsjettet som du velger i **Finansbudsjettnavn-feltet**.</span><span class="sxs-lookup"><span data-stu-id="a1da6-113">The forecasted values are retrieved from the general ledger budget that you select in the **G/L Budget Name** field.</span></span> <span data-ttu-id="a1da6-114">**Obs!** Hvis du vil hente KPIer som viser prognosetall etter en bestemt dato og faktiske tall før datoen, kan du endre feltet **Bokf. tillatt fra** i vinduet **Finansoppsett**.</span><span class="sxs-lookup"><span data-stu-id="a1da6-114">**Note:**  To obtain KPIs that show forecasted figures after a certain date and actual figures before the date, you can change the **Allow Posting From** field in the **General Ledger Setup** window.</span></span> <span data-ttu-id="a1da6-115">Hvis du vil ha mer informasjon, kan du se Bokf. tillatt fra.</span><span class="sxs-lookup"><span data-stu-id="a1da6-115">For more information, see Allow Posting From.</span></span>|  
    |<span data-ttu-id="a1da6-116">**Finansbudsjettnavn**</span><span class="sxs-lookup"><span data-stu-id="a1da6-116">**G/L Budget Name**</span></span>|<span data-ttu-id="a1da6-117">Angi navnet på finansbudsjettet som gir prognoseverdier til webtjenesten for kontoskjema-KPI.</span><span class="sxs-lookup"><span data-stu-id="a1da6-117">Specify the name of the general ledger budget that provides forecasted values to the account-schedule KPI web service.</span></span>|  
    |<span data-ttu-id="a1da6-118">**Periode**</span><span class="sxs-lookup"><span data-stu-id="a1da6-118">**Period**</span></span>|<span data-ttu-id="a1da6-119">Angi perioden som webtjenesten for kontoskjema-KPI er basert på.</span><span class="sxs-lookup"><span data-stu-id="a1da6-119">Specify the period that the account-schedule KPI web service is based on.</span></span>|  
    |<span data-ttu-id="a1da6-120">**Vis etter**</span><span class="sxs-lookup"><span data-stu-id="a1da6-120">**View By**</span></span>|<span data-ttu-id="a1da6-121">Angi hvilket tidsintervall kontoskjemaets KPI vises i.</span><span class="sxs-lookup"><span data-stu-id="a1da6-121">Specify which time interval the account-schedule KPI is shown in.</span></span>|  
    |<span data-ttu-id="a1da6-122">**Webtjenestenavn**</span><span class="sxs-lookup"><span data-stu-id="a1da6-122">**Web Service Name**</span></span>|<span data-ttu-id="a1da6-123">Angi navnet på webtjenesten for kontoskjema-KPI.</span><span class="sxs-lookup"><span data-stu-id="a1da6-123">Specify the name of the account-schedule KPI web service.</span></span><br /><br /> <span data-ttu-id="a1da6-124">Dette navnet vil vises i feltet **Tjenestenavn** i vinduet **Webtjenester**.</span><span class="sxs-lookup"><span data-stu-id="a1da6-124">This name will appear in the **Service Name** field in the **Web Services** window.</span></span>|  

    <span data-ttu-id="a1da6-125">Angi ett eller flere kontoskjemaer som du vil publisere som en KPI-webtjeneste i samsvar med oppsettet som du lagde i den forrige tabellen.</span><span class="sxs-lookup"><span data-stu-id="a1da6-125">Specify one or more account schedules that you want to publish as a KPI web service according to the setup that you made in the previous table.</span></span>  

3.  <span data-ttu-id="a1da6-126">På hurtigfanen **Kontoskjemaer** fyller du ut feltene som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a1da6-126">On the **Account Schedules** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="a1da6-127">Felt</span><span class="sxs-lookup"><span data-stu-id="a1da6-127">Field</span></span>|<span data-ttu-id="a1da6-128">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a1da6-128">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="a1da6-129">**Kontoskjemanavn**</span><span class="sxs-lookup"><span data-stu-id="a1da6-129">**Acc. Schedule Name**</span></span>|<span data-ttu-id="a1da6-130">Angi kontoskjemaet som KPI-webtjenesten er basert på.</span><span class="sxs-lookup"><span data-stu-id="a1da6-130">Specify the account schedule that the KPI web service is based on.</span></span>|  
    |<span data-ttu-id="a1da6-131">**Beskrivelse av kontoskjema**</span><span class="sxs-lookup"><span data-stu-id="a1da6-131">**Acc. Schedule Description**</span></span>|<span data-ttu-id="a1da6-132">Angi beskrivelsen av kontoskjemaet som KPI-webtjenesten er basert på.</span><span class="sxs-lookup"><span data-stu-id="a1da6-132">Specify the description of the account schedule that the KPI web service is based on.</span></span>|  

4.  <span data-ttu-id="a1da6-133">Gjenta trinn 3 for alle kontoskjemaer som du vil basere webtjenesten for kontoskjema-KPI på.</span><span class="sxs-lookup"><span data-stu-id="a1da6-133">Repeat step 3 for all the account schedules that you want to base the account-schedule KPI web service on.</span></span>  
5.  <span data-ttu-id="a1da6-134">Hvis du vil vise eller redigere det valgte kontoskjemaet, velger du **Rediger kontoskjema** på hurtigfanen **Kontoskjema**.</span><span class="sxs-lookup"><span data-stu-id="a1da6-134">To view or edit the selected account schedule, on the **Account Schedule** FastTab, choose the **Edit Account Schedule** action.</span></span>  
6.  <span data-ttu-id="a1da6-135">Hvis du vil vise kontoskjemaets KPI-data som du har definert, velger du **KPI-webtjeneste for kontoskjema**.</span><span class="sxs-lookup"><span data-stu-id="a1da6-135">To view the account-schedule KPI data that you have set up, choose the **Account Schedule KPI Web Service** action.</span></span>  
7.  <span data-ttu-id="a1da6-136">Hvis du vil publisere KPI-webtjenesten for kontoskjemaet, velger du **Publiserer webtjeneste**.</span><span class="sxs-lookup"><span data-stu-id="a1da6-136">To publish the account-schedule KPI web service, choose the **Publish Web Service** action.</span></span> <span data-ttu-id="a1da6-137">Webtjenesten er lagt til listen over publiserte webtjenester i **Webtjenester**-vinduet.</span><span class="sxs-lookup"><span data-stu-id="a1da6-137">The web service is added to the list of published web services in the **Web Services** window.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="a1da6-138">Du kan også publisere KPI-webtjenesten ved å velge sideobjektet **Oppsett av KPI-webtjeneste for kontoskjema** fra **Webtjenester**-vinduet.</span><span class="sxs-lookup"><span data-stu-id="a1da6-138">You can also publish the KPI web service by pointing to the **Account Schedule KPI Web Service Setup** page object from the **Web Services** window.</span></span> <span data-ttu-id="a1da6-139">Hvis du vil ha mer informasjon, kan du se [Publisere en webtjeneste](across-how-publish-web-service.md).</span><span class="sxs-lookup"><span data-stu-id="a1da6-139">For more information, see [Publish a Web Service](across-how-publish-web-service.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="a1da6-140">Se også</span><span class="sxs-lookup"><span data-stu-id="a1da6-140">See Also</span></span>  
[<span data-ttu-id="a1da6-141">Forretningsintelligens</span><span class="sxs-lookup"><span data-stu-id="a1da6-141">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="a1da6-142">Finans</span><span class="sxs-lookup"><span data-stu-id="a1da6-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="a1da6-143">Konfigurere finans</span><span class="sxs-lookup"><span data-stu-id="a1da6-143">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="a1da6-144">Finans og kontoplanen</span><span class="sxs-lookup"><span data-stu-id="a1da6-144">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="a1da6-145">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a1da6-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

