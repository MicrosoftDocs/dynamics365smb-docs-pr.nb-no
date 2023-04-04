---
title: Feilsøk automatiserte arbeidsflyter
description: Lær hvordan du feilsøker tilkoblingen mellom Business Central og Power Automate når du bygger en automatisert arbeidsflyt.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions, Power Automate,'
ms.date: 08/04/2022
ms.author: edupont
---

# Feilsøk automatiserte arbeidsflyter for [!INCLUDE[prod_short](includes/prod_short.md)]

Når du kobler [!INCLUDE [prod_short](includes/prod_short.md)] til Power Automate for å opprette automatiserte arbeidsflyter, kan du støte på feilmeldinger. Denne artikkelen gir forslag til problemer som gjentar seg.

## Flyten kjøres ikke på alle poster som er opprettet eller endret

### Problem

Hvis en hendelse oppretter eller endrer mange poster, kjøres ikke flyten i noen av eller alle postene.

### Mulig årsak

For øyeblikket er det en grense for hvor mange poster flyten kan behandle. Hvis flere enn 100 poster opprettes eller endres innen 30 sekunder, blir flyten ikke utløst.

> [!NOTE]
> For utviklere utføres flytutløsing via webhook-varsler, og denne begrensningen skyldes måten Business Central-koblingen håndterer `collection`-varslinger på. Finn ut mer under [Arbeid med Webhook i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/api-reference/v2.0/dynamics-subscriptions#notes-for-power-automate-flows) i hjelpen for utviklere og administrasjon.

## Feilen Finner ikke enhetssettet

### Problem

Når du oppretter en ny Power Automate-flyt ved hjelp av en [!INCLUDE[prod_short](includes/prod_short.md)]-godkjenningsutløser, som *Det bes om godkjenning av et kjøpsdokument*, kan det vises en feilmelding som ligner på denne:

`Entity set not found: \<name\>`

Plassholderen `\<name\>` er navnet på tjenesten til den manglende nettjenesten, for eksempel *workflowWebhookSubscriptions* eller *workflowPurchaseDocumentLines*.

### Mulig årsak

Bruk av Power Automate for godkjenninger krever at visse side- og codeunit-objekter er publisert som nettjenester. Som standard publiseres de fleste av de nødvendige objektene som nettjenester. I enkelte tilfeller kan miljøet ha blitt tilpasset slik at disse objektene ikke lenger er publisert.

### Fast

Gå til siden **Nettjenester**, og kontroller at følgende objekter er publisert som nettjenester. Det skal være en oppføring i listen for hvert objekt med merking for **Publisert**.  

| Objekttype | Objekt-ID | Objektnavn | Tjenestenavn |
|--|--|--|--|
| Kodeenhet | 1544 | WorkflowWebhookSubscription | WorkflowActionResponse |
| Side | 6408 | workflowCustomers | workflowCustomers |
| Side | 6406 | workflowGenJournalBatches | workflowGenJournalBatches |
| Side | 6407 | workflowGenJournalLines | workflowGenJournalLines |
| Side | 6409 | workflowItems | workflowItems |
| Side | 6405 | Enhet for kjøpsdokumentlinje | workflowPurchaseDocumentLines |
| Side | 6404 | workflowPurchaseDocuments | workflowPurchaseDocuments |
| Side | 6403 | Enhet for salgsdokumentlinje | workflowSalesDocumentLines |
| Side | 6402 | workflowSalesDocuments | workflowSalesDocuments |
| Side | 6410 | workflowVendors | workflowVendors |
| Side | 831 | workflowWebhookSubscriptions | workflowWebhookSubscriptions |

> [!NOTE]
> Verdien **Tjenestenavn** må være nøyaktig som vist i tabellen. Ikke endre eller oversett tjenestenavnet.

Finn ut mer om publisering av nettjenester under [Publisere en nettjeneste](across-how-publish-web-service.md).

## Se relatert opplæring på [Microsoft Learn](/learn/modules/use-power-automate/).

## Se også

[Bruk Power Automate-flyter i [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md)  
[Arbeidsflyt](across-workflow.md)  
[Konfigurer automatiserte arbeidsflyter](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Slå på direkteflyter](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  
[Administrer Power Automate-flyter](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
