---
title: Arbeide med finanskladder for å bokføre direkte i Finans
description: Finn ut hvordan du bruker kladder til å bokføre finanstransaksjoner på finanskonti og andre konti, for eksempel bank-, kunde- og leverandørkonti. Bruk gjentakelseskladder til å bokføre avsetninger og fordele saldoer etter dimensjonsverdier.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: journals, recurring, accrual, renumber, bulk-post
ms.search.form: 39, 101, 102, 182, 184, 185, 201, 207, 250, 251, 253, 255, 256, 261, 262, 283, 519, 750, 751, 752, 753, 754, 755, 12409, 12410, 12411, 1290, 10101, 11400, 11402, 11403, 11405, 11300, 2000000, 2000001, 2000003, 2000020, 2000021, 2000022, 9020, 9022, 9026, 9027, 9030, 9000, 9004, 9005, 9018, 9006, 9007, 9010, 9016, 9017
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1d042d2a399f6bf0fb329aa9287e4ced37e43fef
ms.sourcegitcommit: 75a388b1d8917e2bbd49398ef76cf86cf37e6767
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323087"
---
# <a name="working-with-general-journals"></a>Arbeide med finanskladder

De fleste finanstransaksjoner bokføres i Finans via dedikerte forretningsdokumenter, for eksempel kjøpsfakturaer eller ordrer. Men du kan også behandle forretningsaktiviteter som kjøp, betaling, ved å bruke gjentakelseskladder til å bokføre justeringer, eller refundering av ansattutgifter ved bokføring av kladdelinjene som opprettes i de forskjellige kladdene i [!INCLUDE[prod_short](includes/prod_short.md)].  

De fleste kladder er basert på *Finanskladd*, og du kan behandle alle transaksjonene på siden **Finanskladd**. Hvis du vil ha mer informasjon, kan du se [Bokføre transaksjoner direkte i Finans](finance-how-post-transactions-directly.md).  

Du kan for eksempel bokføre ansattes utlegg for firmarelaterte utgifter for senere refusjon. Hvis du vil ha mer informasjon, kan du se [Registrere og refundere ansattes utgifter](finance-how-record-reimburse-employee-expenses.md).

Men i mange tilfeller vil du bruke kladder som er tilpasset for bestemte typer transaksjoner, som **Utbetalingskladd**, til å registrere betalinger. Hvis du vil ha mer informasjon, se [Registrere betalinger og refusjoner i utbetalingskladden](payables-how-post-payments-refunds.md).  

Du bruker finanskladder til å bokføre finanstransaksjoner direkte på finanskonti og andre konti, for eksempel bank-, kunde-, leverandør- og ansattkonti. Bokføring med en finanskladd oppretter alltid poster på finanskonti. Dette gjelder selv om en kladdelinje for eksempel bokføres på en kundekonto, ettersom en post bokføres til en finanssamlekonto via en bokføringsgruppe.

Opplysningene du angir i en kladd, er midlertidige og kan endres mens de fortsatt befinner seg i kladden. Når du bokfører kladden, overføres opplysningene til poster i individuelle konti, der de ikke kan endres. Du kan imidlertid oppheve utligningen av bokførte poster, og du kan bokføre tilbakeførings- eller korrigeringsposter. Hvis du vil ha mer informasjon, kan du se [Tilbakeføre kladdebokføringer og angre mottak/leveringer](finance-how-reverse-journal-posting.md).

> [!NOTE]
> [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]  

## <a name="using-journal-templates-and-batches"></a>Bruke kladder og kladdemaler

Det finnes flere finanskladdemaler. Hver kladdemal er representert på en egen side med bestemte funksjoner og feltene som er nødvendige for å støtte disse funksjonene, for eksempel siden **Betalingsavstemmingskladd** for å behandle betalinger og **Betalingskladd** for å betale leverandører eller gi ansatte refusjon. Hvis du vil ha mer informasjon, se [Foreta betalinger](payables-make-payments.md) og [Avstem kundebetalinger med innbetalingskladden eller fra kundeposter](receivables-how-apply-sales-transactions-manually.md).

Du kan definere dine egne personlige kladder som en kladd for hver enkelt kladdemal. Du kan for eksempel definere din egen kladd for betalingskladden som har personlig oppsett og innstillinger. Tipset nedenfor er et eksempel på hvordan du kan tilpasse en kladd.

