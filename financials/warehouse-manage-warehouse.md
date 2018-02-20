---
title: Lageraktiviteter | Microsoft-dokumentasjon
description: "Etter mottak av varer og før varene sendes, utføres det en rekke interne lageraktiviteter for å sørge for en effektiv strøm av varer gjennom lageret, og organisere og vedlikeholde selskapet lagre."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 5aa3728aa5658f61fd5bb094c7274405f6f9daa2
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---
# <a name="warehouse-management"></a>Lagerstyring
Etter mottak av varer og før varene sendes, utføres det en rekke interne lageraktiviteter for å sørge for en effektiv strøm av varer gjennom lageret, og organisere og vedlikeholde selskapet lagre.

Vanlige lageraktiviteter omfatter å plassere varer, flytte varer på lageret eller mellom ulike lager, og plukke varer til montering, produksjon eller for levering. Montering av varer for salg eller lager kan også regnes som lageraktiviteter, men disse dekkes andre steder. Hvis du vil ha mer informasjon, se [Monteringsstyring](assembly-assemble-items.md).  

På store lager kan de ulike håndteringsoppgavene legges til ulike avdelinger, mens integreringen administreres av en styrt arbeidsflyt. I enklere installasjoner er flyten mindre formalisert, og lageraktivitetene utføres med såkalte lagerplasseringer og lagerplukk. Hvis du vil ha mer informasjon om enkle kontra avanserte lageroppsett, kan du se [Designdetaljer: Lageroversikt](design-details-warehouse-overview.md).

Før du kan utføre lageraktiviteter, må du definere systemet for den aktuelle kompleksiteten for lagerbehandlingen. Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).

 Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Registrer mottaket av varer på lagerlokasjoner, enten bare med en bestilling, i enkle lokasjonsoppsett eller med et lagermottak i tilfelle halvautomatisert eller fullstendig automatisert lagerbehandling på lokasjonen.|[Motta varer](warehouse-how-receive-items.md)|
|Omgå plasseringen, og velg prosesser for å påskynde en vare rett fra mottak eller produksjon til levering.|[Kryssoverføringsvarer](warehouse-how-to-cross-dock-items.md)|    
|Plassere varer som mottas etter kjøp, salgsreturer, overføringer eller produksjonsavgang i henhold til den konfigurerte lagerprosessen.|[Plassere varer](warehouse-put-away-items.md)|
|Flytte varer mellom hyller på lageret.|[Flytte varer](warehouse-move-items.md)|
|Plukke varer som skal leveres, overføres eller anvendes i monteringen eller produksjonen, i henhold til den konfigurerte lagerprosessen.|[Plukke varer](warehouse-pick-items.md)|
|Registrer leveringen av varer fra lagerlokasjoner, enten bare med en ordre, i enkle lokasjonsoppsett eller med en lagerlevering i tilfelle halvautomatiserte eller fullstendig automatiserte lagerprosesser på lokasjonen.|[Levere varer](warehouse-how-ship-items.md)|  

## <a name="see-also"></a>Se også  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

