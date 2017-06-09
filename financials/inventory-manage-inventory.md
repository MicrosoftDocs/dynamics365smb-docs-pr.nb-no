---
title: Lager| Microsoft-dokumentasjon
description: Beskriver hvordan du administrerer fysiske varer.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: b53cae82cfa532fb0620cc9e1f305216c2321785
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017

---

# <a name="inventory"></a>Lager
Du må opprette et varekort av typen **Lager** for hvert fysiske produkt du handler i. Varer du tilbyr til kunder, men ikke har på lager, kan du registrere som katalogvarer, som du kan konvertere til lagervarer når det er nødvendig. Du kan øke eller redusere antall varer på lager ved å bokføre direkte til varepostene, for eksempel etter en fysisk opptelling eller hvis du ikke registrerer kjøp.

Lagerøkning og -reduksjon registreres også når du bokfører henholdsvis salgs- og kjøpsdokumenter. Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md), [Selge produkter](sales-how-sell-products.md) og [Fakturere salg](sales-how-invoice-sales.md). Overføringer mellom lokasjoner endrer lagerantallene på tvers av selskapets lagere.   

Hvis du vil ha bedre oversikt over varene og hjelp til å finne dem, kan du kategorisere varene og gi dem attributter til å søke og sortere etter.

Du må sørge for at kostnadene for varene videresendes til den relaterte utgående mva-transaksjonen, spesielt i situasjoner der du selger varer før du fakturerer kjøp av disse varene. Dette kalles kostjustering, som du kan utføre manuelt eller definere at skal skje automatisk når du bokfører en varetransaksjon.

Endringer i lagerverdien fra handel er automatisk avstemt med dine økonomiske bøker når du bokfører transaksjoner for varen.

|Hvis du vil |Se |
|---|----|
|Opprett varekort for lagervarer som du handler med.|[Registrere nye varer](inventory-how-register-new-items.md)|
|Strukturer overordnede varer som selges som sett som består av komponenter for den overordnede varen, eller som du monterer til bestilling eller lager.|[Arbeide med stykklister](inventory-how-work-BOMs.md)|
|Hold oversikt over varer og gjør det enklere å finne og sortere varer ved å ordne dem i kategorier.|[Kategorisere varer](inventory-how-categorize-items.md)|
|Tilordne vareattributter av ulike verdityper til varene, for å gjøre det enklere for deg å sortere og finne varer.|[Arbeide med vareattributter](inventory-how-work-item-attributes.md)|
|Opprett spesielle varekort for varer som du tilbyr til kunder, men som du ikke har på lager.|[Arbeide med katalogvarer](inventory-how-work-nonstock-items.md)|
|Øk eller reduser en vares lagerantall, for eksempel etter en fysisk opptelling, eller som en enkel metode for å registrere kjøpsmottak.|[Fremgangsmåte: Juster lagerbeholdning](inventory-how-adjust-inventory.md)|
|Vis tilgjengeligheten av varer per lokasjon, etter periode, ved salg eller kjøpshendelse eller ved bruk på monteringsstykklister.|[Få en oversikt over tilgjengelighet](inventory-how-availability-overview.md)|
|Overføre varer mellom lokasjoner med overføringsordrer for å administrere lageraktiviteter, eller med varereklassifiseringskladden.|[Overføre beholdning mellom lokasjoner](inventory-how-transfer-between-locations.md)|
|Skriv opp eller skriv ned verdien av én eller flere varer på lager ved postering av den gjeldende, beregnede verdien.|[Revaluere beholdning](inventory-how-revalue-inventory.md)|
|Juster varekost, enten automatisk eller manuelt, for å til videreføre kostnadsendringer fra inngående poster til relaterte utgående poster.|[Justere varekost](inventory-how-adjust-item-costs.md)|
|Finn ut hvordan endringer i lagerverdien fra handel er automatisk avstemt med dine økonomiske bøker.|[Avansert: Lageravstemming](advanced-inventory-reconciliation.md).|

## <a name="see-also"></a>Se også  
[Innkjøp](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)    
[Forsyningskjede](madeira-supply-chain.md)  
[Arbeide med [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
