---
title: Definer Intrastat-rapportering
description: Denne artikkelen forklarer hvordan du konfigurerer Intrastat-rapporteringsfunksjoner for å rapportere handel med selskaper i andre EU-land.
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 04/05/2023
ms.custom: bap-template
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077'
---
# <a name="set-up-intrastat-reporting"></a><a name="set-up-intrastat-reporting"></a><a name="set-up-intrastat-reporting"></a>Definer Intrastat-rapportering

Alle selskaper i EU må rapportere handel med andre EU-land/-regioner. Varebevegelsen må hver måned rapporteres til statistikkmyndighetene i landet/regionen der selskapet befinner seg, og rapporten må leveres til skattemyndighetene. Intrastat er et system som brukes til å samle inn handelsstatistikk om varer i disse landene/områdene. Bruk Intrastat-rapporten til å fylle ut periodisk Intrastat-rapportering ved å samle inn, registrere og rapportere handelen av varer i henhold til lokal lovgivning.

Intrastat-rapportering er basert på standard EU-forskrifter som gjelder for alle land. Det er imidlertid forskjeller i de enkelte landene. Hvert land har regler om hva og hvordan det skal rapporteres.

> [!NOTE]
> Intrastat-informasjon gjelder ikke flytting av tjenester mellom land. Informasjonen gjelder i stedet bare varer som varer og aktiva. Hvis den lokale regjeringen krever at du registrerer flytting av tjenester mellom land, kan du bruke funksjonen **Tjenestedeklarasjon**.
>
> Denne funksjonen er tilgjengelig fra november 2022 som en app du kan laste ned fra [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646). Hvis du vil bruke denne funksjonen, må du installere den på siden **Administrasjon av utvidelse**.

> [!IMPORTANT]
> Denne artikkelen dekker den nye Intrastat-funksjonen som er tilgjengelig fra [!INCLUDE[prod_short](includes/prod_short.md)], versjon 21. Kontakt administratoren for å finne ut hvilken versjon selskapet bruker, og om du skal aktivere den nye funksjonaliteten.
>
> Les den forrige versjonens Intrastat-oppsett og bruksartikkel [Konfigurer og rapporter Intrastat](finance-how-setup-report-intrastat-v20.md).

## <a name="enable-the-new-intrastat-experience"></a><a name="enable-the-new-intrastat-experience"></a><a name="enable-the-new-intrastat-experience"></a>Aktivere den nye Intrastat-opplevelsen

I lanseringsbølge 2 i 2022 inkluderer [!INCLUDE[prod_short](includes/prod_short.md)] en Intrastat-funksjon med ny utforming som leverer utvidede funksjoner. Hvis den nye Intrastat-funksjonaliteten ikke er aktivert i miljøet ditt, kan en administrator aktivere den på siden **Funksjonsstyring**.

