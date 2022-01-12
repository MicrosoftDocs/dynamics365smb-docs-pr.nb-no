---
title: Opprette bankkonti (inneholder video)
description: Lær hvordan bankkonti brukes i Business Central, og hvordan du kan avstemme beløp med banken.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: f7984f5bf96208582be5a25a817cabb77589fe99
ms.sourcegitcommit: 4c97f38fc53c1c1ec534054a4a100d8cfb73175b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2021
ms.locfileid: "7940604"
---
# <a name="set-up-bank-accounts"></a>Opprette bankkonti

Du bruker bankkonti i [!INCLUDE[prod_short](includes/prod_short.md)] til å holde orden på banktransaksjonene dine. Konti kan utstedes i norske kroner eller i fremmed valuta. Når du har opprettet bankkonti, kan du bruke mulighetene for utskriving av sjekker (gjelder ikke Norge). Bankkontiene omfatter ekstra funksjonalitet for [betalingsavstemming](receivables-apply-payments-auto-reconcile-bank-accounts.md), [bankavstemming](bank-how-reconcile-bank-accounts-separately.md) og import og eksport av bankfiler. Bankkontiene kan også inkluderes i transaksjoner i finanskladdene. Hver bankkonto er knyttet til en konto i kontoplanen gjennom den tilordnede bankbokføringsgruppen. Hvis du bruker en bankkonto i en betalingstransaksjon, opprettes automatisk en post både på bankkontoen og den tilkoblede finanskontoen.  

Bankkonti fungerer på ulike måter avhengig av om en valutakode er angitt:

- Valutakoden er tom

  Alle transaksjoner i bankkontoen vil være i den lokale valutaen (LV) for det gjeldende selskapet. Hvis det gjøres en transaksjon til kontoen i en annen valuta, bokføres beløpene til kontoen i LV basert på den relevante valutakursen. Eventuelle sjekker som er utstedt fra denne kontoen, må utstedes i LV. Hvis bankkontoen brukes i en kladd, vil kladdelinjen automatisk arve den tomme valutakoden.  
- Valutakoden er angitt

  Alle transaksjoner som gjøres til denne kontoen, må være i samme valuta som angitt på kontoen. Alle sjekker som er utstedt fra denne kontoen, må også ha denne valutaen.  

En bankkonto er en integrert del av [!INCLUDE[prod_short](includes/prod_short.md)] og spiller en rolle i mange andre funksjoner. Følgende illustrasjon viser de viktigste relasjonene:

![Bilde av bankkontorelasjoner.](media/Set-Up-Bank-Accounts/Bank_Account_Relations.png)

Dette betyr at det er mulig å opprette en bankkonto slik at den blir tilgjengelig alle steder over og i tillegg blir speilet for den aktuelle finanskontoen og på siden **Selskapsopplysninger**.

En bankkonto overvåkes vanligvis daglig for å sikre at nye betalinger fra kunder registreres så raskt som mulig. Dette sikrer at den faktiske statusen for kundene gjenspeiles i [!INCLUDE[prod_short](includes/prod_short.md)] slik at selgerne, regnskapsførere og andre ansatte har tilgang til relevant og oppdatert informasjon. På denne måten unngår du at kunden får unødvendige samtaler med kunden angående forfalte fakturaer eller forsinkelse i forsendelser.  

![Bilde av bankbetaling.](media/Set-Up-Bank-Accounts/Bank-payment-flow.png)

En annen aktivitet er å importere leverandørvalutabetalingene med de realiserte valutakursene for å sikre at den faktiske statusen for leverandørene er oppdatert. Den enkleste måten for å sikre at bankkontoen er oppdatert på er ved hjelp av funksjonen for [betalingsavstemming](receivables-apply-payments-auto-reconcile-bank-accounts.md). I **betalingsavstemmingskladden** kan du importere banktransaksjoner direkte fra et elektronisk bankprogram og få dem automatisk bokført mer eller mindre. Kladden identifiserer og bokfører automatisk følgende:  

