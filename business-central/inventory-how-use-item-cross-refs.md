---
title: Bruke varekryssreferanser
description: Definer referanser mellom beskrivelsene som du og leverandøren bruker for en vare, slik at du kan sette inn leverandørens varebeskrivelse i kjøpsdokumenter.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 01/12/2021
ms.author: edupont
ms.openlocfilehash: 2f500d7df80235b8f092fc3f0a7ae8fd27cd8aea
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377626"
---
# <a name="use-item-cross-references"></a><span data-ttu-id="c2966-103">Bruke varekryssreferanser</span><span class="sxs-lookup"><span data-stu-id="c2966-103">Use Item Cross References</span></span>
<span data-ttu-id="c2966-104">Hvis du har definert en kryssreferanse mellom varebeskrivelsen som du bruker for en vare, og beskrivelsen som leverandøren av varen bruker, settes leverandørvarebeskrivelsen automatisk inn på kjøpsdokumenter for leverandøren når du fyller ut **Kryssreferansenr.**</span><span class="sxs-lookup"><span data-stu-id="c2966-104">If you set up a cross reference between the item description that you use for an item and the description that the vendor of that item uses, then the vendor's item description is automatically inserted on purchase documents for the vendor when you fill in the **Cross-Reference No.**</span></span> <span data-ttu-id="c2966-105">.</span><span class="sxs-lookup"><span data-stu-id="c2966-105">field.</span></span> <span data-ttu-id="c2966-106">Den samme funksjonaliteten gjelder for kundevarenumre på salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="c2966-106">The same functionality applies for customer item numbers on sales documents.</span></span>

<span data-ttu-id="c2966-107">Den følgende fremgangsmåten beskriver hvordan du bruker varekryssreferanser på kjøpssiden.</span><span class="sxs-lookup"><span data-stu-id="c2966-107">The following procedures describe how to use item cross references on the purchase side.</span></span> <span data-ttu-id="c2966-108">Trinnene er de samme for salgssiden.</span><span class="sxs-lookup"><span data-stu-id="c2966-108">The steps are similar for the sales side.</span></span>

> [!NOTE]
> <span data-ttu-id="c2966-109">Det blir mer vanlig at vare-ID-er, for eksempel GTIN eller GUID, inneholder 30 eller flere tegn, som er mer enn den gjeldende funksjonen for varekryssreferanser kan håndtere.</span><span class="sxs-lookup"><span data-stu-id="c2966-109">It's becoming more common for item identifiers such as GTINs or GUIDs to contain 30 or more characters, which is more than the current feature for item cross references can handle.</span></span> <span data-ttu-id="c2966-110">Hvis du må bruke referanser som inneholder mer enn 30 tegn, kan systemansvarlig aktivere funksjonen **Skriv lengre varereferanser** på siden [Funksjonsstyring](https://businesscentral.dynamics.com/?page=2610) (koblingen krever at du har en [!INCLUDE[prod_short](includes/prod_short.md)]-leietaker).</span><span class="sxs-lookup"><span data-stu-id="c2966-110">If you need to use references that contain more than 30 characters, your administrator can turn on the **Write longer item references** feature on the [Feature Management](https://businesscentral.dynamics.com/?page=2610) page (link requires that you have a [!INCLUDE[prod_short](includes/prod_short.md)] tenant).</span></span> <span data-ttu-id="c2966-111">Hvordan du bruker referanser endres ikke, men navnet på ting som sider og knapper vil bli endret.</span><span class="sxs-lookup"><span data-stu-id="c2966-111">How you use references doesn't change, but the names of things like pages and buttons will.</span></span> <span data-ttu-id="c2966-112">Siden **Varekryssreferanseposter** vil for eksempel bli siden **Varereferanseposter**.</span><span class="sxs-lookup"><span data-stu-id="c2966-112">For example, the **Item Cross-Reference Entries** page will become the **Item Reference Entries** page.</span></span>

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a><span data-ttu-id="c2966-113">Slik definerer du en varekryssreferanse til en leverandørs varebeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c2966-113">To set up an item cross reference to a vendor's item description</span></span>

1. <span data-ttu-id="c2966-114">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="c2966-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="c2966-115">Åpne kortet for en vare som du vil opprette en kryssreferanse for til varebeskrivelsen som leverandøren bruker for denne varen.</span><span class="sxs-lookup"><span data-stu-id="c2966-115">Open the card for an item for which you want to create a cross reference to the item description that the vendor uses for that item.</span></span>
3. <span data-ttu-id="c2966-116">Velg **Kryssreferanser**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="c2966-116">Choose the **Cross References** action.</span></span>

     <span data-ttu-id="c2966-117">Hvis du ikke finner handlingen **Kryssreferanser**, velger du å vise flere alternativer og finner det under **Relatert** > **Vare**.</span><span class="sxs-lookup"><span data-stu-id="c2966-117">If you cannot find the **Cross References** action, choose to view more options, and then find it under **Related** > **Item**.</span></span>
  
4. <span data-ttu-id="c2966-118">På en ny linje på siden **Varekryssreferanseposter** fyller du ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="c2966-118">On a new line on the **Item Cross-Reference Entries** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="c2966-119">.</span><span class="sxs-lookup"><span data-stu-id="c2966-119">.</span></span>

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a><span data-ttu-id="c2966-120">Slik angir du en leverandørs varebeskrivelse på en bestilling</span><span class="sxs-lookup"><span data-stu-id="c2966-120">To enter a vendor's item description on a purchase order</span></span>

1. <span data-ttu-id="c2966-121">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bestillinger**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="c2966-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="c2966-122">Opprett en bestilling for leverandøren du angav en varekryssreferanse for i den forrige prosedyren.</span><span class="sxs-lookup"><span data-stu-id="c2966-122">Create a purchase order for the vendor that you set up an item cross reference for in the previous procedure.</span></span>
3. <span data-ttu-id="c2966-123">Opprett en bestillingslinje for varen som du angav en varekryssreferanse for i den forrige prosedyren.</span><span class="sxs-lookup"><span data-stu-id="c2966-123">Create a purchase line for the item that you set up an item cross reference for in the previous procedure.</span></span>
4. <span data-ttu-id="c2966-124">I **Kryssreferansetypenr.**</span><span class="sxs-lookup"><span data-stu-id="c2966-124">In the **Cross-Reference No.**</span></span> <span data-ttu-id="c2966-125">-feltet velger du varekryssreferansen du har opprettet, og deretter velger du **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="c2966-125">field, select the item cross reference that you have created, and then choose the **OK** button.</span></span>

<span data-ttu-id="c2966-126">**Beskrivelse**-feltet på linjen overskrives med leverandørens varebeskrivelse, slik den er angitt opp på varekryssreferanseposten.</span><span class="sxs-lookup"><span data-stu-id="c2966-126">The **Description** field on the line is overwritten with the vendor's item description, as set up on the item cross-reference entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2966-127">Se også</span><span class="sxs-lookup"><span data-stu-id="c2966-127">See Also</span></span>
[<span data-ttu-id="c2966-128">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="c2966-128">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="c2966-129">Lager</span><span class="sxs-lookup"><span data-stu-id="c2966-129">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="c2966-130">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c2966-130">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]