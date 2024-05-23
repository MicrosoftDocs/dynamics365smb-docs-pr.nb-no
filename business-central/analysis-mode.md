---
title: Analyser listesiden og spørringsdata ved hjelp av dataanalyse
description: Lær hvordan du bruker analysemodusen i Business Central til å analysere data.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 04/29/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.search.form: '456, 457, 458, 459, 460, 461, 16, 22, 25, 26, 27, 31, 143, 144, 9300, 9301, 9303, 9304, 9305, 9306, 9307, 9309, 9310, 9311'
---
# Analyser listesiden og spørringsdata ved hjelp av dataanalysefunksjon

> **GJELDER:** Offentlig forhåndsversjon i lanseringsbølge 1 for 2023 og nyere for Business Central for analyse av listesider. Generelt tilgjengelig i lanseringsbølge 2 for 2023 for Business Central for analyse av data fra listesider og spørringer.

Denne artikkelen forklarer hvordan du bruker dataanalysefunksjonen fra listesider og spørringer. Dataanalysen lar deg analysere data direkte fra siden, uten å måtte kjøre en rapport eller åpne et annet program, for eksempel Excel. Funksjonen gir en interaktiv og allsidig måte å beregne, summere og undersøke data på. I stedet for å kjøre rapporter ved hjelp av ulike alternativer og filtre, kan du legge til flere faner som representerer forskjellige oppgaver eller visninger på dataene. Noen eksempler er Mine kunder, Følg opp varer, Nylig tillagte leverandører, Salgsstatistikk eller en annen visning du kan forestille deg.

> [!TIP]
> En god ting med dataanalysefunksjonen er at den ikke endrer de underliggende dataene for en listeside eller spørring. Det endrer heller ikke oppsettet for siden eller spørringen når den ikke er i analysemodus. Den beste måten å lære mer om hva du kan gjøre i analysemodus, er derfor å prøve ut dette.

## Forutsetninger

- Hvis du bruker [!INCLUDE [prod_short](includes/prod_short.md)] versjon 22, er dataanalysefunksjonen i forhåndsversjon. Så en administrator må aktivere den før du kan bruke den. For å aktivere den går du til **Funksjonsstyring**-sidne og aktiverer **Funksjonsoppdatering: Analysemodus, analyser data raskt direkte i Business Central**. [Finn ut mer om Funksjonsstyring](/dynamics365/business-central/dev-itpro/administration/feature-management).
- I versjon 23 og nyere må kontoen din tilordnes tillatelsessettet **DATA ANALYSIS - EXEC** eller inkludere kjøretillatelse på systemobjektet  **9640 Tillat dataanalysemodus**. Som administrator kan du utelate disse tillatelsene for brukere som du ikke vil skal ha tilgang til analysemodus.

> [!NOTE]
> Noen listesider som ikke tilbyr veksleknappen **Angi analysemodus** for å aktivere analysemodus. Årsaken er at utviklere kan deaktivere analysemodus på bestemte sider ved hjelp av egenskapen [egenskapen AnalysisModeEnabled](/dynamics365/business-central/dev-itpro/developer/properties/devenv-analysismodeenabled-property) i AL.

## Kom i gang

Følg disse trinnene for å starte analysemodus.

>[!TIP]
> Analysemodusen inneholder også en Copilot-funksjon kalt *analysehjelp* som kan hjelpe deg med å komme i gang. [Finn ut mer om analysehjelp med Copilot](analysis-assist.md).

1. Åpne listesiden eller spørringen.

   Hvis du for eksempel vil arbeide med **kundeposter**-siden, velger du ikonet ![Forstørrelsesglass som åpner funksjonen Fortell meg.](media/ui-search/search_small.png) (<kbd>Alt</kbd>+<kbd>Q</kbd>), angir *kundeposter*, og deretter velger du den relaterte koblingen. 

