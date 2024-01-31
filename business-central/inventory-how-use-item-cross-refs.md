---
title: Bruk varereferanser
description: 'Definer referanser mellom beskrivelser, enheter og varianter som du og leverandøren eller kunden bruker for en vare.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: 'item reference, cross reference, inventory'
ms.search.forms: '5737, 5735, 5736'
ms.date: 10/02/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Bruk varereferanser

Hvis du kjøper eller selger varer som du og leverandøren eller kunden bruker forskjellige betingelser for, kan du definere en referanse mellom betingelsene for varene og betingelsene som kunden eller leverandøren av denne varen bruker. På denne måten settes leverandørens eller kundens varebeskrivelse, enhet eller variantkode automatisk inn i de relevante dokumentene når du fyller ut feltet **Varenr.** .  

## Slik definerer du en varereferanse

1. Velg ikonet :::image type="icon" source="media/ui-search/search_small.png" border="false":::, angi **Varer**, og velg deretter den relaterte koblingen.
2. Åpne kortet for en vare som du vil opprette en referanse for.
3. Velg handlingen **Varereferanser**.

     Hvis du ikke finner handlingen **Varereferanser**, velger du å vise flere alternativer og finner det under **Relatert** > **Vare**.
  
4. På en ny linje på siden **Varereferanseposter** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Den følgende fremgangsmåten beskriver hvordan du angir varereferansen på en bestilling. Lignende fremgangsmåte gjelder salgsdokumenter og andre kjøpsdokumenter.  

## Slik angir du en leverandørs varebeskrivelse på et dokument

1. Velg ikonet :::image type="icon" source="media/ui-search/search_small.png" border="false":::, angi **Bestillinger**, og velg deretter den relaterte koblingen.
2. Opprett en bestilling for leverandøren du angav en varereferanse for i den forrige prosedyren.
3. Opprett en bestillingslinje for varen som du angav en varereferanse for i den forrige prosedyren.
4. I **Varereferansetypenr.** -feltet velger du relevant varereferanse, og deretter velger du **OK**-knappen.

**Beskrivelse**-feltet på linjen overskrives med leverandørens varebeskrivelse, slik den er angitt opp på varereferanseposten. Hvis varereferansen inneholder en variantkode eller en enhet, kopieres også disse verdiene til dokumentet.  

## Skanne strekkoder med Business Central-mobilappen

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

Tabellene nedenfor inneholder en oversikt over sidene som støtter strekkodeskanning for varereferanser fra mobilappen [!INCLUDE [prod_short](includes/prod_short.md)].

|Side  |Feltverdien du kan skanne  |
|---------|---------|
|Varereferanse     | Referansenr.        |
|Varekladdelinje     | Varereferansenr.        |
|Ordrelinje for vareopptelling     |Varereferansenr.         |
|Bestillingslinje     |   Varereferansenr.      |
|Salgslinje     | Varereferansenr.        |

## Se også

[Registrer nye varer](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
