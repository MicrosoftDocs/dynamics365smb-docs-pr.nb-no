---
title: Lukke resultatregnskapskonti | Microsoft-dokumentasjon
description: "Ved årsavslutning må du kjøre kjørselen Lukk resultatregnskapet for å lukke regnskapsperiodene som utgjør regnskapsåret."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 20bc194772d1aa0a8caadf0605911d0a214a9ab2
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="close-income-statement-accounts"></a>Lukke resultatregnskapskonti
Når et regnskapsår er over, må du lukke periodene som utgjør regnskapsåret. Hvis du vil gjøre dette, kjører du den satsvise jobben **Lukk resultatregnskapet**. Denne jobben overfører årets resultat til en konto i balansen og lukke resultatregnskapskontoene. Dette gjør du ved å opprette linjer i en kladd som du deretter kan bokføre.

## <a name="to-run-the-close-income-statement-batch-job"></a>Kjøre den satsvise jobben Lukk resultatregnskapet
1. Avslutte regnskapsåret. Regnskapsåret må avsluttes før den satsvise jobben kan kjøres. Hvis du vil ha mer informasjon, kan du se [Avslutte regnskapsperioder](year-close-account-periods.md).
2. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lukk resultatregnskap**, og velg deretter den relaterte koblingen.
3. Velg **OK** for å kjøre kjørselen.

## <a name="about-the-close-income-statement-batch-job"></a>Den satsvise jobben Lukk resultatregnskapet
Kjørselen behandler alle finanskonti av typen Resultatregnskap og oppretter poster som utsletter deres respektive saldoer. Det vil si at hver post er summen av alle finansposter på kontoen i regnskapsåret. Disse nye postene plasseres i en kladd der du må angi en motkonto, konto for fri egenkapital, i balansen før du bokfører. Når du bokfører kladden, bokføres en post på hver resultatkonto slik at saldoen blir null og samtidig overføres årsresultatet til balansen.

Du må bokføre kladden selv. Kjørselen bokfører ikke postene automatisk, med unntak av når en tilleggsrapporteringsvaluta brukes. Når en tilleggsrapporteringsvaluta brukes, bokfører den satsvise jobben poster direkte mot Finans.

Datoen på linjene som kjørselen setter inn i kladden, er alltid en sluttdato for regnskapsåret. Avslutningsdatoen er en fiktiv dato mellom siste dag i det gamle regnskapsåret og første dag i det nye. Fordelen med å bokføre på en avslutningsdato er at du ivaretar riktig saldo for de ordinære datoene i regnskapsåret.

Den satsvise jobben **Lukk resultatregnskapet** kan brukes flere ganger. Du kan bokføre i et tidligere år, selv etter at resultatkontiene er avsluttet, hvis du kjører kjørselen på nytt.

## <a name="see-also"></a>Se også
[Avslutte tablåer](year-close-books.md)  
[Bokføre avslutningsposten for årsslutt](year-how-post-year-end-close-entry.md)  
[Åpne et nytt regnskapsår](finance-how-open-new-fiscal-year.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

