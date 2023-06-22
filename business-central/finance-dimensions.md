---
title: Arbeide med dimensjoner for å spore og analysere data
description: 'Bruk dimensjoner til å kategorisere poster, for eksempel etter avdeling eller prosjekt, slik at det er enklere å spore og analysere data slik at du kan ta gode forretningsbeslutninger.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/27/2023
ms.custom: bap-template
ms.search.keywords: 'analysis, history, track, business intelligence'
ms.search.form: '408, 479, 480, 481, 484, 536, 537, 538, 539, 540, 541, 542, 543, 544, 545, 548, 560, 562, 564, 567, 568, 577, 578, 580, 699, 1343, 2580, 2581, 2582, 2583, 2584, 2585, 2586, 2587, 2588, 2590, 2591, 2592, 2593, 9083, 9233, 9251, 9252, 9253'
---
# <a name="work-with-dimensions" />Arbeid med dimensjoner

Dimensjoner er attributter og verdier som kategoriserer poster slik at du kan spore og analysere dem på dokumenter, for eksempel ordrer. Dimensjoner kan for eksempel angi hvilket prosjekt eller hvilken avdeling en post kommer fra.  

I stedet for å opprette separate finanskonti for hver avdeling og hvert prosjekt, kan du for eksempel bruke dimensjoner som grunnlag for analyse og unngå å måtte opprette en komplisert kontoplan. Finn ut mer om [Forretningsintelligens](bi.md).

Et annet eksempel er å definere en dimensjon som kalles *Avdeling* og deretter bruke denne dimensjonen når du bokfører salgsdokumenter. Dermed kan du bruke verktøyene for forretningsanalyse til å se hvilken avdeling hvilke varer som er solgt. Jo flere dimensjoner du bruker, jo mer detaljerte rapporter kan du basere dine forretningsavgjørelser på. En enkelt salgspost kan faktisk omfatte informasjon fra flere dimensjoner som:  

* Kontoen varesalget er bokført til.  
* Hvor varen ble solgt.
* Hvem som solgte den.
* Hvilken kunde som kjøpte produktet.

## <a name="analyzing-by-dimensions" />Analysere etter dimensjoner

Dimensjoner spiller en viktig rolle i forretningsintelligens, for eksempel når du definerer analysevisninger. Lær mer på [Analysere data etter dimensjoner](bi-how-analyze-data-dimension.md).

> [!TIP]
> En rask måte å analysere transaksjonsdata etter dimensjoner på er å bruke handlingen **Angi dimensjonsfilter** til å filtrere totalene etter dimensjoner i kontoplanen og på siden for poster.

> [!NOTE]
> Analysevisninger bruker ofte data fra dimensjoner. Hvis du oppdager at en feil dimensjon er blitt brukt i bokførte finansposter, kan du korrigere dimensjonsverdiene og oppdatere analysevisningene. Dette bidrar til at finansrapporter og analyser holdes nøyaktige. Se mer på [Feilsøke og korrigere dimensjoner](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting).

## <a name="dimension-sets" />Dimensjonssett

Et dimensjonssett er en unik kombinasjon av dimensjonsverdier. De lagres som dimensjonssettposter i databasen. Hver dimensjonssettpost representerer én enkelt dimensjonsverdi. I tillegg identifiseres hvert dimensjonssett og dimensjonssettoppføring i det, med en felles dimensjonssett-ID.  

Når du oppretter en kladdelinje, et dokumenthode eller en dokumentlinje, kan du angi en kombinasjon av dimensjonsverdier. I stedet for at hver dimensjonsverdi lagres eksplisitt i databasen, tilordnes en dimensjonssett-ID til kladdelinjen, dokumenthodet eller dokumentlinjen for å angi dimensjonssettet.  

## <a name="setting-up-dimensions" />Opprette dimensjoner

Du kan definere dimensjonene og dimensjonsverdiene for å kategorisere i kladder og dokumenter, for eksempel salgsordrer og bestillinger. Du definerer dimensjoner på **Dimensjoner**-siden der du oppretter én linje for hver dimensjon, som *Prosjekt*, *Avdeling*, *Område* og *Selger*.

