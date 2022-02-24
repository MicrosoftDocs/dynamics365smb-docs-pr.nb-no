---
title: Vise statusen til synkroniseringsjobber | Microsoft Docs
description: Finn ut hvordan du viser statusen etter synkronisering av koblede poster.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 022e364b6a40fe8df1f9c4e3425030d35f729e6a
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304495"
---
# <a name="view-the-status-of-synchronization-jobs"></a>Vise statusen til synkroniseringsjobber
Bruk siden **Feil ved synkronisering av koblede data** for å vise statusen til synkroniseringsjobber som har blitt kjørt for koblede poster i en [!INCLUDE[crm_md](includes/crm_md.md)]-integrasjon. Dette inkluderer jobber som ble kjørt fra jobbkøen, og manuelle synkroniseringsjobber som kjørte på poster fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det kan for eksempel være nyttig å vise statusen deres når du feilsøker, fordi det gir deg tilgang til detaljer om feil relatert til koblede poster. Vanligvis er disse feiltypene forårsaket av brukerhandlinger, for eksempel når følgende er tilfelle:  

* To personer foretok en endring i den samme posten i begge bedriftsappene.
* Noen slettet en post i en av appene, men ikke i begge.

> [!Note]
> Siden **Feil ved synkronisering av koblede data** viser informasjon om jobber relatert til koblede poster. Hvis du løser alle feilene, men poster fremdeles ikke synkroniseres, kan det ha noe å gjøre med en innstilling for integrasjonen. Vanligvis må disse feiltypene løses av administratoren.   

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098171]

## <a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a>Slik viser du og løser synkroniseringsfeil for koblede poster
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Feil ved synkronisering av koblede data**, og velg deretter den relaterte koblingen.
2. Siden **Feil ved synkronisering av koblede data** viser problemer som oppstod da du synkroniserte koblede poster. Følgende tabell inneholder handlinger som du kan bruke til å løse problemer ett etter ett:

|Handling|Beskrivelse|
|----|----|
|**Fjern kobling**|Opphever kobling av postene, og de vil ikke lenger synkroniseres. Hvis du vil gjenoppta synkronisering av postene, må du koble dem sammen på nytt.|
|**Prøv på nytt**|For hver post der det oppdages en feil, blir synkronisering hoppet over med mindre du løser problemet manuelt. Hvis du prøver på nytt, inkluderes posten i neste synkronisering.|
|**Synkroniser**|Appen vil prøve å løse en konflikt der en post ble endret i begge bedriftsappene. Du kan velge hvilken versjon av posten som skal brukes i begge appene.|
|**Gjenopprett poster** og **Slett poster**|Dette er nyttig i tilfeller der en post ble slettet i en av appene. Slett poster sletter posten i appen der den fortsatt finnes. Gjenopprett gjenskaper posten i appen der den ble slettet.|

## <a name="to-view-the-synchronization-log-for-a-specific-manually-synchronized-record"></a>Slik viser du synkroniseringsloggen for en bestemt (manuelt synkronisert) post
1. Åpne for eksempel en kunde, vare eller en annen post som synkroniserer data mellom [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)].
2. Velg **Synkroniseringslogg**-handlingen for å vise synkroniseringsloggen for en valgt post. For eksempel en bestemt kunde du synkroniserte manuelt.

## <a name="see-also"></a>Se også  
[Sette opp brukerkontoer for integrasjon med Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Bruke Dynamics 365 Sales fra Business Central](marketing-integrate-dynamicscrm.md)