> [!IMPORTANT]
> Du kan ikke bruke gamle og nye funksjoner parallelt. Før du aktiverer utvidelsen i et produksjonsmiljø, anbefaler vi at du tester den i et sandkassemiljø ved å bruke en kopi av produksjonsdataene. Etter at du aktiverer en ny brukeropplevelse i produksjonsmiljøet, kan du ikke gå tilbake til den gamle Intrastat-funksjonaliteten.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Funksjonsstyring**, og velg deretter den relaterte koblingen.
2. På siden **Funksjonsstyring** velger du linjen for **Funksjonsoppdatering: Erstatt den eksisterende Intrastat-funksjonaliteten med den nye Intrastat-utvidelsen**. Hvis du vil finne ut mer om funksjonsstyring, kan du se [Aktiver kommende funksjoner på forhånd](/dynamics365/business-central/dev-itpro/administration/feature-management).
3. Velg **Alle brukere** i kolonnen **Aktiver for**.
4. Les forklaring om hvordan systemet blir oppgradert, og velg deretter **Ja** for å godta.
5. Velg **Neste**. Du får det grunnleggende oppsettet for Intrastat. Hvis du vil lese mer om Intrastat-oppsettet, kan du se delen [Intrastat-konfigurasjon](#intrastat-configuration) senere i denne artikkelen.
6. Når oppsettet er fullført, velger du **Fullfør** for å begynne å bruke den nye Intrastat-opplevelsen.

    > [!NOTE]
    > Avhengig av selskapets lokasjon er det nok å aktivere funksjonen beskrevet tidligere. For land som har bestemte funksjoner for Intrastat-rapportering, må du aktivere den landspesifikke Intrastat-appen i tillegg til kjerneutvidelsen.

## <a name="intrastat-configuration"></a><a name="intrastat-configuration"></a><a name="intrastat-configuration"></a>Intrastat-konfigurasjon

Før du kan bruke Intrastat-rapporter er det flere konfigurasjoner som må defineres.

### <a name="intrastat-reporting-setup"></a><a name="intrastat-reporting-setup"></a><a name="intrastat-reporting-setup"></a>Intrastat-rapporteringsoppsett

Bruk siden **Intrastat-rapporteringsoppsett** til å aktivere og angi standardvirkemåte for Intrastat-rapportering. Du kan angi om du må rapportere Intrastat fra forsendelser (utsendelser), mottak (ankomster) eller begge deler, avhengig av terskler som er angitt i dine lokale forskrifter. Du kan også angi standard transaksjonstyper for vanlige dokumenter og returdokumenter som brukes til transaksjonsrapportering.

Følg denne fremgangsmåten for å konfigurere Intrastat-rapportering.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Oppsett for Intrastat-rapport**, og velg deretter den relaterte koblingen.
2. På hurtigfanen **Generelt** velger eller angir du feltinformasjon etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Tabellen nedenfor beskriver noen av nøkkelfeltene.

   | Felt | Description |
   | --- | --- |
   | **Rapporter kvitteringer** | Angir at du må inkludere ankomster av mottatte varer i Intrastatrapporter. |
   | **Rapportleveringer** | Angir at du må inkludere leveringer av sendte varer i Intrastatrapporter. |
   | **Leveringer basert på**  | Angir landskoden basert på hvilke Intrastat-rapportlinjer som er brukt.  |
   | **Org.nr. basert på** | Angir kunde- eller leverandørkoen basert på hvilket merverdinummer (mva.) som er brukt for Intrastat-rapporten.  |
   | **Registrert org.nr. mva. for selskap** | Angir hvordan selskapets organisasjonsnummer eksporteres til Intrastat-filen.  |
   | **Registrert org.nr. mva. for leverandør** | Angir hvordan en leverandørs organisasjonsnummer eksporteres til Intrastat-filen.  |
   | **Registrert org.nr. mva. for kunde** | Angir hvordan en kundes organisasjonsnummer eksporteres til Intrastat-filen.  |
   | **Hent mva. for partner for** | Angir hvilken type Intrastat-rapportlinje partnerens organisasjonsnummer oppdateres fra. Avhengig av hvilke lokale krav du har, kan du bare velge mottakslinjer, bare velge leveringslinjer eller begge typer linjer. |

3. På hurtigfanen **Standardtransaksjoner** velger eller angir du feltinformasjon etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Tabellen nedenfor beskriver noen av nøkkelfeltene.

   | Felt | Description |
   | --- | --- |
   | **Standard trans.art** | Angir standard transaksjonsart for vanlige følgesedler, servicefølgesedler og kjøpsmottak. |
   | **Standard trans.art – returer** | Angir standard transaksjonsart for ordrereturer, servicereturer og kjøpsreturer. |
   | **Standard mva-nr. for privatperson** | Angir standard mva-nummer for privatperson hvis privatpersonen må ha et eget mva-nummer på Intrastat-rapporten. |
   | **Standard mva-nr. for tredjepartshandel** | Angir standard tredjeparts mva-nummer hvis du ikke har mva-nummeret. |
   | **Standard-mva. for ukjent delstat** | Angir standard mva-nummer for en ukjent delstat. |
   | **Standard lands-/områdekode** | Angir standard mottakslandskode. |

4. På hurtigfanen **Rapportering** velger eller angir du feltinformasjonen etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Tabellen nedenfor beskriver noen av nøkkelfeltene.

   | Felt | Description |
   | --- | --- |
   | **Kode for datautveksl.def.** | Angir koden for datautvekslingsdefinisjonen for å generere Intrastat-filen. Dette feltet er bare tilgjengelig hvis feltet **Del mottaks-/leveringsfiler** er satt til **Nei**. |
   | **Del mottaks-/leveringsfiler** | Angir om mottak og leveringer skal rapporteres i to separate filer. |
   | **ZIP-fil(er)** | Angir om rapportfilene skal legges til i ZIP-filen. |
   | **Kode for datautveksl.def. – mottak** | Angir koden for datautvekslingsdefinisjonen for å generere Intrastat-filen for mottatte vare. Dette feltet er bare tilgjengelig hvis feltet **Del mottaks-/leveringsfiler** er satt til **Ja**. |
   | **Kode for datautveksl.def. – levering** | Angir koden for datautvekslingsdefinisjonen for å generere Intrastat-filen for sendte varer. Dette feltet er bare tilgjengelig hvis feltet **Del mottaks-/leveringsfiler** er satt til **Ja**. |

5. På hurtigfanen **Nummerering** angir du verdien i feltet **Intrastat-numre**.

### <a name="set-up-a-reporting-file"></a><a name="set-up-a-reporting-file"></a><a name="set-up-a-reporting-file"></a>Konfigurere en rapporteringsfil

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Datautvekslingsdefinisjoner**, og velg deretter den tilknyttede koblingen.
2. Velg **Opprett**, og angi deretter informasjon om datautvekslingsdefinisjonen, datafiltypen, kolonneskilletegnet, relaterte codeunits, XMLport og andre felt ved behov på hurtigfanen **Generelt**.
3. På hurtigfanen **Linjedefinisjoner** angir du en verdi i feltet **Linjetype** for å beskrive formateringen av linjer i datafilen og hvor du må definere antall kolonner for denne linjen.
4. På hurtigfanen **Kolonnedefinisjoner** fyller du ut linjen for hver planlagte kolonne. Du kan definere kolonnenavn, datatyper (som tekst, dato eller desimal), lengden på linjen med fast bredde, som inneholder kolonnen hvis filen er av typen *Fast tekst*, og noen andre parametere.
5. Velg **Felttildeling** på hurtigfanen **Linjedefinisjoner**.
6. Opprett en ny post på siden **Felttildeling**. 
7. På hurtigfanen **Generelt** velger du verdien **Tabell-ID** (for **Intrastat-rapportlinje** velger du **4812**) og angir følgende feltinformasjon:

   1. Angi nøkkelindeksen for å sortere kildeoppføringene før eksport i feltet **Nøkkelindeks**.
   2. Velg en verdi i feltet **Codeunit for tildeling**.

8. I hurtigfanen **Felttildeling** legger du til kolonnene som du konfigurerte tidligere, i hurtigfanen **Kolonnedefinisjoner**, og deretter legger du til følgende:

   1. Angi verdien **Felt-ID** for hver kolonne.
   2. Angi verdien **Transformeringsregelen** for hver kolonne etter behov. Verdien angir regelen som omdanner importert tekst til en støttet verdi før den kan tildeles til et angitt felt i [!INCLUDE[prod_short](includes/prod_short.md)]. Når du velger en verdi i dette feltet, blir den nøyaktige verdien angitt i feltet for **Transformeringsregel** i **Buffer for felttilordning for datautveksl.** tabellen. (Når du velger en verdi i dette feltet, blir den nøyaktige verdien angitt i feltet for **Transformeringsregel** i **Buffer for felttildeling for datautveksl.** tabellen, velges en verdi i dette feltet.)

9. Hvis du må gruppere poster basert på noen kolonner, velger du feltene du vil bruke til gruppering, på hurtigfanen **Feltgruppering**.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] inneholder den forhåndskonfigurerte datautvekslingsdefinisjonen for Intrastat for alle lokaliserte land. Hvis du vil finne ut mer om hvordan du oppretter en ny datautvekslingsdefinisjon, kan du se [Definer datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md).

