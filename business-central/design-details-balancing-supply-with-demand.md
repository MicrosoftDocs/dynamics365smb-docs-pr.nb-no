---
title: "Designdetaljer – Balansere forsyning med behov | Microsoft-dokumentasjon"
description: "Kjernen i planleggingssystemet omfatter balansering av behov og forsyning ved å foreslå brukerhandlinger som endrer forsyningsordrene hvis det oppstår ubalanse. Dette skjer per kombinasjon av variant og lokasjon."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 51555bbfbd7fec6ca46bc1b2e6b02382288a41bc
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-balancing-supply-with-demand"></a>Designdetaljer: Balansere forsyning med behov
Kjernen i planleggingssystemet omfatter balansering av behov og forsyning ved å foreslå brukerhandlinger som endrer forsyningsordrene hvis det oppstår ubalanse. Dette skjer per kombinasjon av variant og lokasjon.  

Tenk deg at hver lagerprofil inneholder en streng med behovshendelser (sortert etter dato og prioritet) og en tilsvarende streng for forsyningshendelser. Hver hendelse refererer tilbake til kildetype og identifikasjon. Reglene for utligning av varen er enkle. Fire forekomster av tilsvarende behov og forsyning kan oppstå når som helst i prosessen:  

1. Det finnes verken behov eller forsyning for varen = > planleggingen er ferdig (eller skal ikke starte).  
2. Det finnes behov, men ingen forsyning = > forsyning må foreslås.  
3. Det finnes forsyning, men ikke behov for det = > forsyning må avbrytes.  
4. Både behov og forsyning finnes => spørsmål må stilles og besvares før systemet kan sikre at behovet kan dekkes og forsyningen er tilstrekkelig.  

     Hvis tidspunktet for forsyningen ikke passer, kan kanskje forsyningen planlegges på nytt som følger:  

    1.  Hvis forsyningen plasseres tidligere enn behovet, kan kanskje forsyningen planlegges ut slik at beholdningen er så lavt som mulig.  
    2.  Hvis forsyningen plasseres senere enn behovet, kan kanskje forsyningen planlegges inn. Hvis ikke vil systemet foreslå ny forsyning.  
    3.  Hvis forsyningen oppfyller behovet på datoen, kan planleggingssystemet fortsette å undersøke om forsyningsantallet kan dekke behovet.  

     Når tidsberegningen er på plass, kan det tilstrekkelig antallet som skal leveres, beregnes slik:  

    1.  Hvis forsyningsantallet er mindre enn behovet, kan det hende at forsyningsantallet kan reduseres (eller ikke, hvis det er begrenset av et prinsipp for maksimumsantall).  
    2.  Hvis forsyningsantallet er større enn behovet, kan det hende at forsyningsantallet kan reduseres (eller ikke, hvis det er begrenset av et prinsipp for minimumsantall).  

     På dette tidspunktet finnes en av disse to situasjonene:  

    1.  Gjeldende behov kan dekkes, og i så fall kan det lukkes, og planlegging for neste behov kan starte.  
    2.  Forsyningen har nådd maksimumet, og noe av behovsmengden er ikke dekket. I slike tilfeller kan planleggingssystemet lukke gjeldende forsyningen og fortsette til den neste.  

 Prosessen starter helt på nytt med det neste behovet og den aktuelle forsyningen eller omvendt. Gjeldende forsyning kan kanskje dekke neste behov også, eller gjeldende behov er ikke fullstendig dekket ennå.  

## <a name="rules-concerning-actions-for-supply-events"></a>Regler vedrørende handlinger for forsyningshendelser  
Når planleggingssystemet utfører en beregning ovenfra og nedover der forsyning må dekke behov, tas behovet som gitt, det vil si at planleggingssystemet ikke kan kontrollere det. Forsyningssiden kan Imidlertid administreres. Planleggingssystemet foreslår derfor å opprette nye forsyningsordrer, tidsplanlegge eksisterende på nytt og/eller endre ordreantallet. Hvis en eksisterende forsyningsordre blir overflødige foreslår planleggingssystemet at brukeren avbryter den.  

Hvis brukeren vil utelate en eksisterende forsyningsordre fra planleggingsforslagene, kan det angis at den ikke har planleggingsfleksibilitet (Planleggingsfleksibilitet = ingen). Overflødig forsyning fra denne ordren brukes deretter til å dekke behovet, men ingen handling foreslås.  

All forsyning har vanligvis en planleggingsfleksibilitet som er begrenset av betingelsene i hver av de foreslåtte handlingene.  

