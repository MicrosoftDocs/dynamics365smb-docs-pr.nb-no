---
title: Opprette og administrere katalogvarer | Microsoft dokumenter
description: Beskriver hvordan du handler med varer som er i leverandørerlisten for varer, men som ikke er i din egen oversikt over varer.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 328417821e8e5cc14bc8267e64687ce2a14f15af
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588554"
---
# <a name="work-with-catalog-items"></a>Arbeide med katalogvarer
Du kan tilby bestemte varer til kundene for å gjøre det mer bekvemmelig for dem, som du ikke vil administrere i systemet før du begynner å selge dem. Når du vil begynne å administrere slike varer i systemet, kan du konvertere dem til vanlige varekort på to måter.

* Fra et katalogvarekort kan du opprette et nytt varekort basert på en mal.
* Fra en salgsordrelinje av typen **Vare** med et tomt **Nei**-felt velger du en katalogvare. Et varekort opprettes deretter automatisk for katalogvaren.

> [!NOTE]  
> Du kan ikke velge en katalogvare fra **Salgsfaktura**-siden.<br /><br />
> Du kan velge en katalogvare fra **Tilbud**-siden, men katalogvaren vil ikke bli konvertert til en vanlig vare når du bruker **Lag ordre**-funksjonen.

En katalogvare har vanligvis varenummeret til leverandøren som leverer den. For å gjøre det mulig å konvertere et katalogvarekort til et vanlig varekort, må du først definere hvordan varenummerering for leverandør skal konverteres til din egen varenummerering.   

> [!Important]
> Katalogvarer må ikke forveksles med ikke-lagervarer, som er vanlige varer som blir gitt typen **Ikke-lagervare** for å utelukke dem fra tilgjengelighet og kostberegninger, for eksempel fordi de bare brukes internt og har en lav kostnad. Hvis du vil ha mer informasjon, kan du se [Om varetyper](inventory-about-item-types.md).

## <a name="to-create-a-catalog-item"></a>Slik oppretter du en katalogvare
Katalogvarekort har mye mindre informasjon enn vanlige varekort fordi du bare bruker dem til tilbud i salgstilbud og på andre måter. Derfor må de konverteres til vanlige varekort før du kan bokføre salgstransaksjoner for dem.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Katalogvarer**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a>Slik definerer du hvordan katalogvarenumre konverteres til din egen nummerering:
For å gjøre det mulig å konvertere et katalogvarekort til et vanlig varekort, må du først definere hvordan varenummereringen for leverandøren skal konverteres til ditt eget varenummereringsformat.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Oppsett av katalogvare**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov.

## <a name="to-convert-a-catalog-item-to-a-normal-item"></a>Slik konverterer du en katalogvare til en vanlig vare:
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Katalogvarer**, og velg deretter den relaterte koblingen.
2. Åpne kortet for katalogvaren som du vil konvertere til en vanlig vare.
3. På siden **Katalogvarekort** velger du handlingen **Opprett vare**.

Et nytt varekort forhåndsutfylt med informasjon fra katalogvaren og en relevant varemal opprettes. Du kan deretter fylle ut eller redigere felt på det nye varekortet etter behov. Hvis du vil ha mer informasjon, kan du se [Registrere nye varer](inventory-how-register-new-items.md).

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a>Slik selger du en katalogvare og konverterer den til en vanlig vare:
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**. Fyll ut feltene på hurtigfanen **Generelt** som for ordrer. Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).
3. På en ny salgslinje, i **Type**-feltet velger du **Vare**, men lar feltet **Nr.** stå tomt.
4. Velg handlingen **Linje** og velg deretter handlingen **Velg katalogvarer**.

    Katalogvaren konverteres til en vanlig vare. Et nytt varekort forhåndsutfylt med informasjon fra katalogvaren og en relevant varemal opprettes.
5. På siden **Katalogvarer** velger du katalogvaren du vil selge, og velger deretter **OK**-knappen.
6. Når ordren er fullført, kan du velge handlingen **Bokfør**.

Du kan deretter fylle ut eller redigere felt på det nye varekortet etter behov. Hvis du vil ha mer informasjon, kan du se [Registrere nye varer](inventory-how-register-new-items.md).

> [!NOTE]  
>   En varereferanse er automatisk vare mellom leverandørens varenummer og det nye varenummeret ditt. Se [Bruke varereferanser](inventory-how-use-item-cross-refs.md) for mer informasjon.

## <a name="see-also"></a>Se også
[Registrere nye varer](inventory-how-register-new-items.md)  
[Opprette spesialbestillinger](sales-how-to-create-special-orders.md)|  
[Lager](inventory-manage-inventory.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]