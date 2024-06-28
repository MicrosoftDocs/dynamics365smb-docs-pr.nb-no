---
title: Avstemme bankkontoer
description: Lære hvordan du avstemmer transaksjoner i Business Central med transaksjoner i oppgaver fra banken.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 10/24/2023
ms.custom: bap-template
---
# Avstemme bankkontoer

Bankavstemming bidrar til å sikre at innholdet i bøkene dine samsvarer med oppgaver du mottar fra banken. Bankkontoavstemming sammenligner og samstemmer poster i bankkontiene du har definert i [!INCLUDE[prod_short](includes/prod_short.md)], med banktransaksjoner hos banken. Avstemming kan deretter bokføre saldoene på bankkontiene i [!INCLUDE[prod_short](includes/prod_short.md)] for å gjøre dem tilgjengelige for finansledere. Bankavstemming er også en praktisk måte å oppdage og løse manglende betalinger og bokføringsfeil.

Denne artikkelen beskriver hvordan du samstemmer bankkonti fra siden **Bankkontoavstemming**.

Du kan imidlertid avstemme bankkontoer på siden **Betalingsavstemmingskladd** når du behandler betalinger. Åpne bankkontoposter relatert til den gjeldende kunde- eller leverandørpostene, blir lukket når du velger handlingen **Bokfør betalinger og avstem bankkonto**. Dette avstemmer automatisk bankkontoen for betalinger du bokfører med kladden. Hvis du vil ha mer informasjon, kan du se [Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> I nord-amerikanske versjoner tilbys siden **Bankavstemmingsforslag**, som er mer egnet for sjekker og innskudd, men lar det ikke importere filer med bankkontoutdrag. Hvis du vil bruke denne siden i stedet for **Bankkontoavstemming**-siden, fjerner du feltet **Bankavstemming med automatisk samsvar** på siden **Finansoppsett**. Hvis du vil ha mer informasjon, kan du se delen [Avstemme bankkontoer](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) under lokal funksjonalitet for USA.

Linjene på siden **Bankkontoavstemming** er delt i to ruter. Ruten **Bankkontoutdragslinjer** viser importerte banktransaksjoner eller poster med utestående betalinger. Ruten **Bankkontoposter** viser postene i den interne bankkontoen.

## Om bankavstemming 

Avstemming av transaksjoner i oppgaver fra banken med bankposter i [!INCLUDE[prod_short](includes/prod_short.md)] kalles *avstemming*. Det finnes tre måter å avstemme transaksjoner med bankposter på:

* Automatisk ved å bruke handlingen **Avstem automatisk**.

* Automatisk ved hjelp av handlingen **Avstem med Copilot**.

  Denne handlingen er tilgjengelig som en del av funksjonen for bankavstemmingshjelp (forhåndsversjon), som er en funksjon drevet av kunstig intelligens. [Lær om bankkontoavstemmingshjelpen](bank-reconciliation-with-copilot.md).
* Manuelt ved å velge linjer manuelt i begge rutene for å koble hver bankkontoutdragslinje til én eller flere relaterte bankkontoposter, og deretter bruke handlingen **Avstem manuelt**.

Det er merket av for **Utlignet** på linjer der postene som er utlignet. Hvis du vil ha mer informasjon, kan du se [Definere regler for automatisk utligning av betalinger](receivables-how-set-up-payment-application-rules.md). Hvis du angir en utdragssluttdato på bankavstemmingen etter at du har avstemt linjene med poster, vil [!INCLUDE [prod_short](includes/prod_short.md)] gjøre om treffene for linjer og poster som er etter denne datoen.

> [!NOTE]
> Når du har angitt en dato i feltet **Utdragsdato**, filtrerer siden **Bankkontoavstemming** bankposter slik at den bare viser poster frem til denne datoen. Du kan bare bokføre bankavstemminger med bankposter på eller før sluttdatoen for utdraget. Filteret sikrer at bankkontoen din balanserer med bankkontoutdraget på sluttdatoen for utdraget, med differansen som er utestående betalinger og sjekker.

Når verdien i feltet **Total saldo** i ruten **Bankkontoutdragslinjer** er lik totalverdien i feltet **Saldo som skal avstemmes** pluss feltet **Saldo ved forrige utdrag** i ruten **Bankkontoposter**, kan du velge handlingen **Bokfør**. Bankkontoposter som ikke samsvarer, blir værende på siden, som angir avvik du må løse for å avstemme bankkontoen.

Alle linjer som ikke kan sammenlignes, angitt med en verdi i **Differanse**-feltet, blir værende på siden **Bankkontoavstemming** etter bokføring. De representerer en form for avvik som du må løse før du kan fullføre bankkontoavstemmingen. Tabellen nedenfor beskriver noen vanlige forretningssituasjoner som kan forårsake forskjeller.

| Differanse | Årsak | Løsning |
|------------|--------|------------|
| En transaksjon på bankkontoen i [!INCLUDE[prod_short](includes/prod_short.md)] er ikke på bankkontoutdraget. | Banktransaksjonen ble ikke opprettet selv om det ble gjort en bokføring i [!INCLUDE[prod_short](includes/prod_short.md)]. | Opprett den manglende transaksjonen (eller be en debitor om å gjøre det). Deretter importerer du bankkontoutdragsfilen på nytt eller angir transaksjonen manuelt. |
| En transaksjon på bankkontoutdraget finnes ikke som et bilag eller en kladdelinje i [!INCLUDE[prod_short](includes/prod_short.md)]. | En banktransaksjon ble foretatt uten en tilsvarende bokføring i [!INCLUDE[prod_short](includes/prod_short.md)], for eksempel en kladdelinjebokføring for en utgift. | Opprett og bokfør den manglende oppføringen. Hvis du vil ha informasjon om hvordan du raskt gjør dette, kan du se [Opprette manglende poster for utligning av banktransaksjoner](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines). |
| En transaksjon i den interne bankkontoen tilsvarer en banktransaksjon, men noe informasjon er for forskjellig for å utgjøre et samsvar. | Informasjon, for eksempel beløpet eller kundenavnet, ble skrevet inn på en annen måte i banktransaksjonen eller den interne posteringen. | Se gjennom informasjonen, og samsvar de to deretter manuelt. Du kan eventuelt korrigere dette manglende samsvaret. |

Du må løse forskjellene, for eksempel ved å opprette manglende poster og korrigere ikke-samsvarende informasjon, eller ved å utføre transaksjoner som mangler penger, til bankkontoavstemmingen er fullført og postert.

Du kan fylle ut ruten **Bankkontoutdragslinjer** på siden **Bankkontoavstemming** på følgende måter:

* Automatisk, ved hjelp av funksjonen **Importer bankkontoutdrag** for å fylle ut ruten **Bankkontoutdragslinjer** med banktransaksjoner i henhold til en importert fil eller strøm oppgitt av banken.
* Manuelt, ved hjelp av funksjonen **Foreslå linjer**, for å fulle ut ruten **Bankkontoutdragslinjer** i henhold til fakturaer i [!INCLUDE[prod_short](includes/prod_short.md)] som har utestående betalinger.

## Legge til bankavstemmingslinjer ved å importere et bankkontoutdrag

Ruten **Bankkontoutdragslinjer** fylles ut med banktransaksjoner i henhold til en importert fil eller strøm fra banken.

For å kunne importere bankkontoutdrag som bankfeeder, må du sette opp tjenesten Envestnet Yodlee Bank Feed. Dette oppsettet inkluderer kobling til bankkontoen i [!INCLUDE[prod_short](includes/prod_short.md)] til den relaterte nettbankkontoen. Hvis du vil ha mer informasjon, kan du se [Konfigurere Envestnet Yodlee Bank Feeds-tjenesten](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> Du kan også importere bankkontoutdragsfiler i komma- eller semikolondelt format (.CSV). Bruk veiviseren **Definer et filformat for bankkontoutdrag** for assistert installasjon til å definere importformater for bankkontoutdrag og knytte formatet til en bankkonto. Du kan deretter bruke disse formatene når du importerer bankkontoutdrag på siden **Bankkontoavstemming**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") angi **Bankkontoavstemming**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. I feltet **Bankkontonr.** velger du den aktuelle bankkontoen. Bankkontoposter som finnes i å bankkontoen som vises i ruten **Bankkontoposter**.
4. I feltet **Utdragsdato** angir du datoen på utdraget fra banken.
5. I feltet **Utdrag - sluttsaldo** angi du saldoen fra kontoutdraget fra banken.
6. Hvis du har en fil for bankkontoutdrag, velger handlingen **Importer bankkontoutdrag**.
7. Finn filen, og velg deretter **Åpne**-knappen for å importere banktransaksjonene til ruten **Bankkontoutdragslinjer** på siden **Bankkontoavstemming**.

## Slik fyller du bankavstemmingslinjer med handlingen Foreslå linjer

Ruten **Bankkontoutdragslinjer** fylles ut i henhold til fakturaer i [!INCLUDE[prod_short](includes/prod_short.md)] som har utestående betalinger.  

1. På siden **Bankkontoavstemming** velger du handlingen **Foreslå linjer**.
2. I feltet **Startdato** angir du den første bokføringsdatoen postene skal avstemmes for.
3. I feltet **Sluttdato** angir du den siste bokføringsdatoen postene skal avstemmes for.

    > [!NOTE]
    > Vanligvis vil sluttdatoen være lik den datoen som er angitt i feltet **Utdragsdato**. Hvis du imidlertid vil avstemme transaksjoner bare for en del av en periode, kan du angi en annen sluttdato.

4. Hvis du ikke vil at bankkontoposten skal inneholde ikke-samsvarende åpne tilbakeførte poster, velger du **Utelat tilbakeførte poster**. Som standard inkluderer listen over bankkontoposter tilbakeførte poster inntil kontoutdragsdatoen.
5. Velg **OK**-knappen.

## Avstemme bankkontoutdragslinjer med bankkontoposter automatisk

Siden **Bankkontoavstemming** inneholder automatisk samsvarsfunksjonalitet basert på samsvar av tekst på en bankkontoutdragslinje (venstre rute) med tekst på én eller flere bankkontoposter (høyre rute). Du kan overskrive foreslått automatisk samsvar, og du kan velge ikke å bruke automatisk samsvar i det hele tatt. Hvis du vil ha mer informasjon, kan du se [Avstemme bankkontoutdragslinjer med bankkontoposter manuelt](#match-bank-statement-lines-with-bank-account-ledger-entries-manually).

Du kan undersøke grunnlaget for avstemming ved å bruke handlingen **Avstemmingsdetaljer**. Detaljene vil for eksempel omfatte navnene på feltene som inneholder samsvarende verdier.  

1. På siden **Bankkontoavstemming** velger du handlingen **Avstem automatisk**. Siden **Avstem bankposter** åpnes.
2. I feltet **Toleranse for transaksjonsdato (dager)** angir du antall dager før og etter bankkontopostens bokføringsdato som handlingen søker innenfor etter samsvarende transaksjonsdatoer i bankkontoutdraget.

    Hvis du skriver inn 0 eller la feltet stå tomt, vil **Avstem automatisk**-handlingen bare søke etter samsvarende transaksjonsdatoer på bankkontopostens bokføringsdato.
3. Velg **OK**-knappen.

    Linjene er fargekodet for å gjøre det enklere å forstå hva du skal gjøre med dem. Bankkontoutdragslinjer og bankkontoposter som er avstemt i nåværende bankavstemming, endres til fet, grønn skrift. Bankkontoposter som er samsvart i andre bankavstemminger, vises med kursiv, blå skrift.
4. Hvis du vil fjerne en avstemming, merker du bankkontoutdragslinjen og deretter velger du handlingen **Fjern avstemming**.

> [!TIP]
> Du kan bruke en blanding av manuell og automatisk avstemming. Hvis du har avstemt poster manuelt, vil ikke automatisk avstemming overskrive valgene dine.

## Avstemme bankkontoutdragslinjer med bankkontoposter manuelt

> [!TIP]
> Når du skal tilordne linjer og poster manuelt, kan handlingene **Vis alle**, **Vis tilbakeførte poster**, **Skjul tilbakeførte poster** og **Vis ikke-avstemt** gjøre det enklere å få en oversikt. Som standard inneholder ikke bankkontopostene ikke-samsvarende tilbakeførte poster. Hvis du vil inkludere disse postene i oversikten og tilordne dem manuelt, velger du handlingen **Vis tilbakeførte poster**. Hvis du velger å skjule tilbakeførte poster etter at du har gjort ett eller flere samsvar, vises de samsvarende postene fremdeles.

> [!NOTE]
> Du kan ikke postere en bankavstemming hvis du gjør mange-til-én-samsvar og de kombinerte beløpene inneholder differanser. Dette gjelder selv om de kombinerte differansene balanserer til null.
>
> Her er et eksempel på en mange-til-én-samsvar som har differanser. Verdien på 200 for bankkontoutdragsoppføring 1 samsvarer med to bankposter som har en totalverdi på 180. Differansen er 20. Verdien på 350 for bankkontoutdrag 2 samsvarer med to andre bankposter som har en totalverdi på 370. Differansen er –20, som balanserer verdien av 20 for bankkontoutdrag 1.  
>
> Hvis du vil bokføre en bankavstemming mot differanser på linjene, bokfører du forskjellene og samsvarer dem mot de bokførte postene.

1. Velg en ikke-avstemt linje i ruten **Bankkontoutdragslinjer** på siden **Bankkontoavstemming**.
2. I ruten **Bankkontoposter** velger du én eller flere bankkontoposter som kan avstemmes med den valgte bankkontoutdragslinjen. Hvis du vil velge flere linjer, velger og holder du nede <kbd>Ctrl</kbd>-tasten og deretter velger du linjene.

   > [!TIP]
   > Du kan også manuelt tilordne flere bankkontoutdragslinjer til én bankkontopost. Dette kan for eksempel være nyttig hvis bankbeløpet inneholder flere betalingsmåter, for eksempel kredittkort fra ulike utstedere, og banken viser de som separate linjer.
3. Velg handlingen **Avstem manuelt**.

    De valgte bankoppgavelinjene og de valgte bankkontopostene endres til grønn skrift, og det er merket av for **Utlignet** i ruten til høyre.
4. Gjenta trinn 1 til 3 for alle bankkontoutdragslinjene som ikke er avstemt.

> [!TIP]
> Hvis du vil fjerne en avstemming, merker du bankkontoutdragslinjen og deretter velger du handlingen **Fjern avstemming**. Hvis du har tilordnet flere bankkontoutdragslinjer til en post og du må fjerne en eller flere av avstemte linjer, fjernes alle de manuelle postene for posten når du velger **Fjern avstemming**.

## Validere bankavstemmingen

Hvis du vil dobbeltsjekke bankkontoavstemmingen før du bokfører den, bruker du handlingen **Test rapport** for å forhåndsvise avstemmingen. Følgende rapport er tilgjengelig i følgende kontekster:

* Når du forbereder en bankavstemming på siden **Bankkontoavstemming**.
* Når du avstemmer bankkonti på siden **Betalingsavstemmingskladder**.

Linjer som ikke kan samsvare, forblir på siden **Bankkontoavstemming** etter bokføring. Disse linjene inneholder en verdi i feltet **Differanse**. Differansen representerer et avvik som du må løse før du kan fullføre bankkontoavstemmingen. Tabellen nedenfor beskriver noen vanlige forretningssituasjoner som kan forårsake forskjeller.

| Differanse | Årsak | Løsning |
|------------|--------|------------|
| En transaksjon på bankkontoen i [!INCLUDE[prod_short](includes/prod_short.md)] er ikke på bankkontoutdraget. | Banktransaksjonen ble ikke opprettet selv om det ble gjort en bokføring i [!INCLUDE[prod_short](includes/prod_short.md)]. | Opprett den manglende transaksjonen (eller be en debitor om å gjøre det). Deretter importerer du bankkontoutdragsfilen på nytt eller angir transaksjonen manuelt. |
| En transaksjon på bankkontoutdraget finnes ikke som et bilag eller en kladdelinje i [!INCLUDE[prod_short](includes/prod_short.md)]. | En banktransaksjon ble foretatt uten en tilsvarende bokføring i [!INCLUDE[prod_short](includes/prod_short.md)], for eksempel en kladdelinjebokføring for en utgift. | Opprett og bokfør den manglende oppføringen. Hvis du vil ha informasjon om hvordan du raskt gjør dette, kan du se [Opprette manglende poster for utligning av banktransaksjoner](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines). |
| En transaksjon i den interne bankkontoen tilsvarer en banktransaksjon, men noe informasjon er for forskjellig for å utgjøre et samsvar. | Informasjon, for eksempel beløpet eller kundenavnet, ble skrevet inn på en annen måte i banktransaksjonen eller den interne posteringen. | Se gjennom informasjonen, og samsvar de to deretter manuelt. Du kan eventuelt korrigere dette manglende samsvaret. |

Du må løse forskjellene, for eksempel ved å opprette manglende poster og korrigere ikke-samsvarende informasjon, eller ved å utføre transaksjoner som mangler penger, til bankkontoavstemmingen er fullført og postert.

> [!NOTE]
> Siden Bankavstemming og testrapporten forutsetter at du bare avstemmer innen perioden frem til sluttdatoen for utdraget. Hvis du samsvarer en bankkontoutdragslinje med en bankkontopost før du angir en sluttdato for utdrag, og deretter angir en sluttdato for utdraget etter sluttdatoen for bankkontoposten, blir dataene i testrapporten feil.

Tabellen nedenfor beskriver felter i testrapporten som kan hjelpe deg med å fullføre bankavstemmingen.

|Felt  |Description  |
|---------|---------|
|Utdragsdato| Datoen som er angitt i feltet **Utdragsdato** på siden **Bankkontoavstemming**.|
|Saldo ved forrige utdrag|Saldoen som er angitt i feltet **Saldo ved forrige utdrag** på siden **Bankkontoavstemming**. Dette fylles ut automatisk fra den siste avstemmingen for samme bankkonto. Verdien er null hvis dette er din første bankkontoavstemming.|
|Utdrag – sluttsaldo|Saldoen som er angitt i feltet **Utdrag – sluttsaldo** på siden **Bankkontoavstemming**. |
|Finanskontonummer <*nummer*> Saldo på <*dato*> | Saldoen på finanskontoen på utdragets sluttdato. Dette er den ufiltrerte saldoen per denne datoen. Hvis banken bruker den lokale valutaen, bør denne saldoen være den samme som bankkontosaldoen (vist til høyre i rapporttoppteksten) når du har samsvart med alle utdragslinjene. En tom **()** i navnet på dette feltet betyr at banken bruker lokal valuta.<br><br>Et avvik i dette og de forrige feltene kan indikere at du har bokført direkte til finanskontoen, eller at du bruker samme finanskonto for flere banker, noe som ikke anbefales. Bankene er knyttet til økonomimodulen gjennom bankkontobokføringsgruppen som er angitt for kontoen.<br><br>Testrapporten viser en advarsel hvis du har direkte bokføringer, selv om saldoen for bokføringen er null. Direkte bokføringer som ikke er balansert, fører ofte til akkumulerte differanser for fremtidige bankavstemminger. Du bør kontrollere finanssaldoen og finanspostene før du bokfører bankavstemmingen. Hvis du vil vite mer om direkte bokføring, kan du gå til [Unngå direkte bokføring](#avoid-direct-posting).|
|Finanskontonummer <*nummer*> Saldo (<*lokal valuta*>) på <*dato*>| Saldoen på finanskontoen på utdragets sluttdato i lokal valuta. Saldoen konverteres til bankkontoens valuta ved hjelp av valutakursen som var gyldig på utdragets sluttdato. Dette er den ufiltrerte saldoen per denne datoen. Du sammenligner dette med **Finanskontonummer <* nummer *> Saldo på <* dato*>*-felt hvis banken bruker utenlandsk valuta. Verdien i finanskontonummer <* nummer *> Saldo på <* dato*>-feltet for lokal valuta kan variere noe fordi valutakonvertering kan føre til små differanser. Bankens saldo bør være svært nær denne saldoen.  |
|Bankkontosaldo på <*dato*>| Saldoen på bankkontoen på utdragets sluttdato.|
|Differansesum    | Summen av differansene for utdragslinjene. Hvis du vil ha tilgang til detaljene, aktiverer du veksleknappen **Skriv ut utestående transaksjoner** når du angir vilkår for rapporten. En differanse er en bankkontoutdragslinje som ikke samsvarer fullstendig med én eller flere bankposter. Du kan ikke bokføre en bankkontoavstemming som har differanser. Du kan bokføre en bankavstemming som inneholder bankposter som ikke samsvarer med utdragslinjer. Denne verdien vises i feltet **Utestående banktransaksjoner** og i en egen del hvis du aktiverer veksleknappen Skriv ut utestående transaksjoner.      |
|Kontoutdragssaldo     | Verdien som er angitt i feltet **Utdrag – sluttsaldo** på siden **Bankkontoavstemming**.  |
|Utestående banktransaksjoner     | Summen av ikke-samsvarende, ikke-sjekkbankposter som har en bokføringsdato på eller før sluttdatoen for utdraget. Dette skjer når du registrerer transaksjoner før de er registrert i banken. For eksempel på slutten av en periode. Når du oppretter den neste bankavstemmingen, kan du avstemme disse postene.        |
|Utestående sjekker     | Summen av ikke-samsvarende bankposter for sjekker som har en bokføringsdato på eller før sluttdatoen for utdraget. Dette skjer når du registrerer transaksjoner før de er registrert i banken. Dette kan for eksempel skje for sjekker hvis en leverandør ikke løser inn en sjekk i samme periode som du registrerte den. Når du oppretter den neste bankavstemmingen, kan du avstemme disse postene.        |
|Bankkontosaldo     | Summen av verdiene for sluttsaldoen på bankkontoutdraget, utestående banktransaksjoner og utestående sjekker. Når du har håndtert alle differanser på samsvarende poster, samsvarer denne saldoen med banksaldoen. Du har for eksempel tatt høyde for alle samsvarende poster i tillegg til postene du ikke kunne samsvare for dette kontoutdraget. Du kan bokføre avstemmingen.        |

> [!TIP]
> Hvis du kjører **testrapporten** fra siden **Betalingsavstemmingskladd**, beregner [!INCLUDE [prod_short](includes/prod_short.md)] verdien i **sluttsaldoen for utdrag** på følgende måte:
>
> * saldo ved forrige utdrag + summen av alle linjer i betalingsavstemmingskladd
>
> Du kan bruke verdien til å sammenligne med kontoutskriften.

## Opprette manglende poster for utligning av bankkontoutdragslinjer

Noen ganger inneholder et bankkontoutdrag et rente- eller gebyrbeløp. Slike bankkontoutdragslinjer kan ikke utlignes fordi det ikke finnes noen relaterte poster i [!INCLUDE[prod_short](includes/prod_short.md)]. Du må deretter bokfører en kladdelinje for hver transaksjon for å opprette en relatert post som den kan utlignes mot.

1. På siden **Bankkontoavstemming** velger du handlingen **Overfør til finanskladd**.  
2. På siden **Overfør bankavst. til finans** angir du hvilken finanskladd du vil bruke, og velger deretter **OK**-knappen.

    Siden **Finanskladd** åpnes med nye kladdelinjer for bankerkontoutdragslinjer som mangler poster.
3. Fyll ut kladdelinjen med informasjon, for eksempel motkonto. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).  
4. Hvis du vil se gjennom resultatet av bokføringen før du bokfører, velger du handlingen **Testrapport**, og deretter velger du et alternativ for tilgang til rapporten. **Bankkontoutdrag**-rapporten viser de samme feltene som ved overskriften i **Bankkontoavstemming**-siden.
5. Velg handlingen **Bokfør**.

    Når posten er bokført, samsvarer du bankkontoutdragslinjen med den.
6. Oppdater eller åpne siden **Bankkontoavstemming**. Den nye posten vises i ruten **Bankkontoposter**.
7. Utligne bankkontoutdragslinjen med bankkontopost, enten manuelt eller automatisk.

## Finne utestående transaksjoner for tidligere perioder

Du kan bruke rapporten Bankkontoutdrag til å finne utestående transaksjoner i tidligere perioder. Utestående transaksjoner ble åpnet før utdragsdatoen og er ikke lukket, eller ble lukket etter at bankavstemmingen ble bokført.

Når du kjører rapporten Bankkontoutdrag fra siden Bankkontoutdrag, kan du aktivere funksjonen for **Utestående poster**, og rapporten vil inkludere en inndeling som viser utestående poster.

**Eksempel** Vi har bankkontoposter A, B og C i bankkontoen vår for august måned. Når vi avstemmer vår bankkonto i august, finner vi en bankkontoutdragslinje som samsvarer med post A, men ingen for B og C. Derfor bokfører vi avstemmingen med post A avstemt og B og C som utestående poster.

I september mottar vi en betaling for post B og fastsetter for å avstemme bankkontoen. Hvis vi kjører rapporten Bankkontoutdrag før bokførring av avstemmingen, har vi én avstemt transaksjon og én utestående transaksjon.

Hvis vi skriver ut rapporten for august, har vi utestående transaksjoner til våre B- og C-oppføringer, selv om vi lukket post B i september.

## Angre en bankkontoavstemming

Hvis du oppdager en feil i en bokført bankavstemming, kan du ved hjelp av **Angre**-handlingen på **Bankkontoutdragsliste**-siden rette den opp. Når du angrer en bokført bankavstemming, flyttes postene til **Bankavstemming**-siden og merkes som **Åpne**, og det betyr at de ikke er avstemt. Deretter kan du korrigere bankavstemmingen og bokføre den på nytt.

> [!NOTE]
> Hvis du vil bruke Angre-funksjonen for bokførte bankavstemminger og bankkontoutdrag i Nord-Amerika, må du aktivere **Bankavstemming med automatisk samsvar** på **Finansoppsett**-siden. Angre-funksjonen er ikke tilgjengelig for bankkontoutdrag som er bokført fra bankavstemmingsforslag.

### Bruke bankkontoutdragsnummeret på nytt

Bankkontoutdragsnummeret som brukes for den nye bankavstemmingen, hentes fra bankkontoen, som er Saldo ved forrige utdrag. Du kan endre disse verdiene før du starter en ny bankavstemming. Når du oppretter en ny bankavstemming, kontrollerer imidlertid [!INCLUDE[d365fin](includes/d365fin_md.md)] om utdragsnummeret allerede er tilordnet et bokført bankkontoutdrag. Hvis nummeret er i bruk, men du vil at det nye bankkontoutdraget skal bruke det i stedet, kan du bruke handlingen **Endre utdragsnummer** på siden **Bankkontoavstemming**.

### Eksempler

Nedenfor følger noen få eksempler på hvordan du kan rette opp en feil i en bokført bankavstemming med eller uten å bruke det samme kontoutdragsnummeret.

#### Eksempel 1

Du gjorde bankavstemminger for januar, februar og mars. Bankkontoutdragsnummeret er 100 for mars. Senere oppdager du at mars bare tok med poster frem til 30. Dette betyr at det mangler poster for 31. Du må derfor gjøre om bankavstemmingen for mars. I dette tilfellet åpner du siden **Bankkontoutdrag**, velger utdraget for mars, og deretter velger du **Angre**. 

Den nye bankavstemmingen får kontoutdragsnummer 101. Hvis du vil tilordne nummeret 100 på nytt, velger du **Endre utdragsnummer** og angir **100**. 

> [!TIP]
> Husk å angi den aktuelle sluttdatoen for utdraget (i dette eksemplet er det 31. mars), og rediger feltet **Saldo ved forrige utdrag**. 

#### Eksempel 2

Du gjorde bankavstemminger for januar, februar, juni og juli. Du oppdager at februar var feil. La oss anta at den har utdragsnummer 100. Som i eksempel 1 bruker du handlingene Angre og Endre utdragsnummer til å endre kontoutdragsnummeret, som i eksempel 1 ovenfor, og du kan nå gjøre om bankavstemmingen for februar.  

Når du har bokført den korrigerte bankavstemmingen for februar, på det tilhørende bankkontokortet, viser feltet **Siste kontoutdragsnr.** **100**, og feltet **Saldo ved forrige utdrag** viser sluttsaldoen for februar-utdraget. 

Hvis den neste bankavstemmingen gjelder mars, tilordner [!INCLUDE[d365fin](includes/d365fin_md.md)] 101 som utdragsnummer og gir den riktig **Saldo ved forrige utdrag**.

Hvis den neste bankavstemmingen er for august, kan du vurdere å endre verdiene i feltene **Siste kontoutdragsnr.** og **Saldo ved forrige utdrag** på kortet **Bankkonto** før du oppretter den neste bankavstemmingen, eller bruke handlingen **Endre utdragsnummer** og endre verdien i feltet **Saldo ved forrige utdrag** på bankavstemmingssiden.

> [!NOTE]
> Kontoutdragsnummeret er viktig når du gjør bankavstemminger med importerte CAMT-filer som inneholder kontoutdragsnumre, eller når du avstemmer basert på utskrevne bankkontoutdrag. Hvis du bare laster ned en rekke banktransaksjoner fra nettbanken, er utdragsnummeret vanligvis ikke viktig.  
>
> Saldo ved forrige utdrag beholdes på bankkontoen for å redusere feil ved bankavstemming, men den kan også redigeres, slik at du kan gjøre bankavstemmingene i den rekkefølgen du ønsker. Dette betyr også at hvis du angrer et bankkontoutdrag, kan det hende at den nye sluttsaldoen ikke er saldoen ved siste utdrag på neste bankutdrag. Det finnes ingen funksjon som gjør at du kan flytte en saldo fremover til alle påfølgende bankkontoutdrag, så vær klar over dette når du bruker Angre.  

## Unngå direkte bokføring

Ikke bruk en finanskonto som tillater direkte bokføring i bankkontobokføringsgruppen. Direkte bokføring vil bryte forbindelsen mellom bankkontoposten og finanskontoposten. Når du avstemmer bankkontoen, tas ikke postene som er bokført direkte til finanskontoen, og det er vanskelig å fullføre avstemmingen.

Denne feilen oppstår ofte når du angir en startsaldo for en bankkonto. Det er viktig at du ikke bokfører åpningssaldoen direkte i finans. Poster på finanskontoen som bokføres direkte på finanskontoen, forårsaker problemer. Disse postene kan for eksempel hindre deg i å avstemme bankkontoen. Når det gjelder bankkonti i fremmed valuta, kan postene føre til at differansene akkumuleres etter at du har bokført flere bankavstemminger, på grunn av valutakursjusteringer. Ofte bokfører du åpningssaldoen direkte til bankkontoen, og beløpet ender deretter opp i finanskontoen. Alternativt kan du tilbakeføre det senere mot finanskontoen som du bruker til å balansere den åpne finanssaldoen. I begge tilfeller må du balansere eventuell direkte bokføring til finanskontoen før du starter den første bankavstemmingen, og spesielt hvis bankkontoen er i en utenlandsk valuta.


## Se også

[Avstemme bankkonter](bank-manage-bank-accounts.md)  
[Avstemme bankkonti ved hjelp av bankavstemmingshjelp (forhåndsversjon)](bank-reconciliation-with-copilot.md)
[Utligne betalinger automatisk og avstemme bankkontoer](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Konfigurere banktjenester](bank-setup-banking.md)  
[Definere regler for automatisk utligning av betalinger](receivables-how-set-up-payment-application-rules.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
