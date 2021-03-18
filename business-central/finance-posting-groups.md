---
title: Konfigurasjon av bokføringsgruppe | Microsoft-dokumentasjon
description: Oversikt over bokføringsgrupper du kan bruke for å spare tid og unngå feil når du bokfører transaksjoner.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting setup, initialize
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: b94b3ed97c0bd4d76c2ee5072bfda5de6ba86604
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379969"
---
# <a name="setting-up-posting-groups"></a>Definere bokføringsgrupper
Bokføringsgrupper tilordner enheter som kunder, leverandører, varer, ressurser og salgs- og kjøpsdokumenter til finanskonti. De sparer tid og unngår feil når du bokfører transaksjoner. Transaksjonsverdiene går til kontiene som er angitt i bokføringsgruppen for den bestemte enheten. Det eneste kravet er at du har en kontoplan. Hvis du vil ha mer informasjon, kan du se [Definere kontoplanen](finance-setup-chart-accounts.md).  

Bokføringsgruppene er dekket av tre paraplyer:  

* Generelt - definere hvem du selger til og kjøpe fra, og hva du selger og hva du kjøper. Du kan også slå sammen grupper for å angi ting som resultatkontiene bokføres til, eller du kan bruke grupper til å filtrere rapporter.  
* Spesifikk - bruk salgsdokumenter, i stedet for å bokføre direkte til Finans. Når du oppretter poster i finans, sikrer bokføringsgruppene at tilsvarende poster opprettes i Finans.  
* Mva - definere mva-prosent og beregningstyper som gjelder hvem du selger til og kjøpe fra, og hva du selger og hva du kjøper.

De følgende tabellene beskriver bokføringsgruppene under hver paraply.  

| Generelle bokføringsgrupper | Beskrivelse |
| --- | --- |
| Bokføringsgruppe - firma |Tilordne denne gruppen til kunder og leverandører for å angi hvem du selger til, og som du kjøper fra. Definer disse på siden **Bokføringsgrupper - firma**. Når du gjør, Tenk om hvor mange grupper du trenger å bryte ned kjøp og salg. Hvis du for eksempel gruppere kunder og leverandører etter geografisk område, eller ved type virksomhet. |
| Bokføringsgruppe - vare |Tilordne denne gruppen til varer og ressurser til å angi hva du selger, og hva du kjøper. Definer disse på siden **Bokføringsgrupper - vare**. Når du gjør, bør du vurdere hvor mange grupper du trenger til å bryte ned salg etter produkt (varer og ressurser) og kjøp av varer. Hvis du for eksempel del disse gruppene av råvarer, detaljhandel, ressurser, kapasitet og så videre. |
| Generelle bokføringsoppsett |Kombiner firma- og varebokføringsgrupper, og velg kontoene det skal posteres til. For hver kombinasjon av bokføringsgrupper for firma og vare kan du tilordne et sett med finanskontoer. Du kan eksempel bokføre salget av samme vare til ulike salgskonti i Finans fordi kunder er tilordnet til ulike bokføringsgrupper for firma. Definer disse på siden **Generelt bokføringsoppsett**. |

