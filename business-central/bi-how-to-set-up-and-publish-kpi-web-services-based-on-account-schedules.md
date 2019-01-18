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
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 89ea440851c359db7e08d4f0265a647cb9424330
ms.contentlocale: nb-no
ms.lasthandoff: 11/26/2018

---
# <a name="set-up-and-publish-kpi-web-services-based-on-account-schedules"></a><span data-ttu-id="9c4e7-103">Konfigurere og publisere KPI-webtjenester basert på kontoskjemaer</span><span class="sxs-lookup"><span data-stu-id="9c4e7-103">Set Up and Publish KPI Web Services Based on Account Schedules</span></span>
<span data-ttu-id="9c4e7-104">På siden **Oppsett av KPI-webtjeneste for kontoskjema** definerer du hvordan du vil vise kontoskjemaets KPI-data og hvilke bestemte kontoplaner KPI-ene skal baseres på.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-104">On the **Account Schedule KPI Web Service Setup** page, you set up how to show the account-schedule KPI data and which specific account schedules to base the KPIs on.</span></span> <span data-ttu-id="9c4e7-105">Når du velger **Publiser webtjeneste**, legges kontoskjemaets angitte KPI-data til i listen over publiserte webtjenester i vinduet over publiserte webtjenester på siden **Webtjenester**.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-105">When you choose the **Publish Web Service** button, the specified account-schedule KPI data is added to the list of published web services on the **Web Services** page.</span></span>  

## <a name="to-set-up-and-publish-a-kpi-web-service-that-is-based-on-account-schedules"></a><span data-ttu-id="9c4e7-106">Slik konfigurerer og publiserer du en KPI-webtjeneste som er basert på kontoskjemaer</span><span class="sxs-lookup"><span data-stu-id="9c4e7-106">To set up and publish a KPI web service that is based on account schedules</span></span>  
1.  <span data-ttu-id="9c4e7-107">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Oppsett av KPI-webtjeneste for kontoskjema**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedule KPI Web Service Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="9c4e7-108">I hurtigfanen **Generelt** fyller du ut feltene som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-108">On the **General** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="9c4e7-109">Felt</span><span class="sxs-lookup"><span data-stu-id="9c4e7-109">Field</span></span>|<span data-ttu-id="9c4e7-110">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="9c4e7-110">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="9c4e7-111">**Startdato for prognoseberegnede verdier**</span><span class="sxs-lookup"><span data-stu-id="9c4e7-111">**Forecasted Values Start**</span></span>|<span data-ttu-id="9c4e7-112">Angi på hvilket tidspunkt prognoseberegnede verdier vises på kontoskjemaets KPI-grafikk.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-112">Specify at what point in time forecasted values are shown on the account-schedule KPI graphic.</span></span><br /><br /> <span data-ttu-id="9c4e7-113">Prognoserverdiene hentes fra finansbudsjettet som du velger i **Finansbudsjettnavn-feltet**.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-113">The forecasted values are retrieved from the general ledger budget that you select in the **G/L Budget Name** field.</span></span> <span data-ttu-id="9c4e7-114">**Obs!** Hvis du vil hente KPIer som viser prognosetall etter en bestemt dato og faktiske tall før datoen, kan du endre feltet **Bokf. tillatt fra** på siden **Finansoppsett**.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-114">**Note:**  To obtain KPIs that show forecasted figures after a certain date and actual figures before the date, you can change the **Allow Posting From** field on the **General Ledger Setup** page.</span></span> <span data-ttu-id="9c4e7-115">Hvis du vil ha mer informasjon, kan du se Bokf. tillatt fra.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-115">For more information, see Allow Posting From.</span></span>|  
    |<span data-ttu-id="9c4e7-116">**Finansbudsjettnavn**</span><span class="sxs-lookup"><span data-stu-id="9c4e7-116">**G/L Budget Name**</span></span>|<span data-ttu-id="9c4e7-117">Angi navnet på finansbudsjettet som gir prognoseverdier til webtjenesten for kontoskjema-KPI.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-117">Specify the name of the general ledger budget that provides forecasted values to the account-schedule KPI web service.</span></span>|  
    |<span data-ttu-id="9c4e7-118">**Periode**</span><span class="sxs-lookup"><span data-stu-id="9c4e7-118">**Period**</span></span>|<span data-ttu-id="9c4e7-119">Angi perioden som webtjenesten for kontoskjema-KPI er basert på.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-119">Specify the period that the account-schedule KPI web service is based on.</span></span>|  
    |<span data-ttu-id="9c4e7-120">**Vis etter**</span><span class="sxs-lookup"><span data-stu-id="9c4e7-120">**View By**</span></span>|<span data-ttu-id="9c4e7-121">Angi hvilket tidsintervall kontoskjemaets KPI vises i.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-121">Specify which time interval the account-schedule KPI is shown in.</span></span>|  
    |<span data-ttu-id="9c4e7-122">**Webtjenestenavn**</span><span class="sxs-lookup"><span data-stu-id="9c4e7-122">**Web Service Name**</span></span>|<span data-ttu-id="9c4e7-123">Angi navnet på webtjenesten for kontoskjema-KPI.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-123">Specify the name of the account-schedule KPI web service.</span></span><br /><br /> <span data-ttu-id="9c4e7-124">Dette navnet vil vises i feltet **Tjenestenavn** på siden **Webtjenester**.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-124">This name will appear in the **Service Name** field on the **Web Services** page.</span></span>|  

    <span data-ttu-id="9c4e7-125">Angi ett eller flere kontoskjemaer som du vil publisere som en KPI-webtjeneste i samsvar med oppsettet som du lagde i den forrige tabellen.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-125">Specify one or more account schedules that you want to publish as a KPI web service according to the setup that you made in the previous table.</span></span>  

