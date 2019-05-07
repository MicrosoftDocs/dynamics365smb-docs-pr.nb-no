---
title: Endre utseendet på en rapport ved å velge et annet oppsett | Microsoft-dokumentasjon
description: Du kan bruke ulike oppsett for en rapport og bytte mellom oppsett for å endre utseendet på den.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: f24f1cd24a31ddbd0b455b876821ae0173a677c3
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/16/2019
ms.locfileid: "969812"
---
# <a name="change-which-layout-is-currently-used-on-a-report"></a>Endre gjeldende oppsett som skal brukes i en rapport
En rapport kan defineres med flere rapportoppsett, som du deretter kan bytte mellom etter behov.

Avhengig av oppsettene som er tilgjengelige for en rapport, kan du velge om du vil bruke et innebygd RDLC-rapportoppsett, et innebygd Word-rapportoppsett eller et egendefinert oppsett. Hvis du vil ha mer informasjon om RDLC- og Word-rapportoppsett, innebygde og egendefinerte oppsett og mer, kan du se [Håndtere rapportoppsett](ui-manage-report-layouts.md).

> [!TIP]  
> Dokumentrapporter (ikke oversikter) som bruker et Word-rapportoppsett, er vanligvis raskere enn de som bruker et RDLC-rapportoppsett. Så hvis du kan velge mellom et Word- eller RDLC-rapportoppsett for en dokumentrapport, bør du bruke Word-rapportoppsettet for best ytelse.  

## <a name="to-change-the-layout-that-is-used-on-a-report"></a>Slik endrer du oppsettet som brukes i en rapport
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rapportoppsettsvalg**, og velg deretter den relaterte koblingen.  
   Siden **Rapportoppsettsvalg** viser alle rapportene som er tilgjengelige for selskapet som er angitt i feltet Selskap øverst på siden. Feltet Valgt oppsett angir oppsettet som brukes i rapporten for øyeblikket.
2. Sett feltet **Selskap** øverst på siden til selskapet som inkluderer rapporten.
3. Hvis du vil endre oppsettet som brukes av en rapport, angir du ett av følgende alternativer for feltet **Valgt oppsett** i raden for rapporten i listen:
   * RDLC (innebygd): Bruker det innebygde RDLC-rapportoppsettet i rapporten.
   * Word (innebygd): Bruker det innebygde Word-rapportoppsettet i rapporten.
   * Egendefinert: Bruker et egendefinert oppsett i rapporten.  
     Du kan se hvilke egendefinerte oppsett som er tilgjengelige for rapporten, i faktaboksen Rapportoppsettsdel. Hvis det ikke finnes noen egendefinerte oppsett for rapporten, må du først opprette et. Hvis du velger dette alternativet, går du til neste fremgangsmåte for å angi det egendefinerte oppsettet du vil bruke.

    > [!NOTE]  
    >   Hvis du velger **RDLC (innebygd)** eller **Word (innebygd)** og får en feilmelding om at rapporten ikke har et oppsett for den angitte typen, må du velge et annet oppsettalternativ eller opprette et egendefinert rapportoppsett av typen du vil bruke.

Hvis du valgte et innebygd RDLC- eller Word-rapportoppsett, kreves ingen ytterligere handling, og oppsettet brukes neste gang rapporten kjøres.

## <a name="to-specify-a-custom-layout-on-a-report"></a>Angi et egendefinert oppsett i en rapport
1. Du angir hvilket egendefinert oppsett som skal brukes i rapporten, fra siden **Egendefinerte rapportoppsett**. Hvis siden **Egendefinerte rapportoppsett** ikke er åpen, velger du oppslagsknappen i feltet **Beskrivelse av rapportoppsett**.
2. Merk raden for det egendefinerte oppsettet du vil bruke, på siden **Egendefinerte rapportoppsett**, og lukk deretter siden.

Du går tilbake siden **Egendefinerte rapportoppsett**. Navnet på det valgte egendefinerte oppsettet vises i feltet **Beskrivelse av egendefinert oppsett**. Det egendefinerte oppsettet brukes neste gang du kjører rapporten.

## <a name="see-also"></a>Se også
[Håndtere rapportoppsett](ui-manage-report-layouts.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
