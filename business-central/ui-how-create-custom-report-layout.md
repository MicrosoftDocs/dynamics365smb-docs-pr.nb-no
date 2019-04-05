---
title: Lage og endre egendefinerte oppsett for rapporter og dokumenter | Microsoft-dokumentasjon
description: Finn ut hvordan du lager dine egne egendefinerte oppsett for å tilpasse utseendet på en rapport når den vises, skrives ut eller lagres.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 10/01/2018
ms.author: jswymer
ms.openlocfilehash: 2f86eb50422b5d780ea7a0be2f6798c0b2cc3bfd
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/19/2019
ms.locfileid: "852335"
---
# <a name="create-and-modify-a-custom-report-or-document-layout"></a>Opprette og endre et egendefinert rapportoppsett eller dokumentoppsett
En rapport har som standard et innebygd rapportoppsett, som kan være et RDLC-rapportoppsett, et innebygd Word-rapportoppsett eller i noen tilfeller begge typer. Du kan ikke endre innebygde oppsett. Du kan imidlertid opprette egendefinerte oppsett der du kan endre utseendet på rapporten når den vises, skrives ut eller lagres. Du kan opprette flere egendefinerte rapportoppsett for samme rapport og deretter bytte oppsettet som brukes av en rapport, etter behov.

> [!NOTE]  
>   I [!INCLUDE[d365fin](includes/d365fin_md.md)] dekker betegnelsen «rapport» også eksternt rettede dokumenter, for eksempel salgsfakturaer og ordrebekreftelser som du sender til kunder som PDF-filer.

Hvis du vil opprette et egendefinert oppsett, kan du lage en kopi av et eksisterende egendefinert oppsett eller legge til et nytt egendefinert oppsett, som i de fleste tilfeller er basert på et innebygd oppsett. Når du legger til et nytt egendefinert oppsett, kan du legge til en RDLC-rapportoppsettype, en Word-rapportoppsettype eller begge typer. Det nye egendefinerte oppsettet baseres automatisk på det innebygde oppsettet for rapporten hvis det er tilgjengelig. Hvis det ikke finnes noen innebygde oppsett for typen, opprettes et nytt, tomt oppsett, som du må endre og utforme fra grunnen av. Hvis du vil ha mer informasjon om RDLC- og Word-rapportoppsett, innebygde og egendefinerte oppsett og mer, kan du se [Håndtere rapportoppsett](ui-manage-report-layouts.md).  

## <a name="to-create-a-custom-layout"></a>Slik oppretter du et egendefinert oppsett
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rapportoppsettsvalg**, og velg deretter den relaterte koblingen.

    Siden **Rapportoppsettsvalg** viser alle rapportene som er tilgjengelige i selskapet som er angitt i feltet **Selskap** øverst på siden.
2. Angi selskapet du vil opprette rapportoppsettet i, i **Selskap**-feltet.
3. Velg raden for rapporten du vil bruke opprette oppsettet for, og velg deretter handlingen **Egendefinerte oppsett**.  
   Siden **Egendefinerte rapportoppsett** vises og inneholder en oversikt over alle de egendefinerte oppsettene som er tilgjengelige for den valgte rapporten.
4. Hvis du vil opprette en kopi av et eksisterende egendefinert oppsett, velger du det eksisterende egendefinerte oppsettet fra listen, og deretter velger du handlingen **Kopier**.  
   Kopien av det egendefinerte oppsettet vises på siden **Egendefinerte rapportoppsett** og inneholder ordene *Kopi av* i **Beskrivelse**-feltet.
5. Hvis du vil legge til et nytt egendefinert oppsett som er basert på et innebygd oppsett, gjør du følgende:  
   1. Velg handlingen **Ny**. Siden **Sett inn innebygd oppsett for en rapport** vises. Feltene **ID** og **Navn** fylles ut automatisk.
   2. Hvis du vil legge til en egendefinert Word-rapportoppsettype, merker du av for **Sett inn Word-oppsett**.
   3. Hvis du vil legge til en egendefinert RDLC-rapportoppsettype, merker du av for **Sett inn RDLC-oppsett**.
   4. Velg **OK**.  
      De nye egendefinerte oppsettene vises på siden **Egendefinerte rapportoppsett**. Hvis et nytt oppsett er basert på et innebygd oppsett, står det **Kopi av innebygd oppsett** i **Beskrivelse**-feltet. Hvis det ikke finnes noe innebygd oppsett for rapporten, står det **Nytt oppsett** i **Beskrivelse**-feltet, som angir at det egendefinerte oppsettet er tomt.
6. **Selskapsnavn**-feltet er som standard tomt, noe som betyr at det egendefinerte oppsettet er tilgjengelig for rapporten i alle selskaper. Hvis du vil gjøre det egendefinerte oppsettet bare tilgjengelig i et bestemt selskap, velger du **Rediger**, og deretter angir ønsket selskap i **Selskapsnavn**-feltet.

Det egendefinerte oppsettet er opprettet. Du kan nå endre det egendefinerte oppsettet etter behov.

