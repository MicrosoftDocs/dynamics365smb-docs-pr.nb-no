---
title: Prosjektrapporter og analyser
description: Se hvilke prosjektrapporter og analyser som er tilgjengelige i standardversjonen av Business Central, slik at du kan holde oversikt over virksomheten.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: ff5294df5cdbeaf0054249f017906bfd60ee4bf7
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216386"
---
# <a name="project-reports-and-analytics-in-business-central"></a>Prosjektrapporter og analyser i Business Central

Prosjektrapportering i [!INCLUDE [prod_short](includes/prod_short.md)] gjør det mulig for prosjekt- og forretningsfolk å få innsikt og statistikk om gjeldende og tidligere prosjektaktiviteter.  

## <a name="reports"></a>Rapporter

Tabellen nedenfor beskriver noen av nøkkelrapportene i prosjektrapportering.

|Rapport |Objekt-ID|Beskrivelse  |
|---------|---------|---------|
|**Prosjektanalyse**|1008|Analyserer prosjektet ved å bruke innstillinger du angir. Du kan for eksempel opprette en rapport som viser deg de budsjetterte prisene, forbruksprisene og fakturerbare prisene, og som deretter sammenligner de tre settene med priser.<br>Bruk en kombinasjon av de tilgjengelige **Beløp**-feltene for å opprette din egen analyse. For hvert felt kan du velge én av de følgende verdiene for priser, kost eller fortjeneste: Estimat, Forbruk, Kontrakt og Fakturert. <br>Velg om valutaen skal angis i Lokal valuta eller Utenlandsk valuta. |
|**Prosjektplanleggingslinjer**|1006|Denne rapporten viser de forskjellige prosjektplanleggings- og prosjektoppgavelinjene, inkludert linjetype, antall, enhet, totale kostnader og så videre.|
|**Prosjekt – etterkalkulasjon**|1009|Sammenligner planlagte beløp og forbruksbeløp for utvalgte prosjekter. Alle linjene i det valgte prosjektet inneholder antall, kostbeløp og linjebeløp. <br>Denne rapporten er ment for avsluttede prosjekter, selv om du kan bruke den når som helst i løpet av et prosjekt.<br>I USA, Canada og Mexico er ikke denne rapporten tilgjengelig. Bruk i stedet rapportene **Faktisk prosjektkost til budsjett (kostnad)** (10210) eller **Faktisk prosjektpris til budsjett (pris)** (10211).|
|**Faktureringsforslag for prosjekt**|1011|Viser en oversikt over alle prosjekter, gruppert etter kunde. Den viser hvor mye kunden allerede er fakturert, og hvor mye som gjenstår å fakturere, det vil si faktureringsforslag. <br>I USA, Canada og Mexico er ikke denne rapporten tilgjengelig. Bruk i stedet rapporten **Faktureringsforslag for prosjektkostnad** (10219).|
|**Prosjekter per kunde**|1012|Viser en oversikt over alle prosjektene, gruppert etter kunde. Den gir deg muligheten til å sammenligne planlagt pris, prosent for ferdiggjørelse, fakturert pris og prosent for fakturert beløp for hver **kunde som skal faktureres**.|
|**Varer per prosjekt** eller **Prosjekter per vare**|1013 eller 1014|En oversikt over de brukte varene i et prosjekt. Avhengig av hvilken rapport du vil bruke til å få en oversikt over de planlagte varene for et prosjekt, kan du angi et tilleggsfilter. Rapporten viser de relevante varene og en akkumulert verdi om kostnadene.|
|**Prosjekt – kontoutdrag**|1007|Med denne rapporten får du en oversikt over de bokførte prosjektoppgavene, for eksempel ressurser og varer. Inneholder detaljert informasjon om de totale kostbeløpene og salgsprisene samt informasjon som gjelder linjerabatter og så videre. Rapporten viser data fra prosjektpostene.|
|**Prosjekt – VIA til Finans**|1010|Viser verdien til varer i arbeid i prosjektene du velger, sammenlignet med beløpet som er bokført i Finans.|




## <a name="tasks"></a>Oppgaver

Følgende artikler beskriver noen av de viktige oppgavene for å analysere tilstanden i virksomheten din:

* [Overvåke prosjektfremdrift og -ytelse](projects-how-monitor-progress-performance.md)  


## <a name="see-also"></a>Se også

[Konfigurere prosjektstyring](projects-setup-projects.md)  
[Prosjektstyring](projects-manage-projects.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
