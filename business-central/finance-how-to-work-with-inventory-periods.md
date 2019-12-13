---
title: Arbeide med lagerperioder | Microsoft-dokumentasjon
description: Du kan kontrollere tidsrammen som brukere kan bokføre endringer i lageret, ved å definere lagerperioder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: inventory, periods
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8b2a34db5d4e40f99fceb844150312d6c6dffc55
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879635"
---
# <a name="work-with-inventory-periods"></a>Arbeide med lagerperioder
Lagerperioder er tidsperioder som du kan bokføre lagerendringer i. En lagerperiode defineres av datoen den slutter på, eller sluttdatoen. En lagerperiode defineres av datoen den slutter på, eller sluttdatoen. Du kan ikke bokføre eventuelle nye verdier til lageret før sluttdatoen. Hvis du har åpne vareposter i en lukket periode, det vil si positivt antall som ennå ikke er utlignet mot utgående transaksjoner, kan du fortsatt utligne utgående antall mot disse postene, selv om perioden er lukket.  

De følgende delene handler om hvordan du kan:

* Opprett lagerperioder.  
* Lukk lagerperioder.  
* Åpne lagerperioder på nytt.  

## <a name="to-create-an-inventory-period"></a>Slik oppretter du en lagerperiode  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagerperioder**, og velg deretter den relaterte koblingen.  
2. Opprett en ny linje.  
3. Angi den siste datoen i lagerperioden du vil definere, i **Sluttdato**-feltet. Når perioden er lukket, kan du ikke bokføre lagerendringer før denne datoen.  
4. Skriv inn et beskrivende navn i **Navn**-feltet. Velg **OK**.  

## <a name="closing-inventory-periods"></a>Lukke lagerperioder  
**Lukket**-feltet angir om lagerperioden er lukket eller ikke for lagerverdiendringer. Du kan ikke redigere dette feltet.  

Du kan lukke en hvilken som helst lagerperiode gitt at følgende betingelser er oppfylt:  

* Det er ingen utgående vareposter, det vil si negativ beholdning, i perioden.  
* Kostbeløpet for alle varer er justert ved hjelp av kjørselen **Juster kostverdi - vareposter**.  

Dette betyr at alle utgående transaksjonsantall, for eksempel de fra ordrer, utgående overføringer, salgsfakturaer, bestillingsreturer eller kjøpskreditnotaer, må utlignes mot eksisterende antall på lageret.  

### <a name="to-close-an-inventory-period"></a>Slik lukker du en lagerperiode:  
1. Før du lukker en lagerperiode, velger du handlingen **Juster kostverdi – vareposter** for å sikre at alle kostjusteringer er bokført.

     Kjør rapporten **Lukk lagerperiode - test** for å fastslå om det er noen åpne utgående vareposter i lagerperioden eller varer som kost ikke er justert for ennå.  
2. Velg **Lukk lagerperiode - test**.  

     Kjør kjørselen **Bokfør lagerkost i Finans** for å sikre at all kost bokføres i Finans.  
3. Velg handlingen **Bokfør lager i Finans**.  
4. På siden **Lagerperioder** velger du lagerperioden du vil lukke.  
5. Velg **Lukk periode**. Når lagerperioden er lukket, kan du ikke bokføre lagerendringer før sluttdatoen. Du må justere kostbeløpet for alle varer med kjørselen **Juster kostverdi - vareposter** før du lukker lagerperioden.  
6. Velg **Ja** for å bekrefte at du vil lukke perioden, eller velg **Nei** hvis du ikke vil lukke den.  
7. Lagerperioden lukkes og en bekreftelsesmelding vises når prosessen er ferdig.  

## <a name="reopening-inventory-periods"></a>Åpne lagerperioder på nytt  
Når du har lukket lagerperioden, kan du ikke slette den. Du kan imidlertid åpne den på nytt hvis du vil tillate bokføring før sluttdatoen i lagerperioden. Hvis du åpner en periode på nytt, åpnes også alle lagerperioder med sluttdatoer som er senere enn perioden du åpner på nytt.  

### <a name="to-reopen-an-inventory-period"></a>Åpne en lagerperiode på nytt  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagerperioder**, og velg deretter den relaterte koblingen.  
2. Velg lagerperioden du vil åpne på nytt.  
3. Velg **Åpne periode på nytt**. Bekreft at du vil åpne perioden på nytt.  
4. Alle lagerperioder med sluttdatoer som er senere enn perioden du valgte, åpnes på nytt.  

## <a name="see-also"></a>Se også  
[Designdetaljer: Beholdningsperioder](design-details-inventory-periods.md)  
[Finans](finance.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeide med Financials](ui-work-product.md)
