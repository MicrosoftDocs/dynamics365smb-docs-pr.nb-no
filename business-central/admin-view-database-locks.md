---
title: Vise databaselåser
description: Lær hvordan du kan vise informasjon om en databaselås rett fra klientgrensesnittet i Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 6880ffa9a2ab42c1af7c22f9cace64697c9f905b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922320"
---
# <a name="viewing-database-locks"></a>Visning av databaselåser

Databaselåsing kontrollerer tilgang for flere brukere til de samme dataene samtidig. For å beskytte en transaksjon mot andre transaksjoner som endrer de samme dataene, setter den første transaksjonen en lås på dataene. Låsen blir værende til transaksjonen er ferdig.

Brukere kan bli blokkert fra å fullføre transaksjoner for de låste dataene. De får vanligvis en melding som angir låsebetingelsen.

## <a name="to-view-database-locks"></a>Slik viser du databaselåser

Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Databaselåser**, og velg deretter den relaterte koblingen.

Siden **Databaselåser** inneholder et øyeblikksbilde av alle gjeldende databaselåser.

Hvis du vil ha mer informasjon om databaselåsing, kan du se [Overvåke databaselåser](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) i hjelpen for utviklere i Business Central og IT-eksperter.

## <a name="see-also"></a>Se også

[Overvåke databaselåser](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 


[!INCLUDE[footer-include](includes/footer-banner.md)]