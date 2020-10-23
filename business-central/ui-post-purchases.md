---
title: Forstå hvordan du bokfører kjøpsdokumenter | Microsoft-dokumentasjon
description: Lær om de forskjellige bokføringsfunksjonene for å bokføre kjøpsdokumenter og hvordan du kan oppdatere bokførte dokumenter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 687a63e1d53db4c120070de0a353b3501a335d27
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914938"
---
# <a name="posting-purchases"></a>Bokføre kjøp
I et kjøpsdokument kan du velge mellom følgende bokføringshandlinger:

* **Bokfør**
* **Forhåndsvis bokføring**
* **Bokfør og skriv ut**
* **Kontrollrapport**
* **Massebokfør**

Når en et kjøpsdokument bokføres, oppdateres leverandørens konto, finans og vareposter, og ressurspostene blir oppdatert.

For hvert kjøpsdokument opprettes det en kjøpspost i tabellen **Finanspost**. Det opprettes også en post på leverandørens konto i **Leverandørpost**-tabellen, og en finanspost opprettes i den relevante samlekontoen. I tillegg kan bokføring av kjøpet resultere i en mva-post og en finanspost for rabattbeløpet. Om en rabattpost skal bokføres, avhenger av innholdet i feltet  **Rabattbokføring** på siden **Kjøpsoppsett**.

Følgende poster vil bli opprettet for hver kjøpslinje:
- En post i tabellen **Varepost** hvis kjøpslinjen er av typen **Vare**.
- En post i tabellen **Finanspost** hvis kjøpslinjene er av typen **Finanskonto**.
- En post i tabellen **Ressurspost** hvis kjøpslinjen er av typen **Ressurs**.

I tillegg registreres alltid kjøpsdokumenter i tabellene **Mottakshode** og **Kjøpsfakturahode**.

Før du starter bokføringen, kan du skrive ut en kontrollrapport som viser alle opplysningene i bestillingen, samt eventuelle feil. Hvis du vil skrive ut rapporten, velger du **Bokføring** og deretter **Kontrollrapport**.

> [!IMPORTANT]  
>   Når du bokfører en bestilling for varer, kan du opprette både et mottak og en faktura. Dette kan gjøres samtidig, eller hver for seg. Du kan også opprette et delvis mottak og en delfaktura ved å fylle ut feltene **Motta (antall)** og **Fakturer (antall)** på de enkelte bestillingsordrelinjene før du bokfører. Legg merke til at du ikke kan opprette en faktura for noe som ikke er mottatt. Det vil si at for å kunne fakturere, må du på forhånd ha registrert et mottak, eller du må velge å motta og fakturere samtidig.

Du kan enten bokføre eller bokføre og skrive ut. Hvis du velger å bokføre og skrive ut, skrives det ut en rapport når ordren bokføres. Du kan også velge funksjonen **Massebokfør** for å bokføre flere bestillinger samtidig. Hvis du vil ha mer informasjon, se [Bokføre flere dokumenter samtidig](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Vise poster
Når bokføringen er utført, fjernes de bokførte kjøpslinjene fra bestillingen. En melding viser når bokføringen er gjennomført. Etter dette vil du kunne se de bokførte postene på de forskjellige sidene som inneholder bokførte poster, for eksempel sidene **Leverandørposter**, **Finansposter**, **Vareposter**, **Ressursposter**, **Kjøpsmottak** og **Bokførte kjøpsfakturaer**.

I de fleste tilfeller kan du åpne poster fra det berørte kortet eller dokumentet. På siden **Leverandørkort** velger du for eksempel handlingen **Poster**.

## <a name="editing-ledger-entries"></a>Redigere poster
Du kan redigere bestemte felt på bokførte kjøpsdokumenter, for eksempel feltet **Betalingsreferanse**. Hvis du vil ha mer informasjon, kan du se [Redigere bokførte dokumenter](across-edit-posted-document.md). Hvis du vil ha mer kritiske felt som påvirker revisjonssporingen, må du tilbakeføre eller angre bokføringen. Hvis du vil ha mer informasjon, kan du se [Tilbakeføre kladdebokføringer og angre mottak/leveringer](finance-how-reverse-journal-posting.md).

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/receive-invoice-dynamics-d365-business-central/index)

## <a name="see-also"></a>Se også
[Redigere bokførte dokumenter](across-edit-posted-document.md)  
[Bokføre flere dokumenter samtidig](ui-batch-posting.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Bokføre dokumenter og kladder](ui-post-documents-journals.md)  
[Korrigere eller annullere ubetalte kjøpsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Finne sider og informasjon med Fortell meg](ui-search.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
