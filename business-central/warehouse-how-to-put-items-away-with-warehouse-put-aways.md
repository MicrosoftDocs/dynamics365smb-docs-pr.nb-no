---
title: Plassere varer med lagerplasseringer | Microsoft-dokumentasjon
description: Når lokasjonen er definert til å bruke plasseringsbehandling og lagermottaksbehandling, må du bruke funksjonen for plasseringsdokumenter til å styre plasseringen av varene.
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
ms.openlocfilehash: 645c11a3d5cfb29dd4e0cbf83086cea58831fe42
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "926584"
---
# <a name="put-items-away-with-warehouse-put-aways"></a>Plassere varer med lagerplasseringer
Når lokasjonen er definert til å bruke plasseringsbehandling og lagermottaksbehandling, må du bruke funksjonen for plasseringsdokumenter til å styre plasseringen av varene.  

Når du bokfører et lagermottak, oppdateres kildedokumentene, for eksempel bestilling, inngående overføringsordre eller ordreretur, antall mottatt i varepostene bokføres, og linjene om varene som er mottatt, sendes til plasseringsfunksjonen i lageret. Hvis du har intern plassering og plukking, kan den interne plasseringen også opprette linjer for plassering.  

Avhengig av lageroppsettet gjøres linjene tilgjengelige for plasseringsforslaget eller brukes til å generere plasseringsinstruksjoner umiddelbart. Hvis du vil ha mer informasjon, kan du se [Planlegge plasseringer i forslag](warehouse-how-to-plan-put-aways-in-worksheets.md).  

I tillegg til standardmåter å opprette plasseringer på, som er beskrevet i dette emnet, kan du opprette plasseringen fra det relaterte bokførte lagermottaket. Dette er nyttig hvis du har slettet plasseringslinjer, eller hvis du bruker lagerstyring og har bestemt deg for å ikke bruke plasseringsforslaget, fordi du kan opprette eller gjenopprette plasseringsinstruksjoner fra de bokførte mottakslinjene.  

## <a name="to-put-items-away-without-directed-put-away-and-pick"></a>Slik plasserer du varer uten lagerstyring  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagerplasseringer**, og velg deretter den relaterte koblingen.  
2.  Åpne lagerplasseringen som er klar til å håndtere.  

    Du kan sortere plasseringslinjene etter ulike kriterier, for eksempel etter vare, hyllenummer eller forfallsdato, og dermed optimalisere plasseringsprosessen.  
3.  På hver linje, i feltet **Ant. som skal håndt.** angir du det antall varer du vil plassere.  
4.  Når du har fullført plasseringen av varene, velger du handlingen **Registrer plassering** for å registrere at aktiviteten er fullført, og gjøre varene tilgjengelig for plukking.  

## <a name="to-put-items-away-with-directed-put-away-and-pick"></a>Slik plasserer du varer med lagerstyring  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagerplasseringer**, og velg deretter den relaterte koblingen.
    Hvis det er opprettet plasseringsinstruksjoner, er en plassering synlig.  
2.  Åpne lagerplasseringen som du vil arbeide med.  
3.  Hvis lageret krever det, angir du bruker-IDen på hurtigfanen **Generelt** når du begynner å arbeide med en bestemt plassering.  
4.  Utfør hentings- og plasseringshandlingene angitt på linjene i feltet **Handlingstype**.  

    Vær oppmerksom på at hver mottakslinje er blitt til mist to linjer i plasseringen:  

    -   Den første linjen, med **Hent** i **Handlingstype**-feltet, angir hvor varene er plassert i mottaksområdet. Du kan ikke endre sone- og hyllefeltet på denne linjen.  
    -   Den neste linjen, med **Plasser** i **Handlingstype**-feltet, viser hvor du må plassere varene i lageret. Hvis lageret har mottatt et stort antall varer på én mottakslinje, kan det hende de må plasseres i flere hyller, det finnes derfor en Plass-linje for hver hylle.  

        Hvis Hent- og Plasser-linjene for hvert mottak ikke følger umiddelbart etter hverandre, og du vil at de skal gjøre det, kan du sortere linjene ved å velge **Vare** i feltet **Sorteringsmetode** i hurtigfanen **Generelt**.  

        Hvis det fysiske oppsettet av lageret gjenspeiler hylleprioriteringene, kan du bruke sorteringsmetoden **Hylleprioritering** til å forberede en plasseringsrunde som vil begrense dine turer gjennom lageret.  

5.  Når du har plassert alle varene i hyller i henhold til instruksjonen, velger du handlingen **Registrer plassering**.  

På steder som er definert for å bruke styrt plassering og plukk, er følgende innstillinger forutsetninger for fremgangsmåten ovenfor:  

- En plasseringsmal konfigureres. Hvis du vil ha mer informasjon, kan du se [Definere plasseringsmaler](warehouse-how-to-set-up-put-away-templates.md).  
- Vekten, kubikkinnholdet og spesielle lagringskrav for varen eller lagerføringsenheten er definert. Hvis du vil ha mer informasjon, kan du se Bruttovekt.  
- Kapasiteten, hylletypen og prioriteringen til hyllene. Hvis du vil ha mer informasjon, kan du se hylleprioritering.  

Hylleprioriteringen trer i kraft hvis det er flere enn én hylle som er i samsvar med plasseringsmalkriteriene. Hvis både plasseringsmalkriteriene og hylleprioriteringen er den samme for flere hyller, velges hyllen med det høyeste nummeret.

## <a name="to-create-a-put-away-from-a-posted-receipt"></a>Slik oppretter du en plassering fra et bokførte mottak:  
 Hvis lokasjonen bruker både plasserings- og mottaksbehandling og du har slettet plasseringslinjer, eller hvis du bruker lagerstyring og har bestemt deg for å ikke bruke plasseringsforslaget, kan du opprette eller gjenopprette plasseringsinstruksjoner for de bokførte mottakslinjene på følgende måte:

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokførte lagermottak**, og velg deretter den relaterte koblingen.  
2.  Velg et bokført mottak som skal plasseres.  
3.  Velg handlingen **Kort**.  

    Hvis feltet **Dokumentstatus** er tomt, er mottaket ikke plassert. Ellers indikerer feltet mottaket som delvis plassert eller fullstendig plassert.  

4.  Hvis mottaket er delvis plassert eller ikke plassert, klikker du på handlingen **Opprett plassering**.  
5.  Fyll ut kjørselssiden for å opprette plasseringen, og klikk deretter **OK**.   

## <a name="see-also"></a>Se også  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
