---
title: Behandle delleveringer
description: Leveringer til ordrer kan behandles i Business Central med delleveringer ved hjelp av feltene Leveringsønske og Levere (antall).
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: 'shipping advice, partial shipments, partial deliveries, trade, customer sales order'
ms.date: 08/12/2022
ms.author: a-reishima
---
# Behandle delleveringer

I en dellevering leveres ikke hele ordren samtidig. I en ordre på 100 enheter sender du for eksempel 40 enheter omgående og 60 senere. Det er ingen begrensninger på antall leveringer for en ordre.

Før du kan bruke delleveringer i [!INCLUDE [prod_short](includes/prod_short.md)], må du imidlertid angi at kunden godtar delleveringer ved å angi feltet **Leveringsønske** på siden **Kundekort**. Hvis kunden vanligvis bare godtar fullstendige leveringer, men deretter ber om en dellevering for en bestemt ordre, kan du endre feltet **Leveringsønske** før bokføring.

Som standard angir [!INCLUDE [prod_short](includes/prod_short.md)] feltet på siden **Kundekort** som **Delvis**, slik at delleveranser kan brukes. Hvis feltet imidlertid har blitt justert til å angi **Komplett**, er feltet **Levere (antall)** sperret i ordrer for den kunden.

[!INCLUDE [order-ship-invoice_md](includes/order-ship-invoice.md)]

## Se også

[Selg produkter med en kundeordre](sales-how-sell-products.md)  
[Levere varer](warehouse-how-ship-items.md)  
[Foreta direkte leveringer](sales-how-drop-shipment.md)  
[Salg](sales-manage-sales.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Administrasjon](admin-setup-and-administration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
