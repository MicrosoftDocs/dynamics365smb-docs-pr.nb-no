---
title: Mva og avgifter for varer og tjenester i USA og Canada | Microsoft-dokumentasjon
description: Finn ut mer om GST og HST.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales tax, local
ms.date: 03/23/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e1866f5047a826f3d527267d901eb30279d5b4e4
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="sales-tax-and-goods-and-services-tax-in-canada"></a>Mva og avgifter for varer og tjenester i USA og Canada
Når en leverandør ikke har en forretningtilstedeværelse i området i Canada som kjøpet foretas i, krever leverandøren bare GST eller HST. Hvis området har PST, må kjøperen imidlertid fortsatt beregne PST og betale den direkte til området. Når det velges en PST-kode, bruker [!INCLUDE[d365fin](includes/d365fin_md.md)] denne til å beregne PST og bokføre den slik at det er en skatteplikt i både Finans og mva-posten. Mva-områdekoden som velges her bør derfor være en der bare PST er inkludert, ikke GST.  

Hvis du vil ha mer informasjon om merverdiavgift, kan du se [Mva- og mva-grupper i USA og Canada](us-finance-sales-tax.md).  

## <a name="submitting-the-gsthst-file"></a>Sende inn GST-/HST-filen
Avgiftsinformasjon i kjøpsdokumenter brukes til å generere en Internett-overføring for GST-/HST-filen som du må levere til skattemyndighetene. Denne filen inneholder GTS og HST. Filen opprettes i et TAX-filformat som kan overføres via Internett.  

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Mva- og mva-grupper i USA og Canada](us-finance-sales-tax.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

