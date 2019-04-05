---
title: Opprette kontaktselskaper | Microsoft-dokumentasjon
description: Beskriver hvordan du oppretter en kontakt for hvert nye selskap eller potensielle selskap du samhandler med eller har et forhold til.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2018
ms.author: jswymer
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: ff585f1a96d509ef317aaaf3671bc91ca46a430a
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803842"
---
# <a name="create-contacts"></a><span data-ttu-id="28ac9-103">Opprette kontakter</span><span class="sxs-lookup"><span data-stu-id="28ac9-103">Create Contacts</span></span>
<span data-ttu-id="28ac9-104">Du kan opprette en kontakt for hvert nytt selskap du utfører en samhandling med, for eksempel kunder, leverandører, prospektive kunder, banker, advokatfirmaer, konsulenter og så videre.</span><span class="sxs-lookup"><span data-stu-id="28ac9-104">You can create a contact for each new company you interact with, for example, a customer, vendor, prospective customer, bank, law firm, consultant, and so on.</span></span>

<span data-ttu-id="28ac9-105">Det er to måter å opprette en kontakt på: fra grunnen av eller fra en eksisterende kunde, leverandør eller bankkonto.</span><span class="sxs-lookup"><span data-stu-id="28ac9-105">There are two ways to create a contact: from scratch or from an existing customer, vendor, or bank account.</span></span>

## <a name="create-a-company-contact-from-scratch"></a><span data-ttu-id="28ac9-106">Opprette en selskapskontakt fra bunnen av</span><span class="sxs-lookup"><span data-stu-id="28ac9-106">Create a company contact from scratch</span></span>
1. <span data-ttu-id="28ac9-107">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kontakter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="28ac9-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Contacts**, and then choose the related link.</span></span>
2. <span data-ttu-id="28ac9-108">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="28ac9-108">Choose the **New** action.</span></span>
3. <span data-ttu-id="28ac9-109">Angi et nummer på kontakten i feltet **Nr.**.</span><span class="sxs-lookup"><span data-stu-id="28ac9-109">In the **No. field**, enter a number for the contact.</span></span>

    <span data-ttu-id="28ac9-110">Hvis du har definert en nummerserie for kontakter på siden **Markedsføringsoppsett**, kan du eventuelt trykke Enter-tasten for å velge det neste tilgjengelige kontaktnummeret.</span><span class="sxs-lookup"><span data-stu-id="28ac9-110">Alternatively, if you have set up a number series for contacts on the **Marketing Setup** page, you can press the Enter key to select the next available contact number.</span></span>  
4. <span data-ttu-id="28ac9-111">Sett **Type** til **Selskap**.</span><span class="sxs-lookup"><span data-stu-id="28ac9-111">Set **Type** to **Company**.</span></span>
5. <span data-ttu-id="28ac9-112">Fyll ut de andre feltene etter behov:</span><span class="sxs-lookup"><span data-stu-id="28ac9-112">Fill in the other fields as required.</span></span>

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a><span data-ttu-id="28ac9-113">Opprette en selskapskontakt fra en kunde, leverandør eller bankkonto</span><span class="sxs-lookup"><span data-stu-id="28ac9-113">To create a company contact from a customer, vendor, or bank account</span></span>
<span data-ttu-id="28ac9-114">Hvis du allerede har definert en rekke kunder, leverandører og bankkonti, kan du opprette kontakter på grunnlag av de eksisterende dataene.</span><span class="sxs-lookup"><span data-stu-id="28ac9-114">If you have already set up a number of customers, vendors, and bank accounts, you can create contacts on the basis of the existing data.</span></span> <span data-ttu-id="28ac9-115">Når du oppretter en kontakt på denne måten, synkroniseres kontaktinformasjonen med informasjon om kunden, leverandøren eller bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="28ac9-115">When you create a contact this way, the contact information is synchronized with the customer, vendor, or bank account information.</span></span>

> [!NOTE]  
>   <span data-ttu-id="28ac9-116">Før du kan opprette kontaktselskaper på denne måten, må du angi en kode for forretningsforbindelse for kunder, leverandører og bankkonti, på siden **Markedsføringsoppsett**.</span><span class="sxs-lookup"><span data-stu-id="28ac9-116">Before you can create contact companies this way, you must specify a business relation code for customers, vendors, and bank accounts on the **Marketing Setup** page.</span></span> <span data-ttu-id="28ac9-117">Hvis du vil opprette kontakter fra en bankkonto, må du også angi nummerserie for bankkonti på siden **Finansoppsett**.</span><span class="sxs-lookup"><span data-stu-id="28ac9-117">If you will be creating contacts from a bank accounts, you must also specify numbers series for bank accounts on the **General Ledger Setup** page.</span></span>