## <a name="ModifyCustomLayout"></a>Endre et egendefinert oppsett
Når du skal endre et rapportoppsett, du må først eksportere rapportoppsettet som en fil til en plassering på datamaskinen eller nettverket, og åpne det eksporterte dokumentet i Word og gjøre endringene. Når du er ferdig å foreta endringer, importerer du rapportoppsettet.

### <a name="to-modify-a-custom-layout"></a>Endre et egendefinert oppsett
1.  Du kan eksportere et egendefinert oppsett fra **Egendefinerte rapportoppsett**-siden. Hvis siden ikke allerede er åpen, kan du søke etter og åpne **Rapportoppsettsvalg**-siden, velge rapporten som har oppsettet du vil endre, og deretter velge handlingen **Egendefinerte oppsett**.  
2.  På siden **Egendefinerte rapportoppsett** velger du oppsettet som du vil endre, velger **Eksporter oppsett**-handlingen og velger deretter **Lagre** eller **Lagre som** for å lagre rapportoppsettsdokumentet på et sted på datamaskinen eller nettverket.  

3.  Åpne rapportoppsettdokumentet du nettopp lagret, og gjør deretter endringene.

      Hvis du endrer et Word-oppsett, kan du åpne oppsettsdokumentet i Word. Se neste del [Endre rapportoppsettet](ui-how-create-custom-report-layout.md#MakeChangesToLayout) hvis du vil ha mer informasjon om redigering.

      RDLC-rapportoppsett er mer avansert enn Word-rapportoppsett. Hvis du vil ha mer informasjon om hvordan du endrer et RDLC-rapportoppsett, kan du se [Utforme RDLC-rapportoppsett](/dynamics-nav/Designing-RDLC-Report-Layouts).

      Husk å lagre endringene når du er ferdig.

4.  Gå tilbake til **Egendefinerte rapportoppsett**-siden, velg rapportoppsettet som du har eksportert eller endret, og velg deretter **Importer oppsett**-handlingen.  

5. I dialogboksen **Importer** velger du **Velg** for å finne og velge rapportoppsettsdokumentet, og velger deretter **Åpne**.

##  <a name="MakeChangesToLayout"></a>Gjøre endringer i et Word-rapportoppsett  
Når du skal foreta generelle formaterings- og oppsettsendringer, for eksempel endre skrift, legge til eller endre en tabell eller fjerne et datafelt, bruker du bare de grunnleggende redigeringsfunksjonene i Word, som du gjør med et Word-dokument.

Hvis du utformer et Word-rapportoppsett fra grunnen av eller legger til nye datafelt, begynner du med å legge til en tabell som inneholder rader og kolonner som omsider skal inneholde datafeltene.

> [!TIP]  
>  Vis tabellrutenettet, slik at du kan se cellegrensene i tabellen. Husk å skjule rutenettet når du er ferdig å redigere. Hvis du vil vise eller skjule tabellrutenett, merker du tabellen. Under **Oppsett** i kategorien **Tabell** velger du deretter **Vis rutenettlinjer**.

### <a name="embedding-fonts-in-word-layouts-for-consistency"></a>Bygge inn skrifter i Word-oppsett for konsekvens

Hvis du vil sikre at rapporter alltid vises og skrives ut med de tiltenkte skriftene, uansett hvor brukere åpner eller skriver ut rapporter, kan du bygge inn skrifter i Word-dokumentet. Vær imidlertid oppmerksom på at innebygde skrifter kan øke størrelsen på Word-filer betydelig. Hvis du vil ha mer informasjon om innebygging av skrifter i Word, se [Bygge inn skrifter i Word, PowerPoint eller Excel](https://support.office.com/en-us/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

###  <a name="RemoveField"></a> Fjerne etikett- og datafelt i Word-oppsett  
 Etikett- og datafelt i en rapport er i innholdskontroller i Word. Den følgende illustrasjonen viser en innholdskontroll når den er valgt i Word-dokumentet.  

 ![Innholdskontroll for felt i Word-rapportoppsett](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 Navnet på etiketten eller datafeltnavnet vises i innholdskontrollen. I dette eksemplet er feltnavnet CompanyAddr1.  

### <a name="to-remove-a-label-or-data-field"></a>Fjerne en etikett eller et datafelt  

1.  Høyreklikk feltet som du vil slette, og velg deretter **Fjern innholdskontroll**.  

     Innholdskontrollen fjernes, men feltnavnet blir stående som tekst.  

2.  Slett den gjenstående teksten etter behov.  

### <a name="adding-data-fields"></a>Legge til datafelt
Å legge til datafelt fra et rapportdatasett er mer avansert og krever noe kjennskap til rapportdatasettet. Hvis du vil ha informasjon om å legge til felt for data, etiketter og bilder, kan du se [Legge til felt i et Word-rapportoppsett](ui-how-add-fields-word-report-layout.md).  

###


## <a name="see-also"></a>Se også
[Håndtere rapportoppsett](ui-manage-report-layouts.md)  
[Endre gjeldende oppsett som skal brukes i en rapport](ui-how-change-layout-currently-used-report.md)  
[Importere og eksportere en egendefinert rapport eller et egendefinert dokumentoppsett](ui-how-import-and-export-report-layout.md)  
[Arbeide med rapporter og kjørsler](ui-work-report.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
