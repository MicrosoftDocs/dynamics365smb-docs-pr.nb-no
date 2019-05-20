---
title: Lage økonomirapporter med kontoskjemaer
description: Beskriver hvordan du bruker kontoskjemaer til å opprette ulike visninger og rapporter for å analysere økonomiske resultatdata.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: e7430c17e090e2b0c3ca13ee7c52cfec749fcc2b
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245377"
---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a><span data-ttu-id="e6ddc-103">Klargjøre finansrapportering med kontoskjemaer og kontokategorier</span><span class="sxs-lookup"><span data-stu-id="e6ddc-103">Prepare Financial Reporting with Account Schedules and Account Categories</span></span>
<span data-ttu-id="e6ddc-104">Du kan bruke kontoskjemaer til å få innsikt i de økonomiske dataene som er lagret i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-104">Use account schedules to get insight into the financial data stored in your chart of accounts.</span></span> <span data-ttu-id="e6ddc-105">Kontoskjemaer analyserer tall på finanskonti og sammenligner faktiske finansposter med finansbudsjettposter.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-105">Account schedules analyze figures in G/L accounts, and compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="e6ddc-106">Resultatet vises i diagrammer i rollesenteret, for eksempel ut Kontantstrøm-diagrammet, og i rapporter, for eksempel rapporten Resultatregnskap og Balanse.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-106">The results display in charts on your Role Center, such as the Cash Flow chart, and in reports, such as the Income Statement and the Balance Sheet reports.</span></span>

<span data-ttu-id="e6ddc-107">Du får tilgang til disse to rapportene for eksempel med handlingen **Årsregnskap** i rollesentrene for forretningsleder og regnskapsfører.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-107">You access these two reports, for example, with the **Financials Statements** action on the Business Manager and Accountant Role Centers.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="e6ddc-108">inneholder et par eksempler på kontoskjemaer som du kan bruke med én gang, eller du kan definere dine egne rader og kolonner for å angi tallene som skal sammenlignes.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-108">provides a few sample account schedules that you can use right away, or you can set up your own rows and columns to specify the figures to compare.</span></span> <span data-ttu-id="e6ddc-109">Du kan for eksempel opprette kontoskjemaer for å beregne fortjenestemarginer for dimensjoner som avdelinger eller kundegrupper.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-109">For example, you can create account schedules to calculate profit margins on dimensions like departments or customer groups.</span></span> <span data-ttu-id="e6ddc-110">Du kan opprette så mange egendefinerte regnskapsrapporter du vil.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-110">You can create as many customized financial statements as you want.</span></span>  

<span data-ttu-id="e6ddc-111">Oppretting av kontoskjemaer krever en forståelse av de økonomiske dataene i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-111">Setting up account schedules requires an understanding of the financial data in the chart of accounts.</span></span> <span data-ttu-id="e6ddc-112">Du kan for eksempel vise finansposter som en prosentandel av budsjettpostene.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-112">For example, you can view general ledger entries as percentages of budget entries.</span></span> <span data-ttu-id="e6ddc-113">Dette krever at budsjetter opprettes.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-113">This requires that budgets are created.</span></span> <span data-ttu-id="e6ddc-114">Hvis du vil ha mer informasjon, kan du se [Opprette finansbudsjetter](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="e6ddc-114">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="account-schedules"></a><span data-ttu-id="e6ddc-115">Kontoskjemaer</span><span class="sxs-lookup"><span data-stu-id="e6ddc-115">Account Schedules</span></span>
<span data-ttu-id="e6ddc-116">Kontoskjemaer brukes til å organisere konti som er oppført i kontoplanen, på måter som egner seg for å presentere informasjon om disse kontiene.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-116">Account schedules are used to arrange accounts listed in the chart of accounts in ways suited for presentation of information about those accounts.</span></span> <span data-ttu-id="e6ddc-117">Du kan definere ulike oppsett for å velge hvilken informasjon du vil trekke ut fra kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-117">You can set up various layouts to define the information that you want to extract from the chart of accounts.</span></span> <span data-ttu-id="e6ddc-118">En av hovedfunksjonene med kontoskjemaer er å tilby et sted for beregninger som ikke kan gjøres direkte i kontoplanen, for eksempel oppretting av delsummer for kontogrupper, som kan inkluderes i nye summer og deretter brukes i andre totalsummer.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-118">One of the main functions of account schedules is to provide a place for calculations that cannot be made directly in the chart of accounts, such as creating subtotals for groups of accounts, which can be included in new totals and can then be used in other totals.</span></span> <span data-ttu-id="e6ddc-119">Brukere kan for eksempel opprette kontoskjemaer for å beregne fortjenestemarginer for dimensjoner som avdelinger eller kundegrupper.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-119">For example, users can create account schedules to calculate profit margins on such dimensions as departments or customer groups.</span></span> <span data-ttu-id="e6ddc-120">I tillegg kan finansposter og finansbudsjettposter filtreres, for eksempel etter bevegelse eller debetbeløp.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-120">In addition, general ledger entries and general ledger budget entries can be filtered, for example, by net change or debit amount.</span></span>

