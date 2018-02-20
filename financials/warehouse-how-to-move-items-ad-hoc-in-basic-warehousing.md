---
title: Flytte varer ad hoc i enkle lageroppsett | Microsoft-dokumentasjon
description: "Av og til kan det være nødvendig å flytte varer mellom interne hyller, hyller som ikke er mottakshyller eller leveringshyller, uten et bestemt behov fra et kildedokument. Du kan utføre disse ad hoc-flyttingene for eksempel for å omorganisere lageret, for å hente varer til et kontrollområde eller for å flytte tilleggsvarer til og fra et produksjonsområde uten et systemforhold til kildedokumentet for produksjonsordren."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 5c64734d9bb5cced1dbe9cb9c98385004885fa67
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---
# <a name="move-items-ad-hoc-in-basic-warehouse-configurations"></a>Flytte varer ad hoc i enkle lageroppsett
Av og til kan det være nødvendig å flytte varer mellom interne hyller, hyller som ikke er mottakshyller eller leveringshyller, uten et bestemt behov fra et kildedokument. Du kan utføre disse ad hoc-flyttingene for eksempel for å omorganisere lageret, for å hente varer til et kontrollområde eller for å flytte tilleggsvarer til og fra et produksjonsområde uten et systemforhold til kildedokumentet for produksjonsordren.  

I grunnleggende lageroppsett, det vil si lokasjoner som bruker oppsettsfeltet **Hylle obligatorisk** og muligens oppsettsfeltene **Plukk nødv.** og **Plassering nødv.**, kan du registrere ad hoc-flyttinger uten kildedokumenter på følgende måter:  

    - I vinduet **Intern flytting**.  
    - Med vinduet **Varereklassifiseringskladd**.  

> [!NOTE]  
>  I avanserte lageroppsett, det vil si lokasjoner der oppsettsfeltet **Bruk Lagerstyring** brukes, bruker du vinduet **Flytteforslag** eller vinduene **Intern plukk** og **Intern plassering** til å flytte varer ad hoc mellom hyller.  

## <a name="to-move-items-as-an-internal-movement"></a>Flytte varer som en intern flytting  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Intern flytting**, og velg deretter den relaterte koblingen.  
2.  På hurtigfanen **Generelt** fyller du ut **Nr.**-feltet enten ved å la det stå eller ved å velge **AssistEdit** for å velge fra nummerserien.  
3.  Angi lokasjonen der flyttingen finner sted, i **Lokasjonskode**-feltet.  

    Hvis lokasjonen er definert som standardlokasjonen for deg som lageransatt, settes lokasjonskoden inn automatisk.  
4.  Angi en kode for hyllen som du vil flytte elementet til, i feltet **Til hylle-kode**. Til produksjonsformål kan dette for eksempel være den åpne produksjonshyllekoden, som definert på lokasjonskortet eller i arbeidssenteret.  
5.  Angi datoen flyttingen må fullføres innen, i **Forfallsdato**-feltet.  
6.  På hurtigfanen **Linjer** velger du **Varenr.**-feltet for å åpne vinduet **Hylleinnhold - oversikt** og velger deretter varen du vil flytte basert på tilgjengeligheten i hyllene. Du kan også velge handlingen **Hent hylleinnhold** for å fylle ut de interne flyttelinjene basert på filtrene dine. Hvis du vil ha mer informasjon, kan du se verktøytipset for handlingen **Hent hylleinnhold**.   

    Når du har valgt varen, blir feltet **Fra hylle-kode** automatisk fylt ut i henhold til det valgte hylleinnholdet, men du kan endre det til en hvilken som helst annen hylle der varen er tilgjengelig.  

    > [!NOTE]  
    >  Siden feltet **Varenr.** og feltet **Fra hylle-kode** er koblet sammen, kan verdiene endres uavhengig når du redigerer et av feltene.  

    Feltet **Til hylle-kode** fylles ut med verdien du anga i hodet, men du kan endre den på linjen til en annen hyllekode som ikke er blokkert eller dedikert til spesielle formål. Hvis du vil ha mer informasjon om hvordan du gjør hyller dedikert, kan du se Dedikert.  
7.  Når du har definert hvilke hyller du vil flytte varen fra og til, angir du antallet som skal flyttes, i feltet **Antall**.  

    > [!NOTE]  
    >  Antallet må være tilgjengelig i Fra hylle-koden.  

8.  Når du er klar til å behandle den interne flyttingen, velger du handlingen **Opprett lagerflytting**.  

    > [!NOTE]  
    >  Når du har opprettet lagerflyttingen, slettes linjene for intern flytting.  

    Du utfører resten av ad hoc-flyttingen i vinduet **Lagerflytting** på samme måte som for en flytting basert på kildedokumenter. Hvis du vil ha mer informasjon, kan du for eksempel se [Flytte komponenter til et operasjonsområde i enkle lageroppsett](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  

## <a name="to-move-items-with-the-item-reclassification-journal"></a>Flytte varer med varereklassifiseringskladden
I stedet for å bruke lagerflyttingsdokumenter kan du registrere flytting av varer ved å reklassifisere hyllekodene. Hvis du vil ha mer informasjon, se [Telle, justere og reklassifisere lagerbeholdning](inventory-how-count-adjust-reclassify.md).   
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Vareoverføringskladd**, og velg deretter den relaterte koblingen.  
2.  På hver kladdelinje kan du definere hyllene du vil flytte elementer til og fra ved å fylle ut feltene **Hyllekode** og **Ny hyllekode**.  

    1.  Hvis du vil flytte hele hylleinnholdet fra en hylle til en annen, velger du handlingen **Hent hylleinnhold**.  
    2.  Angi filtrene for å finne hyllen du vil flytte innholdet fra, og klikk deretter **OK**. Kladdelinjene fylles ut med innholdet i hyllen.  
3.  Fyll ut de gjenstående feltene på hver kladdelinje.   
4.  Bokfør reklassifiseringskladden.  

    > [!NOTE]  
    >  I motsetning til flyttedokumenter oppretter ikke en flytting som bokføres i reklassifiseringskladden, en lagerforespørsel om å utføre den fysiske oppgaven.  

## <a name="see-also"></a>Se også  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

