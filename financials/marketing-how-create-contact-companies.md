---
title: Opprette kontaktselskaper | Microsoft-dokumentasjon
description: Beskriver hvordan du oppretter en kontakt for hvert nye selskap eller potensielle selskap du samhandler med eller har et forhold til.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ed0f75f1e0ee8a282b58458e4fed3b4eef7c46fb
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="create-contact-companies"></a><span data-ttu-id="255a3-103">Opprette kontaktselskaper</span><span class="sxs-lookup"><span data-stu-id="255a3-103">Create Contact Companies</span></span>
<span data-ttu-id="255a3-104">Du kan opprette en kontakt for hvert nytt selskap du utfører en samhandling med, for eksempel kunder, leverandører, prospektive kunder, banker, advokatfirmaer, konsulenter og så videre.</span><span class="sxs-lookup"><span data-stu-id="255a3-104">You can create a contact for each new company you interact with, for example, a customer, vendor, prospective customer, bank, law firm, consultant, and so on.</span></span>

<span data-ttu-id="255a3-105">Det er to måter å opprette en kontakt på: fra grunnen av eller fra en eksisterende kunde, leverandør eller bankkonto.</span><span class="sxs-lookup"><span data-stu-id="255a3-105">There are two ways to create a contact: from scratch or from an existing customer, vendor, or bank account.</span></span>

<span data-ttu-id="255a3-106">Før du oppretter en kontakt, bør du kontrollere innstillingene i vinduet **Markedsføringsoppsett**.</span><span class="sxs-lookup"><span data-stu-id="255a3-106">Before creating a contact, you may want to check the settings in the **Marketing Setup** window.</span></span> <span data-ttu-id="255a3-107">Hvis du vil ha mer informasjon, kan du se [Sette opp forbindelser](marketing-setup-marketing.md).</span><span class="sxs-lookup"><span data-stu-id="255a3-107">For more information, see [Setting Up Relationship Management](marketing-setup-marketing.md).</span></span>

## <a name="create-a-company-contact-from-scratch"></a><span data-ttu-id="255a3-108">Opprette en selskapskontakt fra bunnen av</span><span class="sxs-lookup"><span data-stu-id="255a3-108">Create a company contact from scratch</span></span>
1. <span data-ttu-id="255a3-109">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kontakter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="255a3-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Contacts**, and then choose the related link.</span></span>
2. <span data-ttu-id="255a3-110">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="255a3-110">Choose the **New** action.</span></span>
3. <span data-ttu-id="255a3-111">Angi et nummer på kontakten i feltet **Nr.**.</span><span class="sxs-lookup"><span data-stu-id="255a3-111">In the **No. field**, enter a number for the contact.</span></span>

    <span data-ttu-id="255a3-112">Hvis du har definert en nummerserie for kontakter i vinduet **Markedsføringsoppsett**, kan du eventuelt trykke Enter-tasten for å velge det neste tilgjengelige kontaktnummeret.</span><span class="sxs-lookup"><span data-stu-id="255a3-112">Alternatively, if you have set up a number series for contacts in the **Marketing Setup** window, you can press the Enter key to select the next available contact number.</span></span>  
4. <span data-ttu-id="255a3-113">Sett **Type** til **Selskap**.</span><span class="sxs-lookup"><span data-stu-id="255a3-113">Set **Type** to **Company**.</span></span>
5. <span data-ttu-id="255a3-114">Fyll ut de andre feltene etter behov:</span><span class="sxs-lookup"><span data-stu-id="255a3-114">Fill in the other fields as required.</span></span>

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a><span data-ttu-id="255a3-115">Opprette en selskapskontakt fra en kunde, leverandør eller bankkonto</span><span class="sxs-lookup"><span data-stu-id="255a3-115">To create a company contact from a customer, vendor, or bank account</span></span>
<span data-ttu-id="255a3-116">Hvis du allerede har definert en rekke kunder, leverandører og bankkonti, kan du opprette kontakter på grunnlag av de eksisterende dataene.</span><span class="sxs-lookup"><span data-stu-id="255a3-116">If you have already set up a number of customers, vendors, and bank accounts, you can create contacts on the basis of the existing data.</span></span> <span data-ttu-id="255a3-117">Når du oppretter en kontakt på denne måten, synkroniseres kontaktinformasjonen med informasjon om kunden, leverandøren eller bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="255a3-117">When you create a contact this way, the contact information is synchronized with the customer, vendor, or bank account information.</span></span>

