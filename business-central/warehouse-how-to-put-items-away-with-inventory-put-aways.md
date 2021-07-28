---
title: Plassere varer med lagerplasseringer
description: Les mer om hvordan du bruker lagerplasseringsdokumentet til å registrere og bokføre plasserings- og mottaksopplysninger for kildedokumentene.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: e28e565858f4dc6fc1e01c614914b0b1620c9659
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6438110"
---
# <a name="put-items-away-with-inventory-put-aways"></a>Plassere varer med lagerplasseringer
Hvis lokasjonen er definert for å kreve lagerplasseringsbehandling, men ikke mottaksbehandling, bruker du dokumentet **Lagerplassering** til å registrere og bokføre plasserings- og mottaksopplysninger for kildedokumentet. Det inngående kildedokument kan være en bestilling, en ordreretur, en inngående overføringsordre eller en monterings- eller produksjonsordre med avgang som er klar til å plasseres.  

Du kan opprette lagerplassering på tre måter:  

- Opprett plasseringen i to trinn, ved først å opprette en lagerforespørsel fra kildedokumentet, som fungerer som et signal til lageret om at kildedokumentet er klart for plassering. Lagerplasseringen kan så opprettes på siden **Lagerplassering** basert på kildedokumentet.  
- Opprette lagerplassering direkte fra selve kildedokumentet.  
- Opprett lagerplasseringer for flere kildedokumenter samtidig, ved hjelp av en kjørsel.  

## <a name="to-request-an-inventory-put-away-by-releasing-the-source-document"></a>Be om en lagerplassering ved å frigi kildedokumentet
Når det gjelder bestillinger, ordrereturer, inngående overføringsordrer og monteringsorder, oppretter du lagerforespørselen ved å frigi ordren. Fremgangsmåten nedenfor beskriver hvordan dette gjøres fra en bestilling.  

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bestillinger**, og velg deretter den relaterte koblingen.
2. Velg bestillingen som skal frigis, og velg deretter **Frigi**-handlingen.  

    Når det gjelder produksjonsordrer, oppretter du lagerforespørselen ved å opprette en inngående forespørsel fra den frigitte produksjonsordren.  
3.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Frigitte produksjonsordrer**, og velg deretter den relaterte koblingen.  
4. Velg handlingen **Opprett inng. lagerforespørsel**.  

> [!NOTE]  
>  Du kan også opprette den inngående lagerforespørselen ved å merke av for **Opprett inngående foresp.** når du fornyer produksjonsordren. Hvis du vil ha mer informasjon, se [Fornye eller planlegge produksjonsordrer på nytt](production-how-to-replan-refresh-production-orders.md).  

Når lagerforespørselen er opprettet, kan en lageransatt som har som oppgave å plassere varer, se at kildedokumentet er klart for plassering og opprette et lagerplasseringsdokument.  

## <a name="to-create-an-inventory-put-away-based-on-the-source-document"></a>Slik oppretter du en lagerplassering basert på kildedokumentet
Nå som forespørselen er opprettet, kan den lageransatte opprette en ny lagerplassering basert på det frigitte kildedokumentet.   
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerplassering** og velg den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. Velg hvilken type kildedokument du plasserer for, i **Kildedokument**-feltet.  
4. Velg kildedokumentet i **Kildenr.**-feltet.  
5. Du kan også velge handlingen **Hent kildedokument** for å velge dokumentet fra en liste over inngående kildedokumenter som er klare for plassering på lokasjonen.  
6. Velg **OK**-knappen for å fylle ut plasseringslinjene i henhold til det valgte kildedokumentet.  

## <a name="to-create-an-inventory-put-away-from-the-source-document"></a>Slik oppretter du en lagerplassering fra kildedokumentet  
1.  I kildedokumentet, som kan være en bestilling, ordreretur, inngående overføringsordre eller produksjonsordre, velger du handlingen **Opprett lagerplassering/-plukking**.  
2. Merk av for **Opprett lagerplassering**.
3. Velg **OK**. En ny lagerplassering er opprettet.

## <a name="to-create-multiple-inventory-put-aways-with-a-batch-job"></a>Slik oppretter du flere lagerplasseringer med en kjørsel:  
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Opprett plassering/plukk for lager**, og velg deretter den relaterte koblingen.  
2.  På hurtigfanen **Lagerforespørsel** på forespørselssiden bruker du filtrene **Kildedokumentet** og **Kildenr.** for å filtrere etter bestemte dokumenttyper eller dokumentnummerintervaller.  
3.  Merk av for **Opprett lagerplassering** på hurtigfanen **Alternativer**.
4.  Velg **OK**. De angitte lagerplasseringene blir opprettet.

## <a name="to-record-the-inventory-put-away"></a>Slik registrerer du lagerplasseringen  
1. Åpne et opprettet plasseringsdokument ved å velger et på siden **Lagerplasseringer**.  
2. I **Hyllekode**-feltet på plasseringslinjene foreslås hyllen som varene skal plasseres, per varens standardhylle. Du kan endre hylle på denne siden hvis det er nødvendig.  
3. Utfør plasseringen, og angi opplysninger om det faktiske plasseringsantallet i feltet **Ant. som skal håndt**.

    Hvis varene for én linje må plasseres i mer enn én hylle, for eksempel fordi den angitte hyllen er full, bruker du funksjonen **Del linje** i hurtigfanen **Linjer**. Hvis du vil ha mer informasjon om deling av linjer, kan du se [Dele lageraktivitetslinjer](warehouse-how-to-split-warehouse-activity-lines.md).  
4. Når du har utført plasseringen, velger du handlingen **Bokfør**.  

Bokføringsprosessen bokfører mottaket, eller avgang for produksjonsordrer, av kildedokumentlinjene som er plassert. Hvis lokasjonen bruker hyller, oppretter bokføringen også lagerposter for bokføring av hylleantallendringer.

## <a name="see-also"></a>Se også  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]