### <a name="set-mandatory-fields-with-the-intrastat-report-checklist"></a><a name="set-mandatory-fields-with-the-intrastat-report-checklist"></a><a name="set-mandatory-fields-with-the-intrastat-report-checklist"></a>Angi obligatoriske felt med sjekklisten for Intrastat-rapport

I noen land krever skattemyndighetene at Intrastat-rapporter for eksempel må inkludere leveringsmåten for kjøp eller andre verdier ved salg over en viss grense.

Følg denne fremgangsmåten for å angi obligatoriske felter eller verdier på siden **Intrastat-rapport**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Oppsett for Intrastat-rapport**, og velg deretter den relaterte koblingen.
2. Velg **Sjekkliste for Intrastat-rapport**.
3. Følg denne fremgangsmåten for å legge til de nødvendige linjene for kontroll:
   1. Angi feltet **Feltnr.** til et felt som må kontrolleres for en verdi som ikke er tom.
   2. Angi en verdi i feltet **Filteruttrykk** basert på følgende regler:

        1. Når du åpner **filtersiden**, velger du filteret du må bruke for kontrollen.
        2. Velg en verdi som er knyttet til det valgte filteret.
        3. Hvis du må fylle flere filtre for det valgte feltet, gjentar du de forrige to trinnene for å legge til et annet filter.
        4. Når du er ferdig med å angi filtrene for det valgte feltet, velger du **OK**.

   3. Merk av for **Tilbakeført filteruttrykk** for å angi at kontrollen for felter bare kjøres på linjene som ikke samsvarer med filteruttrykket. Hvis linjen ikke filtreres, ignoreres dette feltet.