2. I handlingsfeltet øverst på siden velger du på knappen **Gå inn i analysemodus** ![Viser knappen for å aktivere analysemodus](media/analysis-mode-icon.png).

    Analysemodusen åpner dataene i en opplevelse som er optimalisert for dataanalyse. I analysemodus erstattes den vanlige handlingslinjen med en spesiell analysemodus. Den følgende illustrasjonen viser de ulike områdene på en side i analysemodusen.

   [![Viser en oversikt over en side i analysemodusen](media/analysis-mode-overview-3.png)](media/analysis-mode-overview-3.png#lightbox)

   Hvert område er forklart i de etterfølgende avsnittene.

3. Bruk de forskjellige områdene til å manipulere, summere og analysere data. Se delene nedenfor for mer informasjon.

4. Når du vil stoppe analysemodusen, velger du knappen **Forlat analysemodus** ![Viser knappen for å deaktivere analysemodus](media/analysis-mode-exit-icon.png)

   Analysefanene du la til, blir værende til du sletter dem. Hvis du går tilbake til analysemodusen igjen, vil du se dem nøyaktig slik du forlot dem.

> [!NOTE]
> Dataene som vises i analysemodus, styres av filtrene eller visningene som er angitt på listesiden. Dermed kan du forhåndsfiltrere dataene før du åpner analysemodus.

## Arbeid med analysemodus

I analysemodusen er siden delt inn i to områder:

- Hovedområdet, som består av dataområdet (1), sammendragslinjen (2) og fanelinjen (5).
- Området for datamanipulering, som består av to ruter: kolonner (3) og analysefiltre (4).

### Dataområde (1)

Dataområdet er der radene og kolonnene på listesidespørringen vises og data summeres. Dataområdet er en allsidig måte å kontrollere kolonneutformingen på og en rask måte å få et sammendrag av dataene på. For kolonner som inneholder numeriske verdier, vises summen av alle verdiene i kolonnen i en siste rad, med mindre du definerer radgrupper. I dette tilfellet vises summene som en delsum for gruppene.  

![Viser en oversikt over et dataområde på en side i analysemodusen](media/analysis-mode-data-area.png)

- Hvis du vil flytte en kolonne, merker du den og drar den til stedet der de gir mest mening i analysen.
- For å sortere på en kolonne velger du kolonneoverskriften. For å sortere på flere kolonner velger og holder du <kbd>Skift</kbd>-tasten mens du velger kolonneoverskriftene du vil sortere på.
- Hvis du vil ha tilgang til flere handlinger du kan utføre på kolonner, høyreklikker du kolonnen eller holder musepekeren over den og velger menyikonet ![Viser ikonet for en kolonne i analysemodus som åpner en handlingsmeny](media/analysis-mode-column-menu-icon.png). Eksempel:

  - Hvis du vil feste en kolonne på dataområdet slik at den ikke flyttes bort fra skjermen når du blar, velger du ![Vis ikonet i en kolonne i analysemodus som åpner en meny med handlinger](media/analysis-mode-column-menu-icon.png) > **Fest kolonne** > **Fest til venstre** kolonnedelen.
  - Definer datafiltre direkte i kolonnedefinisjonen, i stedet for å gå til **Analysefiltre**-rutene. Du kan fremdeles kikke på detaljer om relaterte data og for hver linje og åpne kortet for å lære mer om en gitt enhet.
- Bruk dataområdet til å samhandle med dataene. Når det gjelder kolonner som inneholder numeriske, summerte verdier, kan du få en beskrivende statistikk for et sett med felter ved å merke dem. Statistikken vises på statuslinjen (2) langs bunnen av siden.
- Eksporter data i Excel- eller CSV-format. Høyreklikk på dataområdet eller et utvalg celler du vil eksportere.

### Sammendragslinje (2)

Sammendragslinjen er langs bunnen av siden og viser statistikk om dataene på listesiden eller spørringen. Når du samhandler med kolonner med verdier som kan summeres, for eksempel når du merker flere rader i en kolonne som viser beløp, oppdateres dataene.

![Viser en oversikt over en sammendragslinje i analysemodusen](media/analysis-mode-totals-row.png)

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

### Kolonner (3)

**Kolonnene** er en av to ruter som arbeider sammen for å definere analysen. Det andre området er **Analysefiltre**-ruten. **Kolonne**-ruten brukes til å summere dataene. Bruk **Kolonner**-ruten til å definere hvilke kolonner som skal være med i analysen.

![Viser en oversikt over kolonner-ruten i analysemodusen](media/analysis-mode-columns-3.png)

|Områder|Beskrivelse|
|-|-|
|Søk/merk eller fjern merket for alle boksene|Søke etter kolonner. Merk av i avmerkingsboksen for å merke/fjerne alle kolonner.|
|Avmerkingsbokser|Dette området inneholder en avmerkingsboks for hvert felt i kildetabellen for listen eller spørringen. Bruk dette området til å endre kolonnene som vises. Merk av i boksen for å vise kolonne for feltet på siden. Fjern merket i boksen for å skjule kolonnen. |
|Radgrupper|Bruk dette området til å gruppere og summere data etter et eller flere felter. Du kan bare ta med felter som ikke er numeriske, for eksempel felter for tekst, dato og klokkeslett. Radgrupper brukes ofte i pivotmodus.|
|Verdier|Bruk dette området til å angi felter som du vil ha en totalsum for. Du kan bare inkludere felter som inneholder tall, og som kan legges sammen. Det kan for eksempel være tekst, dato eller klokkeslettfelter.|

Velg grip-ikonet hvis du vil flytte et felt fra et område til et annet ![Viser knappen for å hente et felt i analysemodusen](media/column-grab-icon.png) ved siden av kolonnen i listen, og dra den til målområdet. Du forhindres fra å flytte et felt til et område hvor det ikke er tillatt.

### Analysefiltre (4)

Med **Analysefiltre**-ruten kan du angi flere data filtre i kolonner for å begrense oppføringene i oversikten. Angi filtre på kolonner for å begrense oppføringene i oversikten, og etterfølgende summer med bare de postene du er interessert i. basert på et kriterium du definerer. La oss for eksempel anta at du bare er interessert i data for en bestemt kunde eller salgsordre som overstiger et bestemt beløp. Når du skal definere et filter, merker du kolonnen, velger sammenligningsoperasjonen fra listen (som **Er lik** eller **Begynner med**), og deretter angir du verdien.

![Viser en oversikt over filtre-ruten i analysemodusen](media/analysis-mode-filters-2.png)

> [!NOTE]
> De ekstra filtrene gjelder bare for den gjeldende analysefanen. Dette gjør at du kan definere nøyaktig de ekstra datafiltrene som trengs for en bestemt analyse.

### Faner (5)

I faneområdet øverst kan du opprette forskjellige konfigurasjoner (kolonner og analysefiltre) i separate faner, der du kan manipulere dataene i fanene uavhengig av hverandre. Det finnes alltid minst én fane, kalt **Analysis 1** som standard. Det er nyttig å legge til flere faner for å lagre ofte brukte analysekonfigurasjoner i et datasett. Det kan for eksempel tenkes at du har faner for å analysere data i pivotmodus, og andre faner som filtrerer til et delsett med rader. Noen faner kan vise en detaljert visning med mange kolonner, og andre viser bare noen få nøkkelkolonner.

Her er noen pekere på å arbeide med flere analysefaner:

- Hvis du vil legge til en ny fane, velger du det store **+**-tegnet ved siden av den siste analysefanen.
- Velg pil ned i en fane for å få tilgang til en liste over handlinger du kan utføre i en fane, for eksempel nytt navn, duplikat, sletting og flytting.

   - **Slett** sletter fanen som er åpen. **Slett alle** sletter alle faner du har lagt til, unntatt standardfanen **Analyse 1**.
- Du kan ikke fjerne **Analyse 1** fullstendig, men du kan gi den et nytt navn ved hjelp av **Gi nytt navn**-handlingen og fjerne endringene du har gjort, med **Slett** eller **Slett alle**.  

- Analysefanene du legger til og konfigurerer, blir værende til du sletter dem. Hvis du går tilbake til analysemodusen, er de nøyaktig slik du forlot dem.

   > [!TIP]
   > Fanene du definerer, er bare synlige for deg. Andre brukere vil bare se faner de har opprettet.
- Du kan kopiere analysefaner. Kopiering kan for eksempel være nyttig når du skal eksperimentere med å endre en fane uten å endre originalen. Kopiering er også nyttig hvis du vil opprette forskjellige varianter av samme analyse.

## Datohierarkier

I analysemodus genereres datofelt i datasettet i et År-Kvartal-Måned-hierarki av tre separate felt. Dette hierarkiet er basert på den vanlige kalenderen, ikke økonomiske kalendere som er definert i Business Central.

De ekstra feltene heter *\<field name\> År*, *\<field name\> Kvartal* og *\<field name\> Måned*. Hvis datasettet for eksempel inneholder et felt kalt *Bokføringsdato*, består det tilhørende datohierarkiet av felt kalt *År for bokføringsdato*, *Kvartal for bokføringsdato*, og *Månde for bokføringsdato*.

> [!NOTE]
> Datohierarkiet gjelder for øyeblikket bare for felt av typen dato, ikke for felt av typen datetime.

## Pivotmodus

Du kan bruke pivotmodus til å analysere store mengder numeriske data, og delsummering av data etter kategorier og underkategorier. Pivotmodus er som [pivottabeller i Microsoft Excel](https://support.microsoft.com/office/create-a-pivottable-to-analyze-worksheet-data-a9a84538-bfe9-40a9-a8e9-f99134456576).

Hvis du vil aktivere eller deaktivere pivotmodus, aktiverer du veksleknappen **Pivotmodus** i **Kolonner**-ruten (3). Når du aktiverer pivotmodus, vises **Kolonneetiketter**-området i ruten. Bruk **Kolonneetiketter**-området til å gruppere summer for rader i kategorier. Felter som du legger til i **Kolonneetiketter**-området, vises som kolonner i dataområdet (1).

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

## Analysere store mengder data

Hvis datasettet du vil analysere, overskrider 100 000 rader, foreslås det at du angir en analysemodus som er optimalisert for store datasett. Det er for øyeblikket to begrensninger hvis du bytter til denne modusen: 

- Formatering av felt for følgende fire datatyper kan endres: 

   - valuta 
   - desimaler (alltid vist med to desimaler) 
   - datoer (vises alltid i formatet ÅÅÅÅ-MM-DD)
   - tidssoner
- Felt som brukes i pivotmodus og legges til i kolonneetiketter, må ha et lavt antall distinkte verdier.

   Hvis du aktiverer pivotmodus og drar et felt til området **Kolonneetiketter**, der de underliggende dataene for feltet har for mange distinkte verdier, kan det hende at nettleserfanen ikke svarer. Nettleseren lukkes til slutt, noe som krever at du starter på nytt i en ny økt. I dette tilfellet må du enten ikke pivotere på feltet eller angi et filter på feltet før du legger det til i området **Kolonneetiketter**.

## Dele dataanalyse

Når du har forberedt en analyse på en fane, kan du dele den som en kobling med kolleger og andre i organisasjonen direkte fra klienten. Bare mottakere som har tillatelse til selskapet og dataene, kan bruke koblingen.

1. Velg pil ned i kategorien Analyse, og velg deretter **Kopier kobling**.

   ![Viser handlingen for å kopiere en analyse](media/analysis-mode-copy.png)

   Dialogboksen **Kobling til \<tab name\>** åpnes.

1. Analysen du deler, kobler som standard til siden eller spørringen i selskapet du arbeider i, noe som angis av `company=<company_name>` i URL-feltet ved siden av **Kopier**-knappen. Hvis du vil sende en kobling til en analyse som ikke er knyttet til et bestemt selskap, setter du feltet **Selskap:** til **Ikke koble til et bestemt selskap**.

   ![Viser dialogboksen Kopier kobling for en analysefane](media/analysis-link-copied.svg)

1. Velg **Kopier**.
1. Lim inn koblingen i kommunikasjonsmediet du ønsker, for eksempel Word, Outlook, Teams, OneNote og så videre.
1. Når mottakerne er mottatt, kan de velge koblingen og åpne analysen for siden eller spørringen i [!INCLUDE [prod_short](includes/prod_short.md)]. De blir bedt om å angi et navn for den nye analysekategorien de oppretter.  

## Eksempler på hvordan du analyserer data

Bruk **Dataanalyse**-funksjonen for rask faktasjekking og ad hoc-analyse:

- Hvis du ikke vil kjøre en rapport.
- Hvis det ikke finnes en rapport for ditt spesifikke behov.
- Hvis du vil gjenta raskt for å få en god oversikt over en del av virksomheten din.

De følgende delene inneholder eksempler på scenarier for mange av funksjonsområdene i [!INCLUDE [prod_short](includes/prod_short.md)].

### Eksempel: Finans (kunde)

Hvis du vil se hva kundene dine skylder deg, kanskje inndelt i tidsintervaller for når beløp forfaller, følger du denne fremgangsmåten:

1. Åpne [Kundeposter](https://businesscentral.dynamics.com/?page=25)-listen og velg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Gå inn i analysemodus."::: for å aktivere analysemodus.
1. Gå til **Kolonner**-menyen og fjern alle kolonner (merk av i boksen ved siden av *Søk*-feltet til høyre).
1. Aktiver vekslebryteren **Pivot*-modus** (over **Søk**-feltet til høyre).
1. Dra **Kundenavn**-feltet til **Radgrupper**-området og dra **Restbeløp** til **Verdier**-området.
1. Dra feltet **Forfallsdato (måned)** til **Kolonneetiketter**-området.
1. Hvis du vil utføre analysen for et gitt år eller kvartal, bruker du et filter på menyen **Analysefiltre** (under **Kolonner**-menyen til høyre).
1. Endre navnet på analysefanen til **Aldersfordelte kontoer etter måned** eller noe som beskriver denne analysen.

### Ad hoc-dataanalyseeksempler etter funksjonsområde

Mange av funksjonsområdene i [!INCLUDE[prod_short](includes/prod_short.md)] har artikler med ad hoc-dataanalyseeksempler.

[!INCLUDE[ad-hoc-analysis-scenarios-table](includes/ad-hoc-analysis-scenarios-table.md)]

## Begrensninger i lanseringsbølge 1 for 2023 (forhåndsversjon)

Den offentlige forhåndsversjonen av denne funksjonen har følgende begrensninger:

- Analysemodusvisningen har for øyeblikket en grense på 100 000 rader. Hvis du overskrider denne grensen, får du en melding om dette. Du kan omgå denne begrensningen ved å sette filtrene på siden før du bytter til analysemodus, hvis det er mulig. Kanskje du vil analysere en bestemt gruppe med kunder, eller kanskje du bare vil ha data fra inneværende år. Du kan også velge en forhåndsdefinert visning hvis det skal brukes i analysen.
- Funksjonen for analyse av delingsdata er ikke tilgjengelig.
- Muligheten til å lagre foretrukne dataanalysevalg på listesider og lagre analysemenyer per analysekategori er for øyeblikket ikke tilgjengelig.

## Se også

[Ad hoc-dataanalyse etter funksjonsområde](ad-hoc-data-analysis-by-functional-area.md)   
[Analyse av ad hoc-data](reports-adhoc-analysis.md)  
[Vis og rediger i Excel](across-work-with-excel.md)  
