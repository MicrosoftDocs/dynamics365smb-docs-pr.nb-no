---
title: Planlegge plasseringer i forslaget | Microsoft-dokumentasjon
description: Hvis lokasjonen krever både plasserings- og mottaksbehandling og du vil planlegge plasseringsinstruksjoner for et antall mottak i stedet for at de ansatte skal følge instruksjonene som programmet oppretter for hvert enkelt bokførte mottak, kan du bruke plasseringsforslaget.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1cf1a782a0c36e3f87935c8b2b965deb4ad04e9a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383654"
---
# <a name="plan-put-aways-in-worksheets"></a>Planlegge plasseringer i forslag
Hvis lokasjonen krever både plasserings- og mottaksbehandling og du vil planlegge plasseringsinstruksjoner for et antall mottak i stedet for at de ansatte skal følge instruksjonene som programmet oppretter for hvert enkelt bokførte mottak, kan du bruke plasseringsforslaget.  

Hvis du vil sette opp lageret slik at mottakslinjer blir tilgjengelig i plasseringsforslaget så snart de er bokført, merker du av for **Bruk plasseringsforslag** på hurtigfanen **Lager** på lokasjonskortet for lageret. Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).  

Hvis du ikke velger dette feltet, vil programmet automatisk opprette plasseringsinstruksjoner for mottak etter hvert som de blir bokført.  

> [!NOTE]  
>  Uansett hvilken status feltet **Bruk plasseringsforslag** på lokasjonskortet har, kan du alltid få plasseringsforslagslinjer, det vil si bokførte mottakslinjer, til plasseringsforslaget ved å gjøre følgende:  
>   
>  1.  På siden **Plassering** trykker du CTRL+D for å slette hele plasseringsinstruksjonen, eller du velger linjene som du vil behandle i forslaget, og sletter dem.  
> 2.  Fortsett med prosessen i så mange plasseringer som du ønsker, til du har slettet de linjene du vil arbeide med i forslaget. Velg deretter på **Plasseringsforslag** og fortsett med planleggingen.  

## <a name="to-plan-instructions-in-the-put-away-worksheet"></a>Slik planlegger du instruksjoner i plasseringsforslaget  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Plasseringsforslag**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Hent lagerdokumenter**. **Plasseringsutvalg**-siden åpnes.  

    Du ser alle de bokførte mottakene og registrerte plasseringene som er videresendt til plasseringsfunksjonen, inkludert de som det allerede er opprettet plasseringsinstruksjoner for. Dokumenter med plasseringslinjer som er fullstendig plassert og registrert, blir ikke vist i denne oversikten.  

3. Velg dokumentene du vil arbeide med i forslaget. Du kan arbeide med linjer fra flere dokumenter samtidig.  

    > [!NOTE]  
    >  Hvis du prøver å velge et mottaksdokument eller internplasseringsdokument der du allerede har opprettet instruksjoner for alle linjene, informerer programmet deg om at det ikke er noe å håndtere.  

4. Fyll ut feltet **Sorteringsmetode** for å sortere linjene på den måten du foretrekker.  

    > [!NOTE]  
    >  Måten linjene er sortert på i forslaget, overføres ikke automatisk til plasseringsinstruksjonen, men de samme sorteringsmulighetene finnes sammen med hyllerangering. Linjerekkefølgen du planlegger i forslaget, blir dermed enkelt gjenopprettet når du oppretter plasseringsinstruksjonene eller når du sorterer i plasseringsinstruksjonene.  

5.  Fyll ut feltet **Ant. som skal håndt.**. Velg handlingen **Autoutfyll ant. som skal hndt.**, eller fyll ut feltene manuelt.  
6.  Hvis det er nødvendig, redigerer du linjene manuelt. Du kan slette linjer, for eksempel hvis noen varer må plasseres i en hylle som er langt borte fra hyllene for de andre varene.  

    > [!NOTE]  
    >  Linjer som slettes, blir bare slettet fra dette forslaget, ikke fra plasseringsutvalgsoversikten.  

7.  Velg handlingen **Opprett plassering**. Siden **Opprett dokument** åpnes. Her kan du tilføye mer informasjon for den plasseringen du oppretter, på følgende måte:  

    -   Du kan tilordne plasseringen til en bestemt ansatt.  
    -   Du kan sortere plasseringsinstruksjonslinjene på samme måte som i forslaget eller etter hylleprioritering. Når du sorterer etter hylleprioritering, vises Hent-linjen først, fordi de fleste mottak har hylleprioriteringen 0, og Plasser-linjen vises sist. Den begynner med hyllene med lavest hyllerangering. Hvis du har strukturert lageret slik at hyller med lignende hylleprioritering er side ved side, blir jobben enklere for de lageransatte ved at de slipper å utføre enkelte trinn.  
    -   Du kan velge ikke å se de mellomliggende linjene som blir opprettet når programmet konverterer en større enhet til mindre enheter, ved å merke av i **Angi anbrekksfilter**-feltet. For mer informasjon, se [Aktivere automatisk samlet oppbryting med lagerstyring og plukk](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md)  
    -   Du kan velge at feltet **Ant. som skal håndt.** ikke fylles automatisk ut i plasseringsinstruksjonene.  
    -   Du kan velge å skrive ut dokumentet umiddelbart.  

8.  Velg **OK**-knappen. Programmet oppretter plasseringen i henhold til dine anmodninger.  

## <a name="see-also"></a>Se også  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]