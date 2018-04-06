---
title: "Gjennomgang – Lage kontantstrømprognoser ved å bruke kontoskjemaer | Microsoft-dokumentasjon"
description: "Denne gjennomgangen beskriver hvordan du kan bruke kontoskjemaer til å lage kontantstrømprognoser. Kontoskjemaer utfører beregninger som ikke kan utføres direkte i diagrammet over kontantstrømkontoer. I kontoskjemaer kan du definere delsummer for kontantstrømmottak og -utbetalinger. Disse delsummene kan inkluderes i nye totalsummer som deretter kan brukes til å lage kontantstrømprognoser."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 25319bae1d601d6beddca35cf8edc032ac11eda6
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a><span data-ttu-id="a8a65-106">Gjennomgang: Lage kontantstrømprognoser ved å bruke kontoskjemaer</span><span class="sxs-lookup"><span data-stu-id="a8a65-106">Walkthrough: Making Cash Flow Forecasts by Using Account Schedules</span></span>
<span data-ttu-id="a8a65-107">Denne gjennomgangen beskriver hvordan du kan bruke kontoskjemaer til å lage kontantstrømprognoser.</span><span class="sxs-lookup"><span data-stu-id="a8a65-107">This walkthrough describes how you can use account schedules to make cash flow forecasts.</span></span> <span data-ttu-id="a8a65-108">Kontoskjemaer utfører beregninger som ikke kan utføres direkte i diagrammet over kontantstrømkontoer.</span><span class="sxs-lookup"><span data-stu-id="a8a65-108">Account schedules perform calculations that cannot be done directly in the chart of cash flow accounts.</span></span> <span data-ttu-id="a8a65-109">I kontoskjemaer kan du definere delsummer for kontantstrømmottak og -utbetalinger.</span><span class="sxs-lookup"><span data-stu-id="a8a65-109">In the account schedules, you can set up subtotals for cash flow receipts and disbursements.</span></span> <span data-ttu-id="a8a65-110">Disse delsummene kan inkluderes i nye totalsummer som deretter kan brukes til å lage kontantstrømprognoser.</span><span class="sxs-lookup"><span data-stu-id="a8a65-110">These subtotals can be included in new totals that can then be used in making cash flow forecasts.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="a8a65-111">Denne gjennomgangen</span><span class="sxs-lookup"><span data-stu-id="a8a65-111">About This Walkthrough</span></span>  
<span data-ttu-id="a8a65-112">Denne gjennomgangen beskriver følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="a8a65-112">This walkthrough describes the following tasks:</span></span>  

- <span data-ttu-id="a8a65-113">Definere et nytt navn for kontantstrømkontoskjema.</span><span class="sxs-lookup"><span data-stu-id="a8a65-113">Setting up a new cash flow account schedule name.</span></span>  
- <span data-ttu-id="a8a65-114">Definere kontoskjemalinjer.</span><span class="sxs-lookup"><span data-stu-id="a8a65-114">Setting up account schedule lines.</span></span>  
- <span data-ttu-id="a8a65-115">Definere et nytt kolonneoppsett.</span><span class="sxs-lookup"><span data-stu-id="a8a65-115">Setting up a new column layout.</span></span>  
- <span data-ttu-id="a8a65-116">Tilordne et kolonneoppsett til et kontoskjema.</span><span class="sxs-lookup"><span data-stu-id="a8a65-116">Assigning a column layout to an account schedule.</span></span>  
- <span data-ttu-id="a8a65-117">Vise og skrive ut kontantstrømprognosen.</span><span class="sxs-lookup"><span data-stu-id="a8a65-117">Viewing and printing the cash flow forecast.</span></span>  

### <a name="prerequisites"></a><span data-ttu-id="a8a65-118">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="a8a65-118">Prerequisites</span></span>  
<span data-ttu-id="a8a65-119">For å fullføre denne gjennomgangen må du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="a8a65-119">To complete this walkthrough, you will need:</span></span>  

