---
title: Administrer lageraktiviteter
description: Etter mottak av varer og før varene sendes, utføres det en rekke interne lageraktiviteter for å sørge for en effektiv strøm av varer gjennom lageret.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5774, 5776, 5777, 5785, 5793, 5797, 7318, 7364, 7401, 8909, 9000, 9008, 9009, 9050, 9053, 9056
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: c08331889a0a94e8760b8104b8d5769ea5d0edbf
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529788"
---
# <a name="warehouse-management"></a>Lagerstyring

Etter mottak av varer og før varene sendes, utføres det en rekke interne lageraktiviteter for å sørge for en effektiv strøm av varer gjennom lageret, og organisere og vedlikeholde selskapet lagre.

Vanlige lageraktiviteter omfatter å plassere varer, flytte varer på lageret eller mellom ulike lager, og plukke varer til montering, produksjon eller for levering. Montering av varer for salg eller lager kan også regnes som lageraktiviteter, men disse dekkes andre steder. Hvis du vil ha mer informasjon, se [Monteringsstyring](assembly-assemble-items.md).  

På store lager kan de ulike håndteringsoppgavene legges til ulike avdelinger, mens integreringen administreres av en styrt arbeidsflyt. I enklere installasjoner er flyten mindre formalisert, og lageraktivitetene utføres med såkalte lagerplasseringer og lagerplukk. Hvis du vil ha mer informasjon om enkle kontra avanserte lageroppsett, kan du se [Designdetaljer: Lageroversikt](design-details-warehouse-overview.md).

Før du kan utføre lageraktiviteter, må du definere systemet for den aktuelle kompleksiteten for lagerbehandlingen. Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).

De lagerrelaterte oppgavene med å telle, justere og reklassifisere varene kan omfatte lagerppgaver som må utføres i lagerpostene før de kan synkroniseres med de relaterte varepostene. Hvis du vil ha mer informasjon, se [Telle, justere og reklassifisere lagerbeholdning](inventory-how-count-adjust-reclassify.md).

 Tabellen nedenfor beskriver en sekvens av oppgaver og har koblinger til emnene som beskriver dem.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Registrer mottaket (inkludert overmottak) av varer på lagerlokasjoner, enten bare med en bestilling, i enkle lokasjonsoppsett eller med et lagermottak i tilfelle halvautomatisert eller fullstendig automatisert lagerbehandling på lokasjonen.|[Motta varer](warehouse-how-receive-items.md)|
|Omgå plasseringen, og velg prosesser for å påskynde en vare rett fra mottak eller produksjon til levering.|[Kryssoverføringsvarer](warehouse-how-to-cross-dock-items.md)|
|Plassere varer som mottas etter kjøp, salgsreturer, overføringer eller produksjonsavgang i henhold til den konfigurerte lagerprosessen.|[Plassere varer](warehouse-put-away-items.md)|
|Flytte varer mellom hyller på lageret.|[Flytte varer](warehouse-move-items.md)|
|Plukke varer som skal leveres, overføres eller anvendes i monteringen eller produksjonen, i henhold til den konfigurerte lagerprosessen.|[Plukke varer](warehouse-pick-items.md)|
|Registrer leveringen av varer fra lagerlokasjoner, enten bare med en ordre, i enkle lokasjonsoppsett eller med en lagerlevering i tilfelle halvautomatiserte eller fullstendig automatiserte lagerprosesser på lokasjonen.|[Levere varer](warehouse-how-ship-items.md)|  

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/get-started-warehouse-management/)

## <a name="see-also"></a>Se også

[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)  
[Monteringsstyring](assembly-assemble-items.md)  
[Designdetaljer: Warehouse Management](design-details-warehouse-management.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
