---
title: Vise statusen for en synkronisering | Microsoft Docs
description: Slik viser du statusen for en individuell synkroniseringsjobb.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: d55d8d5ab916cee6600deaf891702a625d76d7ee
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "940277"
---
# <a name="view-the-status-of-a-synchronization"></a>Vise statusen for en synkronisering
Du kan vise statusen for individuelle synkroniseringsjobber som har blitt kjørt for [!INCLUDE[crm_md](includes/crm_md.md)]-integrasjon. Dette inkluderer synkroniseringsjobber som har blitt kjørt fra jobbkøen, og manuelle synkroniseringsjobber som ble utført på poster fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dette er nyttig når du feilsøker synkroniseringsproblemer, fordi det gir deg tilgang til opplysninger om bestemte feil.

### <a name="to-view-all-synchronization-issues"></a>Vise alle synkroniseringsproblemer
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Feil ved synkronisering av koblede data**, og velg deretter den relaterte koblingen.
2. På siden **Feil ved synkronisering av koblede data** kan du se alle problemer som oppstod i synkroniseringen mellom [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)], filtrere og sortere poster på siden etter tabell, feilmelding og utføre handlinger som **Prøv på nytt** eller **Fjern kobling** for å løse problemer enkeltvis eller samlet.

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a>Vise synkroniseringslogg for bestemt (manuelt synkronisert) post
1. Åpne for eksempel kunde, vare eller en annen post som synkroniserer data mellom [!INCLUDE[d365fin](includes/d365fin_md.md)] og Sales
2. Velg **Synkroniseringslogg**-handling for å vise synkroniseringsloggen for valgt post, for eksempel bestemt kunde du synkroniserte manuelt

## <a name="see-also"></a>Se også  
[Definere Dynamics 365 for Sales-integrering i Business Central](admin-setting-up-integration-with-dynamics-sales.md)  
[Bruke Dynamics 365 for Sales fra Business Central](marketing-integrate-dynamicscrm.md)
