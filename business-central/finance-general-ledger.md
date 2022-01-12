---
title: Forstå Finans og kontoplanen
description: Beskriver Finans, kontoplanen og kontokategoriene. Bruk siden Finansoppsett til å angi hvordan du håndterer bestemte regnskapssaker i firmaet.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 12/03/2021
ms.author: edupont
ms.openlocfilehash: 2af34c84c7b359d2cae64d19a9aec151e0d9a3bb
ms.sourcegitcommit: 088bb19634f60891a12736c034ab3e86bdb91891
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2021
ms.locfileid: "7928812"
---
# <a name="understanding-the-general-ledger-and-the-chart-of-accounts"></a>Forstå Finans og Kontoplan

Økonomimodulen lagrer dine økonomiske data, og kontoplanen viser kontoene som alle finansposter bokføres til. [!INCLUDE[prod_short](includes/prod_short.md)] inneholder en standard kontoplan som er klar til å støtte forretningsvirksomheten din.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Finansoppsett og generelt bokføringsoppsett

Oppsettet av finans er i kjernen av økonomiske prosesser fordi den definerer hvordan du kan legge inn data.  

På siden **Finansoppsett** angir du hvordan du håndterer bestemte regnskapssaker i firmaet, for eksempel:  

* Detaljopplysninger om fakturaavrunding  
* Adresseformater  
* Finansrapportering  

> [!TIP]
> Siden **Finansoppsett** inneholder generelle felt og felt som er spesifikke for ditt land eller din region. Hvis du ikke er sikker på betydningen av et felt, foreslår vi at du arbeider med regnskapsføreren for å finne ut om det er av relevans for organisasjonen.  

På siden **Generelt bokføringsoppsett** angir du hvordan du vil definere kombinasjoner av firma- og varebokføringsgrupper. Bokføringsgrupper tilordner enheter som kunder, leverandører, varer, ressurser og salgs- og kjøpsdokumenter til finanskonti. Fyll ut en linje for hver kombinasjon av firma- og varebokføringsgrupper. Men du kan også åpne hver linje i et eget bokføringsoppsettskort. Hvis du vil ha mer informasjon, kan du se [Oppsett av bokføringsgrupper](finance-posting-groups.md).  

> [!TIP]
> Hvis du ikke kan se feltene du leter etter, på siden **Generelt bokføringsoppsett**, bruker du det vannrette rullefeltet nederst på siden til å bla til høyre.  

## <a name="the-chart-of-accounts"></a>Kontoplanen

Kontoplanen viser alle finanskontoer. Fra kontoplanen kan du gjøre ting som:  

* Vise rapporter som viser finansposter og saldoer.  
* Lukke resultatregnskapet.  
* Åpne finanskontokortet for å legge til eller endre innstillinger.  
* Vise en liste over bokføringsgrupper som du posterer til kontoen.
* Vise separate debet- og kreditsaldoer for én konto  

Du kan legge til, endre eller slette finanskontoer. For å unngå avvik kan du imidlertid ikke slette en finanskonto hvis dataene fra den er brukt i kontoplanen.  

## <a name="account-categories"></a>Kontokategorier

Du kan tilpasse strukturen i kontoutskrifter ved å tilordne finanskontoer til kontokategorier.  

Siden **Finanskontokategorier** viser kategoriene og underkategoriene dine samt finanskontiene som er tilordnet til dem. Du kan opprette nye underkategorier og tilordne disse kategoriene til eksisterende kontoer.  

Du kan opprette en kategorigruppe ved å rykke inn andre underkategorier under en linje på siden **Finanskontokategorier**. Dette gjør det enkelt for deg å få en oversikt, fordi hver gruppering viser den totale saldoen. Du kan opprette underkategorier for ulike typer aktiva, og deretter opprette kategorigrupper for aktiva kontra omløpsmidler.  

Du kan angi om kontoene i hver underkategori må inkluderes i bestemte typer rapporter. Kontokategoriene bidra til å definere oppsettet for regnskapsoppgjør.  

### <a name="example"></a>Eksempel

Standard saldoutdrag har for eksempel en underkategori for *kontanter* under *gjeldende aktiva*. Du vil at saldoutdraget skal ta hensyn til håndkasse og sjekker, så du utfører følgende trinn:  

1. Legg til to nye underkategorier:

    * en for håndkasse  
    * en for sjekkontoen  
2. Angi den ekstra rapportdefinisjonen **Kontantkontoer** for disse underkategoriene.  
3. Rykk inn dem under **Kontanter**-underkategori.  

Neste gang du genererer kontoskjemaer, vil utdraget vise en total saldo for kontanter og to linjer med saldoer for håndkasse og sjekkontoen.  

## <a name="getting-a-quick-overview"></a>Få en rask oversikt
Kontoplan-siden viser konti i en hierarkisk liste som gir rask tilgang til viktig informasjon for hver konto. Listen er imidlertid statisk, og hvis du har mange konti, må du kanskje rulle litt for å vise informasjon for ulike konti. Hvis du bare vil ha en rask oversikt over det grunnleggende, for eksempel bevegelser og saldoer, er siden **Kontoplanoversikt** et nyttig alternativ. Kolonneoppsettet på siden er nå det samme som du finner på kontoplansiden (det er bare færre av dem), så du trenger ikke å orientere deg på nytt, og du kan vise eller skjule de hierarkiske nivåene for å få en kompakt visning. For at det skal bli enkelt å bytte mellom sidene er siden **Kontoplanoversikt** tilgjengelig fra Kontoplan-siden.

## <a name="access-to-create-and-edit-accounts-and-account-categories"></a>Tilgang til å opprette og redigere konti og kontokategorier

I en liten organisasjon, for eksempel CRONUS-demoselskapet, kan de fleste brukere redigere kontoplanen, unntatt brukere med en gruppemedlemslisens. I større organisasjoner er imidlertid tilgang til å redigere kontoplanen begrenset av roller og tillatelser. Hvis du er administrator eller du har rollen som *Forretningssjef* eller *Regnskapsfører*, kan du kontrollere tillatelsene for alle brukerne for å være sikker på at de riktige personene har tilgang til de relevante tabellene. Hvis du vil ha mer informasjon, kan du se [For å få en oversikt over en brukers tillatelser](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).  

## <a name="see-also"></a>Se også

[Finans](finance.md)  
[Definere eller endre kontoplanen](finance-setup-chart-accounts.md)  
[Forretningsintelligens](bi.md)  
[Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
