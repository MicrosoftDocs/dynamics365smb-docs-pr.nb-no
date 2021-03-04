---
title: Håndtere partistørrelser | Microsoft Docs
description: Dette emnet beskriver ulike måter å håndtere partistørrelser på.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 6f07828e969d5a8394657bc1e05d44156ada5411
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749021"
---
# <a name="handling-lot-sizes-in-production"></a>Håndtere partistørrelser i produksjon
Når det gjelder antall, kan det hende at antall varer du produserer i en produksjonsoperasjon, ikke koordineres til hvordan de selges. Du kan for eksempel produsere hundrevis av varer i et enkelt parti, men selge hver vare individuelt. Når du konfigurerer produksjonsrutene og stykklistene, er det noen få nyanser du bør ta hensyn til når det gjelder partistørrelser. Dette emnet beskriver hvordan partistørrelser påvirker kostnadsberegninger og ressursplanlegging.

## <a name="units-of-measure-in-production-bill-of-materials"></a>Enhet i produksjonsstykkliste
Selv om du angir lagerenheten for en vare, kan stykklisten bruke en annen enhet for det ferdige produktet. Lagerenhet for en vare kan for eksempel være STK, men stykklisten kreve pall eller tonn. Dette er nyttig når maskiner eller råkomponenter dikterer volumet. Det kan for eksempel hende at du ikke vil bake en enkelt muffins fordi det er vanskelig å bruke en del av et egg. I stedet baker du mange muffins for å redusere avfall. Hvis du vil ha mer informasjon, kan du se [Opprette produksjonsstykklister](production-how-to-create-production-boms.md).

## <a name="lot-size-on-routing-lines"></a>Partistørrelse på rutelinjer
Fra et ruteperspektiv kan du angi en partistørrelse på rutelinjene for å justere kapasiteten for maskinene som produserer varene. Operasjonstiden på rutelinjene reduseres proporsjonalt med partistørrelsen. 

Dette fungerer bra når antallet i en produksjonsordre er en faktor av partistørrelsen i ruten. Hvis det for eksempel er plass til 10 muffins på bakearket, bør du bake 10, 20, 30 og så videre, og ikke 5 eller 15.  Dette er mye mindre problem hvis du håndterer store antall.

Partistørrelse er også populært i produksjonsmiljøer der avgang måles som antall du kan lage i løpet av en fast tidsperiode. Eksempel: Hvis volum per 9 timeskift er 25 000 kubikkfot, kan du angi operasjonstid som 9 timer og partistørrelse som 25 000.
Produksjonsordreantallet blir mindre viktig når produksjonsordrens operasjonstid beregnes som operasjonstid / partistørrelse for å få kjøretid per stykk.
 
> [!NOTE]
> Verdien som er definert i partistørrelse, har ikke innvirkning på tiden som er angitt i feltet **Oppstillingstid** for rutelinjen. Oppsettet skjer bare én gang, selv om det er flere partier. Det kan for eksempel hende at du ikke trenger å bruke ovn for det andre partiet med muffins. Hvis du vil ha mer informasjon, kan du se [Opprette ruter](production-how-to-create-routings.md).

## <a name="lot-sizes-for-items-and-stockkeeping-units"></a>Partistørrelser for varer og lagerføringsenheter
Partistørrelser som er definert for ruter, er ikke det samme som partistørrelser for varer eller lagerføringsenheter. Disse verdiene brukes til ulike formål og har ingen innvirkning på produksjonskapasiteten. 

## <a name="lot-size-on-item-and-stockkeeping-units"></a>Partistørrelser på vare og lagerføringsenheter
For varer og lagerføringsenheter har partistørrelser følgende konsekvenser for kostnadsberegning og forsyningsplanlegging:

* Hvis du aktiverer **Kost inkl. oppstilling** på siden **Produksjonsoppsett**, blir kost for oppsettet lagt til standardkostnaden for beregning av standardkostnaden. Hvis du angir en partistørrelse, vil oppstillingskostnaden for ruteoperasjonen bli redusert i henhold til én partistørrelse. Hvis for eksempel partistørrelsen definert på varekortet er 10, og det tar 15 minutter å varme opp ovnen, vil kostnaden til drivstoffet bli fordelt til 10 muffins som ca. 1,5 minutter. 

> [!NOTE]
> Oppsettkostnadene håndteres forskjellig fra perspektivet standardkostnad og kapasitetsfordeling. Hvis produsert antall ikke samsvarer med partistørrelse definert på varekortet, vil det føre til variasjon. Hvis du vil ha mer informasjon, kan du se [Administrere lagerkostnader](finance-manage-inventory-costs.md). <!--not sure that I got this part right seems to repeat the first example.-->

Når det gjelder forsyningsplanlegging, fungerer innstillingen for partistørrelse på varer med **Standard avdempings-%** på siden **Produksjonsoppsett**. [!INCLUDE[prod_short](includes/prod_short.md)] ignorerer endringer i etterspørsel som er under avdempingsprosenten, og vil ikke opprette planleggingsforslag. Det er for eksempel angitt 15 i feltet standard avdempings-%, og vi har en produksjonsordre på 20 muffins for å mate 20 gjester, men én gjest kan ikke delta. [!INCLUDE[prod_short](includes/prod_short.md)] ignorerer gjesten som mangler, fordi det bare er 10 % av partistørrelsen 10 definert for varen. Hvis to gjester ikke kan komme, vil imidlertid [!INCLUDE[prod_short](includes/prod_short.md)] foreslå at vi reduserer ordreantallet, fordi to er 20 % av partistørrelsen. Hvis du vil ha mer informasjon om planlegging, kan du se [Planlegging](production-planning.md).

## <a name="see-also"></a>Se også
[Opprette produksjonsstykklister](production-how-to-create-production-boms.md)  
[Arbeide med produksjonsbunkeenhet](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)
[Opprett ruter](production-how-to-create-routings.md)  
[Administrere lagerkostnader](finance-manage-inventory-costs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]