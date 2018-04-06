---
title: "Tips og råd - RapidStart Services | Microsoft-dokumentasjon"
description: "Når du konfigurerer selskaper som bruker RapidStart Services, kan du dra nytte av noen tips og råd for å sikre en problemfri implementering."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4e8dc4436b01f69292a01afbc7a5d0381b544a77
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="tips-and-tricks-rapidstart-services"></a>Tips og råd: RapidStart Services
Når du konfigurerer selskaper som bruker RapidStart Services, kan du dra nytte av noen tips og råd for å sikre en problemfri implementering.  

## <a name="take-advantage-of-configuration-templates"></a>Dra nytte av konfigurasjonsmaler  
Konfigurasjonsmaler kan hjelpe deg med å strømlinjeforme implementeringsprosessen. Ved å bruke disse kan du inkludere lignende kunder i segmenter og deretter utvikle en implementeringsprotokoll som behandler alle kunder i et segment på lignende måte. Dermed kan du bruke et forhåndskonfigurasjonsnivå på hvert segment og fortsette med rask implementering.  

## <a name="configuration-questionnaires"></a>Konfigurasjonsspørreskjemaer  
Du bør vurdere å definere standardsvar for å angi anbefalte fremgangsmåter for å forenkle prosessen med å fylle ut konfigurasjonsspørreskjema.  

## <a name="batch-creation-of-journal-lines"></a>Masseoppretting av kladdelinjer  
Vi anbefaler at du bruker verktøyene for dataflytting til å flytte kladdeposter. Ellers, hvis du bruker en kjørsel for å opprette kladdelinjer, som har et begrenset omfang og bare genererer pre-standardfelt i en kladd. Resten av kladden må deretter fylles ut manuelt.  

## <a name="migrating-transactions"></a>Flytte transaksjoner  
Vi anbefaler at du flytter inngående balanser i følgende rekkefølge.  

1.  Flytt finanskontoens inngående balanser uten å bruke finanskontoens underliggende poster. Bruk bestemte motkonti for inngående balanse der én er definert for hvert underregnskap. Definer motkontoer for å aktivere direkte bokføringer.  
2.  Flytt åpne kundeposter.  
3.  Flytte åpne vareposter.  
4.  Flytte åpne aktivaposter.  

## <a name="see-also"></a>Se også  
[Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administrasjon](admin-setup-and-administration.md)

