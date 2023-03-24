---
title: Definere Intrastat-rapportering
description: Lær hvordan du konfigurerer Intrastat-rapporteringsfunksjoner for å rapportere handel med selskaper i andre EU-land.
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077'
---
# Definere Intrastat-rapportering

Alle selskaper i EU må rapportere handel med andre EU-land/-regioner. Varebevegelsen må hver måned rapporteres til statistikkmyndighetene i landet/regionen der selskapet befinner seg, og rapporten må leveres til skattemyndighetene. Intrastat er et system for innsamling av handelsstatistikk for varer i disse landene/regionene. Du bruker **Intrastat-rapport** til å fylle ut periodisk Intrastat-rapportering (vanligvis månedlig), samle inn, registrere og rapportere varer i henhold til lokal lovgivning.

Intrastat-rapportering er basert på standard EU-bestemmelser som gjelder for alle land. Det er imidlertid noen forskjeller innen de enkelte landene i praksis. Hvert land har regler for hva som er nøyaktig og hvordan de rapporterer.

> [!NOTE]
> Intrastat-informasjon gjelder ikke flytting av tjenester mellom land, men bare varer (varer og aktiva). Hvis den lokale regjeringen krever at du må registrere flytting av tjenester mellom land, kan du gjøre det ved å bruke funksjonen for **Tjenestedeklarasjon**.
>
> Denne funksjonen er forventet å være tilgjengelig fra november 2022 som en app i [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646), og hvis du vil bruke den, må du installere den på siden for **Administrasjon av utvidelse**.

> [!IMPORTANT]
> Denne artikkelen dekker den nye Intrastat-opplevelsen som er tilgjengelig fra [!INCLUDE[prod_short](includes/prod_short.md)] versjon 21. Kontakt systemansvarlig for å lære hvilken versjon firmaet bruker, og for å aktivere den nye funksjonaliteten.
>
> Les den forrige versjonens Intrastat-oppsett og bruksartikkel på [Konfigurere og rapportere Intrastat](finance-how-setup-report-intrastat-v20.md).

## Aktivere den nye Intrastat-opplevelsen

