---
title: Planlegge ordre for ordre
description: Denne planleggingsoppgaven kan utføres på siden Ordreplanlegging, som viser alle nye behov sammen med tilgjengelighetsinformasjon og forslag til forsyning.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: 5a3481f1f1b1c08fd3006d1d62b92387414f0d41
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6444233"
---
# <a name="plan-for-new-demand-order-by-order"></a>Planlegge for nytt behov bestilling for bestilling
Denne planleggingsoppgaven kan utføres på siden **Ordreplanlegging**, som viser alle nye behov sammen med tilgjengelighetsinformasjon og forslag til forsyning. Vinduet inneholder visningen og verktøyene som kreves for å planlegge behov fra salgslinjer og komponentlinjer på en effektiv måte og deretter opprette forskjellige typer forsyningsordrer direkte.  

Du kan åpne **Ordreplanlegging**-siden på to måter, avhengig av fokus: fra en ordre du vil planlegge for spesielt, eller i satsvis modus fordi du vil planlegge for alle og eventuelle nye behov.  


## <a name="to-plan-for-new-production-order-demand"></a>Planlegge for et nytt produksjonsordrebehov  
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Planlagte produksjonsordrer** og velg den relaterte koblingen. (Du kan utføre disse trinnene for planlagte, fast planlagte eller frigitte produksjonsordrer).
2.  Åpne produksjonsordren du vil planlegge for, og velg **Planlegging**-handlingen.  
3.  På **Ordreplanlegging**-siden velger du handlingen **Beregn plan**.  

Siden viser planleggingslinjer i henhold til visningsfilteret **Produksjonsbehov**, som betyr komponentlinjer som ikke er oppfylt for alle eksisterende produksjonsordrer. De vises ikke behov for bare den ene produksjonsordren, fordi du må planlegge for én produksjonsordre med en oversikt over behov for eventuelle tidligere komponentlinjer. Planleggingslinjer for produksjonsordren i konteksten utvides.  

## <a name="to-plan-for-any-new-demand"></a>Slik planlegger du for et nytt behov  
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordreplanlegging**, og velg deretter den relaterte koblingen.  
2.  På **Ordreplanlegging**-siden velger du handlingen **Beregn plan**.
3.  Velg **Utvid (+)**-knappen foran datoen i **Behovsdato**-feltet for å se de underliggende planleggingslinjene som representerer behovslinjer med utilstrekkelig tilgjengelighet.  
4.  For hver utvidede planleggingslinje, det vil si behovslinje, kan du vise verdier i informasjonsfeltene nederst på siden.  

    |Alternativ|Description|  
    |----------------------------------|---------------------------------------|  
    |**Tilgjengelig for overføring**|Viser om varen finnes på en annen lokasjon. Du kan deretter finne og velge den.|  
    |**Erstatning finnes**|Viser om en erstatningsvare opprettes for varen. Du kan deretter finne og velge den. Merk at denne funksjonen bare gjelder for komponenter, det vil si fra behovslinjer av typen **Produksjon**.|  
    |**Tilgjengelig antall**|Viser total tilgjengelighet for varen, dvs. beregnet disponibel beholdning.|  
    |**Tidligste tilgjengelige dato**|Viser ankomstdatoen for en inngående forsyningsordre som kan dekke det nødvendige antallet på en dato senere enn behovsdatoen.|  

5.  I feltet **Etterfyllingssystem** velger du hvilken type forsyningsordre som skal opprettes.  

    Standardverdien er den som finnes på varekortet (eller LFE-kortet), men du kan endre den til ett av følgende tre alternativer:  

    |Alternativ|Beskrivelse|  
    |----------------------------------|---------------------------------------|  
    |**Kjøp**|Oppretter en bestilling.|  
    |**Overføring**|Oppretter en overføringsordre.|  
    |**Prod.ordre**|Oppretter en produksjonsordre.|  

    I **Forsyning fra**-feltet må du velge en verdi i henhold til det valgte etterfyllingssystemet.  

    > [!NOTE]  
    >  Hvis feltet ikke er fylt ut, vises det en feilmelding når du bruker funksjonen **Lag forsyningsordrer**, og det opprettes ingen forsyningsordre for den aktuelle planleggingslinjen. Dette er imidlertid ikke tilfelle hvis etterfyllingssystemet er **Prod.ordre**.  

