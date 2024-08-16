---
title: Opprette nye verdiposter for varer på lageret| Microsoft-dokumenter
description: 'Beskriver hvordan du foretar oppskrivning eller avskrivning av verdiposter for én eller flere varer på lageret, ved å bokføre den gjeldende, beregnede verdien.'
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'costing, inventory cost, value entries'
ms.search.forms: '5803,'
ms.date: 07/29/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Revaluere lageret
Hvis du vil endre lagerverdien for en vare eller en bestemt varepost, må du bruke revalueringskladden.

## Slik revaluerer du beholdning
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Revalueringskladd** og velg den relaterte koblingen.
2. Velg handlingen **Beregn lagerverdi**.
3. På siden **Beregn lagerverdi** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Velg **OK**-knappen.
5. Angi den nye enhetskosten **i feltet Enhetskost (revaluert) på hver linje på** siden **Revalueringskladder**  for vare. Du kan eventuelt angi det nye totalbeløpet i feltet **Lagerverdi (revaluert)**.

    De relevante feltene oppdateres automatisk.  **Beløp-feltet** viser den faktiske endringen i lagerverdien for den valgte vareposten. I dette feltet beregnes differansen mellom feltene **Lagerverdi (beregnet)** og **Lagerverdi (revaluert)**.
6. Når du har fullført alle linjene i revalueringskladden, kan du velge handlingen **Bokfør**.

Nye verdiposter opprettes nå for å gjenspeile revalueringer som du har bokført. Du kan se de nye verdiene på de respektive varekortene.

## Se også
[Design Detaljer: Revaluering](design-details-revaluation.md)    
[Lager](inventory-manage-inventory.md)    
[Salg](sales-manage-sales.md)    
[Innkjøp](purchasing-manage-purchasing.md)    
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]