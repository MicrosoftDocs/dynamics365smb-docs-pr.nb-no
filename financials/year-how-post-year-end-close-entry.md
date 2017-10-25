---
title: "Se gjennom og bokføre avslutningsposten for årsslutt | Microsoft-dokumentasjon"
description: "Beskriver hvordan du åpner kladden du angav i kjørselen Lukk resultatregnskapet, og deretter ser gjennom og bokfører avslutningsposten for årsslutt."
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
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 68017b8b031ee4bd368936b6fb4de157328d7030
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-post-the-year-end-closing-entry"></a>Bokføre avslutningsposten for årsslutt
Når du har brukt den satsvise jobben **Lukk resultatregnskapet** til å generere avslutningsposten eller -postene for årsslutt, må du åpne kladden du angav i kjørselen, og deretter se gjennom og bokføre postene.

## <a name="to-post-the-year-end-closing-entry"></a>Bokføre avslutningsposten for årsslutt
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Finanskladd**, og velg deretter den relaterte koblingen.
2. I **Bunkenavn**-feltet i vinduet **Finanskladd**, velger du bunken som inneholder avslutningspostene.
3. Se gjennom postene.
4. Velg handlingen **Bokfør** for å bokføre kladden.

> [!NOTE]  
>   Det vises en feilmelding hvis feil blir oppdaget. Hvis bokføringen lykkes, fjernes de bokførte postene fra kladden. Når bokføringen er fullført, posteres en oppføring på hver resultatregnskapskonto, slik at saldoen blir null og årsresultatet overføres til balansen.

## <a name="see-also"></a>Se også
[Lukke regnskapsperioder](year-close-account-periods.md)  
[Avslutte tablåer](year-close-books.md)  
[Lukk resultatregnskapet](year-close-income-statement.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

