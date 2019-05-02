---
title: Lukke regnskapsperioder for et regnskapsår | Microsoft-dokumentasjon
description: Beskriver hvordan du lukker regnskapsperiodene som utgjør regnskapsåret.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2018
ms.author: jswymer
ms.openlocfilehash: c8f086e0dc7479ece62ab28b64f9553ba2d13b82
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802746"
---
# <a name="close-accounting-periods"></a><span data-ttu-id="6c091-103">Lukke regnskapsperioder</span><span class="sxs-lookup"><span data-stu-id="6c091-103">Close Accounting Periods</span></span>
<span data-ttu-id="6c091-104">Når et regnskapsår er over, må du lukke periodene som utgjør regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="6c091-104">When a fiscal year is over, you must close the periods that comprise it.</span></span>

## <a name="to-close-accounting-periods"></a><span data-ttu-id="6c091-105">Slik lukker du regnskapsperioder</span><span class="sxs-lookup"><span data-stu-id="6c091-105">To close accounting periods</span></span>
1. <span data-ttu-id="6c091-106">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Regnskapsperioder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="6c091-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Accounting Periods**, and then choose the related link.</span></span>
2. <span data-ttu-id="6c091-107">På siden **Regnskapsperioder** velger du handling **Lukk år**.</span><span class="sxs-lookup"><span data-stu-id="6c091-107">On the **Accounting Periods** page, choose the **Close Year** action.</span></span>

    <span data-ttu-id="6c091-108">Hvis flere enn ett regnskapsår er åpne, blir det tidligste valg for lukking.</span><span class="sxs-lookup"><span data-stu-id="6c091-108">If more than one fiscal year is open, the earliest one is automatically selected to be closed.</span></span> <span data-ttu-id="6c091-109">Det vises en melding som sier hvilket år som lukkes, og følgene ved å lukke året forklares.</span><span class="sxs-lookup"><span data-stu-id="6c091-109">A message displays identifying the year that will close and the consequences of closing the year.</span></span>
3. <span data-ttu-id="6c091-110">Hvis du vil lukke året, velger du **Ja**-knappen.</span><span class="sxs-lookup"><span data-stu-id="6c091-110">To close the year, choose the **Yes** button.</span></span>

<span data-ttu-id="6c091-111">Regnskapsåret er lukket, og det er merket av i feltene **Lukket** og **Dato låst** for alle periodene i året.</span><span class="sxs-lookup"><span data-stu-id="6c091-111">The fiscal year is closed, and the **Closed** and **Date Locked** fields for all the periods in the year are selected.</span></span> <span data-ttu-id="6c091-112">Regnskapsåret kan ikke åpnes på nytt, og du kan ikke slette haken i feltene **Lukket** eller **Dato låst**.</span><span class="sxs-lookup"><span data-stu-id="6c091-112">The fiscal year cannot be opened again and you cannot remove the check mark from the **Closed** or **Date Locked** fields.</span></span>

> [!NOTE]  
>   <span data-ttu-id="6c091-113">Det er ikke mulig å avslutte et regnskapsår før et nytt regnskapsår er opprettet.</span><span class="sxs-lookup"><span data-stu-id="6c091-113">You cannot close a fiscal year before you create a new one.</span></span> <span data-ttu-id="6c091-114">Merk at når et regnskapsår er avsluttet, er det ikke mulig å endre startdatoen for det etterfølgende regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="6c091-114">Notice that when a fiscal year has been closed, you cannot change the starting date of the following fiscal year.</span></span>

<span data-ttu-id="6c091-115">Selv om et regnskapsår er avsluttet, kan du bokføre finansposter i det.</span><span class="sxs-lookup"><span data-stu-id="6c091-115">Even though a fiscal year has been closed, you can still post general ledger entries to it.</span></span> <span data-ttu-id="6c091-116">Postene vil, i forbindelse med bokføringen, bli merket som bokført i et avsluttet regnskapsår, og det merkes av for feltet **Etterpost**.</span><span class="sxs-lookup"><span data-stu-id="6c091-116">When you do this, the entries will be marked as posted to a closed fiscal year and the **Prior-Year Entry** field will be selected.</span></span>

<span data-ttu-id="6c091-117">Når et regnskapsår er avsluttet, må du lukke resultatkontiene, og overføre årets resultat til resultatkontoen i balansen.</span><span class="sxs-lookup"><span data-stu-id="6c091-117">After a fiscal year is closed, you must close the income statement accounts and transfer the year's results to an account in the balance sheet.</span></span> <span data-ttu-id="6c091-118">Du kan gjenta dette hver gang du bokfører til det lukkede regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="6c091-118">You can repeat this every time that you post to the closed fiscal year.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c091-119">Se også</span><span class="sxs-lookup"><span data-stu-id="6c091-119">See Also</span></span>
[<span data-ttu-id="6c091-120">Avslutte tablåer</span><span class="sxs-lookup"><span data-stu-id="6c091-120">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="6c091-121">Bokføre avslutningsposten for årsslutt</span><span class="sxs-lookup"><span data-stu-id="6c091-121">Post the Year-End Closing Entry</span></span>](year-how-post-year-end-close-entry.md)  
[<span data-ttu-id="6c091-122">Åpne et nytt regnskapsår</span><span class="sxs-lookup"><span data-stu-id="6c091-122">Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md)  
<span data-ttu-id="6c091-123">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6c091-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>