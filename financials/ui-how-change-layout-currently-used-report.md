---
title: "Endre utseendet på en rapport ved å velge et annet oppsett | Microsoft-dokumentasjon"
description: "Du kan bruke ulike oppsett for en rapport og bytte mellom oppsett for å endre utseendet på den."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: c9eb0f1270a431c0996bffdd610cdebeaf85c216
ms.openlocfilehash: 54cc709845a79f33034ced2e720948733216cc04
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-change-which-layout-is-currently-used-on-a-report"></a><span data-ttu-id="34a01-103">Endre gjeldende oppsett som skal brukes i en rapport</span><span class="sxs-lookup"><span data-stu-id="34a01-103">How to: Change Which Layout is Currently Used on a Report</span></span>
<span data-ttu-id="34a01-104">En rapport kan defineres med flere rapportoppsett, som du deretter kan bytte mellom etter behov.</span><span class="sxs-lookup"><span data-stu-id="34a01-104">A report can be set up with more than one report layout, which you can then switch among as needed.</span></span>

<span data-ttu-id="34a01-105">Avhengig av oppsettene som er tilgjengelige for en rapport, kan du velge om du vil bruke et innebygd RDLC-rapportoppsett, et innebygd Word-rapportoppsett eller et egendefinert oppsett.</span><span class="sxs-lookup"><span data-stu-id="34a01-105">Depending on the layouts that are available for a report, you can choose to use a built-in RDLC report layout, a built-in Word report layout, or a custom layout.</span></span> <span data-ttu-id="34a01-106">Hvis du vil ha mer informasjon om RDLC- og Word-rapportoppsett, innebygde og egendefinerte oppsett og mer, kan du se [Håndtere rapportoppsett](ui-manage-report-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="34a01-106">For more information about RDLC and Word report layouts, built-in and custom layouts, and more, see [Manage Report Layouts](ui-manage-report-layouts.md).</span></span>

## <a name="to-change-the-layout-that-is-used-on-a-report"></a><span data-ttu-id="34a01-107">Slik endrer du oppsettet som brukes i en rapport</span><span class="sxs-lookup"><span data-stu-id="34a01-107">To change the layout that is used on a report</span></span>
1. <span data-ttu-id="34a01-108">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Search for Page or Report icon"), angi **Rapportoppsettsvalg**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="34a01-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Layout Selection**, and then choose the related link.</span></span>  
   <span data-ttu-id="34a01-109">Vinduet **Rapportoppsettsvalg** viser alle rapportene som er tilgjengelige for selskapet som er angitt i feltet Selskap øverst i vinduet.</span><span class="sxs-lookup"><span data-stu-id="34a01-109">The **Report Layout Selection** window lists all the reports that are available for the company that is specified in the Company field at the top of the window.</span></span> <span data-ttu-id="34a01-110">Feltet Valgt oppsett angir oppsettet som brukes i rapporten for øyeblikket.</span><span class="sxs-lookup"><span data-stu-id="34a01-110">The Selected Layout field specifies the layout that is currently used on the report.</span></span>
2. <span data-ttu-id="34a01-111">Angi selskapet som inkluderer rapporten, i **Selskap**-feltet øverst i vinduet.</span><span class="sxs-lookup"><span data-stu-id="34a01-111">Set the **Company** field at the top of the window to the company that includes the report.</span></span>
3. <span data-ttu-id="34a01-112">Hvis du vil endre oppsettet som brukes av en rapport, angir du ett av følgende alternativer for feltet **Valgt oppsett** i raden for rapporten i listen:</span><span class="sxs-lookup"><span data-stu-id="34a01-112">To change the layout that is used by a report, in the row for the report in the list, set the **Selected Layout** field to one of the following options:</span></span>
   * <span data-ttu-id="34a01-113">RDLC (innebygd): Bruker det innebygde RDLC-rapportoppsettet i rapporten.</span><span class="sxs-lookup"><span data-stu-id="34a01-113">RDLC (built-in), uses the built-in RDLC report layout on the report.</span></span>
   * <span data-ttu-id="34a01-114">Word (innebygd): Bruker det innebygde Word-rapportoppsettet i rapporten.</span><span class="sxs-lookup"><span data-stu-id="34a01-114">Word (built-in), uses the built-in Word report layout on the report.</span></span>
   * <span data-ttu-id="34a01-115">Egendefinert: Bruker et egendefinert oppsett i rapporten.</span><span class="sxs-lookup"><span data-stu-id="34a01-115">Custom, uses a custom layout on the report.</span></span>  
     <span data-ttu-id="34a01-116">Du kan se hvilke egendefinerte oppsett som er tilgjengelige for rapporten, i faktaboksen Rapportoppsettsdel.</span><span class="sxs-lookup"><span data-stu-id="34a01-116">You can see which custom layouts are available for the report in the Report Layouts Part FactBox.</span></span> <span data-ttu-id="34a01-117">Hvis det ikke finnes noen egendefinerte oppsett for rapporten, må du først opprette et.</span><span class="sxs-lookup"><span data-stu-id="34a01-117">If there are no custom layouts for the report, then you will have to create one first.</span></span> <span data-ttu-id="34a01-118">Hvis du velger dette alternativet, går du til neste fremgangsmåte for å angi det egendefinerte oppsettet du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="34a01-118">If you choose this option, go to the next procedure to specify the custom layout that you want to use.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="34a01-119">Hvis du velger **RDLC (innebygd)** eller **Word (innebygd)** og får en feilmelding om at rapporten ikke har et oppsett for den angitte typen, må du velge et annet oppsettalternativ eller opprette et egendefinert rapportoppsett av typen du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="34a01-119">If you choose **RDLC (built-in)** or **Word (built-in)** and you get an error message that the report does not have a layout of the specified type, then you must choose another layout option or create a custom report layout of the type that you want to use.</span></span>

<span data-ttu-id="34a01-120">Hvis du valgte et innebygd RDLC- eller Word-rapportoppsett, kreves ingen ytterligere handling, og oppsettet brukes neste gang rapporten kjøres.</span><span class="sxs-lookup"><span data-stu-id="34a01-120">If you selected a built-in RDLC or Word report layout, then no further action is required and the layout will be used the next time the report is run.</span></span>

## <a name="to-specify-a-custom-layout-on-a-report"></a><span data-ttu-id="34a01-121">Angi et egendefinert oppsett i en rapport</span><span class="sxs-lookup"><span data-stu-id="34a01-121">To specify a custom layout on a report</span></span>
1. <span data-ttu-id="34a01-122">Du angir hvilket egendefinert oppsett som skal brukes i rapporten, fra vinduet **Egendefinerte rapportoppsett**.</span><span class="sxs-lookup"><span data-stu-id="34a01-122">You specify which custom layout to use on the report from the **Custom Report Layouts** window.</span></span> <span data-ttu-id="34a01-123">Hvis vinduet **Egendefinerte rapportoppsett** ikke er åpent, velger du oppslagsknappen i feltet **Beskrivelse av rapportoppsett**.</span><span class="sxs-lookup"><span data-stu-id="34a01-123">If the **Custom Report Layouts** window is not open, then in the **Report Layout Description** field, choose the lookup button.</span></span>
2. <span data-ttu-id="34a01-124">Merk raden for det egendefinerte oppsettet du vil bruke, i vinduet **Egendefinerte rapportoppsett**, og lukk deretter vinduet.</span><span class="sxs-lookup"><span data-stu-id="34a01-124">In the **Custom Report Layouts** window, select the row for custom layout that you want to use, and then close the window.</span></span>

<span data-ttu-id="34a01-125">Du går tilbake vinduet **Egendefinerte rapportoppsett**.</span><span class="sxs-lookup"><span data-stu-id="34a01-125">You return to the **Report Layout Selection** window.</span></span> <span data-ttu-id="34a01-126">Navnet på det valgte egendefinerte oppsettet vises i feltet **Beskrivelse av egendefinert oppsett**.</span><span class="sxs-lookup"><span data-stu-id="34a01-126">The name of the selected custom layout displays in the **Custom Layout Description** field.</span></span> <span data-ttu-id="34a01-127">Det egendefinerte oppsettet brukes neste gang du kjører rapporten.</span><span class="sxs-lookup"><span data-stu-id="34a01-127">The custom layout will be used the next time that you run the report.</span></span>

## <a name="see-also"></a><span data-ttu-id="34a01-128">Se også</span><span class="sxs-lookup"><span data-stu-id="34a01-128">See Also</span></span>
[<span data-ttu-id="34a01-129">Håndtere rapportoppsett</span><span class="sxs-lookup"><span data-stu-id="34a01-129">Managing Report Layouts</span></span>](ui-manage-report-layouts.md)  
<span data-ttu-id="34a01-130">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="34a01-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

