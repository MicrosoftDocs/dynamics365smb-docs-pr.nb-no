---
title: Lukk vareposter som kom fra bruk av fast utligning
description: Finn ut hvordan du kan opprette en fast utligning manuelt mellom en inngående transaksjon og den opprinnelige utgående transaksjonen i varekladden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/14/2020
ms.author: edupont
ms.openlocfilehash: 2cc663d580da4738247b9fcdbe5fc4504c37fa73
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5013874"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><span data-ttu-id="d295a-103">Lukke åpne vareposter som er resultat av fast utligning i varekladden</span><span class="sxs-lookup"><span data-stu-id="d295a-103">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>

<span data-ttu-id="d295a-104">Du kan bruke feltet **Utlignet fra-post** på siden **Varekladd** til å opprette en fast utligning manuelt mellom en inngående transaksjon og den opprinnelige utgående transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="d295a-104">You can use the **Applies-from Entry** field on the **Item Journal** page to create a fixed application between an inbound transaction and the original outbound transaction.</span></span> <span data-ttu-id="d295a-105">Du kan for eksempel bruke det til å rette den utgående transaksjonen eller behandle returen.</span><span class="sxs-lookup"><span data-stu-id="d295a-105">For example, to correct the outbound transaction or to process its return.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="d295a-106">Faste utligninger som gjøres på denne måten, bruker bare kostnader, ikke antallet.</span><span class="sxs-lookup"><span data-stu-id="d295a-106">Fixed applications made in this manner only apply the cost, not the quantity.</span></span> <span data-ttu-id="d295a-107">Den bokførte positive vareposten vil på samme måte ikke lukke den brukte utgående posten og vil selv forbli åpen.</span><span class="sxs-lookup"><span data-stu-id="d295a-107">Accordingly, the posted positive item ledger entry will not close the applied outbound entry and will itself remain open.</span></span> <span data-ttu-id="d295a-108">Dette gjelder også når du bokfører en fast utligning for en positiv post til en negativ post som ikke er lukket av en vanlig positiv post – da vil både den negative og den positive posten forbli åpne.</span><span class="sxs-lookup"><span data-stu-id="d295a-108">This also applies when you post a fixed application for a positive entry to a negative entry that has not been closed by a regular positive entry, then both the negative and the positive entries will remain open.</span></span>  
>
> <span data-ttu-id="d295a-109">Dette betyr at du ikke kan lukke en lagerperiode hvis det finnes en slik post.</span><span class="sxs-lookup"><span data-stu-id="d295a-109">This also means that you cannot close an inventory period if such an entry exists.</span></span>  

<span data-ttu-id="d295a-110">Under visse betingelser kan du endre og utligne utligningsposter på nytt ved å bruke siden **Utligningsforslag**.</span><span class="sxs-lookup"><span data-stu-id="d295a-110">You can change and reapply application entries under certain conditions by using the **Application Worksheet** page.</span></span>  

<span data-ttu-id="d295a-111">Følgende fremgangsmåte viser hvordan du lukker slike poster ved å utføre to korrigerende bokføringer i varekladden.</span><span class="sxs-lookup"><span data-stu-id="d295a-111">The following procedure shows how to close such entries by performing two corrective postings in the item journal.</span></span>  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><span data-ttu-id="d295a-112">Slik lukker du åpne vareposter som er resultater fra en fast utligning i varekladden:</span><span class="sxs-lookup"><span data-stu-id="d295a-112">To close open item ledger entries that result from a fixed application in the item journal</span></span>  

1. <span data-ttu-id="d295a-113">Bruk feltet **Utlignet-fra post** til å bokføre en oppjustering med tilsvarende antall.</span><span class="sxs-lookup"><span data-stu-id="d295a-113">Use the **Applies-from Entry** field to post a positive adjustment with the corresponding quantity.</span></span> <span data-ttu-id="d295a-114">Dette lukker den opprinnelige negative korreksjonsposten med en fast utligning.</span><span class="sxs-lookup"><span data-stu-id="d295a-114">This closes the original negative entry with a fixed application.</span></span>  

    <span data-ttu-id="d295a-115">Feltet **Utlignet fra-post** angir nummeret på den utgående finansposten som har kostnader som er videresendt til den inngående vareposten, når du bokfører en inngående transaksjon av typen **Oppjustering** eller **Kjøp** med varekladden.</span><span class="sxs-lookup"><span data-stu-id="d295a-115">The **Applies-from Entry** field specifies the number of the outbound item ledger entry whose cost is forwarded to the inbound item ledger entry when you post an inbound transaction of type **Positive Adjmt.** or **Purchase** with the item journal.</span></span>  
2. <span data-ttu-id="d295a-116">Bruk feltet **Utligningspost** til å bokføre en nedjustering.</span><span class="sxs-lookup"><span data-stu-id="d295a-116">Use the **Applies-to Entry** field to post a negative adjustment.</span></span> <span data-ttu-id="d295a-117">Dette lukker den opprinnelige positive korreksjonsposten med en fast utligning.</span><span class="sxs-lookup"><span data-stu-id="d295a-117">This closes the original corrective positive entry with a fixed application.</span></span>  

    <span data-ttu-id="d295a-118">Feltet **Utligningspost** angir om antallet på varekladdelinjen skal utlignes mot et bilag som allerede er bokført.</span><span class="sxs-lookup"><span data-stu-id="d295a-118">The **Applies-to Entry** field specifies if the quantity in the item journal line should be applied to an already-posted document.</span></span> <span data-ttu-id="d295a-119">Hvis dette er tilfelle, angir du løpenummeret på vareposten som varekladdelinjen skal utlignes mot.</span><span class="sxs-lookup"><span data-stu-id="d295a-119">If this is the case, enter the entry number of the item ledger entry to which the item journal line should be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="d295a-120">Se også</span><span class="sxs-lookup"><span data-stu-id="d295a-120">See Also</span></span>

[<span data-ttu-id="d295a-121">Fjerne varefinansposter og utligne dem på nytt</span><span class="sxs-lookup"><span data-stu-id="d295a-121">Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)  
[<span data-ttu-id="d295a-122">Behandle ordrereturer og annulleringer</span><span class="sxs-lookup"><span data-stu-id="d295a-122">Process Sales Returns and Cancellations</span></span>](sales-how-process-sales-returns-cancellations.md)  
[<span data-ttu-id="d295a-123">Definere lagerverdisetting og kostberegning</span><span class="sxs-lookup"><span data-stu-id="d295a-123">Setting Up Inventory Valuation and Costing</span></span>](finance-set-up-inventory-valuation-and-costing.md)  
[<span data-ttu-id="d295a-124">Administrere lagerkostnader</span><span class="sxs-lookup"><span data-stu-id="d295a-124">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="d295a-125">Designdetaljer: Kostmetoder</span><span class="sxs-lookup"><span data-stu-id="d295a-125">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)
