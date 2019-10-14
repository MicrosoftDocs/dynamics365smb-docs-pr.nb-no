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
ms.openlocfilehash: 70f1e51a0cd2c1b6c90ca3d76013fb3a5f30f80e
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2314847"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a><span data-ttu-id="1b2da-106">Gjennomgang: Lage kontantstrømprognoser ved å bruke kontoskjemaer</span><span class="sxs-lookup"><span data-stu-id="1b2da-106">Walkthrough: Making Cash Flow Forecasts by Using Account Schedules</span></span>
<span data-ttu-id="1b2da-107">Denne gjennomgangen beskriver hvordan du kan bruke kontoskjemaer til å lage kontantstrømprognoser.</span><span class="sxs-lookup"><span data-stu-id="1b2da-107">This walkthrough describes how you can use account schedules to make cash flow forecasts.</span></span> <span data-ttu-id="1b2da-108">Kontoskjemaer utfører beregninger som ikke kan utføres direkte i diagrammet over kontantstrømkontoer.</span><span class="sxs-lookup"><span data-stu-id="1b2da-108">Account schedules perform calculations that cannot be done directly in the chart of cash flow accounts.</span></span> <span data-ttu-id="1b2da-109">I kontoskjemaer kan du definere delsummer for kontantstrømmottak og -utbetalinger.</span><span class="sxs-lookup"><span data-stu-id="1b2da-109">In the account schedules, you can set up subtotals for cash flow receipts and disbursements.</span></span> <span data-ttu-id="1b2da-110">Disse delsummene kan inkluderes i nye totalsummer som deretter kan brukes til å lage kontantstrømprognoser.</span><span class="sxs-lookup"><span data-stu-id="1b2da-110">These subtotals can be included in new totals that can then be used in making cash flow forecasts.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="1b2da-111">Denne gjennomgangen</span><span class="sxs-lookup"><span data-stu-id="1b2da-111">About This Walkthrough</span></span>  
<span data-ttu-id="1b2da-112">Denne gjennomgangen beskriver følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="1b2da-112">This walkthrough describes the following tasks:</span></span>  

- <span data-ttu-id="1b2da-113">Definere et nytt navn for kontantstrømkontoskjema.</span><span class="sxs-lookup"><span data-stu-id="1b2da-113">Setting up a new cash flow account schedule name.</span></span>  
- <span data-ttu-id="1b2da-114">Definere kontoskjemalinjer.</span><span class="sxs-lookup"><span data-stu-id="1b2da-114">Setting up account schedule lines.</span></span>  
- <span data-ttu-id="1b2da-115">Definere et nytt kolonneoppsett.</span><span class="sxs-lookup"><span data-stu-id="1b2da-115">Setting up a new column layout.</span></span>  
- <span data-ttu-id="1b2da-116">Tilordne et kolonneoppsett til et kontoskjema.</span><span class="sxs-lookup"><span data-stu-id="1b2da-116">Assigning a column layout to an account schedule.</span></span>  
- <span data-ttu-id="1b2da-117">Vise og skrive ut kontantstrømprognosen.</span><span class="sxs-lookup"><span data-stu-id="1b2da-117">Viewing and printing the cash flow forecast.</span></span>  

### <a name="prerequisites"></a><span data-ttu-id="1b2da-118">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="1b2da-118">Prerequisites</span></span>  
<span data-ttu-id="1b2da-119">For å fullføre denne gjennomgangen må du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="1b2da-119">To complete this walkthrough, you will need:</span></span>  

