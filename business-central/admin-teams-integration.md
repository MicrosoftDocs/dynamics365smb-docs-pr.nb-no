---
title: Administrere Microsoft Teams-integrering med Business Central | Microsoft Docs
description: Administrer Business Central-integrering med Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: 3c04dfb2f77eba906b2567ca9438849e1cc20861
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989361"
---
# <a name="managing-microsoft-teams-integration-with-business-central"></a><span data-ttu-id="feb64-103">Administrere Microsoft Teams-integrering med Business Central</span><span class="sxs-lookup"><span data-stu-id="feb64-103">Managing Microsoft Teams Integration with Business Central</span></span>

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

<span data-ttu-id="feb64-104">Denne artikkelen gir en oversikt over hva du kan gjøre som administrator for å styre Microsoft Teams-integrasjon med [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="feb64-104">This article provides an overview of what you can do as an administrator to control Microsoft Teams integration with [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>

## <a name="in-microsoft-teams"></a><span data-ttu-id="feb64-105">I Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="feb64-105">In Microsoft Teams</span></span>

### <a name="minimum-requirements"></a><span data-ttu-id="feb64-106">Minstekrav</span><span class="sxs-lookup"><span data-stu-id="feb64-106">Minimum requirements</span></span>

<span data-ttu-id="feb64-107">Denne delen beskriver minimumskravene for at [!INCLUDE [prodshort](includes/prodshort.md)]-appfunksjonene skal fungere i Teams.</span><span class="sxs-lookup"><span data-stu-id="feb64-107">This section describes the minimum requirements for the [!INCLUDE [prodshort](includes/prodshort.md)] app features to work in Teams.</span></span>

- <span data-ttu-id="feb64-108">Nødvendige lisenser</span><span class="sxs-lookup"><span data-stu-id="feb64-108">Required licenses</span></span>

    <span data-ttu-id="feb64-109">Denne tabellen gir deg en oversikt over nødvendige lisenser for at [!INCLUDE [prodshort](includes/prodshort.md)]-appfunksjonene skal fungere i Teams.</span><span class="sxs-lookup"><span data-stu-id="feb64-109">This table gives you an overview of the licenses needed for the [!INCLUDE [prodshort](includes/prodshort.md)] app features to work in Teams.</span></span>

    |<span data-ttu-id="feb64-110">Hva</span><span class="sxs-lookup"><span data-stu-id="feb64-110">What</span></span>|<span data-ttu-id="feb64-111">Teams-lisens</span><span class="sxs-lookup"><span data-stu-id="feb64-111">Teams license</span></span>|<span data-ttu-id="feb64-112">Business Central-lisens</span><span class="sxs-lookup"><span data-stu-id="feb64-112">Business Central license</span></span>|
    |----|---|---|
    |<span data-ttu-id="feb64-113">Lim inn en kobling til en [!INCLUDE [prodshort](includes/prodshort.md)]-post i en samtale, og send den som et kort.</span><span class="sxs-lookup"><span data-stu-id="feb64-113">Paste a link to a [!INCLUDE [prodshort](includes/prodshort.md)] record into a conversation, and send it as a card.</span></span>|<span data-ttu-id="feb64-114">![avmerking](media/check.png "avmerking")</span><span class="sxs-lookup"><span data-stu-id="feb64-114">![check mark](media/check.png "check")</span></span>|<span data-ttu-id="feb64-115">![avmerking](media/check.png "avmerking")</span><span class="sxs-lookup"><span data-stu-id="feb64-115">![check mark](media/check.png "check")</span></span>|
    |<span data-ttu-id="feb64-116">Vis et kort for en [!INCLUDE [prodshort](includes/prodshort.md)]-post i en samtale.</span><span class="sxs-lookup"><span data-stu-id="feb64-116">View a card of a [!INCLUDE [prodshort](includes/prodshort.md)] record in a conversation.</span></span>|<span data-ttu-id="feb64-117">![avmerking](media/check.png "avmerking")</span><span class="sxs-lookup"><span data-stu-id="feb64-117">![check mark](media/check.png "check")</span></span>||
    |<span data-ttu-id="feb64-118">Vis flere detaljer i kort for en [!INCLUDE [prodshort](includes/prodshort.md)]-post i en samtale.</span><span class="sxs-lookup"><span data-stu-id="feb64-118">View more details of card for a [!INCLUDE [prodshort](includes/prodshort.md)] record in a conversation.</span></span>|<span data-ttu-id="feb64-119">![avmerking](media/check.png "avmerking")</span><span class="sxs-lookup"><span data-stu-id="feb64-119">![check mark](media/check.png "check")</span></span>|<span data-ttu-id="feb64-120">![avmerking](media/check.png "avmerking")</span><span class="sxs-lookup"><span data-stu-id="feb64-120">![check mark](media/check.png "check")</span></span>|

- <span data-ttu-id="feb64-121">Tillat URL-forhåndsvisninger</span><span class="sxs-lookup"><span data-stu-id="feb64-121">Allow URL previews</span></span>

    <span data-ttu-id="feb64-122">Policyinnstillingen **Tillat URL-forhåndsvisninger** må være aktivert.</span><span class="sxs-lookup"><span data-stu-id="feb64-122">**Allow URL previews** policy setting must be turned on.</span></span> <span data-ttu-id="feb64-123">Ellers kan ikke et kort genereres for Business Central-koblinger som limes inn i en Teams-samtale.</span><span class="sxs-lookup"><span data-stu-id="feb64-123">Otherwise, a card can't be generated for Business Central links pasted into a Teams conversation.</span></span> <span data-ttu-id="feb64-124">Hvis du vil ha mer informasjon om denne innstillingen, kan du se [Administrere meldingspolicyer i Teams](/microsoftteams/messaging-policies-in-teams).</span><span class="sxs-lookup"><span data-stu-id="feb64-124">For more information about this setting, see [Manage messaging policies in Teams](/microsoftteams/messaging-policies-in-teams).</span></span>

### <a name="managing-the-business-central-app-optional"></a><span data-ttu-id="feb64-125">Administrere Business Central-appen (valgfritt)</span><span class="sxs-lookup"><span data-stu-id="feb64-125">Managing the Business Central app (optional)</span></span>

<span data-ttu-id="feb64-126">Som Teams-administrator kan du behandle alle apper for organisasjonen, inkludert [!INCLUDE [prodshort](includes/prodshort.md)]-appen.</span><span class="sxs-lookup"><span data-stu-id="feb64-126">As a Teams administrator, you can manage all apps for your organization, including the [!INCLUDE [prodshort](includes/prodshort.md)] app.</span></span> <span data-ttu-id="feb64-127">Du kan godkjenne eller installere [!INCLUDE [prodshort](includes/prodshort.md)]-appen for organisasjonen, hindre at brukere installerer appen, med mer.</span><span class="sxs-lookup"><span data-stu-id="feb64-127">You can approve or install the [!INCLUDE [prodshort](includes/prodshort.md)] app for your organization, block user's from installing the app, and more.</span></span>

<span data-ttu-id="feb64-128">Hvis du vil ha mer informasjon, kan du se følgende artikler i Microsoft Teams-dokumentasjonen:</span><span class="sxs-lookup"><span data-stu-id="feb64-128">For more information, see the following articles in the Microsoft Teams documentation:</span></span>

- [<span data-ttu-id="feb64-129">Behandle appene i Microsoft Teams-administrasjonssenteret</span><span class="sxs-lookup"><span data-stu-id="feb64-129">Manage your apps in the Microsoft Teams admin center</span></span>](https://docs.microsoft.com/MicrosoftTeams/manage-apps)
- [<span data-ttu-id="feb64-130">Administrere policyer for appoppsett i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="feb64-130">Manage app setup policies in Microsoft Teams</span></span>](https://docs.microsoft.com/microsoftteams/teams-app-setup-policies)

## <a name="in-prodshort"></a><span data-ttu-id="feb64-131">I [!INCLUDE [prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="feb64-131">In [!INCLUDE [prodshort](includes/prodshort.md)]</span></span>

### <a name="minimum-requirements"></a><span data-ttu-id="feb64-132">Minstekrav</span><span class="sxs-lookup"><span data-stu-id="feb64-132">Minimum requirements</span></span>

- <span data-ttu-id="feb64-133">[!INCLUDE [prodshort](includes/prodshort.md)] versjon:</span><span class="sxs-lookup"><span data-stu-id="feb64-133">[!INCLUDE [prodshort](includes/prodshort.md)] version:</span></span>

    <span data-ttu-id="feb64-134">[!INCLUDE [prodshort](includes/prodshort.md)] 2020 lanseringsbølge 2 (versjon 17) eller nyere.</span><span class="sxs-lookup"><span data-stu-id="feb64-134">[!INCLUDE [prodshort](includes/prodshort.md)] 2020 release wave 2 (version 17) or later.</span></span> <span data-ttu-id="feb64-135">Teams-integrasjon støttes bare for [!INCLUDE [prodshort](includes/prodshort.md)] online, ikke lokalt.</span><span class="sxs-lookup"><span data-stu-id="feb64-135">Teams integration is only supported for [!INCLUDE [prodshort](includes/prodshort.md)] online; not on-premises.</span></span>

- <span data-ttu-id="feb64-136">Codeunit **2718 Page Summary Provider** publiseres som en webtjeneste:</span><span class="sxs-lookup"><span data-stu-id="feb64-136">Codeunit **2718 Page Summary Provider** is published as a web service:</span></span>

    <span data-ttu-id="feb64-137">Denne codeunit publiseres som en webtjeneste som standard.</span><span class="sxs-lookup"><span data-stu-id="feb64-137">This codeunit is published as a web service by default.</span></span> <span data-ttu-id="feb64-138">Codeunit-en er en del av [!INCLUDE [prodshort](includes/prodshort.md)]-systemapplikasjonen.</span><span class="sxs-lookup"><span data-stu-id="feb64-138">The codeunit is part of the [!INCLUDE [prodshort](includes/prodshort.md)] system application.</span></span> <span data-ttu-id="feb64-139">Den brukes til å hente feltdataene for en [!INCLUDE [prodshort](includes/prodshort.md)]-side som legges til i en Teams-samtale.</span><span class="sxs-lookup"><span data-stu-id="feb64-139">It's used to get the field data for a [!INCLUDE [prodshort](includes/prodshort.md)] page added to a Teams conversation.</span></span> 

- <span data-ttu-id="feb64-140">Brukertillatelser:</span><span class="sxs-lookup"><span data-stu-id="feb64-140">User permissions:</span></span>

    <span data-ttu-id="feb64-141">For det meste kontrolleres sidene og dataene som brukere kan vise og redigere i en Teams-samtale, av tillatelsene deres i [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="feb64-141">For the most part, the pages and data that users can view and edit in a Teams conversation is controlled by their permissions in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>
    
    - <span data-ttu-id="feb64-142">For å lime inn en [!INCLUDE [prodshort](includes/prodshort.md)]-kobling i en Teams-samtale og la den utvides til et kort, må brukerne minst ha lesetillatelse på siden og tilhørende data.</span><span class="sxs-lookup"><span data-stu-id="feb64-142">To paste a [!INCLUDE [prodshort](includes/prodshort.md)] link into a Teams conversation and have it expand into a card, users must have at least read permission on the page and its data.</span></span>
    - <span data-ttu-id="feb64-143">Når et kort er sendt til en samtale, kan alle brukere i denne samtalen vise kortet uten tillatelse til Business Central.</span><span class="sxs-lookup"><span data-stu-id="feb64-143">Once a card is submitted into a conversation, any user in that conversation can view that card without permission to Business Central.</span></span>
    - <span data-ttu-id="feb64-144">For å vise flere detaljer for et kort eller åpne posten i [!INCLUDE [prodshort](includes/prodshort.md)], må brukere ha lesetillatelse på siden og tilhørende data.</span><span class="sxs-lookup"><span data-stu-id="feb64-144">To view more details for a card or open the record in [!INCLUDE [prodshort](includes/prodshort.md)], users must have read permission on the page and its data.</span></span>
    - <span data-ttu-id="feb64-145">For å endre data må brukere ha endringstillatelse.</span><span class="sxs-lookup"><span data-stu-id="feb64-145">To change data, user's need modify permissions.</span></span>
    
    <span data-ttu-id="feb64-146">Hvis du vil ha informasjon om tillatelser, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="feb64-146">For information about permissions, see [Assign Permissions to Users and Groups](ui-define-granular-permissions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="feb64-147">Se også</span><span class="sxs-lookup"><span data-stu-id="feb64-147">See Also</span></span>
[<span data-ttu-id="feb64-148">Oversikt over Business Central og Microsoft Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="feb64-148">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="feb64-149">[Installere [!INCLUDE [prodshort](includes/prodshort.md)]-appen for Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="feb64-149">[Install the [!INCLUDE [prodshort](includes/prodshort.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="feb64-150">Utvikle for Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="feb64-150">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[<span data-ttu-id="feb64-151">Komme i gang</span><span class="sxs-lookup"><span data-stu-id="feb64-151">Getting Started</span></span>](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
