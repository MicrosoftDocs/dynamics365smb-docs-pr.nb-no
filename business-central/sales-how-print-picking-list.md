---
title: Skrive ut en lagerplukkliste fra en ordre
description: Du kan skrive ut en plukkliste for lager direkte fra en ordre, salg, faktura og andre utgående salgsdokumenter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/27/2020
ms.author: edupont
ms.openlocfilehash: fadf974c41b34a5beb7b3b313847cc6a5bfcec78
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2020
ms.locfileid: "3781638"
---
# <a name="print-the-picking-list"></a><span data-ttu-id="ddeef-103">Skrive ut plukklisten</span><span class="sxs-lookup"><span data-stu-id="ddeef-103">Print the Picking List</span></span>
<span data-ttu-id="ddeef-104">Du kan skrive ut en plukkliste for lager direkte fra en ordre, salgsfaktura eller andre dokumenter som igangsetter levering av varer.</span><span class="sxs-lookup"><span data-stu-id="ddeef-104">You can print an inventory picking list directly from a sales order, a sales invoice, or any other document that initiates shipment of items.</span></span>

<span data-ttu-id="ddeef-105">Denne rapporten brukes vanligvis i selskaper uten egen funksjonalitet for lagerstyring, slik at en lagerarbeider ganske enkelt kan vise eller skrive ut plukklisten fra det tilknyttede salgsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="ddeef-105">This report is typically used in companies without dedicated functionality for warehouse management, so that an inventory worker can simply view or print the picking list from the related sales document.</span></span> <span data-ttu-id="ddeef-106">I selskaper med høyere volum eller mer komplekse prosesser, planlegges plukking og utføres i egne lagerdokumenter.</span><span class="sxs-lookup"><span data-stu-id="ddeef-106">In companies with higher volume or more complex processes, picking is planned and performed in dedicated warehouse documents.</span></span> <span data-ttu-id="ddeef-107">Hvis du vil ha mer informasjon, kan du se [Plukke varer](warehouse-pick-items.md).</span><span class="sxs-lookup"><span data-stu-id="ddeef-107">For more information, see [Pick Items](warehouse-pick-items.md).</span></span>

## <a name="to-print-a-picking-list-from-a-sales-order"></a><span data-ttu-id="ddeef-108">Skrive ut en plukkliste fra en ordre</span><span class="sxs-lookup"><span data-stu-id="ddeef-108">To print a picking list from a sales order</span></span>  
<span data-ttu-id="ddeef-109">Følgende fremgangsmåte er basert på en ordre.</span><span class="sxs-lookup"><span data-stu-id="ddeef-109">The following procedure is based on a sales order.</span></span> <span data-ttu-id="ddeef-110">Fremgangsmåten er de samme for alle salgsdokumenter som kan brukes til å starte levering av varer.</span><span class="sxs-lookup"><span data-stu-id="ddeef-110">The steps are similar for all sales documents that can be used to initiate shipment of items.</span></span>

1. <span data-ttu-id="ddeef-111">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="ddeef-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ddeef-112">Åpne ordren du vil plukke varer for.</span><span class="sxs-lookup"><span data-stu-id="ddeef-112">Open the sales order that you want to pick items for.</span></span>  
3. <span data-ttu-id="ddeef-113">Velg **Rapport**-handlingen, og velg deretter **Plukklisten etter ordre**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="ddeef-113">Choose the **Report** action, and then choose the **Picking List by Order** action.</span></span>  
4. <span data-ttu-id="ddeef-114">Velg **Skriv ut** for å skrive ut plukklisten, eller velg **Forhåndsvisning** for å vise den på skjermen.</span><span class="sxs-lookup"><span data-stu-id="ddeef-114">Choose the **Print** button to print the picking list or choose the **Preview** button to view it on the screen.</span></span>

<span data-ttu-id="ddeef-115">Du kan også lagre plukklisten som et dokument, for eksempel for å sende til noen, eller legge til som et vedlegg i ordren.</span><span class="sxs-lookup"><span data-stu-id="ddeef-115">You can also save the picking list as a document, for example, to send to someone or to add as an attachment to the sales order.</span></span> <span data-ttu-id="ddeef-116">Se [Behandle vedlegg, koblinger og merknader på kort og dokumenter](ui-how-add-link-to-record.md) hvis du vil ha mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="ddeef-116">For more information, see [Manage Attachments, Links, and Notes on Cards and Documents](ui-how-add-link-to-record.md).</span></span>

> [!NOTE]
> <span data-ttu-id="ddeef-117">Hvis du brukte **Utfold stykkliste**-funksjonen på ordren, vises bare komponentene for den tilknyttede monteringsvaren i rapporten.</span><span class="sxs-lookup"><span data-stu-id="ddeef-117">If you used the **Explode BOM** function on the sales order, then only the components of the related assembly item are shown in the report.</span></span> <span data-ttu-id="ddeef-118">Hvis du vil ha mer informasjon, kan du se [Arbeide med stykklister](inventory-how-work-BOMs.md).</span><span class="sxs-lookup"><span data-stu-id="ddeef-118">For more information, see [Work with Bills of Material](inventory-how-work-BOMs.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ddeef-119">Se også</span><span class="sxs-lookup"><span data-stu-id="ddeef-119">See Also</span></span>  
[<span data-ttu-id="ddeef-120">Lager</span><span class="sxs-lookup"><span data-stu-id="ddeef-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="ddeef-121">Plukke varer</span><span class="sxs-lookup"><span data-stu-id="ddeef-121">Pick Items</span></span>](warehouse-pick-items.md)  
<span data-ttu-id="ddeef-122">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ddeef-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>   
