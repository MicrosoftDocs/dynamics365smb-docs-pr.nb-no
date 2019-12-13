---
title: Opprette et sandkassemiljø | Microsoft-dokumentasjon
description: Opprett et miljø for utforsking, læring, demoer, utvikling og testing.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 12/06/2019
ms.author: solsen
ms.openlocfilehash: 0f8f0f85df89c1d71fc3e114ebd902f2aa85f802
ms.sourcegitcommit: b6e506a45a1cd632294bafa1c959746cc3a144f6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896112"
---
# <a name="creating-a-sandbox-environment-in-include-prodshortincludesprodshortmd"></a><span data-ttu-id="20cb8-103">Opprette et sandkassemiljø i [!INCLUDE [prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="20cb8-103">Creating a Sandbox Environment in [!INCLUDE [prodshort](includes/prodshort.md)]</span></span>

<span data-ttu-id="20cb8-104">Med [!INCLUDE [prodshort](includes/prodshort.md)] kan du enkelt opprette et sikkert miljø der du kan teste, lære opp eller feilsøke uten å forstyrre firmaets arbeidsprosesser eller forretningsdata.</span><span class="sxs-lookup"><span data-stu-id="20cb8-104">With [!INCLUDE [prodshort](includes/prodshort.md)], you can easily create a safe environment where you can test, train, or troubleshoot without disturbing your company's work processes or business data.</span></span> <span data-ttu-id="20cb8-105">Et slikt ikke-produksjonsmiljø kalles en *sandkasse*.</span><span class="sxs-lookup"><span data-stu-id="20cb8-105">Such a non-production environment is called a *sandbox*.</span></span> <span data-ttu-id="20cb8-106">Isolert fra produksjon er et sandkassemiljø stedet der du trygt kan utforske, lære, demonstrere, utvikle og teste tjenesten uten risikoen ved å påvirke data og innstillinger i produksjonsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="20cb8-106">Isolated from production, a sandbox environment is the place to safely explore, learn, demo, develop, and test the service without the risk of affecting the data and settings of your production environment.</span></span>  

