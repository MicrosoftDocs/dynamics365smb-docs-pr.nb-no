---
title: Opprette egendefinerte konfigurasjonspakker for selskap | Microsoft-dokumentasjon
description: "Etter hvert som virksomheten øker, kommer du sannsynligvis til å være avhengig av et sett med selskapstyper som du bruker med de fleste av kundene dine. Du kan forenkle implementeringsprosessen ved å gjøre disse typene om til selskapskonfigurasjonspakker som kan brukes på nytt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 37fe7a482b88626adff1ef16496a785399d19a8d
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="98438-104">Opprette egendefinerte konfigurasjonspakker for selskap</span><span class="sxs-lookup"><span data-stu-id="98438-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="98438-105">Etter hvert som virksomheten øker, kommer du sannsynligvis til å være avhengig av et sett med selskapstyper som du bruker med de fleste av kundene dine.</span><span class="sxs-lookup"><span data-stu-id="98438-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="98438-106">Du kan forenkle implementeringsprosessen ved å gjøre disse typene om til selskapskonfigurasjonspakker som kan brukes på nytt.</span><span class="sxs-lookup"><span data-stu-id="98438-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="98438-107">Vanligvis oppretter du en konfigurasjonspakke per funksjonsområde. Du kan for eksempel opprette en pakke for produksjonsfunksjonaliteten.</span><span class="sxs-lookup"><span data-stu-id="98438-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="98438-108">Dette gjør at du kan bruke og definere nye områder i et selskap etter hvert som du trenger dem.</span><span class="sxs-lookup"><span data-stu-id="98438-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="98438-109">En annen tilnærming ville være å opprette en pakke som inneholder tabeller som definerer oppsett, for eksempel følgende:</span><span class="sxs-lookup"><span data-stu-id="98438-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="98438-110">Aktivaoppsett</span><span class="sxs-lookup"><span data-stu-id="98438-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="98438-111">Finansoppsett</span><span class="sxs-lookup"><span data-stu-id="98438-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="98438-112">Lageroppsett</span><span class="sxs-lookup"><span data-stu-id="98438-112">Inventory Setup</span></span>  
-   <span data-ttu-id="98438-113">Produksjonsoppsett</span><span class="sxs-lookup"><span data-stu-id="98438-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="98438-114">Kjøpsoppsett</span><span class="sxs-lookup"><span data-stu-id="98438-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="98438-115">Markedsføringsoppsett</span><span class="sxs-lookup"><span data-stu-id="98438-115">Marketing Setup</span></span>  
-   <span data-ttu-id="98438-116">Serviceoppsett</span><span class="sxs-lookup"><span data-stu-id="98438-116">Service Setup</span></span>  
-   <span data-ttu-id="98438-117">Oppsett av kunde- og leverandørkonto</span><span class="sxs-lookup"><span data-stu-id="98438-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="98438-118">Lagerstyringsoppsett</span><span class="sxs-lookup"><span data-stu-id="98438-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="98438-119">Generelt bokføringsoppsett</span><span class="sxs-lookup"><span data-stu-id="98438-119">General Posting Setup</span></span>  
-   <span data-ttu-id="98438-120">Mva-bokføringsoppsett</span><span class="sxs-lookup"><span data-stu-id="98438-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="98438-121">Lagerbokføringsoppsett</span><span class="sxs-lookup"><span data-stu-id="98438-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="98438-122">Hvis du vil vise en fullstendig liste over oppsettstabeller, velger du ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angir **Oppsett** og velger deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="98438-122">To see a complete list of setup tables, Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Setup**, and then choose the related link.</span></span>  

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="98438-123">Opprette egendefinerte konfigurasjonspakker for selskap</span><span class="sxs-lookup"><span data-stu-id="98438-123">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="98438-124">Opprette en ny [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="98438-124">Create a new [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="98438-125">***IKKE MULIG Kobling til hjelp for "Opprette en ny leier"***.</span><span class="sxs-lookup"><span data-stu-id="98438-125">***NOT POSSIBLE Link to help for "Creating a New Tenant"***.</span></span>   
2.  <span data-ttu-id="98438-126">Opprett et nytt selskap for bransje- eller løsningsmalen.</span><span class="sxs-lookup"><span data-stu-id="98438-126">Create a new company for the industry or solution template.</span></span> <span data-ttu-id="98438-127">Hvis du vil ha mer informasjon, kan du se [Opprette et nytt selskap](admin-how-to-create-a-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="98438-127">For more information, see [Create a New Company](admin-how-to-create-a-new-company.md).</span></span>  
3.  <span data-ttu-id="98438-128">Konfigurer det nye selskapet etter dine behov.</span><span class="sxs-lookup"><span data-stu-id="98438-128">Setup the new company in the way you need.</span></span> <span data-ttu-id="98438-129">Fyll ut alle nødvendige oppsettstabeller.</span><span class="sxs-lookup"><span data-stu-id="98438-129">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="98438-130">Åpne det nye selskapet.</span><span class="sxs-lookup"><span data-stu-id="98438-130">Open the new company.</span></span>
5. <span data-ttu-id="98438-131">Åpne vinduet **Konfigurasjonsforslag**.</span><span class="sxs-lookup"><span data-stu-id="98438-131">Open the **Configuration Worksheet** window.</span></span>  
6.  <span data-ttu-id="98438-132">Legg til tabellene du vil overføre til et annet selskap, i forslaget.</span><span class="sxs-lookup"><span data-stu-id="98438-132">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="98438-133">Tilordne forslagslinjene til pakken.</span><span class="sxs-lookup"><span data-stu-id="98438-133">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="98438-134">Opprett et spørreskjema for de mest brukte oppsettstabellene.</span><span class="sxs-lookup"><span data-stu-id="98438-134">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="98438-135">Opprett konfigurasjonsmaler for å gjøre det enklere å opprette hoveddata, for eksempel kunder eller varer.</span><span class="sxs-lookup"><span data-stu-id="98438-135">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="98438-136">Eksporter pakken som en .rapidstart-fil.</span><span class="sxs-lookup"><span data-stu-id="98438-136">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="98438-137">Se også</span><span class="sxs-lookup"><span data-stu-id="98438-137">See Also</span></span>  
[<span data-ttu-id="98438-138">Konfigurere et selskap med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="98438-138">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="98438-139">Administrasjon</span><span class="sxs-lookup"><span data-stu-id="98438-139">Administration</span></span>](admin-setup-and-administration.md)

