---
title: 'Sortere, søke etter og filtrere oversikter'
description: 'Økt effektivitet i oversikter ved å søke på tvers av data, sortere kolonner og forbedring av resultater ved hjelp av filtersymboler og tastatursnarveier.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'delimit, FlowFilter, totals, limit, advanced'
ms.search.form: null
ms.date: 04/01/2021
ms.author: jswymer
---
# <a name="sorting-searching-and-filtering"></a>Sortere, søke etter og filtrere

Det finnes et par ting du kan gjøre som hjelper deg med å skanne, finne og begrense poster i en liste eller i en rapport eller XMLport. Dette omfatter sortering, søk og filtrering. Du kan bruke noen av eller alle disse samtidig til å finne eller analysere data raskt.

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

For rapporter og XMLport-er kan du definere filtre som i lister for å avgrense hvilke data som skal inkluderes i rapporten eller XMLport, men du kan ikke sortere og søke.

> [!TIP]
> Når du viser dataene som fliser, kan du søke etter og bruke filtrering. Hvis du vil bruke hele settet med avanserte funksjoner for å sortere, søke og filtrere, velger du ikonet ![Vis som liste](media/ui_show_as_list_icon.png "Vis som liste, pil venstre") for å vise postene som en liste.

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria, you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a>Sortering

Sortering gjør det enkelt å få et raskt overblikk over dataene. Hvis du for eksempel har mange kunder, kan du velge å sortere dem etter **Kundenr.**, **Valutakode** eller **Lands-/områdekode** for å få nødvendig oversikt.

Hvis du vil sortere en liste, kan du:

- velge en kolonneoverskriftstekst for å veksle mellom stigende og synkende rekkefølge, eller
- velge rullegardinpilen i kolonneoverskriften, og deretter velge handlingen **Stigende** eller **Synkende**.  

> [!NOTE]  
> Sortering støttes ikke for bilder, BLOB-felt, FlowFilters og felt som ikke hører til i en tabell.  

## <a name="searching"></a>Søke

<!--## Searching by using the Quick Filter -->
Øverst på hver listeside finner du en ![Søkeliste.](media/ui-search/search-list.png "Søkeliste-ikon") **Søk**-handling som gir en rask og enkel måte å redusere postene i en oversikt på, og viser bare postene som inneholder dataene du interessert i å se på.

For å søke velger du **Søk**-handlingen, og deretter skriver inn teksten som du søker etter, i boksen. Du kan skrive inn bokstaver, tall og andre symboler.

Vanligvis vil søket forsøke å samsvare tekst i alle felt. Det skiller ikke mellom store og små bokstaver og samsvarer tekst plassert hvor som helst i feltet, ved begynnelsen, ved slutten eller i midten.

