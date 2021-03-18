---
title: Vise statusen til synkroniseringsjobber | Microsoft Docs
description: Finn ut hvordan du viser statusen etter synkronisering av koblede poster.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: a54ce7805deafa5d67c3e25b89606a1a40634ad6
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378151"
---
# <a name="view-the-status-of-synchronization-jobs"></a><span data-ttu-id="d4733-103">Vise statusen til synkroniseringsjobber</span><span class="sxs-lookup"><span data-stu-id="d4733-103">View the Status of Synchronization Jobs</span></span>
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

<span data-ttu-id="d4733-104">Bruk siden **Feil ved synkronisering av koblede data** for å vise statusen til synkroniseringsjobber som har blitt kjørt for koblede poster i en Dataverse- eller [!INCLUDE[crm_md](includes/crm_md.md)]-integrasjon.</span><span class="sxs-lookup"><span data-stu-id="d4733-104">Use the **Coupled Data Synchronization Errors** page to view the status of synchronization jobs that have been run for coupled records in a Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)] integrations.</span></span> <span data-ttu-id="d4733-105">Dette inkluderer jobber som ble kjørt fra jobbkøen, og manuelle synkroniseringsjobber som kjørte på poster fra [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="d4733-105">This includes jobs that were run from the job queue and manual synchronization jobs that ran on records from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="d4733-106">Det kan for eksempel være nyttig å vise statusen deres når du feilsøker, fordi det gir deg tilgang til detaljer om feil relatert til koblede poster.</span><span class="sxs-lookup"><span data-stu-id="d4733-106">For example, viewing their status is helpful when troubleshooting because it gives you access to details about errors related to coupled records.</span></span> <span data-ttu-id="d4733-107">Vanligvis er disse feiltypene forårsaket av brukerhandlinger, for eksempel når følgende er tilfelle:</span><span class="sxs-lookup"><span data-stu-id="d4733-107">Typically, these types of errors are caused by user actions, for example, when:</span></span>  

* <span data-ttu-id="d4733-108">To personer foretok en endring i de samme dataene i begge bedriftsappene.</span><span class="sxs-lookup"><span data-stu-id="d4733-108">Two people made a change to the same data in both business apps.</span></span>
* <span data-ttu-id="d4733-109">Noen slettet data i en av appene, men ikke i begge.</span><span class="sxs-lookup"><span data-stu-id="d4733-109">Someone deleted data in one of the apps, but not both.</span></span>

> [!Note]
> <span data-ttu-id="d4733-110">Siden **Feil ved synkronisering av koblede data** viser informasjon om jobber relatert til koblede poster.</span><span class="sxs-lookup"><span data-stu-id="d4733-110">The **Coupled Data Synchronization Errors** page shows information about jobs related to coupled records.</span></span> <span data-ttu-id="d4733-111">Hvis du løser alle feilene, men poster fremdeles ikke synkroniseres, kan det ha noe å gjøre med en innstilling for integrasjonen.</span><span class="sxs-lookup"><span data-stu-id="d4733-111">If you resolve all of the errors but records are still not synchronizing, it might have something to do with a setting for the integration.</span></span> <span data-ttu-id="d4733-112">Vanligvis må disse feiltypene løses av administratoren.</span><span class="sxs-lookup"><span data-stu-id="d4733-112">Typically, your administrator will need to resolve those types of errors.</span></span>   

<!--

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098171]

-->

## <a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a><span data-ttu-id="d4733-113">Slik viser du og løser synkroniseringsfeil for koblede poster</span><span class="sxs-lookup"><span data-stu-id="d4733-113">To view and resolve synchronization errors for coupled records</span></span>
1. <span data-ttu-id="d4733-114">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Feil ved synkronisering av koblede data**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="d4733-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Coupled Data Synchronization Errors**, and then choose the related link.</span></span>
2. <span data-ttu-id="d4733-115">Siden **Feil ved synkronisering av koblede data** viser problemer som oppstod da du synkroniserte koblede poster.</span><span class="sxs-lookup"><span data-stu-id="d4733-115">The **Coupled Data Synchronization Errors** page shows issues that occurred when you synchronized coupled records.</span></span> <span data-ttu-id="d4733-116">Følgende tabell inneholder handlinger som du kan bruke til å løse problemer ett etter ett:</span><span class="sxs-lookup"><span data-stu-id="d4733-116">The following table includes actions that you can use to resolve issues one by one:</span></span>

