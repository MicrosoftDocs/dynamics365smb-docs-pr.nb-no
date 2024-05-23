---
title: Kjør og skriv ut rapporter
description: Finn ut hvordan du legger inn en rapport i en jobbkø og planlegger at den skal behandles på en bestemt dato og et bestemt klokkeslett.
author: jswymer
ms.author: jswymer
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'task, process, report, print, schedule, save, Excel, PDF, Word, dataset'
ms.search.form: null
ms.date: 09/04/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Kjør og skriv ut rapporter

En rapport samler informasjon basert på et angitt sett med kriterier. Den organiserer og presenterer informasjonen i et leservennlig format som du kan skrive ut eller lagre som en fil. Det finnes mange tilgjengelige rapporter i programmet. Rapportene inneholder informasjon i forhold til konteksten på siden du er på. **Kunde**-siden inneholder for eksempel rapporter for de 10 beste kundene, salgsstatistikk og mer.

> [!NOTE]
> Satsvise jobber og XML-porter utfører mer eller mindre det samme som rapporter, men brukes mer til å behandling og eksport av data. For eksempel oppretter **Opprett purringer**-kjørselen purredokumenter som skal sendes til kunder med forfalte betalinger. Denne artikkelen dreier seg hovedsakelig om rapporter, men lignende informasjon gjelder kjørsler og XML-porter.

## Kom i gang

Du finner rapporter i menyen **Rapporter** på utvalgte sider, lister og kort, eller du kan bruke søket ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") til å finne rapporter etter navn. Hvis du vil ha en oversikt over innebygde rapporter du kan bruke i [!INCLUDE[prod_short](includes/prod_short.md)], sortert etter kategorier, kan du se [Tilgjengelige rapporter i [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md).

Når du velger en rapport, vises vanligvis en forespørselsside, med tittelen til rapportens navn, der du kan angi forskjellige alternativer og filtre som bestemmer hvilke data som er inkludert. De følgende delene forklarer hvordan du bruker forespørselssiden til å bygge, forhåndsvise og skrive ut en rapport.

## <a name="SavedSettings"></a>Bruk standardverdier – forhåndsdefinerte innstillinger

De fleste rapportforespørselssidene inkluderer feltet **Bruk standardverdi fra**. Med dette feltet kan du velge forhåndsdefinerte innstillinger for rapporten, som automatisk angir alternativer og filtre. Velg en oppføring fra rullegardinlisten for å se at alternativene og filtrene på rapportforespørselssiden endres i henhold til dette.

Oppføringen som kalles **Sist brukte alternativer og filtre**, er alltid tilgjengelig. Denne posten angir at rapporten bruker alternativene og filtrene du brukte forrige gang du kjørte rapporten.

Feltet **Bruk standardverdi fra** gir en rask, pålitelig og konsekvent metode for å generere rapporter som inneholder riktige data. Når du har valgt en post, kan du endre alle alternativene og filtrene før du forhåndsviser eller skriver ut rapporten. Endringene du gjør, blir ikke lagret i oppføringen for forhåndsdefinerte innstillinger du valgte, men de blir lagret i oppføringen **Sist brukte alternativer og filtre**.

> [!NOTE]
> De forhåndsdefinerte innstillingene konfigureres og administreres vanligvis av en administrator. Finn ut mer under [Behandle lagrede innstillinger for rapporter og satsvise jobber](reports-saving-reusing-settings.md).

## Spesifisere dataene som skal inkluderes i en rapport

