---
title: Koble Power BI til Business Central | Microsoft-dokumentasjon
description: "Få innsikt, forretningsintelligens og KPI-er fra Business Central-dataene på en enkel måte med Power BI og Business Central-innholdspakkene."
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 10/01/2018
ms.author: solsen
redirect_url: admin-powerbi
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 448b8fa9d1b239f98c7ca3700b9f7f56f08d7854
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="connecting-power-bi-to-dynamics-365-business-central-content-packs"></a><span data-ttu-id="62275-103">Koble Power BI til Dynamics 365 Business Central-innholdspakker</span><span class="sxs-lookup"><span data-stu-id="62275-103">Connecting Power BI to Dynamics 365 Business Central Content Packs</span></span>
<span data-ttu-id="62275-104">Få innsikt i Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-dataene på en enkel måte med Power BI og Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-innholdspakkene.</span><span class="sxs-lookup"><span data-stu-id="62275-104">Getting insights into your Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data is easy with Power BI and the Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] content packs.</span></span> <span data-ttu-id="62275-105">Power BI henter dataene, og bygger deretter et forhåndskonfigurert instrumentbord og rapporter basert på dataene.</span><span class="sxs-lookup"><span data-stu-id="62275-105">Power BI retrieves your data then builds an out-of-the-box dashboard and reports based on that data.</span></span>

<span data-ttu-id="62275-106">Du må ha en gyldig konto for Dynamics 365 og Power BI.</span><span class="sxs-lookup"><span data-stu-id="62275-106">You must have a valid account with Dynamics 365 and with Power BI.</span></span> <span data-ttu-id="62275-107">Du må også laste ned [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) hvis du vil opprette dine egne Power BI-rapporter.</span><span class="sxs-lookup"><span data-stu-id="62275-107">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) if you wish to create your own Power BI reports.</span></span> <span data-ttu-id="62275-108">Power BI-innholdspakker krever tilgang til tabellene der opplysningene hentes fra.</span><span class="sxs-lookup"><span data-stu-id="62275-108">Power BI content packs require permissions to the tables where data is retrieved from.</span></span> <span data-ttu-id="62275-109">Du finner mer informasjon om kravene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="62275-109">More details on the requirements are described below.</span></span>  

