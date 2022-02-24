---
title: Definere lagerverdisetting og kostberegning | Microsoft-dokumentasjon
description: Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: ab2ae5103a1bcc613309412744e913b09a054647
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182879"
---
# <a name="setting-up-inventory-valuation-and-costing"></a>Definere lagerverdisetting og kostberegning
For å sikre at lagerkost registreres riktig, må du definere ulike felt og sider før du begynner å opprette varetransaksjoner.

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Angi en lagermetode for hver vare for å styre hvordan innkommende kost brukes til å vurdere lagerverdi og solgte varers kost.|[Registrere nye varer](inventory-how-register-new-items.md)|  
|Sikre at kost automatisk bokføres mot Finans når en lagertransaksjons bokføres.|Feltet **Automatisk kostbokføring** på siden **Lageroppsett**|  
|Sikre at forventet kost bokføres mot Finans for å se en beregning av skyldige beløp og solgte varers kost i midlertidige finanskonti før de faktisk faktureres.|Feltet **Bokf. av forventet kost i Finans** på siden **Lageroppsett**|  
|Definere at systemet skal justeres automatisk for eventuelle kostendringer hver gang du bokfører lagertransaksjoner.|[Justere varekost](inventory-how-adjust-item-costs.md)|  
|Definere om gjennomsnittlig kost skal beregnes bare per vare, eller per vare for hver lagerføringsenhet og hver variant av varen.|Feltet **Beregn.type for gj.snittskost** på siden **Lageroppsett**|  
|Velg hvilken tidsperiode du vil bruke til å beregne vektet gjennomsnittlig kost for varer som bruker lagermetoden Gjennomsnitt.|Feltet **Gjennomsnittskostperiode** på siden **Lageroppsett**|  
|Definere lagerperioder for å kontrollere lagerverdi over tid ved å forby transaksjonsbokføring i lukkede lagerperioder.|[Arbeide med lagerperioder](finance-how-to-work-with-inventory-periods.md)|  
|Sikre at salgsreturer utlignes mot den opprinnelige utgående transaksjonen for å opprettholde lagerverdi.|Feltet **Bruk opprinnelig kostpris** på siden **Salg**|  
|Sikre at kjøpsreturer utlignes mot den opprinnelige inngående transaksjonen for å opprettholde lagerverdi.|Feltet **Bruk opprinnelig kostpris** på siden **Kjøp**|
|Definere avrundingsreglene som skal brukes ved justering av eller forslag om varepriser, og når standardkost skal justeres eller foreslås.|Siden **Avrundingsmetode**|  

## <a name="see-also"></a>Se også  
[Administrere lagerkostnader](finance-manage-inventory-costs.md)  
[Arbeide med Business Central](ui-work-product.md)  
[Finans](finance.md)  