<span data-ttu-id="e6ddc-121">Du kan også sammenligne to eller flere kontoskjemaer og kolonneoppsett ved hjelp av formler.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-121">You can also compare two or more account schedules and column layouts by using formulas.</span></span> <span data-ttu-id="e6ddc-122">Denne typen sammenligning gir muligheter for følgende:</span><span class="sxs-lookup"><span data-stu-id="e6ddc-122">This kind of comparison provides the ability to:</span></span>

* <span data-ttu-id="e6ddc-123">Opprette tilpassede finansrapporter.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-123">Create customized financial reports.</span></span>
* <span data-ttu-id="e6ddc-124">Opprette så mange kontoskjemaer som nødvendig, med unike navn.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-124">Create as many account schedules as needed, each with a unique name.</span></span>
* <span data-ttu-id="e6ddc-125">Definere ulike rapportoppsett og skrive ut rapportene med gjeldende tall.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-125">Set up various report layouts and print the reports with the current figures.</span></span>

## <a name="account-categories"></a><span data-ttu-id="e6ddc-126">Kontokategorier</span><span class="sxs-lookup"><span data-stu-id="e6ddc-126">Account Categories</span></span>
<span data-ttu-id="e6ddc-127">Du kan bruke kontokategoriene til å endre oppsettet for regnskapsoppgjørene.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-127">You can use account categories to change the layout of your financial statements.</span></span> <span data-ttu-id="e6ddc-128">Når du har definert kontokategoriene på siden **Finanskontokategorier** og du velger handlingen **Generer kontoskjemaer**, oppdateres de underliggende kontoskjemaene for kjernefinansrapporter.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-128">After you set up your account categories on the **G/L Account Categories** page, and you choose the **Generate Account Schedules** action, the underlying account schedules for the core financial reports are updated.</span></span> <span data-ttu-id="e6ddc-129">Neste gang du kjører en av disse rapportene, for eksempel saldoutdrag, legges ny totaler og underoppføringer til, basert på endringene.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-129">The next time you run one of these reports, such as the Balance Statement report, new totals and subentries are added, based on your changes.</span></span> <span data-ttu-id="e6ddc-130">Se [Kontokategorier](finance-general-ledger.md#account-categories) for mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-130">For more information, see [Account Categories](finance-general-ledger.md#account-categories).</span></span>  

## <a name="to-create-a-new-account-schedule"></a><span data-ttu-id="e6ddc-131">Opprette et nytt kontoskjema</span><span class="sxs-lookup"><span data-stu-id="e6ddc-131">To create a new account schedule</span></span>  
<span data-ttu-id="e6ddc-132">Du bruker kontoskjemaer til å analysere tall på finanskonti eller til å sammenligne faktiske finansposter med finansbudsjettposter.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-132">You use account schedules to analyze figures in general ledger accounts or to compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="e6ddc-133">Du kan for eksempel vise finansposter som en prosentandel av budsjettpostene.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-133">For example, you can view the general ledger entries as percentages of the budget entries.</span></span>

<span data-ttu-id="e6ddc-134">Kontoskjemaene i standardversjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] er grunnlaget for standard finansrapporter som kanskje ikke oppfylle kravene til virksomheten.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-134">The account schedules in the standard version of [!INCLUDE[d365fin](includes/d365fin_md.md)] are the basis of the standard financial reports, which may not suit the needs of your business.</span></span> <span data-ttu-id="e6ddc-135">Hvis du raskt vil opprette dine egne finansrapporter, kan du begynne med å kopiere et eksisterende kontoskjema.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-135">To quickly create your own financial reports, you can start by copying an existing account schedule.</span></span> <span data-ttu-id="e6ddc-136">Se trinn 3 nedenfor.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-136">See step 3 below.</span></span>