I 2022-lanseringsbølge 2 [!INCLUDE[prod_short](includes/prod_short.md)] inkluderer en redesigned Intrastat-opplevelse med utvidede funksjoner. Hvis den nye Intrastat-funksjonaliteten ikke er aktivert i ditt miljø, kan den aktiveres manuelt av en administrator på siden **Funksjonsstyring**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Funksjonsstyring**, og velg deretter den relaterte koblingen.
2. På siden **Funksjonsstyring** velger du linjen **Funksjonsoppdatering: Erstatt den eksisterende Intrastat-funksjonaliteten med den nye Intrastat-utvidelsen**. Lære mer om funksjonsbehandling på [Aktivere kommende funksjoner på forhånd](/dynamics365/business-central/dev-itpro/administration/feature-management) i administrasjonsinnholdet.
3. Velg **Alle brukere** i kolonnen **Aktiver for**.
4. Les forklaring av hvordan systemet vil bli oppgradert, og velg **Ja** hvis du er enig.
5. Velg **Neste**, og du får et grunnleggende oppsett for Intrastat. Les mer om Intrastat-oppsettet i delen [Intrastat-konfigurasjon](#intrastat-configuration).
6. Når du har fullført oppsettet, velger **Fullfør** for å begynne å bruke den nye Intrastat-opplevelsen.

> [!IMPORTANT]
> Husk at du ikke kan bruke gamle og nye opplevelser parallelt. Før utvidelsen aktiveres i et produksjonsmiljø anbefales det at du først aktiverer og tester denne funksjonen i et sandkassemiljø med en kopi av produksjonsdataene før du gjør dette i et produksjonsmiljø. Når du aktiverer en ny brukeropplevelse i produksjonsmiljøet, kan du ikke gå tilbake til den gamle Intrastat-funksjonaliteten.

> [!NOTE]
> Avhengig av selskapets lokasjon er aktivering av funksjonen som beskrives ovenfor, nok. For land med bestemte funksjoner for Intrastat-rapportering, bør du aktivere den landspesifikke Intrastat-appen i tillegg til kjerneutvidelsen.

## Intrastat-konfigurasjon

Før du kan bruke Intrastat-rapporter er det flere konfigurasjoner som må defineres.

### Intrastat-rapporteringsoppsett

Siden **Intrastat-rapportersoppsett** brukes til å aktivere Intrastat-rapportering og angi standarder for den. Du kan angi om du må rapportere Intrastat fra forsendelser (utsendelser), mottak (ankomster) eller begge deler, avhengig av terskler som er angitt i dine lokale forskrifter. Du kan også angi standard transaksjonstyper for vanlige dokumenter og returdokumenter, som brukes til transaksjonsrapportering.

Slik definerer du Intrastat-rapportering:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") angi **Oppsett for Intrastat-rapport**, og velg den relaterte koblingen.
2. Åpne hurtigfanen **Generelt**, og fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Tabellen nedenfor beskriver noen av nøkkelfeltene:

   | Felt | Description |
   | --- | --- |
   | **Rapportkvitteringer** | Angir at du må inkludere ankomster av mottatte varer i Intrastatrapporter. |
   | **Rapportleveringer** | Angir at du må inkludere leveringer av sendte varer i Intrastatrapporter. |
   | **Leveringer basert på**  | Angir hvilken landskode som blir brukt for Intrastat-rapportlinjer. Du kan velge ett av alternativene: **Salg til-land**, **Faktura til-land** eller **Lever til-land**. |
   | **Org.nr. basert på** | Angir hvilket mva-nummer for kunde-/leverandørkode som blir brukt for Intrastat-rapporten. Du kan velge ett av alternativene: **Salg til-mva** eller **Faktura til-mva**. |
   | **Registrert org.nr. mva. for selskap** | Angir hvordan selskapets organisasjonsnummer skal eksporteres til Intrastat-filen. Du kan velge ett av alternativene: Organisasjonsnr. mva., legge til EU-landskoden som et prefiks og fjerne EU-landskoden fra feltet Mva-reg. |
   | **Registrert org.nr. mva. for leverandør** | Angir hvordan en leverandørs organisasjonsnummer eksporteres til Intrastat-filen. Du kan velge ett av alternativene: Organisasjonsnr. mva., legge til EU-landskoden som et prefiks og fjerne EU-landskoden fra feltet Mva-reg. |
   | **Registrert org.nr. mva. for kunde** | Angir hvordan en kundes organisasjonsnummer eksporteres til Intrastat-filen. Du kan velge ett av alternativene: Organisasjonsnr. mva., legge til EU-landskoden som et prefiks og fjerne EU-landskoden fra feltet Mva-reg. |
   | **Hent mva. for partner for** | Angir hvilken type **Intrastat-rapport**-linje partnerens organisasjonsnummer oppdateres fra. Avhengig av hvilke lokale krav du har, kan du velge bare for mottak, bare for forsendelse eller for begge typer linjer. |
3. Åpne hurtigfanen **Standard transaksjoner**, og fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Tabellen nedenfor beskriver noen av nøkkelfeltene:

   | Felt | Description |
   | --- | --- |
   | **Standard trans.art** | Angir standard transaksjonsart for vanlige følgesedler, servicefølgesedler og kjøpsmottak. |
   | **Standard trans.art – returer** | Angir standard transaksjonsart for ordrereturer, servicereturer og kjøpsreturer. |
   | **Standard mva-nr. for privatperson** | Angir standard mva-nummer for privatperson i tilfelle privatpersonen må ha et eget mva-nummer på Intrastat-rapporten. |
   | **SStandard mva-nr. for tredjepartshandel** | Angir standard tredjeparts mva-nummer i tilfelle du ikke har mva-nummeret. |
   | **Standard-mva. for ukjent delstat** | Angir standard mva-nummer for en ukjent delstat. |
   | **Standard lands-/områdekode** | Angir standard mottakslandskode. |
4. Åpne hurtigfanen **Rapportering**, og fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Tabellen nedenfor beskriver noen av nøkkelfeltene:

   | Felt | Description |
   | --- | --- |
   | **Kode for datautveksl.def.** | Angir koden for datautvekslingsdefinisjonen for å generere Intrastat-filen. Den fungerer bare hvis feltet **Del mottaks-/leveringsfiler** er satt til **Nei**. |
   | **Del mottaks-/leveringsfiler** | Angir om mottak og leveringer skal rapporteres i to separate filer. |
   | **ZIP-fil(er)** | Angir om rapportfilen(e) skal legges til i ZIP-filen. |
   | **Kode for datautveksl.def. – mottak** | Angir koden for datautvekslingsdefinisjonen for å generere Intrastat-filen for mottatte vare. Den fungerer bare hvis feltet **Del mottaks-/leveringsfiler** er satt til **Ja**. |
   | **Kode for datautveksl.def. – levering** | Angir koden for datautvekslingsdefinisjonen for å generere Intrastat-filen for sendte varer. Den fungerer bare hvis feltet **Del mottaks-/leveringsfiler** er satt til **Ja**. |
5. Åpnbe **Nummerering**-hurtigfanen for å definere **Intrastat-numre**.

### Konfigurere en rapporteringsfil

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Datautvekslingsdefinisjoner**, og velg deretter den tilknyttede koblingen.
2. Velg handlingen **Ny**.
3. I hurtigfanen **Generelt** beskriver du datautvekslingsdefinisjonen, datafiltypen, kolonneskilletegnet, relaterte codeunits, XMLport og andre felt ved å fylle ut feltene.
4. På hurtigfanen **Linjedefinisjoner** beskriver du formateringen av linjer i datafilen ved å fylle ut feltene basert på **Linjetype**-feltet, og hvor du må definere antall kolonner for denne linjen.
5. På hurtigfanen **Kolonnedefinisjoner** fyller du ut linjen for hver planlagte kolonne. Du kan definere kolonnenavn, datatyper (*Tekst*, *Dato* eller *Desimal*), lengden på linjen med fast bredde, som inneholder kolonnen hvis filen er av typen Fast tekst, og noen andre parametere.
6. Velg handlingen **Felttilordning** på hurtigfanen **Linjedefinisjoner** for å åpne siden **Felttilordning**.
7. Opprett den nye posten, og velg riktig **Tabell-ID** (for **Intrastat-rapporten**, velg 4812) på hurtigfanen **Generelt**, og fyll deretter ut flere felt:
   1. Angi nøkkelindeksen for å sortere kildeoppføringene før eksport i feltet **Nøkkelindeks**.
   2. Velg riktig **Codeunit for tilordning**.
8. I hurtigfanen **Felttilordning** legger du til kolonnene du konfigurerte tidligere, i hurtigfanen **Kolonnedefinisjoner** , og deretter legger du til følgende:
   1. Angi **Felt-ID** for hver kolonne.
   2. Angi **Transformeringsregelen** for hver kolonne du trenger den. Den angir regelen som omdanner importert tekst til en støttet verdi før den kan tilordnes til et angitt felt i [!INCLUDE[prod_short](includes/prod_short.md)]. Når du velger en verdi i dette feltet, blir den nøyaktige verdien angitt i feltet for **Transformeringsregel** i **Buffer for felttilordning for datautveksl.** -abellen, og vice versa.
9. Hvis du må gruppere poster basert på noen kolonner, velger du feltene du vil bruke til gruppering, på hurtigfanen **Feltgruppering**.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] inneholder den forhåndskonfigurerte datautvekslingsdefinisjonen for Intrastat for alle lokaliserte land. Finn ut mer om oppretting av en ny datautvekslingsdefinisjon i artikkelen [Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md).

