---
title: Arbeide med katalogvarer| Microsoft-dokumentasjon
description: "Beskriver hvordan du kan handler med varer som ikke er på lager."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ae4710c0771d2b10c691f878ad6532e95f3b2912
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-work-with-nonstock-items"></a>Arbeide med katalogvarer
Du kan tilby bestemte varer til kundene for å gjøre det mer bekvemmelig for dem, som du ikke vil ha på lager før du begynner å selge dem. Når du vil begynne å ha slike varer på lager, kan du konvertere dem til vanlige varekort på to måter.

* Fra et katalogvarekort kan du opprette et nytt varekort basert på en mal.
* Fra en salgsordrelinje av typen **Vare** med et tomt **Nei*-felt velger du en katalogvare. Et varekort opprettes automatisk for katalogvaren.

**Merk**: Du kan ikke velge en katalogvare fra **Salgsfaktura**-vinduet. Du kan velge en katalogvare fra **Tilbud**-vinduet, men katalogvaren vil ikke bli konvertert til en vanlig vare når du bruker **Lag ordre**-funksjonen.

En katalogvare har vanligvis varenummeret til leverandøren som leverer den. For å gjøre det mulig å konvertere et katalogvarekort til et vanlig varekort, må du først definere hvordan varenummerering for leverandør skal konverteres til din egen varenummerering.   

## <a name="to-create-a-nonstock-item"></a>Slik oppretter du en katalogvare:
Katalogvarekort har mye mindre informasjon enn vanlige varekort fordi du bare bruker dem til tilbud i salgstilbud og på andre måter. Derfor må de konverteres til vanlige varekort før du kan bokføre salgstransaksjoner for dem.

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Katalogvarer**, og deretter velger du den beslektede koblingen.
2. Velg handlingen **Ny**.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-how-nonstock-item-numbers-are-converted-to-your-own-numbering"></a>Slik definerer du hvordan katalogvarenumre konverteres til din egen nummerering:
For å gjøre det mulig å konvertere et katalogvarekort til et vanlig varekort, må du først definere hvordan varenummereringen for leverandøren skal konverteres til ditt eget varenummereringsformat.

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Katalogvare - oppsett**, og deretter velger du den beslektede koblingen.
2. Fyll ut feltene etter behov.

## <a name="to-convert-a-nonstock-item-to-a-normal-item"></a>Slik konverterer du en katalogvare til en vanlig vare:
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Katalogvarer**, og deretter velger du den beslektede koblingen.
2. Åpne kortet for katalogvaren som du vil konvertere til en vanlig vare.
3. I vinduet **Kort for katalogvare** velger du handlingen **Opprett vare**.

Et nytt varekort forhåndsutfylt med informasjon fra katalogvaren og en relevant varemal opprettes. Du kan deretter fylle ut eller redigere felt på det nye varekortet etter behov. Hvis du vil ha mer informasjon, kan du se [Registrere nye varer](inventory-how-register-new-items.md).

## <a name="to-sell-a-nonstock-item-and-convert-it-to-a-normal-item"></a>Slik selger du en katalogvare og konverterer den til en vanlig vare:
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Ordrer**, og deretter velger du den beslektede koblingen.
2. Velg handlingen **Ny**. Fyll ut feltene på hurtigfanen **Generelt** som for ordrer. Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).
3. På en ny salgslinje, i **Type**-feltet velger du **Vare**, men lar feltet **Nr.** stå tomt.
4. Velg handlingen **Linje** og velg deretter handlingen **Velg katalogvarer**.

    Katalogvaren konverteres til en vanlig vare. Et nytt varekort forhåndsutfylt med informasjon fra katalogvaren og en relevant varemal opprettes.
5. I **Katalogvarer**-vinduet velger du katalogvaren du vil selge, og velger deretter **OK**-knappen.
6. Når ordren er fullført, kan du velge handlingen **Bokfør**.

Du kan deretter fylle ut eller redigere felt på det nye varekortet etter behov. Hvis du vil ha mer informasjon, kan du se [Registrere nye varer](inventory-how-register-new-items.md).

**Merk**: En varekryssreferansepost opprettes automatisk for leverandøren av varen mellom leverandørens varenummer og det nye varenummeret ditt.

## <a name="see-also"></a>Se også
[Registrere nye varer](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

