---
title: Aktivere plukking etter FEFO | Microsoft-dokumentasjon
description: 'FEFO (først utløpt, først ut) er en sorteringsmetode som sikrer at de eldste elementene, det vil si de med de tidligste utløpsdato, plukkes først.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---
# Aktivere plukking av varer etter FEFO
FEFO (først utløpt, først ut) er en sorteringsmetode som sikrer at de eldste elementene, det vil si de med de tidligste utløpsdato, plukkes først.  

 Denne funksjonaliteten fungerer bare når følgende kriterier er oppfylt:  

-   Varen må ha et serie-/partinummer.  
-   På varens varesporingskodeoppsett må feltet **Lagers.nr. - sporing** eller feltet **Lagerparti - sporing** velges.  
-   Varen må bokføres til lager med en utløpsdato.  
-   På lokasjonen må valgene **Plukk nødv.**, **Plukk i henhold til FEFO** og **Hylle obligatorisk** være aktivert.  

 Når alle kriteriene er oppfylt, sorteres serie-/partinummererte varer som skal plukkes, med de eldste først i alle plukk og flyttinger, unntatt for varer som bruker SN-spesifikk eller partispesifikk sporing.  

> [!NOTE]  
> Hvis enkelte serie- eller partinummererte varer bruker spesifikk sporing, har disse førsteprioritet, og under disse vises de gjenstående, ikke-spesifikke serie-/partinumrene i henhold til FEFO.
<br /><br />
Hvis to serie- eller partinummererte varer har samme utløpsdato, velges varen med lavest serie- eller partinummer.
<br /><br />
Når du plukker serie- eller partinummererte varer i lokasjoner definert for lagerstyring, blir bare antall i hyller av typen *Plukk* plukket i henhold til FEFO.  
<br /><br />
Når du skal aktivere flyttinger i henhold til FEFO, må du la feltet **Fra hylle** stå tomt på siden **Lagerflytting** eller **Flytteforslag**.  
<br /><br />
Hvis feltet **Bruk ikke etter utløpsdato** er valgt på **kortet for varesporingskode**, blir bare varer som ikke er utgått, tatt med i plukkingen, og linjene sorteres i henhold til FEFO-prinsippet.

## Se også  
[Plukke varer for lagerlevering](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Plukke varer med lagerplukk](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]