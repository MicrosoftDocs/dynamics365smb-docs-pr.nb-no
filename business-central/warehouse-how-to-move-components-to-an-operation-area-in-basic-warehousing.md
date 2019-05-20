---
title: Flytte komponenter til et operasjonsområde i enkle lageroppsett | Microsoft-dokumentasjon
description: Hvis det forekommer varebehandlingsoperasjoner på lagerlokasjonen, må du kanskje flytte elementer mellom interne hyller for å reagere på interne kildedokumenter, for eksempel produksjon, montering eller serviceordrer på lokasjonen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0c14ae1300d0e569e04159484da6ffb6e0541947
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1248804"
---
# <a name="move-components-to-an-operation-area-in-basic-warehouse-configurations"></a>Flytte komponenter til et operasjonsområde i enkle lageroppsett
Hvis det forekommer varebehandlingsoperasjoner på lagerlokasjonen, må du kanskje flytte elementer mellom interne hyller for å reagere på interne kildedokumenter, for eksempel produksjon, montering eller serviceordrer på lokasjonen.  

> [!NOTE]  
>  Hvis du vil ha informasjon om hvordan du flytter varer mellom hyller uten kildedokumenter, kan du se Intern flytting.  

I avanserte lageroppsett, som er lokasjoner der oppsettfeltet **Bruk Lagerstyring** brukes, kan du bruke **Flytteforslag**-siden til å flytte varer mellom hyller. Hvis du vil ha mer informasjon, kan du se [Flytte varer i avanserte lageroppsett](warehouse-how-to-move-items-in-advanced-warehousing.md).  

I grunnleggende lageroppsett, som er lokasjoner som bruker oppsettsfeltet **Hylle obligatorisk** og **Plukk nødv.**, kan du registrere flytting av varer til interne operasjonsområder baser på interne kildedokumenter på følgende måter:  

-   På siden **Lagerflytting**.  
-   Med siden **Lagerplukk**.  

> [!NOTE]  
>  Lagerplukk bokfører også negative vareposter som forbruk og støttes bare for produksjonskomponenter. Du finner mer informasjon på siden Lagerplukk.  

Hvis du vil ha detaljert informasjon om lagerflyttinger, kan du se siden Lagerflytting.  

To forskjellige roller kan opprette den innledende lagerflyttingen. En monteringsarbeider kan for eksempel opprette den fra en frigitt monteringsordre, slik at den vises i lagermedarbeiderens liste over arbeid som skal utføres. Hvis du vil opprette en lagerflytting for monteringsordrelinjer som har komponenter som er klare for flytting til angitte hyller, bruker montøren funksjonen **Opprett lagerflytting**.  

En lagermedarbeider kan også opprette den ved å peke på den aktuelle frigitte monteringsordren. Dette er beskrevet i følgende fremgangsmåte.  

> [!NOTE]  
>  Hvis flyttingen er for en monteringsordre der varen er montert til en ordre, kan du angi at lagerflyttingsdokumentet opprettes automatisk når du oppretter lagerplukkdokumentet som tar den ferdige monteringsvaren og bokfører leveringen. Hvis du vil konfigurere dette, kan du velge feltet **Opprett flyttinger automatisk** på siden **Monteringsoppsett**  
>   
>  Hvis du vil ha mer informasjon om monteringsordrer og grunnleggende lageroppsett, kan du se [Håndtere montere-til-ordre-varer med lagerplukk](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

Denne fremgangsmåten viser hvordan du oppretter en lagerflytting fra siden **Lagerflytting** ved å referere til en frigitt monteringsordre som et kildedokument. Fremgangsmåten er den samme når du flytter komponenter for produksjonsordrer og serviceordrer.  

## <a name="to-move-components-to-an-operation-area-in-basic-warehouse-configurations"></a>Flytte komponenter til et operasjonsområde i enkle lageroppsett  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagerflytting**, og velg den relevante koblingen.  
2.  På hurtigfanen **Generelt** fyller du ut **Nr.**-feltet . Du kan trykke ENTER for å velge fra nummerserien.  
3.  Angi lokasjonen der flyttingen finner sted, i **Lokasjonskode**-feltet.  
4.  Velg handlingen **Hent kildedokumenter**. Du kan også fylle ut feltet **Kildedokument** og deretter velge **AssistEdit**-knappen i feltet **Kildenr.**  
5.  Velg monteringsordren du vil flytte komponenter for, på siden **Kildedokumenter**, og klikk deretter **OK**.  

    For hver nødvendige komponent som kan flyttes, genereres én Hent-linje og én Plasser-linje på siden **Lagerflyttinger**. Alle felt bortsett fra **Ant. som skal håndt.** er forhåndsutfylt i henhold til kildedokumentlinjene. Feltet **Ant. som skal håndt.** settes til null inntil du angir antallet du faktisk har flyttet.  

    Du kan endre hyllekoden på en Hent-linje, men bare i henhold til tilgjengelighet. Hvis du klikker **AssistEdit**-knappen i **Hyllekode**-feltet på en Hent-linje, åpnes **Hylleinnhold**-siden, der bare hyller hvor komponenten er tilgjengelig, vises.  

    Du kan ikke endre hyllekoden på en Plasser-linje. Det er bare hyllekoden som er definert på komponentlinjen i kildedokumentet som godtas. Dette støtter prinsippet om at rollen som ber om en komponent, som er en monteringsarbeider i denne prosedyren, vet hvor komponenten må plasseres. Hvis du vil plassere komponentene på en annen hylle, må du først endre hyllekoden på komponentlinjen og deretter opprette lagerflyttingslinjene på nytt.  
6.  Angi angi det hele eller delvise antallet du faktisk har flyttet, i feltet **Ant. som skal håndt.**. Verdiene på Hent- og Plasser-linjene må være like. Eller kan du ikke registrere flyttingen.  

    > [!NOTE]  
    >  Som i andre lageraktiviteter kan du dele Plasser-linjen ved å velge handlingen **Handlinger** og deretter **Del linje**. I dette tilfellet må summen av to delte Plasser-linjene være lik antallet på Hent-linjen.  

7.  Når du er klar til å registrere flyttingene som du har utført, velger du handlingen **Registrer lagerflytting**.  

    Lagerposter opprettes og gjenspeiler at komponentene nå er i hyllene som er angitt på monteringsordrelinjene.  

    > [!NOTE]  
    >  I motsetning til når du flytter komponenter en lagerplukking, bokføres ikke forbruk når du registrerer en lagerflytting. Dette trinnet må utføres separat ved å bokføre avgang og forbruk av monteringsordren. Hvis du vil ha mer informasjon, kan du se Monteringsordre.  

## <a name="see-also"></a>Se også  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
