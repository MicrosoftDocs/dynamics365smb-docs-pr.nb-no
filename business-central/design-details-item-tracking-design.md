---
title: Designdetaljer – Varesporingsutforming
description: Dette emnet beskriver utformingen bak varesporing i Business Central etter hvert som de er modne for produktversjoner.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, item, tracking, tracing'
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-item-tracking-design"></a><a name="design-details-item-tracking-design"></a>Designdetaljer: Varesporingsutforming

Varesporing i [!INCLUDE[prod_short](includes/prod_short.md)] startet med [!INCLUDE [navnow_md](includes/navnow_md.md)]. Varesporingsfunksjonaliteten er i en separat objektstruktur med intrikate koblinger til bokførte dokumenter og vareposter, og den er integrert med reservasjonssystemet, som håndterer reservasjons-, ordresporings- og handlingsmeldinger. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Reservasjon, ordresporing og handlingsmeldinger](design-details-reservation-order-tracking-and-action-messaging.md) i designdetaljene for Forsyningsplanlegging.  

Denne utformingen omfatter varesporingsposter i samlede tilgjengelighetsberegninger i hele systemet, inkludert planlegging, produksjon og lager. Serie- og partinumre brukes for vareposter for å sikre enkel tilgang til historiske data for varesporingsformål. Med lanseringsbølge 1 for 2021 omfatter varesporing i [!INCLUDE [prod_short](includes/prod_short.md)] pakkenumre.  

Med tilføyelsen av serie-, parti- og pakkenumre håndterer reservasjonssystemet permanente vareattributter samtidig som det håndterer uregelmessige koblinger mellom forsyning og behov i form av sporingsposter og reservasjonsposter. Et annet ulikt kjennetegn på serie- eller partinumre sammenlignet med vanlige reservasjonsdata, er at de kan bokføres delvis eller fullstendig. **Reservasjonspost**-tabellen (T337) fungerer derfor nå med den tilknyttede **Sporingsspesifikasjon**-tabellen (T336), som behandler og viser summering på tvers av aktive og bokførte varesporingsantall. Hvis du vil ha mer informasjon, se [Designdetaljer: Aktive kontra historiske varesporingsposter](design-details-active-versus-historic-item-tracking-entries.md).  

Diagrammet nedenfor gir en oversikt over utformingen av varesporingsfunksjonaliteten i [!INCLUDE[prod_short](includes/prod_short.md)].  

![Eksempel på varesporingsflyt.](media/design_details_item_tracking_design.png "Eksempel på varesporingsflyt")  

Hovedbokføringsobjektet er omformet slik at det kan håndtere den unike underklassifiseringen av en dokumentlinje i form av serie- eller partinumre, og spesielle relasjonstabeller er lagt til for å opprette én-til-mange-relasjoner mellom bokførte dokumenter og de delte varepostene og verdipostene.  

Kodeenhet 22, **Varekld. – Posteringslinje**, deler nå posteringen i henhold til varesporingsnumrene som er angitt på dokumentlinjen. Hvert unike varesporingsnummer på linjen, oppretter sin egen varepost for varen. Dette betyr at koblingen fra den bokførte dokumentlinjen til de tilknyttede varepostene nå er en én-til-mange-relasjon. Denne relasjonen håndteres av følgende relasjonstabeller for varesporing.  

|Felt|Beskrivelse|  
|---------------|---------------------------------------|  
|**Vareposttilknytning** (T6507)|Knytter leverte eller mottatte linjer til vareposter|  
|**Verdiposttilknytning** (T6508)|Knytter fakturerte linjer til verdiposter|  

Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Bokføringsstruktur for varesporing](design-details-item-tracking-posting-structure.md).  

## <a name="see-also"></a><a name="see-also"></a>Se også

[Designdetaljer: Varesporing](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]  
