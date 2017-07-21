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
ms.lasthandoff: 07/07/2017


---
# <a name="reporting-sales-tax-and-goodsservices-tax-in-canada"></a>Rapportere salgsmva og avgifter for varer/tjenester i Canada
Når en leverandør ikke har en forretningtilstedeværelse i området i Canada som kjøpet foretas i, krever leverandøren bare GST eller HST. Hvis området har PST, må kjøperen imidlertid fortsatt beregne PST og betale den direkte til området. Når det velges en PST-kode, bruker [!INCLUDE[d365fin](includes/d365fin_md.md)] denne til å beregne PST og bokføre den slik at det er en skatteplikt i både Finans og mva-posten. Mva-områdekoden som velges her bør derfor være en der bare PST er inkludert, ikke GST.  

Hvis du vil ha mer informasjon om merverdiavgift, kan du se [Mva- og mva-grupper i USA og Canada](us-finance-sales-tax.md).  

## <a name="submitting-the-gsthst-file"></a>Sende inn GST-/HST-filen
Avgiftsinformasjon i kjøpsdokumenter brukes til å generere en Internett-overføring for GST-/HST-filen som du må levere til skattemyndighetene. Denne filen inneholder GTS og HST. Filen opprettes i et TAX-filformat som kan overføres via Internett.  

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Mva- og mva-grupper i USA og Canada](us-finance-sales-tax.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

