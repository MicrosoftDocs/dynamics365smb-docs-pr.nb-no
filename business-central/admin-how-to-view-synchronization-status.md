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
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245688"
---
# <a name="view-the-status-of-a-synchronization"></a><span data-ttu-id="0c23e-103">Vise statusen for en synkronisering</span><span class="sxs-lookup"><span data-stu-id="0c23e-103">View the Status of a Synchronization</span></span>
<span data-ttu-id="0c23e-104">Du kan vise statusen for individuelle synkroniseringsjobber som har blitt kjørt for [!INCLUDE[crm_md](includes/crm_md.md)]-integrasjon.</span><span class="sxs-lookup"><span data-stu-id="0c23e-104">You can view the status of the individual synchronization jobs that have been run for [!INCLUDE[crm_md](includes/crm_md.md)] integration.</span></span> <span data-ttu-id="0c23e-105">Dette inkluderer synkroniseringsjobber som har blitt kjørt fra jobbkøen, og manuelle synkroniseringsjobber som ble utført på poster fra [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="0c23e-105">This includes synchronization jobs that have been run from the job queue and manual synchronization jobs that were performed on records from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="0c23e-106">Dette er nyttig når du feilsøker synkroniseringsproblemer, fordi det gir deg tilgang til opplysninger om bestemte feil.</span><span class="sxs-lookup"><span data-stu-id="0c23e-106">This is helpful when troubleshooting synchronization problems because it gives you access to details about specific errors.</span></span>

### <a name="to-view-all-synchronization-issues"></a><span data-ttu-id="0c23e-107">Vise alle synkroniseringsproblemer</span><span class="sxs-lookup"><span data-stu-id="0c23e-107">To view all synchronization issues</span></span>
1. <span data-ttu-id="0c23e-108">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Feil ved synkronisering av koblede data**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0c23e-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Coupled Data Synchronization Errors**, and then choose the related link.</span></span>
2. <span data-ttu-id="0c23e-109">På siden **Feil ved synkronisering av koblede data** kan du se alle problemer som oppstod i synkroniseringen mellom [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)], filtrere og sortere poster på siden etter tabell, feilmelding og utføre handlinger som **Prøv på nytt** eller **Fjern kobling** for å løse problemer enkeltvis eller samlet.</span><span class="sxs-lookup"><span data-stu-id="0c23e-109">On the **Coupled Data Synchronization Errors** page you can view of all issues that occurred in synchronization of data between [!INCLUDE[crm_md](includes/crm_md.md)] and [!INCLUDE[d365fin](includes/d365fin_md.md)], filter and sort records in the page by table, error message and take actions such as **Retry** or **Remove Coupling** to resolve issues one by one or in bulk.</span></span>

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a><span data-ttu-id="0c23e-110">Vise synkroniseringslogg for bestemt (manuelt synkronisert) post</span><span class="sxs-lookup"><span data-stu-id="0c23e-110">To view synchronization log for specific (manually synchronized) record</span></span>
1. <span data-ttu-id="0c23e-111">Åpne for eksempel kunde, vare eller en annen post som synkroniserer data mellom [!INCLUDE[d365fin](includes/d365fin_md.md)] og Sales</span><span class="sxs-lookup"><span data-stu-id="0c23e-111">Open, for example, customer, item or any other record that is synchronizing data between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Sales</span></span>
2. <span data-ttu-id="0c23e-112">Velg **Synkroniseringslogg**-handling for å vise synkroniseringsloggen for valgt post, for eksempel bestemt kunde du synkroniserte manuelt</span><span class="sxs-lookup"><span data-stu-id="0c23e-112">Choose **Synchronization Log** action to view the synchronization log for selected record, for example, specific customer you synchronized manually</span></span>

## <a name="see-also"></a><span data-ttu-id="0c23e-113">Se også</span><span class="sxs-lookup"><span data-stu-id="0c23e-113">See Also</span></span>  
[<span data-ttu-id="0c23e-114">Definere Dynamics 365 for Sales-integrering i Business Central</span><span class="sxs-lookup"><span data-stu-id="0c23e-114">Setting Up Dynamics 365 for Sales Integration in Business Central</span></span>](admin-setting-up-integration-with-dynamics-sales.md)  
[<span data-ttu-id="0c23e-115">Bruke Dynamics 365 for Sales fra Business Central</span><span class="sxs-lookup"><span data-stu-id="0c23e-115">Using Dynamics 365 for Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
