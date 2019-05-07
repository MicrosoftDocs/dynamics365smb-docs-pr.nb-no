---
title: Gi tilbud på et montere-til-ordre-salg | Microsoft-dokumentasjon
description: Du kan bruke monteringsstyring for å tilpasse en monteringsvare i henhold til en kundeforespørsel under salgsprosessen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: b69433a365e6c67f31863f8289cddb21d0f7f4b7
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "936486"
---
# <a name="quote-an-assemble-to-order-sale"></a><span data-ttu-id="4af80-103">Gi tilbud på et montere-til-ordre-salg</span><span class="sxs-lookup"><span data-stu-id="4af80-103">Quote an Assemble-to-Order Sale</span></span>
<span data-ttu-id="4af80-104">Du kan bruke monteringsstyring for å tilpasse en monteringsvare i henhold til en kundeforespørsel under salgsprosessen.</span><span class="sxs-lookup"><span data-stu-id="4af80-104">You can use assembly management to customize an assembly item to a customer’s request during the sales process.</span></span> <span data-ttu-id="4af80-105">Hvis du vil ha mer informasjon, kan du se [Selge varer som er montert til ordre](assembly-how-to-sell-items-assembled-to-order.md).</span><span class="sxs-lookup"><span data-stu-id="4af80-105">For more information, see [Sell Items Assembled to Order](assembly-how-to-sell-items-assembled-to-order.md).</span></span>  

<span data-ttu-id="4af80-106">Etter hvert som du selger en hvilken som helst annen type vare, kan du også opprette et tilbud for en tilpasset monteringsvare før du konverterer det til en ordre.</span><span class="sxs-lookup"><span data-stu-id="4af80-106">As when you sell any other type of item, you can also create a sales quote for a customized assembly item before converting it to a sales order.</span></span> <span data-ttu-id="4af80-107">Denne prosessen omfatter flere ekstra trinn når du sammenligner den med å opprette et vanlig tilbud, og den bruker en variant av en koblet monteringsordre, som er et monteringstilbud.</span><span class="sxs-lookup"><span data-stu-id="4af80-107">This process involves several extra steps when you compare it to creating a regular sales quote, and it uses a variation of a linked assembly order, which is an assembly quote.</span></span>

> [!NOTE]  
>  <span data-ttu-id="4af80-108">I likhet med alle typer tilbud brukes ikke antallene på monteringstilbud i tilgjengelighet, planlegging eller reservasjoner.</span><span class="sxs-lookup"><span data-stu-id="4af80-108">Like all types of quotes, the quantities on assembly quotes are not used in availability, planning, or reservations.</span></span>  

## <a name="to-create-a-sales-quote-for-an-assemble-to-order-item"></a><span data-ttu-id="4af80-109">Slik oppretter du et tilbud for en montere-til-ordre-vare:</span><span class="sxs-lookup"><span data-stu-id="4af80-109">To create a sales quote for an assemble-to-order item</span></span>  
1.  <span data-ttu-id="4af80-110">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Tilbud**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="4af80-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Quote**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4af80-111">Opprette en ny tilbudslinje med én linje for en monteringsvare.</span><span class="sxs-lookup"><span data-stu-id="4af80-111">Create a sales quote line with one line for an assembly item.</span></span> <span data-ttu-id="4af80-112">Hvis du vil ha mer informasjon, kan du se [Gi salgstilbud](sales-how-make-offers.md).</span><span class="sxs-lookup"><span data-stu-id="4af80-112">For more information, see [Make Sales Quotes](sales-how-make-offers.md).</span></span>  
3.  <span data-ttu-id="4af80-113">Angi hele antallet i feltet **Ant. som skal monteres til ordre**.</span><span class="sxs-lookup"><span data-stu-id="4af80-113">In the **Qty. to Assemble to Order** field, enter the full quantity.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="4af80-114">Du bør ikke gi tilbud på et delvist antall.</span><span class="sxs-lookup"><span data-stu-id="4af80-114">You should not quote a partial quantity.</span></span> <span data-ttu-id="4af80-115">Du må derfor angi samme antall som du skrev inn i feltet **Antall** på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="4af80-115">Therefore, you must enter the same quantity that you entered in the **Quantity** field on the sales quote line.</span></span>  

