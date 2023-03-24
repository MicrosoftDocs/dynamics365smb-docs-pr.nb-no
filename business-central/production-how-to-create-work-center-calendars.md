---
title: Definere produksjonskalendere
description: 'Oppretting og aktivering av en arbeidssenterkalender omfatter flere oppgaver, inkludert oppsett av produksjonskalendere og oppretting av arbeidsskift.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '9291, 9293, 9295, 99000750, 99000751, 99000752, 99000753, 99000759, 99000769, 99000770, 99000771, 99000772, 99000920'
ms.date: 06/22/2021
ms.author: edupont
---
# Definere produksjonskalendere

En arbeidssenter- eller maskinkalender angir virkedager/arbeidstider, skift, ferie og fravær som utgjør senterets disponible kapasitet (målt i tid) i henhold til senterets definerte effektivitets- og kapasitetsverdier.

Som grunnlag for beregning av en bestemt arbeidssenter- eller produksjonsressurskalender må du først definere en eller flere generelle produksjonskalendere. En produksjonskalender definerer en standard arbeidsuke i henhold til starten og slutten på arbeidsdagen samt skiftarbeid. I tillegg definerer produksjonskalenderen faste feriedager i løpet av året.  

I det følgende beskrives hvordan du arbeidssenterkalendere. Trinnene ligner når du definerer produksjonsressurskalendere.  

## Slik oppretter du arbeidsskift  
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Arbeidsskift**, og velg deretter den relaterte koblingen.  
2.  På en tom linje skriver du inn nummeret i **Kode**-feltet for å identifisere arbeidsskiftet, for eksempel **1**.  
3.  Beskriv arbeidsskiftet i **Beskrivelse**-feltet, for eksempel **1. skift**.  
4.  Fyll eventuelt ut linjer for et andre eller tredje arbeidsskift.  

Selv om arbeidssentrene ikke fungerer for andre arbeidsskift, angir du minst én arbeidsskiftkode.  

## Slik definerer du en produksjonskalender  
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Produksjonskalender**, og velg deretter den relaterte koblingen.  
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

## Slik beregner du en arbeidssenterkalender  

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Arbeidssentre**, og velg deretter den relaterte koblingen.
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

## Slik registrerer du fravær ved et arbeidssenter  
1.  På siden **Arbeidssenterkalender** velger du **Vis matrise**.
2. På siden **Matrise for arbeidssenterkalender** velger du arbeidssenteret og kalenderdagen når fraværstiden skal registreres. Deretter velger du **Fravær**.  
3.  På **Fravær**-siden definerer du starttidspunktet, sluttidspunktet og beskrivelsen av dagens fravær. Eksempel:  

    25/01/01 08:00 10:00 Vedlikehold  

4.  Velg **Oppdater**-handlingen, og lukk deretter **Fravær**-siden.  

Kapasiteten for den valgte dagen er nå redusert med den registrerte fraværstiden.  

## Se også  
[Definere hovedkalendere](across-how-to-assign-base-calendars.md)  
[Konfigurere arbeidssentre og produksjonsressurser](production-how-to-set-up-work-and-machine-centers.md)  
[Definere produksjon](production-configure-production-processes.md)  
[Produksjon](production-manage-manufacturing.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]