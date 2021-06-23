---
title: Deling av Business Central-oppføringer i Microsoft Teams
description: Lær hvordan du bruker Business Central-appen for Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records
ms.date: 05/19/2021
ms.author: jswymer
ms.openlocfilehash: 8add662badbc0d791d6a37d0feb4e3a756519f00
ms.sourcegitcommit: 5a916b0aa0a2eef0c22b5722a0af041757e6d7c2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/19/2021
ms.locfileid: "6074590"
---
# <a name="sharing-business-central-records-in-microsoft-teams"></a><span data-ttu-id="539cd-103">Deling av Business Central-oppføringer i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="539cd-103">Sharing Business Central Records in Microsoft Teams</span></span>

[!INCLUDE [online_only](includes/online_only.md)]

<span data-ttu-id="539cd-104">[!INCLUDE [prod_short](includes/prod_short.md)] tilbyr en app som kobler Microsoft Teams til forretningsdataene dine i [!INCLUDE [prod_short](includes/prod_short.md)], slik at du raskt kan dele detaljer mellom gruppemedlemmer og svare raskere på forespørsler.</span><span class="sxs-lookup"><span data-stu-id="539cd-104">[!INCLUDE [prod_short](includes/prod_short.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)], so you can quickly share details across team members and respond faster to inquiries.</span></span> <span data-ttu-id="539cd-105">I denne artikkelen lærer du hvordan du bruker appen til å dele [!INCLUDE [prod_short](includes/prod_short.md)]-oppføringer, for eksempel en kunde, ordre eller faktura, med kolleger i en Teams-samtale.</span><span class="sxs-lookup"><span data-stu-id="539cd-105">In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] records, like a customer, sales order, or invoice, with coworkers in a Teams conversation.</span></span>

## <a name="overview"></a><span data-ttu-id="539cd-106">Oversikt</span><span class="sxs-lookup"><span data-stu-id="539cd-106">Overview</span></span>

<span data-ttu-id="539cd-107">[!INCLUDE [prod_short](includes/prod_short.md)]-appen lar deg:</span><span class="sxs-lookup"><span data-stu-id="539cd-107">The [!INCLUDE [prod_short](includes/prod_short.md)] app lets you:</span></span>

- <span data-ttu-id="539cd-108">Kopier en kobling til en Business Central-oppføring, og lim den inn i en Teams-samtale for å dele med kollegene dine.</span><span class="sxs-lookup"><span data-stu-id="539cd-108">Copy a link to any Business Central record and paste it into a Teams conversation to share with your coworkers.</span></span> <span data-ttu-id="539cd-109">Appen utvider deretter koblingen til et kompakt, interaktivt kort som viser informasjon om posten.</span><span class="sxs-lookup"><span data-stu-id="539cd-109">The app will then expand the link into a compact, interactive card that displays information about the record.</span></span>
- <span data-ttu-id="539cd-110">Når du er i samtalen, kan du og kollegaene dine vise flere detaljer om posten, redigere data og utføre handlinger uten å forlate Teams.</span><span class="sxs-lookup"><span data-stu-id="539cd-110">Once in the conversation, you and coworkers can view more details about the record, edit data, and take action&mdash;without leaving Teams.</span></span>

