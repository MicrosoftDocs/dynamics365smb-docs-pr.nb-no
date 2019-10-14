---
title: Definere betalingslinjeinformasjon
description: Utbetalingskladdelinjeinformasjon for remitteringsoppdraget angis på siden Betalingsinformasjon.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 83bb1fe0c5f152e6d711edd7b7121c38beeb6251
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2301224"
---
# <a name="set-up-payment-line-information"></a>Definere betalingslinjeinformasjon
Utbetalingskladdelinjeinformasjon for remitteringsoppdraget angis på siden **Betalingsinformasjon**.  

## <a name="to-set-up-payment-line-information"></a>Definere betalingslinjeinformasjon  

1.  Velg ikonet ![Søk etter side eller rapport](../../media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Betalingskladder**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Betalingsinformasjon**.  
3.  Fyll ut feltene som beskrevet i tabellen nedenfor, i hurtigfanen **Generelt** på siden **Betalingsinformasjon**.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**Remitteringskontokode**|Velg remitteringskontokoden.|  
    |**Remitteringsavtalekode**|Angi avtalekoden som er knyttet til kontokoden.|  
    |**Remitteringstype**|Angi remitteringstypen som er tilordnet til kontokoden. Remitteringstyper omfatter **Innland** og **Utland**.|  

4.  I hurtigfanen **Innland** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**Mottakerref. 1 - 3**|Angi betalingsteksten som sendes til leverandøren.|  
    |**KID (kundens ID-nummer)**|Angi nummeret som sendes til leverandøren når betalingen skal utføres.|  
    |**Vårt kontonr.**|Angi kontonummeret til ditt firma.|  
    |**Eksterndokumentnr.**|Angi nummeret på det eksterne dokumentet.|  
    |**Betalingsartkode innland**|Angi betalingstypekoden som er tilordnet til betalingen.|  

    > [!NOTE]  
    >  Mottakerreferansen og KID-nummeret kan ikke angis for den samme betalingen. Hvis KID benyttes, er dette den eneste informasjonen som leverandøren mottar.  

5.  I hurtigfanen **Utland** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**Mottakerref. utland**|Angi betalingsteksten som sendes til leverandøren.|  
    |**Betalingsartkode utland**|Angi betalingstypekoden som er tilordnet til betalingen.|  
    |**Sjekk**|Angi om det skal utstedes en sjekk.<br /><br /> * <br />                        **Nei** - ingen sjekk utstedes.<br /><br /> * **Sendes oppdragsgiver** - sjekken utstedes og sendes til oppdragsgiver.<br /><br /> * **Sendes betalingsmottaker** - sjekken utstedes og sendes til betalingsmottaker.|  
    |**Haster**|Velg om betalingen haster og må behandles som en hasteoverføring.|  
    |**Avtalt kurs**|Angi valutakursen som avtales med banken.|  
    |**Avtalt med**|Angi hvem avtalen er inngått med, hvis det er avtalt en valutakurs.|  
    |**Terminskontraktnr.**|Angi terminskontraktnummeret som brukes for denne betalingen.|  
    |**Terminskontraktkurs**|Angi terminskontraktkursen som brukes for denne betalingen.|  

6.  Velg **OK**.  

## <a name="see-also"></a>Se også  
 [Elektroniske betalinger til leverandører i Norge](electronic-payments-to-vendors-in-norway.md)   
 [Sette opp remitteringsavtaler](how-to-set-up-remittance-agreements.md)   
 [Opprette remitteringskontoer](how-to-create-remittance-accounts.md)   
 [Angi leverandører for remittering](how-to-set-up-vendors-for-remittance.md)   
 [Mottakerreferansekoder](recipient-reference-codes.md)   
 [Opprette remitteringsforslag](how-to-create-remittance-suggestions.md)   
 [Opprette manuelle remitteringsoppdrag](how-to-create-manual-remittance-payments.md)   
 [Kontrollere remitteringsoppdrag](how-to-test-remittance-payments.md)   
 [Eksportere remitteringsoppdrag](how-to-export-remittance-payments.md)   
 [Typer betalingsreturfiler](types-of-payment-returns-files.md)   
 [Importere betalingsreturdata](how-to-import-payment-return-data.md)   
 [Slette remitteringsoppdrag](how-to-delete-remittance-payment-orders.md)   
 [Remitteringsfeil](remittance-errors.md)   
 [Vise remitteringsfeilkoder](how-to-view-remittance-error-codes.md)   
 [Annullere betalinger](how-to-cancel-payments.md)
