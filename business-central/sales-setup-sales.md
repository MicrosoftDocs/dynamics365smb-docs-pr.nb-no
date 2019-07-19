---
title: Oversikt over oppgaver for å konfigurere salgsprosesser | Microsoft-dokumentasjon
description: Gir en oversikt over oppgaver for å definere regler og verdier som definerer salgsprinsipper og -prosesser.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, configure
ms.date: 06/17/2019
ms.author: sgroespe
ms.openlocfilehash: 3ece1edb7ba18cb96099cba34065c96164390e82
ms.sourcegitcommit: 6dc83b27ac47f3b39a7b84cfb7446e7f48b8ce63
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/17/2019
ms.locfileid: "1632709"
---
# <a name="setting-up-sales"></a><span data-ttu-id="a028b-103">Sette opp salg</span><span class="sxs-lookup"><span data-stu-id="a028b-103">Setting Up Sales</span></span>
<span data-ttu-id="a028b-104">Før du kan håndtere salgsprosesser, må du konfigurere regler og verdier som definerer selskapets salgsprinsipper.</span><span class="sxs-lookup"><span data-stu-id="a028b-104">Before you can manage sales processes, you must configure the rules and values that define the company's sales policies.</span></span>

<span data-ttu-id="a028b-105">Du må definere det generelle oppsettet, for eksempel hvilke salgsdokumenter som kreves, og hvordan dokumentenes verdier skal bokføres.</span><span class="sxs-lookup"><span data-stu-id="a028b-105">You must define the general setup, such as which sales documents are required and how their values are posted.</span></span> <span data-ttu-id="a028b-106">Dette generelle oppsettet foretas vanligvis én gang under den første implementeringen.</span><span class="sxs-lookup"><span data-stu-id="a028b-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="a028b-107">En egen rekke oppgaver relatert til registrering av nye kunder er å registrere alle spesialpris eller rabattavtaler som du har med hver kunde.</span><span class="sxs-lookup"><span data-stu-id="a028b-107">A separate series of tasks related to registering new customers is to record any special price or discount agreements that you have with each customer.</span></span>

<span data-ttu-id="a028b-108">Finansrelatert salgsoppsett, for eksempel betalingsmåte og valutaer, beskrives i avsnittet Finansoppsett.</span><span class="sxs-lookup"><span data-stu-id="a028b-108">Finance-related sales setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="a028b-109">Hvis du vil ha mer informasjon, kan du se [Konfigurere finans](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="a028b-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="a028b-110">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="a028b-110">To</span></span> | <span data-ttu-id="a028b-111">Se</span><span class="sxs-lookup"><span data-stu-id="a028b-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="a028b-112">Opprett et kundekort for hver kunde du selger til.</span><span class="sxs-lookup"><span data-stu-id="a028b-112">Create a customer card for each customer that you sell to.</span></span> |[<span data-ttu-id="a028b-113">Registrere nye kunder</span><span class="sxs-lookup"><span data-stu-id="a028b-113">Register New Customers</span></span>](sales-how-register-new-customers.md) |
| <span data-ttu-id="a028b-114">Lar kunder betale via PayPal ved å velge PayPal-logoen på salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="a028b-114">Enable customers to pay through PayPal by choosing the PayPal logo on sales documents.</span></span> |[<span data-ttu-id="a028b-115">Aktivere kundebetalinger gjennom PayPal</span><span class="sxs-lookup"><span data-stu-id="a028b-115">Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md) |
| <span data-ttu-id="a028b-116">Angi ulike rabatter og spesialpriser som du gir kundene, avhengig av vare, antall og/eller dato.</span><span class="sxs-lookup"><span data-stu-id="a028b-116">Enter the different discounts and special prices that you grant to customers depending on item, quantities, and/or date.</span></span> |[<span data-ttu-id="a028b-117">Registrere avtaler om salgspris, rabatt og betaling</span><span class="sxs-lookup"><span data-stu-id="a028b-117">Record Sales Price, Discount, and Payment Agreements</span></span>](sales-how-record-sales-price-discount-payment-agreements.md) |
| <span data-ttu-id="a028b-118">Definere selgere, slik at du kan tilordne dem til kundekontakter eller måle selgernes prestasjoner som et grunnlag for beregning av salgsprovisjon eller bonus.</span><span class="sxs-lookup"><span data-stu-id="a028b-118">Set up salespeople so that you can assign them to customer contacts or measure salespeople's performance as a basis for calculating the sales commission or bonus.</span></span> |[<span data-ttu-id="a028b-119">Definere selgere</span><span class="sxs-lookup"><span data-stu-id="a028b-119">Set Up Salespeople</span></span>](sales-how-setup-salespeople.md) |
| <span data-ttu-id="a028b-120">Angi for hver enkelt kunde eller for alle kunder hvordan salgsdokumenter sendes som standard når du velger **Konter og send**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="a028b-120">Specify for individual customers or for all customers how sales documents are sent by default when you choose the **Post and Send** action.</span></span> |[<span data-ttu-id="a028b-121">Definere en profil for dokumentsending</span><span class="sxs-lookup"><span data-stu-id="a028b-121">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md) |
| <span data-ttu-id="a028b-122">Angi at e-post skal inneholde et sammendrag av informasjonen i salgsdokumentet som sendes.</span><span class="sxs-lookup"><span data-stu-id="a028b-122">Set your email up to contain a summary of information in the sales document that is being sent.</span></span> |<span data-ttu-id="a028b-123">[Sende dokumenter i e-post](ui-how-send-documents-email.md)</span><span class="sxs-lookup"><span data-stu-id="a028b-123">[Send Documents by Email](ui-how-send-documents-email.md).</span></span> |
|<span data-ttu-id="a028b-124">Bruke en EU-webtjeneste for å bekrefte kundens organisasjonsnummer.</span><span class="sxs-lookup"><span data-stu-id="a028b-124">Use an EU web service to verify a customer's VAT registration number.</span></span>|[<span data-ttu-id="a028b-125">Bekrefte organisasjonsnumre</span><span class="sxs-lookup"><span data-stu-id="a028b-125">Verify VAT Registration Numbers</span></span>](finance-setup-vat.md)|
|<span data-ttu-id="a028b-126">Definer de ulike incoterms-vilkårene som du tilbyr kunder eller som leverandører tilbyr deg.</span><span class="sxs-lookup"><span data-stu-id="a028b-126">Define the different incoterms that you offer to customers or that your vendors offer you.</span></span>|[<span data-ttu-id="a028b-127">Sette opp leveringsmåter</span><span class="sxs-lookup"><span data-stu-id="a028b-127">Set Up Shipment Methods</span></span>](sales-how-set-up-shipment-methods.md)|
|<span data-ttu-id="a028b-128">Angi informasjon om de ulike transportørene du benytter, inkludert en kobling til pakkesporingstjenesten.</span><span class="sxs-lookup"><span data-stu-id="a028b-128">Enter information about the different transportation vendors you use, including a link to their package tracking service.</span></span>|[<span data-ttu-id="a028b-129">Definere transportører</span><span class="sxs-lookup"><span data-stu-id="a028b-129">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)|

## <a name="see-also"></a><span data-ttu-id="a028b-130">Se også</span><span class="sxs-lookup"><span data-stu-id="a028b-130">See Also</span></span>
[<span data-ttu-id="a028b-131">Salg</span><span class="sxs-lookup"><span data-stu-id="a028b-131">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="a028b-132">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a028b-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
