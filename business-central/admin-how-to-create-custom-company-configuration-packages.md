---
title: Opprette egendefinerte konfigurasjonspakker for selskap | Microsoft-dokumentasjon
description: Etter hvert som virksomheten øker, kommer du sannsynligvis til å være avhengig av et sett med selskapstyper som du bruker med de fleste av kundene dine. Du kan forenkle implementeringsprosessen ved å gjøre disse typene om til selskapskonfigurasjonspakker som kan brukes på nytt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 12/07/2018
ms.author: sgroespe
ms.openlocfilehash: a51628085e640cc2e5f022272eccb89d5cec38b7
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803305"
---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="35c4c-104">Opprette egendefinerte konfigurasjonspakker for selskap</span><span class="sxs-lookup"><span data-stu-id="35c4c-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="35c4c-105">Etter hvert som virksomheten øker, kommer du sannsynligvis til å være avhengig av et sett med selskapstyper som du bruker med de fleste av kundene dine.</span><span class="sxs-lookup"><span data-stu-id="35c4c-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="35c4c-106">Du kan forenkle implementeringsprosessen ved å gjøre disse typene om til selskapskonfigurasjonspakker som kan brukes på nytt.</span><span class="sxs-lookup"><span data-stu-id="35c4c-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="35c4c-107">Vanligvis oppretter du en konfigurasjonspakke per funksjonsområde. Du kan for eksempel opprette en pakke for produksjonsfunksjonaliteten.</span><span class="sxs-lookup"><span data-stu-id="35c4c-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="35c4c-108">Dette gjør at du kan bruke og definere nye områder i et selskap etter hvert som du trenger dem.</span><span class="sxs-lookup"><span data-stu-id="35c4c-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="35c4c-109">En annen tilnærming ville være å opprette en pakke som inneholder tabeller som definerer oppsett, for eksempel følgende:</span><span class="sxs-lookup"><span data-stu-id="35c4c-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="35c4c-110">Aktivaoppsett</span><span class="sxs-lookup"><span data-stu-id="35c4c-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="35c4c-111">Finansoppsett</span><span class="sxs-lookup"><span data-stu-id="35c4c-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="35c4c-112">Lageroppsett</span><span class="sxs-lookup"><span data-stu-id="35c4c-112">Inventory Setup</span></span>  
-   <span data-ttu-id="35c4c-113">Produksjonsoppsett</span><span class="sxs-lookup"><span data-stu-id="35c4c-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="35c4c-114">Kjøpsoppsett</span><span class="sxs-lookup"><span data-stu-id="35c4c-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="35c4c-115">Markedsføringsoppsett</span><span class="sxs-lookup"><span data-stu-id="35c4c-115">Marketing Setup</span></span>  
-   <span data-ttu-id="35c4c-116">Serviceoppsett</span><span class="sxs-lookup"><span data-stu-id="35c4c-116">Service Setup</span></span>  
-   <span data-ttu-id="35c4c-117">Oppsett av kunde- og leverandørkonto</span><span class="sxs-lookup"><span data-stu-id="35c4c-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="35c4c-118">Lagerstyringsoppsett</span><span class="sxs-lookup"><span data-stu-id="35c4c-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="35c4c-119">Generelt bokføringsoppsett</span><span class="sxs-lookup"><span data-stu-id="35c4c-119">General Posting Setup</span></span>  
-   <span data-ttu-id="35c4c-120">Mva-bokføringsoppsett</span><span class="sxs-lookup"><span data-stu-id="35c4c-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="35c4c-121">Lagerbokføringsoppsett</span><span class="sxs-lookup"><span data-stu-id="35c4c-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="35c4c-122">Hvis du vil se en fullstendig liste over oppsettstabeller, velger du ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angir **Manuelt oppsett** og velger deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="35c4c-122">To see a complete list of setup tables, Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Manual Setup**, and then choose the related link.</span></span>  

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="35c4c-123">Opprette egendefinerte konfigurasjonspakker for selskap</span><span class="sxs-lookup"><span data-stu-id="35c4c-123">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="35c4c-124">Opprett et nytt selskap.</span><span class="sxs-lookup"><span data-stu-id="35c4c-124">Create a new company.</span></span> <span data-ttu-id="35c4c-125">Hvis du vil ha mer informasjon, kan du se [Opprette nye selskaper i Business Central](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="35c4c-125">For more information, see [Creating New Companies in Business Central](about-new-company.md).</span></span>  
3.  <span data-ttu-id="35c4c-126">Konfigurere det nye selskapet etter dine behov.</span><span class="sxs-lookup"><span data-stu-id="35c4c-126">Set up the new company in the way you need.</span></span> <span data-ttu-id="35c4c-127">Fyll ut alle nødvendige oppsettstabeller.</span><span class="sxs-lookup"><span data-stu-id="35c4c-127">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="35c4c-128">Åpne det nye selskapet.</span><span class="sxs-lookup"><span data-stu-id="35c4c-128">Open the new company.</span></span>
5. <span data-ttu-id="35c4c-129">Åpne siden **Konfigurasjonsforslag**.</span><span class="sxs-lookup"><span data-stu-id="35c4c-129">Open the **Configuration Worksheet** page.</span></span>  
6.  <span data-ttu-id="35c4c-130">Legg til tabellene du vil overføre til et annet selskap, i forslaget.</span><span class="sxs-lookup"><span data-stu-id="35c4c-130">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="35c4c-131">Tilordne forslagslinjene til pakken.</span><span class="sxs-lookup"><span data-stu-id="35c4c-131">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="35c4c-132">Opprett et spørreskjema for de mest brukte oppsettstabellene.</span><span class="sxs-lookup"><span data-stu-id="35c4c-132">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="35c4c-133">Opprett konfigurasjonsmaler for å gjøre det enklere å opprette hoveddata, for eksempel kunder eller varer.</span><span class="sxs-lookup"><span data-stu-id="35c4c-133">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="35c4c-134">Eksporter pakken som en .rapidstart-fil.</span><span class="sxs-lookup"><span data-stu-id="35c4c-134">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="35c4c-135">Se også</span><span class="sxs-lookup"><span data-stu-id="35c4c-135">See Also</span></span>  
[<span data-ttu-id="35c4c-136">Konfigurere et selskap med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="35c4c-136">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="35c4c-137">Administrasjon</span><span class="sxs-lookup"><span data-stu-id="35c4c-137">Administration</span></span>](admin-setup-and-administration.md)
