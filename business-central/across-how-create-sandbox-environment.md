---
title: Opprett et sandkassemiljø
description: Opprett et miljø for utforsking, læring, demoer, utvikling og testing innenfra Business Central.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 06/08/2021
ms.author: solsen
ms.openlocfilehash: a76ae33815b8e9368f45b72fd8703bfc47cbd079
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215631"
---
# <a name="creating-a-sandbox-environment-in-prod_short"></a><span data-ttu-id="0108e-103">Opprette et sandkassemiljø i [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="0108e-103">Creating a Sandbox Environment in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

<span data-ttu-id="0108e-104">Med [!INCLUDE[prod_short](includes/prod_short.md)] kan du enkelt opprette et sikkert miljø der du kan teste, lære opp eller feilsøke uten å forstyrre firmaets arbeidsprosesser eller forretningsdata.</span><span class="sxs-lookup"><span data-stu-id="0108e-104">With [!INCLUDE[prod_short](includes/prod_short.md)], you can easily create a safe environment where you can test, train, or troubleshoot without disturbing your company's work processes or business data.</span></span> <span data-ttu-id="0108e-105">Et slikt ikke-produksjonsmiljø kalles en *sandkasse*.</span><span class="sxs-lookup"><span data-stu-id="0108e-105">Such a non-production environment is called a *sandbox*.</span></span> <span data-ttu-id="0108e-106">Isolert fra produksjon er et sandkassemiljø stedet der du trygt kan utforske, lære, demonstrere, utvikle og teste tjenesten uten risikoen ved å påvirke data og innstillinger i produksjonsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="0108e-106">Isolated from production, a sandbox environment is the place to safely explore, learn, demo, develop, and test the service without the risk of affecting the data and settings of your production environment.</span></span>  