> [!NOTE]
> Når du åpner linjen **Filterside** fra linjen **Filteruttrykk**, kan du bruke alle standard filteruttrykk som er knyttet til det bestemte feltet du vil filtrere.
>
> Vær forsiktig når du definerer valideringsregler ettersom de kan være forskjellige mellom land.

## <a name="use-custom-codeunits-in-intrastat-reporting"></a><a name="use-custom-codeunits-in-intrastat-reporting"></a><a name="use-custom-codeunits-in-intrastat-reporting"></a>Bruke egendefinerte codeunits i Intrastat-rapportering

Hvis du vil endre hvordan Intrastat fungerer og standardkonfigurasjonen ikke er nok, kan du tilpasse systemet ved å utvide standardfunksjonene. Hvis du må endre virkemåten for Intrastat ytterligere, kan du utvikle egne codeunits. Når du oppretter codeunits, må du foreta flere endringer for å bruke dem. Følg denne fremgangsmåten for å konfigurere systemet til å bruke dine egne objekter.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konfigurasjon av mva-rapporter**, og velg deretter den relaterte koblingen.
2. Legg til en ny linje på **Konfigurasjon av mva-rapporter**-siden.
3. I feltet **Mva-rapporttype** velger du **Intrastat-rapport**.
4. I feltet **Versjon av mva-rapport** angir du hvilken versjon av rapporten.
5. Legg til codeunits for følgende alternativer:
   1. I feltet **Codeunit-ID for Foreslå linjer** angir du den nye codeuniten for å foreslå linjer i Intrastat-rapportens linjer.
   2. I feltet **Codeunit-ID for innhold** angir du den nye codeuniten for å eksportere data som en fil ved hjelp av en datautvekslingsdefinisjon.
   3. I feltet **Valider codeunit-ID** angir du den nye codeuniten for valideringsresultater i Intrastat-rapportens linjer.

> [!IMPORTANT]
> Denne linjen må være tom hvis du bruker standard codeunits. Du bør bare opprette en linje og konfigurere den hvis du har utviklet egendefinerte codeunits.

## <a name="other-intrastat-configurations"></a><a name="other-intrastat-configurations"></a><a name="other-intrastat-configurations"></a>Andre Intrastat-konfigurasjoner

Kundekort og leverandørkort inneholder feltet **Intrastat-partnertype** som har samme alternativverdier som feltet **Partnertype**: 

- "" (tom)
- *Selskap*
- *Person*
    
