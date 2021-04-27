---
title: Slik sperrer du varer fra salg eller kjøp
description: Du kan hindre at en vare brukes, for eksempel i salgs- og kjøpsdokumenter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4bc130d6982d969084f7fcbf3618893978317f36
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786051"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="574a1-103">Blokkere varer fra salg eller kjøp</span><span class="sxs-lookup"><span data-stu-id="574a1-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="574a1-104">Du kan blokkere en vare fra å bli lagt inn på linjer i salgs- eller bestillingsdokumenter, og du kan blokkere den fra å bli bokført i en transaksjon.</span><span class="sxs-lookup"><span data-stu-id="574a1-104">You can block an item from being entered on lines in sales or purchase documents, and you can block it from being posted in any transaction.</span></span> <span data-ttu-id="574a1-105">Dette er for eksempel nyttig når en vare har en kjent defekt.</span><span class="sxs-lookup"><span data-stu-id="574a1-105">For example, this is useful when an item has a known defect.</span></span> <span data-ttu-id="574a1-106">Hvis noen velger en sperret vare på et salgs- eller kjøpsdokument, vil en melding gi beskjed om at varen er sperret.</span><span class="sxs-lookup"><span data-stu-id="574a1-106">If someone chooses a blocked item on a sales or purchase document a message will inform them that the item is blocked.</span></span>

<span data-ttu-id="574a1-107">Tabellen nedenfor beskriver hva som skjer når varer er sperret.</span><span class="sxs-lookup"><span data-stu-id="574a1-107">The following table describes what occurs when items are blocked.</span></span>  

|<span data-ttu-id="574a1-108">Alternativ</span><span class="sxs-lookup"><span data-stu-id="574a1-108">Option</span></span>|<span data-ttu-id="574a1-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="574a1-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="574a1-110">**Sperret salg**</span><span class="sxs-lookup"><span data-stu-id="574a1-110">**Sales Blocked**</span></span>|<span data-ttu-id="574a1-111">Du kan ikke legge inn varen i et salgsdokument eller i en salgsvarekladd.</span><span class="sxs-lookup"><span data-stu-id="574a1-111">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="574a1-112">**Innkjøp blokkert**</span><span class="sxs-lookup"><span data-stu-id="574a1-112">**Purchasing Blocked**</span></span>|<span data-ttu-id="574a1-113">Du kan ikke legge inn varen i et kjøpsdokument, i en varekladd for kjøp eller i kjøpsplanleggingsprosesser.</span><span class="sxs-lookup"><span data-stu-id="574a1-113">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="574a1-114">**Sperret**</span><span class="sxs-lookup"><span data-stu-id="574a1-114">**Blocked**</span></span>|<span data-ttu-id="574a1-115">Du kan ikke bruke varen til noen varetransaksjon.</span><span class="sxs-lookup"><span data-stu-id="574a1-115">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="574a1-116">Sperrede varer kan returneres.</span><span class="sxs-lookup"><span data-stu-id="574a1-116">Blocked items can be returned.</span></span> <span data-ttu-id="574a1-117">Dette betyr at ingen av innstillingene ovenfor gjelder når varen brukes i returordrer og kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="574a1-117">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

<span data-ttu-id="574a1-118">Når du bruker funksjonen **Kopier fra dokument** til å opprette nye dokumenter som er basert på eksisterende dokumenter, blir du varslet hvis det blir sperret varer på kildedokumentlinjene.</span><span class="sxs-lookup"><span data-stu-id="574a1-118">When you use the **Copy from Document** function to create new documents based on existing documents, you are notified if any items on the source document lines are blocked.</span></span> <span data-ttu-id="574a1-119">De sperrede dokumentlinjene utelates fra det nye dokumentet, og en melding viser en oversikt over alle dokumentlinjene som er sperret i kildedokumentet.</span><span class="sxs-lookup"><span data-stu-id="574a1-119">The blocked document lines are excluded from the new document, and a notification shows an overview of all document lines that are blocked in the source document.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="574a1-120">Sperre en vare fra å legges inn på salgslinjer</span><span class="sxs-lookup"><span data-stu-id="574a1-120">To block an item from being entered on sales lines</span></span>  
1.  <span data-ttu-id="574a1-121">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="574a1-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="574a1-122">Velg varen du vil sperre, og velg deretter avmerkingsboksen **Sperret salg**.</span><span class="sxs-lookup"><span data-stu-id="574a1-122">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="574a1-123">Sperre en vare fra å legges inn på kjøpslinjer</span><span class="sxs-lookup"><span data-stu-id="574a1-123">To block an item from being entered on purchase lines</span></span>  
1.  <span data-ttu-id="574a1-124">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="574a1-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="574a1-125">Velg varen du vil sperre, og velg deretter avmerkingsboksen **Sperret kjøp**.</span><span class="sxs-lookup"><span data-stu-id="574a1-125">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="574a1-126">Sperre en vare fra å bli bokført</span><span class="sxs-lookup"><span data-stu-id="574a1-126">To block an item from being posted</span></span>
1. <span data-ttu-id="574a1-127">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="574a1-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="574a1-128">Velg varen du vil sperre, og velg deretter avmerkingsboksen **Sperret**.</span><span class="sxs-lookup"><span data-stu-id="574a1-128">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="574a1-129">Se også</span><span class="sxs-lookup"><span data-stu-id="574a1-129">See Also</span></span>  
[<span data-ttu-id="574a1-130">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="574a1-130">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="574a1-131">Lager</span><span class="sxs-lookup"><span data-stu-id="574a1-131">Inventory</span></span>](inventory-manage-inventory.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]