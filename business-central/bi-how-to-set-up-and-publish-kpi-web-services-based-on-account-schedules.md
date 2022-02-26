---
title: Konfigurere og publisere KPI-nettjenester for kontoskjemaer
description: Dette emnet beskriver hvordan du viser kontoskjemaet KPI-data som er basert på bestemte kontoskjemaer.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/15/2021
ms.author: bholtorf
ms.openlocfilehash: b224ea5e9bb2d0f53ce41c2dac66a1686dd5a90b
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6437004"
---
# <a name="set-up-and-publish-kpi-web-services-based-on-account-schedules"></a>Konfigurere og publisere KPI-webtjenester basert på kontoskjemaer
På siden **Oppsett av KPI-webtjeneste for kontoskjema** definerer du hvordan du vil vise kontoskjemaets KPI-data og hvilke bestemte kontoplaner KPI-ene skal baseres på. Når du velger **Publiser webtjeneste**, legges kontoskjemaets angitte KPI-data til i listen over publiserte webtjenester i vinduet over publiserte webtjenester på siden **Webtjenester**.  

> [!NOTE]
> Når du bruker denne nettjenesten, tas ikke avslutningsdatoer med i datasettet. Dermed kan du bruke filtre i Power BI til å analysere ulike tidsperioder.

## <a name="to-set-up-and-publish-a-kpi-web-service-that-is-based-on-account-schedules"></a>Slik konfigurerer og publiserer du en KPI-webtjeneste som er basert på kontoskjemaer  
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Oppsett av KPI-nettjeneste for kontoskjema**, og velg deretter den relaterte koblingen.  
2.  I hurtigfanen **Generelt** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Startdato for prognoseberegnede verdier**|Angi på hvilket tidspunkt prognoseberegnede verdier vises på kontoskjemaets KPI-grafikk.<br /><br /> Prognoserverdiene hentes fra finansbudsjettet som du velger i **Finansbudsjettnavn-feltet**. **Obs!** Hvis du vil hente KPIer som viser prognosetall etter en bestemt dato og faktiske tall før datoen, kan du endre feltet **Bokf. tillatt fra** på siden **Finansoppsett**. Hvis du vil ha mer informasjon, kan du se Bokf. tillatt fra.|  
    |**Finansbudsjettnavn**|Angi navnet på finansbudsjettet som gir prognoseverdier til webtjenesten for kontoskjema-KPI.|  
    |**Periode**|Angi perioden som webtjenesten for kontoskjema-KPI er basert på.|  
    |**Vis etter**|Angi hvilket tidsintervall kontoskjemaets KPI vises i.|  
    |**Webtjenestenavn**|Angi navnet på webtjenesten for kontoskjema-KPI.<br /><br /> Dette navnet vil vises i feltet **Tjenestenavn** på siden **Webtjenester**.|  

    Angi ett eller flere kontoskjemaer som du vil publisere som en KPI-webtjeneste i samsvar med oppsettet som du lagde i den forrige tabellen.  

3.  På hurtigfanen **Kontoskjemaer** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Kontoskjemanavn**|Angi kontoskjemaet som KPI-webtjenesten er basert på.|  
    |**Beskrivelse av kontoskjema**|Angi beskrivelsen av kontoskjemaet som KPI-webtjenesten er basert på.|  

4.  Gjenta trinn 3 for alle kontoskjemaer som du vil basere webtjenesten for kontoskjema-KPI på.  
5.  Hvis du vil vise eller redigere det valgte kontoskjemaet, velger du **Rediger kontoskjema** på hurtigfanen **Kontoskjema**.  
6.  Hvis du vil vise kontoskjemaets KPI-data som du har definert, velger du **KPI-webtjeneste for kontoskjema**.  
7.  Hvis du vil publisere KPI-webtjenesten for kontoskjemaet, velger du **Publiserer webtjeneste**. Webtjenesten er lagt til listen over publiserte webtjenester på **Webtjenester**-siden.  

> [!NOTE]  
>  Du kan også publisere KPI-webtjenesten ved å velge sideobjektet **Oppsett av KPI-webtjeneste for kontoskjema** fra **Webtjenester**-siden. Hvis du vil ha mer informasjon, kan du se [Publisere en webtjeneste](across-how-publish-web-service.md).  

## <a name="see-also"></a>Se også  
[Forretningsintelligens](bi.md)  
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Finans og kontoplanen](finance-general-ledger.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]