---
title: "Opprette et kundekort for å registrere nye kunder | Microsoft-dokumentasjon"
description: "Beskriver hvordan du oppretter et kundekort for å registrere informasjon om hver nye kunde eller klient du selger til."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ea9b4a6310df319df06d02c53b9d6156caaee24f
ms.openlocfilehash: 6ca938a5bcd0fd160c98358d89740e4dfd756e79
ms.contentlocale: nb-no
ms.lasthandoff: 03/28/2018

---
# <a name="register-new-customers"></a><span data-ttu-id="1ad9e-103">Registrere nye kunder</span><span class="sxs-lookup"><span data-stu-id="1ad9e-103">Register New Customers</span></span>
<span data-ttu-id="1ad9e-104">Kunder er kilden til dine inntekter.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-104">Customers are the source of your income.</span></span> <span data-ttu-id="1ad9e-105">Du må registrere gver kunde du selger til, som et kundekort.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-105">You must register each customer you sell to as a customer card.</span></span> <span data-ttu-id="1ad9e-106">Kundekort inneholder informasjonen som er nødvendig for å selge produkter til kunden.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-106">Customer cards hold the information that is required to sell products to the customer.</span></span> <span data-ttu-id="1ad9e-107">Hvis du vil ha mer informasjon, kan du se [Fakturere salg](sales-how-invoice-sales.md) og [Registrere nye varer](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="1ad9e-107">For more information, see [Invoice Sales](sales-how-invoice-sales.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>  

<span data-ttu-id="1ad9e-108">Før du kan registrere nye kunder, må du definere forskjellige salgskoder som du kan velge fra når du fyller ut kundekort.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-108">Before you can register new customers, you must set up various sales codes that you can select from when you fill in customer cards.</span></span> <span data-ttu-id="1ad9e-109">Hvis du vil ha mer informasjon, kan du se [Sette opp salg](sales-setup-sales.md).</span><span class="sxs-lookup"><span data-stu-id="1ad9e-109">For more information, see [Setting Up Sales](sales-setup-sales.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="1ad9e-110">Hvis det finnes kundemaler for ulike kundetyper, vises et vindu når du oppretter et nytt kundekort der du kan velge en passende mal.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-110">If customer templates exist for different customer types, then a window appears when you create a new customer card from where you can select an appropriate template.</span></span> <span data-ttu-id="1ad9e-111">Hvis det bare finnes én kundemal, brukes alltid denne malen i nye kundekort.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-111">If only one customer template exists, then new customer cards always use that template.</span></span>

## <a name="to-create-a-new-customer-card"></a><span data-ttu-id="1ad9e-112">Opprette et nytt kundekort</span><span class="sxs-lookup"><span data-stu-id="1ad9e-112">To create a new customer card</span></span>
1. <span data-ttu-id="1ad9e-113">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kunder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1ad9e-114">I vinduet **Kunder** velger du handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-114">In the **Customers** window, choose the **New** action.</span></span>

    <span data-ttu-id="1ad9e-115">Hvis det bare finnes én kundemal, åpnes et nytt kundekort med noen felt som er fylt ut med informasjon fra malen.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-115">If only one customer template exists, then a new customer card opens with some fields filled with information from the template.</span></span>

    <span data-ttu-id="1ad9e-116">Hvis det finnes mer enn én kundemal, åpnes et vindu der du kan velge en kundemal.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-116">If more than one customer template exists, then a window opens from which you can select a customer template.</span></span> <span data-ttu-id="1ad9e-117">I det tilfellet følger du de to neste trinnene.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-117">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="1ad9e-118">I vinduet **Velg en mal for en ny kunde** velger du malen som du vil bruke for det nye kundekortet.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-118">In the **Select a template for a new customer** window, choose the template that you want to use for the new customer card.</span></span>
