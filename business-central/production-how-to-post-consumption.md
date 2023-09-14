---
title: Massebokføre forbruk
description: 'Hvis trekkmetoden er Manuell, må du bokføre komponentene manuelt ved hjelp av forbrukskladdene.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000846, 99000850'
ms.date: 03/08/2023
ms.author: bholtorf
---
# Massebokføre produksjonsforbruk

Hvis trekkmetoden er **Manuell**, må du bruke en forbrukskladd til å bokføre komponentene manuelt.  

> [!NOTE]
> Hvis du satte en hake i feltet **Plukk nødv.** på lokasjonskortet for å vise at lokasjonen krever legerplukkbehandling, trenger du ikke å bruke denne kjørselen. [!INCLUDE[prod_short](includes/prod_short.md)] skal håndtere forbruk når du bokfører lagerplukkingen. Hvis du vil ha mer informasjon, kan du se [Plukke for produksjon i enkle lageroppsett](warehouse-how-to-pick-for-production.md).  

Du kan også konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] til automatisk å bokføre (*lagertrekke*) komponenter når du starter eller ferdigstiller produksjonsordrer. Hvis du vil ha mer informasjon, kan du se [Aktivere lagertrekk av komponenter i henhold til operasjonsavgang](production-how-to-flush-components-according-to-operation-output.md).

## Slik bokfører du forbruk for en eller flere produksjonsordrelinjer

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Forbrukskladd** og velg den relaterte koblingen.  
2. Fyll ut feltene med produksjonsordre- og forbruksinformasjonen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Bruk handlingen **Beregn forbruk** til å generere journallinjer fra produksjonsordrer basert på den faktiske avgangen (antall ferdigvarer du har rapportert) eller den forventede avgangen (antall ferdigvarer du forventer å produsere).

    > [!NOTE]
    > Hvis du konfigurerte lokasjonskortet til å kreve lagerplukkbehandling, kan du bare angi antall varer som allerede er plukket via en lageraktivitet, i feltet **Antall** på siden **Forbrukskladd**, og ikke beregnet antall. Hvis du vil ha mer informasjon, kan du se [Plukke for montering eller produksjon i avansert lageroppsett](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)

3. Velg handlingen **Bokfør** for å bokføre forbruket. De relaterte beholdningene reduseres.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## Se også

[Produksjon](production-manage-manufacturing.md)  
[Definere produksjon](production-configure-production-processes.md)  
[Planlegging](production-planning.md)  
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
