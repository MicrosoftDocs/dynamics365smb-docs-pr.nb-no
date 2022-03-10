---
title: Avstemme bankkontoer
description: Dette emnet beskriver hvordan du avstemmer transaksjonene i de interne bankkontiene med transaksjonene i kontoutdrag fra banken.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.search.form: 379, 388, 1290, 10124
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: 89fc1b881ce738d50ae40088be265d3944491f21
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8129002"
---
# <a name="reconcile-bank-accounts"></a>Avstemme bankkontoer

Du utfører bankavstemming for å sikre at de ulike forretningstransaksjonene og utgiftene gjenspeiles riktig i selskapstablåene. Dette gjør du ved å sammenligne og utligne poster i de interne bankkontoene med banktransaksjoner i banken, og deretter bokføre saldoene på de interne bankkontoene for å gjøre totaler tilgjengelige for finansledere. Bankavstemming er også en praktisk måte å oppdage og løse manglende betalinger og bokføringsfeil.

Følgende beskriver hvordan du utfører bankavstemming med siden **Bankkontoavstemming**.

> [!TIP]
> Du kan avstemme bankkontoer på siden **Betalingsavstemmingskladd** når du behandler betalinger. Alle åpne bankposter relatert til den utlignede kunden- eller leverandørposter lukkes når du velger handlingen **Bokfør betalinger og avstem bankkonto**. Dette avstemmer automatisk bankkontoen for betalinger du bokfører med kladden. Hvis du vil ha mer informasjon, kan du se [Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> I nord-amerikanske versjoner kan du også utføre dette arbeidet på **Bankavstemmingsforslag**-siden, som er mer egnet for sjekker og innskudd, men tilbyr ikke import av filer med bankkontoutdrag. Hvis du vil bruke denne siden i stedet for **Bankkontoavstemming**-siden, fjerner du feltet **Bankavstemming med automatisk samsvar** på siden **Finansoppsett**. Hvis du vil ha mer informasjon, kan du se delen [Avstemme bankkontoer](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) under lokal funksjonalitet for USA.

Linjene på siden **Bankkontoavstemming** er delt i to ruter. Ruten **Bankkontoutdragslinjer** viser importerte banktransaksjoner eller poster med utestående betalinger. Ruten **Bankkontoposter** viser postene i den interne bankkontoen.

Avstemming av banktransaksjoner med interne bankposter refereres til som *samsvarende*. Du kan angi at avstemming skal utføres automatisk, ved å bruke funksjonen **Avstem automatisk**. Du kan eventuelt velge linjer manuelt i begge rutene for å koble hver bankkontoutdragslinje til én eller flere relaterte bankkontoposter, og deretter bruke funksjonen **Avstem manuelt**. Det er merket av for **Utlignet** på linjer der postene som er utlignet. Hvis du vil ha mer informasjon, kan du se [Definere regler for automatisk utligning av betalinger](receivables-how-set-up-payment-application-rules.md).

> [!NOTE]  
> Hvis bankeoppgavelinjene vedrører sjekkposter, kan du ikke bruke avstemmingsfunksjonene. I stedet må du velge handlingen **Utlign poster** og deretter velge den relevante sjekkposten som bankkontoutdragslinjen skal utlignes mot.

Når verdien i feltet **Total saldo** i ruten **Bankkontoutdragslinjer** er lik totalverdien i feltet **Saldo som skal avstemmes** pluss feltet **Saldo ved forrige utdrag** i ruten **Bankkontoposter**, kan du velge handlingen **Bokfør**. Bankkontoposter som ikke samsvarer, blir værende på siden, som angir avvik du må løse for å avstemme bankkontoen.

Alle linjer som ikke kan sammenlignes, angitt med en verdi i **Differanse**-feltet, blir værende på siden **Bankkontoavstemming** etter bokføring. De representerer en form for avvik som du må løse før du kan fullføre bankkontoavstemmingen. Typiske forretningssituasjoner som kan forårsake forskjeller:

| Differanse | Årsak | Løsning |
|------------|--------|------------|
| En transaksjon i den interne bankkontoen er ikke på bankkontoutdraget. | Banktransaksjonen inntraff ikke, selv om det ble gjort en bokføring i [!INCLUDE[prod_short](includes/prod_short.md)]. | Utfør den manglende pengetransaksjonen (eller be en debitor om å utføre den), og importer deretter bankkontoutdragsfilen eller angi transaksjonen manuelt. |
| En transaksjon på bankkontoutdraget finnes ikke som et bilag eller en kladdelinje i [!INCLUDE[prod_short](includes/prod_short.md)]. | En banktransaksjon ble foretatt uten en tilsvarende bokføring i [!INCLUDE[prod_short](includes/prod_short.md)], for eksempel en kladdelinjebokføring for en utgift. | Opprett og bokfør den manglende oppføringen. Hvis du vil ha informasjon om hvordan du raskt kan starte dette, kan du se [Opprette manglende poster for utligning av banktransaksjoner](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines-with). |
| En transaksjon i den interne bankkontoen tilsvarer en banktransaksjon, men noe informasjon er for forskjellig for å utgjøre et samsvar. | Informasjon, for eksempel beløpet eller kundenavnet, ble skrevet inn på en annen måte i forbindelse med banktransaksjonen eller den interne posteringen. | Se gjennom informasjonen, og samsvar de to deretter manuelt. Du kan eventuelt korrigere informasjonen som ikke samsvarer. |

Du må løse forskjellene, for eksempel ved å opprette manglende poster og korrigere ikke-samsvarende informasjon, eller ved å utføre transaksjoner som mangler penger, til bankkontoavstemmingen er fullført og postert.

Du kan fylle ut ruten **Bankkontoutdragslinjer** på siden **Bankkontoavstemming** på følgende måter:

* Automatisk, ved hjelp av funksjonen **Importer bankkontoutdrag** for å fylle ut ruten **Bankkontoutdragslinjer** med banktransaksjoner i henhold til en importert fil eller strøm oppgitt av banken.
* Manuelt, ved hjelp av funksjonen **Foreslå linjer**, for å fulle ut ruten **Bankkontoutdragslinjer** i henhold til fakturaer i [!INCLUDE[prod_short](includes/prod_short.md)] som har utestående betalinger.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Fylle ut bankavstemmingslinjer ved å importere et bankkontoutdrag

Ruten **Bankkontoutdragslinjer** fylles ut med banktransaksjoner i henhold til en importert fil eller strøm fra banken.

Hvis du vil aktivere importer av bankkontoutdrag som bankfeeder, må du først konfigurere og aktivere tjenesten Envestnet Yodlee Bank Feeds og deretter knytte bankkontoene til relaterte nettbankkonti. Hvis du vil ha mer informasjon, kan du se [Konfigurere Envestnet Yodlee Bank Feeds-tjenesten](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> Du kan også importere bankkontoutdragsfiler i komma- eller semikolondelt format (.CSV). Bruk veiviseren **Definer et filformat for bankkontoutdrag** for assistert installasjon til å definere importformater for bankkontoutdrag og knytte formatet til en bankkonto. Du kan deretter bruke disse formatene når du importerer bankkontoutdrag på siden **Bankkontoavstemming**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") angi **Bankkontoavstemming**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. I feltet **Bankkontonr.** velger du den aktuelle bankkontoen. Bankkontoposter som finnes i å bankkontoen som vises i ruten **Bankkontoposter**.
4. I feltet **Utdragsdato** angir du datoen på utdraget fra banken.
5. I feltet **Utdrag - sluttsaldo** angi du saldoen fra kontoutdraget fra banken.
6. Hvis du har en fil for bankkontoutdrag, velger handlingen **Importer bankkontoutdrag**.
7. Finn filen, og velg deretter **Åpne**-knappen for å importere banktransaksjonene til ruten **Bankkontoutdragslinjer** på siden **Bankkontoavstemming**.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>Fylle ut bankavstemmingslinjer med funksjonen Foreslå linjer

Ruten **Bankkontoutdragslinjer** fylles ut i henhold til fakturaer i [!INCLUDE[prod_short](includes/prod_short.md)] som har utestående betalinger.  

1. På siden **Bankkontoavstemming** velger du handlingen **Foreslå linjer**.
2. I feltet **Startdato** angir du den første bokføringsdatoen postene skal avstemmes for.
3. I feltet **Sluttdato** angir du den siste bokføringsdatoen postene skal avstemmes for.

> [!NOTE]
> Vanligvis vil sluttdatoen være lik den datoen som er angitt i feltet **Utdragsdato**. Hvis du imidlertid vil avstemme transaksjoner bare for en del av en periode, kan du angi en annen sluttdato. 

1. Hvis du vil foreslå sjekkposter i stedet for bankkontoposter, merker du av for **Ta med sjekker**.
1. Velg **OK**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Avstemme bankkontoutdragslinjer med bankkontoposter automatisk

Siden **Bankkontoavstemming** inneholder automatisk samsvarsfunksjonalitet basert på samsvar av tekst på en bankkontoutdragslinje (venstre rute) med tekst på én eller flere bankkontoposter (høyre rute). Merk at du kan overskrive foreslått automatisk samsvar, og du kan velge ikke å bruke automatisk samsvar i det hele tatt. Hvis du vil ha mer informasjon, kan du se [Avstemme bankkontoutdragslinjer med bankkontoposter manuelt](bank-how-reconcile-bank-accounts-separately.md#to-match-bank-statement-lines-with-bank-account-ledger-entries-manually).

Automatisk avstemming avstemmer oppføringer basert på et sett med regler for betalingsprogram. Hvis du vil ha mer informasjon, kan du se [Definere regler for automatisk utligning av betalinger](receivables-how-set-up-payment-application-rules.md). Du kan undersøke grunnlaget for avstemming ved å bruke handlingen **Avstemmingsdetaljer**. Detaljene vil for eksempel omfatte navnene på feltene som inneholder samsvarende verdier.  

1. På siden **Bankkontoavstemming** velger du handlingen **Avstem automatisk**. Siden **Avstem bankposter** åpnes.
2. I feltet **Toleranse for transaksjonsdato (dager)** angir du antall dager før og etter bankkontopostens bokføringsdato som funksjonen søker innenfor etter samsvarende transaksjonsdatoer i bankkontoutdraget.

    Hvis du skriver inn 0 eller la feltet stå tomt, vil **Avstem automatisk**-handlingen bare søke etter samsvarende transaksjonsdatoer på bankkontopostens bokføringsdato.
3. Velg **OK**.

    Alle bankkontoutdragslinjer og bankkontoposter som kan avstemmes endres til grønn skrift, og det er merket av for **Utlignet**.
4. Hvis du vil fjerne en avstemming, merker du bankkontoutdragslinjen og deretter velger du handlingen **Fjern avstemming**.

> [!TIP]
> Du kan bruke en blanding av manuell og automatisk avstemming. Hvis du har avstemt poster manuelt, vil ikke automatisk avstemming overskrive valgene dine. 

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Avstemme bankkontoutdragslinjer med bankkontoposter manuelt
1. Velg en ikke-avstemt linje i ruten **Bankkontoutdragslinjer** på siden **Bankkontoavstemming**.
2. I ruten **Bankkontoposter** velger du én eller flere bankkontoposter som kan avstemmes med den valgte bankkontoutdragslinjen. Hvis du vil velge flere linjer, trykker du og holder nede Ctrl-tasten.

   > [!TIP]
   > Du kan også manuelt tilordne flere bankkontoutdragslinjer til én bankkontopost. Dette kan for eksempel være nyttig hvis bankbeløpet inneholder flere betalingsmåter, for eksempel kredittkort fra ulike utstedere, og banken viser de som separate linjer. 
3. Velg handlingen **Avstem manuelt**.

    De valgte bankoppgavelinjene og de valgte bankkontopostene endres til grønn skrift, og det er merket av for **Utlignet** i ruten til høyre.
4. Gjenta trinn 1 til 3 for alle bankkontoutdragslinjene som ikke er avstemt.

> [!TIP]
> Hvis du vil fjerne en avstemming, merker du bankkontoutdragslinjen og deretter velger du handlingen **Fjern avstemming**. Hvis du har tilordnet flere bankkontoutdragslinjer til en post og du må fjerne en eller flere av avstemte linjer, fjernes alle de manuelle postene for posten når du velger **Fjern avstemming**. 

## <a name="to-create-missing-ledger-entries-to-match-bank-statement-lines-with"></a>Opprette manglende poster for utligning av bankkontoutdragslinjer med

Noen ganger inneholder et bankkontoutdrag et rente- eller gebyrbeløp. Slike bankkontoutdragslinjer kan ikke utlignes fordi det ikke finnes noen relaterte poster i [!INCLUDE[prod_short](includes/prod_short.md)]. Du må deretter bokfører en kladdelinje for hver transaksjon for å opprette en relatert post som den kan utlignes mot.

1. På siden **Bankkontoavstemming** velger du handlingen **Overfør til finanskladd**.  
2. På siden **Overfør bankavst. til finans** angir du hvilken finanskladd du vil bruke, og velger deretter **OK**-knappen.

    Siden **Finanskladd** åpnes, som inneholder nye kladdelinjer for bankerkontoutdragslinjer med manglende poster.
3. Fyll ut kladdelinjen med relevant informasjon, for eksempel motkonto. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).  
4. Hvis du vil se resultatet av bokføringen før du bokfører, kan du velge **Kontrollrapport**-handlingen. **Bankkontoutdrag**-rapporten åpnes, og viser de samme feltene som ved overskriften i **Bankkontoavstemming**-siden.
5. Velg handlingen **Bokfør**.

    Når posten er bokført, utligner du bankkontoutdragslinjen mot den.
6. Oppdater eller åpne siden **Bankkontoavstemming**. Den nye posten vises i ruten **Bankkontoposter**.
7. Utligne bankkontoutdragslinjen med bankkontopost, enten manuelt eller automatisk.

## <a name="undo-a-bank-account-reconciliation"></a>Angre en bankkontoavstemming
Hvis du oppdager en feil i en bokført bankavstemming, kan du ved hjelp av **Angre**- handlingen på **Bankkontoutdrag**-siden rette opp feilen. Når du angrer en bokført bankavstemming, flyttes postene til **Bankavstemming**-siden og merkes som **Åpne**, og det betyr at de ikke er avstemt. Deretter kan du korrigere bankavstemmingen og bokføre den på nytt.

> [!NOTE]
> Hvis du vil bruke Angre-funksjonen for bokførte bankavstemminger og bankkontoutdrag i Nord-Amerika, må du aktivere **Bankavstemming med automatisk samsvar** på **Finansoppsett**-siden. Angre-funksjonen er ikke tilgjengelig for bankkontoutdrag som er bokført fra bankavstemmingsforslag.

### <a name="reusing-the-bank-statement-number"></a>Bruke bankkontoutdragsnummeret på nytt
Bankkontoutdragsnummeret som brukes for den nye bankavstemmingen, hentes fra bankkontoen, som er Saldo ved forrige utdrag. Du kan endre disse verdiene før du starter en ny bankavstemming. Når du oppretter en ny bankavstemming, kontrollerer imidlertid [!INCLUDE[d365fin](includes/d365fin_md.md)] om utdragsnummeret allerede er tilordnet et bokført bankkontoutdrag. Hvis nummeret er i bruk, men du vil at det nye bankkontoutdraget skal bruke det i stedet, kan du bruke handlingen **Endre utdragsnummer** på siden **Bankkontoavstemming**.

### <a name="examples"></a>Eksempler
Nedenfor følger noen få eksempler på hvordan du kan rette opp en feil i en bokført bankavstemming med eller uten å bruke det samme kontoutdragsnummeret.

#### <a name="example-1"></a>Eksempel 1
Du gjorde bankavstemminger for januar, februar og mars. Bankkontoutdragsnummeret er 100 for mars. Senere oppdager du at mars bare tok med poster frem til 30. Dette betyr at det mangler poster for 31. Du må derfor gjøre om bankavstemmingen for mars. I dette tilfellet åpner du siden **Bankkontoutdrag**, velger utdraget for mars, og deretter velger du **Angre**. 

Den nye bankavstemmingen får kontoutdragsnummer 101. Hvis du vil tilordne nummeret 100 på nytt, velger du **Endre utdragsnummer** og angir **100**. 

> [!TIP]
> Husk å angi den aktuelle sluttdatoen for utdraget (i dette eksemplet er det 31. mars), og rediger feltet **Saldo ved forrige utdrag**. 

#### <a name="example-2"></a>Eksempel 2
Du gjorde bankavstemminger for januar, februar, juni og juli. Du oppdager at februar var feil. La oss anta at den har utdragsnummer 100. Som i eksempel 1 bruker du handlingene Angre og Endre utdragsnummer til å endre kontoutdragsnummeret, som i eksempel 1 ovenfor, og du kan nå gjøre om bankavstemmingen for februar.  

Når du har bokført den korrigerte bankavstemmingen for februar, på det tilhørende bankkontokortet, viser feltet **Siste kontoutdragsnr.** **100**, og feltet **Saldo ved forrige utdrag** viser sluttsaldoen for februar-utdraget. 

Hvis den neste bankavstemmingen gjelder mars, tilordner [!INCLUDE[d365fin](includes/d365fin_md.md)] 101 som utdragsnummer og gir den riktig **Saldo ved forrige utdrag**.

Hvis den neste bankavstemmingen er for august, kan du vurdere å endre verdiene i feltene **Siste kontoutdragsnr.** og **Saldo ved forrige utdrag** på kortet **Bankkonto** før du oppretter den neste bankavstemmingen, eller bruke handlingen Endre utdragsnummer og endre verdien i feltet Saldo ved forrige utdrag på bankavstemmingssiden.

> [!NOTE]
> Kontoutdragsnummeret er viktig når du gjør bankavstemminger med importerte CAMT-filer som inneholder kontoutdragsnumre, eller når du avstemmer basert på utskrevne bankkontoutdrag. Hvis du bare laster ned en rekke banktransaksjoner fra nettbanken, er utdragsnummeret vanligvis ikke viktig. 
>
>Saldo ved forrige utdrag beholdes på bankkontoen for å redusere feil ved bankavstemming, men den kan også redigeres, slik at du kan gjøre bankavstemmingene i den rekkefølgen du ønsker. Dette betyr også at hvis du angrer et bankkontoutdrag, kan det hende at den nye sluttsaldoen ikke er saldoen ved siste utdrag på neste bankutdrag. Det finnes ingen funksjon som gjør at du kan flytte en saldo fremover til alle påfølgende bankkontoutdrag, så vær klar over dette når du bruker Angre. 

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/bank-reconciliation-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Avstemme bankkonter](bank-manage-bank-accounts.md)  
[Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Konfigurere banktjenester](bank-setup-banking.md)  
[Definere regler for automatisk utligning av betalinger](receivables-how-set-up-payment-application-rules.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]