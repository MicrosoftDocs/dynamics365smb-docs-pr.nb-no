---
title: Kryssoverføre varer| Microsoft-dokumentasjon
description: Kryssoverføringsfunksjonalitet er tilgjengelig hvis du har definert lokasjonen slik at den krever lagermottaksbehandling og plasseringsbehandling.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 558b93677d4045f68bdc6fea0b68936658816b92
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759845"
---
# <a name="cross-dock-items"></a>Kryssoverføringsvarer
Kryssoverføringsfunksjonalitet er tilgjengelig hvis du har definert lokasjonen slik at den krever lagermottaksbehandling og plasseringsbehandling.  

Når du kryssoverfører varer, behandler du varer i mottak og levering uten å plassere dem på lager, og derved ekspederer du varen ved hjelp av plasserings- og plukkprosesser, og begrenser den fysiske håndteringen av varer. Du kan kryssoverføre varer for både leveringer og produksjonsordrer. Når du forbereder en levering eller plukker varer for produksjon og bruker hyller, plukkes varen automatisk fra en kryssoverføringshylle før noen annen hylle. Du må se i kryssoverføringsområdet for å finne ut om de varene du trenger, er tilgjengelig der før du henter varene fra det vanlige lagringsområdet.  

Hvis du har beregnet kryssoverføringsantall, opprettes plasseringslinjer til kryssoverføringshyllen for kryssoverføringsberegning når du bokfører mottaket. Andre plasseringslinjer blir opprettet som vanlig.  

Hvis du vil bokføre de kryssoverførte varene med en gang slik at de blir tilgjengelig for plukking, må du også registrere en plassering for de andre varene som kom fra mottakslinjen, nemlig de som må lagres. Hvis bare noen av varene på en mottakslinje blir kryssoverført, må du derfor sørge for å plassere resten av varene så snart som mulig. Lageret kan også ha regler som sier at kryssoverføring av hele mottakslinjer skal utføres så sant det er mulig.  

I plasseringsinstruksjonen kan du med fordel slette både Hent- og Plasser-instuksjonslinjer for hver mottakslinje som gjelder mottak som helt skal plasseres på lager. Disse linjene kan senere opprettes som plasseringslinjer fra plasseringsforslaget eller det bokførte mottaket. Når de er slettet, kan du plassere og registrere linjene som dreier seg om kryssoverførte varer.  

Hvis du har valgt feltet **Bruk plasseringsforslag** på lokasjonskortet og har bokført mottaket med beregnede kryssoverføringer, blir alle mottakslinjene tilgjengelig i forslaget. Informasjonen om kryssoverføringen går tapt, og den kan ikke gjenopprettes. Hvis du ønsker å bruke kryssoverføringsfunksjonaliteten, bør du derfor overføre linjer til plasseringsforslaget ved å slette plasseringsinstruksjoner i stedet for å bruke den automatiske overføringsfunksjonen i feltet **Bruk plasseringsforslag**.  

Hvis du bokfører lagermottaket og du ikke har valgt feltet **Bruk plasseringsforslag**, vises varene som skal kryssoverføres som separate linjer i plasseringsinstruksen. Feltet **Kryssoverføringsinformasjon** på hver plasseringslinje viser om linjen inneholder kryssoverførte varer, varer fra samme mottak som alle må lagres, eller varer som må lagres som kommer fra en mottakslinje der noen av varene skal kryssoverføres. Med dette feltet kan de ansatte enkelt se hvorfor hele mottaksantallet ikke blir plassert på lager.  

Programmet har ikke separate poster om varer som er kryssoverført, men det registrerer dem som vanlige plasseringsinstruksjoner.  

## <a name="to-set-up-the-warehouse-for-cross-docking"></a>Slik definerer du lageret for kryssoverføring  
1.  Definer minst én kryssoverføringshylle hvis du bruker hyller. Definer en kryssoverføringssone hvis du bruker lagerstyring.  

    Det er merket av for **Kryssoverføringshylle** for en kryssoverføringshylle, og både hylletypen **Motta** og **Plukke** må være valgt. Hvis du vil ha mer informasjon, kan du se [Opprette hyller](warehouse-how-to-create-individual-bins.md) og [Definere hylletyper](warehouse-how-to-set-up-bin-types.md).  

    Hvis du bruker soner, oppretter du en sone for kryssoverføringshyllene og velger feltet **Kryssoverføringshyllesone**. Hvis du vil ha mer informasjon, kan du se [Definere lokasjoner slik at de bruker hyller](warehouse-how-to-set-up-locations-to-use-bins.md).  

