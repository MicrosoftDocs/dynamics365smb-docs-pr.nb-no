---
title: Se gjennom og bokføre avslutningsposten for årsslutt | Microsoft-dokumentasjon
description: Beskriver hvordan du åpner kladden du angav i kjørselen Lukk resultatregnskapet, og deretter ser gjennom og bokfører avslutningsposten for årsslutt.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 1fa624ecda5914c0ba4e395025f051bc5d8cc457
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191741"
---
# <a name="post-the-year-end-closing-entry"></a>Bokføre avslutningsposten for årsslutt
Når du har brukt den satsvise jobben **Lukk resultatregnskapet** til å generere avslutningsposten eller -postene for årsslutt, må du åpne kladden du angav i kjørselen, og deretter se gjennom og bokføre postene.

## <a name="to-post-the-year-end-closing-entry"></a>Bokføre avslutningsposten for årsslutt
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finanskladd**, og velg deretter den relaterte koblingen.
2. I **Bunkenavn**-feltet, på siden **Finanskladd**, velger du bunken som inneholder avslutningspostene.
3. Se gjennom postene.
4. Velg handlingen **Bokfør** for å bokføre kladden.

> [!NOTE]  
>   Det vises en feilmelding hvis feil blir oppdaget. Hvis bokføringen lykkes, fjernes de bokførte postene fra kladden. Når bokføringen er fullført, posteres en oppføring på hver resultatregnskapskonto, slik at saldoen blir null og årsresultatet overføres til balansen.

## <a name="see-also"></a>Se også
[Lukke regnskapsperioder](year-close-account-periods.md)  
[Avslutte tablåer](year-close-books.md)  
[Lukk resultatregnskapet](year-close-income-statement.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
