---
title: Arbeide med finanskladder for å bokføre direkte i Finans
description: 'Finn ut hvordan du bruker kladder til å bokføre finanstransaksjoner på finanskonti og andre konti, for eksempel bank-, kunde- og leverandørkonti.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 04/12/2024
ms.custom: bap-template
ms.search.keywords: 'journals, recurring, accrual, renumber, bulk-post'
ms.search.form: '39, 101, 102, 182, 184, 185, 201, 207, 250, 251, 253, 255, 256, 261, 262, 283, 519, 750, 751, 752, 753, 754, 755, 12409, 12410, 12411, 1290, 10101, 11400, 11402, 11403, 11405, 11300, 2000000, 2000001, 2000003, 2000020, 2000021, 2000022'
---
# <a name="work-with-general-journals"></a>Arbeid med finanskladder

De fleste finanstransaksjoner bokføres i Finans via dokumenter, for eksempel kjøpsfakturaer eller ordrer. Du kan imidlertid også behandle forretningsaktiviteter som:

* Kjøp
* Betalinger
* Bruk av gjentakende kladder til å bokføre avsetninger
* Refundering av ansattutgifter ved å bokføre kladdelinjer i kladder  

De fleste kladder er basert på finanskladden, og du kan behandle alle transaksjonene på siden **Finanskladd**. Finn ut mer på [Bokfør transaksjoner direkte i Finans](finance-how-post-transactions-directly.md).  

Du kan for eksempel bruke Bokfør ansattutgifter for refusjon. Finn ut mer på [Registrere og refundere ansattes utgifter](finance-how-record-reimburse-employee-expenses.md).

[!INCLUDE [prod_short](includes/prod_short.md)] tilbyr også kladder som er tilpasset for bestemte typer transaksjoner, som **Utbetalingskladd**, til å registrere betalinger. Finn ut mer under [Registrere betalinger og refusjoner i utbetalingskladden](payables-how-post-payments-refunds.md).  

Du bruker finanskladder til å bokføre finanstransaksjoner til finanskontoer og ulike andre kontoer. De andre kontoene inkluderer bank-, kunde-, leverandør- og ansattkontoer. Bokføring med en finanskladd oppretter poster på finanskontoer selv om du for eksempel bokfører en kladdelinje for en kundekonto. Posten bokføres på en samle konto for finans via en bokføringsgruppe.

Opplysningene du angir i en kladd, er midlertidige og kan endres mens de fortsatt befinner seg i kladden. Når du bokfører kladden, overføres opplysningene til poster i individuelle konti, der de ikke kan endres. Du kan imidlertid oppheve utligningen av bokførte poster, og du kan bokføre tilbakeførings- eller korrigeringsposter. Finn ut mer under [Tilbakefør kladdebokføringer og angre mottak/leveringer](finance-how-reverse-journal-posting.md).

> [!NOTE]
> [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]  

## <a name="add-context-to-general-journal-transactions"></a>Legg til kontekst i finanskladdetransaksjoner

Når du oppretter en kladd, kan du legge til koblinger som gir kontekst til transaksjonene. Når du bokfører kladden, kopierer [!INCLUDE [prod_short](includes/prod_short.md)] koblingene til den bokførte kladden og postene som kladden oppretter. Hvis du for eksempel oppgir koblinger, kan det bli enklere for revisoren. Hvis du oppbevarer bilder av utgiftskvitteringene på selskapets Sharepoint-nettsted, kan du legge til koblinger til filene. Når du bokfører kladden for å sende inn utgiftene, kan revisoren raskt få tilgang til kvitteringsfilene.

## <a name="use-journal-templates-and-batches"></a>Bruk kladder og kladdemaler

Det finnes flere finanskladdemaler. Hver kladdemal er representert på en egen side med bestemte funksjoner og feltene som er nødvendige for å støtte disse funksjonene, for eksempel siden **Betalingsavstemmingskladd** for å behandle betalinger og **Betalingskladd** for å betale leverandører eller gi ansatte refusjon. Finn ut mer under [Foreta betalinger](payables-make-payments.md) og [Avstem kundebetalinger med innbetalingskladden eller fra kundeposter](receivables-how-apply-sales-transactions-manually.md).