- Direct Debit-betalinger fra kunder  
- Kundebetalinger for enkeltfakturaer  
- Engangsbetalinger fra kunder  
- Kundebetalinger i utenlandsk valuta  
- Leverandørbetalinger  
- Leverandørbetalinger i utenlandsk valuta  
- Gjentakende leverandørbetalinger og abonnementer  
- Bankgebyrer og renter  

Betalingsavstemming gir massive tidsbesparelser i bokføring av inngående og utgående betalinger. Transaksjonene på bankkontoen i [!INCLUDE[prod_short](includes/prod_short.md)] er imidlertid ikke vurdert 100 % riktig før du kjører en bankavstemming.  

Bankavstemming er måten du sørger for at bankkontoen er i [!INCLUDE[prod_short](includes/prod_short.md)] samsvar med den eksterne kontoen i banken.  

 ![Bilde av bankkontoavstemming.](media/Set-Up-Bank-Accounts/BankReconciliation.png)

I illustrasjonen ovenfor representerer den venstre siden bankkontoen i [!INCLUDE[prod_short](includes/prod_short.md)], og den høyre siden representerer transaksjonene som importeres fra banken via det elektroniske bankprogrammet. Diagrammet i midten viser transaksjonene fra begge sider, som er bankavstemmingen.

Fra bankkontoen i [!INCLUDE[prod_short](includes/prod_short.md)] blir de fleste transaksjoner kjent for den fysiske banken. De eneste unntakene omfatter følgende tilfeller:  

- Korrigeringer bokført i [!INCLUDE[prod_short](includes/prod_short.md)]  
- Sjekker utstedt som ikke er blitt betalt ennå  
- Leverandørbetalinger som ikke er godkjent av banken  

Fra den fysiske kontoen i banken kommer det hele tiden ukjente transaksjoner som ikke ble identifisert i betalingsavstemmingskladden, for eksempel følgende:  

- Nye leverandørabonnementer  
- Kundebetalinger uten beskrivelse
- Bankrenter
- Bankgebyrer
- Kredittkortgebyrer som ikke er rapportert ennå

Jo bedre tilordningsopplysningene du gjør i betalingsavstemmingskladden er, jo mer bokføres transaksjoner automatisk og desto enklere blir regelmessig bankavstemming.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

<br><br>

> [!WARNING]
> Noen felter kan inneholde sensitive opplysninger, for eksempel feltene **Bankregistreringsnr.**, **Bankkontonr.**, **SWIFT-kode** og **IBAN- kode**. Hvis du vil ha mer informasjon, se [Overvåke sensitive felt](across-log-changes.md#monitoring-sensitive-fields).

## <a name="to-set-up-bank-accounts"></a>Slik setter du opp bankkonti

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bankkonti**, og velg deretter den relaterte koblingen.
2. På siden **Bankkonti** velger du handlingen **Ny**.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Noen felter er skjult inntil du velger **Vis flere**-handling, vanligvis fordi de brukes sjelden. Andre må legges til ved hjelp av tilpasning. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).

Du kan opprette så mange bankkonti du trenger for virksomheten. For hver bankkonto må du angi informasjon som gjør bankkontoen unikt identifiserbar. Denne informasjonen omfatter bankens geografiske adresse, nummerserie for forskjellige transaksjonstyper, for eksempel direkte debet og kredittoverføringer, valutaen som beløpene er angitt i, og informasjon som brukes til å importere bankkontoutdrag. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
<!--
The following table explains key fields.

