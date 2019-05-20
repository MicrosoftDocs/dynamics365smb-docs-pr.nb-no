---
title: Administrere brukere og roller | Microsoft-dokumentasjon
description: Finn ut hvordan du administrerer brukere og rollesentre i Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: fc52d943938616041881c55f70c510e4c63b5de6
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245812"
---
# <a name="understanding-users-profiles-and-role-centers"></a><span data-ttu-id="06d30-103">Forstå brukere, profiler og rollesentre</span><span class="sxs-lookup"><span data-stu-id="06d30-103">Understanding Users, Profiles, and Role Centers</span></span>

<span data-ttu-id="06d30-104">I [!INCLUDE[d365fin](includes/d365fin_md.md)] legges brukere til av en administrator som gir også brukere tilgang til deler av [!INCLUDE[d365fin](includes/d365fin_md.md)] som de trenger i arbeidet.</span><span class="sxs-lookup"><span data-stu-id="06d30-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], users are added by an administrator who also gives users access to the areas of [!INCLUDE[d365fin](includes/d365fin_md.md)] that they need in their work.</span></span>  

<span data-ttu-id="06d30-105">Tilgang til funksjonene behandles gjennom *brukergrupper* og *profiler*.</span><span class="sxs-lookup"><span data-stu-id="06d30-105">Access to functionality is managed through *user groups* and *profiles*.</span></span> <span data-ttu-id="06d30-106">Du kan som administrator legge til og fjerne brukere som en del av [!INCLUDE[d365fin](includes/d365fin_md.md)]-abonnementet, og du kan tilordne brukertillatelser gjennom brukergrupper.</span><span class="sxs-lookup"><span data-stu-id="06d30-106">As an administrator, you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription, and you can assign users permissions through user groups.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="06d30-107">Legge til brukere</span><span class="sxs-lookup"><span data-stu-id="06d30-107">Adding Users</span></span>

