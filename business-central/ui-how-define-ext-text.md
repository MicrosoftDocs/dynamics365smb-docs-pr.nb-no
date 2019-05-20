---
title: Legge til ekstra linjer for å definere utvidede varebeskrivelser | Microsoft-dokumentasjon
description: Du kan legge til ekstra linjer for å utvide standardteksten som beskriver en vare.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a43cca28bb24c5723d81ca28a3d1f86a38f5ad7c
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1248398"
---
# <a name="add-extended-item-text"></a>Legge til utvidet varetekst
Du kan utvide en standardtekst for varer ved å legge til ekstra linjer, og du kan opprette betingelser for bruk av de ekstra linjene. Dette kan du gjøre fra varekort.

## <a name="to-define-extended-text-for-an-item-description"></a>Slik definerer du utvidet tekst for en varebeskrivelse
1. Åpne kortet for en vare som du vil legge til utvidet tekst for, og velg deretter handlingen **Utvidet tekst**.
2. Fyll ut feltene **Kode** og **Beskrivelse**.
3. Velg **Ny**.
4. Fyll ut **Språkkode**-feltet eller merk av for **Alle språkkoder** hvis du bruker språkkoder.
5. Fyll ut feltene **Startdato** og **Sluttdato** hvis du vil begrense perioden for bruk av den utvidete teksten.
6. I feltet **Tekst** angir du koden for den utvidete teksten.
7. Merk av for de aktuelle dokumenttypene du vil at de utvidete tekstene skal skrives ut på.
8. Lukk siden.

## <a name="to-add-an-extended-item-text-on-a-sales-order-line"></a>Legge til teksten for utvidet vare på en ordrelinje
1. Åpne en ordre med en salgslinje for en vare som har utvidet tekst som er definert. Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).
2. Velg den aktuelle linjen og velg deretter **Sett inn utv. tekster**-handlingen.

## <a name="see-also"></a>Se også
[Definere lager](inventory-setup-inventory.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
