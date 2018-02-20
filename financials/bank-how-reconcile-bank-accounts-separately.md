---
title: Avstemme bankkonti separat | Microsoft-dokumentasjon
description: Beskriver hvordan lagerverdien avstemmes med finans.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: fa1225e8467ab805fc14afdd39eef556dc7ad5fc
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---
# <a name="reconcile-bank-accounts-separately"></a>Avstemme bankkonti separat
Hvis du vil avstemme bankkonti i [!INCLUDE[d365fin](includes/d365fin_md.md)] med oppgaver som er mottatt fra banken, må du fylle ut linjene i vinduet **Bankkontoavstemming**.

> [!NOTE]  
>   Du kan også avstemme bankkonti i vinduet **Betalingsavstemmingskladd**. Alle åpne bankposter relatert til den utlignede kunden- eller leverandørposter lukkes når du velger handlingen **Bokfør betalinger og avstem bankkonto**. Dette betyr at bankkontoen automatisk avstemmes for betalinger du bokfører med kladden. Hvis du vil ha mer informasjon, kan du se [Avstemme betalinger ved hjelp av automatisk utligning](receivables-how-reconcile-payments-auto-application.md).

Hvis du vil aktivere importer av bankkontoutdrag som bankfeeder, må du først konfigurere og aktivere bankfeedtjenesten Envestnet Yodlee og deretter knytte bankkontoene til relaterte nettbankkonti. Hvis du vil ha mer informasjon, kan du se [Konfigurere bankfeedservicen Envestnet Yodlee](bank-how-setup-bank-statement-service.md)

Linjene i vinduet **Bankkontoavstemming** er delt i to ruter. Ruten **Bankkontoutdragslinjer** viser importerte banktransaksjoner eller poster med utestående betalinger. Ruten **Bankkontoposter** viser postene i bankkontoen.

Aktiviteten med å finne og utligne poster som skal utlignes, kalles *avstemming*. Du kan angi at avstemming skal utføres automatisk, ved å bruke funksjonen **Avstem automatisk**. Du kan eventuelt velge linjer manuelt i begge rutene for å koble hver bankkontoutdragslinje til én eller flere relaterte bankkontoposter, og deretter bruke funksjonen **Avstem manuelt**. Det er merket av for **Utlignet** på linjer der postene som er utlignet.

Du kan fylle ut ruten **Bankkontoutdragslinjer** i vinduet **Bankkontoavstemming** på følgende måter:

* Automatisk, ved hjelp av funksjonen **Importer bankkontoutdrag** for å fylle ut linjene i henhold til faktiske bankkontoutdrag basert på en fil fra banken.
* Manuelt, ved hjelp av funksjonen **Foreslå linjer**, for å fylle ut linjene med postene for fakturaer som har utestående betalinger.

Når verdien i feltet **Total saldo** i ruten **Bankkontoutdragslinjer** er lik verdien i feltet **Saldo som skal avstemmes** i ruten **Bankkontoposter**, kan du velge handlingen **Bokfør** for å avstemme de utlignede bankkontopostene. Alle bankkontopost som ikke er utlignet forblir i vinduet, dette angir at betalinger som er behandlet for bankkontoen ikke gjenspeiles i det siste bankkontoutdraget, eller at noen betalinger er mottatt som sjekk.

