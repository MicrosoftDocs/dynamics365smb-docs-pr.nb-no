---
title: Definere priser og kostnader for servicer | Microsoft-dokumentasjon
description: Finn ut hvordan du definerer priser og ekstra kostnader for servicer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 44f6064d33d132f4a7d80bc8adc9dbff55d3a516
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773708"
---
# <a name="set-up-pricing-and-additional-costs-for-services"></a>Definere priser og ekstra kostnader for servicer
Du kan bruke prissettingsfunksjonene i [!INCLUDE[prod_short](includes/prod_short.md)] til å definere og tilpasse programmet slik at du bruker og justerer prissetting for servicevarer, -reparasjoner og -ordrer. Disse prissettingsavgjørelsene kan deretter enkelt overføres til faktureringsprosessen.  
  
Alt etter implementering kan du definere prissettingsgrupper og knytte dem til bestemte tidsperioder, kunder eller valutaer. Du kan definere fast, minimum eller maksimum prissetting, avhengig av servicekontraktene du har med kundene. Når du justerer prisene, kan du vise og godkjenne endringene før de bokføres.  

## <a name="to-set-up-a-service-price-group"></a>Slik definerer du serviceprisgrupper
Du kan definere grupper som inneholder servicevarer som du vil skal ha samme spesielle serviceprissetting. Du tilordner serviceprisgrupper til servicevarer på servicevarelinjer. Du kan dessuten tilordne serviceprisgrupper til servicevaregrupper.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Serviceprisgrupper**, og velg deretter den relaterte koblingen.  
2. Opprett en ny serviceprisgruppe.  
3. Fyll ut feltene **Kode** og **Beskrivelse**.  
4. Velg handlingen **Oppsett**.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

 > [!Tip]
 > Feltene **Justeringstype** og **Beløp** fungerer sammen for å angi om justeringen gjelder et fast beløp, eller bare gjelder når den samlede serviceprisen er høyere eller lavere enn beløpet i feltet **Beløp**.  

## <a name="to-set-up-a-service-price-adjustment-group"></a>Slik definerer du serviceprisjusteringsgrupper  
Du kan definere prisjusteringsgrupper for å justere serviceprissetting av servicevarer. Du kan for eksempel definere prisjusteringsgrupper som justerer prisen på frakt eller reservedeler.  
  
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Serviceprisjusteringsgrupper**, og velg deretter den relaterte koblingen.  
2. Opprett en ny serviceprisjusteringsgruppe.  
3. Fyll ut feltene **Kode** og **Beskrivelse**.  
4. Angi hvilken posttype du vil justere, i **Type**-feltet.  
  
    * Hvis du vil justere bare én bestemt post, kan du angi nummeret for posten i feltet **Nr.** . Hvis du lar dette feltet være tomt, vil justeringsgruppen justere alle poster av den definerte typen i feltet **Type**.  
    * Hvis du vil justere servicepriser relatert til bare én bestemt service, kan du fylle ut feltet **Arbeidstype**. Hvis du lar dette feltet være tomt, blir det oversett.  
  
5. I feltet **Beskrivelse** kan du angi en kort beskrivelse av serviceprisjusteringen.  
6. Hvis du vil justere servicepriser relatert til bare én bestemt varebokføringsgruppe, fyller du ut feltet **Bokføringsgruppe - vare**.

> [!Tip]
> Du kan velge **Detaljer** for å legge til tilleggsinformasjon om justeringsgruppen. Du kan for eksempel definere hvilke varer som hører til en serviceprisjusteringsgruppe, og om dette er en vare, ressurs, ressursgruppe eller servicekostnad.  

## <a name="to-set-up-additional-costs-for-services"></a>Definere ekstra kostnader for servicer
Når du arbeider med servicevarer og serviceordrer, kan det hende du må registrere tilleggskostnader, for eksempel reiseutgifter til bestemte servicesoner eller startgebyrer. Når du oppretter en serviceordre, kan du sette inn disse kostnadene, og en linje av typen **Kost** legges til i ordren. Hvis du vil bruke kostnaden for alle serviceordrer, kan du definere en standardkost. For eksempel hvis du vil bruke et startgebyr.
  
### <a name="to-set-up-service-costs"></a>Definere servicekostnader
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicekostnader**, og velg deretter den relaterte koblingen. 
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

### <a name="to-specify-a-default-cost-for-service-orders"></a>Angi en standardkost for serviceordrer
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Serviceoppsett**, og velg deretter den relaterte koblingen. 
2. I feltet **Startgebyr for serviceordre** velger du den aktuelle servicekostnaden.

## <a name="see-also"></a>Se også
[Konfigurere servicehåndtering](service-setup-service.md)  
[Servicebehandling](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]