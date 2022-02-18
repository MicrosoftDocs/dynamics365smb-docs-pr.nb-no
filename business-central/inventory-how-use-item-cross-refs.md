---
title: Bruk varereferanser
description: Definer referanser mellom beskrivelser, enheter og varianter som du og leverandøren eller kunden bruker for en vare.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.search.forms: 5737, 5735, 5736
ms.date: 10/27/2021
ms.author: edupont
ms.openlocfilehash: c649b444b0ebec908aa115261569a693f1ef0ce4
ms.sourcegitcommit: 189bf08d7ddf6c8b7ef2c09058c6847aa6e590d3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8060251"
---
# <a name="use-item-references"></a>Bruk varereferanser

Hvis du kjøper eller selger varer som du og leverandøren eller kunden bruker forskjellige betingelser for, kan du definere en referanse mellom betingelsene for varene og betingelsene som kunden eller leverandøren av denne varen bruker. På denne måten settes leverandørens eller kundens varebeskrivelse, enhet eller variantkode automatisk inn i de relevante dokumentene når du fyller ut feltet **Varenr.** -feltet.  

> [!NOTE]
> [!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]
>
> Ikke alle selskaper bruker varereferanser. For å få mindre rot på sider har vi skjult de relaterte feltene og handlingene som standard. Hvis du bestemmer deg for å bruke dem, velger du feltet **Bruk varereferanser** på siden **Lageroppsett**. Når du har aktivert varereferanser, er feltene og handlingene tilgjengelige på sidene Varekort, Leverandørkort og Kundekort samt fra salgs- og kjøpsdokumenter.
>
> I versjoner tidligere enn lanseringsbølge 2 for 2021 kan administratoren aktivere funksjonen *Skriv lengre varereferanser* på siden [Funksjonsstyring](https://businesscentral.dynamics.com/?page=2610) (koblingen krever at du har en [!INCLUDE [prod_short](includes/prod_short.md)]-leietaker). Hvordan du bruker referanser endres ikke, men navnet på ting som sider og knapper vil bli endret. Siden **Varekryssreferanseposter** vil for eksempel bli siden **Varereferanseposter**.

## <a name="to-start-using-item-references"></a>Slik begynner du å bruke varereferanser

[!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]

1. Velg ikonet :::image type="icon" source="media/ui-search/search_small.png" border="false":::, angi **Lageroppsett** og velg den relaterte koblingen.
2. Velg feltet **Bruk varereferanser**.

## <a name="to-set-up-an-item-reference"></a>Slik definerer du en varereferanse

1. Velg ikonet :::image type="icon" source="media/ui-search/search_small.png" border="false":::, angi **Varer**, og velg deretter den relaterte koblingen.
2. Åpne kortet for en vare som du vil opprette en referanse for.
3. Velg handlingen **Varereferanser**.

     Hvis du ikke finner handlingen **Varereferanser**, velger du å vise flere alternativer og finner det under **Relatert** > **Vare**.
  
4. På en ny linje på siden **Varereferanseposter** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Den følgende fremgangsmåten beskriver hvordan du angir varereferansen på en bestilling. Lignende fremgangsmåte gjelder salgsdokumenter og andre kjøpsdokumenter.  

## <a name="to-enter-a-vendors-item-description-on-a-document"></a>Slik angir du en leverandørs varebeskrivelse på et dokument

1. Velg ikonet :::image type="icon" source="media/ui-search/search_small.png" border="false":::, angi **Bestillinger**, og velg deretter den relaterte koblingen.
2. Opprett en bestilling for leverandøren du angav en varereferanse for i den forrige prosedyren.
3. Opprett en bestillingslinje for varen som du angav en varereferanse for i den forrige prosedyren.
4. I **Varereferansetypenr.** -feltet velger du relevant varereferanse, og deretter velger du **OK**-knappen.

**Beskrivelse**-feltet på linjen overskrives med leverandørens varebeskrivelse, slik den er angitt opp på varereferanseposten. Hvis varereferansen inneholder en variantkode eller en enhet, kopieres også disse verdiene til dokumentet.  

## <a name="see-also"></a>Se også

[Registrere nye varer](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]