3.  <span data-ttu-id="9c4e7-126">På hurtigfanen **Kontoskjemaer** fyller du ut feltene som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-126">On the **Account Schedules** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="9c4e7-127">Felt</span><span class="sxs-lookup"><span data-stu-id="9c4e7-127">Field</span></span>|<span data-ttu-id="9c4e7-128">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="9c4e7-128">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="9c4e7-129">**Kontoskjemanavn**</span><span class="sxs-lookup"><span data-stu-id="9c4e7-129">**Acc. Schedule Name**</span></span>|<span data-ttu-id="9c4e7-130">Angi kontoskjemaet som KPI-webtjenesten er basert på.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-130">Specify the account schedule that the KPI web service is based on.</span></span>|  
    |<span data-ttu-id="9c4e7-131">**Beskrivelse av kontoskjema**</span><span class="sxs-lookup"><span data-stu-id="9c4e7-131">**Acc. Schedule Description**</span></span>|<span data-ttu-id="9c4e7-132">Angi beskrivelsen av kontoskjemaet som KPI-webtjenesten er basert på.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-132">Specify the description of the account schedule that the KPI web service is based on.</span></span>|  

4.  <span data-ttu-id="9c4e7-133">Gjenta trinn 3 for alle kontoskjemaer som du vil basere webtjenesten for kontoskjema-KPI på.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-133">Repeat step 3 for all the account schedules that you want to base the account-schedule KPI web service on.</span></span>  
5.  <span data-ttu-id="9c4e7-134">Hvis du vil vise eller redigere det valgte kontoskjemaet, velger du **Rediger kontoskjema** på hurtigfanen **Kontoskjema**.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-134">To view or edit the selected account schedule, on the **Account Schedule** FastTab, choose the **Edit Account Schedule** action.</span></span>  
6.  <span data-ttu-id="9c4e7-135">Hvis du vil vise kontoskjemaets KPI-data som du har definert, velger du **KPI-webtjeneste for kontoskjema**.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-135">To view the account-schedule KPI data that you have set up, choose the **Account Schedule KPI Web Service** action.</span></span>  
7.  <span data-ttu-id="9c4e7-136">Hvis du vil publisere KPI-webtjenesten for kontoskjemaet, velger du **Publiserer webtjeneste**.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-136">To publish the account-schedule KPI web service, choose the **Publish Web Service** action.</span></span> <span data-ttu-id="9c4e7-137">Webtjenesten er lagt til listen over publiserte webtjenester på **Webtjenester**-siden.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-137">The web service is added to the list of published web services on the **Web Services** page.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="9c4e7-138">Du kan også publisere KPI-webtjenesten ved å velge sideobjektet **Oppsett av KPI-webtjeneste for kontoskjema** fra **Webtjenester**-siden.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-138">You can also publish the KPI web service by pointing to the **Account Schedule KPI Web Service Setup** page object from the **Web Services** page.</span></span> <span data-ttu-id="9c4e7-139">Hvis du vil ha mer informasjon, kan du se [Publisere en webtjeneste](across-how-publish-web-service.md).</span><span class="sxs-lookup"><span data-stu-id="9c4e7-139">For more information, see [Publish a Web Service](across-how-publish-web-service.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="9c4e7-140">Se også</span><span class="sxs-lookup"><span data-stu-id="9c4e7-140">See Also</span></span>  
[<span data-ttu-id="9c4e7-141">Forretningsintelligens</span><span class="sxs-lookup"><span data-stu-id="9c4e7-141">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="9c4e7-142">Finans</span><span class="sxs-lookup"><span data-stu-id="9c4e7-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="9c4e7-143">Konfigurere finans</span><span class="sxs-lookup"><span data-stu-id="9c4e7-143">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="9c4e7-144">Finans og kontoplanen</span><span class="sxs-lookup"><span data-stu-id="9c4e7-144">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="9c4e7-145">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9c4e7-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

