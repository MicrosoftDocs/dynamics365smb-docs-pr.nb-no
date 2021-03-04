---
title: Tips og triks - RapidStart Services | Microsoft-dokumentasjon
description: Når du konfigurerer selskaper som bruker RapidStart Services, kan du dra nytte av noen tips og råd for å sikre en problemfri implementering.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9e9506697eacfb4bd411266078e4245e59a11353
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922420"
---
# <a name="tips-and-tricks-rapidstart-services"></a>Tips og triks: RapidStart Services

Når du konfigurerer selskaper som bruker RapidStart Services, kan du dra nytte av noen tips og råd for å sikre en problemfri implementering.  

## <a name="take-advantage-of-configuration-templates"></a>Dra nytte av konfigurasjonsmaler

Konfigurasjonsmaler kan hjelpe deg med å strømlinjeforme implementeringsprosessen. Ved å bruke disse kan du inkludere lignende kunder i segmenter og deretter utvikle en implementeringsprotokoll som behandler alle kunder i et segment på lignende måte. Dermed kan du bruke et forhåndskonfigurasjonsnivå på hvert segment og fortsette med rask implementering.  

## <a name="configuration-questionnaires"></a>Konfigurasjonsspørreskjemaer

Du bør vurdere å definere standardsvar for å angi anbefalte fremgangsmåter for å forenkle prosessen med å fylle ut konfigurasjonsspørreskjema.  

## <a name="batch-creation-of-journal-lines"></a>Masseoppretting av kladdelinjer

Vi anbefaler at du bruker verktøyene for dataflytting til å flytte kladdeposter. Ellers, hvis du bruker en kjørsel for å opprette kladdelinjer, som har et begrenset omfang og bare genererer pre-standardfelt i en kladd. Resten av kladden må deretter fylles ut manuelt.  

## <a name="migrating-transactions"></a>Flytte transaksjoner

Vi anbefaler at du flytter inngående balanser i følgende rekkefølge. <!--Be aware that you cannot insert ledger entries directly. Instead you must use journals to post the journal lines-->

1. Flytt finanskontoens inngående balanser uten å bruke finanskontoens underliggende poster. Bruk bestemte motkonti for inngående balanse der én er definert for hvert underregnskap. Definer motkontoer for å aktivere direkte bokføringer.  
2. Flytt åpne kundeposter.  <!--work on these-->
3. Flytte åpne vareposter.  
4. Flytte åpne aktivaposter.  

## <a name="make-each-package-manageable"></a>Gjøre hver pakke håndterbar

Når du bruker konfigurasjonspakker til å overføre data, deler du dataene inn i separate pakker for å gjøre det enklere å flytte dem. Hvis du for eksempel vil overføre 20 år med poster, kan importen ta mange timer og dager. Du kan i stedet dele inn dataene slik at hver pakke blir mer håndterbar. Det er for øyeblikket ingen faste regler for hva som gjør en pakke effektiv, men hvis du får problemer med å importere eller eksportere en pakke, kan du prøve å gjøre den mindre og se om det hjelper.  

## <a name="see-also"></a>Se også

[Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administrasjon](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]