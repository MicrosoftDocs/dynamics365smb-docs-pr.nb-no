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
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0b4642f6ca4c7701cbb49e8441debccfbd32b9be
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8134720"
---
# <a name="create-and-modify-custom-report-layouts"></a>Opprette og endre et egendefinert rapportoppsett

En rapport har som standard et innebygd rapportoppsett, som kan være et RDLC-rapportoppsett, et innebygd Word-rapportoppsett eller i noen tilfeller begge typer. Du kan ikke endre innebygde oppsett. Du kan imidlertid opprette egendefinerte oppsett der du kan endre utseendet på rapporten når den vises, skrives ut eller lagres. Du kan opprette flere egendefinerte rapportoppsett for samme rapport og deretter bytte oppsettet som brukes av en rapport, etter behov.

> [!NOTE]  
> I [!INCLUDE[prod_short](includes/prod_short.md)] dekker betegnelsen «rapport» også eksternt rettede dokumenter, for eksempel salgsfakturaer og ordrebekreftelser som du sender til kunder som PDF-filer.

Hvis du vil opprette et egendefinert oppsett, kan du lage en kopi av et eksisterende egendefinert oppsett eller legge til et nytt egendefinert oppsett, som i de fleste tilfeller er basert på et innebygd oppsett. Når du legger til et nytt egendefinert oppsett, kan du legge til en RDLC-rapportoppsettype, en Word-rapportoppsettype eller begge typer. Det nye egendefinerte oppsettet baseres automatisk på det innebygde oppsettet for rapporten hvis det er tilgjengelig. Hvis det ikke finnes noe innebygd oppsett for typen, opprettes et nytt, tomt oppsett. Du må endre og utforme det tomme oppsettet fra grunnen av. Hvis du vil ha mer informasjon om RDLC- og Word-rapportoppsett, innebygde og egendefinerte oppsett og mer, kan du se [Håndtere rapportoppsett](ui-manage-report-layouts.md).  

> [!TIP]
> Du kan bruke kontoskjemaer til å få innsikt i de økonomiske dataene som er lagret i kontoplanen. Hvis du vil ha mer informasjon, se [Klargjøre Financial Reporting med kontoskjemaer og kontokategorier](bi-how-work-account-schedule.md).

Når egendefinerte rapportoppsett er definert, kan du velge dem fra kunde- og leverandørkortene for å angi at de valgte oppsettene skal brukes for dokumenter du oppretter for den aktuelle kunden eller leverandøren. Hvis du vil ha mer informasjon, se [Definere dokumentoppsett for kunder og leverandører](ui-define-customer-vendor-document-layouts.md).

## <a name="to-create-a-custom-layout"></a>Slik oppretter du et egendefinert oppsett

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Rapportoppsettsvalg**, og velg deretter den relaterte koblingen.

    Siden **Rapportoppsettsvalg** viser alle rapportene som er tilgjengelige i selskapet som er angitt i feltet **Selskapsnavn** øverst på siden.
2. Angi selskapet du vil opprette rapportoppsettet i, i **Selskap**-feltet.
3. Velg raden for rapporten du vil bruke opprette oppsettet for, og velg deretter handlingen **Egendefinerte oppsett**.  

   Siden **Egendefinerte rapportoppsett** vises og inneholder en oversikt over alle de egendefinerte oppsettene som er tilgjengelige for den valgte rapporten.
4. Hvis du vil opprette en kopi av et eksisterende egendefinert oppsett, velger du det eksisterende egendefinerte oppsettet fra listen, og deretter velger du handlingen **Kopier**.  

   Kopien av det egendefinerte oppsettet vises på siden **Egendefinerte rapportoppsett** og inneholder ordene *Kopi av* i **Beskrivelse**-feltet.
5. Hvis du vil legge til et nytt egendefinert oppsett som er basert på et innebygd oppsett, gjør du følgende trinn:  
   1. Velg handlingen **Ny**. Siden **Sett inn innebygd oppsett for en rapport** vises. Feltene **ID** og **Navn** fylles ut automatisk.
   2. Hvis du vil legge til en egendefinert Word-rapportoppsettype, merker du av for **Sett inn Word-oppsett**.
   3. Hvis du vil legge til en egendefinert RDLC-rapportoppsettype, merker du av for **Sett inn RDLC-oppsett**.
   4. Velg **OK**-knappen.  

    Det nye egendefinerte oppsettet vises på siden **Egendefinerte rapportoppsett**. Hvis et nytt oppsett er basert på et innebygd oppsett, står det **Kopi av innebygd oppsett** i **Beskrivelse**-feltet. Hvis det ikke finnes noe innebygd oppsett for rapporten, står det **Nytt oppsett** i **Beskrivelse**-feltet, som angir at det egendefinerte oppsettet er tomt.
6. **Selskapsnavn**-feltet er som standard tomt, noe som betyr at det egendefinerte oppsettet er tilgjengelig for rapporten i alle selskaper. Hvis du vil gjøre det egendefinerte oppsettet bare tilgjengelig i et bestemt selskap, velger du **Rediger**, og deretter angir ønsket selskap i **Selskapsnavn**-feltet.

Det egendefinerte oppsettet er opprettet. Du kan nå endre det egendefinerte oppsettet etter behov.

> [!TIP]
> Du kan eksportere rapportresultatene til en Excel-fil for å vise hele datasettet, inkludert alle kolonner, men uten oppsettet. Excel-filen kan hjelpe deg med å validere at rapporten returnerer de forventede dataene eller diagnostisere problemer. Hvis du vil ha mer informasjon, kan du se [Analyser rapportdata med Excel](report-analyze-excel.md).

