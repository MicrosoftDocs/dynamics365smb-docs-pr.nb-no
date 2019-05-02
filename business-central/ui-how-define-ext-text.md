---
title: Legge til ekstra linjer for å definere utvidede varebeskrivelser | Microsoft-dokumentasjon
description: Du kan legge til ekstra linjer for å utvide standardteksten som beskriver en vare.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 02/26/2019
ms.author: sgroespe
ms.openlocfilehash: ecf0dab7e8c1215c6e121735fe7507ee28cc25b8
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802879"
---
# <a name="add-extended-item-text"></a><span data-ttu-id="9dd17-103">Legge til utvidet varetekst</span><span class="sxs-lookup"><span data-stu-id="9dd17-103">Add Extended Item Text</span></span>
<span data-ttu-id="9dd17-104">Du kan utvide en standardtekst for varer ved å legge til ekstra linjer, og du kan opprette betingelser for bruk av de ekstra linjene.</span><span class="sxs-lookup"><span data-stu-id="9dd17-104">You can extend a standard text for items by adding extra lines, and you can set up conditions for use of the extra lines.</span></span> <span data-ttu-id="9dd17-105">Dette kan du gjøre fra varekort.</span><span class="sxs-lookup"><span data-stu-id="9dd17-105">You do this from item cards.</span></span>

## <a name="to-define-extended-text-for-an-item-description"></a><span data-ttu-id="9dd17-106">Slik definerer du utvidet tekst for en varebeskrivelse</span><span class="sxs-lookup"><span data-stu-id="9dd17-106">To define extended text for an item description</span></span>
1. <span data-ttu-id="9dd17-107">Åpne kortet for en vare som du vil legge til utvidet tekst for, og velg deretter handlingen **Utvidet tekst**.</span><span class="sxs-lookup"><span data-stu-id="9dd17-107">Open the card for an item that you want to add extended text to, and then choose the **Extended Text** action.</span></span>
2. <span data-ttu-id="9dd17-108">Fyll ut feltene **Kode** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="9dd17-108">Fill in the **Code** and **Description** fields.</span></span>
3. <span data-ttu-id="9dd17-109">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9dd17-109">Choose the **New**.</span></span>
4. <span data-ttu-id="9dd17-110">Fyll ut **Språkkode**-feltet eller merk av for **Alle språkkoder** hvis du bruker språkkoder.</span><span class="sxs-lookup"><span data-stu-id="9dd17-110">Fill in the **Language Code** field or select the **All Language Codes** check box if you use language codes.</span></span>
5. <span data-ttu-id="9dd17-111">Fyll ut feltene **Startdato** og **Sluttdato** hvis du vil begrense perioden for bruk av den utvidete teksten.</span><span class="sxs-lookup"><span data-stu-id="9dd17-111">Fill in the **Starting Date** and **Ending Date** fields if you want to limit the dates on which the extended text is used.</span></span>
6. <span data-ttu-id="9dd17-112">I feltet **Tekst** angir du koden for den utvidete teksten.</span><span class="sxs-lookup"><span data-stu-id="9dd17-112">In the **Text** field, write the extended text.</span></span>
7. <span data-ttu-id="9dd17-113">Merk av for de aktuelle dokumenttypene du vil at de utvidete tekstene skal skrives ut på.</span><span class="sxs-lookup"><span data-stu-id="9dd17-113">Select relevant check boxes for the document types where you want the extended text printed.</span></span>
8. <span data-ttu-id="9dd17-114">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9dd17-114">Close the page.</span></span>

## <a name="to-add-an-extended-item-text-on-a-sales-order-line"></a><span data-ttu-id="9dd17-115">Legge til teksten for utvidet vare på en ordrelinje</span><span class="sxs-lookup"><span data-stu-id="9dd17-115">To add an extended item text on a sales order line</span></span>
1. <span data-ttu-id="9dd17-116">Åpne en ordre med en salgslinje for en vare som har utvidet tekst som er definert.</span><span class="sxs-lookup"><span data-stu-id="9dd17-116">Open a sales order with a sales line for an item that has extended text defined.</span></span> <span data-ttu-id="9dd17-117">Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="9dd17-117">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="9dd17-118">Velg den aktuelle linjen og velg deretter **Sett inn utv. tekster**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="9dd17-118">Select the line in question, and then choose the **Insert Ext. Text** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="9dd17-119">Se også</span><span class="sxs-lookup"><span data-stu-id="9dd17-119">See Also</span></span>
[<span data-ttu-id="9dd17-120">Definere lager</span><span class="sxs-lookup"><span data-stu-id="9dd17-120">Setting Up Inventory</span></span>](inventory-setup-inventory.md)  
<span data-ttu-id="9dd17-121">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9dd17-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>