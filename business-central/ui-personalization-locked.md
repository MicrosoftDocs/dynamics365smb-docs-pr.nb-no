---
title: Hvorfor kan jeg ikke tilpasse en side?
description: Forklarer hvorfor du kan ikke tilpasse en side og hva du kan gjøre for å låse den opp slik at du kan tilpasse den.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8fd90f7bf90209496f67d52ab32a93cfdbaf803f
ms.sourcegitcommit: 652e4b0e1a09bff265014d9f8eb3b038ab0db79e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/21/2021
ms.locfileid: "6087647"
---
# <a name="why-a-page-is-locked-from-personalization"></a><span data-ttu-id="44ade-103">Hvorfor en side er låst fra tilpasning</span><span class="sxs-lookup"><span data-stu-id="44ade-103">Why a Page is Locked from Personalization</span></span>

<span data-ttu-id="44ade-104">Det finnes to betingelser som hindrer deg i å tilpasse en side.</span><span class="sxs-lookup"><span data-stu-id="44ade-104">There are two conditions that prevent you from personalizing a page.</span></span> <span data-ttu-id="44ade-105">Siden er låst (som angitt av ikonet ![Tilpassingslås](media/personalization-lock-icon.png "Tilpass lås")), eller den er blokkert (angitt av ikonet ![Tilpassing blokkert](media/personalization-blocked-icon.png "Tilpassing blokkert")).</span><span class="sxs-lookup"><span data-stu-id="44ade-105">Either the page is locked (as indicated by the ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock")) icon or it is blocked (as indicated by the ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon).</span></span>

## <a name="locked-from-personalizing"></a><span data-ttu-id="44ade-106">Låst for tilpasning</span><span class="sxs-lookup"><span data-stu-id="44ade-106">Locked from Personalizing</span></span>

<span data-ttu-id="44ade-107">Hvis ikonet ![Tilpassingslås](media/personalization-lock-icon.png "Tilpass lås") vises på **Tilpasse**-banneret når du åpner en side, betyr dette at du ikke kan foreta flere tilpassingsendringer av siden.</span><span class="sxs-lookup"><span data-stu-id="44ade-107">If there is a ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon in the **Personalizing** banner when you open a page, this means that you are currently prevented from making any more personalization changes to the page.</span></span>

<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

<span data-ttu-id="44ade-108">Det kan være to årsaker til dette:</span><span class="sxs-lookup"><span data-stu-id="44ade-108">There can be two reasons for this:</span></span>

1. <span data-ttu-id="44ade-109">Du har brukt tilpasning på siden før, men det ble gjort ved hjelp av tidligere versjon av produktet.</span><span class="sxs-lookup"><span data-stu-id="44ade-109">You have personalized the page before, but it was done using an earlier version of the product.</span></span> <span data-ttu-id="44ade-110">Vi endret hvordan tilpasningen fungerer i bakgrunnen siden forrige gang du tilpasset siden.</span><span class="sxs-lookup"><span data-stu-id="44ade-110">We changed the way personalization works behind the scenes since the last time that you personalized the page.</span></span> <span data-ttu-id="44ade-111">Dessverre fungerer ikke den gamle og nye måten å gjøre ting på.</span><span class="sxs-lookup"><span data-stu-id="44ade-111">Unfortunately, the old way and new way of doing things do not work together.</span></span>

2. <span data-ttu-id="44ade-112">Hittil har du bare brukt [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] til å tilpasse siden.</span><span class="sxs-lookup"><span data-stu-id="44ade-112">Until now, you have only used the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] to personalize the page.</span></span>

### <a name="unlocking-the-page"></a><span data-ttu-id="44ade-113">Låse opp siden</span><span class="sxs-lookup"><span data-stu-id="44ade-113">Unlocking the Page</span></span>

<span data-ttu-id="44ade-114">Hvis du vil låse opp en side og fortsette med å tilpasse den, velger du ikonet ![Tilpassingslås](media/personalization-lock-icon.png "Tilpass lås") og deretter handlingen **Lås opp**.</span><span class="sxs-lookup"><span data-stu-id="44ade-114">If you want to unlock a page and continue personalizing it, choose the ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon, and then choose the **Unlock** action.</span></span>  

