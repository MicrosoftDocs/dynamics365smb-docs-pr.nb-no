---
title: "Arbeide med stykklister for å håndtere komponenter | Microsoft-dokumentasjon"
description: "Du oppretter en monteringsstykkliste for å angi komponentene eller ressursene som kreves for å sette sammen varen som monteringsstykklisten representerer, og du kan vise komponentene for en monteringsvare."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: e6aef60ee5b206b0ae978f72b92e6f8778290509
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-work-with-bills-of-material"></a><span data-ttu-id="4a427-103">Arbeide med stykklister</span><span class="sxs-lookup"><span data-stu-id="4a427-103">How to: Work with Bills of Material</span></span>
> [!NOTE]  
>   <span data-ttu-id="4a427-104">Gjeldende versjon av [!INCLUDE[d365fin](includes/d365fin_md.md)] inneholder bare den første delen av funksjonen for monteringsstyring.</span><span class="sxs-lookup"><span data-stu-id="4a427-104">The current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] only contains the first part of the Assembly Management feature.</span></span> <span data-ttu-id="4a427-105">Nå kan du opprette bare monteringsstykklister og håndtere de relaterte overordnede varene som vanlige varer.</span><span class="sxs-lookup"><span data-stu-id="4a427-105">For now, you can only create assembly BOMs and then handle the related parent items as normal inventory items.</span></span> <span data-ttu-id="4a427-106">Du kan behandle den faktiske samlingen av varer fra komponenter, enten i montering til lager eller montering til ordreflyter i en fremtidig oppdatering, og du kan selge komponenter som sett.</span><span class="sxs-lookup"><span data-stu-id="4a427-106">In a future update, you can manage the actual assembly of items from components, either in assemble-to-stock or assemble-to-order flows, and you can sell components as kits.</span></span>

<span data-ttu-id="4a427-107">Du kan bruke stykklister til å strukturere overordnede varer som selges som sett som består av komponenter for den overordnede varen, eller som du monterer til bestilling eller lager.</span><span class="sxs-lookup"><span data-stu-id="4a427-107">You use bills of materials (BOMs) to structure parent items that you sell as kits consisting of the parent's components or that you assemble to order or to stock.</span></span>

<span data-ttu-id="4a427-108">I [!INCLUDE[d365fin](includes/d365fin_md.md)] er en stykkliste referert til som en "monteringsstykkliste".</span><span class="sxs-lookup"><span data-stu-id="4a427-108">In [!INCLUDE[d365fin](includes/d365fin_md.md)], a bill of materials is referred to as an "assembly BOM".</span></span> <span data-ttu-id="4a427-109">Monteringsstykklister angir hvilke komponenter som inngår i overordnede varer.</span><span class="sxs-lookup"><span data-stu-id="4a427-109">Assembly BOMs specify which components are contained in parent items.</span></span> <span data-ttu-id="4a427-110">En overordnet vare blir referert til som en "monteringsvare" i denne dokumentasjonen.</span><span class="sxs-lookup"><span data-stu-id="4a427-110">In this documentation, a parent item is referred to as an "assembly item".</span></span>

<span data-ttu-id="4a427-111">Monteringsstykklister inneholder vanligvis varer, men kan også inneholde en eller flere ressurser som trengs for å sette monteringsvaren sammen.</span><span class="sxs-lookup"><span data-stu-id="4a427-111">Assembly BOMs usually contain items but can also contain one or more resources that are required to put the assembly item together.</span></span>

<span data-ttu-id="4a427-112">Monteringsstykklister kan ha flere nivåer, noe som betyr at en komponent i monteringsstykklisten selv kan være en monteringsvare.</span><span class="sxs-lookup"><span data-stu-id="4a427-112">Assembly BOMs can have multiple levels, which means that a component on the assembly BOM can be an assembly item itself.</span></span> <span data-ttu-id="4a427-113">I så fall skal **Monteringsstykkliste**-feltet på monteringsstykklistelinjen inneholde **Ja**.</span><span class="sxs-lookup"><span data-stu-id="4a427-113">In that case, the **Assembly BOM** field on the assembly BOM line contains **Yes**.</span></span>

