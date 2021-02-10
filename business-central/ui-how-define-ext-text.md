---
title: Legge til ekstra linjer for å definere utvidede beskrivelser
description: Du kan legge til ekstra linjer for å utvide standardteksten som beskriver en vare, en finanskonto og andre data.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9e443a44135bbdaf75f6a064370983592797b10b
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756920"
---
# <a name="add-extended-text"></a>Legge til utvidet tekst

Du kan utvide beskrivelsen av varer, lagerføringsenheter, finanskonti og ressurser ved å legge til ekstra linjer som utvidet tekst. Du kan også definere betingelser for bruk av de ekstra linjene.  

Delen nedenfor beskriver hvordan du legger til utvidet tekst i en beskrivelse av en vare. De samme trinnene gjelder også for lagerføringsenheter, finanskonti og ressurser.  

## <a name="to-define-extended-text-for-an-description"></a>Slik definerer du utvidet tekst for en beskrivelse

1. Åpne kortet for en vare som du vil legge til utvidet tekst for, og velg deretter handlingen **Utvidet tekst**.
2. Fyll ut feltene **Kode** og **Beskrivelse**.
3. Velg **Ny**.
4. Fyll ut **Språkkode**-feltet eller merk av for **Alle språkkoder** hvis du bruker språkkoder.
5. Fyll ut feltene **Startdato** og **Sluttdato** hvis du vil begrense perioden for bruk av den utvidete teksten.
6. I feltet **Tekst** angir du koden for den utvidete teksten.
7. Merk av for de aktuelle dokumenttypene du vil at de utvidete tekstene skal skrives ut på.
8. Lukk siden.

Du kan nå legge til den utvidede teksten i dokumenter. Fremgangsmåten nedenfor forklarer hvordan du legger til utvidet tekst i en ordre, men den samme fremgangsmåten gjelder alle andre dokumenter du har angitt for den utvidede teksten.  

## <a name="to-add-an-extended-item-text-on-a-sales-order-line"></a>Legge til teksten for utvidet vare på en ordrelinje

1. Åpne en ordre med en salgslinje for en vare som har utvidet tekst som er definert. Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).
2. Velg den aktuelle linjen og velg deretter **Sett inn utv. tekster**-handlingen.

## <a name="see-also"></a>Se også

[Definere lager](inventory-setup-inventory.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
