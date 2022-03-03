---
title: Spore relasjoner mellom behov og forsyning
description: Dette emnet forklarer de forskjellige måtene å spore relasjoner mellom behov og forsyning, for eksempel sporing av koblede varer og håndtering av ikke-sporede planleggingselementer.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5830, 9101, 99000822, 99000855
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 27dce308070eb72ae7699bae084b6bedb0324ba7
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8146371"
---
# <a name="track-relations-between-demand-and-supply"></a>Spore relasjoner mellom behov og forsyning

Fra ethvert forsynings- eller behovsdokument i det såkalte ordrenettverket kan du spore ordrebehovet (sporet antall), prognosen, rammebestillingen eller planleggingsparameteren (ikke-sporet antall) som har forårsaket den aktuelle planleggingslinjen.

Planleggingsforslagene gir også støtteinformasjon for planlegging for ikke-ordreenheter for å hjelpe planleggeren med å opprette en optimal forsyningsplan. Hvis du vil ha mer informasjon, kan du se [Ikke-sporet planleggingselement](production-how-track-demand-supply.md#untracked-planning-elements).

## <a name="to-track-linked-items"></a>Spore tilknyttede varer
Sporing viser hvordan ordrer, produksjonsordrer og bestillinger er knyttet til produksjonsordrer gjennom planleggings- og reservasjonssystemer.

Nedenfor beskrives hvordan du kan spore tilknyttede varer på en fast planlagt produksjonsordre. Fremgangsmåten er lik for alle andre ordretyper og fra planleggingsforslagslinjer.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Fast planlagt prod.ordre** og velg den relaterte koblingen.
2. Åpne den aktuelle fast planlagte produksjonsordren fra oversikten.
3. På hurtigfanen **Linjer** velger du **Funksjoner**-handlingen og deretter **Sporing**.

Linjene i **Sporing**-vinduet viser hvilke dokumenter som er knyttet til den aktuelle produksjonsordrelinjen.

## <a name="untracked-planning-elements"></a>Ikke-sporede planleggingselementer
Siden **Ikke-sporede planleggingselementer** åpnes når du velger feltet **Ikke-sporet antall** på siden **Ordreplanlegging**. Det har to formål:

1. Inneholde informasjon om ikke-sporede antall som vises når brukeren slår opp ikke-sporede antall fra Sporing-siden.
2. Inneholde advarsler som vises når brukeren klikker et **advarselsikon** på siden **Planleggingsforslag**.

Siden inneholder poster som gjør rede for et ikke-sporet overskuddsantall i ordresporingsnettverket. Disse postene genereres under planleggingskjøringen og forklarer hvor det ikke-sporede overskuddsantallet på sporingslinjene kommer fra. Dette ikke-sporede overskuddet kan komme fra:

- Produksjonsprognose
- Rammeordrer
- Sikkerhetslagerantall
- Gjenbestillingspunkt
- Maks. beholdning
- Gjenbestillingsantall
- Maks. bestillingsantall
- Min. bestillingsantall
- Bestillingsfaktor
- Avdemping (% av partistr.)

## <a name="see-also"></a>Se også  
[Planlegging](production-planning.md)   
[Definere produksjon](production-configure-production-processes.md)  
[Produksjon](production-manage-manufacturing.md)    
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Designdetaljer: Reservasjon, sporing og handlingsmeldinger](design-details-reservation-order-tracking-and-action-messaging.md)  
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)   
[Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging](setup-best-practices-supply-planning.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]