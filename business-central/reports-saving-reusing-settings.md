---
title: Bruke og endre lagrede innstillinger i rapporter | Microsoft-dokumentasjon
description: Beskriver hvordan du bruker forhåndsdefinerte alternativer og filtre til å tilpasse rapporter og generere riktige data.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 3e7b00d54a9c655a77b7b7f4854e59993866427e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251226"
---
# <a name="managing-saved-settings-on-reports"></a><span data-ttu-id="d07ab-103">Administrere lagrede innstillinger i rapporter</span><span class="sxs-lookup"><span data-stu-id="d07ab-103">Managing Saved Settings on Reports</span></span>
<span data-ttu-id="d07ab-104">Når en rapport skal kjøres, ser brukere vanligvis en side der de kan angi bestemte alternativer og filtre for å endre dataene som er inkludert i den genererte rapporten.</span><span class="sxs-lookup"><span data-stu-id="d07ab-104">When running a reports, users are typically presented with a page that lets them set certain options and filters for changing the data that is included in the generated report.</span></span> <span data-ttu-id="d07ab-105">Denne siden kalles rapportforespørselssiden.</span><span class="sxs-lookup"><span data-stu-id="d07ab-105">This page is called the report request page.</span></span> <span data-ttu-id="d07ab-106">En rapport kan inneholde en eller flere *lagrede innstillinger* som brukere kan bruke på rapporten fra forespørselssiden.</span><span class="sxs-lookup"><span data-stu-id="d07ab-106">A report can include one or more *saved settings* that users can apply to the report from the request page.</span></span> <span data-ttu-id="d07ab-107">*Lagrede innstillinger* er i hovedsak forhåndsdefinerte alternativer og filtre.</span><span class="sxs-lookup"><span data-stu-id="d07ab-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="d07ab-108">Lagrede innstillinger er en rask, pålitelig og konsekvent metode for å generere rapporter som inneholder de riktige dataene.</span><span class="sxs-lookup"><span data-stu-id="d07ab-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span> <span data-ttu-id="d07ab-109">Hvis du vil ha mer informasjon om hvordan lagrede innstillingene brukes, kan du se [Bruke lagrede innstillinger](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="d07ab-109">For more information about how saved settings are used, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

<span data-ttu-id="d07ab-110">Hvis du har riktige tillatelser, kan du vise, opprette og endre de lagrede innstillingene for alle rapporter for alle brukere i firmaet.</span><span class="sxs-lookup"><span data-stu-id="d07ab-110">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in company.</span></span> <span data-ttu-id="d07ab-111">Du kan tilordne lagrede innstillingene for en rapport til enkeltbrukere eller alle brukerne i firmaet.</span><span class="sxs-lookup"><span data-stu-id="d07ab-111">You can assign saved settings for a report to individual users or all users in the company.</span></span>

<!--
## Apply saved settings to a report
1. Open the report.

   The report request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="create-and-modify-saved-settings-for-all-users"></a><span data-ttu-id="d07ab-112">Opprette og endre lagrede innstillinger for alle brukere</span><span class="sxs-lookup"><span data-stu-id="d07ab-112">Create and modify saved settings for all users</span></span>
<span data-ttu-id="d07ab-113">Du kan administrere lagrede innstillinger fra siden **1560 Rapportinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="d07ab-113">You manage saved settings from page **1560 Reports Settings**.</span></span> <span data-ttu-id="d07ab-114">Det er to måter å åpne en side på:</span><span class="sxs-lookup"><span data-stu-id="d07ab-114">There are two ways to open this page:</span></span>
-   <span data-ttu-id="d07ab-115">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rapportinnstillinger**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="d07ab-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Settings**, and then choose the related link.</span></span>
-   <span data-ttu-id="d07ab-116">Åpne en rapport, velg oppslag ved siden av boksen **Bruk standardverdi fra:**, og velg **Velge fra hele listen**.</span><span class="sxs-lookup"><span data-stu-id="d07ab-116">Open a report, choose the lookup next to the **Used default values from:** box, choose **Select from full list**.</span></span>

<span data-ttu-id="d07ab-117">Siden viser alle eksisterende lagrede innstillinger for alle brukere.</span><span class="sxs-lookup"><span data-stu-id="d07ab-117">The page displays all the existing save settings entries for all users.</span></span> <span data-ttu-id="d07ab-118">Hvis det er et brukernavn i kolonnen **Tilordnet**, kan bare den brukeren bruke innstillingene som er lagret for den tilknyttede rapporten.</span><span class="sxs-lookup"><span data-stu-id="d07ab-118">If there is a user name in the **Assigned to** column, only that user can use the saved settings for the associated report.</span></span> <span data-ttu-id="d07ab-119">Hvis det er en hake i kolonnen **Del med alle brukerne**, kan alle brukere bruke innstillingene som er lagret i rapporten.</span><span class="sxs-lookup"><span data-stu-id="d07ab-119">If there is a check mark in the **Share with all users** column, all users can use the saved settings for the report.</span></span>

<span data-ttu-id="d07ab-120">Fra siden **Rapportinnstillinger**-siden kan du:</span><span class="sxs-lookup"><span data-stu-id="d07ab-120">From the **Report Settings** page, you can:</span></span>
-   <span data-ttu-id="d07ab-121">Velg **Ny** for å opprette en helt ny post med lagrede innstillinger.</span><span class="sxs-lookup"><span data-stu-id="d07ab-121">Choose **New** to create a new saved settings entry from scratch.</span></span>
-   <span data-ttu-id="d07ab-122">Velg en post med lagrede innstillinger fra oversikten, og velg **Kopier** for å lage en kopi.</span><span class="sxs-lookup"><span data-stu-id="d07ab-122">Select a saved settings entry from the list, and choose **Copy** to create a copy.</span></span>
-   <span data-ttu-id="d07ab-123">Velg en post med lagrede innstillinger fra oversikten, og velg **Rediger** for å endre en post med lagrede innstillinger.</span><span class="sxs-lookup"><span data-stu-id="d07ab-123">Select a saved settings entry from the list, and choose **Edit** to modify a saved settings entry.</span></span>


> [!Important]
> <span data-ttu-id="d07ab-124">Vurder navnet som du gir en post med lagrede innstillinger.</span><span class="sxs-lookup"><span data-stu-id="d07ab-124">Consider the name that you give a saved settings entry.</span></span> <span data-ttu-id="d07ab-125">Hvis du oppretter en post med lagrede innstillinger for alle brukere, og den har samme navn som en eksisterende post med lagrede innstillinger som er tilordnet en bestemt bruker, kan brukeren ikke bruke posten med lagrede innstillinger som er tilordnet til alle.</span><span class="sxs-lookup"><span data-stu-id="d07ab-125">If you create a saved settings entry for all users, and you give it the same name as an existing saved settings entry that is assigned to a specific user only, then that user will not be able to use the saved settings entry that is assigned to everyone.</span></span>  <span data-ttu-id="d07ab-126">I **Lagrede innstillinger** på rapportforespørselssiden, vil brukeren se to lagrede innstillingsposter med samme navn.</span><span class="sxs-lookup"><span data-stu-id="d07ab-126">Under **Saved Settings** on the report request page, the user will see two saved settings entries with the same name.</span></span> <span data-ttu-id="d07ab-127">Uansett hvilket alternativ som velges, vil imidlertid den brukerspesifikke posten med lagrede innstillingene bli brukt.</span><span class="sxs-lookup"><span data-stu-id="d07ab-127">However, no matter which option he chooses, the user-specific saved settings entry will be used.</span></span>

> [!NOTE]
> <span data-ttu-id="d07ab-128">Funksjonen for lagrede innstillinger i rapporter er kun tilgjengelig når [SaveValues-egenskapen](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) for forespørselssiden er satt til `Yes`.</span><span class="sxs-lookup"><span data-stu-id="d07ab-128">The saved settings feature is available only on reports where the [SaveValues property](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) of the report's request page is set to `Yes`.</span></span> <span data-ttu-id="d07ab-129">**SaveValues**-egenskapen angis i utviklingsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="d07ab-129">The **SaveValues** property is set in the development environment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d07ab-130">Se også</span><span class="sxs-lookup"><span data-stu-id="d07ab-130">See Also</span></span>
[<span data-ttu-id="d07ab-131">Arbeide med rapporter og kjørsler</span><span class="sxs-lookup"><span data-stu-id="d07ab-131">Working with Reports and Batch Jobs</span></span>](ui-work-report.md)  
