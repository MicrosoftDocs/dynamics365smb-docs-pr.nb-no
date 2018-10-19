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
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8e63e507411f41c67caa94834f4d99861bd1ae77
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a><span data-ttu-id="91458-103">Klargjøre finansrapportering med kontoskjemaer og kontokategorier</span><span class="sxs-lookup"><span data-stu-id="91458-103">Prepare Financial Reporting with Account Schedules and Account Categories</span></span>
<span data-ttu-id="91458-104">Du kan bruke kontoskjemaer til å få innsikt i de økonomiske dataene som er lagret i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="91458-104">Use account schedules to get insight into the financial data stored in your chart of accounts.</span></span> <span data-ttu-id="91458-105">Kontoskjemaer analyserer tall på finanskonti og sammenligner faktiske finansposter med finansbudsjettposter.</span><span class="sxs-lookup"><span data-stu-id="91458-105">Account schedules analyze figures in G/L accounts, and compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="91458-106">Resultatet vises i diagrammer i rollesenteret, for eksempel ut Kontantstrøm-diagrammet, og i rapporter, for eksempel rapporten Resultatregnskap og Balanse.</span><span class="sxs-lookup"><span data-stu-id="91458-106">The results display in charts on your Role Center, such as the Cash Flow chart, and in reports, such as the Income Statement and the Balance Sheet reports.</span></span>

<span data-ttu-id="91458-107">Du får tilgang til disse to rapportene for eksempel med handlingen **Årsregnskap** i rollesentrene for forretningsleder og regnskapsfører.</span><span class="sxs-lookup"><span data-stu-id="91458-107">You access these two reports, for example, with the **Financials Statements** action on the Business Manager and Accountant Role Centers.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="91458-108">inneholder et par eksempler på kontoskjemaer som du kan bruke med én gang, eller du kan definere dine egne rader og kolonner for å angi tallene som skal sammenlignes.</span><span class="sxs-lookup"><span data-stu-id="91458-108">provides a few sample account schedules that you can use right away, or you can set up your own rows and columns to specify the figures to compare.</span></span> <span data-ttu-id="91458-109">Du kan for eksempel opprette kontoskjemaer for å beregne fortjenestemarginer for dimensjoner som avdelinger eller kundegrupper.</span><span class="sxs-lookup"><span data-stu-id="91458-109">For example, you can create account schedules to calculate profit margins on dimensions like departments or customer groups.</span></span> <span data-ttu-id="91458-110">Du kan opprette så mange egendefinerte regnskapsrapporter du vil.</span><span class="sxs-lookup"><span data-stu-id="91458-110">You can create as many customized financial statements as you want.</span></span>  

