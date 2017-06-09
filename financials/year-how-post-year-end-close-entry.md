---
title: "Bokføre avslutningsposten for årsslutt | Microsoft-dokumentasjon"
description: "Beskriver hvordan du bokfører avslutningsposten for årsslutt."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: fe04f75ed84a959cbacd9e9d4806d43d41186edb
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-post-year-end-closing-entry"></a>Bokføre avslutningsposten for årsslutt
Når du har brukt den satsvise jobben **Lukk resultatregnskapet** til å generere avslutningsposten eller -postene for årsslutt, må du åpne kladden du angav i kjørselen, og deretter se gjennom og bokføre postene.

## <a name="to-post-the-year-end-closing-entry"></a>Bokføre avslutningsposten for årsslutt
1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Finanskladd**, og deretter velger du den beslektede koblingen.
2. I **Bunkenavn**-feltet i vinduet **Finanskladd**, velger du bunken som inneholder avslutningspostene.
3. Se gjennom postene.
4. Velg handlingen **Bokfør** for å bokføre kladden.

**Merk**: Det vises en feilmelding hvis feil blir oppdaget. Hvis bokføringen lykkes, fjernes de bokførte postene fra kladden. Når bokføringen er fullført, posteres en oppføring på hver resultatregnskapskonto, slik at saldoen blir null og årsresultatet overføres til balansen.

## <a name="see-also"></a>Se også
[Lukke regnskapsperioder](year-close-account-periods.md)  
[Avslutte tablåer](year-close-books.md)  
[Lukk resultatregnskapet](year-close-income-statement.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

