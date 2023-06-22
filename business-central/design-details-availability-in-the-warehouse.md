---
title: Utformingsdetaljer – Tilgjengelighet i lageret
description: Finn ut mer om de forskjellige faktorene som påvirker varedisposisjon i lageret.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
---
# <a name="design-details-availability-in-the-warehouse" />Designdetaljer: Tilgjengelighet i lageret

Hold deg oppdatert på varedisposisjon for å sikre at utgående bestillinger flyter effektivt, og at leveringstidene er optimale.  

Tilgjengelighet kan variere, avhengig av flere faktorer. Eksempel:

* Tildelinger på hyllenivået når lageraktiviteter som plukking og flytting skjer.
* Når lagerreservasjonssystemet ikke overholder restriksjoner å samsvare med.

Før tildelingsantall for valg for utgående flyter, bekrefter [!INCLUDE [prod_short](includes/prod_short.md)] at alle betingelsene er oppfylt.

Når betingelsene ikke er oppfylt, vises det feilmeldinger. En typisk melding er den generelle Ingenting å håndtere. meldingen. Meldingen kan vises av mange ulike årsaker, i utgående og inngående flyter, der en dokumentlinje inneholder feltet **Ant. som skal håndt**.

## <a name="bin-content-and-reservations" />Hylleinnhold og reservasjoner

Vareantall eksisterer både som lagerposter og som vareposter i lager. Disse to posttypene inneholder forskjellig informasjon om hvor varene er, og om de er tilgjengelige. Lagerposter angir disposisjonen til en vare etter hylle og hylletype, som kalles hylleinnhold. Vareposter angir varens tilgjengelighet ved reservasjon for utgående dokumenter.  

[!INCLUDE [prod_short](includes/prod_short.md)] beregner antallet som er tilgjengelig for plukking når hylleinnholdet er kombinert med reservasjoner.  

## <a name="quantity-available-to-pick" />Antall tilgjengelig for plukk

[!INCLUDE [prod_short](includes/prod_short.md)] reserverer varer for ventende ordreforsendelser slik at de ikke plukkes for andre ordrer som leveres tidligere. [!INCLUDE [prod_short](includes/prod_short.md)] trekker fra antall varer som allerede er i ferd med å utføres på følgende måte:

* Antall reservert for andre utgående dokumenter.
* Antall i eksisterende plukkdokumenter.
* Antall plukket, men ennå ikke levert eller forbrukt.  

Resultatet beregnes dynamisk og vises i feltet **Disp. antall som kan plukkes** på siden **Plukkforslag**. Verdien beregnes også når brukere oppretter plukkinger direkte for utgående dokumenter. Følgende er eksempler på utgående kildedokumenter:

* Ordrer
* Produksjonsforbruk
* Utgående overføringer

Resultatet er tilgjengelig i disse dokumentene i antallsfeltene, for eksempel feltet **Ant. som skal håndt**.  

> [!NOTE]  
> Når det gjelder reservasjonsprioriteter, blir antallet som skal reserveres trukket fra antallet som er tilgjengelige for plukk. Hvis for eksempel antallet som er tilgjengelig i plukkhyller er 5 enheter, men 100 enheter er i plasseringshyller, vil det vises en feilmelding når du prøver å reservere flere enn 5 enheter for en annen ordre, fordi resten av antallet må være tilgjengelig i plukkhyller.  

### <a name="calculating-the-quantity-available-to-pick" />Beregn antall tilgjengelig for plukk

[!INCLUDE [prod_short](includes/prod_short.md)] beregner antallet som er disponibelt for plukking som følger:  

Antall tilgjengelige for plukk = Antallet i plukkhyller - Antallet i plukk og flyttinger – (Reservert antall i plukkhyller + Reservert antall i plukk og flyttinger)  

Diagrammet nedenfor viser de ulike elementene i beregningen.  

![Disponibelt for plukking med reservasjonsoverlapping.](media/design_details_warehouse_management_availability_2.png "Disponibelt for plukking med reservasjonsoverlapping")  

## <a name="quantity-available-to-reserve" />Antall tilgjengelig for reservasjon

Siden konsepter for hylleinnhold og reservasjon sameksisterer, må antall varer som er tilgjengelige for reservasjon, justeres etter tildelinger til utgående lagerdokumenter.  

Du kan reservere alle lagervarer, unntatt varer som utgående behandling har startet for. Antallet som er tilgjengelig for å reservere, blir definert som antallet på alle dokumenter og alle hylletyper. Følgende utgående antall er unntak:  

* Antall på uregistrerte plukkdokumenter  
* Antall i leveringshyller  
* Antall i til produksjon-hyller  
* Antall i åpne produksjonshyller  
* Antall i til montering-hyller  
* Antall i justeringshyller  

Resultatet vises i feltet **Totalt disp. antall** på **Reservasjon**-siden.  

Antallet som ikke kan reserveres på en reservasjonslinje fordi det er tildelt i lageret, vises i feltet **Tildelt antall på lager** på **Reservasjon**-siden.  

### <a name="calculating-the-quantity-available-to-reserve" />Beregn antall tilgjengelig for reservasjon

[!INCLUDE [prod_short](includes/prod_short.md)] beregner antallet som er disponibelt for reservasjon, som følger:  

Antall tilgjengelige for reservasjon = Totalt antall på lager - Antallet i plukk og flyttinger for kildedokumenter - Reservert antall - Antall i utgående hyller  

Diagrammet nedenfor viser de ulike elementene i beregningen.  

![Disponibelt for reservering per lagerlokasjon.](media/design_details_warehouse_management_availability_3.png "Disponibelt for reservering per lagerlokasjon")  

## <a name="see-also" />Se også

[Oversikt over Warehouse Management](design-details-warehouse-management.md)
[Vis tilgjengelighet for varer](inventory-how-availability-overview.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
