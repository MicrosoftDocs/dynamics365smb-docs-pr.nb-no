---
title: Definere kontoplanen| Microsoft-dokumentasjon
description: Beskriver hvordan du kan endre kontoplanen.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 03/28/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 48202a9e9a763dcb22bed9975aa9c4a39d2dc4ae
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a>Definere eller endre kontoplanen
Kontoplanen viser finanskontoene som lagrer dine økonomiske data. [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] inneholder en standard kontoplan som er klar til å støtte forretningsvirksomheten din.
Du kan imidlertid endre standardkontoene, og du kan legge til nye kontoer.  

## <a name="adding-or-changing-accounts"></a>Legge til eller endre kontoer
For hver kontoplan kan du åpne finanskontoen og legge til eller endre innstillinger.

**Merk**: Du kan slette en finanskonto. Før du sletter den, må imidlertid følgende være oppfylt:  

* Saldo på kontoen må være null.  
* Feltet **Tillat sletting av finanskto. før** må være satt i vinduet **Finansoppsett**, og kontoen kan ikke ha finansposter på eller etter denne datoen.  
* Hvis feltet **Kontroller finanskontobruk** er valgt i vinduet **Finansoppsett**, må ikke kontoen brukes i bokføringsgrupper eller bokføringsoppsett.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] hindrer deg i å slette en finanskonto som lagrer data som er nødvendige i kontoplanen.  

## <a name="see-also"></a>Se også
[Økonomimodulen og kontoplanen](finance-general-ledger.md)  
[Håndtere bankkonti](bank-manage-bank-accounts.md)  
[Dimensjoner](finance-dimensions.md)  
[Importere data fra andre økonomisystemer](upload-data.md)  
[Arbeide med GIFI-koder i Canada](ca-finance-work-gifi-codes.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
