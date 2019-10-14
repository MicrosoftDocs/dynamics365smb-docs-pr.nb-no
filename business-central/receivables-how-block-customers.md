---
title: Slik sperrer du varer fra salg eller kjøp ved salg til kunder
description: I Business Central kan en vare være merket som sperret for salg, sperret for kjøp eller sperret for alt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: c2b0d5b15571b7e8af1ed1dbee22859f4c131aa3
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2316623"
---
# <a name="block-customers"></a>Sperre kunder
Du kan sperre en kunde, for eksempel på grunn av insolvens, slik at kunden ikke kan legges til i salgsdokumenter, eller slik at ingen transaksjoner kan bokføres for kunden.

I tillegg til å sperre en kunde kan du angi at fordringstransaksjoner for kunden skal settes på vent i forbindelse med purringer. Hvis du vil ha mer informasjon, kan du se [Innkreve utestående saldi](receivables-collect-outstanding-balances.md).   

Tabellen nedenfor beskriver de ulike sperrealternativene.  

|Alternativ|Description|  
|--------------------|------------|  
|**Tom**|Transaksjoner er tillatt for denne kunden.|
|**Levering**|Det kan ikke opprettes nye ordrer og nye leveringer for denne kunden. Eksisterende leveringer som ennå ikke er fakturert, kan faktureres.|  
|**Fakturering**|Det kan ikke opprettes nye ordrer, nye leveringer og nye fakturaer for denne kunden. Eksisterende leveringer som ennå ikke er fakturert, kan ikke faktureres.|  
|**Alle**|Ingen transaksjoner er tillatt for denne kunden, inkludert betalinger.|  

## <a name="to-block-a-customer"></a>Slik sperrer du en kunde:  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kunder**, og velg deretter den relaterte koblingen.
2. Velg en kunde, og velg handlingen **Rediger**.
3. Fyll ut feltet **Sperret** med ett av alternativene ovenfor.

## <a name="see-also"></a>Se også  
[Registrere nye kunder](sales-how-register-new-customers.md)  
[Innkreve utestående saldi](receivables-collect-outstanding-balances.md)  
[Håndtere fordringer](receivables-manage-receivables.md)  
