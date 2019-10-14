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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0fccda42a69cd1d1d7129380518890fac5b8986c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315087"
---
# <a name="posting-purchases"></a>Bokføre kjøp
I **Bokføringsgruppe** i et kjøpsdokument, kan du velge mellom følgende bokføringsfunksjoner:

* **Bokfør**
* **Forhåndsvis bokføring**
* **Bokfør og skriv ut**
* **Kontrollrapport**
* **Massebokfør**

Når du har fylt ut alle linjene og angitt alle opplysningene i bestillingen, kan du bokføre den. Det vil si at du oppretter et mottak og en faktura.

Når en bestilling bokføres, oppdateres leverandørens konto, finans og varepostene.

For hver bestilling opprettes det en kjøpspost i **Finanspost**-tabellen. Det opprettes også en post på leverandørens konto i **Leverandørpost**-tabellen, og en finanspost opprettes i den relevante samlekontoen. I tillegg kan bokføring av bestillingen resultere i en mva-post og en finanspost for rabattbeløpet. Om en rabattpost skal bokføres, avhenger av innholdet i feltet  **Rabattbokføring** på siden **Kjøpsoppsett**.

For hver bestillingslinje opprettes det en varepost i tabellen **Varepost** (hvis bestillingslinjen inneholder varenumre), eller en finanspost i tabellen **Finanspost** (hvis bestillingslinjen inneholder en finanskonto). I tillegg registreres alltid bestillinger i tabellene **Mottakshode** og **Kjøpsfakturahode**.

Før du starter bokføringen, kan du skrive ut en kontrollrapport som viser alle opplysningene i bestillingen, samt eventuelle feil. Hvis du vil skrive ut rapporten, velger du **Bokføring** og deretter **Kontrollrapport**.

> [!IMPORTANT]  
>   Når du bokfører en bestilling, kan du opprette både et mottak og en faktura. Dette kan gjøres samtidig, eller hver for seg. Du kan også opprette et delvis mottak og en delfaktura ved å fylle ut feltene **Motta (antall)** og **Fakturer (antall)** på de enkelte bestillingsordrelinjene før du bokfører. Legg merke til at du ikke kan opprette en faktura for noe som ikke er mottatt. Det vil si at for å kunne fakturere, må du på forhånd ha registrert et mottak, eller du må velge å motta og fakturere samtidig.

Du kan enten bokføre eller bokføre og skrive ut. Hvis du velger å bokføre og skrive ut, skrives det ut en rapport når ordren bokføres. Du kan også velge funksjonen **Massebokfør** for å bokføre flere bestillinger samtidig. Hvis du vil ha mer informasjon, se [Bokføre flere dokumenter samtidig](ui-batch-posting.md).

Når bokføringen er utført, fjernes de bokførte kjøpslinjene fra bestillingen. En melding viser når bokføringen er gjennomført. Etter dette vil du kunne se de bokførte postene på de forskjellige sidene som inneholder bokførte poster, for eksempel sidene **Kundeposter**, **Finansposter**, **Vareposter**, **Kjøpsmottak** og **Bokførte kjøpsfakturaer**.

Du kan redigere bestemte felt på bokførte kjøpsdokumenter, for eksempel feltet **Betalingsreferanse**. Hvis du vil ha mer informasjon, kan du se [Redigere bokførte dokumenter](across-edit-posted-document.md).

## <a name="see-also"></a>Se også
[Redigere bokførte dokumenter](across-edit-posted-document.md)  
[Bokføre flere dokumenter samtidig](ui-batch-posting.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Bokføre dokumenter og kladder](ui-post-documents-journals.md)  
[Korrigere eller annullere ubetalte kjøpsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Finne sider og informasjon med Fortell meg](ui-search.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
