---
title: Konfigurere lagerprosesser | Microsoft-dokumentasjon
description: "Selskapets distribusjonsstrategi avspeiles i oppsettet av lagerprosessene. Dette omfatter å definere hvordan ulike varer skal håndteres på ulike lagerlokasjoner, for eksempel graden av hyllekontroll og omfanget av påkrevd arbeidsflyt mellom lageraktiviteter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e39f84abe2fe1a4e49c615de10dc36599cc9ecc4
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---
# <a name="setting-up-warehouse-management"></a>Definere lagerstyring
Selskapets distribusjonsstrategi avspeiles i oppsettet av lagerprosessene. Dette omfatter å definere hvordan ulike varer skal håndteres på ulike lagerlokasjoner, for eksempel graden av hyllekontroll og omfanget av påkrevd arbeidsflyt mellom lageraktiviteter.  

 Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Få en oversikt over hvilke muligheter som finnes i grunnleggende og avansert lagerfunksjonalitet.|[Designdetaljer: Lageroversikt](design-details-warehouse-overview.md)|  
|Sette opp åtte ulike hylletyper, for eksempel Plukkhylle, for å definere flytaktivitetene som er knyttet til hver hylletype.|[Definere hylletyper](warehouse-how-to-set-up-bin-types.md)|  
|Opprett hyller, enten manuelt eller automatisk, med informasjon, for eksempel navn, nummerserier og kategori, i samsvar med en hyllemal.|[Opprette hyller](warehouse-how-to-create-individual-bins.md)|  
|Definere hvilke varer du vil lagre i en gitt hylle, og opprette reglene som bestemmer når hyllen skal fylles med en bestemt vare.|[Opprette hylleinnhold](warehouse-how-to-set-up-bin-contents.md)|  
|Angi at en vare alltid skal plasseres i en bestemt hylle.|[Tilordne standardhyller til varer](warehouse-how-to-assign-default-bins-to-items.md)|
|Opprette maler som skal styre hvor og hvordan varer skal plasseres ved bruk av lagerstyring.|[Definere plasseringsmaler](warehouse-how-to-set-up-put-away-templates.md)|
|Definere brukere som lageransatte i bestemte lokasjoner.|[Definere lageransatte](warehouse-how-to-set-up-warehouse-employees.md)|
|Definere ulike hylletyper i hele lageret, for å styre plasseringen av varer i henhold til type, prioritering eller håndteringsnivå.|[Definere lokasjoner slik at de bruker hyller](warehouse-how-to-set-up-locations-to-use-bins.md)|
|Angi flere innstillinger for en eksisterende lokasjon for å klargjøre den for lageraktiviteter.|[Konvertere eksisterende lokasjoner til lagerlokasjoner](warehouse-how-to-convert-existing-locations-to-warehouse-locations.md)|
|Aktiver plukking, flytting og plassering for monterings- eller produksjonsorder i enkle lageroppsett.|[Opprette grunnleggende lagre med operasjonsområder](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|  
|Konfigurer varer og lokasjoner for det mest avanserte lagerstyringsområdet, der alle aktiviteter må følge en streng arbeidsflyt.|[Definere varer og lokasjoner for lagerstyring](warehouse-how-to-set-up-items-for-directed-put-away-and-pick.md)|  
|Definere når og hvordan varer på lagerlokasjoner skal telles for vedlikeholdsformål eller til bruk i økonomiske rapporter.|[Telle, justere eller reklassifisere lagerbeholdning](inventory-how-count-adjust-reclassify.md)|
|Aktiver lagermedarbeidere til å dele en større enhet i mindre enheter for å oppfylle behovene i kildedokumenter.|[Aktivere automatisk samlet oppbryting med lagerstyring og plukk](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md)|  
|Konfigurere lageret til å automatisk foreslå plukking av varer som utløper først.|[Aktivere plukking etter FEFO](warehouse-picking-by-fefo.md)|
|Integrer strekkodelesere i lagerstyringsløsningen.|[Bruk ADCS (Se automatisk datahentesystem)](warehouse-use-automated-data-capture-systems-adcs.md)|  
|Ha tips om hvordan du omorganiserer lokasjoner, hyller eller soner for å gjøre lageraktivitetene mer effektive.|[Omstrukturere lagre](warehouse-how-to-restructure-warehouses.md)|  

## <a name="see-also"></a>Se også  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

