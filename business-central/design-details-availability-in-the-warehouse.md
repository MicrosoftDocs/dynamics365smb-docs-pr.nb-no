---
title: Designdetaljer – Tilgjengelighet i lageret | Microsoft-dokumentasjon
description: Systemet må holde konstant kontroll over varedisposisjon på lageret, slik at utgående ordrer kan flyte effektivt og gi optimale leveringer.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 670fbfc0f7e576f92ef26e31418d0d44f6262eec
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8132084"
---
# <a name="design-details-availability-in-the-warehouse"></a>Designdetaljer: Tilgjengelighet i lageret
Systemet må holde konstant kontroll over varedisposisjon på lageret, slik at utgående ordrer kan flyte effektivt og gi optimale leveringer.  

Tilgjengelighet varierer avhengig av tildelinger på hyllenivå når det oppstår lageraktiviteter som plukking og flytting, og når lagerreservasjonssystemet bruker begrensninger som må overholdes. En ganske komplisert algoritme bekrefter at alle betingelsene er oppfylt før tildeling av antall i plukk for utgående flyter.

Hvis én eller flere betingelser ikke er oppfylt, kan forskjellige feilmeldinger vises, inkludert den generiske "Ingenting å håndtere." meldingen. "Ingenting å håndtere." meldingen kan oppstå av mange ulike årsaker, både i utgående og inngående flyter, der en direkte eller indirekte involvert dokumentlinje inneholder feltet **Ant. som skal håndt**.

> [!NOTE]
> Informasjon vil snart bli publisert her om mulige årsaker og løsninger for "Ingenting å håndtere". meldingen.

## <a name="bin-content-and-reservations"></a>Hylleinnhold og reservasjoner  
 I en installasjon av lagerstyring finnes vareantall både som lagerposter i modulen Lager og som varepostene i modulen Beholdning. Disse to posttypene inneholder forskjellig informasjon om hvor varene er, og om de er tilgjengelige. Lagerposter angir disposisjonen til en vare etter hylle og hylletype, som kalles hylleinnhold. Vareposter angir varens tilgjengelighet ved reservasjon til utgående dokumenter.  

 I plukkealgoritmen er det spesialfunksjonalitet som brukes til å beregne antallet som er disponibelt for plukking når hylleinnhold er knyttet til reservasjoner.  

## <a name="quantity-available-to-pick"></a>Antall tilgjengelig for plukk  
 Hvis for eksempel plukkalgoritmen tar hensyn til vareantall som er reservert for en ventende ordrelevering, kan disse varene plukkes for en annen ordre som er sendt tidligere, noe som hindrer at det første salget fullføres. For å unngå denne situasjonen trekker plukkealgoritmen fra antall som er reservert for andre utgående dokumenter, antall i eksisterende plukkdokumenter og antall som er plukket, men ennå ikke er levert eller forbrukt.  

 Resultatet vises i feltet **Disp. antall som kan plukkes** på siden **Plukkforslag**, der feltet beregnes dynamisk. Verdien beregnes også når brukere oppretter plukkinger direkte for utgående dokumenter. Slike utgående dokumenter kan være ordrer, produksjonsforbruk eller utgående overføringer, der resultatet gjenspeiles i de tilknyttede antallsfeltene, for eksempel **Ant. som skal håndt.**.  

> [!NOTE]  
>  Når det gjelder reservasjonsprioriteter, blir antallet som skal reserveres trukket fra antallet som er tilgjengelige for plukk. Hvis for eksempel antallet som er tilgjengelig i plukkhyller er 5 enheter, men 100 enheter er i plasseringshyller, vil det vises en feilmelding når du prøver å reservere flere enn 5 enheter for en annen ordre, fordi resten av antallet må være tilgjengelig i plukkhyller.  

### <a name="calculating-the-quantity-available-to-pick"></a>Beregne antall tilgjengelig for plukk  
 Antallet som er disponibelt for plukking, beregnes som følger:  

 Antall tilgjengelige for plukk = Antallet i plukkhyller - Antallet i plukk og flyttinger – (Reservert antall i plukkhyller + Reservert antall i plukk og flyttinger)  

 Diagrammet nedenfor viser de ulike elementene i beregningen.  

 ![Disponibelt for plukking med reservasjonsoverlapping.](media/design_details_warehouse_management_availability_2.png "Disponibelt for plukking med reservasjonsoverlapping")  

## <a name="quantity-available-to-reserve"></a>Antall tilgjengelig for reservasjon  
 Siden konsepter for hylleinnhold og reservasjon sameksisterer, må antall varer som er tilgjengelige for reservasjon, justeres etter tildelinger til utgående lagerdokumenter.  

 Det skal være mulig å reservere alle varene i beholdningen, unntatt de som har startet utgående behandling. Antallet som er tilgjengelig for å reservere blir derfor definert som antallet på alle dokumenter og alle hylletyper, unntatt følgende utgående antall:  

-   Antall på uregistrerte plukkdokumenter  
-   Antall i leveringshyller  
-   Antall i til produksjon-hyller  
-   Antall i åpne produksjonshyller  
-   Antall i til montering-hyller  
-   Antall i justeringshyller  

 Resultatet vises i feltet **Totalt disp. antall** på **Reservasjon**-siden.  

 Antallet som ikke kan reserveres på en reservasjonslinje fordi det er tildelt i lageret, vises i feltet **Tildelt antall på lager** på **Reservasjon**-siden.  

### <a name="calculating-the-quantity-available-to-reserve"></a>Beregne antall tilgjengelig for reservasjon  
 Antallet som er disponibelt for reservasjon, beregnes som følger:  

 Antall tilgjengelige for reservasjon = Totalt antall på lager - Antallet i plukk og flyttinger for kildedokumenter - Reservert antall - Antall i utgående hyller  

 Diagrammet nedenfor viser de ulike elementene i beregningen.  

 ![Disponibelt for reservering per lagerlokasjon.](media/design_details_warehouse_management_availability_3.png "Disponibelt for reservering per lagerlokasjon")  

## <a name="see-also"></a>Se også  
 [Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
 [Vis tilgjengeligheten av varer](inventory-how-availability-overview.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]