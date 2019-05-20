---
title: Motta og konvertere elektroniske dokumenter | Microsoft-dokumentasjon
description: Du kan motta elektroniske dokumenter direkte fra handelspartnere eller fra en OCR-tjeneste.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a121363d04de0aea69e423df8de5c50c24744061
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1252185"
---
# <a name="receive-and-convert-electronic-documents"></a>Motta og konvertere elektroniske dokumenter
Den generelle versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] kan motta elektroniske fakturaer og kreditnotaer i PEPPOL-format, som støttes av de største leverandørene av dokumentutvekslingstjenester. Hvis du vil motta en faktura fra en leverandør som et elektronisk PEPPOL-dokument, kan du behandle dokumentet på siden Inngående dokumenter for å konvertere det til en kjøpsfaktura eller finanskladd i [!INCLUDE[d365fin](includes/d365fin_md.md)].

 I tillegg til å motta elektroniske dokumenter direkte fra handelspartnere, kan du motta elektroniske dokumenter fra en OCR-tjeneste som har gjort om PDF- eller bildefiler til elektroniske dokumenter.  

 Før du kan motta elektroniske dokumenter gjennom dokumentutvekslingstjenesten, må du definere forskjellige hoveddata, for eksempel firmainformasjon, leverandører, varer og enheter. Disse brukes til å identifisere forretningspartnere og elementer ved konvertering av data i elementer i den innkommende dokumentfilen til felt i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du vil ha mer informasjon, kan du se [Konfigurere en dokumentutvekslingstjeneste](across-how-to-set-up-a-document-exchange-service.md).  

 Før du kan motta elektroniske dokumenter gjennom OCR-tjenesten, må du sette opp og aktiverer den forhåndskonfigurerte tjenestetilkoblingen. Hvis du vil ha mer informasjon, kan du se [Konfigurere inngående dokumenter](across-how-setup-income-documents.md).  

 Trafikk for elektroniske dokumenter inn og ut av [!INCLUDE[d365fin](includes/d365fin_md.md)] administreres av jobbkøfunksjonen. Før du kan motta elektroniske dokumenter, må relevant jobbkø være startet.  

 Du kan enten starte konverteringen av elektroniske dokumenter manuelt, slik det er beskrevet i denne fremgangsmåten, eller du kan aktivere en arbeidsflyt til å konvertere elektroniske dokumenter automatisk når de mottas. Den generelle versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] inneholder en arbeidsflytmal, *Arbeidsflyten Fra innkommende elektronisk via OCR til Åpne kjøpsfakturaer*, som er klar til å bli kopiert til en arbeidsflyt og aktivert. Hvis du vil ha mer informasjon, kan du se [Arbeidsflyt](across-workflow.md).  

> [!NOTE]  
>  Når du konverterer elektroniske dokumenter som er mottatt fra OCR-tjenesten, til dokumenter eller kladdelinjer i [!INCLUDE[d365fin](includes/d365fin_md.md)], summeres flere linjer i kildedokumentet på én linje. Enkeltlinjen kommer til å være av typen Finanskonto, og feltene **Beskrivelse** og **Nr.** på finanskonto. -feltene kommer til å være tomme. Verdien i **Beløp**-feltet kommer til å være lik det totale beløpet ekskl. mva. på alle linjene i kildedokumentet.  
>   
>  Forsikre deg om at **Beskrivelse**- og **Nr.** -feltene er utfylt, og velg **Tilordne tekst til konto**-knappen på siden **Inngående dokumenter** for å definere at en bestemt fakturatekst alltid er tilordnet en bestemt debet- eller kreditkonto i finans. Videre utfylles **Beskrivelse**-feltet i dokument- eller kladdelinjer som er opprettet fra et elektronisk dokument for kunden eller leverandøren, med den aktuelle teksten og **Nr.** for finanskonto. -feltet med den aktuelle kontoen.  
>   
>  I stedet for tilordning til en finanskonto, kan du tilordne til en bankkonto. Dette er praktisk, for eksempel for elektroniske dokumenter for utgifter som allerede er betalt, der du vil opprette en finanskladdelinje som er klar til å bokføre på en bankkonto.  

 Følgende prosedyre beskriver hvordan du mottar en leverandørfaktura og konverterer den til en kjøpsfaktura i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Fremgangsmåten er den samme når du konverterer en leverandørfaktura til en finanskladdelinje.  

### <a name="to-receive-and-convert-an-electronic-invoice-to-a-purchase-invoice"></a>Slik mottar og konverterer du en elektronisk faktura til en kjøpsfaktura  

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Inngående dokumenter**, og velg deretter den relaterte koblingen.  

2.  Velg linjen for den innkommende dokumentposten som representerer en ny innkommende elektronisk faktura, og velg deretter **Rediger** under **Behandle** i kategorien **Hjem**.  

     På siden **Kort for inngående dokument** blir den relaterte XML-filen koblet til, og de fleste feltene er forhåndsutfylt med informasjon fra den elektroniske fakturaen. Hvis du vil ha mer informasjon, kan du se [Opprette innkommende dokumentposter](across-how-create-income-document-records.md).  

3.  I feltet **Datautvekslingstype** velger du **PEPPOL – faktura** eller **OCR – faktura**, avhengig av kilden til det elektroniske dokumentet.  

4.  Hvis du vil tilordne tekst på leverandørfakturaen til en bestemt debetkonto, velger du **Tilordne tekst til konto** i fanen **Handlinger** i gruppen **Generelt**, og deretter fyller du ut siden **Tekst-til-konto-tilordning**.  

5.  I kategorien **Handlinger**, under **Generelt**, velger du **Opprett dokument**.  

     Det blir opprettet en kjøpsfaktura i [!INCLUDE[d365fin](includes/d365fin_md.md)] basert på informasjonen i det elektroniske dokumentet.  

     Eventuelle valideringsfeil, vanligvis knyttet til feil eller manglende hoveddata i [!INCLUDE[d365fin](includes/d365fin_md.md)], vises i hurtigfanen **Feilmeldinger**.  

## <a name="see-also"></a>Se også  
[Administrere skyldige beløp](payables-manage-payables.md)  
[Inngående dokumenter](across-income-documents.md)  
[Konfigurere sending og mottak av elektroniske dokumenter](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Utveksle data elektronisk](across-data-exchange.md)   
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  
