---
title: Opprette bankkonti| Microsoft-dokumentasjon
description: Opprette bankkonti
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 665c07a7242796718cfb01a1eb901d4df04ef8c9
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-bank-accounts"></a>Opprette bankkonti
Du bruker bankkonti i [!INCLUDE[d365fin](includes/d365fin_md.md)] til å holde orden på banktransaksjonene dine. Konti kan utstedes i norske kroner eller i fremmed valuta. Når du har opprettet bankkonti, kan du bruke mulighetene for utskriving av sjekker (gjelder ikke Norge).

## <a name="to-set-up-bank-accounts"></a>Slik setter du opp bankkonti
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Bankkonti**, og deretter velger du den beslektede koblingen.
2. I vinduet **Bankkonti** velger du handlingen **Ny**.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Opprette din bankkonto for import eller eksport av bankfilene
Felt i hurtigafnen **Overføring** i vinduet **Bankkontokort** er relatert til import og eksport av bankfeeder og filer. Hvis du vil ha mer informasjon, kan du se [Konfigurere konverteringstjenesten for bankdata](bank-how-setup-bank-data-conversion-service.md) og [Kofigurere Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Bankkonti**, og deretter velger du den beslektede koblingen.
2. Åpne kortet for en bankkonto som du vil eksportere eller importere bankfiler for.
3. Fyll ut feltene på hurtigfanen **Overføring** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**Merk**: Andre fileksporttjenester og formater krever ulike oppsettsverdier i vinduet **Bankkort**. Du blir informert om feil eller manglende oppsettsverdier når du prøver å eksportere filen. Les derfor de korte beskrivelsene av feltene nøye, eller se relaterte fremgangsmåteeemner. Hvis du for eksempel eksporterer en betalingsfil for Nord-Amerika elektronisk pengeoverføring (EFT) krever at både **Nr. for siste remitteringsmelding** og **Transittnr.** er fylt ut. Hvis du vil ha mer informasjon, kan du se [Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md).

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Opprette dine leverandørbankkonti for import eller eksport av bankfilene
Felt i hurtigafnen **Overføring** i vinduet **Leverandørs bankkort** er relatert til eksport av bankfeeder og filer. Hvis du vil ha mer informasjon, se [Konfigurere tjeneste for konvertering av bankdata](bank-how-setup-bank-data-conversion-service.md) og [Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md).

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Leverandører**, og deretter velger du den beslektede koblingen.
2. Åpne kortet for en leverandør med en bankkonto som du vil eksportere betalingsbankfiler til.
3. Velg **Bankkonti**-handlingen.
3. I vinduet **Leverandørs bankkort**, i hurtigfanen **Overføring**, fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Se også
[Konfigurere banktjenester](bank-setup-banking.md)  
[Håndtere bankkonti](bank-manage-bank-accounts.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

