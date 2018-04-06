---
title: Planlegge plukkinger i forslaget | Microsoft-dokumentasjon
description: "Hvis lageret er definert til å kreve både plukkbehandling og lagerleveringsbehandling, kan lageret velge å fungere slik at linjene på leveringsdokumentene ikke automatisk blir omgjort til plukkinstrukser, men at de i stedet blir gjort tilgjengelig for plukkforslaget."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: c46e446c4af97e9699b1e454ff0d63173322f81e
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="plan-picks-in-worksheets"></a>Planlegge plukkinger i forslaget
Hvis lageret er definert til å kreve både plukkbehandling og lagerleveringsbehandling, kan lageret velge å fungere slik at linjene på leveringsdokumentene ikke automatisk blir omgjort til plukkinstrukser, men at de i stedet blir gjort tilgjengelig for plukkforslaget.  

> [!NOTE]  
>  Hvis det allerede er opprettet plukkinstruksjoner, og du vil slå dem sammen til én effektiv plukkinstruksjon, må du slette de individuelle plukkingene. Linjene som skal plukkes, kan nå vises i forslaget.  

I plukkforslaget kan du definere plukklister for ansatte som begrenser tiden de ansatte trenger til å flytte seg rundt for å plukke varene i lageret. Det finnes felt som inneholder opplysninger om antall varer som er tilgjengelige i kryssoverføringshyllene. Dette er nyttig i direkteoverføringssituasjoner for å planlegge arbeidsoppgavene, fordi programmet alltid vil foreslå en plukking fra en kryssoverføringshylle før noen annen hylle, uansett enhet. Linjene i forslaget kan komme fra flere ulike kildedokumenter, og de kan være sortert etter vare, hyllenummer, kildedokument, forfallsdato eller lever til-adresse.  

Hvis du sorterer etter forfallsdato, kan du velge å slette alle linjer fra forslaget unntatt de som trenger umiddelbar oppmerksomhet. Linjer som ikke haster så mye, blir ikke virkelig slettet, men bare sendt tilbake til **Plukkutvalg**-forslaget. Når du oppretter plukkingen, er linjene allerede sortert etter forfallsdato, og du kan velge å tilordne plukkingen til en bestemt ansatt.  

> [!NOTE]  
>  Plukking for lagerlevering av varer som er montert til ordren som leveres følger samme fremgangsmåte som for vanlig lagerplukking for levering, som beskrevet i dette emnet. Antall plukklinjer per antall som skal leveres, kan imidlertid være mange til én fordi du plukker komponentene, ikke monteringsvaren.  
>   
>  Lagerplukklinjene opprettes for verdien i **Restantall**-feltet på linjene i monteringsordren som er knyttet til ordrelinjen som skal leveres. Dette sikrer at alle komponentene er plukket i én handling.  
>   
>  Hvis du vil ha mer informasjon, kan du se "Håndtere montere til ordre-varer i lagerleveringer" i Lagerlevering.  
>   
>  Hvis du vil ha informasjon om plukking av komponenter for monteringsordrer generelt, inkludert situasjoner der monteringsvaren ikke forfaller på en følgeseddel, kan du se [Plukke for montering eller produksjon i avanserte lageroppsett](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).  

## <a name="to-plan-picks-in-the-worksheet"></a>Slik planlegger du plukkinger i forslaget  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Plukkforslag**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Hent lagerdokumenter**.  
3.  Velg de følgesedlene du vil forberede plukking for. Du kan nå sortere linjene i en viss grad, men sorteringen du utfører her, vil ikke bli overført til plukkinstruksjonen. Du kan også slette noen av linjene for å få en mer effektiv plukking. Hvis det for eksempel finnes et antall linjer med varer i kryssoverføringshyller, er det mulig at du vil opprette en plukking for alle linjene som er knyttet til disse linjene. De kryssoverførte varene vil bli levert (sammen med andre varer på følgesedlene), og kryssoverføringshyllene vil ha plass til flere inngående varer.  
4.  Velg handlingen **Opprett plukk**, og fyll ut vinduet for **Opprett plukk**-forespørselen. Den sorteringen du ber om her, vil sortere de plukklinjene du oppretter. Du kan for eksempel opprette en plukking for hver sone, og sortere linjene etter hylleprioritering innenfor hver plukking.  
5.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Plukking**, og velg deretter den relaterte koblingen. Vinduet **Plukking** åpnes.  
6.  Du kan nå finne plukktilordningen du nettopp opprettet, ved å velge plukkingen med det høyeste nummeret.  
7.  I plukkingen kan du fremdeles endre den tilordnede bruker-IDen og måten linjene er sortert på, hvis det er nødvendig.  
8.  Velg handlingen **Skriv ut** hvis du vil skrive ut plukkinstruksjonene.  
9. Når du har utført plukkingen, velger du handlingen **Journal**.  

Hvis hyllene er nummererte på en måte som gjenspeiler det fysiske oppsettet av lageret, kan plukkeren bruke linjene som er sortert etter hyllekode, til å plukke til et antall leveringer i én runde i lageret. Den ansatte tar det nødvendige antall varer for hver følgeseddellinje ut av hver hylle og plasserer dem sammen med andre varer for den bestemte følgeseddelen. En plukker kan spare mye tid ved å plukke til flere følgesedler med ett besøk til hyllen.  

Et annet effektivt sorteringsalternativ er hylleprioritering, hvis det fysiske oppsettet av lageret er mer tilpasset hylleprioritering enn hyllekode.  

I plukkforslaget kan du også sortere etter lever til-adresse. Det gjør at du først kan samle og levere bestillinger til kunder som er langt bort.  

## <a name="see-also"></a>Se også
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