### Angi obligatoriske felt med sjekklisten for Intrastat-rapport

I noen land krever skattemyndighetene at Intrastat-rapporter for eksempel må inkludere leveringsmåten for kjøp eller andre verdier ved salg over en viss grense.

Slik angir du obligatoriske felt og/eller verdier på siden **Intrastat-rapport**:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Oppsett for Intrastat-rapport** og velger den relaterte koblingen.
2. Velg handlingen **Sjekkliste for Intrastat-rapport**.
3. Legg til de nødvendige linjene for å kontrollere ved hjelp av følgende instruksjoner:
   1. Angi feltet **Feltnr.** til et felt som må kontrolleres for en verdi som ikke er tom.
   2. Fyll om nødvendig ut feltet **Filteruttrykk** basert på følgende regler:
      1. Når du åpner **Filterside**, velger du **Filter** du må bruke for kontrollen.
      2. I neste trinn velger du en verdi relatert til **Filteret** du brukte.
      3. Hvis du har flere filtre du må fylle ut for dette feltet, kan du legge til et annet filter ved å følge samme fremgangsmåte.
      4. Når du er ferdig med å angi filtrene for det valgte feltet, velger du **OK**.
   3. Velg feltet **Tilbakeført filteruttrykk** for å angi at kontrollen for felter bare kjøres på linjene som ikke samsvarer med filteruttrykket. Hvis linjen ikke filtreres, ignoreres dette feltet.

