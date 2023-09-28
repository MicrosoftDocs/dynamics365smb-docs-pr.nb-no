---
title: Opprett og administrer katalogvarer
description: Lær hvordan du selger varer som du ikke beholder i listen over varer.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 03/08/2023
ms.custom: bap-template
ms.search.keywords: non-inventoriable
ms.search.forms: '5725, 5726, 5732'
---

# <a name="work-with-catalog-items"></a>Arbeide med katalogvarer

Katalogvarer er varer som du ikke administrerer i [!INCLUDE[prod_short](includes/prod_short.md)] før du selger dem. Når du bruker handlingen **Velg katalogvare** til å legge til en katalogvare på en linje i en ordre, et tilbud eller en rammeordre, konverteres katalogvaren til en vanlig vare.

> [!NOTE]  
> Du kan ikke velge en katalogvare fra **Salgsfaktura**-siden.

En katalogvare har vanligvis varenummeret til leverandøren som leverer den. Før du kan konvertere en katalogvare til en normal vare, må du angi hvordan du vil konvertere leverandørvarenumre til varenummereringen. Hvis du vil ha mer om varenummerering, kan du gå til [Definer hvordan katalogvarenumre konverteres til din egen nummerering](#specify-how-catalog-item-numbers-are-converted-to-your-own-numbering).  

> [!IMPORTANT]
> Katalogvarer må ikke forveksles med ikke-lagervarer, som er vanlige varer som blir gitt typen **Ikke-lagervare** for å utelukke dem fra tilgjengelighet og kostberegninger, for eksempel fordi de bare brukes internt og har en lav kostnad. Hvis du vil lære mer om varer som ikke er lager, går du til [Om varetyper](inventory-about-item-types.md).

## <a name="create-a-catalog-item"></a>Opprett en katalogvare

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Katalogvarer**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="specify-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a>Definer hvordan katalogvarenumre konverteres til din egen nummerering

Før du kan konvertere en katalogvare til en vanlig vare, må du angi hvordan du vil konvertere leverandørvarenumre til strukturen du bruker for varenumre.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Oppsett av katalogvare**, og velg deretter den relaterte koblingen.
2. Velg alternativet du foretrekker, i feltet **Nummerformat**.

## <a name="convert-a-catalog-item-to-a-normal-item"></a>Konverter en katalogvare til en vanlig vare

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Katalogvarer**, og velg deretter den relaterte koblingen.
2. Åpne kortet for katalogvaren som du vil konvertere til en vanlig vare.
3. På siden **Katalogvarekort** velger du handlingen **Opprett vare**.

Et nytt varekort forhåndsutfylt med informasjon fra katalogvaren og en varemal opprettes. Du kan redigere opplysningene om den nye varen om nødvendig. Hvis du vil finne ut mer om oppretting av varer, går du til [Registrer nye varer](inventory-how-register-new-items.md).

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a>Slik selger du en katalogvare og konverterer den til en vanlig vare

Følgende fremgangsmåte bruker en ordre, men trinnene er de samme for rammeordrer og tilbud.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**. Fyll ut feltene på hurtigfanen **Generelt** som for ordrer. Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).
3. På en ny salgslinje, i **Type**-feltet velger du **Vare**, men lar feltet **Nr.** stå tomt.
4. Velg handlingen **Linje** og velg deretter handlingen **Velg katalogvarer**.
5. På siden **Katalogvarer** velger du katalogvaren du vil selge, og velger deretter **OK**-knappen.
6. Når ordren er fullført, kan du velge handlingen **Bokfør**.

> [!NOTE]  
> En varereferanse er automatisk vare mellom leverandørens varenummer og det nye varenummeret ditt. Hvis du vil lære mer om varereferanser, går du til [Bruk varereferanser](inventory-how-use-item-cross-refs.md).

## <a name="see-also"></a>Se også

[Registrer nye varer](inventory-how-register-new-items.md)  
[Opprett spesialbestillinger](sales-how-to-create-special-orders.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
