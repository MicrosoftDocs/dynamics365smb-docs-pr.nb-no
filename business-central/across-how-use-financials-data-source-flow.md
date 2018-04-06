---
title: Koble dataene med Flow | Microsoft-dokumentasjon
description: "Du kan gjøre Financials-dataene tilgjengelige som en datakilde og angi en OData-URL-adresse til webtjenestene dine for å utvikle automatisk arbeidsflyt."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 23e9ebbb75d23595d568d022526e551bf590a979
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a><span data-ttu-id="afb81-103">Bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] i en automatisk arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="afb81-103">Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow</span></span>
<span data-ttu-id="afb81-104">Du kan bruke dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del av en arbeidsflyt i Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="afb81-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="afb81-105">Du må ha en gyldig konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] og med Flow.</span><span class="sxs-lookup"><span data-stu-id="afb81-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a><span data-ttu-id="afb81-106">Legge til [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde i Flow</span><span class="sxs-lookup"><span data-stu-id="afb81-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in Flow</span></span>
1. <span data-ttu-id="afb81-107">I leseren, kan du gå til [flow.microsoft.com](https://flow.microsoft.com/en-us/), og deretter logge på.</span><span class="sxs-lookup"><span data-stu-id="afb81-107">In your browser, navigate to [flow.microsoft.com](https://flow.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="afb81-108">Velg **Mine Flow-er** fra båndet øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="afb81-108">Choose **My Flows** from the ribbon at the top of the page.</span></span>
3. <span data-ttu-id="afb81-109">I vinduet **Mine Flow-er** velger du **Opprett fra tom**.</span><span class="sxs-lookup"><span data-stu-id="afb81-109">In the **My Flows** window, choose the **Create from blank** option.</span></span>
4. <span data-ttu-id="afb81-110">Fra listen over tilgjengelige utløsere velger du én av de tilgjengelige [!INCLUDE[d365fin](includes/d365fin_md.md)]-utløserne:</span><span class="sxs-lookup"><span data-stu-id="afb81-110">From the list of available triggers, select one of the [!INCLUDE[d365fin](includes/d365fin_md.md)] triggers available:</span></span>  
    <span data-ttu-id="afb81-111">*Det bes om godkjenning av en kunde*,</span><span class="sxs-lookup"><span data-stu-id="afb81-111">*When a customer approval is requested*,</span></span>  
    <span data-ttu-id="afb81-112">*Det bes om godkjenning av en finanskladd*.</span><span class="sxs-lookup"><span data-stu-id="afb81-112">*When a general journal batch approval is requested*,</span></span>  
    <span data-ttu-id="afb81-113">*Det bes om godkjenning av en finanskladdelinje*,</span><span class="sxs-lookup"><span data-stu-id="afb81-113">*When a general journal line approval is requested*,</span></span>  
    <span data-ttu-id="afb81-114">*Det bes om godkjenning av en vare*.</span><span class="sxs-lookup"><span data-stu-id="afb81-114">*When an item approval is requested*,</span></span>  
    <span data-ttu-id="afb81-115">*Det bes om godkjenning av et kjøpsdokument*,</span><span class="sxs-lookup"><span data-stu-id="afb81-115">*When a purchase document approval is requested*,</span></span>  
    <span data-ttu-id="afb81-116">*Det bes om godkjenning av et salgsdokument* eller</span><span class="sxs-lookup"><span data-stu-id="afb81-116">*When a sales document approval is requested*, or</span></span>  
    <span data-ttu-id="afb81-117">*Det bes om godkjenning av en leverandør*.</span><span class="sxs-lookup"><span data-stu-id="afb81-117">*When a vendor aproval is requested*.</span></span>
5. <span data-ttu-id="afb81-118">Flow ber deg om å velge et annet selskap i din [!INCLUDE[d365fin](includes/d365fin_md.md)]-leier.</span><span class="sxs-lookup"><span data-stu-id="afb81-118">Flow will prompt you to select a company within your [!INCLUDE[d365fin](includes/d365fin_md.md)] tenant.</span></span> <span data-ttu-id="afb81-119">Siden hvert trinn i Flow er uavhengig av neste, kan det hende at må definere selskapet flere ganger når du bruker en [!INCLUDE[d365fin](includes/d365fin_md.md)]-mal.</span><span class="sxs-lookup"><span data-stu-id="afb81-119">Because each step in the Flow is independent of the next, you may be required to define the company multiple times when using a [!INCLUDE[d365fin](includes/d365fin_md.md)] template.</span></span>

<span data-ttu-id="afb81-120">Nå har du koblet til Business Central-dataene og er klar til å begynne å bygge din flyt.</span><span class="sxs-lookup"><span data-stu-id="afb81-120">At this point, you have successfully connected to your Business Central data and are ready to begin building your flow.</span></span> <span data-ttu-id="afb81-121">Hvis du ønsker mer informasjon, se [Flow-dokumentasjonen](https://flow.microsoft.com/documentation/getting-started/).</span><span class="sxs-lookup"><span data-stu-id="afb81-121">For more information, see the [Flow documentation](https://flow.microsoft.com/documentation/getting-started/).</span></span>

<span data-ttu-id="afb81-122">Hvis du vil feilsøke Microsoft Flow, kan du se [Feilsøke integrering med Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="afb81-122">For troubleshooting your Microsoft Flow, see [Troubleshooting Integration with Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="afb81-123">Se også</span><span class="sxs-lookup"><span data-stu-id="afb81-123">See Also</span></span>
<span data-ttu-id="afb81-124">[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="afb81-124">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="afb81-125">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="afb81-125">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="afb81-126">[Administrere brukere og tillatelser](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="afb81-126">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="afb81-127">[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="afb81-127">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="afb81-128">Finans</span><span class="sxs-lookup"><span data-stu-id="afb81-128">Finance</span></span>](finance.md)  