-   **Tidsplanlegg ut på nytt**: Datoen for en eksisterende forsyningsordre kan tidsplanlegges ut for å oppfylle forfallsdatoen for behovet med mindre følgende gjelder:  

    -   Den representerer beholdning (alltid på dag null).  
    -   Den har en ordre-til-ordre som er koblet til er annet behov.  
    -   Dette ligger utenfor vinduet for å planlegge på nytt, som angitt av tidsperioden.  
    -   En forsyning som er nærmere, kan brukes.  
    -   På den annen side kan brukeren velge ikke å planlegge på nytt fordi:  
    -   Forsyningsordren er allerede knyttet til et annet behov på en tidligere dato.  
    -   Den nye planleggingen som kreves, er så minimal at brukeren synes den er ubetydelig.  

-   **Tidsplanlegg inn på nytt**: datoen for en eksisterende forsyningsordre kan tidsplanlegges inn, unntatt når følgende gjelder:  

    -   Den er koblet direkte til et annet behov.  
    -   Dette ligger utenfor vinduet for å planlegge på nytt, som angitt av tidsperioden.  

> [!NOTE]  
>  Når en vare planlegges ved hjelp av et gjenbestillingspunkt, kan forsyningsordren alltid om nødvendig tidsplanlegges inn. Dette er vanlig i fremoverplanlagte forsyningsordrer som utløses av et gjenbestillingspunkt.  

-   **Øk antall**: Antallet i en eksisterende forsyningsordre kan økes for å dekke behovet, med mindre forsyningsordren er koblet direkte til et behov med en ordre-til-ordre-kobling.  

> [!NOTE]  
>  Selv om det er mulig å øke forsyningsordren, kan det være begrenset på grunn av et maksimumsordreantall.  

-   **Reduser antall**: En eksisterende forsyningsordre med et overskudd sammenlignet med et eksisterende behov kan reduseres for å dekke behovet.  

> [!NOTE]  
>  Selv om antallet kan reduseres, kan det fortsatt være noen overskudd sammenlignet med behovet på grunn av et angitt minimumsordreantall eller en bestillingsfaktor.  

-   **Avbryt**: Forsyningsordren kan avbrytes som en spesiell hendelse for handlingen for å redusere antallet, hvis den er blitt redusert til null.  
-   **Ny**: Hvis det ikke allerede finnes en forsyningsordre eller en eksisterende ikke kan endres til å dekke det nødvendige antallet på den etterspurte forfallsdatoen, blir det foreslått en ny forsyningsordre.  

## <a name="determining-the-supply-quantity"></a>Fastslå forsyningsantall  
Planleggingsparametre angitt av brukeren, styrer foreslåtte antall for hver ordre.  

Når planleggingssystemet beregner antallet for en ny forsyningsordre eller det endrede antallet i en eksisterende, kan foreslåtte antallet være forskjellig fra antallet det faktisk er behov for.  

Hvis maksimumsbeholdning eller fast ordreantall som er valgt, kan det foreslåtte vareantallet økes for å oppfylle det faste antallet eller maksimumsbeholdningen. Hvis gjenbestillingsprinsippet bruker et gjenbestillingspunkt, kan antallet i det minste økes for å dekke gjenbestillingspunktet.  

 Du kan endre det foreslåtte antallet i denne rekkefølgen:  

1. Ned til maks maksimumsordreantallet (hvis det finnes).  
2. Opp til det minste bestillingsantallet.  
3. Opp for oppfylle nærmeste bestillingsfaktor. (Dette kan bryte med maksimumsordreantallet ved feile innstillinger.)  

## <a name="order-tracking-links-during-planning"></a>Sporingskoblinger under planlegging  
Når det gjelder sporing under planleggingen, er det viktig å nevne at planleggingssystemet ordner de dynamisk opprettede sporingskoblingene for vare-/variant-/lokasjonskombinasjoner.  

Det er to årsaker til dette:  

-   Planleggingssystemet må kunne justere forslagene, slik at alle behov dekkes, og at ingen forsyningsordrer er overflødige.  
-   Sporingskoblinger som er opprettet dynamisk må balanseres på nytt regelmessig.  

Over tid kommer dynamiske sporingskoblinger ut av balanse fordi hele ordrensporingsnettverket ikke endres på nytt før en behovs- eller forsyningshendelse faktisk er lukket.  

Før du balansere forsyningen ved behov, slettes alle eksisterende sporingskoblinger. Når en en behovs- eller forsyningshendelse deretter lukkes under balanseringsprosessen, oppretter det nye sporingskoblinger mellom behov og forsyning.  

> [!NOTE]  
>  Selv om varen ikke er konfigurert for dynamisk ordresporing, vil det planlagte systemet opprette balanserte sporingskoblinger, som beskrevet ovenfor.  

## <a name="see-also"></a>Se også  
[Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md)   
[Designdetaljer: Sentrale begreper for planleggingssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)

