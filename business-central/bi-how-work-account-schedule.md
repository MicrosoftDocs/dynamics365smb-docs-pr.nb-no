---
title: "Lage økonomirapporter med kontoskjemaer"
description: "Beskriver hvordan du bruker kontoskjemaer til å opprette ulike visninger og rapporter for å analysere økonomiske resultatdata."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 04/16/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: f9f5b3a25a24d4d10c80d048153e68030733bf9e
ms.contentlocale: nb-no
ms.lasthandoff: 04/18/2018

---
# <a name="work-with-account-schedules"></a><span data-ttu-id="57f82-103">Arbeide med kontoskjemaer</span><span class="sxs-lookup"><span data-stu-id="57f82-103">Work with Account Schedules</span></span>
<span data-ttu-id="57f82-104">Du kan bruke kontoskjemaer til å få innsikt i de økonomiske dataene som er lagret i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="57f82-104">Use account schedules to get insight into the financial data stored in your chart of accounts.</span></span> <span data-ttu-id="57f82-105">Kontoskjemaer analyserer tall på finanskonti og sammenligner faktiske finansposter med finansbudsjettposter.</span><span class="sxs-lookup"><span data-stu-id="57f82-105">Account schedules analyze figures in G/L accounts, and compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="57f82-106">Resultatene vises i diagrammene i rollesenteret, for eksempel Kontantstrøm-diagrammet.</span><span class="sxs-lookup"><span data-stu-id="57f82-106">The results display in charts on your Role Center, such as the Cash Flow chart.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="57f82-107"> inneholder et par eksempler på kontoskjemaer som du kan bruke med én gang, eller du kan definere dine egne rader og kolonner for å angi tallene som skal sammenlignes.</span><span class="sxs-lookup"><span data-stu-id="57f82-107"> provides a few sample account schedules that you can use right away, or you can set up your own rows and columns to specify the figures to compare.</span></span> <span data-ttu-id="57f82-108">Du kan for eksempel opprette kontoskjemaer for å beregne fortjenestemarginer for dimensjoner som avdelinger eller kundegrupper.</span><span class="sxs-lookup"><span data-stu-id="57f82-108">For example, you can create account schedules to calculate profit margins on dimensions like departments or customer groups.</span></span> <span data-ttu-id="57f82-109">Du kan opprette så mange egendefinerte regnskapsrapporter du vil.</span><span class="sxs-lookup"><span data-stu-id="57f82-109">You can create as many customized financial statements as you want.</span></span>  