2.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lokasjon**, og velg deretter den relaterte koblingen.  
3.  Velg lokasjonen der du vil definere lageret for kryssoverføring, på siden **Lokasjon**, og velg deretter **Rediger**-handlingen.  
4.  På hurtigfanen **Lager**, merker du av for **Bruk kryssoverføring** og fyller ut feltet **Kryssoverføring forfallsdatoberegn.** med tidspunktet for å søke etter kryssoverføringsmuligheter.

    Alternativet **Bruk kryssoverføring** er bare tilgjengelig hvis feltene **Mottak nødv.**, **Levering nødv.**, **Plukk nødv.** og **Plassering nødv.** er valgt.  

5.  Hvis du bruker hyller, fyller du ut feltet **Hyllekode for kryssoverføring** på hurtigfanen **Hyller** med koden for hyllen du vil bruke som standard kryssoverføringshylle.  
6.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagerføringsenhet**, og velg deretter den relaterte koblingen.  
7.  For hver vare eller lagerføringsenhet du ønsker å kunne kryssoverføre, velger du varen og deretter **Rediger**-handlingen.
8. På siden **Lagerføringsenhetskort** merker du av for **Bruk kryssoverføring**.  

> [!NOTE]  
>  Kryssoverføring er mulig bare hvis du har definert lokasjonen til å kreve lagermottaksbehandling og plasseringsbehandling.  

## <a name="to-cross-dock-items-without-viewing-the-opportunities"></a>Slik kryssoverfører du varer uten å vise mulighetene  
1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagermottak**, og velg deretter den relaterte koblingen.  
2.  Opprett et lagermottak for en vare som er ankommet, og som kanskje kan kryssoverføres. Hvis du vil ha mer informasjon, kan du se [Motta varer](warehouse-how-receive-items.md).  
3.  Fyll ut feltet **Motta (antall)**, og velg deretter **Beregn kryssoverføring**-handlingen.  

    Utgående kildedokumenter som ber om varene som er planlagt å skulle forlate lageret innefor datoformelens tidsperiode, identifiseres.  [!INCLUDE[prod_short](includes/prod_short.md)] beregner antall slik at du kan kryssoverføre så mye som mulig og unngå å plassere varene, uten å samle opp for mange varer i kryssoverføringsområdet. Verdien i feltet **Ant. som skal kryssoverf** blir derved den minste av enten summen av alle de utgående linjene som ber om varen innenfor beregningstiden minus det antallet varer som allerede er plassert i kryssoverføringsområdet, eller verdien i feltet **Motta (antall)** på mottakslinjen. Du kan ikke kryssoverføre mer enn du har mottatt.  

4.  Hvis du vil kryssoverføre det antallet som blir foreslått, bokfører du mottaket. Du kan også bestemme deg for å endre antallet som skal kryssoverføres til en høyere eller lavere verdi, og deretter bokføre mottaket.  

    Antallene som skal kryssoverføres, blir nå vist som linjer i plasseringsinstruksjonen, forutsatt at feltet **Bruk plasseringsforslag** er tomt. Antallene som ikke er kryssoverført, blir til linjer i plasseringsinstruksjonen.  

    Hvis du har hyller, har de kryssoverførte varene blitt tilordnet til standard kryssoverføringshylle på lokasjonskortet.  

5.  Slett **Hent**- og **Plasser**-linjene for varer som ikke skal kryssoverføres i det hele tatt.  
6.  Skriv ut plasseringsinstruksjonen for de resterende linjene, og plasser de antallene av mottaket som skal lagres i de passende hyllene eller i det passende området av lageret. Plasser de kryssoverførte varene i området eller hyllen som er definert for dem av lagerets prinsipper. Enkelte ganger kan lagerets retningslinjer kreve at du lar dem ligge i mottaksområdet.  
7.  Velg **Registrer**-handlingen for å registrere de kryssoverførte varene som plassert og tilgjengelig for plukking.  

