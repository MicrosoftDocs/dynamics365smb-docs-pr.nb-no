---
title: "Oversikt over oppgaver for å behandle leverandørgjeld | Microsoft-dokumentasjon"
description: "Gir en oversikt over oppgavene for å behandle leverandørgjeld, for eksempel betale kreditorer eller utligne utgående betalinger mot poster for å lukke fakturaer eller kreditnotaer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9684a91268927a4f1f4d249fef019c8f6ac00325
ms.contentlocale: nb-no
ms.lasthandoff: 07/07/2017


---
# <a name="managing-payables"></a>Administrere skyldige beløp
En stor del av administrasjon av skyldige beløp består av å betale dine leverandører. Du kan bruke funksjoner til å legge til betalingslinjer for forfalte kjøpsfakturaer i vinduet **Utbetalingskladd**. Du kan sende transaksjoner til banken din ved å eksportere flere betalingskladdelinjer til en fil og deretter laste opp filen til banken. Du kan også betale med sjekk, inkludert å overføre sjekker som elektroniske betalinger.

En annen vanlig oppgave er å utligne utgående betalinger mot deres relaterte leverandørposter for å kunne lukke de beslektede kjøpsfakturaene eller kjøpskreditnotaene som betalt. Du kan gjøre dette i vinduet **Betalingsavstemmingskladd** ved å importere en bankkontoutdragsfil for hurtig å registrere betalinger. Betaling brukes til å åpne kunde- eller kundepostoppføringer ved å sammenligne betalingstekst for oppføringsinformasjon. Det finnes ulike måter å se gjennom og endre treff før du bokfører kladden. Du kan velge å lukke alle åpne bankposter relatert til de utlignede postene når du bokfører kladden. Bankkontoen avstemmes automatisk når alle betalinger er utlignet.

Du kan også bruke utgående betalinger manuelt i vinduet **Betalingskladd** eller fra de relaterte leverandørpostene.

Tabellen nedenfor beskriver en sekvens av oppgaver i leverandørgjeld, og har koblinger til emnene som beskriver dem.

| Hvis du vil | Se |
| --- | --- |
| Generere forfalte leverandørbetalinger prioritert i henhold til kontantrabatter og forfalte straffegebyrer. Du kan også eksportere betalingene til en bankfil ved bokføring. |[Foreta betalinger](payables-make-payments.md) |
| Utligne leverandørbetalinger automatisk på ubetalte kjøpsfakturaer ved å importere en bankkontoutdragsfil. |[Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Utligne leverandørbetalinger på ubetalte fakturaer manuelt. |[Avstemme leverandørbetalinger manuelt](payables-how-apply-purchase-transactions-manually.md) |
|Sikre riktig lagerverdisetting ved å tilordne ekstra varekost, for eksempel frakt, fysisk håndtering, forsikring og transport, som du pådrar deg ved innkjøp.|[Bruke varegebyr til å gjøre rede for ekstra handelskostnader](payables-how-assign-item-charges.md)|

## <a name="see-also"></a>Se også
[Innkjøp](purchasing-manage-purchasing.md)  
[Håndtere fordringer](receivables-manage-receivables.md)  
[Bruke varegebyr til å gjøre rede for ekstra handelskostnader](payables-how-assign-item-charges.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