1. <span data-ttu-id="28ac9-118">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi ett av følgende, alt etter hvor du vil opprette kontakter fra, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="28ac9-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter one of the following, depending on from where you want to create contacts, and then choose the related link.</span></span>
   * <span data-ttu-id="28ac9-119">**Opprett kontakter fra kunder**</span><span class="sxs-lookup"><span data-stu-id="28ac9-119">**Create Contacts from Customers**</span></span>
   * <span data-ttu-id="28ac9-120">**Opprett kontakter fra leverandører**</span><span class="sxs-lookup"><span data-stu-id="28ac9-120">**Create Contacts from Vendors**</span></span>
   * <span data-ttu-id="28ac9-121">**Opprett kontakter fra bankkonti**</span><span class="sxs-lookup"><span data-stu-id="28ac9-121">**Create Contacts from Bank Accounts**</span></span>
2. <span data-ttu-id="28ac9-122">Hvis du bare vil opprette kontakter fra bestemte kunder, leverandører eller bankkonti, definerer du filtre i inndelingen **Kunde**, **Leverandør** eller **Bankkonto** på siden for kjørselen som åpnes.</span><span class="sxs-lookup"><span data-stu-id="28ac9-122">In the batch job page that opens, in the **Customer**, **Vendor**, or **Bank Account** section, set filters if you want to create contacts from specific customers, vendors, or bank accounts.</span></span>
3. <span data-ttu-id="28ac9-123">Velg **OK** for å starte oppretting av kontrakter.</span><span class="sxs-lookup"><span data-stu-id="28ac9-123">Choose the **OK** button to start creating contacts.</span></span>

    <span data-ttu-id="28ac9-124">De neste kontaktnumrene i nummerserien tilordnes de nye kontaktene.</span><span class="sxs-lookup"><span data-stu-id="28ac9-124">The next contact numbers in the number series are assigned to the new contacts.</span></span> <span data-ttu-id="28ac9-125">Forretningsforbindelsen for leverandører som er angitt på siden **Markedsføringsoppsett**, tilordnes til nyopprettede kontakter.</span><span class="sxs-lookup"><span data-stu-id="28ac9-125">The business relation for vendors that is specified on the **Marketing Setup** page is assigned to the newly created contacts.</span></span>

> [!TIP]  
>   <span data-ttu-id="28ac9-126">Du kan også opprette en kunde, leverandør eller bankkonto fra en kontakt.</span><span class="sxs-lookup"><span data-stu-id="28ac9-126">You can also create a customer, vendor, or bank account from a contact.</span></span> <span data-ttu-id="28ac9-127">Hvis du vil ha mer informasjon, kan du se [Opprette en kunde, leverandør eller bankkonto fra en kontakt](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="28ac9-127">For more information, see [Create a Customer, Vendor, or Bank Account From a Contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="28ac9-128">Se også</span><span class="sxs-lookup"><span data-stu-id="28ac9-128">See Also</span></span>
[<span data-ttu-id="28ac9-129">Synkronisere kontakter med kunder, leverandører og bankkonti</span><span class="sxs-lookup"><span data-stu-id="28ac9-129">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[<span data-ttu-id="28ac9-130">Tilordne forretningsforbindelser til en kontakt</span><span class="sxs-lookup"><span data-stu-id="28ac9-130">Assign Business Relations to a Contact</span></span>](marketing-business-relations.md#AssignBusRelContact)  
[<span data-ttu-id="28ac9-131">Tilordne bransjegrupper til en kontakt</span><span class="sxs-lookup"><span data-stu-id="28ac9-131">Assign Industry Groups to a Contact</span></span>](marketing-industry-groups.md#AssignIndustryGroupContact)  
[<span data-ttu-id="28ac9-132">Tilordne postgrupper til en kontakt</span><span class="sxs-lookup"><span data-stu-id="28ac9-132">Assign Mailing Groups to a Contact</span></span>](marketing-mailing-groups.md#AssignMailGroupContact)  
[<span data-ttu-id="28ac9-133">Opprette kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="28ac9-133">Create Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="28ac9-134">Arbeide med Business Central</span><span class="sxs-lookup"><span data-stu-id="28ac9-134">Working with Business Central</span></span>](ui-work-product.md)
