---
title: Elektroniske betalinger til leverandører i Norge
description: Norske forbedringer omfatter automatisk betaling til leverandører i den norske versjonen av Business Central.
services: project-madeira
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/18/2021
ms.author: bholtorf
---
# <a name="electronic-payments-to-vendors-in-norway"></a>Elektroniske betalinger til leverandører i Norge
[!INCLUDE[prod_short](../../includes/prod_short.md)]inkluderer forbedringer i den norske versjonen for automatisk betaling til leverandører. Dette reduserer sjansen for at feil skal oppstå på grunn av manuell registrering av data. Denne funksjonaliteten kan brukes til å utføre følgende operasjoner:  

- Søke etter fakturaer som er forfalt, basert på ulike kriterier.  
- Sende betalinger til banken.  
- Motta meldinger fra banken om status for betalinger.  
- Motta informasjon om betalte transaksjoner som skal bokføres.  

Du kan utføre elektroniske betalinger i følgende formater:  

- TelePay  
- Remitteringsoppdrag  

## <a name="electronic-payment-process"></a>Elektronisk betalingsprosess
Elektroniske betalinger behandles på følgende måte:  

1.  Betalingsforslaget kjøres i den elektroniske betalingsfunksjonen og overføres til banken ved hjelp av bankens programvare.  
2.  Bankens programvare mottar betalingene og overfører dem til banken.  
3.  Banken mottar betalingene og sender den første mottaksreturen til [!INCLUDE[prod_short](../../includes/prod_short.md)] via bankens programvare.  
4.  Banken utfører betalingene og sender avregningsreturen (andre mottaksretur) til [!INCLUDE[prod_short](../../includes/prod_short.md)] via bankens programvare, hvor betalingene bokføres.  

## <a name="vendor-payment-requirements"></a>Krav til leverandørbetalinger
Hvis betalingstransaksjonene ikke oppfyller kravene, vises en feilmelding, og du kan ikke opprette en betalingsfil for overføringer til banken. Følgende kriterier må oppfylles ved når du behandler betalinger til leverandører:  

- Betalingstransaksjonen må være positiv eller null. En betalingstransaksjon må overføre et positivt beløp (eller null) til betalingsmottakeren. Dette betyr at når en kreditnota skal trekkes fra, må fakturaen i samme betalingstransaksjon lyde på det samme eller et høyere beløp. Det er ikke mulig å trekke fra penger på leverandørens konto.  

- Det må anvendes en kreditnota sammen med fakturaen. En kreditnota inneholder vanligvis ikke en Kunde-ID (KID). Du kan ikke betale en kreditnota i en betalingstransaksjon med fakturaer som inneholder et KID-nummer. Årsaken er at betalinger vanligvis deles opp i transaksjoner med eller uten KID-nummer. Det betyr at hvis en kreditnota uten KID-nummer betales sammen med en faktura i samme betalingstransaksjon, må fakturaen betales uten KID-nummer, og mottakerreferansenummeret må brukes i stedet.  

- Hvis fakturaen og kreditnotaen betales i samme betalingstransaksjon, må betalingen finne sted på samme dato, i samme valuta og med samme valutakurs.  

## <a name="see-also"></a>Se også
 [Funksjonalitet som er spesifikk for norske brukere](norway-local-functionality.md)   
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
 [Remitteringsfeil](remittance-errors.md)   
 [Vise remitteringsfeilkoder](how-to-view-remittance-error-codes.md)   
 [Annullere betalinger](how-to-cancel-payments.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
