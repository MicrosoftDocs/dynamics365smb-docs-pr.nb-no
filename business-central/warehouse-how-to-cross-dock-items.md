---
title: Kryssoverføringsvarer
description: Lær hvordan du mottar og sender varer uten å plassere dem på lager.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 10/09/2023
ms.custom: bap-template
ms.search.form: '15, 5703, 7302, 7332, 5768'
---
# Kryssoverføringsvarer

Kryssoverføringsvarer er varer du mottar og leverer uten å plassere dem. Plasserings- og plukkprosessene krever begrenset behandling av varer. Du kan kryssoverføre varer for leveringer og produksjonsordrer.

## Kryssoverføringshyller og -soner

Hvis du bruker hyller, oppretter du minst én kryssoverføringshylle, og deretter angir du hyllen i feltet **Hyllekode for kryssoverføring** på lokasjonene. Hvis du bruker lagerstyring, setter du opp en kryssoverføringssone.

Når du forbereder en levering eller plukker varer for produksjon og bruker hyller, plukkes varen automatisk fra en kryssoverføringshylle før noen annen hylle. Du må se i kryssoverføringsområdet for å finne ut om de varene du trenger, er tilgjengelig der før du henter varene fra det vanlige lagringsområdet.  

Hvis du har beregnet kryssoverføringsantall, opprettes plasseringslinjer til kryssoverføringshyllen for kryssoverføringsberegning når du bokfører mottaket. Andre plasseringslinjer blir opprettet som vanlig.  

## Kryssoverføring velg linjer for et mottak

Hvis du vil bokføre de kryssoverførte varene med en gang slik at de blir tilgjengelig for plukking, må du også registrere en plassering for de andre varene som kom fra mottakslinjen, nemlig de som må lagres. Hvis bare noen av varene på en mottakslinje blir kryssoverført, må du derfor sørge for å plassere resten av varene så snart som mulig. Lageret kan også ha regler som sier at kryssoverføring av hele mottakslinjer skal utføres så sant det er mulig.

I plasseringsinstruksjonen sletter du Hent og plasser-instruksjonslinjene for hver mottakslinje for varene som skal plasseres. Du kan gjenopprette instruksjonslinjene senere som plasseringslinjer fra plasseringsforslaget eller det bokførte mottaket. Når du har slettet instruksjonslinjene, kan du plassere og registrere linjene for kryssoverførte varer.  

## Om siden Plasseringsforslag

Hvis du slo på **Bruk plasseringsforslag** på siden **Lokasjonskort** og bokførte mottaket med beregnede kryssoverføringer, blir alle mottakslinjene tilgjengelig i forslaget. Informasjonen om kryssoverføringen går tapt, og den kan ikke gjenopprettes. Hvis du vil å bruke kryssoverføringsfunksjonaliteten, bør du overføre linjer til plasseringsforslaget ved å slette plasseringsinstruksjoner i stedet for å bruke den automatiske overføringsfunksjonen i feltet **Bruk plasseringsforslag**.  

Hvis du bokfører lagermottaket og vekslebryteren **Bruk plasseringsforslag** er slått av, blir kryssoverføringsvarene separate linjer i plasseringsinstruksen. Feltet **Kryssoverføringsinformasjon** på hver plasseringslinje viser om linjen inneholder følgende:

* Kryssoverføringsvarer.
* Alle varene fra et mottak må lagres.
* Noen varer fra et mottak må lagres, og noen skal kryssoverføres.

[!INCLUDE [prod_short](includes/prod_short.md)] beholder ikke separate poster for kryssoverførte varer. Det registrerer dem som vanlige plasseringsinstrukser.  

## Slik definerer du lageret for kryssoverføring  

