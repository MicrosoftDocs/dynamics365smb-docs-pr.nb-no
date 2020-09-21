---
title: Vise egendefinerte Power BI-rapporter for Business Central-data | Microsoft Docs
description: Du kan bruke Power BI-rapporter til å få ytterligere innsikt i data i lister.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 5d3acaf05952a61845eb8bb72b2556f2e54f8208
ms.sourcegitcommit: aeaa0dc64e54432a70c4b0e1faf325cd17d01389
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697701"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prodshort"></a><span data-ttu-id="69548-103">Opprette Power BI-rapporter for å vise listedata i [!INCLUDE[prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="69548-103">Creating Power BI Reports for Displaying List Data in [!INCLUDE[prodshort](includes/prodshort.md)]</span></span>

[!INCLUDE[prodlong](includes/prodlong.md)] <span data-ttu-id="69548-104">omfatter et element for faktabokskontroll på en rekke viktige listesider som gir ytterligere innsikt i dataene i listen.</span><span class="sxs-lookup"><span data-stu-id="69548-104">includes a FactBox control element on a number of key list pages that provide additional insight into the data in the list.</span></span> <span data-ttu-id="69548-105">Når du flytter mellom radene i listen, er oppdateres og filtreres rapporten for den valgte posten.</span><span class="sxs-lookup"><span data-stu-id="69548-105">As you move between rows in the list, the report is updated and filtered for the selected entry.</span></span> <span data-ttu-id="69548-106">Du kan opprette egendefinerte rapporter som skal vises i denne kontrollen.</span><span class="sxs-lookup"><span data-stu-id="69548-106">You can create custom reports to display in this control.</span></span> <span data-ttu-id="69548-107">Det finnes imidlertid noen få regler du må følge, for å sikre at rapporter fungerer som forventet.</span><span class="sxs-lookup"><span data-stu-id="69548-107">However, there are a few rules to follow to ensure that reports work as expected.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="69548-108">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="69548-108">Prerequisites</span></span>

- <span data-ttu-id="69548-109">En Power BI-konto.</span><span class="sxs-lookup"><span data-stu-id="69548-109">A Power BI account.</span></span>
- <span data-ttu-id="69548-110">Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="69548-110">Power BI Desktop.</span></span>

<span data-ttu-id="69548-111">Hvis du vil ha mer informasjon om hvordan du kommer i gang, kan du se [Bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde for Power BI](across-how-use-financials-data-source-powerbi.md).</span><span class="sxs-lookup"><span data-stu-id="69548-111">For more information about getting started, see [Using [!INCLUDE[d365fin](includes/d365fin_md.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).</span></span>

## <a name="defining-the-report-data-set"></a><span data-ttu-id="69548-112">Definere rapportdatasettet</span><span class="sxs-lookup"><span data-stu-id="69548-112">Defining the report data set</span></span>

<span data-ttu-id="69548-113">Angi datakilden som inneholder dataene som er knyttet til listen.</span><span class="sxs-lookup"><span data-stu-id="69548-113">Specify the data source that contains the data related to the list.</span></span> <span data-ttu-id="69548-114">Hvis du for eksempel vil opprette en rapport for Salgsoversikt, sikrer du at datasettet inneholder informasjon knyttet til salg.</span><span class="sxs-lookup"><span data-stu-id="69548-114">For example, to create a report for the Sales List, ensure the data set contains information related to sales.</span></span>  

## <a name="defining-the-report-filter"></a><span data-ttu-id="69548-115">Definere rapportfilteret</span><span class="sxs-lookup"><span data-stu-id="69548-115">Defining the report filter</span></span>

<span data-ttu-id="69548-116">For å oppdatere dataene til den valgte posten i listen legger du til et filter i rapporten.</span><span class="sxs-lookup"><span data-stu-id="69548-116">To make the data update to the selected record in the list, you add a filter to the report.</span></span> <span data-ttu-id="69548-117">Filteret må inneholde et felt for datakilden som brukes som *primærnøkkelen*.</span><span class="sxs-lookup"><span data-stu-id="69548-117">The filter must include a field of the data source that's used as the *primary key*.</span></span> <span data-ttu-id="69548-118">I de fleste tilfeller er primærnøkkelen for en liste **Nr.**</span><span class="sxs-lookup"><span data-stu-id="69548-118">In most cases, the primary key for a list is the **No.**</span></span> <span data-ttu-id="69548-119">-feltet.</span><span class="sxs-lookup"><span data-stu-id="69548-119">field.</span></span>

<span data-ttu-id="69548-120">Hvis du vil definere et filter for rapporten, velger du primærnøkkelen fra listen over tilgjengelige felt, og deretter dra og slippe feltet i **Rapportfilter**-delen.</span><span class="sxs-lookup"><span data-stu-id="69548-120">To define a filter for the report, select the primary key from the list of available fields, and then drag and drop that field into the **Report Filter** section.</span></span> <span data-ttu-id="69548-121">Filteret må være et grunnleggende rapportfilter.</span><span class="sxs-lookup"><span data-stu-id="69548-121">The filter must be basic report filter.</span></span> <span data-ttu-id="69548-122">Det kan ikke være en side, en visualisering eller et avansert filter.</span><span class="sxs-lookup"><span data-stu-id="69548-122">It can't be page, visual, or advanced filter.</span></span> 

![Angi rapportfilteret for Salgsfaktura-aktivitetsrapporten](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter.png)

## <a name="setting-the-report-size-and-color"></a><span data-ttu-id="69548-124">Angi rapportstørrelsen og -fargen</span><span class="sxs-lookup"><span data-stu-id="69548-124">Setting the report size and color</span></span>

<span data-ttu-id="69548-125">Størrelsen på rapporten må settes til 325 x 310 piksler.</span><span class="sxs-lookup"><span data-stu-id="69548-125">The size of the report must be set to 325 pixels by 310 pixels.</span></span> <span data-ttu-id="69548-126">Denne størrelsen gir riktig skalering av rapporten på den ledige plassen for Power BI-faktabokskontrollen i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="69548-126">This size provides the proper scaling of the report in the available space of the Power BI FactBox control in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="69548-127">Hvis du vil definere størrelsen på rapporten, fokusere utenfor oppsettsområdet til rapporten, og velg deretter malerrulleikonet.</span><span class="sxs-lookup"><span data-stu-id="69548-127">To define the size of the report, place focus outside of the report layout area, and then choose the paint roller icon.</span></span>

![Angi bredden og høyden på Salgsfaktura-aktivitetsrapporten](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing.png)

<span data-ttu-id="69548-129">Du kan endre bredden og høyden på rapporten ved å velge **Egendefinert** i **Type**-feltet.</span><span class="sxs-lookup"><span data-stu-id="69548-129">You can change the width and height of the report by choosing **Custom** in the **Type** field.</span></span>

<span data-ttu-id="69548-130">Hvis du vil at bakgrunnen i rapporten skal blandes med bakgrunnsfargen til Power BI-faktabokskontrollen, setter du rapportbakgrunnsfargen til *#FFFFFF*.</span><span class="sxs-lookup"><span data-stu-id="69548-130">If you want the background of the report to blend with the background color of the Power BI FactBox control, set report background color to *#FFFFFF*.</span></span> 

## <a name="using-reports-with-multiple-pages"></a><span data-ttu-id="69548-131">Bruke rapporter med flere sider</span><span class="sxs-lookup"><span data-stu-id="69548-131">Using reports with multiple pages</span></span>

<span data-ttu-id="69548-132">Du kan opprette én enkelt rapport med flere sider med Power BI.</span><span class="sxs-lookup"><span data-stu-id="69548-132">With Power BI, you can create a single report with multiple pages.</span></span> <span data-ttu-id="69548-133">Når det gjelder rapporter som skal vises på listesider, anbefaler vi ikke at de har flere enn én side.</span><span class="sxs-lookup"><span data-stu-id="69548-133">However, for reports that will display with list pages, we don't recommend that they have more than one page.</span></span> <span data-ttu-id="69548-134">Power BI-faktaboksen viser bare den første siden i rapporten.</span><span class="sxs-lookup"><span data-stu-id="69548-134">The Power BI FactBox will only show the first page of your report.</span></span>

## <a name="naming-the-report"></a><span data-ttu-id="69548-135">Gi navn til rapporten</span><span class="sxs-lookup"><span data-stu-id="69548-135">Naming the report</span></span>

<span data-ttu-id="69548-136">Gi rapporten et navn som inneholder navnet på listesiden som er knyttet til rapporten.</span><span class="sxs-lookup"><span data-stu-id="69548-136">Give the report a name that contains the name of the list page associated with the report.</span></span> <span data-ttu-id="69548-137">Hvis rapporten for eksempel er for listesiden **Leverandør**, tar du med ordet *leverandør* et sted i navnet.</span><span class="sxs-lookup"><span data-stu-id="69548-137">For example, if the report is for the **Vendor** list page, include the word *vendor* somewhere in the name.</span></span>  

<span data-ttu-id="69548-138">Denne navnekonvensjonen er ikke et krav.</span><span class="sxs-lookup"><span data-stu-id="69548-138">This naming convention isn't a requirement.</span></span> <span data-ttu-id="69548-139">Den gjør det imidlertid raskere å velge rapporter i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="69548-139">However, it makes selecting reports in [!INCLUDE[d365fin](includes/d365fin_md.md)] quicker.</span></span> <span data-ttu-id="69548-140">Når siden for valg av rapport åpnes fra en listeside, filtreres den automatisk basert på sidenavnet.</span><span class="sxs-lookup"><span data-stu-id="69548-140">When the report selection page opens from a list page, it's automatically filtered based on the page name.</span></span> <span data-ttu-id="69548-141">Denne filtreringen utføres for å begrense antall rapporter som vises.</span><span class="sxs-lookup"><span data-stu-id="69548-141">This filtering is done to limit the reports that are displayed.</span></span> <span data-ttu-id="69548-142">Brukere kan fjerne filteret for å få en fullstendig liste over rapporter som er tilgjengelige i Power BI.</span><span class="sxs-lookup"><span data-stu-id="69548-142">Users can clear the filter to get a full list of reports available in Power BI.</span></span>  

## <a name="fixing-problems"></a><span data-ttu-id="69548-143">Løse problemer</span><span class="sxs-lookup"><span data-stu-id="69548-143">Fixing problems</span></span>

<span data-ttu-id="69548-144">Denne delen inneholder en løsning for de vanligste problemene som kan oppstå når du oppretter en Power BI-rapport.</span><span class="sxs-lookup"><span data-stu-id="69548-144">This section provides a workaround for the most typical problems that can occur when you create the Power BI report.</span></span>  

#### <a name="you-cant-see-a-report-on-the-select-report-page"></a><span data-ttu-id="69548-145">Det er en rapport som ikke vises på Velg rapport-siden</span><span class="sxs-lookup"><span data-stu-id="69548-145">You can't see a report on the Select Report page</span></span>

<span data-ttu-id="69548-146">Dette skjer sannsynligvis fordi navnet på rapporten ikke inneholder navnet på listesiden.</span><span class="sxs-lookup"><span data-stu-id="69548-146">It's probably because the report's name doesn't contain the name of the list page.</span></span> <span data-ttu-id="69548-147">Fjern filteret for å få en fullstendig liste over tilgjengelige Power BI-rapporter.</span><span class="sxs-lookup"><span data-stu-id="69548-147">Clear the filter to get a full list of Power BI reports available.</span></span>  

#### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a><span data-ttu-id="69548-148">Rapporten er lastet inn, men tom, ikke filtrert eller filtrert feil</span><span class="sxs-lookup"><span data-stu-id="69548-148">Report is loaded but blank, not filtered or filtered incorrectly</span></span>

<span data-ttu-id="69548-149">Kontroller at rapportfilteret inneholder riktig primærnøkkel.</span><span class="sxs-lookup"><span data-stu-id="69548-149">Verify that the report filter contains the right primary key.</span></span> <span data-ttu-id="69548-150">I de fleste tilfeller er dette **Nr.**-feltet,</span><span class="sxs-lookup"><span data-stu-id="69548-150">In most cases, this field is the **No.**</span></span> <span data-ttu-id="69548-151">men i **Finanspost**-tabellen, for eksempel, må du bruke **Løpenr.**-feltet.</span><span class="sxs-lookup"><span data-stu-id="69548-151">field, but in the **G/L Entry** table, for example, you must use the **Entry No.** field.</span></span>

#### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a><span data-ttu-id="69548-152">Rapporten er lastet inn, men den viser en side du ikke forventet</span><span class="sxs-lookup"><span data-stu-id="69548-152">Report is loaded, but it shows a page you didn't expect</span></span>

<span data-ttu-id="69548-153">Kontroller at siden du vil vise, er den første siden i rapporten.</span><span class="sxs-lookup"><span data-stu-id="69548-153">Verify that the page you want displayed is the first page in your report.</span></span>  

#### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a><span data-ttu-id="69548-154">Rapporten vises med en uønsket grå kantlinje, eller den er for liten eller for stor</span><span class="sxs-lookup"><span data-stu-id="69548-154">Report appears with an unwanted gray boarder, or it's too small or too large</span></span>

<span data-ttu-id="69548-155">Kontroller at størrelsen på rapporten er satt til 325 x 310 piksler.</span><span class="sxs-lookup"><span data-stu-id="69548-155">Verify that the report size is set to 325 pixels x 310 pixels.</span></span> <span data-ttu-id="69548-156">Lagre rapporten, og deretter oppdater listesiden.</span><span class="sxs-lookup"><span data-stu-id="69548-156">Save the report, and then refresh the list page.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="69548-157">Se relatert opplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="69548-157">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="69548-158">Se også</span><span class="sxs-lookup"><span data-stu-id="69548-158">See Also</span></span>

[<span data-ttu-id="69548-159">Aktivere forretningsdata for Power BI</span><span class="sxs-lookup"><span data-stu-id="69548-159">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
<span data-ttu-id="69548-160">[Bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] som en Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="69548-160">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
[<span data-ttu-id="69548-161">Komme i gang</span><span class="sxs-lookup"><span data-stu-id="69548-161">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="69548-162">[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="69548-162">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="69548-163">Finans</span><span class="sxs-lookup"><span data-stu-id="69548-163">Finance</span></span>](finance.md)  