Feltet **Intrastat-partnertype** erstattet feltet **Partnertype** i Intrastat-rapportering. Feltet **Partnertype** brukes i området SEPA (Single EURO Payments Area) for å definere (SEPA) til å definere SEPA Direct Debit Scheme (Core eller B2B). Feltet **Intrastat-partnertype** brukes bare til Intrastat-rapportering. Derfor kan du angi ulike verdier for de to feltene, hvis du trenger det.

Hvis feltet **Intrastat-partnertype** er tomt, brukes verdien fra feltet **Partnertype** til Intrastat-rapportering.

I tillegg til **Oppsett for Intrastat-rapport**, **Datautvekslingsdefinisjon** og **Sjekkliste for Intrastat-rapport** må følgende innstillinger konfigureres.

| Side | Description |
| ---- | ----------- |
| **Land/områder** | På siden **Land/områder** legger du til informasjonen **Lands-/områdekode for EU** og **Intrastat-kode** for å angi en kode for landet/området du handler med. Denne informasjonen blir bruk i Intrastat-rapportering. |
| **Tariffnumre** | I mange land lager toll- og skattemyndighetene åttesifrede koder for ulike varer. Hvis du vil gjøre at vareposter inneholder den nødvendige informasjonen når programmet importerer dem til Intrastat-kladdelinjen, må du angi varekoden på siden **Tariffnumre**. Finn kodene for varene som selskapet ditt handler med, og angi dem på **Tariffnumre**-siden. |
| **Transportmåter** | Det finnes sju ensifrede koder for Intrastat-transportmetoder: **1** for båt, **2** for jernbane, **3** for bil, **4** for fly, **5** for post **7** for faste installasjoner og **9** for egen fremdrift (for eksempel transportere en bil ved å kjøre den). [!INCLUDE[prod_short](includes/prod_short.md)] krever ikke disse spesifikke kodene. Vi anbefaler imidlertid at beskrivelsene formidler en lignende betydning. |
| **Transaksjonsarter** | Land og regioner har forskjellige koder for Intrastat-transaksjonstyper, for eksempel vanlig kjøp, salg, utveksling av returnerte varer og utveksling av ikke-returnerte varer. Definer alle kodene som gjelder for landet/regionen. Disse kodene brukes deretter på hurtigfanen **Utenrikshandel** på salgs- og kjøpsdokumenter, og når du behandler returer. |
| **Transaksjonsspesifikasjoner** | Definer koder for å supplere transaksjonstypebeskrivelsene. |
  
> [!NOTE]
> Fra og med januar 2022 krever Intrastat forskjellig transaksjonskoder for fordeling til private enkeltpersoner eller ikke-mva-registrerte selskaper og mva-registrerte selskaper. For å overholde dette kravet anbefaler vi at du ser gjennom eller legger til nye transaksjonskoder på siden **Transaksjonstyper** i henhold til kravene i ditt land. Du bør også kontrollere og oppdatere feltet **Intrastat-partnertype** til *Personer* for private eller ikke-mva-selskapers forretningskunder på den relevante **Kunde**-siden. Hvis du er usikker på hvilken Intrastat-partnertype eller transaksjonstype som er riktig å bruke, anbefaler vi at du spør en ekspert i landet eller området ditt.

|   Felt   |   Description   |
| --------- | --------------- |
| **Nettovekt** | Vekt er en av de grunnleggende konfigurasjonene som er knyttet til Intrastat-rapportering, fordi totalvekt er obligatorisk for rapportering. For å være klar for dette kravet må du angi en verdi i feltet **Nettovekt** på vare- eller aktivumkortet. |
| **Kode for opprinnelsesland** | Bruk de to bokstavers ISO alfa-kodene på elementet eller aktivakortet for landet der varen ble anskaffet eller produsert. Hvis varen ble produsert i mer enn ett land, er opprinnelseslandet det siste landet der det ble behandlet betraktelig. |
| **Mva-nummer for partneroperatøren i medlemslandet for importen** | Dette mva-nummer for partneroperatøren i medlemslandet for importen. Mva-ID-en brukes også i utvekslingen av data mellom EU-eksport mellom medlemslandene, og tillater at medlemsland fordeler de mottatte dataene til importselskapet i sitt eget land. Rapporteringsenheter må rapportere mva-ID-en til selskapet som deklarerer den intra-unionhenting av varer i medlemslandet for import. |

