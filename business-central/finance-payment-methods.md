---
title: Definere betalingsmåter | Microsoft-dokumentasjon
description: Du bruker betalingsmåter, for eksempel sjekk, bankoverføring, kontanter eller PayPal, til å definere hvordan salgs- og kjøpsfakturaer skal betales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, bank transfer, cash, PayPal
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 708ae474b15724e151cba367842091763544a434
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182975"
---
# <a name="defining-payment-methods"></a><span data-ttu-id="a0a36-103">Definere betalingsmåter</span><span class="sxs-lookup"><span data-stu-id="a0a36-103">Defining Payment Methods</span></span>
<span data-ttu-id="a0a36-104">Betalingsmåter definerer hvordan du foretrekker at kunder betaler deg, og hvordan du vil betale leverandørene.</span><span class="sxs-lookup"><span data-stu-id="a0a36-104">Payment methods define the way you prefer for customers to pay you, and how you like to pay your vendors.</span></span> <span data-ttu-id="a0a36-105">Metoden kan variere for hver kunde eller leverandør.</span><span class="sxs-lookup"><span data-stu-id="a0a36-105">The method can vary for each customer or vendor.</span></span> <span data-ttu-id="a0a36-106">Eksempler på typiske betalingsmåter er **bank**, **kontant**, **sjekk** eller **konto**.</span><span class="sxs-lookup"><span data-stu-id="a0a36-106">Examples of typical payment methods are **bank**, **cash**, **check**, or **account**.</span></span>

<span data-ttu-id="a0a36-107">Du kan knytte en betalingsmåte til kunder og leverandører slik at den samme metoden alltid brukes på salgs- og kjøpsdokumenter du oppretter for dem.</span><span class="sxs-lookup"><span data-stu-id="a0a36-107">You can assign a payment method to customers and vendors so that the same method is always used on the sales and purchase documents you create for them.</span></span> <span data-ttu-id="a0a36-108">Hvis det er nødvendig, kan du endre metoden på salgs- eller kjøpsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="a0a36-108">If needed, you can change the method on the sales or purchase document.</span></span> <span data-ttu-id="a0a36-109">Hvis du for eksempel vil betale en bestemt kjøpsfaktura kontant i stedet for med sjekk.</span><span class="sxs-lookup"><span data-stu-id="a0a36-109">For example, if you want to pay a particular purchase invoice in cash rather than by check.</span></span> <span data-ttu-id="a0a36-110">Dette endrer ikke standard betalingsmåten som er knyttet til leverandøren.</span><span class="sxs-lookup"><span data-stu-id="a0a36-110">This does not change the default payment method assigned to the vendor.</span></span>

<span data-ttu-id="a0a36-111">Samme betalingsmåter brukes for salgs- og kjøpsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="a0a36-111">The same payment methods are used for sales and purchase documents.</span></span> <span data-ttu-id="a0a36-112">For eksempel en _kontant_ betalingsmåte brukes både når du foretar betalinger og når du mottar dem.</span><span class="sxs-lookup"><span data-stu-id="a0a36-112">For example, a _cash_ payment method is used both when you make payments and when you receive them.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="a0a36-113">vet at når du oppretter en salgsfaktura, forventer du å motta betaling, og motsatt for kjøpsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="a0a36-113">knows that when you are creating a sales invoice you expect to receive payment, and the opposite for purchase invoices.</span></span>

<span data-ttu-id="a0a36-114">Kreditnotaer for returer er imidlertid unntak fordi penger flyter i motsatte retninger, fra deg til leverandøren og fra leverandøren til deg.</span><span class="sxs-lookup"><span data-stu-id="a0a36-114">Credit memos for returns, however, are exceptions because money is flowing in the opposite directions, from you to your customer and from your vendor to you.</span></span> <span data-ttu-id="a0a36-115">En standard betalingsmåte tilordnes derfor ikke til kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="a0a36-115">Therefore, a default payment method is not assigned to credit memos.</span></span> <span data-ttu-id="a0a36-116">Du kan imidlertid unngå dette hvis du har angitt betalingsbetingelser for kunden eller leverandøren.</span><span class="sxs-lookup"><span data-stu-id="a0a36-116">There is, however, a workaround if you have specified terms of payment for the customer or vendor.</span></span> <span data-ttu-id="a0a36-117">Selv om feltet **Beregn kontantrab. for kred.nota** ikke er beregnet for dette, hvis du velger å merke av i boksen på **Betalingsbetingelser**, legges en standard betalingsmåte til når du oppretter en kreditnota.</span><span class="sxs-lookup"><span data-stu-id="a0a36-117">Though the **Calc. Pmt. Disc. on Cr. Memos** field is not intended for this, if you choose the check box on the **Payment Terms** page a default payment method will be added when you create a credit memo.</span></span> <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE476Ys?rel=0]

## <a name="to-set-up-a-payment-method"></a><span data-ttu-id="a0a36-118">Slik definerer du betalingsmåter</span><span class="sxs-lookup"><span data-stu-id="a0a36-118">To set up a payment method</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="a0a36-119">inneholder noen betalingsmåter som bedrifter bruker ofte.</span><span class="sxs-lookup"><span data-stu-id="a0a36-119">provides a few payment methods that businesses often use.</span></span> <span data-ttu-id="a0a36-120">Du kan imidlertid legge til så mange du trenger.</span><span class="sxs-lookup"><span data-stu-id="a0a36-120">You can, however, add as many as you need.</span></span>

1. <span data-ttu-id="a0a36-121">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Betalingsmåter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a0a36-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="a0a36-122">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="a0a36-122">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a><span data-ttu-id="a0a36-123">Slik tilordner du en betalingsmåte til en kunde eller leverandør</span><span class="sxs-lookup"><span data-stu-id="a0a36-123">To assign a payment method to a customer or vendor</span></span>
1. <span data-ttu-id="a0a36-124">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunde** eller **Leverandør**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a0a36-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer** or **Vendor**, and then choose the related link.</span></span>
2. <span data-ttu-id="a0a36-125">I **Betalingsmåte - kode**-feltet velger du metoden som skal brukes som standard for kunden eller leverandøren.</span><span class="sxs-lookup"><span data-stu-id="a0a36-125">In the **Payment Method Code** field, choose the method to use by default for the customer or vendor.</span></span>

## <a name="see-also"></a><span data-ttu-id="a0a36-126">Se også</span><span class="sxs-lookup"><span data-stu-id="a0a36-126">See Also</span></span>
[<span data-ttu-id="a0a36-127">Registrere nye kunder</span><span class="sxs-lookup"><span data-stu-id="a0a36-127">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="a0a36-128">Finans</span><span class="sxs-lookup"><span data-stu-id="a0a36-128">Finance</span></span>](finance.md)  
<span data-ttu-id="a0a36-129">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a0a36-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
