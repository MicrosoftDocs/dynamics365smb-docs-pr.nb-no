---
title: Varianter
description: Gjennomgang for å lære hvordan du oppdaterer behovsprognose for hver variant av et produkt i Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.openlocfilehash: 86b70b3caf1896804ffdc3c76610ffe10ae73c5c
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2022
ms.locfileid: "8525192"
---
# <a name="walkthrough-variants"></a>Gjennomgang: varianter

I denne artikkelen tar vi deg gjennom trinnene for å bruke Contoso Coffee-demodataene for å lære om varianter.

## <a name="scenario"></a>Scenario

Du er produksjonsplanleggeren hos Contoso Coffee. Du må oppdatere behovsprognose for hver variant av varen SP-SCM1006, AutoDripLite. Ettersom de har forskjellige farger, må du kontrollere at den riktige stykklisten brukes for hver variant. Kjør planleggingsforslaget for å beregne forsyning.  

## <a name="steps"></a>Trinn

1. Definer lagerføringsenheter for varen SP-SCM1006, AutoDripLite. Tildel en stykkliste for SKU med variantene RØD og HVIT.

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi *Varer* og velg den relaterte koblingen.  

    2. Åpne varen **SP-SCM1006, AutoDripLite**.

    3. Velg **Opprett lagerføringsenhet**-handlingen.  

    4. Sett feltet **Opprett per** til *Lokasjon og variant*.

    5. Angi et filter for lokasjon til *Nord* , og klikk deretter på **OK**-knappen.

    6. Velg handlingen **Lagerføringsenheter**.  

    7. Oppdater produksjonsstykklistene for følgende lagerføringsenheter:

        1. RØD på NORD, angi SP-SCM1006-RED  

        2. HVIT på NORD, angi SP-SCM1006-WHITE  

        3. Behold produksjonsstykklistenr. tom for SVART på NORD  

2. Oppdater produksjonsoppsett og respekter behovsprognose på lokasjoner og varianter.  

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi *Produksjonsoppsett* og velg den relaterte koblingen.  

    2. Slå på feltet **Bruk prognose på lokasjon**.

    3. Slå på feltet **Bruk prognose på variant**.

    4. Lukk **Produksjonsoppsett**-vinduet.

3. Opprett en ny månedlig behovsprognose, *AUTODRIP*. Filtrer det etter varen SP-SCM1006 og lokasjon NORD. Angi behov for mai for hver variant. 

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi *Behovsprognose*, og velg deretter den relaterte koblingen.

    2. Opprett en ny behovsprognose med navnet *AUTODRIP*.

    3. Velg handlingen **Rediger behovsprognose**.

    4. Velg **Måned** i *Vis etter*-feltet.

    5. I feltet **SP-SCM1006** velger du *Varefilter*

    6. Slå på feltet **Bruk prognose på lokasjon**.

    7. I feltet **Lokasjonsfilter** velger du *NORD*.

    8. Slå på feltet **Bruk prognose på variant**.

    9. For hver linje oppdaterte verdier i kolonnen mai

        1. RØD på NORD, angi 100

        2. HVIT på NORD, angi 200

        3. SVART på NORD, angi 300

    10. Lukk vinduer for behovsprognose

4. Kjør MPS-plan i mai for opprettede behovsprognoser. Gå gjennom komponenter for å se at varemaling samsvarer med variant.

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn *Planleggingsforslag*, og velg deretter den relaterte koblingen.

    2. Velg **Beregn replanlegging**-handlingen.

    3. Slå på **MPS**-feltet.

    4. Slå av **MPS**-feltet.

    5. I feltet **Startdato** kan du velge *1. mai*

    6. I feltet **Sluttdato** kan du velge *31. mai*

    7. I feltet **Bruk prognose** velger du *AUTODRIP*

    8. Velg handlingen **OK**.

    9. For hver opprettet linje velger du **komponent**-handlingen og ser gjennom hvilken maling som brukes.  

## <a name="see-also"></a>Se også

[Innføring i demodata for Contoso Coffee](contoso-coffee-intro.md)  