Du kan også konfigurere følgende:

* **Varekoder**: Toll- og skattemyndighetene har laget numeriske koder som klassifiserer varer og tjenester. Du kan angi disse kodene for varene.
* **Områder**: Supplerende informasjon om land og regioner.
* **Inn-/utpunkt**: Angi lokasjonene der du leverer eller mottar varer til eller fra andre land. En flyplass er et eksempel på et inn-/utpunkt. Du angir inn-/utpunkt på hurtigfanen **Utenrikshandel** i salgs- og kjøpsdokumenter. Denne informasjonen kopieres fra varepostene når du oppretter Intrastat-kladden.
* **Supplerende enhet**: Antall varer for Intrastat-rapportering kan være enten nettovekt (i kilo) eller en tilleggsenhet. Hvis det kreves tilleggsenheter, må du konfigurere dem for varer og aktiva.

#### <a name="set-up-transport-methods"></a><a name="set-up-transport-methods"></a><a name="set-up-transport-methods"></a>Definere transportmåter

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Transportmåter**, og velg deretter den relaterte koblingen.
2. Fyll ut feltinformasjonen etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="set-up-transaction-nature-codes"></a><a name="set-up-transaction-nature-codes"></a><a name="set-up-transaction-nature-codes"></a>Definere transaksjonskoder

1. velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Transaksjonstyper**, og velg deretter den relaterte koblingen.
2. Fyll ut feltinformasjonen etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="other-related-configurations"></a><a name="other-related-configurations"></a><a name="other-related-configurations"></a>Andre relaterte konfigurasjoner

Før du bruker funksjonen for Intrastat-rapportering, må du definere felter på vare-, aktiva-, kunde- og leverandørkortene.

#### <a name="item-cards"></a><a name="item-cards"></a><a name="item-cards"></a>Varekort

Følg denne fremgangsmåten for å konfigurere alle nødvendige opplysninger som er knytet til Intrastat på varekort.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.
2. Velg elementet du vil konfigurere.
3. På hurtigfanen **Kostnader og bokføring** angir du en verdi i feltene **Tariffnr.**, **Supplerende enhet** og **Kode for opprinnelsesland/-område**.

    > [!NOTE]
    > Hvis du vil bruke en enhet som tillegg for grunnenheten, konfigurerer du supplerende enhet på siden **Vareenheter**.

4. På hurtigfanen **Beholdning** angir du en verdi i desimalformat i feltet **Nettovekt**.

> [!NOTE]
> Når du legger til tariffnummeret for en enhet som er definert for varen, fyller [!INCLUDE [prod_short](includes/prod_short.md)] automatisk ut feltet **Supplerende enhet** basert på tariffnummerkonfigurasjonen. Du kan endre feltet **Supplerende enhet** etter behov.

#### <a name="set-up-fixed-assets-for-intrastat"></a><a name="set-up-fixed-assets-for-intrastat"></a><a name="set-up-fixed-assets-for-intrastat"></a>Definer aktiva for Intrastat

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Aktiva**, og velg deretter den relaterte koblingen.
2. Velg aktivaet du vil konfigurere.
3. I hurtigfanen **Intrastat** angir du en verdi i feltene **Tariffnummer**, **Nettovekt** og **Supplerende enhet**.

> [!NOTE]
> Du kan bruke forskjellige enheter som tilleggsenhet. Men uansett **Enhetskode** du velger, vil **Antall** i Intrastat alltid være 1.

#### <a name="set-up-vendors-for-intrastat"></a><a name="set-up-vendors-for-intrastat"></a><a name="set-up-vendors-for-intrastat"></a>Konfigurer leverandører for Intrastat

Før du kan ta med en leverandør i Intrastat-rapportering, angir du opplysningene på siden **Leverandørkort**. Angi for eksempel en verdi for **Lands-/områdenummer** og en verdi for **Organisasjonsnr.**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Leverandører** og velg den relaterte koblingen.
2. Velg leverandøren du vil konfigurere.
3. På hurtigfanen **Intrastat** kan du angi en standardverdi for feltene **Standard trans.art**, **Standard trans.art – returer** og **Standard transportmåte**.
4. Utvid hurtigfanen **Betalinger**, og velg feltet **Intrastat-partnertype**, og angi om leverandøren er en person eller et selskap.

