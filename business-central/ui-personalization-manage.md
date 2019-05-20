---
title: Administrere tilpasnings om administrator i Business Central | Microsoft-dokumentasjon
description: Finn ut hvordan du kan tilpasse brukergrensesnittet slik at det passer til din arbeidsmåte.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 37cdf2d7dcc46b1286cbb7a5ad620547e364309e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250598"
---
# <a name="managing-personalization-as-an-administrator"></a><span data-ttu-id="790c2-103">Administrere tilpasning som Administrator</span><span class="sxs-lookup"><span data-stu-id="790c2-103">Managing Personalization as an Administrator</span></span>

<span data-ttu-id="790c2-104"> Brukere kan tilpasse arbeidsområdet etter egne behov.</span><span class="sxs-lookup"><span data-stu-id="790c2-104">Users can personalize their workspace to suit their own preferences.</span></span> <span data-ttu-id="790c2-105">Som en administrator kan du kontrollere og håndtere tilpasning av:</span><span class="sxs-lookup"><span data-stu-id="790c2-105">As an administrator, you control and manage personalization by:</span></span>

-   <span data-ttu-id="790c2-106">Aktivering eller deaktivering av funksjonen for tilpasning for hele programmet (bare lokal installasjon).</span><span class="sxs-lookup"><span data-stu-id="790c2-106">Enabling or disabling the personalization feature for the entire the application (on-premises installation only).</span></span>
-   <span data-ttu-id="790c2-107">Aktivering eller deaktivering av funksjonen for tilpasning for brukere av en bestemt profil.</span><span class="sxs-lookup"><span data-stu-id="790c2-107">Enabling or disabling the personalization feature for users of a specific profile.</span></span>
-   <span data-ttu-id="790c2-108">Fjerning av sidetilpasninger som brukere har opprettet.</span><span class="sxs-lookup"><span data-stu-id="790c2-108">Clearing any page personalizations that users have made.</span></span>

## <a name="EnablePersonalization"></a><span data-ttu-id="790c2-109">Aktivere eller deaktivere tilpasning (bare lokalt)</span><span class="sxs-lookup"><span data-stu-id="790c2-109">To enable or disable personalization (On-Premises Only)</span></span>

<span data-ttu-id="790c2-110">Som standard er tilpasning ikke aktivert i klienten.</span><span class="sxs-lookup"><span data-stu-id="790c2-110">By default, personalization is not enabled in the client.</span></span> <span data-ttu-id="790c2-111">Du aktiverer eller deaktiverer tilpasning ved å endre konfigurasjonsfilen (navsettings.json) for webserverforekomsten av Business Central som betjener klientene.</span><span class="sxs-lookup"><span data-stu-id="790c2-111">You enable or disable personalization by modifying the configuration file (navsettings.json) of the Business Central Web Server instance that serves the clients.</span></span>

1. <span data-ttu-id="790c2-112">Legg til følgende linje i filen navsettings.json for å aktivere tilpasning:</span><span class="sxs-lookup"><span data-stu-id="790c2-112">To enable personalization, add the following line in the navsettings.json file:</span></span>

    ```
    "PersonalizationEnabled": "true"
    ```

    <span data-ttu-id="790c2-113">Hvis du vil deaktivere tilpasning, fjerner du linjen eller endrer den til:</span><span class="sxs-lookup"><span data-stu-id="790c2-113">To disable personalization, remove this line or change it to:</span></span>

    ```
    "PersonalizationEnabled": "false"
    ```

    <span data-ttu-id="790c2-114">Du finner mer informasjon om hvordan du kan endre filen navsettings.json, i [Endre filen navsettings.json direkte](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings).</span><span class="sxs-lookup"><span data-stu-id="790c2-114">For more information about how to modify the navsettings.json file, see [Modify the navsettings.json file directly](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings).</span></span>

