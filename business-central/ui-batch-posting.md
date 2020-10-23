---
title: Bokføre flere dokumenter samtidig | Microsoft Docs
description: I stedet for å bokføre enkeltdokumenter én etter én, kan du velge flere dokumenter som ikke er bokført, i en liste for massebokføring, enten det er for umiddelbar bokføring eller planlagt, for eksempel på slutten av dagen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1fd25f8b07a359414f62ef4757162f8a73889c27
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912724"
---
# <a name="post-multiple-documents-at-the-same-time"></a>Bokføre flere dokumenter samtidig

I stedet for å bokføre enkeltdokumenter én etter én, kan du velge flere dokumenter som ikke er bokført, i en liste for umiddelbar bokføring eller massebokføring i henhold til en tidsplan, for eksempel på slutten av dagen. Dette kan være nyttig hvis bare en arbeidsleder kan bokføre dokumenter som er opprettet av andre brukere, eller for å unngå problemer med systemytelse ved bokføring i arbeidstiden.

## <a name="to-post-multiple-purchase-orders-immediately"></a>Bokføre flere bestillinger umiddelbart

Fremgangsmåten nedenfor forklarer hvordan du bokfører flere bestillinger umiddelbart. Trinnene er lignende for alle kjøps- og salgsdokumenter.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bestillinger**, og velg deretter den relaterte koblingen.
2. På **Bestilling**-siden fortsetter du for å velge alle bestillinger som skal bokføres:
3. I **Nr.** -feltet velger du de tre loddrette prikkene for å åpne hurtigmenyen, og deretter velger du handlingen **Velg flere**.
4. Merk av i boksen for alle linjene som representerer ordrer du vil bokføre samtidig.
5. Velg handlingen **Bokføring**, og velg deretter handlingen **Bokfør**.
6. Velg **Ja** i bekreftelsesmeldingen.

## <a name="to-batch-post-multiple-purchase-orders"></a>Massebokføre flere bestillinger

Fremgangsmåten nedenfor forklarer hvordan du massebokfører bestillinger. Trinnene er de samme for alle kjøps- og salgsdokumenter der handlingen **Massebokfør** er tilgjengelig.

> [!NOTE]
> Massebokføring av dokumenter skjer i bakgrunnen. [!INCLUDE [prodshort](includes/prodshort.md)] Online omfatter standardjobber for bakgrunnsbokføring og massebokføring. Hvis du vil ha mer informasjon, kan du se [Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bestillinger**, og velg deretter den relaterte koblingen.  
2. På **Bestilling**-siden fortsetter du for å velge alle bestillinger som skal bokføres:
3. I **Nr.** -feltet velger du de tre loddrette prikkene for å åpne hurtigmenyen, og deretter velger du handlingen **Velg flere**.
4. Merk av i boksen for alle linjene som representerer ordrer du vil bokføre samtidig.
5. Velg handlingen **Bokføring**, og velg deretter handlingen **Massebokfør**.
6. På siden **Bestillinger - massebokfør** fyller du ut resten av feltene. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Velg **OK**-knappen.
8. Hvis du vil vise potensielle problemer som oppstod under massebokføring av dokumenter, åpner du siden **Feilmeldingsregister**.

Bestillingene blir nå lagt til i en dedikert jobbkø, som definerer når dokumentene bokføres. Hvis du vil ha mer informasjon, kan du se [Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).

Hvis du velger **PDF** i feltet **Rapportutdatatype**, vil bokførte bestillinger være tilgjengelige i delen **Rapportinnboks** i rollesenteret.

## <a name="see-also"></a>Se også

[Bokføre dokumenter og kladder](ui-post-documents-journals.md)  
[Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md)  
[Redigere bokførte dokumenter](across-edit-posted-document.md)  
[Korrigere eller annullere ubetalte kjøpsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Finne sider og informasjon med Fortell meg](ui-search.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
