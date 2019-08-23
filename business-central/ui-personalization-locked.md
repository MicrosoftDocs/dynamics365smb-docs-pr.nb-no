---
title: Hvorfor kan jeg ikke tilpasse en side? | Microsoft-dokumentasjon
description: Forklarer hvorfor du kan ikke tilpasse en side og hva du kan gjøre for å låse den opp slik at du kan tilpasse den.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 1a3edaca2e76388d82ea8991c3196410dd9c7288
ms.sourcegitcommit: a88d1e9c0ab647cb8d9d81d32c0bdc82843f4145
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/31/2019
ms.locfileid: "1796767"
---
# <a name="why-a-page-is-locked-from-personalization"></a><span data-ttu-id="d0fdd-103">Hvorfor en side er låst fra tilpasning</span><span class="sxs-lookup"><span data-stu-id="d0fdd-103">Why a Page is Locked from Personalization</span></span>

<span data-ttu-id="d0fdd-104">Det finnes to betingelser som hindrer deg i å tilpasse en side.</span><span class="sxs-lookup"><span data-stu-id="d0fdd-104">There are two conditions that prevent you from personalizing a page.</span></span> <span data-ttu-id="d0fdd-105">Enten hvis siden er låst (som angis av ![Tilpassingslås](media/personalization-lock-icon.png "Tilpassingslås")), eller den er sperret (som angis av ![Tilpassing sperret](media/personalization-blocked-icon.png "Tilpassing sperret")).</span><span class="sxs-lookup"><span data-stu-id="d0fdd-105">Either the page is locked (as indicated by ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock")) or it is blocked (as indicated by ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked")).</span></span>

## <a name="locked-from-personalizing"></a><span data-ttu-id="d0fdd-106">Låst for tilpasning</span><span class="sxs-lookup"><span data-stu-id="d0fdd-106">Locked from Personalizing</span></span>

<span data-ttu-id="d0fdd-107">Hvis det er et ![Tilpassingslås](media/personalization-lock-icon.png "Tilpassingslås")-ikon i **Tilpassing**-banneret når du åpner en side (som vist), betyr dette at du er hindret fra å foreta flere tilpasningsendringer av siden.</span><span class="sxs-lookup"><span data-stu-id="d0fdd-107">If there is a ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon in the **Personalizing** banner when you open a page (as shown), this means that you are currently prevented from making any more personalization changes to the page.</span></span>

<span data-ttu-id="d0fdd-108">![Tilpassingslås](media/personalization-locked.png "Tilpassingslås")</span><span class="sxs-lookup"><span data-stu-id="d0fdd-108">![Personalize Lock](media/personalization-locked.png "Personalize lock")</span></span>


<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

<span data-ttu-id="d0fdd-109">Det kan være to årsaker til dette:</span><span class="sxs-lookup"><span data-stu-id="d0fdd-109">There can be two reasons for this:</span></span>

1. <span data-ttu-id="d0fdd-110">Du har brukt tilpasning på siden før, men det ble gjort ved hjelp av tidligere versjon av produktet.</span><span class="sxs-lookup"><span data-stu-id="d0fdd-110">You have personalized the page before, but it was done using an earlier version of the product.</span></span> <span data-ttu-id="d0fdd-111">Vi endret hvordan tilpasningen fungerer i bakgrunnen siden forrige gang du tilpasset siden.</span><span class="sxs-lookup"><span data-stu-id="d0fdd-111">We changed the way personalization works behind the scenes since the last time that you personalized the page.</span></span> <span data-ttu-id="d0fdd-112">Dessverre fungerer ikke den gamle og nye måten å gjøre ting på.</span><span class="sxs-lookup"><span data-stu-id="d0fdd-112">Unfortunately, the old way and new way of doing things do not work together.</span></span>

2. <span data-ttu-id="d0fdd-113">Hittil har du bare brukt [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] til å tilpasse siden.</span><span class="sxs-lookup"><span data-stu-id="d0fdd-113">Until now, you have only used the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] to personalize the page.</span></span>

### <a name="unlocking-the-page"></a><span data-ttu-id="d0fdd-114">Låse opp siden</span><span class="sxs-lookup"><span data-stu-id="d0fdd-114">Unlocking the Page</span></span>

