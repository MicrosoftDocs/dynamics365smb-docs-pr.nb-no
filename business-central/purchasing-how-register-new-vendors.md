---
title: Opprette et leverandørkort for å registrere en ny leverandør | Microsoft-dokumentasjon
description: Finn ut hvordan du oppretter et leverandørkort for å registrere en ny leverandør.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f1028b91101f8faa38d4d4d5d2695ee498ff6d2e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772657"
---
# <a name="register-new-vendors"></a><span data-ttu-id="f5436-103">Registrere nye leverandører</span><span class="sxs-lookup"><span data-stu-id="f5436-103">Register New Vendors</span></span>

<span data-ttu-id="f5436-104">Leverandører tilbyr produktene du selger.</span><span class="sxs-lookup"><span data-stu-id="f5436-104">Vendors provide the products that you sell.</span></span> <span data-ttu-id="f5436-105">Hver leverandør du kjøper fra, må være registrert som et leverandørkort.</span><span class="sxs-lookup"><span data-stu-id="f5436-105">Each vendor that you purchase from must be registered as a vendor card.</span></span>

<span data-ttu-id="f5436-106">Før du kan registrere nye leverandører, må du definere forskjellige kjøpskoder som du kan velge fra når du fyller ut leverandørkort.</span><span class="sxs-lookup"><span data-stu-id="f5436-106">Before you can register new vendors, you must set up various purchase codes that you can select from when you fill vendor cards.</span></span> <span data-ttu-id="f5436-107">Når du har angitt alle nødvendige hoveddata, kan du konfigurere leverandøren ytterligere, for eksempel angi betalingsprioritet og vise en oversikt over varer som leverandøren og andre leverandører kan levere.</span><span class="sxs-lookup"><span data-stu-id="f5436-107">When all of the required master data is created, you can perform additional configuration of the vendor, such as prioritize the vendor for payment purposes and list items that the vendor and other vendors can supply.</span></span> <span data-ttu-id="f5436-108">En annen gruppe med oppsettsoppgaver for leverandører er å registrere avtaler om rabatter, priser og betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="f5436-108">Another group of setup tasks for vendors is to record your agreements concerning discounts, prices, and payment methods.</span></span> <span data-ttu-id="f5436-109">Hvis du vil ha mer informasjon, kan du se [Definere kjøp](purchasing-setup-purchasing.md).</span><span class="sxs-lookup"><span data-stu-id="f5436-109">For more information, see [Setting Up Purchasing](purchasing-setup-purchasing.md).</span></span>