Du også definere verdier for dimensjoner. La oss si at verdier representerer selskapets avdelinger. Dimensjonsverdier kan defineres i en hierarkisk struktur som ligner på kontoplanen. Dette betyr at data kan deles inn i ulike detaljnivåer, og delsett med dimensjonsverdier kan legges sammen. Du kan definere så mange dimensjoner og dimensjonsverdier som du trenger, og alle i firmaet kan bruke dem.

Når dimensjoner og verdier settes opp, kan du definere globale dimensjoner og snarveisdimensjoner på siden **Finansoppsett**. Disse dimensjonene er deretter alltid tilgjengelige for deg å velge som felt i kladde- og dokumentlinjer, og poster, uten å måtte åpne **Dimensjoner**-siden først. Lær mer i delen [Definere globale dimensjoner og snarveisdimensjoner](finance-dimensions.md#to-set-up-global-and-shortcut-dimensions).

* **Globale dimensjoner** brukes som filtre, for eksempel i rapporter, kjørsler og XMLport-er. Du kan bruke bare to globale dimensjoner, så velge dimensjonene du vil bruke ofte.
* **Snarveisdimensjoner** er tilgjengelige som felt på journaler, dokumentlinjer og finansposter. Du kan opprette opptil åtte av disse.  

> [!NOTE]
> Når du har brukt en ny dimensjon i en post, for eksempel en linje eller ny post, kan du ikke slette dimensjonen, selv om du ikke bokfører posten. Dette skyldes at [!INCLUDE[prod_short](includes/prod_short.md)] umiddelbart oppretter et dimensjonssett for linjen eller posten. Lær mer i delen [Dimensjonssett](finance-dimensions.md#dimension-sets).

### <a name="to-set-up-default-dimensions-for-customers-vendors-and-other-accounts" />Definere standarddimensjoner for kunder, leverandører og andre kontoer

Du kan tilordne en standarddimensjon for en spesifikk konto. Dimensjonen kopieres til kladden eller bilaget når du angi nummeret på en linje, men du kan slette eller endre koden på linjen, hvis aktuelt. Du kan også kreve en dimensjon for postering av en oppføring i en bestemt type konto. > 

> [!NOTE]
> Standard dimensjonsprioriteter åpner for scenarioer i salg og kjøp som du kanskje vil være ekstra oppmerksom på. Når du bruker standard dimensjonsprioriteter i salgs- og kjøpsdokumenter, anser [!INCLUDE [prod_short](includes/prod_short.md)] alltid dimensjonene i toppteksten som om den kommer fra kunden eller leverandøren. Dette gjelder dimensjoner du angir manuelt eller som standard, og er spesielt relevant når du bruker standarddimensjoner på lokasjoner og varer, men ikke på kunder eller leverandører.
>
> **Eksempel**
>
> Du har et scenario med følgende dimensjonsinnstillinger:
>
> * En kunde uten standarddimensjoner
> * En vare med ADM som dimensjonsverdien for AVDELING-dimensjonen
> * En lokasjon med PROD som dimensjonsverdien for AVDELING-dimensjonen
> * Standard dimensjonsprioriteter angis som kunde > vare > lokasjon
>
> Når du oppretter et nytt dokument i dette scenarioet, brukes dimensjoner på følgende måte:
>
> * Hvis du oppretter et nytt dokument og legger til en lokasjon, vil standardverdien for nye linjer være PROD. Når du legger til linjer med varer, beholder [!INCLUDE [prod_short](includes/prod_short.md)] PROD. fordi det kommer fra toppteksten til dokumentet.
>
> * Hvis du oppretter et nytt dokument og legger til varer som har en ADM-dimensjonsverdi, og deretter angir en lokasjon i dokumenttoppteksten, spør [!INCLUDE [prod_short](includes/prod_short.md)] om du vil overskrive eksisterende linjer fordi det er en konflikt.
>
> Vi anbefaler at du tester standard dimensjonsoppsett, dimensjonsprioriteter og rekkefølgen du registrerer data i, i dokumenter.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Dimensjoner**, og velg deretter den relaterte koblingen.  
2. Velg den relevante dimensjonen på siden **Dimensjoner**, og velg deretter handlingen **Kontotypens standarddim.**.  
3. Fyll ut en linje for hver ny standarddimensjon du vil definere. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
> Hvis du vil kreve en dimensjon, men uten å tilordne en standardverdi til dimensjonen, lar du feltet **Dimensjonsverdikode** være tomt, og deretter velger du **Obligatorisk kode** i feltet **Verdibokføring**.  

> [!WARNING]  
> Hvis en konto brukes i den satsvise jobben **Juster valutakurser** eller i **Bokfør lagerkost i Finans**, må du ikke velge **Obligatorisk kode** eller **Samme kode**. Disse kjørslene kan ikke bruke dimensjonskoder.  

> [!NOTE]  
> Hvis en konto må ha en annen dimensjon enn standarddimensjonen som er tilordnet kontotypen, må du opprette en standarddimensjon for denne kontoen. Standarddimensjonen for kontoen erstatter da standarddimensjonen for kontotypen.  

### <a name="to-set-up-default-dimension-priorities" />Slik setter du opp standard dimensjonsprioriteringer

Ulike kontotyper, for eksempel en kundekonto og en varekonto, kan ha ulike standarddimensjoner. Følgelig kan en post ha mer enn én foreslått standarddimensjon. For å unngå en slik konflikt, kan du sette opp prioriteringsregler for de ulike kildene.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Standarddimensjonsprioriteter**, og velg deretter den relaterte koblingen.  
2. På siden **Standarddimensjonsprioriteter**, i **Kildekode**-feltet, angir du kildesporet for posttabellen som standarddimensjonsprioriteter skal gjelde for.  
3. Fyll ut en linje for hver standarddimensjonsprioritet du vil bruke for det valgte kildesporet.
4. Gjenta prosedyren for hvert kildespor du vil definere standarddimensjonsprioriteter for.  

> [!IMPORTANT]  
> Hvis du definerer to tabeller med samme prioritet for samme kildespor, velger [!INCLUDE[prod_short](includes/prod_short.md)] alltid tabellen med lavest tabell-ID.  

### <a name="to-set-up-dimension-combinations" />Slik definerer du dimensjonskombinasjoner

For å unngå å bokføre poster med mostridende eller uaktuelle dimensjoner, kan du sperre eller begrense bestemte kombinasjoner av to dimensjoner. Hvis en dimensjonskombinasjon sperres, kan du ikke bokføre begge dimensjoner på samme post uansett hva dimensjonsverdiene er. En dimensjonskombinasjon derimot lar deg bokføre begge dimensjonene på samme post, men bare for bestemte kombinasjoner av dimensjonsverdier.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Dimensjonskombinasjoner**, og velg deretter den relaterte koblingen.  
2. Velg feltet for dimensjonskombinasjonen fra de følgende alternativene på siden **Dimensjonskombinasjoner**.  

    |Felt|Description|
    |----------------------------------|---------------------------------------|  
    |**Ingen begrensning**|Denne dimensjonskombinasjonen har ingen begrensninger. Alle dimensjonsverdiene er tillatt.|  
    |**Begrenset**|Denne dimensjonskombinasjonen har begrensninger som avhenger av hvilke dimensjonsverdier du angir. Du må definere begrensningene på siden **Dimensjonsverdikombinasjoner**.|  
    |**Sperret**|Denne dimensjonskombinasjonen er ikke tillatt.|  

3. Hvis du valgte alternativet **Begrenset**, må du definere hvilke kombinasjoner av dimensjonsverdier som skal sperres. Hvis du vil gjøre dette, velger du feltet for å definere verdikombinasjonen.  
4. Velg nå en dimensjonsverdikombinasjon som er sperret, og angi **Sperret** i feltet. Hvis feltet er tomt, betyr dette at dimensjonsverdikombinasjonen er tillatt. Gjenta hvis flere kombinasjoner er sperret.  

> [!NOTE]  
> De samme dimensjonene vises i både rader og kolonner, og derfor vises alle dimensjonskombinasjoner to ganger. [!INCLUDE[prod_short](includes/prod_short.md)] viser automatisk innstillingene i begge felt. Du kan ikke velge noe i feltene fra øverst til høyre og nedover fordi disse feltene har de samme dimensjonene i både rader og kolonner.  
>
> Det alternativet du har valgt vises ikke før du går ut av feltet.  
>
> Hvis du vil vise navnet på dimensjonene i stedet for koden, velger du feltet **Vis kolonnenavn**.

### <a name="to-set-up-global-and-shortcut-dimensions" />Definere globale dimensjoner og snarveisdimensjoner

Globale dimensjoner og snarveisdimensjoner kan brukes som filtre overalt i [!INCLUDE[prod_short](includes/prod_short.md)], inkludert i rapporter, kjørsler, finanspostsider og analysevisninger. Globale dimensjoner og snarveisdimensjoner kan settes inn direkte uten først å åpne **Dimensjoner** først. På kladdelinjer og dokumentlinjer kan du velge globale dimensjoner og snarveisdimensjoner i et felt på linjen. Du kan også definere to globale dimensjoner og åtte snarveisdimensjoner. Velg dimensjonene du bruker mest.

> [!IMPORTANT]
> Hvis du endrer en global dimensjon eller snarveisdimensjon, kreves det at alle poster med dimensjonen kan oppdateres. Hvis du vil endre en global dimensjon, kan du bruke funksjonen **Endre globale dimensjoner**, men det kan ta tid og kan påvirke ytelsen og tabeller kan være låst i løpet av oppdateringen. Sørg for å velge de globale dimensjonene og snarveisdimensjonene med omhu, slik at du trenger ikke å endre dem senere. Hvis du vil endre en snarveisdimensjon, bruker du handlingen **Endre dimensjoner**.
>
> Lær mer i delen [Endre globale dimensjoner](finance-dimensions.md#to-change-global-dimensions).

> [!NOTE]
> Når du legger til eller endrer en global dimensjon eller snarveisdimensjon, logges du automatisk av og på igjen, slik at den nye verdien klargjøres for bruk.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finansoppsett**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene på hurtigfanen **Dimensjoner**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="to-change-global-dimensions" />Endre globale dimensjoner

Når du endrer en global dimensjon eller snarveisdimensjon, oppdateres alle poster med dimensjonen. Denne prosessen kan ta tid, og det kan påvirke ytelsen, to forskjellige moduser oppgir for å tilpasse prosessen til størrelsen på databasen.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finansoppsett**, og velg deretter den relaterte koblingen.
2. Velg **Endre globale dimensjoner**-handlingen.
3. Øverst på siden velger du ett av følgende to modi for å kjøre den satsvise jobben.

    |Alternativ|Description|
    |-|-|
    |**Sekvensiell**|(Standard) Endringen utføres i én transaksjon som tilbakestiller alle poster til dimensjonene de hadde før endringen.<br /><br />Dette alternativet anbefales hvis selskapet inneholder relativt få bokførte poster, som det i så fall vil ta kortest tid å fylle det ut. Prosessen låser flere tabeller og blokkerer andre brukere til den er fullført. Vær oppmerksom på at i store databaser er det mulig at prosessen ikke kan fullføres i denne modusen. I dette tilfellet bruker du **Parallell**-alternativet.|
    |**Parallell**|Dimensjonsendringen oppstår i flere bakgrunnsøkter, og operasjonen deles inn i flere transaksjoner. Hvis du vil bruke dette alternativet, aktiverer du **Parallell behandling**. <br /><br />Dette alternativet anbefales for store databaser eller selskap med mange bokførte poster fordi det vil ta kort tid å fylle det ut. Vær oppmerksom på at når du bruker denne modusen, vil ikke oppdateringsprosessen starte hvis det finnes mer enn én aktiv databaseøkt.|  

4. Angi de nye dimensjonene   feltene **Global dimensjon 1-kode** eller **Global dimensjon 2-kode**. Nåværende dimensjoner vises i grått bak feltene.
5. Gjør ett av følgende, avhengig av modusen:
    * I **sekvensiell** modus velger du handlingen **Start**.
    * I **parallell** modus velger du handlingen **Klargjør**.

    **Loggposter**-fanen fylles ut med informasjon om dimensjonene som blir endret.
6. Logg av [!INCLUDE[prod_short](includes/prod_short.md)], og logg deretter på igjen.
7. Velg **Start**-handlingen for å starte parallell behandling av dimensjonsendringene.

### <a name="example-of-dimension-setup" />Eksempel på dimensjonsoppsett

La oss si at selskapet ønsker å spore transaksjoner som er basert på organisasjonsstruktur og geografiske steder. Hvis du vil gjøre dette, kan du definere to dimensjoner på **Dimensjoner**-siden:

* **OMRÅDE**  
* **AVDELING**  

|  - kode | Name | Kodetekst | Filtertekst |
| --- | --- | --- | --- |
| DISTRIKT |Distrikt |Områdekode |Områdefilter |
| AVDELING |Avdeling |Avdelingskode |Avdelingsfilter |

For **OMRÅDE** legger du til følgende dimensjonsverdier:

|  - kode | Name | Dimensjonsverditype |
| --- | --- | --- |
| 10 |Amerika |Fra-sum |
| 20 |Nord-Amerika |Standard |
| 30 |Stillehavet |Standard |
| 40 |Sør-Amerika |Standard |
| 50 |Amerika, totalt |Til-sum |
| 60 |Europa |Fra-sum |
| 70 |EU |Standard |
| 80 |Ikke-EU |Standard |
| 90 |Europa, totalt |Til-sum |

For de to viktigste geografiske områdene, Amerika og Europa, kan du legge til underkategorier for områder ved å rykke inn dimensjonsverdiene. Dette gjør at du kan rapportere på salg- eller utgifter i områder, og få totaler for større geografiske områder. Du kan også velge å bruke land, regioner, områder eller byer som dine dimensjonsverdier, avhengig av virksomheten din.

> [!NOTE]  
> Hvis du vil definere et hierarki, må kodene være i alfabetisk rekkefølge. Dette inkluderer kodene for dimensjonsverdiene som tilbys i [!INCLUDE[prod_short](includes/prod_short.md)].  

For **AVDELING** legger du til følgende dimensjonsverdier:

|  - kode | Name | Dimensjonsverditype |
| --- | --- | --- |
| ADMIN |Administrasjon |Standard |
| PROD |Produksjon |Standard |
| SALG |Salg |Standard |

Med dette satt opp kan du deretter legge til de to dimensjonene som to globale dimensjoner på **Finansoppsett**-siden. Dette betyr at du kan bruke OMRÅDE og AVDELING som filtre for finansposter og alle rapporter. Begge de globale dimensjonene blir også automatisk tilgjengelige til å brukes på postlinjer, i dokumenthoder og som snarveisdimensjoner.

## <a name="getting-an-overview-of-dimensions-used-multiple-times" />Få en oversikt over dimensjoner som brukes flere ganger

Siden **Standarddimensjoner – flere** angir hvordan en kontogruppe bruker dimensjoner og dimensjonsverdier. Du kan definere dette ved å utheve flere konti, angi standard dimensjoner og dimensjons verdier for dem. Deretter foreslår programmet disse dimensjonene og dimensjonsverdiene når én av disse kontiene brukes, for eksempel på en kladdelinje. Dette gjør det lettere for brukeren å bokføre poster, siden dimensjonsfeltene fylles ut automatisk. Legg imidlertid også merke til at dimensjonsverdiene som foreslås, kan endres på for eksempel kladdelinjer.

Siden **Standarddimensjoner – flere** inneholder følgende felt:

|Felt|Description|
|-----|-----------|  
|**Dimensjonskode**|Viser alle dimensjonene som er opprettet som standarddimensjoner i én eller flere av de uthevede kontiene. Ved å velge dette feltet kan du se en oversikt over alle tilgjengelige dimensjoner. Hvis du velger en dimensjon, defineres denne dimensjonen som standarddimensjon for alle uthevede konti.|
|**Dimensjonsverdikode**|Viser enten en enkelt dimensjonsverdi eller betingelsen (Konflikt). Hvis en dimensjonsverdi vises i feltet, har alle uthevede konti samme standarddimensjonsverdi for en dimensjon. Hvis betingelsen (Konflikt) vises i feltet, har ikke alle de uthevede kontiene samme standarddimensjonsverdi for en dimensjon. Når du velger feltet **Dimensjonskode**, vil du se en oversikt over alle tilgjengelige dimensjonsverdier for en dimensjon. Hvis du velger en dimensjonsverdi, defineres den som en standarddimensjonsverdi for alle uthevede konti.|
|**Verdibokføring**|Viser enten en enkelt regel for verdibokføring eller betingelsen (Konflikt). Hvis en verdibokføringsregel vises i feltet, har alle konti som er merket samme verdibokføringsregel for en dimensjonsverdi. Hvis betingelsen (Konflikt) vises i feltet, har ikke alle de merkede kontiene samme verdibokføringsregel for en dimensjonsverdi. Ved å velge feltet **Verdibokføring** vil du se en liste over verdibokføringsregler for en dimensjon. Hvis du velger en verdibokføringsregel, brukes den på alle uthevede kontoer.|

## <a name="use-dimensions" />Bruke dimensjoner

I et dokument, for eksempel en ordre, kan du legge til dimensjonsinformasjon om én enkelt dokumentlinje og selve dokumentet. På siden **Ordre** kan du for eksempel angi dimensjonsverdier for de to første snarveisdimensjonene direkte på de enkelte salgslinjene, og du kan legge til mer dimensjonsinformasjon hvis du velger knappen **Dimensjoner**.  

Hvis du i stedet arbeider i en kladd, kan du legge til dimensjonsinformasjon i en post på samme måte, forutsatt at du har opprettet snarveisdimensjoner som felt direkte i kladdelinjer.  

Du kan også definere standarddimensjoner for konti eller kontotyper, slik at dimensjoner og dimensjonsverdier fylles ut automatisk.

### <a name="to-view-global-dimensions-in-ledger-entry-pages" />Slik viser du globale dimensjoner på postsider:

Globale dimensjoner er alltid definerteog navngitt i henhold til selskap. Du viser de globale dimensjonene for selskapet ditt ved å åpne **Finansoppsett**-siden.

På en postside kan du se om det finnes globale dimensjoner for postene. De to globale dimensjonene skiller seg fra av dimensjoner ved at de kan brukes som filter over alt i [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kontoplan** og velger deretter den relaterte koblingen.  
2. På siden **Kontoplan** velger du handlingen **Poster**.  
3. Hvis du bare vil vise relevante poster, angir du ett eller flere filtre på siden.  
4. Hvis du vil vise alle dimensjonene for en post, velger du posten og klikker deretter på handlingen **Dimensjoner**.  

> [!NOTE]  
> Siden **Postdimensjoner** viser alle dimensjonene for én post om gangen. Når du blar gjennom postene, vil du se at innholdet endres på siden **Postdimensjoner** fortløpende.

## <a name="see-related-microsoft-trainingtrainingmodulesdimensions-dynamics--business-centralindex" />Se relatert [Microsoft-opplæring](/training/modules/dimensions-dynamics-365-business-central/index)

## <a name="see-also" />Se også

[Forretningsintelligens](bi.md)  
[Finans](finance.md)  
[Analysere data etter dimensjoner](bi-how-analyze-data-dimension.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
