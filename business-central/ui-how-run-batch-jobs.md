---
title: Kjøre satsvise jobber og XML-porter
description: Du kjører kjørsler for å behandle data og oppdatere informasjon, for eksempel for å gjøre periodiske regnskapsoppgaver eller beregninger.
author: SusanneWindfeldPedersen
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.search.form: 672, 676, 682, 9020, 9022, 9026, 9027, 9030, 9000, 9004, 9005, 9018, 9006, 9007, 9010, 9016, 9017
ms.date: 04/01/2021
ms.author: solsen
ms.openlocfilehash: 7d06ebd368f42c142d7cb222ee378da79706132e
ms.sourcegitcommit: cdb57f14960f58b1d36a1b373fbf35dfed5fad9e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/23/2022
ms.locfileid: "8335399"
---
# <a name="run-batch-jobs-and-xmlports"></a>Kjøre satsvise jobber og XML-porter

Satsvise jobber er rutineoppgaver som behandler data bunkevis, for eksempel den satsvise jobben **Juster valutakurser**. Det finnes kjørsler som utfører periodiske regnskapsoppgaver, som for eksempel å avslutte resultatregnskapet på slutten av et regnskapsår. Mange kjørsler utfører beregninger, for eksempel beregning av renteinntekter/-utgifter, justering av valutakurser og utregning av salgspris.

En satsvis jobb ligner på en rapport, bortsett fra at den satsvise jobben bruker resultatet av det den gjør til å oppdatere informasjonen direkte, i stedet for å skrive ut resultatene.

Du kan planlegge når en kjørsel skal kjøres. Hvis du vil ha mer informasjon, kan du se [Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).

## <a name="to-run-a-batch-job"></a>Slik kjører du en satsvis jobb
1. Hvis du vil åpne forespørselssiden for den aktuelle kjørselen, velger du ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriver inn navnet på kjørselen, og deretter velger du den tilknyttede koblingen.
2. Hvis kjørselen har hurtigfanen **Alternativer**, fyller du ut feltene for å bestemme hva kjørselen skal gjøre.
3. Siden kan inneholde én eller flere hurtigfaner med filtre som du kan bruke til å begrense hvilke data som skal inkluderes i kjørselen. Du kan legge inn kriterier i de foreslåtte filtrene eller legge til flere filtre.
4. Velg **OK** for å starte kjørselen.

## <a name="see-also"></a>Se også
[Sortere, søke etter og filtrere oversikter](ui-enter-criteria-filters.md)  
[Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]