Du kan definere dine egne personlige kladder som en kladd for hver enkelt kladdemal. Du kan for eksempel definere din egen kladd for betalingskladden som har personlig oppsett og innstillinger. Tipset nedenfor er et eksempel på hvordan du kan tilpasse en kladd.

> [!TIP]  
> Hvis du merker av for **Foreslå motkontobeløp** på linjen for den kladden på siden **Finanskladder**, vil deretter for eksempel **Beløp**-feltet på finanskladdelinjer for samme dokumentnummer, automatisk forhåndsutfylles med verdien som kreves for å balansere dokumentet. Finn ut mer under [La [!INCLUDE[prod_short](includes/prod_short.md)] foreslå verdier](ui-let-system-suggest-values.md).

> [!TIP]
> Du kan legge til eller fjerne felter i kladder ved å tilpasse dem. Finn ut mer under [Tilpass arbeidsområdet](ui-personalization-user.md).

### <a name="validating-general-journal-batches"></a>Validere finanskladder

Du kan aktivere en bakgrunnskontroll som bidrar til å forhindre forsinkelser ved bokføring. Sjekken gir deg beskjed når en feil i finanskladden du arbeider på, hindrer deg i å bokføre kladden. På siden **Finanskladd** kan du velge **Bakgrunnsfeilkontroll** for at [!INCLUDE[prod_short](includes/prod_short.md)] skal validere finanskladder, for eksempel finans- eller utbetalingskladder, mens du arbeider med dem.

Når du aktiverer valideringen, viser faktaboksen **Kladdkontroll** feil i nåværende linje og i hele kladden. Valideringen skjer når du laster inn en finanskladd, og når du velger en annen kladdelinje. Flisen **Totalt antall problemer** i faktaboksen viser totalt antall problemer som [!INCLUDE[prod_short](includes/prod_short.md)] har funnet, og du kan velge den for å åpne en oversikt over problemene.

Du kan bruke handlingene **Vis linjer med problemer** og **Vis alle linjer** for å veksle mellom kladdelinjer som har eller ikke har problemer. Faktaboksen **Kladdelinjedetaljer** gir rask oversikt over og tilgang til data fra kladdelinjer, for eksempel finanskonto, kunde eller leverandør samt bokføringsoppsettet for bestemte kontoer.

[!INCLUDE [background_doc_journal_check](includes/background_doc_journal_check.md)]  

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Forstå hovedkontoer og motkontoer

Hvis du definerte standard motkontoer for kladdene, blir motkontoen på siden **Finanskladder** fylt ut automatisk når du fyller ut **Kontonr.**-feltet. Hvis ikke fyller du ut feltene **Kontonr.** og **Motkontonr.** manuelt. Et positivt beløp i **Beløp**-feltet debiteres hovedkontoen og krediteres motkontoen. Et negativt beløp krediteres hovedkontoen og debiteres motkontoen.

> [!NOTE]  
> Mva beregnes separat for hovedkontoen og motkontoen, så de kan bruke ulike mva-prosentsatser.

## <a name="work-with-recurring-journals"></a>Arbeid med gjentakelseskladder

