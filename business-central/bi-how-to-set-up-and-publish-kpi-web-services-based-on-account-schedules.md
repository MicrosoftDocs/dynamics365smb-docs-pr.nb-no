---
title: Konfigurere og publisere KPI-webtjenester for kontoskjemaer | Microsoft-dokumentasjon
description: "Dette emnet beskriver hvordan du viser kontoskjemaet KPI-data som er basert på bestemte kontoskjemaer."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 9e7adbe575df0b9253ead53ca2a5c782fa27e064
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-and-publish-kpi-web-services-based-on-account-schedules"></a>Konfigurere og publisere KPI-webtjenester basert på kontoskjemaer
I vinduet **Oppsett av KPI-webtjeneste for kontoskjema** definerer du hvordan du vil vise kontoskjemaets KPI-data og hvilke bestemte kontoplaner KPI-ene skal baseres på. Når du velger **Publiser webtjeneste**, legges kontoskjemaets angitte KPI-data til i listen over publiserte webtjenester i vinduet over publiserte webtjenester i vinduet **Webtjenester**.  

## <a name="to-set-up-and-publish-a-kpi-web-service-that-is-based-on-account-schedules"></a>Slik konfigurerer og publiserer du en KPI-webtjeneste som er basert på kontoskjemaer  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Oppsett av KPI-webtjeneste for kontoskjema**, og velg deretter den relaterte koblingen.  
2.  I hurtigfanen **Generelt** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Startdato for prognoseberegnede verdier**|Angi på hvilket tidspunkt prognoseberegnede verdier vises på kontoskjemaets KPI-grafikk.<br /><br /> Prognoserverdiene hentes fra finansbudsjettet som du velger i **Finansbudsjettnavn-feltet**. **Obs!** Hvis du vil hente KPIer som viser prognosetall etter en bestemt dato og faktiske tall før datoen, kan du endre feltet **Bokf. tillatt fra** i vinduet **Finansoppsett**. Hvis du vil ha mer informasjon, kan du se Bokf. tillatt fra.|  
    |**Finansbudsjettnavn**|Angi navnet på finansbudsjettet som gir prognoseverdier til webtjenesten for kontoskjema-KPI.|  
    |**Periode**|Angi perioden som webtjenesten for kontoskjema-KPI er basert på.|  
    |**Vis etter**|Angi hvilket tidsintervall kontoskjemaets KPI vises i.|  
    |**Webtjenestenavn**|Angi navnet på webtjenesten for kontoskjema-KPI.<br /><br /> Dette navnet vil vises i feltet **Tjenestenavn** i vinduet **Webtjenester**.|  

    Angi ett eller flere kontoskjemaer som du vil publisere som en KPI-webtjeneste i samsvar med oppsettet som du lagde i den forrige tabellen.  

3.  På hurtigfanen **Kontoskjemaer** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Kontoskjemanavn**|Angi kontoskjemaet som KPI-webtjenesten er basert på.|  
    |**Beskrivelse av kontoskjema**|Angi beskrivelsen av kontoskjemaet som KPI-webtjenesten er basert på.|  

4.  Gjenta trinn 3 for alle kontoskjemaer som du vil basere webtjenesten for kontoskjema-KPI på.  
5.  Hvis du vil vise eller redigere det valgte kontoskjemaet, velger du **Rediger kontoskjema** på hurtigfanen **Kontoskjema**.  
6.  Hvis du vil vise kontoskjemaets KPI-data som du har definert, velger du **KPI-webtjeneste for kontoskjema**.  
7.  Hvis du vil publisere KPI-webtjenesten for kontoskjemaet, velger du **Publiserer webtjeneste**. Webtjenesten er lagt til listen over publiserte webtjenester i **Webtjenester**-vinduet.  

> [!NOTE]  
>  Du kan også publisere KPI-webtjenesten ved å velge vindusobjektet **Oppsett av KPI-webtjeneste for kontoskjema** fra **Webtjenester**-vinduet. Hvis du vil ha mer informasjon, kan du se [Publisere en webtjeneste](across-how-publish-web-service.md).  

## <a name="see-also"></a>Se også  
[Forretningsintelligens](bi.md)  
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Finans og kontoplanen](finance-general-ledger.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

