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
# <a name="view-the-status-of-a-synchronization"></a><span data-ttu-id="c2b01-103">Vise statusen for en synkronisering</span><span class="sxs-lookup"><span data-stu-id="c2b01-103">View the Status of a Synchronization</span></span>
<span data-ttu-id="c2b01-104">Du kan vise statusen for individuelle synkroniseringsjobber som har blitt kjørt for [!INCLUDE[crm_md](includes/crm_md.md)]-integrasjon.</span><span class="sxs-lookup"><span data-stu-id="c2b01-104">You can view the status of the individual synchronization jobs that have been run for [!INCLUDE[crm_md](includes/crm_md.md)] integration.</span></span> <span data-ttu-id="c2b01-105">Dette inkluderer synkroniseringsjobber som har blitt kjørt fra jobbkøen, og manuelle synkroniseringsjobber som ble utført på poster fra [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c2b01-105">This includes synchronization jobs that have been run from the job queue and manual synchronization jobs that were performed on records from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="c2b01-106">Dette er nyttig når du feilsøker synkroniseringsproblemer, fordi det gir deg tilgang til opplysninger om bestemte feil.</span><span class="sxs-lookup"><span data-stu-id="c2b01-106">This is helpful when troubleshooting synchronization problems because it gives you access to details about specific errors.</span></span>

### <a name="to-view-synchronization-issues-for-coupled-records"></a><span data-ttu-id="c2b01-107">Slik viser du synkroniseringsproblemer for koblede poster</span><span class="sxs-lookup"><span data-stu-id="c2b01-107">To view synchronization issues for coupled records</span></span>
1. <span data-ttu-id="c2b01-108">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Feil ved synkronisering av koblede data**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="c2b01-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Coupled Data Synchronization Errors**, and then choose the related link.</span></span>
2. <span data-ttu-id="c2b01-109">Siden **Feil ved synkronisering av koblede data** viser problemer som oppstod da du synkroniserte koblede poster.</span><span class="sxs-lookup"><span data-stu-id="c2b01-109">The **Coupled Data Synchronization Errors** page shows issues that occurred when you synchronized coupled records.</span></span> <span data-ttu-id="c2b01-110">Du kan filtrere og sortere poster og utføre handlinger som for eksempel **Gjenopprett** eller **Slett poster** for å løse ett og ett problem.</span><span class="sxs-lookup"><span data-stu-id="c2b01-110">You can filter and sort records and take actions such as **Restore** or **Delete Records** to resolve issues one by one.</span></span>

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a><span data-ttu-id="c2b01-111">Vise synkroniseringslogg for bestemt (manuelt synkronisert) post</span><span class="sxs-lookup"><span data-stu-id="c2b01-111">To view synchronization log for specific (manually synchronized) record</span></span>
1. <span data-ttu-id="c2b01-112">Åpne for eksempel kunde, vare eller en annen post som synkroniserer data mellom [!INCLUDE[d365fin](includes/d365fin_md.md)] og Sales.</span><span class="sxs-lookup"><span data-stu-id="c2b01-112">Open, for example, a customer, item or any other record that is synchronizing data between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Sales.</span></span>
2. <span data-ttu-id="c2b01-113">Velg **Synkroniseringslogg**-handlingen for å vise synkroniseringsloggen for en valgt post.</span><span class="sxs-lookup"><span data-stu-id="c2b01-113">Choose the **Synchronization Log** action to view the synchronization log for a selected record.</span></span> <span data-ttu-id="c2b01-114">For eksempel en bestemt kunde du synkroniserte manuelt.</span><span class="sxs-lookup"><span data-stu-id="c2b01-114">For example, a specific customer you synchronized manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2b01-115">Se også</span><span class="sxs-lookup"><span data-stu-id="c2b01-115">See Also</span></span>  
[<span data-ttu-id="c2b01-116">Definere Dynamics 365 for Sales-integrering i Business Central</span><span class="sxs-lookup"><span data-stu-id="c2b01-116">Setting Up Dynamics 365 for Sales Integration in Business Central</span></span>](admin-setting-up-integration-with-dynamics-sales.md)  
[<span data-ttu-id="c2b01-117">Bruke Dynamics 365 for Sales fra Business Central</span><span class="sxs-lookup"><span data-stu-id="c2b01-117">Using Dynamics 365 for Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
