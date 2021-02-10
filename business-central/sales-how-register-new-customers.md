---
title: Opprette et kundekort for å registrere nye kunder | Microsoft-dokumentasjon
description: Beskriver hvordan du oppretter et kundekort for å registrere informasjon om hver nye kunde eller klient du selger til.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 86527387653d198bc8cf6f7817058b5ff551e1d0
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748322"
---
# <a name="register-new-customers"></a><span data-ttu-id="52344-103">Registrere nye kunder</span><span class="sxs-lookup"><span data-stu-id="52344-103">Register New Customers</span></span>

<span data-ttu-id="52344-104">Kunder er kilden til dine inntekter.</span><span class="sxs-lookup"><span data-stu-id="52344-104">Customers are the source of your income.</span></span> <span data-ttu-id="52344-105">Du må registrere gver kunde du selger til, som et kundekort.</span><span class="sxs-lookup"><span data-stu-id="52344-105">You must register each customer you sell to as a customer card.</span></span> <span data-ttu-id="52344-106">Kundekort inneholder informasjonen som er nødvendig for å selge produkter til kunden.</span><span class="sxs-lookup"><span data-stu-id="52344-106">Customer cards hold the information that is required to sell products to the customer.</span></span> <span data-ttu-id="52344-107">Hvis du vil ha mer informasjon, kan du se [Fakturere salg](sales-how-invoice-sales.md) og [Registrere nye varer](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="52344-107">For more information, see [Invoice Sales](sales-how-invoice-sales.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>  

<span data-ttu-id="52344-108">Før du kan registrere nye kunder, må du definere forskjellige salgskoder som du kan velge fra når du fyller ut kundekort.</span><span class="sxs-lookup"><span data-stu-id="52344-108">Before you can register new customers, you must set up various sales codes that you can select from when you fill in customer cards.</span></span> <span data-ttu-id="52344-109">Hvis du vil ha mer informasjon, kan du se [Sette opp salg](sales-setup-sales.md).</span><span class="sxs-lookup"><span data-stu-id="52344-109">For more information, see [Setting Up Sales](sales-setup-sales.md).</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers"></a><span data-ttu-id="52344-110">Legge til nye kunder</span><span class="sxs-lookup"><span data-stu-id="52344-110">Adding new customers</span></span>

<span data-ttu-id="52344-111">Hvis du vil registrere en ny kunde, må du fylle ut et kundekort.</span><span class="sxs-lookup"><span data-stu-id="52344-111">To register a new customer, you must fill in a customer card.</span></span> <span data-ttu-id="52344-112">Du kan opprette maler for ulike kundeprofiler, eller du kan legge til kunder uten maler.</span><span class="sxs-lookup"><span data-stu-id="52344-112">You can establish templates for different customer profiles, or you can add customers without templates.</span></span>  

> [!NOTE]  
> <span data-ttu-id="52344-113">Hvis det finnes kundemaler for ulike kundetyper, vises en side når du oppretter et nytt kundekort der du kan velge en passende mal.</span><span class="sxs-lookup"><span data-stu-id="52344-113">If customer templates exist for different customer types, then a page appears when you create a new customer card from where you can select an appropriate template.</span></span> <span data-ttu-id="52344-114">Hvis det bare finnes én kundemal, brukes alltid denne malen i nye kundekort.</span><span class="sxs-lookup"><span data-stu-id="52344-114">If only one customer template exists, then new customer cards always use that template.</span></span>  

### <a name="to-create-a-new-customer-card"></a><span data-ttu-id="52344-115">Opprette et nytt kundekort</span><span class="sxs-lookup"><span data-stu-id="52344-115">To create a new customer card</span></span>

1. <span data-ttu-id="52344-116">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="52344-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>  
2. <span data-ttu-id="52344-117">På siden **Kunder** velger du handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="52344-117">On the **Customers** page, choose the **New** action.</span></span>

    <span data-ttu-id="52344-118">Hvis det bare finnes én kundemal, åpnes et nytt kundekort med noen felt som er fylt ut med informasjon fra malen.</span><span class="sxs-lookup"><span data-stu-id="52344-118">If only one customer template exists, then a new customer card opens with some fields filled with information from the template.</span></span>

    <span data-ttu-id="52344-119">Hvis det finnes mer enn én kundemal, åpnes en side der du kan velge en kundemal.</span><span class="sxs-lookup"><span data-stu-id="52344-119">If more than one customer template exists, then a page opens from which you can select a customer template.</span></span> <span data-ttu-id="52344-120">I det tilfellet følger du de to neste trinnene.</span><span class="sxs-lookup"><span data-stu-id="52344-120">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="52344-121">På siden **Velg en mal for en ny kunde** velger du malen som du vil bruke for det nye kundekortet.</span><span class="sxs-lookup"><span data-stu-id="52344-121">On the **Select a template for a new customer** page, choose the template that you want to use for the new customer card.</span></span>
4. <span data-ttu-id="52344-122">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="52344-122">Choose the **OK** button.</span></span> <span data-ttu-id="52344-123">Det åpnes et nytt kundekort med noen felt som er fylt ut med informasjon fra malen.</span><span class="sxs-lookup"><span data-stu-id="52344-123">A new customer card opens with some fields filled with information from the template.</span></span>  
5. <span data-ttu-id="52344-124">Fortsette med å fylle ut eller endre feltet på kundekortet etter behov.</span><span class="sxs-lookup"><span data-stu-id="52344-124">Proceed to fill or change fields on the customer card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="52344-125">I hurtigfanen **Salgspriser** kan du vise spesialpriser eller rabatter som skal gis til kunden hvis bestemte kriterier oppfylles, for eksempel vare, minimumsordreantall eller sluttdato.</span><span class="sxs-lookup"><span data-stu-id="52344-125">On the **Sales Prices** FastTab, you can view special prices or discounts that you grant for the customer if certain criteria are met, such as item, minimum order quantity, or ending date.</span></span> <span data-ttu-id="52344-126">Hver rad representerer en spesialpris eller linjerabatt.</span><span class="sxs-lookup"><span data-stu-id="52344-126">Each row represents a special price or line discount.</span></span> <span data-ttu-id="52344-127">Hver kolonne representerer et vilkår som må brukes for å garantere spesialprisen du angir i feltet **Enhetspris**, eller linjerabatten du angir i feltet **Linjerabatt-%**.</span><span class="sxs-lookup"><span data-stu-id="52344-127">Each column represents a criterion that must apply to warrant the special price that you enter in the **Unit Price** field, or the line discount that you enter in the **Line Discount %** field.</span></span> <span data-ttu-id="52344-128">Hvis du vil ha mer informasjon, kan du se [Registrere avtaler om salgspris, rabatt og betaling](sales-how-record-sales-price-discount-payment-agreements.md).</span><span class="sxs-lookup"><span data-stu-id="52344-128">For more information, see [Record Sales Price, Discount, and Payment Agreements](sales-how-record-sales-price-discount-payment-agreements.md).</span></span>

<span data-ttu-id="52344-129">Kunden er nå registrert, og kundekortet er klart til å brukes på salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="52344-129">The customer is now registered, and the customer card is ready to be used on sales documents.</span></span>

<span data-ttu-id="52344-130">Hvis du vil bruke dette kundekortet som en mal når du oppretter nye kundekort, kan du lagre det som en mal.</span><span class="sxs-lookup"><span data-stu-id="52344-130">If you want to use this customer card as a template when you create new customer cards, you can save it as a template.</span></span> <span data-ttu-id="52344-131">Hvis du vil ha mer informasjon, kan du se følgende avsnitt:</span><span class="sxs-lookup"><span data-stu-id="52344-131">For more information, see the following section.</span></span>  

### <a name="to-save-the-customer-card-as-a-template"></a><span data-ttu-id="52344-132">Lagre kundekortet som en mal</span><span class="sxs-lookup"><span data-stu-id="52344-132">To save the customer card as a template</span></span>

1. <span data-ttu-id="52344-133">På siden **Kundekort** velger du handlingen **Lagre som mal**.</span><span class="sxs-lookup"><span data-stu-id="52344-133">On the **Customer Card** page, choose the **Save as Template** action.</span></span> <span data-ttu-id="52344-134">**Kundemal**-siden åpnes og viser kundekortet som en mal.</span><span class="sxs-lookup"><span data-stu-id="52344-134">The **Customer Template** page opens showing the customer card as a template.</span></span>
2. <span data-ttu-id="52344-135">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="52344-135">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="52344-136">Hvis du vil bruke dimensjoner i maler, velger du handlingen **Dimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="52344-136">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="52344-137">**Dimensjonsmaler**-siden åpnes med alle dimensjonskoder som er definert for kunden.</span><span class="sxs-lookup"><span data-stu-id="52344-137">The **Dimension Templates** page opens showing any dimension codes that are set up for the customer.</span></span>
4. <span data-ttu-id="52344-138">Rediger eller angi dimensjonskoder som skal gjelde for nye kundekort som opprettes ved hjelp av malen.</span><span class="sxs-lookup"><span data-stu-id="52344-138">Edit or enter dimension codes that will apply to new customer cards created by using the template.</span></span>  
5. <span data-ttu-id="52344-139">Når du har fullført den nye kundemalen, kan du velge **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="52344-139">When you have completed the new customer template, choose the **OK** button.</span></span>

<span data-ttu-id="52344-140">Kundemalen legges til i listen over kundemaler, slik at du kan bruke den til å opprette nye kundekort.</span><span class="sxs-lookup"><span data-stu-id="52344-140">The customer template is added to the list of customer templates, so that you can use it to create new customer cards.</span></span>

## <a name="deleting-customer-cards"></a><span data-ttu-id="52344-141">Slette kundekort</span><span class="sxs-lookup"><span data-stu-id="52344-141">Deleting customer cards</span></span>

<span data-ttu-id="52344-142">Hvis du har bokført en transaksjon for en kunde, kan du ikke slette kortet, fordi postene kan være nødvendige for revisjon.</span><span class="sxs-lookup"><span data-stu-id="52344-142">If you have posted a transaction for a customer, you cannot delete the card because the ledger entries may be needed for auditing.</span></span> <span data-ttu-id="52344-143">Hvis du vil slette kundekort med poster, kontakter du Microsoft-partneren for å gjøre det gjennom kode.</span><span class="sxs-lookup"><span data-stu-id="52344-143">To delete customer cards with ledger entries, contact your Microsoft partner to do so through code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="52344-144">Se også</span><span class="sxs-lookup"><span data-stu-id="52344-144">See Also</span></span>

[<span data-ttu-id="52344-145">Definere betalingsmåter</span><span class="sxs-lookup"><span data-stu-id="52344-145">Defining Payment Methods</span></span>](finance-payment-methods.md)  
[<span data-ttu-id="52344-146">Slå sammen dupliserte poster</span><span class="sxs-lookup"><span data-stu-id="52344-146">Merge Duplicate Records</span></span>](sales-how-merge-duplicate-records.md)  
[<span data-ttu-id="52344-147">Opprette nummerserier</span><span class="sxs-lookup"><span data-stu-id="52344-147">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="52344-148">Salg</span><span class="sxs-lookup"><span data-stu-id="52344-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="52344-149">Sette opp salg</span><span class="sxs-lookup"><span data-stu-id="52344-149">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="52344-150">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="52344-150">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
