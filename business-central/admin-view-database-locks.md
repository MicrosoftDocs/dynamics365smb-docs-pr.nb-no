---
title: Vise databaselåser
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 1153ffc97d0f22c889ff23c5a27a8c0446b17018
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196386"
---
# <a name="viewing-database-locks"></a>Visning av databaselåser

## <a name="about-locks"></a>Om låser

Databaselåsing kontrollerer tilgang for flere brukere til de samme dataene samtidig. For å beskytte en transaksjon mot andre transaksjoner som endrer de samme dataene, setter den første transaksjonen en lås på dataene. Låsen blir værende til transaksjonen er ferdig.

Brukere kan bli blokkert fra å fullføre transaksjoner for de låste dataene. De får vanligvis en melding som angir låsebetingelsen.

## <a name="to-view-database-locks"></a>Slik viser du databaselåser

Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Databaselåser**, og velg deretter den relaterte koblingen.

Siden **Databaselåser** inneholder et øyeblikksbilde av alle gjeldende databaselåser.

Hvis du vil ha mer informasjon om databaselåsing, kan du se [Overvåke databaselåser](/dynamics365/business-central/a/dev-itpro/administration/monitor-database-locks) i hjelpen for utviklere i Business Central og IT-eksperter.

## <a name="see-also"></a>Se også

[Overvåke databaselåser](/dynamics365/business-central/a/dev-itpro/administration/monitor-database-locks) 