|<span data-ttu-id="d4733-117">Handling</span><span class="sxs-lookup"><span data-stu-id="d4733-117">Action</span></span>|<span data-ttu-id="d4733-118">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d4733-118">Description</span></span>|
|----|----|
|<span data-ttu-id="d4733-119">**Fjern kobling**</span><span class="sxs-lookup"><span data-stu-id="d4733-119">**Remove Coupling**</span></span>|<span data-ttu-id="d4733-120">Opphever kobling av postene, og de vil ikke lenger synkroniseres.</span><span class="sxs-lookup"><span data-stu-id="d4733-120">Uncouples the records and they will no longer synchronize.</span></span> <span data-ttu-id="d4733-121">Hvis du vil starte synkroniseringen på nytt, må du koble dem sammen på nytt.</span><span class="sxs-lookup"><span data-stu-id="d4733-121">To restart the synchronization you must couple them again.</span></span> |
|<span data-ttu-id="d4733-122">**Prøv på nytt** og **Prøv alle på nytt**</span><span class="sxs-lookup"><span data-stu-id="d4733-122">**Retry** and **Retry All**</span></span>|<span data-ttu-id="d4733-123">For hver post der det oppdages en feil, blir synkronisering hoppet over med mindre du løser problemet.</span><span class="sxs-lookup"><span data-stu-id="d4733-123">For each record where an error is found, synchronization is skipped unless you fix the issue.</span></span> <span data-ttu-id="d4733-124">Prøv på nytt vil inkludere den valgte posten i neste synkronisering, og **Prøv alle på nytt** inkluderer alle oppføringene.</span><span class="sxs-lookup"><span data-stu-id="d4733-124">Retry will include the selected record in the next synchronization, and **Retry All** includes all of the records.</span></span>|
|<span data-ttu-id="d4733-125">**Synkroniser**</span><span class="sxs-lookup"><span data-stu-id="d4733-125">**Synchronize**</span></span>|<span data-ttu-id="d4733-126">Appen vil prøve å løse en konflikt der data ble endret i begge bedriftsappene.</span><span class="sxs-lookup"><span data-stu-id="d4733-126">The app will try to resolve a conflict where data was changed in both business apps.</span></span> <span data-ttu-id="d4733-127">Du kan velge dataene som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="d4733-127">You can choose the data to use.</span></span>|
|<span data-ttu-id="d4733-128">**Gjenopprett poster** og **Slett poster**</span><span class="sxs-lookup"><span data-stu-id="d4733-128">**Restore Records** and **Delete Records**</span></span>|<span data-ttu-id="d4733-129">Dette er nyttig i tilfeller der en post ble slettet i en av forretningsappene.</span><span class="sxs-lookup"><span data-stu-id="d4733-129">These are useful when a record was deleted in one of the business apps.</span></span> <span data-ttu-id="d4733-130">Slett poster sletter posten eller raden i appen der den fortsatt finnes.</span><span class="sxs-lookup"><span data-stu-id="d4733-130">Delete Records deletes the record or row in the app where it still exists.</span></span> <span data-ttu-id="d4733-131">Gjenopprett poster gjenskaper posten eller raden i forretningsappen der den ble slettet.</span><span class="sxs-lookup"><span data-stu-id="d4733-131">Restore Records recreates the record or row in the business app where it was deleted.</span></span>|

> [!NOTE]
> <span data-ttu-id="d4733-132">Hvis du vil redusere antall konflikter du må løse, kan du konfigurere integreringstabelltilordningene for å bruke disse handlingene automatisk.</span><span class="sxs-lookup"><span data-stu-id="d4733-132">To reduce the number of conflicts you need to resolve, you can set up your integration table mappings to apply these actions automatically.</span></span> <span data-ttu-id="d4733-133">Hvis du vil ha mer informasjon, kan du se [Tilordne integrasjonstabeller](admin-how-to-modify-table-mappings-for-synchronization.md#mapping-integration-tables).</span><span class="sxs-lookup"><span data-stu-id="d4733-133">For more information, [Mapping Integration Tables](admin-how-to-modify-table-mappings-for-synchronization.md#mapping-integration-tables).</span></span>

## <a name="to-view-the-synchronization-log-for-a-specific-manually-synchronized-record"></a><span data-ttu-id="d4733-134">Slik viser du synkroniseringsloggen for en bestemt (manuelt synkronisert) post</span><span class="sxs-lookup"><span data-stu-id="d4733-134">To view the synchronization log for a specific (manually synchronized) record</span></span>
1. <span data-ttu-id="d4733-135">Åpne for eksempel en kunde, vare eller en annen post som synkroniserer data mellom [!INCLUDE[prod_short](includes/prod_short.md)] og Dataverse eller [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d4733-135">Open, for example, a customer, item or any other record that is synchronizing data between [!INCLUDE[prod_short](includes/prod_short.md)] and Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
2. <span data-ttu-id="d4733-136">Velg **Synkroniseringslogg**-handlingen for å vise synkroniseringsloggen for en valgt post.</span><span class="sxs-lookup"><span data-stu-id="d4733-136">Choose the **Synchronization Log** action to view the synchronization log for a selected record.</span></span> <span data-ttu-id="d4733-137">For eksempel en bestemt kunde du synkroniserte manuelt.</span><span class="sxs-lookup"><span data-stu-id="d4733-137">For example, a specific customer you synchronized manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4733-138">Se også</span><span class="sxs-lookup"><span data-stu-id="d4733-138">See Also</span></span>  
[<span data-ttu-id="d4733-139">Sette opp brukerkontoer for integrasjon med Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="d4733-139">Setting Up User Accounts for Integrating with Dynamics 365 Sales</span></span>](admin-setting-up-integration-with-dynamics-sales.md)  
[<span data-ttu-id="d4733-140">Bruke Dynamics 365 Sales fra Business Central</span><span class="sxs-lookup"><span data-stu-id="d4733-140">Using Dynamics 365 Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]