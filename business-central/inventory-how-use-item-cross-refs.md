---
title: Bruke varekryssreferanser
description: Definer kryssreferanser mellom beskrivelsene som du og leverandøren bruker for en vare for å sette inn leverandørens varebeskrivelse i kjøpsdokumenter.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 853c574f5b262f7b826bc92dd8e35484e902c1f4
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6444948"
---
# <a name="use-item-cross-references"></a>Bruke varekryssreferanser
Hvis du har definert en kryssreferanse mellom varebeskrivelsen som du bruker for en vare, og beskrivelsen som leverandøren av varen bruker, settes leverandørvarebeskrivelsen automatisk inn på kjøpsdokumenter for leverandøren når du fyller ut **Kryssreferansenr.** . Den samme funksjonaliteten gjelder for kundevarenumre på salgsdokumenter.

Den følgende fremgangsmåten beskriver hvordan du bruker varekryssreferanser på kjøpssiden. Trinnene er de samme for salgssiden.

> [!NOTE]
> Det blir mer vanlig at vare-ID-er, for eksempel GTIN eller GUID, inneholder 30 eller flere tegn, som er mer enn den gjeldende funksjonen for varekryssreferanser kan håndtere. Hvis du må bruke referanser som inneholder mer enn 30 tegn, kan systemansvarlig aktivere funksjonen **Skriv lengre varereferanser** på siden [Funksjonsstyring](https://businesscentral.dynamics.com/?page=2610) (koblingen krever at du har en [!INCLUDE[prod_short](includes/prod_short.md)]-leietaker). Hvordan du bruker referanser endres ikke, men navnet på ting som sider og knapper vil bli endret. Siden **Varekryssreferanseposter** vil for eksempel bli siden **Varereferanseposter**.

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a>Slik definerer du en varekryssreferanse til en leverandørs varebeskrivelse

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.
2. Åpne kortet for en vare som du vil opprette en kryssreferanse for til varebeskrivelsen som leverandøren bruker for denne varen.
3. Velg **Kryssreferanser**-handlingen.

     Hvis du ikke finner handlingen **Kryssreferanser**, velger du å vise flere alternativer og finner det under **Relatert** > **Vare**.
  
4. På en ny linje på siden **Varekryssreferanseposter** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a>Slik angir du en leverandørs varebeskrivelse på en bestilling

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bestillinger**, og velg deretter den relaterte koblingen.
2. Opprett en bestilling for leverandøren du angav en varekryssreferanse for i den forrige prosedyren.
3. Opprett en bestillingslinje for varen som du angav en varekryssreferanse for i den forrige prosedyren.
4. I **Kryssreferansetypenr.** -feltet velger du varekryssreferansen du har opprettet, og deretter velger du **OK**-knappen.

**Beskrivelse**-feltet på linjen overskrives med leverandørens varebeskrivelse, slik den er angitt opp på varekryssreferanseposten.

## <a name="see-also"></a>Se også
[Registrere nye varer](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]