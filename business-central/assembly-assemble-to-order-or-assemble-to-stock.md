---
title: Forstå montere til ordre og montere til lager
description: Finn ut mer om montering av varer for ordrer eller for å lagerfør for fremtidige salg.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="understanding-assemble-to-order-and-assemble-to-stock"></a><a name="understanding-assemble-to-order-and-assemble-to-stock"></a>Forstå montere til ordre og montere til lager

[!INCLUDE [prod_short](includes/prod_short.md)] lar deg forsyne monteringsvarer på følgende måter:

* Monter til ordre  
* Monter til lager  

## <a name="assemble-to-order"></a><a name="assemble-to-order"></a>Monter til ordre

Bruk monter-til-ordreprosessen for varer du ikke vil lagre. Det kan for eksempel være av følgende årsaker:

* Du skal tilpasse varene for kundebehov.
* Du vil redusere kostnaden av lagerbeholdningen.

Følgende oversikt beskriver noen av fordelene med monter-til-ordreprosessen:  

* tilpass monteringsvarer når en ordre blir tatt.  
* Oversikt over monteringsvarens og tilhørende komponenters tilgjengelighet.  
* Reserver monteringskomponenter umiddelbart for å garantere ordreoppfyllelse.  
* Bestem lønnsomheten til den tilpassede ordren ved å opprullere pris og kostnad.  
* Integrert med lageret for å forenkle montering og levering.  
* Monter til ordre når du oppretter et tilbud eller en rammeordre.  
* Kombiner lagerantall med monter til ordre-antall.  

I monter-til-ordre-prosessen monterer du varer for en ordre. Det finnes en en-til-en-kobling mellom monteringsordren og ordren.  

Når du angir en monter til ordrevare på en ordrelinje, blir en monteringsordre automatisk opprettet. Monteringsordren er basert på salgslinjen, og linjene er basert på varens monteringsstykkliste. Antall komponenter i monteringsstykklisten multipliseres med ordre antallet. Siden **Monter-til-ordrelinjer** viser detaljer om de koblede linjene for monteringsordren. Detaljene kan hjelpe deg med å tilpasse monteringsvaren. Leveringsdatoen er basert på tilgjengeligheten av komponentene. Hvis du vil finne ut mer om monteringsvarer for ordrer, kan du gå til [Selg varer montert til ordre](assembly-how-to-sell-items-assembled-to-order.md).  

