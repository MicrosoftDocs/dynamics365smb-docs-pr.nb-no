---
title: Vareposter der lagernivået er null
description: Denne artikkelen beskriver et problem der lagernivået er null selv om det finnes åpne vareposter.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# Designdetaljer: Kjent vareutligningsproblem
Denne artikkelen beskriver et problem der lagernivået er null selv om det finnes åpne vareposter i [!INCLUDE[prod_short](includes/prod_short.md)].  

Artikkelen starter med å angi typiske symptomer på problemet, etterfulgt av grunnleggende informasjon om vareutligning for å støtte de angitte årsakene til dette problemet. På slutten av artikkelen er det en løsning for slike åpne vareposter.  

## Symptomer på problemet  
 Typiske symptomer på problemet med null lager selv om det finnes åpne vareposter, er følgende:  

-   Følgende melding når du prøver å lukke en lagerperiode: Lagerperioden kan ikke lukkes, ettersom det finnes negativ beholdning for én eller flere varer.  

-   En varepostsituasjon der både en utgående varepost og den tilhørende inngående vareposten er åpen.  

     Se følgende eksempel på en varepostsituasjon.  

     |Postnr.|Bokføringsdato|Posttype|Dokumenttype|Bilagsnr.|Varenr.|Lokasjonskode|Antall|Kostbeløp (faktisk)|Fakturert antall|Restantall|Åpne|  
     |---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|  
     |333|28.01.2018|Salg|Følgeseddel|102043|TEST|BLÅ|-1|-10|-1|-1|Ja|  
     |334|28.01.2018|Salg|Følgeseddel|102043|TEST|BLÅ|1|10|1|1|Ja|  

## Grunnleggende om vareutligning  
 En vareutligningspost opprettes for hver lagertransaksjon for å knytte kostmottakeren til kostkilden slik at kostnaden kan overføres i henhold til lagermetoden. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Vareutligning](design-details-item-application.md).  

-   For en inngående varepost opprettes vareutligningsposten når vareposten opprettes.  

-   For en utgående varepost opprettes vareutligningsposten når vareposten bokføres, hvis det finnes en åpen inngående varepost med disponibelt antall som den kan utlignes mot. Hvis det ikke finnes noen åpen inngående varepost som den kan utlignes mot, blir den utgående vareposten værende åpen til en inngående varepost som den kan utlignes mot, bokføres.  

 Det finnes to typer vareutligning:  

-   Antallsutligning  

-   Kostutligning  

### Antallsutligning  
 Antallsutligning utføres for alle lagertransaksjoner og opprettes automatisk, eller manuelt i spesielle prosesser. Når det gjøres manuelt, blir antallsutligning referert til som fast utligning.  

 Diagrammet nedenfor viser hvordan antallsutligning utføres.  

![Flyt for kostjustering fra kjøp til salg.](media/helene/TechArticleInventoryZero2.png "Flyt for kostjustering fra kjøp til salg")

 Legg merke til at ovenfor er varepost 1 (kjøp) både leverandør for varen og kostnadskilde for den utlignede vareposten, varepost 2 (salg).  

> [!NOTE]  
>  Hvis den utgående vareposten er verdisatt ved gjennomsnittskost, er ikke den utlignede inngående vareposten den unike kostnadskilden. Den inngår bare i beregningen av gjennomsnittskosten for perioden.  

### Kostutligning  
Kostutligning opprettes bare for innkommende transaksjoner når feltet **Utlignet fra-varepost** fylles ut for å angi en fast utligning. Dette skjer vanligvis i forbindelse med en salgskreditnota eller et scenario der levering angres. Kostutligningen sikrer at varen kommer inn på lageret igjen med samme kost som når den ble levert.  

Diagrammet nedenfor viser hvordan kostutligning utføres.  

|Postnr.|Bokføringsdato|Posttype|Dokumenttype|Bilagsnr.|Varenr.|Lokasjonskode|Antall|Kostbeløp (faktisk)|Fakturert antall|Restantall|Åpne|  
|---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|  
|333|28.01.2018|Salg|Følgeseddel|102043|TEST|BLÅ|-1|-10|-1|-1|Ja|  
|334|28.01.2018|Salg|Følgeseddel|102043|TEST|BLÅ|1|10|1|1|Ja|  

 Legg merke til ovenfor at inngående varepost 3 (ordreretur) er en kostmottaker for den opprinnelige utgående vareposten 2 (salg).  

## Bilde av en grunnleggende kostnadsflyt  
 Anta en komplett kostnadsflyt der en vare mottas, leveres og faktureres, returneres med nøyaktig\-kostnadstilbakeføring, og leveres på nytt.  

 Diagrammet nedenfor viser kostnadsflyten.  