> [!TIP]  
> Hvis du merker av for **Foreslå motkontobeløp** på linjen for den kladden på siden **Finanskladder**, vil deretter for eksempel **Beløp**-feltet på finanskladdelinjer for samme dokumentnummer, automatisk forhåndsutfylles med verdien som kreves for å balansere dokumentet. Hvis du vil ha mer informasjon, kan du se [La [!INCLUDE[prod_short](includes/prod_short.md)] foreslå verdier](ui-let-system-suggest-values.md).

> [!TIP]
> Hvis du vil legge til eller fjerne felt i kladder, bruker du banneret **Tilpass**. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).

### <a name="validating-general-journal-batches"></a>Validere finanskladder
For å unngå forsinkelser ved bokføring kan du aktivere en bakgrunnskontroll som varsler deg når det oppstår en feil i finanskladden du arbeider med, som forhindrer at du bokfører kladden. På siden **Finanskladd** kan du velge **Bakgrunnsfeilkontroll** for at [!INCLUDE[prod_short](includes/prod_short.md)] skal validere finanskladder, for eksempel finans- eller utbetalingskladder, mens du arbeider med dem. 

Når du aktiverer valideringen, vises faktaboksen **Kladdkontroll** ved siden av kladdelinjene, og viser feil i gjeldende linje og i hele kladden. Valideringen skjer når du laster inn en finanskladd, og når du velger en annen kladdelinje. Flisen **Totalt antall problemer** i faktaboksen viser totalt antall problemer som [!INCLUDE[prod_short](includes/prod_short.md)] har funnet, og du kan velge den for å åpne en oversikt over problemene. 

Du kan bruke handlingene **Vis linjer med problemer** og **Vis alle linjer** for å veksle mellom kladdelinjer som har eller ikke har problemer. Den nye faktaboksen **Kladdelinjedetaljer** gir rask oversikt over og tilgang til data fra kladdelinjer, for eksempel finanskonto, kunde eller leverandør, i tillegg til bokføringsoppsettet for bestemte konti.     

### <a name="reversing-journals-to-correct-mistakes"></a>Tilbakeføre kladder for å korrigere feil
Når du arbeider med kladder som har mange linjer, og noe går galt, er det viktig å ha en enkel måte å rette opp feil på. Siden **Bokført finanskladd** inneholder et par handlinger som kan hjelpe.

* **Kopier valgte linjer til kladd** - Kopier bare de linjene du velger.
* **Kopier finansjournal til kladd** - Kopier alle linjer som tilhører samme finansjournal.

Med disse handlingene kan du opprette en kopi av en finanskladdelinje eller en kladd, og deretter angi følgende:

* Kladden som linjene skal kopieres til
* Om med motsatte fortegn (en tilbakeføringskladd)
* En annen bokføringsdato eller et annet bilagsnummer

Hvis du vil tillate at kladder kopieres til bokførte finanskladder, merker du av for **Kopier til bokførte kld.linj.** på siden **Finanskladdemaler**. Når du har tillatt å kopiere bokførte finanskladder, kan du om nødvendig deaktivere kopiering for bestemte kladder.

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Forstå hovedkonti og motkonti
Hvis du har definert standard motkonti for kladdene, vil motkontoen på siden **Finanskladder** bli fylt ut automatisk når du fyller ut **Kontonr.**-feltet. Hvis ikke, fyller du ut feltene **Kontonr.** og **Motkontonr.** manuelt. Et positivt beløp i **Beløp**-feltet debiteres hovedkontoen og krediteres motkontoen. Et negativt beløp krediteres hovedkontoen og debiteres motkontoen.

> [!NOTE]  
> Mva beregnes separat for hovedkontoen og motkontoen, så de kan bruke ulike mva-prosentsatser.

