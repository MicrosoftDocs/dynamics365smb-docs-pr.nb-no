---
title: Definere produksjonskalendere | Microsoft-dokumentasjon
description: "En arbeidssenterkalender angir virkedager og arbeidstider, skift, ferie og fravær som utgjør arbeidssenterets disponible kapasitet, målt i tid, i henhold til senterets definerte effektivitets- og kapasitetsverdier. Opprettelse og aktivering av en arbeidssenterkalender omfatter flere forhåndsoppgaver."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 55cefad889557df37d8869926ee7e200cd145d03
ms.contentlocale: nb-no
ms.lasthandoff: 11/26/2018

---
# <a name="set-up-shop-calendars"></a>Definere produksjonskalendere
En arbeidssenter- eller maskinkalender angir virkedager/arbeidstider, skift, ferie og fravær som utgjør senterets disponible kapasitet (målt i tid) i henhold til senterets definerte effektivitets- og kapasitetsverdier.

Som grunnlag for beregning av en bestemt arbeidssenter- eller produksjonsressurskalender må du først definere en eller flere generelle produksjonskalendere. En produksjonskalender definerer en standard arbeidsuke i henhold til starten og slutten på arbeidsdagen samt skiftarbeid. I tillegg definerer produksjonskalenderen faste feriedager i løpet av året.  

I det følgende beskrives hvordan du arbeidssenterkalendere. Trinnene ligner når du definerer produksjonsressurskalendere.  

## <a name="to-create-work-shifts"></a>Slik oppretter du arbeidsskift  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Arbeidsskift**, og velg deretter den relaterte koblingen.  
2.  På en tom linje skriver du inn nummeret i **Kode**-feltet for å identifisere arbeidsskiftet, for eksempel **1**.  
3.  Beskriv arbeidsskiftet i **Beskrivelse**-feltet, for eksempel **1. skift**.  
4.  Fyll eventuelt ut linjer for et andre eller tredje arbeidsskift.  

Selv om arbeidssentrene ikke fungerer for andre arbeidsskift, angir du minst én arbeidsskiftkode.  

## <a name="to-set-up-a-shop-calendar"></a>Slik definerer du en produksjonskalender  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Produksjonskalendere**, og velg deretter den relaterte koblingen.  
2.  På en tom linje skriver du inn nummeret i **Kode**-feltet for å identifisere produksjonskalenderen.  
3.  Beskriv produksjonskalenderen i **Beskrivelse**-feltet.  
4.  Velg **Virkedager**-handlingen.
5.  På siden **Prod.kalender - virkedager** definerer du en fullstendig arbeidsuke med start- og sluttidspunkt for hver enkelt dag.  

    Velg et av skiftene du har definert tidligere, i feltet **Arbeidsskiftkode**. Legg til en linje for hver arbeidsdag og hvert skift. Eksempel:  

    Mandag  07:00 15:00 1   
    Tirsdag 07:00 15:00 1  

    Hvis du trenger en produksjonskalender med to arbeidsskift, må du fylle den ut slik:  

    Mandag 07:00 15:00 1   
    Mandag 15:00 23:00 2  
    Tirsdag 07:00 15:00 1  
    Tirsdag 15:00 23:00 2  

    Ukedager du ikke definerer i produksjonskalenderen, for eksempel lørdag og søndag, anses ganske enkelt som fridager og har ingen verdi for disponibel kapasitet i en arbeidssenterkalender.  

    Når alle virkedager i en uke er definert, kan du lukke siden **Prod.kalender - virkedager** og fortsette med å registrere ferie.  

6.  På siden **Produksjonskalendere** velger du produksjonskalenderen og velger deretter **Ferie**-handlingen.
7. På siden **Prod.kalender - ferie** definerer du årets ferier ved å angi startdato/-klokkeslett, sluttidspunkt og beskrivelse av hver ferie på egne linjer, for eksempel på følgende måte. Eksempel:  

    04/07/14 0:00:00 23:59:00 Sommerferie  
    05/07/14 0:00:00 23:59:00 Sommerferie  
    06/07/14 0:00:00 23:59:00 Sommerferie  

