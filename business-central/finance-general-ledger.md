---
title: Informasjon om Finans og kontoplan | Microsoft dokumenter
description: Beskriver Finans, kontoplanen og kontokategoriene.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 1c5fda0c8cd063e784ec44448b040a298bfeaf2f
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="understanding-the-general-ledger-and-the-coa"></a>Forstå Finans og kontoplanen
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
* Vise separate debet- og kreditsaldoer for én konto  

Du kan legge til, endre eller slette finanskontoer. For å unngå avvik kan du imidlertid ikke slette en finanskonto hvis dataene fra den er brukt i kontoplanen.  

## <a name="account-categories"></a>Kontokategorier
Du kan tilpasse strukturen i kontoutskrifter ved å tilordne finanskontoer til kontokategorier.  

Vinduet **Finanskontokategorier** viser dine kategorier og underkategorier og finanskonti som er tilordnet til dem. Du kan opprette nye underkategorier og tilordne disse kategoriene til eksisterende kontoer.  

Du kan opprette en kategorigruppe ved å rykke inn andre underkategorier under en linje i vinduet **Finanskontokategorier**. Dette gjør det enkelt for deg å få en oversikt, fordi hver gruppering viser den totale saldoen. Du kan opprette underkategorier for ulike typer aktiva, og deretter opprette kategorigrupper for aktiva kontra omløpsmidler.  

Du kan angi om kontoene i hver underkategori må inkluderes i bestemte typer rapporter. Kontokategoriene bidra til å definere oppsettet for regnskapsoppgjør.  

Standard saldoutdrag har for eksempel en underkategori for kontanter under gjeldende aktiva. Hvis du vil at saldoutdraget skal ta hensyn til håndkasse og sjekker, kan du:  

1. Legge til to nye underkategorier. Én for håndkassen og én for sjekkontoen.  
2. Angi den ekstra rapportdefinisjonen **Kontantkontoer** for disse underkategoriene.  
3. Rykk inn dem under **Kontanter**-underkategori.  

Neste gang du genererer kontoskjemaer, vil utdraget vise en total saldo for kontanter og to linjer med saldoer for håndkasse og sjekkontoen.  

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Definere eller endre kontoplanen](finance-setup-chart-accounts.md)  
[Forretningsintelligens](bi.md)  

