---
title: Foreta betalinger med AMC-bank (USA) eller SEPA-kredittoverføring (EU)
description: Behandle betalinger til leverandører ved å eksportere en fil (EFT) sammen med betalingsinformasjonen fra kladdelinjene.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '256, 1205, 1206, 1209, 10810, 10811'
ms.date: 07/17/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Foreta betalinger med utvidelsen AMC banking 365 fundamentals eller SEPA-kredittoverføring

På **siden Utbetalingskladder** kan du behandle betalinger til leverandørene ved å eksportere en fil sammen med betalingsinformasjonen fra kladdelinjene. Du kan deretter laste opp filen til nettbanken der de relaterte pengeoverføringene behandles. [!INCLUDE[prod_short](includes/prod_short.md)] støtter SEPA-kredittoverføringsformatet, men i landet/området ditt kan andre formater for elektroniske betalinger være tilgjengelige.

> [!NOTE]
> I den generelle versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] er det konfigurert og koblet til en global tjenesteleverandør for å konvertere bankdata til hvilket som helst format banken krever. I versjonene for Nord-Amerika kan den samme servicen brukes til å sende betalingsfiler som elektronisk pengeoverføring (EFT), for eksempel det ofte brukte ACH-nettverket (Automated Clearing House), men med en litt annerledes prosess. Se trinn 6 i [Slik eksporterer du betalinger til en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).  

 Hvis du vil gjøre det mulig å foreta SEPA-kredittoverføringer, må du først opprette en bankkonto, en leverandør og finanskladden som utbetalingskladden er basert på. Deretter klargjør du betalinger til leverandører ved automatisk å fylle ut **Utbetalingskladder-siden** med forfalte betalinger med angitte bokføringsdatoer.  

> [!NOTE]  
> Når du har bekreftet at betalingene er behandlet av banken, kan du begynne å bokføre utbetalingskladdelinjene.  

## Konfigurere AMC Banking 365 Fundamentals-utvidelsen

Aktiver utvidelsen AMC Banking 365 Fundamentals for å konvertere en kontoutdragsfil til et format du kan importere, eller konvertere den eksporterte betalingsfilen til formatet som banken krever. Hvis du vil ha mer informasjon, kan du se [Bruk AMC Banking 365 Fundamentals-utvidelsen](ui-extensions-amc-banking.md).

## Definere SEPA-kredittoverføring

Fra **siden Betalingskladder kan du eksportere betalinger** til en fil for opplasting til den elektroniske banken for behandling av de tilknyttede pengeoverføringene. [!INCLUDE[prod_short](includes/prod_short.md)] støtter SEPA-kredittoverføringsformatet, men i landet/området ditt kan andre formater for elektroniske betalinger være tilgjengelige.  

Hvis du vil aktivere eksport av et bankfilformat som ikke støttes som standard [!INCLUDE[prod_short](includes/prod_short.md)], kan du konfigurere en datautvekslingsdefinisjon ved hjelp av rammeverket for datautveksling. Hvis du vil ha mer informasjon, kan du se [Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md)  

Før du kan behandle betalingen elektronisk ved å eksportere betalingsfiler i formatet for SEPA-kredittoverføring, må du utføre følgende konfigureringstrinn:  

* Definer den aktuelle bankkontoen slik at den kan håndtere SEPA-kredittoverføringsformatet.  
* Definer leverandørkort slik at betalinger behandles ved å eksportere filer i SEPA-kredittoverføringsformatet.  
* Definere den tilknyttede finanskladden for å aktivere betalingseksport fra **Betalingskladder-siden**   
* Knytt datautvekslingsdefinisjon for én eller flere betalingstyper til de(n) aktuelle betalingsmåten(e):  

> [!NOTE]
> Business Central støtter både SEPA-format CT-smerte.001.001.03 og CT-smerter.001.001.09. Du kan velge hvilket som helst format på **bankkonto kort-siden** .  
> [!TIP]
> Denne artikkelen gjelder den generelle versjonen av [!INCLUDE [prod_short](includes/prod_short.md)]. I ditt land eller din region kan flere nødvendige felt ha blitt lagt til på de ulike sidene. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### Slik oppretter du en bankkonto for SEPA-kredittoverføring:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bankkontoer**, og velg deretter den relaterte koblingen.  
2. Åpne kort til bankkontoen du vil eksportere betalingsfiler fra, i SEPA-kredittoverføringsformatet.  
3. Velg **SEPA-formatet du vil bruke, i** feltet Betalingseksportformat **på hurtigfanen Kontoinnehaver** .  
4. I hurtigfanen **Generelt** i feltet **Numre på kredittoverføringsmeldinger**, velger du en nummerserie som tilordnes til SEPA-kreditoverføringer.  
5. Kontroller at **IBAN**-feltet er utfylt.  

    > [!NOTE]  
    > **EUR** må angis i **Valutakode**-feltet fordi SEPA-kredittoverføringer bare kan foretas i euro.  