## <a name="how-to-connect"></a><span data-ttu-id="62275-110">Koble til</span><span class="sxs-lookup"><span data-stu-id="62275-110">How to Connect</span></span>
1. <span data-ttu-id="62275-111">Velg **Hent data** nederst i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="62275-111">Select **Get Data** at the bottom of the left navigation pane.</span></span>  
<span data-ttu-id="62275-112">![Navigere til Hent data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span><span class="sxs-lookup"><span data-stu-id="62275-112">![Navigating to Get Data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span></span>

<span data-ttu-id="62275-113">Du kan også komme i gang fra Dynamics 365 Business Edition.</span><span class="sxs-lookup"><span data-stu-id="62275-113">You may also get starting from within Dynamics 365 Business Edition.</span></span> <span data-ttu-id="62275-114">Gå til rollesenteret og deretter **Rapportvalg** i rollesenterdelen i Power BI.</span><span class="sxs-lookup"><span data-stu-id="62275-114">From the role center, navigate to **Report Selection** in the Power BI Role Center part.</span></span> <span data-ttu-id="62275-115">Velg enten **Service** eller **Min organisasjon** på båndet.</span><span class="sxs-lookup"><span data-stu-id="62275-115">Select either **Service** or **My Organization** from the ribbon.</span></span> <span data-ttu-id="62275-116">Når en av disse handlingene er valgt, kommer du enten til organisasjonsgalleriet i Power BI eller til tjenestebiblioteket i Power BI, som også filtreres for å bare vise innholdspakker knyttet til [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="62275-116">When either of these actions are selected, you will be taken to either the Organization gallery in Power BI or to the services library in Power BI, which will also be filtered to only display content packs related to [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span>

2. <span data-ttu-id="62275-117">I **Tjenester**-boksen velger du **Hent**.</span><span class="sxs-lookup"><span data-stu-id="62275-117">In the **Services** box, select **Get**.</span></span> <span data-ttu-id="62275-118">Dette åpner et vindu med **AppSource** og **Apper for Power BI-apper**.</span><span class="sxs-lookup"><span data-stu-id="62275-118">This will open a window with the **AppSource** and **Apps for Power BI apps**.</span></span>  
<span data-ttu-id="62275-119">![Velge innholdspakker fra elektroniske tjenester](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span><span class="sxs-lookup"><span data-stu-id="62275-119">![Choose content packs from online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span></span>
3. <span data-ttu-id="62275-120">Velg **Apper** fra fanen **Apper for Power BI-apper**, velg innholdspakken **Microsoft Dynamics 365 Business Central** som du vil bruke, og velg deretter **Få det nå**.</span><span class="sxs-lookup"><span data-stu-id="62275-120">Select **Apps** from the **Apps for Power BI apps** tab, choose the **Microsoft Dynamics 365 Business Central** content pack that you want to use, and then select **Get it now**.</span></span>  
<span data-ttu-id="62275-121">![Velg Dynamics 365 Business Central, og velg Få det nå](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span><span class="sxs-lookup"><span data-stu-id="62275-121">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span></span>
4. <span data-ttu-id="62275-122">Når du blir spurt, skriver du inn navnet på *selskapet ditt* i [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="62275-122">When prompted, enter the name of *your company* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="62275-123">Dette er ikke visningsnavnet.</span><span class="sxs-lookup"><span data-stu-id="62275-123">This is not the display name.</span></span> <span data-ttu-id="62275-124">Du finner selskapsnavnet på siden Selskaper i din [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]-forekomst.</span><span class="sxs-lookup"><span data-stu-id="62275-124">The company name can be found on the 'Companies' page within your [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] instance.</span></span> 
<span data-ttu-id="62275-125">![Velg Dynamics 365 Business Central, og velg Få det nå](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span><span class="sxs-lookup"><span data-stu-id="62275-125">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span></span>
5. <span data-ttu-id="62275-126">Når du er tilkoblet, lastes det automatisk inn et instrumentbord, en rapport og et datasett i Power BI-arbeidområdet.</span><span class="sxs-lookup"><span data-stu-id="62275-126">Once connected, a dashboard, report and dataset will automatically be loaded into your Power BI workspace.</span></span> <span data-ttu-id="62275-127">Når du er ferdig, oppdateres flisene med dataene fra [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]-selskapet.</span><span class="sxs-lookup"><span data-stu-id="62275-127">When completed, the tiles will update with data from your [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] company.</span></span>
<span data-ttu-id="62275-128">![Velg Dynamics 365 Business Central, og velg Få det nå](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="62275-128">![Select Dynamics 365 Business Central  and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span></span>

## <a name="what-now"></a><span data-ttu-id="62275-129">Hva nå?</span><span class="sxs-lookup"><span data-stu-id="62275-129">What Now?</span></span>

- <span data-ttu-id="62275-130">Prøv [å stille et spørsmål i spørsmål og svar-boksen](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) øverst i instrumentbordet.</span><span class="sxs-lookup"><span data-stu-id="62275-130">Try [asking a question in the Q&A box](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) at the top of the dashboard.</span></span>
- <span data-ttu-id="62275-131">[Endre flisene](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) i instrumentbordet.</span><span class="sxs-lookup"><span data-stu-id="62275-131">[Change the tiles](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in the dashboard.</span></span>  
- <span data-ttu-id="62275-132">[Velge en flis](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) for å åpne den underliggende rapporten.</span><span class="sxs-lookup"><span data-stu-id="62275-132">[Select a tile](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) to open the underlying report.</span></span>  
- <span data-ttu-id="62275-133">Selv om det er planlagt at datasettet ditt oppdateres daglig, kan du endre oppdateringstidsplanen eller prøve å oppdatere den ved behov ved hjelp av **Oppdater nå**.</span><span class="sxs-lookup"><span data-stu-id="62275-133">While your dataset will be scheduled to refreshed daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="62275-134">Systemkrav</span><span class="sxs-lookup"><span data-stu-id="62275-134">System Requirements</span></span>
<span data-ttu-id="62275-135">Hvis du vil importere [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-dataene til Power BI, må du ha tillatelse til å webtjenestene som brukes for å hente data.</span><span class="sxs-lookup"><span data-stu-id="62275-135">To import your [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data into Power BI, you need to have permissions to the web services used to retrieve data.</span></span> <span data-ttu-id="62275-136">Webtjenestene som kreves for hver innholdspakke:</span><span class="sxs-lookup"><span data-stu-id="62275-136">The web services required for each content pack include:</span></span>

## <a name="role-center-reports"></a><span data-ttu-id="62275-137">Rapporter i rollesenter</span><span class="sxs-lookup"><span data-stu-id="62275-137">Role Center Reports</span></span>

<span data-ttu-id="62275-138">**Microsoft Dynamics 365 Business Central – CRM**</span><span class="sxs-lookup"><span data-stu-id="62275-138">**Microsoft Dynamics 365 Business Central – CRM**</span></span>
- <span data-ttu-id="62275-139">Salgsmuligheter</span><span class="sxs-lookup"><span data-stu-id="62275-139">Sales Opportunities</span></span>
- <span data-ttu-id="62275-140">Excel-mal – Vis selskap</span><span class="sxs-lookup"><span data-stu-id="62275-140">Excel Template View Company</span></span>
- <span data-ttu-id="62275-141">Etiketter for Power BI-rapport</span><span class="sxs-lookup"><span data-stu-id="62275-141">Power BI Report Labels</span></span>

<span data-ttu-id="62275-142">**Microsoft Dynamics 365 Business Central – Finance**</span><span class="sxs-lookup"><span data-stu-id="62275-142">**Microsoft Dynamics 365 Business Central – Finance**</span></span>
- <span data-ttu-id="62275-143">PowerBIFinance</span><span class="sxs-lookup"><span data-stu-id="62275-143">PowerBIFinance</span></span>
- <span data-ttu-id="62275-144">Excel-mal – Vis selskap</span><span class="sxs-lookup"><span data-stu-id="62275-144">Excel Template View Company</span></span>
- <span data-ttu-id="62275-145">Etiketter for Power BI-rapport</span><span class="sxs-lookup"><span data-stu-id="62275-145">Power BI Report Labels</span></span>

<span data-ttu-id="62275-146">**Microsoft Dynamics 365 Business Central – Jobs**</span><span class="sxs-lookup"><span data-stu-id="62275-146">**Microsoft Dynamics 365 Business Central – Jobs**</span></span>
- <span data-ttu-id="62275-147">Prosjektoversikt</span><span class="sxs-lookup"><span data-stu-id="62275-147">Job List</span></span>
- <span data-ttu-id="62275-148">Prosjektplanleggingslinjer</span><span class="sxs-lookup"><span data-stu-id="62275-148">Job Planning Lines</span></span>
- <span data-ttu-id="62275-149">Prosjektoppgavelinjer</span><span class="sxs-lookup"><span data-stu-id="62275-149">Job Task Lines</span></span>
- <span data-ttu-id="62275-150">Etiketter for Power BI-rapport</span><span class="sxs-lookup"><span data-stu-id="62275-150">Power BI Report Labels</span></span>
- <span data-ttu-id="62275-151">Excel-mal – Vis selskap</span><span class="sxs-lookup"><span data-stu-id="62275-151">Excel Template View Company</span></span>

<span data-ttu-id="62275-152">**Microsoft Dynamics 365 Business Central - Sales**</span><span class="sxs-lookup"><span data-stu-id="62275-152">**Microsoft Dynamics 365 Business Central - Sales**</span></span>
- <span data-ttu-id="62275-153">Instrumentbord for salg</span><span class="sxs-lookup"><span data-stu-id="62275-153">Sales Dashboard</span></span>
- <span data-ttu-id="62275-154">Excel-mal – Vis selskap</span><span class="sxs-lookup"><span data-stu-id="62275-154">Excel Template View Company</span></span>
- <span data-ttu-id="62275-155">Etiketter for Power BI-rapport</span><span class="sxs-lookup"><span data-stu-id="62275-155">Power BI Report Labels</span></span>

## <a name="list-page-reports"></a><span data-ttu-id="62275-156">Rapporter for siden Liste</span><span class="sxs-lookup"><span data-stu-id="62275-156">List Page Reports</span></span> 

<span data-ttu-id="62275-157">**Microsoft Dynamics 365 Business Central – Customers List**</span><span class="sxs-lookup"><span data-stu-id="62275-157">**Microsoft Dynamics 365 Business Central – Customers List**</span></span>
- <span data-ttu-id="62275-158">Varesalg etter kunde</span><span class="sxs-lookup"><span data-stu-id="62275-158">Item Sales by Customer</span></span>
- <span data-ttu-id="62275-159">Varekjøpsliste for Power BI</span><span class="sxs-lookup"><span data-stu-id="62275-159">Power BI Item Purchase List</span></span>
- <span data-ttu-id="62275-160">Varesalgsliste for Power BI</span><span class="sxs-lookup"><span data-stu-id="62275-160">Power BI Item Sales List</span></span>
- <span data-ttu-id="62275-161">Instrumentbord for salg</span><span class="sxs-lookup"><span data-stu-id="62275-161">Sales Dashboard</span></span>
- <span data-ttu-id="62275-162">Kundeliste for Power BI</span><span class="sxs-lookup"><span data-stu-id="62275-162">Power BI Customer List</span></span>
- <span data-ttu-id="62275-163">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="62275-163">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="62275-164">Etiketter for Power BI-rapport</span><span class="sxs-lookup"><span data-stu-id="62275-164">Power BI Report Labels</span></span> 

<span data-ttu-id="62275-165">**Microsoft Dynamics 365 Business Central - General Ledger Entries List**</span><span class="sxs-lookup"><span data-stu-id="62275-165">**Microsoft Dynamics 365 Business Central - General Ledger Entries List**</span></span>
- <span data-ttu-id="62275-166">Finansbeløpsliste for Power BI</span><span class="sxs-lookup"><span data-stu-id="62275-166">Power BI GL Amount List</span></span>
- <span data-ttu-id="62275-167">Finansbudsjettert beløp for Power BI</span><span class="sxs-lookup"><span data-stu-id="62275-167">Power BI GL Budgeted Amount</span></span>
- <span data-ttu-id="62275-168">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="62275-168">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="62275-169">Etiketter for Power BI-rapport</span><span class="sxs-lookup"><span data-stu-id="62275-169">Power BI Report Labels</span></span>

<span data-ttu-id="62275-170">**Microsoft Dynamics 365 Business Central – Items List**</span><span class="sxs-lookup"><span data-stu-id="62275-170">**Microsoft Dynamics 365 Business Central – Items List**</span></span>
- <span data-ttu-id="62275-171">Varesalg etter kunde</span><span class="sxs-lookup"><span data-stu-id="62275-171">Item Sales by Customer</span></span>
- <span data-ttu-id="62275-172">Varekjøpsliste for Power BI</span><span class="sxs-lookup"><span data-stu-id="62275-172">Power BI Item Purchase List</span></span>
- <span data-ttu-id="62275-173">Varesalgsliste for Power BI</span><span class="sxs-lookup"><span data-stu-id="62275-173">Power BI Item Sales List</span></span>
- <span data-ttu-id="62275-174">Instrumentbord for salg</span><span class="sxs-lookup"><span data-stu-id="62275-174">Sales Dashboard</span></span>
- <span data-ttu-id="62275-175">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="62275-175">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="62275-176">Etiketter for Power BI-rapport</span><span class="sxs-lookup"><span data-stu-id="62275-176">Power BI Report Labels</span></span>

<span data-ttu-id="62275-177">**Microsoft Dynamics 365 Business Central – Jobs List**</span><span class="sxs-lookup"><span data-stu-id="62275-177">**Microsoft Dynamics 365 Business Central – Jobs List**</span></span>
- <span data-ttu-id="62275-178">Prosjektliste for Power BI</span><span class="sxs-lookup"><span data-stu-id="62275-178">Power BI Jobs List</span></span>
- <span data-ttu-id="62275-179">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="62275-179">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="62275-180">Etiketter for Power BI-rapport</span><span class="sxs-lookup"><span data-stu-id="62275-180">Power BI Report Labels</span></span>

<span data-ttu-id="62275-181">**Microsoft Dynamics 365 Business Central – Purchase Invoices List**</span><span class="sxs-lookup"><span data-stu-id="62275-181">**Microsoft Dynamics 365 Business Central – Purchase Invoices List**</span></span>
- <span data-ttu-id="62275-182">Kjøpsliste for Power BI</span><span class="sxs-lookup"><span data-stu-id="62275-182">Power BI Purchase List</span></span>
- <span data-ttu-id="62275-183">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="62275-183">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="62275-184">Etiketter for Power BI-rapport</span><span class="sxs-lookup"><span data-stu-id="62275-184">Power BI Report Labels</span></span>

<span data-ttu-id="62275-185">**Microsoft Dynamics 365 Business Central – Sales Orders List**</span><span class="sxs-lookup"><span data-stu-id="62275-185">**Microsoft Dynamics 365 Business Central – Sales Orders List**</span></span>
- <span data-ttu-id="62275-186">Salgsliste for Power BI</span><span class="sxs-lookup"><span data-stu-id="62275-186">Power BI Sales List</span></span>
- <span data-ttu-id="62275-187">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="62275-187">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="62275-188">Etiketter for Power BI-rapport</span><span class="sxs-lookup"><span data-stu-id="62275-188">Power BI Report Labels</span></span>


<span data-ttu-id="62275-189">**Microsoft Dynamics 365 Business Central – Vendors List**</span><span class="sxs-lookup"><span data-stu-id="62275-189">**Microsoft Dynamics 365 Business Central – Vendors List**</span></span>
- <span data-ttu-id="62275-190">Varekjøpsliste for Power BI</span><span class="sxs-lookup"><span data-stu-id="62275-190">Power BI Item Purchase List</span></span>
- <span data-ttu-id="62275-191">Varesalgsliste for Power BI</span><span class="sxs-lookup"><span data-stu-id="62275-191">Power BI Item Sales List</span></span>
- <span data-ttu-id="62275-192">Leverandørliste for Power BI</span><span class="sxs-lookup"><span data-stu-id="62275-192">Power BI Vendor List</span></span>
- <span data-ttu-id="62275-193">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="62275-193">ExcelTemplateViewCompany</span></span>
- <span data-ttu-id="62275-194">Etiketter for Power BI-rapport</span><span class="sxs-lookup"><span data-stu-id="62275-194">Power BI Report Labels</span></span>

## <a name="web-services"></a><span data-ttu-id="62275-195">Webtjenester</span><span class="sxs-lookup"><span data-stu-id="62275-195">Web Services</span></span>
<span data-ttu-id="62275-196">Det er enkelt å finne webtjenestene ved å søke etter webtjenester i [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="62275-196">An easy way to find the web services is to search for web services in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="62275-197">Pass på at det er merket av for Publiser i listen for webtjenestene som vises ovenfor.</span><span class="sxs-lookup"><span data-stu-id="62275-197">In the list make sure the Publish box is marked for the web services listed above.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="62275-198">Feilsøking</span><span class="sxs-lookup"><span data-stu-id="62275-198">Troubleshooting</span></span>
<span data-ttu-id="62275-199">Power BI-instrumentbordet er avhengig av de publiserte webtjenestene som er nevnt ovenfor, og du vil se data fra demonstrasjonsselskapet eller ditt eget selskap hvis du importerer data fra din gjeldende økonomiløsning.</span><span class="sxs-lookup"><span data-stu-id="62275-199">The Power BI dashboard relies on the published web services that are listed above, and it will show data from the demonstration company or your own company if you import data from your current finance solution.</span></span> <span data-ttu-id="62275-200">Hvis noe går galt, vil denne delen imidlertid gir en løsning for de vanligste problemene.</span><span class="sxs-lookup"><span data-stu-id="62275-200">However, if something goes wrong, this section provides a workaround for the most typical issues.</span></span>

### <a name="incorrect-company-name"></a><span data-ttu-id="62275-201">Feil selskapsnavn</span><span class="sxs-lookup"><span data-stu-id="62275-201">Incorrect Company Name</span></span>  
<span data-ttu-id="62275-202">En vanlige feil er angi visningsnavnet for selskapet i stedet for selskapsnavnet.</span><span class="sxs-lookup"><span data-stu-id="62275-202">A common mistake is to enter the company display name instead of the company name.</span></span> <span data-ttu-id="62275-203">Søk etter **Selskaper** for å finne selskapsnavnet.</span><span class="sxs-lookup"><span data-stu-id="62275-203">To find the company name search for **Companies**.</span></span> <span data-ttu-id="62275-204">Bruk **Navn**-feltet når du angir selskapsnavnet.</span><span class="sxs-lookup"><span data-stu-id="62275-204">Then use the **Name** field when entering your company name.</span></span>

### <a name="incorrect-user-name-and-password"></a><span data-ttu-id="62275-205">Feil brukernavn og passord</span><span class="sxs-lookup"><span data-stu-id="62275-205">Incorrect User Name and Password</span></span>  
<span data-ttu-id="62275-206">Brukernavnet og passordet som brukes for å koble til, er det samme som brukes for å koble til Microsoft Office 365-kontoen.</span><span class="sxs-lookup"><span data-stu-id="62275-206">The user name and password used to connect will be the same as what is used to connect to your Microsoft Office 365 account.</span></span>  

<span data-ttu-id="62275-207">Innholdspakker krever også at du har en Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-konto.</span><span class="sxs-lookup"><span data-stu-id="62275-207">The content packs also require that you have a Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account.</span></span> <span data-ttu-id="62275-208">Når du angir legitimasjonen, finner vi automatisk Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-leietakerne du har tilgang til.</span><span class="sxs-lookup"><span data-stu-id="62275-208">Once you enter your credentials, we will auto discover any Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] tenants you have access to.</span></span> <span data-ttu-id="62275-209">Hvis du ikke har en Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-konto som er lisensiert eller en prøveversjon, vises en feilmelding.</span><span class="sxs-lookup"><span data-stu-id="62275-209">If you do not have a licensed or trial Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account, you will receive an error message.</span></span>

### <a name="the-key-didnt-match-any-rows-in-the-table"></a><span data-ttu-id="62275-210">Nøkkelen samsvarer ikke med en rad i tabellen</span><span class="sxs-lookup"><span data-stu-id="62275-210">The Key Didn't Match Any Rows in the Table</span></span>
<span data-ttu-id="62275-211">Hvis du angir et ugyldige selskapsnavn under tilkoblingen, kan du få du feilmeldingen Nøkkelen samsvarer ikke med en rad i tabellen.</span><span class="sxs-lookup"><span data-stu-id="62275-211">If you enter a non-valid company name during the connection process, you may get the error message "The key didn't match any rows in the table".</span></span> <span data-ttu-id="62275-212">Angi riktig selskapsnavn, og prøv å koble til på nytt.</span><span class="sxs-lookup"><span data-stu-id="62275-212">Provide the correct company name and try connecting again.</span></span>

## <a name="see-also"></a><span data-ttu-id="62275-213">Se også</span><span class="sxs-lookup"><span data-stu-id="62275-213">See Also</span></span>
[<span data-ttu-id="62275-214">Komme i gang med Power BI</span><span class="sxs-lookup"><span data-stu-id="62275-214">Get started with Power BI</span></span>](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[<span data-ttu-id="62275-215">Power BI – grunnleggende begreper</span><span class="sxs-lookup"><span data-stu-id="62275-215">Power BI - Basic Concepts</span></span>](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)  
[<span data-ttu-id="62275-216">Forretningsintelligens</span><span class="sxs-lookup"><span data-stu-id="62275-216">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="62275-217">Komme i gang</span><span class="sxs-lookup"><span data-stu-id="62275-217">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="62275-218">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="62275-218">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="62275-219">[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="62275-219">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="62275-220">Finans</span><span class="sxs-lookup"><span data-stu-id="62275-220">Finance</span></span>](finance.md)  
<span data-ttu-id="62275-221">[Definere rapportering for [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="62275-221">[Setup Reporting for [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span></span>  