## <a name="working-with-recurring-journals"></a>Arbeide med gjentakelseskladder
En gjentakelseskladd er en finanskladd med spesifikke felt for håndtering av transaksjoner du bokfører ofte, med få eller ingen endringer, for eksempel leie, abonnementer, elektrisitet og varme. Hvis du bruker disse feltene for gjentatte transaksjoner, kan du bokføre både faste og variable beløp. Du kan også angi automatisk tilbakeføringsoppføringer for dagen etter bokføringsdatoen. Du kan også bruke fordelingsnøkler til å dele gjentakende poster mellom flere konti. Hvis du vil ha mer informasjon, kan du se [Fordeler gjentakelseskladden til flere konti](#allocating-recurring-journal-amounts-to-several-accounts).

Når kladden er en gjentakelseskladd, trenger du bare å fylle ut feltene som skal bokføres jevnlig, én gang. Det vil si at kontiene, dimensjonene og dimensjonsverdiene og så videre som du angir, forblir i kladden etter bokføring. Hvis eventuelle justeringer er nødvendig, kan du gjøre det ved hver bokføring.

### <a name="recurring-method-field"></a>Feltet Gjentakelsesprinsipp

Dette feltet angir hvordan beløpet på kladdelinjen skal bli behandlet etter bokføring. Du kan for eksempel velge å la beløpet stå hvis du skal bruke samme beløp hver gang du bokfører linjen. Hvis du vil bruke samme konto og tekst på linjen, men at beløpet vil variere hver gang du bokfører, kan du velge å slette beløpet etter bokføring.

| Hvis du vil | Se |
| --- | --- |
|F Fast|Beløpet på kladdelinjen vil bli stående etter bokføring.|
|V Variabel|Beløpet på kladdelinjen vil bli slettet etter bokføring.|
|S Saldo|Det bokførte beløpet i kontoen på linjen vil bli fordelt til kontiene som er angitt for linjen, i tabellen Fordeling. Saldoen på kontoen blir på denne måten nullstilt. Husk å fylle ut feltet **Andel i pst.** på siden **Fordelinger**. Hvis du vil ha mer informasjon, kan du se [Fordeler gjentakelseskladden til flere konti](#allocating-recurring-journal-amounts-to-several-accounts).|
|FT Fast med tilbakeføring|Beløpet på kladdelinjen vil bestå etter bokføring og en motpost vil bli bokført på den etterfølgende dato.|
|VT Variabel med tilbakeføring|Beløpet på kladdelinjen vil bli slettet etter bokføring og en motpost vil bli bokført på den etterfølgende dato.|
|ST Saldo med tilbakeføring|Det bokførte beløpet i kontoen på linjen vil bli fordelt til kontiene som er angitt for linjen, på siden **Fordelinger**. Saldoen på kontoen blir satt til null, og en motpost bokførtes på den etterfølgende datoen.|
|BD Saldo etter dimensjon|Kladdelinjen fordeler kostnader på grunnlag av saldoen på en finanskonto per dimensjon. Du blir bedt om å angi at dimensjonsfiltrene skal brukes til å beregne saldoen på finanskontoen per dimensjon som du vil fordele kostnader fra. Du kan eventuelt velge handlingen **Angi dimensjonsfiltre** senere.|
|RBD Saldo med tilbakeføring etter dimensjon|Kladdelinjen fordeler kostnader på grunnlag av saldoen med tilbakeføring på en finanskonto per dimensjon. Du blir bedt om å angi at dimensjonsfiltrene skal brukes til å beregne saldoen på finanskontoen per dimensjon som du vil fordele kostnader fra. Du kan eventuelt velge handlingen **Angi dimensjonsfiltre** senere.|

> [!NOTE]  
> Mva. feltene kan fylles ut på gjentakelseskladdelinjen eller på fordelingskladdelinjen, men aldri på begge. Det vil si at disse feltene bare kan fylles ut på siden **Fordelinger** hvis tilsvarende linjer i gjentakelseskladden ikke er fylt ut.

### <a name="recurring-frequency-field"></a>Feltet Gjentakelsesintervall
Dette feltet angir hvor ofte linjen på kladdelinjen skal bokføres. Det er et datoformelfelt, og det må fylles ut for gjentakende kladdelinjer. Hvis du vil ha mer informasjon, kan du se [Bruke datoformler](ui-enter-date-ranges.md#using-date-formulas).

#### <a name="examples"></a>Eksempler
Hvis kladdelinjen skal bokføres hver måned, setter du inn "1M". Etter hver bokføring vil datoen i feltet **Bokføringsdato** bli oppdatert til samme dato neste måned.

Hvis du vil bokføre en post på den siste dagen i hver måned, kan du gjøre ett av følgende:

- Bokfør den første post siste dag i måneden ved å angi 1D+1M-1D (1 dag + 1 måned - 1 dag). Ved hjelp av denne formelen beregnes bokføringsdatoen riktig uansett hvor mange dager det er i måneden.

- Bokfør den første posten på hvilken som helst dag i måneden ved å angi 1M+NM. Ved hjelp av denne formelen vil bokføringsdatoen være etter én hel måned, pluss de resterende dagene av denne måneden.

### <a name="expiration-date-field"></a>Feltet Utløpsdato/-klokkeslett
Dette feltet angir når linjen skal bokføres for siste gang. Linjen tas ikke med i bokføringen etter denne datoen.

Fordelen med å bruke feltet er at linjen ikke slettes fra kladden med en gang, og at du alltid kan erstatte den gjeldende utløpsdatoen med en senere dato, slik at du kan bruke linjen videre.

Hvis feltet er tomt, bokføres linjen hver gang du bokfører, helt til den slettes fra kladden.

### <a name="allocating-recurring-journal-amounts-to-several-accounts"></a>Fordele gjentakelseskladden til flere konti

På siden **Gjentakende finanskladd** kan du velge **Fordelinger**-handlingen for å vise eller håndtere hvordan beløp på gjentakelseskladdelinjen tildeles flere konti og dimensjoner. Vær oppmerksom på at tildeling fungerer som motkontolinje til gjentakelseskladdelinjen.

På samme måte som i en gjentakelseskladd er det tilstrekkelig å angi en fordeling én gang. Du behøver ikke å angi beløp og fordelinger hver gang du bokfører gjentakelseskladdelinjen, fordi fordelingen blir i fordelingskladden etter bokføring.

Hvis **Saldo** eller **Saldo med tilbakeføring** er angitt for det *gjentakende prinsippet* i den gjentakende kladden, tas det ikke hensyn til eventuelle dimensjonsverdikoder i den gjentakende kladden når kontoen nullstilles. Det vil si at hvis du i fordelingskladden fordeler en gjentakelseskladdelinje til forskjellige dimensjonsverdier på siden **Fordelinger**, vil det bare bli opprettet én post i tilbakeføringen. Derfor må du ikke angi samme kode på siden **Fordelinger** hvis du fordeler en gjentakelseskladdelinje som inneholder en dimensjonsverdikode. Hvis du gjør det, vil dimensjonsverdiene bli feile.  

Hvis du vil tildele gjentakende kladdebeløp basert på dimensjoner, setter du feltet **Gjentakelsesprinsipp** til **Saldo etter dimensjon** eller **Saldo med tilbakeføring etter dimensjon** i stedet. Hvis **Saldo etter dimensjon** eller **Saldo med tilbakeføring etter dimensjon** er angitt for det gjentakende prinsippet i den gjentakende kladden, tas det hensyn til eventuelle dimensjonsverdikoder i den gjentakende kladden når kontoen nullstilles. Hvis du tildeler en gjentakende linje til forskjellige dimensjonsverdier på **Fordelinger**-siden, opprettes det en rekke tilbakeførende poster som samsvarer med antall dimensjonsverdikombinasjoner som saldoen består av. Hvis du fordeler kontosaldoen gjennom den gjentakende kladden som inneholder en dimensjonsverdikode, må du huske å bruke **Saldo etter dimensjon** eller **Saldo med tilbakeføring etter dimensjon** for å sikre at dimensjonsverdiene balanseres eller tilbakeføres riktig fra kildekontoen.  

Det kan for eksempel være at selskapet ditt har et par konsern og noen avdelinger som kontrollører har definert som dimensjoner. Når du skal registrere kjøpsfakturaen raskere, bestemmer du deg for å kreve at leverandørens assistenter bare skal fylle ut konserndimensjoner. Ettersom hver forretningsenhet har spesifikke fordelingsnøkler for avdelingsdimensjonen, for eksempel basert på antall ansatte, kan du bruke de gjentakende metodene **BD Saldo etter dimensjon** eller **RBD Saldo med tilbakeføring etter dimensjon** for å tildele utgifter på nytt for hvert konsern, til de riktige avdelingene basert på fordelingsnøklene.  

> [!NOTE]
> Dimensjoner du angir på tildelinglinjer, beregnes ikke automatisk, og du må angi hvilke dimensjonsverdier som skal angis på tildelingskontoene. Hvis du vil beholde koblingen mellom kildekontodimensjonen og fordelingskontodimensjonen, anbefaler vi at du bruker [Kostregnskap](finance-about-cost-accounting.md)-funksjonene i stedet.

#### <a name="example-allocating-rent-payments-to-different-departments"></a>Eksempel: Fordele leiebetalinger til ulike avdelinger
Husleie betales hver måned, så derfor er husleiebeløpet angitt i kassakontoen på gjentakelseskladdelinjen. På siden **Fordelinger** kan du fordele utgiftene på flere avdelinger (avdelingsdimensjon), avhengig av hvor mange kvadratmeter hver avdeling opptar. Beregningen er basert på tildelingsprosenten på hver linje. Du kan for eksempel angi ulike konti på ulike fordelingslinjer (hvis leien også skal fordeles til flere konti), eller du kan angi samme konto, men med forskjellige dimensjonsverdikoder for avdelingsdimensjonen på hver linje.

### <a name="reversal-date-calculation"></a>Beregning av tilbakeføringsdato
Når du bruker gjentakende finanskladder til å bokføre justeringer på slutten av en periode, er det viktig å ha full kontroll over tilbakeføringsposter. På siden **Gjentakende finanskladder** gjør feltet **Beregning av tilbakeføringsdato** at du kan kontrollere datoen som tilbakeføringsposter skal bokføres på når omvendte gjentakelsesmetoder brukes.

#### <a name="example"></a>Eksempel
Justeringer bokføres vanligvis med gjentakelsesprinsippene fast, variabel eller saldo på kladdelinjen. Bokføringsdatoen for det bokførte beløpet på kontoen på kladdelinjen beregnes ved hjelp av gjentakelsesintervallet. Bokføringsdatoen for motposten beregnes ved hjelp av feltet **Beregning av tilbakeføringsdato**, som følger:

* Hvis feltet er tomt, bokføres motposten neste dag.
* Hvis feltet inneholder en datoformel (for eksempel **5D** for fem dager), bokføres motposten med en bokføringsdato som beregnes ved hjelp av beregningen av tilbakeføringsdato.

> [!NOTE]
> Feltet **Beregning av tilbakeføringsdato** er ikke tilgjengelig på siden **Gjentakende finanskladder** som standard. Hvis du vil bruke feltet, må du legge det til ved å tilpasse siden. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).

## <a name="working-with-standard-journals"></a>Arbeide med standardkladder
Når du har opprettet kladdelinjer som du vet at du sannsynligvis vil opprette igjen senere, kan du lagre dem som en standardkladd før du bokfører kladden. Denne funksjonen gjelder varekladder og finanskladder.

> [!NOTE]  
>   Den følgende fremgangsmåten dreier seg om varekladden, men informasjonen gjelder også finanskladden.

### <a name="to-save-a-standard-journal"></a>Slik lagrer du som standardkladd
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varekladder** og velg den relaterte koblingen.
2. Legg inn én eller flere kladdelinjer.
3. Velg kladdelinjene du vil bruke på nytt.
4. Velg handlingen **Lagre som standardkladd**.
5. På forespørselssiden **Lagre som standard varekladd** definerer du en ny eller eksisterende standard varekladd som linjene skal lagres i.

    Hvis du allerede har opprettet én eller flere standard varekladder og vil erstatte en av disse med det nye settet med varekladdelinjer, velger du ønsket kode i feltet Kode.
6. Velg **OK** for å bekrefte at du vil overskrive den eksisterende standardvarekladden og erstatte alt innholdet i den.
7. Velg feltet **Lagre enhetsbeløp** hvis du vil lagre verdiene i standardvarekladdens **Enhetsbeløp**-felt.
8. Velg feltet **Lagre mengde** hvis du vil at programmet skal lagre verdiene i **Antall**-feltet.
9. Velg **OK** for å lagre standardvarekladden.

Når du har lagret standardvarekladden, vises Varekladd-siden, slik at du kan fortsette med å bokføre den – i forvissning om at den enkelt kan gjenopprettes neste gang du har behov for å bokføre de samme eller lignende linjer.

### <a name="to-reuse-a-standard-journal"></a>Bruke en standardkladd på nytt

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varekladder** og velg den relaterte koblingen.
2. Velg handlingen **Hent standardkladder**.

    Siden Standard varekladder åpnes med koder og beskrivelser for alle eksisterende standard varekladder.
3. Hvis du vil se nærmere på en standard varekladd før du velger å bruke den på nytt, velger du handlingen **Vis kladd**.

    Eventuelle endringer du gjør i en standard varekladd, implementeres umiddelbart. De vil være der neste gang du åpner eller gjenbruker den aktuelle standardvarekladden. Du må derfor være sikker på at endringen er viktig nok til å gjelde generelt. I motsatt fall gjør du den ønskede endringen i varekladden etter at linjene fra standardvarekladden er satt inn. Se trinn 4 nedenfor.
4. På siden **Standard varekladder** velger du den standard varekladden du vil bruke på nytt, og deretter velger du **OK**.

    Nå er varekladden fylt med linjene som var lagret som standard varekladd. Hvis det allerede finnes kladdelinjer i varekladden, plasseres de innsatte linjene under de eksisterende kladdelinjene.

    Hvis du ikke merket av for **Lagre enhetsbeløp** da du brukte funksjonsjobben **Lagre som standard varekladd**, blir **Enhetsbeløp**-feltet på linjer du satte inn fra standardkladden, fylt ut automatisk med varens gjeldende verdi, som er kopiert fra **Enhetskost**-feltet på varekortet.

    > [!NOTE]  
    > Hvis du har valgt feltet **Lagre enhetsbeløp** eller **Lagre mengde**, må du kontrollere at de innsatte verdiene er riktige for den aktuelle lagerjusteringen før du bokfører varekladden.

    Hvis de innsatte varekladdelinjene inneholder lagrede enhetsbeløp du ikke vil bokføre, kan du raskt justere verdien til gjeldende verdi for varen, som i det følgende.

5. Velg varekladdelinjene du vil justere, og velg deretter handlingen **Beregn enhetsbeløp på nytt**. Deretter oppdateres Enhetsbeløp-feltet med gjeldende enhetskost for varen.
6. Velg handlingen **Bokfør**.

## <a name="to-renumber-document-numbers-in-journals"></a>Nummerere bilagsnumre i kladder på nytt

Hvis du vil sikre at det ikke oppstår posteringsfeil på grunn av rekkefølgen på bilagsnumrene, kan du bruke funksjonen **Nummerere bilagsnumre på nytt** før du bokfører en kladd.

I alle kladdene som er basert på finanskladden, kan feltet **Bilagsnr.** redigeres, slik at du kan angi forskjellige bilagsnumre for ulike kladdelinjer eller det samme bilagsnummeret for relaterte kladdelinjer.

Hvis feltet **Nummerserie** i den satsvise jobben for kladden er fylt ut, vil deretter posteringsfunksjonen i finanskladder kreve at bilagsnummeret på individuelle eller grupperte kladdelinjene er i sekvensiell rekkefølge. Bare velg handlingen **Nummerer dokumentnumre på nytt** så oppdateres de relevante **Dokumentnr.**-feltene. Hvis relaterte linjer ble gruppert etter bilagsnummer før du brukte funksjonen, forblir de gruppert, men kan tilordnes til et annet bilagsnummer.  

Denne funksjonen fungerer også for filtrerte visninger.

Eventuell ny nummerering av dokumenter vil respektere relaterte programmer, for eksempel en betalingsutligning som er utført fra dokumentet på kladdelinjen til en leverandørkonto. Dette betyr at feltet **Utlignings-ID** og **Utligningsbilagsnr.** i de berørte postene kan oppdateres.

### <a name="to-renumber-documents-in-journals"></a>Slik nummererer du dokumentnumre i kladder på nytt

Følgende fremgangsmåte er basert på siden **Finanskladd**, men gjelder for alle andre kladder som er basert på finanskladden, for eksempel siden **Utbetalingskladd**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finanskladder**, og velg deretter den relaterte koblingen.
2. Når du er klar til å bokføre kladden, velger du handlingen **Nummerer dokumentnumre på nytt**.

Verdier i feltet **Bilagsnr.** endres der det er nødvendig, slik at bilagsnummeret på individuelle eller grupperte kladdelinjer er i sekvensiell rekkefølge. Når dokumenter er nummerert på nytt, kan du fortsette å bokføre kladden.

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/paths/use-journals-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Bokføre transaksjoner direkte i Finans](finance-how-post-transactions-directly.md)  
[Tilbakeføre kladdebokføringer og angre mottak/leveringer](finance-how-reverse-journal-posting.md)  
[Fordele kostnader og inntekter](year-allocate-costs-income.md)  
[Finans](finance.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Lukke åpne vareposter som er resultat av fast utligning i varekladden](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
[Revaluere beholdning i revalueringskladden](inventory-how-revalue-inventory.md)  
[Telle, justere og reklassifisere lagerbeholdning ved hjelp av kladder](inventory-how-count-adjust-reclassify.md)  
[Avstem kundebetalinger med innbetalingskladden eller fra kundeposter](receivables-how-apply-sales-transactions-manually.md)  
[Avstemme leverandørbetalinger med utbetalingskladd eller fra leverandørposter](payables-how-apply-purchase-transactions-manually.md)  
[Arbeide med konserninterne dokumenter og kladder](intercompany-how-work-documents-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]