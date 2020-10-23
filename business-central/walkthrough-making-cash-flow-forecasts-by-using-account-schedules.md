---
title: Gjennomgang – Lage kontantstrømprognoser ved å bruke kontoskjemaer | Microsoft-dokumentasjon
description: Denne gjennomgangen beskriver hvordan du kan bruke kontoskjemaer til å lage kontantstrømprognoser. Kontoskjemaer utfører beregninger som ikke kan utføres direkte i diagrammet over kontantstrømkontoer. I kontoskjemaer kan du definere delsummer for kontantstrømmottak og -utbetalinger. Disse delsummene kan inkluderes i nye totalsummer som deretter kan brukes til å lage kontantstrømprognoser.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 67a6e963800bf5f0ce8e1a293463d53b51470ee5
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914788"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a><span data-ttu-id="a098b-106">Gjennomgang: Lage kontantstrømprognoser ved å bruke kontoskjemaer</span><span class="sxs-lookup"><span data-stu-id="a098b-106">Walkthrough: Making Cash Flow Forecasts by Using Account Schedules</span></span>
<span data-ttu-id="a098b-107">Denne gjennomgangen beskriver hvordan du kan bruke kontoskjemaer til å lage kontantstrømprognoser.</span><span class="sxs-lookup"><span data-stu-id="a098b-107">This walkthrough describes how you can use account schedules to make cash flow forecasts.</span></span> <span data-ttu-id="a098b-108">Kontoskjemaer utfører beregninger som ikke kan utføres direkte i diagrammet over kontantstrømkontoer.</span><span class="sxs-lookup"><span data-stu-id="a098b-108">Account schedules perform calculations that cannot be done directly in the chart of cash flow accounts.</span></span> <span data-ttu-id="a098b-109">I kontoskjemaer kan du definere delsummer for kontantstrømmottak og -utbetalinger.</span><span class="sxs-lookup"><span data-stu-id="a098b-109">In the account schedules, you can set up subtotals for cash flow receipts and disbursements.</span></span> <span data-ttu-id="a098b-110">Disse delsummene kan inkluderes i nye totalsummer som deretter kan brukes til å lage kontantstrømprognoser.</span><span class="sxs-lookup"><span data-stu-id="a098b-110">These subtotals can be included in new totals that can then be used in making cash flow forecasts.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="a098b-111">Denne gjennomgangen</span><span class="sxs-lookup"><span data-stu-id="a098b-111">About This Walkthrough</span></span>  
<span data-ttu-id="a098b-112">Denne gjennomgangen beskriver følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="a098b-112">This walkthrough describes the following tasks:</span></span>  

- <span data-ttu-id="a098b-113">Definere et nytt navn for kontantstrømkontoskjema.</span><span class="sxs-lookup"><span data-stu-id="a098b-113">Setting up a new cash flow account schedule name.</span></span>  
- <span data-ttu-id="a098b-114">Definere kontoskjemalinjer.</span><span class="sxs-lookup"><span data-stu-id="a098b-114">Setting up account schedule lines.</span></span>  
- <span data-ttu-id="a098b-115">Definere et nytt kolonneoppsett.</span><span class="sxs-lookup"><span data-stu-id="a098b-115">Setting up a new column layout.</span></span>  
- <span data-ttu-id="a098b-116">Tilordne et kolonneoppsett til et kontoskjema.</span><span class="sxs-lookup"><span data-stu-id="a098b-116">Assigning a column layout to an account schedule.</span></span>  
- <span data-ttu-id="a098b-117">Vise og skrive ut kontantstrømprognosen.</span><span class="sxs-lookup"><span data-stu-id="a098b-117">Viewing and printing the cash flow forecast.</span></span>  

### <a name="prerequisites"></a><span data-ttu-id="a098b-118">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="a098b-118">Prerequisites</span></span>  
<span data-ttu-id="a098b-119">For å fullføre denne gjennomgangen må du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="a098b-119">To complete this walkthrough, you will need:</span></span>  

