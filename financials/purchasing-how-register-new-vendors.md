---
title: "Opprette et leverandørkort for å registrere en ny leverandør | Microsoft-dokumentasjon"
description: "Finn ut hvordan du oppretter et leverandørkort for å registrere en ny leverandør."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: 2db5100b933c0c94a8fae15c33c2ba24aad2fcf9
ms.contentlocale: nb-no
ms.lasthandoff: 04/16/2018

---
# <a name="register-new-vendors"></a><span data-ttu-id="aa28c-103">Registrere nye leverandører</span><span class="sxs-lookup"><span data-stu-id="aa28c-103">Register New Vendors</span></span>
<span data-ttu-id="aa28c-104">Leverandører tilbyr produktene du selger.</span><span class="sxs-lookup"><span data-stu-id="aa28c-104">Vendors provide the products that you sell.</span></span> <span data-ttu-id="aa28c-105">Hver leverandør du kjøper fra, må være registrert som et leverandørkort.</span><span class="sxs-lookup"><span data-stu-id="aa28c-105">Each vendor that you purchase from must be registered as a vendor card.</span></span>

<span data-ttu-id="aa28c-106">Før du kan registrere nye leverandører, må du definere forskjellige kjøpskoder som du kan velge fra når du fyller ut leverandørkort.</span><span class="sxs-lookup"><span data-stu-id="aa28c-106">Before you can register new vendors, you must set up various purchase codes that you can select from when you fill vendor cards.</span></span> <span data-ttu-id="aa28c-107">Når du har angitt alle nødvendige hoveddata, kan du konfigurere leverandøren ytterligere, for eksempel angi betalingsprioritet og vise en oversikt over varer som leverandøren og andre leverandører kan levere.</span><span class="sxs-lookup"><span data-stu-id="aa28c-107">When all of the required master data is created, you can perform additional configuration of the vendor, such as prioritize the vendor for payment purposes and list items that the vendor and other vendors can supply.</span></span> <span data-ttu-id="aa28c-108">En annen gruppe med oppsettsoppgaver for leverandører er å registrere avtaler om rabatter, priser og betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="aa28c-108">Another group of setup tasks for vendors is to record your agreements concerning discounts, prices, and payment methods.</span></span> <span data-ttu-id="aa28c-109">Hvis du vil ha mer informasjon, kan du se [Definere kjøp](purchasing-setup-purchasing.md).</span><span class="sxs-lookup"><span data-stu-id="aa28c-109">For more information, see [Setting Up Purchasing](purchasing-setup-purchasing.md).</span></span>

