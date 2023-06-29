---
title: 'Typer betalingsreturfiler [NO]'
description: Forbedringer i den norske versjonen omfatter to typer betalingsreturfiler som kan importeres i Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '15000000, 15000002, 15000004, 15000006, 15000007, 15000010'
ms.date: 06/21/2021
ms.author: edupont
---
# <a name="types-of-payment-returns-files-in-the-norwegian-version"></a><a name="types-of-payment-returns-files-in-the-norwegian-version"></a>Typer betalingsreturfiler i den norske versjonen
[!INCLUDE[prod_short](../../includes/prod_short.md)]omfatter to typer importerbare betalingsreturfiler:  

- Mottaksreturer  
- Avregningsreturer  

Du kan også velge å ikke bruke returfiler ved å velge feltet **Returfiler brukes ikke** i **remitteringsavtalen**-tabellen. Se [Sette opp remitteringsavtaler](how-to-set-up-remittance-agreements.md) for mer informasjon.  

## <a name="receipt-returns"></a><a name="receipt-returns"></a>Mottaksreturer
Mottaksreturen mottas fra banken etter at du har sendt remitteringsfilen til banken. Når data leses inn, vises informasjon om hvor mange fakturaer som blir korrekt mottatt og hvor mange som mottas med feilmelding. Når du har importert en mottaksretur, blir statusen for betalingene i vinduet **Ventekladd** satt til **Godkjent**.  

> [!NOTE]  
>  Du kan også motta en avvist retur fra banken. Hvis remitteringen avvises, mottar du ingen avregningsretur.  

## <a name="settlement-returns"></a><a name="settlement-returns"></a>Avregningsreturer
Avregningsreturen mottas fra banken etter at betalingen er utført. Når dataene leses inn, vises informasjon om antall oppgjorte fakturaer.  

Følgende skjer når avregningsreturen leses inn:  

- Betalingsstatusen i tabellen **Ventekladd** settes til **Avregnet**.  
- Da overføres informasjon fra siden **Ventekladd** til utbetalingskladden.  
- Det opprettes en motkonto for hver transaksjon.  
- Det settes inn bilagsnumre for hver transaksjon.  

## <a name="exchange-rates-by-settlement"></a><a name="exchange-rates-by-settlement"></a>Valutakurser ved oppgjør
Ved oppgjør håndteres valutakurser på følgende måter:  

- Betaling fra en konto i lokal valuta – Hvis en betaling i en annen valuta utføres fra en konto i LV, flagger banken avregningsreturen med en advarsel om hvilken vekslingskurs som benyttes mellom LV og valutaen som benyttes for betalingen.  

- Betaling fra en valutakonto – Hvis betalingen utføres fra en valutakonto, benyttes vekslingskursen for denne valutaen og LV. Dette fordi banken ikke informerer systemet om valutakursen.  

## <a name="warnings-on-settlement-returns"></a><a name="warnings-on-settlement-returns"></a>Advarsler i avregningsreturer
Det kan forekomme advarsler når avregningsreturen leses inn. Innbetalingskladdelinjer med advarsler er merket med et symbol. Hvis du vil vite mer om advarselen, kan du åpne siden **Avregningsopplysninger**.  

## <a name="see-also"></a><a name="see-also"></a>Se også
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
 [Importere betalingsreturdata](how-to-import-payment-return-data.md)   
 [Slette remitteringsoppdrag](how-to-delete-remittance-payment-orders.md)   
 [Remitteringsfeil](remittance-errors.md)   
 [Vise remitteringsfeilkoder](how-to-view-remittance-error-codes.md)   
 [Annullere betalinger](how-to-cancel-payments.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
