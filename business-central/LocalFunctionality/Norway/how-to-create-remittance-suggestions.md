---
title: Opprette remitteringsforslag
description: Du kan opprette et remitteringsforslag slik at betalingsforslag sendes til leverandører som skal motta remitteringsoppdrag.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 36facd0f98a1b269615e57dd77a70c03a48af201
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2020
ms.locfileid: "3777904"
---
# <a name="create-remittance-suggestions"></a>Opprette remitteringsforslag
Du kan opprette et remitteringsforslag slik at betalingsforslag sendes til leverandører som skal motta remitteringsoppdrag. Én betalingstransaksjon per bokføringsdato overføres til banken for hver leverandør.  

> [!NOTE]  
>  Du kan unngå å opprette betalingsforslag for leverandører som remitteres når den ordinære leverandørforslagprosessen benyttes, ved å legge til et filter for **Remittering** på siden **Betalingsforslag - leverandør** og sette filteret til **Nei**.  

## <a name="to-create-a-remittance-suggestion"></a>Slik oppretter du et remitteringsforslag:  

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](../../media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Utbetalingskladder**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Remitteringsforslag**.  
3.  Fyll ut feltene som beskrevet i tabellen nedenfor, i hurtigfanen **Alternativer** på siden **Remitteringsforslag**.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**Siste betalingsdato**|Angi den siste betalingsdatoen.|  
    |**Søk etter kontantrabatter**|Velg dette alternativet hvis du vil søke etter poster med kontantrabatter.|  
    |**Bruk leverandørprioritet**|Velg dette alternativet hvis leverandørprioritet skal brukes til å søke i poster.|  
    |**Disponibelt beløp (NOK)**|Angi betalingene for totalsummer som er mindre enn eller lik det angitte beløpet.|  
    |**Bokføringsdato**|Angi en bokføringsdato.|  
    |**Erstatt bokføringsdato med forfallsdato**|Velg for å sette inn forfallsdatoen for posten som bokføringsdato for betalingene.|  
    |**Sjekk bilagstype**|Angi hvilke av følgende bilagstyper som skal sjekkes for betaling:<br /><br /> -   **Alle** - alle bilagstyper sjekkes.<br />-   **Faktura/kreditnota** - Bare faktura- eller kreditnotaposter sjekkes.|  
    |**Bare faktura-/debetposter**|Velg dette for å bare betale faktura- eller debetposter.|  

4.  Velg **OK**.  

## <a name="see-also"></a>Se også  
 [Elektroniske betalinger til leverandører i Norge](electronic-payments-to-vendors-in-norway.md)   
 [Sette opp remitteringsavtaler](how-to-set-up-remittance-agreements.md)   
 [Opprette remitteringskontoer](how-to-create-remittance-accounts.md)   
 [Angi leverandører for remittering](how-to-set-up-vendors-for-remittance.md)   
 [Mottakerreferansekoder](recipient-reference-codes.md)   
 [Opprette manuelle remitteringsoppdrag](how-to-create-manual-remittance-payments.md)   
 [Definere betalingslinjeinformasjon](how-to-set-up-payment-line-information.md)   
 [Kontrollere remitteringsoppdrag](how-to-test-remittance-payments.md)   
 [Eksportere remitteringsoppdrag](how-to-export-remittance-payments.md)   
 [Typer betalingsreturfiler](types-of-payment-returns-files.md)   
 [Importere betalingsreturdata](how-to-import-payment-return-data.md)   
 [Slette remitteringsoppdrag](how-to-delete-remittance-payment-orders.md)   
 [Remitteringsfeil](remittance-errors.md)   
 [Vise remitteringsfeilkoder](how-to-view-remittance-error-codes.md)   
 [Annullere betalinger](how-to-cancel-payments.md)