> [!NOTE]
> Når du åpner linjen **Filterside** fra linjen **Filteruttrykk**, kan du bruke alle standard filteruttrykk som er knyttet til det bestemte feltet du vil filtrere.
>
> Vær forsiktig når du definerer valideringsregler. De kan avvike fra land til land.

## Bruke egendefinerte codeunits i Intrastat-rapportering

Hvis du vil endre hvordan Intrastat fungerer, og standardkonfigurasjonen ikke er nok, kan du tilpasse systemet ved å utvide standardfunksjonene. Hvis du må endre virkemåten for Intrastat ytterligere, kan du utvikle egne codeunits. Når du oppretter codeunits, må du imidlertid foreta flere endringer for å bruke dem. Slik konfigurerer du systemet til å bruke dine egne objekter:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konfigurasjon av mva-rapporter**, og velg deretter den relaterte koblingen.
2. Legg til en ny linje på **Konfigurasjon av mva-rapporter**-siden.
3. Velg alternativet **Intrastat-rapport** i feltet **Mva-rapporttype**.
4. I feltet **Versjon av mva-rapport** angir du hvilken versjon av rapporten.
5. Deretter kan du legge til codeunits for følgende alternativer: a. I feltet **Codeunit-ID for Foreslå linjer** angir du den nye codeuniten for å foreslå linjer i Intrastat-rapportens linjer.
   b. I feltet **Codeunit-ID for innhold** angir du den nye codeuniten for å eksportere data som en fil ved hjelp av en datautvekslingsdefinisjon.
   c. I feltet **Valider codeunit-ID** angir du den nye codeuniten for valideringsresultater i Intrastat-rapportens linjer.

> [!IMPORTANT]
>
> Denne linjen må være tom hvis du bruker standard codeunits. Du bør bare opprette en linje og konfigurere den hvis du har utviklet egendefinerte codeunits.

## Andre Intrastat-konfigurasjoner

> [!IMPORTANT]
> Kundekort og leverandørkort inneholder et felt, **Intrastat-partnertype** som har samme alternativverdier som feltet **Partnertype**: "" (tom), *Selskap* og *Person*. Feltet **Intrastat-partnertype** har erstattet feltet **Partnertype** i Intrastat-rapportering. Feltet **Partnertype** brukes i området SEPA (Single EURO Payments Area) for å definere (SEPA) til å definere SEPA Direct Debit Scheme (Core eller B2B). Feltet **Intrastat-partnertype** brukes bare til Intrastat-rapportering. På denne måten kan du angi ulike verdier for de to feltene, hvis du trenger det.
>
> Hvis feltet **Intrastat-partnertype** er tomt, brukes verdien fra feltet **Partnertype** til Intrastat-rapportering.

