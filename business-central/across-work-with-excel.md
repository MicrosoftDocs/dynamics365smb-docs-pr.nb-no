---
title: Vise og redigere i Excel fra Business Central
description: Lær om hvordan du åpner sidene i Microsoft Excel fra Business Central for bedre dataanalyser.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 6bf12f55f6bce843c4ed12f2a40db542367fffde
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443484"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Vise og redigere i Excel fra Business Central

Med sider som viser en oversikt over poster i rader og kolonner, som en liste over kunder, ordrer eller fakturaer, kan du også vise poster ved hjelp av Microsoft Excel. Avhengig av hvilken side du har, kan du vise to alternativer i Excel. Du kan enten velge **Åpne i Excel**-handling eller **Rediger i Excel**-handlingen på siden. Denne artikkelen forklarer forskjellen mellom de to handlingene.

## <a name="open-in-excel"></a>Åpne i Excel

Med handlingen **Åpne i Excel** kan du gjøre endringer i postene i Excel, men du kan ikke publisere endringene tilbake til [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan bare lagre endringene til Excel-filen på datamaskinen din.

- Med denne handlingen respekterer Excel filtre på siden som avgrenser postene som vises. Excel-arbeidsboken inneholder de samme radene og kolonnene som vises på siden i [!INCLUDE[prod_short](includes/prod_short.md)].

- Denne handlingen fungerer både i Windows- og macOS.

- Fra og med oppdatering 18.3 kan du også vise lister som vises i sidedeler, for eksempel linjene i en ordre. Denne funksjonen er nå en valgfri funksjon, som krever at du aktiverer **Eksport av alle listedeler til Excel** i **Funksjonsstyring**. Hvis du vil ha mer informasjon, kan du se [Aktivering av kommende funksjoner på forhånd](/dynamics365/business-central/dev-itpro/administration/feature-management). 

> [!NOTE]
> For [!INCLUDE[prod_short](includes/prod_short.md)] lokalt er handlingen **Åpne i Excel** tilgjengelig som standard. Hvis du konfigurerer [!INCLUDE[prod_short](includes/prod_short.md)] lokalt for redigering av data i Excel, erstattes handlingen **Åpne i Excel** med handlingen **Rediger i Excel**.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]  

## <a name="edit-in-excel"></a>Rediger i Excel

Med handlingen **Rediger i Excel** kan du gjøre endringer i postene i Excel og deretter publisere endringene tilbake til [!INCLUDE[prod_short](includes/prod_short.md)].

- Med denne handlingen respekterer Excel de fleste filtre på siden som begrenser postene som vises, slik at Excel-arbeidsboken vil inneholde nesten de samme postene og kolonnene.

- Den fungerer bare i Windows, ikke i macOS.

- Du kan bytte ut selskapet du arbeider med. Hvis du vil bytte selskap, velger du ikonet **Alternativer** ![Alternativer for Excel-tillegg.](media/cogwheel.png "Alternativer for Excel-tillegg") i ruten Excel-tillegg og velger selskapet fra feltet **Selskap**.  

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


[!INCLUDE[footer-include](includes/footer-banner.md)]