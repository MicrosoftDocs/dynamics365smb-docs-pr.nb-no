---
title: Bruke QuickBooks Migration-utvidelsen | Microsoft-dokumentasjon
description: "Beskriver hvordan du bruker utvidelsen til å importere kunder, leverandører, varer og konti fra QuickBooks Desktop til Dynamics 365 for Financials."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 4775c945a7721b8f4e52a187840a585396611e47
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="the-quickbooks-data-migration-extension-for-dynamics-365-for-financials"></a>Utvidelsen QuickBooks Data Migration for Dynamics 365 for Financials
Denne utvidelsen gjør det enkelt å overføre kunder, leverandører, varer og konti fra QuickBooks Desktop til [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis virksomheten din bruker QuickBooks i dag, kan du eksportere relevant informasjon og deretter åpner en assistert oppsettsveiledning for å laste opp data til [!INCLUDE[d365fin](includes/d365fin_md.md)].  
Hvis du vil ha mer informasjon, kan du se [Imporere forretningsdata fra andre økonomisystemer](upload-data.md).

## <a name="exporting-data-from-quickbooks-desktop"></a>Eksportere data fra QuickBooks Desktop
Du må ha eksportert noen eller alle eksisterende kunder, leverandører, lagervarer og konti til en IIF-fil (Intuit Interchange Format). QuickBooks Data Migration-utvidelsen inneholder en standard tilordning av QuickBooks-data, slik at du kan bruke de eksisterende dataene til å teste det nye [!INCLUDE[d365fin](includes/d365fin_md.md)]-firmaet. Standardtilordningen vil være tilstrekkelig i de aller fleste tilfeller, men du kan endre tilordningen i den assistert oppsettsveiledningen.  
I QuickBooks inneholder Fil-menyen et verktøy for å eksportere lister. I forbindelse med [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du eksportere følgende lister:

* Kundeoversikt  
* Leverandøroversikt  
* Vareoversikt  
* Kontooversikt  

De eksporterte dataene lagres som en IIF-fil som du deretter kan laste opp til [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="finding-the-quickbooks-data-migration-extension"></a>Finne QuickBooks Data Migration-utvidelsen
Utvidelsen Datamigrering for QuickBooks er installert og klar som en integrert del av den assisterte oppsettsveiledningen for datamigrering. Hvis du er klar til å komme i gang nå og har eksportert dataene fra QuickBooks, velger du ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angir **Automatisk oppsett**, og velger deretter den tilknyttede koblingen. Velg **Overfør forretningsdata**, og følg trinnene i veiledningen.  

## <a name="see-also"></a>Se også
[Importere forretningsdata fra andre økonomisystemer](upload-data.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser ](ui-extensions.md)  

