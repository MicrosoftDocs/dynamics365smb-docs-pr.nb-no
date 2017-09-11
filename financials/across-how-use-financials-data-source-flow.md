---
title: Koble dataene med Flow | Microsoft-dokumentasjon
description: "Du kan gjøre Financials-dataene tilgjengelige som en datakilde og angi en OData-URL-adresse til webtjenestene dine for å utvikle automatisk arbeidsflyt."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 277dda7c954380138af1ecabc02d77121f35aac7
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2017

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a><span data-ttu-id="24fe1-103">Bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] i en automatisk arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="24fe1-103">Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow</span></span>
<span data-ttu-id="24fe1-104">Du kan bruke dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del av en arbeidsflyt i Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="24fe1-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="24fe1-105">Du må ha en gyldig konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] og med Flow.</span><span class="sxs-lookup"><span data-stu-id="24fe1-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a><span data-ttu-id="24fe1-106">Legge til [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde i Flow</span><span class="sxs-lookup"><span data-stu-id="24fe1-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in Flow</span></span>
1. <span data-ttu-id="24fe1-107">I leseren, kan du gå til [flow.microsoft.com](https://flow.microsoft.com/en-us/), og deretter logge på.</span><span class="sxs-lookup"><span data-stu-id="24fe1-107">In your browser, navigate to [flow.microsoft.com](https://flow.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="24fe1-108">Velg **Mine Flow-er** fra båndet øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="24fe1-108">Choose **My Flows** from the ribbon at the top of the page.</span></span>
3. <span data-ttu-id="24fe1-109">I vinduet **Mine Flow-er** velger du **Opprett fra tom**.</span><span class="sxs-lookup"><span data-stu-id="24fe1-109">In the **My Flows** window, choose the **Create from blank** option.</span></span>
4. <span data-ttu-id="24fe1-110">Fra listen over tilgjengelige utløsere velger du en av de to [!INCLUDE[d365fin](includes/d365fin_md.md)]-utløserne tilgjengelig: *Når en oppføring opprettes* eller *Når en oppføring endres*.</span><span class="sxs-lookup"><span data-stu-id="24fe1-110">From the list of available triggers, select one of the two [!INCLUDE[d365fin](includes/d365fin_md.md)] triggers available: *When a record is created*, or *When a record is modified*.</span></span>
5. <span data-ttu-id="24fe1-111">Flow vil vise en tilkoblingsside som ber deg om informasjonen som kreves for å koble til dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data.</span><span class="sxs-lookup"><span data-stu-id="24fe1-111">Flow will display a connection page that prompts you for the information that is required to connect to your [!INCLUDE[d365fin](includes/d365fin_md.md)] data.</span></span> <span data-ttu-id="24fe1-112">Hvis du vil koble til, må du angi et navn for tilkoblingen, en OData URL-adresse, brukernavn, passord og selskapsnavn.</span><span class="sxs-lookup"><span data-stu-id="24fe1-112">To connect, you must specify a name for the connection, an OData URL, username, password, and company name.</span></span>

   <span data-ttu-id="24fe1-113">For *OData URL-adressen*, kan du kopiere OData V4 URL-adressen for web-tjenester som er oppført på siden **Web Services** i [!INCLUDE[d365fin](includes/d365fin_md.md)], som `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.</span><span class="sxs-lookup"><span data-stu-id="24fe1-113">For the *OData URL*, you can copy the OData V4 URL of any of the web services that are listed in the **Web Services** page in [!INCLUDE[d365fin](includes/d365fin_md.md)], such as `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.</span></span>  

   <span data-ttu-id="24fe1-114">For *Selskapsnavn*, bruk navnet som vises i **Navn**-feltet i vinduet **Selskapsopplysninger** i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="24fe1-114">For the *Company Name*, use the name that is shown in the **Name** field in the **Company Information** window in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="24fe1-115">Hvis [!INCLUDE[d365fin](includes/d365fin_md.md)] inneholder flere selskaper, velger du det relevante selskapsnavnet fra listen i **Selskaper**-vinduet.</span><span class="sxs-lookup"><span data-stu-id="24fe1-115">If your [!INCLUDE[d365fin](includes/d365fin_md.md)] contains multiple companies, choose the relevant company name from the list in the **Companies** window.</span></span> <span data-ttu-id="24fe1-116">I begge tilfeller må du kontrollere at navnet du angir i veiviseren for PowerApps tilsvarer teksten som vises i [!INCLUDE[d365fin](includes/d365fin_md.md)], som `My Company`.</span><span class="sxs-lookup"><span data-stu-id="24fe1-116">In both cases, make sure that the name that you specify in the PowerApps wizard matches exactly the text shown in [!INCLUDE[d365fin](includes/d365fin_md.md)], such as `My Company`.</span></span>

   <span data-ttu-id="24fe1-117">Om brukernavn og passord, kan du bruke navnet og web service hurtigtast som er angitt for kontoen i **Brukere**-vinduet i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="24fe1-117">For the username and password, use the name and web service access key that are specified for your account in the **Users** window in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="24fe1-118">Ditt brukernavn er for eksempel *ADMIN*, og web service hurtigtast som fungerer som passordet ditt er *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU =*.</span><span class="sxs-lookup"><span data-stu-id="24fe1-118">For example, your username is *ADMIN*, and the web service access key that serves as your password is *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*.</span></span> <span data-ttu-id="24fe1-119">Hvis du vil ha mer informasjon, kan du se [Administrere brukere og tillatelser](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="24fe1-119">For more information, see [How to: Manage Users and Permissions](ui-how-users-permissions.md).</span></span>
6. <span data-ttu-id="24fe1-120">Velg **Opprett**-knappen nederst på siden for å fortsette.</span><span class="sxs-lookup"><span data-stu-id="24fe1-120">Choose the **Create** button at the bottom of the page to continue.</span></span>

   <span data-ttu-id="24fe1-121">Flow vil vise en liste over tabeller som er tilgjengelige fra [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="24fe1-121">Flow will show a list of tables that are available from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="24fe1-122">Disse tabellene eller endepunktene, representerer alle web-tjenester som du har publisert fra [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="24fe1-122">These tables, or end points, represent all the web services that you have published from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

   <span data-ttu-id="24fe1-123">Alternativt, opprette en ny web service URL i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av **Opprett datasett** i siden **Web Services** ved hjelp av **Sett opp rapportering** assistert installasjonsveiledningen eller ved å velge **Rediger i Excel** i lister.</span><span class="sxs-lookup"><span data-stu-id="24fe1-123">Alternatively, create a new web service URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] by using the **Create Data Set** action in the **Web Services** page, using the **Set Up Reporting** Assisted Setup guide, or by choosing the **Edit in Excel** action in any lists.</span></span>
7. <span data-ttu-id="24fe1-124">Velg dataene du vil bruke i Flow.</span><span class="sxs-lookup"><span data-stu-id="24fe1-124">Choose the data that you want to use for in Flow.</span></span>

<span data-ttu-id="24fe1-125">Nå har du koblet til Dynamics 365-dataene og er klar til å begynne å bygge din flyt.</span><span class="sxs-lookup"><span data-stu-id="24fe1-125">At this point, you have successfully connected to your Dynamics 365 data and are ready to begin building your flow.</span></span> <span data-ttu-id="24fe1-126">Hvis du ønsker mer informasjon, se [Flow-dokumentasjonen](https://flow.microsoft.com/documentation/getting-started/).</span><span class="sxs-lookup"><span data-stu-id="24fe1-126">For more information, see the [Flow documentation](https://flow.microsoft.com/documentation/getting-started/).</span></span>

## <a name="see-also"></a><span data-ttu-id="24fe1-127">Se også</span><span class="sxs-lookup"><span data-stu-id="24fe1-127">See Also</span></span>
<span data-ttu-id="24fe1-128">[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="24fe1-128">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="24fe1-129">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="24fe1-129">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="24fe1-130">[Administrere brukere og tillatelser](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="24fe1-130">[How to: Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="24fe1-131">[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="24fe1-131">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="24fe1-132">Finans</span><span class="sxs-lookup"><span data-stu-id="24fe1-132">Finance</span></span>](finance.md)  

