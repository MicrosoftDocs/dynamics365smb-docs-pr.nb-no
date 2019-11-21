---
title: Gjennomgang – Lage kontantstrømprognoser ved å bruke kontoskjemaer | Microsoft-dokumentasjon
description: Denne gjennomgangen beskriver hvordan du kan bruke kontoskjemaer til å lage kontantstrømprognoser. Kontoskjemaer utfører beregninger som ikke kan utføres direkte i diagrammet over kontantstrømkontoer. I kontoskjemaer kan du definere delsummer for kontantstrømmottak og -utbetalinger. Disse delsummene kan inkluderes i nye totalsummer som deretter kan brukes til å lage kontantstrømprognoser.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 415cabbb859bfc49477f69b19ad4a4daf1137837
ms.sourcegitcommit: 319023e53627dbe8e68643908aacc6fd594a4957
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/04/2019
ms.locfileid: "2554695"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a><span data-ttu-id="52ccc-106">Gjennomgang: Lage kontantstrømprognoser ved å bruke kontoskjemaer</span><span class="sxs-lookup"><span data-stu-id="52ccc-106">Walkthrough: Making Cash Flow Forecasts by Using Account Schedules</span></span>
<span data-ttu-id="52ccc-107">Denne gjennomgangen beskriver hvordan du kan bruke kontoskjemaer til å lage kontantstrømprognoser.</span><span class="sxs-lookup"><span data-stu-id="52ccc-107">This walkthrough describes how you can use account schedules to make cash flow forecasts.</span></span> <span data-ttu-id="52ccc-108">Kontoskjemaer utfører beregninger som ikke kan utføres direkte i diagrammet over kontantstrømkontoer.</span><span class="sxs-lookup"><span data-stu-id="52ccc-108">Account schedules perform calculations that cannot be done directly in the chart of cash flow accounts.</span></span> <span data-ttu-id="52ccc-109">I kontoskjemaer kan du definere delsummer for kontantstrømmottak og -utbetalinger.</span><span class="sxs-lookup"><span data-stu-id="52ccc-109">In the account schedules, you can set up subtotals for cash flow receipts and disbursements.</span></span> <span data-ttu-id="52ccc-110">Disse delsummene kan inkluderes i nye totalsummer som deretter kan brukes til å lage kontantstrømprognoser.</span><span class="sxs-lookup"><span data-stu-id="52ccc-110">These subtotals can be included in new totals that can then be used in making cash flow forecasts.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="52ccc-111">Denne gjennomgangen</span><span class="sxs-lookup"><span data-stu-id="52ccc-111">About This Walkthrough</span></span>  
<span data-ttu-id="52ccc-112">Denne gjennomgangen beskriver følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="52ccc-112">This walkthrough describes the following tasks:</span></span>  

- <span data-ttu-id="52ccc-113">Definere et nytt navn for kontantstrømkontoskjema.</span><span class="sxs-lookup"><span data-stu-id="52ccc-113">Setting up a new cash flow account schedule name.</span></span>  
- <span data-ttu-id="52ccc-114">Definere kontoskjemalinjer.</span><span class="sxs-lookup"><span data-stu-id="52ccc-114">Setting up account schedule lines.</span></span>  
- <span data-ttu-id="52ccc-115">Definere et nytt kolonneoppsett.</span><span class="sxs-lookup"><span data-stu-id="52ccc-115">Setting up a new column layout.</span></span>  
- <span data-ttu-id="52ccc-116">Tilordne et kolonneoppsett til et kontoskjema.</span><span class="sxs-lookup"><span data-stu-id="52ccc-116">Assigning a column layout to an account schedule.</span></span>  
- <span data-ttu-id="52ccc-117">Vise og skrive ut kontantstrømprognosen.</span><span class="sxs-lookup"><span data-stu-id="52ccc-117">Viewing and printing the cash flow forecast.</span></span>  

### <a name="prerequisites"></a><span data-ttu-id="52ccc-118">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="52ccc-118">Prerequisites</span></span>  
<span data-ttu-id="52ccc-119">For å fullføre denne gjennomgangen må du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="52ccc-119">To complete this walkthrough, you will need:</span></span>  

