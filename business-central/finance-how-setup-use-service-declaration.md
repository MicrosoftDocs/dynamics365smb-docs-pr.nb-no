---
title: Konfigurer og bruk tjenesteerklæringsutvidelsen
description: Lær hvordan du konfigurerer og bruker funksjoner for tjenesteerklæring (Intrastat for tjenester) til å rapportere handel med selskaper i andre EU-land.
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/21/2022
ms.custom: bap-template
ms.search.keywords: 'electronic document, Intrastat, trade, EU, service, declaration,'
ms.search.form: '30, 76, 5010, 5022, 5023, 5024, 5800'
---
# <a name="the-service-declaration-extension"></a><a name="the-service-declaration-extension"></a><a name="the-service-declaration-extension"></a>Tjenesteerklæringsutvidelsen

I noen EU-land krever myndighetene at bedrifter rapporterer eksport av tjenester til andre EU-land. Med utvidelsen **Tjenesteerklæring** kan du samle inn informasjon om servicehandel i EU, og rapportere den til myndighetene. Selv om den heter **Tjenesteerklæring**, kan du også bruke den som **Intrastat for tjenester**. Denne utvidelsen er tilgjengelig for alle EU-land som en W1-versjon, og den kan brukes som den er i Belgia. For andre land kreves det en landsbasert utvidelse. Hvis et land bare trenger et annet format, kan du bruke rapportkonfigurasjonen i **datautvekslingsrammeverket** til å endre formatet.

## <a name="enable-the-service-declaration-extension"></a><a name="enable-the-service-declaration-extension"></a><a name="enable-the-service-declaration-extension"></a>Aktiver tjenesteerklæringsutvidelsen

Etter at du har installert utvidelsen i miljøet, må du aktivere den.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Funksjonsstyring**, og velg deretter den relaterte koblingen.
2. Finn **Funksjon: Aktiver bruk av tjenesteerklæring (Intrastat for tjenester)**, og velg **Alle brukere** i **Aktivert for**-feltet. Lære mer om funksjonsbehandling på [Aktivere kommende funksjoner på forhånd](/dynamics365/business-central/dev-itpro/administration/feature-management) i administrasjonsinnholdet.
3. Når du aktiverer funksjonen, må du utføre trinn i oppsettsprosessen gjennom installasjonsveiviseren. De fleste feltene er konfigurert som standard.
4. Legg bare til **Tjenestetransaksjonstyper** i det andre trinnet ved å velge alternativet **Åpne siden for tjenestetransaksjonstyper for å angi en liste med koder**.
5. Før du starter, må du kontrollere **totalt antall koder** for å forstå hvor mange tjenestetransaksjonstyper allerede er angitt.
6. Velg **Fullfør** i det siste trinnet for å fullføre konfigurasjonen.

## <a name="set-up-the-service-declaration-extension"></a><a name="set-up-the-service-declaration-extension"></a><a name="set-up-the-service-declaration-extension"></a>Konfigurer tjenesteerklæringsutvidelsen

Du kan konfigurere utvidelsen manuelt eller ved å bruke en rapporteringsfil i datautvekslingsdefinisjoner.

### <a name="to-set-up-service-declaration-manually"></a><a name="to-set-up-service-declaration-manually"></a><a name="to-set-up-service-declaration-manually"></a>Slik konfigurerer du tjenesteerklæring manuelt

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Oppsett av tjenesteerklæring**, og velg deretter den relaterte koblingen.
2. Konfigurer feltene som beskrevet i tabellen nedenfor, i hurtigfanen **Generelt**:

    |Felt  |Description  |
    |---------|---------|
    |**Erklæringsnummerserie**     | Angir nummerserien som skal brukes til å tildele ID-er til nye poster.        |
    |**Rapporter varegebyr**  | Angir om varegebyr må rapporteres. Hvis det er aktivert, kontrollerer [!INCLUDE [prod_short](includes/prod_short.md)] tjenestetransaksjonskoden for varegebyrer og inkluderer dem i tjenesteerklæringer.        |
    |**Kundenr. for salg til / faktura til**     | Angir kunden som skal brukes til å sammenligne landskoden med landskoden på siden **Selskapsinformasjon**. Bare dokumenter der disse to kodene er forskjellige, inkluderes i tjenesteerklæringen.<br><br>* **Faktura til.**: Bruk landskoden fra **Faktura til-kunden** < br<br>* **Salg til.**: Bruk landskoden fra **Salg til-kunden**.        |
    |**Leverandørnr. for kjøp fra / betal til**  | Angir hvilken leverandør som skal brukes til å sammenligne landskoden med landskoden fra siden **Selskapsinformasjon**. Bare dokumenter der disse to kodene er forskjellige, inkluderes i tjenesteerklæringen.<br><br> * **Kjøp fra**: Bruk landskoden fra **Kjøp fra-leverandøren**. <br><br> * **Betal til.**: Bruk landskoden fra **Betal til-leverandøren**.         |
    |**Kode for datautveksl.def.**  | Angir koden for datautvekslingsdefinisjonen som brukes til å generere den eksporterte filen for tjenesteerklæringen.        |
    |**Aktiver organisasjonsnr.**     |  Angir om **organisasjonsnummeret** er aktivert for tjenesteerklæringen.       |

3. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Tjenestetransaksjonstyper**, og velg deretter den relaterte koblingen.
4. På linjene angir du **koder** og **beskrivelser** for tjenestetransaksjonstypene du skal bruke.

### <a name="set-up-a-reporting-file"></a><a name="set-up-a-reporting-file"></a><a name="set-up-a-reporting-file"></a>Konfigurere en rapporteringsfil

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Datautvekslingsdefinisjoner**, og velg deretter den tilknyttede koblingen.
2. Velg handlingen **Ny**.
3. I hurtigfanen **Generelt** beskriver du datautvekslingsdefinisjonen ved å angi datafiltypen, kolonneskilletegnet, relaterte codeunits, XMLport og fylle ut de andre feltene.
4. På hurtigfanen **Linjedefinisjoner** beskriver du formateringen av linjer i datafilen ved å fylle ut feltene basert på **Linjetype**-feltet, og hvor du må definere antall kolonner for denne linjen.
5. På hurtigfanen **Kolonnedefinisjoner** fyller du ut linjen for hver planlagte kolonne.
6. Velg handlingen **Felttilordning** på hurtigfanen **Linjedefinisjoner** for å åpne siden **Felttilordning**.
7. Opprett en ny post, og velg riktig **Tabell-ID** (for **Tjenesteerklæringslinje** velger du **5024**) på hurtigfanen **Generelt**, og fyll deretter ut feltene slik:
   1. I feltet **Nøkkelindeks** angir du nøkkelindeksen som kildeoppføringene skal sorteres etter, før eksport.
   2. Velg **Codeunit for tildeling**.
8. I hurtigfanen **Felttilordning** legger du til kolonnene du konfigurerte tidligere, i hurtigfanen **Kolonnedefinisjoner**, og deretter legger du til følgende:
   1. Angi **Felt-ID** for hver kolonne.
   2. Angi **Transformeringsregelen** for hver kolonne etter behov. Regelen omdanner importert tekst til en verdi som støttes, før den kan tildeles til et angitt felt i [!INCLUDE[prod_short](includes/prod_short.md)]. Når du velger en verdi i dette feltet, blir den nøyaktige verdien angitt i feltet for **Transformeringsregel** i **Buffer for felttilordning for datautveksl.** -tabellen og omvendt.
9. Hvis du vil gruppere poster basert på kolonner, velger du feltene du vil bruke til gruppering, på hurtigfanen **Feltgruppering**.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] inneholder en forhåndskonfigurert datautvekslingsdefinisjon for **tjenesteerklæring** for alle lokaliserte land. Finn ut mer om oppretting av en ny datautvekslingsdefinisjon i [Definer datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md).

## <a name="other-related-configurations"></a><a name="other-related-configurations"></a><a name="other-related-configurations"></a>Andre relaterte konfigurasjoner

Før du bruker tjenesteerklæringsutvidelsen, må du konfigurere noen felter for varer, ressurser og varegebyrer.

### <a name="items"></a><a name="items"></a><a name="items"></a>Varer

Konfigurer informasjon som er knyttet til tjenesteerklæringen, på varekortsider:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.
2. Velg elementet du vil konfigurere.
3. Utvid hurtigfanen **Vare**, og konfigurer følgende felter:
   1. I feltet **Type** velger du **Tjeneste**.
   2. I feltet **Kode for tjenestetransaksjonstype** angir du koden for en **tjenestetransaksjonstype**.
   3. Hvis du ikke vil inkludere denne servicevaren i tjenesteerklæringer, velger du feltet **Utelat fra tjenesteerklæring**.

### <a name="resources"></a><a name="resources"></a><a name="resources"></a>Ressurser

Konfigurer informasjon som er knyttet til tjenesteerklæringen, på ressurskortsider:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Ressurser** og velg den relaterte koblingen.
2. Velg ressursen du vil konfigurere.
3. Utvid hurtigfanen **Generelt**, og konfigurer følgende felter:
   1. I feltet **Kode for tjenestetransaksjonstype** angir du koden for en **tjenestetransaksjonstype**.
   2. Hvis du ikke vil inkludere denne ressursen i tjenesteerklæringer, velger du feltet **Utelat fra tjenesteerklæring**.

### <a name="item-charges"></a><a name="item-charges"></a><a name="item-charges"></a>Varegebyrer

Konfigurer informasjon som er knyttet til tjenesteerklæringen, for varegebyrer:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varegebyr** og velg den relaterte koblingen.
2. Velg varegebyret du vil konfigurere.
3. I feltet **Kode for tjenestetransaksjonstype** angir du koden for en **tjenestetransaksjonstype**.
4. Hvis du ikke vil inkludere denne varegebyret i tjenesteerklæringer, velger du feltet **Utelat fra tjenesteerklæring**.

