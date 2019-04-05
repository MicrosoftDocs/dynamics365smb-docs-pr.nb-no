---
title: Kriterier for overføring av finansposter til kostposter | Microsoft-dokumentasjon
description: Det er viktig å forstå kriteriene for overføring av finansposter til kostposter. Under overføringen bruker kjørselen **Overfør finansposter til KR** følgende kriterier for å avgjøre om og hvordan finanspostene er overført.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 6e5fcfedbb899633f61c05b0b8b5ec8125112d65
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802765"
---
# <a name="criteria-for-transferring-general-ledger-entries-to-cost-entries"></a>Kriterier for overføring av finansposter til kostposter
Det er viktig å forstå kriteriene for overføring av finansposter til kostposter. Under overføringen bruker kjørselen **Overfør finansposter til KR** følgende kriterier for å avgjøre om og hvordan finanspostene er overført.  

Finansposter overføres hvis følgende er tilfelle:  

-   Postene har dimensjonsverdier som tilsvarer enten et kostsenter eller et kostobjekt.  
-   Postene har dimensjonsverdier som tilsvarer et kostsenter og et kostobjekt. For disse postene har kostsenteret forrang. Dette bidrar til å unngå en situasjon der en kosttype vises i både et kostobjekt og et kostsenter og telles derfor to ganger i statistikken.  
-   Bilagsnummeret i postene er tomt, slik at det vises med bilagsnummeret 0000 i kostpostene.  
-   Postene overføres til en kosttype som tillater kombinerte poster, og disse postene overføres som en kombinert post enten månedlig eller daglig.  

Finansposter overføres ikke hvis følgende er tilfelle:  

-   Postene har dimensjonsverdier som ikke tilsvarer et kostsenter eller et kostobjekt.  
-   Postene har et beløp på null.  
-   Postene har en finanskonto som er slettet.  
-   Postene har en finanskonto som ikke er av typen **Resultatregnskap**.  
-   Postene har en finanskonto som det ikke er tilordnet en kosttype for.  
-   Postene har en bokføringsdato som er tidligere enn **Startdato for finansoverføring**.  
-   Postene er bokført med en avslutningsdato. Dette er vanligvis poster som tilbakestiller saldoen i resultatregnskapet på slutten av året.  

## <a name="see-also"></a>Se også  
[Gjøre rede for kostnader](finance-manage-cost-accounting.md)  
 [Overføre finansposter til kostposter](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md)   
 [Overføre og bokføre kostposter](finance-transfer-and-post-cost-entries.md)   
 [Om kostregnskap](finance-about-cost-accounting.md)  
 [Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