<span data-ttu-id="aa28c-110">Leverandørkort inneholder informasjon som er nødvendig for å kjøpe produkter fra leverandøren.</span><span class="sxs-lookup"><span data-stu-id="aa28c-110">Vendor cards hold the information that is required to buy products from the vendor.</span></span> <span data-ttu-id="aa28c-111">Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md) og [Registrere nye varer](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="aa28c-111">For more information, see [Record Purchases](purchasing-how-record-purchases.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="aa28c-112">Hvis det finnes leverandørmaler for ulike leverandørtyper, vises et vindu når du oppretter et nytt leverandørkort der du kan velge en passende mal.</span><span class="sxs-lookup"><span data-stu-id="aa28c-112">If vendor templates exist for different vendor types, then a window appears when you create a new vendor card from where you can select an appropriate template.</span></span> <span data-ttu-id="aa28c-113">Hvis det bare finnes én leverandørmal, brukes alltid denne malen i nye leverandørkort.</span><span class="sxs-lookup"><span data-stu-id="aa28c-113">If only one vendor template exists, then new vendor cards always use that template.</span></span>

## <a name="to-create-a-new-vendor-card"></a><span data-ttu-id="aa28c-114">Opprette et nytt leverandørkort</span><span class="sxs-lookup"><span data-stu-id="aa28c-114">To create a new vendor card</span></span>
1. <span data-ttu-id="aa28c-115">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Leverandører**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="aa28c-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="aa28c-116">I vinduet **Leverandører** velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="aa28c-116">In the **Vendors** window, Choose **New**.</span></span>

    <span data-ttu-id="aa28c-117">Hvis det finnes mer enn én leverandørmal, åpnes et vindu der du kan velge en leverandørmal.</span><span class="sxs-lookup"><span data-stu-id="aa28c-117">If more than one vendor template exists, then a window opens from which you can select a vendor template.</span></span> <span data-ttu-id="aa28c-118">I det tilfellet følger du de to neste trinnene.</span><span class="sxs-lookup"><span data-stu-id="aa28c-118">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="aa28c-119">I vinduet **Velg en mal for en ny leverandør** velger du malen som du vil bruke for det nye leverandørkortet.</span><span class="sxs-lookup"><span data-stu-id="aa28c-119">In the **Select a template for a new vendor** window, choose the template that you want to use for the new vendor card.</span></span>
4. <span data-ttu-id="aa28c-120">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa28c-120">Choose the **OK** button.</span></span> <span data-ttu-id="aa28c-121">Det åpnes et nytt leverandørkort med noen felt som er fylt ut med informasjon fra malen.</span><span class="sxs-lookup"><span data-stu-id="aa28c-121">A new vendor card opens with some fields filled with information from the template.</span></span>
5. <span data-ttu-id="aa28c-122">Fortsette med å fylle ut eller endre feltet på leverandørkortet etter behov.</span><span class="sxs-lookup"><span data-stu-id="aa28c-122">Proceed to fill or change fields on the vendor card as necessary.</span></span> [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="aa28c-123">Hvis du ikke vet fakturaadressen som skal brukes for hver eneste faktura fra en leverandør, fyller du ikke ut feltet **Betal til-levrd.nr.** på leverandørkortet.</span><span class="sxs-lookup"><span data-stu-id="aa28c-123">If you do not know the invoicing address that will be used for every invoice from a vendor, do not fill in the **Pay-to** field.</span></span> <span data-ttu-id="aa28c-124">I stedet velger du betal til-leverandørnummeret når du har definert en forespørsel, bestilling eller et fakturahode.</span><span class="sxs-lookup"><span data-stu-id="aa28c-124">Instead, choose the pay-to vendor number after you have set up a purchase quote, order, or invoice header.</span></span>

<span data-ttu-id="aa28c-125">Leverandøren er nå registrert, og leverandørkortet er klart til å brukes på kjøpsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="aa28c-125">The vendor is now registered, and the vendor card is ready to be used on purchase documents.</span></span>

<span data-ttu-id="aa28c-126">Hvis du vil bruke dette leverandørkortet som en mal når du oppretter nye leverandørkort, kan du lagre det som en leverandørmal.</span><span class="sxs-lookup"><span data-stu-id="aa28c-126">If you want to use this vendor card as a template when you create new vendor cards, you can save it as a vendor template.</span></span> <span data-ttu-id="aa28c-127">Hvis du vil ha mer informasjon, kan du se følgende avsnitt:</span><span class="sxs-lookup"><span data-stu-id="aa28c-127">For more information, see the following section.</span></span>

## <a name="to-save-the-vendor-card-as-a-template"></a><span data-ttu-id="aa28c-128">Lagre leverandørkortet som en mal</span><span class="sxs-lookup"><span data-stu-id="aa28c-128">To save the vendor card as a template</span></span>
1. <span data-ttu-id="aa28c-129">I vinduet **Leverandørkort** velger du handlingen **Lagre som mal**.</span><span class="sxs-lookup"><span data-stu-id="aa28c-129">In the **Vendor Card** window, choose the **Save as Template** action.</span></span> <span data-ttu-id="aa28c-130">**Leverandørmal**  -vinduet åpnes og viser leverandørkortet som en mal.</span><span class="sxs-lookup"><span data-stu-id="aa28c-130">The **Vendor Template** window opens showing the vendor card as a template.</span></span>
2. <span data-ttu-id="aa28c-131">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="aa28c-131">Fill in the fields as necessary.</span></span> [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="aa28c-132">Hvis du vil bruke dimensjoner i maler, velger du handlingen **Dimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="aa28c-132">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="aa28c-133">**Dimensjonsmaler**-vinduet åpnes med alle dimensjonskoder som er definert for leverandøren.</span><span class="sxs-lookup"><span data-stu-id="aa28c-133">The **Dimension Templates** window opens showing any dimension codes that are set up for the vendor.</span></span>
4. <span data-ttu-id="aa28c-134">Rediger eller angi dimensjonskoder som skal gjelde for nye leverandørkort som opprettes ved hjelp av malen.</span><span class="sxs-lookup"><span data-stu-id="aa28c-134">Edit or enter dimension codes that will apply to new vendor cards created by using the template.</span></span>
5. <span data-ttu-id="aa28c-135">Når du har fullført den nye leverandørmalen, kan du velge **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="aa28c-135">When you have completed the new vendor template, choose the **OK** button.</span></span>  
   <span data-ttu-id="aa28c-136">Leverandørmalen legges til i listen over leverandørmaler, slik at du kan bruke den til å opprette nye leverandørkort.</span><span class="sxs-lookup"><span data-stu-id="aa28c-136">The vendor template is added to the list of vendor templates, so that you can use it to create new vendor cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="aa28c-137">Se også</span><span class="sxs-lookup"><span data-stu-id="aa28c-137">See Also</span></span>
[<span data-ttu-id="aa28c-138">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="aa28c-138">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="aa28c-139">[Registrere kjøp](purchasing-how-record-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="aa28c-139">[Record Purchases](purchasing-how-record-purchases.md) </span></span>  
<span data-ttu-id="aa28c-140">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="aa28c-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

