---
title: Overfør varer mellom lagerlokasjoner
description: 'Finn ut hvordan du flytter beholdning fra ett sted eller lager til et annet, enten med reklassifiseringskladden eller overføringsordrer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'move, warehouse'
ms.search.forms: '5746, 5745, 5759, 5753, 5743, 5758, 5752, 5744, 5749, 5740, 5741, 5742, 5757, 5748, 5747, 9285, 5756, 5755'
---
# Overføre beholdning mellom lokasjoner

Du kan overføre lagervarer mellom lokasjoner ved å opprette overføringsordrer. Du kan også bruke varereklassifiseringskladden.

> [!NOTE]
> Hvis du vil overføre varer, må du definere lokasjoner og overføringsruter. Hvis du vil ha mer informasjon om hvordan du definerer lokasjoner, går du til [Definer lokasjoner](inventory-how-setup-locations.md). Du kan ikke bruke overføringsordrer for *tomme* lokasjoner.

## Overføringsordrer

Du kan levere en utgående overføring fra en lokasjon og mottar en inngående overføring ved destinasjonen. Du kan:

* Spor et antall i transitt
* Definer kalendere, ruter og inngående og utgående håndteringstider for datoberegning og planlegging. Hvis du vil lære mer om planlegging, går du til [Om planleggingsfunksjonalitet](production-about-planning-functionality.md).
* Bruk forskjellige lagerfunksjoner for inngående og utgående lokasjoner.
* Med enkelte begrensninger kan du bruke overføringsordrer for direkte overføringer.

## Varereklassifiseringskladder

* Enkel, direkte overføring av varer mellom lokasjoner.
* Flytt varer mellom hyller. Hvis du vil lære mer om å overføre varer mellom hyller, går du til [Flytt varer som ikke er planlagt, i enkle lageroppsett](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)
* Endre et parti- eller serienummer til et nytt parti- eller serienummer. Hvis du vil lære mer om å reklassifisere serie- og partinumre, går du til [Reklassifisering av serie- eller partinumre](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).
* Endre utløpsdatoen til en ny dato.
* Reklassifiser varer fra en *tom* lokasjon til en faktisk lokasjon.
* Lageraktiviteter administreres ikke. Lagerposter skal opprettes.

## Slik overfører du varer med en overføringsordre

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Overføringsordrer**, og velg deretter den relaterte koblingen.
2. På siden **Overføringsordrer** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Hvis du har fylt ut feltene **I transitt-kode**, **Transportørkode** og **Transportørservice** på siden **Spesif. av overføringsrute** når du definerer overføringsruten, fylles de tilsvarende feltene i overføringsordren ut automatisk.

    Når du fyller ut feltet **Transportørservice**, blir mottaksdatoen for overfør til-lokasjonen beregnet ved at leveringstiden for transportørtjenesten legges til i forsendelsesdatoen.

3. Når du skal fylle ut linjene, kan du angi dem manuelt eller velge ett av følgende alternativer under **Funksjoner**-handlingen:

    * Velg handlingen **Hent hylleinnhold** for å velge eksisterende varer fra en bestemt hylle på lokasjonen.
    * Velg **Hent mottakslinjer** for å velge varer som du nettopp har mottatt på overfør fra-lokasjonen.

    Som lagermedarbeider på overfør fra-lokasjonen, kan du fortsette å levere varene.
4. Velg **Bokfør**-handlingen, velg **Lever**-alternativet, og velg deretter **OK**-knappen.

    Varene er nå i transitt mellom de angitte lokasjonene i henhold til den angitte overføringsruten.

    Som lagermedarbeider på overfør fra-lokasjonen, kan du fortsette å motta varene. Overføringsordrelinjene er de samme som når de sendes, og kan ikke redigeres.
5. Velg **Bokfør**-handlingen, velg **Motta**-alternativet, og velg deretter **OK**-knappen.

## Slik overfører du varer med varereklassifiseringskladden

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Vareoverføringskladder** og velg den relaterte koblingen.
2. På siden **Vareoverføringskladder** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. I **Lokasjonskode**-feltet angir du lokasjonen der varene er lagret.

    > [!NOTE]  
    > Hvis du vil overføre varer uten lokasjonskode, lar du **Lokasjonskode**-feltet være tomt.
4. I feltet **Ny lokasjonskode** angir du lokasjonen du vil overføre varene til.
5. Velg handlingen **Bokfør**.

## Se relatert [Microsoft-opplæring](/training/modules/transfer-items/)

## Se også

[Håndtere lager](inventory-manage-inventory.md)  
[Definer lokasjoner](inventory-how-setup-locations.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
