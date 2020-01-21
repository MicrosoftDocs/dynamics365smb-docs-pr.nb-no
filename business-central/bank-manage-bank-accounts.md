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
ms.date: 01/10/2020
ms.author: sgroespe
ms.openlocfilehash: 0d1a38468f5d07a1170027bc728ba16996f2b782
ms.sourcegitcommit: 2f741f442226b8be74586e355f283f365e43220f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/10/2020
ms.locfileid: "2947240"
---
# <a name="reconciling-bank-accounts"></a>Avstemme bankkonter
En bankavstemming bør fullføres med jevne mellomrom for alle bankkontoene for å sikre at firmaets kontantposter er riktige. Dette gjør du ved å sammenligne og utligne poster i de interne bankkontoene med banktransaksjoner i banken, og deretter bokføre saldoene på de interne bankkontoene for å gjøre totaler tilgjengelige for finansledere. Bankavstemming er også en praktisk måte å oppdage og løse manglende betalinger og bokføringsfeil.

Du kan utføre oppgaven på **Bankkontoavstemming**-siden der du avstemmer bankekontoutdragslinjene i ruten til venstre med de interne bankkontopostene i den høyre ruten. Du kan også utføre denne oppgaven på siden **Betalingsavstemmingskladd** som en del av behandling av betalinger, som er representert i et bankkontoutdrag. På begge sidene kan du fylle ut bankkontoutdragsinformasjon ved å importere en fil eller feed, og du kan bruke automatiske avstemmingsforslag.

> [!NOTE]  
> I nord-amerikanske versjoner kan du også utføre bankavstemming på **Bankavstemmingsforslag**-siden, som er mer egnet for sjekker og innskudd, men tilbyr ikke import av filer med bankkontoutdrag. Hvis du vil bruke denne siden i stedet for **Bankkontoavstemming**-siden, fjerner du avmerkingen for feltet **Bankavstemming med automatisk samsvar** på siden **Finansoppsett**. Hvis du vil ha mer informasjon, kan du se delen Avstemme bankkontoer under lokal funksjonalitet for USA.

Før du kan administrere bankkontoer i [!INCLUDE[d365fin](includes/d365fin_md.md)], må du definere hver bankkonto som et bankkort. I tillegg må du definere elektroniske tjenester som du kan bruke for import av bankutdrag og eksport av betalingsfil. Hvis du vil ha mer informasjon, kan du se [Opprette bankkonti](bank-setup-banking.md).

Tabellen nedenfor beskriver en sekvens av oppgaver og har koblinger til emnene som beskriver dem.

| Hvis du vil | Se |
| --- | --- |
| Du avstemmer bankkontoer som en separat oppgave på siden **Bankkontoavstemming**. |[Avstemme bankkontoer](bank-how-reconcile-bank-accounts-separately.md) |
| Avstemme bankkonti i forbindelse med betalingsbehandling på siden **Betalingsavstemmingskladd**. |[Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md) |

## <a name="see-related-training-at-microsoft-learnlearnpathsreconcile-bank-accounts-dynamics-365-business-central"></a>Se relatert opplæring på [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)

## <a name="see-also"></a>Se også
[Konfigurere banktjenester](bank-setup-banking.md)  
[Overføre bankkapital](bank-how-transfer-bank-funds.md)  
[Håndtere fordringer](receivables-manage-receivables.md)  
[Administrere skyldige beløp](payables-manage-payables.md)    
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)
