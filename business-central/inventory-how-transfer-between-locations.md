---
title: Overfør varer mellom lagerlokasjoner
description: Beskriver hvordan du flytter beholdning fra ett sted eller lager til et annet, enten med reklassifiseringskladden eller overføringsordrer.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.search.forms: 5746, 5745, 5759, 5753, 5743, 5758, 5752, 5744, 5749, 5740, 5741, 5742, 5757, 5748, 5747, 9285, 5756, 5755
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b3fb127931f433ab7f433fca4ab8ba4a9ef306e1
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/19/2022
ms.locfileid: "9534862"
---
# <a name="transfer-inventory-between-locations"></a>Overføre beholdning mellom lokasjoner

Du kan overføre lagervarer mellom lokasjoner ved å opprette overføringsordrer. Du kan også bruke varereklassifiseringskladden.

Med overføringsordrer sender du den utgående overføringen fra én lokasjon og mottar den inngående overføring på den andre lokasjonen. Dette lar deg administrere de involverte lageraktivitetene og gir større visshet om at lagerantallet oppdateres på riktig måte.

Med reklassifiseringskladden fyller du ganske enkelt ut feltene **Lokasjonskode** og **Ny Lokasjonskode**. Når du bokfører kladden, justeres varepostene på de aktuelle lokasjonene. Med denne metoden styres ikke lageraktiviteter.

> [!NOTE]  
>   Hvis du har varer som er registrert på lager uten en lokasjonskode, for eksempel fra en tid da du bare hadde ett lager, kan du ikke overføre disse varene ved å bruke overføringsordrer. I stedet må du bruke reklassifiseringskladden til å klassifisere varer fra en tom lokasjonskode til en faktisk lokasjonskode.  Hvis du vil ha mer informasjon, kan du se trinn 3 i [Slik overfører du varer med varereklassifiseringskladden](inventory-how-transfer-between-locations.md#to-transfer-items-with-the-item-reclassification-journal).

Hvis du vil overføre varer, må lokasjoner og overføringsruter defineres. Hvis du vil ha mer informasjon, kan du se [Definere lokasjoner](inventory-how-setup-locations.md).

## <a name="to-transfer-items-with-a-transfer-order"></a>Slik overfører du varer med en overføringsordre

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Overføringsordrer**, og velg deretter den relaterte koblingen.
2. På siden **Overføringsordrer** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Hvis du har fylt ut feltene **I transitt-kode**, **Transportørkode** og **Transportørservice** på siden **Spesif. av overføringsrute** når du definerer overføringsruten, fylles de tilsvarende feltene i overføringsordren ut automatisk.

    Når du fyller ut feltet **Transportørservice**, blir mottaksdatoen for overfør til-lokasjonen beregnet ved at leveringstiden for transportørtjenesten legges til i forsendelsesdatoen.

3. Når du skal fylle ut linjene, kan du angi dem manuelt eller velge ett av følgende alternativer under **Funksjoner**-handlingen:
    - Velg handlingen **Hent hylleinnhold** for å velge eksisterende varer fra en bestemt hylle på lokasjonen.
    - Velg **Hent mottakslinjer** for å velge varer som du nettopp har mottatt på overfør fra-lokasjonen.   

    Som lagermedarbeider på overfør fra-lokasjonen, kan du fortsette å levere varene.
4. Velg **Bokfør**-handlingen, velg **Lever**-alternativet, og velg deretter **OK**-knappen.

    Varene er nå i transitt mellom de angitte lokasjonene i henhold til den angitte overføringsruten.

    Som lagermedarbeider på overfør fra-lokasjonen, kan du fortsette å motta varene. Overføringsordrelinjene er de samme som når de sendes, og kan ikke redigeres.
5. Velg **Bokfør**-handlingen, velg **Motta**-alternativet, og velg deretter **OK**-knappen.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Slik overfører du varer med varereklassifiseringskladden

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Vareoverføringskladder** og velg den relaterte koblingen.
2. På siden **Vareoverføringskladder** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. I **Lokasjonskode**-feltet angir du lokasjonen der varene er lagret.

    > [!NOTE]  
    >   Hvis du vil overføre varer uten lokasjonskode, lar du **Lokasjonskode**-feltet være tomt.
4. I feltet **Ny lokasjonskode** angir du lokasjonen du vil overføre varene til.
5. Velg handlingen **Bokfør**.

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/transfer-items/)

## <a name="see-also"></a>Se også

[Håndtere lager](inventory-manage-inventory.md)  
[Definer lokasjoner](inventory-how-setup-locations.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
