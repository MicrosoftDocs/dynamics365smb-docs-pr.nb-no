---
title: Behandle produktvarianter
description: 'Lær hvordan du kan registrere produkter som er nesten identiske, men som er forskjellig fra farge, størrelse eller materiale som varevarianter.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'item, variant, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 09/26/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="manage-product-variants"></a>Behandle produktvarianter

Varevarianter er en fin måte å holde listen over produkter på under kontroll. Du har for eksempel har et stort antall varer som nesten er identiske og som bare varierer i farge. Du kan definere hver variant som en separat vare. Men du velger å definere én vare og angi de ulike fargene som varianter av varen.  

> [!TIP]
> Hvis du vil ha en praktisk innføring i å bruke varianter i produksjon, kan du se [Gjennomgang: Varianter](contoso-coffee/manufacturing/variants.md) for Contoso Coffee-demodata.  

## <a name="add-variants-to-an-item"></a>Legg til varianter i en vare

Hvis organisasjonen har bestemt deg for å bruke varianter, er det enkelt nok å definere varianter for en vare.  

### <a name="to-add-variants"></a>Slik legger du til varianter

1. Åpne [siden **Varelister**](https://businesscentral.dynamics.com/?page=31), åpne relevant vare.  
2. På siden **Varekort** velger du **Vare** og velger deretter **Varianter**.  
3. På siden **Varevarianter** viser du variantene.  

Når du deretter oppretter et salgsdokument og legger til varen, kan du angi varianten av varen i feltet **Variantkode**. Det samme gjelder kjøpsdokumenter.  

## <a name="item-availability-by-variant"></a>Disponibelt per variant

[!INCLUDE [inventory_variant-availability](includes/inventory_variant-availability.md)]

## <a name="require-use-of-variants"></a>Krev bruk av varianter

Fra og med lanseringsbølge 2 i 2022 kan administratorer kreve at brukere angir varianten i dokumenter og kladder for varer som har varianter. Når du skal aktivere funksjonen, går du til siden **Lageroppsett** og velger feltet **Variant obligatorisk hvis finnes**. Du kan overstyre denne globale innstillingen for bestemte varer.  

På varekort kan feltet **Variant obligatorisk hvis finnes** ha følgende alternativer:

|Feltverdi |Description|
|---------|----|
|Standard| Innstillingen fra **lageroppsett** gjelder denne varen.|
|Nei| Brukere må ikke angi en variant for denne varen.|
|Ja| Hvis varen har en eller flere varianter, må brukerne angi den relevante varianten. Hvis de ikke er det, blir de blokkert fra bokføring av transaksjonen.|

> [!NOTE]
> Disse innstillingene påvirker ikke elementer som ikke har varianter.

Hvis funksjonen er slått på, kan ikke brukerne bokføre en post hvis varianten ikke er angitt.

## <a name="categories-attributes-and-variants"></a>Kategorier, attributter og varianter

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a>Se også

[Registrere nye varer](inventory-how-register-new-items.md)  
[Definere generell informasjon om lagerbeholdning](inventory-how-setup-general.md)  
[Gjennomgang: varianter](contoso-coffee/manufacturing/variants.md)  