<span data-ttu-id="06d30-108">For å legge til brukere i [!INCLUDE[d365fin](includes/d365fin_md.md)] på nettet må selskapets Office 365-administrator først opprette brukere i administrasjonssenteret for Office 365.</span><span class="sxs-lookup"><span data-stu-id="06d30-108">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="06d30-109">For mer informasjon, se [Legge til brukere i Office 365 for bedrifter](https://aka.ms/CreateOffice365Users).</span><span class="sxs-lookup"><span data-stu-id="06d30-109">For more information, see [Add Users to Office 365 for business](https://aka.ms/CreateOffice365Users).</span></span>

<span data-ttu-id="06d30-110">Administrator kan deretter tilordne tillatelser til hver enkelt bruker og brukergruppe.</span><span class="sxs-lookup"><span data-stu-id="06d30-110">Then, the administrator can assign permissions to each user and groups of users.</span></span> <span data-ttu-id="06d30-111">Hvis du vil ha mer informasjon, kan du se [Administrere brukere og tillatelser](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="06d30-111">For more information, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>  

<span data-ttu-id="06d30-112">De mest avanserte tillatelsene som en bruker kan ha, er SUPER-tillatelsessettet.</span><span class="sxs-lookup"><span data-stu-id="06d30-112">The most powerful permissions that a user can have is the SUPER permission set.</span></span> <span data-ttu-id="06d30-113">Hvert selskap må ha minst én bruker med dette tillatelsessettet, men det er anbefalt å gi hver bruker tillatelser som samsvarer med arbeidsbehovet deres i [!INCLUDE[prodshort](includes/prodshort.md)] og ikke mer enn det.</span><span class="sxs-lookup"><span data-stu-id="06d30-113">Each company must have at least one user with this permission set, but it is a best practice to give each user permissions that match their work needs in [!INCLUDE[prodshort](includes/prodshort.md)] and not more than that.</span></span> <span data-ttu-id="06d30-114">Dette sikrer at brukere bare har tilgang til data som er relevant for arbeidet deres, for eksempel.</span><span class="sxs-lookup"><span data-stu-id="06d30-114">This helps ensure that users only have access to data that is relevant to their work, for example.</span></span>  

> [!TIP]
> <span data-ttu-id="06d30-115">Det er anbefalt å sikre at Office 365-administratoren også har SUPER-tillatelsen angitt i [!INCLUDE[prodshort](includes/prodshort.md)] fordi dette forenkler en rekke administrative oppgaver, inkludert oppsett av integrering med andre programmer.</span><span class="sxs-lookup"><span data-stu-id="06d30-115">It's a best practice to make sure that the Office 365 administrator also has the SUPER permission set in [!INCLUDE[prodshort](includes/prodshort.md)] because that makes many administrative tasks easier, including setting up integration with other apps.</span></span>

### <a name="users-of-on-premises-deployments"></a><span data-ttu-id="06d30-116">Brukere av lokale distribusjoner</span><span class="sxs-lookup"><span data-stu-id="06d30-116">Users of on-premises deployments</span></span>

<span data-ttu-id="06d30-117">For lokale distribusjoner av [!INCLUDE[d365fin](includes/d365fin_md.md)] kan systemansvarlig velge mellom forskjellige legitimasjonsgodkjenningsmekanismer for brukerne.</span><span class="sxs-lookup"><span data-stu-id="06d30-117">For on-premises deployments of [!INCLUDE[d365fin](includes/d365fin_md.md)], the administrator can choose between different credential authorization mechanisms for users.</span></span> <span data-ttu-id="06d30-118">Når du deretter oppretter en bruker, angir du ulike opplysninger avhengig av legitimasjonstypen du bruker i den spesifikke forekomsten av [!INCLUDE[server](includes/server.md)].</span><span class="sxs-lookup"><span data-stu-id="06d30-118">Then, when you create a user, you provide different information depending on the credential type that you are using in the specific [!INCLUDE[server](includes/server.md)] instance.</span></span> <span data-ttu-id="06d30-119">Hvis du vil ha mer informasjon, kan du se [Godkjenning og legitimasjonstyper](/dynamics365/business-central/dev-itpro/administration/users-credential-types) i Administrasjon-delen for utviklere og ITPro-innholdet for [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="06d30-119">For more information, see the [Authentication and Credential Types](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in the Administration section of the developer and ITPro content for [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="profiles"></a><span data-ttu-id="06d30-120">Profiler</span><span class="sxs-lookup"><span data-stu-id="06d30-120">Profiles</span></span>

<span data-ttu-id="06d30-121">Personene i selskapet som har tilgang til [!INCLUDE[d365fin](includes/d365fin_md.md)], er alle tilordnet en *profil* som gir dem tilgang til et *rollesenter*.</span><span class="sxs-lookup"><span data-stu-id="06d30-121">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a *profile* that gives them access to a *Role Center*.</span></span>

<span data-ttu-id="06d30-122">Profiler er samlinger av [!INCLUDE[d365fin](includes/d365fin_md.md)]-brukere som deler samme rollesenter.</span><span class="sxs-lookup"><span data-stu-id="06d30-122">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same Role Center.</span></span> <span data-ttu-id="06d30-123">Et rollesenter er utgangspunktet og hjemmesiden for [!INCLUDE[d365fin](includes/d365fin_md.md)], som gir deg rask tilgang til de viktigste oppgavene og viser forskjellig innsikt og viktige ytelsesindikatorer (KPI-er) om arbeidet.</span><span class="sxs-lookup"><span data-stu-id="06d30-123">A Role Center is the entry point and home page for [!INCLUDE[d365fin](includes/d365fin_md.md)] that gives you quick access to your most important tasks and displays various insights and key performance indicators (KPIs) about your work.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="06d30-124">I den gjeldende versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] på nettet kan du legge til, endre eller slette profiler.</span><span class="sxs-lookup"><span data-stu-id="06d30-124">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] online, you cannot add, edit, or delete profiles.</span></span>  

### <a name="CreateProfile"></a><span data-ttu-id="06d30-125">Opprette en profil</span><span class="sxs-lookup"><span data-stu-id="06d30-125">Create a profile</span></span>

1.  <span data-ttu-id="06d30-126">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Profilliste**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="06d30-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Profile List**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="06d30-127">På siden **Profilliste** velger du handlingen **Ny** for å åpne **Nytt profilkort**-siden.</span><span class="sxs-lookup"><span data-stu-id="06d30-127">On the **Profile List** page, choose the **New** action to open the **New Profile Card** page.</span></span>  

3.  <span data-ttu-id="06d30-128">Skriv inn et navn som beskriver den tiltenkte rollen for brukerne, i **Profil-ID**-feltet.</span><span class="sxs-lookup"><span data-stu-id="06d30-128">In the **Profile ID** field, enter a name that describes the intended role of the users.</span></span>  

4.  <span data-ttu-id="06d30-129">I **Beskrivelse**-feltet angir du en beskrivelse av profil-IDen, for eksempel **Ordrebehandler**.</span><span class="sxs-lookup"><span data-stu-id="06d30-129">In the **Description** field, enter a description of the Profile ID, for example, **Order Processor**.</span></span>  

5.  <span data-ttu-id="06d30-130">Sett **Rollesenter-ID**-felttet til rollesenteret du vil tilordne til profilen.</span><span class="sxs-lookup"><span data-stu-id="06d30-130">Set the **Role Center ID** field to the Role Center that you want to assign to the profile.</span></span>  

<span data-ttu-id="06d30-131">Fremgangsmåten for å endre en eksisterende profil er det samme, bortsett fra at du velger en eksisterende profil på **Profilliste**-siden i stedet for å velge handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="06d30-131">The procedure for modifying an existing profile is the same, except you select an existing profile on the **Profile List** page instead of choosing the **New** action.</span></span>  


### <a name="copy-a-profile"></a><span data-ttu-id="06d30-132">Kopiere en profil</span><span class="sxs-lookup"><span data-stu-id="06d30-132">Copy a profile</span></span>
<span data-ttu-id="06d30-133">Du kan spare tid ved å kopiere en profil hvis du vil bruke lignende innstillinger på en profil, og du bare vil endre noen innstillinger.</span><span class="sxs-lookup"><span data-stu-id="06d30-133">Copying a profile can save you time if you want to use similar settings on a profile and you only want to change a few settings.</span></span>

1.  <span data-ttu-id="06d30-134">Åpne profilen du vil kopiere, og velg deretter **Kopier profil**.</span><span class="sxs-lookup"><span data-stu-id="06d30-134">Open the profile that you want to copy, and then choose the **Copy Profile** action.</span></span>

2.  <span data-ttu-id="06d30-135">I **Ny profil-ID**-feltet skriver du inn et navn for profilen du vil kopiere.</span><span class="sxs-lookup"><span data-stu-id="06d30-135">In **New Profile ID** field, enter a name for the profile that you want to copy.</span></span>

3.  <span data-ttu-id="06d30-136">Sett feltet **Nytt profilomfang** til ett av følgende:</span><span class="sxs-lookup"><span data-stu-id="06d30-136">Set the **New Profile Scope** field to one of the following:</span></span>

    - <span data-ttu-id="06d30-137">**System** slik at den nye profilen blir tilgjengelig for alle leietakerdatabaser som bruker programmet.</span><span class="sxs-lookup"><span data-stu-id="06d30-137">**System** to make the new profile available to all tenant databases that use the application.</span></span>
    - <span data-ttu-id="06d30-138">**Leier** slik at den nye profilen blir tilgjengelig kun for den gjeldende leietakerdatabasen.</span><span class="sxs-lookup"><span data-stu-id="06d30-138">**Tenant** to make the new profile available to just the current tenant database.</span></span>
4. <span data-ttu-id="06d30-139">Når du er ferdig, velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="06d30-139">Choose the **OK** button when done.</span></span>

### <a name="ExportImportProfile"></a><span data-ttu-id="06d30-140">Eksportere og importere profiler</span><span class="sxs-lookup"><span data-stu-id="06d30-140">Export and import profiles</span></span>

<span data-ttu-id="06d30-141">Du kan eksportere og importere profiler som XML-filer til og fra en [!INCLUDE[d365fin](includes/d365fin_md.md)]-database.</span><span class="sxs-lookup"><span data-stu-id="06d30-141">You can export and import profiles as XML files to and from the a [!INCLUDE[d365fin](includes/d365fin_md.md)] database.</span></span> <span data-ttu-id="06d30-142">Du kan spare tid ved å eksportere og importere en profil når du konfigurerer brukergrensesnittet fordi du kan bruke en eksisterende profilkonfigurasjon i stedet for å konfigurere en profil på nytt.</span><span class="sxs-lookup"><span data-stu-id="06d30-142">Exporting and importing a profile can save you time when configuring the user interface because you reuse an existing profile configuration instead of having to configure a profile from scratch.</span></span> <span data-ttu-id="06d30-143">Hvis du har en profil som er konfigurert i en [!INCLUDE[d365fin](includes/d365fin_md.md)]-database, og du vil bruke på hele eller deler av det samme profil oppsettet i en annen database, kan du eksportere profilen til en XML-fil.</span><span class="sxs-lookup"><span data-stu-id="06d30-143">If you have a profile that is configured in a [!INCLUDE[d365fin](includes/d365fin_md.md)] database and you would like to reuse all or some of the same profile configurations in another database, you can export the profile to an XML file.</span></span> <span data-ttu-id="06d30-144">Deretter kan du importere XML-filen for profilen til den andre databasen.</span><span class="sxs-lookup"><span data-stu-id="06d30-144">Then, you can import the profile XML file into the other database.</span></span>

-   <span data-ttu-id="06d30-145">Hvis du vil eksportere en profil, kan du velge **Eksporter profiler**-handlingen fra **Profilliste**- eller **Profilkort**-siden, eller du kan søke etter og åpne **Eksporter profiler**-siden.</span><span class="sxs-lookup"><span data-stu-id="06d30-145">To export a profile, you can either choose the **Export Profiles** action from the **Profile List** or **Profile Card** page or you can search for and open the **Export Profiles** page.</span></span> <span data-ttu-id="06d30-146">Lagre XML-filen på datamaskinen eller i nettverket.</span><span class="sxs-lookup"><span data-stu-id="06d30-146">Save the XML file to a location on your computer or network.</span></span>

-   <span data-ttu-id="06d30-147">Hvis du vil importere en profil, kan du velge **Importer profil**-handlingen fra **Profilliste**-siden, eller du kan søke etter og åpne **Importer profiler**-siden.</span><span class="sxs-lookup"><span data-stu-id="06d30-147">To import a profile, you can either choose the **Import Profile** action from the **Profile List** page, or you can search for and open the **Import Profiles** page.</span></span> 

    > [!NOTE]  
    >  <span data-ttu-id="06d30-148">Du kan ikke importere en profil som allerede finnes i databasen, selv om XML-filen har et annet navn eller annet innhold.</span><span class="sxs-lookup"><span data-stu-id="06d30-148">You cannot import a profile that already exists in the database, even though the XML file is named differently or has different content.</span></span> <span data-ttu-id="06d30-149">Du må slette den eksisterende profilen før du kan importere den nye profilen.</span><span class="sxs-lookup"><span data-stu-id="06d30-149">You must delete the existing profile before you can import the new profile.</span></span>


## <a name="configuration-and-personalization"></a><span data-ttu-id="06d30-150">Konfigurasjon og tilpasning</span><span class="sxs-lookup"><span data-stu-id="06d30-150">Configuration and Personalization</span></span>
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->

<span data-ttu-id="06d30-151">Brukere tilpasser brukergrensesnittet i sin egen versjon ved å tilpasse brukergrensesnittet når de er logget på sine egne konti.</span><span class="sxs-lookup"><span data-stu-id="06d30-151">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="06d30-152">Denne tilpasningen kan slettes av systemansvarlig.</span><span class="sxs-lookup"><span data-stu-id="06d30-152">This personalization can be deleted by the administrator.</span></span> <span data-ttu-id="06d30-153">Hvis du vil ha mer informasjon, se [Tilpasse arbeidsområdet ](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="06d30-153">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="06d30-154">Se også</span><span class="sxs-lookup"><span data-stu-id="06d30-154">See Also</span></span>  
[<span data-ttu-id="06d30-155">Administrere brukere og tillatelser</span><span class="sxs-lookup"><span data-stu-id="06d30-155">Managing Users and Permissions</span></span>](ui-how-users-permissions.md)  
[<span data-ttu-id="06d30-156">Administrere tilpasning som Administrator</span><span class="sxs-lookup"><span data-stu-id="06d30-156">Managing Personalization as an Administrator</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="06d30-157">Tilpasse arbeidsområdet</span><span class="sxs-lookup"><span data-stu-id="06d30-157">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
