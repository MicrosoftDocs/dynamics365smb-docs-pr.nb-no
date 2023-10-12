---
title: Lag og endre egendefinerte oppsett for rapporter og dokumenter
description: 'Finn ut hvordan du lager egendefinerte oppsett for å tilpasse utseendet på en rapport når den vises, skrives ut eller lagres.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 03/06/2022
ms.author: bholtorf
---
# <a name="legacy-create-and-modify-custom-report-layouts"></a>(Eldre) Opprette og endre et egendefinert rapportoppsett

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Rapporter har som standard et innebygd oppsett. Rapportoppsettet kan være et RDLC (klientside for rapportdefinisjonsspråk), et rapportoppsett, Microsoft Word-rapportoppsett eller begge deler. Selv om du ikke kan endre innebygde oppsett, kan du opprette egendefinerte oppsett. En rapport kan ha flere egendefinerte rapportoppsett.

> [!NOTE]  
> I [!INCLUDE[prod_short](includes/prod_short.md)] dekker betegnelsen «rapport» også eksternt rettede dokumenter, for eksempel salgsfakturaer og ordrebekreftelser som du sender til kunder som PDF-filer.

Hvis du vil opprette et egendefinert oppsett, må du enten kopiere et eksisterende egendefinert oppsett eller legge til et nytt egendefinert oppsett. Egendefinerte oppsett er ofte basert på et innebygd oppsett. Når du legger til et nytt egendefinert oppsett, kan du legge til en RDLC- eller et Word-rapportoppsettype eller begge typer. Det nye egendefinerte oppsettet baseres på det innebygde oppsettet for rapporten hvis det er tilgjengelig. Hvis det ikke finnes noe innebygd oppsett for rapporttypen, opprettes et nytt, tomt oppsett. Du må endre og utforme det tomme oppsettet fra grunnen av. finn ut mer om RDLC- og Word-rapportoppsett, innebygde og egendefinerte oppsett og mer under [Håndtere rapportoppsett](ui-manage-report-layouts.md).  

> [!TIP]
> Du kan bruke finansrapporter til å få innsikt i de økonomiske dataene som er lagret i kontoplanen. Finn ut mer under [Klargjøre Financial Reporting med finansdata og kontokategorier](bi-how-work-account-schedule.md).

Når du har definert egendefinert rapportoppsett, kan du velge dem på sidene Kundekort og Leverandørkort. Oppsettene blir deretter brukt når du oppretter dokumenter for kunden eller leverandøren. Finn ut mer under [Definer dokumentoppsett for kunder og leverandører](ui-define-customer-vendor-document-layouts.md).

Du kan også bruke egendefinert rapportoppsett til å legge til innhold i e-postmeldinger. Rapportoppsett kan spare tid og bidra til å sikre konsekvens ved å bruke det samme innholdet på nytt når du kommuniserer med kundene. Hvis du vil bruke egendefinerte rapportoppsett med e-post, må filtypen for oppsettet være Word. Du kan ikke bruke filtypen RDLC. Finn ut mer under [Definer gjenbrukbare e-posttekster og -oppsett](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts).

## <a name="create-a-custom-layout"></a>Opprett et egendefinert oppsett

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Rapportoppsettsvalg**, og velg deretter den relaterte koblingen.

    Siden **Rapportoppsettsvalg** viser alle rapportene som er tilgjengelige i selskapet som er angitt i feltet **Selskapsnavn** øverst på siden.
2. Velg selskapet du vil opprette rapportoppsettet for, i **Selskapsnavn**-feltet.
3. Velg raden for rapporten du vil bruke opprette oppsettet for, og velg deretter handlingen **Egendefinerte oppsett**.  

   Siden **Egendefinerte rapportoppsett** vises og inneholder en oversikt over alle de egendefinerte oppsettene som er tilgjengelige for den valgte rapporten.
4. Hvis du vil opprette en kopi av et eksisterende egendefinert oppsett, velger du det eksisterende egendefinerte oppsettet fra listen, og deretter velger du handlingen **Kopier**.  

   Kopien av det egendefinerte oppsettet vises på siden **Egendefinerte rapportoppsett** og inneholder ordene *Kopi av* i **Beskrivelse**-feltet.
5. Hvis du vil legge til et nytt egendefinert oppsett som er basert på et innebygd oppsett, følger du denne fremgangsmåten:  
   1. Velg handlingen **Ny**. Siden **Sett inn innebygd oppsett for en rapport** vises med feltene **ID** og **Navn** automatisk utfylt.
   2. Slå på vekslebryteren **Sett inn Word-oppsett** for å legge til en egendefinert Word-rapportoppsettype ELLER slå på **Sett inn RDLC-oppsett** for å legge til en egendefinert RDLC-rapportoppsettype.
   4. Velg **OK**-knappen.  

    Det nye egendefinerte oppsettet vises på siden **Egendefinerte rapportoppsett**. Hvis et nytt oppsett er basert på et innebygd oppsett, vises **Kopi av innebygd oppsett** i **Beskrivelse**-feltet. Hvis det ikke finnes noe innebygd oppsett for rapporten, står det **Nytt oppsett** i **Beskrivelse**-feltet, som betyr at det egendefinerte oppsettet er tomt.
6. **Selskapsnavn**-feltet er som standard tomt, og egendefinert oppsett er tilgjengelig for rapporter av alle selskaper. Hvis du vil gjøre det egendefinerte oppsettet bare tilgjengelig i et bestemt selskap, velger du **Rediger**, og deretter angir ønsket selskap i **Selskapsnavn**-feltet.

