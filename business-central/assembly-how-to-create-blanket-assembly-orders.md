---
title: Opprette rammemonteringsordrer | Microsoft-dokumentasjon
description: Opprett rammeordrer for tilpassede monteringsvarer før du med jevne mellomrom oppretter de faktiske ordrene i henhold til rammeordreavtalen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e565a07bf148043de47eab5cba4df5c76beceb5a
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8146933"
---
# <a name="create-blanket-assembly-orders"></a>Opprette rammemonteringsordrer
Du kan bruke monteringsstyring for å tilpasse en monteringsvare i henhold til en kundeforespørsel under salgsprosessen. Hvis du vil ha mer informasjon, kan du se [Selge varer som er montert til ordre](assembly-how-to-sell-items-assembled-to-order.md).  

 Som med alle andre typer varer kan du også opprette rammeordrer for tilpassede monteringsvarer før du med jevne mellomrom lager de faktiske ordrene i henhold til rammeordreavtalen. Denne prosessen omfatter flere ekstra trinn når du sammenligner den med å opprette en vanlig rammeordre, og den bruker en variant av en koblet monteringsordre, som er en rammemonteringsordre.

> [!NOTE]  
>  I likhet med alle rammebestillinger er antallene på monteringsrammebestillinger bare prognoser og ikke operative før de konverteres til faktiske monteringsordrer. Derfor er ordrefunksjonalitet som beregning av tilgjengelighet, reservasjon og varesporing ikke aktiv for rammemonteringsordrer.  

## <a name="to-create-a-blanket-assembly-order-for-an-assemble-to-order-item"></a>Slik oppretter du en rammemonteringsordre for en montere\-til\-ordre-vare  
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Rammeordrer**, og velg deretter den relaterte koblingen.  
2. Opprette en ny rammeordre med én linje for en monteringsvare. Hvis du vil ha mer informasjon, kan du se [Opprette rammeordrer](sales-how-to-create-blanket-sales-orders.md).  
3. Angi hele antallet i feltet **Ant. som skal monteres til ordre** på linjen for rammemonteringsordre.

    > [!NOTE]  
    >  Du bør ikke opprette rammebestillingsavtaler for et delvist antall. Du må derfor angi samme antall som du skrev inn i feltet **Antall** på rammeordrelinjen.  

4. Velg handingen **Monter til ordre**, og velg deretter handlingen **Montere til ordre – linjer**. Du kan også merke feltet **Ant. som skal monteres til ordre** på linjen.  
5. Gå gjennom eller endre monteringsordrelinjene i henhold til rammeordreavtalen du har med kunden, på siden **Montere til ordre – linjer**. Hvis du vil vise mer informasjon, velger du **Vis dokument** for å åpne hele rammemonteringsordren. Du kan ikke endre innholdet i de fleste av feltene, og du kan ikke bokføre.  
6. Når du har justert monteringsordrelinjene i henhold til rammeordreavtalen, lukker du siden **Montere til ordre – linjer** for å gå tilbake til siden **Rammeordre**.  
7. Når kunden ber om å få opprettet en ordre basert på den avtalte rammeordren, oppretter du en ordre for den/de avtalte monteringsvaren(e). Hvis du vil ha mer informasjon, kan du se [Opprette rammeordrer](sales-how-to-create-blanket-sales-orders.md).

Den koblede rammemonteringsordren og eventuelle tilpasninger knyttes til denne nye salgsordren for å klargjøre for montering av varen(e) som skal selges.  

## <a name="see-also"></a>Se også
[Opprette rammeordrer](sales-how-to-create-blanket-sales-orders.md)  
[Monteringsstyring](assembly-assemble-items.md)  
[Arbeide med stykklister](inventory-how-work-BOMs.md)  
[Lager](inventory-manage-inventory.md)  
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]