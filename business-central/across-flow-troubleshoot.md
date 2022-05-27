---
title: Feilsøk automatiserte arbeidsflyter
description: Lær hvordan du feilsøker tilkoblingen mellom Business Central og Power Automate når du bygger en automatisert arbeidsflyt.
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/12/2022
ms.author: edupont
author: jswymer
ms.openlocfilehash: b8fff95ced93e7ee2a3112969f45525532b19445
ms.sourcegitcommit: e86f0bd15604c2fb327e3182929c44a4172790c7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/20/2022
ms.locfileid: "8786199"
---
# <a name="troubleshoot-your-prod_short-automated-workflows"></a>Feilsøk automatiserte arbeidsflyter for [!INCLUDE[prod_short](includes/prod_short.md)]

Når du kobler [!INCLUDE [prod_short](includes/prod_short.md)] til Power Automate for å opprette automatiserte arbeidsflyter, kan du støte på feilmeldinger. Denne artikkelen gir forslag til problemer som gjentar seg ofte.

## <a name="flow-doesnt-run-on-all-records-created-or-changed"></a>Flyten kjøres ikke på alle poster som er opprettet eller endret

### <a name="problem"></a>Problem

Hvis en hendelse oppretter eller endrer mange poster, kjøres ikke flyten i noen av eller alle postene.

### <a name="possible-cause"></a>Mulig årsak

For øyeblikket er det en grense for hvor mange poster flyten kan behandle. Hvis flere enn 100 poster opprettes eller endres innen 30 sekunder, blir flyten ikke utløst.

> [!NOTE]
> For utviklere utføres flytutløsing via webhook-varsler, og denne begrensningen skyldes måten Business Central-koblingen håndterer `collection`-varslinger på. Hvis du vil ha mer informasjon, kan du se [Arbeid med Webhook i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/api-reference/v2.0/dynamics-subscriptions#notes-for-power-automate-flows) i hjelpen for utviklere og administrasjon.

## <a name="entity-set-not-found-error"></a>Feilen Finner ikke enhetssettet

### <a name="problem"></a>Problem

Når du oppretter en ny Power Automate-flyt ved hjelp av en [!INCLUDE[prod_short](includes/prod_short.md)]-godkjenningsutløser, som *Det bes om godkjenning av et kjøpsdokument*, kan det vises en feilmelding som ligner på denne:

`Entity set not found: \<name\>`

Plassholderen `\<name\>` er navnet på tjenesten til den manglende nettjenesten, for eksempel *workflowWebhookSubscriptions* eller *workflowPurchaseDocumentLines*.

### <a name="possible-cause"></a>Mulig årsak

Bruk av Power Automate for godkjenninger krever at visse side- og codeunit-objekter publiseres som nettjenester. Som standard publiseres de fleste av de nødvendige objektene som nettjenester for deg. I enkelte tilfeller kan miljøet ha blitt tilpasset slik at disse objektene ikke lenger er publisert.

### <a name="fix"></a>Løsning

Gå til siden **Nettjenester**, og kontroller at følgende objekter er publisert som nettjenester. Det skal være en oppføring i listen for hvert objekt med merking for **Publisert**.  

|Objekttype|Objekt-ID|Objektnavn|Tjenestenavn|
|-----------|---------|-----------|------------|
|Kodeenhet|  1544    |WorkflowWebhookSubscription|WorkflowActionResponse|
|Side|  6408|   workflowCustomers|  workflowCustomers|
|Side   |6406   |workflowGenJournalBatches| workflowGenJournalBatches|
|Side   |6407   |workflowGenJournalLines|workflowGenJournalLines|
|Side   |6409   |workflowItems| workflowItems|
|Side   |6405   |Enhet for kjøpsdokumentlinje|workflowPurchaseDocumentLines|
|Side|  6404    |workflowPurchaseDocuments| workflowPurchaseDocuments|
|Side|  6403    |Enhet for salgsdokumentlinje |workflowSalesDocumentLines|
|Side|  6402|   workflowSalesDocuments| workflowSalesDocuments|
|Side|  6410    |workflowVendors|   workflowVendors|
|Side|  831 |workflowWebhookSubscriptions|  workflowWebhookSubscriptions|

> [!NOTE]
> Verdien **Tjenestenavn** må være nøyaktig som vist i tabellen. Ikke endre eller oversett tjenestenavnet.

Hvis du vil ha mer informasjon om publisering av webtjenester, kan du se [Publisere en webtjeneste](across-how-publish-web-service.md).

## <a name="see-also"></a>Se også

[Bruk [!INCLUDE[prod_short](includes/prod_short.md)] i en automatisk arbeidsflyt](across-how-use-financials-data-source-flow.md)  
[Arbeidsflyt](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]