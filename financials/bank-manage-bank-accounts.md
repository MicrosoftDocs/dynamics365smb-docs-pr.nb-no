---
title: "Håndtere bankkonti| Microsoft-dokumentasjon"
description: "Du må regelmessig avstemme bankposter i Financials med de relaterte banktransaksjonene i bankkontiene."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 20ff1bad076bff8ce07716cfffc2fa5e05605bb2
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="managing-bank-accounts"></a>Håndtere bankkonti
Med jevne mellomrom må du avstemme bankposter i [!INCLUDE[d365fin](includes/d365fin_md.md)] med tilknyttede banktransaksjoner i bankkontoer i banken din, og deretter bokføre saldoen på bankkontoen din. Du kan utføre denne oppgaven som en del av behandling av betalinger, som er representert i et bankkontoutdrag i **Betalingsavstemmingskladd**. Du kan også utføre oppgaven separat fra betalingsbehandlingen, i vinduet **Bankkontoavstemming**, som støtter sjekkposter. I begge tilfellene fyller du ut vinduene ved å importere bankkontoutdraget til [!INCLUDE[d365fin](includes/d365fin_md.md)].

Noen ganger må du overføre beløp mellom bankkonti i [!INCLUDE[d365fin](includes/d365fin_md.md)] for å gjenspeile overføringer i banken. Du utfører denne oppgaven på ulike måter i vinduet **Finanskladd**, avhengig av valutaen for midlene.

Før du kan administrere bankkonti, må du definere hver bankkonto som et bankkort. I tillegg må du definere elektroniske tjenester som du kan bruke for import av bankutdrag og eksport av betalingsfil. Hvis du vil ha mer informasjon, kan du se [Opprette bankkonti](bank-setup-banking.md).

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.

| Hvis du vil | Se |
| --- | --- |
| Avstemme bankkonti i forbindelse med betalingsbehandling i vinduet **Betalingsavstemmingskladd**. |[Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Avstemme bankkonti, inkludert sjekkposter, som en separat oppgave i vinduet **Bankkontoavstemming**. |[Avstemme bankkonti separat](bank-how-reconcile-bank-accounts-separately.md) |
| Bokføre overføringer mellom bankkonti i samme eller ulike valutaer. |[Overføre bankkapital](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a>Se også
[Konfigurere banktjenester](bank-setup-banking.md)  
[Håndtere fordringer](receivables-manage-receivables.md)  
[Administrere skyldige beløp](payables-manage-payables.md)    
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

