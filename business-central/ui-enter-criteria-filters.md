---
title: Sortere, søke etter og filtrere oversikter | Microsoft-dokumentasjon
description: Økt effektivitet i oversikter ved å søke på tvers av data, sortere kolonner og forbedring av resultater ved hjelp av effektive filtersymboler og tastatursnarveier.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 06/03/2019
ms.author: sgroespe
ms.openlocfilehash: fc9cefd33f6ca11ee4f2936671a84071e142a1bd
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/06/2019
ms.locfileid: "1621186"
---
# <a name="sorting-searching-and-filtering-lists"></a>Sortere, søke etter og filtrere oversikter
Det finnes et par ting du kan gjøre som hjelper deg med å skanne, finne og begrense poster i en oversikt. Dette omfatter sortering, søk og filtrering. Du kan bruke noen av eller alle disse samtidig til å finne eller analysere data raskt.

> [!TIP]
> Når du viser dataene som fliser, kan du søke etter og bruke grunnleggende filtrering. Hvis du vil bruke hele settet med avanserte funksjoner for å sortere, søke og filtrere velger du ikonet ![Vis som liste](media/ui_show_as_list_icon.png "Vis som liste pil venstre") for å vise som en liste.

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a>Sortering
Sortering gjør det enkelt å få et raskt overblikk over dataene. Hvis du har mange kunder, kan du for eksempel velge å sortere dem etter **Kundenr.**, **Bokføringsgruppe - kunde**, **Valutakode**, **Lands-/områdekode** eller **Mva-organisasjonsnummer** for å få nødvendig oversikt.

Hvis du vil sortere en liste, kan du enten velge en kolonneoverskriftstekst og veksle mellom stigende og synkende rekkefølge, eller velge den lille nedpilen i kolonneoverskriften og deretter velge **Stigende** eller **Synkende**.  

> [!NOTE]  
>   Sortering støttes ikke for bilder, BLOB-felt, FlowFilters og felt som ikke hører til i en tabell.  

## <a name="searching"></a>Søke
<!--## Searching by using the Quick Filter -->
Øverst på hver listeside er det et ![Søkeliste](media/ui-search/search-list.png "Søkeliste-ikon") **Søk**-ikon som gir en rask og enkel måte å redusere postene i en oversikt på, og viser bare postene som inneholder dataene du interessert i å se på.

For å søke velger du søkeikonet og skriver inn teksten som du søker etter, i boksen. Du kan skrive inn bokstaver, tall og andre symboler.

### <a name="fine-tuning-the-search"></a>Finjustere søket
Vanligvis prøver Søk å samsvare teksten på tvers av alle feltene. Det skiller ikke mellom store og små bokstaver og samsvarer tekst plassert hvor som helst i feltet (ved begynnelsen, ved slutten eller i midten).

Du kan imidlertid foreta et mer nøyaktig søk ved hjelp av følgende spesialtegn:

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