De definerte feriedagene har ingen disponibel kapasitet i arbeidssenterkalenderen.  

Produksjonskalenderen kan nå tilordnes til et arbeidssenter for å beregne produksjonskalenderen for selve arbeidet. Denne kalenderen styrer all operasjonsplanlegging ved arbeidssenteret.  

## <a name="to-calculate-a-work-center-calendar"></a>Slik beregner du en arbeidssenterkalender  

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Arbeidssentre**, og velg deretter den relaterte koblingen.
2. Åpne arbeidssenteret som du vil oppdatere.  
3. I feltet **Produksjonskalenderkode** velger du hvilken produksjonskalender som skal brukes som grunnlag for en arbeidssenterkalender.  
4. Velg handlingen **Kalender**.  
5. På siden **Arbeidssenterkalender** velger du **Vis matrise**.  

    Til venstre på matrisesiden vises arbeidssentrene som er definert. Til høyre vises en kalender med verdier for disponibel kapasitet for hver virkedag i den definerte enheten, for eksempel **480** minutter. Hver linje representerer kalenderen for ett arbeidssenter.  

    > [!NOTE]  
    >  Du kan også vise kapasitetsverdiene for hver uke eller måned ved å endre valget i **Vis etter**-feltet på siden **Arbeidssenterkalender**.  

    Hvis du vil gjenspeile den nye produksjonskalenderen som en linje i det valgte arbeidssenteret, må den først beregnes.  

6.  Velg handlingen **Beregn**.  
7.  På hurtigfanen **Arbeidssenter** kan du angi et filter som bare beregner for ett arbeidssenter. Hvis du ikke angir et filter, beregnes alle eksisterende arbeidssenterkalendere.  
8.  Definer start- og sluttdato for kalenderperioden som skal beregnes, for eksempel ett år fra 01.01.14 til 31.12.14.
9. Velg **OK**-knappen for å beregne kapasiteten.  

Kalenderposter opprettes eller oppdateres nå med visning av disponibel kapasitet for hver periode i henhold til følgende tre sett med hoveddata:  

- Virkedagene og skiftet som er definert i den tilordnede produksjonskalenderen.  
- Verdien i **Kapasitet**-feltet på arbeidssenterkortet.  
- Verdien i **Effektivitet**-feltet på arbeidssenterkortet.  

Den beregnede arbeidssenterkalenderen definerer nå når og hvor stor kapasitet som er tilgjengelig ved dette arbeidssenteret. Dette kontrollerer den detaljerte tidsplanleggingen av operasjoner som utføres ved arbeidssenteret.  

## <a name="to-record-work-center-absence"></a>Slik registrerer du fravær ved et arbeidssenter  
1.  På siden **Arbeidssenterkalender** velger du **Vis matrise**.
2. På siden **Matrise for arbeidssenterkalender** velger du arbeidssenteret og kalenderdagen når fraværstiden skal registreres. Deretter velger du **Fravær**.  
3.  På **Fravær**-siden definerer du starttidspunktet, sluttidspunktet og beskrivelsen av dagens fravær. Eksempel:  

    25/01/01 08:00 10:00 Vedlikehold  

4.  Velg **Oppdater**-handlingen, og lukk deretter **Fravær**-siden.  

Kapasiteten for den valgte dagen er nå redusert med den registrerte fraværstiden.  

## <a name="see-also"></a>Se også  
[Definere hovedkalendere](across-how-to-assign-base-calendars.md)  
[Konfigurere arbeidssentre og produksjonsressurser](production-how-to-set-up-work-and-machine-centers.md)  
[Definere produksjon](production-configure-production-processes.md)  
[Produksjon](production-manage-manufacturing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

