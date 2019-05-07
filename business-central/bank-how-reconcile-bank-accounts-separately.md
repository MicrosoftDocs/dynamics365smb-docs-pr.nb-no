---
title: Avstemme bankkonti separat | Microsoft-dokumentasjon
description: Beskriver hvordan lagerverdien avstemmes med finans.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 60b3e0d732125f60b092a0e089cabc2b82ad71ef
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "932035"
---
# <a name="reconcile-bank-accounts-separately"></a>Avstemme bankkonti separat
Hvis du skal avstemme bankkonti i [!INCLUDE[d365fin](includes/d365fin_md.md)] med oppgaver som er mottatt fra banken, begynner du med å fylle ut ruten til venstre på siden **Bankkontoavstemming** med bankoppgaveinformasjon, som du deretter avstemmer med bankkontopostene i den høyre ruten. En effektiv måte å fylle ut bankkontoutdragslinjer på, er å importere en bankkontoutdragsfil eller feed.

> [!NOTE]  
> I nord-amerikanske versjoner kan du også utføre dette arbeidet på **Bankavstemmingsforslag**-siden, som er mer egnet for sjekker og innskudd, men tilbyr ikke import av filer med bankkontoutdrag. Hvis du vil bruke denne siden i stedet for **Bankkontoavstemming**-siden, fjerner du avmerkingen for feltet **Bankavstemming med automatisk samsvar** på siden **Finansoppsett**. Hvis du vil ha mer informasjon, kan du se delen Avstemme bankkontoer under lokal funksjonalitet for USA.

> [!TIP]  
> Du kan også avstemme bankkonti på siden **Betalingsavstemmingskladd**. Alle åpne bankposter relatert til den utlignede kunden- eller leverandørposter lukkes når du velger handlingen **Bokfør betalinger og avstem bankkonto**. Dette betyr at bankkontoen automatisk avstemmes for betalinger du bokfører med kladden. Hvis du vil ha mer informasjon, kan du se [Avstemme betalinger ved hjelp av automatisk utligning](receivables-how-reconcile-payments-auto-application.md).

Hvis du vil aktivere importer av bankkontoutdrag som bankfeeder, må du først konfigurere og aktivere bankfeedtjenesten Envestnet Yodlee og deretter knytte bankkontoene til relaterte nettbankkonti. Hvis du vil ha mer informasjon, kan du se [Konfigurere bankfeedservicen Envestnet Yodlee](bank-how-setup-bank-statement-service.md)

Linjene på siden **Bankkontoavstemming** er delt i to ruter. Ruten **Bankkontoutdragslinjer** viser importerte banktransaksjoner eller poster med utestående betalinger. Ruten **Bankkontoposter** viser postene i bankkontoen.

Aktiviteten med å finne og utligne poster som skal utlignes, kalles *avstemming*. Du kan angi at avstemming skal utføres automatisk, ved å bruke funksjonen **Avstem automatisk**. Du kan eventuelt velge linjer manuelt i begge rutene for å koble hver bankkontoutdragslinje til én eller flere relaterte bankkontoposter, og deretter bruke funksjonen **Avstem manuelt**. Det er merket av for **Utlignet** på linjer der postene som er utlignet.

Du kan fylle ut ruten **Bankkontoutdragslinjer** på siden **Bankkontoavstemming** på følgende måter:

* Automatisk, ved hjelp av funksjonen **Importer bankkontoutdrag** for å fylle ut linjene i henhold til faktiske bankkontoutdrag basert på en fil fra banken.
* Manuelt, ved hjelp av funksjonen **Foreslå linjer**, for å fylle ut linjene med postene for fakturaer som har utestående betalinger.

Når verdien i feltet **Total saldo** i ruten **Bankkontoutdragslinjer** er lik verdien i feltet **Saldo som skal avstemmes** i ruten **Bankkontoposter**, kan du velge handlingen **Bokfør** for å avstemme de utlignede bankkontopostene. Alle bankkontopost som ikke er utlignet forblir på siden, dette angir at betalinger som er behandlet for bankkontoen ikke gjenspeiles i det siste bankkontoutdraget, eller at noen betalinger er mottatt som sjekk.