- [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="52ccc-120">installert.</span><span class="sxs-lookup"><span data-stu-id="52ccc-120">installed.</span></span>  
- <span data-ttu-id="52ccc-121">Forslagslinjene for kontantstrøm registreres.</span><span class="sxs-lookup"><span data-stu-id="52ccc-121">The cash flow worksheet lines are registered.</span></span>  

## <a name="roles"></a><span data-ttu-id="52ccc-122">Roller</span><span class="sxs-lookup"><span data-stu-id="52ccc-122">Roles</span></span>  
<span data-ttu-id="52ccc-123">Denne gjennomgangen viser oppgaver som utføres av følgende brukerrolle:</span><span class="sxs-lookup"><span data-stu-id="52ccc-123">This walkthrough demonstrates tasks that are performed by the following user role:</span></span>  

- <span data-ttu-id="52ccc-124">Kontrollør</span><span class="sxs-lookup"><span data-stu-id="52ccc-124">Controller</span></span>  

## <a name="story"></a><span data-ttu-id="52ccc-125">Hovedscenario</span><span class="sxs-lookup"><span data-stu-id="52ccc-125">Story</span></span>  
<span data-ttu-id="52ccc-126">Ken er kontrollør på CRONUS og utarbeider månedlige kontantstrømprognoser.</span><span class="sxs-lookup"><span data-stu-id="52ccc-126">Ken is a controller at CRONUS who makes monthly cash flow forecasts.</span></span> <span data-ttu-id="52ccc-127">Han tar med finans, salg, kjøp og aktiva i prognosen, og deretter viser han den til ØKDIR Sara.</span><span class="sxs-lookup"><span data-stu-id="52ccc-127">He includes finance, sales, purchase, and fixed assets in the forecast, and then he presents it to CFO Sara for business insight.</span></span>  

## <a name="setting-up-a-new-account-schedule-name"></a><span data-ttu-id="52ccc-128">Definere et nytt kontoskjemanavn</span><span class="sxs-lookup"><span data-stu-id="52ccc-128">Setting Up a New Account Schedule Name</span></span>  
<span data-ttu-id="52ccc-129">Et kontoskjema består av et navn på kontoskjemaet for kontantstrøm med en rekke linjer og et kolonneoppsett.</span><span class="sxs-lookup"><span data-stu-id="52ccc-129">An account schedule consists of a cash flow account schedule name with a series of lines and a column layout.</span></span>  

### <a name="to-set-up-a-new-account-schedule-name"></a><span data-ttu-id="52ccc-130">Slik definerer du et nytt kontoskjemanavn</span><span class="sxs-lookup"><span data-stu-id="52ccc-130">To set up a new account schedule name</span></span>  

1.  <span data-ttu-id="52ccc-131">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kontoskjemaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="52ccc-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="52ccc-132">Velg **Ny** på siden **Kontoskjemanavn** for å opprette et nytt navn for kontantstrømkontoskjema.</span><span class="sxs-lookup"><span data-stu-id="52ccc-132">On the **Account Schedule Names** page, choose the **New** to create a new cash flow account schedule name.</span></span>  
3.  <span data-ttu-id="52ccc-133">I **Navn**-feltet angir du **Prognose**.</span><span class="sxs-lookup"><span data-stu-id="52ccc-133">In the **Name** field, enter **Forecast**.</span></span>  
4.  <span data-ttu-id="52ccc-134">I **Beskrivelse**-feltet angir du **Kontantstrømprognose**.</span><span class="sxs-lookup"><span data-stu-id="52ccc-134">In the **Description** field, enter **Cash Flow Forecast**.</span></span>  
5.  <span data-ttu-id="52ccc-135">La feltene **Standard kolonneoppsett** og **Analysevisningsnavn** være tomme.</span><span class="sxs-lookup"><span data-stu-id="52ccc-135">Leave the **Default Column Layout** and **Analysis View Name** fields blank.</span></span>  

## <a name="setting-up-account-schedule-lines"></a><span data-ttu-id="52ccc-136">Definere kontoskjemalinjer</span><span class="sxs-lookup"><span data-stu-id="52ccc-136">Setting Up Account Schedule Lines</span></span>  
<span data-ttu-id="52ccc-137">Etter at et kontoskjemanavn er angitt, definerer Ken hver linje som vises i kontoskjemaet for kontantstrøm.</span><span class="sxs-lookup"><span data-stu-id="52ccc-137">After an account schedule name is set up, Ken defines each line that appears in the cash flow account schedule.</span></span> <span data-ttu-id="52ccc-138">Ken definerer linjer som kan vises i rapporter, i tillegg til linjer som bare er til beregningsformål.</span><span class="sxs-lookup"><span data-stu-id="52ccc-138">Ken defines lines that can be shown in reports in addition to lines that are only for calculation purposes.</span></span>  

### <a name="to-set-up-account-schedule-lines"></a><span data-ttu-id="52ccc-139">Definere kontoskjemalinjer</span><span class="sxs-lookup"><span data-stu-id="52ccc-139">To set up account schedule lines</span></span>  

1.  <span data-ttu-id="52ccc-140">På siden **Kontoskjemanavn** velger du det nye **Prognose**-kontoskjemanavnet du opprettet, og deretter velger du handlingen **Rediger kontoskjema**.</span><span class="sxs-lookup"><span data-stu-id="52ccc-140">On the **Account Schedule Names** page, select the new **Forecast** account schedule name that you have created, and then choose the **Edit Account Schedule** action.</span></span>  
2.  <span data-ttu-id="52ccc-141">På siden **Kontoskjema** angir du hver linje nøyaktig, som vist i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="52ccc-141">On the **Account Schedule** page, enter each line exactly as shown in the following table.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="52ccc-142">Du kan bruke funksjonen **Sett inn kontantstrømkonti** til raskt å merke kontantstrømkontoene i kontantstrømkontoplanen og kopiere dem til kontoskjemalinjer.</span><span class="sxs-lookup"><span data-stu-id="52ccc-142">Using the **Insert CF Accounts** function, you can quickly mark the cash flow accounts from the chart of cash flow accounts and copy them to account schedule lines.</span></span>  

    |<span data-ttu-id="52ccc-143">Radnr.</span><span class="sxs-lookup"><span data-stu-id="52ccc-143">Row No.</span></span>|<span data-ttu-id="52ccc-144">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="52ccc-144">Description</span></span>|<span data-ttu-id="52ccc-145">Sammentellingstype</span><span class="sxs-lookup"><span data-stu-id="52ccc-145">Totaling Type</span></span>|<span data-ttu-id="52ccc-146">Sammentelling</span><span class="sxs-lookup"><span data-stu-id="52ccc-146">Totaling</span></span>|<span data-ttu-id="52ccc-147">Radtype</span><span class="sxs-lookup"><span data-stu-id="52ccc-147">Row Type</span></span>|<span data-ttu-id="52ccc-148">Beløpstype</span><span class="sxs-lookup"><span data-stu-id="52ccc-148">Amount Type</span></span>|<span data-ttu-id="52ccc-149">Vis</span><span class="sxs-lookup"><span data-stu-id="52ccc-149">Show</span></span>|  
    |-------|-----------|-------------|--------|--------|-----------|----|
    |<span data-ttu-id="52ccc-150">C10</span><span class="sxs-lookup"><span data-stu-id="52ccc-150">C10</span></span>|<span data-ttu-id="52ccc-151">Beløp</span><span class="sxs-lookup"><span data-stu-id="52ccc-151">Amount</span></span>|<span data-ttu-id="52ccc-152">Bevegelse</span><span class="sxs-lookup"><span data-stu-id="52ccc-152">Net Change</span></span>|<span data-ttu-id="52ccc-153">Poster</span><span class="sxs-lookup"><span data-stu-id="52ccc-153">Entries</span></span>|<span data-ttu-id="52ccc-154">Nettobeløp</span><span class="sxs-lookup"><span data-stu-id="52ccc-154">Net Amount</span></span>|<span data-ttu-id="52ccc-155">Alltid</span><span class="sxs-lookup"><span data-stu-id="52ccc-155">Always</span></span>|  
    |<span data-ttu-id="52ccc-156">C20</span><span class="sxs-lookup"><span data-stu-id="52ccc-156">C20</span></span>|<span data-ttu-id="52ccc-157">Beløp til dato</span><span class="sxs-lookup"><span data-stu-id="52ccc-157">Amount until Date</span></span>|<span data-ttu-id="52ccc-158">Saldo til dato</span><span class="sxs-lookup"><span data-stu-id="52ccc-158">Balance at Date</span></span>|<span data-ttu-id="52ccc-159">Poster</span><span class="sxs-lookup"><span data-stu-id="52ccc-159">Entries</span></span>|<span data-ttu-id="52ccc-160">Nettobeløp</span><span class="sxs-lookup"><span data-stu-id="52ccc-160">Net Amount</span></span>|<span data-ttu-id="52ccc-161">Alltid</span><span class="sxs-lookup"><span data-stu-id="52ccc-161">Always</span></span>|  
    |<span data-ttu-id="52ccc-162">C30</span><span class="sxs-lookup"><span data-stu-id="52ccc-162">C30</span></span>|<span data-ttu-id="52ccc-163">Hele regnskapsåret</span><span class="sxs-lookup"><span data-stu-id="52ccc-163">Entire Fiscal Year</span></span>|<span data-ttu-id="52ccc-164">Hele regnskapsåret</span><span class="sxs-lookup"><span data-stu-id="52ccc-164">Entire Fiscal Year</span></span>|<span data-ttu-id="52ccc-165">Poster</span><span class="sxs-lookup"><span data-stu-id="52ccc-165">Entries</span></span>|<span data-ttu-id="52ccc-166">Nettobeløp</span><span class="sxs-lookup"><span data-stu-id="52ccc-166">Net Amount</span></span>|<span data-ttu-id="52ccc-167">Alltid</span><span class="sxs-lookup"><span data-stu-id="52ccc-167">Always</span></span>|  

4.  <span data-ttu-id="52ccc-168">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="52ccc-168">Choose the **OK** button.</span></span>  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="52ccc-169">Tilordne kolonneoppsettet til kontoskjemanavnet</span><span class="sxs-lookup"><span data-stu-id="52ccc-169">Assigning the Column Layout to the Account Schedule Name</span></span>  
<span data-ttu-id="52ccc-170">Ken er nå klar til å tilordne kolonneoppsettet til kontoskjemanavnet.</span><span class="sxs-lookup"><span data-stu-id="52ccc-170">Ken is now ready to assign the column layout to the account schedule name.</span></span>  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="52ccc-171">Slik tilordner du kolonneoppsettet til kontoskjemanavnet:</span><span class="sxs-lookup"><span data-stu-id="52ccc-171">To assign the column layout to the account schedule name</span></span>  

1.  <span data-ttu-id="52ccc-172">På siden **Kontoskjemanavn** velger du **Prognose** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="52ccc-172">On the **Account Schedule Names** page, select **Forecast** in the **Name** field.</span></span>  
2.  <span data-ttu-id="52ccc-173">Velg kolonneoppsettet **Kontantstrøm** i feltet **Standard kolonneoppsett** for å bruke det som standard kolonneoppsett.</span><span class="sxs-lookup"><span data-stu-id="52ccc-173">In the **Default Column Layout** field, choose the column layout **Cash Flow** to assign as the default column layout.</span></span>  

### <a name="to-view-and-print-the-cash-flow-forecast"></a><span data-ttu-id="52ccc-174">Slik viser og skriver du ut kontantstrømprognosen:</span><span class="sxs-lookup"><span data-stu-id="52ccc-174">To view and print the cash flow forecast</span></span>  
1.  <span data-ttu-id="52ccc-175">Velg **Oversikt**-handlingen på siden **Kontoskjemanavn** for å vise kontantstrømprognosen.</span><span class="sxs-lookup"><span data-stu-id="52ccc-175">On the **Account Schedule Names** page, choose the **Overview** action to view the cash flow forecast.</span></span>  
2.  <span data-ttu-id="52ccc-176">På siden **Kto.skjemaoversikt** kan du velge et beløp og deretter vise kontantstrømprognosepostene som utgjør beløpet.</span><span class="sxs-lookup"><span data-stu-id="52ccc-176">On the **Acc. Schedule Overview** page, you can select an amount and then view the cash flow forecast entries that make up the amount.</span></span> <span data-ttu-id="52ccc-177">I tillegg kan du vise formelen som brukes til å beregne beløpet.</span><span class="sxs-lookup"><span data-stu-id="52ccc-177">In addition, you can view the formula that is used to calculate the amount.</span></span> <span data-ttu-id="52ccc-178">Du kan også filtrere beløpene etter dato og dimensjon.</span><span class="sxs-lookup"><span data-stu-id="52ccc-178">You can also filter the amounts by date and dimension.</span></span>  
3.  <span data-ttu-id="52ccc-179">Velg **Skriv ut**-handlingen for å skrive ut kontantstrømprognosen.</span><span class="sxs-lookup"><span data-stu-id="52ccc-179">Choose the **Print** action to print the cash flow forecast.</span></span>  

## <a name="see-also"></a><span data-ttu-id="52ccc-180">Se også</span><span class="sxs-lookup"><span data-stu-id="52ccc-180">See Also</span></span>  
 <span data-ttu-id="52ccc-181">[Arbeide med kontoskjemaer](bi-how-work-account-schedule.md) </span><span class="sxs-lookup"><span data-stu-id="52ccc-181">[Work with Account Schedules](bi-how-work-account-schedule.md) </span></span>  
 [<span data-ttu-id="52ccc-182">Gjennomgang av forretningsprosesser</span><span class="sxs-lookup"><span data-stu-id="52ccc-182">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="52ccc-183">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="52ccc-183">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
