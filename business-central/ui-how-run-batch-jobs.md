---
title: Opprette og kjøre en kjørsel | Microsoft-dokumentasjon
description: Du kjører kjørsler for å behandle data og oppdatere informasjon, for eksempel for å gjøre periodiske regnskapsoppgaver eller beregninger.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 10/01/2020
ms.author: solsen
ms.openlocfilehash: 04ae13561f44d544d38b04e3a881a0e707b441b4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760520"
---
# <a name="run-batch-jobs-and-xmlports"></a>Kjøre satsvise jobber og XML-porter
Satsvise jobber er rutineoppgaver som behandler data bunkevis, for eksempel den satsvise jobben **Juster valutakurser**. Det finnes kjørsler som utfører periodiske regnskapsoppgaver, som for eksempel å avslutte resultatregnskapet på slutten av et regnskapsår. Mange kjørsler utfører beregninger, for eksempel beregning av renteinntekter/-utgifter, justering av valutakurser og utregning av salgspris.

En satsvis jobb ligner på en rapport, bortsett fra at den satsvise jobben bruker resultatet av det den gjør til å oppdatere informasjonen direkte, i stedet for å skrive ut resultatene.

Du kan planlegge når en kjørsel skal kjøres. Hvis du vil ha mer informasjon, kan du se [Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).

## <a name="to-run-a-batch-job"></a>Slik kjører du en satsvis jobb
1. Hvis du vil åpne forespørselssiden for den relevante kjørselen, velger du ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angir navnet på kjørselen, og velger deretter den relaterte koblingen.
2. Hvis kjørselen har hurtigfanen **Alternativer**, fyller du ut feltene for å bestemme hva kjørselen skal gjøre.
3. Siden kan inneholde én eller flere hurtigfaner med filtre som du kan bruke til å begrense hvilke data som skal inkluderes i kjørselen. Du kan legge inn kriterier i de foreslåtte filtrene eller legge til flere filtre.
4. Velg **OK** for å starte kjørselen.

## <a name="see-also"></a>Se også
[Sortere, søke etter og filtrere oversikter](ui-enter-criteria-filters.md)  
[Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]