## <a name="to-cross-dock-items-after-viewing-the-opportunities"></a>Slik kryssoverfører du varer etter å ha vist mulighetene  
1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagermottak**, og velg deretter den relaterte koblingen.  
2.  Opprett et lagermottak for en vare som er ankommet, og som kanskje kan kryssoverføres. Hvis du vil ha mer informasjon, kan du se [Motta varer](warehouse-how-receive-items.md).  

    Du vil vise kildedokumentlinjer som ber om varen, før du bokfører mottaket.  
3.  Velg handlingen **Beregn kryssoverføring**.  

    På siden **Kryssoverføringsmuligheter** kan du se de viktigste opplysningene om linjene som ber om varen, for eksempel dokumenttype, forespurt antall og forfallsdatoen. Disse opplysningene kan hjelpe det med å bestemme hvor mye som skal kryssoverføres, hvor varene skal passeres i kryssoverføringsområdet, og hvordan de skal grupperes.  

4.  Velg handlingen **Autoutfyll antall for kryssoverføring** for å se hvordan antallene på mottakslinjene beregnes. Når du endrer antall varer i feltet **Ant. som skal kryssoverf.** på hver linje, oppdateres beregningen etter hvert som du gjør endringer. Dette betyr ikke at den bestemte leveringen eller produksjonen faktisk skal motta varene som er foreslått for kryssoverføring, fordi disse endringene bare blir gjort for testing. Prosessen kan imidlertid være informativ, hvis det blir brukt mer enn én enhet.  
5.  Hvis du vil reservere et antall av varen for en bestemt ordrelinje, plasserer du markøren på denne linjen og velger deretter handlingen **Reserver**. På siden **Reservasjon** kan du nå reservere eventuelt disponibelt antall av varen for denne bestemte ordren. Denne reservasjonen er som andre reservasjoner og har ikke høyere prioritet fordi den ble opprettet i forbindelse med kryssoverføring. Hvis du vil ha mer informasjon, kan du se [Reservere varer](inventory-how-to-reserve-items.md).   
6.  Når du er ferdig med å beregne på nytt eller med å reservere, velger du **OK**-knappen for å hente den beregningen du har revidert, inn i feltet **Ant. som skal kryssoverf.** på mottakslinjen, eller så velger du **Avbryt**-knappen hvis du vil gå tilbake til lagermottaket, der du eventuelt kan beregne kryssoverføringen på nytt.  
7.  Bokfør deretter mottaket, og du kan fortsette i plasseringsinstruksjonen slik det er beskrevet i trinn 3 til 7 i delen "Slik kryssoverfører varer uten å vise salgsmulighetene".  

> [!NOTE]  
>  I plasseringen kan du fortsette å endre antallene som blir plassert på lager eller kryssoverført, slik det er nødvendig. Du kan for eksempel bestemme deg for å kryssoverføre et ekstra antall for å få registreringen av kryssoverføringen til å gå raskere.  

## <a name="to-view-cross-docked-items-in-a-shipment-or-pick-worksheet"></a>Slik viser du kryssoverførte varer i en følgeseddel eller et plukkforslag  
Hvis du bruker hyller, kan du, hver gang du åpner en følgeseddel eller plukkforslaget, se en oppdatert beregning av antallet for hver vare i kryssoverføringshyllene. Dette er verdifull informasjon hvis du venter på at en vare skal komme inn. Når du ser at varen er tilgjengelig i kryssoverføringshyllen, kan du raskt opprette en plukking for alle varene i leveringen. I plukkforslaget kan du endre linjene slik det passer, og deretter opprette en plukking.  

Du må se etter varer i kryssoverføringsområdet før du plukker varer for levering. Hvis du under mottaksprosessen har merket deg hvilke kildedokumenter som var grunnlaget for kryssoverføringen, vil du ha en bedre forståelse av om varen finnes i kryssoverføringsområdet eller ikke.  

Når en produksjonsordre er frigitt, er linjene tilgjengelige i plukkforslaget, og du kan se i feltet **Ant. i kryssoverføringshylle** om de varene du venter på, er ankommet og plassert i kryssoverføringshyllene. Når du oppretter en plukkinstruksjon, foreslår programmet at du først plukker de kryssoverførte varene, og vil senere søke etter varen i lagringshyllene.  

Hvis du ikke bruker hyller, må du huske å kontrollere kryssoverføringsområdet jevnlig. Hvis ikke, må du stole på varsler fra mottak om at varene for produksjon er ankommet.  

## <a name="see-also"></a>Se også  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
