---
title: Designdetaljer – Lagerstyring | Microsoft-dokumentasjon
description: Dette emnet gir en oversikt over designet, begrepene og prinsippene bak funksjonene for lagerstyring i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 37c432a121c8105fbe982a4f8968094105530e3a
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802818"
---
# <a name="design-details-warehouse-management"></a><span data-ttu-id="5b8c5-103">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="5b8c5-103">Design Details: Warehouse Management</span></span>
<span data-ttu-id="5b8c5-104">Denne dokumentasjonen gir en oversikt over begrepene og prinsippene som brukes i lagerstyringsfunksjonene i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5b8c5-104">This documentation gives an overview of the concepts and principles that are used in the Warehouse Management features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="5b8c5-105">Den forklarer utformingen bak sentrale lagerfunksjoner og hvordan lagerstyring integreres med andre forsyningskjedefunksjoner.</span><span class="sxs-lookup"><span data-stu-id="5b8c5-105">It explains the design behind central warehouse features and how warehousing integrates with other supply chain features.</span></span>  

<span data-ttu-id="5b8c5-106">For å skille mellom de ulike kompleksitetsnivåene i lagerstyring er denne dokumentasjonen delt inn i to generelle grupper, grunnleggende og avanserte lagerkonfigurasjoner, som angis av titlene på delene.</span><span class="sxs-lookup"><span data-stu-id="5b8c5-106">To differentiate the different complexity levels of the warehousing, this documentation is divided into two general groups, Basic and Advanced warehouse configurations, indicated by section titles.</span></span> <span data-ttu-id="5b8c5-107">Denne enkle differensieringen dekker ulike kompleksitetsnivåer, som defineres av produktgranuler og lokasjonsoppsettet.</span><span class="sxs-lookup"><span data-stu-id="5b8c5-107">This simple differentiation covers different complexity levels as defined by product granules and location setup.</span></span> <span data-ttu-id="5b8c5-108">Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Lagerstyringsoppsett](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="5b8c5-108">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="5b8c5-109">I denne delen</span><span class="sxs-lookup"><span data-stu-id="5b8c5-109">In This Section</span></span>  
[<span data-ttu-id="5b8c5-110">Designdetaljer: Lageroversikt</span><span class="sxs-lookup"><span data-stu-id="5b8c5-110">Design Details: Warehouse Overview</span></span>](design-details-warehouse-overview.md)  
[<span data-ttu-id="5b8c5-111">Designdetaljer: Lageroppsett</span><span class="sxs-lookup"><span data-stu-id="5b8c5-111">Design Details: Warehouse Setup</span></span>](design-details-warehouse-setup.md)  
[<span data-ttu-id="5b8c5-112">Designdetaljer: Inngående lagerflyt</span><span class="sxs-lookup"><span data-stu-id="5b8c5-112">Design Details: Inbound Warehouse Flow</span></span>](design-details-inbound-warehouse-flow.md)  
[<span data-ttu-id="5b8c5-113">Designdetaljer: Interne lagerflyter</span><span class="sxs-lookup"><span data-stu-id="5b8c5-113">Design Details: Internal Warehouse Flows</span></span>](design-details-internal-warehouse-flows.md)  
[<span data-ttu-id="5b8c5-114">Designdetaljer: Tilgjengelighet i lageret</span><span class="sxs-lookup"><span data-stu-id="5b8c5-114">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)  
[<span data-ttu-id="5b8c5-115">Designdetaljer: Utgående lagerflyt</span><span class="sxs-lookup"><span data-stu-id="5b8c5-115">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="5b8c5-116">Designdetaljer: Integrasjon med lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="5b8c5-116">Design Details: Integration with Inventory</span></span>](design-details-integration-with-inventory.md)