2. <span data-ttu-id="790c2-115">Generere og laste ned programsymbolene.</span><span class="sxs-lookup"><span data-stu-id="790c2-115">Generate and download the application symbols.</span></span>

    <span data-ttu-id="790c2-116">Dette trinnet er valgfritt og kreves ikke for å aktivere tilpasning.</span><span class="sxs-lookup"><span data-stu-id="790c2-116">This step is optional, and not required to enable personalization.</span></span> <span data-ttu-id="790c2-117">Det sikrer imidlertid at nye sider som er opprettet av utviklere, kan tilpasses.</span><span class="sxs-lookup"><span data-stu-id="790c2-117">However, it ensures that new pages that are created by developers can be personalized.</span></span>

    1. <span data-ttu-id="790c2-118">Først må du generere symbolene ved å kjøre finsql.exe med `generatesymbolreference`-kommandoen.</span><span class="sxs-lookup"><span data-stu-id="790c2-118">First, you generate the symbols by running finsql.exe with `generatesymbolreference` command.</span></span> <span data-ttu-id="790c2-119">Filen finsql.exe finnes i installasjonsmappen for [!INCLUDE[server](includes/server.md)] og Dynamics NAV Development Environment (CSIDE).</span><span class="sxs-lookup"><span data-stu-id="790c2-119">The finsql.exe file is located in the installation folder for the [!INCLUDE[server](includes/server.md)] and Dynamics NAV Development Environment (CSIDE).</span></span> <span data-ttu-id="790c2-120">For å generere symbolene åpne en ledetekst, endre katalogen der filen er lagret, og kjør følgende kommando:</span><span class="sxs-lookup"><span data-stu-id="790c2-120">To generate the symbols, open a command prompt, change to the directory where the file is store, and the run the following command:</span></span>

        ```
        finsql.exe Command=generatesymbolreference, Database="<Database Name>", ServerName=<SQL Server Name\<Server Instance>
        ```
    <span data-ttu-id="790c2-121">Eksempel:</span><span class="sxs-lookup"><span data-stu-id="790c2-121">For example:</span></span>

        ```
        finsql.exe Command=generatesymbolreference, Database="Demo Database BC", ServerName=MySQLServer\BCDEMO
        ```

    <span data-ttu-id="790c2-122">Hvis du vil ha mer informasjon, se [Kjøre C/SIDE og AL side ved side](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).</span><span class="sxs-lookup"><span data-stu-id="790c2-122">For more information, see [Running C/SIDE and AL Side-by-Side](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).</span></span>

    2. <span data-ttu-id="790c2-123">Konfigurere [!INCLUDE[nav_server_md](includes/nav_server_md.md)]-forekomst til **Aktivere lasting av programsymbolreferanser ved serveroppstart** (EnableSymbolLoadingAtServerStartup).</span><span class="sxs-lookup"><span data-stu-id="790c2-123">Configure [!INCLUDE[nav_server_md](includes/nav_server_md.md)] instance to **Enable loading application symbol references at server startup** (EnableSymbolLoadingAtServerStartup).</span></span> <span data-ttu-id="790c2-124">Hvis du vil ha mer informasjon, kan du se [Konfigurere Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).</span><span class="sxs-lookup"><span data-stu-id="790c2-124">For more information, see [Configuring Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).</span></span>

## <a name="to-disable-personalization-for-a-profile"></a><span data-ttu-id="790c2-125">Deaktivere tilpasning for en profil</span><span class="sxs-lookup"><span data-stu-id="790c2-125">To disable personalization for a profile</span></span>

<span data-ttu-id="790c2-126">Du kan hindre alle brukere som tilhører en bestemt profil, fra å tilpasse sine sider.</span><span class="sxs-lookup"><span data-stu-id="790c2-126">You can prevent all users that belong to a specific profile from being able to personalize their pages.</span></span>

1. <span data-ttu-id="790c2-127">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Profiler**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="790c2-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Profiles**, and then choose the related link.</span></span>
2. <span data-ttu-id="790c2-128">Velg profilen i listen som du vil endre.</span><span class="sxs-lookup"><span data-stu-id="790c2-128">Select the profile in the list that you want to modify.</span></span>
3. <span data-ttu-id="790c2-129">Merk av for **Deaktiver tilpasning**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="790c2-129">Select the **Disable personalization** check box, and then choose the **OK** button.</span></span>

## <a name="to-clear-user-personalizations"></a><span data-ttu-id="790c2-130">Fjerne brukertilpasninger</span><span class="sxs-lookup"><span data-stu-id="790c2-130">To clear user personalizations</span></span>

<span data-ttu-id="790c2-131">Hvis du fjerner sidetilpasninger, endres siden tilbake til det opprinnelige oppsettet før eventuelle tilpasninger ble utført.</span><span class="sxs-lookup"><span data-stu-id="790c2-131">Clearing page personalization changes the page back to its original layout before any personalization was made.</span></span> <span data-ttu-id="790c2-132">Du kan slette tilpasninger brukere har gjort med sider, på to måter: ved hjelp av siden **Slett brukertilpasning** og ved hjelp av siden **Brukertilpasningskort**.</span><span class="sxs-lookup"><span data-stu-id="790c2-132">There are two ways to clear the personalizations that users have made to pages: using the **Delete User Personalization** page and using the **User Personalization Card** page.</span></span>

### <a name="to-clear-user-personalizations-by-using-the-delete-user-personalization-page"></a><span data-ttu-id="790c2-133">Slette brukertilpasninger ved hjelp av siden Slett brukertilpasning</span><span class="sxs-lookup"><span data-stu-id="790c2-133">To clear user personalizations by using the Delete User Personalization page</span></span>

<span data-ttu-id="790c2-134">Siden **Slett brukertilpasning** lar deg slette tilpasninger for hver enkelt side og bruker.</span><span class="sxs-lookup"><span data-stu-id="790c2-134">The **Delete User Personalization** page enables you to clear personalizations on a per-page basis for each user individually.</span></span>

