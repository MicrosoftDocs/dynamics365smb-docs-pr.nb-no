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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 01e831ddddeffe6a64c6de24b4cd8c1b94bad9c3
ms.sourcegitcommit: a88d1e9c0ab647cb8d9d81d32c0bdc82843f4145
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/31/2019
ms.locfileid: "1796898"
---
# <a name="posting-sales"></a>Bokføre salg
I **Bokføringsgruppe** i et salgsdokument, kan du velge mellom følgende bokføringsfunksjoner:

* **Bokfør**
* **Kontrollrapport**
* **Bokfør og Send**
* **Bokfør og skriv ut**
* **Bokfør og send e-post**
* **Massebokfør**
* **Forhåndsvis bokføring**

Når du har fylt ut alle linjene og angitt alle opplysningene i ordren, kan du bokføre den. Dette oppretter en levering og en faktura.

Når en ordre bokføres, oppdateres kundens konto, finans og varepostene.

For hver ordre opprettes en salgspost i **Finanspost**-tabellen. Det opprettes også en post på leverandørens konto i **Kundepost**-tabellen, og en finanspost opprettes i den relevante kundekontoen. I tillegg kan bokføring av bestillingen resultere i en mva-post og en finanspost for rabattbeløpet. Om en rabattpost skal bokføres, avhenger av innholdet i feltet **Rabattbokføring** på **Salgsoppsett**-siden.

For hver ordrelinje opprettes det en varepost i tabellen **Varepost** (hvis salgslinjen inneholder varenumre), eller det opprettes en finanspost i tabellen **Finanspost** (hvis salgslinjen inneholder en finanskonto). I tillegg til dette registreres alltid ordrer i tabellene **Følgeseddelhode** og **Salgsfakturahode**.

> [!IMPORTANT]  
>   Når du bokfører en ordre, kan du opprette både en følgeseddel og en faktura. Dette kan gjøres samtidig eller hver for seg. Du kan også opprette en dellevering eller en delfaktura ved å fylle ut feltene **Levere (antall)** og **Fakturer (antall)** på hver enkelt ordrelinje før du bokfører. Merk at du ikke kan opprette en faktura for noe som ikke er levert. Det vil si at for å kunne fakturere, er det nødvendig at du på forhånd har registrert en levering, eller at du velger å levere og fakturere samtidig.

Når bokføringen er utført, fjernes de bokførte salgslinjene fra bestillingen. En melding viser når bokføringen er gjennomført. Etter dette vil du kunne se de bokførte postene på de forskjellige sidene som inneholder bokførte poster, for eksempel sidene **Kundeposter**, **Finansposter**, **Vareposter**, **Bokførte følgesedler** og **Bokført salgsfaktura**.  

## <a name="see-also"></a>Se også

[Salg](sales-manage-sales.md)  
[Sende dokumenter i e-post](ui-how-send-documents-email.md)  
[Korrigere eller annullere ubetalte salgsfakturaer](sales-how-correct-cancel-sales-invoice.md)  
[Bruke Fortell meg til å finne funksjoner og informasjon](ui-search.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
