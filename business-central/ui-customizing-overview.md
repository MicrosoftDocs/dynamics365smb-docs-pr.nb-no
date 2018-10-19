---
title: Tilpasse Business Central | Microsoft-dokumentasjon
description: Finn ut hvordan du legger til funksjoner og tilpasser Business Central.
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, add-in, extend, customize
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 63ba198a761b0c79c51ac94d36314310e330fc58
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="customizing-business-central"></a><span data-ttu-id="4e80e-103">Tilpasse Business Central</span><span class="sxs-lookup"><span data-stu-id="4e80e-103">Customizing Business Central</span></span>
<span data-ttu-id="4e80e-104">Det finnes ulike metoder for å tilpasse programmet slik at du og kollegene dine får tilgang til funksjonene, funksjonaliteten og dataen du trenger, på en måte som passer til dine daglige arbeidsoppgaver.</span><span class="sxs-lookup"><span data-stu-id="4e80e-104">There are different ways to customize the application to give you and your colleagues access to the features, functionality, and data that you need most, in a manner that bests suits your daily work.</span></span> <span data-ttu-id="4e80e-105">I denne tabellen beskrives hvem som ser endringene, avhengig av hva du gjør.</span><span class="sxs-lookup"><span data-stu-id="4e80e-105">Those who see the changes will depend on what you do, as described in this table.</span></span>

| <span data-ttu-id="4e80e-106">Hva du kan gjøre</span><span class="sxs-lookup"><span data-stu-id="4e80e-106">What you can do</span></span>    |  <span data-ttu-id="4e80e-107">Description</span><span class="sxs-lookup"><span data-stu-id="4e80e-107">Description</span></span>  |  <span data-ttu-id="4e80e-108">Hvem ser endringene</span><span class="sxs-lookup"><span data-stu-id="4e80e-108">Who sees the changes</span></span>  |  <span data-ttu-id="4e80e-109">Mer informasjon</span><span class="sxs-lookup"><span data-stu-id="4e80e-109">More information</span></span>  |
|-----|---------------|---------|-------|
|<span data-ttu-id="4e80e-110">Installere en utvidelse</span><span class="sxs-lookup"><span data-stu-id="4e80e-110">Install an extension</span></span>|<span data-ttu-id="4e80e-111">Utvidelser er som små programmer som føyer til funksjonalitet, endre virkemåten, gir deg tilgang til nye elektroniske tjenester og så videre.</span><span class="sxs-lookup"><span data-stu-id="4e80e-111">Extensions are like small applications that add functionality, change behavior, provide access to new online services, and more.</span></span> <span data-ttu-id="4e80e-112">Microsoft tilbyr for eksempel en utvidelse som kan gi integrering med PayPal Payments Standard.</span><span class="sxs-lookup"><span data-stu-id="4e80e-112">For example, Microsoft provides an extension that provides integration with PayPal Payments Standard.</span></span>|<span data-ttu-id="4e80e-113">Alle brukere i alle selskaper.</span><span class="sxs-lookup"><span data-stu-id="4e80e-113">All users in all companies.</span></span>|[<span data-ttu-id="4e80e-114">Tilpasse ved hjelp av utvidelser</span><span class="sxs-lookup"><span data-stu-id="4e80e-114">Customizing Using Extensions</span></span>](ui-extensions.md)|
|<span data-ttu-id="4e80e-115">Endre hvilke grensesnittelementer som vises.</span><span class="sxs-lookup"><span data-stu-id="4e80e-115">Change which UI elements are visible.</span></span>|<span data-ttu-id="4e80e-116">Konfigurasjonen **oOpplevelse** bestemmer hvor mye av funksjonaliteten er angitt i brukergrensesnittet.</span><span class="sxs-lookup"><span data-stu-id="4e80e-116">The **Experience** setting determines how much of the functionality is displayed in the user interface.</span></span> <span data-ttu-id="4e80e-117">Velg mellom Essential og Premium.</span><span class="sxs-lookup"><span data-stu-id="4e80e-117">Choose between Essential and Premium.</span></span>|<span data-ttu-id="4e80e-118">Alle brukere i en bestemt bedrift.</span><span class="sxs-lookup"><span data-stu-id="4e80e-118">All users in a specific company.</span></span>|[<span data-ttu-id="4e80e-119">Endre hvilke funksjoner som vises</span><span class="sxs-lookup"><span data-stu-id="4e80e-119">Changing Which Features are Displayed</span></span>](ui-experiences.md)|
|<span data-ttu-id="4e80e-120">Tilpasse arbeidsområdet</span><span class="sxs-lookup"><span data-stu-id="4e80e-120">Personalize your workspace</span></span>|<span data-ttu-id="4e80e-121">Endre oppsett av og innholdet på sidene.</span><span class="sxs-lookup"><span data-stu-id="4e80e-121">Change the layout and content of your pages.</span></span>|<span data-ttu-id="4e80e-122">Bare du.</span><span class="sxs-lookup"><span data-stu-id="4e80e-122">Only you.</span></span>|[<span data-ttu-id="4e80e-123">Tilpasse arbeidsområdet</span><span class="sxs-lookup"><span data-stu-id="4e80e-123">Personalizing Your Workspace</span></span>](ui-personalization-user.md)|

> [!NOTE]
> <span data-ttu-id="4e80e-124">Alle funksjonsbeskrivelser i brukerdokumentasjonen for [!INCLUDE[d365fin](includes/d365fin_md.md)] forutsetter **Premium**-opplevelsen, det vil si at beskrivelsene dekker hele omfanget av grensesnittelementer.</span><span class="sxs-lookup"><span data-stu-id="4e80e-124">All feature descriptions in user documentation for [!INCLUDE[d365fin](includes/d365fin_md.md)] assumes the **Premium** experience, meaning the descriptions cover the full scope of UI elements.</span></span> <span data-ttu-id="4e80e-125">Derfor kan brukere som har **Essential**-opplevelsen i enkelte emner lese om funksjoner og grensesnittelementer som ikke vises i brukergrensesnittet.</span><span class="sxs-lookup"><span data-stu-id="4e80e-125">Therefore, users with the **Essential** experience may in some topics read about functionality and UI elements that are not visible in their user interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="4e80e-126">Se også</span><span class="sxs-lookup"><span data-stu-id="4e80e-126">See Also</span></span>
<span data-ttu-id="4e80e-127">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4e80e-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

