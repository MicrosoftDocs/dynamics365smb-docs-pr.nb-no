---
title: Slik sperrer du varer fra salg eller kjøp
description: I Business Central kan en vare være merket som sperret for salg, sperret for kjøp eller sperret for alt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: c453a10f30d2a45f6d4641bda8b24ee3659b1a32
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182303"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="a3668-103">Blokkere varer fra salg eller kjøp</span><span class="sxs-lookup"><span data-stu-id="a3668-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="a3668-104">Du kan blokkere en vare fra å bli lagt inn på salgs- eller bestillingslinjene, og du kan blokkere den fra å bli bokført i en transaksjon.</span><span class="sxs-lookup"><span data-stu-id="a3668-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="a3668-105">Tabellen nedenfor viser hva som skjer når varer er sperret.</span><span class="sxs-lookup"><span data-stu-id="a3668-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="a3668-106">Alternativ</span><span class="sxs-lookup"><span data-stu-id="a3668-106">Option</span></span>|<span data-ttu-id="a3668-107">Description</span><span class="sxs-lookup"><span data-stu-id="a3668-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="a3668-108">**Sperret salg**</span><span class="sxs-lookup"><span data-stu-id="a3668-108">**Sales Blocked**</span></span>|<span data-ttu-id="a3668-109">Du kan ikke legge inn varen i et salgsdokument eller i en salgsvarekladd.</span><span class="sxs-lookup"><span data-stu-id="a3668-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="a3668-110">**Innkjøp blokkert**</span><span class="sxs-lookup"><span data-stu-id="a3668-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="a3668-111">Du kan ikke legge inn varen i et kjøpsdokument, i en varekladd for kjøp eller i kjøpsplanleggingsprosesser.</span><span class="sxs-lookup"><span data-stu-id="a3668-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="a3668-112">**Sperret**</span><span class="sxs-lookup"><span data-stu-id="a3668-112">**Blocked**</span></span>|<span data-ttu-id="a3668-113">Du kan ikke bruke varen til noen varetransaksjon.</span><span class="sxs-lookup"><span data-stu-id="a3668-113">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="a3668-114">Sperrede varer kan returneres.</span><span class="sxs-lookup"><span data-stu-id="a3668-114">Blocked items can be returned.</span></span> <span data-ttu-id="a3668-115">Dette betyr at ingen av innstillingene ovenfor gjelder når varen brukes i returordrer og kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="a3668-115">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

<span data-ttu-id="a3668-116">Når du bruker funksjonen **Kopier fra dokument** til å opprette nye dokumenter som er basert på eksisterende dokumenter, blir du varslet hvis det blir sperret varer på kildedokumentlinjene.</span><span class="sxs-lookup"><span data-stu-id="a3668-116">When you use the **Copy from Document** function to create new documents based on existing documents, you are notified if any items on the source document lines are blocked.</span></span> <span data-ttu-id="a3668-117">De sperrede dokumentlinjene utelates fra det nye dokumentet, og en melding viser en oversikt over alle dokumentlinjene som er sperret i kildedokumentet.</span><span class="sxs-lookup"><span data-stu-id="a3668-117">The blocked document lines are excluded from the new document, and a notification shows an overview of all document lines that are blocked in the source document.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="a3668-118">Sperre en vare fra å legges inn på salgslinjer</span><span class="sxs-lookup"><span data-stu-id="a3668-118">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="a3668-119">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a3668-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a3668-120">Velg varen du vil sperre, og velg deretter avmerkingsboksen **Sperret salg**.</span><span class="sxs-lookup"><span data-stu-id="a3668-120">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="a3668-121">Hvis du prøver å angi varen i et salgsdokument eller kladdelinjen, vil du få en feilmelding om at varen ble sperret.</span><span class="sxs-lookup"><span data-stu-id="a3668-121">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="a3668-122">Sperre en vare fra å legges inn på kjøpslinjer</span><span class="sxs-lookup"><span data-stu-id="a3668-122">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="a3668-123">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a3668-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a3668-124">Velg varen du vil sperre, og velg deretter avmerkingsboksen **Sperret kjøp**.</span><span class="sxs-lookup"><span data-stu-id="a3668-124">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="a3668-125">Hvis du prøver å angi varen i et kjøpsdokument eller kladdelinjen, vil du få en feilmelding om at varen ble sperret.</span><span class="sxs-lookup"><span data-stu-id="a3668-125">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="a3668-126">Sperre en vare fra å bli bokført</span><span class="sxs-lookup"><span data-stu-id="a3668-126">To block an item from being posted</span></span>
1. <span data-ttu-id="a3668-127">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a3668-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="a3668-128">Velg varen du vil sperre, og velg deretter avmerkingsboksen **Sperret**.</span><span class="sxs-lookup"><span data-stu-id="a3668-128">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="a3668-129">Hvis du prøver å bokføre en transaksjonstype for varen, vil du få en feilmelding om at varen er sperret.</span><span class="sxs-lookup"><span data-stu-id="a3668-129">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3668-130">Se også</span><span class="sxs-lookup"><span data-stu-id="a3668-130">See Also</span></span>  
[<span data-ttu-id="a3668-131">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="a3668-131">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="a3668-132">Lager</span><span class="sxs-lookup"><span data-stu-id="a3668-132">Inventory</span></span>](inventory-manage-inventory.md)  
