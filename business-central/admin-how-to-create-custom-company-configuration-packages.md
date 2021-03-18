---
title: Opprette egendefinerte konfigurasjonspakker for selskap | Microsoft-dokumentasjon
description: Etter hvert som virksomheten øker, kommer du sannsynligvis til å være avhengig av et sett med selskapstyper som du bruker med de fleste av kundene dine. Du kan forenkle implementeringsprosessen ved å gjøre disse typene om til selskapskonfigurasjonspakker som kan brukes på nytt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a1b1bfd5dd685eb57e291842d7b6d2e3691482fc
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378301"
---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="ff54a-104">Opprette egendefinerte konfigurasjonspakker for selskap</span><span class="sxs-lookup"><span data-stu-id="ff54a-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="ff54a-105">Etter hvert som virksomheten øker, kommer du sannsynligvis til å være avhengig av et sett med selskapstyper som du bruker med de fleste av kundene dine.</span><span class="sxs-lookup"><span data-stu-id="ff54a-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="ff54a-106">Du kan forenkle implementeringsprosessen ved å gjøre disse typene om til selskapskonfigurasjonspakker som kan brukes på nytt.</span><span class="sxs-lookup"><span data-stu-id="ff54a-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="ff54a-107">Vanligvis oppretter du en konfigurasjonspakke per funksjonsområde. Du kan for eksempel opprette en pakke for produksjonsfunksjonaliteten.</span><span class="sxs-lookup"><span data-stu-id="ff54a-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="ff54a-108">Dette gjør at du kan bruke og definere nye områder i et selskap etter hvert som du trenger dem.</span><span class="sxs-lookup"><span data-stu-id="ff54a-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="ff54a-109">En annen tilnærming ville være å opprette en pakke som inneholder tabeller som definerer oppsett, for eksempel følgende:</span><span class="sxs-lookup"><span data-stu-id="ff54a-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="ff54a-110">Aktivaoppsett</span><span class="sxs-lookup"><span data-stu-id="ff54a-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="ff54a-111">Finansoppsett</span><span class="sxs-lookup"><span data-stu-id="ff54a-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="ff54a-112">Lageroppsett</span><span class="sxs-lookup"><span data-stu-id="ff54a-112">Inventory Setup</span></span>  
-   <span data-ttu-id="ff54a-113">Produksjonsoppsett</span><span class="sxs-lookup"><span data-stu-id="ff54a-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="ff54a-114">Kjøpsoppsett</span><span class="sxs-lookup"><span data-stu-id="ff54a-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="ff54a-115">Markedsføringsoppsett</span><span class="sxs-lookup"><span data-stu-id="ff54a-115">Marketing Setup</span></span>  
-   <span data-ttu-id="ff54a-116">Serviceoppsett</span><span class="sxs-lookup"><span data-stu-id="ff54a-116">Service Setup</span></span>  
-   <span data-ttu-id="ff54a-117">Oppsett av kunde- og leverandørkonto</span><span class="sxs-lookup"><span data-stu-id="ff54a-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="ff54a-118">Lagerstyringsoppsett</span><span class="sxs-lookup"><span data-stu-id="ff54a-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="ff54a-119">Generelt bokføringsoppsett</span><span class="sxs-lookup"><span data-stu-id="ff54a-119">General Posting Setup</span></span>  
-   <span data-ttu-id="ff54a-120">Mva-bokføringsoppsett</span><span class="sxs-lookup"><span data-stu-id="ff54a-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="ff54a-121">Lagerbokføringsoppsett</span><span class="sxs-lookup"><span data-stu-id="ff54a-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="ff54a-122">Hvis du vil se en fullstendig liste over oppsettstabeller, velger du ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angir **Manuelt oppsett** og velger deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="ff54a-122">To see a complete list of setup tables, Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Manual Setup**, and then choose the related link.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="ff54a-123">Vær forsiktig hvis du velger tabeller eller felt som har samme temporale navn, men som skilles med spesialtegn, for eksempel %, &, <, >, ( og ).</span><span class="sxs-lookup"><span data-stu-id="ff54a-123">Use caution if you choose tables or fields that have the same temporal name but are differentiated by special characters, such as %, &, <, >, (, and ).</span></span> <span data-ttu-id="ff54a-124">Tabellen XYZ kan for eksempel inneholde feltene "Felt 1" og "Felt 1%".</span><span class="sxs-lookup"><span data-stu-id="ff54a-124">For example, table "XYZ" might contain the "Field 1" and "Field 1%" fields.</span></span>
>
> <span data-ttu-id="ff54a-125">XML-prosessoren godtar bare noen spesialtegn, og vil fjerne tegn som ikke godtas.</span><span class="sxs-lookup"><span data-stu-id="ff54a-125">The XML processor accepts only some special characters, and will remove those it does not.</span></span> <span data-ttu-id="ff54a-126">Hvis du fjerner et spesialtegn, for eksempel %-tegnet i "Felt 1%", vil det føre til to eller flere tabeller eller felt får samme navn, og det vil oppstå en feil når du eksporterer eller importerer en konfigurasjonspakke.</span><span class="sxs-lookup"><span data-stu-id="ff54a-126">If removing a special character, such as the % sign in "Field 1%," results in two or more tables or fields with the same name an error will occur when you export or import a configuration package.</span></span>

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="ff54a-127">Opprette egendefinerte konfigurasjonspakker for selskap</span><span class="sxs-lookup"><span data-stu-id="ff54a-127">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="ff54a-128">Opprett et nytt selskap.</span><span class="sxs-lookup"><span data-stu-id="ff54a-128">Create a new company.</span></span> <span data-ttu-id="ff54a-129">Hvis du vil ha mer informasjon, kan du se [Opprette nye selskaper i Business Central](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="ff54a-129">For more information, see [Creating New Companies in Business Central](about-new-company.md).</span></span>  
3.  <span data-ttu-id="ff54a-130">Konfigurere det nye selskapet etter dine behov.</span><span class="sxs-lookup"><span data-stu-id="ff54a-130">Set up the new company in the way you need.</span></span> <span data-ttu-id="ff54a-131">Fyll ut alle nødvendige oppsettstabeller.</span><span class="sxs-lookup"><span data-stu-id="ff54a-131">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="ff54a-132">Åpne det nye selskapet.</span><span class="sxs-lookup"><span data-stu-id="ff54a-132">Open the new company.</span></span>
5. <span data-ttu-id="ff54a-133">Åpne siden **Konfigurasjonsforslag**.</span><span class="sxs-lookup"><span data-stu-id="ff54a-133">Open the **Configuration Worksheet** page.</span></span>  
6.  <span data-ttu-id="ff54a-134">Legg til tabellene du vil overføre til et annet selskap, i forslaget.</span><span class="sxs-lookup"><span data-stu-id="ff54a-134">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="ff54a-135">Tilordne forslagslinjene til pakken.</span><span class="sxs-lookup"><span data-stu-id="ff54a-135">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="ff54a-136">Opprett et spørreskjema for de mest brukte oppsettstabellene.</span><span class="sxs-lookup"><span data-stu-id="ff54a-136">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="ff54a-137">Opprett konfigurasjonsmaler for å gjøre det enklere å opprette hoveddata, for eksempel kunder eller varer.</span><span class="sxs-lookup"><span data-stu-id="ff54a-137">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="ff54a-138">Eksporter pakken som en .rapidstart-fil.</span><span class="sxs-lookup"><span data-stu-id="ff54a-138">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ff54a-139">Se også</span><span class="sxs-lookup"><span data-stu-id="ff54a-139">See Also</span></span>  
[<span data-ttu-id="ff54a-140">Konfigurere et selskap med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="ff54a-140">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="ff54a-141">Administrasjon</span><span class="sxs-lookup"><span data-stu-id="ff54a-141">Administration</span></span>](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]