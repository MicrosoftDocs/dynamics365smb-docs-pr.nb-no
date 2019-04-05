---
title: Opprette et kundekort for å registrere nye kunder | Microsoft-dokumentasjon
description: Beskriver hvordan du oppretter et kundekort for å registrere informasjon om hver nye kunde eller klient du selger til.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 06fe745bca016a776d7a1865141110ec82b1d7d7
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802446"
---
# <a name="register-new-customers"></a><span data-ttu-id="f5a05-103">Registrere nye kunder</span><span class="sxs-lookup"><span data-stu-id="f5a05-103">Register New Customers</span></span>
<span data-ttu-id="f5a05-104">Kunder er kilden til dine inntekter.</span><span class="sxs-lookup"><span data-stu-id="f5a05-104">Customers are the source of your income.</span></span> <span data-ttu-id="f5a05-105">Du må registrere gver kunde du selger til, som et kundekort.</span><span class="sxs-lookup"><span data-stu-id="f5a05-105">You must register each customer you sell to as a customer card.</span></span> <span data-ttu-id="f5a05-106">Kundekort inneholder informasjonen som er nødvendig for å selge produkter til kunden.</span><span class="sxs-lookup"><span data-stu-id="f5a05-106">Customer cards hold the information that is required to sell products to the customer.</span></span> <span data-ttu-id="f5a05-107">Hvis du vil ha mer informasjon, kan du se [Fakturere salg](sales-how-invoice-sales.md) og [Registrere nye varer](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="f5a05-107">For more information, see [Invoice Sales](sales-how-invoice-sales.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>  

<span data-ttu-id="f5a05-108">Før du kan registrere nye kunder, må du definere forskjellige salgskoder som du kan velge fra når du fyller ut kundekort.</span><span class="sxs-lookup"><span data-stu-id="f5a05-108">Before you can register new customers, you must set up various sales codes that you can select from when you fill in customer cards.</span></span> <span data-ttu-id="f5a05-109">Hvis du vil ha mer informasjon, kan du se [Sette opp salg](sales-setup-sales.md).</span><span class="sxs-lookup"><span data-stu-id="f5a05-109">For more information, see [Setting Up Sales](sales-setup-sales.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="f5a05-110">Hvis det finnes kundemaler for ulike kundetyper, vises en side når du oppretter et nytt kundekort der du kan velge en passende mal.</span><span class="sxs-lookup"><span data-stu-id="f5a05-110">If customer templates exist for different customer types, then a page appears when you create a new customer card from where you can select an appropriate template.</span></span> <span data-ttu-id="f5a05-111">Hvis det bare finnes én kundemal, brukes alltid denne malen i nye kundekort.</span><span class="sxs-lookup"><span data-stu-id="f5a05-111">If only one customer template exists, then new customer cards always use that template.</span></span>

## <a name="to-create-a-new-customer-card"></a><span data-ttu-id="f5a05-112">Opprette et nytt kundekort</span><span class="sxs-lookup"><span data-stu-id="f5a05-112">To create a new customer card</span></span>
1. <span data-ttu-id="f5a05-113">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="f5a05-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f5a05-114">På siden **Kunder** velger du handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f5a05-114">On the **Customers** page, choose the **New** action.</span></span>

    <span data-ttu-id="f5a05-115">Hvis det bare finnes én kundemal, åpnes et nytt kundekort med noen felt som er fylt ut med informasjon fra malen.</span><span class="sxs-lookup"><span data-stu-id="f5a05-115">If only one customer template exists, then a new customer card opens with some fields filled with information from the template.</span></span>

    <span data-ttu-id="f5a05-116">Hvis det finnes mer enn én kundemal, åpnes en side der du kan velge en kundemal.</span><span class="sxs-lookup"><span data-stu-id="f5a05-116">If more than one customer template exists, then a page opens from which you can select a customer template.</span></span> <span data-ttu-id="f5a05-117">I det tilfellet følger du de to neste trinnene.</span><span class="sxs-lookup"><span data-stu-id="f5a05-117">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="f5a05-118">På siden **Velg en mal for en ny kunde** velger du malen som du vil bruke for det nye kundekortet.</span><span class="sxs-lookup"><span data-stu-id="f5a05-118">On the **Select a template for a new customer** page, choose the template that you want to use for the new customer card.</span></span>
4. <span data-ttu-id="f5a05-119">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f5a05-119">Choose the **OK** button.</span></span> <span data-ttu-id="f5a05-120">Det åpnes et nytt kundekort med noen felt som er fylt ut med informasjon fra malen.</span><span class="sxs-lookup"><span data-stu-id="f5a05-120">A new customer card opens with some fields filled with information from the template.</span></span>  
5. <span data-ttu-id="f5a05-121">Fortsette med å fylle ut eller endre feltet på kundekortet etter behov.</span><span class="sxs-lookup"><span data-stu-id="f5a05-121">Proceed to fill or change fields on the customer card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="f5a05-122">I hurtigfanen **Salgspriser** kan du vise spesialpriser eller rabatter som skal gis til kunden hvis bestemte kriterier oppfylles, for eksempel vare, minimumsordreantall eller sluttdato.</span><span class="sxs-lookup"><span data-stu-id="f5a05-122">On the **Sales Prices** FastTab, you can view special prices or discounts that you grant for the customer if certain criteria are met, such as item, minimum order quantity, or ending date.</span></span> <span data-ttu-id="f5a05-123">Hver rad representerer en spesialpris eller linjerabatt.</span><span class="sxs-lookup"><span data-stu-id="f5a05-123">Each row represents a special price or line discount.</span></span> <span data-ttu-id="f5a05-124">Hver kolonne representerer et vilkår som må brukes for å garantere spesialprisen du angir i feltet **Enhetspris**, eller linjerabatten du angir i feltet **Linjerabatt-%**.</span><span class="sxs-lookup"><span data-stu-id="f5a05-124">Each column represents a criterion that must apply to warrant the special price that you enter in the **Unit Price** field, or the line discount that you enter in the **Line Discount %** field.</span></span> <span data-ttu-id="f5a05-125">Hvis du vil ha mer informasjon, kan du se [Registrere avtaler om salgspris, rabatt og betaling](sales-how-record-sales-price-discount-payment-agreements.md).</span><span class="sxs-lookup"><span data-stu-id="f5a05-125">For more information, see [Record Sales Price, Discount, and Payment Agreements](sales-how-record-sales-price-discount-payment-agreements.md).</span></span>

<span data-ttu-id="f5a05-126">Kunden er nå registrert, og kundekortet er klart til å brukes på salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="f5a05-126">The customer is now registered, and the customer card is ready to be used on sales documents.</span></span>

<span data-ttu-id="f5a05-127">Hvis du vil bruke dette kundekortet som en mal når du oppretter nye kundekort, kan du lagre det som en mal.</span><span class="sxs-lookup"><span data-stu-id="f5a05-127">If you want to use this customer card as a template when you create new customer cards, you can save it as a template.</span></span> <span data-ttu-id="f5a05-128">Hvis du vil ha mer informasjon, kan du se følgende avsnitt:</span><span class="sxs-lookup"><span data-stu-id="f5a05-128">For more information, see the following section.</span></span>

## <a name="to-save-the-customer-card-as-a-template"></a><span data-ttu-id="f5a05-129">Lagre kundekortet som en mal</span><span class="sxs-lookup"><span data-stu-id="f5a05-129">To save the customer card as a template</span></span>
1. <span data-ttu-id="f5a05-130">På siden **Kundekort** velger du handlingen **Lagre som mal**.</span><span class="sxs-lookup"><span data-stu-id="f5a05-130">On the **Customer Card** page, choose the **Save as Template** action.</span></span> <span data-ttu-id="f5a05-131">**Kundemal**-siden åpnes og viser kundekortet som en mal.</span><span class="sxs-lookup"><span data-stu-id="f5a05-131">The **Customer Template** page opens showing the customer card as a template.</span></span>
2. <span data-ttu-id="f5a05-132">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="f5a05-132">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="f5a05-133">Hvis du vil bruke dimensjoner i maler, velger du handlingen **Dimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="f5a05-133">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="f5a05-134">**Dimensjonsmaler**-siden åpnes med alle dimensjonskoder som er definert for kunden.</span><span class="sxs-lookup"><span data-stu-id="f5a05-134">The **Dimension Templates** page opens showing any dimension codes that are set up for the customer.</span></span>
4. <span data-ttu-id="f5a05-135">Rediger eller angi dimensjonskoder som skal gjelde for nye kundekort som opprettes ved hjelp av malen.</span><span class="sxs-lookup"><span data-stu-id="f5a05-135">Edit or enter dimension codes that will apply to new customer cards created by using the template.</span></span>  
5. <span data-ttu-id="f5a05-136">Når du har fullført den nye kundemalen, kan du velge **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="f5a05-136">When you have completed the new customer template, choose the **OK** button.</span></span>

<span data-ttu-id="f5a05-137">Kundemalen legges til i listen over kundemaler, slik at du kan bruke den til å opprette nye kundekort.</span><span class="sxs-lookup"><span data-stu-id="f5a05-137">The customer template is added to the list of customer templates, so that you can use it to create new customer cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="f5a05-138">Se også</span><span class="sxs-lookup"><span data-stu-id="f5a05-138">See Also</span></span>
[<span data-ttu-id="f5a05-139">Opprette nummerserier</span><span class="sxs-lookup"><span data-stu-id="f5a05-139">Create Number Series</span></span>](ui-create-number-series.md)  
<span data-ttu-id="f5a05-140">[Salg](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="f5a05-140">[Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="f5a05-141">[Sette opp salg](sales-setup-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="f5a05-141">[Setting Up Sales](sales-setup-sales.md)  </span></span>  
<span data-ttu-id="f5a05-142">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f5a05-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
