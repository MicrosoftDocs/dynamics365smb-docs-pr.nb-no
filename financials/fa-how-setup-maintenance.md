---
title: Definere aktivavedlikehold | Microsoft-dokumentasjon
description: "For å administrere aktivareparasjoner og -service angir du generelle vedlikeholdsopplysninger, koder for typen arbeid og en bokføringskonto for kost."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7ae4abacf22d3610194ea56bbaa997390cb7df0a
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-fixed-asset-maintenance"></a><span data-ttu-id="35229-103">Definere aktivavedlikehold</span><span class="sxs-lookup"><span data-stu-id="35229-103">Set Up Fixed Asset Maintenance</span></span>
<span data-ttu-id="35229-104">For å styre vedlikehold av aktiva, må du først definere noen generelle vedlikeholdsopplysninger, en bokføringskonto for vedlikeholdskostnader og vedlikeholdskoder for typer arbeid, for eksempel rutineservice eller reparasjon.</span><span class="sxs-lookup"><span data-stu-id="35229-104">To manage fixed asset maintenance, you must first set up some general maintenance information, a posting account for maintenance costs, and maintenance codes for types of work, such as Routine Service or Repair.</span></span>

## <a name="to-set-up-general-maintenance-information"></a><span data-ttu-id="35229-105">Slik definerer du generelle vedlikeholdsopplysninger:</span><span class="sxs-lookup"><span data-stu-id="35229-105">To set up general maintenance information</span></span>
<span data-ttu-id="35229-106">Hvis du definerer vedlikeholdsfeltene, kan du bokføre vedlikeholdsutgifter fra aktivakladden.</span><span class="sxs-lookup"><span data-stu-id="35229-106">If you set up the fields for maintenance, you can post maintenance expenses from the fixed asset journal.</span></span>

1. <span data-ttu-id="35229-107">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Aktiva**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="35229-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="35229-108">Velg aktivaet du vil definere forsikringsdekning for, og velg deretter handlingen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="35229-108">Select the fixed asset that you to define insurance coverage for, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="35229-109">Fyll ut feltene på hurtigfanen **Vedlikehold** etter behov.</span><span class="sxs-lookup"><span data-stu-id="35229-109">On the **Maintenance** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a><span data-ttu-id="35229-110">Slik definerer du vedlikeholdskoder</span><span class="sxs-lookup"><span data-stu-id="35229-110">To set up maintenance codes</span></span>
<span data-ttu-id="35229-111">Når du bokfører vedlikeholdskostnader fra en finanskladd, fyller du ut feltet **Vedlikeholdskode** for å registrere hva slags vedlikehold som er utført, for eksempel rutineservice eller reparasjon.</span><span class="sxs-lookup"><span data-stu-id="35229-111">When you post maintenance costs from a general journal, you fill in the **Maintenance Code** field to record what kind of maintenance has been performed, such as routine service or repair.</span></span>

1. <span data-ttu-id="35229-112">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Vedlikehold**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="35229-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Maintenance**, and then choose the related link.</span></span>
2. <span data-ttu-id="35229-113">I **Vedlikehold**-vinduet definerer du koder for ulike typer vedlikeholdsarbeid.</span><span class="sxs-lookup"><span data-stu-id="35229-113">In the **Maintenance** window, set up codes for different types of maintenance work.</span></span>

## <a name="to-set-up-maintenance-expense-accounts"></a><span data-ttu-id="35229-114">Slik definerer du utgiftskonti for vedlikehold</span><span class="sxs-lookup"><span data-stu-id="35229-114">To set up maintenance expense accounts</span></span>
<span data-ttu-id="35229-115">Du må først angi et kontonummer i vinduet **Bokf.grupper - aktiva** for å kunne bokføre vedlikeholdskostnader.</span><span class="sxs-lookup"><span data-stu-id="35229-115">To post maintenance costs, you must first enter an account number in the **FA Posting Groups** window.</span></span>

1. <span data-ttu-id="35229-116">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Bokføringsgrupper - aktiva**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="35229-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA Posting Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="35229-117">Fyll ut feltet **Konto for vedlikeholdsutgifter** for hver enkelt bokføringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="35229-117">Fill in the **Maintenance Expense Account** field for each posting group.</span></span>

> [!NOTE]  
>   <span data-ttu-id="35229-118">Hvis du vil at vedlikeholdskostnader skal fordeles på avdelinger eller prosjekter, må du definere en fordelingsnøkkel.</span><span class="sxs-lookup"><span data-stu-id="35229-118">To define that maintenance costs are allocated to departments or projects, set up an allocation keys.</span></span> <span data-ttu-id="35229-119">Hvis du vil ha mer informasjon, kan du se [Definere generelle aktivafunksjoner](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="35229-119">For more information, see [Set Up General Fixed Assets Features](fa-how-setup-general.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="35229-120">Se også</span><span class="sxs-lookup"><span data-stu-id="35229-120">See Also</span></span>
[<span data-ttu-id="35229-121">Definere aktiva</span><span class="sxs-lookup"><span data-stu-id="35229-121">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="35229-122">Aktiva</span><span class="sxs-lookup"><span data-stu-id="35229-122">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="35229-123">Finans</span><span class="sxs-lookup"><span data-stu-id="35229-123">Finance</span></span>](finance.md)  
<span data-ttu-id="35229-124">[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="35229-124">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="35229-125">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="35229-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