- [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="1b2da-120">installert.</span><span class="sxs-lookup"><span data-stu-id="1b2da-120">installed.</span></span>  
- <span data-ttu-id="1b2da-121">Forslagslinjene for kontantstrøm registreres.</span><span class="sxs-lookup"><span data-stu-id="1b2da-121">The cash flow worksheet lines are registered.</span></span>  

## <a name="roles"></a><span data-ttu-id="1b2da-122">Roller</span><span class="sxs-lookup"><span data-stu-id="1b2da-122">Roles</span></span>  
<span data-ttu-id="1b2da-123">Denne gjennomgangen viser oppgaver som utføres av følgende brukerrolle:</span><span class="sxs-lookup"><span data-stu-id="1b2da-123">This walkthrough demonstrates tasks that are performed by the following user role:</span></span>  

- <span data-ttu-id="1b2da-124">Kontrollør</span><span class="sxs-lookup"><span data-stu-id="1b2da-124">Controller</span></span>  

## <a name="story"></a><span data-ttu-id="1b2da-125">Hovedscenario</span><span class="sxs-lookup"><span data-stu-id="1b2da-125">Story</span></span>  
<span data-ttu-id="1b2da-126">Ken er kontrollør på CRONUS og utarbeider månedlige kontantstrømprognoser.</span><span class="sxs-lookup"><span data-stu-id="1b2da-126">Ken is a controller at CRONUS who makes monthly cash flow forecasts.</span></span> <span data-ttu-id="1b2da-127">Han tar med finans, salg, kjøp og aktiva i prognosen, og deretter viser han den til ØKDIR Sara.</span><span class="sxs-lookup"><span data-stu-id="1b2da-127">He includes finance, sales, purchase, and fixed assets in the forecast, and then he presents it to CFO Sara for business insight.</span></span>  

## <a name="setting-up-a-new-account-schedule-name"></a><span data-ttu-id="1b2da-128">Definere et nytt kontoskjemanavn</span><span class="sxs-lookup"><span data-stu-id="1b2da-128">Setting Up a New Account Schedule Name</span></span>  
<span data-ttu-id="1b2da-129">Et kontoskjema består av et navn på kontoskjemaet for kontantstrøm med en rekke linjer og et kolonneoppsett.</span><span class="sxs-lookup"><span data-stu-id="1b2da-129">An account schedule consists of a cash flow account schedule name with a series of lines and a column layout.</span></span>  

### <a name="to-set-up-a-new-account-schedule-name"></a><span data-ttu-id="1b2da-130">Slik definerer du et nytt kontoskjemanavn</span><span class="sxs-lookup"><span data-stu-id="1b2da-130">To set up a new account schedule name</span></span>  

1.  <span data-ttu-id="1b2da-131">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kontoskjemaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="1b2da-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1b2da-132">Velg **Ny** på siden **Kontoskjemanavn** for å opprette et nytt navn for kontantstrømkontoskjema.</span><span class="sxs-lookup"><span data-stu-id="1b2da-132">On the **Account Schedule Names** page, choose the **New** to create a new cash flow account schedule name.</span></span>  
3.  <span data-ttu-id="1b2da-133">I **Navn**-feltet angir du **Prognose**.</span><span class="sxs-lookup"><span data-stu-id="1b2da-133">In the **Name** field, enter **Forecast**.</span></span>  
4.  <span data-ttu-id="1b2da-134">I **Beskrivelse**-feltet angir du **Kontantstrømprognose**.</span><span class="sxs-lookup"><span data-stu-id="1b2da-134">In the **Description** field, enter **Cash Flow Forecast**.</span></span>  
5.  <span data-ttu-id="1b2da-135">La feltene **Standard kolonneoppsett** og **Analysevisningsnavn** være tomme.</span><span class="sxs-lookup"><span data-stu-id="1b2da-135">Leave the **Default Column Layout** and **Analysis View Name** fields blank.</span></span>  

## <a name="setting-up-account-schedule-lines"></a><span data-ttu-id="1b2da-136">Definere kontoskjemalinjer</span><span class="sxs-lookup"><span data-stu-id="1b2da-136">Setting Up Account Schedule Lines</span></span>  
<span data-ttu-id="1b2da-137">Etter at et kontoskjemanavn er angitt, definerer Ken hver linje som vises i kontoskjemaet for kontantstrøm.</span><span class="sxs-lookup"><span data-stu-id="1b2da-137">After an account schedule name is set up, Ken defines each line that appears in the cash flow account schedule.</span></span> <span data-ttu-id="1b2da-138">Ken definerer linjer som kan vises i rapporter, i tillegg til linjer som bare er til beregningsformål.</span><span class="sxs-lookup"><span data-stu-id="1b2da-138">Ken defines lines that can be shown in reports in addition to lines that are only for calculation purposes.</span></span>  

### <a name="to-set-up-account-schedule-lines"></a><span data-ttu-id="1b2da-139">Definere kontoskjemalinjer</span><span class="sxs-lookup"><span data-stu-id="1b2da-139">To set up account schedule lines</span></span>  

1.  <span data-ttu-id="1b2da-140">Velg det nye kontoskjemanavnet for **Prognose** du har opprettet, på siden **Kontoskjemanavn**.</span><span class="sxs-lookup"><span data-stu-id="1b2da-140">On the **Account Schedule Names** page, select the new **Forecast** account schedule name that you have created.</span></span> <span data-ttu-id="1b2da-141">I fanebladet **Hjem**, under **Prosess**, velger du **Rediger kontoskjema**.</span><span class="sxs-lookup"><span data-stu-id="1b2da-141">On the **Home** tab, in the **Process** group, choose **Edit Account Schedule**.</span></span>  
2.  <span data-ttu-id="1b2da-142">På siden **Kontoskjema** angir du hver linje nøyaktig, som vist i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="1b2da-142">On the **Account Schedule** page, enter each line exactly as shown in the following table.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="1b2da-143">Du kan bruke funksjonen **Sett inn kontantstrømkonti** til raskt å merke kontantstrømkontoene i kontantstrømkontoplanen og kopiere dem til kontoskjemalinjer.</span><span class="sxs-lookup"><span data-stu-id="1b2da-143">Using the **Insert CF Accounts** function, you can quickly mark the cash flow accounts from the chart of cash flow accounts and copy them to account schedule lines.</span></span>  

    |<span data-ttu-id="1b2da-144">Radnr.</span><span class="sxs-lookup"><span data-stu-id="1b2da-144">Row No.</span></span>|<span data-ttu-id="1b2da-145">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="1b2da-145">Description</span></span>|<span data-ttu-id="1b2da-146">Sammentellingstype</span><span class="sxs-lookup"><span data-stu-id="1b2da-146">Totaling Type</span></span>|<span data-ttu-id="1b2da-147">Sammentelling</span><span class="sxs-lookup"><span data-stu-id="1b2da-147">Totaling</span></span>|<span data-ttu-id="1b2da-148">Radtype</span><span class="sxs-lookup"><span data-stu-id="1b2da-148">Row Type</span></span>|<span data-ttu-id="1b2da-149">Beløpstype</span><span class="sxs-lookup"><span data-stu-id="1b2da-149">Amount Type</span></span>|<span data-ttu-id="1b2da-150">Vis</span><span class="sxs-lookup"><span data-stu-id="1b2da-150">Show</span></span>|  
    |-------|-----------|-------------|--------|--------|-----------|----|
    |<span data-ttu-id="1b2da-151">C10</span><span class="sxs-lookup"><span data-stu-id="1b2da-151">C10</span></span>|<span data-ttu-id="1b2da-152">Beløp</span><span class="sxs-lookup"><span data-stu-id="1b2da-152">Amount</span></span>|<span data-ttu-id="1b2da-153">Bevegelse</span><span class="sxs-lookup"><span data-stu-id="1b2da-153">Net Change</span></span>|<span data-ttu-id="1b2da-154">Poster</span><span class="sxs-lookup"><span data-stu-id="1b2da-154">Entries</span></span>|<span data-ttu-id="1b2da-155">Nettobeløp</span><span class="sxs-lookup"><span data-stu-id="1b2da-155">Net Amount</span></span>|<span data-ttu-id="1b2da-156">Alltid</span><span class="sxs-lookup"><span data-stu-id="1b2da-156">Always</span></span>|  
    |<span data-ttu-id="1b2da-157">C20</span><span class="sxs-lookup"><span data-stu-id="1b2da-157">C20</span></span>|<span data-ttu-id="1b2da-158">Beløp til dato</span><span class="sxs-lookup"><span data-stu-id="1b2da-158">Amount until Date</span></span>|<span data-ttu-id="1b2da-159">Saldo til dato</span><span class="sxs-lookup"><span data-stu-id="1b2da-159">Balance at Date</span></span>|<span data-ttu-id="1b2da-160">Poster</span><span class="sxs-lookup"><span data-stu-id="1b2da-160">Entries</span></span>|<span data-ttu-id="1b2da-161">Nettobeløp</span><span class="sxs-lookup"><span data-stu-id="1b2da-161">Net Amount</span></span>|<span data-ttu-id="1b2da-162">Alltid</span><span class="sxs-lookup"><span data-stu-id="1b2da-162">Always</span></span>|  
    |<span data-ttu-id="1b2da-163">C30</span><span class="sxs-lookup"><span data-stu-id="1b2da-163">C30</span></span>|<span data-ttu-id="1b2da-164">Hele regnskapsåret</span><span class="sxs-lookup"><span data-stu-id="1b2da-164">Entire Fiscal Year</span></span>|<span data-ttu-id="1b2da-165">Hele regnskapsåret</span><span class="sxs-lookup"><span data-stu-id="1b2da-165">Entire Fiscal Year</span></span>|<span data-ttu-id="1b2da-166">Poster</span><span class="sxs-lookup"><span data-stu-id="1b2da-166">Entries</span></span>|<span data-ttu-id="1b2da-167">Nettobeløp</span><span class="sxs-lookup"><span data-stu-id="1b2da-167">Net Amount</span></span>|<span data-ttu-id="1b2da-168">Alltid</span><span class="sxs-lookup"><span data-stu-id="1b2da-168">Always</span></span>|  

4.  <span data-ttu-id="1b2da-169">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="1b2da-169">Choose the **OK** button.</span></span>  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="1b2da-170">Tilordne kolonneoppsettet til kontoskjemanavnet</span><span class="sxs-lookup"><span data-stu-id="1b2da-170">Assigning the Column Layout to the Account Schedule Name</span></span>  
<span data-ttu-id="1b2da-171">Ken er nå klar til å tilordne kolonneoppsettet til kontoskjemanavnet.</span><span class="sxs-lookup"><span data-stu-id="1b2da-171">Ken is now ready to assign the column layout to the account schedule name.</span></span>  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="1b2da-172">Slik tilordner du kolonneoppsettet til kontoskjemanavnet:</span><span class="sxs-lookup"><span data-stu-id="1b2da-172">To assign the column layout to the account schedule name</span></span>  

1.  <span data-ttu-id="1b2da-173">På siden **Kontoskjemanavn** velger du **Prognose** i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1b2da-173">On the **Account Schedule Names** page, select **Forecast** in the **Name** field.</span></span>  
2.  <span data-ttu-id="1b2da-174">Velg kolonneoppsettet **Kontantstrøm** i feltet **Standard kolonneoppsett** for å bruke det som standard kolonneoppsett.</span><span class="sxs-lookup"><span data-stu-id="1b2da-174">In the **Default Column Layout** field, choose the column layout **Cash Flow** to assign as the default column layout.</span></span>  

### <a name="to-view-and-print-the-cash-flow-forecast"></a><span data-ttu-id="1b2da-175">Slik viser og skriver du ut kontantstrømprognosen:</span><span class="sxs-lookup"><span data-stu-id="1b2da-175">To view and print the cash flow forecast</span></span>  
1.  <span data-ttu-id="1b2da-176">Velg **Oversikt**-handlingen på siden **Kontoskjemanavn** for å vise kontantstrømprognosen.</span><span class="sxs-lookup"><span data-stu-id="1b2da-176">On the **Account Schedule Names** page, choose the **Overview** action to view the cash flow forecast.</span></span>  
2.  <span data-ttu-id="1b2da-177">På siden **Kto.skjemaoversikt** kan du velge et beløp og deretter vise kontantstrømprognosepostene som utgjør beløpet.</span><span class="sxs-lookup"><span data-stu-id="1b2da-177">On the **Acc. Schedule Overview** page, you can select an amount and then view the cash flow forecast entries that make up the amount.</span></span> <span data-ttu-id="1b2da-178">I tillegg kan du vise formelen som brukes til å beregne beløpet.</span><span class="sxs-lookup"><span data-stu-id="1b2da-178">In addition, you can view the formula that is used to calculate the amount.</span></span> <span data-ttu-id="1b2da-179">Du kan også filtrere beløpene etter dato og dimensjon.</span><span class="sxs-lookup"><span data-stu-id="1b2da-179">You can also filter the amounts by date and dimension.</span></span>  
3.  <span data-ttu-id="1b2da-180">Velg **Skriv ut**-handlingen for å skrive ut kontantstrømprognosen.</span><span class="sxs-lookup"><span data-stu-id="1b2da-180">Choose the **Print** action to print the cash flow forecast.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1b2da-181">Se også</span><span class="sxs-lookup"><span data-stu-id="1b2da-181">See Also</span></span>  
 <span data-ttu-id="1b2da-182">[Arbeide med kontoskjemaer](bi-how-work-account-schedule.md) </span><span class="sxs-lookup"><span data-stu-id="1b2da-182">[Work with Account Schedules](bi-how-work-account-schedule.md) </span></span>  
 [<span data-ttu-id="1b2da-183">Gjennomgang av forretningsprosesser</span><span class="sxs-lookup"><span data-stu-id="1b2da-183">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="1b2da-184">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1b2da-184">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
