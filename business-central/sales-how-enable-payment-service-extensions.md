---
title: Aktivere kundebetalinger gjennom betalingstjenester | Microsoft-dokumentasjon
description: Gjør det lettere for kundene å betale sine fakturaer ved å aktivere betalingstjenester.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: e5d4d9fd0c6857c22f2b4c929a6e6ed528cadf26
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1252668"
---
# <a name="enable-customer-payments-through-payment-services"></a><span data-ttu-id="3bfc4-103">Aktivere kundebetalinger gjennom betalingstjenester</span><span class="sxs-lookup"><span data-stu-id="3bfc4-103">Enable Customer Payments Through Payment Services</span></span>
<span data-ttu-id="3bfc4-104">Som et alternativ til å samle inn betalinger via bankoverføring eller kredittkort, kan kundene betale via egne kontoer med betalingstjenester, som Microsoft Pay, PayPal eller WorldPay.</span><span class="sxs-lookup"><span data-stu-id="3bfc4-104">As an alternative to collecting payments through bank transfer or credit cards, your customers can pay you through their account with payment services, such as Microsoft Pay, PayPal, or WorldPay.</span></span>  

<span data-ttu-id="3bfc4-105">Når du har aktivert en betalingstjeneste i [!INCLUDE[d365fin](includes/d365fin_md.md)], en kobling til tjenesten er tilgjengelig på salgsdokumenter som du sender via e-post til kundene dine.</span><span class="sxs-lookup"><span data-stu-id="3bfc4-105">After you enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)], a link to the service is available on sales documents that you send by email to your customers.</span></span> <span data-ttu-id="3bfc4-106">Kunder kan bruke koblingen for å gå til tjenesten og betale fakturaen, direkte fra salgsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="3bfc4-106">Customers can use the link to go to the payment service and pay the bill, directly from the sales document.</span></span> <span data-ttu-id="3bfc4-107">Hvis du ikke vil inkludere koblingen, for eksempel kan Hvis en kunde betaler kontant, du fjerne tjenesten fra fakturaen før bokføring.</span><span class="sxs-lookup"><span data-stu-id="3bfc4-107">If you don't want to include the link, for example, if a customer will pay with cash, you can remove the payment service from the invoice before posting.</span></span>  

<span data-ttu-id="3bfc4-108">Tilleggene Microsoft Pay, PayPal Payments Standard og WorldPay Payments Standard er installert i [!INCLUDE[d365fin](includes/d365fin_md.md)] og er klar til å aktiveres.</span><span class="sxs-lookup"><span data-stu-id="3bfc4-108">The Microsoft Pay, PayPal Payments Standard, and WorldPay Payments Standard extensions are installed in [!INCLUDE[d365fin](includes/d365fin_md.md)], and are ready for you to enable.</span></span>  

## <a name="to-enable-a-payment-service-in-included365finincludesd365finmdmd"></a><span data-ttu-id="3bfc4-109">Slik aktiverer du en betalingstjeneste i [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="3bfc4-109">To enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
1. <span data-ttu-id="3bfc4-110">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Betalingstjenester**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="3bfc4-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3bfc4-111">På siden **Betalingstjenester** velger du handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="3bfc4-111">On the **Payment Services** page, choose the **New** action.</span></span>  
3. <span data-ttu-id="3bfc4-112">Velg betalingstjenesten, og lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="3bfc4-112">Select the payment service, and then close the page.</span></span>  
4. <span data-ttu-id="3bfc4-113">På siden **Betalingstjenester** velger du handlingen **Oppsett**.</span><span class="sxs-lookup"><span data-stu-id="3bfc4-113">On the **Payment Services** page, choose the **Setup** action.</span></span>  
5. <span data-ttu-id="3bfc4-114">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="3bfc4-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="3bfc4-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3bfc4-115">Close the page.</span></span>  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a><span data-ttu-id="3bfc4-116">Velge en betalingstjeneste på en salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="3bfc4-116">To select a payment service on a sales invoice</span></span>
1. <span data-ttu-id="3bfc4-117">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Salgsfakturaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="3bfc4-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3bfc4-118">Åpne Salgsfaktura som du ønsker å betale ved hjelp av betalingstjenesten.</span><span class="sxs-lookup"><span data-stu-id="3bfc4-118">Open the sales invoice that you want to pay by using the payment service.</span></span>  
3. <span data-ttu-id="3bfc4-119">I feltet **Betalingstjeneste** velger du betalingstjenesten.</span><span class="sxs-lookup"><span data-stu-id="3bfc4-119">In the **Payment Service** field, choose the payment service.</span></span>  

    > [!NOTE]  
    > <span data-ttu-id="3bfc4-120">Feltet **Betalingstjeneste** er bare tilgjengelig hvis du har aktivert betalingstjenesten.</span><span class="sxs-lookup"><span data-stu-id="3bfc4-120">The **Payment Service** field is available only if you've enabled the payment service.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3bfc4-121">Se også</span><span class="sxs-lookup"><span data-stu-id="3bfc4-121">See Also</span></span>  
[<span data-ttu-id="3bfc4-122">Sette opp salg</span><span class="sxs-lookup"><span data-stu-id="3bfc4-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="3bfc4-123">Salg</span><span class="sxs-lookup"><span data-stu-id="3bfc4-123">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="3bfc4-124">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="3bfc4-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="3bfc4-125">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3bfc4-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