|Field|Description|  
|---------------------------------|---------------------------------------|  
|**General FastTab**||
|No.|Specifies the number of the bank account, according to the specified number series. If the number series allow manual numbering, any alphanumeric code up to 20 characters can be used.|
|Name|The Name of the bank holding the bank account.|
|Bank Branch No.|The Bank Branch No. is usually used to identify the bank branch in domestic payments. The Bank Branch No. is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Account No.|Bank Account No. is usually used to identify the bank account no. in domestic payments. The Bank Account No. is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Balance|Shows the Balance of the bank account in the account currency.|
|Balance (LCY)|Shows the Balance of the bank account in the local currency (LCY).|
|Our Contact Code|Specifies a code to specify the employee who is responsible for this bank account. The employee must be created in the **Salesperson/Purchaser** table.|
|Blocked|Specifies that the related record is blocked from being posted in transactions, for example the account is obsolete after a bank change.|
|SEPA Direct Debit Exp. Format|Specifies the SEPA format of the bank file that will be exported when you choose the **Create Direct Debit File** button in the **Direct Debit Collect. Entries** window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Credit Transfer Msg. Nos.|Specifies the number series for bank instruction messages that are created with the export file that you create from the Direct Debit Collect. Entries window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Direct Debit Msg. Nos.|Specifies the number series that will be used on the direct debit file that you export for a direct-debit collection entry in the Direct Debit Collect. Entries window. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Creditor No.|Specifies your company as the creditor in connection with payment collection from customers using SEPA Direct Debit. Read more in [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Bank Clearing Standard|The national bank names register used for the sender bank account.|
|Bank Clearing Code|Specifies the code for bank clearing that is required according to the format standard that you selected in the Bank Clearing Standard field. The bank clearing code can be used as an alternative to SWIFT and IBAN to identify your bank as sender of a bank transfer.|
|Last Date Modified|Date of the latest modification of the bank account.|
|**Payment Matching**||
|Disable Automatic Payment Matching|Specifies whether to disable automatic payment matching after importing bank transactions for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Payment Match Tolerance**||
|Match Tolerance Type|Specifies by which tolerance the automatic payment application function will apply the Amount Incl. Tolerance Matched rule for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Match Tolerance Value|Specifies if the automatic payment application function will apply the Amount Incl. Tolerance Matched rule by Percentage or Amount. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Hidden Fields**||
|Search Name|Specifies an alternate name that you can use to search for the record in question when you cannot remember the value in the Name field.|
|Min. Balance|Specifies a minimum balance for the bank account. This field is for information purposes only.|
|Positive Pay Export Code|Specifies a code for the data exchange definition that manages the export of positive-pay files. Read more in [Export Positive Pay Files](finance-how-positive-pay.md).|
|**Communication FastTab**||
|Address|The address of the bank branch.|
|Address 2|An additional address field for the bank branch.|
|Post Code|The post code of the bank branch.|
|City|The city of the bank branch.|
|Country/Region Code|The Country/Region Code of the bank branch.|
|Phone No.|The Phone No. of the bank branch.|
|Mobile Phone No.|The Mobile Phone No. of the bank branch.|
|Contact|The main contact in the bank branch. Additional contacts can be created in the Contacts module.|
|Fax No.|The Fax No. of the bank branch.|
|Email|The Email of the bank branch.|
|Home Page|The Home Page of the bank branch.|
|**Posting FastTab**||
|Currency Code|Specifies the relevant currency code for the bank account. Applying a currency code to a bank account will limit all transactions to only use the applied currency code. Leaving the currency code blank will allow transactions in all currencies, however, the amount will be converted to the local currency (LCY) using the applied currency rate. Checks issued from this account will also follow the same rules.|
|Last Check No.|The number of the latest check issued from this account.|
|Transit No.|Specifies a bank identification number of your own choice.|
|Last Statement No.|The number of the latest bank reconciliation posted to this account. Read more in [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Last Payment Statement No.|The number of the latest payment reconciliation posted to this account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Last Bank Statement|The ending-balance of the last bank statement. Read more in [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Bank Acc. Posting Group|Specifies a code for the bank account posting group for the bank account. The Bank Acc. Posting Group connects the bank account to the G/L Account in the balance sheet.|
|**Transfer**||
|Transit No.|Specifies a bank identification number of your own choice.|
|SWIFT Code|Specifies the international bank identifier code (SWIFT) of the bank where you have the account. The SWIFT Code is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|IBAN|Specifies the bank account's international bank account number. The IBAN Code is very often considered a sensitive field. Read more about [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Statement Import Format|Specifies the format of the bank statement file that can be imported into this bank account. The format is being used in both the payment reconciliation journals and the bank account reconciliations.|
|Payment Export Format|Specifies the format of the bank file that will be exported when you choose the Export Payments to File button in the Payment Journal window.|
-->
> [!NOTE]
> For å kunne fylle ut **Saldo**-feltet med en inngående balanse, må du bokføre en bankkontopost med det aktuelle beløpet. Du kan gjøre dette ved å utføre en bankkontoavstemming. Hvis du vil ha mer informasjon, kan du se [Avstemme bankkontoer](bank-how-reconcile-bank-accounts-separately.md). Du kan eventuelt også implementere den inngående balansen som en del av en generell dataoppretting i nye selskaper ved hjelp av den assisterte oppsettveiledningen **Overfør forretningsdata**. Hvis du vil ha mer informasjon, kan du se [Bli klar til å gjøre forretninger](ui-get-ready-business.md). Hvis du vil ha mer informasjon om hvordan du oppretter åpningssaldoer i [!INCLUDE[prod_short](includes/prod_short.md)], kan du se [Opprette inngående balanser for kladd](admin-how-to-create-journal-opening-balances.md).

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Opprette din bankkonto for import eller eksport av bankfilene

Felt i hurtigfanen **Overføring** på siden **Bankkontokort** er relatert til import og eksport av bankfeeder og filer. Hvis du vil ha mer informasjon, kan du se [Bruke AMC Banking 365 Fundamentals-utvidelsen](ui-extensions-amc-banking.md) og [Konfigurere Envestnet Yodlee Bank Feeds-tjenesten](bank-how-setup-bank-statement-service.md).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bankkonti**, og velg deretter den relaterte koblingen.
2. Åpne kortet for en bankkonto som du vil eksportere eller importere bankfiler for.
3. Fyll ut feltene på hurtigfanen **Overføring** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Andre fileksporttjenester og formater krever ulike oppsettsverdier på siden **Bankkort**. Du blir informert om feil eller manglende oppsettsverdier når du prøver å eksportere filen. Les derfor de korte beskrivelsene av feltene nøye, eller se relaterte fremgangsmåteeemner. Hvis du for eksempel eksporterer en betalingsfil for Nord-Amerika elektronisk pengeoverføring (EFT) krever at både feltet **Nr. for siste remitteringsmelding** og feltet **Transittnr.** er fylt ut. Hvis du vil ha mer informasjon, kan du se [Eksportere betalinger til en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

Feltene i hurtigfanen **Transitt** på bankkontoen dekker ulike formål, avhengig av om betalingen er inngående eller utgående.

Illustrasjonen viser ruten for inngående betalinger:

:::row:::
    :::column:::
        1. Transaksjonene eksporteres fra bankkontoen i et CSV-format som kan leses av mennesker eller i bankens eget format.
        <br><br>
2. *Datautvekslingsdefinisjonen* tilordner informasjonen i filen til feltene i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Definere datautveksling](across-set-up-data-exchange.md)
<br><br>
3. *Oppsettet for dataeksport og -import* definerer eksporten eller importen, og den er koblet til datautvekslingsdefinisjonen.
<br><br>
4. *Importformatet for bankkontoutdrag* kobler importoppsettet til bankkontoen.
<br><br>
5. Betalingene importeres gjennom siden **Betalingsavstemmingskladd** eller **Bankkontoavstemming**.
    :::column-end:::
    :::column:::
        ![Bilde av betalinger mottatt fra banken til bankkonti.](media/Set-Up-Bank-Accounts/payments-in-and-out-1.png)
    :::column-end:::
:::row-end:::

Inngående betalinger importeres alltid gjennom siden for **betalingsavstemmingskladd** eller direkte på siden **Bankkontoavstemming**. Utgående betalinger kan derimot starte fra en hvilken som helst utbetalingskladd. Den eneste forutsetningen er at feltet **Tillat betalingseksport** i den aktuelle utbetalingskladden må velges.

Illustrasjonen viser ruten for utgående betalinger:

:::row:::
    :::column:::
        6. Transaksjonene som er fylt ut i en betalingsjournal, er klargjort for eksport av betalinger til fil.
        <br><br>
        7. *Importformatet for bankkontoutdrag* kobler importoppsettet til bankkontoen
        <br><br>
        8. *Oppsettet for dataeksport og -import* definerer eksporten eller importen, og den er koblet til datautvekslingsdefinisjonen.
        <br><br>
        9. *Datautvekslingsdefinisjonen* tilordner informasjonen i filen til feltene i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Definere datautveksling](across-set-up-data-exchange.md)
        <br><br>
        10. Betalingene eksporteres fra utbetalingskladden og importeres til bankkontoen
    :::column-end:::
    :::column:::
        ![Bilde av betalinger fra bankkonti som sendes til banken.](media/Set-Up-Bank-Accounts/payments-in-and-out-2.png)
    :::column-end:::
:::row-end:::

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Opprette dine leverandørbankkonti for import eller eksport av bankfilene

Felt i hurtigfanen **Overføring** på siden **Leverandørs bankkort** er relatert til eksport av bankfeeder og filer. Hvis du vil ha mer informasjon, se [Bruke AMC Banking 365 Fundamentals-utvidelsen](ui-extensions-amc-banking.md) og [Eksportere betalinger til en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Leverandører** og velger den relaterte koblingen.
2. Åpne kortet for en leverandør med en bankkonto som du vil eksportere betalingsbankfiler til.
3. Velg **Bankkonti**-handlingen.
4. Fra **listen over bankkonti for leverandør** velger eller legger du til den aktuelle bankkontoen eller legget til en ny bankkonto.  
5. På siden **Leverandørs bankkort**, i hurtigfanen **Overføring**, fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!WARNING]
> Noen felter på leverandørbankkontoen kan inneholde sensitive opplysninger, for eksempel feltene **Bankregistreringsnr.**, **Bankkontonr.**, **SWIFT-kode** og **IBAN- kode**. Hvis du vil ha mer informasjon, se [Overvåke sensitive felt](across-log-changes.md#monitoring-sensitive-fields).

## <a name="changing-your-bank-account"></a>Endre bankkontoen

Hvis du vil bruke en annen bankkonto for bedriften, må du opprette den nye bankkontoen i [!INCLUDE[prod_short](includes/prod_short.md)]. Vi anbefaler at du ikke bare erstatter opplysningene om kontoen du bruker, fordi du kan få uriktige data. Det kan for eksempel hende at åpningssaldoen er feil eller at bankfeeden slutter å virke riktig. Det er viktig at du holder gjeldende og nye konti separat.

Når du har opprettet den nye bankkontoen, må du også opprette en ny bankbokføringsgruppe og tilordne den til en ny finanskonto. Du kan bruke en eksisterende bankbokføringsgruppe på nytt, og banktransaksjoner bokføres på de samme finanskontiene som de andre bankkontiene som deler bankbokføringsgruppen. Vi anbefaler imidlertid at du oppretter en ny bankbokføringsgruppe og finanskonto slik at det blir enklere å foreta avstemminger.

> [!NOTE]
> Husk at bankkontoinformasjonen på åpne salgsfakturaer fortsatt viser den opprinnelige bankkontoen. Det betyr at betalinger fortsatt bokføres til denne kontoen. Vi anbefaler at du lar begge kontoene være aktive i en periode etter endringen.

Hvis du vil ha en mer kompakt visning av kontantkontiene i finansrapportering, kan du bruke fra kontiene **Fra-sum** og **Til-sum** i kontoplanen, radene **Sammentelling** i kontoplaner eller finanskontokategorier. Hvis du vil ha mer informasjon, kan du se delen [Business Intelligence og Financial Reporting](bi.md).

## <a name="see-also"></a>Se også

[Konfigurere banktjenester](bank-setup-banking.md)  
[Definere bokføringsgrupper](finance-posting-groups.md)  
[Avstemme bankkonter](bank-manage-bank-accounts.md)  
[Konfigurere Envestnet Yodlee Bank Feeds-tjenesten](bank-how-setup-bank-statement-service.md)  
[SEPA Direct Debit i Business Central](finance-collect-payments-with-sepa-direct-debit.md)  
[Slik konfigurerer du din bankkonto for SEPA direct debit](finance-collect-payments-with-sepa-direct-debit.md#to-set-up-your-bank-account-for-sepa-direct-debit)  
[Slik oppretter du en bankkonto for SEPA-kredittoverføring:](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-set-up-a-bank-account-for-sepa-credit-transfer)  
[Betale med AMC Banking 365 Fundamentals-utvidelsen eller SEPA-kredittoverføring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Betalingsavstemming](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Forstå Finans og kontoplanen](finance-general-ledger.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
