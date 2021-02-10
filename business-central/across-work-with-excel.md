---
title: Vise og redigere i Excel fra Business Central
description: Lær om hvordan du åpner sidene i Microsoft Excel fra Business Central for bedre dataanalyser.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 11/06/2020
ms.author: jswymer
ms.openlocfilehash: cb172cd1d3285128e871fedb44ccd70fb84a669a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754170"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Vise og redigere i Excel fra Business Central

Med sider som viser en oversikt over poster i rader og kolonner, som en liste over kunder, ordrer eller fakturaer, kan du også vise poster ved hjelp av Microsoft Excel. Du har to alternative måter å gjøre dette på. Du kan enten velge **Åpne i Excel**-handling eller **Rediger i Excel**-handlingen på siden. Forskjellene mellom de to handlingen er følgende:  

## <a name="open-in-excel"></a>Åpne i Excel

- Med denne handlingen respekterer Excel filtre på siden som avgrenser postene som vises. Excel-arbeidsboken inneholder de samme radene og kolonnene som vises på siden i [!INCLUDE[prod_short](includes/prod_short.md)].

- Du kan gjøre endringer i postene i Excel, men du kan ikke publiserer endringene tilbake til [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan bare lagre endringene til Excel-filen på datamaskinen din.

- Denne handlingen fungerer både i Windows- og macOS.

> [!NOTE]
> For [!INCLUDE[prod_short](includes/prod_short.md)] lokalt er handlingen **Åpne i Excel** tilgjengelig som standard. Hvis du konfigurerer [!INCLUDE[prod_short](includes/prod_short.md)] lokalt for redigering av data i Excel, erstattes handlingen **Åpne i Excel** med handlingen **Rediger i Excel**.

## <a name="edit-in-excel"></a>Rediger i Excel

- Med denne handlingen respekterer Excel de fleste filtre på siden som begrenser postene som vises, slik at Excel-arbeidsboken vil inneholde nesten de samme postene og kolonnene.

- Fordelen med **Rediger i Excel**-handlingen er at den lar deg gjøre endringer i poster i Excel og deretter publiserer endringene tilbake til [!INCLUDE[prod_short](includes/prod_short.md)].

- Den fungerer bare i Windows, ikke i macOS.

- Du kan bytte ut selskapet du arbeider med. Du bytter selskap ved å velge ikonet **Alternativer** under ![Alternativer for Excel-tillegg](media/cogwheel.png "Alternativer for Excel-tillegg") i ruten Excel-tillegg, og deretter velger du selskapet fra **Selskap**-feltet.  

    > [!IMPORTANT]
    > Når du endrer firmaet, må du sørge for at **Miljø**-feltet ikke er tomt. Hvis det er det, setter du det til ett av de tilgjengelige alternativene. Hvis ikke, vil ikke tillegget fungere som det skal.  

Hvis du gjør endringer i tillegget, må du laste det inn på nytt for å oppdatere tilkoblingen. Du kan laste inn på nytt ved å bruke menyen for ![tillegg i Excel](media/excel-addin-menu.png "Meny for Excel-tillegg") øverst til høyre for tillegget. Hvis du ikke kan laste inn tillegget, kontakter du systemansvarlig. Hvis du er administrator, kan du se [Konfigurere Excel-tillegget for redigering av Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

> [!NOTE]
> For [!INCLUDE[prod_short](includes/prod_short.md)] lokalt er handlingen **Rediger i Excel** bare tilgjengelig hvis Excel-tillegget er konfigurert av systemansvarlig, og den er bare tilgjengelig for webklienten. For administratorer, hvis du vil vite hvordan du installerer Excel-tilleggskomponenten, se [Definere Excel-tillegget for redigering av Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

### <a name="see-the-differences-between-the-options"></a>Se forskjellene mellom alternativene
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Analysere årsregnskap i Microsoft Excel](finance-analyze-excel.md)  
[Arbeide med Business Central](ui-work-product.md)  
[Forbedringer i Excel-integrasjon i 2019 Release Wave 2](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  