Unntatt for **Oppsett for Intrastat-rapport**, **Datautvekslingsdefinisjon** og **Sjekkliste for Intrastat-rapport** må du også konfigurere andre innstillinger:

| Side | Description |
| ---- | ----------- |
| **Land/områder** | Før du begynner å bruke Intrastat-rapporter, må du også definere siden **Land/regioner**. På denne siden må du legge til **Lands-/områdekode for EU** og **Intrastatkode** for å angi en kode for landet/regionen du handler med, slik det vil bli brukt i Intrastat-rapportering. |
| **Tariffnumre** | I mange land lager toll- og skattemyndighetene 8-sifrede koder for ulike varer. For at vareposter skal inneholde den nødvendige informasjonen når de leses inn på Intrastat-kladdelinjen, må du ha angitt varekoden på siden **Tariffnumre**. Finn kodene for varene som selskapet ditt handler med, og angi dem på **Tariffnumre**-siden. |
| **Transportmåter** | Det finnes sju koder med ett siffer for Intrastat-transportmåter. **1** for båt, **2** for jernbane, **3** for bil, **4** for fly, **5** for post **7** for faste installasjoner og **9** for egen fremdrift (for eksempel transportere en bil ved å kjøre den). [!INCLUDE[prod_short](includes/prod_short.md)] trenger ikke disse spesifikke kodene, men vi anbefaler at beskrivelsene formidler en lignende betydning. |
| **Transaksjonsarter** | Land og regioner har forskjellige koder for Intrastat-transaksjonstyper, for eksempel vanlig kjøp, salg, utveksling av returnerte varer og utveksling av ikke-returnerte varer. Definer alle kodene som gjelder for landet/regionen. Disse kodene brukes deretter på hurtigfanen **Utenrikshandel** på salgs- og kjøpsdokumenter, og når du behandler returer. |
| **Transaksjonsspesifikasjoner** | Definer koder for å supplere transaksjonstypebeskrivelsene. |
  > [!NOTE]
  > Fra og med januar 2022 krever Intrastat forskjellig transaksjonskoder for fordeling til private enkeltpersoner eller ikke-mva-registrerte selskaper og mva-registrerte selskaper. For å overholde dette kravet anbefaler vi at du ser gjennom eller legger til nye transaksjonskoder på siden **Transaksjonstyper** i henhold til kravene i ditt land. Du bør også kontrollere og oppdatere feltet **Intrastat-partnertype** til *Personer* for private eller ikke-mva-selskapers forretningskunder på den relevante **Kunde**-siden. Hvis du er usikker på hvilken Intrastat-partnertype eller transaksjonstype som er riktig å bruke, anbefaler vi at du spør en ekspert i landet eller området ditt.

| **Felt** | **Beskrivelse** |
| --------- | --------------- |
| **Nettovekt** | Vekt er en av de grunnleggende konfigurasjonene som er knyttet til Intrastat-rapportering, ettersom **Totalvekt** er obligatorisk for rapportering. For å være klar for dette behovet må du også fylle ut feltet **Nettovekt** på vare- eller aktivakortet. |
| **Kode for opprinnelsesland** | Bruk de to bokstavers ISO alfa-kodene på elementet eller aktivakortet for landet der varen ble anskaffet eller produsert. Hvis varen ble produsert i mer enn ett land, er opprinnelseslandet det siste landet der det ble behandlet betraktelig. |
| **Mva-nummer for partneroperatøren i medlemslandet for importen** | Dette mva-nummer for partneroperatøren i medlemslandet for importen. Mva-ID-en brukes også i utvekslingen av data mellom EU-eksport mellom medlemslandene, og tillater at medlemsland fordeler de mottatte dataene til importselskapet i sitt eget land. Rapporteringsenheter må rapportere mva-ID-en til selskapet som deklarerer den intra-unionhenting av varer i medlemslandet for import. |

Du kan også konfigurere følgende:

* **Varekoder**: Toll- og skattemyndighetene har laget numeriske koder som klassifiserer varer og tjenester. Du angie disse kodene for varene.
* **Områder**: Supplerende informasjon om land og regioner.
* **Inn-/utpunkt**: Angi lokasjonene der du leverer eller mottar varer til eller fra andre land. En flyplass er et eksempel på et inn-/utpunkt. Du angir inn-/utpunkt på hurtigfanen **Utenrikshandel** i salgs- og kjøpsdokumenter. Denne informasjonen blir også kopiert fra varepostene når du oppretter Intrastat-kladden.
* **Supplerende enhet**: Antall varer for Intrastat-rapportering kan være enten nettovekt (i kilo) eller en tilleggsenhet. Hvis det kreves tilleggsenheter, må du konfigurere dem for varer og aktiva.

#### Definere transportmåter

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Transportmåter**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### Definere transaksjonskoder

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Transaksjonstyper**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### Andre relaterte konfigurasjoner

Før du bruker funksjonen for Intrastat-rapportering, må du konfigurere noen felt på vare-, aktiva-, kunde- og leverandørkortene.

#### Varekort

Slik oppretter du alle nødvendige opplysninger i forbindelse med Intrastat på varekort:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.
2. Velg elementet du vil konfigurere.
3. I hurtigfanen **Kostnader og bokføring** fyller du ut feltene **Tariffnr.**, **Supplerende enhet** og **Kode for opprinnelsesland/-område**.
4. På hurtigfanen **Beholdning** angir du desimalverdien i feltet **Nettovekt**.

> [!NOTE]
> Du kan bruke forskjellige enheter som tilleggsenhet. Hvis dette ikke er det samme som **Lagerenhet**, må du konfigurere denne enhetskoden på siden **Vareenheter**.

#### Aktivakort

Slik oppretter du alle nødvendige opplysninger i forbindelse med Intrastat på aktivakort:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktiva**, og velg deretter den relaterte koblingen.
2. Velg aktivaet du vil konfigurere.
3. I hurtigfanen **Intrastat** fyller du ut feltene **Tariffnummer**, **Nettovekt** og **Supplerende enhet**.

> [!NOTE]
> Du kan bruke forskjellige enheter som tilleggsenhet. Men uansett **Enhetskode** du velger, vil **Antall** i Intrastat alltid være 1.

#### Leverandørkort

Før du kan bruke en leverandør i Intrastat-rapportering, må du ha dedikert **Lands-/regionkode** og **Organisasjonsnr.** for hver av dem, i tillegg til mer informasjon om siden **Leverandørkort**:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Leverandører** og velger den relaterte koblingen.
2. Velg leverandøren du vil konfigurere.
3. På hurtigfanen **Intrastat** kan du angi standardverdier for feltene **Standard trans.art**, **Standard trans.art – returer** og **Standard transportmåte**.
4. Utvid hurtigfanen **Betalinger**, og velg feltet **Intrastat-partnertype**, og angi om leverandøren er en person eller et selskap.

#### Kundekort

Før du kan bruke en kunde i Intrastat-rapportering, må du ha dedikert **Lands-/regionkode** og **Organisasjonsnr.** for hver av dem, i tillegg til mer informasjon om siden **Kundekort**:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.
2. Velg kunden du vil konfigurere.
3. På hurtigfanen **Intrastat** kan du angi standardverdier for feltene **Standard trans.art**, **Standard trans.art – returer** og **Standard transportmåte**.
4. Utvid hurtigfanen **Betalinger**, og velg feltet **Intrastat-partnertype**, og angi om leverandøren er en person eller et selskap.

#### Utelate varer og aktiva fra Intrastat-rapportering

Hvis en bestemt vare eller et aktiva skal utelates fra Intrastat-rapportering, må du endre et alternativ på kortet.

##### Utelate en vare fra Intrastat-rapportering

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.
2. Velg elementet du vil konfigurere.
3. I hurtigfanen **Kostnad og bokføring** velger du feltet **Utelat fra Intrastat-rapport**.