| Bestemte bokføringsgrupper | Description |
| --- | --- |
| Bokføringsgrupper - kunde |Definere konti som skal brukes når du bokfører transaksjoner for kortsiktige fordringer. Hvis du bruker lager med kundekonto, er det kombinasjonen av den generelle bokføringsgruppen for firma som er tilordnet kunden, og den generelle bokføringsgruppen for vare som er tilordnet lagervaren, som fastsetter hvilke kontoer salgsordrelinjene bokføres til. Se "Bokføringsgrupper - firma" og "Bokføringsgrupper – vare" under **Generelle bokføringsgrupper** over. Definer disse på siden **Bokføringsgrupper - kunde**. |
| Bokføringsgrupper - leverandør |Definere hvor du vil bokføre transaksjoner for leverandørkonto, gebyr og kontantrabattkontiene. Dette ligner på kundebokføringsgrupper. Definer disse på siden **Bokføringsgrupper - leverandør**. |
| Bokføringsgrupper - lager |Definer lagerbokføringsgrupper, som du deretter tilordner til relevante varekontor på siden **Lagerbokføringsoppsett**. Hvis du gjør dette når du bokfører poster som er knyttet til en vare, utføres det en bokføring i finanskontoen som er opprettet for kombinasjonen av lagerbokføringsgruppe og lokasjon som er knyttet til varen. Bokføringsgrupper for lager gir også et godt utgangspunkt for organisering av lageret, slik at du kan skille varer ved hjelp av bokføringsgruppene når du genererer rapporter. Definer disse på siden **Bokføringsgrupper - lager**. |
| Bokføringsgrupper - bank |Definer kontoer for bankkontoer. Dette kan for eksempel forenkle prosessene i transaksjonssporing og avstemming av bankkontoer. Definer disse på siden **Bokføringsgrupper - bank**. |
| Bokføringsgrupper - aktiva |Definer kontoer for diverse typer utgifter og kostnader, for eksempel anskaffelseskost, akkumulerte avskrivningsbeløp, anskaffelseskost ved salg, akkumulert avskrivning ved salg, vinning ved salg, tap ved salg, vedlikeholdsutgifter og avskrivningsutgifter. Definer disse på siden **Bokføringsgrupper - aktiva**. |

| Mva-bokføringsgruppe | Description |
| --- | --- |
| Mva-bokføringsgrupper - firma |Finn ut hvordan du kan beregne og postere merverdiavgift for kunder og leverandører. Definer disse på siden **Mva-bokføringsgrupper - firma**. Når du gjør, tenker på hvor mange grupper trenger du. Dette avhenger for eksempel av faktorer som lokal lovgivning og om du handler både innen- og utenlands. |
| Mva-bokføringsgrupper - vare |Angi mva-beregninger som trengs for typen varer eller ressurser du kjøper eller selger. |
| Mva-bokføringsoppsett |Kombiner mva-bokføringsgrupper for bedrifter og mva-bokføringsgrupper for varer. Når du fyller ut en kladdelinje, bestillingslinje eller salgslinje, skal vi se på kombinasjon til å identifisere konti som skal brukes. |

## <a name="example-of-linking-posting-groups"></a>Eksempel på kobling av bokføringsgruppe
Her er et scenario.  

Disse bokføringsgruppene er valgt på kundekortet:  

* Firmabokføringsgruppe
* Kundebokføringsgruppe  

Disse bokføringsgruppene er valgt på varekortet:  

* Generell produktbokføringsgruppe  
* Bokføringsgruppe - lager  

Når du oppretter et salgsdokument, bruker salgshodet informasjonen fra kundekortet, og salgslinjene bruker informasjonen fra varekortet.  

* Bokføringen av inntekter (resultat) fastsettes av kombinasjonen av bokføringsgruppen for firma og bokføringsgruppen for vare.  
* Bokføringen av kortsiktige fordringer (balanse) fastsettes av bokføringsgruppen for kunde.  
* Lagerbokføringen (balanse) fastsettes av bokføringsgruppen for lager.  
* Bokføringen av solgte varers kost (resultat) fastsettes av kombinasjonen av bokføringsgruppen for firma og bokføringsgruppen for vare.  

Oppsettet bestemmer når postering skjer. Hvis du for eksempel berørt tidsberegning av når du gjør periodiske aktiviteter, for eksempel bokføre lagerkostnaden eller justere kostverdi-vareposter.

## <a name="copying-posting-setup-lines"></a>Kopiere linjer for bokføringsoppsett
Jo flere bokføringsgrupper for vare og firma du har, jo flere linjer vil du se på siden Generelt bokføringsoppsett. Dette kan innebære mye dataregistrering for å definere det generelle bokføringsoppsettet for firmaet. Selv om det kan være mange ulike kombinasjoner av bokføringsgrupper for firma og vare, kan de ulike kombinasjonene likevel bokføre til de samme finanskontoene. Du kan begrense mengden manuell registrering ved kopiere finanskontoene fra en eksisterende linje på siden **Generelt bokføringsoppsett**.

## <a name="see-also"></a>Se også
[Finans og kontoplanen](finance-general-ledger.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]