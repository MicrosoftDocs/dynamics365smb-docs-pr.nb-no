---
title: Bruke og endre lagrede innstillinger i rapporter | Microsoft-dokumentasjon
description: "Beskriver hvordan du bruker forhåndsdefinerte alternativer og filtre til å tilpasse rapporter og generere riktige data."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9e5f7417579a5ba0629032cf9fa664e0060b9cbf
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2017

---
# <a name="saved-settings-on-reports"></a><span data-ttu-id="b17f4-103">Lagrede innstillinger i rapporter</span><span class="sxs-lookup"><span data-stu-id="b17f4-103">Saved Settings on Reports</span></span>
<span data-ttu-id="b17f4-104">Avhengig av hvilken rapport som skal kjøres, kan det vises en side som lar deg angi bestemte alternativer og filtre for å endre dataene som er inkludert i den genererte rapporten.</span><span class="sxs-lookup"><span data-stu-id="b17f4-104">Depending on the report that is run, you might be presented with a page that lets you to set certain options and filters for changing the data that is included in the generated report.</span></span> <span data-ttu-id="b17f4-105">Denne siden kalles rapportforespørselssiden.</span><span class="sxs-lookup"><span data-stu-id="b17f4-105">This page is known as the report request page.</span></span> <span data-ttu-id="b17f4-106">En rapport kan inneholde en eller flere *lagrede innstillinger* som du kan bruke på rapporten fra forespørselssiden.</span><span class="sxs-lookup"><span data-stu-id="b17f4-106">A report can include one or more *saved settings* that you can apply to the report from the request page.</span></span> <span data-ttu-id="b17f4-107">*Lagrede innstillinger* er i hovedsak forhåndsdefinerte alternativer og filtre.</span><span class="sxs-lookup"><span data-stu-id="b17f4-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="b17f4-108">Lagrede innstillinger er en rask og pålitelig metode for å generere konsekvent rapporter som inneholder de riktige dataene.</span><span class="sxs-lookup"><span data-stu-id="b17f4-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span>

<span data-ttu-id="b17f4-109">Du kan se de lagrede innstillingene som er tilgjengelige for en rapport i delen **Lagrede innstillinger** i rapportforespørselssiden.</span><span class="sxs-lookup"><span data-stu-id="b17f4-109">You can see the saved settings that are available to you for a report in **Saved Settings** section of the report request page.</span></span>  

## <a name="to-apply-saved-settings-to-a-report"></a><span data-ttu-id="b17f4-110">Slik bruker du lagrede innstillinger på en rapport</span><span class="sxs-lookup"><span data-stu-id="b17f4-110">To apply saved settings to a report</span></span>
1. <span data-ttu-id="b17f4-111">Åpne rapporten.</span><span class="sxs-lookup"><span data-stu-id="b17f4-111">Open the report.</span></span>

   <span data-ttu-id="b17f4-112">Rapportforespørselssiden vises.</span><span class="sxs-lookup"><span data-stu-id="b17f4-112">The report request page appears.</span></span>    
2. <span data-ttu-id="b17f4-113">I delen **Lagrede innstillinger** på siden, setter du **Navn**-feltet til de lagrede innstillingene du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="b17f4-113">In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.</span></span>

   <span data-ttu-id="b17f4-114">Delen **Lagrede innstillinger** vises bare hvis rapporten er kjørt tidligere eller hvis det finnes eksisterende oppføringer for lagrede innstillinger.</span><span class="sxs-lookup"><span data-stu-id="b17f4-114">The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries.</span></span> <span data-ttu-id="b17f4-115">Oppføringen med lagrede innstillinger, som kalles **Sist brukte alternativer og filtre**, er alltid tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="b17f4-115">The saved settings entry called **Last used options and filters** is always available.</span></span> <span data-ttu-id="b17f4-116">Disse innstillingene er verdiene for alternativet og filteret som ble brukt sist gang du kjørte rapporten.</span><span class="sxs-lookup"><span data-stu-id="b17f4-116">These settings are the option and filter values that were used the last time you ran the report.</span></span>

