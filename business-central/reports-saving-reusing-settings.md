---
title: Bruke og endre lagrede innstillinger i rapporter | Microsoft-dokumentasjon
description: Beskriver hvordan du bruker forhåndsdefinerte alternativer og filtre til å tilpasse rapporter og generere riktige data.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 3ace06e81029ea38bf393502743716b66b10fe74
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2316503"
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs"></a><span data-ttu-id="d2b7c-103">Behandle lagrede innstillinger for rapporter og satsvise jobber</span><span class="sxs-lookup"><span data-stu-id="d2b7c-103">Manage Saved Settings for Reports and Batch jobs</span></span>
<span data-ttu-id="d2b7c-104">Når en rapport skal kjøres, ser brukere vanligvis en side der de kan velge alternativer og angi filtre for å endre dataene som er inkludert i den genererte rapporten.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-104">When running reports, users are typically presented with a page that lets them select options and set filters to change the data that is included in the generated report.</span></span> <span data-ttu-id="d2b7c-105">Denne siden kalles forespørselssiden.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-105">This page is called the request page.</span></span> <span data-ttu-id="d2b7c-106">En rapport kan inneholde en eller flere *lagrede innstillinger* som brukere kan bruke på rapporten fra forespørselssiden.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-106">A report can include one or more *saved settings* that users can apply to the report from the request page.</span></span> <span data-ttu-id="d2b7c-107">*Lagrede innstillinger* er i hovedsak forhåndsdefinerte alternativer og filtre.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="d2b7c-108">Lagrede innstillinger er en rask, pålitelig og konsekvent metode for å generere rapporter som inneholder de riktige dataene.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span> <span data-ttu-id="d2b7c-109">Hvis du vil ha mer informasjon, kan du se [Bruke lagrede innstillinger](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="d2b7c-109">For more information, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

> [!NOTE]
> <span data-ttu-id="d2b7c-110">Dette emnet dreier seg hovedsakelig om "rapport", men lignende informasjon gjelder kjørsler.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-110">This topic refers mainly to "report", but similar information applies to batch jobs.</span></span>

<span data-ttu-id="d2b7c-111">Hvis du har riktige tillatelser, kan du vise, opprette og endre de lagrede innstillingene for alle rapporter for alle brukere i et selskap.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-111">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in a company.</span></span> <span data-ttu-id="d2b7c-112">Du kan tilordne lagrede innstillingene for en rapport til enkeltbrukere eller til alle brukerne i selskapet.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-112">You can assign saved settings for a report to individual users or to all users in the company.</span></span>

<!--
## Apply saved settings to a report
1. Open the report.

   The request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="to-create-and-modify-saved-settings-for-all-users"></a><span data-ttu-id="d2b7c-113">Opprette og endre lagrede innstillinger for alle brukere</span><span class="sxs-lookup"><span data-stu-id="d2b7c-113">To create and modify saved settings for all users</span></span>
<span data-ttu-id="d2b7c-114">Du kan administrere lagrede innstillinger på siden **Rapportinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-114">You manage saved settings on the **Reports Settings** page.</span></span> <span data-ttu-id="d2b7c-115">Det er to måter å åpne en side på:</span><span class="sxs-lookup"><span data-stu-id="d2b7c-115">There are two ways to open this page:</span></span>
-   <span data-ttu-id="d2b7c-116">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rapportinnstillinger**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Settings**, and then choose the related link.</span></span>
-   <span data-ttu-id="d2b7c-117">Åpne en rapport, velg oppslag i feltet **Bruk standardverdi fra:**, og velg handlingen **Velge fra hele listen**.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-117">Open a report, choose the lookup in the **Use default values from** field, and then choose the **Select from full list** action.</span></span>

<span data-ttu-id="d2b7c-118">Siden viser alle eksisterende lagrede innstillinger for alle brukere.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-118">The page displays all the existing saved settings entries for all users.</span></span> <span data-ttu-id="d2b7c-119">Hvis det er et brukernavn i feltet **Tilordnet**, kan bare den brukeren bruke innstillingene som er lagret for den tilknyttede rapporten.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-119">If there is a user name in the **Assigned to** field, only that user can use the saved settings for the associated report.</span></span> <span data-ttu-id="d2b7c-120">Hvis det er en hake i feltet **Del med alle brukerne**, kan alle brukere bruke innstillingene som er lagret i rapporten.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-120">If there is a check mark in the **Share with all users** field, all users can use the saved settings for the report.</span></span>

<span data-ttu-id="d2b7c-121">Fra siden **Rapportinnstillinger**-siden kan du:</span><span class="sxs-lookup"><span data-stu-id="d2b7c-121">From the **Report Settings** page, you can:</span></span>
-   <span data-ttu-id="d2b7c-122">Velg handlingen **Ny** for å opprette en helt ny post med lagrede innstillinger.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-122">Choose the **New** action to create a new saved settings entry from scratch.</span></span>
-   <span data-ttu-id="d2b7c-123">Velg en post med lagrede innstillinger fra oversikten, og velg handlingen **Kopier** for å lage en kopi.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-123">Select a saved settings entry from the list, and choose the **Copy** action to create a copy.</span></span>
-   <span data-ttu-id="d2b7c-124">Velg en post med lagrede innstillinger fra oversikten, og velg handlingen **Rediger** for å endre en post med lagrede innstillinger.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-124">Select a saved settings entry from the list, and choose the **Edit** action to modify a saved settings entry.</span></span>

> [!Important]
> <span data-ttu-id="d2b7c-125">Vurder navnet som du gir en post med lagrede innstillinger.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-125">Consider the name that you give a saved settings entry.</span></span> <span data-ttu-id="d2b7c-126">Hvis du oppretter en post med lagrede innstillinger for alle brukere, og den har samme navn som en eksisterende post med lagrede innstillinger som er tilordnet en bestemt bruker, kan brukeren ikke bruke posten med lagrede innstillinger som er tilordnet til alle.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-126">If you create a saved settings entry for all users, and you give it the same name as an existing saved settings entry that is assigned to a specific user only, then that user will not be able to use the saved settings entry that is assigned to everyone.</span></span>  <span data-ttu-id="d2b7c-127">I delen **Lagrede innstillinger** på rapportforespørselssiden vil brukeren se to lagrede innstillingsposter med samme navn.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-127">In the **Saved Settings** section on the request page, the user will see two saved settings entries with the same name.</span></span> <span data-ttu-id="d2b7c-128">Uansett hvilket alternativ som velges, vil imidlertid den brukerspesifikke posten med lagrede innstillingene bli brukt.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-128">However, no matter which option they choose, the user-specific saved settings entry will be used.</span></span>

> [!NOTE]
> <span data-ttu-id="d2b7c-129">Funksjonen Lagrede innstillinger er bare tilgjengelig i rapporter der [SaveValues-egenskapen](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) for forespørselssiden er satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-129">The Saved Settings feature is available only on reports where the [SaveValues property](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) of the report's request page is set to **Yes**.</span></span> <span data-ttu-id="d2b7c-130">**SaveValues**-egenskapen angis i utviklingsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="d2b7c-130">The **SaveValues** property is set in the development environment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d2b7c-131">Se også</span><span class="sxs-lookup"><span data-stu-id="d2b7c-131">See Also</span></span>
[<span data-ttu-id="d2b7c-132">Arbeide med rapporter, satsvise jobber og XML-porter</span><span class="sxs-lookup"><span data-stu-id="d2b7c-132">Working with Reports, Batch Jobs, and XMLports</span></span>](ui-work-report.md)  
