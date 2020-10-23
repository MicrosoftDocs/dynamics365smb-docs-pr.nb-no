---
title: Skrive ut en lagerplukkliste fra en ordre
description: Du kan skrive ut en plukkliste for lager direkte fra en ordre, salg, faktura og andre utgående salgsdokumenter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c89cb40559a570605401108d7560f6b989e06773
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3926150"
---
# <a name="print-the-picking-list"></a>Skrive ut plukklisten
Du kan skrive ut en plukkliste for lager direkte fra en ordre, salgsfaktura eller andre dokumenter som igangsetter levering av varer.

Denne rapporten brukes vanligvis i selskaper uten egen funksjonalitet for lagerstyring, slik at en lagerarbeider ganske enkelt kan vise eller skrive ut plukklisten fra det tilknyttede salgsdokumentet. I selskaper med høyere volum eller mer komplekse prosesser, planlegges plukking og utføres i egne lagerdokumenter. Hvis du vil ha mer informasjon, kan du se [Plukke varer](warehouse-pick-items.md).

## <a name="to-print-a-picking-list-from-a-sales-order"></a>Skrive ut en plukkliste fra en ordre  
Følgende fremgangsmåte er basert på en ordre. Fremgangsmåten er de samme for alle salgsdokumenter som kan brukes til å starte levering av varer.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Ordrer**, og velg deretter den relaterte koblingen.  
2. Åpne ordren du vil plukke varer for.  
3. Velg **Rapport**-handlingen, og velg deretter **Plukklisten etter ordre**-handlingen.  
4. Velg **Skriv ut** for å skrive ut plukklisten, eller velg **Forhåndsvisning** for å vise den på skjermen.

Du kan også lagre plukklisten som et dokument, for eksempel for å sende til noen, eller legge til som et vedlegg i ordren. Se [Behandle vedlegg, koblinger og merknader på kort og dokumenter](ui-how-add-link-to-record.md) hvis du vil ha mer informasjon.

> [!NOTE]
> Hvis du brukte **Utfold stykkliste**-funksjonen på ordren, vises bare komponentene for den tilknyttede monteringsvaren i rapporten. Hvis du vil ha mer informasjon, kan du se [Arbeide med stykklister](inventory-how-work-BOMs.md).

## <a name="see-also"></a>Se også  
[Lager](inventory-manage-inventory.md)  
[Plukke varer](warehouse-pick-items.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)   
