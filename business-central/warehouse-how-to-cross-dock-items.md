---
title: Kryssoverføringsvarer
description: Kryssoverføringsfunksjonalitet er tilgjengelig hvis du har definert lokasjonen slik at den krever lagermottaksbehandling og plasseringsbehandling.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '15, 5703, 7302, 7332, 5768'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="cross-dock-items"></a><a name="cross-dock-items"></a>Kryssoverføringsvarer

Kryssoverføringsvarer er varer du mottar og leverer uten å plassere dem. Plasserings- og plukkprosessene krever begrenset behandling av varer. Du kan kryssoverføre varer for leveringer og produksjonsordrer.

## <a name="cross-dock-bins-and-zones"></a><a name="cross-dock-bins-and-zones"></a>Kryssoverføringshyller og -soner

Hvis du bruker hyller, oppretter du minst én kryssoverføringshylle, og deretter angir du hyllen i feltet **Hyllekode for kryssoverføring** på lokasjonene. Hvis du bruker lagerstyring, setter du opp en kryssoverføringssone.

Når du forbereder en levering eller plukker varer for produksjon og bruker hyller, plukkes varen automatisk fra en kryssoverføringshylle før noen annen hylle. Du må se i kryssoverføringsområdet for å finne ut om de varene du trenger, er tilgjengelig der før du henter varene fra det vanlige lagringsområdet.  

Hvis du har beregnet kryssoverføringsantall, opprettes plasseringslinjer til kryssoverføringshyllen for kryssoverføringsberegning når du bokfører mottaket. Andre plasseringslinjer blir opprettet som vanlig.  

## <a name="cross-dock-select-lines-for-a-receipt"></a><a name="cross-dock-select-lines-for-a-receipt"></a>Kryssoverføring velg linjer for et mottak

<!--If a receipt contains items that you want to store, that is, items that you are not cross-docking, you must register a put-away for those items.-->

Hvis du vil bokføre de kryssoverførte varene med en gang slik at de blir tilgjengelig for plukking, må du også registrere en plassering for de andre varene som kom fra mottakslinjen, nemlig de som må lagres. Hvis bare noen av varene på en mottakslinje blir kryssoverført, må du derfor sørge for å plassere resten av varene så snart som mulig. Lageret kan også ha regler som sier at kryssoverføring av hele mottakslinjer skal utføres så sant det er mulig.

I plasseringsinstruksjonen sletter du Hent og plasser-instruksjonslinjene for hver mottakslinje for varene som skal plasseres. Du kan gjenopprette instruksjonslinjene senere som plasseringslinjer fra plasseringsforslaget eller det bokførte mottaket. Når du har slettet instruksjonslinjene, kan du plassere og registrere linjene for kryssoverførte varer.  

## <a name="about-the-put-away-worksheet-page"></a><a name="about-the-put-away-worksheet-page"></a>Om plasseringsforslaget

Hvis du slo på **Bruk plasseringsforslag** på siden Lokasjonskort og har bokført mottaket med beregnede kryssoverføringer, blir alle mottakslinjene tilgjengelig i forslaget. Informasjonen om kryssoverføringen går tapt, og den kan ikke gjenopprettes. Hvis du vil å bruke kryssoverføringsfunksjonaliteten, bør du overføre linjer til plasseringsforslaget ved å slette plasseringsinstruksjoner i stedet for å bruke den automatiske overføringsfunksjonen i feltet **Bruk plasseringsforslag**.  

Hvis du bokfører lagermottaket og vekslebryteren **Bruk plasseringsforslag** er slått av, blir kryssoverføringsvarene separate linjer i plasseringsinstruksen. Feltet **Kryssoverføringsinformasjon** på hver plasseringslinje viser om linjen inneholder følgende:

* Kryssoverføringsvarer.
* Alle varene fra et mottak må lagres.
* Noen varer fra et mottak må lagres, og noen skal kryssoverføres.

De ansatte kan enkelt forstå hvorfor hele antallet ikke er plassert i lageret.  

[!INCLUDE [prod_short](includes/prod_short.md)] har ikke separate poster for kryssoverførte varer, men det registrerer dem som vanlige plasseringsinstruksjoner.  

## <a name="to-set-up-the-warehouse-for-cross-docking"></a><a name="to-set-up-the-warehouse-for-cross-docking"></a>Slik definerer du lageret for kryssoverføring

1. Hvis du bruker hyller, må du sette opp minst én kryssoverføringshylle. Hvis du bruker lagerstyring, setter du opp en kryssoverføringssone.  

    Det er merket av for **Kryssoverføringshylle** for en kryssoverføringshylle, og både hylletypen **Motta** og **Plukke** må være valgt. Hvis du vil ha mer informasjon, kan du se [Opprette hyller](warehouse-how-to-create-individual-bins.md) og [Definere hylletyper](warehouse-how-to-set-up-bin-types.md).  

    Hvis du bruker soner, oppretter du en sone for kryssoverføringshyllene og velger feltet **Kryssoverføringshyllesone**. Hvis du vil ha mer informasjon, kan du se [Definere lokasjoner slik at de bruker hyller](warehouse-how-to-set-up-locations-to-use-bins.md).  

2. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Lokasjon**, og velg deretter den relaterte koblingen.  
3. Velg lokasjonen der du vil definere lageret for kryssoverføring, på siden **Lokasjon**, og velg deretter **Rediger**-handlingen.  
4. På hurtigfanen **Lager**, slår du på vekselbryteren **Bruk kryssoverføring** og fyller ut feltet **Kryssoverføring forfallsdatoberegn.** med tidspunktet for å søke etter kryssoverføringsmuligheter.

    Alternativet **Bruk kryssoverføring** er bare tilgjengelig hvis feltene **Mottak nødv.**, **Levering nødv.**, **Plukk nødv.** og **Plassering nødv.** er valgt.  

