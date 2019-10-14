---
title: Endre utseendet på en rapport ved å velge et annet oppsett | Microsoft-dokumentasjon
description: Du kan bruke ulike oppsett for en rapport og bytte mellom oppsett for å endre utseendet på den.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 07de4be7bc516cf9f4b802a48dc59293b1992f5f
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315255"
---
# <a name="change-the-current-report-layout"></a><span data-ttu-id="59e46-103">Endre gjeldende rapportoppsett</span><span class="sxs-lookup"><span data-stu-id="59e46-103">Change the Current Report Layout</span></span>
<span data-ttu-id="59e46-104">En rapport kan defineres med flere rapportoppsett, som du deretter kan bytte mellom etter behov.</span><span class="sxs-lookup"><span data-stu-id="59e46-104">A report can be set up with more than one report layout, which you can then switch among as needed.</span></span>

<span data-ttu-id="59e46-105">Avhengig av oppsettene som er tilgjengelige for en rapport, kan du velge om du vil bruke et innebygd RDLC-rapportoppsett, et innebygd Word-rapportoppsett eller et egendefinert oppsett.</span><span class="sxs-lookup"><span data-stu-id="59e46-105">Depending on the layouts that are available for a report, you can choose to use a built-in RDLC report layout, a built-in Word report layout, or a custom layout.</span></span> <span data-ttu-id="59e46-106">Hvis du vil ha mer informasjon om RDLC- og Word-rapportoppsett, innebygde og egendefinerte oppsett og mer, kan du se [Håndtere rapportoppsett](ui-manage-report-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="59e46-106">For more information about RDLC and Word report layouts, built-in and custom layouts, and more, see [Manage Report Layouts](ui-manage-report-layouts.md).</span></span>

> [!TIP]  
> <span data-ttu-id="59e46-107">Dokumentrapporter (ikke oversikter) som bruker et Word-rapportoppsett, er vanligvis raskere enn de som bruker et RDLC-rapportoppsett.</span><span class="sxs-lookup"><span data-stu-id="59e46-107">Document reports (not lists) that use a Word report layout are typically faster than those that use an RDLC report layout.</span></span> <span data-ttu-id="59e46-108">Så hvis du kan velge mellom et Word- eller RDLC-rapportoppsett for en dokumentrapport, bør du bruke Word-rapportoppsettet for best ytelse.</span><span class="sxs-lookup"><span data-stu-id="59e46-108">So if you have the option to choose between a Word or RDLC report layout for a document report, use the Word report layout for the best performance.</span></span>  

## <a name="to-change-the-layout-that-is-used-on-a-report"></a><span data-ttu-id="59e46-109">Slik endrer du oppsettet som brukes i en rapport</span><span class="sxs-lookup"><span data-stu-id="59e46-109">To change the layout that is used on a report</span></span>
1. <span data-ttu-id="59e46-110">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rapportoppsettsvalg**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="59e46-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Layout Selection**, and then choose the related link.</span></span>  
   <span data-ttu-id="59e46-111">Siden **Rapportoppsettsvalg** viser alle rapportene som er tilgjengelige for selskapet som er angitt i feltet Selskap øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="59e46-111">The **Report Layout Selection** page lists all the reports that are available for the company that is specified in the Company field at the top of the page.</span></span> <span data-ttu-id="59e46-112">Feltet Valgt oppsett angir oppsettet som brukes i rapporten for øyeblikket.</span><span class="sxs-lookup"><span data-stu-id="59e46-112">The Selected Layout field specifies the layout that is currently used on the report.</span></span>
2. <span data-ttu-id="59e46-113">Sett feltet **Selskap** øverst på siden til selskapet som inkluderer rapporten.</span><span class="sxs-lookup"><span data-stu-id="59e46-113">Set the **Company** field at the top of the page to the company that includes the report.</span></span>
3. <span data-ttu-id="59e46-114">Hvis du vil endre oppsettet som brukes av en rapport, angir du ett av følgende alternativer for feltet **Valgt oppsett** i raden for rapporten i listen:</span><span class="sxs-lookup"><span data-stu-id="59e46-114">To change the layout that is used by a report, in the row for the report in the list, set the **Selected Layout** field to one of the following options:</span></span>
   * <span data-ttu-id="59e46-115">RDLC (innebygd): Bruker det innebygde RDLC-rapportoppsettet i rapporten.</span><span class="sxs-lookup"><span data-stu-id="59e46-115">RDLC (built-in), uses the built-in RDLC report layout on the report.</span></span>
   * <span data-ttu-id="59e46-116">Word (innebygd): Bruker det innebygde Word-rapportoppsettet i rapporten.</span><span class="sxs-lookup"><span data-stu-id="59e46-116">Word (built-in), uses the built-in Word report layout on the report.</span></span>
   * <span data-ttu-id="59e46-117">Egendefinert: Bruker et egendefinert oppsett i rapporten.</span><span class="sxs-lookup"><span data-stu-id="59e46-117">Custom, uses a custom layout on the report.</span></span>  

<span data-ttu-id="59e46-118">Du kan se hvilke egendefinerte oppsett som er tilgjengelige for rapporten, i faktaboksen **Rapportoppsettsdel**.</span><span class="sxs-lookup"><span data-stu-id="59e46-118">You can see which custom layouts are available for the report in the **Report Layouts Part** FactBox.</span></span> <span data-ttu-id="59e46-119">Hvis det ikke finnes noen egendefinerte oppsett for rapporten, må du først opprette et.</span><span class="sxs-lookup"><span data-stu-id="59e46-119">If there are no custom layouts for the report, then you will have to create one first.</span></span> <span data-ttu-id="59e46-120">Hvis du velger dette alternativet, går du til neste fremgangsmåte for å angi det egendefinerte oppsettet du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="59e46-120">If you choose this option, go to the next procedure to specify the custom layout that you want to use.</span></span>

> [!NOTE]
> <span data-ttu-id="59e46-121">Hvis du velger **RDLC (innebygd)** eller **Word (innebygd)** og får en feilmelding om at rapporten ikke har et oppsett for den angitte typen, må du velge et annet oppsettalternativ eller opprette et egendefinert rapportoppsett av typen du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="59e46-121">If you choose **RDLC (built-in)** or **Word (built-in)** and you get an error message that the report does not have a layout of the specified type, then you must choose another layout option or create a custom report layout of the type that you want to use.</span></span>

<span data-ttu-id="59e46-122">Hvis du valgte et innebygd RDLC- eller Word-rapportoppsett, kreves ingen ytterligere handling, og oppsettet brukes neste gang rapporten kjøres.</span><span class="sxs-lookup"><span data-stu-id="59e46-122">If you selected a built-in RDLC or Word report layout, then no further action is required and the layout will be used the next time the report is run.</span></span>

## <a name="to-specify-a-custom-layout-on-a-report"></a><span data-ttu-id="59e46-123">Angi et egendefinert oppsett i en rapport</span><span class="sxs-lookup"><span data-stu-id="59e46-123">To specify a custom layout on a report</span></span>
1. <span data-ttu-id="59e46-124">Du angir hvilket egendefinert oppsett som skal brukes i rapporten, fra siden **Egendefinerte rapportoppsett**.</span><span class="sxs-lookup"><span data-stu-id="59e46-124">You specify which custom layout to use on the report from the **Custom Report Layouts** page.</span></span> <span data-ttu-id="59e46-125">Hvis siden **Egendefinerte rapportoppsett** ikke er åpen, velger du oppslagsknappen i feltet **Beskrivelse av rapportoppsett**.</span><span class="sxs-lookup"><span data-stu-id="59e46-125">If the **Custom Report Layouts** page is not open, then in the **Report Layout Description** field, choose the lookup button.</span></span>
2. <span data-ttu-id="59e46-126">Merk raden for det egendefinerte oppsettet du vil bruke, på siden **Egendefinerte rapportoppsett**, og lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="59e46-126">On the **Custom Report Layouts** page, select the row for custom layout that you want to use, and then close the page.</span></span>

<span data-ttu-id="59e46-127">Du går tilbake siden **Egendefinerte rapportoppsett**.</span><span class="sxs-lookup"><span data-stu-id="59e46-127">You return to the **Report Layout Selection** page.</span></span> <span data-ttu-id="59e46-128">Navnet på det valgte egendefinerte oppsettet vises i feltet **Beskrivelse av egendefinert oppsett**.</span><span class="sxs-lookup"><span data-stu-id="59e46-128">The name of the selected custom layout displays in the **Custom Layout Description** field.</span></span> <span data-ttu-id="59e46-129">Det egendefinerte oppsettet brukes neste gang du kjører rapporten.</span><span class="sxs-lookup"><span data-stu-id="59e46-129">The custom layout will be used the next time that you run the report.</span></span>

## <a name="see-also"></a><span data-ttu-id="59e46-130">Se også</span><span class="sxs-lookup"><span data-stu-id="59e46-130">See Also</span></span>
[<span data-ttu-id="59e46-131">Håndtere rapportoppsett</span><span class="sxs-lookup"><span data-stu-id="59e46-131">Managing Report Layouts</span></span>](ui-manage-report-layouts.md)  
<span data-ttu-id="59e46-132">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="59e46-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