6.  I **Forsyning fra**-feltet kan du slå opp i en aktuell liste og velge hvor forsyningen skal komme fra:  

    - Hvis etterfyllingssystemet er **Kjøp**, slår oppslagsknappen i dette feltet opp på siden **Vare/leverandør-katalog**.  
    - Hvis etterfyllingssystemet er **Overfør**, slår oppslagsknappen i dette feltet opp på siden **Lokasjonsoversikt**.  

    Hvis varen finnes i en annen lokasjon, viser feltet **Tilgjengelig for overføring** nederst en verdi, og du kan deretter finne og velge lokasjonen som varen skal hentes fra, når du lager overføringsordren.  

    Hvis det finnes en erstatning for den etterspurte varen, angis **Ja** i **Erstatning finnes**-feltet, og du kan deretter finne og velge erstatningen på siden **Vareerstatningsposter**.  

7.  Merk av for **Reserver** hvis du vil foreta en reservasjon mellom forsyningsordren du oppretter, og behovslinjen den opprettes for. Reservasjonen er som standard tom.  

    > [!NOTE]  
    >  Du kan bare merke av i dette feltet hvis varen har verdien **Valgfritt** eller **Alltid** i **Reserver**-feltet på varekortet.  

8.  I feltet **Antall for bestilling** kan du registrere antallet for forsyingsordren du oppretter.   
    Standardverdien er det samme antallet som antallet i **Nødvendig antall**-feltet. Du kan imidlertid bestille mer eller mindre enn dette antallet, avhengig av behov. Hvis du for eksempel ser på **Ordreplanlegging**-siden at flere behovslinjer uten forbindelse brukes for den samme kjøpte varen, og at de forfaller på omtrent samme dato, kan du konsolidere disse behovslinjene ved å registrere det totale nødvendige antallet i feltet **Antall for bestilling** for én linje og deretter slette de andre utdaterte planleggingslinjene for denne varen.  

9.  I feltene **Forfallsdato** og **Bestillingsdato** kan du registrere datoene som skal gjelde for de opprettede forsyningsordrene.  

    Disse to feltene er beslektede i henhold til feltet **Standard sikkerhetstid**, som du finner på siden **Produksjonsoppsett**. Som standard er forfallsdatoen den samme som behovsdatoen, men du kan endre disse etter eget behov.  

> [!NOTE]  
>  Hvis du angir en senere dato enn behovsdatoen, får du en advarsel.  

## <a name="to-make-supply-orders"></a>Slik lager du forsyningsordrer  
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Planlagte produksjonsordrer** og velg den relaterte koblingen. Du kan utføre disse trinnene for en planlagt, fast planlagt eller frigitt produksjonsordre.  
2.  Åpne produksjonsordren du vil planlegge for, og velg **Planlegging**-handlingen.  
3.  Plasser markøren på en aktuell planleggingslinje, og velg deretter handlingen **Lag bestillinger**.  
4.  Velg ett av følgende alternativer i feltet **Lag ordrer for** på hurtigfanen **Ordreplanlegging** på siden **Lag forsyningsordrer**.  

    |Alternativ|Beskrivelse|  
    |----------------------------------|---------------------------------------|  
    |**Den aktive linjen**|Lag en forsyningsordre bare for linjen der markøren er plassert.|  
    |**Den aktive ordren**|Lage forsyningsordrer for alle linjer i ordren der markøren er plassert.|  
    |**Alle linjene**|Lag forsyningsordrer for alle linjer på **Ordreplanlegging**-siden.|  

5.  På hurtigfanen **Alternativer** definerer du hvilken type forsyningsordrer eller bestillingsforslagslinjer som skal lages.  

    > [!NOTE]  
    >  Innstillingene du sist angav på siden **Lag forsyningsordrer**, lagres under bruker-IDen slik at de brukes neste gang du åpner siden.  

6.  Velg **OK**-knappen for å lage foreslåtte forsyningsordrene eller bestillingsforslagslinjene.  

Du har nå planlagt for behovet som ikke er oppfylt, ved å lage respektive forsyningsordrer. Detaljer om bestemte arbeidsflyter ved bruk av **Ordreplanlegging**-siden avhenger av selskapets interne policyer.  

Når du har fullført planleggingen på **Ordreplanlegging**-siden, for eksempel ved å definere en alternativ måte å forsyne antallet på, kan du fortsette med å opprette forsyningsordrer for en eller flere av planleggingslinjene.  

> [!NOTE]  
>  Forsyningsordrene du oppretter, kan introdusere et nytt avhengighetsbehov, for eksempel for underliggende produksjonsordrer, og du bør derfor velge **Beregn plan** igjen for å finne dem og løse dette før du går nedover i oversikten.  

## <a name="see-also"></a>Se også  
<!-- [Walkthrough: Planning Supplies Manually](walkthrough-planning-supplies-manually.md)   -->
[Planlegging](production-planning.md)  
[Definere produksjon](production-configure-production-processes.md)  
[Produksjon](production-manage-manufacturing.md)    
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)   
[Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging](setup-best-practices-supply-planning.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]