<span data-ttu-id="57f82-110">Oppretting av kontoskjemaer krever en forståelse av de økonomiske dataene i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="57f82-110">Setting up account schedules requires an understanding of the financial data in the chart of accounts.</span></span> <span data-ttu-id="57f82-111">Du kan for eksempel vise finansposter som en prosentandel av budsjettpostene.</span><span class="sxs-lookup"><span data-stu-id="57f82-111">For example, you can view general ledger entries as percentages of budget entries.</span></span> <span data-ttu-id="57f82-112">Dette krever at budsjetter opprettes.</span><span class="sxs-lookup"><span data-stu-id="57f82-112">This requires that budgets are created.</span></span> <span data-ttu-id="57f82-113">Hvis du vil ha mer informasjon, kan du se [Opprette finansbudsjetter](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="57f82-113">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="account-categories-and-account-schedules"></a><span data-ttu-id="57f82-114">Kontokategorier og kontoskjemaer</span><span class="sxs-lookup"><span data-stu-id="57f82-114">Account Categories and Account Schedules</span></span>
<span data-ttu-id="57f82-115">Du kan bruke kontokategoriene til å endre oppsettet for regnskapsoppgjørene.</span><span class="sxs-lookup"><span data-stu-id="57f82-115">You can use account categories to change the layout of your financial statements.</span></span> <span data-ttu-id="57f82-116">Når du har definert kontokategoriene i vinduet **Finanskontokategorier** og du velger handlingen **Generer kontoskjemaer**, oppdateres de underliggende kontoskjemaene for kjernefinansrapporter.</span><span class="sxs-lookup"><span data-stu-id="57f82-116">After you set up your account categories in the **G/L Account Categories** window, and you choose the **Generate Account Schedules** action, the underlying account schedules for the core financial reports are updated.</span></span> <span data-ttu-id="57f82-117">Neste gang du kjører en av disse rapportene, for eksempel saldoutdrag, legges ny totaler og underoppføringer til, basert på endringene.</span><span class="sxs-lookup"><span data-stu-id="57f82-117">The next time you run one of these reports, such as the balance statement, new totals and subentries are added, based on your changes.</span></span> <span data-ttu-id="57f82-118">Hvis du vil ha mer informasjon, kan du se [Finans og kontoplanen](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="57f82-118">For more information, see [The General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span>  

## <a name="to-create-new-account-schedules"></a><span data-ttu-id="57f82-119">Slik oppretter du nye kontoskjemaer</span><span class="sxs-lookup"><span data-stu-id="57f82-119">To create new account schedules</span></span>  
 <span data-ttu-id="57f82-120">Du bruker kontoskjemaer til å analysere tall på finanskonti eller til å sammenligne faktiske finansposter med finansbudsjettposter.</span><span class="sxs-lookup"><span data-stu-id="57f82-120">You use account schedules to analyze figures in general ledger accounts or to compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="57f82-121">Du kan for eksempel vise finansposter som en prosentandel av budsjettpostene.</span><span class="sxs-lookup"><span data-stu-id="57f82-121">For example, you can view the general ledger entries as percentages of the budget entries.</span></span>

1. <span data-ttu-id="57f82-122">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kontoskjemaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="57f82-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2. <span data-ttu-id="57f82-123">Velg handlingen **Ny** i vinduet **Kontoskjemanavn** for å opprette et nytt kontoskjemanavn.</span><span class="sxs-lookup"><span data-stu-id="57f82-123">In the **Account Schedule Names** window, choose the **New** action to create a new account schedule name.</span></span>
3. <span data-ttu-id="57f82-124">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="57f82-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="57f82-125">Velg handlingen **Rediger kontoskjema**.</span><span class="sxs-lookup"><span data-stu-id="57f82-125">Choose the **Edit Account Schedule** action.</span></span>
5. <span data-ttu-id="57f82-126">Fyll ut feltene etter behov i vinduet **Kontoskjema**.</span><span class="sxs-lookup"><span data-stu-id="57f82-126">In the **Account Schedule** window, fill in the fields as necessary.</span></span>  

    <span data-ttu-id="57f82-127">Når du har opprettet et nytt kontoskjema og definert radene, må du definere kolonner.</span><span class="sxs-lookup"><span data-stu-id="57f82-127">When you have created a new account schedule and set up the rows, you must set up columns.</span></span> <span data-ttu-id="57f82-128">Dette kan du gjøre manuelt eller ved hjelp av et forhåndsdefinert kolonneoppsett.</span><span class="sxs-lookup"><span data-stu-id="57f82-128">You can either set them up manually or assign a predefined column layout to your account schedule.</span></span>
6. <span data-ttu-id="57f82-129">Velg handlingen **Rediger oppsett for kolonneutforming**.</span><span class="sxs-lookup"><span data-stu-id="57f82-129">Choose the **Edit Column Layout Setup** action.</span></span>
7. <span data-ttu-id="57f82-130">I vinduet **Kolonneoppsett** fyller du ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="57f82-130">In the **Column Layout** window, fill in the fields as necessary.</span></span>

> [!NOTE]  
>   <span data-ttu-id="57f82-131">Hvis du ikke tilordnet et standard kolonneoppsett til kontoskjemaet, må du definere kolonnene manuelt.</span><span class="sxs-lookup"><span data-stu-id="57f82-131">If you did not assign a default column layout to the account schedule, you must set the columns up manually.</span></span>   

### <a name="to-create-a-column-that-calculates-percentages"></a><span data-ttu-id="57f82-132">Slik oppretter du en kolonne som beregner prosentdeler</span><span class="sxs-lookup"><span data-stu-id="57f82-132">To create a column that calculates percentages</span></span>  
<span data-ttu-id="57f82-133">Noen ganger vil du kanskje ta med en kolonne i et kontoskjema for å beregne prosentdeler av en sum.</span><span class="sxs-lookup"><span data-stu-id="57f82-133">Sometimes you may want to include a column in an account schedule to calculate percentages of a total.</span></span> <span data-ttu-id="57f82-134">Hvis du for eksempel har et antall rader som bryter ned salg etter dimensjon, vil du kanskje ta med en kolonne som angir hvor stor prosentdel av totalt salg hver rad representerer.</span><span class="sxs-lookup"><span data-stu-id="57f82-134">For example, if you have a number of rows that break down sales by dimension, you may want a column to indicate the percentage of total sales that each row represents.</span></span>

1. <span data-ttu-id="57f82-135">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kontoskjemaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="57f82-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="57f82-136">Velg et kontoskjema i vinduet **Kontoskjemanavn**.</span><span class="sxs-lookup"><span data-stu-id="57f82-136">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="57f82-137">Velg handlingen **Rediger kontoskjema** for å definere en kontoskjemarad som skal brukes til å beregne summen prosentene skal baseres på.</span><span class="sxs-lookup"><span data-stu-id="57f82-137">Choose the **Edit Account Schedule** action to set up an account schedule row to calculate the total on which the percentages will be based.</span></span>  
4. <span data-ttu-id="57f82-138">Sett inn en linje like over den første raden som du vil vise en prosentdel for.</span><span class="sxs-lookup"><span data-stu-id="57f82-138">Insert a line immediately above the first row for which you want to display a percentage.</span></span>  
5. <span data-ttu-id="57f82-139">Fyll ut feltene på linjen som følger: I feltet **Sammentellingstype** angir du **Angi grunnlag for prosent**.</span><span class="sxs-lookup"><span data-stu-id="57f82-139">Fill in the fields on the line as follows: In the **Totaling Type** field, enter **Set Base for Percent**.</span></span> <span data-ttu-id="57f82-140">Skriv inn en formel for summen som prosentdelen skal være basert på, i **Sammentelling**-feltet.</span><span class="sxs-lookup"><span data-stu-id="57f82-140">In the **Totaling** field, enter a formula for the total that the percentage will be based on.</span></span> <span data-ttu-id="57f82-141">Hvis rad 11 for eksempel inneholder totalt salg, angir du **11**.</span><span class="sxs-lookup"><span data-stu-id="57f82-141">For example, if row 11 contains the total sales, enter **11**.</span></span>  
6. <span data-ttu-id="57f82-142">Velg handlingen **Rediger oppsett for kolonneutforming** for å definere en kolonne.</span><span class="sxs-lookup"><span data-stu-id="57f82-142">Choose the **Edit Column Layout Setup** action to set up a column.</span></span>  
7. <span data-ttu-id="57f82-143">Fyll ut feltene på linjen som følger: I feltet **Kolonnetype** velger du **Formel**.</span><span class="sxs-lookup"><span data-stu-id="57f82-143">Fill in the fields on the line as follows: In the **Column Type** field, select **Formula**.</span></span> <span data-ttu-id="57f82-144">Skriv inn en formel for beløpet du vil beregne en prosent for, fulgt av %, i **Formel**-feltet.</span><span class="sxs-lookup"><span data-stu-id="57f82-144">In the **Formula** field, enter a formula for the amount that you want to calculate a percentage for, followed by %.</span></span> <span data-ttu-id="57f82-145">Hvis kolonnenummeret N for eksempel inneholder bevegelsen, angir du **N %**.</span><span class="sxs-lookup"><span data-stu-id="57f82-145">For example, if column number N contains the net change, enter **N%**.</span></span>  
8. <span data-ttu-id="57f82-146">Gjenta trinn 4 til og med 7 for hver gruppe med rader du vil bryte ned i prosentdeler.</span><span class="sxs-lookup"><span data-stu-id="57f82-146">Repeat steps 4 through 7 for each group of rows that you want to break down by percentage.</span></span>

## <a name="to-set-up-account-schedules-with-overviews"></a><span data-ttu-id="57f82-147">Slik setter du opp kontoskjemaer med oversikter</span><span class="sxs-lookup"><span data-stu-id="57f82-147">To set up account schedules with overviews</span></span>  
<span data-ttu-id="57f82-148">Du kan bruke et kontoskjema til å opprette en oppgave som sammenligner finanstall og finansbudsjettall.</span><span class="sxs-lookup"><span data-stu-id="57f82-148">You can use an account schedule to create a statement comparing general ledger figures and general leger budget figures.</span></span>

1. <span data-ttu-id="57f82-149">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kontoskjemaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="57f82-149">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="57f82-150">Velg et kontoskjema i vinduet **Kontoskjemanavn**.</span><span class="sxs-lookup"><span data-stu-id="57f82-150">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="57f82-151">Velg handlingen **Rediger kontoskjema**.</span><span class="sxs-lookup"><span data-stu-id="57f82-151">Choose the **Edit Account Schedule** action</span></span>  
4. <span data-ttu-id="57f82-152">Velg standawrd kontoskjemanavn i **Navn**-feltet i **Kontoskjema**-vinduet.</span><span class="sxs-lookup"><span data-stu-id="57f82-152">In the **Account Schedule** window, in the **Name** field, select the default account schedule name.</span></span>
5. <span data-ttu-id="57f82-153">Velg handlingen **Sett inn konti**.</span><span class="sxs-lookup"><span data-stu-id="57f82-153">Choose the **Insert Accounts** action.</span></span>  
6. <span data-ttu-id="57f82-154">Velg kontiene du vil ta med i oppgaven , og klikk deretter **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="57f82-154">Select the accounts that you want to include in your statement, and then choose the **OK** button.</span></span>

    <span data-ttu-id="57f82-155">Kontiene settes nå inn i kontoskjemaet.</span><span class="sxs-lookup"><span data-stu-id="57f82-155">The accounts are now inserted into your account schedule.</span></span> <span data-ttu-id="57f82-156">Hvis du vil, kan du også endre kolonneoppsettet.</span><span class="sxs-lookup"><span data-stu-id="57f82-156">If you want you can also change the column layout.</span></span>  
7. <span data-ttu-id="57f82-157">Velg handlingen **Oversikt**.</span><span class="sxs-lookup"><span data-stu-id="57f82-157">Choose the **Overview** action.</span></span>  
8. <span data-ttu-id="57f82-158">På hurtigfanen **Dimensjonsfiltre** setter du budsjettfilteret til ønsket filternavn.</span><span class="sxs-lookup"><span data-stu-id="57f82-158">On the **Dimension Filters** FastTab, set the budget filter to the desired filter name.</span></span>  
9. <span data-ttu-id="57f82-159">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="57f82-159">Choose the **OK** button.</span></span>  

<span data-ttu-id="57f82-160">Du kan nå kopiere og lime inn budsjettoppgaven i et regneark.</span><span class="sxs-lookup"><span data-stu-id="57f82-160">Now you can copy and paste your budget statement into a spreadsheet.</span></span>  

## <a name="comparing-accounting-periods-using-period-formulas"></a><span data-ttu-id="57f82-161">Sammenligne regnskapsperioder ved hjelp av periodeformler</span><span class="sxs-lookup"><span data-stu-id="57f82-161">Comparing Accounting Periods using Period Formulas</span></span>
<span data-ttu-id="57f82-162">Kontoskjemaet kan sammenligne resultatene av ulike regnskapsperioder, for eksempel inneværende måned og samme måned i fjor.</span><span class="sxs-lookup"><span data-stu-id="57f82-162">Your account schedule can compare the results of different accounting periods, such as this month versus same month last year.</span></span> <span data-ttu-id="57f82-163">For å gjøre dette må du legge til en kolonne med **Formel - periodesammenligning**-feltet, og deretter angi dette feltet som en periodeformel.</span><span class="sxs-lookup"><span data-stu-id="57f82-163">To do that, you add a column with the **Comparison Period Formula** field, and then set that field to a period formula.</span></span>  

<span data-ttu-id="57f82-164">En regnskapsperiode trenger ikke å sammenfalle med kalenderen, men regnskapsåret må ha samme antall regnskapsperioder, selv om hver periode kan variere i lengde.</span><span class="sxs-lookup"><span data-stu-id="57f82-164">An accounting period does not have to match the calendar, but each fiscal year must have the same number of accounting periods, even though each period can be different in length.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="57f82-165"> bruker periodeformelen til å beregne beløpet fra sammenligningsperioden, i forhold til perioden som er angitt i datofilteret i rapportforespørselen.</span><span class="sxs-lookup"><span data-stu-id="57f82-165"> uses the period formula to calculate the amount from the comparison period in relation to the period represented by the date filter on the report request.</span></span> <span data-ttu-id="57f82-166">Sammenligningsperioden er basert på perioden for startdatoen i datofilteret.</span><span class="sxs-lookup"><span data-stu-id="57f82-166">The comparison period is based on the period of the start date of the date filter.</span></span> <span data-ttu-id="57f82-167">Periodene forkortes slik:</span><span class="sxs-lookup"><span data-stu-id="57f82-167">The abbreviations for period specifications are:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="57f82-168">Forkortelse</span><span class="sxs-lookup"><span data-stu-id="57f82-168">Abbreviation</span></span></th>
<th><span data-ttu-id="57f82-169">Description</span><span class="sxs-lookup"><span data-stu-id="57f82-169">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="57f82-170">P</span><span class="sxs-lookup"><span data-stu-id="57f82-170">P</span></span></p></td>
<td><p><span data-ttu-id="57f82-171">Periode</span><span class="sxs-lookup"><span data-stu-id="57f82-171">Period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57f82-172">SP</span><span class="sxs-lookup"><span data-stu-id="57f82-172">LP</span></span></p></td>
<td><p><span data-ttu-id="57f82-173">Siste periode av et regnskapsår, et halvår eller kvartal.</span><span class="sxs-lookup"><span data-stu-id="57f82-173">Last period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57f82-174">IP</span><span class="sxs-lookup"><span data-stu-id="57f82-174">CP</span></span></p></td>
<td><p><span data-ttu-id="57f82-175">Inneværende periode av et regnskapsår, et halvår eller kvartal.</span><span class="sxs-lookup"><span data-stu-id="57f82-175">Current period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57f82-176">RÅ</span><span class="sxs-lookup"><span data-stu-id="57f82-176">FY</span></span></p></td>
<td><p><span data-ttu-id="57f82-177">Regnskapsår.</span><span class="sxs-lookup"><span data-stu-id="57f82-177">Fiscal year.</span></span> <span data-ttu-id="57f82-178">Eksempelvis viser RÅ [1..3] til første kvartal av inneværende regnskapsår</span><span class="sxs-lookup"><span data-stu-id="57f82-178">For example, FY[1..3] denotes first quarter of the current fiscal year</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="57f82-179">Eksempler på formler:</span><span class="sxs-lookup"><span data-stu-id="57f82-179">Examples of formulas:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="57f82-180">Formel</span><span class="sxs-lookup"><span data-stu-id="57f82-180">Formula</span></span></th>
<th><span data-ttu-id="57f82-181">Description</span><span class="sxs-lookup"><span data-stu-id="57f82-181">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="57f82-182">&lt;Tom&gt;</span><span class="sxs-lookup"><span data-stu-id="57f82-182">&lt;Blank&gt;</span></span></p></td>
<td><p><span data-ttu-id="57f82-183">Inneværende periode</span><span class="sxs-lookup"><span data-stu-id="57f82-183">Current period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57f82-184">-1P</span><span class="sxs-lookup"><span data-stu-id="57f82-184">-1P</span></span></p></td>
<td><p><span data-ttu-id="57f82-185">Forrige periode</span><span class="sxs-lookup"><span data-stu-id="57f82-185">Previous period</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57f82-186">-1RÅ[1..SP]</span><span class="sxs-lookup"><span data-stu-id="57f82-186">-1FY[1..LP]</span></span></p></td>
<td><p><span data-ttu-id="57f82-187">Hele forrige regnskapsår</span><span class="sxs-lookup"><span data-stu-id="57f82-187">Entire previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57f82-188">-1RÅ</span><span class="sxs-lookup"><span data-stu-id="57f82-188">-1FY</span></span></p></td>
<td><p><span data-ttu-id="57f82-189">Inneværende periode i forrige regnskapsår</span><span class="sxs-lookup"><span data-stu-id="57f82-189">Current period in previous fiscal year</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57f82-190">-1RÅ[1..3]</span><span class="sxs-lookup"><span data-stu-id="57f82-190">-1FY[1..3]</span></span></p></td>
<td><p><span data-ttu-id="57f82-191">Første kvartal av forrige regnskapsår</span><span class="sxs-lookup"><span data-stu-id="57f82-191">First quarter of previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57f82-192">-1RÅ[1..IP]</span><span class="sxs-lookup"><span data-stu-id="57f82-192">-1FY[1..CP]</span></span></p></td>
<td><p><span data-ttu-id="57f82-193">Fra begynnelsen av forrige regnskapsår til og med inneværende periode i forrige regnskapsår</span><span class="sxs-lookup"><span data-stu-id="57f82-193">From the beginning of previous fiscal year to current period in previous fiscal year, inclusive</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57f82-194">-1RÅ[IP..SP]</span><span class="sxs-lookup"><span data-stu-id="57f82-194">-1FY[CP..LP]</span></span></p></td>
<td><p><span data-ttu-id="57f82-195">Fra inneværende periode i forrige regnskapsår til og med siste periode i forrige regnskapsår</span><span class="sxs-lookup"><span data-stu-id="57f82-195">From current period in previous fiscal year to last period of previous fiscal year, inclusive</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="57f82-196">Hvis du vil beregne etter regelmessige perioder, må du angi en formel i feltet **Datoformel - sammenligning** i stedet.</span><span class="sxs-lookup"><span data-stu-id="57f82-196">If you want to calculate by regular time periods, you must enter a formula in the **Comparison Date Formula** field instead.</span></span>

> [!NOTE]
> <span data-ttu-id="57f82-197">Det er ikke alltid gjennomsiktig hvilke perioder du sammenligner, siden du kan angi et datofilter i en rapport som inneholder forskjellige datoer enn regnskapsperiodene som gjenspeiles i dataene i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="57f82-197">It is not always transparent which periods you are comparing because you can set a date filter on a report that spans different dates than the accounting periods that are reflected in the data in the chart of accounts.</span></span> <span data-ttu-id="57f82-198">Du oppretter for eksempel et kontoskjema der du vil sammenligne denne perioden med samme periode i fjor, så du setter **Sammenligningsperiode - filter**-feltet til *-1RÅ*.</span><span class="sxs-lookup"><span data-stu-id="57f82-198">For example, you create an account schedule where you want to compare this period with the same period last year, so you set the **Comparison Date Period Filter** field to *-1FY*.</span></span> <span data-ttu-id="57f82-199">Deretter kjører du rapporten 28. februar og setter datofilteret til januar og februar.</span><span class="sxs-lookup"><span data-stu-id="57f82-199">Then, you run the report on February 28th and set the date filter to January and February.</span></span> <span data-ttu-id="57f82-200">Dermed sammenligner kontoskjemaet januar og februar i år med januar i fjor, som er den eneste fullførte regnskapsperioden av de to for forrige år.</span><span class="sxs-lookup"><span data-stu-id="57f82-200">As a result, the account schedule compares January and February this year to January last year, which is the only completed accounting period of the two for last year.</span></span>  


## <a name="see-also"></a><span data-ttu-id="57f82-201">Se også</span><span class="sxs-lookup"><span data-stu-id="57f82-201">See Also</span></span>
[<span data-ttu-id="57f82-202">Forretningsintelligens</span><span class="sxs-lookup"><span data-stu-id="57f82-202">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="57f82-203">Finans</span><span class="sxs-lookup"><span data-stu-id="57f82-203">Finance</span></span>](finance.md)  
[<span data-ttu-id="57f82-204">Konfigurere finans</span><span class="sxs-lookup"><span data-stu-id="57f82-204">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="57f82-205">Finans og kontoplanen</span><span class="sxs-lookup"><span data-stu-id="57f82-205">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="57f82-206">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="57f82-206">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

