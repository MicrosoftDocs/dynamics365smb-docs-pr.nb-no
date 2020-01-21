---
title: Avstemme bankkontoer | Microsoft Docs
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
ms.date: 01/13/2020
ms.author: sgroespe
ms.openlocfilehash: 4d3656c81a6964a01632865b6163be9ec0365de8
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/14/2020
ms.locfileid: "2952797"
---
# <a name="reconcile-bank-accounts"></a>Avstemme bankkontoer
Du utfører bankavstemming for å sikre at de ulike forretningstransaksjonene og utgiftene gjenspeiles riktig i selskapstablåene. Dette gjør du ved å sammenligne og utligne poster i de interne bankkontoene med banktransaksjoner i banken, og deretter bokføre saldoene på de interne bankkontoene for å gjøre totaler tilgjengelige for finansledere. Bankavstemming er også en praktisk måte å oppdage og løse manglende betalinger og bokføringsfeil.

Følgende beskriver hvordan du utfører bankavstemming med siden **Bankkontoavstemming**.

> [!TIP]
> Du kan avstemme bankkontoer på siden **Betalingsavstemmingskladd** i forbindelse med betalingsbehandling. Alle åpne bankposter relatert til den utlignede kunden- eller leverandørposter lukkes når du velger handlingen **Bokfør betalinger og avstem bankkonto**. Dette betyr at bankkontoen automatisk avstemmes for betalinger du bokfører med kladden. Hvis du vil ha mer informasjon, kan du se [Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> I nord-amerikanske versjoner kan du også utføre dette arbeidet på **Bankavstemmingsforslag**-siden, som er mer egnet for sjekker og innskudd, men tilbyr ikke import av filer med bankkontoutdrag. Hvis du vil bruke denne siden i stedet for **Bankkontoavstemming**-siden, fjerner du avmerkingen for feltet **Bankavstemming med automatisk samsvar** på siden **Finansoppsett**. Hvis du vil ha mer informasjon, kan du se delen Avstemme bankkontoer under lokal funksjonalitet for USA.

Linjene på siden **Bankkontoavstemming** er delt i to ruter. Ruten **Bankkontoutdragslinjer** viser importerte banktransaksjoner eller poster med utestående betalinger. Ruten **Bankkontoposter** viser postene i den interne bankkontoen.

Aktiviteten med å avstemme banktransaksjoner med interne bankposter refereres til som *samsvarende*. Du kan angi at avstemming skal utføres automatisk, ved å bruke funksjonen **Avstem automatisk**. Du kan eventuelt velge linjer manuelt i begge rutene for å koble hver bankkontoutdragslinje til én eller flere relaterte bankkontoposter, og deretter bruke funksjonen **Avstem manuelt**. Det er merket av for **Utlignet** på linjer der postene som er utlignet. Hvis du vil ha mer informasjon, kan du se [Definere regler for automatisk utligning av betalinger](receivables-how-set-up-payment-application-rules.md).

> [!NOTE]  
> Hvis bankeoppgavelinjene vedrører sjekkposter, kan du ikke bruke avstemmingsfunksjonene. I stedet må du velge handlingen **Utlign poster** og deretter velge den relevante sjekkposten som bankkontoutdragslinjen skal utlignes mot.

Når verdien i feltet **Total saldo** i ruten **Bankkontoutdragslinjer** er lik verdien i feltet **Saldo som skal avstemmes** i ruten **Bankkontoposter**, kan du velge handlingen **Bokfør**. Alle bankkontoposter som ikke samsvarer, blir værende på siden, noe som angir avvik som du må løse for å avstemme bankkontoen.

Alle linjer som ikke kan sammenlignes, angitt med en verdi i **Differanse**-feltet, blir værende på siden **Bankkontoavstemming** etter bokføring. De representerer en form for avvik som du må løse før du kan fullføre bankkontoavstemmingen. Typiske forretningssituasjoner som kan forårsake forskjeller:

|Differanse|Årsak|Løsning|
|-|-|
|En transaksjon i den interne bankkontoen er ikke på bankkontoutdraget.|Banktransaksjonen inntraff ikke, selv om det ble gjort en bokføring i [!INCLUDE[d365fin](includes/d365fin_md.md)].|Utfør den manglende pengetransaksjonen (eller be en debitor om å utføre den), og importer deretter bankkontoutdragsfilen eller angi transaksjonen manuelt.|
|En transaksjon på bankkontoutdraget finnes ikke som et bilag eller en kladdelinje i [!INCLUDE[d365fin](includes/d365fin_md.md)].|En banktransaksjon ble foretatt uten en tilsvarende bokføring i [!INCLUDE[d365fin](includes/d365fin_md.md)], for eksempel en kladdelinjebokføring for en utgift.|Opprett og bokfør den manglende oppføringen. Hvis du vil ha informasjon om hvordan du raskt kan starte dette, kan du se [Opprette manglende poster for utligning av banktransaksjoner](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines-with).|
|En transaksjon i den interne bankkontoen tilsvarer en banktransaksjon, men noe informasjon er for forskjellig for å utgjøre et samsvar.|Informasjon, for eksempel beløpet eller kundenavnet, ble skrevet inn på en annen måte i forbindelse med banktransaksjonen eller den interne posteringen.|Se gjennom informasjonen, og samsvar de to deretter manuelt. Du kan eventuelt korrigere informasjonen som ikke samsvarer.||

Du må løse forskjellene, for eksempel ved å opprette manglende poster og korrigere ikke-samsvarende informasjon, eller ved å utføre transaksjoner som mangler penger, til bankkontoavstemmingen er fullført og postert.

Du kan fylle ut ruten **Bankkontoutdragslinjer** på siden **Bankkontoavstemming** på følgende måter:

* Automatisk, ved hjelp av funksjonen **Importer bankkontoutdrag** for å fylle ut ruten **Bankkontoutdragslinjer** med banktransaksjoner i henhold til en importert fil eller strøm oppgitt av banken.
* Manuelt, ved hjelp av funksjonen **Foreslå linjer**, for å fulle ut ruten **Bankkontoutdragslinjer** i henhold til fakturaer i [!INCLUDE[d365fin](includes/d365fin_md.md)] som har utestående betalinger.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Fylle ut bankavstemmingslinjer ved å importere et bankkontoutdrag
Ruten **Bankkontoutdragslinjer** fylles ut med banktransaksjoner i henhold til en importert fil eller strøm fra banken.

Hvis du vil aktivere importer av bankkontoutdrag som bankfeeder, må du først konfigurere og aktivere tjenesten Envestnet Yodlee Bank Feeds og deretter knytte bankkontoene til relaterte nettbankkonti. Hvis du vil ha mer informasjon, kan du se [Konfigurere Envestnet Yodlee Bank Feeds-tjenesten](bank-how-setup-bank-statement-service.md).

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bankkontoavstemming**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. I feltet **Bankkontonr.** velger du den aktuelle bankkontoen. Bankkontoposter som finnes i å bankkontoen som vises i ruten **Bankkontoposter**.
4. I feltet **Utdragsdato** angir du datoen på utdraget fra banken.
5. I feltet **Utdrag - sluttsaldo** angi du saldoen fra kontoutdraget fra banken.
6. Hvis du har en fil for bankkontoutdrag, velger handlingen **Importer bankkontoutdrag**.
7. Finn filen, og velg deretter **Åpne**-knappen for å importere banktransaksjonene til ruten **Bankkontoutdragslinjer** på siden **Bankkontoavstemming**.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>Fylle ut bankavstemmingslinjer med funksjonen Foreslå linjer
Ruten **Bankkontoutdragslinjer** fylles ut i henhold til fakturaer i [!INCLUDE[d365fin](includes/d365fin_md.md)] som har utestående betalinger.  
1. På siden **Bankkontoavstemming** velger du handlingen **Foreslå linjer**.
2. I feltet **Startdato** angir du den første bokføringsdatoen postene skal avstemmes for.
3. I feltet **Sluttdato** angir du den siste bokføringsdatoen postene skal avstemmes for.
4. Hvis du vil foreslå sjekkposter i stedet for bankkontoposter, merker du av for **Ta med sjekker**.
5. Velg **OK**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Avstemme bankkontoutdragslinjer med bankkontoposter automatisk
Siden **Bankkontoavstemming** inneholder automatisk samsvarsfunksjonalitet basert på samsvar av tekst på en bankkontoutdragslinje (venstre rute) med tekst på én eller flere bankkontoposter (høyre rute). Merk at du kan overskrive foreslått automatisk samsvar, og du kan velge ikke å bruke automatisk samsvar i det hele tatt. Hvis du vil ha mer informasjon, kan du se [Avstemme bankkontoutdragslinjer med bankkontoposter manuelt](bank-how-reconcile-bank-accounts-separately.md#to-match-bank-statement-lines-with-bank-account-ledger-entries-manually).

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

## <a name="to-create-missing-ledger-entries-to-match-bank-statement-lines-with"></a>Opprette manglende poster for utligning av bankkontoutdragslinjer med
Noen ganger inneholder et bankkontoutdrag et rente- eller gebyrbeløp. Slike bankkontoutdragslinjer kan ikke utlignes fordi det ikke finnes noen relaterte poster i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du må deretter bokfører en kladdelinje for hver transaksjon for å opprette en relatert post som den kan utlignes mot.

1. På siden **Bankkontoavstemming** velger du handlingen **Overfør til finanskladd**.  
2. På siden **Overfør bankavst. til finans** angir du hvilken finanskladd du vil bruke, og velger deretter **OK**-knappen.

    Siden **Finanskladd** åpnes, som inneholder nye kladdelinjer for bankerkontoutdragslinjer med manglende poster.
3. Fyll ut kladdelinjen med relevant informasjon, for eksempel motkonto. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).  
4. Hvis du vil se resultatet av bokføringen før du bokfører, kan du velge **Kontrollrapport**-handlingen. **Bankkontoutdrag**-rapporten åpnes, og viser de samme feltene som ved overskriften i **Bankkontoavstemming**-siden.
4. Velg handlingen **Bokfør**.

    Når posten er bokført, utligner du bankkontoutdragslinjen mot den.
5. Oppdater eller åpne siden **Bankkontoavstemming**. Den nye posten vises i ruten **Bankkontoposter**.
6. Utligne bankkontoutdragslinjen med bankkontopost, enten manuelt eller automatisk.

## <a name="see-related-training-at-microsoft-learnlearnmodulesbank-reconciliation-dynamics-365-business-centralindex"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/bank-reconciliation-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også
[Avstemme bankkonter](bank-manage-bank-accounts.md)  
[Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Konfigurere banktjenester](bank-setup-banking.md)  
[Definere regler for automatisk utligning av betalinger](receivables-how-set-up-payment-application-rules.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
