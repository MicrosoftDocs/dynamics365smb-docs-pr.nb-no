---
title: "Registrere spesielle kjøpspriser og rabatter| Microsoft-dokumentasjon"
description: "Registrere kjøpspriser og rabatter"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 67625231d62a72bb0a62ab362bce92aa16b8956e
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-record-special-purchase-prices-and-discounts"></a>Registrere spesielle kjøpspriser og rabatter
De forskjellige pris- og rabattavtaler som gjelder når du kjøper fra forskjellige leverandører, må defineres slik at avtalte regler og verdier brukes på kjøpsdokumenter du oppretter for leverandørene.

Når du har registrert spesielle priser og linjerabatter for salg og innkjøp, sikrer [!INCLUDE[d365fin](includes/d365fin_md.md)] at din fortjeneste på varehandel alltid er optimal ved automatisk å beregne den beste prisen på salgs- og kjøpsdokumenter og på jobb- og varejournallinjer. Du finner mer informasjon under [Avansert: Beregning av beste pris](advanced-best-price-calculation.md).

Når det gjelder priser, kan du sette inn en spesialkjøpspris på bestillingslinjer hvis en bestemt kombinasjon av leverandør, vare, minste antall, enhet, eller start-/sluttdato finnes.

Når det gjelder rabatter, kan du opprette og bruke to typer kjøpsrabatter:

| Rabattype | Beskrivelse |
| --- | --- |
| **Bestillingslinjerabatt** |Et rabattbeløp som settes inn på bestillingslinjer hvis en bestemt kombinasjon av leverandør, vare, minste antall, enhet, eller start-/sluttdato finnes. Dette fungerer på samme måte som for innkjøpspriser. |
| **Fakturarabatt** |En prosentrabatt som trekkes fra dokumenttotalen hvis beløpet for alle linjer på et kjøpsdokument overskrider et bestemt minimumsbeløp. |

Ettersom bestillingslinjerabatter og kjøpspriser er basert på en kombinasjon av vare og leverandør, kan du også angi denne konfigurasjonen fra varekortet, der regler og verdier er definert. Hvis du vil ha mer informasjon, kan du se [Registrere nye varer](inventory-how-register-new-items.md).

## <a name="to-set-up-a-special-purchase-price-for-a-vendor"></a>Definere en spesialkjøpspris for en leverandør
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Leverandører**, og deretter velger du den beslektede koblingen.
2. Åpne det aktuelle leverandørkortet, og velg deretter handlingen **Priser**.

    **Kjøpstype**-feltet er forhåndsutfylt med **Leverandør**, og **Kjøpskode**-feltet er forhåndsutfylt med leverandørnummeret.
3. Fyll ut feltene på linjen etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Fylle ut en linje for hver kombinasjon som leverandøren gir deg en bestillingslinjerabatt for.

## <a name="to-set-up-a-line-discount-for-a-vendor"></a>Definere en linjerabatt for en leverandør
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Leverandører**, og deretter velger du den beslektede koblingen.
2. Åpne det aktuelle leverandørkortet, og velg deretter handlingen **Linjerabatter**.

    **Kjøpstype**-feltet er forhåndsutfylt med **Leverandør**, og **Kjøpskode**-feltet er forhåndsutfylt med leverandørnummeret.
3. Fyll ut feltene på linjen etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Fylle ut en linje for hver kombinasjon som leverandøren gir deg en bestillingslinjerabatt for.

## <a name="to-set-up-an-invoice-discount-for-a-vendor"></a>Definere en fakturarabatt for en leverandør
Når leverandøren har informert deg om hvilke linjerabatter som gis, angir du fakturarabattkoden på leverandørkortet og definerer betingelsene for hver kode.

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Leverandører**, og deretter velger du den beslektede koblingen.
2. Åpne leverandørkortet for leverandøren som skal ha fakturarabatter.
3. I feltet **Fakturarabattkode** velger du en kode for de aktuelle fakturarabattbetingelsene som skal brukes til å beregne fakturarabatter for leverandøren.

    **Merk**: Fakturarabattkoder representeres av eksisterende leverandørkort. Dette lar deg raskt tilordne fakturarabattbetingelsene til leverandører ved å velge navnet på en annen leverandører som har de samme betingelsene.

    Fortsett å definere nye betingelser for kjøpsfakturarabatt.
4. I vinduet **Leverandørkortet** velger du handlingen **Fakturarabatter**. Vinduet **Levrd./fakt.-rabatter** åpnes.
5. I feltet **Valutakode** angir du koden til en valuta som fakturarabattbetingelsene på linjen gjelder for. La feltet stå tomt for å definere betingelser for fakturarabatt i USD.
6. I **Minimumsbeløp**-feltet angir du hva som er minstebeløpet for at det skal gis rabatt i en faktura.
7. I **Rabatt-%**-feltet angir du fakturarabatten prosentvis av fakturabeløpet.
8. Gjenta trinn 5 til 7 for hver valuta som leverandøren vil motta en forskjellig fakturarabatt for.

Fakturarabatten er nå definert og tilordnet til den aktuelle leverandøren. Når du velger leverandørkoden i **Fakturarabattkode**-feltet på andre leverandørkort, tilordnes den samme fakturarabatten til leverandøren.

## <a name="see-also"></a>Se også
[Avansert: Beregning av beste pris](advanced-best-price-calculation.md)  
[Definere kjøp](purchasing-setup-purchasing.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