<span data-ttu-id="4a427-114">Spesielle krav gjelder for varer i monteringsstykklister med hensyn til tilgjengelighet.</span><span class="sxs-lookup"><span data-stu-id="4a427-114">Special requirements apply to items on assembly BOMs with regards to availability.</span></span> <span data-ttu-id="4a427-115">Hvis du vil ha mer informasjon, kan du se delen «Vise tilgjengeligheten til en vare etter bruk i monteringsstykklister» i [Vise tilgjengeligheten av varer](inventory-how-availability-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4a427-115">For more information, see the "To see the availability of an item by its use in assembly BOMs" section in [How to: View the Availability of Items](inventory-how-availability-overview.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="4a427-116">Denne funksjonen krever at opplevelsen er satt til **Løsning**.</span><span class="sxs-lookup"><span data-stu-id="4a427-116">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="4a427-117">Hvis du vil ha mer informasjon, kan du se [Tilpasse Financials-opplevelsen](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="4a427-117">For more information, see [Customizing Your Financials Experience](ui-experiences.md).</span></span>

## <a name="to-create-an-assembly-bom"></a><span data-ttu-id="4a427-118">Slik oppretter du en monteringsstykkliste:</span><span class="sxs-lookup"><span data-stu-id="4a427-118">To create an assembly BOM</span></span>
<span data-ttu-id="4a427-119">Hvis du vil definere en overordnet vare som består av andre varer, og potensielt av ressursene som kreves for å sette sammen den overordnede varen, må du opprette en monteringsstykkliste.</span><span class="sxs-lookup"><span data-stu-id="4a427-119">To define a parent item that consists of other items, and potentially of resources required to put the parent together, you must create an assembly BOM.</span></span>  

<span data-ttu-id="4a427-120">Oppretting av en monteringsstykkliste foregår i to trinn:</span><span class="sxs-lookup"><span data-stu-id="4a427-120">There are two parts to creating an assembly BOM:</span></span>
- <span data-ttu-id="4a427-121">Definere en ny vare</span><span class="sxs-lookup"><span data-stu-id="4a427-121">Setting up a new item</span></span>
- <span data-ttu-id="4a427-122">Definere stykklistestrukturen for monteringsvaren.</span><span class="sxs-lookup"><span data-stu-id="4a427-122">Defining the BOM structure of the assembly item.</span></span>

1. <span data-ttu-id="4a427-123">Definer en ny vare.</span><span class="sxs-lookup"><span data-stu-id="4a427-123">Set up a new item.</span></span> <span data-ttu-id="4a427-124">Hvis du vil ha mer informasjon, kan du se [Registrere nye varer](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="4a427-124">For more information, see [How to: Register New Items](inventory-how-register-new-items.md).</span></span>

    <span data-ttu-id="4a427-125">Fortsette med å registrere komponenter eller ressurser i monteringsstykklisten.</span><span class="sxs-lookup"><span data-stu-id="4a427-125">Proceed to enter components or resources on the assembly BOM.</span></span>  
2. <span data-ttu-id="4a427-126">I vinduet **Varekort** for en monteringsvare velger du **Montering** og velger deretter **Monteringsstykkliste**.</span><span class="sxs-lookup"><span data-stu-id="4a427-126">In the **Item Card** window for an assembly item, choose the **Assembly** action, and then choose the **Assembly BOM** action.</span></span>
3. <span data-ttu-id="4a427-127">Fyll ut feltene etter behov i vinduet **Monteringsstykkliste**.</span><span class="sxs-lookup"><span data-stu-id="4a427-127">In the **Assembly BOM** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a><span data-ttu-id="4a427-128">Vise komponentene i en monteringsvare som er rykket inn i henhold til stykklistestrukturen</span><span class="sxs-lookup"><span data-stu-id="4a427-128">To view the components of an assembly item indented according to the BOM structure</span></span>
<span data-ttu-id="4a427-129">Fra vinduet **Monteringsstykkliste** kan du åpne et eget vindu som viser komponentene og ressurser som er rykket inn, i henhold til deres stykklisteposisjon under monteringsvaren.</span><span class="sxs-lookup"><span data-stu-id="4a427-129">From the **Assembly BOM** window, you can open a separate window that shows the components and any resources indented according to their BOM position under the assembly item.</span></span>

1. <span data-ttu-id="4a427-130">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Varer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="4a427-130">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="4a427-131">Åpne kortet for en monteringsvare.</span><span class="sxs-lookup"><span data-stu-id="4a427-131">Open the card for an assembly item.</span></span> <span data-ttu-id="4a427-132">(Feltet **Monteringsstykkliste** i vinduet **Varer** inneholder **Ja**.)</span><span class="sxs-lookup"><span data-stu-id="4a427-132">(The **Assembly BOM** field in the **Items** window contains **Yes**.)</span></span>
3. <span data-ttu-id="4a427-133">I vinduet **Varekort** velger du **Montering** og velger deretter **Monteringsstykkliste**.</span><span class="sxs-lookup"><span data-stu-id="4a427-133">In the **Item Card** window, choose the **Assembly** action, and then choose the **Assembly BOM** action.</span></span>
4. <span data-ttu-id="4a427-134">I vinduet **Monteringsstykkliste** velger du handlingen **Vis stykkliste**.</span><span class="sxs-lookup"><span data-stu-id="4a427-134">In the **Assembly BOM** window, choose the **Show BOM** action.</span></span>

## <a name="to-buy-sell-or-transfer-assembly-items"></a><span data-ttu-id="4a427-135">Kjøpe, selge eller overføre monteringsvarer</span><span class="sxs-lookup"><span data-stu-id="4a427-135">To buy, sell, or transfer assembly items</span></span>
<span data-ttu-id="4a427-136">Fordi den gjeldende versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] bare inneholder muligheten til å definere og tilordne monteringsstykklister til varer, kan du bare håndtere monteringsvarer på dokumentlinjene som vanlige varer.</span><span class="sxs-lookup"><span data-stu-id="4a427-136">Because the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] only contains the ability to define and assign assembly BOMs to items, you can handle assembly items on document lines as normal items only.</span></span>

<span data-ttu-id="4a427-137">**Forsiktig**: Lagerantallet av stykklistekomponenter vil ikke bli justert hvis du gjør dette.</span><span class="sxs-lookup"><span data-stu-id="4a427-137">**Caution**: The inventory quantity of BOM components will not be adjusted if you do so.</span></span>

## <a name="see-also"></a><span data-ttu-id="4a427-138">Se også</span><span class="sxs-lookup"><span data-stu-id="4a427-138">See Also</span></span>
[<span data-ttu-id="4a427-139">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="4a427-139">How to: Register New Items</span></span>](inventory-how-register-new-items.md)  
<span data-ttu-id="4a427-140">[Vise tilgjengeligheten av varer](inventory-how-availability-overview.md)   </span><span class="sxs-lookup"><span data-stu-id="4a427-140">[How to: View the Availability of Items](inventory-how-availability-overview.md)   </span></span>  
[<span data-ttu-id="4a427-141">Lager</span><span class="sxs-lookup"><span data-stu-id="4a427-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="4a427-142">[Arbeide med [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4a427-142">[Working with [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>

