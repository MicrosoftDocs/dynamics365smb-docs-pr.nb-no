---
title: Bokføre salgsdokumenter | Microsoft Docs
description: Lær om de forskjellige bokføringsfunksjonene for å bokføre salgsdokumenter og hvordan du kan oppdatere bokførte dokumenter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 01/13/2020
ms.author: sgroespe
ms.openlocfilehash: 842aaeeb5665e8e02ef6873dd2210e03e415aade
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/14/2020
ms.locfileid: "2953974"
---
# <a name="posting-sales"></a>Bokføre salg
I menyen **Bokføring** i et salgsdokument kan du velge mellom følgende bokføringsfunksjoner:

* **Bokfør**
* **Bokfør og ny**
* **Bokfør og Send**
* **Forhåndsvis bokføring**
* **Fakturakladd**
* **Proformafaktura**
* **Kontrollrapport**

Når du har fylt ut alle linjene og angitt alle opplysningene i ordren, kan du bokføre den. Dette oppretter en levering og en faktura.

Når en ordre bokføres, oppdateres kundens konto, finans og varepostene.

For hver ordre opprettes en salgspost i **Finanspost**-tabellen. Det opprettes også en post på leverandørens konto i **Kundepost**-tabellen, og en finanspost opprettes i den relevante kundekontoen. I tillegg kan bokføring av bestillingen resultere i en mva-post og en finanspost for rabattbeløpet. Om en rabattpost skal bokføres, avhenger av innholdet i feltet **Rabattbokføring** på **Salgsoppsett**-siden.

For hver ordrelinje opprettes det en varepost i tabellen **Varepost** (hvis salgslinjen inneholder varenumre), eller det opprettes en finanspost i tabellen **Finanspost** (hvis salgslinjen inneholder en finanskonto). I tillegg til dette registreres alltid ordrer i tabellene **Følgeseddelhode** og **Salgsfakturahode**.

> [!IMPORTANT]  
>   Når du bokfører en ordre, kan du opprette både en følgeseddel og en faktura. Dette kan gjøres samtidig eller hver for seg. Du kan også opprette en dellevering eller en delfaktura ved å fylle ut feltene **Levere (antall)** og **Fakturer (antall)** på hver enkelt ordrelinje før du bokfører. Merk at du ikke kan opprette en faktura for noe som ikke er levert. Det vil si at for å kunne fakturere, er det nødvendig at du på forhånd har registrert en levering, eller at du velger å levere og fakturere samtidig.

Du kan enten bokføre eller bokføre og skrive ut. Hvis du velger å bokføre og skrive ut, skrives det ut en rapport når ordren bokføres. Du kan også velge funksjonen **Massebokfør** for å bokføre flere bestillinger samtidig. Hvis du vil ha mer informasjon, se [Bokføre flere dokumenter samtidig](ui-batch-posting.md).

Når bokføringen er utført, fjernes de bokførte salgslinjene fra bestillingen. En melding viser når bokføringen er gjennomført. Etter dette vil du kunne se de bokførte postene på de forskjellige sidene som inneholder bokførte poster, for eksempel sidene **Kundeposter**, **Finansposter**, **Vareposter**, **Bokførte følgesedler** og **Bokført salgsfaktura**.  

Du kan redigere bestemte felt på bokførte salgsdokumenter, for eksempel **Pakkesporingsnr**. -feltet. Hvis du vil ha mer informasjon, kan du se [Redigere bokførte dokumenter](across-edit-posted-document.md).

## <a name="see-related-training-at-microsoft-learnlearnmodulesship-invoice-items-dynamics-365-business-centralindex"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/ship-invoice-items-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)  
[Bokføre flere dokumenter samtidig](ui-batch-posting.md)  
[Redigere bokførte dokumenter](across-edit-posted-document.md)  
[Sende dokumenter i e-post](ui-how-send-documents-email.md)  
[Korrigere eller annullere ubetalte salgsfakturaer](sales-how-correct-cancel-sales-invoice.md)  
[Finne sider og informasjon med Fortell meg](ui-search.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
