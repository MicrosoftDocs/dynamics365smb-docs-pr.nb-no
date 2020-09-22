---
title: Designdetaljer – Integrasjon med lagerbeholdning | Microsoft-dokumentasjon
description: Modulen Lagerstyring og modulen Lager samhandler med hverandre i vareopptelling og i lagerjustering.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 46d8272903a3a7c9da7247fd96bcd80a16050b58
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2020
ms.locfileid: "3787824"
---
# <a name="design-details-integration-with-inventory"></a>Designdetaljer: Integrasjon med lagerbeholdning
Modulen Lagerstyring og modulen Lager samhandler med hverandre i vareopptelling og i lagerjustering.  
  
## <a name="physical-inventory"></a>Vareopptelling  
 Siden **Lagervareopptellingskladd** brukes med siden **Vareopptellingskladd** for alle avanserte lagerlokasjoner. Lageret beregnes på hyllenivå, og den lageransatte får en listeutskrift. Listen viser hvilke varer som må telles i hvilke hyller.  
  
 Den lageransatte registrerer det opptalte antallet på siden **Lagervareopptellingskladd** og bokfører deretter kladden.  
  
 Hvis det opptalte antallet er større enn antallet på kladdelinjen, blir det bokført en bevegelse for denne forskjellen fra standard justeringshylle til hyllen som telles. Dette øker antallet på den opptalte hyllen og reduserer antallet på standard justeringshylle.  
  
 Hvis det opptalte antallet er mindre enn antallet på kladdelinjen, blir det bokført en flytting for denne forskjellen fra den talte hyllen til standard justeringshylle. Dette reduserer antallet på den opptalte hyllen og øker antallet på standard justeringshylle.  
  
 I avanserte lagerskonfigurasjoner blir verdien i feltet **Antall (beregnet)** hentet fra varepostene, og verdien i feltet **Antall (opptalt)** blir hentet fra lagerposter, unntatt justeringshylleinnholdet. **Antall**-feltet angir forskjellen mellom de to første feltene, som skal være lik innholdet i justeringshyllen.  
  
 Når du bokfører vareopptellingskladden, oppdateres lageret og standard justeringshylle.  
  
### <a name="warehouse-adjustments-to-the-item-ledger"></a>Lagerjusteringer i vareposten  
 Du bruker **Varekladd**-siden og funksjonen **Beregn lagerjustering** til å justere lagerbeholdningen i vareposten i samsvar med en justering som er gjort i vareantallet i en lagerhylle. Hvis du vil opprette en kobling mellom beholdningen og lageret, må du definere en standard justeringshylle per lokasjon.  
  
 Standard justeringshylle registrerer varer på lageret når du bokfører en økning for lageret. Hvis du bokfører en reduksjon, blir imidlertid antallet på standardhyllen også redusert. I begge tilfeller blir det opprettet vareposter og lagerposter.  
  
> [!NOTE]  
>  Justeringshyllen er ikke inkludert i tilgjengelighetsberegningen.  
  
 Hvis du vil justere hylleinnholdet, kan du bruke lagervarekladden der du kan angi varenummer, sonekode, hyllekode og antall som du vil justere.  
  
 Hvis du angir et positivt antall og bokfører linjen, økes beholdningen som er lagret på hyllen, og antallet i standard justeringshylle reduseres tilsvarende.  
  
## <a name="see-also"></a>Se også  
 [Designdetaljer: Lagerstyring](design-details-warehouse-management.md)   
 [Designdetaljer: Tilgjengelighet i lageret](design-details-availability-in-the-warehouse.md)