---
title: Knytte en ordre til en bestilling for direkte levering | Microsoft-dokumentasjon
description: Beskriver hvordan du oppretter en ordre som er koblet til en bestilling, for å sikre levering direkte fra leverandøren til kunden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c5ca9eb1dc14a75d84072f28e7f72fc8b5e89373
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443410"
---
# <a name="make-drop-shipments"></a>Foreta direkte leveringer

En direkte levering er levering av varer fra en av leverandørene dine, direkte til en av kundene dine.

Når en ordre er merket for direkte levering, og du oppretter en bestilling for kunden i **Forsendelsesadresse**-feltet, **Kundeadresse**, kan du koble de to dokumentene og instruere leverandøren til å levere direkte til kunden.
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## <a name="to-create-a-sales-order-for-drop-shipment"></a>Slik oppretter du en ordre med direkte levering:

Hvis du vil klargjøre en direkte levering, kan du opprette en ordre og vise på salgslinjen at salget krever direkte levering.

1. Opprett en ordre for en vare. Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).
2. På ordrelinjen for direkte levering, merker du av for **Direkte levering**. Bruk funksjonen **Velg kolonner** hvis feltet ikke er synlig. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).

## <a name="to-create-the-purchase-order-for-drop-shipment"></a>Slik oppretter du bestillingen med direkte levering:

For å klargjøre en direkte levering angir du på bestilling at den må leveres til kunden, ikke til deg selv.

1. Opprett en bestilling. Ikke fyll ut noen felt på linjene. Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).
2. I **Forsendelsesadresse**-feltet velger du **Kundeadresse**.
3. I **Kunde**-feltet velger du kunden som du selger til.
4. Velg **Direkte levering**-handlingen, og velg deretter **Hent ordre**-handlingen.
5. På siden **Salgsliste** merker du ordren som du har forberedt i [Slik oppretter du en ordre med direkte levering](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).
6. Velg **OK**.

Linjeinformasjonen fra ordren settes inn på bestillingslinjene.

Nå kan du angi at leverandøren skal levere varene til kunden, for eksempel, ved å sende bestillingen på e-post som en PDF-fil.     

## <a name="to-create-multiple-purchase-orders-for-drop-shipments"></a>Slik oppretter du flere bestillinger med direkte leveringer

Du kan også bruke bestillingsforslaget til å opprette bestillingen for leverandøren. Fordelen med å bruke bestillingsforslaget er at det kan opprette bestillinger for alle utestående direkte leveringer, slik at du ikke trenger å opprette hver enkelt individuelt.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Bestillingsforslag**, og velg deretter den relaterte koblingen.
2. Velg **Direkte levering**-handlingen, og velg deretter **Hent ordre**-handlingen.
3. Velg **OK**-knappen.
4. Se gjennom bestillingslinjene, og velg leverandør som leverer nødvendige varer, i feltet **Leverandørnummer**. 
5. Velg handlingen **Utfør handlingsmelding** for å konvertere korrekturleste linjer til en bestilling.

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a>Slik viser du den tilknyttede bestillingen fra ordren:

* Velg ordrelinjen med direkte levering, velg **Ordre**-handlingen, velg **Direkte levering**-handlingen, og velg deretter **Bestilling**-handlingen.

## <a name="to-post-a-drop-shipment"></a>Bokføre en direkte levering

Når leverandøren har levert varene, kan du bokføre ordren som levert. Du kan også bokføre bestillingen, men bare med **Motta**-alternativet til ordren er fakturert.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.
2. Åpne ordren du opprettet i [Slik oppretter du en ordre med direkte levering:](#to-create-a-sales-order-for-drop-shipment).
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
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]