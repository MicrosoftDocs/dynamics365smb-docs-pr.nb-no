---
title: Håndtere ansattes fravær | Microsoft-dokumentasjon
description: Beskriver hvordan du kan registrere ansattes fravær og analysere statistikk.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 89f164207b78a9b1845ed7add0b6dea7c4b6efbc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782141"
---
# <a name="manage-employee-absence"></a><span data-ttu-id="cd57b-103">Håndtere ansattes fravær</span><span class="sxs-lookup"><span data-stu-id="cd57b-103">Manage Employee Absence</span></span>
<span data-ttu-id="cd57b-104">For å kunne håndtere fraværet til en ansatt må du registrere fraværet på siden **Fraværsregistrering**.</span><span class="sxs-lookup"><span data-stu-id="cd57b-104">To manage an employee's absence, you must record the absence on the **Absence Registration** page.</span></span> <span data-ttu-id="cd57b-105">Det kan deretter vises på forskjellige måter for analyse og rapportering.</span><span class="sxs-lookup"><span data-stu-id="cd57b-105">It can then be viewed in different ways for analysis and reporting needs.</span></span>

<span data-ttu-id="cd57b-106">Du kan vise ansattes fravær på to forskjellige sider:</span><span class="sxs-lookup"><span data-stu-id="cd57b-106">You can view employee absence in two different pages:</span></span>

* <span data-ttu-id="cd57b-107">På siden **Fraværsregistrering** der du registrerer alle ansattes fravær med en linje for hvert fravær.</span><span class="sxs-lookup"><span data-stu-id="cd57b-107">The **Absence Registration** page, where you register all employee absences with a line for each absence.</span></span>
* <span data-ttu-id="cd57b-108">På siden **Ansattes fravær** der fraværene for bare én ansatt vises.</span><span class="sxs-lookup"><span data-stu-id="cd57b-108">The **Employee Absences** page, where the absences for one employee only is shown.</span></span> <span data-ttu-id="cd57b-109">Dette er informasjonen du registrerte på siden **Fraværsregistrering**, filtrert etter den bestemte ansatte.</span><span class="sxs-lookup"><span data-stu-id="cd57b-109">This is the information that you entered on the **Absence Registration** page, filtered by the particular employee.</span></span>

<span data-ttu-id="cd57b-110">Hvis du skal ha nytte av statistikken, bør du alltid bruke samme enhet (time eller dag) når du registrerer fraværet til de ansatte.</span><span class="sxs-lookup"><span data-stu-id="cd57b-110">To obtain meaningful statistics, you should always use the same unit of measure (hour or day) when registering employee absences.</span></span>

## <a name="to-register-employee-absence"></a><span data-ttu-id="cd57b-111">Slik registrerer du ansattes fravær</span><span class="sxs-lookup"><span data-stu-id="cd57b-111">To register employee absence</span></span>
<span data-ttu-id="cd57b-112">Du kan registrere fraværet daglig eller etter et annet intervall som oppfyller behovene i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="cd57b-112">You can register employee absences on a daily basis or at some other interval that meets your organizational needs.</span></span>

1. <span data-ttu-id="cd57b-113">I øvre høyre hjørne velger du ikonet **Søk etter side eller rapport**, angir **Fraværsregistrering** og velger deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="cd57b-113">In the top right corner, choose the **Search for Page or Report** icon, enter **Absence Registration**, and then choose the related link.</span></span>
2. <span data-ttu-id="cd57b-114">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cd57b-114">Choose the **New** action.</span></span>
3. <span data-ttu-id="cd57b-115">Fyll ut en linje for hvert ansattfravær du vil registrere.</span><span class="sxs-lookup"><span data-stu-id="cd57b-115">Fill in a line for each employee absence you want to register.</span></span>
4. <span data-ttu-id="cd57b-116">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="cd57b-116">Close the page.</span></span>

    > [!Tip]
    > <span data-ttu-id="cd57b-117">Hvis du skal ha nytte av statistikken, må du alltid bruke samme enhet, time eller dag, når du registrerer fraværet til de ansatte.</span><span class="sxs-lookup"><span data-stu-id="cd57b-117">To obtain meaningful statistics, always use the same unit of measure, hour or day, when registering employee absences.</span></span>

## <a name="to-view-an-individual-employees-absence"></a><span data-ttu-id="cd57b-118">Slik viser du fraværet til én ansatt</span><span class="sxs-lookup"><span data-stu-id="cd57b-118">To view an individual employee's absence</span></span>
1. <span data-ttu-id="cd57b-119">I øvre høyre hjørne velger du ikonet **Søk etter side eller rapport**, angir **Ansatte** og velger deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="cd57b-119">In the top right corner, choose the **Search for Page or Report** icon, enter **Employees**, and then choose the related link.</span></span>
2. <span data-ttu-id="cd57b-120">Velg den aktuelle ansatte, og velg deretter handlingen **Fravær**.</span><span class="sxs-lookup"><span data-stu-id="cd57b-120">Select the relevant employee, and then choose the **Absences** action.</span></span>

    <span data-ttu-id="cd57b-121">Siden **Ansattes fravær** åpnes og viser samlet fravær og når fraværet begynte og sluttet.</span><span class="sxs-lookup"><span data-stu-id="cd57b-121">The **Employee Absences** page opens showing all the absences and the date on which they started and ended.</span></span>

