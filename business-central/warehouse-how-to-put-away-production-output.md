---
title: Plassere produksjonsavgang | Microsoft-dokumentasjon
description: Hvordan du plasserer avgang fra produksjon, avhenger av hvordan lageret er definert som lokasjon.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 9092100816c58fe2882c61214a5008e27591d4f5
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="put-away-production-or-assembly-output"></a>Plassere produksjonsavgang eller monteringsavgang
Hvordan du plasserer avgang fra produksjon, avhenger av hvordan lageret er definert som lokasjon. Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).  

I grunnleggende lageroppsett hvor lokasjonen krever plasseringsbehandling, men ikke mottaksbehandling, bruker du dokumentet **Lagerplassering** til å organisere og registrere plasseringen av avgang.  

I avanserte lageroppsett hvor lokasjonen krever både plasserings- og mottaksbehandling, kan du opprette enten et internt plasseringsdokument eller et flyttedokument for å plassere avgangen.  

Det første trinnet ved opprettelse av plasseringsavgang, er å opprette den inngående lagerforespørselen. Denne forespørselen informerer lageret om at produksjons- eller monteringsordreavgangen er klar til å plasseres.

## <a name="to-create-the-inbound-warehouse-request"></a>Slik oppretter du den inngående lagerforespørselen  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Frigitt produksjonsordre**, og velg deretter den relaterte koblingen.  
2.  På produksjonsordren som er klar til plassering, velger du handlingen **Opprett inngående lagerforespørsel**.  

> [!NOTE]  
>  Du kan også opprette den inngående lagerforespørselen ved å merke av for **Opprett inngående foresp.** når du fornyer produksjonsordren. Hvis du vil ha mer informasjon, se [Fornye eller planlegge produksjonsordrer på nytt](production-how-to-replan-refresh-production-orders.md).  

## <a name="to-put-output-away-with-an-inventory-put-away"></a>Slik plasseres varer med lagerplassering  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagerplassering**, og velg deretter den relaterte koblingen.  
2.  Opprett en ny lagerplassering. Hvis du vil ha mer informasjon, kan du se [Plassere varer med lagerplasseringer](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3.  Du får tilgang til produksjonsordreavgang ved å velge handlingen **Hent kildedokumenter** og deretter velge den frigitte produksjonsordren.  
4.  Fyll ut plasseringslinjene.
5.  Når linjene er klare for bokføring, velger du handlingen **Bokfør**. Bokføringen vil opprette de nødvendige lagerpostene og bokføre avgangen av varene.  

Du kan også opprette en **Lagerplassering** direkte fra den frigitte produksjonsordren. Hvis du vil ha mer informasjon, kan du se [Plassere varer med lagerplasseringer](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Når du bokfører en lagerplassering, antas det at alle operasjonene bokføres i henhold til standardruten, det vil si at avgangsantall bokføres i henhold til den siste operasjonen. Du kan bruke ferdigmeldingskladden til å bokføre avvik i avgangsantall og oppstillingstid og operasjonstid. Hvis det er nødvendig å bokføre delvis etter at du har opprettet lagerplasseringen, kan du gjøre dette for oppstillingstider og antall for alle operasjoner bortsett fra den siste. I dette tilfellet styres den siste operasjonen av lagerplasseringen.  

Hvis du bare trenger å bokføre oppsett eller kjøretid i den siste operasjonen, kan du sette avgangsantallet i den siste operasjonen til 0. Du kan også velge ikke å bokføre den siste linjen i det hele tatt ved å slette den.  

## <a name="to-put-output-away-with-a-warehouse-internal-put-away"></a>Slik plasserer du avgang med intern plassering eller flytting
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Intern plassering**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.
3. Fyll ut hodet til den nye interne plasseringen med minst feltet **Lokasjonskode**.  
4. Fyll ut en linje for hver vare du vil flytte til lageret. Du trenger bare å fylle ut feltene **Varenr.** og **Antall**.  

    > [!NOTE]  
    >  Når du velger feltet **Varenr.**, åpnes **Hylleinnholdsoversikt** i stedet for **Vareoversikt**. Det kommer av at du ønsker å plassere varer som er i en bestemt hylle (et hylleinnhold), ikke bare en vare, og du vet allerede hvilken hylle varen skal tas fra.  

4.  Hvis du vil fylle ut forslagslinjene med hele hylleinnholdet eller det filtrerte hylleinnholdet i hyller i lokasjonen, velger du handlingen **Hent hylleinnhold**.  
5.  Velg handlingen **Opprett plassering**. Varene du vil flytte ut av produksjon, er nå i plasseringsinstruksjoner og venter på å bli lagret i lageret.  

> [!NOTE]  
>  Når lagerlokasjonen er definert til å bruke lagerstyring, er lageret koblet til produksjonsfunksjonen gjennom standardproduksjonshyllene: Dette er de inngående, utgående og åpne produksjonshyllene, som alle defineres på hurtigfanen **Hyller** på lokasjonskortet. Når du bokfører avgangen til en produksjonsordre, plasseres avgangen i den **utgående produksjonshyllen**. Du følger samme fremgangsmåte som den beskrevet ovenfor, til å plassere produksjonsavgangen, bortsett fra at i stedet for å bruke varens standardhylle vil du flytte eller plassere varene fra den **utgående produksjonshyllen** til varens standardhylle.  

## <a name="to-manually-specify-a-bin-to-store-items-from-production-output"></a>Angi en hylle for plassering av varer fra produksjonsavgang manuelt  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Flytteforslag**, og velg deretter den relaterte koblingen.  
2.  Fyll ut hodet, og opprett en linje for hver vare du vil flytte til lageret.  
3.  Fyll ut både feltet **Fra hylle-kode** og feltet **Til hylle-kode**, og angi antallet i feltet **Antall**.  
4.  Hvis du vil fylle ut forslagslinjene med hele hylleinnholdet eller det filtrerte hylleinnholdet i hyller i lokasjonen, velger du handlingen **Hent hylleinnhold**.  
5. Velg handlingen **Opprett flytting**. Lagerflyttingsinstruksjonene opprettes med Hent- og Plasser-linjer som de lageransatte skal utføre.  

> [!NOTE]  
>  Du kan ikke angi kildedokumentnummeret, for eksempel produksjonsordrenummeret, i dokumentene for intern plassering, plukking eller plassering for noen av disse prosedyrene.  

## <a name="see-also"></a>Se også  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

