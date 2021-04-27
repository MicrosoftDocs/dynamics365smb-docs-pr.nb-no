---
title: Vise egendefinerte Power BI-rapporter for Business Central-data | Microsoft Docs
description: Du kan bruke Power BI-rapporter til å få ekstra innsikt i data i lister.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: a600b24e16172134d4f8e78cf47efa4e262cac09
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777519"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prod_short"></a><span data-ttu-id="db1d9-103">Opprette Power BI-rapporter for å vise listedata i [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="db1d9-103">Creating Power BI Reports for Displaying List Data in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

[!INCLUDE[prod_long](includes/prod_long.md)] <span data-ttu-id="db1d9-104">inkluderer et kontrollelement for en Power BI-faktaboks på mange viktige listesider.</span><span class="sxs-lookup"><span data-stu-id="db1d9-104">includes a Power BI FactBox control element on many key list pages.</span></span> <span data-ttu-id="db1d9-105">Formålet med denne faktaboksen er å vise Power BI-rapporter som er knyttet til poster i listene, og som gir ekstra innsikt i dataene.</span><span class="sxs-lookup"><span data-stu-id="db1d9-105">The purpose of this FactBox is to display Power BI reports that are related to records in the lists, providing extra insight into the data.</span></span> <span data-ttu-id="db1d9-106">Poenget er at etter hvert som du flytter mellom radene i listen, oppdateres og filtreres rapporten for den valgte posten.</span><span class="sxs-lookup"><span data-stu-id="db1d9-106">The idea is that as you move between rows in the list, the report is updated and filtered for the selected entry.</span></span>

[!INCLUDE[prod_long](includes/prod_long.md)] <span data-ttu-id="db1d9-107">leveres med noen av disse rapportene.</span><span class="sxs-lookup"><span data-stu-id="db1d9-107">comes ready with some of these reports.</span></span> <span data-ttu-id="db1d9-108">Du kan også opprette egendefinerte rapporter som vises i denne faktaboksen.</span><span class="sxs-lookup"><span data-stu-id="db1d9-108">You can also create your own custom reports that display in this FactBox.</span></span> <span data-ttu-id="db1d9-109">Oppretting av disse rapportene minner om andre rapporter.</span><span class="sxs-lookup"><span data-stu-id="db1d9-109">Creating these reports is similar to other reports.</span></span> <span data-ttu-id="db1d9-110">Det er imidlertid noen få utformingsregler du må følge for å være sikker på at rapportene vises som forventet.</span><span class="sxs-lookup"><span data-stu-id="db1d9-110">But there are a few design rules you'll have to follow to make sure the reports display as expected.</span></span> <span data-ttu-id="db1d9-111">Disse reglene forklares i denne artikkelen.</span><span class="sxs-lookup"><span data-stu-id="db1d9-111">These rules are explained in this article.</span></span>

> [!NOTE]
> <span data-ttu-id="db1d9-112">Hvis du vil ha generell informasjon om hvordan du oppretter og publiserer rapporter for Power BI Business Central, kan du se [Bygge Power BI-rapporter for å vise [!INCLUDE [prod_long](includes/prod_long.md)]-data](across-how-use-financials-data-source-powerbi.md).</span><span class="sxs-lookup"><span data-stu-id="db1d9-112">For general information about creating and publishing Power BI reports for Business Central, see [Building Power BI Reports to Display [!INCLUDE [prod_long](includes/prod_long.md)] Data](across-how-use-financials-data-source-powerbi.md).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="db1d9-113">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="db1d9-113">Prerequisites</span></span>

- <span data-ttu-id="db1d9-114">En Power BI-konto.</span><span class="sxs-lookup"><span data-stu-id="db1d9-114">A Power BI account.</span></span>
- <span data-ttu-id="db1d9-115">Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="db1d9-115">Power BI Desktop.</span></span>

<!-- 
For more information about getting started, see [Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).-->

## <a name="create-a-report-for-a-list-page"></a><span data-ttu-id="db1d9-116">Lage en rapport for en listeside</span><span class="sxs-lookup"><span data-stu-id="db1d9-116">Create a report for a list page</span></span>

1. <span data-ttu-id="db1d9-117">Start Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="db1d9-117">Start Power BI Desktop.</span></span>
2. <span data-ttu-id="db1d9-118">Velg **Hent data**, og begynn med å velge datakilden for rapporten.</span><span class="sxs-lookup"><span data-stu-id="db1d9-118">Select **Get Data**, and start choosing the data source for the report.</span></span>

    <span data-ttu-id="db1d9-119">I dette trinnet angir du listesidene for Business Central som inneholder dataene du vil ha med i rapporten.</span><span class="sxs-lookup"><span data-stu-id="db1d9-119">In this step, you specify the Business Central list pages that contain the data that you want in the report.</span></span> <span data-ttu-id="db1d9-120">Hvis du for eksempel vil opprette en rapport for Salgsoversikt, sikrer du at datasettet inneholder informasjon knyttet til salg.</span><span class="sxs-lookup"><span data-stu-id="db1d9-120">For example, to create a report for the Sales List, ensure the data set contains information related to sales.</span></span>

    <span data-ttu-id="db1d9-121">Hvis du vil ha mer informasjon, følger du instruksjonene under [Legge til [!INCLUDE[prod_short](includes/prod_short.md)] som en datakilde i Power BI Desktop](across-how-use-financials-data-source-powerbi.md#getdata).</span><span class="sxs-lookup"><span data-stu-id="db1d9-121">For more information, follow the instructions [Add [!INCLUDE[prod_short](includes/prod_short.md)] as a data source in Power BI Desktop](across-how-use-financials-data-source-powerbi.md#getdata).</span></span>

3. <span data-ttu-id="db1d9-122">Still inn rapportfilteret.</span><span class="sxs-lookup"><span data-stu-id="db1d9-122">Set the report filter.</span></span>

    <span data-ttu-id="db1d9-123">For å oppdatere dataene til den valgte posten i listen legger du til et filter i rapporten.</span><span class="sxs-lookup"><span data-stu-id="db1d9-123">To make the data update to the selected record in the list, you add a filter to the report.</span></span> <span data-ttu-id="db1d9-124">Filteret må inneholde et felt av datakilden som brukes til entydig identifikasjon av hver post i listen.</span><span class="sxs-lookup"><span data-stu-id="db1d9-124">The filter must include a field of the data source that's used to uniquely identify each record in the list.</span></span> <span data-ttu-id="db1d9-125">I utviklersammenheng er dette feltet *prim'rnøkkelen*.</span><span class="sxs-lookup"><span data-stu-id="db1d9-125">In developer terms, this field is the *primary key*.</span></span> <span data-ttu-id="db1d9-126">I de fleste tilfeller er primærnøkkelen for en liste **Nr.**</span><span class="sxs-lookup"><span data-stu-id="db1d9-126">In most cases, the primary key for a list is the **No.**</span></span> <span data-ttu-id="db1d9-127">-feltet.</span><span class="sxs-lookup"><span data-stu-id="db1d9-127">field.</span></span>

    <span data-ttu-id="db1d9-128">Gjør følgende for å stille inn filteret:</span><span class="sxs-lookup"><span data-stu-id="db1d9-128">To set the filter, do the following steps:</span></span>

    1. <span data-ttu-id="db1d9-129">I **Filtre** velger du primærnøkkelfeltet fra listen over tilgjengelige felt.</span><span class="sxs-lookup"><span data-stu-id="db1d9-129">In the **Filters**, select the primary key field from the list of available fields.</span></span>
    2. <span data-ttu-id="db1d9-130">Dra feltet til ruten **Filtre**, og slipp det i boksen **Filtre på alle sider**.</span><span class="sxs-lookup"><span data-stu-id="db1d9-130">Drag the field to **Filters** pane and drop it in the **Filters on all pages** box.</span></span>
    3. <span data-ttu-id="db1d9-131">Sett verdien for **Filtertype** til **Grunnleggende filtrering**.</span><span class="sxs-lookup"><span data-stu-id="db1d9-131">Set the **Filter type** to **Basic filtering**.</span></span> <span data-ttu-id="db1d9-132">Det kan ikke være en side, en visualisering eller et avansert filter.</span><span class="sxs-lookup"><span data-stu-id="db1d9-132">It can't be page, visual, or advanced filter.</span></span>

    ![Angi rapportfilteret for Salgsfaktura-aktivitetsrapporten](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)
4. <span data-ttu-id="db1d9-134">Utform rapportoppsettet.</span><span class="sxs-lookup"><span data-stu-id="db1d9-134">Design the report layout.</span></span>

    <span data-ttu-id="db1d9-135">Lag oppsettet ved å dra felt og legge til effekter.</span><span class="sxs-lookup"><span data-stu-id="db1d9-135">Create the layout by dragging fields and adding visualizations.</span></span> <span data-ttu-id="db1d9-136">Hvis du vil ha mer informasjon, kan du se [Arbeide med rapportvisning i Power BI Desktop](/power-bi/create-reports/desktop-report-view) i dokumentasjonen for Power BI.</span><span class="sxs-lookup"><span data-stu-id="db1d9-136">For more information, see, [Work with Report view in Power BI Desktop](/power-bi/create-reports/desktop-report-view) in the Power BI documentation.</span></span>

5. <span data-ttu-id="db1d9-137">Se de neste avsnittene om å endre størrelse på rapporten og bruke flere sider.</span><span class="sxs-lookup"><span data-stu-id="db1d9-137">See the next sections about sizing the report and using multiple pages.</span></span>

6. <span data-ttu-id="db1d9-138">Lagre og gi navn til rapporten.</span><span class="sxs-lookup"><span data-stu-id="db1d9-138">Save and name the report.</span></span>

    <span data-ttu-id="db1d9-139">Det er viktig å gi rapporten et navn som inneholder navnet på listesiden som er knyttet til rapporten.</span><span class="sxs-lookup"><span data-stu-id="db1d9-139">It's important to give the report a name that contains the name of the list page associated with the report.</span></span> <span data-ttu-id="db1d9-140">Hvis rapporten for eksempel er for listesiden **Varer**, tar du med ordet *varer* et sted i navnet.</span><span class="sxs-lookup"><span data-stu-id="db1d9-140">For example, if the report is for the **Items** list page, include the word *items* somewhere in the name.</span></span>  

    <span data-ttu-id="db1d9-141">Denne navnekonvensjonen er ikke et krav.</span><span class="sxs-lookup"><span data-stu-id="db1d9-141">This naming convention isn't a requirement.</span></span> <span data-ttu-id="db1d9-142">Den gjør det imidlertid raskere å velge rapporter i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="db1d9-142">However, it makes selecting reports in [!INCLUDE[prod_short](includes/prod_short.md)] quicker.</span></span> <span data-ttu-id="db1d9-143">Når siden for valg av rapport åpnes fra en listeside, filtreres den automatisk basert på sidenavnet.</span><span class="sxs-lookup"><span data-stu-id="db1d9-143">When the report selection page opens from a list page, it's automatically filtered based on the page name.</span></span> <span data-ttu-id="db1d9-144">Denne filtreringen utføres for å begrense antall rapporter som vises.</span><span class="sxs-lookup"><span data-stu-id="db1d9-144">This filtering is done to limit the reports that are displayed.</span></span> <span data-ttu-id="db1d9-145">Brukere kan fjerne filteret for å få en fullstendig liste over rapporter som er tilgjengelige i Power BI.</span><span class="sxs-lookup"><span data-stu-id="db1d9-145">Users can clear the filter to get a full list of reports available in Power BI.</span></span>

7. <span data-ttu-id="db1d9-146">Når du er ferdig, publiserer du rapporten på vanlig måte.</span><span class="sxs-lookup"><span data-stu-id="db1d9-146">When you're done, publish the report as usual.</span></span>

    <span data-ttu-id="db1d9-147">Hvis du vil ha mer informasjon, kan du se [Publisere en rapport](across-how-use-financials-data-source-powerbi.md#publish-reports).</span><span class="sxs-lookup"><span data-stu-id="db1d9-147">For more information, see [Publishing a Report](across-how-use-financials-data-source-powerbi.md#publish-reports).</span></span>

8. <span data-ttu-id="db1d9-148">Test rapporten.</span><span class="sxs-lookup"><span data-stu-id="db1d9-148">Test the report.</span></span>

    <span data-ttu-id="db1d9-149">Når rapportene er publisert på arbeidsområdet, skal det være tilgjengelig fra Power BI-faktaboksen på listesiden i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="db1d9-149">Once the reports been published to your workspace, it should be available from the Power BI FactBox on the list page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

    <span data-ttu-id="db1d9-150">Gjør følgende for å teste det.</span><span class="sxs-lookup"><span data-stu-id="db1d9-150">To test it, do the following steps.</span></span>

    1. <span data-ttu-id="db1d9-151">Åpne [!INCLUDE[prod_short](includes/prod_short.md)] og gå til listesiden.</span><span class="sxs-lookup"><span data-stu-id="db1d9-151">Open [!INCLUDE[prod_short](includes/prod_short.md)] and go to the list page.</span></span>
    2. <span data-ttu-id="db1d9-152">Hvis du ikke ser Power BI-faktaboksen, går du til handlingsfeltet og velger **Handlinger** > **Visning** > **Vis/Skjul Power BI-rapporter**.</span><span class="sxs-lookup"><span data-stu-id="db1d9-152">If you don't see the Power BI FactBox, go the action bar, then select **Actions** > **Display** > **Show/Hide Power BI Reports**.</span></span>
    3. <span data-ttu-id="db1d9-153">I Power BI-faktaboksen velger du **Velg rapporter**, merker av for **Aktiver** for rapporten, og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="db1d9-153">In the Power BI FactBox, select **Select Reports**, select the **Enable** box for the report, then select **OK**.</span></span>

    <span data-ttu-id="db1d9-154">Hvis den er utformet riktig, viser rapporten.</span><span class="sxs-lookup"><span data-stu-id="db1d9-154">If designed correctly, the report displays.</span></span>  

## <a name="set-the-report-size-and-color"></a><span data-ttu-id="db1d9-155">Angi rapportstørrelsen og -fargen</span><span class="sxs-lookup"><span data-stu-id="db1d9-155">Set the report size and color</span></span>

<span data-ttu-id="db1d9-156">Størrelsen på rapporten må settes til 325 x 310 piksler.</span><span class="sxs-lookup"><span data-stu-id="db1d9-156">The size of the report must be set to 325 pixels by 310 pixels.</span></span> <span data-ttu-id="db1d9-157">Denne størrelsen gir riktig skalering av rapporten på den ledige plassen for Power BI-faktabokskontrollen i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="db1d9-157">This size provides the proper scaling of the report in the available space of the Power BI FactBox control in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="db1d9-158">Hvis du vil definere størrelsen på rapporten, fokusere utenfor oppsettsområdet til rapporten, og velg deretter malerrulleikonet.</span><span class="sxs-lookup"><span data-stu-id="db1d9-158">To define the size of the report, place focus outside of the report layout area, and then choose the paint roller icon.</span></span>

![Angi bredden og høyden på Salgsfaktura-aktivitetsrapporten](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

<span data-ttu-id="db1d9-160">Du kan endre bredden og høyden på rapporten ved å velge **Egendefinert** i **Type**-feltet.</span><span class="sxs-lookup"><span data-stu-id="db1d9-160">You can change the width and height of the report by choosing **Custom** in the **Type** field.</span></span>

<span data-ttu-id="db1d9-161">Hvis du vil at bakgrunnen i rapporten skal blandes med bakgrunnsfargen til Power BI-faktabokskontrollen, setter du rapportbakgrunnsfargen til *#FFFFFF* (hvit).</span><span class="sxs-lookup"><span data-stu-id="db1d9-161">If you want the background of the report to blend with the background color of the Power BI FactBox control, set report background color to *#FFFFFF* (white).</span></span> 

> [!TIP]
> <span data-ttu-id="db1d9-162">Bruk [!INCLUDE [prod_short](includes/prod_short.md)]-temafilen til å lage rapporter med de samme farge stilene som [!INCLUDE [prod_short](includes/prod_short.md)]-appene.</span><span class="sxs-lookup"><span data-stu-id="db1d9-162">Use the [!INCLUDE [prod_short](includes/prod_short.md)] theme file to build reports with the same color styling as the [!INCLUDE [prod_short](includes/prod_short.md)] apps.</span></span> <span data-ttu-id="db1d9-163">Hvis du vil ha mer informasjon, kan du se [Bruke [!INCLUDE [prod_short](includes/prod_short.md)]-rapporttemaet](across-how-use-financials-data-source-powerbi.md#theme).</span><span class="sxs-lookup"><span data-stu-id="db1d9-163">For more information, see [Using the [!INCLUDE [prod_short](includes/prod_short.md)] report theme](across-how-use-financials-data-source-powerbi.md#theme).</span></span>

## <a name="reports-with-multiple-pages"></a><span data-ttu-id="db1d9-164">Rapporter med flere sider</span><span class="sxs-lookup"><span data-stu-id="db1d9-164">Reports with multiple pages</span></span>

<span data-ttu-id="db1d9-165">Du kan opprette én enkelt rapport med flere sider med Power BI.</span><span class="sxs-lookup"><span data-stu-id="db1d9-165">With Power BI, you can create a single report with multiple pages.</span></span> <span data-ttu-id="db1d9-166">Når det gjelder rapporter som skal vises på listesider, anbefaler vi ikke at de har flere enn én side.</span><span class="sxs-lookup"><span data-stu-id="db1d9-166">However, for reports that will display with list pages, we don't recommend that they have more than one page.</span></span> <span data-ttu-id="db1d9-167">Power BI-faktaboksen viser bare den første siden i rapporten.</span><span class="sxs-lookup"><span data-stu-id="db1d9-167">The Power BI FactBox will only show the first page of your report.</span></span>

## <a name="fixing-problems"></a><span data-ttu-id="db1d9-168">Løse problemer</span><span class="sxs-lookup"><span data-stu-id="db1d9-168">Fixing problems</span></span>

<span data-ttu-id="db1d9-169">Denne delen inneholder instruksjoner om hvordan du løser problemer som kan oppstå i når du prøver å vise en Power BI-rapport for en listeside i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="db1d9-169">This section provides instructions about how to fix problems that you might run into when trying to view a Power BI report for a list page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

### <a name="you-cant-see-the-power-bi-factbox-on-a-list-page"></a><span data-ttu-id="db1d9-170">Du kan ikke se Power BI-faktaboksen på en listeside</span><span class="sxs-lookup"><span data-stu-id="db1d9-170">You can't see the Power BI FactBox on a list page</span></span>

<span data-ttu-id="db1d9-171">Power BI-faktaboksen er som standard skjult for visning.</span><span class="sxs-lookup"><span data-stu-id="db1d9-171">By default, the Power BI FactBox is hidden from view.</span></span> <span data-ttu-id="db1d9-172">Hvis du vil vise faktaboksen på en side, velger du **Handlinger** > **Visning** > **Vis/Skjul Power BI-rapporter** i handlingsfeltet.</span><span class="sxs-lookup"><span data-stu-id="db1d9-172">To show the FactBox on a page, from the action bar, select **Actions** > **Display** > **Show/Hide Power BI Reports**.</span></span>

### <a name="you-cant-see-the-report-in-the-select-report-pane"></a><span data-ttu-id="db1d9-173">Du kan ikke se rapporten i ruten Velg rapport</span><span class="sxs-lookup"><span data-stu-id="db1d9-173">You can't see the report in the Select Report pane</span></span>

<span data-ttu-id="db1d9-174">Dette skjer sannsynligvis fordi navnet på rapporten ikke inneholder navnet på listesiden som vises.</span><span class="sxs-lookup"><span data-stu-id="db1d9-174">It's probably because the report's name doesn't contain the name of the list page that's being shown.</span></span> <span data-ttu-id="db1d9-175">Fjern filteret for å få en fullstendig liste over tilgjengelige Power BI-rapporter.</span><span class="sxs-lookup"><span data-stu-id="db1d9-175">Clear the filter to get a full list of Power BI reports available.</span></span>  

### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a><span data-ttu-id="db1d9-176">Rapporten er lastet inn, men tom, ikke filtrert eller filtrert feil</span><span class="sxs-lookup"><span data-stu-id="db1d9-176">Report is loaded but blank, not filtered, or filtered incorrectly</span></span>

<span data-ttu-id="db1d9-177">Kontroller at rapportfilteret inneholder riktig primærnøkkel.</span><span class="sxs-lookup"><span data-stu-id="db1d9-177">Verify that the report filter contains the right primary key.</span></span> <span data-ttu-id="db1d9-178">I de fleste tilfeller er dette **Nr.**-feltet,</span><span class="sxs-lookup"><span data-stu-id="db1d9-178">In most cases, this field is the **No.**</span></span> <span data-ttu-id="db1d9-179">men i **Finanspost**-tabellen, for eksempel, må du bruke **Løpenr.**-feltet.</span><span class="sxs-lookup"><span data-stu-id="db1d9-179">field, but in the **G/L Entry** table, for example, you must use the **Entry No.** field.</span></span>

### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a><span data-ttu-id="db1d9-180">Rapporten er lastet inn, men den viser en side du ikke forventet</span><span class="sxs-lookup"><span data-stu-id="db1d9-180">Report is loaded, but it shows a page you didn't expect</span></span>

<span data-ttu-id="db1d9-181">Kontroller at siden du vil vise, er den første siden i rapporten.</span><span class="sxs-lookup"><span data-stu-id="db1d9-181">Verify that the page you want displayed is the first page in your report.</span></span>  

### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a><span data-ttu-id="db1d9-182">Rapporten vises med en uønsket grå kantlinje, eller den er for liten eller for stor</span><span class="sxs-lookup"><span data-stu-id="db1d9-182">Report appears with an unwanted gray boarder, or it's too small or too large</span></span>

<span data-ttu-id="db1d9-183">Kontroller at størrelsen på rapporten er satt til 325 x 310 piksler.</span><span class="sxs-lookup"><span data-stu-id="db1d9-183">Verify that the report size is set to 325 pixels x 310 pixels.</span></span> <span data-ttu-id="db1d9-184">Lagre rapporten, og deretter oppdater listesiden.</span><span class="sxs-lookup"><span data-stu-id="db1d9-184">Save the report, and then refresh the list page.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="db1d9-185">Se relatert opplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="db1d9-185">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="db1d9-186">Se også</span><span class="sxs-lookup"><span data-stu-id="db1d9-186">See Also</span></span>

[<span data-ttu-id="db1d9-187">Aktivere forretningsdata for Power BI</span><span class="sxs-lookup"><span data-stu-id="db1d9-187">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
<span data-ttu-id="db1d9-188">[Bruke [!INCLUDE[prod_short](includes/prod_short.md)] som en Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="db1d9-188">[Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
[<span data-ttu-id="db1d9-189">Bli klar til å gjøre forretninger</span><span class="sxs-lookup"><span data-stu-id="db1d9-189">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
<span data-ttu-id="db1d9-190">[Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="db1d9-190">[Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span></span>  
[<span data-ttu-id="db1d9-191">Finans</span><span class="sxs-lookup"><span data-stu-id="db1d9-191">Finance</span></span>](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]