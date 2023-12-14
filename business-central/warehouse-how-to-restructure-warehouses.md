---
title: Omstrukturere lagre
description: Lær hvordan du omstrukturerer lageret med nye hyllekoder og nye egenskaper for hyllen for å oppnå eller vedlikeholde en mer effektiv operasjon.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '9813, 9814'
ms.date: 06/25/2021
ms.author: bholtorf
---
# <a name="restructure-warehouses"></a>Omstrukturere lagre
Du ønsker kanskje å omstrukturere lageret med nye hyllekoder og nye hylleegenskaper. Dette er en aktivitet du ikke utfører så ofte, men det kan oppstå situasjoner der det er nødvendig med en omklassifisering for å oppnå eller vedlikeholde en mer effektiv drift. Eksempel:  

- Du ønsker kanskje å bytte til hyllekoder som for eksempel støtter bruken av automatisk datafangst med håndholdte enheter.  
- Lageret kan ha anskaffet et nytt reolsystem som gir nye muligheter for lagringen.  
- Selskapet kan ha endret vareassortimentet og flyttet lageret til et nytt fysisk sted i forbindelse med denne endringen.  

Hvis lageret er definert slik at hyller brukes, men ikke lagerstyring, omstrukturerer du lageret ved å opprette de nye hyllene du vil bruke i fremtiden.  

## <a name="to-restructure-a-basic-warehouse-that-uses-bins-only"></a>Omstrukturere et enkelt lager som bare bruker hyller
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lokasjoner**, og velg deretter den relaterte koblingen.  
2.  På hurtigfanen **Lager** angir du feltet **Standard hyllevalg** til **Sist brukte hylle**.  
3.  Flytt alt innholdet fra de nåværende hyllene til de nye hyllene du nettopp opprettet.  

    1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varereklassifiseringskladd** og velg den relaterte koblingen.  
    2.  Velg en kladdelinje, og velg deretter **Hent hylleinnhold**-handlingen.  
    3.  På hurtigfanen **Hylleinnhold** definerer du filtre i feltene **Lokasjonskode**, **Hyllekode** og **Varenr.** for å angi innholdet du vil flytte.  
    4.  Velg **OK**-knappen for å fylle ut en kladdelinje.  
    5.  I feltet **Ny hyllekode** velger du hyllen som varene skal flyttes til.  
    6.  Gjenta trinn b til og med e for alt hylleinnhold som du vil flytte.  
    7.  Velg handlingen **Bokfør**.  

Du har nå tømt hyllene der varene pleide å være. Standardhyllene for varene er nå endret til de nye hyllene.  

## <a name="to-restructure-an-advanced-warehouse-that-uses-directed-put-away-and-pick"></a>Omstrukturere et avansert lager som bruker lagerstyring og plukking

1.  Opprett de nye hyllene du vil bruke i fremtiden. Hvis du vil ha mer informasjon, kan du se [Opprette hyller](warehouse-how-to-create-individual-bins.md).  
2.  Flytt alt innholdet fra de nåværende hyllene til de nye hyllene du nettopp opprettet.  

    1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerreklassifiseringskladd** og velg den relaterte koblingen.  
    2.  For hyller der det ikke var noen virkelig flytting av varer, oppretter du en linje for hver enkelt av de nåværende hyllene i **lageroverføringskladden** med den gamle hyllekoden, **Fra hylle-kode**, og den nye hyllekoden, **Til hylle-kode**.  
    3.  Hvis noen av flyttingene betyr faktiske flyttinger som du vil at de ansatte skal utføre, bruker du **flytteforslag** til å forberede flytteinstruksjoner i stedet for å bruke lagerreklassifiseringskladden. Hvis du vil ha mer informasjon, kan du se [Flytte varer i avanserte lageroppsett](warehouse-how-to-move-items-in-advanced-warehousing.md).  

3.  Når de gamle hyllene er tømt, reklassifiserer du dem som **KK**-hyller (kvalitetskontroll)for å sikre at de ikke tas med i vareflyter.  

    1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lokasjoner**, og velg deretter den relaterte koblingen.  
    2.  Velg linjen med lokasjonen og velg deretter **Hyller**-handlingen.  
    3.  Angi **KK** i feltet **Hylletypekode** på siden **Hyller** for hver av de gamle hyllene du tømte i trinn 3 i fremgangsmåten ovenfor.  

Du har nå fjernet hyllene fra lagerflyten, og du har reklassifisert dem som KK-hyller (kvalitetskontroll). For slike hyller er det ikke merket av i noen av aktivitetsfeltene på siden **Hylletyper**, og det tas derfor ikke hensyn til dem i vareflyten. Hvis du vil ha mer informasjon, kan du se [Definere hylletyper](warehouse-how-to-set-up-bin-types.md).  

## <a name="to-delete-a-bin"></a>Slik sletter du en hylle

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lokasjoner**, og velg deretter den relaterte koblingen.  
2.  Velg lokasjonen der du vil slette hyller. Velg handlingen **Hyller**.  
3.  Velg linjene for hyllene som du vil slette.  
4.  Velg handlingen **Slett**.  

Hvis du velger **Ja**, blir hyllen slettet og kan ikke brukes i fremtiden, men hyllekoden i alle lagerpostene forblir den samme.  

Hvis du ønsker å gi nytt navn til en hylle, slik at alle postene som er tilknyttet hyllen, også får nytt navn, inkludert hylleinnhold, lageraktivitetslinjer, registrerte lageraktivitetslinjer, lagerforslagslinjer, lagermottakslinjer, bokførte lagermottakslinjer, lagerfølgeseddellinjer, bokførte lagerfølgeseddellinjer og lagerposter, kan du gjøre det på siden **Hyller**.  

## <a name="to-rename-a-bin-and-change-the-bin-code-in-all-records"></a>Slik gir du nytt navn til en hylle og endrer hyllekoden i alle poster

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lokasjoner**, og velg deretter den relaterte koblingen.  
2.  Velg lokasjonen der du vil gi nytt navn til en hylle eller endre hyllekoden, og velg handlingen **Hyller**.  
3.  Velg hyllen som du vil endre og angi en ny hyllekode i **Kode**-feltet.  
4.  Velg **Ja**-knappen.  

> [!NOTE]  
>  Hvis du velger **Ja** og det finnes mange poster for denne hyllen, for eksempel fordi du ikke har slettet lagerdokumenter på en stund, kan det ta noe tid å gi postene nytt navn. Hvis du bruker denne metoden, bør du derfor vurdere å kjøre kjørselen **Slett registrerte lagerdokumenter** før du starter prosessen med å gi nytt navn. Merk deg også at de eneste dokumentene som blir slettet i denne kjørselen, er plasseringer, plukkinger og flyttinger.  
>   
>  Hvis du endrer navn på en mottakshylle eller en leveringshylle, endres navnet på alle de bokførte mottakene eller leveringene som henviser til den aktuelle hyllen.  

## <a name="see-also"></a>Se også
[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
