---
title: Lukke åpne vareposter som er resultat av fast utligning i varekladden | Microsoft-dokumentasjon
description: Du kan bruke feltet **Utlignet fra-post** på siden **Varekladd** til å opprette en fast utligning manuelt mellom en inngående transaksjon og den opprinnelige utgående transaksjonen. Du kan for eksempel bruke det til å rette den utgående transaksjonen eller behandle returen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: e3f210b86168d34ec775f85b416b6d0e365cce88
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802890"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><span data-ttu-id="32502-104">Lukke åpne vareposter som er resultat av fast utligning i varekladden</span><span class="sxs-lookup"><span data-stu-id="32502-104">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>
<span data-ttu-id="32502-105">Du kan bruke feltet **Utlignet fra-post** på siden **Varekladd** til å opprette en fast utligning manuelt mellom en inngående transaksjon og den opprinnelige utgående transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="32502-105">You can use the **Applies-from Entry** field on the **Item Journal** page to create a fixed application between an inbound transaction and the original outbound transaction.</span></span> <span data-ttu-id="32502-106">Du kan for eksempel bruke det til å rette den utgående transaksjonen eller behandle returen.</span><span class="sxs-lookup"><span data-stu-id="32502-106">For example, to correct the outbound transaction or to process its return.</span></span> <span data-ttu-id="32502-107">Hvis du vil ha mer informasjon, kan du se Utlignet-fra post.</span><span class="sxs-lookup"><span data-stu-id="32502-107">For more information, see Applies-from Entry.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="32502-108">Faste utligninger som gjøres på denne måten, bruker bare kostnader, ikke antallet.</span><span class="sxs-lookup"><span data-stu-id="32502-108">Fixed applications made in this manner only apply the cost, not the quantity.</span></span> <span data-ttu-id="32502-109">Den bokførte positive vareposten vil på samme måte ikke lukke den brukte utgående posten og vil selv forbli åpen.</span><span class="sxs-lookup"><span data-stu-id="32502-109">Accordingly, the posted positive item ledger entry will not close the applied outbound entry and will itself remain open.</span></span> <span data-ttu-id="32502-110">Dette gjelder også når du bokfører en fast utligning for en positiv post til en negativ post som ikke er lukket av en vanlig positiv post – da vil både den negative og den positive posten forbli åpne.</span><span class="sxs-lookup"><span data-stu-id="32502-110">This also applies when you post a fixed application for a positive entry to a negative entry that has not been closed by a regular positive entry, then both the negative and the positive entries will remain open.</span></span>  
>   
>  <span data-ttu-id="32502-111">Dette betyr at du ikke kan lukke en lagerperiode hvis det finnes en slik post.</span><span class="sxs-lookup"><span data-stu-id="32502-111">This also means that you cannot close an inventory period if such an entry exists.</span></span>  

<span data-ttu-id="32502-112">Følgende fremgangsmåte viser hvordan du lukker slike poster ved å utføre to korrigerende bokføringer i varekladden.</span><span class="sxs-lookup"><span data-stu-id="32502-112">The following procedure shows how to close such entries by performing two corrective postings in the item journal.</span></span>  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><span data-ttu-id="32502-113">Slik lukker du åpne vareposter som er resultater fra en fast utligning i varekladden:</span><span class="sxs-lookup"><span data-stu-id="32502-113">To close open item ledger entries that result from a fixed application in the item journal</span></span>  

1.  <span data-ttu-id="32502-114">Bruk feltet **Utlignet-fra post** til å bokføre en oppjustering med tilsvarende antall.</span><span class="sxs-lookup"><span data-stu-id="32502-114">Use the **Applies-from Entry** field to post a positive adjustment with the corresponding quantity.</span></span> <span data-ttu-id="32502-115">Dette lukker den opprinnelige negative korreksjonsposten med en fast utligning.</span><span class="sxs-lookup"><span data-stu-id="32502-115">This closes the original negative entry with a fixed application.</span></span>  
2.  <span data-ttu-id="32502-116">Bruk feltet **Utligningspost** til å bokføre en nedjustering.</span><span class="sxs-lookup"><span data-stu-id="32502-116">Use the **Applies-to Entry** field to post a negative adjustment.</span></span> <span data-ttu-id="32502-117">Dette lukker den opprinnelige positive korreksjonsposten med en fast utligning.</span><span class="sxs-lookup"><span data-stu-id="32502-117">This closes the original corrective positive entry with a fixed application.</span></span>  

## <a name="see-also"></a><span data-ttu-id="32502-118">Se også</span><span class="sxs-lookup"><span data-stu-id="32502-118">See Also</span></span>  
[<span data-ttu-id="32502-119"> Fjerne varefinansposter og utligne dem på nytt</span><span class="sxs-lookup"><span data-stu-id="32502-119"> Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)  
 <span data-ttu-id="32502-120">[Behandle ordrereturer og annulleringer](sales-how-process-sales-returns-cancellations.md) </span><span class="sxs-lookup"><span data-stu-id="32502-120">[Process Sales Returns and Cancellations](sales-how-process-sales-returns-cancellations.md) </span></span>  
 <span data-ttu-id="32502-121">[Definere lagerverdisetting og kostberegning](finance-set-up-inventory-valuation-and-costing.md) </span><span class="sxs-lookup"><span data-stu-id="32502-121">[Setting Up Inventory Valuation and Costing](finance-set-up-inventory-valuation-and-costing.md) </span></span>  
 <span data-ttu-id="32502-122">[Administrere lagerkostnader](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="32502-122">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 [<span data-ttu-id="32502-123">Designdetaljer: Kostmetoder</span><span class="sxs-lookup"><span data-stu-id="32502-123">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)