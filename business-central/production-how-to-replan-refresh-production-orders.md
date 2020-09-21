---
title: Slik planlegger du på nytt eller fornyer produksjonsordrer direkte | Microsoft-dokumentasjon
description: Produksjonsordrelinjene inneholder varene som skal produseres i produksjonsordren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 48986fc36332c4bbca3f84208261fe8215e58f92
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2020
ms.locfileid: "3781863"
---
# <a name="replan-or-refresh-production-orders-directly"></a>Planlegge på nytt eller fornye produksjonsordrer direkte
Funksjonen **Planlegg på nytt** for produksjonsordrer brukes vanligvis etter at du har lagt til eller endret komponenter som utgjør underliggende produksjonsordrer. Funksjonen beregner endringer som utføres i komponenter og rutelinjer, og den inkluderer varer på lavere produksjonsstykklistenivåer. For disse varene genereres det kanskje nye produksjonsordrer.  

Basert på endringene du har gjort i komponentene og rutelinjene, beregner og planlegger funksjonen Planlegg på nytt for eventuelle nye behov for produksjonsordren.  

**Oppdater**-funksjonen på produksjonsordrene brukes vanligvis etter at du har gjort ett av følgende:

- Opprettet et produksjonsordrehode manuelt for å beregne og opprette linjedata for første gang.
- Gjort endringer i produksjonsordrehodet for å beregne alle linjedata på nytt.

Oppdateringsfunksjonen beregner endringene som utføres i et produksjonsordrehode, og involverer ikke produksjonsstykklistenivåer. Funksjonen beregner og tar initiativ til verdier for komponentlinjer og rutelinjer basert på hoveddata som er definert i den tilordnede produksjonsstykklisten og ruten, samt i henhold til ordreantallet og forfallsdatoen i produksjonsordrens hode.

Du kan enten sette inn produksjonsordrelinjene manuelt, eller bruke funksjonen som beregner produksjonsordrelinjene fra hodet.  

> [!NOTE]
> Hvis du bruker oppdateringsfunksjonen til å beregne produksjonsordrelinjer på nytt, slettes de gamle produksjonsordrelinjene og nye beregnes.  

## <a name="to-replan-a-production-order"></a>Slik planlegger du en produksjonsordre på nytt  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Fast planlagte prod.ordrer**, og velg deretter den relaterte koblingen.  
2.  Åpne produksjonsordren du vil planlegge på nytt.  
3.  På hurtigfanen **Linjer** velger du **Linjer**-handlingen, og deretter **Komponenter**-handlingen.  
4.  Legg til en komponent som er en produsert vare eller et halvfabrikata.  
5.  Velg handlingen **Planlegg på nytt** fra produksjonsordren.  

    På siden **Planlegg prod.ordre på nytt** definerer du hva som skal planlegges på nytt, og hvordan.  
6.  Velg ett av følgende alternativer i **Planleggingsretning**-feltet.  

    |Alternativ|Beskrivelse|  
    |----------------------------------|---------------------------------------|  
    |**Tilbake**|Beregner operasjonssekvensen bakover fra tidligste mulige sluttdato, definert av forfallsdato og/eller andre tidsplanlagte ordrer, til seneste mulige startdato. **Obs!** Dette standardalternativet er relevant i de fleste tilfeller.|  
    |**Fremover**|Beregner operasjonssekvensen fremover fra tidligste reelle startdato, definert av forfallsdato og/eller andre tidsplanlagte ordrer, til tidligste reelle sluttdato. **Obs!** Dette alternativet er bare relevant for hasteordrer.|  

7.  I **Plan**-feltet velger du om du vil beregne produksjonskrav for produserte varer i produksjonsstykklisten, som følger:  

    |Alternativ|Beskrivelse|  
    |----------------------------------|---------------------------------------|  
    |**Ingen nivåer**|Ikke vurder produksjon på lavere nivå. Dette oppdaterer bare varens tidsplan, på samme måte som å fornye.|  
    |**Ett nivå**|Planlegg for produksjonsbehov på første nivå. Produksjonsordrer på første nivåer kan opprettes.|  
    |**Alle nivåer**|Planlegg for produksjonsbehov på alle nivåer. Produksjonsordrer på alle nivåer kan opprettes.|  

8.  Velg **Ett nivå**, og klikk **OK**-knappen for å planlegge produksjonsorden på nytt og beregne og opprette en ny underliggende produksjonsordre for halvfabrikatet, hvis ikke det er fullstendig tilgjengelig.  

> [!NOTE]  
>  Endringer som er implementert ved hjelp av funksjonen **Planlegg på nytt**, vil etter stor sannsynlighet føre til endringer i produksjonsordrens kapasitetsbehov, og du må derfor kanskje tidsplanlegge operasjoner på nytt senere.  

## <a name="to-refresh-a-production-order"></a>Slik fornyer du en produksjonsordre  
Hvis du har endret produksjonsordrelinjer, komponenter eller rutelinjer, må du i tillegg fornye informasjonen i produksjonsordren. I fremgangsmåten nedenfor beregnes komponentene for en fast planlagt produksjonsordre. Trinnene er de samme for rutelinjer.

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Fast planlagt prod.ordre**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Ny**. Hvis du vil ha mer informasjon, kan du se [Opprette produksjonsordrer](production-how-to-create-production-orders.md).  
3.  Velg handlingen **Oppdater**.
4. På siden **Forny produksjonsordre** velger du ett av følgende valg:

    |Alternativ|Description|  
    |----------------------------------|---------------|---------------------------------------|  
    |**Planleggingsretning**|**Fremover**|Planlegging begynner fra startdatoen og fortsetter fremover til ferdigdatoen. Du må fylle inn startdatoen for å bruke dette alternativet.|  
    ||**Bakover**|Planlegging begynner fra sluttdatoen og fortsetter bakover til startdatoen.|  
    |**Beregn**|**Linjer**|Velg dette feltet for å beregne produksjonsordrelinjer.|  
    ||**Ruter**|Dette feltet har ingen innvirkning på beregningen av produksjonslinjene.|  
    ||**Komponentbehov**|Dette feltet har ingen innvirkning på beregningen av produksjonslinjene.|  
    |**Lager**|**Opprett inngående foresp.**|Dette feltet har ingen innvirkning på beregningen av produksjonslinjene.|  

5. Velg **OK**-knappen for å bekrefte valget. Nå er produksjonsordrelinjene beregnet.

> [!NOTE]  
>  Når du beregner produksjonsordrekomponenter, slettes tidligere endringer i komponentene.

## <a name="see-also"></a>Se også  
[Planlegging](production-planning.md)  
[Definere produksjon](production-configure-production-processes.md)  
[Produksjon](production-manage-manufacturing.md)    
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)   
[Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging](setup-best-practices-supply-planning.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
