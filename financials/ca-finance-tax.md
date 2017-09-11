---
title: Salgsmva i Canada | Microsoft-dokumentasjon
description: "Få informasjon om lokal salgsmva og avgifter for varer og tjenester i Canada."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales tax, local
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 571b11f4f18ffd194bdfe1d1d412bca87df4b868
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2017

---
# <a name="reporting-sales-tax-and-goodsservices-tax-in-canada"></a><span data-ttu-id="370c6-103">Rapportere salgsmva og avgifter for varer/tjenester i Canada</span><span class="sxs-lookup"><span data-stu-id="370c6-103">Reporting Sales Tax and Goods/Services Tax in Canada</span></span>
<span data-ttu-id="370c6-104">Når en leverandør ikke har en forretningtilstedeværelse i området i Canada som kjøpet foretas i, krever leverandøren bare GST eller HST.</span><span class="sxs-lookup"><span data-stu-id="370c6-104">In Canada, when a vendor does not have a business presence in the province in which purchases are made, the vendor will charge the Goods and Services Tax (GST) or Harmonized Sales Tax (HST) only.</span></span> <span data-ttu-id="370c6-105">Hvis området har PST, må kjøperen imidlertid fortsatt beregne PST og betale den direkte til området.</span><span class="sxs-lookup"><span data-stu-id="370c6-105">However, if the province has a Provincial Sales Tax (PST), then the purchaser must still calculate the PST and pay it directly to the province.</span></span> <span data-ttu-id="370c6-106">Når det velges en PST-kode, bruker [!INCLUDE[d365fin](includes/d365fin_md.md)] denne til å beregne PST og bokføre den slik at det er en skatteplikt i både Finans og mva-posten.</span><span class="sxs-lookup"><span data-stu-id="370c6-106">When a Provincial Tax Area Code is selected, [!INCLUDE[d365fin](includes/d365fin_md.md)] uses it to calculate the PST and post it so that there is a tax liability in both the general ledger and the tax entry records.</span></span> <span data-ttu-id="370c6-107">Mva-områdekoden som velges her bør derfor være en der bare PST er inkludert, ikke GST.</span><span class="sxs-lookup"><span data-stu-id="370c6-107">Therefore, the tax area code selected here should be one where only the PST is included, not the GST.</span></span>  

<span data-ttu-id="370c6-108">Hvis du vil ha mer informasjon om merverdiavgift, kan du se [Mva- og mva-grupper i USA og Canada](us-finance-sales-tax.md).</span><span class="sxs-lookup"><span data-stu-id="370c6-108">For more information about sales tax, see [Sales Tax and Tax Groups in the US and Canada](us-finance-sales-tax.md).</span></span>  

## <a name="submitting-the-gsthst-file"></a><span data-ttu-id="370c6-109">Sende inn GST-/HST-filen</span><span class="sxs-lookup"><span data-stu-id="370c6-109">Submitting the GST/HST File</span></span>
<span data-ttu-id="370c6-110">Avgiftsinformasjon i kjøpsdokumenter brukes til å generere en Internett-overføring for GST-/HST-filen som du må levere til skattemyndighetene.</span><span class="sxs-lookup"><span data-stu-id="370c6-110">The tax information in purchase documents is used to generate a GST/HST online file transfer that you must provide to the tax authorities.</span></span> <span data-ttu-id="370c6-111">Denne filen inneholder GTS og HST.</span><span class="sxs-lookup"><span data-stu-id="370c6-111">This file includes goods and services tax (GST) and harmonized sales tax (HST).</span></span> <span data-ttu-id="370c6-112">Filen opprettes i et TAX-filformat som kan overføres via Internett.</span><span class="sxs-lookup"><span data-stu-id="370c6-112">The file is created in a .tax file format, which can be transferred online.</span></span>  

## <a name="see-also"></a><span data-ttu-id="370c6-113">Se også</span><span class="sxs-lookup"><span data-stu-id="370c6-113">See Also</span></span>
[<span data-ttu-id="370c6-114">Finans</span><span class="sxs-lookup"><span data-stu-id="370c6-114">Finance</span></span>](finance.md)  
[<span data-ttu-id="370c6-115">Konfigurere finans</span><span class="sxs-lookup"><span data-stu-id="370c6-115">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="370c6-116">Mva- og mva-grupper i USA og Canada</span><span class="sxs-lookup"><span data-stu-id="370c6-116">Sales Tax and Tax Groups in the US and Canada</span></span>](us-finance-sales-tax.md)  
<span data-ttu-id="370c6-117">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="370c6-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