> [!NOTE]  
> Selv om det ikke er en del av standardprosessen, kan du selge lagerantall og monter til ordre-antall på samme ordre. Hvis du vil finne ut mer om kombinering av lager og monter-til-ordrevarer, går du til [Selg lagervarer i montere-til-ordre-flyter](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

Hvis du vil angi at en vare er monter-til-ordre, i feltet **Monteringspolicy** på siden **Varekort** for varen, velger du **Monter-til-ordre**.  

## <a name="assemble-to-stock"></a><a name="assemble-to-stock"></a>Monter til lager

Bruk monter-til-lagerprosessen for varer som du monterer og lagrer for fremtidige salg. Monter-til-lager-varer er standardvarer, for eksempel pakkede pakker som du ikke kan tilpasse. Du kan også bruke disse varene som delmonteringskomponenter. Varene plukkes og behandles som enkeltvarer og behandles som ferdige produksjonsvarer. Hvis du vil finne ut mer om monteringsvarer, går du til [Monter varer](assembly-how-to-assemble-items.md).  

Når du angir en montere-til-lager-vare på en salgslinje, behandles varen på samme måte som andre varer som er solgt fra lager. [!INCLUDE [prod_short](includes/prod_short.md)] kontrollerer for eksempel bare tilgjengeligheten for den monterte varen, og ikke for komponentene.  

> [!NOTE]  
> Selv om det ikke er en del av standardprosessen, kan du montere en vare til ordre selv om varen er definert til å bli montert til lager. Finn ut mer under [Selge montere til ordre-varer og lagervarer sammen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

Hvis du vil angi at en vare er monter-til-lager, i feltet **Monteringspolicy** på siden **Varekort** for varen, velger du **Monter-til-lager**.  

## <a name="combination-scenarios"></a><a name="combination-scenarios"></a>Kombinasjonsscenarioer

Når monter-til-ordre og lagerantall kombineres på en ordre, må monter-til-ordre-antall leveres først.  

Hvis en monteringsordre er koblet til en ordrelinje, kopieres verdien i feltet **Ant. som skal monteres til ordre** på ordrelinjen til feltet **Antall å montere** via **Antall**-feltet i monteringsordren. Finn ut mer under [Selge varer som er montert til ordre](assembly-how-to-sell-items-assembled-to-order.md).  

Verdien i feltet **Antall å montere** er knyttet til **Levere (antall)** på ordrelinjen. Denne relasjonen styrer hvordan du sender delvis og komplett monter-til-ordre-antall:

* Når hele antallet på ordrelinjen er montert til ordre
* I kombinasjonsscenarioer hvor del av salgslinjeantallet er montert til ordren og en del er levert fra lageret.

Kombinasjonsscenarioet gir fleksibilitet for del leveringer. Du kan bruke feltet **Antall som skal monteres** til å angi antallet som skal leveres delvis fra lageret, og ved å sette montere til ordre.  

Hvis hele salgslinjeantallet må monteres til ordre og leveres, kopieres verdien i feltet **Levere (antall)** til feltet **Antall å montere** i den koblede monteringsordren når du endrer antallet som skal leveres. Denne oppdateringen sikrer at antallet som skal leveres forsynes fullstendig av monter-til-ordre-antallet.  

I kombinasjonsscenarier kopieres imidlertid ikke hele verdien i feltet **Levere (antall)** til feltet **Antall å montere** på monteringsordren. I stedet settes det inn en standardverdi i feltet **Antall som skal monteres**. Verdien beregnes fra feltet **Lever (antall)** for å sikre at de monter-til-ordre-antallene leveres først.

Hvis du vil avvike fra standardverdien, for eksempel fordi du bare vil montere flere eller færre av antallet i feltet **Levere (antall)**, kan du endre feltet **Antall å montere** i forhåndsdefinerte regler, som illustrert nedenfor.  

Et eksempel på hvorfor du kan endre antallet som skal monteres, er at du vil bokføre levering av lagerantall delvis før du leverer monteringsavgangen.  

Tabellen nedenfor forklarer reglene som definerer minimums- og maksimumsverdiene som du kan angi i feltet **Antall å montere** for å avvike fra standardverdien i et kombinasjonsscenario. Tabellen viser et kombinasjonsscenario der feltet **Levere (antall)** i den koblede ordrelinjen er endret fra 7 til 4, og **Antall å montere** er derfor som standard satt til 4.  

**Ordrelinje**

|                | **Antall** | **Levere (antall)** | **Ant. som skal monteres til ordre** | **Levert (antall)** |
|----------------|--------------|------------------|-------------------------------|----------------------|
|**Opprinnelig verdi**| 10          | 7                | 7                             | 0                    |
|**Endring**      |              | 4                |                               |                      |

**Monteringsordrehode**

|                | **Antall** | **Levere (antall)** | **Ant. som skal monteres til ordre** | **Levert (antall)** |
|----------------|--------------|------------------|-------------------------------|----------------------|
|**Opprinnelig verdi**| 7           | 7                | 0                             | 7                    |
|**Endring**      |              | 4 (satt inn som standard)|                         |                      |

Basert på dette eksempelet ovenfor kan du endre feltet **Antall å montere** som vist nedenfor:  

* Minimumsantallet du kan angi, er 1. Du må montere minst én enhet for å kunne selge fire enheter, forutsatt at de gjenværende tre er tilgjengelig i lageret.  
* Maksimumsantallet du kan angi, er 4. Denne grensen sikrer at du ikke monterer mer av varen enn du trenger for salget.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/paths/assemble-items-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Se også

[Monteringsstyring](assembly-assemble-items.md)  
[Arbeid med monteringsstykklister](assembly-how-work-assembly-boms.md)  
[Lager](inventory-manage-inventory.md)  
[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
