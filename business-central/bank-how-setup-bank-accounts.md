---
title: Opprette bankkonti | Microsoft-dokumentasjon
description: Du kan avstemme bankkonti med kontoutdrag fra banken.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 07274a495ba7047fafaf31a94225ac29b05aabb4
ms.sourcegitcommit: c6e28db8f78fa21db064c9b8a8d742f49d7db3ae
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/31/2019
ms.locfileid: "2692779"
---
# <a name="set-up-bank-accounts"></a>Opprette bankkonti
Du bruker bankkonti i [!INCLUDE[d365fin](includes/d365fin_md.md)] til å holde orden på banktransaksjonene dine. Konti kan utstedes i norske kroner eller i fremmed valuta. Når du har opprettet bankkonti, kan du bruke mulighetene for utskriving av sjekker (gjelder ikke Norge).<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE3Vhpl]

## <a name="to-set-up-bank-accounts"></a>Slik setter du opp bankkonti
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bankkonti**, og velg deretter den relaterte koblingen.
2. På siden **Bankkonti** velger du handlingen **Ny**.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> For å kunne fylle ut **Saldo**-feltet med en inngående balanse, må du bokføre en bankkontopost med det aktuelle beløpet. Du kan gjøre dette ved å utføre en bankkontoavstemming. Hvis du vil ha mer informasjon, kan du se [Avstemme bankkonti separat](bank-how-reconcile-bank-accounts-separately.md). Du kan eventuelt også implementere den inngående balansen som en del av en generell dataoppretting i nye selskaper ved hjelp av den assisterte oppsettveiledningen **Overfør forretningsdata**. Hvis du vil ha mer informasjon, kan du se [Komme i gang](product-get-started.md).

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Opprette din bankkonto for import eller eksport av bankfilene
Felt i hurtigfanen **Overføring** på siden **Bankkontokort** er relatert til import og eksport av bankfeeder og filer. Hvis du vil ha mer informasjon, se [Bruke utvidelsen AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md) og [Konfigurere Envestnet Yodlee Bank Feeds-tjenesten](bank-how-setup-bank-statement-service.md).

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bankkonti**, og velg deretter den relaterte koblingen.
2. Åpne kortet for en bankkonto som du vil eksportere eller importere bankfiler for.
3. Fyll ut feltene på hurtigfanen **Overføring** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Andre fileksporttjenester og formater krever ulike oppsettsverdier på siden **Bankkort**. Du blir informert om feil eller manglende oppsettsverdier når du prøver å eksportere filen. Les derfor de korte beskrivelsene av feltene nøye, eller se relaterte fremgangsmåteeemner. Hvis du for eksempel eksporterer en betalingsfil for Nord-Amerika elektronisk pengeoverføring (EFT) krever at både feltet **Nr. for siste remitteringsmelding** og feltet **Transittnr.** er fylt ut. Hvis du vil ha mer informasjon, kan du se [Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md).

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Opprette dine leverandørbankkonti for import eller eksport av bankfilene
Felt i hurtigfanen **Overføring** på siden **Leverandørs bankkort** er relatert til eksport av bankfeeder og filer. Hvis du vil ha mer informasjon, se [Bruke utvidelsen AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md) og [Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md).

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Leverandører**, og velg deretter den relaterte koblingen.
2. Åpne kortet for en leverandør med en bankkonto som du vil eksportere betalingsbankfiler til.
3. Velg **Bankkonti**-handlingen.
3. På siden **Leverandørs bankkort**, i hurtigfanen **Overføring**, fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Se også
[Konfigurere banktjenester](bank-setup-banking.md)  
[Definere bokføringsgrupper](finance-posting-groups.md)  
[Håndtere bankkonti](bank-manage-bank-accounts.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
