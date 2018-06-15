---
title: Administrere tilpasnings om administrator i Financials | Microsoft-dokumentasjon
description: "Lær hvordan du kan tilpasse brukergrensesnittet slik at det passer til din arbeidsmåte."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 07/26/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: 2d9b45bf21d325e60beadedfc94827d7f3fda075
ms.contentlocale: nb-no
ms.lasthandoff: 04/18/2018

---
# <a name="managing-personalization-as-an-administrator"></a><span data-ttu-id="da150-103">Administrere tilpasning som Administrator</span><span class="sxs-lookup"><span data-stu-id="da150-103">Managing Personalization as an Administrator</span></span>
<!--NAV in the Web client-->
<span data-ttu-id="da150-104">Brukere kan tilpasse arbeidsområdet etter egne behov.</span><span class="sxs-lookup"><span data-stu-id="da150-104">Users can personalize their workspace to suit their own preferences.</span></span> <span data-ttu-id="da150-105">Som administrator kan du kontrollere og håndtere tilpasning ved å deaktivere muligheten for brukerne til å tilpasse sider og fjerne en hvilken som helst sidetilpasning som brukere har utført.</span><span class="sxs-lookup"><span data-stu-id="da150-105">As an administrator, you can control and manage personalization by disabling the ability for users to personalize pages and clearing any page personalizations that users have made.</span></span>

## <a name="disable-personalization-for-a-profile"></a><span data-ttu-id="da150-106">Deaktivere tilpasning for en profil</span><span class="sxs-lookup"><span data-stu-id="da150-106">Disable personalization for a profile</span></span>
<span data-ttu-id="da150-107">Du kan hindre alle brukere som tilhører en bestemt profil, fra å tilpasse sine sider.</span><span class="sxs-lookup"><span data-stu-id="da150-107">You can prevent all users that belong to a specific profile from being able to personalize their pages.</span></span>
1.  <span data-ttu-id="da150-108">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Profiler**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="da150-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Profiles**, and then choose the related link.</span></span>
2.  <span data-ttu-id="da150-109">Velg profilen i listen som du vil endre.</span><span class="sxs-lookup"><span data-stu-id="da150-109">Select the profile in the list that you want to modify.</span></span>
3. <span data-ttu-id="da150-110">Merk av for **Deaktiver tilpasning**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="da150-110">Select the **Disable personalization** check box, and then choose the **OK** button.</span></span>

## <a name="clear-user-personalizations"></a><span data-ttu-id="da150-111">Fjerne brukertilpasninger</span><span class="sxs-lookup"><span data-stu-id="da150-111">Clear user personalizations</span></span>

<span data-ttu-id="da150-112">Hvis du fjerner sidetilpasninger, endres siden tilbake til det opprinnelige oppsettet før eventuelle tilpasninger ble utført.</span><span class="sxs-lookup"><span data-stu-id="da150-112">Clearing page personalization changes the page back to its original layout before any personalization was made.</span></span> <span data-ttu-id="da150-113">Du kan slette tilpasninger brukere har gjort med sider, på to måter: ved hjelp av siden **Slett brukertilpasning** og ved hjelp av siden **Brukertilpasningskort**.</span><span class="sxs-lookup"><span data-stu-id="da150-113">There are two ways to clear the personalizations that users have made to pages: using the **Delete User Personalization** page and using the **User Personalization Card** page.</span></span>

### <a name="clear-user-personalizations-by-using-the-delete-user-personalization-page"></a><span data-ttu-id="da150-114">Slette brukertilpasninger ved hjelp av siden Slett brukertilpasning</span><span class="sxs-lookup"><span data-stu-id="da150-114">Clear user personalizations by using the Delete User Personalization page</span></span>

<span data-ttu-id="da150-115">Siden **Slett brukertilpasning** lar deg slette tilpasninger for hver enkelt side og bruker.</span><span class="sxs-lookup"><span data-stu-id="da150-115">The **Delete User Personalization** page enables you to clear personalizations on a per-page basis for each user individually.</span></span>

