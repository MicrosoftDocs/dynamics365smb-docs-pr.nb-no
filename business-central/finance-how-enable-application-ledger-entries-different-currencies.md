---
title: Utligne poster i ulike valutaer | Microsoft-dokumentasjon
description: Du kan utligne poster i flere valutaer, for eksempel hvis du selger i én valuta og mottar betaling i en annen.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c11939306e56299347a5f80d9ccfbc35c22fe5aa
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3917029"
---
# <a name="enable-application-of-ledger-entries-in-different-currencies"></a>Aktivere utligning av kundeposter i forskjellige valutaer
Hvis du handler fra en leverandør i én valuta og betaler i en annen valuta, kan du utligne utbetalingen mot kjøpet.

Hvis du selger til en kunde i én valuta og mottar betaling i en annen valuta, kan du også utligne betalingen mot salgsfakturaen.

Fremgangsmåten nedenfor beskriver hvordan du definerer dette for leverandørposter på siden **Kjøpsoppsett**. Oppsettet er det samme for kundeposter på siden **Salgsoppsett**.

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a>Aktivere utligning av leverandørposter i forskjellige valutaer
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kjøpsoppsett**, og velg deretter den relaterte koblingen.
2. I feltet **Utligning mellom valuta** velger du ett av følgende alternativer:

| Alternativ | Beskrivelse |
| --- | --- |
| Ingen |Utligning mellom valutaer er ikke tillatt. |
| ØMU |Utligning mellom ØMU-valutaer er tillatt. |
| Alle |Utligning mellom alle valutaer er tillatt. |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a>Slik konfigurerer du finanskonti for avrundingsdifferanser ved valutautligning  
Hvis du vil utligne poster i ulike valutaer, må du opprette finanskontoer som du vil bokføre avrundingsdifferanser på.  

> [!NOTE]  
>  Du må opprette finanskontoene før du fullfører oppgaven. Hvis du vil ha mer informasjon, kan du se [Forstå finans og kontoplanen](finance-general-ledger.md).

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokføringsgrupper - kunde**, og velg deretter den relaterte koblingen.  
2. Angi de relevante finanskontiene der avrundingsdifferanser skal bokføres, i feltene **Debetkonto for valutaavrund.** og **Kreditkonto for valutaavrund.**.  
3. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokføringsgrupper – leverandør**, og velg deretter den relaterte koblingen.  
4. Angi de relevante finanskontiene der avrundingsdifferanser skal bokføres, i feltene **Debetkonto for valutaavrund.** og **Kreditkonto for valutaavrund.**.  

## <a name="see-also"></a>Se også
[Administrere skyldige beløp](payables-manage-payables.md)  
[Håndtere fordringer](receivables-manage-receivables.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
