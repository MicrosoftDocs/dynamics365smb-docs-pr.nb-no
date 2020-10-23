---
title: Arbeide med Business Central-data i Microsoft Teams | Microsoft Docs
description: Lær hvordan du bruker Business Central-appen for Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: fbe024f724f018aae6d3aeb5251281bf4c3bfbde
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989427"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a><span data-ttu-id="85977-103">Arbeide med Business Central Data i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="85977-103">Working with Business Central Data in Microsoft Teams</span></span>

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

<span data-ttu-id="85977-104">[!INCLUDE [prodshort](includes/prodshort.md)] tilbyr en app som kobler Microsoft Teams til forretningsdataene dine i [!INCLUDE [prodshort](includes/prodshort.md)], slik at du raskt kan dele detaljer mellom gruppemedlemmer og svare raskere på forespørsler.</span><span class="sxs-lookup"><span data-stu-id="85977-104">[!INCLUDE [prodshort](includes/prodshort.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prodshort](includes/prodshort.md)], so you can quickly share details across team members and respond faster to inquiries.</span></span> <span data-ttu-id="85977-105">I denne artikkelen lærer du hvordan du bruker appen til å dele [!INCLUDE [prodshort](includes/prodshort.md)]-data med kolleger i en Teams-samtale.</span><span class="sxs-lookup"><span data-stu-id="85977-105">In this article, you'll learn how to use the app to share [!INCLUDE [prodshort](includes/prodshort.md)] data with coworkers in a Teams conversation.</span></span>

## <a name="overview"></a><span data-ttu-id="85977-106">Oversikt</span><span class="sxs-lookup"><span data-stu-id="85977-106">Overview</span></span>

<span data-ttu-id="85977-107">[!INCLUDE [prodshort](includes/prodshort.md)]-appen lar deg:</span><span class="sxs-lookup"><span data-stu-id="85977-107">The [!INCLUDE [prodshort](includes/prodshort.md)] app lets you:</span></span>

- <span data-ttu-id="85977-108">Kopier en kobling til en Business Central-oppføring, og lim den inn i en Teams-samtale for å dele med kollegene dine.</span><span class="sxs-lookup"><span data-stu-id="85977-108">Copy a link to any Business Central record and paste it into a Teams conversation to share with your coworkers.</span></span> <span data-ttu-id="85977-109">Koblingen vil utvide det til et kompakt, interaktivt kort som viser informasjon om posten.</span><span class="sxs-lookup"><span data-stu-id="85977-109">The link will expand that into a compact, interactive card that displays information about the record.</span></span>
- <span data-ttu-id="85977-110">Når du er i samtalen, kan du og kollegaene dine vise flere detaljer om posten, redigere data og utføre handlinger uten å forlate Teams.</span><span class="sxs-lookup"><span data-stu-id="85977-110">Once in the conversation, you and coworkers can view more details about the record, edit data, and take action - without leaving Teams.</span></span>