## <a name="modifying-a-custom-layout"></a><a name="ModifyCustomLayout"></a>Endre et egendefinert oppsett

Når du skal endre et rapportoppsett, du må først eksportere rapportoppsettet som en fil til en plassering på datamaskinen eller nettverket. Deretter åpner du det eksporterte dokumentet og foretar endringene. Når du er ferdig å foreta endringer, importerer du rapportoppsettet.

### <a name="to-modify-a-custom-layout"></a>Endre et egendefinert oppsett

1.  Du kan eksportere et egendefinert oppsett fra **Egendefinerte rapportoppsett**-siden. Hvis siden ikke allerede er åpen, kan du søke etter og åpne **Rapportoppsettsvalg**-siden, velge rapporten som har oppsettet du vil endre, og deretter velge handlingen **Egendefinerte oppsett**.  
2.  På siden **Egendefinerte rapportoppsett** velger du oppsettet som du vil endre, velger **Eksporter oppsett**-handlingen og velger deretter **Lagre** eller **Lagre som** for å lagre rapportoppsettsdokumentet på et sted på datamaskinen eller nettverket.  

3.  Åpne rapportoppsettdokumentet du lagret, og gjør deretter endringene.

      Hvis du endrer et Word-oppsett, kan du åpne oppsettsdokumentet i Word. Se neste del [Endre rapportoppsettet](ui-how-create-custom-report-layout.md#MakeChangesToLayout) hvis du vil ha mer informasjon om redigering.

      RDLC-rapportoppsett er mer avansert enn Word-rapportoppsett. Hvis du vil ha mer informasjon om hvordan du endrer et RDLC-rapportoppsett, kan du se [Utforme RDLC-rapportoppsett](/dynamics-nav/Designing-RDLC-Report-Layouts).

      Husk å lagre endringene når du er ferdig.

4.  Gå tilbake til **Egendefinerte rapportoppsett**-siden, velg rapportoppsettet som du har eksportert eller endret, og velg deretter **Importer oppsett**-handlingen.  

5. I dialogboksen **Importer** velger du **Velg** for å finne og velge rapportoppsettdokumentet som er endret, og velger deretter **Åpne**.

> [!IMPORTANT]
> Husk å importere rapportoppsettdokumentet du endret. Hvis ikke vil ikke det nye rapportoppsettet være tilgjengelig.

##  <a name="create-and-modify-custom-report-layouts"></a><a name="MakeChangesToLayout"></a> Opprette og endre et egendefinert rapportoppsett

For å foreta generelle formaterings- og oppsettsendringer, for eksempel endre skrift, legge til eller endre en tabell eller fjerne et datafelt, bruker du bare de grunnleggende redigeringsfunksjonene i Word, som du gjør med et Word-dokument.

Hvis du utformer et Word-rapportoppsett fra grunnen av eller legger til nye datafelt, begynner du med å legge til en tabell som inneholder rader og kolonner som omsider skal inneholde datafeltene.

> [!TIP]  
> Vis tabellrutenettet, slik at du kan se cellegrensene i tabellen. Husk å skjule rutenettet når du er ferdig å redigere. Hvis du vil vise eller skjule tabellrutenett, merker du tabellen. Under **Oppsett** i kategorien **Tabell** velger du deretter **Vis rutenettlinjer**.

### <a name="embedding-fonts-in-word-layouts-for-consistency"></a>Bygge inn skrifter i Word-oppsett for konsekvens

Hvis du vil sikre at rapporter alltid vises og skrives ut med de tiltenkte skriftene, uansett hvor brukere åpner eller skriver ut rapporter, kan du bygge inn skrifter i Word-dokumentet. Innebygde skrifter kan imidlertid øke størrelsen på Word-filer betydelig. Hvis du vil ha mer informasjon om innebygging av skrifter i Word, se [Bygge inn skrifter i Word, PowerPoint eller Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

###  <a name="removing-label-and-data-fields-in-word-layouts"></a><a name="RemoveField"></a> Fjerne etikett- og datafelt i Word-oppsett

 Etikett- og datafelt i en rapport er i innholdskontroller i Word. Den følgende illustrasjonen viser en innholdskontroll når den er valgt i Word-dokumentet.  

 ![Innholdskontroll for felt i Word-rapportoppsett.](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 Navnet på etiketten eller datafeltnavnet vises i innholdskontrollen. I dette eksemplet er feltnavnet CompanyAddr1.  

### <a name="to-remove-a-label-or-data-field"></a>Fjerne en etikett eller et datafelt  

1. Høyreklikk feltet som du vil slette, og velg deretter **Fjern innholdskontroll**.  

     Innholdskontrollen fjernes, men feltnavnet blir stående som tekst.  

2. Slett den gjenstående teksten etter behov.  

### <a name="adding-data-fields"></a>Legge til datafelt

Å legge til datafelt fra et rapportdatasett er mer avansert og krever noe kjennskap til rapportdatasettet. Hvis du vil ha informasjon om å legge til felt for data, etiketter og bilder, kan du se [Legge til felt i et Word-rapportoppsett](ui-how-add-fields-word-report-layout.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Håndtere rapportoppsett](ui-manage-report-layouts.md)  
[Endre gjeldende rapportoppsett](ui-how-change-layout-currently-used-report.md)  
[Importere og eksportere en egendefinert rapport eller et egendefinert dokumentoppsett](ui-how-import-and-export-report-layout.md)  
[Arbeide med rapporter, satsvise jobber og XML-porter](ui-work-report.md)  
[Klargjøre Financial Reporting med kontoskjemaer og kontokategorier](bi-how-work-account-schedule.md) 
[Forretningsintelligens](bi.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]