1. <span data-ttu-id="790c2-135">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Slett brukertilpasning**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="790c2-135">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="790c2-136">Siden viser alle sidene som er tilpasset, og brukerne de tilhører.</span><span class="sxs-lookup"><span data-stu-id="790c2-136">The page lists all the pages that have been personalized and the user it belongs to.</span></span>

    >[!NOTE]
    > <span data-ttu-id="790c2-137">Hvis det er merket av for **Gammel tilpassing**-kolonnene, angir dett at tilpassingen ble utført i en eldre versjon av [!INCLUDE[d365fin](includes/d365fin_md.md)], som håndterte tilpassing annerledes enn nå.</span><span class="sxs-lookup"><span data-stu-id="790c2-137">A check mark in the **Legacy Personalization** columns indicates that the personalization was done in an older version of [!INCLUDE[d365fin](includes/d365fin_md.md)], which handled personalization different than it does now.</span></span> <span data-ttu-id="790c2-138">Brukere som prøver å tilpasse disse sidene, er låst fra å gjøre dette med mindre de ønsker å låse opp siden.</span><span class="sxs-lookup"><span data-stu-id="790c2-138">Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.</span></span> <span data-ttu-id="790c2-139">Hvis du vil ha mer informasjon, kan du se [Hvorfor en side er låst fra tilpassing](ui-personalization-locked.md).</span><span class="sxs-lookup"><span data-stu-id="790c2-139">For more information, see [Why a page is locked from personalizing](ui-personalization-locked.md).</span></span>

2. <span data-ttu-id="790c2-140">Velg posten du vil slette, og velg deretter handlingen **Slett**.</span><span class="sxs-lookup"><span data-stu-id="790c2-140">Select the entry that you want to delete, and then choose the **Delete** action.</span></span>

    <span data-ttu-id="790c2-141">Brukeren vil se endringene neste gang vedkommende logger på.</span><span class="sxs-lookup"><span data-stu-id="790c2-141">The user will see the changes the next time they sign-in.</span></span>

### <a name="to-clear-user-personalizations-by-using-the-user-personalization-card-page"></a><span data-ttu-id="790c2-142">Slette brukertilpasninger ved hjelp av siden Brukertilpasningskort</span><span class="sxs-lookup"><span data-stu-id="790c2-142">To clear user personalizations by using the User Personalization Card page</span></span>

<span data-ttu-id="790c2-143">Siden **Brukertilpasningskort** gir deg muligheten til å slette tilpasningen på alle sider for en bestemt bruker.</span><span class="sxs-lookup"><span data-stu-id="790c2-143">The **User Personalization Card** page enables you to clear the personalization on all pages for specific user.</span></span> <span data-ttu-id="790c2-144">Dette krever skrivetilgang til tabellen 2000000072 **profil**.</span><span class="sxs-lookup"><span data-stu-id="790c2-144">This requires write permission to Table 2000000072 **Profile**.</span></span>

1. <span data-ttu-id="790c2-145">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukertilpasning**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="790c2-145">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="790c2-146">Siden **Brukertilpasning** viser alle brukerne som kan ha tilpassede sider.</span><span class="sxs-lookup"><span data-stu-id="790c2-146">The **User Personalization** page lists all users who potentially have personalized pages.</span></span> <span data-ttu-id="790c2-147">Hvis du ikke finner en bruker i listen, betyr det at de ikke har tilpassede sider.</span><span class="sxs-lookup"><span data-stu-id="790c2-147">If you cannot find a user in the list, this means that they do not have any personalized pages.</span></span>

2. <span data-ttu-id="790c2-148">Velg brukeren fra listen, og velg deretter handlingen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="790c2-148">Select the user from the list, and then choose the **Edit** action.</span></span>

3. <span data-ttu-id="790c2-149">I kategorien **Handlinger** velger du **Fjern tilpassede sider**.</span><span class="sxs-lookup"><span data-stu-id="790c2-149">On the **Actions** tab, choose **Clear Personalized Pages**.</span></span>

    <span data-ttu-id="790c2-150">Brukeren vil se endringene neste gang vedkommende logger på.</span><span class="sxs-lookup"><span data-stu-id="790c2-150">The user will see the changes the next time they sign-in.</span></span>

## <a name="see-also"></a><span data-ttu-id="790c2-151">Se også</span><span class="sxs-lookup"><span data-stu-id="790c2-151">See Also</span></span>
[<span data-ttu-id="790c2-152">Tilpasse arbeidsområdet</span><span class="sxs-lookup"><span data-stu-id="790c2-152">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
<span data-ttu-id="790c2-153">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="790c2-153">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="790c2-154">Endre grunnleggende innstillinger</span><span class="sxs-lookup"><span data-stu-id="790c2-154">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="790c2-155">Endre hvilke funksjoner som vises</span><span class="sxs-lookup"><span data-stu-id="790c2-155">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
