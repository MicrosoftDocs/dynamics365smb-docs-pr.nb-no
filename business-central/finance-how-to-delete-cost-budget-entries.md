---
title: Slette kostbudsjettposter | Microsoft-dokumentasjon
description: Du bruker kjørselen Slett kostbudsjettposter til å annullere kostbudsjettposter i kostbudsjettjournalen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b4c81aa62f3548819db3451130c49fd11984b33a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387377"
---
# <a name="delete-cost-budget-entries"></a><span data-ttu-id="14db6-103">Slett kostbudsjettposter</span><span class="sxs-lookup"><span data-stu-id="14db6-103">Delete Cost Budget Entries</span></span>
<span data-ttu-id="14db6-104">Du bruker kjørselen **Slett kostbudsjettposter** til å annullere kostbudsjettposter i kostbudsjettjournalen.</span><span class="sxs-lookup"><span data-stu-id="14db6-104">You use the **Delete Cost Budget Entries** batch job to cancel cost budget entries from the cost budget register.</span></span>  

<span data-ttu-id="14db6-105">Du kan ikke slette én enkelt post eller en bunke med poster midt i listen over journalposter for å hindre hull i kostbudsjettposter og kostjournalposter.</span><span class="sxs-lookup"><span data-stu-id="14db6-105">To prevent any gaps in the cost budget entries and cost register entries, you cannot delete a single entry or a batch of entries in the middle of the list of register entries.</span></span>  

### <a name="to-delete-a-cost-budget-entry"></a><span data-ttu-id="14db6-106">Slik sletter du en kostbudsjettpost:</span><span class="sxs-lookup"><span data-stu-id="14db6-106">To delete a cost budget entry</span></span>  

1.  <span data-ttu-id="14db6-107">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Slett kostbudsjettposter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="14db6-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Cost Budget Entries**, and then choose the related link.</span></span>  

    <span data-ttu-id="14db6-108">Feltet **Til registreringsnr.**</span><span class="sxs-lookup"><span data-stu-id="14db6-108">The **To Register No.**</span></span> <span data-ttu-id="14db6-109">inneholder det siste journalpostnummeret og kan ikke endres.</span><span class="sxs-lookup"><span data-stu-id="14db6-109">field contains the last register entry number and cannot be changed.</span></span>  

    <span data-ttu-id="14db6-110">Du kan bruke feltet **Fra registreringsnr.**</span><span class="sxs-lookup"><span data-stu-id="14db6-110">You can use the **From Register No.**</span></span> <span data-ttu-id="14db6-111">til å velge et journalpostnummer som slettingen skal begynne fra.</span><span class="sxs-lookup"><span data-stu-id="14db6-111">field to select a register entry number from which the deletion should begin.</span></span>  
2.  <span data-ttu-id="14db6-112">Velg **OK**-knappen for å slette de valgte kostbudsjettpostene.</span><span class="sxs-lookup"><span data-stu-id="14db6-112">Choose the **OK** button to delete the selected cost budget entries.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="14db6-113">For å unngå en utilsiktet sletting av kostbudsjettposter kan du lukke journalposter ved å merke linjene som **lukket** i **Lukket**-feltet på siden **Kostbudsjettjournaler**.</span><span class="sxs-lookup"><span data-stu-id="14db6-113">To avoid an accidental deletion of cost budget entries, you can close register entries by marking the lines as **Closed** in the **Closed** field on the **Cost Budget Registers** page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="14db6-114">Se også</span><span class="sxs-lookup"><span data-stu-id="14db6-114">See Also</span></span>  
<span data-ttu-id="14db6-115">[Gjøre rede for kostnader](finance-manage-cost-accounting.md)
[Opprette kostbudsjetter](finance-create-cost-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="14db6-115">[Accounting for Costs](finance-manage-cost-accounting.md)
[Creating Cost Budgets](finance-create-cost-budgets.md)</span></span>  
<span data-ttu-id="14db6-116">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="14db6-116">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]