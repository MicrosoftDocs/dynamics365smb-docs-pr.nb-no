---
title: Legge til ekstra linjer for å definere utvidede beskrivelser
description: Du kan legge til ekstra linjer for å utvide standardteksten som beskriver en vare, en finanskonto og andre data.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ec924b103e6767eaaa888144af5d7ea0cca8f2c1
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385777"
---
# <a name="add-extended-text"></a><span data-ttu-id="ed5cd-103">Legge til utvidet tekst</span><span class="sxs-lookup"><span data-stu-id="ed5cd-103">Add Extended Text</span></span>

<span data-ttu-id="ed5cd-104">Du kan utvide beskrivelsen av varer, lagerføringsenheter, finanskonti og ressurser ved å legge til ekstra linjer som utvidet tekst.</span><span class="sxs-lookup"><span data-stu-id="ed5cd-104">You can extend the description for items, stock-keeping units, general ledger accounts, and resources by adding extra lines as extended text.</span></span> <span data-ttu-id="ed5cd-105">Du kan også definere betingelser for bruk av de ekstra linjene.</span><span class="sxs-lookup"><span data-stu-id="ed5cd-105">You can also set up conditions for use of the extra lines.</span></span>  

<span data-ttu-id="ed5cd-106">Delen nedenfor beskriver hvordan du legger til utvidet tekst i en beskrivelse av en vare.</span><span class="sxs-lookup"><span data-stu-id="ed5cd-106">The following section describes how to add extended text to a description of an item.</span></span> <span data-ttu-id="ed5cd-107">De samme trinnene gjelder også for lagerføringsenheter, finanskonti og ressurser.</span><span class="sxs-lookup"><span data-stu-id="ed5cd-107">But the same steps apply to stock-keeping units, general ledger accounts, and resources.</span></span>  

## <a name="to-define-extended-text-for-an-description"></a><span data-ttu-id="ed5cd-108">Slik definerer du utvidet tekst for en beskrivelse</span><span class="sxs-lookup"><span data-stu-id="ed5cd-108">To define extended text for an description</span></span>

1. <span data-ttu-id="ed5cd-109">Åpne kortet for en vare som du vil legge til utvidet tekst for, og velg deretter handlingen **Utvidet tekst**.</span><span class="sxs-lookup"><span data-stu-id="ed5cd-109">Open the card for an item that you want to add extended text to, and then choose the **Extended Text** action.</span></span>
2. <span data-ttu-id="ed5cd-110">Fyll ut feltene **Kode** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="ed5cd-110">Fill in the **Code** and **Description** fields.</span></span>
3. <span data-ttu-id="ed5cd-111">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ed5cd-111">Choose the **New**.</span></span>
4. <span data-ttu-id="ed5cd-112">Fyll ut **Språkkode**-feltet eller merk av for **Alle språkkoder** hvis du bruker språkkoder.</span><span class="sxs-lookup"><span data-stu-id="ed5cd-112">Fill in the **Language Code** field or select the **All Language Codes** check box if you use language codes.</span></span>
5. <span data-ttu-id="ed5cd-113">Fyll ut feltene **Startdato** og **Sluttdato** hvis du vil begrense perioden for bruk av den utvidete teksten.</span><span class="sxs-lookup"><span data-stu-id="ed5cd-113">Fill in the **Starting Date** and **Ending Date** fields if you want to limit the dates on which the extended text is used.</span></span>
6. <span data-ttu-id="ed5cd-114">I feltet **Tekst** angir du koden for den utvidete teksten.</span><span class="sxs-lookup"><span data-stu-id="ed5cd-114">In the **Text** field, write the extended text.</span></span>
7. <span data-ttu-id="ed5cd-115">Merk av for de aktuelle dokumenttypene du vil at de utvidete tekstene skal skrives ut på.</span><span class="sxs-lookup"><span data-stu-id="ed5cd-115">Select relevant check boxes for the document types where you want the extended text printed.</span></span>
8. <span data-ttu-id="ed5cd-116">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ed5cd-116">Close the page.</span></span>

<span data-ttu-id="ed5cd-117">Du kan nå legge til den utvidede teksten i dokumenter.</span><span class="sxs-lookup"><span data-stu-id="ed5cd-117">You can now add this extended text to documents.</span></span> <span data-ttu-id="ed5cd-118">Fremgangsmåten nedenfor forklarer hvordan du legger til utvidet tekst i en ordre, men den samme fremgangsmåten gjelder alle andre dokumenter du har angitt for den utvidede teksten.</span><span class="sxs-lookup"><span data-stu-id="ed5cd-118">The following procedure explains how to add extended text to a sales order, but the same steps apply to any other document that you specified for the extended text.</span></span>  

## <a name="to-add-an-extended-item-text-on-a-sales-order-line"></a><span data-ttu-id="ed5cd-119">Legge til teksten for utvidet vare på en ordrelinje</span><span class="sxs-lookup"><span data-stu-id="ed5cd-119">To add an extended item text on a sales order line</span></span>

1. <span data-ttu-id="ed5cd-120">Åpne en ordre med en salgslinje for en vare som har utvidet tekst som er definert.</span><span class="sxs-lookup"><span data-stu-id="ed5cd-120">Open a sales order with a sales line for an item that has extended text defined.</span></span> <span data-ttu-id="ed5cd-121">Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="ed5cd-121">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="ed5cd-122">Velg den aktuelle linjen og velg deretter **Sett inn utv. tekster**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="ed5cd-122">Select the line in question, and then choose the **Insert Ext. Text** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed5cd-123">Se også</span><span class="sxs-lookup"><span data-stu-id="ed5cd-123">See Also</span></span>

[<span data-ttu-id="ed5cd-124">Definere lager</span><span class="sxs-lookup"><span data-stu-id="ed5cd-124">Setting Up Inventory</span></span>](inventory-setup-inventory.md)  
<span data-ttu-id="ed5cd-125">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ed5cd-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]