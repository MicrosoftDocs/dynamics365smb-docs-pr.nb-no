---
title: Lag og endre egendefinerte oppsett for rapporter og dokumenter
description: Finn ut hvordan du lager egendefinerte oppsett for å tilpasse utseendet på en rapport når den vises, skrives ut eller lagres.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9650, 9652
ms.date: 03/06/2022
ms.author: edupont
ms.openlocfilehash: 1d9d61ad7a4e9b0b64fd11d8a2c1a29676a8ddb4
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531975"
---
# <a name="legacy-create-and-modify-custom-report-layouts"></a>(Eldre) Opprette og endre et egendefinert rapportoppsett

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Rapporter har som standard et innebygd rapportoppsett. Oppsettet kan enten være et RDLC rapportoppsettet, et Word-rapportoppsett eller begge typer. Du kan ikke endre innebygde oppsett, men du kan opprette egendefinerte oppsett. En rapport kan ha flere egendefinerte rapportoppsett.

> [!NOTE]  
> I [!INCLUDE[prod_short](includes/prod_short.md)] dekker betegnelsen «rapport» også eksternt rettede dokumenter, for eksempel salgsfakturaer og ordrebekreftelser som du sender til kunder som PDF-filer.

Hvis du vil opprette et egendefinert oppsett, må du enten kopiere et eksisterende egendefinert oppsett eller legge til et nytt egendefinert oppsett. Egendefinerte oppsett er ofte basert på et innebygd oppsett. Når du legger til et nytt egendefinert oppsett, kan du legge til en RDLC- eller Word-rapportoppsettype eller begge typer. Det nye egendefinerte oppsettet baseres på det innebygde oppsettet for rapporten hvis det er tilgjengelig. Hvis det ikke finnes noe innebygd oppsett for typen, opprettes et nytt, tomt oppsett. Du må endre og utforme det tomme oppsettet fra grunnen av. Hvis du vil ha mer informasjon om RDLC- og Word-rapportoppsett, innebygde og egendefinerte oppsett og mer, kan du se [Håndtere rapportoppsett](ui-manage-report-layouts.md).  

> [!TIP]
> Du kan bruke kontoskjemaer til å få innsikt i de økonomiske dataene som er lagret i kontoplanen. Hvis du vil ha mer informasjon, se [Klargjøre Financial Reporting med kontoskjemaer og kontokategorier](bi-how-work-account-schedule.md).

Når du har definert oppsett for egendefinerte rapporter, kan du velge dem på sidene Kundekort og Leverandørkort. Oppsettene blir brukt når du oppretter dokumenter for kunden eller leverandøren. Hvis du vil ha mer informasjon, se [Definere dokumentoppsett for kunder og leverandører](ui-define-customer-vendor-document-layouts.md).

Du kan også bruke egendefinert rapportoppsett til å legge til innhold i e-postmeldinger. Rapportoppsett kan spare tid og bidra til å sikre konsekvens ved å bruke det samme innholdet på nytt når du kommuniserer med kundene. Hvis du vil bruke egendefinerte rapportoppsett med e-post, må filtypen for oppsettet være Word. Du kan ikke bruke filtypen RDLC. Hvis du vil ha mer informasjon, kan du se [Definer gjenbrukbare e-tekster og oppsett](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts). 

## <a name="to-create-a-custom-layout"></a>Slik oppretter du et egendefinert oppsett

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Rapportoppsettsvalg**, og velg deretter den relaterte koblingen.

    Siden **Rapportoppsettsvalg** viser alle rapportene som er tilgjengelige i selskapet som er angitt i feltet **Selskapsnavn** øverst på siden.
2. Velg selskapet du vil opprette rapportoppsettet for, i **Selskapsnavn**-feltet.
3. Velg raden for rapporten du vil bruke opprette oppsettet for, og velg deretter handlingen **Egendefinerte oppsett**.  

   Siden **Egendefinerte rapportoppsett** vises og inneholder en oversikt over alle de egendefinerte oppsettene som er tilgjengelige for den valgte rapporten.
4. Hvis du vil opprette en kopi av et eksisterende egendefinert oppsett, velger du det eksisterende egendefinerte oppsettet fra listen, og deretter velger du handlingen **Kopier**.  

   Kopien av det egendefinerte oppsettet vises på siden **Egendefinerte rapportoppsett** og inneholder ordene *Kopi av* i **Beskrivelse**-feltet.
5. Hvis du vil legge til et nytt egendefinert oppsett som er basert på et innebygd oppsett, gjør du følgende trinn:  
   1. Velg handlingen **Ny**. Siden **Sett inn innebygd oppsett for en rapport** vises. Feltene **ID** og **Navn** fylles ut automatisk.
   2. Hvis du vil legge til en egendefinert Word-rapportoppsettype, aktiverer du **Sett inn Word-oppsett**.
   3. Hvis du vil legge til en egendefinert RDLC-rapportoppsettype, aktiverer du **Sett inn RDLC-oppsett**.
   4. Velg **OK**-knappen.  

    Det nye egendefinerte oppsettet vises på siden **Egendefinerte rapportoppsett**. Hvis et nytt oppsett er basert på et innebygd oppsett, står det **Kopi av innebygd oppsett** i **Beskrivelse**-feltet. Hvis det ikke finnes noe innebygd oppsett for rapporten, står det **Nytt oppsett** i **Beskrivelse**-feltet, som angir at det egendefinerte oppsettet er tomt.
