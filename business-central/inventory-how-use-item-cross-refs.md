---
title: Bruke varekryssreferanser | Microsoft Docs
description: Hvis du har definert en kryssreferanse mellom varebeskrivelsen som du bruker for en vare, og beskrivelsen som leverandøren av varen bruker, settes leverandørvarebeskrivelsen automatisk inn på kjøpsdokumenter for leverandøren når du fyller ut **Kryssreferansenr.** .
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 03/12/2019
ms.author: sgroespe
ms.openlocfilehash: 09fb7c17e2fccbd3b2ad3195cffa37493ad40f61
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/19/2019
ms.locfileid: "852266"
---
# <a name="use-item-cross-references"></a><span data-ttu-id="b9019-104">Bruke varekryssreferanser</span><span class="sxs-lookup"><span data-stu-id="b9019-104">Use Item Cross References</span></span>
<span data-ttu-id="b9019-105">Hvis du har definert en kryssreferanse mellom varebeskrivelsen som du bruker for en vare, og beskrivelsen som leverandøren av varen bruker, settes leverandørvarebeskrivelsen automatisk inn på kjøpsdokumenter for leverandøren når du fyller ut **Kryssreferansenr.**</span><span class="sxs-lookup"><span data-stu-id="b9019-105">If you set up a cross reference between the item description that you use for an item and the description that the vendor of that item uses, then the vendor's item description is automatically inserted on purchase documents for the vendor when you fill in the **Cross-Reference No.**</span></span> <span data-ttu-id="b9019-106">.</span><span class="sxs-lookup"><span data-stu-id="b9019-106">field.</span></span> <span data-ttu-id="b9019-107">Den samme funksjonaliteten gjelder for kundevarenumre på salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="b9019-107">The same functionality applies for customer item numbers on sales documents.</span></span>

<span data-ttu-id="b9019-108">Den følgende fremgangsmåten beskriver hvordan du bruker varekryssreferanser på kjøpssiden.</span><span class="sxs-lookup"><span data-stu-id="b9019-108">The following procedures describe how to use item cross references on the purchase side.</span></span> <span data-ttu-id="b9019-109">Trinnene er de samme for salgssiden.</span><span class="sxs-lookup"><span data-stu-id="b9019-109">The steps are similar for the sales side.</span></span>

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a><span data-ttu-id="b9019-110">Slik definerer du en varekryssreferanse til en leverandørs varebeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b9019-110">To set up an item cross reference to a vendor's item description</span></span>
1. <span data-ttu-id="b9019-111">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Varer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b9019-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="b9019-112">Åpne kortet for en vare som du vil opprette en kryssreferanse for til varebeskrivelsen som leverandøren bruker for denne varen.</span><span class="sxs-lookup"><span data-stu-id="b9019-112">Open the card for an item for which you want to create a cross reference to the item description that the vendor uses for that item.</span></span>
3. <span data-ttu-id="b9019-113">Velg **Kryssreferanser**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="b9019-113">Choose the **Cross References** action.</span></span>
4. <span data-ttu-id="b9019-114">På en ny linje på siden **Varekryssreferanseposter** fyller du ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="b9019-114">On a new line on the **Item Cross-Reference Entries** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="b9019-115">.</span><span class="sxs-lookup"><span data-stu-id="b9019-115">.</span></span>

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a><span data-ttu-id="b9019-116">Slik angir du en leverandørs varebeskrivelse på en bestilling</span><span class="sxs-lookup"><span data-stu-id="b9019-116">To enter a vendor's item description on a purchase order</span></span>
1. <span data-ttu-id="b9019-117">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bestillinger**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b9019-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="b9019-118">Opprett en bestilling for leverandøren du angav en varekryssreferanse for i den forrige prosedyren.</span><span class="sxs-lookup"><span data-stu-id="b9019-118">Create a purchase order for the vendor that you set up an item cross reference for in the previous procedure.</span></span>
3. <span data-ttu-id="b9019-119">Opprett en bestillingslinje for varen som du angav en varekryssreferanse for i den forrige prosedyren.</span><span class="sxs-lookup"><span data-stu-id="b9019-119">Create a purchase line for the item that you set up an item cross reference for in the previous procedure.</span></span>
4. <span data-ttu-id="b9019-120">I **Kryssreferansetypenr.**</span><span class="sxs-lookup"><span data-stu-id="b9019-120">In the **Cross-Reference No.**</span></span> <span data-ttu-id="b9019-121">-feltet velger du varekryssreferansen du har opprettet, og deretter velger du **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="b9019-121">field, select the item cross reference that you have created, and then choose the **OK** button.</span></span>

<span data-ttu-id="b9019-122">**Beskrivelse**-feltet på linjen overskrives med leverandørens varebeskrivelse, slik den er angitt opp på varekryssreferanseposten.</span><span class="sxs-lookup"><span data-stu-id="b9019-122">The **Description** field on the line is overwritten with the vendor's item description, as set up on the item cross-reference entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="b9019-123">Se også</span><span class="sxs-lookup"><span data-stu-id="b9019-123">See Also</span></span>
[<span data-ttu-id="b9019-124">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="b9019-124">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="b9019-125">Lager</span><span class="sxs-lookup"><span data-stu-id="b9019-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="b9019-126">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b9019-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>