<span data-ttu-id="f5436-110">Leverandørkort inneholder informasjon som er nødvendig for å kjøpe produkter fra leverandøren.</span><span class="sxs-lookup"><span data-stu-id="f5436-110">Vendor cards hold the information that is required to buy products from the vendor.</span></span> <span data-ttu-id="f5436-111">Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md) og [Registrere nye varer](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="f5436-111">For more information, see [Record Purchases](purchasing-how-record-purchases.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="f5436-112">Hvis det finnes leverandørmaler for ulike leverandørtyper, vises en side når du oppretter et nytt leverandørkort, der du kan velge en passende mal.</span><span class="sxs-lookup"><span data-stu-id="f5436-112">If vendor templates exist for different vendor types, then a page appears when you create a new vendor card from where you can select an appropriate template.</span></span> <span data-ttu-id="f5436-113">Hvis det bare finnes én leverandørmal, brukes alltid denne malen i nye leverandørkort.</span><span class="sxs-lookup"><span data-stu-id="f5436-113">If only one vendor template exists, then new vendor cards always use that template.</span></span>
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="adding-new-vendors"></a><span data-ttu-id="f5436-114">Legge til nye leverandører</span><span class="sxs-lookup"><span data-stu-id="f5436-114">Adding new vendors</span></span>

<span data-ttu-id="f5436-115">Hvis du vil registrere en ny leverandør, må du fylle ut et leverandørkort.</span><span class="sxs-lookup"><span data-stu-id="f5436-115">To register a new vendor, you must fill in a vendor card.</span></span> <span data-ttu-id="f5436-116">Du kan opprette maler for ulike leverandørprofiler, eller du kan legge til leverandør uten maler.</span><span class="sxs-lookup"><span data-stu-id="f5436-116">You can establish templates for different vendor profiles, or you can add vendors without templates.</span></span> <span data-ttu-id="f5436-117">Du kan også opprette en leverandør fra en kontakt.</span><span class="sxs-lookup"><span data-stu-id="f5436-117">You can also create a vendor from a contact.</span></span> <span data-ttu-id="f5436-118">Hvis du vil ha mer informasjon, kan du se [Slik oppretter du en kontakt, leverandør, ansatt eller bankkonto fra en kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).</span><span class="sxs-lookup"><span data-stu-id="f5436-118">For more information, see [To create a customer, vendor, employee, or bank account from a contact](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).</span></span>  

> [!NOTE]  
> <span data-ttu-id="f5436-119">Hvis det finnes leverandørmaler for ulike leverandørtyper, vises en side når du oppretter et nytt leverandørkort, der du kan velge en passende mal.</span><span class="sxs-lookup"><span data-stu-id="f5436-119">If vendor templates exist for different vendor types, then a page appears when you create a new vendor card from where you can select an appropriate template.</span></span> <span data-ttu-id="f5436-120">Hvis det bare finnes én leverandørmal, brukes alltid denne malen i nye leverandørkort.</span><span class="sxs-lookup"><span data-stu-id="f5436-120">If only one vendor template exists, then new vendor cards always use that template.</span></span>  

### <a name="to-create-a-new-vendor-card"></a><span data-ttu-id="f5436-121">Opprette et nytt leverandørkort</span><span class="sxs-lookup"><span data-stu-id="f5436-121">To create a new vendor card</span></span>

1. <span data-ttu-id="f5436-122">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Leverandører**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="f5436-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f5436-123">På **Leverandører**-siden velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f5436-123">On the **Vendors** page, Choose **New**.</span></span>

    <span data-ttu-id="f5436-124">Hvis det finnes mer enn én leverandørmal, åpnes en side der du kan velge en leverandørmal.</span><span class="sxs-lookup"><span data-stu-id="f5436-124">If more than one vendor template exists, then a page opens from which you can select a vendor template.</span></span> <span data-ttu-id="f5436-125">I det tilfellet følger du de to neste trinnene.</span><span class="sxs-lookup"><span data-stu-id="f5436-125">In that case, follow the next two steps.</span></span>
    1. <span data-ttu-id="f5436-126">På siden **Velg en mal for en ny leverandør** velger du malen som du vil bruke for det nye leverandørkortet.</span><span class="sxs-lookup"><span data-stu-id="f5436-126">On the **Select a template for a new vendor** page, choose the template that you want to use for the new vendor card.</span></span>
    2. <span data-ttu-id="f5436-127">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f5436-127">Choose the **OK** button.</span></span> <span data-ttu-id="f5436-128">Det åpnes et nytt leverandørkort med noen felt som er fylt ut med informasjon fra malen.</span><span class="sxs-lookup"><span data-stu-id="f5436-128">A new vendor card opens with some fields filled with information from the template.</span></span>
3. <span data-ttu-id="f5436-129">Fortsette med å fylle ut eller endre feltet på leverandørkortet etter behov.</span><span class="sxs-lookup"><span data-stu-id="f5436-129">Proceed to fill or change fields on the vendor card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!TIP]  
    > <span data-ttu-id="f5436-130">Hvis du ikke vet fakturaadressen som skal brukes for hver eneste faktura fra en leverandør, lar du være å fylle ut feltet **Leverandørnr.** på leverandørkortet.</span><span class="sxs-lookup"><span data-stu-id="f5436-130">If you do not know the invoicing address that will be used for every invoice from a vendor, do not fill in the **Vendor No.** field.</span></span> <span data-ttu-id="f5436-131">I stedet velger du betal til-leverandørnummeret når du har definert en forespørsel, bestilling eller et fakturahode.</span><span class="sxs-lookup"><span data-stu-id="f5436-131">Instead, choose the pay-to vendor number after you have set up a purchase quote, order, or invoice header.</span></span>

<span data-ttu-id="f5436-132">Leverandøren er nå registrert, og leverandørkortet er klart til å brukes på kjøpsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="f5436-132">The vendor is now registered, and the vendor card is ready to be used on purchase documents.</span></span>

<span data-ttu-id="f5436-133">Hvis du vil bruke dette leverandørkortet som en mal når du oppretter nye leverandørkort, kan du lagre det som en leverandørmal.</span><span class="sxs-lookup"><span data-stu-id="f5436-133">If you want to use this vendor card as a template when you create new vendor cards, you can save it as a vendor template.</span></span> <span data-ttu-id="f5436-134">Hvis du vil ha mer informasjon, kan du se delen [Slik lagrer du leverandørkortet som en mal](#to-save-the-vendor-card-as-a-template).</span><span class="sxs-lookup"><span data-stu-id="f5436-134">For more information, see the [To save the vendor card as a template](#to-save-the-vendor-card-as-a-template) section.</span></span>

### <a name="deleting-vendor-cards"></a><span data-ttu-id="f5436-135">Slette leverandørkort</span><span class="sxs-lookup"><span data-stu-id="f5436-135">Deleting vendor cards</span></span>

<span data-ttu-id="f5436-136">Hvis du har bokført en transaksjon for en leverandør, kan du ikke slette kortet, fordi postene kan være nødvendige for revisjon.</span><span class="sxs-lookup"><span data-stu-id="f5436-136">If you have posted a transaction for a vendor, you cannot delete the card because the ledger entries may be needed for auditing.</span></span> <span data-ttu-id="f5436-137">Hvis du vil slette leverandørkort med poster, kontakter du Microsoft-partneren for å gjøre det via kode.</span><span class="sxs-lookup"><span data-stu-id="f5436-137">To delete vendor cards with ledger entries, contact your Microsoft partner to do so through code.</span></span>

## <a name="to-save-the-vendor-card-as-a-template"></a><span data-ttu-id="f5436-138">Lagre leverandørkortet som en mal</span><span class="sxs-lookup"><span data-stu-id="f5436-138">To save the vendor card as a template</span></span>

1. <span data-ttu-id="f5436-139">På siden **Leverandørkort** velger du handlingen **Lagre som mal**.</span><span class="sxs-lookup"><span data-stu-id="f5436-139">On the **Vendor Card** page, choose the **Save as Template** action.</span></span> <span data-ttu-id="f5436-140">**Leverandørmal**-siden åpnes og viser leverandørkortet som en mal.</span><span class="sxs-lookup"><span data-stu-id="f5436-140">The **Vendor Template** page opens showing the vendor card as a template.</span></span>
2. <span data-ttu-id="f5436-141">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="f5436-141">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="f5436-142">Hvis du vil bruke dimensjoner i maler, velger du handlingen **Dimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="f5436-142">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="f5436-143">**Dimensjonsmaler**-siden åpnes med alle dimensjonskoder som er definert for leverandøren.</span><span class="sxs-lookup"><span data-stu-id="f5436-143">The **Dimension Templates** page opens showing any dimension codes that are set up for the vendor.</span></span>
4. <span data-ttu-id="f5436-144">Rediger eller angi dimensjonskoder som skal gjelde for nye leverandørkort som opprettes ved hjelp av malen.</span><span class="sxs-lookup"><span data-stu-id="f5436-144">Edit or enter dimension codes that will apply to new vendor cards created by using the template.</span></span>
5. <span data-ttu-id="f5436-145">Når du har fullført den nye leverandørmalen, kan du velge **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="f5436-145">When you have completed the new vendor template, choose the **OK** button.</span></span>  
   <span data-ttu-id="f5436-146">Leverandørmalen legges til i listen over leverandørmaler, slik at du kan bruke den til å opprette nye leverandørkort.</span><span class="sxs-lookup"><span data-stu-id="f5436-146">The vendor template is added to the list of vendor templates, so that you can use it to create new vendor cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="f5436-147">Se også</span><span class="sxs-lookup"><span data-stu-id="f5436-147">See Also</span></span>

[<span data-ttu-id="f5436-148">Slå sammen dupliserte poster</span><span class="sxs-lookup"><span data-stu-id="f5436-148">Merge Duplicate Records</span></span>](sales-how-merge-duplicate-records.md)  
[<span data-ttu-id="f5436-149">Opprette nummerserier</span><span class="sxs-lookup"><span data-stu-id="f5436-149">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="f5436-150">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="f5436-150">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="f5436-151">Registrere kjøp</span><span class="sxs-lookup"><span data-stu-id="f5436-151">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
<span data-ttu-id="f5436-152">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f5436-152">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  

[!INCLUDE[footer-include](includes/footer-banner.md)]