> [!TIP]
> Du kan velge <kbd>F3</kbd> for å aktivere og deaktivere søkeboksen. Hvis du vil ha mer informasjon, kan du se [Hurtigtaster](keyboard-shortcuts.md#KeyboardFilter).

> [!NOTE]  
> Søket vil ikke tilsvare verdier i bilder, BLOB-felt, FlowFilters, FlowFields og andre felt som ikke er en del av en tabell.


### <a name="fine-tuning-the-search-with-filter-criteria"></a>Finjustere søket med filterkriterier

Du kan foreta et mer nøyaktig søk ved å bruke filteroperatorer, uttrykk og filterkoder. I motsetning til filtrering brukes disse på tvers av alle felter når de brukes i søkefeltet, noe som gjør dem mindre effektive enn filtrering.

- Hvis du vil finne bare feltverdiene som nøyaktig samsvarer med hele teksten og store/små bokstaver, setter du tekst mellom enkle anførselstegn `''` (for eksempel `'man'`).

- Hvis du vil finne bare feltverdiene som starter med en viss tekst og store/små bokstaver, setter du `*` etter søketeksten (for eksempel `man*`).

- Hvis du vil finne bare feltverdiene som slutter med en viss tekst og store/små bokstaver, setter du `*` før søketeksten (for eksempel `*man`).

- Når du bruker `''` eller `*`, søket skiller mellom store og små bokstaver. Hvis du vil at søket ikke skal skille mellom store og små bokstaver, setter du inn `@` før teksten (for eksempel `@man*`).

Tabellen nedenfor inneholder eksempler som forklarer hvordan du kan bruke søket.

|Søkekriterier|Finner...|
|---------------|----------|
|`man`<br />eller <br />`Man`|Alle poster med felt som inneholder teksten **man**, uavhengig av store/små bokstaver. For eksempel **Manchester**, **manuell** eller **sportsmann**. |
|`'Man'`|Alle poster med felt som inneholder bare teksten **Man**, og store/små bokstaver må samsvare.|
|`Man*`|Alle poster med felt som starter med teksten <b>Man</b>, og store/små bokstaver må samsvare. For eksempel **Manchester**, men ikke **manuell** eller **sportsmann**.|
|`@Man*`|Alle poster med felt som starter med teksten **man**, uavhengig av store/små bokstaver. For eksempel **Manchester** og **manuell**, men ikke **sportsmann**.|
|`@*man`|Alle poster som slutter med teksten **man**, uavhengig av store/små bokstaver. For eksempel **Sportsman**, men ikke **Manchester** eller **manuell**.|


## <a name="filtering"></a><a name="filtering"></a>Filtrering

Filtrering er en mer avansert og allsidig måte å kontrollere hvilke poster som tas med i en liste, rapport eller XMLport. Det finnes to viktige forskjeller mellom søking og filtrering, som beskrevet i tabellen nedenfor.

|| **Søke** | **Filtrering** |
|--|----------|------------|
| **Gjeldende felt** | Søker i alle feltene som vises på siden. | Filtrerer ett eller flere felt hver for seg, og du kan velge fra et hvilket som helst felt i tabellen, inkludert felt som ikke vises på siden. |
| **Avstemming** | Viser poster med felter som samsvarer med søketeksten, uavhengig av store/små bokstaver i teksten eller plassering av teksten i feltet. | Viser poster der feltet samsvarer med filteret nøyaktig, og skiller mellom store/små bokstaver i teksten, med mindre spesielle filtersymboler er angitt.

Med filtrering kan du vise poster for bestemte konti eller kunder, datoer, beløp og annen informasjon ved å angi filterkriterier. Bare poster som samsvarer med kriteriene, vises i oversikten eller inkluderes i rapporten, den satsvise jobben eller XMLport. Hvis du angir kriterier for flere felt, vises bare poster som samsvarer med alle kriteriene.

For lister vises filtrene i en filtreringsrute som vises til venstre for listen når du aktiverer den. For rapporter, kjørsler og XMLport-er vises filtrene direkte på forespørselssiden.

### <a name="filtering-with-option-fields"></a>Filtrere med alternativfelt

Når det gjelder «vanlige» felt som inneholder data, oppsettdata eller forretningsdata, kan du angi filtre både ved å merke dataene og skrive inn filterverdier, og du kan bruke symboler til å definere avanserte filterkriterier. Hvis du vil ha mer informasjon, kan du se [Angi filterkriterier](ui-enter-criteria-filters.md#entering-filter-criteria).

For felt av typen **Alternativ** kan du imidlertid bare angi et filter ved å velge ett eller flere alternativer fra en rullegardinliste med de tilgjengelige alternativene. Et eksempel på et alternativfelt er feltet **Status** på siden **Salgsordrer**.

> [!NOTE]
> Når du velger flere alternativer som filterverdi, defineres relasjonene mellom alternativene som *ELLER*. Hvis du for eksempel velger både avmerkingsboksen **Åpen** og **Frigitt** i filterfeltet **Status** på siden **Salgsordrer**, betyr det at salgsordrer som enten er åpne eller frigitte, vises.

### <a name="setting-filters-on-lists"></a>Definere filtre på oversikter

I lister kan du definere filtre ved hjelp av filtreringsruten. Hvis du vil vise filtreringsruten for en liste, velger du rullegardinpilen ved siden av navnet på siden, og deretter velger du handlingen **Vis filterrute**. Du kan eventuelt velge <kbd>Skift</kbd>+<kbd>F3</kbd>.

Hvis du vil vise filtreringsruten for en kolonne på en liste, velger du rullegardinpilen, og deretter velger du handlingen **Filter**. Du kan eventuelt velge <kbd>Skift</kbd>+<kbd>F3</kbd>. Filtreringsruten åpnes med den valgte kolonnen vist som et filtreringfelt i delen **Filtrer listen etter**.

Filtreringsruten viser gjeldende filtre for en liste og gjør det mulig å angi egendefinerte filtre på ett eller flere felt ved å velge handlingen **+ Filter**.

 En filtreringsrute er inndelt i tre deler: **Visninger**, **Filtrer listen etter** og **Filtrer totaler etter**:

- **Visninger**

  Enkelte lister inkluderer delen **Visninger**. Visninger er variasjoner av listen som er forhåndsdefinert med filtre. Du kan definere og lagre så mange visninger som du ønsker per liste. Visningene vil være tilgjengelige på alle enheter du logger på. Hvis du vil ha mer informasjon, kan du se [Lagre og tilpasse listevisninger](ui-views.md).

- **Filtrer listen etter**

  Det er i denne inndelingen du legger til filtre på bestemte felt for å redusere antall poster som vises. Hvis du vil legge til et filter, velger du **+ Filter**-handlingen. Skriv deretter inn navnet på feltet du vil filtrere listen etter, eller velg et felt fra rullegardinlisten.

- **Filtrer totaler etter**

  Enkelte lister som viser beregnede felt, for eksempel beløp og antall, inkluderer delen **Filtrer totaler etter**, der du kan justere forskjellige dimensjoner som påvirker beregninger. Hvis du vil legge til et filter, velger du **+ Filter**-handlingen. Skriv deretter inn navnet på feltet du vil filtrere listen etter, eller velg et felt fra rullegardinlisten.

  > [!NOTE]
  > Filtre i delen **Filtrer totaler etter** kontrolleres av FlowFilters i utformingen av siden. For teknisk Informasjon, se [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).

Du kan angi et enkelt filter direkte i en liste ved hjelp av filtreringsruten, det vil si et filter som viser bare poster med samme verdi som i den valgte cellen. Velg en celle i listen, velg rullegardinpilen, og velg deretter handlingen **Filtrer på denne verdien**. Du kan eventuelt velge <kbd>Alt</kbd>+<kbd>F3</kbd>.

### <a name="setting-filters-in-reports-batch-jobs-and-xmlports"></a>Definere filtre i rapporter, kjørsler og XMLport-er

For rapporter og XMLport-er vises filtrene direkte på forespørselssiden. På forespørselssiden vises de sist brukte filtrene i henhold til valget i feltet **Bruk standardverdi fra**. Hvis du vil ha mer informasjon, kan du se [Bruk lagrede innstillinger](ui-work-report.md#SavedSettings).

Hoveddelen for **Filter** viser standardfilterfeltene du bruker til å avgrense hvilke poster som skal tas med i rapporten eller XMLport. Hvis du vil legge til et filter, velger du **+ Filter**-handlingen. Skriv deretter inn navnet på feltet du vil filtrere etter, eller velg et felt fra rullegardinlisten.

I delen **Filtrer totaler etter** kan du justere ulike dimensjoner som påvirker beregninger i rapporten eller XMLport. Hvis du vil legge til et filter, velger du **+ Filter**-handlingen. Skriv deretter inn navnet på feltet du vil filtrere etter, eller velg et felt fra rullegardinlisten.

## <a name="entering-filter-criteria"></a>Angi filtervilkår

Både i filtreringsruten og på forespørselssiden angir du filterkriteriene i boksen under filterfeltet.

Typen filterfelt bestemmer hvilke kriterier du kan angi. For eksempel kan filtrering av et felt som har faste verdier, gjøre at du bare kan velge mellom disse verdiene. Du finner mer informasjon om spesielle filtersymboler i [Filterkriterier](#FilterCriteria) og [Filtersymboler](#FilterTokens).

Kolonner som allerede har filtre, angis av ikonet ![filterikon](media/ui-search/filter-icon.png "Filter-ikon") i kolonneoverskriften. Hvis du vil fjerne et filter, velger du rullegardinpilen, og deretter velger du handlingen **Fjern filter**.

> [!TIP]
> Raskere søk analyse av data ved hjelp av kombinasjoner av tastatursnarveier. Du kan for eksempel velge et felt ved å bruke <kbd>Skift</kbd>+<kbd>Alt</kbd>+<kbd>F3</kbd> for å legge til feltet i filtreringsruten, skrive inn filterkriteriene, bruke <kbd>Ctrl</kbd>+<kbd>Enter</kbd> til å returnere til radene, velge et annet felt og bruke <kbd>Alt</kbd>+<kbd>F3</kbd> til å filtrere til den verdien. Hvis du vil ha mer informasjon, kan du se [Hurtigtaster](keyboard-shortcuts.md#KeyboardFilter).

### <a name="a-namefiltercriteria-afilter-criteria-and-operators"></a><a name="FilterCriteria"> </a>Filterkriterier og -operatorer

Når du angir kriterier, kan du bruke alle tallene og bokstavene du normalt kan bruke i feltet. Men det er også et sett med spesialtegn du kan bruke som operatorer, til å filtrere resultatene ytterligere. Følgende avsnitt beskriver disse symbolene og hvordan de brukes som operatorer i filtre.

> [!TIP]
> Hvis du vil ha mer informasjon om filtrering av datoer og klokkeslett, kan du se [Arbeid med datoer og klokkeslett i kalenderen](ui-enter-date-ranges.md).

> [!IMPORTANT]
> - Det kan oppstå situasjoner der verdien du vil filtrere på, inneholder et symbol som er en operator. Hvis du vil ha mer informasjon om hvordan du håndterer disse situasjonene, kan du se [Filtrere etter verdier som inneholder symboler](#symbols) for å få mer informasjon om hvordan du håndterer denne situasjonen.
>
> - Hvis det er mer enn 200 operatører i ett enkelt filter, vil systemet automatisk gruppere enkelte uttrykk i parenteser `()` for å behandle det. Dette har ingen innvirkning på filteret eller resultatet.  

#### <a name="-interval"></a>(..) Intervall

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`1100..2100`|Tall fra og med 1100 til og med 2100|  
|`..2500`|Tall til og med 2500|  
|`..12 31 00`|Datoer til og med 31.12.00|  
|`P8..`|Opplysninger for regnskapsperiode 8 og fremover|  
|`..23`|Fra startdatoen til 23. i inneværende måned og inneværende år 23.59.59|  
|`23..`|Fra 23. i inneværende måned og inneværende år 00.00.00 til slutten av tid|  
|`22..23`|Fra 23. i inneværende måned og inneværende år 0.00.00 til 23. i inneværende måned og inneværende år 23.59.59| 

> [!TIP]
> Hvis du bruker et numerisk tastatur, kan det hende at tasten for desimalskilletegn sender et annet tegn enn et punktum (.). For å bytte til et punktum velger du tastene <kbd>Alt</kbd>+<kbd>desimalskilletegn</kbd> på det numeriske tastaturet. Når du vil bytte tilbake, velger du <kbd>Alt</kbd>+<kbd>desimalskilletegnet</kbd> igjen. Se [Angi desimalskilletegnet som brukes av numeriske tastaturer](ui-enter-data.md#decimal) for mer informasjon.

#### <a name="124-eitheror"></a>(&#124;) Enten/eller

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`1200|1300`|Tall med 1200 eller 1300|  

#### <a name="-not-equal-to"></a>(<>) Ikke lik med

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`<>0`|Alle tall unntatt 0<br /><br /> I SQL Server Option kan du kombinere dette symbolet med et jokertegnuttrykk. <>A* betyr for eksempel ikke lik noen tekst som begynner med A.|  

#### <a name="-greater-than"></a>(>) Større enn

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`>1200`|Tall som er større enn 1200|  

#### <a name="-greater-than-or-equal-to"></a>(>=) Større enn eller lik med

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`>=1200`|Tall som er større enn eller lik 1200|  

#### <a name="-less-than"></a>(<) Mindre enn

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`<1200`|Tall som er mindre enn 1200|  

#### <a name="-less-than-or-equal-to"></a>(<=) Mindre enn eller lik med

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`<=1200`|Tall som er mindre enn eller lik 1200|  

#### <a name="-and"></a>(&) Og

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`>200&<1200`|Numre som er større enn 200, men mindre enn 1 200.|  

#### <a name="-an-exact-character-match"></a>('') Finne et nøyaktig tegntreff

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`'man'`|Tekst som samsvarer nøyaktig med **man** og skiller mellom store og små bokstaver.|  
|`''`|Tekst som er tom.|  

#### <a name="-case-insensitive"></a>(@) Skiller ikke mellom små og store bokstaver

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`@man*`|Tekst som begynner med **man** og skiller mellom store og små bokstaver.|  

#### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Et ubegrenset antall ukjente tegn

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`*Co*`|Tekst som inneholder **A/S** og skiller mellom små og store bokstaver.|  
|`*Co`|Tekst som slutter med **A/S** og skiller mellom små og store bokstaver.|  
|`Co*`|Tekst som begynner med **A/S** og skiller mellom små og store bokstaver.|  

#### <a name="-one-unknown-character"></a>(?) Ett ukjent tegn

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`Hans?n`|Tekst som for eksempel **Hansen** eller **Hanson**|  

#### <a name="combined-format-expressions"></a>Kombinerte formatuttrykk

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|Nummer 5999 og numrene fra og med 8100 til og med 8490.|  
|`..1299|1400..`|Ta med poster som har numre som er mindre enn eller lik 1299 eller nummeret 1400 eller høyere (alle numre utenom fra og med 1300 til og med 1399).|  
|`>50&<100`|Inkluder poster med numre som er større enn 50 og mindre enn 100 (det vil si tallene fra og med 51 til og med 99).|  

### <a name="filtering-on-values-that-contain-symbols"></a><a name="symbols"></a>Filtrere etter verdier som inneholder symboler

Det kan være tilfeller der feltverdier inneholder ett av følgende symboler:

- &
- (
- )
- =
- &#124;

Hvis du vil filtrere etter noen av disse symbolene, plasserer du filteruttrykket i enkle anførselstegn (`'<expression with symbol>'`). Hvis du for eksempel vil filtrere på poster som begynner med teksten *J & V*, er filteruttrykket `'J & V*'`.

Dette kravet er ikke nødvendig for andre symboler.

### <a name="a-namefiltertokens-afilter-tokens"></a><a name="FilterTokens"> </a>Filtersymboler

Når du angir filterkriterier, kan du også skrive inn ord som har spesiell betydning, som kalles filtersymboler. Når du har angitt symbolordet, erstattes ordet av verdien eller verdiene det representerer. Filterkoder gjør filtreringen enklere ved å redusere behovet for å navigere til en annen side for å slå opp verdiene du vil legge til i filteret. Tabellen nedenfor beskriver noen av symbolene du kan bruke som filterkriterier.

> [!TIP]
> Organisasjonen kan bruke egendefinerte symboler. Hvis du vil vite mer om det fullstendige settet med symboler du kan bruke, eller legge til flere egendefinerte symboler, kontakt systemansvarlig. For teknisk informasjon, se [Legge til filtersymboler](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).

#### <a name="me-or-userid-records-assigned-to-you"></a>(%me eller %userid) Poster som er tilordnet til deg

Bruk `%me` eller `%userid` når du filtrerer felt som inneholder bruker-ID-en, for eksempel feltet **Tilordnet til bruker-ID**, for å vise alle postene som er tilordnet til deg.

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`%me`<br />eller<br />`%userid`|Poster som er knyttet til brukerkontoen. |  

#### <a name="mycustomers-customers-in-my-customers"></a>(%mycustomers) Kunder i Mine kunder

Bruk `%mycustomers` i kundens **Nummer**-felt for å vise alle postene for kunder som er inkludert i listen **Mine kunder** i rollesenteret.

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`%mycustomers`|Kunder i vinduet **Mine kunder** i rollesenteret. |  

#### <a name="myitems-items-in-my-items"></a>(%myitems) Varer i Mine varer

Bruk `%myitems` i varens **Nummer**-felt for å vise alle postene for varer som er inkludert i listen **Mine varer** i rollesenteret.

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`%myitems`|Varer i vinduet **Mine varer** i rollesenteret. |  

#### <a name="myvendors-vendors-in-my-vendors"></a>(%myvendors) Leverandører i Mine leverandører

Bruk `%myvendors` i leverandørens **Nummer**-felt for å vise alle postene for leverandører som er inkludert i listen **Mine leverandører** i rollesenteret.

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`%myvendors`|Leverandører i vinduet **Mine leverandører** i rollesenteret. |  

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/search-filter-sort-data-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Vanlige spørsmål om søk og filtrering](ui-search-filter-faq.yml)  
[Lagre og tilpass listevisninger](ui-views.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
