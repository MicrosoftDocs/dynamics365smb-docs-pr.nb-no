---
title: Vise databaselåser
description: Lær hvordan du kan vise informasjon om en kundedatabaselås rett fra klientgrensesnittet i Business Central.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.form: 9511
ms.date: 06/14/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="viewing-database-locks"></a>Visning av databaselåser

Databaselåsing kontrollerer tilgang for flere brukere til de samme dataene samtidig. For å beskytte en transaksjon mot andre transaksjoner som endrer de samme dataene, setter den første transaksjonen en lås på dataene. Låsen blir værende til transaksjonen er ferdig.

Brukere kan bli blokkert fra å fullføre transaksjoner for de låste dataene. De får vanligvis en melding som angir låsebetingelsen.

## <a name="to-view-database-locks"></a>Slik viser du databaselåser

Velg ikonet ![Søk etter side eller rapport.](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport") og angi **Databaselåser**, og velg deretter den relaterte koblingen.

Siden **Databaselåser** inneholder et øyeblikksbilde av alle gjeldende databaselåser.

Hvis du vil ha mer informasjon om databaselåsing, kan du se [Overvåke databaselåser](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) i hjelpen for utviklere i Business Central og IT-eksperter.

## <a name="see-also"></a>Se også

[Overvåke databaselåser](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 


[!INCLUDE[footer-include](includes/footer-banner.md)]