## <a name="to-view-an-employees-absence-by-categories"></a><span data-ttu-id="cd57b-122">Slik viser du fraværet til en ansatt etter kategorier</span><span class="sxs-lookup"><span data-stu-id="cd57b-122">To view an employee's absence by categories</span></span>
1. <span data-ttu-id="cd57b-123">I øvre høyre hjørne velger du ikonet **Søk etter side eller rapport**, angir **Ansatte** og velger deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="cd57b-123">In the top right corner, choose the **Search for Page or Report** icon, enter **Employees**, and then choose the related link.</span></span>
2. <span data-ttu-id="cd57b-124">Velg den aktuelle ansatte, og velg deretter handlingen **Fravær per kategori**.</span><span class="sxs-lookup"><span data-stu-id="cd57b-124">Select the relevant employee, and then choose the **Absences by Categories** action.</span></span>
3. <span data-ttu-id="cd57b-125">På siden **Ansattes fravær per kategori** fyller du ut filterfeltene etter behov, og deretter velger du handlingen **Vis matrise**.</span><span class="sxs-lookup"><span data-stu-id="cd57b-125">On the **Empl. Absences by categories** page, fill in the filter fields as necessary, and then choose the **Show Matrix** action.</span></span>

    <span data-ttu-id="cd57b-126">Siden **Ansattes fravær per kat. - matrise** åpnes og viser alt fravær, inndelt etter fraværsårsak.</span><span class="sxs-lookup"><span data-stu-id="cd57b-126">The **Empl. Absences by Cat. Matrix** page opens showing all absences, broken down by causes of absence.</span></span>

## <a name="to-view-all-employee-absences-by-category"></a><span data-ttu-id="cd57b-127">Slik viser du alt ansattfravær etter kategori:</span><span class="sxs-lookup"><span data-stu-id="cd57b-127">To view all employee absences by category</span></span>
1. <span data-ttu-id="cd57b-128">I øvre høyre hjørne velger du ikonet **Søk etter side eller rapport**, angir **Fraværsregistrering** og velger deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="cd57b-128">In the top right corner, choose the **Search for Page or Report** icon, enter **Absence Registration**, and then choose the related link.</span></span>
2. <span data-ttu-id="cd57b-129">På siden **Fraværsregistrering** velger handlingen du **Oversikt per kategori**.</span><span class="sxs-lookup"><span data-stu-id="cd57b-129">On the **Absence Registration** page, choose the **Overview by Categories** action.</span></span>
3. <span data-ttu-id="cd57b-130">På siden **Fravær per kategori - oversikt** angir du et filter i **Filter - ansattnr.**, slik at du kan vise fraværet til en bestemt ansatt eller en definert gruppe av ansatte.</span><span class="sxs-lookup"><span data-stu-id="cd57b-130">On the **Absence Overview by Categories** page, set a filter in the **Employee No. Filter** field to view employee absences for individual or a defined group of employees.</span></span>
4. <span data-ttu-id="cd57b-131">Velg handlingen **Vis matrise**.</span><span class="sxs-lookup"><span data-stu-id="cd57b-131">Choose the **Show Matrix** action.</span></span>

    <span data-ttu-id="cd57b-132">Siden **Matrise for fraværsoversikt etter kategorier** åpnes og viser fraværet til alle de ansatte, inndelt etter ulike fraværsårsaker.</span><span class="sxs-lookup"><span data-stu-id="cd57b-132">The **Absence Overview by Categories Matrix** page opens showing all employees’ absences broken down by the various causes of absence.</span></span>

## <a name="to-view-all-employee-absences-by-period"></a><span data-ttu-id="cd57b-133">Slik viser du alt ansattfravær etter periode:</span><span class="sxs-lookup"><span data-stu-id="cd57b-133">To view all employee absences by period</span></span>
1. <span data-ttu-id="cd57b-134">I øvre høyre hjørne velger du ikonet **Søk etter side eller rapport**, angir **Fraværsregistrering** og velger deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="cd57b-134">In the top right corner, choose the **Search for Page or Report** icon, enter **Absence Registration**, and then choose the related link.</span></span>
   <span data-ttu-id="cd57b-135">På siden **Fraværsregistrering** velger handlingen du **Oversikt per periode**.</span><span class="sxs-lookup"><span data-stu-id="cd57b-135">On the **Absence Registration** page, choose the **Overview by Periods** action.</span></span>
2. <span data-ttu-id="cd57b-136">På siden **Fraværsovers. per periode** angir du et filter i feltet **Filter årsak til fravær**, slik at du kan vise ansattfravær med bestemte årsaker.</span><span class="sxs-lookup"><span data-stu-id="cd57b-136">On the **Absence Overview by Periods** page, set a filter in the **Cause of Absence Filter** field to view employee absences for specified causes of absence.</span></span>
3. <span data-ttu-id="cd57b-137">Velg handlingen **Vis matrise**.</span><span class="sxs-lookup"><span data-stu-id="cd57b-137">Choose the **Show Matrix** action.</span></span>

    <span data-ttu-id="cd57b-138">Siden **Fraværsovers. per periode - matrise** åpnes og viser fraværet til ansatte, inndelt etter perioder.</span><span class="sxs-lookup"><span data-stu-id="cd57b-138">The **Abs. Overview by Periods Matrix** page opens showing employee absences broken down by periods.</span></span>

## <a name="see-also"></a><span data-ttu-id="cd57b-139">Se også</span><span class="sxs-lookup"><span data-stu-id="cd57b-139">See Also</span></span>
[<span data-ttu-id="cd57b-140">Administrere personale</span><span class="sxs-lookup"><span data-stu-id="cd57b-140">Manage Human Resources</span></span>](hr-manage-human-resources.md)  
[<span data-ttu-id="cd57b-141">Finans</span><span class="sxs-lookup"><span data-stu-id="cd57b-141">Finance</span></span>](finance.md)  
<span data-ttu-id="cd57b-142">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cd57b-142">[Working With [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="cd57b-143">Endre hvilke funksjoner som vises</span><span class="sxs-lookup"><span data-stu-id="cd57b-143">Change Which Features are Displayed</span></span>](ui-experiences.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]