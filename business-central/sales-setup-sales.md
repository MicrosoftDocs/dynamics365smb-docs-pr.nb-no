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
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 445b2c8ad3b5d4989324bae3d27423163d6808b5
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803751"
---
# <a name="setting-up-sales"></a><span data-ttu-id="a33b2-103">Sette opp salg</span><span class="sxs-lookup"><span data-stu-id="a33b2-103">Setting Up Sales</span></span>
<span data-ttu-id="a33b2-104">Før du kan håndtere salgsprosesser, må du konfigurere regler og verdier som definerer selskapets salgsprinsipper.</span><span class="sxs-lookup"><span data-stu-id="a33b2-104">Before you can manage sales processes, you must configure the rules and values that define the company's sales policies.</span></span>

<span data-ttu-id="a33b2-105">Du må definere det generelle oppsettet, for eksempel hvilke salgsdokumenter som kreves, og hvordan dokumentenes verdier skal bokføres.</span><span class="sxs-lookup"><span data-stu-id="a33b2-105">You must define the general setup, such as which sales documents are required and how their values are posted.</span></span> <span data-ttu-id="a33b2-106">Dette generelle oppsettet foretas vanligvis én gang under den første implementeringen.</span><span class="sxs-lookup"><span data-stu-id="a33b2-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="a33b2-107">En egen rekke oppgaver relatert til registrering av nye kunder er å registrere alle spesialpris eller rabattavtaler som du har med hver kunde.</span><span class="sxs-lookup"><span data-stu-id="a33b2-107">A separate series of tasks related to registering new customers is to record any special price or discount agreements that you have with each customer.</span></span>

<span data-ttu-id="a33b2-108">Finansrelatert salgsoppsett, for eksempel betalingsmåte og valutaer, beskrives i avsnittet Finansoppsett.</span><span class="sxs-lookup"><span data-stu-id="a33b2-108">Finance-related sales setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="a33b2-109">Hvis du vil ha mer informasjon, kan du se [Konfigurere finans](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="a33b2-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="a33b2-110">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="a33b2-110">To</span></span> | <span data-ttu-id="a33b2-111">Se</span><span class="sxs-lookup"><span data-stu-id="a33b2-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="a33b2-112">Opprett et kundekort for hver kunde du selger til.</span><span class="sxs-lookup"><span data-stu-id="a33b2-112">Create a customer card for each customer that you sell to.</span></span> |[<span data-ttu-id="a33b2-113">Registrere nye kunder</span><span class="sxs-lookup"><span data-stu-id="a33b2-113">Register New Customers</span></span>](sales-how-register-new-customers.md) |
| <span data-ttu-id="a33b2-114">Lar kunder betale via PayPal ved å velge PayPal-logoen på salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="a33b2-114">Enable customers to pay through PayPal by choosing the PayPal logo on sales documents.</span></span> |[<span data-ttu-id="a33b2-115">Aktivere kundebetalinger gjennom PayPal</span><span class="sxs-lookup"><span data-stu-id="a33b2-115">Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md) |
| <span data-ttu-id="a33b2-116">Angi ulike rabatter og spesialpriser som du gir kundene, avhengig av vare, antall og/eller dato.</span><span class="sxs-lookup"><span data-stu-id="a33b2-116">Enter the different discounts and special prices that you grant to customers depending on item, quantities, and/or date.</span></span> |[<span data-ttu-id="a33b2-117">Registrere avtaler om salgspris, rabatt og betaling</span><span class="sxs-lookup"><span data-stu-id="a33b2-117">Record Sales Price, Discount, and Payment Agreements</span></span>](sales-how-record-sales-price-discount-payment-agreements.md) |
| <span data-ttu-id="a33b2-118">Definere selgere, slik at du kan tilordne dem til kundekontakter eller måle selgernes prestasjoner som et grunnlag for beregning av salgsprovisjon eller bonus.</span><span class="sxs-lookup"><span data-stu-id="a33b2-118">Set up salespeople so that you can assign them to customer contacts or measure salespeople's performance as a basis for calculating the sales commission or bonus.</span></span> |[<span data-ttu-id="a33b2-119">Definere selgere</span><span class="sxs-lookup"><span data-stu-id="a33b2-119">Set Up Salespeople</span></span>](sales-how-setup-salespeople.md) |
| <span data-ttu-id="a33b2-120">Angi for hver enkelt kunde eller for alle kunder hvordan salgsdokumenter sendes som standard når du velger **Konter og send**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="a33b2-120">Specify for individual customers or for all customers how sales documents are sent by default when you choose the **Post and Send** action.</span></span> |[<span data-ttu-id="a33b2-121">Definere en profil for dokumentsending</span><span class="sxs-lookup"><span data-stu-id="a33b2-121">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md) |
| <span data-ttu-id="a33b2-122">Angi at e-post skal inneholde et sammendrag av informasjonen i salgsdokumentet som sendes.</span><span class="sxs-lookup"><span data-stu-id="a33b2-122">Set your email up to contain a summary of information in the sales document that is being sent.</span></span> |<span data-ttu-id="a33b2-123">[Sende dokumenter i e-post](ui-how-send-documents-email.md)</span><span class="sxs-lookup"><span data-stu-id="a33b2-123">[Send Documents by Email](ui-how-send-documents-email.md).</span></span> |
|<span data-ttu-id="a33b2-124">Bruke en EU-webtjeneste for å bekrefte kundens organisasjonsnummer.</span><span class="sxs-lookup"><span data-stu-id="a33b2-124">Use an EU web service to verify a customer's VAT registration number.</span></span>|[<span data-ttu-id="a33b2-125">Bekrefte organisasjonsnumre</span><span class="sxs-lookup"><span data-stu-id="a33b2-125">Verify VAT Registration Numbers</span></span>](finance-setup-vat.md)|
|<span data-ttu-id="a33b2-126">Angi informasjon om de ulike transportørene du benytter, inkludert en kobling til pakkesporingstjenesten.</span><span class="sxs-lookup"><span data-stu-id="a33b2-126">Enter information about the different transportation vendors you use, including a link to their package tracking service.</span></span>|[<span data-ttu-id="a33b2-127">Definere transportører</span><span class="sxs-lookup"><span data-stu-id="a33b2-127">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)|

## <a name="see-also"></a><span data-ttu-id="a33b2-128">Se også</span><span class="sxs-lookup"><span data-stu-id="a33b2-128">See Also</span></span>
[<span data-ttu-id="a33b2-129">Salg</span><span class="sxs-lookup"><span data-stu-id="a33b2-129">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="a33b2-130">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a33b2-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
