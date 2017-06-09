---
title: "Økonomimodulen og kontoplanen| Microsoft-dokumentasjon"
description: "Beskriver økonomimodulen, kontoplanen og kontokategoriene."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 02/14/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 04b94fa9f737765edbb1c93c506b444179b86fcf
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="the-general-ledger-and-the-chart-of-accounts"></a>Økonomimodulen og kontoplanen
Økonomimodulen lagrer dine økonomiske data, og kontoplanen viser kontoene som alle finansposter bokføres til. [!INCLUDE[d365fin](includes/d365fin_md.md)] inneholder en standard kontoplan som er klar til å støtte forretningsvirksomheten din.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Finansoppsett og generelt bokføringsoppsett
Oppsettet av finans er i kjernen av økonomiske prosesser fordi den definerer hvordan du kan legge inn data.  

I vinduet **Finansoppsett** angir du hvordan du håndterer bestemte regnskapssaker i firmaet, for eksempel:  

* Detaljopplysninger om fakturaavrunding  
* Adresseformater  
* Finansrapportering  

I vinduet **Generelt bokføringsoppsett** angir du hvordan du vil definere kombinasjoner av firma- og varebokføringsgrupper. Bokføringsgrupper tilordner enheter som kunder, leverandører, varer, ressurser og salgs- og kjøpsdokumenter til finanskonti. Fyll ut en linje for hver kombinasjon av firma- og varebokføringsgrupper. Hvis du vil ha mer informasjon, kan du se [Oppsett av bokføringsgrupper](finance-posting-groups.md)  

## <a name="the-chart-of-accounts"></a>Kontoplanen
Kontoplanen viser alle finanskontoer. Fra kontoplanen kan du gjøre ting som:  

* Vise rapporter som viser finansposter og saldoer.  
* Lukke resultatregnskapet.  
* Åpne Finanskonto-kortet for å legge til eller endre innstillinger.  
* Vise en liste over bokføringsgrupper som du posterer til kontoen.  

Du kan legge til, endre eller slette finanskontoer. For å unngå avvik kan du imidlertid ikke slette en finanskonto hvis dataene fra den er brukt i kontoplanen.  

## <a name="account-categories"></a>Kontokategorier
Du kan tilpasse strukturen i kontoutskrifter ved å tilordne finanskontoer til kontokategorier.  

Vinduet **Finanskontokategorier** viser dine kategorier og underkategorier og finanskonti som er tilordnet til dem. Du kan opprette nye underkategorier og tilordne disse kategoriene til eksisterende kontoer.  

Du kan opprette en kategorigruppe ved å rykke inn andre underkategorier under en linje i vinduet **Finanskontokategorier**. Dette gjør det enkelt for deg å få en oversikt, fordi hver gruppering viser den totale saldoen. Du kan opprette underkategorier for ulike typer aktiva, og deretter opprette kategorigrupper for anleggsmidler kontra omløpsmidler.  

Du kan angi om kontoene i hver underkategori må inkluderes i bestemte typer rapporter. Kontokategoriene bidra til å definere oppsettet for regnskapsoppgjør.  

Standard saldoutdrag har for eksempel en underkategori for kontanter under gjeldende aktiva. Hvis du vil at saldoutdraget skal ta hensyn til håndkasse og sjekker, kan du:  

1. Legge til to nye underkategorier. Én for håndkassen og én for sjekkontoen.  
2. Angi den ekstra rapportdefinisjonen **Kontantkontoer** for disse underkategoriene.  
3. Rykk inn dem under **Kontanter**-underkategori.  

Neste gang du genererer kontoskjemaer, vil utdraget vise en total saldo for kontanter og to linjer med saldoer for håndkasse og sjekkontoen.  

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Definere eller endre kontoplanen](finance-setup-chart-accounts.md)  
[Kontoskjemaer](finance-account-schedule.md)  