1. Hvis du bruker hyller, må du sette opp minst én kryssoverføringshylle. Hvis du bruker lagerstyring, setter du opp en kryssoverføringssone.  

    Det er merket av for **Kryssoverføringshylle** for en kryssoverføringshylle, og både hylletypen **Motta** og **Plukke** må være valgt. Hvis du vil lære mer om hyller, går du til [Opprett hyller](warehouse-how-to-create-individual-bins.md) og [Definer hylletyper](warehouse-how-to-set-up-bin-types.md).  

    Hvis du bruker soner, oppretter du en sone for kryssoverføringshyllene og velger feltet **Kryssoverføringshyllesone**. Hvis du vil ha mer informasjon om soner, går du til [Definer lokasjoner for å bruke hyller](warehouse-how-to-set-up-locations-to-use-bins.md).  

2. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Lokasjon**, og velg deretter den relaterte koblingen.  
3. Velg lokasjonen der du vil definere lageret for kryssoverføring, på siden **Lokasjon**, og velg deretter **Rediger**-handlingen.  
4. På hurtigfanen **Lager**, slår du på vekselbryteren **Bruk kryssoverføring** og fyller ut feltet **Kryssoverføring forfallsdatoberegn.** med tidspunktet for å søke etter kryssoverføringsmuligheter.

    Alternativet **Bruk kryssoverføring** er bare tilgjengelig hvis feltene **Mottak nødv.**, **Levering nødv.**, **Plukk nødv.** og **Plassering nødv.** er valgt.  

5. Hvis du bruker hyller, fyller du ut feltet **Hyllekode for kryssoverføring** på hurtigfanen **Hyller** med koden for hyllen du vil bruke som standard kryssoverføringshylle.  
6. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Lagerføringsenhet**, og velg deretter den relaterte koblingen.  
7. For hver vare eller lagerføringsenhet du ønsker å kunne kryssoverføre, velger du varen og deretter **Rediger**-handlingen.
8. På siden **Lagerføringsenhetskort** merker du av for **Bruk kryssoverføring**.  

> [!NOTE]  
>  Kryssoverføring er mulig bare hvis du har definert lokasjonen til å kreve lagermottaksbehandling og plasseringsbehandling.  

## Slik kryssoverfører du varer uten å vise mulighetene  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagermottak** og velg den relaterte koblingen.  
2. Opprett et lagermottak for en vare som er ankommet, og som kan kryssoverføres. Hvis du vil finne ut mer om mottak, går du til [Motta varer](warehouse-how-receive-items.md).  
3. Fyll ut feltet **Motta (antall)**, og velg deretter **Beregn kryssoverføring**-handlingen.  

    Utgående kildedokumenter som ber om varene som er planlagt å skulle forlate lageret innefor datoformelens tidsperiode, identifiseres. [!INCLUDE[prod_short](includes/prod_short.md)] beregner antall slik at du kan kryssoverføre så mye som mulig og unngå å plassere varene, uten å samle opp for mange varer i kryssoverføringsområdet. Verdien i feltet **Ant. som skal kryssoverf** blir den minste av enten summen av alle de utgående linjene for varen innenfor beregningstiden minus det antallet som allerede er plassert i kryssoverføringsområdet, eller verdien i feltet **Motta (antall)** på mottakslinjen. Du kan ikke kryssoverføre mer enn du har mottatt.  

4. Hvis du vil kryssoverføre det antallet som blir foreslått, bokfører du mottaket. Du kan også bestemme deg for å endre antallet som skal kryssoverføres til en høyere eller lavere verdi, og deretter bokføre mottaket.  

    Antallene som skal kryssoverføres, blir nå vist som linjer i plasseringsinstruksjonen, forutsatt at feltet **Bruk plasseringsforslag** er tomt. Antallene som ikke er kryssoverført, blir til linjer i plasseringsinstruksjonen.  

    Hvis du har hyller, har de kryssoverførte varene blitt tilordnet til standard kryssoverføringshylle på lokasjonskortet.  