<span data-ttu-id="d0fdd-115">Hvis du vil frigi en side og fortsette med å tilpasse den, velger du ![Tilpassingslås](media/personalization-lock-icon.png "Tilpassingslås") og deretter **Lås opp**.</span><span class="sxs-lookup"><span data-stu-id="d0fdd-115">If you want to unlock a page and continue personalizing it, choose ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock"), and then **Unlock**.</span></span>  

<span data-ttu-id="d0fdd-116">Før du låser opp siden må du være oppmerksom på følgende:</span><span class="sxs-lookup"><span data-stu-id="d0fdd-116">Before you unlock the page, be aware of the following:</span></span>

- <span data-ttu-id="d0fdd-117">Gjeldende tilpasning av siden slettes.</span><span class="sxs-lookup"><span data-stu-id="d0fdd-117">The current personalization of the page will be cleared.</span></span> <span data-ttu-id="d0fdd-118">Siden vil gå tilbake til det opprinnelige oppsettet, og du må begynne fra begynnelsen.</span><span class="sxs-lookup"><span data-stu-id="d0fdd-118">The page will go back to its original layout, and you will have to start from scratch.</span></span>

- <span data-ttu-id="d0fdd-119">I [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] vil siden forbli som den er, og vil ikke bli påvirket av de nye tilpasningsendringene i Business Central-klienten.</span><span class="sxs-lookup"><span data-stu-id="d0fdd-119">In the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], the page will remain as-is and will not be affected by the new personalization changes made in the Business Central client.</span></span> <span data-ttu-id="d0fdd-120">I fremtiden vil tilpasningen i [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] og Business Central-klienten være helt atskilte fra hverandre.</span><span class="sxs-lookup"><span data-stu-id="d0fdd-120">Going forward, the personalization in the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] and Business Central client will be completely separate from each other.</span></span>

## <a name="blocked-from-personalizing"></a><span data-ttu-id="d0fdd-121">Blokkert for tilpasning</span><span class="sxs-lookup"><span data-stu-id="d0fdd-121">Blocked from Personalizing</span></span>

<span data-ttu-id="d0fdd-122">Hvis det er et ![Tilpassing sperret](media/personalization-blocked-icon.png "Tilpassing sperret")-ikon i tilpasningsbanneret, betyr det at du er sperret for å gjøre eventuelle tilpasninger på siden.</span><span class="sxs-lookup"><span data-stu-id="d0fdd-122">If there is a ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon in the Personalizing banner, this means that you are blocked from doing any personalization to the page.</span></span>

<span data-ttu-id="d0fdd-123">![Tilpassing sperret](media/personalization-blocked.png "Tilpassing sperret")</span><span class="sxs-lookup"><span data-stu-id="d0fdd-123">![Personalize blocked](media/personalization-blocked.png "Personalize lock")</span></span>

<span data-ttu-id="d0fdd-124">Dette er fordi rollesenteret eller rollen som er knyttet til brukerkontoen, endrer denne siden spesielt for din rolle.</span><span class="sxs-lookup"><span data-stu-id="d0fdd-124">The reason for this is that the Role Center or role that is currently associated with your user account modifies this page specifically for your role.</span></span> <span data-ttu-id="d0fdd-125">Kontakt systemansvarlig for å få hjelp eller, hvis det er hensiktsmessig, prøv å bytte til et rollesenter (fra [**Mine innstillinger**](https://businesscentral.dynamics.com?page=9176 "Gå direkte til siden med brukerinnstillinger i Business Central")) som inkluderer skreddersydde roller for denne siden.</span><span class="sxs-lookup"><span data-stu-id="d0fdd-125">Please contact your administrator for assistance or, if it makes sense, try switching to a Role Center (from  [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central")) that does include role-tailoring for this page.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0fdd-126">Se også</span><span class="sxs-lookup"><span data-stu-id="d0fdd-126">See Also</span></span>
[<span data-ttu-id="d0fdd-127">Tilpasse arbeidsområdet</span><span class="sxs-lookup"><span data-stu-id="d0fdd-127">Personalizing Your Workspace</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="d0fdd-128">Administrere tilpasning</span><span class="sxs-lookup"><span data-stu-id="d0fdd-128">Managing Personalization</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="d0fdd-129">Endre grunnleggende innstillinger</span><span class="sxs-lookup"><span data-stu-id="d0fdd-129">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="d0fdd-130">Endre hvilke funksjoner som vises</span><span class="sxs-lookup"><span data-stu-id="d0fdd-130">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