### Slik oppretter du et leverandørkort for SEPA-kredittoverføring:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Leverandører** og velger den relaterte koblingen.  
2. Åpne kortet for leverandøren som du vil betale elektronisk, ved å eksportere betalingsfiler i formatet for SEPA-kredittoverføring.  
3. Velg **BANK** **i feltet Betalingsmåte - kode** på **hurtigfanen Betalinger**.  
4.  **I feltet Foretrukket bankkonto** velger du banken som pengene skal overføres til når de behandles av den elektroniske banken.  

    Hvis du ennå ikke har definert en bank for denne leverandøren, kan du gjøre det nå. Hvis du vil ha mer informasjon, kan du se [Definere bankkonti for eksport av bankfiler](bank-how-setup-bank-accounts.md#to-set-up-vendor-bank-accounts-for-export-of-bank-files). Verdien i feltet **Foretrukket bankkonto** overføres til feltet **Mottakerbankkonto** på siden **Utbetalingskladd**.  

### Slik definerer du utbetalingskladden for eksport av betalingsfiler:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Utbetalingskladder** og velg den relaterte koblingen.  
2. Velg rulle\-gardinknappen i **Bunkenavn**-feltet.  
3. På siden **Finanskladder** velger du handlingen **Rediger liste**.  
4. På linjen for betalingskladden du skal bruke til å eksportere betalinger, Velg du avmerkingsboksen **Tillat betalingseksport** .  

### Slik knytter du datautvekslingsdefinisjon for én eller flere betalingstyper til de(n) aktuelle betalingsmåten(e):

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Betalingsmåter**, og velg deretter den relaterte koblingen.  
2. På siden **Betalingsmåter** velger du betalingsmåten som brukes til å eksportere betalinger fra, og deretter velger du feltet **Definisjon av betalingseksportlinje**.  
3. På siden **Definisjoner av betalingseksportlinje** velger du koden du angav i **Kode**-feltet på hurtigfanen **Linjedefinisjoner** i trinn 4 i delen "Slik beskriver du formateringen av linjer og kolonner i filen" i fremgangsmåten [Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md).  

## Klargjøre utbetalingskladden

Fylle ut utbetalingskladden med linjer for utestående leverandørfordringer, med mulighet til å sette inn bokføringsdatoer basert på forfallsdatoen til de relaterte kjøpsdokumentene. Hvis du vil ha mer informasjon, kan du se [Administrere skyldige beløp](payables-manage-payables.md).

## Eksportere betalinger til en bankfil

Når du er klar til å foreta utbetalinger til leverandørene eller refusjoner til de ansatte, kan du eksportere en fil med betalingsinformasjonen på linjene på **Betalingskladder-siden** . Du kan deretter laste opp filen til banken for å behandle de relaterte pengeoverføringene.

AMC Banking 365 Fundamentals-utvidelsen er tilgjengelig i den generelle versjonen av [!INCLUDE[prod_short](includes/prod_short.md)]. I Nord-Amerika-versjoner kan den samme utvidelsen brukes til å sende betalingsfiler som elektronisk pengeoverføring (EFT), men med en litt annen prosess. Se trinn 6 i [Slik eksporterer du betalinger til en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).

> [!NOTE]  
> Før du kan eksportere betalingsfiler fra betalingsjournalen, må du angi det elektroniske formatet for bankkontoen som er involvert, og du må aktivere AMC Banking 365 Fundamentals-utvidelsen. Hvis du vil ha mer informasjon, kan du se [Konfigurere bankkontoer](bank-how-setup-bank-accounts.md) og [Bruk AMC Banking 365 Fundamentals-utvidelsen](ui-extensions-amc-banking.md). I tillegg må du merke av for **Tillat betalingseksport** på siden **Finanskladder**. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).  

Du bruker siden **Kredittoverføringsregistre** til å vise betalingsfilene som er eksportert fra betalingskladden. Fra denne siden kan du også eksportere betalingsfiler på nytt ved tekniske feil eller endringer. Vær imidlertid oppmerksom på at eksporterte EFT-filer ikke vises på denne siden og ikke kan eksporteres på nytt.  

### Slik eksporterer du betalinger til en bankfil:

Nedenfor beskrives hvordan du betaler en leverandør med sjekk. Fremgangsmåten er lik refusjon til kunde med sjekk.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Utbetalingskladder** og velg den relaterte koblingen.
2. Fyll ut utbetalingskladdelinjene. Hvis du vil ha mer informasjon, kan du se [Registrere betalinger og refusjoner](payables-how-post-payments-refunds.md).

    > [!NOTE]
    > Hvis du bruker EFT, må du velge enten **Elektronisk betaling** eller **Elektronisk betaling-IAT** i feltet **Bankbetalingstype**. Andre fileksporttjenester og formater krever ulike oppsettsverdier på siden **Bankkort** og **Leverandørs bankkort**. Du blir informert om feil eller manglende oppsettsverdier når du prøver å eksportere filen.
    >
    > EFT-funksjonen kan bare brukes for bankkonti i lokal valuta. Den kan ikke brukes med utenlandsk valuta, angitt med en verdi i feltet **Valutakode**. (Tom feltverdi betyr lokal valuta.)