Det egendefinerte oppsettet er opprettet, og du kan endre det etter behov.

> [!TIP]
> Du kan eksportere rapportresultatene til en Microsoft Excel-fil for å vise hele datasettet, inkludert alle kolonner, men uten oppsettet. Excel-filen kan hjelpe deg med å validere at rapporten returnerer de forventede dataene eller diagnostisere problemer. Finn ut mer under [Analyser rapportdata med Excel](report-analyze-excel.md).

## <a name="modifying-a-custom-layout"></a><a name="ModifyCustomLayout"></a>Endre et egendefinert oppsett

Når du skal endre et egendefinert rapportoppsett, du må først eksportere rapportoppsettet som en fil til en plassering på datamaskinen eller nettverket. Deretter åpner du det eksporterte dokumentet og foretar endringene. Når du er ferdig å foreta endringer, importerer du rapportoppsettet.

### <a name="modify-a-custom-layout"></a>Endre et egendefinert oppsett

1. Eksporter et egendefinert oppsett fra **Egendefinerte rapportoppsett**-siden. Hvis siden ikke allerede er åpen, kan du søke etter og åpne **Rapportoppsettsvalg**-siden, velge rapporten som har oppsettet du vil endre, og deretter velge handlingen **Egendefinerte oppsett**.  
2. På siden **Egendefinerte rapportoppsett** velger du oppsettet som du vil endre, velger **Eksporter oppsett**-handlingen og velger deretter **Lagre** eller **Lagre som** for å lagre rapportoppsettsdokumentet på et sted på datamaskinen eller nettverket.  
3. Åpne rapportoppsettdokumentet du lagret, og gjør endringene.

   Hvis du endrer et Word-oppsett, kan du åpne oppsettsdokumentet i Word. Lær mer om å redigere Word-rapporter under [Arbeid med Word-oppsett](ui-how-add-fields-word-report-layout.md)<!--the next section [Making Changes to the Report Layout](ui-how-create-custom-report-layout.md#MakeChangesToLayout)-->.

   RDLC-rapportoppsett er mer avansert enn Word-rapportoppsett. Finn ut mer om hvordan du endrer et RDLC-rapportoppsett under [Utform RDLC-rapportoppsett](/dynamics-nav/Designing-RDLC-Report-Layouts).

   Husk å lagre endringene når du er ferdig.

4. Gå tilbake til **Egendefinerte rapportoppsett**-siden, velg rapportoppsettet som du har eksportert eller endret, og velg deretter **Importer oppsett**-handlingen.  

5. I dialogboksen **Importer** velger du **Velg** for å finne og velge rapportoppsettdokumentet som er endret, og velger deretter **Åpne**.

> [!IMPORTANT]
> Husk å importere rapportoppsettdokumentet du endret. Hvis ikke vil ikke det nye rapportoppsettet være tilgjengelig.

<!--
## <a name="create-and-modify-custom-report-layouts"></a><a name="MakeChangesToLayout"></a>Create and modify custom report layouts

To make general formatting and layout changes, such as changing text font, adding and modifying a table, or removing a data field, just use the basic editing features of Word like you do with any Word document.

If you're designing a Word report layout from scratch or adding new data fields, then start by adding a table that includes rows and columns that will eventually hold the data fields.

> [!TIP]  
> Show the table gridlines so that you see the boundaries of table cells. Remember to hide the gridlines when you're done editing. To show or hide table gridlines, select the table, and then under **Layout** on the **Table** tab, choose **View Gridlines**.

### <a name="embedding-fonts-in-word-layouts-for-consistency"></a>Embedding fonts in Word layouts for consistency

To ensure that reports always display and print with the intended fonts, wherever users open or print the reports, you can embed the fonts in the Word document. However, embedding fonts can significantly increase the size of the Word files. Learn more about embedding fonts in Word at [Embed fonts in Word, PowerPoint, or Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

### <a name="removing-label-and-data-fields-in-word-layouts"></a><a name="RemoveField"></a>Removing label and data fields in Word layouts

 Label and data fields of a report are contained in content controls in Word. The following figure illustrates a content control when it's selected in the Word document.  

 ![Content control for field in Word report layout.](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 The name of the label or data field name displays in the content control. In the example, the field name is CompanyAddr1.  

### <a name="to-remove-a-label-or-data-field"></a>To remove a label or data field

1. Right-click the field you want to delete, then choose **Remove Content Control**.  

     The content control is removed, but the field name remains as text.  

2. Delete the remaining text as needed.  

### <a name="adding-data-fields"></a>Adding data fields

Adding data fields from a report dataset is more advanced and requires some knowledge of the report dataset. Learn more about adding fields for data, labels, and images at [Add Fields to a Word Report Layout](ui-how-add-fields-word-report-layout.md).  -->

## <a name="see-also"></a>Se også

[Håndtere rapportoppsett](ui-manage-report-layouts.md)  
[Endre gjeldende rapportoppsett](ui-how-change-layout-currently-used-report.md)  
[Importere og eksportere en egendefinert rapport eller et egendefinert dokumentoppsett](ui-how-import-and-export-report-layout.md)  
[Arbeid med rapporter, satsvise jobber og XMLport-er](ui-work-report.md)  
[Klargjøre Financial Reporting med finansdata og kontokategorier](bi-how-work-account-schedule.md)  
[Forretningsintelligens](bi.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
