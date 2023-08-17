---
title: Opprette bankkonti (inneholder video)
description: 'Lær hvordan bankkonti brukes i Business Central, og hvordan du kan avstemme beløp med banken.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'Yodlee, feed, stream'
ms.search.form: '370, 371, 372, 373, 375, 423, 424, 425, 426, 1240, 1280'
ms.date: 08/03/2023
ms.custom: bap-template
---
# <a name="set-up-bank-accounts"></a>Opprette bankkonti

Du bruker bankkonti i [!INCLUDE[prod_short](includes/prod_short.md)] til å holde orden på banktransaksjonene dine. Konti kan utstedes i norske kroner eller i fremmed valuta. Når du har opprettet bankkonti, kan du bruke mulighetene for utskriving av sjekker (gjelder ikke Norge). Bankkontiene omfatter ekstra funksjonalitet for [betalingsavstemming](receivables-apply-payments-auto-reconcile-bank-accounts.md), [bankavstemming](bank-how-reconcile-bank-accounts-separately.md) og import og eksport av bankfiler. Bankkontiene kan også inkluderes i transaksjoner i finanskladdene. Hver bankkonto er knyttet til en konto i kontoplanen gjennom den tilordnede bankbokføringsgruppen. Hvis du bruker en bankkonto i en betalingstransaksjon, opprettes automatisk en post både på bankkontoen og den tilkoblede finanskontoen.  

Bankkonti fungerer på ulike måter avhengig av om en valutakode er angitt:

- Hvis valutakoden er tom

  Alle transaksjoner i bankkontoen vil være i den lokale valutaen (LV) for det gjeldende selskapet. Hvis det gjøres en transaksjon til kontoen i en annen valuta, bokføres beløpene til kontoen i LV basert på den relevante valutakursen. Eventuelle sjekker som er utstedt fra denne kontoen, må utstedes i LV. Hvis bankkontoen brukes i en kladd, vil kladdelinjen automatisk arve den tomme valutakoden.  
  
- Valutakoden er angitt

  Alle transaksjoner som gjøres til og kontroller som utstedes fra denne kontoen, må være i samme valuta som angitt på kontoen.

Du kan spare tid på dataregistrering ved å lage en bankkonto som standardkonto som skal brukes for valutaen som er angitt for kontoen. Hvis du gjør det, tildeles kontoen til salgs- og servicedokumenter som bruker valutaen. Hvis du vil gjøre kontoen til standard for salgs- og servicedokumenter, aktiverer du alternativet **Bruk som standard for valuta** på **Bankkontokort**-siden. Hvis det er nødvendig, kan du velge en annen konto når du arbeider med et dokument.

En bankkonto er en integrert del av [!INCLUDE[prod_short](includes/prod_short.md)] og spiller en rolle i mange andre funksjoner. Følgende illustrasjon viser de viktigste relasjonene:

![Bilde av bankkontorelasjoner.](media/Set-Up-Bank-Accounts/Bank_Account_Relations.png)

Du kan se at det er mulig å opprette en bankkonto slik at den blir tilgjengelig alle steder over og i tillegg blir speilet for den aktuelle finanskontoen og på siden **Selskapsopplysninger**.

En bankkonto overvåkes vanligvis daglig for å sikre at nye betalinger fra kunder registreres så raskt som mulig. Dette sikrer at kundens faktiske status gjenspeiles i [!INCLUDE[prod_short](includes/prod_short.md)]. Dette gir selgere, regnskapsførere og andre ansatte tilgang til de mest relevante og oppdaterte opplysningene, slik at de unngår å foreta unødvendige anrop til kunden med hensyn til forfalte fakturaer eller forsinkelser i forsendelse.  

![Bilde av bankbetaling.](media/Set-Up-Bank-Accounts/Bank-payment-flow.png)

En annen aktivitet er å importere leverandørvalutabetalingene med de realiserte valutakursene for å sikre at den faktiske statusen for leverandørene er oppdatert. Det er den enkleste måten å bruke funksjonen for [betalingsavstemming](receivables-apply-payments-auto-reconcile-bank-accounts.md) på. I **betalingsavstemmingskladden** kan du importere banktransaksjoner direkte fra et elektronisk bankprogram og få dem automatisk bokført mer eller mindre. Kladden identifiserer og bokfører automatisk følgende:  

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

Fra bankkontoen i [!INCLUDE[prod_short](includes/prod_short.md)] blir de fleste transaksjoner kjent for den fysiske banken. De få unntakene omfatter følgende tilfeller:  

- Korrigeringer bokført i [!INCLUDE[prod_short](includes/prod_short.md)]  
- Sjekker utstedt som ikke er blitt betalt ennå 
- Leverandørbetalinger som ikke er godkjent av banken ennå  