<span data-ttu-id="20cb8-107">Systemansvarlig kan opprette sandkassemiljøer i [administrasjonssenteret](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), men hvis du raskt vil teste noe, kan du opprette et sandkassemiljø fra innsiden [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="20cb8-107">Your administrator can create sandbox environments in the [administration center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), but if you want to quickly test something, you can create a sandbox environment from inside [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>  

> [!NOTE]
> <span data-ttu-id="20cb8-108">Teknisk sett er sandkassemiljøer svært forskjellige fra produksjonsmiljøer, selv om systemansvarlig oppretter en sandkasse som inkluderer produksjonsdata.</span><span class="sxs-lookup"><span data-stu-id="20cb8-108">Technically, sandbox environments are very different from production environments, even if your administrator creates a sandbox that includes production data.</span></span> <span data-ttu-id="20cb8-109">Du kan ikke bruke en sandkasse for ytelsestester, og du kan for eksempel ikke be om databaseeksport.</span><span class="sxs-lookup"><span data-stu-id="20cb8-109">You cannot use a sandbox for benchmarking, and you cannot request a database export, for example.</span></span> <span data-ttu-id="20cb8-110">Hvis du vil opprette en sandkasse for ytelsestest, kan systemansvarlig opprette et eget produksjonsmiljø i administrasjonssenteret.</span><span class="sxs-lookup"><span data-stu-id="20cb8-110">If you want to create a sandbox for benchmarking, your administrator can create a dedicated production environment in the administration center.</span></span> <span data-ttu-id="20cb8-111">Hvis du vil ha mer informasjon, kan du se [Typer miljøer](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).</span><span class="sxs-lookup"><span data-stu-id="20cb8-111">For more information, see [Types of environments](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).</span></span>

## <a name="to-create-a-sandbox-environment-in-your-include-prodshortincludesprodshortmd"></a><span data-ttu-id="20cb8-112">Slik oppretter du et sandkassemiljø i [!INCLUDE [prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="20cb8-112">To create a sandbox environment in your [!INCLUDE [prodshort](includes/prodshort.md)]</span></span>

1. <span data-ttu-id="20cb8-113">Logg deg på din produksjonsforekomst av [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="20cb8-113">Sign in to your production instance of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

2. <span data-ttu-id="20cb8-114">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Sandkassemiljø**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="20cb8-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sandbox Environment**, and then choose the related link.</span></span>
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. <span data-ttu-id="20cb8-115">Velg **Opprett**-knappen.</span><span class="sxs-lookup"><span data-stu-id="20cb8-115">Choose the **Create** button.</span></span>  

    <span data-ttu-id="20cb8-116">Det åpnes en annen fane med [!INCLUDE[d365fin](includes/d365fin_md.md)], der du kan fullføre oppsettet av sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="20cb8-116">Another tab with [!INCLUDE[d365fin](includes/d365fin_md.md)] opens where you can finish the setup of your sandbox environment.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="20cb8-117">Hvis du har aktivert popup-blokkering i webleseren, endrer du den til å tillate URL-adresser fra adressen \*.businesscentral.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="20cb8-117">If you have pop-up blocker enabled in your browser, change it to allow URLs from the \*.businesscentral.dynamics.com address.</span></span>

<span data-ttu-id="20cb8-118">Når sandkassemiljøet er klart, vil du bli videresendt til velkomstveiviseren i sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="20cb8-118">When the sandbox environment is ready, you will be redirected to sandbox environment's Welcome wizard.</span></span>
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

<span data-ttu-id="20cb8-119">Du kan velge **Finn ut mer**-knappen for å lese om utviklerscenarioer som du kan prøve i et sandkassemiljø, eller velg **Lukk**-knappen for å fortsette til Rollesenteret for [!INCLUDE[d365fin](includes/d365fin_md.md)]-sandkasseforekomsten din.</span><span class="sxs-lookup"><span data-stu-id="20cb8-119">You can choose the **Learn more** button to read about developer scenarios that you can try in a sandbox environment or choose the **Close** button to continue to the Role Center of your [!INCLUDE[d365fin](includes/d365fin_md.md)] sandbox instance.</span></span>

<span data-ttu-id="20cb8-120">Øverst i rollesenteret vises en melding som varsler deg at dette er et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="20cb8-120">At the top of the Role Center, a notification appears to inform you that this is a sandbox environment.</span></span> <span data-ttu-id="20cb8-121">Du kan også se typen miljø på tittellinjen i klienten.</span><span class="sxs-lookup"><span data-stu-id="20cb8-121">You can also see the type of the environment in the title bar of the client.</span></span>
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> <span data-ttu-id="20cb8-122">Et sandkassemiljø som er opprettet på denne måten, inneholder bare standard demonstrasjonsdata for CRONUS-selskapet.</span><span class="sxs-lookup"><span data-stu-id="20cb8-122">A sandbox environment created in this way only contains the default demonstration data for the CRONUS company.</span></span> <span data-ttu-id="20cb8-123">Ingen data kopieres eller blir ellers overført fra produksjonsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="20cb8-123">No data is copied or otherwise transferred from the production environment.</span></span><br /><br />
> <span data-ttu-id="20cb8-124">Du kan også opprette et sandkassemiljø som inneholder produksjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="20cb8-124">You can also create a sandbox environment containing the production data.</span></span> <span data-ttu-id="20cb8-125">Du må gjøre dette ved hjelp av administrasjonssenteret.</span><span class="sxs-lookup"><span data-stu-id="20cb8-125">You must do this through the administration center.</span></span> <span data-ttu-id="20cb8-126">Hvis du vil ha mer informasjon, kan du se [Administrere miljøer](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) i hjelpen for utviklere og IT-eksperter.</span><span class="sxs-lookup"><span data-stu-id="20cb8-126">For more information, see [Managing Environments](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) in the Developer and IT-Pro help.</span></span>

<span data-ttu-id="20cb8-127">Når som helst kan du gå tilbake til siden **Sandkassemiljø** og tilbakestille sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="20cb8-127">At any time, you can return to the **Sandbox Environment** page, and reset the sandbox environment.</span></span>

> [!NOTE]  
> <span data-ttu-id="20cb8-128">Tilbakestilling av sandkassemiljøet fjerner det fullstendig, og deretter opprettes det på nytt med standard demonstrasjonsdata.</span><span class="sxs-lookup"><span data-stu-id="20cb8-128">Resetting the sandbox environment will remove it completely, and then create it again with the default demonstration data.</span></span>  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

<span data-ttu-id="20cb8-129">En administrator kan begrense eller blokkere tilgang for enkelte brukere til sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="20cb8-129">An administrator can limit or even block access for some users to the sandbox environment.</span></span> <span data-ttu-id="20cb8-130">Dette kan gjøres ved hjelp av produktets standard sikkerhetsfunksjoner, for eksempel brukerkort, brukergrupper og tillatelsessett.</span><span class="sxs-lookup"><span data-stu-id="20cb8-130">This can be done by using the standard security features of the product, such as the User card, user groups, and permission sets.</span></span> <span data-ttu-id="20cb8-131">Hvis du vil ha mer informasjon, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="20cb8-131">For more information, see [Assign Permissions to Users and Groups](ui-define-granular-permissions.md).</span></span>  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a><span data-ttu-id="20cb8-132">Avanserte funksjoner i sandkassemiljøet</span><span class="sxs-lookup"><span data-stu-id="20cb8-132">Advanced Functionality in the Sandbox Environment</span></span>

<span data-ttu-id="20cb8-133">Sandkassemiljøet er ikke minst nyttig fordi det inneholder et par nyttige funksjoner.</span><span class="sxs-lookup"><span data-stu-id="20cb8-133">The sandbox environment is not least useful because it includes a couple of handy features.</span></span>

### <a name="designer"></a><span data-ttu-id="20cb8-134">Designer</span><span class="sxs-lookup"><span data-stu-id="20cb8-134">Designer</span></span>

<span data-ttu-id="20cb8-135">I et sandkassemiljø finner du **Designer** aktivert.</span><span class="sxs-lookup"><span data-stu-id="20cb8-135">In a sandbox environment, you will find the **Designer** enabled.</span></span> <span data-ttu-id="20cb8-136">Du kan aktivere Designer ved å velge designikonet ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) på en side, eller ved å velge **Utforming**-menyen på menyen ![Innstillinger](media/ui-experience/settings_icon_small.png).</span><span class="sxs-lookup"><span data-stu-id="20cb8-136">You can activate Designer by selecting the design icon ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) on a page, or by choosing the **Design** menu item in the ![Settings](media/ui-experience/settings_icon_small.png) Settings menu.</span></span>

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="to-enable-the-advanced-user-experience"></a><span data-ttu-id="20cb8-137">Slik aktiverer du den avanserte brukeropplevelsen</span><span class="sxs-lookup"><span data-stu-id="20cb8-137">To enable the advanced user experience</span></span>
<span data-ttu-id="20cb8-138">Det er mulig å aktivere og prøve de avanserte (alle) funksjonene i [!INCLUDE[d365fin](includes/d365fin_md.md)] i en sandkasseleietaker ved å angi **Opplevelse**-feltet på **Selskapsopplysninger**-siden.</span><span class="sxs-lookup"><span data-stu-id="20cb8-138">It is possible to enable and try the advanced (full) functionality of [!INCLUDE[d365fin](includes/d365fin_md.md)] in a sandbox tenant by setting the **Experience** field on the **Company Information** page.</span></span>

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

<span data-ttu-id="20cb8-139">Når du har aktivert de avanserte funksjonene i en sandkasseleietaker, får du tilgang til alle standardprofiler (roller) og rollesentre.</span><span class="sxs-lookup"><span data-stu-id="20cb8-139">After you have enabled the advanced functionality in a sandbox tenant, you get access to all the standard profiles (roles) and Role Centers.</span></span> <span data-ttu-id="20cb8-140">Du kan også opprette et evalueringsselskap med et fullstendig oppsett, inkludert demonstrasjonsdata og tilgang til avanserte områder i produktet.</span><span class="sxs-lookup"><span data-stu-id="20cb8-140">You can also create an evaluation company that is fully set up, including demonstration data and access to the advanced areas of the product.</span></span>

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->

## <a name="see-also"></a><span data-ttu-id="20cb8-141">Se også</span><span class="sxs-lookup"><span data-stu-id="20cb8-141">See Also</span></span>

<span data-ttu-id="20cb8-142">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="20cb8-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="20cb8-143">[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] Prøveversjoner og abonnementer](across-preview.md)</span><span class="sxs-lookup"><span data-stu-id="20cb8-143">[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] Trials and Subscriptions](across-preview.md)</span></span>  
[<span data-ttu-id="20cb8-144">Behandle miljøer i administrasjonssenteret for Business Central</span><span class="sxs-lookup"><span data-stu-id="20cb8-144">Managing Environments in the Business Central administration center</span></span>](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  
