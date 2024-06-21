---
title: Konsolidere data fra flere selskaper
description: Denne artikkelen forklarer hvordan du kan konsolidere finanspostene fra to eller flere atskilte selskaper (datterselskaper) i et konsolidert selskap.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 06/27/2023
ms.custom: bap-template
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.service: dynamics-365-business-central
---

# Konsolidere finansielle data fra flere selskaper

Noen organisasjoner bruker [!INCLUDE [prod_short](includes/prod_short.md)] i flere konsern eller juridiske enheter. Andre bruker [!INCLUDE [prod_short](includes/prod_short.md)] i datterselskaper som må rapportere til overordnede organisasjoner. [!INCLUDE [prod_short](includes/prod_short.md)] gir regnskapsførere verktøy som hjelper dem med å overføre finansposter fra to eller flere selskaper (datterselskaper) til et konsolidert selskap.  

Hvert selskap som er involvert i en konsolidering, kalles et konsern. Selskapet der du kombinerer dataene, kalles de konsoliderte selskapet.  

Du kan overføre økonomiske data fra datterselskaper til det konsoliderte selskapet, selv om datterselskapene bruker [!INCLUDE [prod_short](includes/prod_short.md)] i forskjellige miljøer. Hvis du vil lære mer om hvordan du kobler til andre miljøer, kan du gå til [Definere selskapskonsolidering](finance-consolidated-company-reporting-setup.md#busunit).

Hvis årsregnskapene i et konsern er i en annen valuta enn i det konsoliderte selskapet, må du definere valutakurser for konsolidering. Hvis du vil lære mer om valutakurser for konsolideringer, kan du gå til [Definere selskapskonsolidering](finance-consolidated-company-reporting-setup.md#exchrates).  

Du kan konsolidere:  

* På tvers av selskaper med ulike kontoplaner.  
* Selskaper med ulike regnskapsår og i ulike valutaer.  
* Hele beløpet eller en prosentdel av den økonomiske informasjonen i et selskap.
* Bruke ulike valutakurser i individuelle finanskontoer.
* Selskaper i andre regnskaps- og forretningsstyringsprogrammer.
* Selskaper i ulike [!INCLUDE [prod_short](includes/prod_short.md)]-miljøer.

Du definerer det konsoliderte selskapet på samme måte som du definerer andre selskaper. Kontoplanen er uavhengig av kontoplanen i konsernene. Kontoplanen i konsernene kan være forskjellige fra hverandre. Hvis du vil ha mer informasjon om hvordan du definerer en konsolidering, går du til [Konfigurer selskapskonsolidering](finance-consolidated-company-reporting-setup.md).  

> [!TIP]
> Konsolidere økonomisk data kan være spesielt aktuelt for konserninterne prosesser. Hvis du vil lære mer om konserninterne funksjoner, kan du gå til [Behandle konserninterne transaksjoner](intercompany-manage.md).

## Konsolidere data

Før du konsoliderer er det lurt å teste dataene før du overfører dem til det konsoliderte selskapet. [!INCLUDE[prod_short](includes/prod_short.md)] ser etter forskjeller mellom informasjonen i konsernet og det konsoliderte selskapet. Dette kan for eksempel være om kontonumre eller dimensjonskoder er forskjellige. Korriger feil du finner, før du kan kjøre rapporten. Du kan teste databasen, eller, hvis du importerer data fra en XML-fil, filen.

### Teste dataene før konsolidering

1. Åpne det konsoliderte selskapet.  
2. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konsern**, og velg deretter den relaterte koblingen.  
3. Test filen og databasen på følgende måte:  

    * For å teste en fil velger du **Test fil**, angir navnet på filen som skal testes, og velger deretter **Skriv ut**.  
    * Hvis du vil teste databasen, kan du velge **Test database**.  

### Kjøre konsolideringen

Når du har testet dataene, kan du overføre dem til det konsoliderte selskapet. En assistert oppsettsveiledning hjelper deg gjennom prosessen.

> [!NOTE]
> Når du kjører konsolideringen, kan du velge hvilke selskaper du vil ha med videre. Hvis det konsoliderte selskapet ikke har tilgang til ett eller flere datterselskaper, lar veiledningen deg gi tilgang til dem.

1. Logg deg på det konsoliderte selskapet.  
2. På siden **Konsern** velger du handlingen **Konsolider**.  
3. Fyll ut de obligatoriske feltene.  

## Bruk rapporten Konsolidert råbalanse

Rapporten **Konsolidert råbalanse** kan gi deg en samlet oversikt over den generelle økonomiske situasjonen. Rapporten kombinerer finansposter fra hvert av selskapene i et nytt selskap du opprettet for de konsoliderte dataene. Det konsoliderte selskapet er bare en beholder for de konsoliderte dataene og har ikke noen publiserte forretningsdata. Selskapene du tar med i det konsoliderte selskapet, blir **Konserner** i rapporten. Hvis du har fire eller færre konsern, kan du også bruke rapporten **Kons.råbalanse - 4 firma**.  

Rapporten viser en linje for hver konto, og følger strukturen til kontoplanen. En konto skrives ikke ut hvis alle beløp på linjen er 0. Rapporter viser følgende opplysningene om hver konto:

* Kontonummeret og navnet på kontoen.
* Totalene for det konsoliderte selskapet og for hvert konsern. Totalene kan vises som bevegelse eller saldo til dato.
* Elimineringer foretatt i det konsoliderte selskapet. Elimineringer vises alltid for en periode som tilsvarer det konsoliderte selskapets regnskapsår.
* Totalen for det konsoliderte selskapet etter elimineringer vises som bevegelse eller saldo.

## Fjerne gjentatte transaksjoner

Når du konsoliderer selskapene, må du finne og eliminere transaksjoner som er registrert mer enn én gang på tvers av flere selskaper. Behandle konsoliderte elimineringer i en manuell prosess.  

Slik fjerner du gjentatte transaksjoner:

1. Finn transaksjoner som kanskje må justeres, og angi finanskladdelinjer for å fjerne dem.
2. Kjør rapporten **Konsoliderte elimineringer for finans** for å vurdere resultatet av finanskladdelinjene før bokføringen.
3. Bokfør justeringstransaksjonene.

Rapporten **Finanskonsolideringselimineringer** viser en foreløpig råbalanse der du kan simulere konsekvensene av å eliminere poster. Rapporten sammenligner postene i det konsoliderte selskapet med elimineringene som er angitt i finanskladden.

Før du kan inkludere en forretningsenhet i rapporten, må du sette opp enheten på siden **Konsern**. Sørg for å slå på **Konsolider**-bryteren .

En linje opprettes for hver konto, i likhet med kontoplanens oppbygning. En konto skrives ikke ut hvis alle beløp på linjen er 0. Rapporter viser følgende opplysningene om hver konto:

* Kontonummer.
* Kontonavn.
* Hvis du har valgt en eller flere konsernkoder i feltet **Konsernkode** på forespørselssiden, vises totalen for det konsoliderte selskapet ekskluderer de valgte konsernene og elimineringene. Hvis du ikke har fylt ut feltet **Konsernkode**, vises totalen for det konsoliderte selskapet ekskludert elimineringer.
* Hvis du har valgt en konsernkode i feltet **Konsernkode** på forespørselssiden, vises totalen for de innleste postene fra konsernet. Hvis du ikke har fylt ut feltet **Konsernkode**, vises totalen for bokførte elimineringer i det konsoliderte selskapet.
* Totalen for det konsoliderte selskapet med alle konsern og alle bokførte elimineringer.
* Elimineringer som skal gjøres i det konsoliderte selskapet. Det vil si oppføringene i finanskladden som er valgt på forespørselssiden.
* Bokføringsteksten kopiert fra finanskladden.
* Det konsoliderte selskapets total etter elimineringen hvis den bokføres.

## Eksportere og importere konsoliderte data mellom databaser

Hvis data for et konsern er i en annen database, kan du utføre en manuell filbasert overføring eller automatisere prosessen ved hjelp av en API. Hvis du vil vite mer om API-et, kan du gå til [Bruk API-et vårt til å dele data automatisk på tvers av miljøer](#use-our-api-to-automatically-share-data-across-environments).

Denne delen beskriver den manuelle, filbaserte prosessen.

Du eksporterer dataene til en fil før du inkluderer dem i konsolideringen. Eksportere hvert selskap separat ved hjelp av kjørselen **Eksporter konsolidering** .  

> [!TIP]
> Bruk samme prosess for å eksportere konsoliderte data som du må sende til Dynamics 365 Finance. Hvis for eksempel konsernet er et datterselskap og morselskapet bruker Dynamics 365 Finance.

Når du kjører den satsvise jobben, behandles alle postene i finanskontiene. For hver kombinasjon av valgte dimensjoner og dato legges innholdet fra postenes **Beløp**-felt sammen og eksporteres. Den neste kombinasjonen av de valgte dimensjonene og datoene med samme kontonummer behandles. Deretter behandles kombinasjonene i det neste kontonummeret og så videre.  

De eksporterte postene inneholder følgende felt: **Kontonr.**, **Bokføringsdato** og **Beløp**. Hvis dimensjonsinformasjon også ble eksportert, er dimensjonskoder og dimensjonsverdier også inkludert.  

1. For hver eksporterte linje eksporteres kontonummeret som er definert i konsernets **Kons. debetkonto**-felt, til linjen, hvis summen i **Beløp**-feltene er et debetbeløp. Hvis summen er et kreditbeløp, eksporteres det tilsvarende nummeret i **Kons. kreditkonto**-feltet til linjen.  
2. Datoen som brukes for hver eksporterte linje, er periodens sluttdato eller den nøyaktige datoen for beregningen, hvis overføringen skjer hver dag.  
3. Dimensjonsverdien som eksporteres for posten, vil være dimensjonsverdien for det konsoliderte selskapet som er angitt i **Konsolideringskode**-feltet for den aktuelle dimensjonsverdien. Hvis en dimensjonsverdi for konsolidert selskap ikke er angitt i **Konsolideringskode**-feltet for den aktuelle dimensjonsverdien, vil selve dimensjonsverdien bli eksportert til linjen.  
4. XML-filene inneholder også valutakursene i konsolideringsperioden. Disse kursene er inkludert i en separat del på begynnelsen av filen.  

## Bruk vår API til automatisk å dele data på tvers av miljøer

[!INCLUDE [prod_short](includes/prod_short.md)] gir deg en API som lar deg automatisere prosessen med å dele økonomiske data fra konsern til det konsoliderte selskapet. API-en er gratis å bruke og enkel å sette opp. Det lar deg til og med dele data på tvers av [!INCLUDE [prod_short](includes/prod_short.md)]-miljøer. Det kan for eksempel hende at du må dele på tvers av miljøer når forretningsenheter ikke er i de samme Azure-geografiene. Hvis du vil lære mer om hvordan du bruker API-en til å automatisere konsolideringsprosessen, kan du gå til [Konfigurere selskapskonsolidering](finance-consolidated-company-reporting-setup.md#busunit).

## Se også

[Konfigurer selskapskonsolidering](finance-consolidated-company-reporting-setup.md)  
[Behandle konserninterne transaksjoner](intercompany-manage.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Eksporter forretningsdataene til Excel](about-export-data.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]