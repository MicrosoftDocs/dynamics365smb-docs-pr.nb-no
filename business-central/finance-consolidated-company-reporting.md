---
title: Konsolidere data fra flere selskaper | Microsoft-dokumentasjon
description: "Få en oversikt over den økonomiske situasjonen for alle selskapene dine."
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: consolidation, subsidiaries, consolidate
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 035eb85050ec6feb9e65ee924ebf4dbd2064e5ba
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---

# <a name="consolidating-financial-data-from-multiple-companies"></a>Konsolidere finansielle data fra flere selskaper
Hvis du har mer enn ett selskap i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan rapporten for konsolidert råbalanse i Rollesenter for regnskapsfører gi deg en samlet oversikt over den økonomiske situasjonen.  

Rapporten kombinerer finansposter fra hvert av selskapene i et nytt selskap du oppretter med de konsoliderte dataene. Dette selskapet kalles vanligvis for "det konsoliderte selskapet". Det konsoliderte selskapet er bare en beholder for de konsoliderte dataene og har ikke noen live forretningsdata. Selskapene du tar med i det konsoliderte selskapet, blir **Konserner** i rapporten.

Konsolidere økonomisk data kan være spesielt aktuelt i forbindelse med konserninterne prosesser. Hvis du vil ha mer informasjon, kan du se [Behandle konserninterne transaksjoner](intercompany-manage.md).

Du kan konsolidere:  

* På tvers av selskaper med ulike kontoplaner.  
* Selskaper med ulike regnskapsår og i ulike valutaer.  
* Hele beløpet eller en prosentdel av den økonomiske informasjonen i et selskap
* Bruke ulike valutakurser i individuelle finanskontoer

Det finnes to måter å definere rapporten på, avhengig av forretningenes kompleksitet:

* Hvis du ikke trenger avanserte innstillinger, for eksempel inkludere et selskap som du bare eier en del av, kan du bruke veiledningen **Selskapskonsolidering** med assistert oppsett for å definere en konsolidering raskt. Veiledningen hjelper deg gjennom de grunnleggende trinnene.
* Hvis du trenger mer avanserte innstillinger, kan du definere det konsoliderte selskapet og konsernene selv.

## <a name="to-do-a-simple-consolidation-setup"></a>Slik utfører du et enkelt konsolideringsoppsett
Hvis konsolideringen er enkel, for eksempel fordi du er eneeier av konsernene som skal konsolideres, vil veiledningen **Selskapskonsolidering** med assistert oppsett hjelpe deg gjennom følgende trinn:

* Velg om du vil opprette et nytt konsolidert selskap eller om du vil konsolidere dataene i et selskap som allerede er opprettet for konsolidering. Selskapet kan ikke inneholde transaksjoner.
* Forhåndsvis resultatene. [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerer at hoveddata og transaksjoner kan bli overført til det konsoliderte selskapet.

Hvis du vil bruke veiledningen med assistert oppsett, gjør du følgende:

1. I **Regnskapsfører**-rollesenteret velger du **Assistert oppsett**.
2. Velg **Konfigurer konsolideringsrapportering**, og fullfør deretter hvert trinn i veiledningen med assistert oppsett.

## <a name="to-do-an-advanced-consolidation-setup"></a>Slik gjør du et avansert konsolideringsoppsett
Hvis du trenger mer avanserte innstillingene for konsolideringen, kan du definere konsolideringen manuelt. For eksempel hvis du har selskaper som du bare eier delvis, eller hvis du har selskaper som du ikke vil ta med i konsolideringen. Du definerer det konsoliderte selskapet på samme måte som du definerer andre selskaper. Hvis du vil ha mer informasjon, kan du se [Bli klar til å gjøre forretninger](ui-get-ready-business.md).  

[!INCLUDE[d365fin](includes/d365fin_md.md)] lar deg sette opp en liste over selskaper som skal konsolideres, bekrefte regnskapsdataene før du konsoliderer dem, importere filer og generere konsolideringsrapporter.  

1. Logg deg på det konsoliderte selskapet.
2. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konsern**, og velg deretter den relaterte koblingen.  
3. Velg **Ny**, og fyll deretter ut de obligatoriske feltene.  

Hvis konsernet bruker en fremmed valuta, må du angi hvilken valutakurs som skal brukes i konsolideringen. Du må også angi konsolideringsopplysninger om konsernets finanskonti. Disse prosessene beskrives nedenfor.

### <a name="to-prepare-general-ledger-accounts-for-consolidation"></a>Slik klargjør du finanskonti for konsolidering
Hvis kontoplanen i konsernet er forskjellig fra det konsoliderte selskapet, må du klargjøre finanskonti for konsolidering. Du kan angi kontiene for å bokføre debet og kredit og metoden som skal brukes til å oversette valutaer i det konsoliderte selskapet. Dette er for eksempel nyttig hvis du kjører rapporten ofte.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kontoplan**, og velg deretter den relaterte koblingen.  
2. Åpne kortet for kontoen, og deretter fyller du ut feltene på **Konsolidering**-hurtigfanen.

### <a name="to-specify-exchange-rates-for-consolidations"></a>Slik angir du valutakurser for konsolideringer
Hvis et konsern bruker en annen valuta enn det konsoliderte selskapet, må du angi valutakursmetoder for hver konto før du konsoliderer. For hver konto bestemmer innholdet i feltet **Kons. oversettelsesmetode** valutakursen. På hvert konsernkort angir du i **Valutakurstabell**-feltet om konsolidering skal bruke valutakurser fra konsernselskapet eller det konsoliderte selskapet. Hvis du bruker valutakurser fra det konsoliderte selskapet, kan du endre valutakursene for et konsern. For konserner, hvis feltet **Valutakurstabell** på konsernkortet inneholder **Lokal**, kan du endre valutakursen fra konsernkortet. Valutakurser kopieres fra **Valutakurs**-tabellen, men du kan endre dem før konsolidering.

Tabellen nedenfor beskriver valutakursmetodene du kan bruke for kontoer.

|Valutakurs | Vanlig bruk |
|---|---|
|Gjennomsnittskurs (manuell) | Du beregner gjennomsnittskursen manuelt for perioden som skal konsolideres. Beregn gjennomsnittet som et aritmetisk gjennomsnitt eller som et best mulig overslag, og angi resultatet for hvert konsern. Brukes for resultatregnskapskonti.|
|Sluttkurs | Brukes for balansekonti.|
|Siste sluttkurs | Kursen som gjaldt på valutamarkedet på datoen som balansen eller resultatregnskapet forberedes for. Du angir denne kursen for hvert konsern. Brukes for balansekonti.|
|Historisk kurs | Valutakursen som var gyldig da transaksjonen ble utført.|
|Sammensatt kurs | Gjeldende periodebeløp omregnes med gjennomsnittskursen og legges til i den tidligere registrerte balansen i det konsoliderte selskapet. Denne metoden brukes vanligvis for konti for fri egenkapital fordi de inkluderer beløp fra forskjellige perioder og består dermed av en sammensetning av beløp som er omregnet med forskjellig valutakurs.|
|Egenkapitalkurs | Dette ligner på **Sammensatt**. Forskjellene bokføres på separate finanskonti.|   

Du kan angi valutakurser for konserner ved å gjøre følgende:

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konsern**, og velg deretter den relaterte koblingen.  
2. I vinduet **Konsernoversikt** velger du konsernet og velger deretter **Gjennomsnittskurs (manuell)**.   
3. I vinduet **Endre valutakurs** har innholdet i feltet **Tilhørende valutakursbeløp** blitt kopiert fra **Valutakurs**-tabellen, men du kan endre det. Lukk siden.  
4. Velg handlingen **Sluttkurs**.  
5. I feltet **Tilhørende valutakursbeløp** angir du valutakursen.

<!-- ### To include or exclude dimensions

COMMENTING THIS OUT BECAUSE i CANNOT REPRODUCE THE SETTINGS. tHERE IS NO CONSOLIDATION CODE FIELD ON DIMENSIONS OR DIMENSIOIN VALUES.

You can consolidate dimension information and general ledger accounts, as follows:

* To exclude dimension information in the consolidation, leave the **Consolidation Code** field blank, and do not choose dimensions in the **Copy Dimensions** fields in any consolidation functions or reports described later in this topic.
* To include dimension information in the consolidation, leave the **Consolidation Code** field blank. However, the consolidation will only work if the dimension values in the business unit are the same as the consolidated company.
* To consolidate the dimension value code in the business unit with a different dimension value code in the consolidated company, fill in the **Consolidation Code**. -->

### <a name="to-exclude-a-company-from-consolidation"></a>Slik utelater du et selskap fra konsolidering
Hvis du ikke vil ta med et konsern i konsolideringen, kan du utelate det. Hvis du vil gjøre dette, går du til konsernkortet og fjerner merket for **Konsolider**.

### <a name="to-include-a-partially-owned-company-in-consolidation"></a>Slik inkluderer du et delvis eid selskap i konsolideringen
Hvis du bare eier en del av et selskap, kan du ta med en prosentandel av hver enkelt transaksjon som samsvarer med prosentdelen av selskapet du eier. Hvis du for eksempel eier 70 % av selskapet, vil konsolideringen inkludere 70 kr av en faktura på 100 kr. For å angi hvor stor del av selskapet du eier, går du til konsernkortet og skriver inn prosentsatsen i feltet **Konsoliderings-%**.  

### <a name="to-test-the-data-before-you-consolidate"></a>Slik tester du dataene før konsolidering
Du kan teste dataene før du overfører dem til det konsoliderte selskapet. [!INCLUDE[d365fin](includes/d365fin_md.md)] ser etter forskjeller mellom informasjonen i konsernet og det konsoliderte selskapet. Dette kan for eksempel være om kontonumre eller dimensjonskoder er forskjellige. Du må korrigere feilene før du kan kjøre rapporten. Du kan teste databasen, eller hvis du importerer data fra en XML-fil, kan du teste filen.   

1. Åpne det konsoliderte selskapet.  
2. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konsern**, og velg deretter den relaterte koblingen.  
3. Gjør ett av følgende:  

    * For å teste en fil velger du **Test fil**, angir navnet på filen som skal testes, og velger deretter **Skriv ut**.  
    * Hvis du vil teste databasen, kan du velge **Test database**.  

## <a name="to-run-the-consolidation"></a>Slik kjører du konsolideringen
Når du har testet dataene, kan du overføre dem til det konsoliderte selskapet.  

1. Logg deg på det konsoliderte selskapet.  
2. I **Regnskapsfører-rollesenteret** velger du **Kjør konsolidering**.  
3. Fyll ut de obligatoriske feltene.  
4. I **Der**-feltet velger du **Selskapsnavn** og velger deretter det konsoliderte selskapet i **er**-feltet.  

## <a name="to-export-and-import-consolidated-data-between-databases"></a>Slik eksporterer og importerer du konsoliderte data mellom databaser
Hvis data for et konsern er i en annen database, må du eksportere dataene til en fil før du kan inkludere dem i konsolideringen. Hvert selskap må eksporteres separat. Til dette formålet brukes kjørselen **Eksporter konsolidering**.  

Når du kjører den satsvise jobben, behandles alle postene i finanskontiene. For hver kombinasjon av valgte dimensjoner og dato legges innholdet fra postenes **Beløp**-felt sammen og eksporteres. Neste kombinasjon av valgte dimensjoner og dato med samme kontonummer blir behandlet, deretter behandles kombinasjonene for neste kontonummer og så videre.  

De eksporterte postene inneholder følgende felt: **Kontonr.**, **Bokføringsdato** og **Beløp**. Hvis dimensjonsinformasjon også ble eksportert, er dimensjonskoder og dimensjonsverdier også inkludert.  

1. For hver eksporterte linje eksporteres kontonummeret som er definert i konsernets **Kons. debetkonto**-felt, til linjen, hvis summen i **Beløp**-feltene er et debetbeløp. Hvis summen er et kreditbeløp, eksporteres det tilsvarende nummeret i **Kons. kreditkonto**-feltet til linjen.  
2. Datoen som brukes for hver eksporterte linje, er periodens sluttdato eller den nøyaktige datoen for beregningen, hvis overføringen skjer hver dag.  
3. Dimensjonsverdien som eksporteres for posten, vil være dimensjonsverdien for det konsoliderte selskapet som er definert i **Konsolideringskode**-feltet for den aktuelle dimensjonsverdien. Hvis ingen dimensjonsverdi for konsolidert selskap er angitt i **Konsolideringskode**-feltet for den aktuelle dimensjonsverdien, vil selve dimensjonsverdien bli eksportert til linjen.   
4. XML-filene inneholder også valutakursene i konsolideringsperioden. Disse kursene er inkludert i en separat del på begynnelsen av filen.

## <a name="see-also"></a>Se også
[Behandle konserninterne transaksjoner](intercompany-manage.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Eksportere forretningsdataene til Excel](about-export-data.md)