6. **Selskapsnavn**-feltet er som standard tomt, noe som betyr at det egendefinerte oppsettet er tilgjengelig for rapporten i alle selskaper. Hvis du vil gjøre det egendefinerte oppsettet bare tilgjengelig i et bestemt selskap, velger du **Rediger**, og deretter angir ønsket selskap i **Selskapsnavn**-feltet.

Det egendefinerte oppsettet er opprettet. Du kan nå endre det egendefinerte oppsettet etter behov.

> [!TIP]
> Du kan eksportere rapportresultatene til en Excel-fil for å vise hele datasettet, inkludert alle kolonner, men uten oppsettet. Excel-filen kan hjelpe deg med å validere at rapporten returnerer de forventede dataene eller diagnostisere problemer. Hvis du vil ha mer informasjon, kan du se [Analyser rapportdata med Excel](report-analyze-excel.md).

## <a name="modifying-a-custom-layout"></a><a name="ModifyCustomLayout"></a>Endre et egendefinert oppsett

Når du skal endre et rapportoppsett, du må først eksportere rapportoppsettet som en fil til en plassering på datamaskinen eller nettverket. Deretter åpner du det eksporterte dokumentet og foretar endringene. Når du er ferdig å foreta endringer, importerer du rapportoppsettet.

### <a name="to-modify-a-custom-layout"></a>Endre et egendefinert oppsett

1. Du kan eksportere et egendefinert oppsett fra **Egendefinerte rapportoppsett**-siden. Hvis siden ikke allerede er åpen, kan du søke etter og åpne **Rapportoppsettsvalg**-siden, velge rapporten som har oppsettet du vil endre, og deretter velge handlingen **Egendefinerte oppsett**.  
2. På siden **Egendefinerte rapportoppsett** velger du oppsettet som du vil endre, velger **Eksporter oppsett**-handlingen og velger deretter **Lagre** eller **Lagre som** for å lagre rapportoppsettsdokumentet på et sted på datamaskinen eller nettverket.  
3. Åpne rapportoppsettdokumentet du lagret, og gjør deretter endringene.

   Hvis du endrer et Word-oppsett, kan du åpne oppsettsdokumentet i Word. Hvis du vil ha redigeringsdetaljer, kan du se [Arbeid med Word-oppsett](ui-how-add-fields-word-report-layout.md)<!--the next section [Making Changes to the Report Layout](ui-how-create-custom-report-layout.md#MakeChangesToLayout)-->.

   RDLC-rapportoppsett er mer avansert enn Word-rapportoppsett. Hvis du vil ha mer informasjon om hvordan du endrer et RDLC-rapportoppsett, kan du se [Utforme RDLC-rapportoppsett](/dynamics-nav/Designing-RDLC-Report-Layouts).

   Husk å lagre endringene når du er ferdig.

4. Gå tilbake til **Egendefinerte rapportoppsett**-siden, velg rapportoppsettet som du har eksportert eller endret, og velg deretter **Importer oppsett**-handlingen.  

5. I dialogboksen **Importer** velger du **Velg** for å finne og velge rapportoppsettdokumentet som er endret, og velger deretter **Åpne**.

> [!IMPORTANT]
> Husk å importere rapportoppsettdokumentet du endret. Hvis ikke vil ikke det nye rapportoppsettet være tilgjengelig.

<!--
##  <a name="MakeChangesToLayout"></a> Create and Modify Custom Report Layouts

To make general formatting and layout changes, such as changing text font, adding and modifying a table, or removing a data field, just use the basic editing features of Word, like you do with any Word document.

If you're designing a Word report layout from scratch or adding new data fields, then start by adding a table that includes rows and columns that will eventually hold the data fields.

> [!TIP]  
> Show the table gridlines so that you see the boundaries of table cells. Remember to hide the gridlines when you're done editing. To show or hide table gridlines, select the table, and then under **Layout** on the **Table** tab, choose **View Gridlines**.

### Embedding Fonts in Word Layouts for Consistency

To ensure that reports always display and print with the intended fonts, wherever users open or print the reports, you can embed the fonts in the Word document. However, embedding fonts can significantly increase the size of the Word files. For more information about embedding fonts in Word, see [Embed fonts in Word, PowerPoint, or Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

###  <a name="RemoveField"></a> Removing Label and Data Fields in Word Layouts

 Label and data fields of a report are contained in content controls in Word. The following figure illustrates a content control when it's selected in the Word document.  

 ![Content control for field in Word report layout.](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 The name of the label or data field name displays in the content control. In the example, the field name is CompanyAddr1.  

### To remove a label or data field  

1. Right-click the field that you want to delete, and then choose **Remove Content Control**.  

     The content control is removed, but the field name remains as text.  

2. Delete the remaining text as needed.  

### Adding data fields

Adding data fields from a report dataset is a more advanced and requires some knowledge of the report dataset. For information about adding fields for data, labels, data, and images, see [Add Fields to a Word Report Layout](ui-how-add-fields-word-report-layout.md).  -->

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Håndtere rapportoppsett](ui-manage-report-layouts.md)  
[Endre gjeldende rapportoppsett](ui-how-change-layout-currently-used-report.md)  
[Importere og eksportere en egendefinert rapport eller et egendefinert dokumentoppsett](ui-how-import-and-export-report-layout.md)  
[Arbeid med rapporter, satsvise jobber og XMLport-er](ui-work-report.md)  
[Klargjøre Financial Reporting med kontoskjemaer og kontokategorier](bi-how-work-account-schedule.md)  
[Forretningsintelligens](bi.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
