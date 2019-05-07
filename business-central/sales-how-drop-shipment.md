---
title: Knytte en ordre til en bestilling for direkte levering | Microsoft-dokumentasjon
description: Beskriver hvordan du oppretter en ordre som er koblet til en bestilling, for å sikre levering direkte fra leverandøren til kunden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7a87023445ea10aa19cc0cc4f60d76ce4cf3e365
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "929362"
---
# <a name="make-drop-shipments"></a>Foreta direkte leveringer
En direkte levering er levering av varer fra en av leverandørene dine, direkte til en av kundene dine.

Når en ordre merkes for direkte levering, og du oppretter en bestilling som angir kunden i **Salg til kundenr.**-feltet, kan du koble de to dokumentene og dermed be leverandøren levere direkte til kunden.

## <a name="to-create-a-sales-order-for-drop-shipment"></a>Slik oppretter du en ordre med direkte levering:
Hvis du vil klargjøre en direkte levering, kan du opprette en ordre for en vare som vanlig, bortsett fra at du må vise på salgslinjen at salget krever direkte levering.

1. Opprett en ordre for en vare. Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).
2. På ordrelinjen for direkte levering, merker du av for **Direkte levering**. Bruk funksjonen **Velg kolonner** hvis feltet ikke er synlig. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet ](ui-personalization-user.md).

## <a name="to-create-the-purchase-order-for-drop-shipment"></a>Slik oppretter du bestillingen med direkte levering:
Hvis du vil klargjøre en direkte levering for varen som skal selges, oppretter du en bestilling som vanlig, bortsett fra at du må angi på bestillingen at den må leveres til kunden, ikke til deg selv.

1. Opprett en bestilling. Ikke fyll ut noen felt på linjene. Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).
2. I feltet **Salg til-kundenr.** velger du kunden som du selger til.
3. Velg **Direkte levering**-handlingen, og velg deretter **Hent ordre**-handlingen.
4. På siden **Salgsliste** merker du ordren som du har forberedt i [Slik oppretter du en ordre med direkte levering](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).
5. Velg **OK**.

Linjeinformasjonen fra ordren settes inn på bestillingslinjene.

Nå kan du angi at leverandøren skal levere varene til kunden, for eksempel, ved å sende bestillingen på e-post som en PDF-fil.     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a>Slik viser du den tilknyttede bestillingen fra ordren:
* Velg ordrelinjen med direkte levering, velg **Ordre**-handlingen, velg **Direkte levering**-handlingen, og velg deretter **Bestilling**-handlingen.

## <a name="to-post-a-drop-shipment"></a>Bokføre en direkte levering
Når leverandøren har levert varene, kan du bokføre ordren som levert. Du kan også bokføre bestillingen, men bare med **Motta**-alternativet til ordren er fakturert.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Ordrer**, og velg deretter den relaterte koblingen.
2. Åpne ordren som du laget i [Slik oppretter du en ordre med direkte levering]().
3. I **Levere (antall)**-feltet angir du hvor mye av ordreantallet som skal leveres, hele eller deler av ordreantallet.
4. Velg handlingen **Bokfør** eller **Bokfør og send**.
5. Velg **Levere** hvis du vil fakturere senere, eller **Levere og fakturere** hvis du vil fakturere med en gang.

## <a name="see-also"></a>Se også
[Opprette spesialbestillinger](sales-how-to-create-special-orders.md)  
[Kjøpe varer for salg](purchasing-how-purchase-products-sale.md)  
[Selge produkter](sales-how-sell-products.md)  
[Registrere kjøp](purchasing-how-record-purchases.md)  
[Salg](sales-manage-sales.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
