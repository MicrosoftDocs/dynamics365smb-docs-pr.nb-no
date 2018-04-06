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
ms.date: 03/16/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 315d4b188cdd834e82676a0c5ef77272ad873eb7
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="connecting-power-bi-to-business-central-content-packs"></a><span data-ttu-id="fb39f-103">Koble Power BI til Business Central-innholdspakker</span><span class="sxs-lookup"><span data-stu-id="fb39f-103">Connecting Power BI to Business Central Content Packs</span></span>
<span data-ttu-id="fb39f-104">Få innsikt i Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-dataene på en enkel måte med Power BI og Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-innholdspakkene.</span><span class="sxs-lookup"><span data-stu-id="fb39f-104">Getting insights into your Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data is easy with Power BI and the Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] content packs.</span></span> <span data-ttu-id="fb39f-105">Power BI henter dataene, og bygger deretter et forhåndskonfigurert instrumentbord og rapporter basert på dataene.</span><span class="sxs-lookup"><span data-stu-id="fb39f-105">Power BI retrieves your data then builds an out-of-the-box dashboard and reports based on that data.</span></span>

> [!NOTE]  
>  <span data-ttu-id="fb39f-106">Du må ha en gyldig konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] og med Power BI.</span><span class="sxs-lookup"><span data-stu-id="fb39f-106">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Power BI.</span></span> <span data-ttu-id="fb39f-107">Du må også laste ned [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span><span class="sxs-lookup"><span data-stu-id="fb39f-107">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span></span>  
>  <span data-ttu-id="fb39f-108">Power BI-innholdspakker krever tilgang til tabellene der opplysningene hentes fra.</span><span class="sxs-lookup"><span data-stu-id="fb39f-108">Power BI content packs require permissions to the tables where data is retrieved from.</span></span> <span data-ttu-id="fb39f-109">Du finner mer informasjon om kravene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="fb39f-109">More details on the requirements are described below.</span></span>  

## <a name="how-to-connect"></a><span data-ttu-id="fb39f-110">Koble til</span><span class="sxs-lookup"><span data-stu-id="fb39f-110">How to Connect</span></span>
1. <span data-ttu-id="fb39f-111">Velg **Hent data** nederst i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="fb39f-111">Select **Get Data** at the bottom of the left navigation pane.</span></span>  
<span data-ttu-id="fb39f-112">![Navigere til Hent data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span><span class="sxs-lookup"><span data-stu-id="fb39f-112">![Navigating to Get Data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span></span>
2. <span data-ttu-id="fb39f-113">I **Tjenester**-boksen velger du **Hent**.</span><span class="sxs-lookup"><span data-stu-id="fb39f-113">In the **Services** box, select **Get**.</span></span> <span data-ttu-id="fb39f-114">Dette åpner et vindu med **AppSource** og **Apper for Power BI-apper**.</span><span class="sxs-lookup"><span data-stu-id="fb39f-114">This will open a window with the **AppSource** and **Apps for Power BI apps**.</span></span>  
<span data-ttu-id="fb39f-115">![Velge innholdspakker fra elektroniske tjenester](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span><span class="sxs-lookup"><span data-stu-id="fb39f-115">![Choose content packs from online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span></span>
3. <span data-ttu-id="fb39f-116">Velg **Apper** fra fanen **Apper for Power BI-apper**, og velg innholdspakken **Microsoft Dynamics 365 Business Central** som du vil bruke, og velg deretter **Få det nå**.</span><span class="sxs-lookup"><span data-stu-id="fb39f-116">Select **Apps** from the **Apps for Power BI apps** tab, and choose the **Microsoft Dynamics 365 Business Central** content pack that you want to use, and then select **Get it now**.</span></span>  
<span data-ttu-id="fb39f-117">![Velg Dynamics 365 Business Central, og velg Få det nå](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span><span class="sxs-lookup"><span data-stu-id="fb39f-117">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span></span>
4. <span data-ttu-id="fb39f-118">Når du blir spurt, skriver du inn navnet på *selskapet ditt* i [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fb39f-118">When prompted, enter the name of *your company* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="fb39f-119">Dette er ikke visningsnavnet.</span><span class="sxs-lookup"><span data-stu-id="fb39f-119">This is not the display name.</span></span>  
<span data-ttu-id="fb39f-120">![Velg Dynamics 365 Business Central, og velg Få det nå](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span><span class="sxs-lookup"><span data-stu-id="fb39f-120">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span></span>
5. <span data-ttu-id="fb39f-121">Når du er tilkoblet, lastes det automatisk inn et instrumentbord, en rapport og et datasett i Power BI-arbeidområdet.</span><span class="sxs-lookup"><span data-stu-id="fb39f-121">Once connected, a dashboard, report and dataset will automatically be loaded into your Power BI workspace.</span></span> <span data-ttu-id="fb39f-122">Når du er ferdig, oppdateres flisene med dataene fra kontoen.</span><span class="sxs-lookup"><span data-stu-id="fb39f-122">When completed, the tiles will update with data from your account.</span></span>
<span data-ttu-id="fb39f-123">![Velg Dynamics 365 Business Central, og velg Få det nå](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="fb39f-123">![Select Dynamics 365 Business Central  and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span></span>

## <a name="what-now"></a><span data-ttu-id="fb39f-124">Hva nå?</span><span class="sxs-lookup"><span data-stu-id="fb39f-124">What Now?</span></span>

- <span data-ttu-id="fb39f-125">[Endre flisene](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) i instrumentbordet.</span><span class="sxs-lookup"><span data-stu-id="fb39f-125">[Change the tiles](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in the dashboard.</span></span>  
- <span data-ttu-id="fb39f-126">[Velge en flis](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) for å åpne den underliggende rapporten.</span><span class="sxs-lookup"><span data-stu-id="fb39f-126">[Select a tile](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) to open the underlying report.</span></span>  
- <span data-ttu-id="fb39f-127">Selv om det er planlagt at datasettet ditt oppdateres daglig, kan du endre oppdateringstidsplanen eller prøve å oppdatere den ved behov ved hjelp av **Oppdater nå**.</span><span class="sxs-lookup"><span data-stu-id="fb39f-127">While your dataset will be scheduled to refreshed daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="fb39f-128">Systemkrav</span><span class="sxs-lookup"><span data-stu-id="fb39f-128">System Requirements</span></span>
<span data-ttu-id="fb39f-129">Hvis du vil importere [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-dataene til Power BI, må du ha tillatelse til å webtjenestene som brukes for å hente data.</span><span class="sxs-lookup"><span data-stu-id="fb39f-129">To import your [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data into Power BI, you need to have permissions to the web services used to retrieve data.</span></span> <span data-ttu-id="fb39f-130">Webtjenestene som kreves for hver innholdspakke:</span><span class="sxs-lookup"><span data-stu-id="fb39f-130">The web services required for each content pack include:</span></span>

<span data-ttu-id="fb39f-131">**Microsoft Dynamics 365 Business Central – CRM**</span><span class="sxs-lookup"><span data-stu-id="fb39f-131">**Microsoft Dynamics 365 Business Central – CRM**</span></span>
- <span data-ttu-id="fb39f-132">SalesOpportunities</span><span class="sxs-lookup"><span data-stu-id="fb39f-132">SalesOpportunities</span></span>
- <span data-ttu-id="fb39f-133">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="fb39f-133">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="fb39f-134">**Microsoft Dynamics 365 Business Central – salg**</span><span class="sxs-lookup"><span data-stu-id="fb39f-134">**Microsoft Dynamics 365 Business Central – Sales**</span></span>
- <span data-ttu-id="fb39f-135">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="fb39f-135">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="fb39f-136">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="fb39f-136">SalesDashboard</span></span>
- <span data-ttu-id="fb39f-137">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="fb39f-137">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="fb39f-138">**Microsoft Dynamics 365 Business Central – finans**</span><span class="sxs-lookup"><span data-stu-id="fb39f-138">**Microsoft Dynamics 365 Business Central – Finance**</span></span>
- <span data-ttu-id="fb39f-139">PowerBIFinance</span><span class="sxs-lookup"><span data-stu-id="fb39f-139">PowerBIFinance</span></span>
- <span data-ttu-id="fb39f-140">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="fb39f-140">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="fb39f-141">**Microsoft Dynamics 365 Business Central – prosjekter**</span><span class="sxs-lookup"><span data-stu-id="fb39f-141">**Microsoft Dynamics 365 Business Central – Jobs**</span></span>
- <span data-ttu-id="fb39f-142">Prosjektoversikt</span><span class="sxs-lookup"><span data-stu-id="fb39f-142">Job List</span></span>
- <span data-ttu-id="fb39f-143">Prosjektplanleggingslinjer</span><span class="sxs-lookup"><span data-stu-id="fb39f-143">Job Planning Lines</span></span>
- <span data-ttu-id="fb39f-144">Prosjektoppgavelinjer</span><span class="sxs-lookup"><span data-stu-id="fb39f-144">Job Task Lines</span></span>

<span data-ttu-id="fb39f-145">**Microsoft Dynamics 365 Business Central – kundeliste**</span><span class="sxs-lookup"><span data-stu-id="fb39f-145">**Microsoft Dynamics 365 Business Central – Customers List**</span></span>
- <span data-ttu-id="fb39f-146">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="fb39f-146">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="fb39f-147">Varekjøpsliste_for_Power_BI</span><span class="sxs-lookup"><span data-stu-id="fb39f-147">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="fb39f-148">Varesalgsliste_for_Power_BI</span><span class="sxs-lookup"><span data-stu-id="fb39f-148">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="fb39f-149">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="fb39f-149">SalesDashboard</span></span>
- <span data-ttu-id="fb39f-150">Kundeliste_for_Power_BI</span><span class="sxs-lookup"><span data-stu-id="fb39f-150">Power_BI_Customer_List</span></span>
- <span data-ttu-id="fb39f-151">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="fb39f-151">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="fb39f-152">**Microsoft Dynamics 365 Business Central – vareliste**</span><span class="sxs-lookup"><span data-stu-id="fb39f-152">**Microsoft Dynamics 365 Business Central – Items List**</span></span>
- <span data-ttu-id="fb39f-153">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="fb39f-153">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="fb39f-154">Varekjøpsliste_for_Power_BI</span><span class="sxs-lookup"><span data-stu-id="fb39f-154">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="fb39f-155">Varesalgsliste_for_Power_BI</span><span class="sxs-lookup"><span data-stu-id="fb39f-155">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="fb39f-156">Varer</span><span class="sxs-lookup"><span data-stu-id="fb39f-156">Items</span></span>
- <span data-ttu-id="fb39f-157">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="fb39f-157">SalesDashboard</span></span>
- <span data-ttu-id="fb39f-158">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="fb39f-158">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="fb39f-159">**Microsoft Dynamics 365 Business Central – leverandørliste**</span><span class="sxs-lookup"><span data-stu-id="fb39f-159">**Microsoft Dynamics 365 Business Central – Vendors List**</span></span>
- <span data-ttu-id="fb39f-160">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="fb39f-160">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="fb39f-161">Varekjøpsliste_for_Power_BI</span><span class="sxs-lookup"><span data-stu-id="fb39f-161">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="fb39f-162">Varesalgsliste_for_Power_BI</span><span class="sxs-lookup"><span data-stu-id="fb39f-162">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="fb39f-163">Varer</span><span class="sxs-lookup"><span data-stu-id="fb39f-163">Items</span></span>
- <span data-ttu-id="fb39f-164">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="fb39f-164">SalesDashboard</span></span>
- <span data-ttu-id="fb39f-165">Kundeliste_for_Power_BI</span><span class="sxs-lookup"><span data-stu-id="fb39f-165">Power_BI_Customer_List</span></span>
- <span data-ttu-id="fb39f-166">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="fb39f-166">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="fb39f-167">Leverandørliste_for_Power_BI</span><span class="sxs-lookup"><span data-stu-id="fb39f-167">Power_BI_Vendor_List</span></span>
- <span data-ttu-id="fb39f-168">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="fb39f-168">ExcelTemplateViewCompany</span></span>

## <a name="web-services"></a><span data-ttu-id="fb39f-169">Webtjenester</span><span class="sxs-lookup"><span data-stu-id="fb39f-169">Web Services</span></span>
<span data-ttu-id="fb39f-170">Det er enkelt å finne webtjenestene ved å søke etter webtjenester i [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fb39f-170">An easy way to find the web services is to search for web services in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="fb39f-171">Pass på at det er merket av for Publiser i listen for webtjenestene som vises ovenfor.</span><span class="sxs-lookup"><span data-stu-id="fb39f-171">In the list make sure the Publish box is marked for the web services listed above.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="fb39f-172">Feilsøking</span><span class="sxs-lookup"><span data-stu-id="fb39f-172">Troubleshooting</span></span>
<span data-ttu-id="fb39f-173">Power BI-instrumentbordet er avhengig av de publiserte webtjenestene som er nevnt ovenfor, og du vil se data fra demonstrasjonsselskapet eller ditt eget selskap hvis du importerer data fra din gjeldende økonomiløsning.</span><span class="sxs-lookup"><span data-stu-id="fb39f-173">The Power BI dashboard relies on the published web services that are listed above, and it will show data from the demonstration company or your own company if you import data from your current finance solution.</span></span> <span data-ttu-id="fb39f-174">Hvis noe går galt, vil denne delen imidlertid gir en løsning for de vanligste problemene.</span><span class="sxs-lookup"><span data-stu-id="fb39f-174">However, if something goes wrong, this section provides a workaround for the most typical issues.</span></span>

### <a name="incorrect-company-name"></a><span data-ttu-id="fb39f-175">Feil selskapsnavn</span><span class="sxs-lookup"><span data-stu-id="fb39f-175">Incorrect Company Name</span></span>  
<span data-ttu-id="fb39f-176">En vanlige feil er angi visningsnavnet for selskapet i stedet for selskapsnavnet.</span><span class="sxs-lookup"><span data-stu-id="fb39f-176">A common mistake is to enter the company display name instead of the company name.</span></span> <span data-ttu-id="fb39f-177">Søk etter **Selskaper** for å finne selskapsnavnet.</span><span class="sxs-lookup"><span data-stu-id="fb39f-177">To find the company name search for **Companies**.</span></span> <span data-ttu-id="fb39f-178">Bruk **Navn**-feltet når du angir selskapsnavnet.</span><span class="sxs-lookup"><span data-stu-id="fb39f-178">Then use the **Name** field when entering your company name.</span></span>

### <a name="incorrect-user-name-and-password"></a><span data-ttu-id="fb39f-179">Feil brukernavn og passord</span><span class="sxs-lookup"><span data-stu-id="fb39f-179">Incorrect User Name and Password</span></span>  
<span data-ttu-id="fb39f-180">Brukernavnet og passordet som brukes for å koble til, er det samme som brukes for å koble til Microsoft Office 365-kontoen.</span><span class="sxs-lookup"><span data-stu-id="fb39f-180">The user name and password used to connect will be the same as what is used to connect to your Microsoft Office 365 account.</span></span>  

<span data-ttu-id="fb39f-181">Innholdspakker krever også at du har en Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-konto.</span><span class="sxs-lookup"><span data-stu-id="fb39f-181">The content packs also require that you have a Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account.</span></span> <span data-ttu-id="fb39f-182">Når du angir legitimasjonen, finner vi automatisk Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-leietakerne du har tilgang til.</span><span class="sxs-lookup"><span data-stu-id="fb39f-182">Once you enter your credentials, we will auto discover any Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] tenants you have access to.</span></span> <span data-ttu-id="fb39f-183">Hvis du ikke har en Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-konto som er lisensiert eller en prøveversjon, vises en feilmelding.</span><span class="sxs-lookup"><span data-stu-id="fb39f-183">If you do not have a licensed or trial Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account, you will receive an error message.</span></span>

### <a name="the-key-didnt-match-any-rows-in-the-table"></a><span data-ttu-id="fb39f-184">Nøkkelen samsvarer ikke med en rad i tabellen</span><span class="sxs-lookup"><span data-stu-id="fb39f-184">The Key Didn't Match Any Rows in the Table</span></span>
<span data-ttu-id="fb39f-185">Hvis du angir et ugyldige selskapsnavn under tilkoblingen, kan du få du feilmeldingen Nøkkelen samsvarer ikke med en rad i tabellen.</span><span class="sxs-lookup"><span data-stu-id="fb39f-185">If you enter a non valid company name during the connection process, you may get the error message "The key didn't match any rows in the table".</span></span> <span data-ttu-id="fb39f-186">Angi riktig selskapsnavn, og prøv å koble til på nytt.</span><span class="sxs-lookup"><span data-stu-id="fb39f-186">Provide the correct company name and try connecting again.</span></span>

## <a name="see-also"></a><span data-ttu-id="fb39f-187">Se også</span><span class="sxs-lookup"><span data-stu-id="fb39f-187">See Also</span></span>
[<span data-ttu-id="fb39f-188">Komme i gang med Power BI</span><span class="sxs-lookup"><span data-stu-id="fb39f-188">Get started with Power BI</span></span>](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
<span data-ttu-id="fb39f-189">[Power BI – grunnleggende begreper](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Forretningsintelligens](bi.md)</span><span class="sxs-lookup"><span data-stu-id="fb39f-189">[Power BI - Basic Concepts](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Business Intelligence](bi.md)</span></span>  
<span data-ttu-id="fb39f-190">[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="fb39f-190">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="fb39f-191">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="fb39f-191">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="fb39f-192">[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="fb39f-192">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="fb39f-193">Finans</span><span class="sxs-lookup"><span data-stu-id="fb39f-193">Finance</span></span>](finance.md)  
<span data-ttu-id="fb39f-194">[Definere rapportering for [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="fb39f-194">[Setup Reporting for [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span></span>  

