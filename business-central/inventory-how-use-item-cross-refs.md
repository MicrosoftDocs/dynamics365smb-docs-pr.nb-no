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
---
# <a name="use-item-references"></a>Bruk varereferanser

Hvis du kjøper eller selger varer som du og leverandøren eller kunden bruker forskjellige betingelser for, kan du definere en referanse mellom betingelsene for varene og betingelsene som kunden eller leverandøren av denne varen bruker. På denne måten settes leverandørens eller kundens varebeskrivelse, enhet eller variantkode automatisk inn i de relevante dokumentene når du fyller ut feltet **Varenr.** -feltet.  

> [!NOTE]
> Ikke alle selskaper bruker varereferanser. For å få mindre rot på sider har vi skjult de relaterte feltene og handlingene som standard. Hvis du bestemmer deg for å bruke dem, velger du feltet **Bruk varereferanser** på siden **Lageroppsett**. Når du har aktivert varereferanser, er feltene og handlingene tilgjengelige på sidene Varekort, Leverandørkort og Kundekort samt fra salgs- og kjøpsdokumenter.
>
> I versjoner tidligere enn lanseringsbølge 2 for 2021 kan administratoren aktivere funksjonen *Skriv lengre varereferanser* på siden [Funksjonsstyring](https://businesscentral.dynamics.com/?page=2610) (koblingen krever at du har en [!INCLUDE [prod_short](includes/prod_short.md)]-leietaker). Hvordan du bruker referanser endres ikke, men navnet på ting som sider og knapper vil bli endret. Siden **Varekryssreferanseposter** vil for eksempel bli siden **Varereferanseposter**.

## <a name="to-start-using-item-references"></a>Slik begynner du å bruke varereferanser

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

## <a name="scan-barcodes-with-the-business-central-mobile-app"></a>Skanne strekkoder med Business Central-mobilappen

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

Tabellene nedenfor inneholder en oversikt over sidene som støtter strekkodeskanning for varereferanser fra mobilappen [!INCLUDE [prod_short](includes/prod_short.md)].

|Side  |Feltverdien du kan skanne  |
|---------|---------|
|Varereferanse     | Referansenr.        |
|Varekladdelinje     | Varereferansenr.        |
|Ordrelinje for vareopptelling     |Varereferansenr.         |
|Bestillingslinje     |   Varereferansenr.      |
|Salgslinje     | Varereferansenr.        |

## <a name="see-also"></a>Se også

[Registrer nye varer](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
