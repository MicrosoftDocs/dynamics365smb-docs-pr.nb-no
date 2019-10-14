---
title: Håndtere bankkonti| Microsoft-dokumentasjon
description: Du må regelmessig avstemme bankposter med de relaterte banktransaksjonene i bankkontiene.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 9e5fe99fe822ca94758a3030659bf484f917fcaa
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308383"
---
# <a name="managing-bank-accounts"></a>Håndtere bankkonti
Med jevne mellomrom må du avstemme bankposter i [!INCLUDE[d365fin](includes/d365fin_md.md)] med tilknyttede banktransaksjoner i bankkontoer i banken din, og deretter bokføre saldoen på bankkontoen din. Du kan utføre denne oppgaven som en del av behandling av betalinger, som er representert i et bankkontoutdrag i **Betalingsavstemmingskladd**. Alternativt kan du utføre oppgaven separat fra betalingsbehandlingen på **Bankkontoavstemming**-siden der du avstemmer bankekontoutdragslinjene i ruten til venstre med de interne bankkontopostene i den høyre ruten. På begge sidene kan du fylle ut bankkontoutdragsinformasjon ved å importere en fil eller feed, og du kan bruke automatiske avstemmingsforslag.

> [!NOTE]  
> I nord-amerikanske versjoner kan du også utføre bankavstemming på **Bankavstemmingsforslag**-siden, som er mer egnet for sjekker og innskudd, men tilbyr ikke import av filer med bankkontoutdrag. Hvis du vil bruke denne siden i stedet for **Bankkontoavstemming**-siden, fjerner du avmerkingen for feltet **Bankavstemming med automatisk samsvar** på siden **Finansoppsett**. Hvis du vil ha mer informasjon, kan du se delen Avstemme bankkontoer under lokal funksjonalitet for USA.

Noen ganger må du overføre beløp mellom bankkonti i [!INCLUDE[d365fin](includes/d365fin_md.md)] for å gjenspeile overføringer i banken. Du utfører denne oppgaven på ulike måter på siden **Finanskladd**, avhengig av valutaen for midlene.

Før du kan administrere bankkonti, må du definere hver bankkonto som et bankkort. I tillegg må du definere elektroniske tjenester som du kan bruke for import av bankutdrag og eksport av betalingsfil. Hvis du vil ha mer informasjon, kan du se [Opprette bankkonti](bank-setup-banking.md).

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.

| Hvis du vil | Se |
| --- | --- |
| Avstemme bankkonti i forbindelse med betalingsbehandling på siden **Betalingsavstemmingskladd**. |[Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Avstemme bankkonti, inkludert sjekkposter, som en separat oppgave på siden **Bankkontoavstemming**. |[Avstemme bankkonti separat](bank-how-reconcile-bank-accounts-separately.md) |
| Bokføre overføringer mellom bankkonti i samme eller ulike valutaer. |[Overføre bankkapital](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a>Se også
[Konfigurere banktjenester](bank-setup-banking.md)  
[Håndtere fordringer](receivables-manage-receivables.md)  
[Administrere skyldige beløp](payables-manage-payables.md)    
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 