> [!NOTE]  
>   <span data-ttu-id="255a3-118">Før du kan opprette kontaktselskaper på denne måten, må du angi en kode for forretningsforbindelse for kunder, leverandører og bankkonti, i vinduet **Markedsføringsoppsett**.</span><span class="sxs-lookup"><span data-stu-id="255a3-118">Before you can create contact companies this way, you must specify a business relation code for customers, vendors, and bank accounts in the **Marketing Setup** window.</span></span> <span data-ttu-id="255a3-119">Hvis du vil opprette kontakter fra en bankkonto, må du også angi nummerserie for bankkonti i vinduet **Finansoppsett**.</span><span class="sxs-lookup"><span data-stu-id="255a3-119">If you will be creating contacts from a bank accounts, you must also specify numbers series for bank accounts in the **General Ledger Setup** window.</span></span>

1. <span data-ttu-id="255a3-120">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi ett av følgende, avhengig av hvor du vil opprette kontakter fra, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="255a3-120">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter one of the following, depending on from where you want to create contacts, and then choose the related link.</span></span>
   * <span data-ttu-id="255a3-121">**Opprett kontakter fra kunder**</span><span class="sxs-lookup"><span data-stu-id="255a3-121">**Create Contacts from Customers**</span></span>
   * <span data-ttu-id="255a3-122">**Opprett kontakter fra leverandører**</span><span class="sxs-lookup"><span data-stu-id="255a3-122">**Create Contacts from Vendors**</span></span>
   * <span data-ttu-id="255a3-123">**Opprett kontakter fra bankkonti**</span><span class="sxs-lookup"><span data-stu-id="255a3-123">**Create Contacts from Bank Accounts**</span></span>
2. <span data-ttu-id="255a3-124">Hvis du bare vil opprette kontakter fra bestemte kunder, leverandører eller bankkonti, definerer du filtre i inndelingen **Kunde**, **Leverandør** eller **Bankkonto** i vinduet for kjørselen som åpnes.</span><span class="sxs-lookup"><span data-stu-id="255a3-124">In the batch job window that opens, in the **Customer**, **Vendor**, or **Bank Account** section, set filters if you want to create contacts from specific customers, vendors, or bank accounts.</span></span>
3. <span data-ttu-id="255a3-125">Velg **OK** for å starte oppretting av kontrakter.</span><span class="sxs-lookup"><span data-stu-id="255a3-125">Choose the **OK** button to start creating contacts.</span></span>

    <span data-ttu-id="255a3-126">De neste kontaktnumrene i nummerserien tilordnes de nye kontaktene.</span><span class="sxs-lookup"><span data-stu-id="255a3-126">The next contact numbers in the number series are assigned to the new contacts.</span></span> <span data-ttu-id="255a3-127">Forretningsforbindelsen for leverandører som er angitt i vinduet **Markedsføringsoppsett**, tilordnes til nyopprettede kontakter.</span><span class="sxs-lookup"><span data-stu-id="255a3-127">The business relation for vendors that is specified in the **Marketing Setup** window is assigned to the newly created contacts.</span></span>

> [!TIP]  
>   <span data-ttu-id="255a3-128">Du kan også opprette en kunde, leverandør eller bankkonto fra en kontakt.</span><span class="sxs-lookup"><span data-stu-id="255a3-128">You can also create a customer, vendor, or bank account from a contact.</span></span> <span data-ttu-id="255a3-129">Hvis du vil ha mer informasjon, kan du se [Opprette en kunde, leverandør eller bankkonto fra en kontakt](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="255a3-129">For more information, see [Create a Customer, Vendor, or Bank Account From a Contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="255a3-130">Se også</span><span class="sxs-lookup"><span data-stu-id="255a3-130">See Also</span></span>
[<span data-ttu-id="255a3-131">Synkronisere kontakter med kunder, leverandører og bankkonti</span><span class="sxs-lookup"><span data-stu-id="255a3-131">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[<span data-ttu-id="255a3-132">Tilordne forretningsforbindelser til en kontakt</span><span class="sxs-lookup"><span data-stu-id="255a3-132">Assign Business Relations to a Contact</span></span>](marketing-business-relations.md#AssignBusRelContact)  
[<span data-ttu-id="255a3-133">Tilordne bransjegrupper til en kontakt</span><span class="sxs-lookup"><span data-stu-id="255a3-133">Assign Industry Groups to a Contact</span></span>](marketing-industry-groups.md#AssignIndustryGroupContact)  
[<span data-ttu-id="255a3-134">Tilordne postgrupper til en kontakt</span><span class="sxs-lookup"><span data-stu-id="255a3-134">Assign Mailing Groups to a Contact</span></span>](marketing-mailing-groups.md#AssignMailGroupContact)  
[<span data-ttu-id="255a3-135">Opprette kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="255a3-135">Create Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="255a3-136">Arbeide med Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="255a3-136">Working with Finance and Operations, Business edition</span></span>](ui-work-product.md)

