---
title: Registrere nye varer| Microsoft-dokumentasjon
description: Opprett kort for nye fysiske produkter som selges fra beholdningen i for eksempel stykker, eller for tjenester som selges i timer.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item, finished good, component, raw material, assembly item
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 582e006291e51e19d80304d24ae055ce6ac8d698
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-register-new-items"></a>Registrere nye varer
Varer, blant andre produkter, er grunnlaget for virksomheten din, varer eller tjenester som du handler med. Hver vare må være registrert som et varekort.

Varekort inneholder informasjonen som er nødvendig for å kjøpe, lagre, selge, levere og gjøre rede for varer.

Varekortet kan være av typen **Beholdning** eller **Tjeneste** for å angi om varen er en fysisk enhet eller arbeidstidsenhet. Bortsett fra noen av feltene som er relatert til de fysiske aspektene av en vare, fungerer alle felt på et varekort på samme måte for lagervarer og tjenester. Hvis du vil ha mer informasjon om hvordan du selger en vare, kan du se [Selge produkter](sales-how-sell-products.md) eller [Fakturere salg](sales-how-invoice-sales.md).

En vare kan struktureres som en overordnet vare med underliggende underordnede varer i en stykkliste. I [!INCLUDE[d365fin](includes/d365fin_md.md)]er en stykkliste referert til som en monteringsstykkliste. Du kan bruke monteringsstykklister til å strukturere overordnede varer som selges som sett som består av komponenter for den overordnede varen, eller som du monterer til bestilling eller lager. Hvis du vil ha mer informasjon, kan du se [Arbeide med stykklister](inventory-how-work-BOMs.md).

**Merk**: Hvis det finnes varemaler for ulike varetyper, vises et vindu når du oppretter et nytt kundekort der du kan velge en passende mal. Hvis det bare finnes én varemal, brukes alltid denne malen i nye varekort.

## <a name="to-create-a-new-item-card"></a>Opprette et nytt varekort
1. På Hjem-siden velger du handlingen **Varer** for å åpne listen over eksisterende varer.  
2. I vinduet **Varer** velger du handlingen **Ny**.

    Hvis det bare finnes én varemal, åpnes et nytt varekort med noen felt som er fylt ut med informasjon fra malen.
3. I vinduet **Velg en mal for en ny vare** velger du malen som du vil bruke for det nye varekortet.
4. Velg **OK**-knappen. Det åpnes et nytt varekort med noen felt som er fylt ut med informasjon fra malen.
5. Fortsette med å fylle ut eller endre feltet på varekortet etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

I hurtigfanen **Pris og bokføring** kan du vise spesialpriser eller rabatter som skal gis for varen hvis bestemte kriterier oppfylles, for eksempel kunde, minimumsordreantall eller sluttdato. Hver rad representerer en spesialpris eller linjerabatt. Hver kolonne representerer et vilkår som må brukes for å garantere spesialprisen du angir i feltet **Enhetspris**, eller linjerabatten du angir i feltet **Linjerabatt-%**. Hvis du vil ha mer informasjon, kan du se [Registrere avtaler om salgspris, rabatt og betaling](sales-how-record-sales-price-discount-payment-agreements.md).

Varen er nå registrert, og varekortet er klart til å brukes på kjøps- og salgsdokumenter.

Hvis du vil bruke dette varekortet som en mal når du oppretter nye varekort, kan du lagre det som en mal. Hvis du vil ha mer informasjon, kan du se følgende avsnitt:

## <a name="to-save-the-item-card-as-a-template"></a>Lagre varekortet som en mal
1. I vinduet **Varekort** velger du handlingen **Lagre som mal**. **Varemal**  -vinduet åpnes og viser varekortet som en mal.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Hvis du vil bruke dimensjoner i maler, velger du handlingen **Dimensjoner**. **Dimensjonsmaler**-vinduet åpnes med alle dimensjonskoder som er definert for varen.
4. Rediger eller angi dimensjonskoder som skal gjelde for nye varekort som opprettes ved hjelp av malen.
5. Når du har fullført den nye varemalen, kan du velge **OK**-knappen.

Varemalen legges til i listen over varemaler, slik at du kan bruke den til å opprette nye varekort.

## <a name="see-also"></a>Se også
  [Lager](inventory-manage-inventory.md)  
  [Innkjøp](purchasing-manage-purchasing.md)  
  [Salg](sales-manage-sales.md)  
  [Arbeide med [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
