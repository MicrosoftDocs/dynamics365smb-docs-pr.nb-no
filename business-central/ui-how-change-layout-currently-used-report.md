---
title: Endre utseendet på en rapport ved å velge et annet oppsett | Microsoft-dokumentasjon
description: Du kan bruke ulike oppsett for en rapport og bytte mellom oppsett for å endre utseendet på den.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2785550b59e79d3bbda3a59422aabd7adac94c6e
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393852"
---
# <a name="change-the-current-report-layout"></a>Endre gjeldende rapportoppsett
En rapport kan defineres med flere rapportoppsett, som du deretter kan bytte mellom etter behov.

Avhengig av oppsettene som er tilgjengelige for en rapport, kan du velge om du vil bruke et innebygd RDLC-rapportoppsett, et innebygd Word-rapportoppsett eller et egendefinert oppsett. Hvis du vil ha mer informasjon om RDLC- og Word-rapportoppsett, innebygde og egendefinerte oppsett og mer, kan du se [Håndtere rapportoppsett](ui-manage-report-layouts.md).

Når egendefinerte rapportoppsett er definert, kan du velge dem fra kunde- og leverandørkortene for å angi at de valgte oppsettene skal brukes for dokumenter du oppretter for den aktuelle kunden eller leverandøren. Hvis du vil ha mer informasjon, se [Definere dokumentoppsett for kunder og leverandører](ui-define-customer-vendor-document-layouts.md).

> [!TIP]  
> Dokumentrapporter (ikke oversikter) som bruker et Word-rapportoppsett, er vanligvis raskere enn de som bruker et RDLC-rapportoppsett. Så hvis du kan velge mellom et Word- eller RDLC-rapportoppsett for en dokumentrapport, bør du bruke Word-rapportoppsettet for best ytelse.

## <a name="to-change-which-report-layout-to-use-for-a-report-or-document"></a>Slik endrer du hvilket rapportoppsett som skal brukes i en rapport eller et dokument
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rapportoppsettsvalg**, og velg deretter den relaterte koblingen.  
   Siden **Rapportoppsettsvalg** viser alle rapportene som er tilgjengelige for selskapet som er angitt i feltet **Selskap** øverst på siden. Feltet **Valgt oppsett** angir oppsettet som brukes i rapporten for øyeblikket.
2. Sett feltet **Selskap** øverst på siden til selskapet som inkluderer rapporten.
3. Hvis du vil endre oppsettet som brukes av en rapport, angir du ett av følgende alternativer for feltet **Valgt oppsett** i raden for rapporten:
   * **RDLC (innebygd)**: Bruker det innebygde RDLC-rapportoppsettet i rapporten.
   * **Word (innebygd)**: Bruker det innebygde Word-rapportoppsettet i rapporten.
   * **Egendefinert**: Bruker et egendefinert oppsett i rapporten.  

> [!NOTE]
> Hvis du velger et rapportoppsett av typen **RDLC (innebygd)** eller **Word (innebygd)** og får en feilmelding om at rapporten ikke har et oppsett for den angitte typen, må du velge et annet oppsettalternativ eller opprette et egendefinert rapportoppsett av typen du vil bruke. Se den neste fremgangsmåten.

Hvis du valgte et innebygd RDLC- eller Word-rapportoppsett, kreves ingen ytterligere handling, og oppsettet brukes neste gang rapporten kjøres.

## <a name="to-change-the-custom-layout-to-use-for-a-report-layout"></a>Slik endrer du det egendefinerte rapportoppsettet som skal brukes for et rapportoppsett
Det kan også hende du vil endre det egendefinerte oppsettet som brukes. Hvis du vil ha mer informasjon, kan du se [Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md).

Alle egendefinerte rapportoppsett som finnes for rapportoppsett i et selskap, vises på siden **Egendefinerte rapportoppsett**. På siden **Rapportoppsettsvalg** kan du se hvilke egendefinerte oppsett som er tilgjengelige for hver rapporten i faktaboksen **Egendefinerte oppsett**.

1. På siden **Egendefinerte rapportoppsett**, på linjen for rapportoppsett du vil endre, velger du oppsettknappen i feltet **Beskrivelse av egendefinert oppsett**.
2. På siden **Egendefinerte rapportoppsett** velger du raden for den egendefinerte oppsettet du vil bruke, og deretter velger du **OK**-knappen.

Navnet på det valgte egendefinerte oppsettet vises nå i feltet **Beskrivelse av egendefinert oppsett** og vil bli brukt neste gang rapporten eller dokumentet forhåndsvises, skrives ut eller sendes.

Nå kan du gå til kunde- og leverandørkortene for å angi hvilke oppsett som skal brukes for forskjellige dokumenter som du oppretter for den aktuelle kunden eller leverandøren, for eksempel ordrebekreftelser eller purringer. Hvis du vil ha mer informasjon, se [Definere dokumentoppsett for kunder og leverandører](ui-define-customer-vendor-document-layouts.md).

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også
[Håndtere rapportoppsett](ui-manage-report-layouts.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]