---
title: "Overføre varer mellom lagerlokasjoner | Microsoft-dokumentasjon"
description: "Beskriver hvordan du flytter beholdning fra ett sted eller lager til et annet, enten med reklassifiseringskladden eller overføringsordrer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 01/25/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 8ee703865f86c0edcc5bff77d8bd04cc2bd107be
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="transfer-inventory-between-locations"></a>Overføre beholdning mellom lokasjoner
Du kan overføre lagervarer mellom lokasjoner ved å opprette overføringsordrer. Du kan også bruke varereklassifiseringskladden.

Med overføringsordrer sender du den utgående overføringen fra én lokasjon og mottar den inngående overføring på den andre lokasjonen. Dette lar deg administrere de involverte lageraktivitetene og gir større visshet om at lagerantallet oppdateres på riktig måte.

Med reklassifiseringskladden fyller du ganske enkelt ut feltene **Lokasjonskode** og **Ny Lokasjonskode**. Når du bokfører kladden, justeres varepostene på de aktuelle lokasjonene. Med denne metoden styres ikke lageraktiviteter.

> [!NOTE]  
>   Hvis du har varer som er registrert på lager uten en lokasjonskode, for eksempel fra en tid da du bare hadde ett lager, kan du ikke overføre disse varene ved å bruke overføringsordrer. I stedet må du bruke reklassifiseringskladden til å klassifisere varer fra en tom lokasjonskode til en faktisk lokasjonskode.  Hvis du vil ha mer informasjon, kan du se trinn 3 i delen "Slik overfører du varer med varereklassifiseringskladden".

Hvis du vil overføre varer, må lokasjoner og overføringsruter defineres. Hvis du vil ha mer informasjon, kan du se [Definere lokasjoner](inventory-how-setup-locations.md).

## <a name="to-transfer-items-with-a-transfer-order"></a>Slik overfører du varer med en overføringsordre
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Overføringsordrer**, og velg deretter den relaterte koblingen.
2. I vinduet **Overføringsordrer** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
>   Hvis du har fylt ut feltene **I transitt-kode**, **Transportørkode** og **Transportørservice** i vinduet **Spesif. av overføringsrute** når du definerer overføringsruten, fylles de tilsvarende feltene i overføringsordren ut automatisk.

    Når du fyller ut feltet **Transportørservice**, blir mottaksdatoen for overfør til-lokasjonen beregnet ved at leveringstiden for transportørtjenesten legges til i forsendelsesdatoen.

    Som lagermedarbeider på overfør fra-lokasjonen, kan du fortsette å levere varene.
3. Velg **Bokfør**-handlingen, velg **Lever**-alternativet, og velg deretter **OK**-knappen.

    Varene er nå i transitt mellom de angitte lokasjonene i henhold til den angitte overføringsruten.

    Som lagermedarbeider på overfør fra-lokasjonen, kan du fortsette å motta varene.
4. Velg **Bokfør**-handlingen, velg **Motta**-alternativet, og velg deretter **OK**-knappen.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Slik overfører du varer med varereklassifiseringskladden
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Vareoverføringskladder**, og velg deretter den relaterte koblingen.
2. I vinduet **Vareoverføringskladder** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. I **Lokasjonskode**-feltet angir du lokasjonen der varene er lagret.

    > [!NOTE]  
>   Hvis du vil overføre varer uten lokasjonskode, lar du **Lokasjonskode**-feltet være tomt.
4. I feltet **Ny lokasjonskode** angir du lokasjonen du vil overføre varene til.
5. Velg handlingen **Bokfør**.

## <a name="see-also"></a>Se også
[Håndtere lager](inventory-manage-inventory.md)  
[Definer lokasjoner](inventory-how-setup-locations.md)  

[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)]-opplevelsen](ui-experiences.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)

