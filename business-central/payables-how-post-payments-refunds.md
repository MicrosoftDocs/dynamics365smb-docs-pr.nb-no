---
title: Registrere betalinger og refusjoner i utbetalingskladder
description: 'Les om hvordan du registrerer betalinger du gjør til leverandører og refusjoner du gjør til kunder, på siden Utbetalingskladd.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment journal, print check, vendor payment, customer refund, refund check, creditor, debt, balance due, AP'
ms.search.form: '256, 233, 624, 1228'
ms.date: 07/17/2024
ms.service: dynamics-365-business-central
---
# <a name="record-payments-and-refunds-in-the-payment-journal"></a>Registrere betalinger og refusjoner i utbetalingskladden

På **siden Utbetalingskladder** registrerer du betalinger du gjør til leverandører, og refusjoner du gjør til kunder. Når du bokfører en utbetalingskladdelinje, registreres det betalte beløpet på den angitte bankkontoen. Deretter må du utføre trinnene for å foreta den faktiske pengeoverføringen fra den aktuelle bankkontoen.  

Utbetalingskladder er finanskladder som er tilpasset for betalinger. Du kan raskt legge til linjer manuelt, du kan la [!INCLUDE[prod_short](includes/prod_short.md)] foreslå leverandørbetalinger, og du kan utligne betalingen mot bokførte dokumenter. Selv om du foretar betalinger, kan du angi et positivt beløp i feltet **Dokumentbeløp**. Avhengig av dokumenttypen for kladdelinjen konverteres dette beløpet deretter til et negativt beløp i de underliggende transaksjonene. På denne måten er det raskere for deg å legge til kladdelinjene manuelt. Hvis du foretrekker å angi negative beløp, kan du tilpasse utbetalingskladden til å vise feltet **Beløp** i stedet. Hvis du vil ha mer informasjon om å tilpasse sider, kan du gå til [Start tilpasning ved å bruke tilpasningsmodus](ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode).  

- Utligne betalinger mot fakturaer eller kreditnotaer

    Hvis du fyller ut feltet **Utligningsbilagsnr.** med fakturaen eller kreditnotaen som skal betales eller refunderes, settes dokumentet til **Betalt** når du bokfører kladden. Dette omtales som «utlignet». Som et alternativ til å utligne når du bokfører en betaling, kan du bruke sidene **Utlign levrd.poster** og **Utlign kundeposter** når du har bokført betalingen. Hvis du vil ha mer informasjon, kan du for eksempel gå til [Avstemme leverandørbetalinger med utbetalingskladd eller fra leverandørposter](payables-how-apply-purchase-transactions-manually.md).  

- Hente foreslåtte betalinger til leverandører eller ansatte

    Handlingene **Betalingsforslag - leverandør** og **Betalingsforslag - ansatt** kan hjelpe deg med å fylle ut betalingskladdelinjene automatisk i henhold til leverandørprioritering og forfallsdatoer. Hvis du vil vite mer, kan du gå til [Betalingsforslag - leverandør](payables-how-suggest-vendor-payments.md). Med denne funksjonen er **Utligningsbilagsnr.**-feltet alltid fylt ut.  

- Skrive ut sjekker og sende betalinger elektronisk til banken

    I tillegg til å registrere at betalingen er utført, kan du også bruke siden **Utbetalingskladd** for å legge ut betalingen for ytterligere behandling av banken. Hvis du vil ha mer informasjon, kan du gå til [Foreta sjekkbetalinger](payables-how-work-checks.md) og [Foreta elektroniske betalinger](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).  

## <a name="to-make-payments-in-the-payment-journal"></a>Foreta betalinger i utbetalingskladden

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Utbetalingskladder** og velg den relaterte koblingen.
2. Åpne kladden som du bruker for betalinger.
3. Hvis du vet hvem du skal betale, fyller du ut feltene manuelt. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Hvis du også vil utligne betalingen mot den tilknyttede fakturaen eller kreditnotaen, velger du utligningsbilagsnummeret **.** -feltet, **Velg den aktuelle fakturaen eller kreditnotaen på siden Bruk leverandørposter**, og deretter velger du **OK** .

    Mange felter som **Dokumentbeløp** og **Forfallsdato** inneholder nå opplysninger fra det valgte dokumentet.
5. Du kan også bruke handlingen **Betalingsforslag - leverandør**. Alle utligningsopplysninger og beløper angis også på kladdelinjene. Hvis du vil vite mer, kan du gå til [Betalingsforslag - leverandør](payables-how-suggest-vendor-payments.md).
6. Når du har fullført alle utbetalingskladdelinjene, kan du velge handlingen **Bokfør**.

## <a name="to-issue-a-refund-check"></a>Slik utsteder du en refusjonssjekk

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Utbetalingskladder**, og velg deretter den relaterte koblingen.
2. Velg **Refusjon** i **Bilagstype**-feltet.  
3. Angi en referanse for refusjonssjekken (for eksempel ordrereturnummeret) i feltet **Eksternt dokumentnr.**.  
4. Velg **Kunde** i **Kontotype**-feltet.  
5. Velg kundens kontonummer som refusjonssjekken skal utstedes til, i feltet **Kontonr.**.  
6. Angi beløpet som skal refunderes i feltet **Beløp**.  
7. Velg **Bankkonto** i **Motkontotype**-feltet.  
8. I Motkontonr **.** -feltet, Velg bankkontoen sjekken kommer ut av.  
9. I **Utligningsbilagsnr.** -feltet velger du dokumentene som krever refusjon.  
10. Når du har fullført alle utbetalingskladdelinjene, velger du handlingen **Bokfør/Skriv ut**, velger handlingen **Bokfør og skriv ut** og velger deretter **Ja**.  
  
## <a name="see-also"></a>Se også

[Foreta sjekkbetalinger](payables-how-work-checks.md)  
[Utfør elektroniske betalinger](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[Administrere skyldige beløp](payables-manage-payables.md)  
[Konfigurere banktjenester](bank-setup-banking.md)  
[Eksportere en Positive Pay-fil](finance-how-positive-pay.md)  
[Arbeid med finanskladder](ui-work-general-journals.md)  
[Tilpasse arbeidsområdet](ui-personalization-user.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
