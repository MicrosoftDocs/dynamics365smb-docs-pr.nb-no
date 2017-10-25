---
title: Opprette spesialbestillinger | Microsoft-dokumentasjon
description: "Du kan opprette en spesialbestilling for en bestemt katalogvare som skal leveres til en bestemt kunde. Leverandøren din leverer varen til lageret ditt, og du kan deretter sende bare denne varen videre til kunden eller sammen med andre varer i en annen ordre."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c7e5d7cda12abd94a999031af3bc8d505b7f6c5e
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-special-orders"></a>Opprette spesialbestillinger
Du kan opprette en spesialbestilling for en bestemt katalogvare som skal leveres til en bestemt kunde. Leverandøren din leverer varen til lageret ditt, og du kan deretter sende bare denne varen videre til kunden eller sammen med andre varer i en annen ordre.  

Spesialbestillinger betyr at bestillingen og ordren er knyttet til hverandre for å sikre at den bestemte katalogvaren plukkes og leveres til kunden.  

Før du kan bruke denne funksjonen, må du først konfigurere kunden, leverandøren og de varekortene som kreves for ordren.  

## <a name="to-create-a-special-order"></a>Slik oppretter du en spesialbestilling  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Ordre**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**. Opprett og fyll ut en  ordre for varen. Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).
3.  På hurtigfanen **Linjer** fyller du inn salgslinjen. Velg en kjøpskode som **Spesialbestilling**-feltet er valgt for, i **Kjøpskode**-feltet.

    Du må nå opprette en bestilling fra et bestillingsforslag.  
4. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Bestillingsforslag**, og velg deretter den relaterte koblingen.  
5. Velg **Spesialbestilling**-handlingen, og velg deretter **Hent ordre**-handlingen.  
6.  Vis resultater der **Bilagsnr.** er ordrenummeret, i **Hent ordrer**-vinduet. Velg **OK**-knappen. Det opprettes en bestillingsforslagslinje for varen.  
7.  På bestillingsforslagslinjen velger du **Ny** i feltet **Handlingsmelding**.  
8.  I **Best. forslag**-vinduet velger du handlingen **Utfør handlingsmelding**. Vinduet **Utfør handlingsmeld. - forslag** åpnes. Velg **OK**.  

    Det vises en melding om at bestillingene er opprettet. Velg **OK**-knappen.  

En bestilling som er opprettet som en spesialbestilling for en salgsordre, blir respektert av planleggingssystemet som balanserer behov og forsyning. Det vil si at bestillingen (tilbud) forblir koblet til ordren (etterspørsel), selv om den aktuelle bestillingen ville kunnet forsyne et annet tidligere behov. Hvis du vil ha mer informasjon, se [Designdetaljer: Gjenbestillingsprinsipper](design-details-reservation-order-tracking-and-action-messaging.md).  

> [!NOTE]  
>  Du kan ikke bruke funksjonen for spesialbestilling hvis varen allerede er reservert. For varer som selges på spesialbestilling, må du derfor passe på at feltet **Reserver** på varekortet ikke er satt til **Alltid**.  

## <a name="see-also"></a>Se også  
[Arbeide med katalogvarer](inventory-how-work-nonstock-items.md)  
[Salg](sales-manage-sales.md)  
[Foreta direkte leveringer](sales-how-drop-shipment.md)   
[Designdetaljer: Gjenbestillingsprinsipper](design-details-reservation-order-tracking-and-action-messaging.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