## <a name="administer-saved-report-settings-for-users"></a><span data-ttu-id="b17f4-117">Administrere lagrede rapportinnstillinger for brukere</span><span class="sxs-lookup"><span data-stu-id="b17f4-117">Administer saved report settings for users</span></span>
<span data-ttu-id="b17f4-118">Hvis du har riktige tillatelser, kan du vise, opprette og endre de lagrede innstillingene for alle rapporter for alle brukere i firmaet.</span><span class="sxs-lookup"><span data-stu-id="b17f4-118">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in company.</span></span> <span data-ttu-id="b17f4-119">Du kan tilordne lagrede innstillingene for en rapport til enkeltbrukere eller alle brukerne i firmaet.</span><span class="sxs-lookup"><span data-stu-id="b17f4-119">You can assign saved settings for a report to individual users or all users in the company.</span></span>

<span data-ttu-id="b17f4-120">Du kan administrere lagrede innstillinger fra siden 1506 **Rapportinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="b17f4-120">You manage saved settings from page 1506 **Reports Settings**.</span></span> <span data-ttu-id="b17f4-121">Du åpner denne siden ved å velge ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Rapportinnstillinger** og deretter velge den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b17f4-121">To open this page, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Settings**, and then choose the related link.</span></span>

<span data-ttu-id="b17f4-122">Fra siden **Rapportinnstillinger** kan du opprette en ny innstillinger fra bunnen av eller du kan kopiere og endre eksisterende innstillinger.</span><span class="sxs-lookup"><span data-stu-id="b17f4-122">From the **Report Settings** page, you can create a new settings from scratch or you can make a copy and modify existing settings.</span></span> <span data-ttu-id="b17f4-123">Hvis du vil endre alternativer og filtre for en innstillingene, velger du **Rediger**-handling.</span><span class="sxs-lookup"><span data-stu-id="b17f4-123">To modify the options and filters for a settings, choose the **Edit** action.</span></span>

<span data-ttu-id="b17f4-124">**Merknader:**</span><span class="sxs-lookup"><span data-stu-id="b17f4-124">**Notes:**</span></span>

* <span data-ttu-id="b17f4-125">Funksjonen for lagrede innstillinger i rapporter gjelder bare når SaveValues-egenskapen for forespørselssiden er satt til Ja.</span><span class="sxs-lookup"><span data-stu-id="b17f4-125">The saved settings feature on reports is only relevant when the SaveValues property of the request page is set to Yes.</span></span> <span data-ttu-id="b17f4-126">SaveValues-egenskapen angis i utviklingsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="b17f4-126">The SaveValues property property is set in the development environment.</span></span>
* <span data-ttu-id="b17f4-127">Hvis du oppretter et element for lagrede innstillinger for alle brukere, og det har samme navn som eksisterende lagrede innstillinger for en bestemt bruker, kan ikke brukeren bruke de lagrede innstillingene som er tilordnet til alle.</span><span class="sxs-lookup"><span data-stu-id="b17f4-127">If you create a saved settings item for all users, and it has the same name as an existing saved settings for a specific user, then that user will not be able to use the saved settings that is assigned to everyone.</span></span>  <span data-ttu-id="b17f4-128">I feltet Lagrede innstillinger på rapportforespørselssiden, vil brukeren se to lagrede innstillingsalternativer med samme navn.</span><span class="sxs-lookup"><span data-stu-id="b17f4-128">In the Saved Settings field on the report request page, the user will see two saved settings options with the same name.</span></span> <span data-ttu-id="b17f4-129">Uansett hvilket alternativ som velges, vil imidlertid de brukerspesifikke lagrede innstillingene bli brukt.</span><span class="sxs-lookup"><span data-stu-id="b17f4-129">However, no matter which option he chooses, the user-specific saved settings will be used.</span></span>

## <a name="see-also"></a><span data-ttu-id="b17f4-130">Se også</span><span class="sxs-lookup"><span data-stu-id="b17f4-130">See Also</span></span>
[<span data-ttu-id="b17f4-131">Planlegge en rapport for kjøring</span><span class="sxs-lookup"><span data-stu-id="b17f4-131">Schedule a Rpeort to Run</span></span>](ui-schedule-report.md)  

