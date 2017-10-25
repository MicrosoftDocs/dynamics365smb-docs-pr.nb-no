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
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a16201e48cc823e687c9941082d34044d9612a29
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-sales"></a><span data-ttu-id="41767-103">Sette opp salg</span><span class="sxs-lookup"><span data-stu-id="41767-103">Setting Up Sales</span></span>
<span data-ttu-id="41767-104">Før du kan håndtere salgsprosesser, må du konfigurere regler og verdier som definerer selskapets salgsprinsipper.</span><span class="sxs-lookup"><span data-stu-id="41767-104">Before you can manage sales processes, you must configure the rules and values that define the company's sales policies.</span></span>

<span data-ttu-id="41767-105">Du må definere det generelle oppsettet, for eksempel hvilke salgsdokumenter som kreves, og hvordan dokumentenes verdier skal bokføres.</span><span class="sxs-lookup"><span data-stu-id="41767-105">You must define the general setup, such as which sales documents are required and how their values are posted.</span></span> <span data-ttu-id="41767-106">Dette generelle oppsettet foretas vanligvis én gang under den første implementeringen.</span><span class="sxs-lookup"><span data-stu-id="41767-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="41767-107">En egen rekke oppgaver relatert til registrering av nye kunder er å registrere alle spesialpris eller rabattavtaler som du har med hver kunde.</span><span class="sxs-lookup"><span data-stu-id="41767-107">A separate series of tasks related to registering new customers is to record any special price or discount agreements that you have with each customer.</span></span>

<span data-ttu-id="41767-108">Finansrelatert salgsoppsett, for eksempel betalingsmåte og valutaer, beskrives i avsnittet Finansoppsett.</span><span class="sxs-lookup"><span data-stu-id="41767-108">Finance-related sales setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="41767-109">Hvis du vil ha mer informasjon, kan du se [Konfigurere finans](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="41767-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="41767-110">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="41767-110">To</span></span> | <span data-ttu-id="41767-111">Se</span><span class="sxs-lookup"><span data-stu-id="41767-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="41767-112">Opprett et kundekort for hver kunde du selger til.</span><span class="sxs-lookup"><span data-stu-id="41767-112">Create a customer card for each customer that you sell to.</span></span> |[<span data-ttu-id="41767-113">Registrere nye kunder</span><span class="sxs-lookup"><span data-stu-id="41767-113">How to: Register New Customers</span></span>](sales-how-register-new-customers.md) |
| <span data-ttu-id="41767-114">Lar kunder betale via PayPal ved å velge PayPal-logoen på salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="41767-114">Enable customers to pay through PayPal by choosing the PayPal logo on sales documents.</span></span> |[<span data-ttu-id="41767-115">Aktiver kundebetalinger gjennom PayPal</span><span class="sxs-lookup"><span data-stu-id="41767-115">How to: Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md) |
| <span data-ttu-id="41767-116">Angi ulike rabatter og spesialpriser som du gir kundene, avhengig av vare, antall og/eller dato.</span><span class="sxs-lookup"><span data-stu-id="41767-116">Enter the different discounts and special prices that you grant to customers depending on item, quantities, and/or date.</span></span> |[<span data-ttu-id="41767-117">Registrere avtaler om salgspris, rabatt og betaling</span><span class="sxs-lookup"><span data-stu-id="41767-117">How to: Record Sales Price, Discount, and Payment Agreements</span></span>](sales-how-record-sales-price-discount-payment-agreements.md) |
| <span data-ttu-id="41767-118">Definere selgere, slik at du kan tilordne dem til kundekontakter eller måle selgernes prestasjoner som et grunnlag for beregning av salgsprovisjon eller bonus.</span><span class="sxs-lookup"><span data-stu-id="41767-118">Set up salespeople so that you can assign them to customer contacts or measure salespeople's performance as a basis for calculating the sales commission or bonus.</span></span> |[<span data-ttu-id="41767-119">Definere selgere</span><span class="sxs-lookup"><span data-stu-id="41767-119">How to: Set Up Salespeople</span></span>](sales-how-setup-salespeople.md) |
| <span data-ttu-id="41767-120">Angi for hver enkelt kunde eller for alle kunder hvordan salgsdokumenter sendes som standard når du velger **Konter og send**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="41767-120">Specify for individual customers or for all customers how sales documents are sent by default when you choose the **Post and Send** action.</span></span> |[<span data-ttu-id="41767-121">Definere en profil for dokumentsending</span><span class="sxs-lookup"><span data-stu-id="41767-121">How to: Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md) |
| <span data-ttu-id="41767-122">Angi at e-post skal inneholde et sammendrag av informasjonen i salgsdokumentet som sendes.</span><span class="sxs-lookup"><span data-stu-id="41767-122">Set your email up to contain a summary of information in the sales document that is being sent.</span></span> |<span data-ttu-id="41767-123">[Sende dokumenter i e-post](ui-how-send-documents-email.md).</span><span class="sxs-lookup"><span data-stu-id="41767-123">[How to: Send Documents by Email](ui-how-send-documents-email.md).</span></span> |
|<span data-ttu-id="41767-124">Bruke en EU-webtjeneste for å bekrefte kundens organisasjonsnummer.</span><span class="sxs-lookup"><span data-stu-id="41767-124">Use an EU web service to verify a customer's VAT registration number.</span></span>|[<span data-ttu-id="41767-125">Bekrefte organisasjonsnumre</span><span class="sxs-lookup"><span data-stu-id="41767-125">How to: Verify VAT Registration Numbers</span></span>](sales-how-to-verify-vat-registration-numbers.md)|
|<span data-ttu-id="41767-126">Angi informasjon om de ulike transportørene du benytter, inkludert en kobling til pakkesporingstjenesten.</span><span class="sxs-lookup"><span data-stu-id="41767-126">Enter information about the different transportation vendors you use, including a link to their package tracking service.</span></span>|[<span data-ttu-id="41767-127">Definere transportører</span><span class="sxs-lookup"><span data-stu-id="41767-127">How to: Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)|

## <a name="see-also"></a><span data-ttu-id="41767-128">Se også</span><span class="sxs-lookup"><span data-stu-id="41767-128">See Also</span></span>
[<span data-ttu-id="41767-129">Salg</span><span class="sxs-lookup"><span data-stu-id="41767-129">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="41767-130">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="41767-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

