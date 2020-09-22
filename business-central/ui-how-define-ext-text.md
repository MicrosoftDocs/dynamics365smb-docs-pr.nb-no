---
title: Legge til ekstra linjer for å definere utvidede beskrivelser
description: Du kan legge til ekstra linjer for å utvide standardteksten som beskriver en vare, en finanskonto og andre data.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 07/08/2020
ms.author: edupont
ms.openlocfilehash: cf0418f4182e9d66da88af9262dd807a34dd3572
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782321"
---
# <a name="add-extended-text"></a><span data-ttu-id="31845-103">Legge til utvidet tekst</span><span class="sxs-lookup"><span data-stu-id="31845-103">Add Extended Text</span></span>

<span data-ttu-id="31845-104">Du kan utvide beskrivelsen av varer, lagerføringsenheter, finanskonti og ressurser ved å legge til ekstra linjer som utvidet tekst.</span><span class="sxs-lookup"><span data-stu-id="31845-104">You can extend the description for items, stock-keeping units, general ledger accounts, and resources by adding extra lines as extended text.</span></span> <span data-ttu-id="31845-105">Du kan også definere betingelser for bruk av de ekstra linjene.</span><span class="sxs-lookup"><span data-stu-id="31845-105">You can also set up conditions for use of the extra lines.</span></span>  

<span data-ttu-id="31845-106">Delen nedenfor beskriver hvordan du legger til utvidet tekst i en beskrivelse av en vare.</span><span class="sxs-lookup"><span data-stu-id="31845-106">The following section describes how to add extended text to a description of an item.</span></span> <span data-ttu-id="31845-107">De samme trinnene gjelder også for lagerføringsenheter, finanskonti og ressurser.</span><span class="sxs-lookup"><span data-stu-id="31845-107">But the same steps apply to stock-keeping units, general ledger accounts, and resources.</span></span>  

## <a name="to-define-extended-text-for-an-description"></a><span data-ttu-id="31845-108">Slik definerer du utvidet tekst for en beskrivelse</span><span class="sxs-lookup"><span data-stu-id="31845-108">To define extended text for an description</span></span>

1. <span data-ttu-id="31845-109">Åpne kortet for en vare som du vil legge til utvidet tekst for, og velg deretter handlingen **Utvidet tekst**.</span><span class="sxs-lookup"><span data-stu-id="31845-109">Open the card for an item that you want to add extended text to, and then choose the **Extended Text** action.</span></span>
2. <span data-ttu-id="31845-110">Fyll ut feltene **Kode** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="31845-110">Fill in the **Code** and **Description** fields.</span></span>
3. <span data-ttu-id="31845-111">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="31845-111">Choose the **New**.</span></span>
4. <span data-ttu-id="31845-112">Fyll ut **Språkkode**-feltet eller merk av for **Alle språkkoder** hvis du bruker språkkoder.</span><span class="sxs-lookup"><span data-stu-id="31845-112">Fill in the **Language Code** field or select the **All Language Codes** check box if you use language codes.</span></span>
5. <span data-ttu-id="31845-113">Fyll ut feltene **Startdato** og **Sluttdato** hvis du vil begrense perioden for bruk av den utvidete teksten.</span><span class="sxs-lookup"><span data-stu-id="31845-113">Fill in the **Starting Date** and **Ending Date** fields if you want to limit the dates on which the extended text is used.</span></span>
6. <span data-ttu-id="31845-114">I feltet **Tekst** angir du koden for den utvidete teksten.</span><span class="sxs-lookup"><span data-stu-id="31845-114">In the **Text** field, write the extended text.</span></span>
7. <span data-ttu-id="31845-115">Merk av for de aktuelle dokumenttypene du vil at de utvidete tekstene skal skrives ut på.</span><span class="sxs-lookup"><span data-stu-id="31845-115">Select relevant check boxes for the document types where you want the extended text printed.</span></span>
8. <span data-ttu-id="31845-116">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="31845-116">Close the page.</span></span>

<span data-ttu-id="31845-117">Du kan nå legge til den utvidede teksten i dokumenter.</span><span class="sxs-lookup"><span data-stu-id="31845-117">You can now add this extended text to documents.</span></span> <span data-ttu-id="31845-118">Fremgangsmåten nedenfor forklarer hvordan du legger til utvidet tekst i en ordre, men den samme fremgangsmåten gjelder alle andre dokumenter du har angitt for den utvidede teksten.</span><span class="sxs-lookup"><span data-stu-id="31845-118">The following procedure explains how to add extended text to a sales order, but the same steps apply to any other document that you specified for the extended text.</span></span>  

## <a name="to-add-an-extended-item-text-on-a-sales-order-line"></a><span data-ttu-id="31845-119">Legge til teksten for utvidet vare på en ordrelinje</span><span class="sxs-lookup"><span data-stu-id="31845-119">To add an extended item text on a sales order line</span></span>

1. <span data-ttu-id="31845-120">Åpne en ordre med en salgslinje for en vare som har utvidet tekst som er definert.</span><span class="sxs-lookup"><span data-stu-id="31845-120">Open a sales order with a sales line for an item that has extended text defined.</span></span> <span data-ttu-id="31845-121">Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="31845-121">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="31845-122">Velg den aktuelle linjen og velg deretter **Sett inn utv. tekster**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="31845-122">Select the line in question, and then choose the **Insert Ext. Text** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="31845-123">Se også</span><span class="sxs-lookup"><span data-stu-id="31845-123">See Also</span></span>

[<span data-ttu-id="31845-124">Definere lager</span><span class="sxs-lookup"><span data-stu-id="31845-124">Setting Up Inventory</span></span>](inventory-setup-inventory.md)  
<span data-ttu-id="31845-125">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="31845-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
