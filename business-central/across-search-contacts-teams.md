---
title: Søke etter kontakter fra Microsoft Teams
description: Finn ut hvordan du slår opp kunder, leverandører og andre kontakter for Business Central fra Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, contacts, search, messaging extensions
ms.date: 04/12/2021
ms.author: jswymer
ms.openlocfilehash: 6d094e365ad0c7da73467e5a3160d926902c45d9
ms.sourcegitcommit: c11ad91a389ed72532f5513654fdc7909b20aed9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935164"
---
# <a name="searching-for-customers-vendors-and-other-contacts-from-microsoft-teams"></a><span data-ttu-id="84547-103">Søke etter kunder, leverandører og andre kontakter fra Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="84547-103">Searching for Customers, Vendors, and Other Contacts from Microsoft Teams</span></span>

<span data-ttu-id="84547-104">[!INCLUDE [online_only](includes/online_only.md)].</span><span class="sxs-lookup"><span data-stu-id="84547-104">[!INCLUDE [online_only](includes/online_only.md)].</span></span> <span data-ttu-id="84547-105">Introdusert i lanseringsbølge 1 for 2021.</span><span class="sxs-lookup"><span data-stu-id="84547-105">Introduced in 2021 release wave 1.</span></span>

<span data-ttu-id="84547-106">[!INCLUDE [prod_short](includes/prod_short.md)] har et omfattende administrasjonssystem for forretningskontakter som er nødvendig for brukere i salg, operasjoner eller andre avdelingsroller.</span><span class="sxs-lookup"><span data-stu-id="84547-106">[!INCLUDE [prod_short](includes/prod_short.md)] has a comprehensive business contact management system that is essential for users in sales, operations, or other departmental roles.</span></span> <span data-ttu-id="84547-107">Hvis du er en bruker i en av disse rollene, må du ofte slå opp, møte eller starte en samtale med leverandører, kunder og andre kontakter.</span><span class="sxs-lookup"><span data-stu-id="84547-107">If you're a user in one of these roles, you'll often need to look up, meet, or start a conversation with your vendors, customers, and other contacts.</span></span> <span data-ttu-id="84547-108">Med [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Teams kan du utføre disse oppgavene direkte fra grupper, uten å måtte bytte til [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="84547-108">With the [!INCLUDE [prod_short](includes/prod_short.md)] app for Teams, you can do these tasks directly from Teams, without having to switch to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="84547-109">I Teams kan du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="84547-109">From within Teams, you can:</span></span>

- <span data-ttu-id="84547-110">Slå opp [!INCLUDE [prod_short](includes/prod_short.md)]-kontakter fra kommandoboksen i Teams eller fra meldingsområdet.</span><span class="sxs-lookup"><span data-stu-id="84547-110">Look up [!INCLUDE [prod_short](includes/prod_short.md)] contacts from the Teams command box or from the message compose area.</span></span> <span data-ttu-id="84547-111">Kontakter kan omfatte kundeemner, leverandører, kunder eller andre forretningsforhold.</span><span class="sxs-lookup"><span data-stu-id="84547-111">Contacts can include prospects, vendors, customers, or other business relationships.</span></span>
- <span data-ttu-id="84547-112">Dele en kontakt som et kort i en Teams-samtale.</span><span class="sxs-lookup"><span data-stu-id="84547-112">Share a contact as a card in a Teams conversation.</span></span>
- <span data-ttu-id="84547-113">Vise detaljer om kontakten, samhandlingsloggen og annen innsikt som utestående betalinger eller åpne dokumenter.</span><span class="sxs-lookup"><span data-stu-id="84547-113">View details about the contact, interaction history, and other insights like outstanding payments or open documents.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="84547-114">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="84547-114">Prerequisites</span></span>

- <span data-ttu-id="84547-115">Du har tilgang til Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="84547-115">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="84547-116">Du har installert [!INCLUDE [prod_short](includes/prod_short.md)]-appen i Teams.</span><span class="sxs-lookup"><span data-stu-id="84547-116">You've installed the [!INCLUDE [prod_short](includes/prod_short.md)] app in Teams.</span></span> <span data-ttu-id="84547-117">Hvis du vil ha mer informasjon, se [Installere [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="84547-117">For more information, see [Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>
- <span data-ttu-id="84547-118">Du har en [!INCLUDE [prod_short](includes/prod_short.md)]-konto med tilgang til kontakter i minst ett selskap.</span><span class="sxs-lookup"><span data-stu-id="84547-118">You've got a [!INCLUDE [prod_short](includes/prod_short.md)] account with access to contacts in at least one company.</span></span>

> [!NOTE]
> <span data-ttu-id="84547-119">Det kan hende at du blir bedt om å logge på eller sette opp appen første gang når du søker fra kommandoboksen eller meldingsboksen.</span><span class="sxs-lookup"><span data-stu-id="84547-119">Whether you searching from the command box or message compose box, you may be asked to sign in or set up the app the first time.</span></span> <span data-ttu-id="84547-120">Dette trinnet er nødvendig for å søke etter kontakter i det rette Business Central-selskapet.</span><span class="sxs-lookup"><span data-stu-id="84547-120">This step is necessary to search for contacts in the right Business Central company.</span></span> <span data-ttu-id="84547-121">Hvis du vil ha informasjon om hvordan du definerer appen for å velge selskap, kan du se [Endre selskap og andre innstillinger i Teams](across-teams-settings.md).</span><span class="sxs-lookup"><span data-stu-id="84547-121">For information about setting up the app to choose your company, see [Changing Company and Other Settings in Teams](across-teams-settings.md).</span></span>

## <a name="look-up-contacts-from-the-command-box"></a><span data-ttu-id="84547-122">Slå opp kontakter fra kommandoboksen</span><span class="sxs-lookup"><span data-stu-id="84547-122">Look up contacts from the command box</span></span>

<span data-ttu-id="84547-123">Kommandoboksen vises øverst i alle skjermbilder i Teams.</span><span class="sxs-lookup"><span data-stu-id="84547-123">The command box is at the top of every screen in Teams.</span></span> <span data-ttu-id="84547-124">Det gjør det mulig å søke, utføre raske handlinger eller starte apper, for eksempel [!INCLUDE [prod_short](includes/prod_short.md)]-appen.</span><span class="sxs-lookup"><span data-stu-id="84547-124">It lets you search, take quick actions, or launch apps, like the [!INCLUDE [prod_short](includes/prod_short.md)] app.</span></span> <span data-ttu-id="84547-125">Søking fra kommandoboksen er nyttig for raskt å finne frem til kontakter og tilhørende data for eget bruk.</span><span class="sxs-lookup"><span data-stu-id="84547-125">Searching from the command box is great for quickly looking up contacts and their related data for your own use.</span></span> <span data-ttu-id="84547-126">La oss for eksempel anta at du vil slå opp en e-postadresse for en leverandør for å opprette et kalendermøte.</span><span class="sxs-lookup"><span data-stu-id="84547-126">For example, suppose you want to look up an email address of a vendor to set up a calendar meeting.</span></span> <span data-ttu-id="84547-127">Eller kanskje du vil søke etter samhandlingslogg mens du møter med en kunde.</span><span class="sxs-lookup"><span data-stu-id="84547-127">Or maybe you want to look up interaction history during a meeting with a customer.</span></span>

1. <span data-ttu-id="84547-128">Skriv inn **@Business Central** i kommandoboksen, og velg deretter Business Central-appen fra resultatene.</span><span class="sxs-lookup"><span data-stu-id="84547-128">In the command box, type **@Business Central**, then select the Business Central app from the results.</span></span>

    ![Åpne Business Central-appen hvis du vil søke etter kontakter fra kommandoboks](media/teams-contacts-command-1.png)

2. <span data-ttu-id="84547-130">I **Business Central**-boksen begynner du å skrive søketekst, som navn, adresse eller telefonnummer.</span><span class="sxs-lookup"><span data-stu-id="84547-130">In the **Business Central** box, start typing search text, like a name, address, or phone number.</span></span>

    <span data-ttu-id="84547-131">Etter hvert som du skriver inn, vises samsvarsresultater.</span><span class="sxs-lookup"><span data-stu-id="84547-131">As you type, matching results will appear.</span></span>

    ![Søk etter Business Central-kontakter fra kommandoboksen i Teams](media/teams-contacts-command-2.png)
3. <span data-ttu-id="84547-133">Velg en kontakt fra resultatene.</span><span class="sxs-lookup"><span data-stu-id="84547-133">Select a contact from the results.</span></span>

    <span data-ttu-id="84547-134">Kontaktkortet vises under kommandoboksen.</span><span class="sxs-lookup"><span data-stu-id="84547-134">The contact card appears beneath the command box.</span></span>

4. <span data-ttu-id="84547-135">Hvis du vil legge til kontaktkortet i en samtale, går du til øvre høyre hjørne på kortet og velger **... (Flere alternativer)** > **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="84547-135">If you want to add the contact card into a conversation, go to the upper right corner of the card, select **... (More options)** > **Copy**.</span></span> <span data-ttu-id="84547-136">Deretter limer du inn kopien i meldingsboksen i en samtale.</span><span class="sxs-lookup"><span data-stu-id="84547-136">Then, paste the copy in the message compose box of a conversation.</span></span>  

<span data-ttu-id="84547-137">Hvis du vil ha mer generell informasjon om kommandoboksen i Teams, kan du se [Teams – bruke kommandoboksen](https://support.microsoft.com/en-us/office/use-the-command-box-13c4e429-7324-4886-b377-5dbed539193b).</span><span class="sxs-lookup"><span data-stu-id="84547-137">For more general information about the command box in Teams, see [Teams - Use the command box](https://support.microsoft.com/en-us/office/use-the-command-box-13c4e429-7324-4886-b377-5dbed539193b).</span></span>

## <a name="look-up-contacts-from-the-message-compose-box"></a><span data-ttu-id="84547-138">Slå opp kontakter fra meldingsboksen</span><span class="sxs-lookup"><span data-stu-id="84547-138">Look up contacts from the message compose box</span></span>

<span data-ttu-id="84547-139">Fordelen med å bruke meldingsboksen er at du kan legge til et kontaktkort direkte i en samtale, slik at andre kan se det.</span><span class="sxs-lookup"><span data-stu-id="84547-139">The advantage of using the message compose box is that you can add a contact card directly to a conversation, for others to see.</span></span>

1. <span data-ttu-id="84547-140">Under til meldingsboksen velger du **Business Central**-ikonet for å starte appen.</span><span class="sxs-lookup"><span data-stu-id="84547-140">Beneath to message compose box, select the **Business Central** icon to launch the app.</span></span>

    <span data-ttu-id="84547-141">Hvis **Business Central**-ikonet ikke vises, velger du **... (Meldingsutvidelser)**.</span><span class="sxs-lookup"><span data-stu-id="84547-141">If you don't see the **Business Central** icon, select **... (Messaging extensions)**.</span></span>

    ![Åpne Business Central-appen hvis du vil søke etter kontakter fra meldingsboks](media/teams-contacts-message-box.png)

2. <span data-ttu-id="84547-143">I **Business Central**-boksen begynner du å skrive søketekst, som navn, adresse eller telefonnummer.</span><span class="sxs-lookup"><span data-stu-id="84547-143">In the **Business Central** box, start typing search text, like a name, address, or phone number.</span></span>

    <span data-ttu-id="84547-144">Etter hvert som du skriver inn, vises samsvarsresultater.</span><span class="sxs-lookup"><span data-stu-id="84547-144">As you type, matching results will appear.</span></span>

    ![Søke etter Business Central-kontakter fra meldingsboks](media/teams-contacts-5.png)
3. <span data-ttu-id="84547-146">Velg en kontakt fra resultatene.</span><span class="sxs-lookup"><span data-stu-id="84547-146">Select a contact from the results.</span></span>

    <span data-ttu-id="84547-147">Kontaktkortet vises i meldingsboksen.</span><span class="sxs-lookup"><span data-stu-id="84547-147">The contact card appears in the message compose box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="84547-148">Kontaktkortet blir ikke sendt til samtalen med en gang slik at andre kan se det.</span><span class="sxs-lookup"><span data-stu-id="84547-148">The contact card isn't sent to the conversation right away for others to see.</span></span> <span data-ttu-id="84547-149">Du har muligheten til å gå gjennom innholdet på kortet, og legge til tekst før eller etter det etter behov.</span><span class="sxs-lookup"><span data-stu-id="84547-149">You have the opportunity to review the contents of the card, and add text before or after it as you like.</span></span> <span data-ttu-id="84547-150">Send deretter meldingen til chatten når du er klar.</span><span class="sxs-lookup"><span data-stu-id="84547-150">Then, send your message to the chat when ready.</span></span>

### <a name="heres-another-way"></a><span data-ttu-id="84547-151">Her er en annen måte</span><span class="sxs-lookup"><span data-stu-id="84547-151">Here's another way</span></span>

1. <span data-ttu-id="84547-152">I stedet for å bruke **Business Central**-ikonet, skriver du inn **@Business Central** direkte i meldingsboksen.</span><span class="sxs-lookup"><span data-stu-id="84547-152">Instead of using the **Business Central** icon, type **@Business Central** directly in the message compose box.</span></span>
2. <span data-ttu-id="84547-153">Skriv inn søkevilkårene i boksen.</span><span class="sxs-lookup"><span data-stu-id="84547-153">Enter your search terms in the box.</span></span>
3. <span data-ttu-id="84547-154">Bruk pil opp og pil ned på tastaturet til å velge en kontakt, og trykk deretter ENTER for å velge kontakten.</span><span class="sxs-lookup"><span data-stu-id="84547-154">Use the up and down arrow keys on the keyboard to choose a contact, then press Enter to select it.</span></span>

## <a name="viewing-contact-card-details"></a><span data-ttu-id="84547-155">Vise kontaktkortdetaljer</span><span class="sxs-lookup"><span data-stu-id="84547-155">Viewing contact card details</span></span>

<span data-ttu-id="84547-156">Kontaktkortet i Teams gir deg en rask oversikt over kunden, leverandøren eller kontakten.</span><span class="sxs-lookup"><span data-stu-id="84547-156">The contact card in Teams gives you a quick overview of the customer, vendor, or contact.</span></span> <span data-ttu-id="84547-157">Kortet er interaktivt&mdash;noe som betyr at du kan vise mer informasjon eller endre en kontakt ved hjelp av knappen **Detaljer** eller **Eget vindu**.</span><span class="sxs-lookup"><span data-stu-id="84547-157">The card is interactive&mdash;meaning you can view more information or even modify a contact by using the **Details** or **Pop-out** buttons.</span></span>

<span data-ttu-id="84547-158">Knappen **Detaljer** åpner et vindu i Teams som viser mer informasjon om kontakten, men ikke like mye som i [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="84547-158">The **Details** button opens a window within Teams that displays more information about the contact, but not as much as you'd see in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="84547-159">Hvis du vil vise all informasjon om en kontakt i [!INCLUDE [prod_short](includes/prod_short.md)], velger du **Eget vindu**.</span><span class="sxs-lookup"><span data-stu-id="84547-159">To see all the information about a contact in [!INCLUDE [prod_short](includes/prod_short.md)], select **Pop-out**.</span></span>

<span data-ttu-id="84547-160">Kontaktkortet fungerer på samme måte som kort for poster, for eksempel varer, kunder eller ordrer.</span><span class="sxs-lookup"><span data-stu-id="84547-160">The contact card works just like cards for records, like items, customers, or sales orders.</span></span> <span data-ttu-id="84547-161">Hvis du vil ha mer informasjon om kort, kan du se [Vise kortdetaljer](across-working-with-teams.md#view-card-details).</span><span class="sxs-lookup"><span data-stu-id="84547-161">For more information about cards, see [View card details](across-working-with-teams.md#view-card-details).</span></span>

> [!NOTE]
> <span data-ttu-id="84547-162">Alle deltakere i en Teams-samtale kan vise kort for Business Central-kontakten du sender til en samtale.</span><span class="sxs-lookup"><span data-stu-id="84547-162">All participants in a Teams conversation will be able to view cards for Business Central contact that you submit to a conversation.</span></span> <span data-ttu-id="84547-163">Men hvis de vil vise flere detaljer om poster, ved hjelp av **Detaljer** eller **Eget vindu**-knappene på et kort, trenger de tilgang til [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="84547-163">But to view more details about records, by using the **Details** or **Pop out** buttons on a card, they'll need access to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="84547-164">Hvis du vil ha mer informasjon, kan du se [Administrere Microsoft Teams-integrering](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="84547-164">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>

## <a name="see-also"></a><span data-ttu-id="84547-165">Se også</span><span class="sxs-lookup"><span data-stu-id="84547-165">See Also</span></span>

[<span data-ttu-id="84547-166">Oversikt over Business Central og Microsoft Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="84547-166">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="84547-167">[Installer [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="84547-167">[Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="84547-168">Vanlige spørsmål om Teams</span><span class="sxs-lookup"><span data-stu-id="84547-168">Teams FAQ</span></span>](teams-faq.md)  
[<span data-ttu-id="84547-169">Feilsøke Teams</span><span class="sxs-lookup"><span data-stu-id="84547-169">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  
[<span data-ttu-id="84547-170">Utvikle for Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="84547-170">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]