4. <span data-ttu-id="1ad9e-119">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-119">Choose the **OK** button.</span></span> <span data-ttu-id="1ad9e-120">Det åpnes et nytt kundekort med noen felt som er fylt ut med informasjon fra malen.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-120">A new customer card opens with some fields filled with information from the template.</span></span>  
5. <span data-ttu-id="1ad9e-121">Fortsette med å fylle ut eller endre feltet på kundekortet etter behov.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-121">Proceed to fill or change fields on the customer card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="1ad9e-122">I hurtigfanen **Salgspriser** kan du vise spesialpriser eller rabatter som skal gis til kunden hvis bestemte kriterier oppfylles, for eksempel vare, minimumsordreantall eller sluttdato.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-122">On the **Sales Prices** FastTab, you can view special prices or discounts that you grant for the customer if certain criteria are met, such as item, minimum order quantity, or ending date.</span></span> <span data-ttu-id="1ad9e-123">Hver rad representerer en spesialpris eller linjerabatt.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-123">Each row represents a special price or line discount.</span></span> <span data-ttu-id="1ad9e-124">Hver kolonne representerer et vilkår som må brukes for å garantere spesialprisen du angir i feltet **Enhetspris**, eller linjerabatten du angir i feltet **Linjerabatt-%**.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-124">Each column represents a criterion that must apply to warrant the special price that you enter in the **Unit Price** field, or the line discount that you enter in the **Line Discount %** field.</span></span> <span data-ttu-id="1ad9e-125">Hvis du vil ha mer informasjon, kan du se [Registrere avtaler om salgspris, rabatt og betaling](sales-how-record-sales-price-discount-payment-agreements.md).</span><span class="sxs-lookup"><span data-stu-id="1ad9e-125">For more information, see [Record Sales Price, Discount, and Payment Agreements](sales-how-record-sales-price-discount-payment-agreements.md).</span></span>

<span data-ttu-id="1ad9e-126">Kunden er nå registrert, og kundekortet er klart til å brukes på salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-126">The customer is now registered, and the customer card is ready to be used on sales documents.</span></span>

<span data-ttu-id="1ad9e-127">Hvis du vil bruke dette kundekortet som en mal når du oppretter nye kundekort, kan du lagre det som en mal.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-127">If you want to use this customer card as a template when you create new customer cards, you can save it as a template.</span></span> <span data-ttu-id="1ad9e-128">Hvis du vil ha mer informasjon, kan du se følgende avsnitt:</span><span class="sxs-lookup"><span data-stu-id="1ad9e-128">For more information, see the following section.</span></span>

## <a name="to-save-the-customer-card-as-a-template"></a><span data-ttu-id="1ad9e-129">Lagre kundekortet som en mal</span><span class="sxs-lookup"><span data-stu-id="1ad9e-129">To save the customer card as a template</span></span>
1. <span data-ttu-id="1ad9e-130">I vinduet **Kundekort** velger du handlingen **Lagre som mal**.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-130">In the **Customer Card** window, choose the **Save as Template** action.</span></span> <span data-ttu-id="1ad9e-131">**Kundemal**  -vinduet åpnes og viser kundekortet som en mal.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-131">The **Customer Template** window opens showing the customer card as a template.</span></span>
2. <span data-ttu-id="1ad9e-132">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-132">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="1ad9e-133">Hvis du vil bruke dimensjoner i maler, velger du handlingen **Dimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-133">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="1ad9e-134">**Dimensjonsmaler**-vinduet åpnes med alle dimensjonskoder som er definert for kunden.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-134">The **Dimension Templates** window opens showing any dimension codes that are set up for the customer.</span></span>
4. <span data-ttu-id="1ad9e-135">Rediger eller angi dimensjonskoder som skal gjelde for nye kundekort som opprettes ved hjelp av malen.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-135">Edit or enter dimension codes that will apply to new customer cards created by using the template.</span></span>  
5. <span data-ttu-id="1ad9e-136">Når du har fullført den nye kundemalen, kan du velge **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-136">When you have completed the new customer template, choose the **OK** button.</span></span>

<span data-ttu-id="1ad9e-137">Kundemalen legges til i listen over kundemaler, slik at du kan bruke den til å opprette nye kundekort.</span><span class="sxs-lookup"><span data-stu-id="1ad9e-137">The customer template is added to the list of customer templates, so that you can use it to create new customer cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="1ad9e-138">Se også</span><span class="sxs-lookup"><span data-stu-id="1ad9e-138">See Also</span></span>
[<span data-ttu-id="1ad9e-139">Opprette nummerserier</span><span class="sxs-lookup"><span data-stu-id="1ad9e-139">Create Number Series</span></span>](ui-create-number-series.md)  
<span data-ttu-id="1ad9e-140">[Salg](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="1ad9e-140">[Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="1ad9e-141">[Sette opp salg](sales-setup-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="1ad9e-141">[Setting Up Sales](sales-setup-sales.md)  </span></span>  
<span data-ttu-id="1ad9e-142">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1ad9e-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

