---
title: Arbeide med egendefinerte og innebygde oppsett for rapporter og dokumenter | Microsoft-dokumentasjon
description: "Bruk rapportoppsett til å tilpasse dokumenter, for eksempel tilpasse skriften, logoen eller sideinnstillingene for PDF-filer du sender til kunder."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 445172287ae09032ff53e02d0e64dc967456a7bb
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="managing-report-and-document-layouts"></a>Administrere rapport- og dokumentoppsett
Et rapportoppsett styrer innholdet og formatet for rapporten, blant annet hvilke datafelt i et rapportdatasett som skal vises i rapporten, hvordan de er ordnet, samt tekststil, bilder og mer. Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du endre oppsettet som skal brukes i en rapport, opprette nytt oppsett eller endre eksisterende oppsett.

> [!NOTE]  
>   I [!INCLUDE[d365fin](includes/d365fin_md.md)] dekker betegnelsen «rapport» også eksternt rettede dokumenter, for eksempel salgsfakturaer og ordrebekreftelser som du sender til kunder som PDF-filer.

Et rapportoppsett brukes især til å konfigurere følgende:

* Etikett- og datafeltene som skal tas med fra datasettet for [!INCLUDE[d365fin](includes/d365fin_md.md)]-rapporten.
* Tekstformatet, for eksempel skrifttype, størrelse og farge.
* Selskapets logo og plasseringen.
* Generelle sideinnstillinger, for eksempel marger og bakgrunnsbilder.

En [!INCLUDE[d365fin](includes/d365fin_md.md)]-rapport kan defineres med flere rapportoppsett, som du kan bytte mellom etter behov. Du kan bruke ett av de innebygde rapportoppsettene, eller du kan opprette egendefinerte rapportoppsett og tilordne dem til rapportene etter behov. Hvis du vil ha mer informasjon, kan du se [Opprette en egendefinert rapport eller et egendefinert dokumentoppsett](ui-how-create-custom-report-layout.md).

Det finnes to typer rapportoppsett som du kan bruke i rapporter: Word og RDLC.

## <a name="word-report-layout-overview"></a>Oversikt over rapportoppsett for Word
Et Word-rapportoppsett er basert på et Word-dokument (DOCX-filtypen). Rapportoppsett for Word lar deg utforme rapportoppsett ved hjelp av Microsoft Word 2013 eller nyere. Et rapportoppsettet for Word bestemmer rapportens innhold – kontrollere hvordan innholdselementer ordnes og hvordan de ser ut. I et Word-rapportoppsettdokument brukes vanligvis tabeller til å ordne innhold, der cellene kan inneholde datafelt, tekst eller bilder.

 ![Eksempel på et rapportoppsettsdokument i Word for NAV](media/nav_wordreportlayout_edit_in_word_example.png "NAV_WordReportLayout_Edit_In_Word_Example")  

## <a name="rdlc-layout-overview"></a>Oversikt over RDLC-oppsett
RDLC-oppsett er basert på oppsett for rapportdefinisjon for klient (filtypen RDLC eller RDL). Disse oppsettene er opprettet og endret ved hjelp av SQL Server Report Builder. Konseptet for utforming for RDLC ligner på Word-oppsett, der oppsettet definerer det generelle formatet for rapporten og bestemmer feltene fra datasettet som skal inkluderes. Å utforme RDLC-oppsett er en mer avansert oppgave enn å utforme Word-oppsett. Hvis du vil ha mer informasjon, kan du se [Utforme RDLC-rapportoppsett](https://msdn.microsoft.com/en-us/dynamics-nav/designing-rdlc-report-layouts).

## <a name="built-in-and-custom-report-layouts"></a>Innebygde og egendefinerte rapportoppsett
[!INCLUDE[d365fin](includes/d365fin_md.md)] inneholder flere innebygde oppsett. Innebygde oppsett er forhåndsdefinerte oppsett som er utformet for bestemte rapporter. [!INCLUDE[d365fin](includes/d365fin_md.md)]-rapporter har en innebygget utforming som et RDLC-rapportoppsett, Word-rapportoppsett, eller i noen tilfeller begge. Du kan ikke endre innebygde rapportoppsett fra [!INCLUDE[d365fin](includes/d365fin_md.md)], men du bruker dem som et utgangspunkt for å lage egendefinerte rapportoppsett.

Egendefinerte oppsett er rapportoppsett du utformer for å endre utseendet på en rapport. Vanligvis oppretter du et egendefinert oppsett basert på et innebygd oppsett, men du kan opprette dem fra grunnen av eller fra en kopi av et eksisterende egendefinert oppsett. Egendefinerte oppsett gjør at du kan ha flere oppsett for samme rapport som du kan bytte mellom etter behov. Du kan for eksempel ha ulike oppsett for hvert selskap i [!INCLUDE[d365fin](includes/d365fin_md.md)], eller du kan ha ulike oppsett for samme selskap for bestemte anledninger eller hendelser, for eksempel en kampanje eller julehøytiden.

## <a name="deciding-whether-to-use-a-word-or-rdlc-report-layout"></a>Avgjøre om du skal bruke et Word- eller RDLC-rapportoppsett
Et rapportoppsett kan være basert på et Word-dokument eller en RDLC-fil. Når du skal velge mellom et Word-rapportoppsett og et RDLC-rapportoppsett, avhenger valget av hvordan du vil at den genererte rapporten skal se ut, og hvor god kjennskap du har til Word og SQL Server Report Builder.

Generelle utformingskonsepter for Word og RDLC oppsett er svært like. Hver type har imidlertid visse utformingsfunksjoner som påvirker hvordan den genererte rapporten vises i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dette betyr at Word-rapportoppsettet og RDLC-rapportoppsettet kan gi ulike utseender i samme rapport.

Prosessen for å definere Word-rapportoppsett og RDLC-rapportoppsett i rapporter er den samme. Den viktigste forskjellen er måten du endrer oppsett på. Word-rapportoppsettene er vanligvis enklere å opprette og endre enn RDLC-rapportoppsett, fordi du kan bruke Word. RDLC-rapportoppsett endres ved hjelp av SQL Server Report Builder, der målgruppen er mer erfarne brukere.

Hvis du vil ha informasjon om hvordan du endrer hvilket oppsett du vil bruke, kan du se [Endre gjeldende oppsett som skal brukes i en rapport](ui-how-change-layout-currently-used-report.md).

## <a name="see-also"></a>Se også
[Oppdatere rapport- og dokumentoppsett](ui-update-report-layouts.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Lage og endre en egendefinert rapport eller et egendefinert dokumentoppsett](ui-how-create-custom-report-layout.md)  
[Importere og eksportere en egendefinert rapport eller et egendefinert dokumentoppsett](ui-how-import-and-export-report-layout.md)  
[Sende dokumenter i e-post](ui-how-send-documents-email.md)  
[Arbeide med rapporter](ui-work-report.md)  

