---
title: Remitteringsfeil
description: Remitteringsfeil for betalinger kan oppstå ved overføring av data og etter at betalingene er sendt til banken. Begge typer feil rapporteres på siden Returfeil.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 113aa93d2984147df2f0b19da29e95adc27eda38
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181007"
---
# <a name="remittance-errors"></a>Remitteringsfeil
Remitteringsfeil for betalinger kan oppstå ved overføring av data og etter at betalingene er sendt til banken. Begge typer feil rapporteres på siden **Returfeil**.  

Remitteringssystemet håndterer alle feilkoder som kan sendes via returfiler. Det er ikke nødvendig å utføre manuelle annulleringer av betalinger som er avvist av banken.  

## <a name="types-of-errors"></a>Feiltyper  
Det finnes to typer remitteringsfeil:  

- Overføringsfeil  
- Avvisning  

## <a name="transfer-errors"></a>Overføringsfeil  
Hvis det oppstår feil under overføring, og det ikke opprettes returdata, har ikke banken mottatt betalingene.  

Hvis betalingsfilen ikke kan sendes til banken, må du annullere oppdraget i remitteringssystemet.  

## <a name="rejections"></a>Avslag  
Hvis det oppstår en feil eller mangler informasjon i forbindelse med en betaling som ble sendt til banken, inneholder returen en avvisning av betalingen.  

> [!NOTE]  
>  Avvisninger kan variere fra bank til bank. Kontakt banken din for å få informasjon om hvordan du skal håndtere avvisning av betalinger.  

Hvis betalingen avvises, vises feilkoden fra banken samt en forklaring for betalingen på siden **Ventekladd**. Du må håndtere avvisningen, avhengig av hvordan remitteringsavtalen er satt opp. Se [Sette opp remitteringsavtaler](how-to-set-up-remittance-agreements.md) for mer informasjon.  

## <a name="see-also"></a>Se også  
 [Elektroniske betalinger til leverandører i Norge](electronic-payments-to-vendors-in-norway.md)   
 [Sette opp remitteringsavtaler](how-to-set-up-remittance-agreements.md)   
 [Opprette remitteringskontoer](how-to-create-remittance-accounts.md)   
 [Angi leverandører for remittering](how-to-set-up-vendors-for-remittance.md)   
 [Mottakerreferansekoder](recipient-reference-codes.md)   
 [Opprette remitteringsforslag](how-to-create-remittance-suggestions.md)   
 [Opprette manuelle remitteringsoppdrag](how-to-create-manual-remittance-payments.md)   
 [Definere betalingslinjeinformasjon](how-to-set-up-payment-line-information.md)   
 [Kontrollere remitteringsoppdrag](how-to-test-remittance-payments.md)   
 [Eksportere remitteringsoppdrag](how-to-export-remittance-payments.md)   
 [Typer betalingsreturfiler](types-of-payment-returns-files.md)   
 [Importere betalingsreturdata](how-to-import-payment-return-data.md)   
 [Slette remitteringsoppdrag](how-to-delete-remittance-payment-orders.md)   
 [Vise remitteringsfeilkoder](how-to-view-remittance-error-codes.md)   
 [Annullere betalinger](how-to-cancel-payments.md)
