---
title: "Opprette inngående dokument fra dokumenter | Microsoft-dokumentasjon"
description: "Du kan opprette poster for inngående dokumenter, for eksempel e-fakturaer, og behandle OCR-oppgaver, e-handel og dokumentutveksling."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 44105a8bf043795d60ecab135c6a8b61712b4f60
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-incoming-document-records-directly-from-documents-and-entries"></a>Opprette innkommende dokumentposter direkte fra dokumenter og poster
Du kan lagre eksterne forretningsdokumenter i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved å knytte dokumentfilene til de relaterte innkommende dokumentpostene. Hvis dokumentet, for eksempel en kjøpsfaktura, ikke ble opprettet som en innkommende dokumentpost, kan du likevel opprette og koble en innkommende dokumentpost til det senere. Du kan også knytte inngående dokumentfiler til bokførte kjøps- og salgsdokumenter og til leverandør-, kunde- og finansposter ved hjelp av faktaboksen **Inngående dokumentfiler**, for eksempel i vinduet **Bokførte kjøpsfakturaer** og **Leverandørposter**.

Fra vinduene **Kontoplan** og **Finansposter** kan du bruke søkefunksjonen til å finne finansposter for bokførte kjøps- og salgsdokumenter som ikke har innkommende dokumentposter, og deretter sentralt koble eksisterende poster eller opprette nye med vedlagte dokumentfiler. Hvis du vil ha mer informasjon, kan du se [Finne bokførte dokumenter uten innkommende dokumentposter](across-how-find-posted-documents-without-income-document-records.md).

De følgende fremgangsmåtene viser hvordan du knytter en fil til en eksisterende kjøpsfaktura som ikke ble opprettet fra en innkommende dokumentpost, og hvordan du knytter en fil til en leverandørpost. Å knytte en en fil til bokførte kjøps- eller salgsdokumenter fungerer på en lignende måte.

## <a name="to-create-and-connect-an-incoming-document-record-from-a-purchase-invoice"></a>Slik oppretter og kobler du en innkommende dokumentpost fra en kjøpsfaktura:
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.
2. Velg linjen for en kjøpsfaktura du vil knytte en fil til, og velg deretter handlingen **Opprett inngående dokument fra fil**.
3. Du kan eventuelt velge linjen for en kjøpsfaktura du vil knytte en fil til, og deretter velge handlingen **Tilknytt fil**.
4. I vinduet **Sett inn fil** velger du filen som representerer det innkommende dokumentet, og deretter velger du **Åpne**- knappen.

## <a name="to-create-and-connect-an-incoming-document-record-from-a-vendor-ledger-entry"></a>Slik oppretter og kobler du en innkommende dokumentpost fra en leverandørpost:
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Leverandørposter**, og velg deretter den relaterte koblingen.
2. Velg en linje for en leverandørpost du vil knytte en fil til, og velg deretter handlingen **Opprett inngående dokument fra fil**.
3. Du kan eventuelt velge en linje for en leverandørpost du vil knytte en fil til, og deretter velge handlingen **Tilknytt fil**.
4. I vinduet **Sett inn fil** velger du filen som representerer det innkommende dokumentet, og deretter velger du **Åpne**- knappen.

## <a name="to-remove-a-connection-from-an-incoming-document-record-to-a-posted-document"></a>Slik fjerner du tilkoblingen fra en innkommende dokumentpost til et bokført dokument:
Du kan fjerne filvedlegg fra ikke-bokførte dokumenter når som helst ved å slette den relaterte innkommende dokumentposten. Hvis dokumentet er bokført, må du først fjerne tilkoblingen fra den innkommende dokumentposten.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Inngående dokumenter**, og velg deretter den relaterte koblingen.
2. Velg linjen for en inngående dokumentpost som er koblet til et bokført dokument du vil fjerne, og velg deretter handlingen **Fjern referanse til post**.

Tilkoblingen til det bokførte dokumentet fjernes. Nå kan du fortsette med å koble en annen innkommende dokumentpost til det bokførte dokumentet, som beskrevet i dette emnet.

## <a name="see-also"></a>Se også
[Behandle inngående dokumenter](across-process-income-documents.md)  
[Inngående dokumenter](across-income-documents.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

