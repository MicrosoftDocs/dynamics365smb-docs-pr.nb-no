---
title: Skriv ut en lagerplukkliste fra ordre
description: Du kan skrive ut en plukkliste for lager direkte fra en ordre, salg, faktura og andre utgående salgsdokumenter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 50c0a9836a45bac0dfd4a190040c908d28d5617f
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6436829"
---
# <a name="print-the-picking-list"></a>Skrive ut plukklisten

Du kan skrive ut en plukkliste for lager direkte fra en ordre og andre dokumenter som igangsetter leveringen av varer.

Denne rapporten brukes vanligvis i selskaper uten egen funksjonalitet for lagerstyring, slik at en lagerarbeider ganske enkelt kan vise eller skrive ut plukklisten fra det tilknyttede salgsdokumentet. I selskaper med høyere volum eller mer komplekse prosesser, planlegges plukking og utføres i egne lagerdokumenter. Hvis du vil ha mer informasjon, kan du se [Plukke varer](warehouse-pick-items.md).

## <a name="to-print-a-picking-list-from-a-sales-order"></a>Skrive ut en plukkliste fra en ordre

Følgende fremgangsmåte er basert på en ordre. Fremgangsmåten er de samme for alle andre dokumenter som kan brukes til å starte levering av varer, for eksempel en overføringsordre.

1. Velg ikonet ![Søk etter side eller rapport.](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.  
2. Åpne ordren du vil plukke varer for.  
3. Velg **Rapport**-handlingen, og velg deretter **Plukklisten etter ordre**-handlingen.  
4. Velg **Skriv ut** for å skrive ut plukklisten, eller velg **Forhåndsvisning** for å vise den på skjermen.

Du kan også lagre plukklisten som et dokument, for eksempel for å sende til noen, eller legge til som et vedlegg i ordren. Se [Behandle vedlegg, koblinger og merknader på kort og dokumenter](ui-how-add-link-to-record.md) hvis du vil ha mer informasjon.

> [!NOTE]
> Hvis du brukte **Utfold stykkliste**-funksjonen på ordren, vises bare komponentene for den tilknyttede monteringsvaren i rapporten. Hvis du vil ha mer informasjon, kan du se [Arbeide med stykklister](inventory-how-work-BOMs.md).

## <a name="see-also"></a>Se også

[Lager](inventory-manage-inventory.md)  
[Plukke varer](warehouse-pick-items.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]