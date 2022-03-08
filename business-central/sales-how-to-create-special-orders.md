---
title: Opprette spesialbestillinger | Microsoft-dokumentasjon
description: Du kan opprette en spesialbestilling for en bestemt katalogvare som skal leveres til en bestemt kunde. Leverandøren din leverer varen til lageret ditt, og du kan deretter sende bare denne varen videre til kunden eller sammen med andre varer i en annen ordre.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 31c119958b12701f6e5e18d21ea4b48246255042
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194790"
---
# <a name="create-special-orders"></a>Opprette spesialbestillinger
Du kan opprette en spesialbestilling for en bestemt katalogvare som skal leveres til en bestemt kunde. Leverandøren din leverer varen til lageret ditt, og du kan deretter sende bare denne varen videre til kunden eller sammen med andre varer i en annen ordre.  

Spesialbestillinger betyr at bestillingen og ordren er knyttet til hverandre for å sikre at den bestemte katalogvaren plukkes og leveres til kunden.  

Før du kan bruke denne funksjonen, må du først konfigurere kunden, leverandøren og de varekortene som kreves for ordren.  

## <a name="to-create-a-special-order"></a>Slik oppretter du en spesialbestilling  
1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ordre**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**. Opprett og fyll ut en  ordre for varen. Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).
3.  På hurtigfanen **Linjer** fyller du inn salgslinjen. Velg en kjøpskode som **Spesialbestilling**-feltet er valgt for, i **Kjøpskode**-feltet.

    Du må nå opprette en bestilling fra et bestillingsforslag.  
4. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bestillingsforslag**, og velg deretter den relaterte koblingen.  
5. Velg **Spesialbestilling**-handlingen, og velg deretter **Hent ordre**-handlingen.  
6.  Vis resultater der **Bilagsnr.** er ordrenummeret, på siden **Hent ordrer**. Velg **OK**-knappen. Det opprettes en bestillingsforslagslinje for varen.  
7.  På bestillingsforslagslinjen velger du **Ny** i feltet **Handlingsmelding**.  
8.  På siden **Best.forslag** velger du handlingen **Utfør handlingsmelding**. Siden **Utfør handlingsmeld. - forslag** åpnes. Velg **OK**.  

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
