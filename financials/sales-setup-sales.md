---
title: "Oversikt over oppgaver for å konfigurere salgsprosesser | Microsoft-dokumentasjon"
description: "Gir en oversikt over oppgaver for å definere regler og verdier som definerer salgsprinsipper og -prosesser."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, configure
ms.date: 06/01/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 75ed584feda066a6c412f861bd624646c4c31085
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2017

---
# <a name="setting-up-sales"></a><span data-ttu-id="11be7-103">Sette opp salg</span><span class="sxs-lookup"><span data-stu-id="11be7-103">Setting Up Sales</span></span>
<span data-ttu-id="11be7-104">Før du kan håndtere salgsprosesser, må du konfigurere regler og verdier som definerer selskapets salgsprinsipper.</span><span class="sxs-lookup"><span data-stu-id="11be7-104">Before you can manage sales processes, you must configure the rules and values that define the company's sales policies.</span></span>

<span data-ttu-id="11be7-105">Du må definere det generelle oppsettet, for eksempel hvilke salgsdokumenter som kreves, og hvordan dokumentenes verdier skal bokføres.</span><span class="sxs-lookup"><span data-stu-id="11be7-105">You must define the general setup, such as which sales documents are required and how their values are posted.</span></span> <span data-ttu-id="11be7-106">Dette generelle oppsettet foretas vanligvis én gang under den første implementeringen.</span><span class="sxs-lookup"><span data-stu-id="11be7-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="11be7-107">En egen rekke oppgaver relatert til registrering av nye kunder er å registrere alle spesialpris eller rabattavtaler som du har med hver kunde.</span><span class="sxs-lookup"><span data-stu-id="11be7-107">A separate series of tasks related to registering new customers is to record any special price or discount agreements that you have with each customer.</span></span>

<span data-ttu-id="11be7-108">Finansrelatert salgsoppsett, for eksempel betalingsmåte og valutaer, beskrives i avsnittet Finansoppsett.</span><span class="sxs-lookup"><span data-stu-id="11be7-108">Finance-related sales setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="11be7-109">Hvis du vil ha mer informasjon, kan du se [Konfigurere finans](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="11be7-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="11be7-110">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="11be7-110">To</span></span> | <span data-ttu-id="11be7-111">Se</span><span class="sxs-lookup"><span data-stu-id="11be7-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="11be7-112">Opprett et kundekort for hver kunde du selger til.</span><span class="sxs-lookup"><span data-stu-id="11be7-112">Create a customer card for each customer that you sell to.</span></span> |[<span data-ttu-id="11be7-113">Registrere nye kunder</span><span class="sxs-lookup"><span data-stu-id="11be7-113">How to: Register New Customers</span></span>](sales-how-register-new-customers.md) |
| <span data-ttu-id="11be7-114">Lar kunder betale via PayPal ved å velge PayPal-logoen på salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="11be7-114">Enable customers to pay through PayPal by choosing the PayPal logo on sales documents.</span></span> |[<span data-ttu-id="11be7-115">Aktiver kundebetalinger gjennom PayPal</span><span class="sxs-lookup"><span data-stu-id="11be7-115">How to: Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md) |
| <span data-ttu-id="11be7-116">Angi ulike rabatter og spesialpriser som du gir kundene, avhengig av vare, antall og/eller dato.</span><span class="sxs-lookup"><span data-stu-id="11be7-116">Enter the different discounts and special prices that you grant to customers depending on item, quantities, and/or date.</span></span> |[<span data-ttu-id="11be7-117">Registrere avtaler om salgspris, rabatt og betaling</span><span class="sxs-lookup"><span data-stu-id="11be7-117">How to: Record Sales Price, Discount, and Payment Agreements</span></span>](sales-how-record-sales-price-discount-payment-agreements.md) |
| <span data-ttu-id="11be7-118">Definere selgere, slik at du kan tilordne dem til kundekontakter eller måle selgernes prestasjoner som et grunnlag for beregning av salgsprovisjon eller bonus.</span><span class="sxs-lookup"><span data-stu-id="11be7-118">Set up salespeople so that you can assign them to customer contacts or measure salespeople's performance as a basis for calculating the sales commission or bonus.</span></span> |[<span data-ttu-id="11be7-119">Definere selgere</span><span class="sxs-lookup"><span data-stu-id="11be7-119">How to: Set Up Salespeople</span></span>](sales-how-setup-salespeople.md) |
| <span data-ttu-id="11be7-120">Angi for hver enkelt kunde eller for alle kunder hvordan salgsdokumenter sendes som standard når du velger **Konter og send**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="11be7-120">Specify for individual customers or for all customers how sales documents are sent by default when you choose the **Post and Send** action.</span></span> |[<span data-ttu-id="11be7-121">Definere en profil for dokumentsending</span><span class="sxs-lookup"><span data-stu-id="11be7-121">How to: Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md) |
| <span data-ttu-id="11be7-122">Angi at e-post skal inneholde et sammendrag av informasjonen i salgsdokumentet som sendes.</span><span class="sxs-lookup"><span data-stu-id="11be7-122">Set your email up to contain a summary of information in the sales document that is being sent.</span></span> |<span data-ttu-id="11be7-123">[Sende dokumenter i e-post](ui-how-send-documents-email.md).</span><span class="sxs-lookup"><span data-stu-id="11be7-123">[How to: Send Documents by Email](ui-how-send-documents-email.md).</span></span> |

## <a name="see-also"></a><span data-ttu-id="11be7-124">Se også</span><span class="sxs-lookup"><span data-stu-id="11be7-124">See Also</span></span>
[<span data-ttu-id="11be7-125">Salg</span><span class="sxs-lookup"><span data-stu-id="11be7-125">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="11be7-126">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="11be7-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