## <a name="create-new-service-declaration"></a><a name="create-new-service-declaration"></a><a name="create-new-service-declaration"></a>Opprett ny tjenesteerklæring

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Tjenesteerklæringer**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. Fyll ut følgende felter på hurtigfanen **Generelt**:
    1. I feltet **Konfigurasjonskode** angir du konfigurasjonskoden som brukes til å foreslå linjer og opprette filer. Du må velge en som en **tjenesteerklæring**.
    2. I feltene **Startdato** og **Sluttdato** angir du start- og sluttdatoene for perioden som skal tas med i tjenesteerklæringen.
4. Velg handlingen **Foreslå linjer** for å starte en kjørsel som samler inn linjer fra dokumenter og fyller ut tjenesteerklæringslinjene.

Kjørselen henter alle poster fra gjeldende kjøps- og salgsdokumenter i perioden du har behov for, og legger dem til på tjenesteerklæringslinjene. Hold markøren over feltene i linjer for å lese en kort beskrivelse.

## <a name="modify-a-service-declaration"></a><a name="modify-a-service-declaration"></a><a name="modify-a-service-declaration"></a>Endre en tjenesteerklæring

Om nødvendig kan du endre linjene eller legge til nye.

1. På siden **Tjenesteerklæring** velger du **Ny linje**-handlingen i hurtigfanen **Linjer**.
2. I feltet **Dokumenttype** velger du alternativet knyttet til dokumentet du vil bruke.
3. Basert på **dokumenttypen** fyller du ut feltet **Dokumentnr.**.
4. Fyll ut feltene som gjenstår.

## <a name="overview-the-service-declaration-lines"></a><a name="overview-the-service-declaration-lines"></a><a name="overview-the-service-declaration-lines"></a>Oversikt over tjenesteerklæringslinjene

Når du har opprettet en tjenesteerklæring, bruker du handlingen **Oversikt** til å få en oversikt over tjenesteerklæringslinjene. Du kan gruppere og summere linjene på samme måte som den eksporterte filen. Du kan også åpne linjene i Excel.

## <a name="report-service-declaration-in-a-file"></a><a name="report-service-declaration-in-a-file"></a><a name="report-service-declaration-in-a-file"></a>Rapporter tjenesteerklæring i en fil

Du kan sende tjenesteerklæringen som en fil basert på kravene til lokale myndigheter. Slik oppretter du en fil:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Tjenesteerklæringer**, og velg deretter den relaterte koblingen.
2. Velg tjenesteerklæringen du vil rapportere som en fil.
3. Hvis du ikke allerede har gjort det, fyller du ut tjenesteerklæringen manuelt eller velger handlingen **Foreslå linjer**.
4. Velg handlingen **Opprett fil**.
5. Tjenesteerklæringsfilen lagres i påkrevd format.

## <a name="other-considerations"></a><a name="other-considerations"></a><a name="other-considerations"></a>Andre hensyn

Når du bruker utvidelsen **Tjenesteerklæring**, er det flere ting å tenke på. Det er for eksempel viktig at gruppene samsvarer med krav fra myndigheter. Det er også viktig at tjenestene er inkludert på riktig måte i salgs- og kjøpsdokumenter.

### <a name="grouping-lines"></a><a name="grouping-lines"></a><a name="grouping-lines"></a>Grupperingslinjer

På tjenesteerklæringslinjer finnes det ingen gruppering av noen felter. Alle poster kopieres fra det opprinnelige dokumentet som en kilde.

Gruppering som kreves av myndighetene, vil bli oppgitt i den eksporterte filen. Du må konfigurere gruppene i **datautvekslingsdefinisjonen**, som kan konfigureres fullstendig. Finn ut mer under [Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md).

### <a name="using-services-in-document-lines"></a><a name="using-services-in-document-lines"></a><a name="using-services-in-document-lines"></a>Bruk av tjenester i dokumentlinjer

Når du oppretter en kjøps-, salgs- eller servicefaktura, finner du to felter som er knyttet til tjenesteerklæringer i linjene. Begge feltene fylles ut med standardverdiene fra vare-, ressurs- eller varegebyroppsettene.

- **Kode for tjenestetransaksjonstype** – angir koden for en tjenestetransaksjonstype.
- **Kan bruke tjenesteerklæring** – angir om en vare eller ressurs kan bruke en tjenesteerklæring.

Du kan endre verdiene i disse feltene, men hvis du velger feltet **Kan bruke tjenesteerklæring**, må du angi en verdi i feltet **Kode for tjenestetransaksjonstype**. Hvis du ikke gjør det, kan du ikke bokføre dokumentet.

Hvis du angir en verdi i feltet **Kode for tjenestetransaksjonstype**, men ikke velger feltet **Kan bruke tjenesteerklæring**, kan du bokføre dokumentet, men linjen blir ikke beregnet når du gjør det.

## <a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Konfigurer Intrastat-rapportering](finance-how-setup-report-intrastat.md)
[Intrastat-rapportering i Business Central](finance-how-report-intrastat.md)  
[Økonomistyring](finance.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