<span data-ttu-id="85977-111">[![Teams-integrering med Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="85977-111">[![Teams integration with Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="85977-112">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="85977-112">Prerequisites</span></span>

- <span data-ttu-id="85977-113">Du har tilgang til Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="85977-113">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="85977-114">Du har installert [!INCLUDE [prodshort](includes/prodshort.md)]-appen i Teams.</span><span class="sxs-lookup"><span data-stu-id="85977-114">You've installed the [!INCLUDE [prodshort](includes/prodshort.md)] app in Teams.</span></span> <span data-ttu-id="85977-115">Hvis du vil ha mer informasjon, se [Installere [!INCLUDE [prodshort](includes/prodshort.md)]-appen for Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="85977-115">For more information, see [Install the [!INCLUDE [prodshort](includes/prodshort.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>

> [!NOTE]
> <span data-ttu-id="85977-116">Alle deltakere i en Teams-samtale kan vise kort for Business Central-oppføringer som du sender til samtalen.</span><span class="sxs-lookup"><span data-stu-id="85977-116">All participants in a Teams conversation will be able to view cards for Business Central records that you submit to the conversation.</span></span> <span data-ttu-id="85977-117">Men hvis de vil vise flere detaljer om poster, ved hjelp av **Detaljer** eller **Eget vindu**-knappene på et kort, trenger de tilgang til [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="85977-117">But to view more details about records, by using the **Details** or **Pop-out** buttons on a card, they'll need access to [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="85977-118">Hvis du vil ha mer informasjon, kan du se [Administrere Microsoft Teams-integrering](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="85977-118">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>
<!--
- People You and your coworkers have the following permissions in [!INCLUDE [prodshort](includes/prodshort.md)]
  - To paste a [!INCLUDE [prodshort](includes/prodshort.md)] link into a Teams conversation and have it expand into a card, you have to have at least permission to view the page and its data.
  - Once a card is submitted into a conversation, any user in that conversation can view that card without having permission to Business Central.
  - For other users to view more details from card, they must also have view permission, as a minimum, to the page and its data. If they want to change data, they'll need modify permissions.

  Setting up permissions is typically done by an administrator. For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md).-->

## <a name="include-a-business-central-card-in-a-teams-conversation"></a><span data-ttu-id="85977-119">Ta med et Business Central-kort i en Teams-samtale</span><span class="sxs-lookup"><span data-stu-id="85977-119">Include a Business Central card in a Teams conversation</span></span>

1. <span data-ttu-id="85977-120">Logg på [!INCLUDE [prodshort](includes/prodshort.md)] ved å bruke leseren.</span><span class="sxs-lookup"><span data-stu-id="85977-120">Sign in to [!INCLUDE [prodshort](includes/prodshort.md)] using your browser.</span></span>
2. <span data-ttu-id="85977-121">Åpne posten du vil dele.</span><span class="sxs-lookup"><span data-stu-id="85977-121">Open the record that you want to share.</span></span>

    <span data-ttu-id="85977-122">Appen er utformet for å vise korttypesider fra [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="85977-122">The app is designed to display card type pages from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="85977-123">Så åpne en side som viser én enkelt post, for eksempel en vare, kunde eller ordre.</span><span class="sxs-lookup"><span data-stu-id="85977-123">So open a page that displays a single record, like an item, customer, or sales order.</span></span> <span data-ttu-id="85977-124">Du kan ikke bruke den til rollesentre eller sider som viser flere poster i en liste.</span><span class="sxs-lookup"><span data-stu-id="85977-124">You can't use it for role centers or pages that display several records in a list.</span></span>

3. <span data-ttu-id="85977-125">Kopier hele URL-adressen fra adresselinjen i nettleseren.</span><span class="sxs-lookup"><span data-stu-id="85977-125">Copy the entire URL from the browser's address bar.</span></span>

   ![Kopier URL-adressen for Business Central fra leseren](media/teams-url.png)
4. <span data-ttu-id="85977-127">Gå til Teams og start en samtale, som kan være en chat med en person, gruppe med personer eller en teamkanal.</span><span class="sxs-lookup"><span data-stu-id="85977-127">Go to Teams and start a conversation, which can be chat with a person, group of persons, or a team channel.</span></span>

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. <span data-ttu-id="85977-128">Lim inn URL-adressen i boksen der du legger til en melding.</span><span class="sxs-lookup"><span data-stu-id="85977-128">Paste the URL into the box where you add a message.</span></span>

   ![Lim inn URL-adresse for Business Central i Teams](media/teams-paste-url.png)
6. <span data-ttu-id="85977-130">Første gang du limer inn en kobling i en samtale, blir du bedt om å logge på [!INCLUDE [prodshort](includes/prodshort.md)] og gi samtykke til at appen kan hente data.</span><span class="sxs-lookup"><span data-stu-id="85977-130">The first time you paste a link into a conversation, you'll be asked to sign in to [!INCLUDE [prodshort](includes/prodshort.md)] and give consent for the app to retrieve data.</span></span> <span data-ttu-id="85977-131">Bare følg instruksjonene på skjermen.</span><span class="sxs-lookup"><span data-stu-id="85977-131">Just follow the on-screen instructions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="85977-132">Du trenger bare å utføre dette trinnet én gang.</span><span class="sxs-lookup"><span data-stu-id="85977-132">You'll only have to do this step once.</span></span>

7. <span data-ttu-id="85977-133">Vent et øyeblikk mens et kort genereres i meldingsboksen.</span><span class="sxs-lookup"><span data-stu-id="85977-133">Wait a moment while a card is generated in the message box.</span></span>

8. <span data-ttu-id="85977-134">Når kortet vises, kan du se nøye gjennom innholdet på kortet for eventuell sensitiv informasjon før du sender meldingen.</span><span class="sxs-lookup"><span data-stu-id="85977-134">When the card appears, review the contents of the card carefully for any sensitive information before sending the message.</span></span> <span data-ttu-id="85977-135">Dette trinnet er viktig fordi når du sender meldingen, kan alle i samtalen se kortet.</span><span class="sxs-lookup"><span data-stu-id="85977-135">This step is important because once you send the message, everyone in the conversation can see the card.</span></span>

9. <span data-ttu-id="85977-136">Hvis kortet ser bra ut, velger du **Send** for å sende det til samtalen.</span><span class="sxs-lookup"><span data-stu-id="85977-136">If the card looks good, select **Send** to submit it to the conversation.</span></span>

    > [!TIP]
    > <span data-ttu-id="85977-137">Når kortet vises, og før du velger **Send**, kan du slette den innlimte URL-adressen hvis du vil det.</span><span class="sxs-lookup"><span data-stu-id="85977-137">After the card appears, and before you select **Send**, you can delete the pasted URL if you like.</span></span>

10. <span data-ttu-id="85977-138">Hvis du vil vise flere detaljer eller gjøre endringer i posten, velger du **Detaljer**.</span><span class="sxs-lookup"><span data-stu-id="85977-138">To view more details or make changes to the record, select **Details**.</span></span>

    <span data-ttu-id="85977-139">Detaljsiden ligner på det du ser i [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="85977-139">The details page is similar to what you'd see in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="85977-140">Men den er noe trimmet for Teams.</span><span class="sxs-lookup"><span data-stu-id="85977-140">But it's slightly trimmed for Teams.</span></span> <span data-ttu-id="85977-141">Når du er ferdig med å vise og gjøre endringer, lukker du vinduet for å gå tilbake til Teams-samtalen.</span><span class="sxs-lookup"><span data-stu-id="85977-141">When you're finished viewing and making changes, close the window to return to the Teams conversation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="85977-142">Eventuelle endringer du foretar, gjenspeiles ikke i kortet før neste gang du limer inn koblingen i en samtale.</span><span class="sxs-lookup"><span data-stu-id="85977-142">Any changes you make won't be reflected in the card until the next time you paste its link in a conversation.</span></span>

## <a name="see-also"></a><span data-ttu-id="85977-143">Se også</span><span class="sxs-lookup"><span data-stu-id="85977-143">See Also</span></span>

[<span data-ttu-id="85977-144">Oversikt over Business Central og Microsoft Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="85977-144">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="85977-145">[Installere [!INCLUDE [prodshort](includes/prodshort.md)]-appen for Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="85977-145">[Install the [!INCLUDE [prodshort](includes/prodshort.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="85977-146">Utvikle for Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="85977-146">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[<span data-ttu-id="85977-147">Komme i gang</span><span class="sxs-lookup"><span data-stu-id="85977-147">Getting Started</span></span>](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