<span data-ttu-id="0108e-107">Administratoren administrerer sandkassemiljøer i [administrasjonssenteret](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), men hvis du raskt vil teste noe, kan du opprette et sandkassemiljø innenfra [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="0108e-107">Your administrator manages sandbox environments in the [administration center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), but if you want to quickly test something, you can create a sandbox environment from inside [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="0108e-108">Når du er ferdig, kan du fjerne sandkassen ved å bruke administrasjonssenteret.</span><span class="sxs-lookup"><span data-stu-id="0108e-108">Once you're done, you can remove the sandbox, using the administration center.</span></span>  

> [!NOTE]
> <span data-ttu-id="0108e-109">Teknisk sett er sandkassemiljøer svært forskjellige fra produksjonsmiljøer, selv om systemansvarlig oppretter en sandkasse som inkluderer produksjonsdata.</span><span class="sxs-lookup"><span data-stu-id="0108e-109">Technically, sandbox environments are very different from production environments, even if your administrator creates a sandbox that includes production data.</span></span> <span data-ttu-id="0108e-110">Du kan ikke bruke en sandkasse for ytelsestester, og du kan for eksempel ikke be om databaseeksport.</span><span class="sxs-lookup"><span data-stu-id="0108e-110">You cannot use a sandbox for benchmarking, and you cannot request a database export, for example.</span></span> <span data-ttu-id="0108e-111">Hvis du vil opprette en sandkasse for ytelsestest, kan systemansvarlig opprette et eget miljø i administrasjonssenteret.</span><span class="sxs-lookup"><span data-stu-id="0108e-111">If you want to create a sandbox for benchmarking, your administrator can create a dedicated environment in the administration center.</span></span> <span data-ttu-id="0108e-112">Hvis du vil ha mer informasjon, kan du se [Produksjons- og sandkassemiljøer](/dynamics365/business-central/dev-itpro/administration/environment-types).</span><span class="sxs-lookup"><span data-stu-id="0108e-112">For more information, see [Production and Sandbox Environments](/dynamics365/business-central/dev-itpro/administration/environment-types).</span></span>

## <a name="to-create-a-sandbox-environment-in-your-prod_short"></a><span data-ttu-id="0108e-113">Slik oppretter du et sandkassemiljø i [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="0108e-113">To create a sandbox environment in your [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

1. <span data-ttu-id="0108e-114">Logg deg på din produksjonsforekomst av [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="0108e-114">Sign in to your production instance of [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

2. <span data-ttu-id="0108e-115">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Sandkassemiljø**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0108e-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sandbox Environment**, and then choose the related link.</span></span>
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. <span data-ttu-id="0108e-116">Velg **Opprett**-knappen.</span><span class="sxs-lookup"><span data-stu-id="0108e-116">Choose the **Create** button.</span></span>  

    <span data-ttu-id="0108e-117">Det åpnes en annen fane med [!INCLUDE[prod_short](includes/prod_short.md)], der du kan fullføre oppsettet av sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="0108e-117">Another tab with [!INCLUDE[prod_short](includes/prod_short.md)] opens where you can finish the setup of your sandbox environment.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="0108e-118">Hvis du har aktivert popup-blokkering i webleseren, endrer du den til å tillate URL-adresser fra adressen \*.businesscentral.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="0108e-118">If you have pop-up blocker enabled in your browser, change it to allow URLs from the \*.businesscentral.dynamics.com address.</span></span>

<span data-ttu-id="0108e-119">Når sandkassemiljøet er klart, vil du bli videresendt til velkomstveiviseren i sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="0108e-119">When the sandbox environment is ready, you will be redirected to sandbox environment's Welcome wizard.</span></span>
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

<span data-ttu-id="0108e-120">Du kan velge **Finn ut mer**-knappen for å lese om utviklerscenarioer som du kan prøve i et sandkassemiljø, eller velg **Lukk**-knappen for å fortsette til Rollesenteret for [!INCLUDE[prod_short](includes/prod_short.md)]-sandkasseforekomsten din.</span><span class="sxs-lookup"><span data-stu-id="0108e-120">You can choose the **Learn more** button to read about developer scenarios that you can try in a sandbox environment or choose the **Close** button to continue to the Role Center of your [!INCLUDE[prod_short](includes/prod_short.md)] sandbox instance.</span></span>

<span data-ttu-id="0108e-121">Øverst i rollesenteret vises en melding som varsler deg at dette er et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="0108e-121">At the top of the Role Center, a notification appears to inform you that this is a sandbox environment.</span></span> <span data-ttu-id="0108e-122">Du kan også se typen miljø på tittellinjen i klienten.</span><span class="sxs-lookup"><span data-stu-id="0108e-122">You can also see the type of the environment in the title bar of the client.</span></span>
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> <span data-ttu-id="0108e-123">Et sandkassemiljø som er opprettet på denne måten, inneholder bare standard demonstrasjonsdata for CRONUS-selskapet.</span><span class="sxs-lookup"><span data-stu-id="0108e-123">A sandbox environment created in this way only contains the default demonstration data for the CRONUS company.</span></span> <span data-ttu-id="0108e-124">Ingen data kopieres eller blir ellers overført fra produksjonsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="0108e-124">No data is copied or otherwise transferred from the production environment.</span></span>
>
> <span data-ttu-id="0108e-125">Du kan eventuelt opprette et sandkassemiljø basert på produksjonsdata.</span><span class="sxs-lookup"><span data-stu-id="0108e-125">Alternatively, create a sandbox environment based on production data.</span></span> <span data-ttu-id="0108e-126">Du må gjøre dette ved hjelp av administrasjonssenteret.</span><span class="sxs-lookup"><span data-stu-id="0108e-126">You must do this through the administration center.</span></span> <span data-ttu-id="0108e-127">Hvis du vil ha mer informasjon, kan du se [Administrere miljøer](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) i utvikler- og administrasjonsinnholdet.</span><span class="sxs-lookup"><span data-stu-id="0108e-127">For more information, see [Managing Environments](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) in the developer and administration content.</span></span>  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

<span data-ttu-id="0108e-128">En administrator kan begrense eller blokkere tilgang for enkelte brukere til sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="0108e-128">An administrator can limit or even block access for some users to the sandbox environment.</span></span> <span data-ttu-id="0108e-129">Dette kan gjøres ved hjelp av produktets standard sikkerhetsfunksjoner, for eksempel brukerkort, brukergrupper og tillatelsessett.</span><span class="sxs-lookup"><span data-stu-id="0108e-129">This can be done by using the standard security features of the product, such as the User card, user groups, and permission sets.</span></span> <span data-ttu-id="0108e-130">Hvis du vil ha mer informasjon, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="0108e-130">For more information, see [Assign Permissions to Users and Groups](ui-define-granular-permissions.md).</span></span>  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a><span data-ttu-id="0108e-131">Avanserte funksjoner i sandkassemiljøet</span><span class="sxs-lookup"><span data-stu-id="0108e-131">Advanced Functionality in the Sandbox Environment</span></span>

<span data-ttu-id="0108e-132">Sandkassemiljøet er ikke minst nyttig fordi det inneholder et par nyttige funksjoner:</span><span class="sxs-lookup"><span data-stu-id="0108e-132">The sandbox environment is not least useful because it includes a couple of handy features:</span></span>

* [<span data-ttu-id="0108e-133">Avansert brukeropplevelse</span><span class="sxs-lookup"><span data-stu-id="0108e-133">Advanced user experience</span></span>](#advanced-user-experience)  
* [<span data-ttu-id="0108e-134">Fullstendige eksempeldata</span><span class="sxs-lookup"><span data-stu-id="0108e-134">Complete sample data</span></span>](#complete-sample-data)  
* [<span data-ttu-id="0108e-135">Utforming</span><span class="sxs-lookup"><span data-stu-id="0108e-135">Designer</span></span>](#designer)  

### <a name="advanced-user-experience"></a><span data-ttu-id="0108e-136">Avansert brukeropplevelse</span><span class="sxs-lookup"><span data-stu-id="0108e-136">Advanced user experience</span></span>

<span data-ttu-id="0108e-137">Det er mulig å aktivere og prøve alle funksjonene i standardversjonen av [!INCLUDE[prod_short](includes/prod_short.md)] i en sandkasseleietaker ved å sette **Opplevelse**-feltet på **Selskapsopplysninger**-siden til *Premium*.</span><span class="sxs-lookup"><span data-stu-id="0108e-137">It is possible to enable and try the full functionality of the standard version of [!INCLUDE[prod_short](includes/prod_short.md)] in a sandbox tenant by setting the **Experience** field on the **Company Information** page to *Premium*.</span></span> Finn **Selskapsopplysninger**-siden på ikonmenyen for :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="Innstillinger":::.  

<span data-ttu-id="0108e-139">Når du har aktivert *Premium*-brukeropplevelsen, får du tilgang til alle standardprofilene (rollene) og rollesentrene i standardversjonen.</span><span class="sxs-lookup"><span data-stu-id="0108e-139">After you have enabled the *Premium* user experience, you get access to all the standard profiles (roles) and Role Centers in the standard version.</span></span> <span data-ttu-id="0108e-140">Du kan også opprette et evalueringsselskap med et fullstendig oppsett, inkludert demonstrasjonsdata og tilgang til avanserte områder i produktet.</span><span class="sxs-lookup"><span data-stu-id="0108e-140">You can also create an evaluation company that is fully set up, including demonstration data and access to the advanced areas of the product.</span></span> <span data-ttu-id="0108e-141">Alternativt kan du kontakte en videresalgspartner for en demonstrasjon av funksjonene.</span><span class="sxs-lookup"><span data-stu-id="0108e-141">Alternatively, contact a reselling partner for a demonstration of the capabilities.</span></span> <span data-ttu-id="0108e-142">Hvis du vil ha mer informasjon, kan du se [Hvordan finner jeg en partner for videresalg?](/dynamics365/business-central/across-faq.yml#findpartner).</span><span class="sxs-lookup"><span data-stu-id="0108e-142">For more information, see [How do I find a reselling partner?](/dynamics365/business-central/across-faq.yml#findpartner).</span></span>  

### <a name="complete-sample-data"></a><span data-ttu-id="0108e-143">Fullstendige eksempeldata</span><span class="sxs-lookup"><span data-stu-id="0108e-143">Complete sample data</span></span>

<span data-ttu-id="0108e-144">I situasjoner der du trenger flere eksempeldata, kontakter du partneren for videresalg.</span><span class="sxs-lookup"><span data-stu-id="0108e-144">For situations where you need additional sample data, please talk to your reselling partner.</span></span>
<!-- In the sandbox environment, you can also create a new company with the **Advanced Evaluation - Complete Sample Data** option so that you can take training or step through walkthroughs that require additional sample data, such as [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).   -->

#### <a name="to-create-a-company-with-complete-sample-data-in-a-sandbox"></a><span data-ttu-id="0108e-145">Slik oppretter du et selskap med fullstendige eksempeldata i en sandkasse</span><span class="sxs-lookup"><span data-stu-id="0108e-145">To create a company with complete sample data in a sandbox</span></span>

1. <span data-ttu-id="0108e-146">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Selskaper**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0108e-146">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Companies**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0108e-147">Velg handlingen **Ny**, og velg deretter **Opprett nytt selskap**.</span><span class="sxs-lookup"><span data-stu-id="0108e-147">Choose the **New** action, and then choose **Create New Company**.</span></span>  
3. <span data-ttu-id="0108e-148">Velg **Neste** på siden for **assistert oppsett av oppretting av et selskap**.</span><span class="sxs-lookup"><span data-stu-id="0108e-148">In the **Assisted Setup for Creating a Company** page, choose **Next**.</span></span>  
4. <span data-ttu-id="0108e-149">Angi et navn for det nye selskapet, og velg deretter **Avansert evaluering - Fullfør eksempeldata** i feltet **Velg dataene og oppsettet for å komme i gang**.</span><span class="sxs-lookup"><span data-stu-id="0108e-149">Specify a name for the new company, and then, in the **Select the data and setup to get started** field, choose **Advanced Evaluation - Complete Sample Data**.</span></span>  
5. <span data-ttu-id="0108e-150">Fullfør resten av den assisterte oppsettsveiledningen.</span><span class="sxs-lookup"><span data-stu-id="0108e-150">Complete the rest of the assisted setup guide.</span></span>  

<span data-ttu-id="0108e-151">Når veiledningen for assistert oppsett er fullført, kan du begynne å utforske det nye selskapet med de fullstendige eksempeldataene.</span><span class="sxs-lookup"><span data-stu-id="0108e-151">When the assisted setup guide completes, you can start exploring the new company with the complete sample data.</span></span> <span data-ttu-id="0108e-152">Hvis du vil ha mer informasjon, kan du se [Opprette nye selskaper i [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="0108e-152">For more information, see [Creating New Companies in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).</span></span>  

### <a name="designer"></a><span data-ttu-id="0108e-153">Designer</span><span class="sxs-lookup"><span data-stu-id="0108e-153">Designer</span></span>

<span data-ttu-id="0108e-154">I et sandkassemiljø finner du **Designer** aktivert.</span><span class="sxs-lookup"><span data-stu-id="0108e-154">In a sandbox environment, you will find the **Designer** enabled.</span></span> <span data-ttu-id="0108e-155">Du kan aktivere Designer ved å velge designikonet ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) på en side, eller ved å velge **Utforming**-menyen på menyen ![Innstillinger](media/ui-experience/settings_icon_small.png).</span><span class="sxs-lookup"><span data-stu-id="0108e-155">You can activate Designer by selecting the design icon ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) on a page, or by choosing the **Design** menu item in the ![Settings](media/ui-experience/settings_icon_small.png) Settings menu.</span></span>  

<span data-ttu-id="0108e-156">Hvis du vil ha mer informasjon, kan du se [Bruk av utformingen](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) i innholdet for utviklere og administratorer (bare på engelsk).</span><span class="sxs-lookup"><span data-stu-id="0108e-156">For more information, see [Using Designer](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) in the developer and admin content (in English only).</span></span>  

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-also"></a><span data-ttu-id="0108e-157">Se også</span><span class="sxs-lookup"><span data-stu-id="0108e-157">See Also</span></span>

<span data-ttu-id="0108e-158">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0108e-158">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="0108e-159">[[!INCLUDE[prod_long](includes/prod_long.md)] Prøveversjoner og abonnementer](across-preview.md)</span><span class="sxs-lookup"><span data-stu-id="0108e-159">[[!INCLUDE[prod_long](includes/prod_long.md)] Trials and Subscriptions](across-preview.md)</span></span>  
[<span data-ttu-id="0108e-160">Behandle miljøer i administrasjonssenteret for Business Central</span><span class="sxs-lookup"><span data-stu-id="0108e-160">Managing Environments in the Business Central administration center</span></span>](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
