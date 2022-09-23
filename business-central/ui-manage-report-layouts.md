---
title: Administrere rapport- og dokumentoppsett
description: Bruk rapportoppsett til å tilpasse dokumenter, for eksempel tilpasse skriften, logoen eller sideinnstillingene for PDF-filer du sender til kunder.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9652, 9650
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 0c5a8d8e9cbb556b25a3b1c5ee6069ac07c7cc9f
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/19/2022
ms.locfileid: "9534781"
---
# <a name="report-and-document-layouts-overview"></a>Oversikt over rapport- og dokumentoppsett

Et rapportoppsett styrer innholdet og formatet for rapporten, blant annet hvilke datafelt i et rapportdatasett som skal vises i rapporten, hvordan de er ordnet, samt tekststil, bilder og mer. Fra [!INCLUDE[prod_short](includes/prod_short.md)] kan du endre oppsettet som skal brukes i en rapport, opprette nytt oppsett eller endre eksisterende oppsett.

> [!NOTE]  
> I [!INCLUDE[prod_short](includes/prod_short.md)] dekker betegnelsen «rapport» også eksternt rettede dokumenter, for eksempel salgsfakturaer og ordrebekreftelser som du sender til kunder som PDF-filer.

Du kan også bruke rapportoppsett til å legge til innhold i e-postmeldinger. Rapportoppsett kan for eksempel spare tid og bidra til å sikre konsekvens ved å bruke det samme innholdet på nytt når du kommuniserer med kundene. Hvis du vil bruke egendefinerte rapportoppsett med e-post, må filtypen for oppsettet være Word. Du kan ikke bruke filtypen RDLC. Hvis du vil ha mer informasjon, kan du se [Definer gjenbrukbare e-tekster og oppsett](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts). 

## <a name="introduction"></a>Introduksjon

Et rapportoppsett brukes især til å konfigurere følgende ting:

* Etikett- og datafeltene som skal tas med fra datasettet for [!INCLUDE[prod_short](includes/prod_short.md)]-rapporten.
* Tekstformatet, for eksempel skrifttype, størrelse og farge.
* Selskapets logo og plasseringen.
* Generelle sideinnstillinger, for eksempel marger og bakgrunnsbilder.

En rapport kan defineres med flere rapportoppsett, som du kan bytte mellom etter behov. 

<!--You can use one of the built-in report layouts or you can create custom report layouts and assign them to your reports as needed. For more information, see [Create a Custom Report or Document Layout](ui-how-create-custom-report-layout.md).-->

Det finnes to viktige sider ved rapportoppsett som påvirker hvordan du arbeider med dem: *oppsettstypen* og *oppsettskilden*. Oppsettstypen angir typen fil som oppsettet er basert på. Kildetypen angir oppsettets opprinnelse.

## <a name="layout-types"></a>Oppsettstype

Det finnes fire typer oppsett som du kan bruke i rapporter: Word, RDLC, Excel og eksternt.

### <a name="word"></a>Word

Word-oppsett er basert på et Word-dokumenter (DOCX-filtypen). Oppsett for Word lar deg utforme rapportoppsett ved hjelp av Microsoft Word. Et oppsettet for Word bestemmer rapportens innhold – kontrollere hvordan innholdselementer ordnes og hvordan de ser ut. I et Word-oppsettdokument brukes vanligvis tabeller til å ordne innhold, der cellene kan inneholde datafelt, tekst eller bilder.

