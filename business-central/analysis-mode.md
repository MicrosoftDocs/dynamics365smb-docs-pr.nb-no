---
title: Analyser data på listesider og spørringer ved hjelp av dataanalysemodus
description: Lær hvordan du bruker dataanalysemodusen i Business Central til å analysere data.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 10/05/2023
ms.custom: bap-template
ms.service: dynamics365-business-central
ms.search.form: '456, 457, 458, 459, 460, 461, 16, 22, 25, 26, 27, 31, 143, 144, 9300, 9301, 9303, 9304, 9305, 9306, 9307, 9309, 9310, 9311'
---
# <a name="analyze-list-page-and-query-data-using-data-analysis-mode"></a>Analyser listesiden og spørringsdata ved hjelp av dataanalysemodus

> **GJELDER:** Offentlig forhåndsversjon i lanseringsbølge 1 for 2023 og nyere for Business Central for analyse av listesider. Generelt tilgjengelig i lanseringsbølge 2 for 2023 for Business Central for analyse av data fra listesider og spørringer.

I denne artikkelen lærer du hvordan du analyserer data fra listesider og spørringer ved hjelp av *dataanalysemodus*. I dataanalysemodusen kan du analysere data direkte fra siden, uten å måtte kjøre en rapport eller bytte til et annet program, for eksempel Excel. Det gir en interaktiv og allsidig måte å beregne, summere og undersøke data på. I stedet for å kjøre rapporter ved hjelp av ulike alternativer og filtre, kan du legge til flere faner som representerer forskjellige oppgaver eller visninger på dataene. Eksempler kan være Mine kunder, Følg opp varer, Nylig tillagte leverandører, Salgsstatistikk eller en annen visning du kan forestille deg.

> [!TIP]
> En bra ting med dataanalysemodusen er at den ikke endrer noen av de underliggende dataene på listesiden eller spørringen eller oppsettet av siden eller spørringen når den ikke er i dataanalysemodus. Den beste måten å lære mer om hva du kan gjøre i dataanalysemodusen, er derfor å prøve ut dette.

## <a name="prerequisites"></a>Forutsetninger

- Hvis du bruker Business Central versjon 22, er dataanalysemodusen i forhåndsversjon. Så en administrator må aktivere den før du kan bruke den. For å aktivere den går du til **Funksjonsstyring**-sidne og aktiverer **Funksjonsoppdatering: Analysemodus, analyser data raskt direkte i Business Central**. [Finn ut mer om Funksjonsstyring](/dynamics365/business-central/dev-itpro/administration/feature-management).
- I versjon 23 og nyere må kontoen din tilordnes tillatelsessettet **DATA ANALYSIS - EXEC** eller inkludere kjøretillatelse på systemobjektet  **9640 Tillat dataanalysemodus**. Som administrator kan du utelate disse tillatelsene for brukere som du ikke vil skal ha tilgang til analysemodus.

> [!NOTE]
> Det kan hende du legger merke til noen listesider som ikke inkluderer bryteren **Analyser** for å endre til analysemodus. Årsaken er at utviklere kan deaktivere analysemodus på bestemte sider ved hjelp av egenskapen [egenskapen AnalysisModeEnabled](/dynamics365/business-central/dev-itpro/developer/properties/devenv-analysismodeenabled-property) i AL.

## <a name="get-started"></a>Kom i gang

1. Åpne listesiden eller spørringen.

   Hvis du for eksempel vil arbeide med **kundeposter**-siden, velger du ikonet ![Forstørrelsesglass som åpner funksjonen Fortell meg.](media/ui-search/search_small.png) (<kbd>Alt</kbd>+<kbd>Q</kbd>), angir *kundeposter*, og deretter velger du den relaterte koblingen. 