3. Når du har fullført alle betalingskladdlinjene, velger du **Eksporter**.
4. På siden **Eksporter elektroniske betalinger** fyller du ut feltene etter behov.

    Eventuelle feilmeldinger vises i faktaboksen **Feil i betalingsfil**, der du også kan velge en feilmelding hvis du vil ha mer informasjon. Du må løse alle feil før betalingsfilen kan eksporteres.

    > [!TIP]  
    > Når du bruker AMC Banking 365 Fundamentals-utvidelsen, kan du få en vanlig feilmelding om at bankkontonummeret ikke har lengden som banken krever. Du kan unngå eller løse feilen ved å fjerne verdien i **IBAN**-feltet på siden **Bankkort** og deretter angi et bankkontonummer i formatet som banken krever, i feltet **Bankkontonr.**

5. På siden **Lagre som** angir du plasseringen som filen som blir eksportert til, og deretter velger du **Lagre**.

    > [!NOTE]  
    > Hvis du bruker EFT, lagrer du det resulterende remitteringsskjemaet for leverandører som et Word-dokument, eller du velger at det skal sendes direkte til leverandøren via e-post. Betalingene er nå lagt til på siden **Generer EFT-fil**, og derfra kan du generere flere betalingsordrer sammen for å spare overføringskostnader. Hvis du vil ha mer informasjon, kan du se følgende trinn.
6. På **siden Utbetalingskladder** velger du handlingen **Generer EFT-fil** .

    På siden **Generer EFT-fil** vises alle betalinger som er definert for EFT som du har eksportert fra utbetalingskladden for en bestemt bankkonto, men som ennå ikke er generert på hurtigfanen **Linjer**.
7. Velg **Generer EFT-fil** for å eksportere en fil for alle EFT-betalinger.
8. På siden **Lagre som** angir du plasseringen som filen som blir eksportert til, og deretter velger du **Lagre**.

Bankbetalingsfilen eksporteres til plasseringen du angir, og du kan deretter laste den opp til nettbankkontoen og foreta de faktiske betalingene. Deretter kan du bokføre den eksporterte betalingen journallinjer.

### Planlegge når du bokfører eksporterte betalinger

Hvis du ikke vil bokføre en betalingskladdelinje for en eksportert betaling, for eksempel fordi du venter på bekreftelse på at transaksjonen er behandlet av banken, kan du bare slette kladdelinjen. Når du senere oppretter en utbetalingskladdelinje for å betale restbeløpet på fakturaen, viser feltet **Totalt eksportert beløp** hvor mye av betalingsbeløpet som allerede er eksportert. Du kan også finne detaljert informasjon om det eksporterte totalbeløpet ved å velge knappen **Poster i kredittoverføringsreg.** for å vise mer informasjon om eksporterte betalingsfiler.

Hvis du følger en prosess der du ikke bokfører betalinger før du har fått bekreftet at betalingene er behandlet i banken, kan du kontrollere dette på to måter.

* I en betalingskladd med foreslåtte betalingslinjer kan du sortere etter **kolonnen Eksportert til betalingsfil** eller **Totalt eksportert beløp**, og deretter slette betalingsforslag for åpne fakturaer som det allerede er foretatt betalinger for, og du ikke vil foreta betalinger for.
* På **siden Betalingsforslag fra leverandør**, der du angir hvilke betalinger som skal settes inn i betalingskladden, kan du Velg avmerkingsboksen **Hopp over eksporterte betalinger** hvis du ikke vil sette inn kladdelinjer for betalinger som allerede er eksportert.

Du kan vise informasjon om eksporterte betalinger ved å velge handlingen **Historikk for betalingseksport**.

### Eksportere betalinger til en bankfil på nytt

Du kan eksportere betalingsfiler på nytt fra siden **Kredittoverføringsregistre**. Før du sletter eller bokfører betalingskladdelinjer, kan du også eksportere betalingsfilen på nytt fra **Betalingskladder-siden** ved å eksportere den på nytt. Hvis du sletter eller bokfører betalingskladdelinjene etter at du har eksportert, kan du eksportere den samme betalingsfilen på nytt fra **siden Kredittoverføringsjournaler** . Velg linjen for bunken med kredittoverføringer du vil eksportere på nytt, og bruk handlingen **Eksporter betalinger til fil på nytt**.

> [!NOTE]  
> Eksporterte EFT-filer vises ikke på siden **Kredittoverføringsregistre** og kan ikke eksporteres på nytt.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kredittoverføringsregistre**, og velg deretter den relaterte koblingen.
2. Velg en betalingseksport som du vil eksportere på nytt, og velg deretter **Eksporter betaling til fil på nytt**.

## Bokføring av betalinger

Bokfør betalingene når den elektroniske betalingen er behandlet av banken. Hvis du vil ha mer informasjon, kan du se [Utføre betalinger](payables-make-payments.md).

## Se også

[Bruk utvidelsen AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)  
[Administrere skyldige beløp](payables-manage-payables.md)  
[Arbeid med finanskladder](ui-work-general-journals.md)  
[Innkrev betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
