---
title: Arbeide med lagerperioder
description: 'Du kan kontrollere tidsrammen som brukere kan bokføre endringer i lageret, ved å definere lagerperioder.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'inventory, periods'
ms.search.form: 5828
ms.date: 07/29/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Arbeide med lagerperioder

Lagerperioder er tidsperioder som du kan bokføre lagerendringer i. En lagerperiode defineres av datoen den slutter på, eller sluttdatoen. Når du lukker en lagerperiode, kan du ikke bokføre endringer i lageret, verken forventede eller fakturerte, før denne sluttdatoen. Du kan ikke bokføre nye verdier i lageret før sluttdatoen. Hvis du har åpne vareposter i en lukket periode, det vil si positivt antall som ennå ikke er utlignet mot utgående transaksjoner, kan du fortsatt bruke utgående antall på disse postene, selv om perioden er lukket.  

De følgende delene handler om hvordan du kan:

* Opprett lagerperioder.  
* Lukk lagerperioder.  
* Åpne lagerperioder på nytt.  

## Slik oppretter du en lagerperiode

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerperioder**, og velg deretter den relaterte koblingen.  
2. Opprett en ny linje.  
3. Angi den siste datoen i lagerperioden du vil definere, i **Sluttdato**-feltet. Når perioden er lukket, kan du ikke bokføre lagerendringer før denne datoen.  
4. Skriv inn et beskrivende navn i **Navn**-feltet. Velg **OK**-knappen.  

## Slik lukker du lagerperioder:

**Lukket**-feltet angir om lagerperioden er lukket eller ikke for lagerverdiendringer. Du kan ikke redigere dette feltet.  

Du kan lukke en hvilken som helst lagerperiode hvis følgende er oppfylt:  

* Det er ingen utgående vareposter, det vil si negativ beholdning, i perioden.  
* Kostbeløpet for alle varer er justert ved hjelp av kjørselen **Juster kostverdi - vareposter**.  

Dette betyr at alle utgående transaksjonsantall, for eksempel de fra ordrer, utgående overføringer, salgsfakturaer, bestillingsreturer eller kjøpskreditnotaer, må utlignes mot eksisterende antall på lageret.  

### Slik lukker du en lagerperiode:  

1. Før du lukker en lagerperiode, velger du handlingen **Juster kostverdi – vareposter** for å sikre at alle kostjusteringer er bokført.

    Kjør **rapporten Lukk lagerperiode – test** for å fastslå om Der er noen åpne utgående vareposter i lagerperioden, eller varer som kost ennå ikke er justert for.  
2. Velg handlingen **Kontrollrapport**.  

    Kjør kjørselen **Bokfør lagerkost i Finans** for å sikre at all kost bokføres i Finans.  
3. Velg handlingen **Bokfør lager i Finans**.  
4. På siden **Lagerperioder** velger du lagerperioden du vil lukke.  
5. Velg **Lukk periode**. Når lagerperioden er lukket, kan du ikke bokføre lagerendringer før sluttdatoen. Du må justere kostbeløpet for alle varer med kjørselen **Juster kostverdi - vareposter** før du lukker lagerperioden.  
6. Velg **Ja** for å bekrefte at du vil lukke perioden, eller velg **Nei** hvis du ikke vil lukke den.  
7. Lagerperioden lukkes, og det vises en bekreftelsesmelding når den er ferdig.  

## Åpne lagerperioder på nytt  
Når du har lukket lagerperioden, kan du ikke slette lagerperioden. Du kan imidlertid åpne den på nytt hvis du vil tillate bokføring før sluttdatoen i lagerperioden. Hvis du åpner en periode på nytt, åpnes også alle lagerperioder med sluttdatoer som er senere enn perioden du åpner på nytt.  

### Åpne en lagerperiode på nytt  
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerperioder**, og velg deretter den relaterte koblingen.  
2. Velg lagerperioden du vil åpne på nytt.  
3. Velg **Åpne periode på nytt**. Bekreft at du vil åpne perioden på nytt.  
4. Alle lagerperioder med sluttdatoer som er senere enn perioden du valgte, åpnes på nytt.  

## Se også  
[Utformingsdetaljer: Lagerperioder](design-details-inventory-periods.md)    
[Finans](finance.md)    
[Lager](inventory-manage-inventory.md)    
[Arbeid med Financials](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]