Bruk feltene under **Alternativer** og **Filtre** for å endre eller avgrense informasjon du ønsker i rapporten. Du kan definere filtre i en rapport mer eller mindre på samme måte som du angir filtre for oversikter. Finn ut mer i delen [Filtrering](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> Hurtigfanen **Filter** på en rapportforespørselsside gir generell filtreringsfunksjonalitet for rapporter. Disse filtrene er valgfrie.
>
> Noen rapporter overser slike filtre, som betyr at uansett hvilket filter som er angitt i hurtigfanen **Filter**, vil resultatet av rapporten være det samme. Det er ikke mulig å gi en oversikt over hvilke felt som ignoreres i hvilke rapporter, så du må eksperimentere med filtrene når du bruker dem.
>
> **Eksempel**: Når du bruker kjørselen **Opprett purringer** ignoreres et filter for feltet **Kundeposter** for **Siste utstedte purregrad**, fordi filtre fikses for denne kjørselen.

## Forhåndsvise en rapport

Ved å forhåndsvise en rapport kan du se hvordan rapporten vil se ut før du skriver den ut. Forhåndsvisningen er ikke basert på skriveren valgt i feltet **Skriver** på forespørselssiden. Det kontrolleres av nettleseren. Etter forhåndsvisning kan du gå tilbake til forespørselssiden og gjøre endringer i alternativer og filtre etter behov.

Forhåndsvisningsvalgene på siden **Rapportforespørsel** avhengig av rapporten. For enkelte rapporter kan du velge **Forhåndsvis**, men for andre er alternativet **Forhåndsvis og lukk**. Begge valgene åpner en forhåndsvisning av rapporten. Forskjellen er at **Forhåndsvisning** holder forespørselssiden åpen, slik at du kan gå tilbake til den, gjøre endringer, forhåndsvise på nytt eller skrive ut. I motsetning med **Forhåndsvis og lukk** lukkes forespørselssiden, og du må åpne rapporten på nytt for å gjøre endringer eller skrive ut.

> [!NOTE]
> Hvis du bruker lanseringsbølge 1 i 2020 for Business Central eller tidligere, er det eneste valget **Forhåndsvisning**, som lukker forespørselssiden ved forhåndsvisning, som beskrevet ovenfor for **Forhåndsvis og lukk**.

### Arbeid med forhåndsvisningen

I forhåndsvisningen bruker du menylinjen i rapportforhåndsvisningen for å:

- Gå gjennom sider
- Zoome inn og ut
- Endre størrelse for å tilpasse siden
- Velg tekst

    Du kan kopiere tekst fra en rapport og lime den inn et annet sted, for eksempel en side i [!INCLUDE[prod_short](includes/prod_short.md)] eller Microsoft Word. Du kan for eksempel bruke musen til å velge venstre museknapp og holde nede der du vil begynne. Skyv musen for å merke et eller flere ord, setninger eller avsnitt. Velg deretter høyreklikknappen og velg **Kopier**. Du kan nå lime inn den merkede teksten der du vil ha den.
- Panorer dokumentet

    Du kan flytte det synlige området i rapporten i en hvilken som helst retning for å vise andre områder i rapporten. Panorering er nyttig når du har zoomet inn for å vise detaljer. Ved hjelp av musen kan du for eksempel velge og holde venstre museknapp hvor som helst i rapportforhåndsvisningen, og deretter flytte musen for å velge en del i rapporten.

- Last ned til en PDF-fil på datamaskinen eller nettverket.
- Skriv ut

## Lagre en rapport i en fil

Du kan lagre en rapport i et PDF-dokument, Microsoft Word-dokument, Microsoft Excel-arbeidsbok eller XML-dokument ved å velge **Send til**, og deretter velge. En fil lastes ned til enheten.

Hvis organisasjonen har konfigurert OneDrive for systemfunksjoner i stedet for å laste den ned, åpnes Excel-arbeidsbøker og Word-dokumenter i nettleseren med enten Excel eller Word for nettet.

> [!TIP]
> Alternativene **Microsoft Excel-dokument (bare data)** og **XML-dokumenter** er mest for avanserte formål. Du bruker vanligvis disse alternativene til å foreta detaljert dataanalyse. Finn ut mer under [Analyser rapportdata med Excel og XML](report-analyze-excel.md).
>
> Du kan også bruke **Microsoft Excel-dokument (bare data)** til å opprette nye Excel-oppsett for en gitt rapport. Finn ut mer under [Arbeid med Excel-oppsett](ui-excel-report-layouts.md).  

## <a name="ScheduleReport"></a> Planlegg en rapport for kjøring senere eller regelmessig

Du kan planlegge at en enkelt eller gjentakende rapport som skal kjøres på en bestemt dato og et bestemt klokkeslett. Planlagte rapporter legges i jobbkøen og behandles på det planlagte tidspunktet, på samme måte som andre jobber. Velg alternativet **Planlegg** etter at du har valgt **Send til**, og angi deretter informasjon som skriver, dato og klokkeslett. Rapporten legges til i jobbkøen og kjøres på angitt tidspunkt. Når rapporten er behandlet, fjernes elementet fra jobbkøen. Finn ut mer under [Bruk jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).  

Når du planlegger å kjøre en rapport, kan du for eksempel angi at den må kjøre hver torsdag ved å sette feltet **Datoformel for neste kjøring** til *D4*. Finn ut mer i delen [Bruk datoformler](ui-enter-date-ranges.md#use-date-formulas).  

Du kan velge å lagre rapporten som en fil (for eksempel en Excel-, Word- eller PDF-fil), skrive den ut eller bare generere rapporten. Hvis du lagrer rapporten i en fil, sendes den behandlede rapporten til siden **Rapportinnboks** på rollesenteret for å vise den. Finn ut mer under [Del og eksporter rapporter med rapportinnboksen](ui-work-report-inbox.md)

### Administrer planlagte gjentatte rapporter

Planlagte rapporter genereres av kjørsler som er behandlet på siden **Jobbkøposter**. Du kan se status og annen informasjon for hver rapport på siden, stanse midlertidig / fortsette rapporten, og generere rapporten ved behov.

Du kan også endre noen av rapportparameterne fra siden **Jobbkøposter** for eksempel utdatafiltypen, regelmessighet, kjøringsdato og start- og sluttidspunkter. Før du redigerer en eksisterende planlagt rapport, er det imidlertid nødvendig å sette rapportjobbkøen på vent:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Jobbkøposter**, og velg deretter den relaterte koblingen.  
2. På siden **Jobbkøposter** velger du ønsker rapport.
3. Velg handlingen **Satt på vent**.
4. Åpne og rediger den planlagte rapporten ved å velge statusen (*På vent*).

Når du har redigert rapportalternativene, gjentar du de første to trinnene og velger deretter handlingen **Sett status til klar** for å gjenoppta generering av rapporten.

Lær mer om håndtering av jobbkø under [Bruk jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).  

## <a name="PrintReport"></a>Skriv ut en rapport

Hvis du vil skrive ut en rapport, velger du **Skriv ut** på rapportforespørselssiden eller på menylinjen på siden **Forhåndsvisning**.

Når en rapport bruker et Excel-oppsett, ser du ikke feltet **Skriver**-feltet, **Skriv ut**- eller **Forhåndsvis**-knappene. Det finnes et **Last ned**-alternativ i stedet. Du skriver ut ved å velge **Last ned** og åpne den nedlastede filen i Excel og skrive ut derfra.

### <a name="Printer"></a>Skriver

**Skriver**-feltet på forespørselssiden viser navnet på skriveren som rapporten sendes til. Hvis du vil bytte skriver, velger du ganske enkelt skriveren fra listen.

> [!NOTE]
> Alternativet **(Håndteres av nettleseren)** angir at det ikke finnes noen tilordnet skriver for rapporten. I dette tilfellet vil nettleseren behandle utskriften og vise standard utskriftstrinn, der du kan velge en lokal skriver som er koblet til enheten. Alternativet **(Håndteres av nettleseren)** er ikke tilgjengelig i [!INCLUDE[prod_short](includes/prod_short.md)]-mobilappen eller appen for Microsoft Teams.

> [!TIP]
> Skriveren som er valgt som standard, konfigureres på siden **Skrivervalg**. Lær mer om hvordan du endrer standard skrive ren i delen [Definer standardskrivere](ui-specify-printer-selection-reports.md#default).

### Skrive ut rapporter på thailandsk

Spesielt for den thailandske versjonen av [!INCLUDE[prod_short](includes/prod_short.md)], kan ikke **Utskrift**-knappen skrive ut rapporter riktig på grunn av begrensninger i tjenesten som genererer den utskrivbare PDF-filen. Du kan i stedet åpne rapporten i Word og deretter lagre den som en utskrivbar PDF.  

Du kan også be systemansvarlig om å opprette et Word-rapportoppsett for de mest brukte rapportene. Finn ut mer under [Administrere rapport- og dokumentoppsett](ui-manage-report-layouts.md).  

## Bytt rapportoppsettet

Et rapportoppsett styrer hva som skal vises i en rapport, hvordan det er ordnet og stilen som brukes. Det er noen få måter å endre oppsettet på:

- Når du setter opp til å kjøre en rapport, vises det nåværende oppsettet i feltet **Rapportoppsett** på forespørselssiden. Hvis du midlertidig vil bytte til et annet oppsett, velger du feltet **Rapportoppsett** og velger fra en liste over tilgjengelige oppsett for rapporten.
- Hvis du vil endre standardoppsettet som brukes i en rapport, går du til enten sidene **Rapportoppsett** eller **Valg av rapportoppsett**.

Finn ut mer under [Definer oppsettet som brukes av en rapport](ui-set-report-layout.md). Hvis du vil tilpasse ditt eget rapportoppsett, kan du gå til [Kom i gang med å opprette oppsett](ui-get-started-layouts.md).

## Endre språk og format for tall, datoer og klokkeslett

Som standard er språket i tekst og format for tall, datoer og klokkeslett i en rapport basert på arbeidsspråket og områdeinnstillingene, som er definert på siden **Mine innstillinger**. Du kan imidlertid endre språket og formatområdet i hvert tilfelle når du forhåndsviser, skriver ut eller sender en rapport. På forespørselssiden angir du alternativene **Språk** og **Formatområde** til dine innstillinger. Du kan også angi språk- og regionformatet som skal brukes som standard for kunder og leverandører, på kortsidene deres.

Avhengig av hvor du har angitt språk- og formatinnstillingene, [!INCLUDE [prod_short](includes/prod_short.md)]  bestemmer du innstillingene som skal brukes i følgende rekkefølge:

1. Innstillingene du angir når du genererer en rapport.
2. Innstillingene som er angitt i dokumentet, som kommer fra kundens eller leverandørens innstillinger.
3. Innstillingene som er angitt i AL-objektet for rapport.
4. Innstillingene som er definert i Mine innstillinger.

Hvis du vil ha mer informasjon om siden **Mine innstillinger**, går du til [Endre grunnleggende innstillinger](ui-change-basic-settings.md#region).

## Avanserte alternativer

Feltene under hurtigfanen **Avansert** setter begrensninger på den genererte rapporten for å kontrollere skriverressurser. Du trenger vanligvis ikke endre disse innstillingene, med mindre du har en stor rapport. Hvis en rapport overskrider disse begrensningene når du prøver å forhåndsvise eller skrive ut, angir en melding hvilken begrensning som ble overskredet. Deretter kan du endre innstillingene slik at de passer til rapporten. Hvert felt har imidlertid en maksimumsverdi som du bør være klar over:

|Felt|Maksimumsverdi|
|-----|-------------|
|Maksimal gjengivelsestid|12:00:00|
|Maksimalt antall rader|1000000|
|Maksimalt antall dokumenter|500|

> [!NOTE]
> Maksimumsverdiene kan være forskjellige for [!INCLUDE[prod_short](includes/prod_short.md)] lokalt, og en administrator kan endre dem. Finn ut mer i delen [Konfigurere Business Central Server – Rapporter](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Reports). Hvis du vil ha en oversikt over rapportbegrensninger i [!INCLUDE[prod_short](includes/prod_short.md)] online, kan du se [Driftsgrenser](/dynamics365/business-central/dev-itpro/administration/operational-limits-online).

## Se også

[Tilgjengelige rapporter i [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md)  
[Bruk rapporter i daglig arbeid](reports-use-reports.md)  
[Oversikt over forretningsanalyse og rapportering](reports-bi-reporting.md)  
[Konfigurere skrivere](ui-specify-printer-selection-reports.md)  
[Kjøre satsvise jobber og XML-porter](ui-how-run-batch-jobs.md)  
[Arbeid med datoer og klokkeslett i kalenderen](ui-enter-date-ranges.md)  
[Administrer rapport- og dokumentoppsett](ui-manage-report-layouts.md)  
[Finansforretningsanalyse](bi.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
