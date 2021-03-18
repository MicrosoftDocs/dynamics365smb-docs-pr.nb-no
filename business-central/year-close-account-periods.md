---
title: Lukke regnskapsperioder for et regnskapsår | Microsoft-dokumentasjon
description: Beskriver hvordan du lukker regnskapsperiodene som utgjør regnskapsåret.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 336c6c8a4596aae26846d6a06091b6f5c4fff970
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386277"
---
# <a name="close-accounting-periods"></a>Lukke regnskapsperioder
Når et regnskapsår er over, må du lukke periodene som utgjør regnskapsåret.

## <a name="to-close-accounting-periods"></a>Slik lukker du regnskapsperioder
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Regnskapsperioder**, og velg deretter den relaterte koblingen.
2. På siden **Regnskapsperioder** velger du handling **Lukk år**.

    Hvis flere enn ett regnskapsår er åpne, blir det tidligste valg for lukking. Det vises en melding som sier hvilket år som lukkes, og følgene ved å lukke året forklares.
3. Hvis du vil lukke året, velger du **Ja**-knappen.

Regnskapsåret er lukket, og det er merket av i feltene **Lukket** og **Dato låst** for alle periodene i året. Regnskapsåret kan ikke åpnes på nytt, og du kan ikke slette haken i feltene **Lukket** eller **Dato låst**.

> [!NOTE]  
>   Det er ikke mulig å avslutte et regnskapsår før et nytt regnskapsår er opprettet. Merk at når et regnskapsår er avsluttet, er det ikke mulig å endre startdatoen for det etterfølgende regnskapsåret.

Selv om et regnskapsår er avsluttet, kan du bokføre finansposter i det. Postene vil, i forbindelse med bokføringen, bli merket som bokført i et avsluttet regnskapsår, og det merkes av for feltet **Etterpost**.

Når et regnskapsår er avsluttet, må du lukke resultatkontiene, og overføre årets resultat til resultatkontoen i balansen. Du kan gjenta dette hver gang du bokfører til det lukkede regnskapsåret.

## <a name="see-also"></a>Se også

[Avslutte tablåer](year-close-books.md)  
[Bokføre avslutningsposten for årsslutt](year-how-post-year-end-close-entry.md)  
[Arbeide med regnskapsperioder og regnskapsår](finance-accounting-periods-and-fiscal-years.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]