##### Utelate et aktiva fra Intrastat-rapportering

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktiva**, og velg deretter den relaterte koblingen.
2. Velg aktivaet du vil konfigurere.
3. Utvid hurtigfanen **Intrastat**, og velg deretter feltet **Utelat fra Intrastat-rapport**.

## Landsspesifikt Intrastat-oppsett

Intrastat-kravene er lignende i alle medlemsstatene i EU, selv om det finnes viktige unntak. I teorien må reglene brukes enhetlig i alle medlemsstater. Det finnes imidlertid forskjeller i implementeringen, fordi noen medlemsstater har retningslinjer for hvordan du bruker de generelle prinsippene i bestemmelsene skal brukes i bestemte situasjoner. Det kan for eksempel være kommersielle eksempler, retur av varer og så videre. Disse retningslinjene kan gi forskjellige resultater for ulike situasjoner i EU-medlemsland. På grunn av dette har noen land noen ekstra spesifikk informasjon atskilt fra andre land. De bruker også et annet filformat for rapportering.

### Østerrike

Intrastat-rapportering i Østerrike krever to forskjellige filer for mottak og leveringer. Følg denne fremgangsmåten for å kontrollere at oppsettet er riktig:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") angi **Oppsett for Intrastat-rapport**, og velg den relaterte koblingen.  
2. I hurtigfanen **Rapportering** kontrollerer du om **Del mottaks-/leveringsfiler** er valgt. Knyttet til dette finner du to separate **Koder for datautveksl.def** konfigurert. Feltet **ZIP-fil(er)** er også valgt for å sikre at rapportfilene legges til i zip-filen.

Prosessen med å arbeide med Intrastat-rapporter er den samme som den globale funksjonen.

<!-- ### Belgium-->

### Den tsjekkiske rep.

Den nye Intrastat-rapporten for den tsjekkiske republikk vil være tilgjengelig fra 2023 Release Wave 1. I mellomtiden kan du fortsette å bruke funksjonen **Intrastatkladd** .

### Finland

I Finland er det noen ekstra trinn du kan bruke for å definere Intrastat. Intrastat-rapportering i Finland krever to forskjellige filer for mottak og leveringer. Knyttet til dette finner du to separate **Koder for datautveksl.def** konfigurert.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") angi **Oppsett for Intrastat-rapport**, og velg den relaterte koblingen.  
2. Fyll ut feltene som beskrevet i tabellen nedenfor, i hurtigfanen **Filoppsett** på siden **Oppsett for Intrastat-rapport**.

    |Felt|Beskrivelse|  
    |------------------------------------|---------------------------------------|
    | **Egendefinert kode**|Angir en egendefinert kode for informasjon om oppsett av Intrastat-fil. |
    | **Foretaksnr./avtalenr.**|Angir et serienummer for selskapet for informasjon om oppsett av Intrastat-fil. |

3. I hurtigfanen **Rapportering** kontrollerer du om **Del mottaks-/leveringsfiler** er valgt.

Prosessen med å arbeide med Intrastat-rapporter er den samme som den globale funksjonen.

<!-- ### Germany-->

### Italia

Ny Intrastat-rapporterfaring for Italia er tilgjengelig fra februar 2023. I mellomtiden kan du fortsette å bruke funksjonen **Intrastatkladd**.

<!-- ### France-->

### Sverige

Intrastat-rapportering i Sverige krever to forskjellige filer for mottak og leveringer. Følg denne fremgangsmåten for å kontrollere at oppsettet er riktig:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") angi **Oppsett for Intrastat-rapport**, og velg den relaterte koblingen.  
2. I hurtigfanen **Rapportering** kontrollerer du om **Del mottaks-/leveringsfiler** er valgt. Knyttet til dette finner du to separate **Koder for datautveksl.def** konfigurert.

Prosessen med å arbeide med Intrastat-rapporter er den samme som i den globale funksjonen.

<!-- ### United Kingdom-->

## Se relatert opplæring på [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## Se også

[Intrastat-rapportering i Business Central](finance-how-report-intrastat.md)  
[Økonomistyring](finance.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
