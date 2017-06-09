---
title: Foreta betalinger Microsoft-dokumentasjon
description: Foreta betalinger
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: f6721c0359b4499a597b349a280afb56818a1f28
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="make-payments"></a>Foreta betalinger
Når du foretar betalinger til leverandører, kan du bokføre de relaterte betalingslinjene i vinduet **Betalingskladd**. Du kan bruke funksjonen **Betalingsforslag – leverandør** til å finne betalinger som har forfalt. Du kan også bruker rapporten **Leverandør – forfallsoversikt** til å få oversikt over betalinger som har forfalt.

Fra betalingskladden kan du skrive ut maskinelle sjekker eller registrere når sjekker skrives. Hvis du velger **Maskinell sjekk** i feltet **Bankbetalingstype**, må eventuelle linjer som representerer sjekker skrives ut før betalingskladden kan bokføres.

Når betalingene er bokført, kan du eksportere dem til en bankfil for opplasting til banken for behandling.

Når betalingene er foretatt i banken, må du utligne dem på deres tilknyttede åpne leverandørposter. Du kan gjøre dette manuelt eller ved å importere en bankkontoutdragsfil og utligne betalingene automatisk. Hvis du vil ha mer informasjon, kan du se [Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.

| Hvis du vil | Se |
| --- | --- |
| Bruke en funksjon til å foreslå leverandørbetalinger i henhold til valgte kriterier som forfallsdato, rabatt arbeidstillatelse og din likviditet. |[Foreslå leverandørbetalinger](payables-how-suggest-vendor-payments.md) |
| Utstede sjekker for betalinger, enten som utskrifter eller maskinelle sjekker. Kansellere sjekker før eller etter bokføring. |[Arbeide med sjekker](payables-how-work-checks.md) |
| Du kan sørge for at at banken bare fjerner validerte sjekker og beløp ved å sende dem en fil som inneholder informasjon om leverandør, sjekk og betaling. |[Eksportere en Positive Pay-fil](finance-how-positive-pay.md) |
|Eksporter betalinger fra vinduet **Utbetalingskladd** til en bankfil som du laster opp til banken for behandling, inkludert EFT (elektronisk pengeoverføring) i Nord-Amerika. |[Fremgangsmåte: Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md)|  

## <a name="see-also"></a>Se også
[Administrere skyldige beløp](payables-manage-payables.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Håndtere fordringer](receivables-manage-receivables.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