[![Eksempel på et Word-rapportoppsettsdokument for Business Central.](media/word-layout-overview.png)](media/word-layout-overview.png#lightbox) 

<!--![Example of a word report layout document for Business Central.](media/nav_wordreportlayout_edit_in_word_example.png) -->

Hvis du vil ha mer informasjon, kan du se [Arbeid med Word-oppsett](ui-how-add-fields-word-report-layout.md).

### <a name="excel"></a>Excel

Oppsett for Excel er basert på Microsoft Excel-arbeidsbøker (XLSX-filtyper). De gjør det mulig å opprette rapporter ved hjelp av velkjente Excel-funksjoner for oppsummering, analyse og presentasjon av data med verktøy for eksempel formler, pivottabeller, pivotdiagrammer med mer.

[![Viser et eksempel på et Excel-oppsett.](media/excel-layout-2.png)](media/excel-layout-2.png#lightbox)

Hvis du vil ha mer informasjon, kan du se [Arbeid med Excel-oppsett](ui-excel-report-layouts.md).

### <a name="rdlc"></a>RDLC

RDLC-oppsett er basert på oppsettsfiler for rapportdefinisjon for klient (filtypen RDLC eller RDL). Disse oppsettene er opprettet og endret ved hjelp av SQL Server Report Builder eller Microsoft RDLC Report Designer. Utformingskonseptet for RDLC-oppsett ligner på Word-oppsett, der oppsettet bestemmer hvilke felter som skal vises, og hvordan de skal organiseres. Å utforme RDLC-oppsett er imidlertid en mer avansert oppgave enn å utforme Word-oppsett.

[![Viser et eksempel på et RDLC-oppsett.](media/rdlc-layout-overview.png)](media/rdlc-layout-overview.png#lightbox)

Hvis du vil ha mer informasjon, kan du se [Arbeid med RDLC-oppsett](ui-rdlc-report-layouts.md).

### <a name="external"></a>Eksternt

En ekstern oppsettstype viser til en avansert type som er spesiallaget for bestemte rapporter. Rapportene og oppsettene leveres vanligvis av partnere, ikke Microsoft. Den faktiske filtypen for oppsettet vil variere avhengig av leverandøren.

Hvis du vil ha mer informasjon, kan du se [Utvikle en egendefinert rapportgjengivelse](/dynamics365/business-central/dev-itpro/developer/devenv-report-custom-render).

## <a name="layout-sources"></a>Oppsettskilder

I tillegg til typen er oppsett ytterligere inndelt i tre kategorier, basert på kilden eller opprinnelsen.

* Utvidelsesoppsett

   Utvidelsesoppsett er oppsett som er en del av en utvidelse som er installert på miljøet. Disse oppsettene er vanligvis standardoppsett av Microsoft, for eksempel i basisprogrammet. De kan eventuelt være oppsett som er inkludert i utvidelser fra andre programvareleverandører. Du kan gjenkjenne utvidelsesoppsett på siden **Rapportoppsett** fordi utvidelsesnavnet og utgiveren vises i kolonnen **Utvidelse**.

* Brukerdefinert oppsett

   Den andre kilden til oppsett er sluttbrukeren. I Business Central kan en bruker med riktige tillatelser legge til nye oppsett på ulike måter. Du kan for eksempel starte fra et eksisterende utvidelsesoppsett eller et annet brukerdefinert oppsett. På **Rapportoppsett** vil det brukerdefinerte oppsettet være en tom **Utvidelse**-kolonne.

   Hvis du vil ha mer informasjon, kan du se [Kom i gang med å opprette rapportoppsett](ui-get-started-layouts.md).

* Egendefinerte oppsett

  Egendefinerte oppsett er også oppsett som opprettes av brukere. Forskjellen er at disse oppsettene blir opprettet fra en eldre **Egendefinerte rapportoppsett**-side for egendefinerte rapporter, og de kan bare være Word- og RDLC-type. Selv om du fortsatt kan opprette egendefinerte oppsett, blir de gjort om til fordel for brukerdefinerte oppsett.

  Hvis du vil ha mer informasjon, kan du se [(Eldre) Opprett og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md).

Hvis du vil ha mer informasjon om hvordan du avgjør hvilken type som er best, kan du se [Angi hvilken type oppsett du ønsker](ui-get-started-layouts.md#decide).

> [!IMPORTANT]
> Det er viktig å huske at du ikke kan endre utvidelsesoppsett fra Business Central-klienten. Du kan for eksempel ikke endre oppsettsnavnet eller -typen, eller du kan laste opp og erstatte det med en annen versjon. Hvis du prøver, får du en feilmelding. Du må opprette et brukerdefinert eller egendefinert oppsett basert på utvidelsesoppsettet i stedet.

<!--
### Built-in and custom report layouts



[!INCLUDE[prod_short](includes/prod_short.md)] includes several built-in layouts. Built-in layouts are predefined layouts that are designed for specific reports. [!INCLUDE[prod_short](includes/prod_short.md)] reports will have a built-in layout as either an RDLC report layout, Word report layout, or in some cases both. You can’t modify a built-in report layout from [!INCLUDE[prod_short](includes/prod_short.md)] but you use them as a starting point for building your own custom report layouts.

Custom layouts are report layouts that you design to change the appearance of a report. You typically create a custom layout based on a built-in layout, but you can create them from scratch or from a copy of an existing custom layout. Custom layouts enable you to have multiple layouts for the same report, which you switch among as needed. For example, you can have different layouts for each [!INCLUDE[prod_short](includes/prod_short.md)] company, or you can have different layouts for the same company for specific occasions or events, like a special campaign or holiday season.


Deciding on whether to use a Word, Excel, or RDLC layout type will depend on how you want the generated report to look and your knowledge of tools for creating the layouts, like Word, Excel, and SQL Server Report Builder.

* The general design concepts for Word and RDLC layouts are similar. However each type has certain design features that affect how the generated report appears in [!INCLUDE[prod_short](includes/prod_short.md)]. This means that the same report might look different when using the Word report layout compared to the RDLC report layout.

* The process for setting up Word, Excel, and RDLC report layouts on reports is the same. The main difference is in the way you modify the layouts. Word and especially Excel layouts are typically easier to create and modify than RDLC report layouts because you use Word and Excel. RDLC report layouts are modified by using SQL Server Report builder, which targets more advanced users.

* Not all reports and document have a dataset that is optimized for use with an Excel layout. For example, aggregations and complex calculations work best with RDLC or Word layouts. The same is true for documents.

For information about how to switch the layout currently used on a report, see [Set the Layout Used by a Report](ui-set-report-layout.md).

-->



## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Oppdater egendefinerte rapportoppsett](ui-update-report-layouts.md)  
[Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md)  
[Importere og eksportere en egendefinert rapport eller et egendefinert dokumentoppsett](ui-how-import-and-export-report-layout.md)  
[Definere spesielle dokumentoppsett for kunder og leverandører](ui-define-customer-vendor-document-layouts.md)  
[Send dokumenter i e-post](ui-how-send-documents-email.md)  
[Arbeid med rapporter, satsvise jobber og XMLport-er](ui-work-report.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
