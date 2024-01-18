---
title: Opprett en fast planlagt produksjonsordre og endre den
description: 'Gjennomgang for en produksjonsplanlegger hos Contoso Coffee som ønsker å opprette en fast planlagt produksjonsordre, og deretter endre den.'
ms.date: 12/12/2023
ms.topic: article
ms.service: dynamics365-business-central
author: brentholtorf
ms.author: bholtorf
---

# <a name="walkthrough-create-a-firm-planned-production-order-and-change-it"></a>Gjennomgang: Opprett en fast planlagt produksjonsordre og endre den

I denne artikkelen tar vi deg gjennom trinnene for å bruke Contoso Coffee-demodataene for å arbeide med produksjonsordrer.  

## <a name="scenario"></a>Scenario

Eduardo, produksjonsplanleggeren hos Contoso Coffee, må opprette en ny produksjonsordre for ti enheter av varen **SP-SCM1009, Airpot** som må være klar 28. april. Eduardo bakoverplanlegger denne og bekrefter at han kan starte ordren 27. april.  

Kort tid etter at denne oppgaven er fullført, blir Eduardo bedt om å øke ordren til 50 enheter. Når han gjør dette, trykker funksjonen for bakoverplanlegging ordrens startdato for tidlig. Derfor planlegger Eduardo å viderekoble ordren fra 23. april for å kunne avgjøre en mer realistisk sluttdato.  

## <a name="steps"></a>Trinn

1. Opprett den innledende produksjonsordren for ti enheter av varen **SP-SCM1009, Airpot**.

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Fast planlagte prod.ordrer** og velg den relaterte koblingen.  

    2. Velg handlingen **Ny** og fyll deretter ut feltene som beskrevet i tabellen nedenfor.  

        |Felt  |Verdi  |
        |---------|---------|
        |**Kildetype** |Vare|
        |**Kildenr.** |SP-SCM1009|
        |**Antall** |10|
        |**Forfallsdato**|April 28  |

    3. Velg handlingen **Oppdater produksjonsordre**.  

    4. På siden **Oppdater produksjonsordre** godtar du alle standarder og velger **OK**-knappen for å starte prosessen.  

        I nåværende oppsett bruker denne prosessen bakoverplanlegging. I den nye linjen på produksjonsordren er startdatoen 26. april.  

2. Endre produksjonsordrens antall til 50 enheter, og planlegg ordren.  

    1. På hurtigfanen **Linjer** i **produksjonsstykklisten** velger du den nylig tillagte linjen, og deretter angir du **50** i feltet *Antall*.  

3. Velg handlingen **Oppdater produksjonsordre**.  

    Startdatoen er nå flyttet tilbake til 20. april. Dette er ikke en akseptabel dato for Eduardo.

4. Utløs en fremoverplanlegging for produksjonsordren.

    1. På hurtigfanen **Tidsplan** angir du feltet **Startdato** til *23. april*.

    Starten på ordren er nå 25. april, og sluttdatoen er 2. mai. Forfallsdatoen for ordren er angitt én dag senere, 3. mai. Eduardo vet nå at det vil ta frem til 3. mai å levere den økte ordren.

> [!NOTE]
> Planlegging av en ordre ved å endre start- eller sluttdato krever ikke den satsvise jobben **Forny produksjonsordre** fordi alle datoer beregnes på nytt automatisk.

Den nye produksjonsordren er nå definert, og Eduardos krav er oppfylt.  

## <a name="see-also"></a>Se også

[Innføring i demodata for Contoso Coffee](../contoso-coffee-intro.md)  
