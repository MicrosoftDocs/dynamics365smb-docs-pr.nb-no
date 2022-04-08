---
title: Bruk ordreplanlegging til å opprette og reservere forsyning
description: Gjennomgang for å lære hvordan du bruker ordreplanlegging til å opprette den nødvendige produksjonsordren for forsyningen i Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.openlocfilehash: 496eaa1fd1aa8828125018a554c701743bccd5db
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2022
ms.locfileid: "8525193"
---
# <a name="walkthrough-use-order-planning-to-create-and-reserve-supply"></a>Gjennomgang: Bruk ordreplanlegging til å opprette og reservere forsyning

I denne artikkelen tar vi deg gjennom trinnene for å bruke Contoso Coffee-demodataene i ordreplanlegging.

## <a name="scenario"></a>Scenario

Du er produksjonsplanleggeren hos Contoso Coffee. Du har opprettet en produksjonsordre for 100 enheter av varen **SP-SCM1009, Airpot**, og du vil planlegge halvfabrikater for denne ordren. Du bruker ordreplanlegging til å opprette den nødvendige produksjonsordren for forsyningen. Siden du oppretter produksjonsordren for å oppfylle kravene til en bestemt ordre, bestemmer du deg for å reservere avgangen for produksjonsordren.  

## <a name="steps"></a>Trinn

1. Opprett den nylig frigitte produksjonsordren for 100 enheter av varen **SP-SCM1009, Airpot**.

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Frigitt produksjonsordre**, og velg deretter den relaterte koblingen.  

    2. Velg handlingen **Ny** og fyll deretter ut feltene som beskrevet i tabellen nedenfor.  

        |Felt  |Verdi  |
        |---------|---------|
        |**Kildetype** |Vare|
        |**Kildenr.** |SP-SCM1009|
        |**Antall** |100|
    3. Velg handlingen **Oppdater produksjonsordre**.  

    Skriv ned nummeret på den frigitte produksjonsordren.

2. Åpne **Ordreplanlegging**-siden og beregn en ny plan.

    1. Velg handlingen **Planlegging**.  

    2. På **Ordreplanlegging**-siden velger du handlingen **Beregn plan**.  

    3. Bla ned til behovslinjen som representerer den frigitte produksjonsordren du opprettet tidligere.  

    4. Vis linjen for å vise detaljene for behovslinjen. Bekreft at det er et forslag for en produksjonsordre på 100 enheter av vare 1001.  

3. Opprett en ny produksjonsordre for 100 enheter av vare **SP-BOM2000, beholdermontering**, og reserver avgangen for produksjonsordren på vegne av den tilknyttede overordnede ordren.  

    1. Merk av i avmerkingsboksen i **Reserver**-feltet på behovslinjen for 100 enheter for varen SP-BOM2000.

    2. Velg handlingen **Lag bestillinger**.  

    3. Sett feltet **Lag ordrer for** til *Den aktive linjen*.  

    4. Sett feltet **Opprett produksjonsordre** til *Fast planlagt*.

    5. Velg **OK**-knappen for å opprette produksjonsordren.

    6. På **Ordreplanlegging**-siden kontrollerer du at behovslinjen for 100 enheter av varen 1001 er fjernet.

Det er for ordreplanlegging i [!INCLUDE [prod_short](../includes/prod_short.md)].  

## <a name="see-also"></a>Se også

[Innføring i demodata for Contoso Coffee](contoso-coffee-intro.md)  
[Om produksjonsordrer](../production-about-production-orders.md)  