5.  Hvis du bruker hyller, fyller du ut feltet **Hyllekode for kryssoverføring** på hurtigfanen **Hyller** med koden for hyllen du vil bruke som standard kryssoverføringshylle.  
6.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Lagerføringsenhet**, og velg deretter den relaterte koblingen.  
7.  For hver vare eller lagerføringsenhet du ønsker å kunne kryssoverføre, velger du varen og deretter **Rediger**-handlingen.
8. På siden **Lagerføringsenhetskort** merker du av for **Bruk kryssoverføring**.  

> [!NOTE]  
>  Kryssoverføring er mulig bare hvis du har definert lokasjonen til å kreve lagermottaksbehandling og plasseringsbehandling.  

## <a name="to-cross-dock-items-without-viewing-the-opportunities"></a><a name="to-cross-dock-items-without-viewing-the-opportunities"></a>Slik kryssoverfører du varer uten å vise mulighetene
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagermottak** og velg den relaterte koblingen.  
2.  Opprett et lagermottak for en vare som er ankommet, og som kanskje kan kryssoverføres. Hvis du vil ha mer informasjon, kan du se [Motta varer](warehouse-how-receive-items.md).  
3.  Fyll ut feltet **Motta (antall)**, og velg deretter **Beregn kryssoverføring**-handlingen.  

    Utgående kildedokumenter som ber om varene som er planlagt å skulle forlate lageret innefor datoformelens tidsperiode, identifiseres.  [!INCLUDE[prod_short](includes/prod_short.md)] beregner antall slik at du kan kryssoverføre så mye som mulig og unngå å plassere varene, uten å samle opp for mange varer i kryssoverføringsområdet. Verdien i feltet **Ant. som skal kryssoverf** blir derved den minste av enten summen av alle de utgående linjene som ber om varen innenfor beregningstiden minus det antallet varer som allerede er plassert i kryssoverføringsområdet, eller verdien i feltet **Motta (antall)** på mottakslinjen. Du kan ikke kryssoverføre mer enn du har mottatt.  

4.  Hvis du vil kryssoverføre det antallet som blir foreslått, bokfører du mottaket. Du kan også bestemme deg for å endre antallet som skal kryssoverføres til en høyere eller lavere verdi, og deretter bokføre mottaket.  

    Antallene som skal kryssoverføres, blir nå vist som linjer i plasseringsinstruksjonen, forutsatt at feltet **Bruk plasseringsforslag** er tomt. Antallene som ikke er kryssoverført, blir til linjer i plasseringsinstruksjonen.  

    Hvis du har hyller, har de kryssoverførte varene blitt tilordnet til standard kryssoverføringshylle på lokasjonskortet.  

5.  Slett **Hent**- og **Plasser**-linjene for varer som ikke skal kryssoverføres i det hele tatt.  
6.  Skriv ut plasseringsinstruksjonen for de resterende linjene, og plasser de antallene av mottaket som skal lagres i de passende hyllene eller i det passende området av lageret. Plasser de kryssoverførte varene i området eller hyllen som er definert for dem av lagerets prinsipper. Enkelte ganger kan lagerets retningslinjer kreve at du lar dem ligge i mottaksområdet.  
7.  Velg **Registrer**-handlingen for å registrere de kryssoverførte varene som plassert og tilgjengelig for plukking.  

## <a name="to-cross-dock-items-after-viewing-the-opportunities"></a><a name="to-cross-dock-items-after-viewing-the-opportunities"></a>Slik kryssoverfører du varer etter å ha vist mulighetene
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagermottak** og velg den relaterte koblingen.  
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

## <a name="to-view-cross-docked-items-in-a-shipment-or-pick-worksheet"></a><a name="to-view-cross-docked-items-in-a-shipment-or-pick-worksheet"></a>Slik viser du kryssoverførte varer i en følgeseddel eller et plukkforslag
Hvis du bruker hyller, kan du, hver gang du åpner en følgeseddel eller plukkforslaget, se en oppdatert beregning av antallet for hver vare i kryssoverføringshyllene. Dette er verdifull informasjon hvis du venter på at en vare skal komme inn. Når du ser at varen er tilgjengelig i kryssoverføringshyllen, kan du raskt opprette en plukking for alle varene i leveringen. I plukkforslaget kan du endre linjene slik det passer, og deretter opprette en plukking.  

Du må se etter varer i kryssoverføringsområdet før du plukker varer for levering. Hvis du under mottaksprosessen har merket deg hvilke kildedokumenter som var grunnlaget for kryssoverføringen, vil du ha en bedre forståelse av om varen finnes i kryssoverføringsområdet eller ikke.  

Når en produksjonsordre er frigitt, er linjene tilgjengelige i plukkforslaget, og du kan se i feltet **Ant. i kryssoverføringshylle** om de varene du venter på, er ankommet og plassert i kryssoverføringshyllene. Når du oppretter en plukkinstruksjon, foreslår programmet at du først plukker de kryssoverførte varene, og vil senere søke etter varen i lagringshyllene.  

Hvis du ikke bruker hyller, må du huske å kontrollere kryssoverføringsområdet jevnlig. Hvis ikke, må du stole på varsler fra mottak om at varene for produksjon er ankommet.  

## <a name="see-also"></a><a name="see-also"></a>Se også
[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