En gjentakende kladd er en finanskladd med spesifikke felter for håndtering av transaksjoner du bokfører ofte, med få eller ingen endringer. Det kan for eksempel være transaksjoner for utgifter som leie, abonnementer, elektrisitet og varme. Ved hjelp av gjentakende kladder kan du bokføre faste og variable beløp og angi automatiske tilbakeføringsposter for dagen etter bokføringsdatoen. Med tildelingsnøkler kan du også dele gjentakende poster mellom flere kontoer. Finn ut mer under [Fordele gjentakelseskladden til flere kontoer](#allocating-recurring-journal-amounts-to-several-accounts).

Når kladden er en gjentakende kladd, oppretter du postene som du bokfører jevnlig, én gang. Kontoer, dimensjoner og dimensjonsverdier og så videre blir for eksempel liggende i kladden etter bokføring. Hvis det trengs endringer, kan du gjøre det hver gang du bokfører.

### <a name="recurring-method-field"></a>Feltet Gjentakelsesprinsipp

Feltet **Gjentakelsesprinsipp** er viktig. Det angir hvordan beløpet på kladdelinjen skal behandles etter bokføring. Du kan for eksempel velge å la beløpet stå hvis du skal bruke samme beløp hver gang du bokfører linjen. Hvis du vil bruke samme konto og tekst på linjen, men vil at beløpet varierer hver gang du bokfører, kan du slette beløpet etter bokføring.

| Til | Se |
| --- | --- |
|F Fast|Beløpet på kladdelinjen blir stående etter bokføring. Linjer med beløp på null beholdes i kladden, men bokføres ikke. Du kan oppdatere beløpet i en senere kjøring.  |
|V Variabel|Beløpet på kladdelinjen slettes etter bokføring.|
|S Saldo|Det bokførte beløpet i kontoen på linjen fordeles til kontoene som er angitt for linjen, i tabellen Fordeling. Saldoen på kontoen blir nullstilt. Husk å fylle ut feltet **Andel i pst.** på siden **Fordelinger**. Hvis du vil ha mer informasjon, kan du se [Fordeler gjentakelseskladden til flere konti](#allocating-recurring-journal-amounts-to-several-accounts).|
|FT Fast med tilbakeføring|Beløpet på kladdelinjen består etter bokføring og en motpost bokføres på den etterfølgende dato.|
|VT Variabel med tilbakeføring|Beløpet på kladdelinjen blir slettet etter bokføring og en motpost bokføres på den etterfølgende dato.|
|ST Saldo med tilbakeføring|Det bokførte beløpet i kontoen på linjen blir fordelt til kontoene som er angitt for linjen, på siden **Fordelinger**. Saldoen på kontoen blir satt til null, og en motpost bokførtes på den etterfølgende datoen.|
|BD-saldo etter dimensjon|Kladdelinjen fordeler kostnader på grunnlag av saldoen på en finanskonto per dimensjon. Du blir bedt om å angi at dimensjonsfiltrene skal brukes til å beregne saldoen på finanskontoen per dimensjon som du vil fordele kostnader fra. Du kan eventuelt velge handlingen **Angi dimensjonsfiltre** senere.|
|RBD Saldo med tilbakeføring etter dimensjon|Kladdelinjen fordeler kostnader på grunnlag av saldoen med tilbakeføring på en finanskonto per dimensjon. Du blir bedt om å angi at dimensjonsfiltrene skal brukes til å beregne saldoen på finanskontoen per dimensjon som du vil fordele kostnader fra. Du kan også velge handlingen **Angi dimensjonsfiltre** senere.|

> [!NOTE]  
> Mva. feltene kan fylles ut på gjentakelseskladdelinjen eller på fordelingskladdelinjen, men aldri på begge. Det vil si at disse feltene bare kan fylles ut på siden **Fordelinger** hvis tilsvarende linjer i gjentakelseskladden ikke er fylt ut.

### <a name="recurring-frequency-field"></a>Feltet Gjentakelsesintervall

Dette datoformelfeltet angir hvor ofte posten på kladdelinjen skal bokføres, og det må fylles ut. Finn ut mer under [Bruk datoformler](ui-enter-date-ranges.md#use-date-formulas).

#### <a name="examples"></a>Eksempler

Hvis kladdelinjen skal bokføres hver måned, setter du inn **1M**. Etter hver bokføring vil datoen i feltet **Bokføringsdato** bli oppdatert til samme dato neste måned.

Hvis du vil bokføre en post på den siste dagen i hver måned, kan du gjøre en av følgende handlinger:

* Bokfør den første post siste dag i måneden ved å angi 1D+1M-1D (1 dag + 1 måned - 1 dag). Ved hjelp av denne formelen beregnes bokføringsdatoen riktig uansett hvor mange dager det er i måneden.

* Bokfør den første posten på hvilken som helst dag i måneden ved å angi 1M+NM. Ved hjelp av denne formelen vil bokføringsdatoen være etter én hel måned, pluss de resterende dagene av denne måneden.

### <a name="expiration-date-field"></a>Feltet Utløpsdato/-klokkeslett

Dette feltet angir når linjen skal bokføres for siste gang. Linjen tas ikke med i bokføringen etter denne datoen.

Fordelen med å bruke feltet Utløpsdato er at linjen ikke slettes fra kladden med en gang. Du kan angi en senere dato slik at du kan bruke linjen i fremtiden.

Hvis feltet er tomt, bokføres linjen hver gang du bokfører, helt til du sletter den fra kladden.

### <a name="allocating-recurring-journal-amounts-to-several-accounts"></a>Fordele gjentakelseskladden til flere kontoer

På siden **Gjentakende finanskladd** kan du velge **Fordelinger**-handlingen for å angi hvordan beløp på gjentakelseskladdelinjen skal tildeles flere kontoer og dimensjoner. Tildeling fungerer som motkontolinje til gjentakende kladdelinje.

I likhet med gjentakende kladder angir du en tildeling én gang, og den forblir i tildelingskladden etter bokføring. Du trenger ikke å angi beløp og tildelinger hver gang du bokfører gjentakende kladdelinje.

Hvis **Saldo** eller **Saldo med tilbakeføring** er angitt for det gjentakende prinsippet i den gjentakende kladden, tas det ikke hensyn til dimensjonsverdikoder i den gjentakende kladden når kontoen nullstilles. Hvis du i tildelingskladden fordeler en gjentakelseskladdelinje til dimensjonsverdier på siden **Fordelinger**, blir det bare opprettet én post i tilbakeføringen.

> [!NOTE]
> Du må ikke angi samme kode på siden **Tildelinger** hvis du fordeler en gjentakende kladdelinje som inneholder en dimensjonsverdikode. Hvis du gjør det, vil dimensjonsverdiene bli feile.  

Hvis du vil tildele gjentakende kladdebeløp basert på dimensjoner, setter du feltet **Gjentakelsesprinsipp** til **Saldo etter dimensjon** eller **Saldo med tilbakeføring etter dimensjon**. Hvis **Saldo etter dimensjon** eller **Saldo med tilbakeføring etter dimensjon** er angitt for det gjentakende prinsippet i den gjentakende kladden, tas det hensyn til dimensjonsverdikoder i den gjentakende kladden når kontoen nullstilles. Hvis du tildeler en gjentakende linje til dimensjonsverdier på **Tildelinger**-siden, opprettes det tilbakeførende poster som samsvarer med antall dimensjonsverdikombinasjoner som saldoen består av. Hvis du fordeler kontosaldoen gjennom en gjentakende kladd som inneholder en dimensjonsverdikode, må du huske å bruke **Saldo etter dimensjon** eller **Saldo med tilbakeføring etter dimensjon** for å sikre at dimensjonsverdiene balanseres eller tilbakeføres riktig fra kildekontoen.  

Det kan for eksempel være at selskapet ditt har et par konsern og noen avdelinger som kontrollører definerte som dimensjoner. Når du skal registrere kjøpsfakturaen raskere, bestemmer du deg for å kreve at leverandørens assistenter bare skal fylle ut konserndimensjoner. Ettersom hver forretningsenhet har spesifikke fordelingsnøkler for avdelingsdimensjonen, for eksempel basert på antall ansatte, kan du bruke de gjentakende metodene **BD Saldo etter dimensjon** eller **RBD Saldo med tilbakeføring etter dimensjon** for å tildele utgifter på nytt for hvert konsern, til de riktige avdelingene basert på tildelingsnøklene.  

> [!NOTE]
> Dimensjoner du angir på tildelinglinjer, beregnes ikke automatisk, og du må angi hvilke dimensjonsverdier som skal angis på tildelingskontoene. Hvis du vil beholde koblingen mellom kildekontodimensjonen og fordelingskontodimensjonen, anbefaler vi at du bruker [Kostregnskap](finance-about-cost-accounting.md)-funksjonene i stedet.

#### <a name="example-allocating-rent-payments-to-different-departments"></a>Eksempel: Fordele leiebetalinger til ulike avdelinger

Husleie betales månedlig, så du angir beløpet i kassakontoen på en gjentakende kladdelinje. På siden **Tildelinger** kan du bruke dimensjonen Avdeling til å fordele utgiftene på flere avdelinger. I henhold til antall kvadratmeter som hver avdeling opptar, kan dette for eksempel være kvadratfot. Beregningen er basert på tildelingsprosenten på hver linje. Du kan tildele på ulike måter:

* Angi ulike kontoer på ulike tildelingslinjer for å dele leieutgift på flere kontoer.
* Angi samme konto, men bruk forskjellige dimensjonsverdikoder for Avdeling-dimensjonen på hver linje.

[!INCLUDE [rev-general-journal](includes/rev-general-journal.md)]

### <a name="calculate-the-reversal-date"></a>Beregn tilbakeføringsdatoen

Når du bruker gjentakende finanskladder til å bokføre justeringer på slutten av en periode, er det viktig å ha full kontroll over tilbakeføringsposter. På siden **Gjentakende finanskladder** gjør feltet **Beregning av tilbakeføringsdato** at du kan kontrollere datoen som tilbakeføringsposter bokføres på når omvendte gjentakelsesmetoder brukes.

#### <a name="example"></a>Eksempel

Justeringer bokføres vanligvis med gjentakelsesprinsippene **fast**, **variabel** eller **saldo** på kladdelinjen. Bokføringsdatoen for det bokførte beløpet på kontoen på kladdelinjen beregnes ved hjelp av gjentakelsesintervallet. Bokføringsdatoen for motposten beregnes ved hjelp av feltet **Beregning av tilbakeføringsdato**, som følger:

* Hvis feltet er tomt, bokføres motposten neste dag.
* Hvis feltet inneholder en datoformel (f.eks. **5D** for fem dager), bokføres motposten med en bokføringsdato som beregnes ved hjelp av beregningen av tilbakeføringsdato.

> [!NOTE]
> Feltet **Beregning av tilbakeføringsdato** er ikke tilgjengelig på siden **Gjentakende finanskladder** som standard. Hvis du vil bruke feltet, må du legge det til ved å tilpasse siden. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).

## <a name="work-with-standard-journals"></a>Arbeid med standardkladder

Når du oppretter kladdelinjer som du vet at du sannsynligvis vil opprette igjen senere, kan du lagre dem som en standardkladd før du bokfører kladden. Det samme gjelder varekladder og finanskladder.

> [!NOTE]
> Standardkladder kan ikke inneholde alle feltene du vil ta med i postene som opprettes. Hvis du for eksempel bruker en standard finanskladd til å registrere en betaling, inneholder ikke postene feltet Betalingsmåte – kode.

> [!NOTE]  
> Den følgende fremgangsmåten dreier seg om varekladden, men informasjonen gjelder også finanskladden.

### <a name="to-save-a-standard-journal"></a>Slik lagrer du som standardkladd

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varekladder** og velg den relaterte koblingen.
2. Legg inn én eller flere kladdelinjer.
3. Velg kladdelinjene du vil bruke på nytt.
4. Velg handlingen **Lagre som standardkladd**.
5. På forespørselssiden **Lagre som standard varekladd** definerer du en ny eller eksisterende standard varekladd som linjene skal lagres i.

    Hvis du har en eller flere standard varekladder og vil erstatte en av dem med det nye settet med varekladdelinjer, velger du varekladden i feltet **Kode**.
6. Velg **OK** for å bekrefte at du vil erstatte innholdet i den eksisterende standardvarekladden.
7. Hvis du vil lagre verdiene i feltet **Enhetsbeløp** i standardvarekladden, velger du **Lagre enhetsbeløp**-felt.
8. Hvis du vil lagre verdiene i feltet **Antall**, velger du **Lagre antall**-feltet.
9. Velg **OK** for å lagre standardvarekladden.

Når du lagrer standardvarekladden, vises siden Varekladd slik at du kan bokføre den.

### <a name="to-reuse-a-standard-journal"></a>Bruke en standardkladd på nytt

> [!NOTE]
> Standardkladder har ikke alltid de samme feltene som finanskladder. Når du bruker handlingen Hent standardkladd til å kopiere feltene til finanskladden, kan finanskladden ha mer informasjon enn hvis du opprettet den manuelt. 

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varekladder** og velg den relaterte koblingen.
2. Velg handlingen **Hent standardkladder**.
3. Hvis du vil se nærmere på en standard varekladd før du velger å bruke den på nytt, velger du handlingen **Vis kladd**.

    Endringer som gjøres i en standard varekladd, implementeres umiddelbart, og det tas vare på endringene til neste gang du åpner standardvarekladden eller bruker den på nytt. Vær sikker på at endringen er viktig nok til å gjelde generelt. I motsatt fall gjør du den ønskede endringen i varekladden etter at linjene fra standardvarekladden er lagt til. Se trinn 4.
4. På siden **Standard varekladder** velger du den standard varekladden du vil bruke på nytt, og deretter velger du **OK**.

    Varekladden inneholder linjene du lagret. Hvis det allerede finnes linjer i varekladden, vises de nye linjene etter dem.

    Hvis du ikke slo på vekslebryteren **Lagre enhetsbeløp** da du lagret kladden, inneholder feltet **Enhetsbeløp** på linjer som er lagt til fra standard kladden, verdien fra feltet **Enhetskost** på varekortet.

    > [!NOTE]  
    > Hvis du har slo på vekslebryterne **Lagre enhetsbeløp** eller **Lagre antall** da du lagret kladden, må du kontrollere at de nye verdiene er riktige før du bokfører varekladden.
    >
    > Hvis de innsatte varekladdelinjene inneholder lagrede enhetsbeløp du ikke vil bokføre, kan du justere verdien til gjeldende verdi for varen.

5. Velg varekladdelinjene du vil justere, og velg deretter handlingen **Beregn enhetsbeløp på nytt**. Denne handlingen oppdaterer Enhetsbeløp-feltet med gjeldende enhetskost for varen.
6. Velg handlingen **Bokfør**.

## <a name="to-renumber-document-numbers-in-journals"></a>Nummerere bilagsnumre i kladder på nytt

Hvis du vil unngå bokføringsfeil på grunn av rekkefølgen på bilagsnumrene, kan du bruke handlingen **Nummerer bilagsnumre på nytt** før du bokfører en kladd.

I alle kladdene som er basert på finanskladden, kan feltet **Bilagsnr.** redigeres, slik at du kan angi forskjellige bilagsnumre for ulike kladdelinjer eller det samme bilagsnummeret for relaterte kladdelinjer.

Hvis feltet **Nummerserie** i den satsvise jobben for kladden er fylt ut, vil deretter posteringsfunksjonen i finanskladder kreve at bilagsnummeret på individuelle eller grupperte kladdelinjene er i sekvensiell rekkefølge. Bare velg handlingen **Nummerer dokumentnumre på nytt** så oppdateres de relevante **Dokumentnr.**-feltene. Hvis relaterte linjer grupperes etter bilagsnummer før du brukte funksjonen, forblir de gruppert, men kan tildeles til et annet bilagsnummer.  

Denne funksjonen fungerer også for filtrerte visninger.

Ny nummerering av dokumenter respekterer relaterte programmer, for eksempel en betalingsutligning som er utført fra dokumentet på kladdelinjen til en leverandørkonto. Dette betyr at feltet **Utlignings-ID** og **Utligningsbilagsnr.** oppdateres på finanspostene.

### <a name="to-renumber-documents-in-journals"></a>Slik nummererer du dokumentnumre i kladder på nytt

Følgende fremgangsmåte er basert på siden **Finanskladd**, men gjelder for alle andre kladder som er basert på finanskladden, for eksempel siden **Utbetalingskladd**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finanskladder**, og velg deretter den relaterte koblingen.
2. Når du er klar til å bokføre kladden, velger du handlingen **Nummerer dokumentnumre på nytt**.

Verdier i feltet **Bilagsnr.** endres der det er nødvendig, slik at bilagsnummeret på individuelle eller grupperte kladdelinjer er i sekvensiell rekkefølge. Når dokumenter er nummerert på nytt, kan du bokføre kladden.

## <a name="see-also"></a>Se også

[Bokfør transaksjoner direkte i finans](finance-how-post-transactions-directly.md)  
[Tilbakefør kladdebokføringer og angre mottak/leveringer](finance-how-reverse-journal-posting.md)  
[Fordele kostnader og inntekter](year-allocate-costs-income.md)  
[Finans](finance.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Lukke åpne vareposter som er resultat av fast utligning i varekladden](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
[Revaluere beholdning i revalueringskladden](inventory-how-revalue-inventory.md)  
[Telle, justere og reklassifisere lagerbeholdning ved hjelp av kladder](inventory-how-count-adjust-reclassify.md)  
[Avstem kundebetalinger med innbetalingskladden eller fra kundeposter](receivables-how-apply-sales-transactions-manually.md)  
[Avstemme leverandørbetalinger med utbetalingskladd eller fra leverandørposter](payables-how-apply-purchase-transactions-manually.md)  
[Arbeide med konserninterne dokumenter og kladder](intercompany-how-work-documents-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