<span data-ttu-id="e6ddc-137">Siden **Kto.skjemaoversikt** er der du kan forhåndsvise den økonomiske rapporten som kontoskjemaet definerer.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-137">The **Acc. Schedule Overview** page is where you preview the financial report that the account schedule defines.</span></span> <span data-ttu-id="e6ddc-138">I det følgende er det viktig å forstå at det du definerer som kontoskjemarader og -kolonner, bare kan ses og valideres på siden **Kto.skjemaoversikt**, som du åpner fra et kontoskjema ved å velge **Oversikt**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-138">In the following, it is important to understand that what you set up as account schedule rows and columns can only be seen and validated on the **Acc. Schedule Overview** page, which you open from an account schedule by choosing the **Overview** action.</span></span> <span data-ttu-id="e6ddc-139">Selve **Kontoskjema**-siden er bare et oppsettsområde.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-139">The **Account Schedule** page itself is only a setup area.</span></span>  

1. <span data-ttu-id="e6ddc-140">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kontoskjemaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-140">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e6ddc-141">Velg handlingen **Ny** på siden **Kontoskjemaer** for å opprette et nytt kontoskjemanavn.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-141">On the **Account Schedules** page, choose the **New** action to create a new account schedule name.</span></span>
3. <span data-ttu-id="e6ddc-142">Du kan også velge handlingen **Kopier kontoskjema**, fylle ut de to feltene, og deretter velge **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-142">Alternatively, choose the **Copy Account Schedule** action, fill in the two fields, and then choose the **OK** button.</span></span>
4. <span data-ttu-id="e6ddc-143">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-143">Fill in the fields as necessary.</span></span> <span data-ttu-id="e6ddc-144">I feltet **Standard kolonneoppsett** velger du et eksisterende oppsett.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-144">In the **Default Column Layout** field select an existing layout.</span></span> <span data-ttu-id="e6ddc-145">Det kan endres senere om du vil.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-145">You can edit it later if you want.</span></span>

    <span data-ttu-id="e6ddc-146">Du bruker kolonneoppsett til å definere kolonner for ulike parametere som finansielle data i radene vises etter.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-146">You use column layouts to define columns for different parameters by which the financial data on the rows are shown.</span></span> <span data-ttu-id="e6ddc-147">Du kan for eksempel utforme et kolonneoppsett for å sammenligne bevegelse og saldo for samme periode i år og i fjor, med fire kolonner.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-147">For example, you can design a column layout to compare net change and balance for the same period this year and last year, with four columns.</span></span> <span data-ttu-id="e6ddc-148">Hvis du vil ha mer informasjon, kan du se [Redigere et kolonneoppsett](bi-how-work-account-schedule.md#to-edit-a-column-layout).</span><span class="sxs-lookup"><span data-stu-id="e6ddc-148">For more information, see [To edit a column layout](bi-how-work-account-schedule.md#to-edit-a-column-layout).</span></span>

5. <span data-ttu-id="e6ddc-149">Velg handlingen **Rediger kontoskjema**.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-149">Choose the **Edit Account Schedule** action.</span></span>
6. <span data-ttu-id="e6ddc-150">Opprett en rad for hvert økonomiske element som du vil skal vises i rapporten, for eksempel en rad for gjeldende aktiva og en ny rad for aktiva.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-150">Create a row for each financial element that you want to appear in the report, such as one row for current assets and another row for fixed assets.</span></span> <span data-ttu-id="e6ddc-151">For inspirasjon kan du se eksisterende kontoskjemaer i demoselskapet CRONUS.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-151">For inspiration, see existing account schedules in the CRONUS demonstration company.</span></span>
7. <span data-ttu-id="e6ddc-152">Velg handlingen **Oversikt** for å se den resulterende økonomiske rapporten.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-152">Choose the **Overview** action to see the resulting financial report.</span></span>
8. <span data-ttu-id="e6ddc-153">På siden **Kto.skjemaoversikt** i feltet **Navn på kolonneoppsett** velger du et annet kolonneoppsett for å vise økonomiske data etter andre parametere.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-153">On the **Acc. Schedule Overview** page, in the **Column Layout Name** field, select another column layout to see the financial data by other parameters.</span></span>
9. <span data-ttu-id="e6ddc-154">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-154">Choose the **OK** button.</span></span>

<span data-ttu-id="e6ddc-155">Du har nå definert grunnlaget for kontoskjemaet, radene med økonomiske data som skal vises, og et eksisterende kolonneoppsett for å vise dataene i radene per ulike parametere.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-155">You have now defined the basis of the account schedule, the rows of financial data to be displayed, and an existing layout of columns to show the data on the rows per different parameters.</span></span> <span data-ttu-id="e6ddc-156">Hvis standardkolonneoppsettet du valgte i trinn 4, ikke dekker behovet ditt, følger du fremgangsmåten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-156">If the default column layout that you selected in step 4 does not suit your purpose, follow the next procedure.</span></span>

### <a name="to-edit-a-column-layout"></a><span data-ttu-id="e6ddc-157">Redigere et kolonneoppsett</span><span class="sxs-lookup"><span data-stu-id="e6ddc-157">To edit a column layout</span></span>
<span data-ttu-id="e6ddc-158">Du bruker kolonneoppsett til å angi hvilke kolonner som skal være med i den resulterende rapporten.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-158">You use column layouts to define what columns should be included in the resulting report.</span></span> <span data-ttu-id="e6ddc-159">Du kan for eksempel sammenligne bevegelse og saldo for samme periode i år og i fjor.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-159">For example, you can design a layout to compare net change and balance for the same period this year and last year.</span></span>

> [!NOTE]
> <span data-ttu-id="e6ddc-160">En utskrifts-/forhåndsvisnings-/lagret versjon av et kontoskjema kan vise maksimalt fem kolonner.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-160">A printed/previewed/saved version of an account schedule can display a maximum of five columns.</span></span> <span data-ttu-id="e6ddc-161">Hvis kontoskjemaet bare er beregnet for analyse på siden **Kto.skjemaoversikt**, kan du opprette så mange kolonner du vil.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-161">If the account schedule is only meant for analysis on the **Acc. Schedule Overview** page, you can create as many columns as you want.</span></span>

1. <span data-ttu-id="e6ddc-162">På **Kontoskjemaer**-siden velger du det aktuelle kontoskjemaet, og velger deretter **Rediger oppsett for kolonneutforming**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-162">On the **Account Schedules** page, select the relevant account schedule, and then choose the **Edit Column Layout Setup** action.</span></span>
2. <span data-ttu-id="e6ddc-163">På siden **Kolonneoppsett** oppretter du en rad for hver kolonne som økonomiske data skal vises etter i den økonomiske rapporten.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-163">On the **Column Layouts** page, create a row for each column by which financial data is shown in the financial report.</span></span> [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="e6ddc-164">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-164">Choose the **OK** button.</span></span>
4. <span data-ttu-id="e6ddc-165">Åpne siden **Kto.skjemaoversikt** med jevne mellomrom for å kontrollere at det nye kolonneoppsettet fungerer som forventet.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-165">Open the **Acc. Schedule Overview** page from time to time to verify that the new column layout works as intended.</span></span>

> [!NOTE]
> <span data-ttu-id="e6ddc-166">Kolonnene som du definerer på hver rad, representerer kolonner 3 og oppover på **Kto.skjemaoversikt**-siden.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-166">The columns that you define on each row represent columns 3 and up on the **Acc. Schedule Overview** page.</span></span> <span data-ttu-id="e6ddc-167">De to første kolonnene, **Radnr.**</span><span class="sxs-lookup"><span data-stu-id="e6ddc-167">The first two columns, **Row No.**</span></span> <span data-ttu-id="e6ddc-168">og **Beskrivelse**, er faste.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-168">and **Description**, are fixed.</span></span>  

### <a name="to-create-a-column-that-calculates-percentages"></a><span data-ttu-id="e6ddc-169">Slik oppretter du en kolonne som beregner prosentdeler</span><span class="sxs-lookup"><span data-stu-id="e6ddc-169">To create a column that calculates percentages</span></span>  
<span data-ttu-id="e6ddc-170">Noen ganger vil du kanskje ta med en kolonne i et kontoskjema for å beregne prosentdeler av en sum.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-170">Sometimes you may want to include a column in an account schedule to calculate percentages of a total.</span></span> <span data-ttu-id="e6ddc-171">Hvis du for eksempel har et antall rader som bryter ned salg etter dimensjon, vil du kanskje ta med en kolonne som angir hvor stor prosentdel av totalt salg hver rad representerer.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-171">For example, if you have a number of rows that break down sales by dimension, you may want a column to indicate the percentage of total sales that each row represents.</span></span>

1. <span data-ttu-id="e6ddc-172">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kontoskjemaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-172">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="e6ddc-173">Velg et kontoskjema på siden **Kontoskjemanavn**.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-173">On the **Account Schedule Names** page, select an account schedule.</span></span>  
3. <span data-ttu-id="e6ddc-174">Velg handlingen **Rediger kontoskjema** for å definere en kontoskjemarad som skal brukes til å beregne summen prosentene skal baseres på.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-174">Choose the **Edit Account Schedule** action to set up an account schedule row to calculate the total on which the percentages will be based.</span></span>  
4. <span data-ttu-id="e6ddc-175">Sett inn en linje like over den første raden som du vil vise en prosentdel for.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-175">Insert a line immediately above the first row for which you want to display a percentage.</span></span>  
5. <span data-ttu-id="e6ddc-176">Fyll ut feltene på linjen som følger: I feltet **Sammentellingstype** angir du **Angi grunnlag for prosent**.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-176">Fill in the fields on the line as follows: In the **Totaling Type** field, enter **Set Base for Percent**.</span></span> <span data-ttu-id="e6ddc-177">Skriv inn en formel for summen som prosentdelen skal være basert på, i **Sammentelling**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-177">In the **Totaling** field, enter a formula for the total that the percentage will be based on.</span></span> <span data-ttu-id="e6ddc-178">Hvis rad 11 for eksempel inneholder totalt salg, angir du **11**.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-178">For example, if row 11 contains the total sales, enter **11**.</span></span>  
6. <span data-ttu-id="e6ddc-179">Velg handlingen **Rediger oppsett for kolonneutforming** for å definere en kolonne.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-179">Choose the **Edit Column Layout Setup** action to set up a column.</span></span>  
7. <span data-ttu-id="e6ddc-180">Fyll ut feltene på linjen som følger: I feltet **Kolonnetype** velger du **Formel**.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-180">Fill in the fields on the line as follows: In the **Column Type** field, select **Formula**.</span></span> <span data-ttu-id="e6ddc-181">Skriv inn en formel for beløpet du vil beregne en prosent for, fulgt av %, i **Formel**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-181">In the **Formula** field, enter a formula for the amount that you want to calculate a percentage for, followed by %.</span></span> <span data-ttu-id="e6ddc-182">Hvis kolonnenummeret N for eksempel inneholder bevegelsen, angir du **N %**.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-182">For example, if column number N contains the net change, enter **N%**.</span></span>  
8. <span data-ttu-id="e6ddc-183">Gjenta trinn 4 til og med 7 for hver gruppe med rader du vil bryte ned i prosentdeler.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-183">Repeat steps 4 through 7 for each group of rows that you want to break down by percentage.</span></span>

## <a name="to-set-up-account-schedules-with-overviews"></a><span data-ttu-id="e6ddc-184">Slik setter du opp kontoskjemaer med oversikter</span><span class="sxs-lookup"><span data-stu-id="e6ddc-184">To set up account schedules with overviews</span></span>  
<span data-ttu-id="e6ddc-185">Du kan bruke et kontoskjema til å opprette en oppgave som sammenligner finanstall og finansbudsjettall.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-185">You can use an account schedule to create a statement comparing general ledger figures and general leger budget figures.</span></span>

1. <span data-ttu-id="e6ddc-186">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kontoskjemaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-186">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="e6ddc-187">Velg et kontoskjema på siden **Kontoskjemanavn**.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-187">On the **Account Schedule Names** page, select an account schedule.</span></span>  
3. <span data-ttu-id="e6ddc-188">Velg handlingen **Rediger kontoskjema**.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-188">Choose the **Edit Account Schedule** action</span></span>  
4. <span data-ttu-id="e6ddc-189">Velg standard kontoskjemanavn i **Navn**-feltet på **Kontoskjema**-siden.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-189">On the **Account Schedule** page, in the **Name** field, select the default account schedule name.</span></span>
5. <span data-ttu-id="e6ddc-190">Velg handlingen **Sett inn konti**.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-190">Choose the **Insert Accounts** action.</span></span>  
6. <span data-ttu-id="e6ddc-191">Velg kontiene du vil ta med i oppgaven , og klikk deretter **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-191">Select the accounts that you want to include in your statement, and then choose the **OK** button.</span></span>

    <span data-ttu-id="e6ddc-192">Kontiene settes nå inn i kontoskjemaet.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-192">The accounts are now inserted into your account schedule.</span></span> <span data-ttu-id="e6ddc-193">Hvis du vil, kan du også endre kolonneoppsettet.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-193">If you want you can also change the column layout.</span></span>  
7. <span data-ttu-id="e6ddc-194">Velg handlingen **Oversikt**.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-194">Choose the **Overview** action.</span></span>  
8. <span data-ttu-id="e6ddc-195">På hurtigfanen **Dimensjonsfiltre** på **Kto.skjemaoversikt**-siden setter du budsjettfilteret til ønsket filternavn.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-195">On the **Acc. Schedule Overview** page, on the **Dimension Filters** FastTab, set the budget filter to the desired filter name.</span></span>  
9. <span data-ttu-id="e6ddc-196">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-196">Choose the **OK** button.</span></span>  

<span data-ttu-id="e6ddc-197">Du kan nå kopiere og lime inn budsjettoppgaven i et regneark.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-197">Now you can copy and paste your budget statement into a spreadsheet.</span></span>  

## <a name="comparing-accounting-periods-using-period-formulas"></a><span data-ttu-id="e6ddc-198">Sammenligne regnskapsperioder ved hjelp av periodeformler</span><span class="sxs-lookup"><span data-stu-id="e6ddc-198">Comparing Accounting Periods using Period Formulas</span></span>
<span data-ttu-id="e6ddc-199">Kontoskjemaet kan sammenligne resultatene av ulike regnskapsperioder, for eksempel inneværende måned og samme måned i fjor.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-199">Your account schedule can compare the results of different accounting periods, such as this month versus same month last year.</span></span> <span data-ttu-id="e6ddc-200">For å gjøre dette må du legge til en kolonne med **Formel - periodesammenligning**-feltet, og deretter angi dette feltet som en periodeformel.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-200">To do that, you add a column with the **Comparison Period Formula** field, and then set that field to a period formula.</span></span>  

<span data-ttu-id="e6ddc-201">En regnskapsperiode trenger ikke å sammenfalle med kalenderen, men regnskapsåret må ha samme antall regnskapsperioder, selv om hver periode kan variere i lengde.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-201">An accounting period does not have to match the calendar, but each fiscal year must have the same number of accounting periods, even though each period can be different in length.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="e6ddc-202">bruker periodeformelen til å beregne beløpet fra sammenligningsperioden, i forhold til perioden som er angitt i datofilteret i rapportforespørselen.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-202">uses the period formula to calculate the amount from the comparison period in relation to the period represented by the date filter on the report request.</span></span> <span data-ttu-id="e6ddc-203">Sammenligningsperioden er basert på perioden for startdatoen i datofilteret.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-203">The comparison period is based on the period of the start date of the date filter.</span></span> <span data-ttu-id="e6ddc-204">Periodene forkortes slik:</span><span class="sxs-lookup"><span data-stu-id="e6ddc-204">The abbreviations for period specifications are:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e6ddc-205">Forkortelse</span><span class="sxs-lookup"><span data-stu-id="e6ddc-205">Abbreviation</span></span></th>
<th><span data-ttu-id="e6ddc-206">Description</span><span class="sxs-lookup"><span data-stu-id="e6ddc-206">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6ddc-207">P</span><span class="sxs-lookup"><span data-stu-id="e6ddc-207">P</span></span></p></td>
<td><p><span data-ttu-id="e6ddc-208">Periode</span><span class="sxs-lookup"><span data-stu-id="e6ddc-208">Period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6ddc-209">SP</span><span class="sxs-lookup"><span data-stu-id="e6ddc-209">LP</span></span></p></td>
<td><p><span data-ttu-id="e6ddc-210">Siste periode av et regnskapsår, et halvår eller kvartal.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-210">Last period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6ddc-211">IP</span><span class="sxs-lookup"><span data-stu-id="e6ddc-211">CP</span></span></p></td>
<td><p><span data-ttu-id="e6ddc-212">Inneværende periode av et regnskapsår, et halvår eller kvartal.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-212">Current period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6ddc-213">RÅ</span><span class="sxs-lookup"><span data-stu-id="e6ddc-213">FY</span></span></p></td>
<td><p><span data-ttu-id="e6ddc-214">Regnskapsår.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-214">Fiscal year.</span></span> <span data-ttu-id="e6ddc-215">Eksempelvis viser RÅ [1..3] til første kvartal av inneværende regnskapsår</span><span class="sxs-lookup"><span data-stu-id="e6ddc-215">For example, FY[1..3] denotes first quarter of the current fiscal year</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e6ddc-216">Eksempler på formler:</span><span class="sxs-lookup"><span data-stu-id="e6ddc-216">Examples of formulas:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e6ddc-217">Formel</span><span class="sxs-lookup"><span data-stu-id="e6ddc-217">Formula</span></span></th>
<th><span data-ttu-id="e6ddc-218">Description</span><span class="sxs-lookup"><span data-stu-id="e6ddc-218">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6ddc-219">&lt;Tom&gt;</span><span class="sxs-lookup"><span data-stu-id="e6ddc-219">&lt;Blank&gt;</span></span></p></td>
<td><p><span data-ttu-id="e6ddc-220">Inneværende periode</span><span class="sxs-lookup"><span data-stu-id="e6ddc-220">Current period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6ddc-221">-1P</span><span class="sxs-lookup"><span data-stu-id="e6ddc-221">-1P</span></span></p></td>
<td><p><span data-ttu-id="e6ddc-222">Forrige periode</span><span class="sxs-lookup"><span data-stu-id="e6ddc-222">Previous period</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6ddc-223">-1RÅ[1..SP]</span><span class="sxs-lookup"><span data-stu-id="e6ddc-223">-1FY[1..LP]</span></span></p></td>
<td><p><span data-ttu-id="e6ddc-224">Hele forrige regnskapsår</span><span class="sxs-lookup"><span data-stu-id="e6ddc-224">Entire previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6ddc-225">-1RÅ</span><span class="sxs-lookup"><span data-stu-id="e6ddc-225">-1FY</span></span></p></td>
<td><p><span data-ttu-id="e6ddc-226">Inneværende periode i forrige regnskapsår</span><span class="sxs-lookup"><span data-stu-id="e6ddc-226">Current period in previous fiscal year</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6ddc-227">-1RÅ[1..3]</span><span class="sxs-lookup"><span data-stu-id="e6ddc-227">-1FY[1..3]</span></span></p></td>
<td><p><span data-ttu-id="e6ddc-228">Første kvartal av forrige regnskapsår</span><span class="sxs-lookup"><span data-stu-id="e6ddc-228">First quarter of previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6ddc-229">-1RÅ[1..IP]</span><span class="sxs-lookup"><span data-stu-id="e6ddc-229">-1FY[1..CP]</span></span></p></td>
<td><p><span data-ttu-id="e6ddc-230">Fra begynnelsen av forrige regnskapsår til og med inneværende periode i forrige regnskapsår</span><span class="sxs-lookup"><span data-stu-id="e6ddc-230">From the beginning of previous fiscal year to current period in previous fiscal year, inclusive</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6ddc-231">-1RÅ[IP..SP]</span><span class="sxs-lookup"><span data-stu-id="e6ddc-231">-1FY[CP..LP]</span></span></p></td>
<td><p><span data-ttu-id="e6ddc-232">Fra inneværende periode i forrige regnskapsår til og med siste periode i forrige regnskapsår</span><span class="sxs-lookup"><span data-stu-id="e6ddc-232">From current period in previous fiscal year to last period of previous fiscal year, inclusive</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e6ddc-233">Hvis du vil beregne etter regelmessige perioder, må du angi en formel i feltet **Datoformel - sammenligning** i stedet.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-233">If you want to calculate by regular time periods, you must enter a formula in the **Comparison Date Formula** field instead.</span></span>

> [!NOTE]
> <span data-ttu-id="e6ddc-234">Det er ikke alltid gjennomsiktig hvilke perioder du sammenligner, siden du kan angi et datofilter i en rapport som inneholder forskjellige datoer enn regnskapsperiodene som gjenspeiles i dataene i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-234">It is not always transparent which periods you are comparing because you can set a date filter on a report that spans different dates than the accounting periods that are reflected in the data in the chart of accounts.</span></span> <span data-ttu-id="e6ddc-235">Du oppretter for eksempel et kontoskjema der du vil sammenligne denne perioden med samme periode i fjor, så du setter **Sammenligningsperiode - filter**-feltet til *-1RÅ*.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-235">For example, you create an account schedule where you want to compare this period with the same period last year, so you set the **Comparison Date Period Filter** field to *-1FY*.</span></span> <span data-ttu-id="e6ddc-236">Deretter kjører du rapporten 28. februar og setter datofilteret til januar og februar.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-236">Then, you run the report on February 28th and set the date filter to January and February.</span></span> <span data-ttu-id="e6ddc-237">Dermed sammenligner kontoskjemaet januar og februar i år med januar i fjor, som er den eneste fullførte regnskapsperioden av de to for forrige år.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-237">As a result, the account schedule compares January and February this year to January last year, which is the only completed accounting period of the two for last year.</span></span>  


## <a name="see-also"></a><span data-ttu-id="e6ddc-238">Se også</span><span class="sxs-lookup"><span data-stu-id="e6ddc-238">See Also</span></span>
[<span data-ttu-id="e6ddc-239">Forretningsintelligens</span><span class="sxs-lookup"><span data-stu-id="e6ddc-239">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="e6ddc-240">Finans</span><span class="sxs-lookup"><span data-stu-id="e6ddc-240">Finance</span></span>](finance.md)  
[<span data-ttu-id="e6ddc-241">Konfigurere finans</span><span class="sxs-lookup"><span data-stu-id="e6ddc-241">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="e6ddc-242">Finans og kontoplanen</span><span class="sxs-lookup"><span data-stu-id="e6ddc-242">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="e6ddc-243">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e6ddc-243">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
