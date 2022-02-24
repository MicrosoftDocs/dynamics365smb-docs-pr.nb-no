---
title: Bruke varekryssreferanser | Microsoft Docs
description: Hvis du har definert en kryssreferanse mellom varebeskrivelsen som du bruker for en vare, og beskrivelsen som leverandøren av varen bruker, settes leverandørvarebeskrivelsen automatisk inn på kjøpsdokumenter for leverandøren når du fyller ut **Kryssreferansenr.** .
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 89a99080723ee57270583ee2f277250d767b8dde
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181943"
---
# <a name="use-item-cross-references"></a>Bruke varekryssreferanser
Hvis du har definert en kryssreferanse mellom varebeskrivelsen som du bruker for en vare, og beskrivelsen som leverandøren av varen bruker, settes leverandørvarebeskrivelsen automatisk inn på kjøpsdokumenter for leverandøren når du fyller ut **Kryssreferansenr.** . Den samme funksjonaliteten gjelder for kundevarenumre på salgsdokumenter.

Den følgende fremgangsmåten beskriver hvordan du bruker varekryssreferanser på kjøpssiden. Trinnene er de samme for salgssiden.

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a>Slik definerer du en varekryssreferanse til en leverandørs varebeskrivelse
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varer**, og velg deretter den relaterte koblingen.
2. Åpne kortet for en vare som du vil opprette en kryssreferanse for til varebeskrivelsen som leverandøren bruker for denne varen.
3. Velg **Kryssreferanser**-handlingen.
4. På en ny linje på siden **Varekryssreferanseposter** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a>Slik angir du en leverandørs varebeskrivelse på en bestilling
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bestillinger**, og velg deretter den relaterte koblingen.
2. Opprett en bestilling for leverandøren du angav en varekryssreferanse for i den forrige prosedyren.
3. Opprett en bestillingslinje for varen som du angav en varekryssreferanse for i den forrige prosedyren.
4. I **Kryssreferansetypenr.** -feltet velger du varekryssreferansen du har opprettet, og deretter velger du **OK**-knappen.

**Beskrivelse**-feltet på linjen overskrives med leverandørens varebeskrivelse, slik den er angitt opp på varekryssreferanseposten.

## <a name="see-also"></a>Se også
[Registrere nye varer](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