<span data-ttu-id="539cd-111">[![Teams-integrering med Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="539cd-111">[![Teams integration with Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="539cd-112">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="539cd-112">Prerequisites</span></span>

- <span data-ttu-id="539cd-113">Du har tilgang til Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="539cd-113">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="539cd-114">Du har installert [!INCLUDE [prod_short](includes/prod_short.md)]-appen i Teams.</span><span class="sxs-lookup"><span data-stu-id="539cd-114">You've installed the [!INCLUDE [prod_short](includes/prod_short.md)] app in Teams.</span></span> <span data-ttu-id="539cd-115">Hvis du vil ha mer informasjon, se [Installere [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="539cd-115">For more information, see [Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>

> [!NOTE]
> <span data-ttu-id="539cd-116">Alle deltakere i en Teams-samtale kan vise kort for Business Central-oppføringer som du sender til samtalen.</span><span class="sxs-lookup"><span data-stu-id="539cd-116">All participants in a Teams conversation will be able to view cards for Business Central records that you submit to the conversation.</span></span> <span data-ttu-id="539cd-117">Men hvis de vil vise flere detaljer om poster, ved hjelp av **Detaljer** eller **Eget vindu**-knappene på et kort, trenger de tilgang til [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="539cd-117">But to view more details about records, by using the **Details** or **Pop out** buttons on a card, they'll need access to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="539cd-118">Hvis du vil ha mer informasjon, kan du se [Administrere Microsoft Teams-integrering](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="539cd-118">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>

## <a name="include-a-business-central-card-in-a-teams-conversation"></a><span data-ttu-id="539cd-119">Ta med et Business Central-kort i en Teams-samtale</span><span class="sxs-lookup"><span data-stu-id="539cd-119">Include a Business Central card in a Teams conversation</span></span>

1. <span data-ttu-id="539cd-120">Logg på [!INCLUDE [prod_short](includes/prod_short.md)] ved å bruke leseren.</span><span class="sxs-lookup"><span data-stu-id="539cd-120">Sign in to [!INCLUDE [prod_short](includes/prod_short.md)] using your browser.</span></span>
2. <span data-ttu-id="539cd-121">Åpne posten du vil dele.</span><span class="sxs-lookup"><span data-stu-id="539cd-121">Open the record that you want to share.</span></span>

    <span data-ttu-id="539cd-122">Appen er utformet for å vise korttypesider fra [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="539cd-122">The app is designed to display card type pages from [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="539cd-123">Så åpne en side som viser én enkelt post, for eksempel en vare, kunde eller ordre.</span><span class="sxs-lookup"><span data-stu-id="539cd-123">So open a page that displays a single record, like an item, customer, or sales order.</span></span> <span data-ttu-id="539cd-124">Du kan ikke bruke den til rollesentre eller sider som viser flere poster i en liste.</span><span class="sxs-lookup"><span data-stu-id="539cd-124">You can't use it for role centers or pages that display several records in a list.</span></span>

3. <span data-ttu-id="539cd-125">Kopier hele URL-adressen fra adresselinjen i nettleseren.</span><span class="sxs-lookup"><span data-stu-id="539cd-125">Copy the entire URL from the browser's address bar.</span></span>

   ![Kopier URL-adressen for Business Central fra leseren](media/teams-url-v2.png)
4. <span data-ttu-id="539cd-127">Gå til Teams og start en samtale, som kan være en chat med en person, gruppe med personer eller en teamkanal.</span><span class="sxs-lookup"><span data-stu-id="539cd-127">Go to Teams and start a conversation, which can be chat with a person, group of persons, or a team channel.</span></span>

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. <span data-ttu-id="539cd-128">Lim inn URL-adressen i meldingsboksen der du skriver en melding.</span><span class="sxs-lookup"><span data-stu-id="539cd-128">Paste the URL in the message box where you compose a message.</span></span>

   ![Lim inn URL-adresse for Business Central i Teams](media/teams-paste-url-v2.png)
6. <span data-ttu-id="539cd-130">Første gang du limer inn en kobling i en samtale, blir du bedt om å logge på [!INCLUDE [prod_short](includes/prod_short.md)] og gi samtykke til at appen kan hente data.</span><span class="sxs-lookup"><span data-stu-id="539cd-130">The first time you paste a link into a conversation, you'll be asked to sign in to [!INCLUDE [prod_short](includes/prod_short.md)] and give consent for the app to retrieve data.</span></span> <span data-ttu-id="539cd-131">Bare følg instruksjonene på skjermen.</span><span class="sxs-lookup"><span data-stu-id="539cd-131">Just follow the on-screen instructions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="539cd-132">Du trenger bare å utføre dette trinnet én gang.</span><span class="sxs-lookup"><span data-stu-id="539cd-132">You'll only have to do this step once.</span></span>

7. <span data-ttu-id="539cd-133">Vent et øyeblikk mens et kort genereres i meldingsboksen.</span><span class="sxs-lookup"><span data-stu-id="539cd-133">Wait a moment while a card is generated in the message box.</span></span>

8. <span data-ttu-id="539cd-134">Når kortet vises, kan du se nøye gjennom innholdet på kortet for eventuell sensitiv informasjon før du sender meldingen.</span><span class="sxs-lookup"><span data-stu-id="539cd-134">When the card appears, review the contents of the card carefully for any sensitive information before sending the message.</span></span> <span data-ttu-id="539cd-135">Dette trinnet er viktig fordi når du sender meldingen, kan alle i samtalen se kortet.</span><span class="sxs-lookup"><span data-stu-id="539cd-135">This step is important because once you send the message, everyone in the conversation can see the card.</span></span>

9. <span data-ttu-id="539cd-136">Hvis kortet ser bra ut, velger du **Send** for å sende det til samtalen.</span><span class="sxs-lookup"><span data-stu-id="539cd-136">If the card looks good, select **Send** to submit it to the conversation.</span></span>

    > [!TIP]
    > <span data-ttu-id="539cd-137">Når kortet vises, og før du velger **Send**, kan du slette den innlimte URL-adressen hvis du vil det.</span><span class="sxs-lookup"><span data-stu-id="539cd-137">After the card appears, and before you select **Send**, you can delete the pasted URL if you like.</span></span>

10. <span data-ttu-id="539cd-138">Hvis du vil vise flere detaljer eller gjøre endringer i posten som vises på kortet, velger du **Detaljer**.</span><span class="sxs-lookup"><span data-stu-id="539cd-138">To view more details or make changes to the record shown in the card, select **Details**.</span></span> <span data-ttu-id="539cd-139">Hvis du vil ha mer informasjon, kan du se neste avsnitt.</span><span class="sxs-lookup"><span data-stu-id="539cd-139">For more information, see the next section.</span></span>

## <a name="view-card-details"></a><span data-ttu-id="539cd-140">Vis kortdetaljer</span><span class="sxs-lookup"><span data-stu-id="539cd-140">View card details</span></span>

<span data-ttu-id="539cd-141">Når et kort er sendt til en samtale, kan alle deltakerne med de [riktige tillatelsene](admin-teams-integration.md#permissions) velge **Detaljer** for å åpne et vindu som viser mer informasjon om posten, og eventuelt gjøre endringer i posten.</span><span class="sxs-lookup"><span data-stu-id="539cd-141">Once a card's been sent to a conversation, all participants with the [proper permissions](admin-teams-integration.md#permissions) can select **Details** to open a window that displays more information about the record&mdash;and possibly make changes to the record.</span></span> <span data-ttu-id="539cd-142">Det spiller ingen rolle om du er den som sender kortet, eller den som mottar kortet.</span><span class="sxs-lookup"><span data-stu-id="539cd-142">It doesn't matter if you're the one sending the card or the one receiving the card.</span></span> <span data-ttu-id="539cd-143">**Detaljer**-funksjonen er spesielt nyttig for mottakere fordi den raskt gir dem konsis, målrettet informasjon om posten, i motsetning til å måtte skanne hele posten.</span><span class="sxs-lookup"><span data-stu-id="539cd-143">The **Details** feature is especially useful to recipients, because it quickly provides them with concise, targeted information about the record, as opposed to having to scan the full record.</span></span>

<span data-ttu-id="539cd-144">Detaljvinduet ligner på det du ser i [!INCLUDE [prod_short](includes/prod_short.md)]-posten.</span><span class="sxs-lookup"><span data-stu-id="539cd-144">The details window is similar to what you'd see in [!INCLUDE [prod_short](includes/prod_short.md)] the record.</span></span> <span data-ttu-id="539cd-145">Men den er noe trimmet for Teams.</span><span class="sxs-lookup"><span data-stu-id="539cd-145">But it's slightly trimmed for Teams.</span></span> <span data-ttu-id="539cd-146">Når du er ferdig med å vise og gjøre endringer, lukker du vinduet for å gå tilbake til Teams-samtalen.</span><span class="sxs-lookup"><span data-stu-id="539cd-146">When you're finished viewing and making changes, close the window to return to the Teams conversation.</span></span>

<span data-ttu-id="539cd-147">Her er noen ting du må huske på når du arbeider med kortdetaljene:</span><span class="sxs-lookup"><span data-stu-id="539cd-147">Here are a couple things to keep in mind when working with the card details:</span></span>

- <span data-ttu-id="539cd-148">For å vise kortdetaljene må brukere ha tillatelse på siden og tilhørende data i [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="539cd-148">To open the card details, users must have permission on the page and its data in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span>
- <span data-ttu-id="539cd-149">Kort i Teams-chatter oppdateres ikke automatisk til endringer.</span><span class="sxs-lookup"><span data-stu-id="539cd-149">Cards in Teams chats aren't automatically updated to changes.</span></span> <span data-ttu-id="539cd-150">Eventuelle endringer du lagrer i en post i detaljvinduet, lagres i [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="539cd-150">Any changes you save to a record in the details window are saved in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="539cd-151">Kortet i Teams viser derfor ikke endringene i konverteringen før du limer inn koblingen på nytt.</span><span class="sxs-lookup"><span data-stu-id="539cd-151">But the card in Teams won't show the changes in the conversion, until you paste the link again.</span></span>

<span data-ttu-id="539cd-152">Hvis du vil vite mer om hvordan du arbeider med kort og kortdetaljer, kan du se [Vanlige spørsmål om Teams](teams-faq.md).</span><span class="sxs-lookup"><span data-stu-id="539cd-152">To learn more about working with cards and card details, see [Teams FAQ](teams-faq.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="539cd-153">Se også</span><span class="sxs-lookup"><span data-stu-id="539cd-153">See Also</span></span>

[<span data-ttu-id="539cd-154">Oversikt over Business Central og Microsoft Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="539cd-154">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="539cd-155">[Installer [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="539cd-155">[Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="539cd-156">Vanlige spørsmål om Teams</span><span class="sxs-lookup"><span data-stu-id="539cd-156">Teams FAQ</span></span>](teams-faq.md)  
[<span data-ttu-id="539cd-157">Feilsøke Teams</span><span class="sxs-lookup"><span data-stu-id="539cd-157">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  
[<span data-ttu-id="539cd-158">Utvikle for Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="539cd-158">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]