> [!NOTE]  
>   Hvis bankeoppgavelinjene vedrører sjekkposter, kan du ikke bruke avstemmingsfunksjonene. I stedet må du velge handlingen **Utlign poster** og deretter velge den relevante sjekkposten som bankkontoutdragslinjen skal utlignes mot.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Fylle ut bankavstemmingslinjer ved å importere et bankkontoutdrag
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Bankkontoavstemming**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. I feltet **Bankkontonr.** velger du den aktuelle bankkontoen. Bankkontoposter som finnes i å bankkontoen som vises i ruten **Bankkontoposter**.
4. I feltet **Utdragsdato** angir du datoen på utdraget fra banken.
5. I feltet **Utdrag - sluttsaldo** angi du saldoen fra kontoutdraget fra banken.
6. Hvis du har en fil for bankkontoutdrag, velger handlingen **Importer bankkontoutdrag**.
7. Finn filen, og velg deretter **Åpne**-nappen for å importere banktransaksjonene til linjene i vinduet **Bankkontoavstemming**.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>Fylle ut bankavstemmingslinjer med funksjonen Foreslå linjer
1. I vinduet **Bankkontoavstemming** velger du handlingen **Foreslå linjer**.
2. I feltet **Startdato** angir du den første bokføringsdatoen postene skal avstemmes for.
3. I feltet **Sluttdato** angir du den siste bokføringsdatoen postene skal avstemmes for.
4. Hvis du vil foreslå sjekkposter i stedet for bankkontoposter, merker du av for **Ta med sjekker**.
5. Velg **OK**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Avstemme bankkontoutdragslinjer med bankkontoposter automatisk
1. I vinduet **Bankkontoavstemming** velger du handlingen **Avstem automatisk**. Vinduet **Avstem bankposter** åpnes.
2. I feltet **Toleranse for transaksjonsdato (dager)** angir du antall dager før og etter bankkontopostens bokføringsdato som funksjonen søker innenfor etter samsvarende transaksjonsdatoer i bankkontoutdraget.

    Hvis du skriver inn 0 eller la feltet stå tomt, vil **Avstem automatisk**-funksjonen bare søke etter samsvarende transaksjonsdatoer på bankkontopostens bokføringsdato.
3. Velg **OK**.

    Alle bankkontoutdragslinjer og bankkontoposter som kan avstemmes endres til grønn skrift, og det er merket av for **Utlignet**.
4. Hvis du vil fjerne en avstemming, merker du bankkontoutdragslinjen og deretter velger du handlingen **Fjern avstemming**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Avstemme bankkontoutdragslinjer med bankkontoposter manuelt
1. Velg en ikke-avstemt linje i ruten **Bankkontoutdragslinjer** i vinduet **Bankkontoavstemming**.
2. I ruten **Bankkontoposter** velger du én eller flere bankkontoposter som kan avstemmes med den valgte bankkontoutdragslinjen. Hvis du vil velge flere linjer, trykker du og holder nede Ctrl-tasten.
3. Velg handlingen **Avstem manuelt**.

    De valgte bankoppgavelinjene og de valgte bankkontopostene endres til grønn skrift, og det er merket av for **Utlignet** i ruten til høyre.
4. Gjenta trinn 1 til 3 for alle bankkontoutdragslinjene som ikke er avstemt.
5. Hvis du vil fjerne en avstemming, merker du bankkontoutdragslinjen og deretter velger du handlingen **Fjern avstemming**.

## <a name="to-create-missing-ledger-entries-to-match-bank-transactions-with"></a>Opprette manglende poster for utligning av banktransaksjoner
Noen ganger inneholder et bankkontoutdrag et rente- eller gebyrbeløp. Slike banktransaksjoner kan ikke utlignes fordi det ikke finnes noen relaterte poster i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du må deretter bokfører en kladdelinje for hver transaksjon for å opprette en relatert post som den kan utlignes mot.

1. I vinduet **Bankkontoavstemming** velger du handlingen **Overfør til finanskladd**.  
2. I vinduet **Overfør bankavst. til finans** angir du hvilken finanskladd du vil bruke, og velger deretter **OK**-knappen.

    Vinduet **Finanskladd** åpnes, som inneholder nye kladdelinjer for bankerkontoutdragslinjer med manglende poster.
3. Fyll ut kladdelinjen med relevant informasjon, for eksempel motkonto. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).  
4. Velg handlingen **Bokfør**.

    Når posten er bokført, utligner du bankkontoutdragstransaksjonen mot den.
5. Oppdater eller åpne vinduet **Bankkontoavstemming**. Den nye posten vises i ruten **Bankkontoposter**.
6. Utligne bankkontoutdragslinjen med bankkontopost, enten manuelt eller automatisk.

## <a name="see-also"></a>Se også
[Håndtere bankkonti](bank-manage-bank-accounts.md)  
[Konfigurere banktjenester](bank-setup-banking.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

