---
title: Bokføre lagerkost i finans | Microsoft-dokumentasjon
description: Beskriver hvordan du håndterer de fysiske produktene du handler med, for eksempel håndtering av varene på lageret.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: ce4b573500967e6981fa2cba9b306324f2f43339
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183359"
---
# <a name="reconcile-inventory-costs-with-the-general-ledger"></a>Avstemme lagerkost med finans
Når du bokfører lagertransaksjoner, for eksempel følgesedler, kjøpsfakturaer eller lagerjusteringer, registreres endringene i varekostnader i vareverdipostene. For å gjenspeile endringen i lagerverdien i regnskapet, blir lagerkost automatisk bokført til de relaterte lagerkontoene i Finans. For hver lagertransaksjon du bokfører, bokføres de aktuelle verdiene i lagerkontoen, justeringskontoen og vareforbrukskontoen i Finans.

Automatisk kostnadsbokføring er definert i feltet **Automatisk kostbokføring** på siden **Lageroppsett**.

Selv om lagerkost bokføres automatisk til finans, er det fortsatt nødvendig å sikre at kostbeløpene for varer videresendes til de relaterte utgående salgstransaksjonene. Dette er særlig viktig i situasjoner der du selger varer før du fakturerer kjøpet av varene. Dette kalles kostjustering. Varekostnader justeres automatisk når du bokfører varetransaksjoner, men du kan også justere varekostnader manuelt. Hvis du vil ha mer informasjon, kan du se [Justere varekost](inventory-how-adjust-item-costs.md).

## <a name="to-post-inventory-costs-manually"></a>Slik bokfører du lagerkost manuelt
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokfør lagerkost i Finans**, og velg deretter den relaterte koblingen.
2. Bokfør lagerkost manuelt i Finans ved å starte kjørselen. Når du kjører denne kjørselen, opprettes finansposter på grunnlag av verdiposter. Du kan bokføre postene slik at de summeres per bokføringsgruppe.

> [!NOTE]  
> Når du kjører denne kjørselen, kan det oppstå feil som har å gjøre med manglende oppsett eller inkompatibelt dimensjonsoppsett. Hvis det oppstår feil i dimensjonsoppsettet, overstyrer kjørselen disse feilene og bruker dimensjonene til verdiposten. Hvis det oppstår en annen type feil, hopper kjørselen over bokføringen av verdipostene og viser en oversikt over dem på slutten av rapporten, i en del med overskriften “Poster som er hoppet over”. Hvis du vil bokføre disse postene, må du rette opp feilene.

Hvis du vil ha en oversikt over feil før du kjører bokføringskjørselen, kan du kjøre rapporten **Bokfør lagerkost i Finans - test**. Kontrollrapporten viser en oversikt over alle feilene som har oppstått under en kontrollbokføring. Du kan deretter rette opp feilene og kjøre kjørselen for lagerkost uten å hoppe over noen poster.

Hvis du ganske enkelt vil ha en oversikt over hvilke verdier som kan bokføres i Finans, uten faktisk å utføre bokføringen, kan du kjøre kjørselen **Bokfør lagerkost i Finans** uten faktisk å bokføre verdiene i Finans. Du gjør dette ved å fjerne merket i **Bokfør**-feltet på forespørselssiden. På denne måten genereres rapporten som viser verdiene som er klare til bokføring i Finans, når du kjører kjørselen, men de bokføres ikke.

## <a name="to-audit-the-reconciliation-between-the-inventory-ledger-and-the-general-ledger"></a>Spore avstemmingen mellom lagerposten og Finans
Siden **Lager - finansavstemming** inneholder følgende:

- Viser avstemmingsdifferanser ved å sammenligne hva som er registrert i finans, og hva som er registrert i lager (verdiposter).
- Viser ikke-avstemte kostbeløp i verdipostene i lager som om de var tilordnet til tilsvarende lagerrelaterte konti i finans, og sammenligner disse med totalbeløpene som faktisk er registrert i de samme kontiene i finans.
- Gjenspeiler den doble poststrukturen i finans ved å presentere dataene visuelt på denne måten. En vareforbrukspost har for eksempel en tilsvarende lagerpost.
- Lar brukere vise poster som utgjør kostbeløpene.
- Inkluderer filtre for å avgrense analysen etter dato, vare og lokasjon.
- Forklarer årsaker til avstemmingsdifferanser i informative meldinger.


I **Navn**-kolonnen helt til venstre i rutenettet vises de ulike finanskontotypene som er knyttet til lageret.

Kolonnene **Beholdning**, **Lager (midlertidig)** og **VIA - beholdning** viser fakturert beløp, ufakturert beløp og VIA-beløp for hver finanskontotype. Dette beregnes fra verdiposter, det vil si at de prosjekteres til finanskontiene der de vil havne når de til slutt bokføres til finans.

**I alt**-kolonnen viser summen (i fet skrift) for verdipostbeløpene i de tre lagerkolonnene.

**Finanssum**-kolonnen viser beløpene (i fet skrift) for hver finanskontotype som finnes i finans. Disse beregnes fra finansposter, det vil si at de står for lagerkost som allerede er bokført til finans.

**Differanse**-kolonnen står for differansen mellom **Finanssum** og **I alt**.

Øverst på siden **Lager - finansavstemming** kan du for eksempel angi filtre for å begrense perioden du vil ha informasjon fra.

Hvis du merker av for **Vis advarsel**, og hvis det er avvik mellom lagertotalene og finanstotalene, vises meldinger i **Advarsel**-feltet i rutenettet som forklarer avviket. Hvis du velger Advarsel-feltet, får du mer informasjon om hva advarselen betyr.

Når du har angitt alle relevante filtre, velger du **Vis matrise**. Dataene beregnes og matrisesiden vises.

I kolonnen helt til venstre i rutenettet vises de ulike finanskontotypene som er knyttet til lageret. Deretter vises de fakturerte og ikke-fakturerte (midlertidige) totalene og VIA-beholdningstotalene for hver av disse kontotypene. Disse totalene beregnes fra verdipostene.

De neste kolonnene viser totalene for de samme kontotypene som er beregnet fra finanspostene.

Velg beløpet i et av totalfeltene for å vise postene i lagerrapporten som ble brukt til å beregne totalene. For lagertotaler er postene i lagerrapporten summene av verdipostene for varene. For finanstotalene er postene i lagerrapporten summene fra finanspostene.

## <a name="see-also"></a>Se også  
[Administrere lagerkostnader](finance-manage-inventory-costs.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)    
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)
