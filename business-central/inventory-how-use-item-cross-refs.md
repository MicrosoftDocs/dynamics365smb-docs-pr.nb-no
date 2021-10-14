---
title: Bruk varereferanser
description: Definer referanser mellom beskrivelsene som du og leverandøren bruker for en vare for å sette inn leverandørens varebeskrivelse i kjøpsdokumenter.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 4eed6fce594b0b6835020fcdddb7275489b4d160
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588604"
---
# <a name="use-item-references"></a>Bruk varereferanser
Hvis du har definert en referanse mellom varebeskrivelsen som du bruker for en vare, og beskrivelsen som leverandøren av varen bruker, settes leverandørvarebeskrivelsen automatisk inn på kjøpsdokumenter for leverandøren når du fyller ut **Varereferansenr.** -feltet. Den samme funksjonaliteten gjelder for kundevarenumre på salgsdokumenter.

Den følgende fremgangsmåten beskriver hvordan du bruker varereferanser på kjøpssiden. Trinnene er de samme for salgssiden.

> [!NOTE]
> Ikke alle selskaper bruker varereferanser, slik at det blir mindre rot på sider vi har skjult de relaterte feltene og handlingene. Hvis du bestemmer deg for å bruke dem, kan du aktivere **Bruk varereferanser** på siden **Lageroppsett**. Når du har aktivert varereferanser, er feltene og handlingene tilgjengelige på sidene Varekort, Leverandørkort og Kundekort samt fra salgs- og kjøpsdokumenter.

## <a name="to-start-using-item-references"></a>Slik begynner du å bruke varereferanser
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lageroppsett** og velg den relaterte koblingen.
2. Aktivere **Bruk varereferanser**.

## <a name="to-set-up-an-item-reference-to-a-vendors-item-description"></a>Slik definerer du en varereferanse til en leverandørs varebeskrivelse

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.
2. Åpne kortet for en vare som du vil opprette en referanse for til varebeskrivelsen som leverandøren bruker for denne varen.
3. Velg handlingen **Varereferanser**.

     Hvis du ikke finner handlingen **Varereferanser**, velger du å vise flere alternativer og finner det under **Relatert** > **Vare**.
  
4. På en ny linje på siden **Varereferanseposter** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a>Slik angir du en leverandørs varebeskrivelse på en bestilling

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bestillinger**, og velg deretter den relaterte koblingen.
2. Opprett en bestilling for leverandøren du angav en varereferanse for i den forrige prosedyren.
3. Opprett en bestillingslinje for varen som du angav en varereferanse for i den forrige prosedyren.
4. I **Varereferansetypenr.** -feltet velger du varereferansen du har opprettet, og deretter velger du **OK**-knappen.

**Beskrivelse**-feltet på linjen overskrives med leverandørens varebeskrivelse, slik den er angitt opp på varereferanseposten.

## <a name="see-also"></a>Se også
[Registrere nye varer](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]