- [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="a098b-120">installert.</span><span class="sxs-lookup"><span data-stu-id="a098b-120">installed.</span></span>  
- <span data-ttu-id="a098b-121">Forslagslinjene for kontantstrøm registreres.</span><span class="sxs-lookup"><span data-stu-id="a098b-121">The cash flow worksheet lines are registered.</span></span>  

## <a name="roles"></a><span data-ttu-id="a098b-122">Roller</span><span class="sxs-lookup"><span data-stu-id="a098b-122">Roles</span></span>  
<span data-ttu-id="a098b-123">Denne gjennomgangen viser oppgaver som utføres av følgende brukerrolle:</span><span class="sxs-lookup"><span data-stu-id="a098b-123">This walkthrough demonstrates tasks that are performed by the following user role:</span></span>  

- <span data-ttu-id="a098b-124">Kontrollør</span><span class="sxs-lookup"><span data-stu-id="a098b-124">Controller</span></span>  

## <a name="story"></a><span data-ttu-id="a098b-125">Hovedscenario</span><span class="sxs-lookup"><span data-stu-id="a098b-125">Story</span></span>  
<span data-ttu-id="a098b-126">Ken er kontrollør på CRONUS og utarbeider månedlige kontantstrømprognoser.</span><span class="sxs-lookup"><span data-stu-id="a098b-126">Ken is a controller at CRONUS who makes monthly cash flow forecasts.</span></span> <span data-ttu-id="a098b-127">Han tar med finans, salg, kjøp og aktiva i prognosen, og deretter viser han den til ØKDIR Sara.</span><span class="sxs-lookup"><span data-stu-id="a098b-127">He includes finance, sales, purchase, and fixed assets in the forecast, and then he presents it to CFO Sara for business insight.</span></span>  

## <a name="setting-up-a-new-account-schedule-name"></a><span data-ttu-id="a098b-128">Definere et nytt kontoskjemanavn</span><span class="sxs-lookup"><span data-stu-id="a098b-128">Setting Up a New Account Schedule Name</span></span>  
<span data-ttu-id="a098b-129">Et kontoskjema består av et navn på kontoskjemaet for kontantstrøm med en rekke linjer og et kolonneoppsett.</span><span class="sxs-lookup"><span data-stu-id="a098b-129">An account schedule consists of a cash flow account schedule name with a series of lines and a column layout.</span></span>  

### <a name="to-set-up-a-new-account-schedule-name"></a><span data-ttu-id="a098b-130">Slik definerer du et nytt kontoskjemanavn</span><span class="sxs-lookup"><span data-stu-id="a098b-130">To set up a new account schedule name</span></span>  

1.  <span data-ttu-id="a098b-131">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kontoskjemaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a098b-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a098b-132">Velg **Ny** på siden **Kontoskjemanavn** for å opprette et nytt navn for kontantstrømkontoskjema.</span><span class="sxs-lookup"><span data-stu-id="a098b-132">On the **Account Schedule Names** page, choose the **New** to create a new cash flow account schedule name.</span></span>  
3.  <span data-ttu-id="a098b-133">I **Navn**-feltet angir du **Prognose**.</span><span class="sxs-lookup"><span data-stu-id="a098b-133">In the **Name** field, enter **Forecast**.</span></span>  
4.  <span data-ttu-id="a098b-134">I **Beskrivelse**-feltet angir du **Kontantstrømprognose**.</span><span class="sxs-lookup"><span data-stu-id="a098b-134">In the **Description** field, enter **Cash Flow Forecast**.</span></span>  
5.  <span data-ttu-id="a098b-135">La feltene **Standard kolonneoppsett** og **Analysevisningsnavn** være tomme.</span><span class="sxs-lookup"><span data-stu-id="a098b-135">Leave the **Default Column Layout** and **Analysis View Name** fields blank.</span></span>  

## <a name="setting-up-account-schedule-lines"></a><span data-ttu-id="a098b-136">Definere kontoskjemalinjer</span><span class="sxs-lookup"><span data-stu-id="a098b-136">Setting Up Account Schedule Lines</span></span>  
<span data-ttu-id="a098b-137">Etter at et kontoskjemanavn er angitt, definerer Ken hver linje som vises i kontoskjemaet for kontantstrøm.</span><span class="sxs-lookup"><span data-stu-id="a098b-137">After an account schedule name is set up, Ken defines each line that appears in the cash flow account schedule.</span></span> <span data-ttu-id="a098b-138">Ken definerer linjer som kan vises i rapporter, i tillegg til linjer som bare er til beregningsformål.</span><span class="sxs-lookup"><span data-stu-id="a098b-138">Ken defines lines that can be shown in reports in addition to lines that are only for calculation purposes.</span></span>  

### <a name="to-set-up-account-schedule-lines"></a><span data-ttu-id="a098b-139">Definere kontoskjemalinjer</span><span class="sxs-lookup"><span data-stu-id="a098b-139">To set up account schedule lines</span></span>  

1.  <span data-ttu-id="a098b-140">På siden **Kontoskjemanavn** velger du det nye **Prognose**-kontoskjemanavnet du opprettet, og deretter velger du handlingen **Rediger kontoskjema**.</span><span class="sxs-lookup"><span data-stu-id="a098b-140">On the **Account Schedule Names** page, select the new **Forecast** account schedule name that you have created, and then choose the **Edit Account Schedule** action.</span></span>  
2.  <span data-ttu-id="a098b-141">På siden **Kontoskjema** angir du hver linje nøyaktig, som vist i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a098b-141">On the **Account Schedule** page, enter each line exactly as shown in the following table.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="a098b-142">Du kan bruke funksjonen **Sett inn kontantstrømkonti** til raskt å merke kontantstrømkontoene i kontantstrømkontoplanen og kopiere dem til kontoskjemalinjer.</span><span class="sxs-lookup"><span data-stu-id="a098b-142">Using the **Insert CF Accounts** function, you can quickly mark the cash flow accounts from the chart of cash flow accounts and copy them to account schedule lines.</span></span>  

    |<span data-ttu-id="a098b-143">Radnr.</span><span class="sxs-lookup"><span data-stu-id="a098b-143">Row No.</span></span>|<span data-ttu-id="a098b-144">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a098b-144">Description</span></span>|<span data-ttu-id="a098b-145">Sammentellingstype</span><span class="sxs-lookup"><span data-stu-id="a098b-145">Totaling Type</span></span>|<span data-ttu-id="a098b-146">Sammentelling</span><span class="sxs-lookup"><span data-stu-id="a098b-146">Totaling</span></span>|<span data-ttu-id="a098b-147">Radtype</span><span class="sxs-lookup"><span data-stu-id="a098b-147">Row Type</span></span>|<span data-ttu-id="a098b-148">Beløpstype</span><span class="sxs-lookup"><span data-stu-id="a098b-148">Amount Type</span></span>|<span data-ttu-id="a098b-149">Vis</span><span class="sxs-lookup"><span data-stu-id="a098b-149">Show</span></span>|  
    |-------|-----------|-------------|--------|--------|-----------|----|
    |<span data-ttu-id="a098b-150">C10</span><span class="sxs-lookup"><span data-stu-id="a098b-150">C10</span></span>|<span data-ttu-id="a098b-151">Beløp</span><span class="sxs-lookup"><span data-stu-id="a098b-151">Amount</span></span>|<span data-ttu-id="a098b-152">Bevegelse</span><span class="sxs-lookup"><span data-stu-id="a098b-152">Net Change</span></span>|<span data-ttu-id="a098b-153">Poster</span><span class="sxs-lookup"><span data-stu-id="a098b-153">Entries</span></span>|<span data-ttu-id="a098b-154">Nettobeløp</span><span class="sxs-lookup"><span data-stu-id="a098b-154">Net Amount</span></span>|<span data-ttu-id="a098b-155">Alltid</span><span class="sxs-lookup"><span data-stu-id="a098b-155">Always</span></span>|  
    |<span data-ttu-id="a098b-156">C20</span><span class="sxs-lookup"><span data-stu-id="a098b-156">C20</span></span>|<span data-ttu-id="a098b-157">Beløp til dato</span><span class="sxs-lookup"><span data-stu-id="a098b-157">Amount until Date</span></span>|<span data-ttu-id="a098b-158">Saldo til dato</span><span class="sxs-lookup"><span data-stu-id="a098b-158">Balance at Date</span></span>|<span data-ttu-id="a098b-159">Poster</span><span class="sxs-lookup"><span data-stu-id="a098b-159">Entries</span></span>|<span data-ttu-id="a098b-160">Nettobeløp</span><span class="sxs-lookup"><span data-stu-id="a098b-160">Net Amount</span></span>|<span data-ttu-id="a098b-161">Alltid</span><span class="sxs-lookup"><span data-stu-id="a098b-161">Always</span></span>|  
    |<span data-ttu-id="a098b-162">C30</span><span class="sxs-lookup"><span data-stu-id="a098b-162">C30</span></span>|<span data-ttu-id="a098b-163">Hele regnskapsåret</span><span class="sxs-lookup"><span data-stu-id="a098b-163">Entire Fiscal Year</span></span>|<span data-ttu-id="a098b-164">Hele regnskapsåret</span><span class="sxs-lookup"><span data-stu-id="a098b-164">Entire Fiscal Year</span></span>|<span data-ttu-id="a098b-165">Poster</span><span class="sxs-lookup"><span data-stu-id="a098b-165">Entries</span></span>|<span data-ttu-id="a098b-166">Nettobeløp</span><span class="sxs-lookup"><span data-stu-id="a098b-166">Net Amount</span></span>|<span data-ttu-id="a098b-167">Alltid</span><span class="sxs-lookup"><span data-stu-id="a098b-167">Always</span></span>|  

4.  <span data-ttu-id="a098b-168">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="a098b-168">Choose the **OK** button.</span></span>  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="a098b-169">Tilordne kolonneoppsettet til kontoskjemanavnet</span><span class="sxs-lookup"><span data-stu-id="a098b-169">Assigning the Column Layout to the Account Schedule Name</span></span>  
<span data-ttu-id="a098b-170">Ken er nå klar til å tilordne kolonneoppsettet til kontoskjemanavnet.</span><span class="sxs-lookup"><span data-stu-id="a098b-170">Ken is now ready to assign the column layout to the account schedule name.</span></span>  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="a098b-171">Slik tilordner du kolonneoppsettet til kontoskjemanavnet:</span><span class="sxs-lookup"><span data-stu-id="a098b-171">To assign the column layout to the account schedule name</span></span>  

1.  <span data-ttu-id="a098b-172">På siden **Kontoskjemanavn** velger du **Prognose** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a098b-172">On the **Account Schedule Names** page, select **Forecast** in the **Name** field.</span></span>  
2.  <span data-ttu-id="a098b-173">Velg kolonneoppsettet **Kontantstrøm** i feltet **Standard kolonneoppsett** for å bruke det som standard kolonneoppsett.</span><span class="sxs-lookup"><span data-stu-id="a098b-173">In the **Default Column Layout** field, choose the column layout **Cash Flow** to assign as the default column layout.</span></span>  

### <a name="to-view-and-print-the-cash-flow-forecast"></a><span data-ttu-id="a098b-174">Slik viser og skriver du ut kontantstrømprognosen:</span><span class="sxs-lookup"><span data-stu-id="a098b-174">To view and print the cash flow forecast</span></span>  
1.  <span data-ttu-id="a098b-175">Velg **Oversikt**-handlingen på siden **Kontoskjemanavn** for å vise kontantstrømprognosen.</span><span class="sxs-lookup"><span data-stu-id="a098b-175">On the **Account Schedule Names** page, choose the **Overview** action to view the cash flow forecast.</span></span>  
2.  <span data-ttu-id="a098b-176">På siden **Kto.skjemaoversikt** kan du velge et beløp og deretter vise kontantstrømprognosepostene som utgjør beløpet.</span><span class="sxs-lookup"><span data-stu-id="a098b-176">On the **Acc. Schedule Overview** page, you can select an amount and then view the cash flow forecast entries that make up the amount.</span></span> <span data-ttu-id="a098b-177">I tillegg kan du vise formelen som brukes til å beregne beløpet.</span><span class="sxs-lookup"><span data-stu-id="a098b-177">In addition, you can view the formula that is used to calculate the amount.</span></span> <span data-ttu-id="a098b-178">Du kan også filtrere beløpene etter dato og dimensjon.</span><span class="sxs-lookup"><span data-stu-id="a098b-178">You can also filter the amounts by date and dimension.</span></span>  
3.  <span data-ttu-id="a098b-179">Velg **Skriv ut**-handlingen for å skrive ut kontantstrømprognosen.</span><span class="sxs-lookup"><span data-stu-id="a098b-179">Choose the **Print** action to print the cash flow forecast.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a098b-180">Se også</span><span class="sxs-lookup"><span data-stu-id="a098b-180">See Also</span></span>  
 <span data-ttu-id="a098b-181">[Arbeide med kontoskjemaer](bi-how-work-account-schedule.md) </span><span class="sxs-lookup"><span data-stu-id="a098b-181">[Work with Account Schedules](bi-how-work-account-schedule.md) </span></span>  
 [<span data-ttu-id="a098b-182">Gjennomgang av forretningsprosesser</span><span class="sxs-lookup"><span data-stu-id="a098b-182">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="a098b-183">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a098b-183">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
