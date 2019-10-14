---
title: Lagertrekke komponenter i henhold til operasjonsavgang | Microsoft-dokumentasjon
description: For varer som er definert med trekkmetoden Bakover, er standard virkemåte å beregne og bokføre komponentforbruk når du endrer statusen for en frigitt produksjonsordre til **Ferdig**. Hvis du vil ha mer informasjon, kan du se Trekkmetode.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 3c1bcf36ed2ec494b54fe8fdf3b26b07aa834f7f
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2313399"
---
# <a name="flush-components-according-to-operation-output"></a>Lagertrekke komponenter i henhold til operasjonsavgang
For varer som er definert med trekkmetoden Bakover, er standard virkemåte å beregne og bokføre komponentforbruk når du endrer statusen for en frigitt produksjonsordre til **Ferdig**.  

Hvis du også definerer rutekoblingskoder, skjer beregning og bokføring når hver operasjon er fullført, og antallet som faktisk ble forbrukt i operasjonen, bokføres. Hvis du vil ha mer informasjon, kan du se [Opprette ruter](production-how-to-create-routings.md).  

Hvis en produksjonsordre om å produsere 800 meter for eksempel krever 8 kg av en komponent, bokføres 2 kg automatisk som forbruk når du bokfører 200 meter som avgang.  

Denne funksjonaliteten er nyttig av følgende årsaker:  

-   **Lagerverdisetting** -Verdipostene for avgang og forbruk opprettes parallelt ettersom produksjonsordren går fremover. Uten rutekoblingskoder vil lagerverdien øke etter hvert som avgangen bokføres og deretter reduseres på et senere tidspunkt når verdien for komponentforbruk bokføres sammen med den ferdige produksjonsordren.  
-   **Lagertilgjengelighet** - Med gradvis forbruksbokføring er komponentvarenes tilgjengelighet mer oppdatert, noe som er viktig for å opprettholde den interne balansen mellom behov og forsyning. Uten rutekoblingskoder kan andre behov for komponenten tro at den er tilgjengelig så lenge den venter på en forsinket forbruksbokføring.  
-   **Til rett tid**  – Med evnen til å tilpasse produktene til kundens ønsker kan du minimere svinn ved å kontrollere at arbeids- og systemendringer bare forekommer når det er nødvendig.  

Følgende fremgangsmåte viser hvordan du kombinerer lagertrekk bakover og rutekoblingskoder slik at lagertrekksantallet for hver operasjon er proporsjonalt med den faktiske avgangen for den fullførte operasjonen.  

## <a name="to-flush-components-according-to-operation-output"></a>Slik utfører du lagertrekk i henhold til operasjonsavgang:  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Varer**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Rediger**.  
3.  På hurtigfanen **Etterfylling**, i **Trekkmetode**- feltet, velger du **Fremover**.  

    > [!NOTE]  
    >  Velg **Plukk + Fremover** hvis komponenten er brukt på en lokasjon som er konfigurert for lagerstyring.  

4.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ruter**, og velg deretter den relaterte koblingen.  
5.  Definer rutekoblingskoder for hver operasjon som forbruker komponenten. Hvis du vil ha mer informasjon, kan du se [Opprette ruter](production-how-to-create-routings.md).  
6.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Produksjonsstykkliste**, og velg deretter den relaterte koblingen.  
7.  Definer rutekoblingskoder fra hver forekomst av komponenten til operasjonen der den er brukt.

    > [!IMPORTANT]  
    >  Komponenten må ha en rutekobling til den siste operasjonen i ruten.  

## <a name="see-also"></a>Se også  
[Opprette produksjonsstykklister](production-how-to-create-production-boms.md)  
[Definere produksjon](production-configure-production-processes.md)  
[Produksjon](production-manage-manufacturing.md)    
[Planlegging](production-planning.md)   
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