1.  <span data-ttu-id="da150-116">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Slett brukertilpasning**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="da150-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="da150-117">Siden viser alle sidene som er tilpasset, og brukerne de tilhører.</span><span class="sxs-lookup"><span data-stu-id="da150-117">The page lists all the pages that have been personalized and the user it belongs to.</span></span>

    >[!NOTE]
    > <span data-ttu-id="da150-118">Hvis det er merket av for **Gammel tilpassing**-kolonnene, angir dett at tilpassingen ble utført i en eldre versjon av [!INCLUDE[d365fin](includes/d365fin_md.md)], som håndterte tilpassing annerledes enn nå.</span><span class="sxs-lookup"><span data-stu-id="da150-118">A check mark in the **Legacy Personalization** columns indicates that the personalization was done in an older version of [!INCLUDE[d365fin](includes/d365fin_md.md)], which handled personalization different than it does now.</span></span> <span data-ttu-id="da150-119">Brukere som prøver å tilpasse disse sidene, er låst fra å gjøre dette med mindre de ønsker å låse opp siden.</span><span class="sxs-lookup"><span data-stu-id="da150-119">Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.</span></span> <span data-ttu-id="da150-120">Hvis du vil ha mer informasjon, kan du se [Hvorfor en side er låst fra tilpassing](ui-personalization-locked.md).</span><span class="sxs-lookup"><span data-stu-id="da150-120">For more information, see [Why a page is locked from personalizing](ui-personalization-locked.md).</span></span>

2. <span data-ttu-id="da150-121">Velg posten du vil slette, og velg deretter handlingen **Slett**.</span><span class="sxs-lookup"><span data-stu-id="da150-121">Select the entry that you want to delete, and then choose the **Delete** action.</span></span>

    <span data-ttu-id="da150-122">Brukeren vil se endringene neste gang vedkommende logger på.</span><span class="sxs-lookup"><span data-stu-id="da150-122">The user will see the changes the next time they sign-in.</span></span>

### <a name="clear-user-personalizations-by-using-the-user-personalization-card-page"></a><span data-ttu-id="da150-123">Slette brukertilpasninger ved hjelp av siden Brukertilpasningskort</span><span class="sxs-lookup"><span data-stu-id="da150-123">Clear user personalizations by using the User Personalization Card page</span></span>

<span data-ttu-id="da150-124">Siden **Brukertilpasningskort** gir deg muligheten til å slette tilpasningen på alle sider for en bestemt bruker.</span><span class="sxs-lookup"><span data-stu-id="da150-124">The **User Personalization Card** page enables you to clear the personalization on all pages for specific user.</span></span> <span data-ttu-id="da150-125">Dette krever skrivetilgang til tabellen 2000000072 **profil**.</span><span class="sxs-lookup"><span data-stu-id="da150-125">This requires write permission to Table 2000000072 **Profile**.</span></span>

1.  <span data-ttu-id="da150-126">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Brukertilpasning**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="da150-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="da150-127">Siden **Brukertilpasning** viser alle brukerne som kan ha tilpassede sider.</span><span class="sxs-lookup"><span data-stu-id="da150-127">The **User Personalization** page lists all users who potentially have personalized pages.</span></span> <span data-ttu-id="da150-128">Hvis du ikke finner en bruker i listen, betyr det at de ikke har tilpassede sider.</span><span class="sxs-lookup"><span data-stu-id="da150-128">If you cannot find a user in the list, this means that they do not have any personalized pages.</span></span>

2. <span data-ttu-id="da150-129">Velg brukeren fra listen, og velg deretter handlingen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="da150-129">Select the user from the list, and then choose the **Edit** action.</span></span>

3.  <span data-ttu-id="da150-130">I kategorien **Handlinger** velger du **Fjern tilpassede sider**.</span><span class="sxs-lookup"><span data-stu-id="da150-130">On the **Actions** tab, choose **Clear Personalized Pages**.</span></span>

    <span data-ttu-id="da150-131">Brukeren vil se endringene neste gang vedkommende logger på.</span><span class="sxs-lookup"><span data-stu-id="da150-131">The user will see the changes the next time they sign-in.</span></span>

## <a name="see-also"></a><span data-ttu-id="da150-132">Se også</span><span class="sxs-lookup"><span data-stu-id="da150-132">See Also</span></span>
[<span data-ttu-id="da150-133">Tilpasse arbeidsområdet</span><span class="sxs-lookup"><span data-stu-id="da150-133">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
<span data-ttu-id="da150-134">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="da150-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="da150-135">Endre grunnleggende innstillinger</span><span class="sxs-lookup"><span data-stu-id="da150-135">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="da150-136">Endre hvilke funksjoner som vises</span><span class="sxs-lookup"><span data-stu-id="da150-136">Changing Which Features are Displayed</span></span>](ui-experiences.md)  

