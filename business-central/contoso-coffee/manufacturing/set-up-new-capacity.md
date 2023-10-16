---
title: Definer ny kapasitet
description: Gjennomgang for å lære hvordan du oppretter et nytt arbeidssenter med en kapasitetskalender for ett enkelt skift i Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: brentholtorf
ms.author: bholtorf
---

# Gjennomgang: Definer ny kapasitet

I denne artikkelen tar vi deg gjennom trinnene for å bruke Contoso Coffee-demodataene til å administrerer kapasitet.  

## Scenario

Du er produksjonsplanleggeren hos Contoso Coffee. Som et svar på endringer i produksjonen, må du definere et nytt arbeidssenter, testavdeling. Det nye arbeidssenteret har én produksjonsressurs, tester. De nye sentrene må ha kapasitetskalenderen for ett skift fra 08:00 til 16:00, mandag til fredag.  

## Trinn

1. Definer arbeidssenteret.

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **arbeidssentre**, og velg deretter den relaterte koblingen.  

    2. Velg handlingen **Ny** og fyll deretter ut feltene som beskrevet i tabellen nedenfor.  

        |Felt  |Verdi  |
        |---------|---------|
        |**Nr.** |700|
        |**Navn** |Testavdeling|
        |**Arbeidssentergruppekode** |1, Produksjonsavdeling|
        |**Direkte enhetskost**|3.25|
        |**Beregning av enhetskost**|Klokkeslett|
        |**Trekkmetode**|Manuell|
        |**Bokføringsgruppe – vare**|UTEN MVA.</br></br>Vær oppmerksom på at dette valget avhenger av regnskapsoppsettet og landet/området.|
        |**Enhetskode** |MINUTTER|
        |**Kapasitet** |1|
        |**Effektivitet** |90|
        |**Produksjonskalenderkode** |1|

        I feltet **Produksjonskalenderen** betyr innstillingen 1 ett skift fra mandag til fredag.

    3. Lukk arbeidssenterkortet.

2. Definer produksjonsressursene.

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **produksjonsressurser**, og velg deretter den relaterte koblingen.  

    2. Velg handlingen **Ny** og fyll deretter ut feltene som beskrevet i tabellen nedenfor.  

        |Felt  |Verdi  |
        |---------|---------|
        |**Nr.** |760|
        |**Navn** |Tester|
        |**Arbeidssenternr.** |700, Testavdeling|
        |**Direkte enhetskost**|3.25|
        |**Trekkmetode**|Manuell|
        |**Bokføringsgruppe – vare**|UTEN MVA.</br></br>Vær oppmerksom på at dette valget avhenger av regnskapsoppsettet og landet.|
        |**Kapasitet** |1|
        |**Effektivitet** |90|
    3. Utvid hurtigfanen **Ruteoppsett**, og angi **10** i feltet *Oppstillingstid*.  

3. Beregn kapasitetskalender for produksjonsressurs.  

    1. Velg handlingen **Kalender**.  

    2. I siden **Produksjonsressurskalender** på hurtigfanen **Matrisealternativer** angir du feltet **Vis etter** til *Måned*.  

    3. Velg handlingen **Vis matrise**.  

    4. På siden **Matrise for produksjonsressurskalender** velger du **Beregn**.  

    5. I siden **Beregn produksjonsressurskalender** på hurtigfanen **Alternativer** angir du feltet **Startdato** til *1. januar*.  

    6. Sett **Sluttdato**-feltet til 31. desember.  

    7. På hurtigfanen **Produksjonsressurs** fyller du ut **Nr.**-filterfeltet velger du *760, Testing*.  

    8. Velg **OK**-knappen. Når kjørselen er ferdig, går du tilbake til siden **Matrise for produksjonsressurskalenderen**.  

    9. Velg handlingen **Oppdater**.  

    10. På linjen for produksjonsressurs 760, testing, går du nedover i verdien i kolonnen Januar.  

På siden **Kalenderposter** er postene for daglig kapasitet i feltet **Kapasitet (total)** 480 minutter. Dette gjenspeiler ett åttetimers skift for hver arbeidsdag. I tillegg viser feltet **Kapasitet (effektiv)** 432 minutter. Dette gjenspeiler 90 prosent effektivitetsraten du tildelte til produksjonsressursen.  

## Se også

[Innføring i demodata for Contoso Coffee](../contoso-coffee-intro.md)  
