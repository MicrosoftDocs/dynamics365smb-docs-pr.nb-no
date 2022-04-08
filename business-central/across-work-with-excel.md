---
title: Vise og redigere i Excel fra Business Central (inneholder video)
description: Lær om hvordan du åpner sidene i Microsoft Excel fra Business Central for bedre dataanalyser.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: f03e67b0205af92fcdbb731a74ffe7f4507c39d3
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511262"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Vise og redigere i Excel fra Business Central

Med sider som viser en oversikt over poster i rader og kolonner, som en liste over kunder, ordrer eller fakturaer, kan du også eksportere listen til Microsoft Excel og vise den der. Avhengig av hvilken side du har, kan du vise to alternativer i Excel. Begge alternativene er tilgjengelige fra **Del**-ikonet ![Del en side i en annen app.](media/share-icon.png) øverst på en side. Du kan enten velge **Åpne i Excel**-handling eller **Rediger i Excel**-handlingen på siden. Denne artikkelen forklarer forskjellen mellom de to handlingene.

## <a name="open-in-excel"></a>Åpne i Excel

Med handlingen **Åpne i Excel** kan du gjøre endringer i postene i Excel, men du kan ikke publisere endringene tilbake til [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan bare lagre endringene i Excel-filen, uten at det påvirker dataene i [!INCLUDE[prod_short](includes/prod_short.md)].

- Med denne handlingen respekterer Excel filtre på siden som avgrenser postene som vises. Excel-arbeidsboken inneholder de samme radene og kolonnene som vises på siden i [!INCLUDE[prod_short](includes/prod_short.md)].

- Denne handlingen fungerer både i Windows- og macOS.

- Fra og med oppdatering 18.3 kan du også vise lister som vises i sidedeler, for eksempel linjene i en ordre. 

> [!NOTE]
> For [!INCLUDE[prod_short](includes/prod_short.md)] lokalt er handlingen **Åpne i Excel** tilgjengelig som standard. Hvis du konfigurerer [!INCLUDE[prod_short](includes/prod_short.md)] lokalt for redigering av data i Excel, erstattes handlingen **Åpne i Excel** med handlingen **Rediger i Excel**.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]  

## <a name="edit-in-excel"></a>Rediger i Excel

Handlingen **Rediger i Excel** er tilgjengelig i de fleste listene, men ikke alle. Med handlingen **Rediger i Excel** kan du gjøre endringer i postene i Excel og deretter publisere endringene tilbake til [!INCLUDE[prod_short](includes/prod_short.md)]. Når Excel åpnes, vises ruten for **Excel-tillegg** til høyre.

- Med denne handlingen respekterer Excel de fleste filtre på siden som begrenser postene som vises, slik at Excel-arbeidsboken vil inneholde nesten de samme postene og kolonnene.

- Du får de siste dataene fra [!INCLUDE[prod_short](includes/prod_short.md)] ved å velge **Oppdater** i ruten Excel-tillegg.

- Du kan bytte ut selskapet du arbeider med. Hvis du vil bytte selskap, velger du ikonet **Alternativer** ![Alternativer for Excel-tillegg.](media/cogwheel.png "Alternativer for Excel-tillegg") i ruten Excel-tillegg og velger selskapet fra feltet **Selskap**.  

    > [!IMPORTANT]
    > Når du endrer firmaet, må du sørge for at **Miljø**-feltet ikke er tomt. Hvis det er det, setter du det til ett av de tilgjengelige alternativene. Hvis ikke, vil ikke tillegget fungere som det skal.  

Hvis du gjør endringer i tillegget, må du laste det inn på nytt for å oppdatere tilkoblingen. Du kan laste inn på nytt ved å bruke menyen for ![tillegg i Excel](media/excel-addin-menu.png "Meny for Excel-tillegg") øverst til høyre for tillegget. Hvis du ikke kan laste inn tillegget, kontakter du systemansvarlig. Hvis du er administrator, kan du se [Hent Business Central-tillegget for Excel](admin-deploy-excel-addin.md).

> [!NOTE]
> Tillegget fungerer med Excel for nettet (online) fra alle enheter så lenge du bruker en nettleser som støttes. Det fungerer også med Excel-appen for Windows (PC), men ikke for macOS.
>
> For [!INCLUDE[prod_short](includes/prod_short.md)] lokalt er handlingen **Rediger i Excel** bare tilgjengelig hvis Excel-tillegget er konfigurert av systemansvarlig, og den er bare tilgjengelig for webklienten. For administratorer, hvis du vil vite hvordan du installerer Excel-tilleggskomponenten, se [Definere Excel-tillegget for redigering av Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).


<!-- Note for later: here we're immediately jumping to pretty advanced topics like changing company or reloading the addin. Fine to keep them for now. In the future, we will first need to explain in more detail the actual functionality of the addin, primarily these sub-sections:

Refreshing record data in Excel
Editing and publishing back to Business Central
Creating new records from Excel
Crafting your own editable Excel.
Point (4) is where it gets interesting for changing/specifying company, environment and other connection settings-->

### <a name="first-time-sign-in"></a>Første pålogging

Handlingen **Rediger i Excel** krever at Business Central-tillegget er installert i Excel. I noen tilfeller har administratoren kanskje ordnet det slik at tillegget installeres automatisk. I dette tilfellet må du bare logge deg på Business Central i ruten **Excel-tillegg** med brukernavn og passord. Ellers åpnes ruten **Ny Office-tillegg**. Hvis du vil installere tillegget, velger du **Klarer dette tillegget**, noe som installerer tillegget direkte fra Office store.

Hvis tillegget av en eller annen grunn ikke blir installert, kontakter du administratoren eller prøver å installere det manuelt. Hvis du vil ha mer informasjon, kan du se [Installer tillegget manuelt for egen bruk](admin-deploy-excel-addin.md#install).

## <a name="see-the-differences-between-the-options"></a>Se forskjellene mellom alternativene
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Analyser årsregnskap i Microsoft Excel](finance-analyze-excel.md)  
[Arbeid med Business Central](ui-work-product.md)  
[Forbedringer i Excel-integrasjon i 2019 lanseringsbølge 2](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]