> [!TIP]
> Du kan trykke F3 for å aktivere og deaktivere søkeboksen. Hvis du vil ha mer informasjon, kan du se [Hurtigtaster](keyboard-shortcuts.md#KeyboardFilter)

## <a name="Filtering"> </a>Filtrering
Filtrering er en mer avansert og allsidig måte for å kontrollere hvilke poster som vises i en oversikt. Det finnes to viktige forskjeller mellom søking og filtrering, som beskrevet i tabellen nedenfor.

|| **Søke** | **Filtrering** |
|--|----------|------------|
| **Gjeldende felt** | Søker i alle feltene som vises på siden. | Filtrerer ett eller flere felt hver for seg, og du kan velge fra et hvilket som helst felt i tabellen, inkludert felt som ikke vises på siden. |
| **Avstemming** | Viser poster med felt som samsvarer med søketeksten, uavhengig av store/små bokstaver eller plassering av teksten. | Viser poster der feltet samsvarer med filteret nøyaktig, og skiller mellom store/små bokstaver, med mindre spesielle filtersymboler er angitt.

Med filtrering kan du vise poster for bestemte konti eller kunder, datoer, beløp og annen informasjon ved å angi filterkriterier. Bare poster som samsvarer med kriteriene, vises. Hvis du angir kriterier for flere felt, vises bare poster som samsvarer med alle kriteriene.

### <a name="working-in-the-filter-pane"></a>Arbeide i filtreringsruten

For å vise filtreringsruten kan du velge ![Filtreringsruteikon](media/open-filter-pane-icon.png "Filtreringsruteikon") øverst i oversikten eller trykke på **Skift+F3**. For lister i rollesenteret kan du også velge pil ned i nærheten av sidetittelen på navigasjonslinjen over listen og deretter velge **Vis filtreringsrute**, som vist her.

![Vis filtreringsrute](media/open-filter-pane.png "Vis filtreringsrute")

Filtreringsruten viser gjeldende filtre for en liste og gjør det mulig å angi egendefinerte filtre på ett eller flere felt. Figuren nedenfor viser et eksempel på en filtreringsrute for en tilbudsliste.

![Oversikt over filtreringsruten](media/filter-pane-overview.png "Filterikonet")

En filtreringsrute er inndelt i tre deler: **Visninger**, **Filtrer listen etter** og **Filtrer totaler etter**:

- **Visninger**

  Enkelte lister inkluderer **Visninger**-delen. Visninger er variasjoner av listen som er forhåndsdefinert med filtre. Du kan bytte til en annen visning av listen ved å ganske enkelt velge en annen kobling. Du kan endre filtrene i en visning midlertidig, men endringene vil ikke lagres permanent.

- **Filtrer listen etter**

  Delen **Filtre listen etter** er der du legger til filtre på bestemte felt for å redusere antall poster som vises. Hvis du vil legge til et filter, velger du **+ Filter**, velger feltet du vil filtrere fra alle feltene i tabellen, og angir deretter filterkriterier i boksen.

- **Filtrer totaler etter**

  Enkelte lister som viser beregnede felt, for eksempel beløp og antall, inkluderer delen **Filtrer totaler etter**, der du kan justere forskjellige dimensjoner som påvirker beregninger. For eksempel kan du raskt analysere kontoplanen ved å filtrere beløp etter en bestemt periode, eller du kan vise totalverdiene for ordrer fra et bestemt lager.

  Hvis du vil legge til et filter, velger du **+ Filter**, velger én av de forhåndsdefinerte dimensjonene, og legger deretter til filterkriteriene i boksen.

  > [!NOTE]
  > Filtre i delen **Filtrer totaler etter** kontrolleres av FlowFilters i utformingen av siden. For teknisk Informasjon, se [FlowFilters](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).


### <a name="entering-filter-criteria-in-the-filter-pane"></a>Angi filterkriterier i filtreringsruten
Gjør ett av følgende for å velge et felt som skal filtreres:
  - I filtreringsruten, velg **+ Felt**. Skriv inn navnet på feltet som du ønsker å filtrere, eller velg et felt fra menyen som inneholder alle feltene i tabellen.

  - Velg pil ned i en kolonneoverskrift, og velg deretter **Filter...**. Dette åpner filtreringsruten og legger til kolonnen i filtreringsruten.

Du kan nå skrive inn eller velge filterkriterier i boksen. Typen felt du filtrerer, bestemmer hvilke kriterier du kan angi. For eksempel kan filtrering av et felt som har faste verdier, gjøre at du bare kan velge mellom disse verdiene. Du finner mer informasjon om spesielle filtersymboler i [Filterkriterier](#FilterCriteria) og [Filtersymboler](#FilterTokens).

Kolonner som allerede har filtre, angis av ![filterikonet](media/ui-search/filter-icon.png "filterikonet") i kolonneoverskriften. Hvis du vil fjerne et filter, velger du kolonneoverskriven og velger deretter **Fjern Filter**.


### <a name="entering-filter-criteria-without-using-the-filter-pane"></a>Angi filterkriterier uten å bruke filtreringsruten
Du kan angi enkeltfiltre direkte fra listen uten å måtte bruke filtreringsruten.
Når et feltet er merket på en rad, kan du bruke **Alt+F3**-hurtigtasten for å vise bare poster som har samme verdi. Du kan deretter velge et annet felt og bruke samme hurtigast på nytt for å fortsette finjustering av filtrene. Hvis det valgte feltet allerede filtreres, kan du fjerne dette filteret ved hjelp av **Alt+F3**.

> [!TIP]
> Raskere søk analyse av data ved hjelp av kombinasjoner av tastatursnarveier. Du kan for eksempel velge et felt ved å bruke**Alt+Skift+F3** for å legge til feltet i filtreringsruten, skrive inn filterkriteriene, bruke **Ctrl+Enter** til å returnere til radene, velge et annet felt og bruke **Alt+F3** til å filtrere til den verdien.
Hvis du vil ha mer informasjon, kan du se [Hurtigtaster](keyboard-shortcuts.md#KeyboardFilter)


## <a name="FilterCriteria"> </a>Filterkriterier og symboler
Når du angir kriterier, kan du bruke alle tallene og bokstavene du normalt kan bruke i feltet. I tillegg til dette kan du bruke spesielle symboler til å filtrere resultatene ytterligere. Tabellene nedenfor viser hvilke symboler som kan brukes i filtre. For dato og klokkeslett kan du også se [Arbeide med datoer og klokkeslett i kalenderen](ui-enter-date-ranges.md) for mer informasjon.

> [!IMPORTANT]  
>  Det kan være tilfeller der feltverdiene inneholder disse symbolene og du vil filtrere på dem. Hvis du vil gjøre dette, må du ta med filteruttrykket som inneholder symbolet, i anførselstegn (''). Hvis du for eksempel vil filtrere på poster som begynner med teksten *S&R*, er filteruttrykket `'S&R*'`.  

### <a name="-interval"></a>(..) Intervall

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`1100..2100`|Tall fra og med 1100 til og med 2100|  
|`..2500`|Tall til og med 2500|  
|`..12 31 00`|Datoer til og med 31.12.00|  
|`P8..`|Opplysninger for regnskapsperiode 8 og fremover|  
|`..23`|Fra startdatoen til 23. i inneværende måned og inneværende år 23.59.59|  
|`23..`|Fra 23. i inneværende måned og inneværende år 00.00.00 til slutten av tid|  
|`22..23`|Fra 23. i inneværende måned og inneværende år 0.00.00 til 23. i inneværende måned og inneværende år 23.59.59|  

### <a name="124-eitheror"></a>(&#124;) Enten/eller  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`1200|1300`|Tall med 1200 eller 1300|  

### <a name="-not-equal-to"></a>(<>) Ikke lik med  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`<>0`|Alle tall unntatt 0<br /><br /> I SQL Server Option kan du kombinere dette symbolet med et jokertegnuttrykk. <>A* betyr for eksempel ikke lik noen tekst som begynner med A.|  

### <a name="-greater-than"></a>(>) Større enn  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`>1200`|Tall som er større enn 1200|  

### <a name="-greater-than-or-equal-to"></a>(>=) Større enn eller lik med  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`>=1200`|Tall som er større enn eller lik 1200|  

### <a name="-less-than"></a>(<) Mindre enn  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`<1200`|Tall som er mindre enn 1200|  

### <a name="-less-than-or-equal-to"></a>(<=) Mindre enn eller lik med  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`<=1200`|Tall som er mindre enn eller lik 1200|  

### <a name="-and"></a>(&) Og  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`>200&<1200`|Numre som er større enn 200, men mindre enn 1 200.|  

### <a name="-an-exact-character-match"></a>('') Finne et nøyaktig tegntreff  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`'man'`|Tekst som samsvarer nøyaktig med man og skiller mellom store og små bokstaver.|  

### <a name="-case-insensitive"></a>(@) Skiller ikke mellom små og store bokstaver  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`@man*`|Tekst som begynner med man og skiller mellom store og små bokstaver.|  

### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Et ubegrenset antall ukjente tegn

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`*Co*`|Tekst som inneholder A/S og skiller mellom små og store bokstaver.|  
|`*Co`|Tekst som slutter med A/S og skiller mellom små og store bokstaver.|  
|`Co*`|Tekst som begynner med A/S og skiller mellom små og store bokstaver.|  

> [!NOTE]  
>   Du kan ikke bruke `*` når du filtrerer på alternativfelt (opplisting), for eksempel feltet **Status** i salgsordrer. Hvis du vil angi et filter for denne typen felt, kan du angi den numeriske verdien som en parameter for filtrering. I feltet **Status** i en ordre som har verdiene **Åpen**, **Frigitt**, **Venter på godkjenning** og **Venter på forskudd**, må du bruke verdiene `0`, `1`, `2` og `3` for å filtrere etter disse alternativene.

### <a name="-one-unknown-character"></a>(?) Ett ukjent tegn  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`Hans?n`|Tekst som for eksempel Hansen eller Hanson|  

### <a name="combined-format-expressions"></a>Kombinerte formatuttrykk  

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|Nummer 5999 og numrene fra og med 8100 til og med 8490.|  
|`..1299|1400..`|Ta med poster som har numre som er mindre enn eller lik 1299 eller nummeret 1400 eller høyere (alle numre utenom fra og med 1300 til og med 1399).|  
|`>50&<100`|Inkluder poster med numre som er større enn 50 og mindre enn 100 (det vil si tallene fra og med 51 til og med 99).|  


## <a name="FilterTokens"> </a>Filtersymboler
Når du angir filterkriterier, kan du også skrive inn ord som har spesiell betydning, som kalles filtersymboler. Når du har angitt symbolordet, erstattes ordet av verdien eller verdiene det representerer. Dermed blir filtreringen enklere ved å redusere behovet for å navigere til en annen side for å slå opp verdiene du vil legge til i filteret. Tabellen nedenfor beskriver noen av symbolene du kan bruke som filterkriterier.

> [!TIP]
> Organisasjonen kan bruke egendefinerte symboler. Hvis du vil vite mer om det fullstendige settet med symboler du kan bruke, eller legge til flere egendefinerte symboler, kontakt systemansvarlig. For teknisk informasjon, se [Legge til filtersymboler](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).


### <a name="me-or-userid-records-assigned-to-you"></a>(%me eller %userid) Poster som er tilordnet til deg

Bruk `%me` eller `%userid` når du filtrerer felt som inneholder bruker-ID-en, for eksempel feltet **Tilordnet til bruker-ID**, for å vise alle postene som er tilordnet til deg.

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`%me`<br />eller<br />`%userid`|Poster som er knyttet til brukerkontoen. |  

### <a name="mycustomers-customers-in-my-customers"></a>(%mycustomers) Kunder i Mine kunder

Bruk `%mycustomers` i kundens **Nummer**-felt for å vise alle postene for kunder som er inkludert i listen **Mine kunder** i rollesenteret.

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`%mycustomers`|Kunder i vinduet **Mine kunder** i rollesenteret. |  

### <a name="myitems-items-in-my-items"></a>(%myitems) Varer i Mine varer

Bruk `%myitems` i varens **Nummer**-felt for å vise alle postene for varer som er inkludert i listen **Mine varer** i rollesenteret.

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`%myitems`|Varer i vinduet **Mine varer** i rollesenteret. |  

### <a name="myvendors-vendors-in-my-vendors"></a>(%myvendors) Leverandører i Mine leverandører

Bruk `%myvendors` i leverandørens **Nummer**-felt for å vise alle postene for leverandører som er inkludert i listen **Mine leverandører** i rollesenteret.

|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|`%myvendors`|Leverandører i vinduet **Mine leverandører** i rollesenteret. |  


## <a name="see-also"></a>Se også
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Vanlige spørsmål om søking og filtrering](ui-search-filter-faq.md)