- [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="a8a65-120"> installert.</span><span class="sxs-lookup"><span data-stu-id="a8a65-120"> installed.</span></span>  
- <span data-ttu-id="a8a65-121">Forslagslinjene for kontantstrøm registreres.</span><span class="sxs-lookup"><span data-stu-id="a8a65-121">The cash flow worksheet lines are registered.</span></span>  

## <a name="roles"></a><span data-ttu-id="a8a65-122">Roller</span><span class="sxs-lookup"><span data-stu-id="a8a65-122">Roles</span></span>  
<span data-ttu-id="a8a65-123">Denne gjennomgangen viser oppgaver som utføres av følgende brukerrolle:</span><span class="sxs-lookup"><span data-stu-id="a8a65-123">This walkthrough demonstrates tasks that are performed by the following user role:</span></span>  

- <span data-ttu-id="a8a65-124">Kontrollør</span><span class="sxs-lookup"><span data-stu-id="a8a65-124">Controller</span></span>  

## <a name="story"></a><span data-ttu-id="a8a65-125">Hovedscenario</span><span class="sxs-lookup"><span data-stu-id="a8a65-125">Story</span></span>  
<span data-ttu-id="a8a65-126">Ken er kontrollør i CRONUS og utarbeider månedlige kontantstrømprognoser.</span><span class="sxs-lookup"><span data-stu-id="a8a65-126">Ken is a controller at CRONUS who makes monthly cash flow forecasts.</span></span> <span data-ttu-id="a8a65-127">Han tar med finans, salg, kjøp og aktiva i prognosen, og deretter viser han den til ØKDIR Sara.</span><span class="sxs-lookup"><span data-stu-id="a8a65-127">He includes finance, sales, purchase, and fixed assets in the forecast, and then he presents it to CFO Sara for business insight.</span></span>  

## <a name="setting-up-a-new-account-schedule-name"></a><span data-ttu-id="a8a65-128">Definere et nytt kontoskjemanavn</span><span class="sxs-lookup"><span data-stu-id="a8a65-128">Setting Up a New Account Schedule Name</span></span>  
<span data-ttu-id="a8a65-129">Et kontoskjema består av et navn på kontoskjemaet for kontantstrøm med en rekke linjer og et kolonneoppsett.</span><span class="sxs-lookup"><span data-stu-id="a8a65-129">An account schedule consists of a cash flow account schedule name with a series of lines and a column layout.</span></span>  

### <a name="to-set-up-a-new-account-schedule-name"></a><span data-ttu-id="a8a65-130">Slik definerer du et nytt kontoskjemanavn</span><span class="sxs-lookup"><span data-stu-id="a8a65-130">To set up a new account schedule name</span></span>  

1.  <span data-ttu-id="a8a65-131">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kontoskjemaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a8a65-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a8a65-132">Velg **Ny** i vinduet **Kontoskjemanavn** for å opprette et nytt navn for kontantstrømkontoskjema..</span><span class="sxs-lookup"><span data-stu-id="a8a65-132">In the **Account Schedule Names** window, choose the **New** to create a new cash flow account schedule name.</span></span>  
3.  <span data-ttu-id="a8a65-133">I **Navn**-feltet angir du **Prognose**.</span><span class="sxs-lookup"><span data-stu-id="a8a65-133">In the **Name** field, enter **Forecast**.</span></span>  
4.  <span data-ttu-id="a8a65-134">I **Beskrivelse**-feltet angir du **Kontantstrømprognose**.</span><span class="sxs-lookup"><span data-stu-id="a8a65-134">In the **Description** field, enter **Cash Flow Forecast**.</span></span>  
5.  <span data-ttu-id="a8a65-135">La feltene **Standard kolonneoppsett** og **Analysevisningsnavn** være tomme.</span><span class="sxs-lookup"><span data-stu-id="a8a65-135">Leave the **Default Column Layout** and **Analysis View Name** fields blank.</span></span>  

## <a name="setting-up-account-schedule-lines"></a><span data-ttu-id="a8a65-136">Definere kontoskjemalinjer</span><span class="sxs-lookup"><span data-stu-id="a8a65-136">Setting Up Account Schedule Lines</span></span>  
<span data-ttu-id="a8a65-137">Etter at et kontoskjemanavn er angitt, definerer Ken hver linje som vises i kontoskjemaet for kontantstrøm.</span><span class="sxs-lookup"><span data-stu-id="a8a65-137">After an account schedule name is set up, Ken defines each line that appears in the cash flow account schedule.</span></span> <span data-ttu-id="a8a65-138">Ken definerer linjer som kan vises i rapporter, i tillegg til linjer som bare er til beregningsformål.</span><span class="sxs-lookup"><span data-stu-id="a8a65-138">Ken defines lines that can be shown in reports in addition to lines that are only for calculation purposes.</span></span>  

### <a name="to-set-up-account-schedule-lines"></a><span data-ttu-id="a8a65-139">Definere kontoskjemalinjer</span><span class="sxs-lookup"><span data-stu-id="a8a65-139">To set up account schedule lines</span></span>  

1.  <span data-ttu-id="a8a65-140">Velg det nye kontoskjemanavnet for **Prognose** du har opprettet, i vinduet **Kontoskjemanavn**.</span><span class="sxs-lookup"><span data-stu-id="a8a65-140">In the **Account Schedule Names** window, select the new **Forecast** account schedule name that you have created.</span></span> <span data-ttu-id="a8a65-141">I fanebladet **Hjem**, under **Prosess**, velger du **Rediger kontoskjema**.</span><span class="sxs-lookup"><span data-stu-id="a8a65-141">On the **Home** tab, in the **Process** group, choose **Edit Account Schedule**.</span></span>  
2.  <span data-ttu-id="a8a65-142">I vinduet **Kontoskjema** angir du hver linje nøyaktig, som vist i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a8a65-142">In the **Account Schedule** window, enter each line exactly as shown in the following table.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="a8a65-143">Du kan bruke funksjonen **Sett inn kontantstrømkonti** til raskt å merke kontantstrømkontoene i kontantstrømkontoplanen og kopiere dem til kontoskjemalinjer.</span><span class="sxs-lookup"><span data-stu-id="a8a65-143">Using the **Insert CF Accounts** function, you can quickly mark the cash flow accounts from the chart of cash flow accounts and copy them to account schedule lines.</span></span>  

    <span data-ttu-id="a8a65-144">|Radnr.|Beskrivelse|Sammentellingstype|Sammentelling|Radtype|Beløpstype|Vis|</span><span class="sxs-lookup"><span data-stu-id="a8a65-144">|Row No.|Description|Totaling Type|Totaling|Row Type|Amount Type|Show|</span></span>  
    <span data-ttu-id="a8a65-145">|-------|-----------|-------------|--------|--------|---  ------|----| |C10|Beløp|Bevegelse|Poster|Nettobeløp|Alltid|</span><span class="sxs-lookup"><span data-stu-id="a8a65-145">|-------|-----------|-------------|--------|--------|---  ------|----| |C10|Amount|Net Change|Entries|Net Amount|Always|</span></span>  
    <span data-ttu-id="a8a65-146">|C20|Beløp til dato|Saldo per dato|Poster|Nettobeløp|Alltid|</span><span class="sxs-lookup"><span data-stu-id="a8a65-146">|C20|Amount until Date|Balance at Date|Entries|Net Amount|Always|</span></span>  
    <span data-ttu-id="a8a65-147">|C30|Helt regnskapsår|Helt regnskapsår|Poster|Nettobeløp Beløp|Alltid|</span><span class="sxs-lookup"><span data-stu-id="a8a65-147">|C30|Entire Fiscal Year|Entire Fiscal Year|Entries|Net Amount|Always|</span></span>  

4.  <span data-ttu-id="a8a65-148">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a8a65-148">Choose the **OK** button.</span></span>  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="a8a65-149">Tilordne kolonneoppsettet til kontoskjemanavnet</span><span class="sxs-lookup"><span data-stu-id="a8a65-149">Assigning the Column Layout to the Account Schedule Name</span></span>  
<span data-ttu-id="a8a65-150">Ken er nå klar til å tilordne kolonneoppsettet til kontoskjemanavnet.</span><span class="sxs-lookup"><span data-stu-id="a8a65-150">Ken is now ready to assign the column layout to the account schedule name.</span></span>  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="a8a65-151">Slik tilordner du kolonneoppsettet til kontoskjemanavnet:</span><span class="sxs-lookup"><span data-stu-id="a8a65-151">To assign the column layout to the account schedule name</span></span>  

1.  <span data-ttu-id="a8a65-152">I vinduet **Kontoskjemanavn** velger du **Prognose** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a8a65-152">In the **Account Schedule Names** window, select **Forecast** in the **Name** field.</span></span>  
2.  <span data-ttu-id="a8a65-153">Velg kolonneoppsettet **Kontantstrøm** i feltet **Standard kolonneoppsett** for å bruke det som standard kolonneoppsett.</span><span class="sxs-lookup"><span data-stu-id="a8a65-153">In the **Default Column Layout** field, choose the column layout **Cash Flow** to assign as the default column layout.</span></span>  

### <a name="to-view-and-print-the-cash-flow-forecast"></a><span data-ttu-id="a8a65-154">Slik viser og skriver du ut kontantstrømprognosen:</span><span class="sxs-lookup"><span data-stu-id="a8a65-154">To view and print the cash flow forecast</span></span>  
1.  <span data-ttu-id="a8a65-155">Velg **Oversikt**-handlingen i vinduet **Kontoskjemanavn** for å vise kontantstrømprognosen.</span><span class="sxs-lookup"><span data-stu-id="a8a65-155">In the **Account Schedule Names** window, choose the **Overview** action to view the cash flow forecast.</span></span>  
2.  <span data-ttu-id="a8a65-156">I vinduet **Kto.skjemaoversikt** kan du velge et beløp og deretter vise kontantstrømprognosepostene som utgjør beløpet.</span><span class="sxs-lookup"><span data-stu-id="a8a65-156">In the **Acc. Schedule Overview** window, you can select an amount and then view the cash flow forecast entries that make up the amount.</span></span> <span data-ttu-id="a8a65-157">I tillegg kan du vise formelen som brukes til å beregne beløpet.</span><span class="sxs-lookup"><span data-stu-id="a8a65-157">In addition, you can view the formula that is used to calculate the amount.</span></span> <span data-ttu-id="a8a65-158">Du kan også filtrere beløpene etter dato og dimensjon.</span><span class="sxs-lookup"><span data-stu-id="a8a65-158">You can also filter the amounts by date and dimension.</span></span>  
3.  <span data-ttu-id="a8a65-159">Velg **Skriv ut**-handlingen for å skrive ut kontantstrømprognosen.</span><span class="sxs-lookup"><span data-stu-id="a8a65-159">Choose the **Print** action to print the cash flow forecast.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a8a65-160">Se også</span><span class="sxs-lookup"><span data-stu-id="a8a65-160">See Also</span></span>  
 <span data-ttu-id="a8a65-161">[Arbeide med kontoskjemaer](bi-how-work-account-schedule.md) </span><span class="sxs-lookup"><span data-stu-id="a8a65-161">[Work with Account Schedules](bi-how-work-account-schedule.md) </span></span>  
 [<span data-ttu-id="a8a65-162">Gjennomgang av forretningsprosesser</span><span class="sxs-lookup"><span data-stu-id="a8a65-162">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="a8a65-163">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a8a65-163">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