5. Slett **Hent**- og **Plasser**-linjene for varer som du ikke kryssoverfører.  
6. Skriv ut plasseringsinstruksjonen for de resterende linjene, og plasser de antallene av mottaket som skal lagres i de passende hyllene eller i det passende området av lageret. Plasser de kryssoverførte varene i området eller hyllen som er definert for dem av lagerets prinsipper. Enkelte ganger kan lagerets retningslinjer kreve at du lar dem ligge i mottaksområdet.  
7. Velg **Registrer**-handlingen for å registrere de kryssoverførte varene som plassert og tilgjengelig for plukking.  

## Slik kryssoverfører du varer etter å ha vist mulighetene  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagermottak** og velg den relaterte koblingen.  
2. Opprett et lagermottak for en vare som er ankommet, og som kan kryssoverføres.  

    Du vil vise kildedokumentlinjer som ber om varen, før du bokfører mottaket.  
3. Velg handlingen **Beregn kryssoverføring**.  

   På siden **Kryssoverføringsmuligheter** kan du se de viktigste opplysningene om linjene som ber om varen, for eksempel dokumenttype, forespurt antall og forfallsdatoen. Disse opplysningene kan hjelpe det med å bestemme hvor mye som skal kryssoverføres, hvor varene skal passeres i kryssoverføringsområdet, og hvordan de skal grupperes.  

4. Velg handlingen **Autoutfyll antall for kryssoverføring** for å vise hvordan antallene på mottakslinjene beregnes. Når du endrer antall varer i feltet **Ant. som skal kryssoverf.** på hver linje, oppdateres beregningen. Oppdateringen betyr ikke at leveringen eller produksjonsordren faktisk vil motta varene som blir foreslått for kryssoverføring. Det er bare for testformål. Prosessen kan imidlertid være informativ, hvis det blir brukt mer enn én enhet.  
5. Hvis du vil reservere et antall av varen for en ordrelinje, velger du linjen og velger deretter handlingen **Reserver**. Reserver tilgjengelig antall av varen på **Reservasjon**-siden. Reservasjonen er som andre reservasjoner og har ikke høyere prioritet fordi den ble opprettet i forbindelse med kryssoverføring. Hvis du vil finne ut mer om reserverasjoner, går du til [Reserver varer](inventory-how-to-reserve-items.md).   
6. Når du er ferdig med å beregne på nytt eller med å reservere, velger du **OK**-knappen for å hente den beregningen til feltet **Ant. som skal kryssoverf.** på mottakslinjen, eller så velger du **Avbryt**-knappen hvis du vil gå tilbake til lagermottaket og beregne kryssoverføringen på nytt.  
7. Bokfør mottaket. Du kan fortsette i plasseringsinstruksjonen slik det er beskrevet i trinn 3 til 7 i [Slik kryssoverfører varer uten å vise salgsmulighetene](#to-cross-dock-items-without-viewing-the-opportunities).  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

    > [!NOTE]  
    > I plasseringen kan du fortsette å endre antallene som blir plassert på lager eller kryssoverført, slik det er nødvendig. Du kan for eksempel bestemme deg for å kryssoverføre et ekstra antall for å få registreringen av kryssoverføringen til å gå raskere.  

## Slik viser du kryssoverførte varer i en følgeseddel eller et plukkforslag  

Hvis du bruker hyller, når du åpner en følgeseddel eller plukkforslaget, oppdateres hver vare i kryssoverføringshyllene. Når varen er tilgjengelig i kryssoverføringshyllen, kan du opprette en plukking for varene i leveringen. I plukkforslaget kan du redigere linjene etter behov.  

Når en produksjonsordre er frigitt, er linjene tilgjengelig i plukkforslaget, og feltet **Ant. i kryssoverføringshylle** viser om de varene er ankommet og er i kryssoverføringshyllene. Når du oppretter en plukkinstruks, foreslår [!INCLUDE [prod_short](includes/prod_short.md)] at du plukker de kryssoverførte varene først. Varer i lagerhyller foreslås etterpå.  

Hvis du ikke bruker hyller, må du huske å kontrollere kryssoverføringsområdet jevnlig. Hvis ikke, må du stole på varsler fra mottak om at varene for produksjon er ankommet.  

## Se også  

[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]