<span data-ttu-id="44ade-115">Før du låser opp siden må du være oppmerksom på følgende:</span><span class="sxs-lookup"><span data-stu-id="44ade-115">Before you unlock the page, be aware of the following:</span></span>

- <span data-ttu-id="44ade-116">Gjeldende tilpasning av siden slettes.</span><span class="sxs-lookup"><span data-stu-id="44ade-116">The current personalization of the page will be cleared.</span></span> <span data-ttu-id="44ade-117">Siden vil gå tilbake til det opprinnelige oppsettet, og du må begynne fra begynnelsen.</span><span class="sxs-lookup"><span data-stu-id="44ade-117">The page will go back to its original layout, and you will have to start from scratch.</span></span>

- <span data-ttu-id="44ade-118">I [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] vil siden forbli som den er, og vil ikke bli påvirket av de nye tilpasningsendringene i Business Central-klienten.</span><span class="sxs-lookup"><span data-stu-id="44ade-118">In the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], the page will remain as-is and will not be affected by the new personalization changes made in the Business Central client.</span></span> <span data-ttu-id="44ade-119">I fremtiden vil tilpasningen i [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] og Business Central-klienten være helt atskilte fra hverandre.</span><span class="sxs-lookup"><span data-stu-id="44ade-119">Going forward, the personalization in the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] and Business Central client will be completely separate from each other.</span></span>

## <a name="blocked-from-personalizing"></a><span data-ttu-id="44ade-120">Blokkert for tilpasning</span><span class="sxs-lookup"><span data-stu-id="44ade-120">Blocked from Personalizing</span></span>

<span data-ttu-id="44ade-121">Hvis ikonet ![Tilpassing blokkert](media/personalization-blocked-icon.png "Tilpassing blokkert") vises på **Tilpasse**-banneret, betyr det at du ikke kan gjøre eventuelle tilpassinger på siden.</span><span class="sxs-lookup"><span data-stu-id="44ade-121">If there is a ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon in the **Personalizing** banner, this means that you are blocked from doing any personalization to the page.</span></span>

<!-- Only text is translated, so removing this image for non-English UX reasons.  ![Personalize blocked](media/personalization-blocked.png "Personalize lock") -->

<span data-ttu-id="44ade-122">Dette er fordi rollesenteret eller rollen som er knyttet til brukerkontoen, endrer denne siden spesielt for din rolle.</span><span class="sxs-lookup"><span data-stu-id="44ade-122">The reason for this is that the Role Center or role that is currently associated with your user account modifies this page specifically for your role.</span></span> <span data-ttu-id="44ade-123">Kontakt systemansvarlig for å få hjelp.</span><span class="sxs-lookup"><span data-stu-id="44ade-123">Contact your administrator for assistance.</span></span> <span data-ttu-id="44ade-124">Du kan eventuelt prøve å bytte til et rollesenter som inkluderer rolleskreddersying for denne siden.</span><span class="sxs-lookup"><span data-stu-id="44ade-124">Alternatively, try switching to a Role Center that does include role-tailoring for this page.</span></span> <span data-ttu-id="44ade-125">Hvis du vil ha mer informasjon, kan du se [Endre grunnleggende innstillinger](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="44ade-125">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="44ade-126">Se også</span><span class="sxs-lookup"><span data-stu-id="44ade-126">See Also</span></span>
[<span data-ttu-id="44ade-127">Tilpasse arbeidsområdet</span><span class="sxs-lookup"><span data-stu-id="44ade-127">Personalize Your Workspace</span></span>](ui-personalization-user.md)  
[<span data-ttu-id="44ade-128">Tilpasse sider for profiler</span><span class="sxs-lookup"><span data-stu-id="44ade-128">Customize Pages for Profiles</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="44ade-129">Endre grunnleggende innstillinger</span><span class="sxs-lookup"><span data-stu-id="44ade-129">Change Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="44ade-130">Endre hvilke funksjoner som vises</span><span class="sxs-lookup"><span data-stu-id="44ade-130">Change Which Features are Displayed</span></span>](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
