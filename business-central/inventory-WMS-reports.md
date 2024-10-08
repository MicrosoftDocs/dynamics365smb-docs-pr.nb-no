---
title: Lager og lagerrapporter og analyse
description: 'Se hvilke beholdnings- og lagerrapporter og analyser som er tilgjengelige i standardversjonen av Business Central, slik at du kan holde oversikt over virksomheten.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: reporting
ms.search.form: 'Report_707, Report_716, Report_813, Report_1001, Report_5807, Report_5808, Report_5809, Report_7313, Report_7319, Report_7320'
ms.date: 03/21/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="inventory-and-warehouse-reports-and-analytics"></a>Lager og lagerrapporter og analyse

Beholdnings- og lagerrapportering i [!INCLUDE [prod_short](includes/prod_short.md)] gjør det mulig for lager- og forretningsfolk å få innsikt og statistikk om gjeldende og tidligere beholdnings- og lageraktiviteter.  

## <a name="reports"></a>Rapporter

[!INCLUDE [inventory_WMS_reports](includes/inventory-WMS-reports-include.md)]

## <a name="tasks"></a>Oppgaver

Følgende artikler beskriver noen av de viktige oppgavene for å analysere tilstanden i virksomheten din:

* [Opprett analyserapporter](bi-how-create-analysis-views-reports.md)  
* [Vis tilgjengeligheten av varer](inventory-how-availability-overview.md)

## <a name="print-and-scan-barcodes"></a>Skriv ut og skann strekkoder

Bruk av strekkoder kan bidra til å effektivisere inngående, utgående og interne lagerprosesser. 

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

Når du har installert appen, kan du bruke handlingen **Skriv ut etikett** til å skrive ut 1D- og 2D-strekkoder fra sidene som er oppført i tabellen nedenfor.

|Side  |Strekkoder for feltverdier kan omfatte  |
|---------|---------|
|Varer, varekort     |Varenr., Beskrivelse og GTIN         |
|Varereferanseliste, Varereferanse     |Varenr., Beskrivelse, Enhet og Referansenr.         |
|Informasjonsoversikt for partinummer, Partinr.etikett     |Varenr., Beskrivelse og Partinummer       |
|Serienr.etikett     |Nr., Beskrivelse og Serienummer         |

> [!NOTE]
> Noen skrivere og strekkode/QR-kodeformater krever en spesifikk implementering. Du må kanskje laste opp en annen Word-mal eller klone rapporten for å opprette din egen tilpassede versjon.


## <a name="explore-inventory-reports-with-report-explorer"></a>Utforske lagerrapporter med Rapportutforsker

Hvis du vil ha en oversikt over rapportene som er tilgjengelige for lager, velger du **Alle rapporter** på startsiden. Denne handlingen åpner rolleutforskeren, som er filtrert etter funksjonene i alternativet **Rapport og analyse**. Under overskriften **Salg og markedsføring** velger du **Utforsk**.

:::image type="content" source="media/report-explorer-sales.png" alt-text="Eksempel på rapporter i finansrollesenteret." lightbox="media/report-explorer-sales.png":::

Hvis du vil finne ut mer, kan du gå til [Finn rapporter med rolleutforskeren](ui-role-explorer.md).


## <a name="see-also"></a>Se også

[Ad hoc-analyse av lagerdata](ad-hoc-analysis-inventory.md)  
[Oversikt over lageranalyse](inventory-analytics-overview.md)   
[Definere lager](inventory-setup-inventory.md)  
[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)  
[Oversikt over lagerstyring](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
