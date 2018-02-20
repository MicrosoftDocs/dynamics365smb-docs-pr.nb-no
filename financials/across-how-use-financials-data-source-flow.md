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
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ef4d841723b6bb0af37695a8c3ed1d805319be78
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a><span data-ttu-id="1983b-103">Bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] i en automatisk arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="1983b-103">Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow</span></span>
<span data-ttu-id="1983b-104">Du kan bruke dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del av en arbeidsflyt i Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="1983b-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="1983b-105">Du må ha en gyldig konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] og med Flow.</span><span class="sxs-lookup"><span data-stu-id="1983b-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a><span data-ttu-id="1983b-106">Legge til [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde i Flow</span><span class="sxs-lookup"><span data-stu-id="1983b-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in Flow</span></span>
1. <span data-ttu-id="1983b-107">I leseren, kan du gå til [flow.microsoft.com](https://flow.microsoft.com/en-us/), og deretter logge på.</span><span class="sxs-lookup"><span data-stu-id="1983b-107">In your browser, navigate to [flow.microsoft.com](https://flow.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="1983b-108">Velg **Mine Flow-er** fra båndet øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="1983b-108">Choose **My Flows** from the ribbon at the top of the page.</span></span>
3. <span data-ttu-id="1983b-109">I vinduet **Mine Flow-er** velger du **Opprett fra tom**.</span><span class="sxs-lookup"><span data-stu-id="1983b-109">In the **My Flows** window, choose the **Create from blank** option.</span></span>
4. <span data-ttu-id="1983b-110">Fra listen over tilgjengelige utløsere velger du én av de tilgjengelige [!INCLUDE[d365fin](includes/d365fin_md.md)]-utløserne:</span><span class="sxs-lookup"><span data-stu-id="1983b-110">From the list of available triggers, select one of the [!INCLUDE[d365fin](includes/d365fin_md.md)] triggers available:</span></span>  
    <span data-ttu-id="1983b-111">*Når en post opprettes*,</span><span class="sxs-lookup"><span data-stu-id="1983b-111">*When a record is created*,</span></span>  
    <span data-ttu-id="1983b-112">*Når en post slettes*,</span><span class="sxs-lookup"><span data-stu-id="1983b-112">*When a record is deleted*,</span></span>  
    <span data-ttu-id="1983b-113">*Når en post endres*,</span><span class="sxs-lookup"><span data-stu-id="1983b-113">*When a record is modified*,</span></span>  
    <span data-ttu-id="1983b-114">*Det bes om godkjenning av en kunde*,</span><span class="sxs-lookup"><span data-stu-id="1983b-114">*When a customer approval is requested*,</span></span>  
    <span data-ttu-id="1983b-115">*Det bes om godkjenning av en finanskladd*.</span><span class="sxs-lookup"><span data-stu-id="1983b-115">*When a general journal batch approval is requested*,</span></span>  
    <span data-ttu-id="1983b-116">*Det bes om godkjenning av en finanskladdelinje*,</span><span class="sxs-lookup"><span data-stu-id="1983b-116">*When a general journal line approval is requested*,</span></span>  
    <span data-ttu-id="1983b-117">*Det bes om godkjenning av en vare*.</span><span class="sxs-lookup"><span data-stu-id="1983b-117">*When an item approval is requested*,</span></span>  
    <span data-ttu-id="1983b-118">*Det bes om godkjenning av et kjøpsdokument*,</span><span class="sxs-lookup"><span data-stu-id="1983b-118">*When a purchase document approval is requested*,</span></span>  
    <span data-ttu-id="1983b-119">*Det bes om godkjenning av et salgsdokument* eller</span><span class="sxs-lookup"><span data-stu-id="1983b-119">*When a sales document approval is requested*, or</span></span>  
    <span data-ttu-id="1983b-120">*Det bes om godkjenning av en leverandør*.</span><span class="sxs-lookup"><span data-stu-id="1983b-120">*When a vendor aproval is requested*.</span></span>
5. <span data-ttu-id="1983b-121">Flow vil be deg om informasjonen som kreves for å koble til [!INCLUDE[d365fin](includes/d365fin_md.md)]-dataene dine.</span><span class="sxs-lookup"><span data-stu-id="1983b-121">Flow will prompt you for the information that is required to connect to your [!INCLUDE[d365fin](includes/d365fin_md.md)] data.</span></span> <span data-ttu-id="1983b-122">Hvis du har valgt én av følgende utløsere: *Når en post opprettes*, *Når en post endres* eller *Når en post slettes*, må du velge en selskapsnavnet og tabellnavn.</span><span class="sxs-lookup"><span data-stu-id="1983b-122">If you selected one of the following triggers: *When a record is created*, *When a record is modified*, or *When a record is deleted*, you must select a company name and table name.</span></span> <span data-ttu-id="1983b-123">For alle andre utløsere kreves bare selskapsnavnet for å koble til.</span><span class="sxs-lookup"><span data-stu-id="1983b-123">With any other trigger, only the company name is required to connect.</span></span>

   <span data-ttu-id="1983b-124">Flow vil vise en liste over selskaper og tabeller som er tilgjengelige fra [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="1983b-124">Flow will show a list of companies and tables that are available from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="1983b-125">Disse tabellene eller endepunktene, representerer alle web-tjenester som du har publisert fra [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="1983b-125">These tables, or end points, represent all the web services that you have published from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

   <span data-ttu-id="1983b-126">Alternativt, opprette en ny web service URL i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av **Opprett datasett** i siden **Web Services** ved hjelp av **Sett opp rapportering** assistert installasjonsveiledningen eller ved å velge **Rediger i Excel** i lister.</span><span class="sxs-lookup"><span data-stu-id="1983b-126">Alternatively, create a new web service URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] by using the **Create Data Set** action in the **Web Services** page, using the **Set Up Reporting** Assisted Setup guide, or by choosing the **Edit in Excel** action in any lists.</span></span>

<span data-ttu-id="1983b-127">Nå har du koblet til Finance and Operations, Business edition-dataene og er klar til å begynne å bygge flyten.</span><span class="sxs-lookup"><span data-stu-id="1983b-127">At this point, you have successfully connected to your Finance and Operations, Business edition data and are ready to begin building your flow.</span></span> <span data-ttu-id="1983b-128">Hvis du ønsker mer informasjon, se [Flow-dokumentasjonen](https://flow.microsoft.com/documentation/getting-started/).</span><span class="sxs-lookup"><span data-stu-id="1983b-128">For more information, see the [Flow documentation](https://flow.microsoft.com/documentation/getting-started/).</span></span>

<span data-ttu-id="1983b-129">Hvis du vil feilsøke Microsoft Flow, kan du se [Feilsøke integrering med Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="1983b-129">For troubleshooting your Microsoft Flow, see [Troubleshooting Integration with Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="1983b-130">Se også</span><span class="sxs-lookup"><span data-stu-id="1983b-130">See Also</span></span>
<span data-ttu-id="1983b-131">[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="1983b-131">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="1983b-132">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="1983b-132">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="1983b-133">[Administrere brukere og tillatelser](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="1983b-133">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="1983b-134">[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="1983b-134">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="1983b-135">Finans</span><span class="sxs-lookup"><span data-stu-id="1983b-135">Finance</span></span>](finance.md)  

