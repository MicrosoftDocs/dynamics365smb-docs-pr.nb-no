---
title: Arbeid med RDLC-oppsett
description: Få en innføring i RDLC-rapportoppsett.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 03/14/2022
ms.author: jswymer
---
# <a name="working-with-rdlc-layouts" />Arbeid med RDLC-oppsett

RDLC-oppsett er basert på oppsettsfiler for rapportdefinisjon for klient (filtypen RDLC eller RDL). Utformingskonseptene for RDLC-oppsett ligner på andre typer oppsett. Oppsettet bestemmer hvilke felter som skal vises, og hvordan de skal organiseres. Å utforme RDLC-oppsett er imidlertid en mer avansert oppgave enn å utforme Word- og Excel-oppsett.

[![Viser de ulike elementene på et RDLC-oppsett.](media/rdlc-layout.png)](media/rdlc-layout.png#lightbox)

## <a name="required-tools" />Obligatoriske verktøy

Hvis du vil endre RDL-oppsett, kan du bruke enten Microsoft SQL Server Report Builder eller Microsoft RDLC Report Designer.

- Report Builder er en frittstående app som er installert på datamaskinen av deg eller en administrator. Med Business Central on-Premises installeres Report Builder automatisk med installasjonen av Business Central Server. Hvis du vil ha mer informasjon om hvordan du installerer Report Builder, kan du se [Installer Report Builder](/sql/reporting-services/install-windows/install-report-builder) i SQL Server-dokumentasjonen.

- RDLC Report Designer er en utvidelse for Visual Studio 2017 og nyere. Du kan laste ned og installere RDLC Report Designer fra [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=ProBITools.MicrosoftRdlcReportDesignerforVisualStudio-18001).

## <a name="create-and-modify-rdlc-layouts" />Opprett og endre RDLC-oppsett

Oppretting og endring av RDLC-oppsett er en avansert oppgave som ofte gjøres av privilegerte brukere eller utviklere. De grunnleggende konseptene er ikke spesifikke for Business Central-reportoppsett. Av den grunn henviser vi deg til følgende dokumentasjon:

- [Opprett RDL-oppsettsrapport](/dynamics365/business-central/dev-itpro/developer/devenv-howto-rdl-report-layout)

    Denne artikkelen forklarer hvordan du oppretter et RDLC-rapportoppsett fra AL-kode.

- [Rapporter, rapportdeler og rapportdefinisjoner ](/sql/reporting-services/report-design/reports-report-parts-and-report-definitions-report-builder-and-ssrs?)

 Koblingene til SQL Server Reporting Services-dokumentasjonen for RDL/RDLC. Dokumentasjonen forklarer begrepene  
bak RDL/RDLC og hvordan du bruker Report Builder.

> [!NOTE]
> Report Builder gjenkjenner bare filtypen RDL, ikke RDLC. Oppsettsfiler som er eksportert fra Business Central, er RDLC-filtyper. Hvis du vil endre oppsettet i Report Builder, gir du filen nytt navn til RDL.

## <a name="see-related-microsoft-trainingtrainingmoduleschange-documents-dynamics--business-centralindex" />Se relatert [Microsoft-opplæring](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also" />Se også

[Håndtere rapportoppsett](ui-manage-report-layouts.md)  
[Definer oppsettet som brukes av en rapport](ui-set-report-layout.md)  
[Kom i gang med å opprette rapportoppsett](ui-get-started-layouts.md)  
[Arbeid med rapporter, satsvise jobber og XMLport-er](ui-work-report.md)  
[Forretningsintelligens](bi.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Analyser rapportdata med Excel](report-analyze-excel.md).

[!INCLUDE[footer-include](includes/footer-banner.md)]
