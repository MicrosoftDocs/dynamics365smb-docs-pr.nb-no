---
title: Bokfør kjøpsdokumenter
description: Lær om de forskjellige måtene for å bokføre kjøpsdokumenter og hvordan du oppdaterer bokførte dokumenter.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.form: ''
ms.date: 08/08/2022
ms.author: edupont
ms.openlocfilehash: 1bae22c83f1e7138fbfe16bb39aea3ad9d65d788
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531003"
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

Følgende poster blir opprettet for hver kjøpslinje, etter behov, i:

* **Varepost**-tabellen hvis kjøpslinjen er av typen **Vare**.
* **Finanspost**-tabellen hvis kjøpslinjen er av typen **Finanskonto**.
* **Ressurspost**-tabellen hvis kjøpslinjen er av typen **Ressurs**.

I tillegg registreres alltid kjøpsdokumenter i tabellene **Mottakshode** og **Kjøpsfakturahode**.

Før du starter bokføringen, kan du skrive ut en kontrollrapport som viser alle opplysningene i bestillingen, samt eventuelle feil. Hvis du vil skrive ut rapporten, velger du **Bokføring** og deretter **Kontrollrapport**.

> [!IMPORTANT]  
> Når du bokfører en bestilling for varer, kan du opprette både et mottak og en faktura. Dette kan gjøres samtidig, eller hver for seg. Du kan også opprette et delvis mottak og en delfaktura ved å fylle ut feltene **Motta (antall)** og **Fakturer (antall)** på de enkelte bestillingsordrelinjene før du bokfører. Legg merke til at du ikke kan opprette en kjøpsfaktura fra en bestilling for produkter eller tjenester som ikke er mottatt. Det vil si at for å kunne fakturere, må du på forhånd ha registrert et mottak, eller du må velge å motta og fakturere samtidig.
>
> Hvis du vil bokføre en kjøpsfaktura uten å registrere et kjøpsmottak i [!INCLUDE[prod_short](includes/prod_short.md)], oppretter du dokumentet på **Kjøpsfakturaer**-siden. Finn ut mer under [Registrer kjøp med kjøpsfakturaer](purchasing-how-record-purchases.md).

Du kan enten bokføre eller bokføre og skrive ut. Hvis du velger å bokføre og skrive ut, skrives det ut en rapport når ordren bokføres. Du kan også velge handlingen **Massebokfør** for å bokføre flere bestillinger samtidig. Finn ut mer under [Bokfør flere dokumenter samtidig](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Vis poster

Når bokføringen er utført, fjernes de bokførte kjøpslinjene fra bestillingen. En melding viser når bokføringen er gjennomført. Etter dette kan du se de bokførte postene på de forskjellige sidene, inkludert sidene **Leverandørposter**, **Finansposter**, **Vareposter**, **Ressursposter**, **Kjøpsmottak** og **Bokførte kjøpsfakturaer**.

I de fleste tilfeller kan du åpne poster fra det berørte kortet eller dokumentet. På siden **Leverandørkort** velger du for eksempel handlingen **Poster**.

## <a name="editing-ledger-entries"></a>Rediger poster

Du kan redigere bestemte felt på bokførte kjøpsdokumenter, for eksempel feltet **Betalingsreferanse**. Finn ut mer under [Rediger bokførte dokumenter](across-edit-posted-document.md). Hvis du vil ha mer kritiske felt som påvirker revisjonssporingen, må du tilbakeføre eller angre bokføringen. Finn ut mer under [Tilbakefør kladdebokføringer og angre mottak/leveringer](finance-how-reverse-journal-posting.md).

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/receive-invoice-dynamics-d365-business-central/index).

## <a name="see-also"></a>Se også

[Redigere bokførte dokumenter](across-edit-posted-document.md)  
[Bokfør flere dokumenter samtidig](ui-batch-posting.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Bokføre dokumenter og kladder](ui-post-documents-journals.md)  
[Korrigere eller annullere ubetalte kjøpsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Finne sider og informasjon med Fortell meg](ui-search.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