#### <a name="set-up-customers-for-intrastat"></a><a name="set-up-customers-for-intrastat"></a><a name="set-up-customers-for-intrastat"></a>Konfigurer kunder for Intrastat

Før du kan ta med en kunde i Intrastat-rapportering, angir du opplysningene på siden **Kundekort**. Du må for eksempel angi en verdi for **Lands-/områdenummer** og en verdi for **Organisasjonsnr.**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kunder** og velger den relaterte koblingen.
2. Velg kunden du vil konfigurere.
3. På hurtigfanen **Intrastat** kan du angi standardverdien for feltene **Standard trans.art**, **Standard trans.art – returer** og **Standard transportmåte**.
4. Utvid hurtigfanen **Betalinger**, og velg feltet **Intrastat-partnertype**, og angi om leverandøren er en person eller et selskap.

#### <a name="exclude-items-and-fixed-assets-from-intrastat-reporting"></a><a name="exclude-items-and-fixed-assets-from-intrastat-reporting"></a><a name="exclude-items-and-fixed-assets-from-intrastat-reporting"></a>Utelate varer og aktiva fra Intrastat-rapportering

Hvis det er en grunn til å utelate en bestemt vare eller et aktivum fra Intrastat-rapportering, endrer du alternativet på kortet.

##### <a name="exclude-an-item-from-intrastat-reporting"></a><a name="exclude-an-item-from-intrastat-reporting"></a><a name="exclude-an-item-from-intrastat-reporting"></a>Utelate en vare fra Intrastat-rapportering

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.
2. Velg varen du vil konfigurere, og merk av for **Utelat fra Intrastat-rapportering** på hurtigfanen **Kostnad og bokføring**.

##### <a name="exclude-a-fixed-asset-from-intrastat-reporting"></a><a name="exclude-a-fixed-asset-from-intrastat-reporting"></a><a name="exclude-a-fixed-asset-from-intrastat-reporting"></a>Utelate et aktiva fra Intrastat-rapportering

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Aktiva**, og velg deretter den relaterte koblingen.
2. Velg aktivaet du vil konfigurere.
3. Utvid hurtigfanen **Intrastat**, og merk av for **Utelat fra Intrastat-rapport**.

#### <a name="set-up-tariff-numbers"></a><a name="set-up-tariff-numbers"></a><a name="set-up-tariff-numbers"></a>Konfigurer tariffnumre

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Tariffnumre**, og velg deretter den relaterte koblingen.  
2. På siden **Tariffnumre** angir du informasjon i feltene som beskrevet i tabellen nedenfor.

    | Felt | Description |  
    |-------|-------------|
    | **Nr.** | Angir tariffnummeret. |
    | **Beskrivelse** | Angir en beskrivelse av det relaterte tariffnummeret. |
    | **Supplerende enheter** | Angir om toll og skattemyndighetene krever informasjon om antall og enheter for denne varen. |
    | **Konverteringsfaktor** | Angir konverteringsfaktoren for tariffnummeret. |
    | **Måleenhet** | Angir enheten for tariffnummeret. |

> [!NOTE]
> Hvis du legger til en supplerende enhet, spør [!INCLUDE [prod_short](includes/prod_short.md)] om du vil oppdatere relaterte varer. Hvis du velger å oppdatere relaterte varer, oppdateres **Enhet**-verdien på siden **Enheter** for alle varer som har samme tariffnummer.
> 
> Når du legger til et tariffnummer som har en definert **Enhet**-verdi for varen, legger [!INCLUDE [prod_short](includes/prod_short.md)] automatisk til en ny enhet i **Enheter**-verdien for varen. Verdien **Antall per enhet** er basert på feltet **Avrundingspresisjon for antall**.

## <a name="enter-countryregion-intrastat-settings"></a><a name="enter-country-specific-intrastat-settings"></a><a name="enter-country-specific-intrastat-settings"></a>Angi landsspesifikke Intrastat-innstillinger