Fra den fysiske kontoen i banken kommer det hele tiden uidentifiserte transaksjoner i betalingsavstemmingskladden, for eksempel følgende:  

- Nye leverandørabonnementer  
- Kundebetalinger uten beskrivelse
- Bankrenter
- Bankgebyrer
- Kredittkortgebyr ennå ikke rapportert

Jo bedre tilordningsopplysningene du gjør i betalingsavstemmingskladden er, jo mer bokføres transaksjoner automatisk og desto enklere blir regelmessig bankavstemming.

Se i videoen under de grunnleggende trinnene for å opprette en bankkonto i [!INCLUDE[prod_short](includes/prod_short.md)].

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

> [!WARNING]
> Noen felter kan inneholde sensitive opplysninger, for eksempel feltene **Bankregistreringsnr.**, **Bankkontonr.**, **SWIFT-kode** og **IBAN- kode**. Lær mer på [Overvåk sensitive felter](across-log-changes.md#monitor-sensitive-fields).

## <a name="to-set-up-bank-accounts"></a>Slik setter du opp bankkonti

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bankkontoer**, og velg deretter den relaterte koblingen.
2. På siden **Bankkonti** velger du handlingen **Ny**.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Et eksempel vil være Feltet **Bankkontobokføringsgruppe**, som kobler bankkontoen til den underliggende finanskontoen i balansen. Finn ut mer under [Definere bokføringsgrupper](finance-posting-groups.md).

> [!TIP]
> Noen felter er skjult inntil du velger **Vis flere**-handling, vanligvis fordi de brukes sjelden. Andre må legges til ved hjelp av tilpasning. Finn ut mer under [Tilpass arbeidsområdet](ui-personalization-user.md).

Du kan opprette så mange bankkonti du trenger for virksomheten. For hver bankkonto må du angi informasjon som gjør bankkontoen unikt identifiserbar. Denne informasjonen omfatter bankens geografiske adresse, nummerserie for forskjellige transaksjonstyper, for eksempel direkte debet og kredittoverføringer, valutaen som beløpene er angitt i, og informasjon som brukes til å importere bankkontoutdrag. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
<!--
The following table explains key fields.

|Field|Description|  
|---------------------------------|---------------------------------------|  
|**General FastTab**||
|No.|Specifies the number of the bank account, according to the specified number series. If the number series allow manual numbering, any alphanumeric code up to 20 characters can be used.|
|Name|The Name of the bank holding the account.|
|Bank Branch No.|Typically used to identify the bank branch in domestic payments, it's very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Account No.|Typically used to identify the bank account number in domestic payments, it's very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Balance|Shows the bank account balance in the account currency.|
|Balance (LCY)|Shows the bank account balance in the local currency (LCY).|
|Our Contact Code|Specifies a code to identify the employee responsible for this bank account. The employee must be created in the **Salesperson/Purchaser** table.|
|Blocked|Specifies the related record is blocked from being posted in transactions, for example the account is obsolete after a bank change.|
|SEPA Direct Debit Exp. Format|Specifies the single euro payments area (SEPA) format of the bank file to be exported when you choose **Create Direct Debit File** on the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Credit Transfer Msg. Nos.|Specifies the number series for bank instruction messages created with the export file you create from the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Direct Debit Msg. Nos.|Specifies the number series to be used on the direct debit file you export for a direct debit collection entry on the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Creditor No.|Specifies your company as the creditor in connection with payment collection from customers using SEPA direct debit. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Bank Clearing Standard|The national bank names register used for the sender bank account.|
|Bank Clearing Code|Specifies the code for bank clearing required according to the format standard you selected in the **Bank Clearing Standard** field. The bank clearing code can be used as an alternative to SWIFT and IBAN to identify your bank as the sender of a bank transfer.|
|Last Date Modified|Date of the latest modification of the bank account.|
|**Payment Matching**||
|Disable Automatic Payment Matching|Specifies whether or not to disable automatic payment matching after importing bank transactions for this bank account. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Payment Match Tolerance**||
|Match Tolerance Type|Specifies the tolerance the automatic payment application function will use to apply the *Amount Incl. Tolerance Matched* rule for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Match Tolerance Value|Specifies if the automatic payment application function will apply the *Amount Incl. Tolerance Matched* rule by percentage or amount. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Hidden Fields**||
|Search Name|Specifies an alternate name you can use to search for the record in question when you can't remember the value in the **Name** field.|
|Min. Balance|Specifies a minimum balance for the bank account. This field is for information purposes only.|
|Positive Pay Export Code|Specifies a code for the data exchange definition managing the export of positive-pay files. Learn more at [Export Positive Pay Files](finance-how-positive-pay.md).|
|**Communication FastTab**||
|Address|The address of the bank branch.|
|Address 2|An additional address field for the bank branch.|
|Post Code|The post code of the bank branch.|
|City|The city of the bank branch.|
|Country/Region Code|The country/region code of the bank branch.|
|Phone No.|The phone number of the bank branch.|
|Mobile Phone No.|The mobile phone number of the bank branch.|
|Contact|The main contact in the bank branch. Additional contacts can be created in the **Contacts** module.|
|Fax No.|The fax number of the bank branch.|
|Email|The email address of the bank branch.|
|Home Page|The home page address of the bank branch website.|
|**Posting FastTab**||
|Currency Code|Specifies the relevant currency code for the bank account. Applying a currency code to a bank account limits all transactions to only using the applied currency code. Leaving the currency code blank allows transactions in all currencies, however, the amount will eventually be converted to the LCY using the applied currency rate. Checks issued from this account follow the same rules.|
|Last Check No.|The number of the latest check issued from this account.|
|Transit No.|Specifies a bank identification number of your own choice.|
|Last Statement No.|The number of the latest bank reconciliation posted to this account. Learn more at [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Last Payment Statement No.|The number of the latest payment reconciliation posted to this account. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Last Bank Statement|The ending balance of the last bank statement. Learn more at [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Bank Acc. Posting Group|Specifies a code for the bank account's posting group. The **Bank Acc. Posting Group** connects the bank account to the G/L account in the balance sheet.|
|**Transfer**||
|Transit No.|Specifies a bank identification number of your own choice.|
|SWIFT Code|Specifies the international bank identifier (SWIFT) code of the bank in which you have account. The SWIFT code is very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|IBAN|Specifies the bank account's international bank account number (IBAN). The IBAN code is very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Statement Import Format|Specifies the format of the bank statement file imported into this bank account. This format is used in both the payment reconciliation journals and bank account reconciliations.|
|Payment Export Format|Specifies the format of the bank file that is exported when you choose **Export Payments to File** on the **Payment Journal** page.|
-->

## <a name="to-enter-an-opening-balance"></a>Slik angir du en startsaldo

For å kunne fylle ut **Saldo**-feltet med en inngående balanse, må du bokføre en bankkontopost med det aktuelle beløpet. Du kan gjøre dette ved å utføre en bankkontoavstemming. Finn ut mer på [Avstemme bankkontoer](bank-how-reconcile-bank-accounts-separately.md).  
>
> Du kan eventuelt også implementere den inngående balansen som en del av en generell dataoppretting i nye selskaper ved hjelp av veiledningen for assistert oppsett for **Overfør forretningsdata**. Finn ut mer under [Bli klar til å gjøre forretninger](ui-get-ready-business.md).  

> [!IMPORTANT]
> Ikke bokfør åpningssaldoen direkte i finans. Det fører til at poster i finanskontoen som ble bokført direkte, vanligvis fører til at du ikke kan avstemme bankkontoen. Med bankkontoer med utenlandsk valuta vil en slik øvelse resultere i forskjeller som akkumuleres når du bokfører flere bankavstemminger. Vanligvis bokfører du åpningssaldoen direkte til bankkontoen, og beløpet ender deretter opp i finanskontoen. Alternativt kan du senere tilbakeføre det fra finanskontoen som du bruker til å balansere den åpne finanssaldoen. I begge tilfeller må du balansere eventuell direkte bokføring til finanskontoen før du starter den første bankavstemmingen, og spesielt hvis bankkontoen er i en utenlandsk valuta.

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Opprette din bankkonto for import eller eksport av bankfilene

Feltene som er knyttet til import og eksport av bankfeeder og -filer, er på hurtigfanen **Overføring** på siden **Bankkontokort**. Se mer på [Bruke AMC Banking 365 Fundamentals-utvidelsen](ui-extensions-amc-banking.md) og [Konfigurere Envestnet Yodlee Bank Feeds-tjenesten](bank-how-setup-bank-statement-service.md).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 2.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bankkontoer**, og velg deretter den relaterte koblingen.
2. Åpne kortet for bankkontoen som du vil eksportere eller importere bankfiler for.
3. Fyll ut feltene på hurtigfanen **Overføring** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Andre fileksporttjenester og formater krever ulike oppsettsverdier på siden **Bankkort**. Du blir informert om feil eller manglende oppsettsverdier når du eksporterer filen. Les derfor de korte beskrivelsene av feltene nøye, eller se relaterte fremgangsmåteemner. Hvis du for eksempel eksporterer en betalingsfil for Nord-Amerika elektronisk pengeoverføring (EFT) krever at både feltene **Nr. for siste remitteringsmelding** og **Transittnr.** er fylt ut. Finn ut mer på [Eksportere betalinger til en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

Feltene i hurtigfanen **Transitt** på bankkontoen dekker ulike formål, avhengig av om betalingen er inngående eller utgående.

Illustrasjonen nedenfor viser ruten for inngående betalinger (numrene i beskrivelsen stemmer med de i illustrasjonen):

:::row:::
    :::column:::

1. Transaksjonene eksporteres fra bankkontoen i et CSV-format som kan leses av mennesker eller i bankens eget format.
2. *Datautvekslingsdefinisjonen* tilordner informasjonen i filen til feltene i [!INCLUDE[prod_short](includes/prod_short.md)]. Finn ut mer under [Definere datautveksling](across-set-up-data-exchange.md)
3. *Oppsettet for dataeksport og -import* definerer eksporten eller importen, og den er koblet til datautvekslingsdefinisjonen.
4. *Importformatet for bankkontoutdrag* kobler importoppsettet til bankkontoen.
5. Betalingene importeres gjennom siden **Betalingsavstemmingskladd** eller **Bankkontoavstemming**.

  :::column-end:::
  :::column:::

        ![Bilde av betalinger mottatt fra banken til bankkonti.](media/Set-Up-Bank-Accounts/payments-in-and-out-1.png)

  :::column-end:::
:::row-end:::

Inngående betalinger importeres alltid gjennom siden for **betalingsavstemmingskladd** eller direkte på siden **Bankkontoavstemming**. Utgående betalinger kan derimot starte fra en hvilken som helst utbetalingskladd. Den eneste forutsetningen er at feltet **Tillat betalingseksport** i den aktuelle utbetalingskladden må velges.

Illustrasjonen nedenfor viser ruten for utgående betalinger (numrene i beskrivelsen stemmer med de i illustrasjonen):

:::row:::
    :::column:::

6. Transaksjonene som er fylt ut i en betalingsjournal, er klargjort for eksport av betalinger til fil.
7. *Importformatet for bankkontoutdrag* kobler importoppsettet til bankkontoen.
8. *Oppsettet for dataeksport og -import* definerer eksporten eller importen, og den er koblet til datautvekslingsdefinisjonen.
9. *Datautvekslingsdefinisjonen* tilordner informasjonen i filen til feltene i [!INCLUDE[prod_short](includes/prod_short.md)]. Finn ut mer under [Definere datautveksling](across-set-up-data-exchange.md)
10. Betalingene eksporteres fra utbetalingskladden og importeres til bankkontoen.

  :::column-end:::
  :::column:::

        ![Bilde av betalinger fra bankkonti som sendes til banken.](media/Set-Up-Bank-Accounts/payments-in-and-out-2.png)

  :::column-end:::
:::row-end:::

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Opprette dine leverandørbankkonti for import eller eksport av bankfilene

Felt i hurtigfanen **Overføring** på siden **Leverandørs bankkort** er relatert til eksport av bankfeeder og filer. Hvis du vil ha mer informasjon, se [Bruke AMC Banking 365 Fundamentals-utvidelsen](ui-extensions-amc-banking.md) og [Eksporter betalinger til en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

[!INCLUDE[purchase-vendor-bank-account](includes/purchase-vendor-bank-account.md)]

## <a name="changing-your-bank-account"></a>Endre bankkontoen

For å bruke en annen bankkonto for bedriften, må du opprette den nye bankkontoen i [!INCLUDE[prod_short](includes/prod_short.md)]. Vi anbefaler at du ikke bare erstatter opplysningene om kontoen du bruker, fordi du kan få uriktige data. Det kan for eksempel hende at åpningssaldoen er feil eller at bankfeeden slutter å virke riktig. Det er viktig at du holder gjeldende og nye konti separat.

Når du har opprettet den nye bankkontoen, må du også opprette en ny bankbokføringsgruppe og tilordne den til en ny finanskonto. Du kan bruke en eksisterende bankbokføringsgruppe på nytt, og banktransaksjoner bokføres på de samme finanskontiene som de andre bankkontiene som deler bankbokføringsgruppen. Vi anbefaler imidlertid at du oppretter en ny bankbokføringsgruppe og finanskonto slik at det blir enklere å foreta avstemminger.

> [!NOTE]
> Husk at bankkontoinformasjonen på åpne salgsfakturaer fortsatt viser den opprinnelige bankkontoen. Det betyr at betalinger fortsatt bokføres til denne kontoen. Vi anbefaler at du lar begge kontoene være aktive i en periode etter endringen.

Hvis du vil ha en mer kompakt visning av kontantkontiene i finansrapportering, kan du bruke fra kontiene **Fra-sum** og **Til-sum** i kontoplanen, radene **Sammentelling** i finansrapporter eller finanskontokategorier. Finn ut mer på [Business Intelligence og Financial Reporting](bi.md).

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/cash-management-dynamics-365-business-central/)

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
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
