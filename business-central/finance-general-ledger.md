---
title: Informasjon om Finans og kontoplan | Microsoft dokumenter
description: Beskriver Finans, kontoplanen og kontokategoriene.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f242bce26f55fe446ac8dc96335a8da835dd259c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774008"
---
# <a name="understanding-the-general-ledger-and-the-coa"></a>Forstå Finans og kontoplanen

Økonomimodulen lagrer dine økonomiske data, og kontoplanen viser kontoene som alle finansposter bokføres til. [!INCLUDE[prod_short](includes/prod_short.md)] inneholder en standard kontoplan som er klar til å støtte forretningsvirksomheten din.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Finansoppsett og generelt bokføringsoppsett

Oppsettet av finans er i kjernen av økonomiske prosesser fordi den definerer hvordan du kan legge inn data.  

På siden **Finansoppsett** angir du hvordan du håndterer bestemte regnskapssaker i firmaet, for eksempel:  

* Detaljopplysninger om fakturaavrunding  
* Adresseformater  
* Finansrapportering  

På siden **Generelt bokføringsoppsett** angir du hvordan du vil definere kombinasjoner av firma- og varebokføringsgrupper. Bokføringsgrupper tilordner enheter som kunder, leverandører, varer, ressurser og salgs- og kjøpsdokumenter til finanskonti. Fyll ut en linje for hver kombinasjon av firma- og varebokføringsgrupper. Hvis du vil ha mer informasjon, kan du se [Oppsett av bokføringsgrupper](finance-posting-groups.md).  

> [!TIP]
> Siden **Finansoppsett** inneholder generelle felt og felt som er spesifikke for ditt land eller din region. Hvis du ikke er sikker på betydningen av et felt, foreslår vi at du arbeider med regnskapsføreren for å finne ut om det er av relevans for organisasjonen.  

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

Siden **Finanskontokategorier** viser dine kategorier og underkategorier og finanskonti som er tilordnet til dem. Du kan opprette nye underkategorier og tilordne disse kategoriene til eksisterende kontoer.  

Du kan opprette en kategorigruppe ved å rykke inn andre underkategorier under en linje på siden **Finanskontokategorier**. Dette gjør det enkelt for deg å få en oversikt, fordi hver gruppering viser den totale saldoen. Du kan opprette underkategorier for ulike typer aktiva, og deretter opprette kategorigrupper for aktiva kontra omløpsmidler.  

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


[!INCLUDE[footer-include](includes/footer-banner.md)]