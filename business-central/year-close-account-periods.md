---
title: Lukke regnskapsperioder for et regnskapsår | Microsoft-dokumentasjon
description: Beskriver hvordan du lukker regnskapsperiodene som utgjør regnskapsåret.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2019
ms.author: jswymer
ms.openlocfilehash: ba6cd85d50f9d2b4d98fb45cbd38bcc57e08e3a2
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2313811"
---
# <a name="close-accounting-periods"></a>Lukke regnskapsperioder
Når et regnskapsår er over, må du lukke periodene som utgjør regnskapsåret.

## <a name="to-close-accounting-periods"></a>Slik lukker du regnskapsperioder
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Regnskapsperioder**, og velg deretter den relaterte koblingen.
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
[Åpne et nytt regnskapsår](finance-how-open-new-fiscal-year.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
