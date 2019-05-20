---
title: Norsk mva-rapportering
description: Forbedringer i den norske versjonen gjør det mulig for deg å beregne og rapportere mva til de norske skattemyndighetene.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8a2ea2ee6021daf0469b24cac33d149ed998f432
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245395"
---
# <a name="norwegian-vat-reporting"></a><span data-ttu-id="04a34-103">Norsk mva-rapportering</span><span class="sxs-lookup"><span data-stu-id="04a34-103">Norwegian VAT Reporting</span></span>
[!INCLUDE[d365fin](../../includes/d365fin_md.md)]<span data-ttu-id="04a34-104">../../inkluderer orbedringer i den norske versjonen som gjør det mulig for deg å beregne og rapportere mva til de norske skattemyndighetene.</span><span class="sxs-lookup"><span data-stu-id="04a34-104">../../includes Norwegian enhancements that allow you to calculate and report VAT to the Norwegian tax authorities.</span></span>  

<span data-ttu-id="04a34-105">Dette emnet forklarer de vanlige trinnene du skal følge når du rapporterer norsk mva.</span><span class="sxs-lookup"><span data-stu-id="04a34-105">This topic shows the typical steps that you should follow when reporting Norwegian VAT.</span></span>  

## <a name="print-the-trade-settlement"></a><span data-ttu-id="04a34-106">Skrive ut omsetningsoppgaven</span><span class="sxs-lookup"><span data-stu-id="04a34-106">Print the Trade Settlement</span></span>  
<span data-ttu-id="04a34-107">Først må du må skrive ut omsetningsoppgaven.</span><span class="sxs-lookup"><span data-stu-id="04a34-107">First, you must print the trade settlement.</span></span> <span data-ttu-id="04a34-108">Bruk **Omsetningsoppgaven**-rapporten til å skrive ut omsetningsoppgaven som kreves av skattemyndighetene.</span><span class="sxs-lookup"><span data-stu-id="04a34-108">Use the **Tradesettlement** report to print the trade settlement that is required by the authorities.</span></span>  

<span data-ttu-id="04a34-109">Denne rapporten skriver ut detaljerte opplysninger om bokført mva i den angitte perioden.</span><span class="sxs-lookup"><span data-stu-id="04a34-109">This report prints detailed information about the posted VAT in the specified period.</span></span> <span data-ttu-id="04a34-110">Den faktisk omsetningsoppgaven som skal rapporteres skrives ut på siste side av rapporten.</span><span class="sxs-lookup"><span data-stu-id="04a34-110">On the last page of the report, the actual trade settlement to report is printed.</span></span>  

<span data-ttu-id="04a34-111">Denne rapporten kan skrives ut så mange ganger som nødvendig.</span><span class="sxs-lookup"><span data-stu-id="04a34-111">This report can be printed as many times as required.</span></span> <span data-ttu-id="04a34-112">Ingen bokføring eller andre endringer utføres på dataene når du bruker denne rapporten.</span><span class="sxs-lookup"><span data-stu-id="04a34-112">No posting or other changes are made to the data when you use this report.</span></span>  

## <a name="check-the-trade-settlement"></a><span data-ttu-id="04a34-113">Sjekk omsetningsoppgaven</span><span class="sxs-lookup"><span data-stu-id="04a34-113">Check the Trade Settlement</span></span>  
<span data-ttu-id="04a34-114">Så må du må sjekke omsetningsoppgaven.</span><span class="sxs-lookup"><span data-stu-id="04a34-114">Next, you must check the trade settlement.</span></span> <span data-ttu-id="04a34-115">Kontroller at beløpene i omsetningsoppgaven er riktig, og foreta eventuelle justeringer.</span><span class="sxs-lookup"><span data-stu-id="04a34-115">Verify that the amounts in the trade settlement are correct, and make any necessary adjustments.</span></span>  

## <a name="post-vat"></a><span data-ttu-id="04a34-116">Bokfør Mva.</span><span class="sxs-lookup"><span data-stu-id="04a34-116">Post VAT</span></span>  
<span data-ttu-id="04a34-117">Hvis informasjonen i omsetningsoppgaven er riktig, er det siste trinnet å bokføre mva ved hjelp av rapporten **Beregn og Bokfør mva-oppgjør**.</span><span class="sxs-lookup"><span data-stu-id="04a34-117">If the information in the trade settlement is correct, the final step is to post the VAT using the **Calc. and Post VAT Settlement** report.</span></span> <span data-ttu-id="04a34-118">Det er nødvendig at du manuelt angi riktig mva-periode i feltene **Startdato** og **Sluttdato**.</span><span class="sxs-lookup"><span data-stu-id="04a34-118">It is required that you manually specify the correct VAT period in the **Starting Date** and **Ending Date** fields.</span></span> <span data-ttu-id="04a34-119">Vanligvis korresponderer disse datoene til perioden som tidligere er angitt i **Omsetningsoppgaven**-rapporten.</span><span class="sxs-lookup"><span data-stu-id="04a34-119">Generally, these dates correspond to the period previously specified in the **Tradesettlement** report.</span></span>  

<span data-ttu-id="04a34-120">Når du bruker denne rapporten, kan du velge å ikke bokføre hvis du vil kontrollere resultatene før du faktisk bokfører mva.</span><span class="sxs-lookup"><span data-stu-id="04a34-120">When using this report, you can decide not to post if you want to check the results before you actually post VAT.</span></span>  

<span data-ttu-id="04a34-121">Når du bokfører mva., opprettes den tilsvarende mva-perioden, og merkes som lukket i **Oppgjort mva-periode**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="04a34-121">When posting VAT, the corresponding VAT period is created and marked as closed in the **Settled VAT Period** table.</span></span> <span data-ttu-id="04a34-122">Hvis du angir en periode som ikke svarer til én av de vanlige seks norske mva periodene, avsluttes alle periodene som berøres av den angitte periode.</span><span class="sxs-lookup"><span data-stu-id="04a34-122">If you specify a period that does not correspond to one of the typical six Norwegian VAT periods, all periods that are affected by the specified date interval are closed.</span></span>  

## <a name="see-also"></a><span data-ttu-id="04a34-123">Se også</span><span class="sxs-lookup"><span data-stu-id="04a34-123">See Also</span></span>  
 [<span data-ttu-id="04a34-124">Funksjonalitet som er spesifikk for norske brukere</span><span class="sxs-lookup"><span data-stu-id="04a34-124">Norway Local Functionality</span></span>](norway-local-functionality.md)
