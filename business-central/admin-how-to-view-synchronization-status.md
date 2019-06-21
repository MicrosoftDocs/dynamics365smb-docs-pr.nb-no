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
ms.openlocfilehash: 11e29674c2d12031fdf4e7f66e767be4fcc74795
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/06/2019
ms.locfileid: "1620887"
---
# <a name="view-the-status-of-a-synchronization"></a>Vise statusen for en synkronisering
Du kan vise statusen for individuelle synkroniseringsjobber som har blitt kjørt for [!INCLUDE[crm_md](includes/crm_md.md)]-integrasjon. Dette inkluderer synkroniseringsjobber som har blitt kjørt fra jobbkøen, og manuelle synkroniseringsjobber som ble utført på poster fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dette er nyttig når du feilsøker synkroniseringsproblemer, fordi det gir deg tilgang til opplysninger om bestemte feil.

### <a name="to-view-synchronization-issues-for-coupled-records"></a>Slik viser du synkroniseringsproblemer for koblede poster
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Feil ved synkronisering av koblede data**, og velg deretter den relaterte koblingen.
2. Siden **Feil ved synkronisering av koblede data** viser problemer som oppstod da du synkroniserte koblede poster. Du kan filtrere og sortere poster og utføre handlinger som for eksempel **Gjenopprett** eller **Slett poster** for å løse ett og ett problem.

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a>Vise synkroniseringslogg for bestemt (manuelt synkronisert) post
1. Åpne for eksempel kunde, vare eller en annen post som synkroniserer data mellom [!INCLUDE[d365fin](includes/d365fin_md.md)] og Sales.
2. Velg **Synkroniseringslogg**-handlingen for å vise synkroniseringsloggen for en valgt post. For eksempel en bestemt kunde du synkroniserte manuelt.

## <a name="see-also"></a>Se også  
[Definere Dynamics 365 for Sales-integrering i Business Central](admin-setting-up-integration-with-dynamics-sales.md)  
[Bruke Dynamics 365 for Sales fra Business Central](marketing-integrate-dynamicscrm.md)