2. På handlingslinjen øverst på siden slår du på bryteren **Analyser**.

    Dataanalysemodus åpner dataene i en opplevelse som er optimalisert for dataanalyse.  I dataanalysemodus erstattes den vanlige handlingslinjen med en spesiell dataanalysemodus. Den følgende illustrasjonen viser de ulike områdene på en side i dataanalysemodusen.

   [![Viser en oversikt over en side i dataanalysemodusen](media/analysis-mode-overview-2.png)](media/analysis-mode-overview-2.png#lightbox)

   Hvert område er forklart i de etterfølgende avsnittene.

3. Bruk de forskjellige områdene til å manipulere, summere og analysere data. Se delene nedenfor for mer informasjon.

4. Når du vil avslutte analysemodusen, slår du av bryteren **Analyser**.

   Analysefanene du har lagt til, blir værende til du sletter dem. Hvis du går tilbake til dataanalysemodusen igjen, vil du se dem nøyaktig slik du forlot dem.

> [!NOTE]
> Dataene som vises i analysemodus, styres av filtrene eller visningene som er angitt på listesiden. Dermed kan du forhåndsfiltrere dataene før du åpner analysemodus.

## <a name="work-with-data-analysis-mode"></a>Arbeid med dataanalysemodus

I dataanalysemodusen er siden delt inn i to områder:

- Hovedområdet, som består av dataområdet (1), sammendragslinjen (2) og fanelinjen (5)
- Området for datamanipulering, som består av to ruter: kolonner (3) og analysefiltre (4).

### <a name="data-area-1"></a>Dataområde (1)

Dataområdet er der radene og kolonnene på listesidespørringen vises og data summeres. Dataområdet er en allsidig måte å kontrollere kolonneutformingen på og en rask måte å få et sammendrag av dataene på. For kolonner som inneholder numeriske verdier, vises summen av alle verdiene i kolonnen i en siste rad, med mindre du har definert radgrupper. I dette tilfellet vises summene som en delsum for gruppene.  

![Viser en oversikt over et dataområde på en side i dataanalysemodusen](media/analysis-mode-data-area.png)

- Hvis du vil flytte en kolonne, merker du den og drar den til stedet der de gir mest mening i analysen.
- Høyreklikk på kolonnen eller hold pekeren over den, og velg menyikonet ![Viser ikonet for en kolonne i dataanalysemodus som åpner en handlingsmeny](media/analysis-mode-column-menu-icon.png) for å få tilgang til flere handlinger du kan gjøre på kolonner. Eksempel:

  - Hvis du vil feste en kolonne til venstre eller høyre for dataområdet slik at den ikke flyttes bort fra skjermen når du blar, velger du ![Vis ikonet i en kolonne i dataanalysemodus som åpner en meny med handlinger](media/analysis-mode-column-menu-icon.png) > **Fest kolonne** > **Fest til venstre** kolonnedelen.
  - Definer datafiltre direkte i kolonnedefinisjonen, i stedet for å gå til **Analysefiltre**-rutene. Du kan fremdeles kikke på detaljer om relaterte data og for hver linje og åpne kortet for å lære mer om en gitt enhet.
- Bruk dataområdet til å samhandle med dataene. Når det gjelder kolonner som inneholder numeriske, summerte verdier, kan du få en beskrivende statistikk for et sett med felter ved å merke dem. Statistikken vises på statuslinjen (2) langs bunnen av siden.
- Eksporter data i Excel- eller CSV-format. Høyreklikk på dataområdet eller et utvalg celler du vil eksportere.

### <a name="summary-bar-2"></a>Sammendragslinje (2)

Sammendragslinjen er langs bunnen av siden og viser statistikk om dataene på listesiden eller spørringen. Når du samhandler med kolonner med verdier som kan summeres, for eksempel når du merker flere rader i en kolonne som viser beløp, oppdateres dataene.

![Viser en oversikt over en sammendragslinje i dataanalysemodusen](media/analysis-mode-totals-row.png)

Tabellen nedenfor beskriver de ulike numrene som vises i totaler-området.

|Nummer|Beskrivelse|
|-|-|
|Rader|Antall merkede rader som en del av det totale antallet tilgjengelige rader. |
|Rader totalt|Antall rader i den ufiltrerte listen eller spørringen.|
|Filtrert|Antall rader som vises som et resultat av filtrene som brukes i listen eller spørringen.|
|Gjennomsnitt|Gjennomsnittsverdien i alle valgte summerte felter.|
|Antall|Antall valgte rader.|
|Min.|Minimumsverdien i alle valgte summerte felter.|
|Maks|Maksimumsverdien i alle valgte summerte felter.|
|Sum|Summen av alle verdiene i de valgte summerte feltene.|

### <a name="columns-3"></a>Kolonner (3)

**Kolonnene** er en av to ruter som arbeider sammen for å definere analysen. Det andre området er **Analysefiltre**-ruten. **Kolonne**-ruten brukes til å summere dataene. Bruk **Kolonner**-ruten til å definere hvilke kolonner som skal være med i analysen.

![Viser en oversikt over kolonner-ruten i dataanalysemodusen](media/analysis-mode-columns-2.png)

|Områder|Beskrivelse|
|-|-|
|Søk/merk eller fjern merket for alle boksene|Søke etter kolonner. Merk avmerkingsboksen for å merke/fjerne alle kolonner.|
|Avmerkingsbokser|Dette området inneholder en avmerkingsboks for hvert felt i kildetabellen for listen eller spørringen. Bruk dette området til å endre kolonnene som vises. Merk av i boksen for å vise kolonne for feltet på siden. Fjern merket i boksen for å skjule kolonnen. |
|Radgrupper|Bruk dette området til å gruppere og summere data etter et eller flere felter. Du kan bare ta med felter som ikke er numeriske, for eksempel felter for tekst, dato og klokkeslett. Radgrupper brukes ofte i pivotmodus.|
|Verdier|Bruk dette området til å angi felter som du vil ha en totalsum for. Du kan bare inkludere felter som inneholder tall, og som kan legges sammen. Det kan for eksempel være tekst, dato eller klokkeslettfelter.|

Velg grip-ikonet hvis du vil flytte et felt fra et område til et annet ![Viser en oversikt over en side i analysemodusen](media/column-grab-icon.png) ved siden av kolonnen i listen, og dra den til målområdet. Du forhindres fra å flytte et felt til et område hvor det ikke er tillatt.

### <a name="analysis-filters-4"></a>Analysefiltre (4)

Med **Analysefiltre**-ruten kan du angi flere data filtre i kolonner for å begrense oppføringene i oversikten. Angi filtre på kolonner for å begrense oppføringene i oversikten, og etterfølgende summer med bare de postene du er interessert i. basert på et kriterium du definerer. La oss for eksempel anta at du bare er interessert i data for en bestemt kunde eller salgsordre som overstiger et bestemt beløp. Når du skal definere et filter, merker du kolonnen, velger sammenligningsoperasjonen fra listen (som **Er lik** eller **Begynner med**), og deretter angir du verdien.

![Viser en oversikt over filtre-ruten i analysemodusen](media/analysis-mode-filters.png)

> [!NOTE]
> De ekstra filtrene gjelder bare for den gjeldende analysefanen. Dette gjør at du kan definere nøyaktig de ekstra datafiltrene som trengs for en bestemt analyse.

### <a name="tabs-5"></a>Faner (5)

I faneområdet øverst kan du opprette forskjellige konfigurasjoner (kolonner og analysefiltre) i separate faner, der du kan manipulere dataene i fanene uavhengig av hverandre. Det finnes alltid minst én fane, kalt **Analysis 1** som standard. Det er nyttig å legge til flere faner for å lagre ofte brukte analysekonfigurasjoner i et datasett. Det kan for eksempel tenkes at du har faner for å analysere data i pivotmodus, og andre faner som filtrerer til et delsett med rader. Noen faner kan vise en detaljert visning med mange kolonner, og andre viser bare noen få nøkkelkolonner.

Her er noen pekere på å arbeide med flere analysefaner:

- Hvis du vil legge til en ny fane, velger du det store **+**-tegnet ved siden av den siste analysefanen.
- Velg pil ned i en fane for å få tilgang til en liste over handlinger du kan utføre i en fane, for eksempel nytt navn, duplikat, sletting og flytting.

   - **Slett** sletter fanen som er åpen. **Slett alle** sletter alle faner du har lagt til, unntatt standardfanen **Analyse 1**.
- Du kan ikke fjerne **Analyse 1** fullstendig, men du kan gi den et nytt navn ved hjelp av **Gi nytt navn**-handlingen og fjerne endringene du har gjort, med **Slett** eller **Slett alle**.  

- Analysefanene du har lagt til og konfigurert, blir værende til du sletter dem. Hvis du går tilbake til dataanalysemodusen igjen, vil du se dem nøyaktig slik du forlot dem.

   > [!TIP]
   > Fanene du definerer, er bare synlige for deg. Andre brukere vil bare se faner de har opprettet.
- Du kan kopiere analysefaner. Kopiering kan være nyttig hvis du vil eksperimentere med å endre en fane uten å endre originalen, eller hvis du vil opprette forskjellige varianter av den samme analysen.


## <a name="date-hierarchies"></a>Datohierarkier

I analysemodus genereres datofelt i datasettet i et År-Kvartal-Måned-hierarki av tre separate felt. Dette hierarkiet er basert på den vanlige kalenderen, ikke økonomiske kalendere som er definert i Business Central.

De ekstra feltene heter _\<field name\> År_, _\<field name\> Kvartal_ og _\<field name\> Måned_. Hvis datasettet for eksempel inneholder et felt kalt _Bokføringsdato_, består det tilhørende datohierarkiet av felt kalt _År for bokføringsdato_, _Kvartal for bokføringsdato_, og _Månde for bokføringsdato_.

> [!NOTE]
> Datohierarkiet gjelder for øyeblikket bare for felt av typen dato, ikke for felt av typen datetime.

## <a name="pivot-mode"></a>Pivotmodus

Du kan bruke pivotmodus til å analysere store mengder numeriske data, og delsummering av data etter kategorier og underkategorier. Pivotmodus er som [pivottabeller i Microsoft Excel](https://support.microsoft.com/office/create-a-pivottable-to-analyze-worksheet-data-a9a84538-bfe9-40a9-a8e9-f99134456576).

Hvis du vil aktivere eller deaktivere pivotmodus, skyver du bryteren **Pivotmodus** i **Kolonner**-ruten (3). Når du aktiverer pivotmodus, vises **Kolonneetiketter**-området i ruten. Bruk **Kolonneetiketter**-området til å gruppere summer for rader i kategorier. Felter som du legger til i **Kolonneetiketter**-området, vises som kolonner i dataområdet (1).

Når du bygger inn dataanalysen i pivotmodus, må du flytte felter til de tre områdene: **Radgrupper**, **Kolonneetiketter** og **Verdier**. Den følgende illustrasjonen viser hvor feltene som er tilknyttet dataområdet (1), der `sum` er beregnede data, og eventuelt **Verdier**.

<table>
<tr><th></th><th>Kolonneetikett</th><th></th><th>Kolonneetikett</th><th></th></tr>
<tr><th>Radgruppe</th><th>Verdi</th><th>Verdi</th><th>Verdi</th><th>Verdi</th></tr>
<tr><td>rad</td><td>sum</td><td>sum</td><td>sum</td><td>sum</td></tr>
<tr><td>rad</td><td>sum</td><td>sum</td><td>sum</td><td>sum</td></tr>
<tr><td>rad</td><td>sum</td><td>sum</td><td>sum</td><td>sum</td></tr>
<tr><td>rad</td><td>sum</td><td>sum</td><td>sum</td><td>sum</td></tr>
</table>

> [!TIP]
> Kolonner som bare inneholder noen få verdier, er de beste kandidatene for bruk i kolonnen **Verdier**.


## <a name="analyze-large-amounts-of-data"></a>Analysere store mengder data

Hvis datasettet du vil analysere, overskrider 100 000 rader, foreslås det at du angir en analysemodus som er optimalisert for store datasett. Det er for øyeblikket to begrensninger hvis du bytter til denne modusen: 

- Formatering av felt for følgende fire datatyper kan endres: 

   - valuta 
   - desimaler (alltid vist med to desimaler) 
   - datoer (vises alltid i formatet ÅÅÅÅ-MM-DD)
   - tidssoner
- Felt som brukes i pivotmodus og legges til i kolonneetiketter, må ha et lavt antall distinkte verdier.

   Hvis du aktiverer pivotmodus og drar et felt til området **Kolonneetiketter**, der de underliggende dataene for feltet har for mange distinkte verdier, kan det hende at nettleserfanen ikke svarer og lukkes til slutt, noe som krever at du starter på nytt i en ny økt. I dette tilfellet må du enten ikke pivotere på feltet eller angi et filter på feltet før du legger det til i området **Kolonneetiketter**.

## <a name="share-data-analysis"></a>Dele dataanalyse

Når du har forberedt en analyse på en fane, kan du dele den som en kobling med kolleger og andre i organisasjonen direkte fra klienten. Bare mottakere som har tillatelse til selskapet og dataene, kan bruke koblingen.

1. Velg pil ned i kategorien Analyse, og velg deretter **Kopier kobling**.

   ![Viser handlingen for å kopiere en analyse](media/copy-analysis.svg)

   Dialogboksen **Kobling til \<tab name\>** åpnes.

1. Analysen du deler, kobler som standard til siden eller spørringen i selskapet du arbeider i, noe som angis av `company=<company_name>` i URL-feltet ved siden av **Kopier**-knappen. Hvis du vil sende en kobling til en analyse som ikke er knyttet til et bestemt selskap, setter du feltet **Selskap:** til **Ikke koble til et bestemt selskap**.

   ![Viser dialogboksen Kopier kobling for en analysefane](media/analysis-link-copied.svg)

1. Velg **Kopier**.

1. Lim inn koblingen i kommunikasjonsmediet du ønsker, for eksempel Word, Outlook, Teams, OneNote og så videre. 

2. Når mottakerne er mottatt, kan de velge koblingen og åpne analysen for siden eller spørringen i Business Central. De blir bedt om å angi et navn for den nye analysekategorien som skal opprettes.  

## <a name="limitations-in-2023-release-wave-1-preview"></a>Begrensninger i lanseringsbølge 1 for 2023 (forhåndsversjon)

Den offentlige forhåndsversjonen av denne funksjonen har følgende begrensninger:

- Analysemodusvisningen har for øyeblikket en grense på 100 000 rader. Hvis du overskrider denne grensen, får du en melding om dette. Du kan omgå denne begrensningen ved å sette filtrene på siden før du bytter til analysemodus, hvis det er mulig. Kanskje du vil analysere en bestemt gruppe med kunder, eller kanskje du bare vil ha data fra inneværende år. Du kan også velge en forhåndsdefinert visning hvis det skal brukes i analysen.
- Funksjonen for analyse av delingsdata er ikke tilgjengelig.
- Muligheten til å lagre foretrukne dataanalysevalg på listesider og lagre analysemenyer per analysekategori er for øyeblikket ikke tilgjengelig.

## <a name="see-also"></a>Se også

[Analyse av ad hoc-data](reports-adhoc-analysis.md)  
[Vis og rediger i Excel](across-work-with-excel.md)  