Intrastat-kravene er lignende i alle medlemsstatene i EU, selv om det finnes viktige unntak. I teorien må reglene brukes enhetlig i alle medlemsstater. Det finnes imidlertid forskjeller i implementeringer fordi noen medlemsstater har retningslinjer om hvordan de generelle prinsippene i bestemmelsene skal brukes i bestemte situasjoner (f.eks. kommersielle eksempler og retur av varer). Disse retningslinjene kan gi forskjellige resultater for ulike situasjoner. Informasjonen som land må angi, kan derfor være forskjellige og det kan filformatet de bruker til rapportering også.

### <a name="austria"></a><a name="austria"></a><a name="austria"></a>Østerrike

Intrastat-rapportering i Østerrike krever to forskjellige filer for mottak og leveringer. Følg denne fremgangsmåten for å kontrollere at oppsettet er riktig.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Oppsett for Intrastat-rapport**, og velg deretter den relaterte koblingen.  
2. I hurtigfanen **Rapportering** kontrollerer du om **Del mottaks-/leveringsfiler** er valgt. Hvis det er det, finner du to separate verdier for **Kode for datautveksl.def** konfigurert. 
3. Bekreft at feltet **ZIP-fil(er)** er valgt for å sikre at rapportfilene legges til i ZIP-filen.

Prosessen med å arbeide med Intrastat-rapporter er den samme som den globale funksjonen.

<!-- ### Belgium-->

### <a name="czech-republic"></a><a name="czech-republic"></a><a name="czech-republic"></a>Den tsjekkiske republikk

Den nye Intrastat-rapporten for den tsjekkiske republikk vil være tilgjengelig i lanseringsbølge 1 i 2023. I mellomtiden kan du fortsette å bruke funksjonen **Intrastat-kladd**.

### <a name="finland"></a><a name="finland"></a><a name="finland"></a>Finland

I Finland er det noen ekstra trinn du kan bruke for å definere Intrastat. Intrastat-rapportering i Finland krever to forskjellige filer for mottak og leveringer. Du finner også at det er to separate verdier for **Kode for datautveksl.def** konfigurert.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Oppsett for Intrastat-rapport**, og velg deretter den relaterte koblingen.  
2. Angi feltinformasjonen som beskrevet i tabellen nedenfor, i hurtigfanen **Filoppsett** på siden **Oppsett for Intrastat-rapport**.

    |                 Felt              |            Description                |  
    |------------------------------------|---------------------------------------|
    | **Egendefinert kode** | Angir en egendefinert kode for informasjon om oppsett av Intrastat-fil. |
    | **Foretaksnr./avtalenr.** | Angir et serienummer for selskapet for informasjon om oppsett av Intrastat-fil. |

3. I hurtigfanen **Rapportering** kontrollerer du om **Del mottaks-/leveringsfiler** er valgt.

Prosessen med å arbeide med Intrastat-rapporter er den samme som den globale funksjonen.

<!-- ### Germany-->

### <a name="italy"></a><a name="italy"></a><a name="italy"></a>Italia

En ny Intrastat-rapportfunksjon for Italia er tilgjengelig fra og med februar 2023. I mellomtiden kan du fortsette å bruke funksjonen **Intrastat-kladd**.

<!-- ### France-->

### <a name="sweden"></a><a name="sweden"></a><a name="sweden"></a>Sverige

Intrastat-rapportering i Sverige krever to forskjellige filer for mottak og leveringer. Følg denne fremgangsmåten for å kontrollere at oppsettet er riktig.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Oppsett for Intrastat-rapport**, og velg deretter den relaterte koblingen.  
2. I hurtigfanen **Rapportering** kontrollerer du at **Del mottaks-/leveringsfiler** er valgt. Hvis det er det, finner du to separate verdier for **Kode for datautveksl.def** konfigurert.

Prosessen med å arbeide med Intrastat-rapporter er den samme som i den globale funksjonen.

<!-- ### United Kingdom-->

## <a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Intrastat-rapportering i Business Central](finance-how-report-intrastat.md)  
[Økonomistyring](finance.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