<span data-ttu-id="91458-111">Oppretting av kontoskjemaer krever en forståelse av de økonomiske dataene i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="91458-111">Setting up account schedules requires an understanding of the financial data in the chart of accounts.</span></span> <span data-ttu-id="91458-112">Du kan for eksempel vise finansposter som en prosentandel av budsjettpostene.</span><span class="sxs-lookup"><span data-stu-id="91458-112">For example, you can view general ledger entries as percentages of budget entries.</span></span> <span data-ttu-id="91458-113">Dette krever at budsjetter opprettes.</span><span class="sxs-lookup"><span data-stu-id="91458-113">This requires that budgets are created.</span></span> <span data-ttu-id="91458-114">Hvis du vil ha mer informasjon, kan du se [Opprette finansbudsjetter](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="91458-114">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="account-categories-and-account-schedules"></a><span data-ttu-id="91458-115">Kontokategorier og kontoskjemaer</span><span class="sxs-lookup"><span data-stu-id="91458-115">Account Categories and Account Schedules</span></span>
<span data-ttu-id="91458-116">Du kan bruke kontokategoriene til å endre oppsettet for regnskapsoppgjørene.</span><span class="sxs-lookup"><span data-stu-id="91458-116">You can use account categories to change the layout of your financial statements.</span></span> <span data-ttu-id="91458-117">Når du har definert kontokategoriene i vinduet **Finanskontokategorier** og du velger handlingen **Generer kontoskjemaer**, oppdateres de underliggende kontoskjemaene for kjernefinansrapporter.</span><span class="sxs-lookup"><span data-stu-id="91458-117">After you set up your account categories in the **G/L Account Categories** window, and you choose the **Generate Account Schedules** action, the underlying account schedules for the core financial reports are updated.</span></span> <span data-ttu-id="91458-118">Neste gang du kjører en av disse rapportene, for eksempel saldoutdrag, legges ny totaler og underoppføringer til, basert på endringene.</span><span class="sxs-lookup"><span data-stu-id="91458-118">The next time you run one of these reports, such as the Balance Statement report, new totals and subentries are added, based on your changes.</span></span> <span data-ttu-id="91458-119">Hvis du vil ha mer informasjon, kan du se delen Kontokategorier i [Forstå finans og kontoplanen](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="91458-119">For more information, see The "Account Categories" section in [Understanding the General Ledger and the COA](finance-general-ledger.md).</span></span>  

## <a name="to-create-new-account-schedules"></a><span data-ttu-id="91458-120">Slik oppretter du nye kontoskjemaer</span><span class="sxs-lookup"><span data-stu-id="91458-120">To create new account schedules</span></span>  
 <span data-ttu-id="91458-121">Du bruker kontoskjemaer til å analysere tall på finanskonti eller til å sammenligne faktiske finansposter med finansbudsjettposter.</span><span class="sxs-lookup"><span data-stu-id="91458-121">You use account schedules to analyze figures in general ledger accounts or to compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="91458-122">Du kan for eksempel vise finansposter som en prosentandel av budsjettpostene.</span><span class="sxs-lookup"><span data-stu-id="91458-122">For example, you can view the general ledger entries as percentages of the budget entries.</span></span>

1. <span data-ttu-id="91458-123">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kontoskjemaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="91458-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2. <span data-ttu-id="91458-124">Velg handlingen **Ny** i vinduet **Kontoskjemanavn** for å opprette et nytt kontoskjemanavn.</span><span class="sxs-lookup"><span data-stu-id="91458-124">In the **Account Schedule Names** window, choose the **New** action to create a new account schedule name.</span></span>
3. <span data-ttu-id="91458-125">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="91458-125">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="91458-126">Velg handlingen **Rediger kontoskjema**.</span><span class="sxs-lookup"><span data-stu-id="91458-126">Choose the **Edit Account Schedule** action.</span></span>
5. <span data-ttu-id="91458-127">Fyll ut feltene etter behov i vinduet **Kontoskjema**.</span><span class="sxs-lookup"><span data-stu-id="91458-127">In the **Account Schedule** window, fill in the fields as necessary.</span></span>  

    <span data-ttu-id="91458-128">Når du har opprettet et nytt kontoskjema og definert radene, må du definere kolonner.</span><span class="sxs-lookup"><span data-stu-id="91458-128">When you have created a new account schedule and set up the rows, you must set up columns.</span></span> <span data-ttu-id="91458-129">Dette kan du gjøre manuelt eller ved hjelp av et forhåndsdefinert kolonneoppsett.</span><span class="sxs-lookup"><span data-stu-id="91458-129">You can either set them up manually or assign a predefined column layout to your account schedule.</span></span>
6. <span data-ttu-id="91458-130">Velg handlingen **Rediger oppsett for kolonneutforming**.</span><span class="sxs-lookup"><span data-stu-id="91458-130">Choose the **Edit Column Layout Setup** action.</span></span>
7. <span data-ttu-id="91458-131">I vinduet **Kolonneoppsett** fyller du ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="91458-131">In the **Column Layout** window, fill in the fields as necessary.</span></span>

> [!NOTE]  
> <span data-ttu-id="91458-132">Hvis du ikke tilordnet et standard kolonneoppsett til kontoskjemaet, må du definere kolonnene manuelt.</span><span class="sxs-lookup"><span data-stu-id="91458-132">If you did not assign a default column layout to the account schedule, you must set the columns up manually.</span></span>

### <a name="to-copy-an-existing-account-schedule"></a><span data-ttu-id="91458-133">Kopiere et eksisterende kontoskjema</span><span class="sxs-lookup"><span data-stu-id="91458-133">To copy an existing account schedule</span></span>
<span data-ttu-id="91458-134">Kontoskjemaene i standardversjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] er grunnlaget for standard finansrapporter som kanskje ikke oppfylle kravene til virksomheten.</span><span class="sxs-lookup"><span data-stu-id="91458-134">The account schedules in the standard version of [!INCLUDE[d365fin](includes/d365fin_md.md)] are the basis of the standard financial reports, which may not suit the needs of your business.</span></span> <span data-ttu-id="91458-135">Hvis du raskt vil opprette dine egne finansrapporter, kan du begynne med å kopiere et eksisterende kontoskjema.</span><span class="sxs-lookup"><span data-stu-id="91458-135">To quickly create your own financial reports, you can start by copying an existing account schedule.</span></span>
1. <span data-ttu-id="91458-136">Velg kontoskjema i vinduet **Kontoskjemaer**, og velg deretter handlingen **Kopier kontoskjema**.</span><span class="sxs-lookup"><span data-stu-id="91458-136">In the **Account Schedules** window, select an account schedule, and then choose the **Copy Account Schedule** action.</span></span>
2. <span data-ttu-id="91458-137">I vinduet **Kopier kontoskjema** fyller du ut feltene etter behov, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="91458-137">In the **Copy Account Schedule** window, fill in the fields as necessary, and then choose the **OK** button.</span></span>

### <a name="to-create-a-column-that-calculates-percentages"></a><span data-ttu-id="91458-138">Slik oppretter du en kolonne som beregner prosentdeler</span><span class="sxs-lookup"><span data-stu-id="91458-138">To create a column that calculates percentages</span></span>  
<span data-ttu-id="91458-139">Noen ganger vil du kanskje ta med en kolonne i et kontoskjema for å beregne prosentdeler av en sum.</span><span class="sxs-lookup"><span data-stu-id="91458-139">Sometimes you may want to include a column in an account schedule to calculate percentages of a total.</span></span> <span data-ttu-id="91458-140">Hvis du for eksempel har et antall rader som bryter ned salg etter dimensjon, vil du kanskje ta med en kolonne som angir hvor stor prosentdel av totalt salg hver rad representerer.</span><span class="sxs-lookup"><span data-stu-id="91458-140">For example, if you have a number of rows that break down sales by dimension, you may want a column to indicate the percentage of total sales that each row represents.</span></span>

1. <span data-ttu-id="91458-141">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kontoskjemaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="91458-141">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="91458-142">Velg et kontoskjema i vinduet **Kontoskjemanavn**.</span><span class="sxs-lookup"><span data-stu-id="91458-142">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="91458-143">Velg handlingen **Rediger kontoskjema** for å definere en kontoskjemarad som skal brukes til å beregne summen prosentene skal baseres på.</span><span class="sxs-lookup"><span data-stu-id="91458-143">Choose the **Edit Account Schedule** action to set up an account schedule row to calculate the total on which the percentages will be based.</span></span>  
4. <span data-ttu-id="91458-144">Sett inn en linje like over den første raden som du vil vise en prosentdel for.</span><span class="sxs-lookup"><span data-stu-id="91458-144">Insert a line immediately above the first row for which you want to display a percentage.</span></span>  
5. <span data-ttu-id="91458-145">Fyll ut feltene på linjen som følger: I feltet **Sammentellingstype** angir du **Angi grunnlag for prosent**.</span><span class="sxs-lookup"><span data-stu-id="91458-145">Fill in the fields on the line as follows: In the **Totaling Type** field, enter **Set Base for Percent**.</span></span> <span data-ttu-id="91458-146">Skriv inn en formel for summen som prosentdelen skal være basert på, i **Sammentelling**-feltet.</span><span class="sxs-lookup"><span data-stu-id="91458-146">In the **Totaling** field, enter a formula for the total that the percentage will be based on.</span></span> <span data-ttu-id="91458-147">Hvis rad 11 for eksempel inneholder totalt salg, angir du **11**.</span><span class="sxs-lookup"><span data-stu-id="91458-147">For example, if row 11 contains the total sales, enter **11**.</span></span>  
6. <span data-ttu-id="91458-148">Velg handlingen **Rediger oppsett for kolonneutforming** for å definere en kolonne.</span><span class="sxs-lookup"><span data-stu-id="91458-148">Choose the **Edit Column Layout Setup** action to set up a column.</span></span>  
7. <span data-ttu-id="91458-149">Fyll ut feltene på linjen som følger: I feltet **Kolonnetype** velger du **Formel**.</span><span class="sxs-lookup"><span data-stu-id="91458-149">Fill in the fields on the line as follows: In the **Column Type** field, select **Formula**.</span></span> <span data-ttu-id="91458-150">Skriv inn en formel for beløpet du vil beregne en prosent for, fulgt av %, i **Formel**-feltet.</span><span class="sxs-lookup"><span data-stu-id="91458-150">In the **Formula** field, enter a formula for the amount that you want to calculate a percentage for, followed by %.</span></span> <span data-ttu-id="91458-151">Hvis kolonnenummeret N for eksempel inneholder bevegelsen, angir du **N %**.</span><span class="sxs-lookup"><span data-stu-id="91458-151">For example, if column number N contains the net change, enter **N%**.</span></span>  
8. <span data-ttu-id="91458-152">Gjenta trinn 4 til og med 7 for hver gruppe med rader du vil bryte ned i prosentdeler.</span><span class="sxs-lookup"><span data-stu-id="91458-152">Repeat steps 4 through 7 for each group of rows that you want to break down by percentage.</span></span>

## <a name="to-set-up-account-schedules-with-overviews"></a><span data-ttu-id="91458-153">Slik setter du opp kontoskjemaer med oversikter</span><span class="sxs-lookup"><span data-stu-id="91458-153">To set up account schedules with overviews</span></span>  
<span data-ttu-id="91458-154">Du kan bruke et kontoskjema til å opprette en oppgave som sammenligner finanstall og finansbudsjettall.</span><span class="sxs-lookup"><span data-stu-id="91458-154">You can use an account schedule to create a statement comparing general ledger figures and general leger budget figures.</span></span>

1. <span data-ttu-id="91458-155">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kontoskjemaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="91458-155">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="91458-156">Velg et kontoskjema i vinduet **Kontoskjemanavn**.</span><span class="sxs-lookup"><span data-stu-id="91458-156">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="91458-157">Velg handlingen **Rediger kontoskjema**.</span><span class="sxs-lookup"><span data-stu-id="91458-157">Choose the **Edit Account Schedule** action</span></span>  
4. <span data-ttu-id="91458-158">Velg standawrd kontoskjemanavn i **Navn**-feltet i **Kontoskjema**-vinduet.</span><span class="sxs-lookup"><span data-stu-id="91458-158">In the **Account Schedule** window, in the **Name** field, select the default account schedule name.</span></span>
5. <span data-ttu-id="91458-159">Velg handlingen **Sett inn konti**.</span><span class="sxs-lookup"><span data-stu-id="91458-159">Choose the **Insert Accounts** action.</span></span>  
6. <span data-ttu-id="91458-160">Velg kontiene du vil ta med i oppgaven , og klikk deretter **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="91458-160">Select the accounts that you want to include in your statement, and then choose the **OK** button.</span></span>

    <span data-ttu-id="91458-161">Kontiene settes nå inn i kontoskjemaet.</span><span class="sxs-lookup"><span data-stu-id="91458-161">The accounts are now inserted into your account schedule.</span></span> <span data-ttu-id="91458-162">Hvis du vil, kan du også endre kolonneoppsettet.</span><span class="sxs-lookup"><span data-stu-id="91458-162">If you want you can also change the column layout.</span></span>  
7. <span data-ttu-id="91458-163">Velg handlingen **Oversikt**.</span><span class="sxs-lookup"><span data-stu-id="91458-163">Choose the **Overview** action.</span></span>  
8. <span data-ttu-id="91458-164">På hurtigfanen **Dimensjonsfiltre** setter du budsjettfilteret til ønsket filternavn.</span><span class="sxs-lookup"><span data-stu-id="91458-164">On the **Dimension Filters** FastTab, set the budget filter to the desired filter name.</span></span>  
9. <span data-ttu-id="91458-165">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="91458-165">Choose the **OK** button.</span></span>  

<span data-ttu-id="91458-166">Du kan nå kopiere og lime inn budsjettoppgaven i et regneark.</span><span class="sxs-lookup"><span data-stu-id="91458-166">Now you can copy and paste your budget statement into a spreadsheet.</span></span>  

## <a name="comparing-accounting-periods-using-period-formulas"></a><span data-ttu-id="91458-167">Sammenligne regnskapsperioder ved hjelp av periodeformler</span><span class="sxs-lookup"><span data-stu-id="91458-167">Comparing Accounting Periods using Period Formulas</span></span>
<span data-ttu-id="91458-168">Kontoskjemaet kan sammenligne resultatene av ulike regnskapsperioder, for eksempel inneværende måned og samme måned i fjor.</span><span class="sxs-lookup"><span data-stu-id="91458-168">Your account schedule can compare the results of different accounting periods, such as this month versus same month last year.</span></span> <span data-ttu-id="91458-169">For å gjøre dette må du legge til en kolonne med **Formel - periodesammenligning**-feltet, og deretter angi dette feltet som en periodeformel.</span><span class="sxs-lookup"><span data-stu-id="91458-169">To do that, you add a column with the **Comparison Period Formula** field, and then set that field to a period formula.</span></span>  

<span data-ttu-id="91458-170">En regnskapsperiode trenger ikke å sammenfalle med kalenderen, men regnskapsåret må ha samme antall regnskapsperioder, selv om hver periode kan variere i lengde.</span><span class="sxs-lookup"><span data-stu-id="91458-170">An accounting period does not have to match the calendar, but each fiscal year must have the same number of accounting periods, even though each period can be different in length.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="91458-171">bruker periodeformelen til å beregne beløpet fra sammenligningsperioden, i forhold til perioden som er angitt i datofilteret i rapportforespørselen.</span><span class="sxs-lookup"><span data-stu-id="91458-171">uses the period formula to calculate the amount from the comparison period in relation to the period represented by the date filter on the report request.</span></span> <span data-ttu-id="91458-172">Sammenligningsperioden er basert på perioden for startdatoen i datofilteret.</span><span class="sxs-lookup"><span data-stu-id="91458-172">The comparison period is based on the period of the start date of the date filter.</span></span> <span data-ttu-id="91458-173">Periodene forkortes slik:</span><span class="sxs-lookup"><span data-stu-id="91458-173">The abbreviations for period specifications are:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91458-174">Forkortelse</span><span class="sxs-lookup"><span data-stu-id="91458-174">Abbreviation</span></span></th>
<th><span data-ttu-id="91458-175">Description</span><span class="sxs-lookup"><span data-stu-id="91458-175">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91458-176">P</span><span class="sxs-lookup"><span data-stu-id="91458-176">P</span></span></p></td>
<td><p><span data-ttu-id="91458-177">Periode</span><span class="sxs-lookup"><span data-stu-id="91458-177">Period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91458-178">SP</span><span class="sxs-lookup"><span data-stu-id="91458-178">LP</span></span></p></td>
<td><p><span data-ttu-id="91458-179">Siste periode av et regnskapsår, et halvår eller kvartal.</span><span class="sxs-lookup"><span data-stu-id="91458-179">Last period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91458-180">IP</span><span class="sxs-lookup"><span data-stu-id="91458-180">CP</span></span></p></td>
<td><p><span data-ttu-id="91458-181">Inneværende periode av et regnskapsår, et halvår eller kvartal.</span><span class="sxs-lookup"><span data-stu-id="91458-181">Current period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91458-182">RÅ</span><span class="sxs-lookup"><span data-stu-id="91458-182">FY</span></span></p></td>
<td><p><span data-ttu-id="91458-183">Regnskapsår.</span><span class="sxs-lookup"><span data-stu-id="91458-183">Fiscal year.</span></span> <span data-ttu-id="91458-184">Eksempelvis viser RÅ [1..3] til første kvartal av inneværende regnskapsår</span><span class="sxs-lookup"><span data-stu-id="91458-184">For example, FY[1..3] denotes first quarter of the current fiscal year</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="91458-185">Eksempler på formler:</span><span class="sxs-lookup"><span data-stu-id="91458-185">Examples of formulas:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91458-186">Formel</span><span class="sxs-lookup"><span data-stu-id="91458-186">Formula</span></span></th>
<th><span data-ttu-id="91458-187">Description</span><span class="sxs-lookup"><span data-stu-id="91458-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91458-188">&lt;Tom&gt;</span><span class="sxs-lookup"><span data-stu-id="91458-188">&lt;Blank&gt;</span></span></p></td>
<td><p><span data-ttu-id="91458-189">Inneværende periode</span><span class="sxs-lookup"><span data-stu-id="91458-189">Current period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91458-190">-1P</span><span class="sxs-lookup"><span data-stu-id="91458-190">-1P</span></span></p></td>
<td><p><span data-ttu-id="91458-191">Forrige periode</span><span class="sxs-lookup"><span data-stu-id="91458-191">Previous period</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91458-192">-1RÅ[1..SP]</span><span class="sxs-lookup"><span data-stu-id="91458-192">-1FY[1..LP]</span></span></p></td>
<td><p><span data-ttu-id="91458-193">Hele forrige regnskapsår</span><span class="sxs-lookup"><span data-stu-id="91458-193">Entire previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91458-194">-1RÅ</span><span class="sxs-lookup"><span data-stu-id="91458-194">-1FY</span></span></p></td>
<td><p><span data-ttu-id="91458-195">Inneværende periode i forrige regnskapsår</span><span class="sxs-lookup"><span data-stu-id="91458-195">Current period in previous fiscal year</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91458-196">-1RÅ[1..3]</span><span class="sxs-lookup"><span data-stu-id="91458-196">-1FY[1..3]</span></span></p></td>
<td><p><span data-ttu-id="91458-197">Første kvartal av forrige regnskapsår</span><span class="sxs-lookup"><span data-stu-id="91458-197">First quarter of previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91458-198">-1RÅ[1..IP]</span><span class="sxs-lookup"><span data-stu-id="91458-198">-1FY[1..CP]</span></span></p></td>
<td><p><span data-ttu-id="91458-199">Fra begynnelsen av forrige regnskapsår til og med inneværende periode i forrige regnskapsår</span><span class="sxs-lookup"><span data-stu-id="91458-199">From the beginning of previous fiscal year to current period in previous fiscal year, inclusive</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91458-200">-1RÅ[IP..SP]</span><span class="sxs-lookup"><span data-stu-id="91458-200">-1FY[CP..LP]</span></span></p></td>
<td><p><span data-ttu-id="91458-201">Fra inneværende periode i forrige regnskapsår til og med siste periode i forrige regnskapsår</span><span class="sxs-lookup"><span data-stu-id="91458-201">From current period in previous fiscal year to last period of previous fiscal year, inclusive</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="91458-202">Hvis du vil beregne etter regelmessige perioder, må du angi en formel i feltet **Datoformel - sammenligning** i stedet.</span><span class="sxs-lookup"><span data-stu-id="91458-202">If you want to calculate by regular time periods, you must enter a formula in the **Comparison Date Formula** field instead.</span></span>

> [!NOTE]
> <span data-ttu-id="91458-203">Det er ikke alltid gjennomsiktig hvilke perioder du sammenligner, siden du kan angi et datofilter i en rapport som inneholder forskjellige datoer enn regnskapsperiodene som gjenspeiles i dataene i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="91458-203">It is not always transparent which periods you are comparing because you can set a date filter on a report that spans different dates than the accounting periods that are reflected in the data in the chart of accounts.</span></span> <span data-ttu-id="91458-204">Du oppretter for eksempel et kontoskjema der du vil sammenligne denne perioden med samme periode i fjor, så du setter **Sammenligningsperiode - filter**-feltet til *-1RÅ*.</span><span class="sxs-lookup"><span data-stu-id="91458-204">For example, you create an account schedule where you want to compare this period with the same period last year, so you set the **Comparison Date Period Filter** field to *-1FY*.</span></span> <span data-ttu-id="91458-205">Deretter kjører du rapporten 28. februar og setter datofilteret til januar og februar.</span><span class="sxs-lookup"><span data-stu-id="91458-205">Then, you run the report on February 28th and set the date filter to January and February.</span></span> <span data-ttu-id="91458-206">Dermed sammenligner kontoskjemaet januar og februar i år med januar i fjor, som er den eneste fullførte regnskapsperioden av de to for forrige år.</span><span class="sxs-lookup"><span data-stu-id="91458-206">As a result, the account schedule compares January and February this year to January last year, which is the only completed accounting period of the two for last year.</span></span>  


## <a name="see-also"></a><span data-ttu-id="91458-207">Se også</span><span class="sxs-lookup"><span data-stu-id="91458-207">See Also</span></span>
[<span data-ttu-id="91458-208">Forretningsintelligens</span><span class="sxs-lookup"><span data-stu-id="91458-208">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="91458-209">Finans</span><span class="sxs-lookup"><span data-stu-id="91458-209">Finance</span></span>](finance.md)  
[<span data-ttu-id="91458-210">Konfigurere finans</span><span class="sxs-lookup"><span data-stu-id="91458-210">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="91458-211">Finans og kontoplanen</span><span class="sxs-lookup"><span data-stu-id="91458-211">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="91458-212">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="91458-212">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