![Flyt for kostjustering fra salg til ordreretur.](media/helene/TechArticleInventoryZero4.png "Flyt for kostjustering fra salg til ordreretur")

 Legg merke til ovenfor at kostnaden overføres til varepost 2 (salg), deretter til varepost 3 (ordreretur), og til sist til varepost 4 (salg 2).  

## Årsaker til problemet  
 Problemet med null lager selv om det finnes åpne vareposter, kan oppstå i følgende scenarioer:  

-   Scenario 1: En følgeseddel og faktura bokføres selv om varen ikke er tilgjengelig. Bokføringen blir deretter tilbakeført med opprinnelig kostpris med en salgskreditnota.  

-   Scenario 2: En følgeseddel bokføres selv om varen ikke er tilgjengelig. Bokføringen angres deretter med funksjonen Angre levering.  

 Diagrammet nedenfor viser hvordan vareutligning utføres i begge tilfellene.  

![Flyt for kostjustering går i begge retninger.](media/helene/TechArticleInventoryZero6.png "Flyt for kostjustering går i begge retninger")  

 Legg merke til ovenfor at en kostutligning utføres (angitt med blå pil) for å sikre at varepost 2 (ordreretur) tilordnes samme kostnader som vareposten som den tilbakefører, varepost 1 (salg 1). En antallsutligning (representert med rød pil) utføres imidlertid ikke.  

 Varepost 2 (ordreretur) kan ikke både være en kostnadsmottaker for den opprinnelige vareposten og samtidig være leverandør for varer og deres kostnadskilde Derfor forblir den opprinnelige vareposten 1 (salg 1) åpen til en gyldig kilde vises.  

## Identifisere problemet  
 For å finne ut om åpne vareposter er opprettet, kan du gjøre som følger for det respektive scenarioet:  

 For scenario 1, identifiser problemet på følgende måte:  

-   På siden **Bokført salgskreditnota** eller **Bokført returseddel** slår du opp fra feltet **Utlignet fra\--varepost** for å se om feltet er fylt ut, og i tilfelle til hvilken varepost returseddelen er kostnadsutlignet.  

 For scenario 2, identifiser problemet på en av følgende måter:  

-   Se etter en åpen utgående varepost og en inngående varepost med samme nummer i **Bilagsnr.**-feltet, og Ja i **Korreksjon**-feltet. Se følgende eksempel på en slik varepostsituasjon.  

|Postnr.|Bokføringsdato|Posttype|Dokumenttype|Bilagsnr.|Varenr.|Lokasjonskode|Antall|Kostbeløp (faktisk)|Fakturert antall|Restantall|Åpne|Korreksjon|  
|---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|---------|
|333|28.01.2018|Salg|Følgeseddel|102043|TEST|BLÅ|-1|-10|-1|-1|Ja|Nei|  
|334|28.01.2018|Salg|Følgeseddel|102043|TEST|BLÅ|1|10|1|1|Ja|**Ja**|  

-   På siden **Bokført følgeseddel** slår du opp fra feltet **Utlignet fra-varepost** for å se om feltet er fylt ut, og i tilfelle til hvilken varepost returseddelen er kostnadsutlignet.  

> [!NOTE]  
>  Kostnadsutligning kan ikke identifiseres på siden **Utlignede vareposter** fordi denne siden bare viser antallsutligning.  

 I begge scenarioene finner du den involverte kostnadsutligningen på følgende måte:  

1.  Åpne **Vareutligningspost**-tabellen.  

2.  Filtrer på **Varepostnr.**-feltet ved hjelp av nummeret på Ordreretur-vareposten.  

3.  Analyser vareutligningsposten og merk følgende:  

     Hvis feltet **Utgående vareløpenr.** er fylt ut for en inngående varepost (positivt antall), betyr det at den inngående vareposten er kostnadsmottakeren av den utgående vareposten.  

     Se følgende eksempel på en vareutligningspost,  

     |Postnr.|Varepostnr.|Inngående vareløpenr.|Utgående vareløpenr.|Antall|Bokføringsdato|Kostutligning|  
     |---------|---------------------|----------------------|-----------------------|--------|------------|----------------|  
     |299|334|334|333|1|28.01.2018|Ja|  
<!--![Why is inventory zero 8.](media/helene/TechArticleInventoryZero8.png "Whyisinventoryzero\_8")  -->

 Legg merke til ovenfor at den inngående vareposten 334 er utlignet mot utgående varepost 333.  

## Løsning for problemet  
 På **Varekladd**-siden bokfører du følgende linjer for den aktuelle varen:  

-   En oppjustering for å lukke den åpne utgående vareposten.  

-   En nedjustering med samme antall.  

     Denne justeringen balanserer lagerøkningen forårsaket av oppjusteringen og lukker den åpne inngående vareposten.  

 Resultatet er at beholdningen er null og alle vareposter lukkes.  

## Se også  
[Designdetaljer: Vareutligning](design-details-item-application.md)   
[Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]