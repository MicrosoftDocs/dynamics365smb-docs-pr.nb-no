---
title: Koble dataene med Power Automate | Microsoft Docs
description: Du kan gjøre Business Central-dataene tilgjengelige som en datakilde og angi en OData-URL-adresse til webtjenestene dine for å utvikle automatisk arbeidsflyt.
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions
ms.date: 07/27/2021
ms.author: edupont
author: jswymer
ms.openlocfilehash: 62718df1c80cb419501b72bcbdb6d7a6f9f18402
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2022
ms.locfileid: "8518470"
---
# <a name="use-prod_short-in-an-automated-workflow"></a>Bruk [!INCLUDE[prod_short](includes/prod_short.md)] i en automatisk arbeidsflyt

Du kan bruke dine [!INCLUDE[prod_short](includes/prod_short.md)]-data som en del av en arbeidsflyt i Microsoft Power Automate.

> [!NOTE]
> I tillegg til Power Automate kan du bruke arbeidsflytfunksjonaliteten i [!INCLUDE[prod_short](includes/prod_short.md)]. Legg merke til at selv om de er to separate arbeidsflytsystemer, legges en arbeidsflytmal som du oppretter med Power Automate, til i listen over arbeidsflyter i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Arbeidsflyt](across-workflow.md).  

> [!NOTE]  
> Du må ha en gyldig konto med [!INCLUDE[prod_short](includes/prod_short.md)] og med Power Automate.  

## <a name="add-prod_short-as-a-data-source-in-power-automate"></a>Legg til [!INCLUDE[prod_short](includes/prod_short.md)] som en datakilde i Power Automate

1. I leseren, kan du gå til [flow.microsoft.com](https://flow.microsoft.com), og deretter logge på.
2. Velg **Mine flyter** fra båndet øverst på siden.
3. Du kan opprette en flyt på tre måter: **Start fra mal**, **Begynn med tom** og **Start fra en kobling**. En mal er en forhåndsdefinert flyt som er opprettet for deg. Hvis du vil bruke en mal, velger du den og oppretter en kobling for hver tjeneste malen bruker. Med alternativene **Begynn med tom** og **Start fra en kobling** kan du opprette en ny flyt fullstendig fra grunnen av.
4. Når du skal opprette fra en tom, går du til siden **Mine flyter** og velger alternativene **Opprett fra tom** og **Automatisk flyt**.
5. Søk etter **Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]** connector.
6. Definer et navn og velg utløseren du vil bruke for flyten.
7. Fra listen over tilgjengelige utløsere velger du én av de tilgjengelige [!INCLUDE[prod_short](includes/prod_short.md)]-utløserne:  

    - *Det bes om godkjenning av en leverandør*  
    - *Det bes om godkjenning av en finanskladdelinje* 
    - *Når en post slettes*
    - *Når en post endres*
    - *Når en post opprettes*
    - *Når en post endres*
    - *Det bes om godkjenning av en finanskladd* 
    - *Det bes om godkjenning av en kunde*
    - *Det bes om godkjenning av en vare*
    - *Det bes om godkjenning av et kjøpsdokument*
    - *Det bes om godkjenning av et salgsdokument*

8. Power Automate ber deg om å velge et miljø eller selskap i din [!INCLUDE[prod_short](includes/prod_short.md)]-leier, i tillegg til eventuelle forhold i dataene du vil lytte til.

    > [!NOTE]
    > Kontakten [!INCLUDE[prod_short](includes/prod_short.md)] for Power Automate støtter flere produksjons- og sandkassemiljøer. Hvis du ikke har opprettet flere produksjons- eller sandkassemiljøer, er **Produksjon** det eneste tilgjengelige alternativet du kan velge.  

    Nå har du koblet til Business Central[!INCLUDE[prod_short](includes/prod_short.md)]-dataene og er klar til å begynne å bygge din flyt.

9. Når du skal opprette fra en mal, velger du **Start fra mal**.
10. Søk etter **Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]**-maler.
11. Fra listen over tilgjengelige maler velger du én av malene, og deretter velger du **Opprett**.  

    - *Be om godkjenning for Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-ordren*
    - *Be om godkjenning for Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-tilbudet*
    - *Be om godkjenning for Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-salgsfakturaen*
    - *Be om godkjenning for Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-salgskreditnotaen*
    - *Be om godkjenning for Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-kunden*
    - *Be om godkjenning for Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-bestillingen*
    - *Be om godkjenning for Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-kjøpsfakturaen*
    - *Be om godkjenning for Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-kjøpskreditnotaen*  
    - *Be om godkjenning for Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-varen*
    - *Be om godkjenning for Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-leverandøren*
    - *Be om godkjenning for Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-finanskladden*  
    - *Be om godkjenning for Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-finanskladdelinjer*
12. Power Automate vil vise en liste over tjenester som brukes i flytmalen, og vil forsøke å koble automatisk til disse tjenestene. Hvis du ikke tidligere har koblet til en tjeneste, blir du bedt om å logge deg på hver av tjenestene du må koble til. En grønn hake vises ved siden av hver tjeneste når en tilkobling er opprettet. Velg **Fortsett**.
13. Power Automate ber deg om å velge et miljø og selskap i din [!INCLUDE[prod_short](includes/prod_short.md)]-leier. Siden hvert trinn i flyten er uavhengig av neste, kan det hende at du må definere miljøet og selskapet flere ganger når du bruker en [!INCLUDE[prod_short](includes/prod_short.md)] Power Automate-mal.

Hvis du vil ha mer informasjon, kan du se [Power Automate-dokumentasjonen](/power-automate/getting-started).

## <a name="troubleshooting"></a>Feilsøking

### <a name="entity-set-not-found-error"></a>Feilen Finner ikke enhetssettet

#### <a name="problem"></a>Problem

Når du oppretter en ny Power Automate-flyt ved hjelp av en [!INCLUDE[prod_short](includes/prod_short.md)]-godkjenningsutløser, som *Det bes om godkjenning av et kjøpsdokument* vises det en feilmelding som ligner på:

**Finner ikke enhetssettet: \<name\>**

der **\<name\>** er navnet på tjenesten til den manglende nettjenesten, for eksempel **workflowWebhookSubscriptions** eller **workflowPurchaseDocumentLines**.

#### <a name="possible-cause"></a>Mulig årsak

Bruk av Power Automate til å integrere med [!INCLUDE[prod_short](includes/prod_short.md)]-godkjenninger krever at visse side- og codeunit-objekter publiseres som nettjenester. Som standard publiseres de fleste av de nødvendige objektene som nettjenester for deg. I enkelte tilfeller kan miljøet ha blitt tilpasset slik at disse objektene ikke lenger er publisert.

#### <a name="fix"></a>Løsning

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

[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Arbeidsflyt](across-workflow.md)  
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md)  
[Administrer arbeidsflyter for [!INCLUDE[prod_long](includes/prod_long.md)]](across-use-workflows.md)  
[Brukeroppsett for godkjenning](across-how-to-set-up-approval-users.md)  
[Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finans](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]