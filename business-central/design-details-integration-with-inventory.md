---
title: Designdetaljer – Integrasjon med lagerbeholdning
description: Modulen Lagerstyring og modulen Lager samhandler med hverandre i vareopptelling og i lagerjustering.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# Designdetaljer: Integrasjon med lagerbeholdning

Lagerstyring og lagerfunksjoner samhandler med hverandre i vareopptelling og i lagerjustering.  

## Vareopptelling  

Siden **Lagervareopptellingskladd** brukes med siden **Vareopptellingskladd** for alle avanserte lagerlokasjoner. Lageret beregnes på hyllenivå, og den lageransatte får en listeutskrift. Listen viser hvilke varer som må telles i hvilke hyller.  
  
Den lageransatte registrerer det opptalte antallet på siden **Lagervareopptellingskladd** og bokfører deretter kladden.  
  
Hvis det opptalte antallet er større enn antallet på kladdelinjen, blir det bokført en bevegelse for denne forskjellen fra standard justeringshylle til hyllen som telles. Dette øker antallet på den opptalte hyllen og reduserer antallet på standard justeringshylle.  
  
Hvis det opptalte antallet er mindre enn antallet på kladdelinjen, blir det bokført en flytting for denne forskjellen fra den talte hyllen til standard justeringshylle. Dette reduserer antallet på den opptalte hyllen og øker antallet på standard justeringshylle.  
  
I avanserte lagerskonfigurasjoner blir verdien i feltet **Antall (beregnet)** hentet fra varepostene, og verdien i feltet **Antall (opptalt)** blir hentet fra lagerposter, unntatt justeringshylleinnholdet. **Antall**-feltet angir forskjellen mellom de to første feltene, som skal være lik innholdet i justeringshyllen.  
  
Når du bokfører vareopptellingskladden, oppdateres lageret og standard justeringshylle.  

[!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]
  
## Lagerjusteringer i vareposten  

Du bruker **Varekladd**-siden og funksjonen **Beregn lagerjustering** til å justere lagerbeholdningen i vareposten i samsvar med en justering som er gjort i vareantallet i en lagerhylle. Hvis du vil opprette en kobling mellom beholdningen og lageret, må du definere en standard justeringshylle per lokasjon.  
  
Standard justeringshylle registrerer varer på lageret når du bokfører en økning for lageret. Hvis du bokfører en reduksjon, blir imidlertid antallet på standardhyllen også redusert. I begge tilfeller blir det opprettet vareposter og lagerposter.  
  
> [!NOTE]  
> Lagerberegninger inkluderer ikke justeringshyllen.  
  
For å justere hylleinnholdet kan du bruke en lagervarekladd der du kan angi varenummer, sonekode, hyllekode og antall som du vil justere.  
  
Hvis du angir et positivt antall og bokfører linjen, økes beholdningen som er lagret på hyllen, og antallet i standard justeringshylle reduseres tilsvarende.  
  
## Se også  

[Oversikt over lagerstyring](design-details-warehouse-management.md)  
[Designdetaljer: Tilgjengelighet i lageret](design-details-availability-in-the-warehouse.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]