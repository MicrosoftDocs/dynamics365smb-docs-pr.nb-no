---
title: Definere aktivavedlikehold | Microsoft-dokumentasjon
description: For å administrere aktivareparasjoner og -service angir du generelle vedlikeholdsopplysninger, koder for typen arbeid og en bokføringskonto for kost.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: b3ecec35e4dc99d330424a009218fad5009ce7d5
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2020
ms.locfileid: "3780238"
---
# <a name="set-up-fixed-asset-maintenance"></a><span data-ttu-id="346f4-103">Definere aktivavedlikehold</span><span class="sxs-lookup"><span data-stu-id="346f4-103">Set Up Fixed Asset Maintenance</span></span>
<span data-ttu-id="346f4-104">For å styre vedlikehold av aktiva, må du først definere noen generelle vedlikeholdsopplysninger, en bokføringskonto for vedlikeholdskostnader og vedlikeholdskoder for typer arbeid, for eksempel rutineservice eller reparasjon.</span><span class="sxs-lookup"><span data-stu-id="346f4-104">To manage fixed asset maintenance, you must first set up some general maintenance information, a posting account for maintenance costs, and maintenance codes for types of work, such as Routine Service or Repair.</span></span>

## <a name="to-set-up-general-maintenance-information"></a><span data-ttu-id="346f4-105">Slik definerer du generelle vedlikeholdsopplysninger:</span><span class="sxs-lookup"><span data-stu-id="346f4-105">To set up general maintenance information</span></span>
<span data-ttu-id="346f4-106">Hvis du definerer vedlikeholdsfeltene, kan du bokføre vedlikeholdsutgifter fra aktivakladden.</span><span class="sxs-lookup"><span data-stu-id="346f4-106">If you set up the fields for maintenance, you can post maintenance expenses from the fixed asset journal.</span></span>

1. <span data-ttu-id="346f4-107">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Aktiva**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="346f4-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="346f4-108">Velg aktivaet du vil definere forsikringsdekning for, og velg deretter handlingen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="346f4-108">Select the fixed asset that you to define insurance coverage for, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="346f4-109">Fyll ut feltene på hurtigfanen **Vedlikehold** etter behov.</span><span class="sxs-lookup"><span data-stu-id="346f4-109">On the **Maintenance** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a><span data-ttu-id="346f4-110">Slik definerer du vedlikeholdskoder</span><span class="sxs-lookup"><span data-stu-id="346f4-110">To set up maintenance codes</span></span>
<span data-ttu-id="346f4-111">Når du bokfører vedlikeholdskostnader fra en finanskladd, fyller du ut feltet **Vedlikeholdskode** for å registrere hva slags vedlikehold som er utført, for eksempel rutineservice eller reparasjon.</span><span class="sxs-lookup"><span data-stu-id="346f4-111">When you post maintenance costs from a general journal, you fill in the **Maintenance Code** field to record what kind of maintenance has been performed, such as routine service or repair.</span></span>

1. <span data-ttu-id="346f4-112">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Vedlikehold**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="346f4-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Maintenance**, and then choose the related link.</span></span>
2. <span data-ttu-id="346f4-113">På **Vedlikehold**-siden definerer du koder for ulike typer vedlikeholdsarbeid.</span><span class="sxs-lookup"><span data-stu-id="346f4-113">On the **Maintenance** page, set up codes for different types of maintenance work.</span></span>

## <a name="to-set-up-maintenance-expense-accounts"></a><span data-ttu-id="346f4-114">Slik definerer du utgiftskonti for vedlikehold</span><span class="sxs-lookup"><span data-stu-id="346f4-114">To set up maintenance expense accounts</span></span>
<span data-ttu-id="346f4-115">Du må først angi et kontonummer på siden **Bokf.grupper - aktiva** for å kunne bokføre vedlikeholdskostnader.</span><span class="sxs-lookup"><span data-stu-id="346f4-115">To post maintenance costs, you must first enter an account number on the **FA Posting Groups** page.</span></span>

1. <span data-ttu-id="346f4-116">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokføringsgrupper – aktiva**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="346f4-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **FA Posting Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="346f4-117">Fyll ut feltet **Konto for vedlikeholdsutgifter** for hver enkelt bokføringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="346f4-117">Fill in the **Maintenance Expense Account** field for each posting group.</span></span>

> [!NOTE]  
>   <span data-ttu-id="346f4-118">Hvis du vil at vedlikeholdskostnader skal fordeles på avdelinger eller prosjekter, må du definere en fordelingsnøkkel.</span><span class="sxs-lookup"><span data-stu-id="346f4-118">To define that maintenance costs are allocated to departments or projects, set up an allocation keys.</span></span> <span data-ttu-id="346f4-119">Hvis du vil ha mer informasjon, kan du se [Definere generelle aktivafunksjoner](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="346f4-119">For more information, see [Set Up General Fixed Assets Features](fa-how-setup-general.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="346f4-120">Se også</span><span class="sxs-lookup"><span data-stu-id="346f4-120">See Also</span></span>
[<span data-ttu-id="346f4-121">Definere aktiva</span><span class="sxs-lookup"><span data-stu-id="346f4-121">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="346f4-122">Aktiva</span><span class="sxs-lookup"><span data-stu-id="346f4-122">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="346f4-123">Finans</span><span class="sxs-lookup"><span data-stu-id="346f4-123">Finance</span></span>](finance.md)  
[<span data-ttu-id="346f4-124">Komme i gang</span><span class="sxs-lookup"><span data-stu-id="346f4-124">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="346f4-125">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="346f4-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