4.  <span data-ttu-id="4af80-116">På hurtigfanen **Linjer**, velg **Linje**, **Monter til ordre**, og deretter **Montere til ordre – linjer**.</span><span class="sxs-lookup"><span data-stu-id="4af80-116">On the **Lines** FastTab, choose **Line**, choose **Assemble to Order**, and then choose **Assemble-to-Order Lines**.</span></span> <span data-ttu-id="4af80-117">Du kan også merke feltet **Ant. som skal monteres til ordre** på linjen.</span><span class="sxs-lookup"><span data-stu-id="4af80-117">Alternatively, choose the **Qty. to Assemble to Order** field on the line.</span></span>  
5.  <span data-ttu-id="4af80-118">Gå gjennom eller endre monteringsordrelinjene i henhold til tilbudet kunden ber om, på siden **Montere til ordre – linjer**.</span><span class="sxs-lookup"><span data-stu-id="4af80-118">On the **Assemble-to-Order Lines** page, review or modify the assembly order lines according to the quote that the customer is requesting.</span></span> <span data-ttu-id="4af80-119">Hvis du vil vise mer informasjon, velger du **Vis dokument** for å åpne hele rammetilbudsordren.</span><span class="sxs-lookup"><span data-stu-id="4af80-119">If you want to view more information, choose the **Show Document** action to open the complete blanket quote order.</span></span> <span data-ttu-id="4af80-120">Du kan ikke endre innholdet i de fleste av feltene, og du kan ikke bokføre.</span><span class="sxs-lookup"><span data-stu-id="4af80-120">You cannot change the contents of most fields, and you cannot post.</span></span>  
6.  <span data-ttu-id="4af80-121">Når du har justert monteringsordrelinjene i henhold til tilbudet, lukker du siden **Montere til ordre – linjer** for å gå tilbake til siden **Tilbud**.</span><span class="sxs-lookup"><span data-stu-id="4af80-121">When you have adjusted the assembly order lines according to the quote, close the **Assemble-to-Order Lines** page to return to the **Sales Quote** page.</span></span>  
7.  <span data-ttu-id="4af80-122">Hvis kunden godtar tilbudet, oppretter du en ordre for den aktuelle monteringsvaren.</span><span class="sxs-lookup"><span data-stu-id="4af80-122">If the customer accepts the quote, then create a sales order for the quoted assembly item.</span></span> <span data-ttu-id="4af80-123">Hvis du vil ha mer informasjon, kan du se [Gi salgstilbud](sales-how-make-offers.md).</span><span class="sxs-lookup"><span data-stu-id="4af80-123">For more information, see [Make Sales Quotes](sales-how-make-offers.md).</span></span> <span data-ttu-id="4af80-124">Det koblede monteringstilbudet og eventuelle tilpasninger knyttes til denne nye salgsordren for å klargjøre for montering av varen(e) som skal selges.</span><span class="sxs-lookup"><span data-stu-id="4af80-124">The linked assembly quote and any customizations are linked to that new sales order to prepare for assembly of the item or items to be sold.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4af80-125">Se også</span><span class="sxs-lookup"><span data-stu-id="4af80-125">See Also</span></span>  
[<span data-ttu-id="4af80-126">Monteringsstyring</span><span class="sxs-lookup"><span data-stu-id="4af80-126">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="4af80-127">Arbeide med stykklister</span><span class="sxs-lookup"><span data-stu-id="4af80-127">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)  
[<span data-ttu-id="4af80-128">Lager</span><span class="sxs-lookup"><span data-stu-id="4af80-128">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="4af80-129">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="4af80-129">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="4af80-130">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4af80-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
