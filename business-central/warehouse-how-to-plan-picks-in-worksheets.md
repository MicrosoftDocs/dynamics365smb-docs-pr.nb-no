---
title: Planlegge plukkinger i forslaget
description: Finn ut hvordan du kan gjøre linjer på forsendelsesdokumenter tilgjengelige på plukkforslag for lagermedarbeidere.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/13/2021
ms.author: edupont
ms.openlocfilehash: 24e19eb56bf28b7871ec18f254dc5dbbaa0b290a
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9078339"
---
# <a name="plan-picks-in-worksheets"></a>Planlegge plukkinger i forslaget

Hvis lageret er definert til å kreve både plukk- og leveringsbehandling, kan du velge å lage linjer på forsendelsesdokumenter som er tilgjengelig i plukkforslag i stedet for plukkinstruksjoner.  

> [!NOTE]  
> Hvis det allerede er opprettet plukkinstruksjoner, og du vil slå dem sammen til én plukkinstruksjon, må du slette de individuelle plukkingene. Linjene som skal plukkes, kan nå vises på et plukkforslag.  

På siden **Plukkforslag** kan du opprette plukklister som hjelper ansatte med å samle varer i lageret. Siden viser antall som er tilgjengelig i kryssoverføringshyller, som er nyttig når du skal planlegge arbeidsoppgaver i situasjoner for kryssoverføring. [!INCLUDE[prod_short](includes/prod_short.md)] foreslår alltid en plukking fra en kryssoverføringshylle først. Linjene i forslaget kan komme fra flere kildedokumenter. De kan for eksempel komme fra mer enn en ordre. 

> [!NOTE]  
> Plukking av varer som er montert til en ordre som leveres følger samme fremgangsmåte som for vanlig lagerplukking for levering. Antall plukklinjer per antall som skal leveres, kan imidlertid være mange til én fordi du plukker komponentene, ikke monteringsvaren.  
>
> Lagerplukklinjene opprettes for verdien i **Restantall**-feltet på linjene i monteringsordren som er knyttet til ordrelinjen som skal leveres. Dette sikrer at alle komponentene er plukket i én handling. Hvis du vil ha mer informasjon, kan du se [Selg av lagervarer i montere-til-ordre-flyter](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  
>
> Hvis du vil ha informasjon om plukking av komponenter for monteringsordrer generelt, inkludert situasjoner der monteringsvaren ikke forfaller på en følgeseddel, kan du se [Plukke for montering eller produksjon i avanserte lageroppsett](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).  

## <a name="sorting-lines-on-a-pick-worksheet"></a>Sortering av linjer i et plukkforslag

Du kan sortere linjer etter vare, hyllenummer, kildedokument, forfallsdato eller mål. Her kommer det noen eksempler på hvor nyttig sortering kan være.

* Hvis du sorterer etter forfallsdato, kan du velge å slette alle linjer unntatt de som trenger umiddelbar oppmerksomhet. Linjer som ikke haster så mye, blir ikke virkelig slettet, men bare sendt tilbake til **Plukkutvalg**-forslaget. Når du oppretter plukkingen, er linjene allerede sortert etter forfallsdato, og du kan velge å tilordne plukkingen til en ansatt.
* Hvis hyllene er nummerert slik at de samsvarer med lageret, kan du sortere linjene etter hyllekode for å gjøre det enklere å plukke for flere leveringer samtidig. 
* Hvis du bruker hylleprioriteringen, kan sortering med rangering spare litt tid. 
* Du kan sortere etter mål, slik at du kan samle og levere ordrer per kunde.

## <a name="to-plan-picks-in-the-worksheet"></a>Slik planlegger du plukkinger i forslaget

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Plukkforslag**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Hent lagerdokumenter**.  
3. Velg de følgesedlene du vil forberede plukking for. Du kan sortere linjene, men sorteringen brukes ikke på plukkinstruksjonen. Du kan også slette noen av linjene for å få en mer effektiv plukking. Hvis det for eksempel finnes flere linjer med varer som er i kryssoverføringshyller, er det mulig at du vil opprette en plukking for alle linjene. De kryssoverførte varene vil bli levert (sammen med andre varer på følgesedlene), og kryssoverføringshyllene vil ha plass til flere inngående varer.  
4. Velg handlingen **Opprett plukk**, og fyll ut siden **Opprett plukk**. Den sorteringen du ber om her, vil sortere de plukklinjene du oppretter. Du kan for eksempel opprette en plukking for hver sone, og sortere linjene etter hylleprioritering innenfor hver plukking.  
5. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerplukk** og velg den relaterte koblingen. **Lagerplukk**-vinduet åpnes.  
6. Du kan nå finne plukktilordningen ved å velge plukkingen med det høyeste nummeret.  
7. Du kan om nødvendig tilordne en annen bruker eller sortere linjene annerledes.  
8. Velg handlingen **Skriv ut** hvis du vil skrive ut plukkinstruksjonene.  
9. Når du har fullført plukkingen, velger du handlingen **Registrer**.  

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/pick-ship-items-warehouse/)

## <a name="see-also"></a>Se også

[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)  
[Monteringsstyring](assembly-assemble-items.md)  
[Designdetaljer: Warehouse Management](design-details-warehouse-management.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]