> [!NOTE]  
>   Hvis bankeoppgavelinjene vedrører sjekkposter, kan du ikke bruke avstemmingsfunksjonene. I stedet må du velge handlingen **Utlign poster** og deretter velge den relevante sjekkposten som bankkontoutdragslinjen skal utlignes mot.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Fylle ut bankavstemmingslinjer ved å importere et bankkontoutdrag
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bankkontoavstemming**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. I feltet **Bankkontonr.** velger du den aktuelle bankkontoen. Bankkontoposter som finnes i å bankkontoen som vises i ruten **Bankkontoposter**.
4. I feltet **Utdragsdato** angir du datoen på utdraget fra banken.
5. I feltet **Utdrag - sluttsaldo** angi du saldoen fra kontoutdraget fra banken.
6. Hvis du har en fil for bankkontoutdrag, velger handlingen **Importer bankkontoutdrag**.
7. Finn filen, og velg deretter **Åpne**-knappen for å importere banktransaksjonene til linjene på siden **Bankkontoavstemming**.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>Fylle ut bankavstemmingslinjer med funksjonen Foreslå linjer
1. På siden **Bankkontoavstemming** velger du handlingen **Foreslå linjer**.
2. I feltet **Startdato** angir du den første bokføringsdatoen postene skal avstemmes for.
3. I feltet **Sluttdato** angir du den siste bokføringsdatoen postene skal avstemmes for.
4. Hvis du vil foreslå sjekkposter i stedet for bankkontoposter, merker du av for **Ta med sjekker**.
5. Velg **OK**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Avstemme bankkontoutdragslinjer med bankkontoposter automatisk
Siden inneholder automatisk samsvarsfunksjonalitet som gjelder betalinger til de relaterte åpne postene, basert på samsvar av tekst på en bankkontoutdragslinje (venstre rute) med tekst på én eller flere bankkontoposter (høyre rute). Merk at du kan overskrive foreslått automatisk bruk, og du kan velge ikke å bruke automatisk bruk i det hele tatt. Hvis du vil ha mer informasjon, kan du se neste fremgangsmåte.

1. På siden **Bankkontoavstemming** velger du handlingen **Avstem automatisk**. Siden **Avstem bankposter** åpnes.
2. I feltet **Toleranse for transaksjonsdato (dager)** angir du antall dager før og etter bankkontopostens bokføringsdato som funksjonen søker innenfor etter samsvarende transaksjonsdatoer i bankkontoutdraget.

    Hvis du skriver inn 0 eller la feltet stå tomt, vil **Avstem automatisk**-funksjonen bare søke etter samsvarende transaksjonsdatoer på bankkontopostens bokføringsdato.
3. Velg **OK**.

    Alle bankkontoutdragslinjer og bankkontoposter som kan avstemmes endres til grønn skrift, og det er merket av for **Utlignet**.
4. Hvis du vil fjerne en avstemming, merker du bankkontoutdragslinjen og deretter velger du handlingen **Fjern avstemming**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Avstemme bankkontoutdragslinjer med bankkontoposter manuelt
1. Velg en ikke-avstemt linje i ruten **Bankkontoutdragslinjer** på siden **Bankkontoavstemming**.
2. I ruten **Bankkontoposter** velger du én eller flere bankkontoposter som kan avstemmes med den valgte bankkontoutdragslinjen. Hvis du vil velge flere linjer, trykker du og holder nede Ctrl-tasten.
3. Velg handlingen **Avstem manuelt**.

    De valgte bankoppgavelinjene og de valgte bankkontopostene endres til grønn skrift, og det er merket av for **Utlignet** i ruten til høyre.
4. Gjenta trinn 1 til 3 for alle bankkontoutdragslinjene som ikke er avstemt.
5. Hvis du vil fjerne en avstemming, merker du bankkontoutdragslinjen og deretter velger du handlingen **Fjern avstemming**.

## <a name="to-create-missing-ledger-entries-to-match-bank-transactions-with"></a>Opprette manglende poster for utligning av banktransaksjoner
Noen ganger inneholder et bankkontoutdrag et rente- eller gebyrbeløp. Slike banktransaksjoner kan ikke utlignes fordi det ikke finnes noen relaterte poster i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du må deretter bokfører en kladdelinje for hver transaksjon for å opprette en relatert post som den kan utlignes mot.

1. På siden **Bankkontoavstemming** velger du handlingen **Overfør til finanskladd**.  
2. På siden **Overfør bankavst. til finans** angir du hvilken finanskladd du vil bruke, og velger deretter **OK**-knappen.

    Siden **Finanskladd** åpnes, som inneholder nye kladdelinjer for bankerkontoutdragslinjer med manglende poster.
3. Fyll ut kladdelinjen med relevant informasjon, for eksempel motkonto. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).  
4. Hvis du vil se resultatet av bokføringen før du bokfører, kan du velge **Kontrollrapport**-handlingen. **Bankkontoutdrag**-rapporten åpnes, og viser de samme feltene som ved overskriften i **Bankkontoavstemming**-siden.
4. Velg handlingen **Bokfør**.

    Når posten er bokført, utligner du bankkontoutdragstransaksjonen mot den.
5. Oppdater eller åpne siden **Bankkontoavstemming**. Den nye posten vises i ruten **Bankkontoposter**.
6. Utligne bankkontoutdragslinjen med bankkontopost, enten manuelt eller automatisk.

## <a name="see-also"></a>Se også
[Håndtere bankkonti](bank-manage-bank-accounts.md)  
[Konfigurere banktjenester](bank-setup-banking.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
