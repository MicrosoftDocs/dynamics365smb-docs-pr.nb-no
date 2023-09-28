---
title: Bokføre salgsdokumenter
description: Lær om de forskjellige bokføringsfunksjonene for å bokføre salgsdokumenter og hvordan du kan oppdatere bokførte dokumenter.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: bholtorf
ms.search.form: '130, 142, 1350'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Bokføre salg

I menyen **Bokføring** i et salgsdokument kan du velge mellom følgende bokføringsfunksjoner:

* **Bokfør**
* **Bokfør og ny**
* **Bokfør og Send**
* **Forhåndsvis bokføring**
* **Massebokfør**
* **Kontrollrapport**

> [!NOTE]
> For salgsordrer kan du også se alternativer som er knyttet til funksjonene for forskuddsbetaling. Hvis du vil ha mer informasjon, kan du se [Fakturere forskuddsbetalinger](finance-invoice-prepayments.md).

Når du har fylt ut alle linjene og angitt alle opplysningene i ordren, kan du bokføre den. Dette oppretter en levering og en faktura.

Når en ordre bokføres, oppdateres kundens konto, finans og varepostene.

For hver ordre opprettes en salgspost i **Finanspost**-tabellen. Det opprettes også en post på leverandørens konto i **Kundepost**-tabellen, og en finanspost opprettes i den relevante kundekontoen. I tillegg kan bokføring av bestillingen resultere i en mva-post og en finanspost for rabattbeløpet. Om en rabattpost skal bokføres, avhenger av innholdet i feltet **Rabattbokføring** på **Salgsoppsett**-siden.

For hver ordrelinje opprettes det en varepost i tabellen **Varepost** (hvis salgslinjen inneholder varenumre), eller det opprettes en finanspost i tabellen **Finanspost** (hvis salgslinjen inneholder en finanskonto). I tillegg til dette registreres alltid ordrer i tabellene **Følgeseddelhode** og **Salgsfakturahode**.

[!INCLUDE [order-ship-invoice](includes/order-ship-invoice.md)]

Du kan enten bokføre eller bokføre og sende. Hvis du velger å bokføre og sende, genereres en PDF-fil som du deretter kan sende. Du kan også velge funksjonen **Massebokfør** for å bokføre flere bestillinger samtidig. Hvis du vil ha mer informasjon, se [Bokføre flere dokumenter samtidig](ui-batch-posting.md).

## Vise poster

Når bokføringen er utført, fjernes de bokførte salgslinjene fra bestillingen. En melding viser når bokføringen er gjennomført. Etter dette vil du kunne se de bokførte postene på de forskjellige sidene som inneholder bokførte poster, for eksempel sidene **Kundeposter**, **Finansposter**, **Vareposter**, **Bokførte følgesedler** og **Bokført salgsfaktura**.  

I de fleste tilfeller kan du åpne poster fra det berørte kortet eller dokumentet. På siden **Kundekort** velger du for eksempel handlingen **Poster**.

## Redigere poster

Du kan redigere bestemte felt på bokførte kjøpsdokumenter, for eksempel **Pakkesporingsnr.** -feltet. Hvis du vil ha mer informasjon, kan du se [Redigere bokførte dokumenter](across-edit-posted-document.md). Hvis du vil ha mer kritiske felt som påvirker revisjonssporingen, må du tilbakeføre eller angre bokføringen. Hvis du vil ha mer informasjon, kan du se [Tilbakeføre kladdebokføringer og angre mottak/leveringer](finance-how-reverse-journal-posting.md).

## Se også

[Salg](sales-manage-sales.md)  
[Bokfør flere dokumenter samtidig](ui-batch-posting.md)  
[Redigere bokførte dokumenter](across-edit-posted-document.md)  
[Sende dokumenter i e-post](ui-how-send-documents-email.md)  
[Korrigere eller annullere ubetalte salgsfakturaer](sales-how-correct-cancel-sales-invoice.md)  
[Finne sider og informasjon med Fortell meg](ui-search.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]  
