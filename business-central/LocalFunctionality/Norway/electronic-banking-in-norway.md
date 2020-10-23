---
title: Elektroniske banktjenester i Norge
description: Forbedringer i den norske versjonen omfatter elektroniske banktjenester.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2c4e8ddb72ce78b2a4738dd185f1f049b4c8294e
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919803"
---
# <a name="electronic-banking-in-norway"></a><span data-ttu-id="21ecb-103">Elektroniske banktjenester i Norge</span><span class="sxs-lookup"><span data-stu-id="21ecb-103">Electronic Banking in Norway</span></span>
[!INCLUDE[d365fin](../../includes/d365fin_md.md)] <span data-ttu-id="21ecb-104">omfatter forbedringer i den norske versjonen for elektroniske banktjenester.</span><span class="sxs-lookup"><span data-stu-id="21ecb-104">includes Norwegian enhancements to electronic banking.</span></span> <span data-ttu-id="21ecb-105">Denne funksjonaliteten kan brukes til å utføre følgende operasjoner:</span><span class="sxs-lookup"><span data-stu-id="21ecb-105">You can use this functionality to perform the following operations:</span></span>  

- <span data-ttu-id="21ecb-106">Motta elektroniske betalinger basert på en OCR-betalings-ID (optisk tegngjenkjenning).</span><span class="sxs-lookup"><span data-stu-id="21ecb-106">Receive electronic payments based on an optical character recognition (OCR) payment ID.</span></span>  
- <span data-ttu-id="21ecb-107">Skrive ut kunde-ID-numre (KID) på salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="21ecb-107">Print Kunde ID (KID) numbers on sales and receivables documents.</span></span>  
- <span data-ttu-id="21ecb-108">Sende elektroniske betalinger til leverandører.</span><span class="sxs-lookup"><span data-stu-id="21ecb-108">Send electronic payments to vendors.</span></span>  

## <a name="customer-identification-numbers"></a><span data-ttu-id="21ecb-109">Kundeidentifikasjonsnummer</span><span class="sxs-lookup"><span data-stu-id="21ecb-109">Customer Identification Numbers</span></span>  
 <span data-ttu-id="21ecb-110">Kunde-ID (KID) er et kundeidentifikasjonsnummer som inneholder en betalingsreferanse til leverandøren, og sikrer at betalingen bokføres riktig hos leverandøren.</span><span class="sxs-lookup"><span data-stu-id="21ecb-110">Kunde ID (KID) is a customer identification number that provides a payment reference to the vendor and ensures that the vendor is posting the payment correctly.</span></span> <span data-ttu-id="21ecb-111">Hvis leverandørdokumentene inneholder KID-nummer, må du bruke dette nummeret fordi det kan påløpe et tilleggsgebyr for betalingen hvis du ikke bruker nummeret.</span><span class="sxs-lookup"><span data-stu-id="21ecb-111">If the vendor documents include the KID number, you should use this number as there may be a higher cost for the payment if you do not.</span></span>  

 <span data-ttu-id="21ecb-112">KID kan angis på følgende lokasjoner:</span><span class="sxs-lookup"><span data-stu-id="21ecb-112">The KID can be entered in the following locations:</span></span>  

- <span data-ttu-id="21ecb-113">Salgsfakturaer</span><span class="sxs-lookup"><span data-stu-id="21ecb-113">Sales invoices</span></span>  
- <span data-ttu-id="21ecb-114">Rentenotaer</span><span class="sxs-lookup"><span data-stu-id="21ecb-114">Finance charge memos</span></span>  
- <span data-ttu-id="21ecb-115">Purringer</span><span class="sxs-lookup"><span data-stu-id="21ecb-115">Reminders</span></span>  
- <span data-ttu-id="21ecb-116">Bestillinger</span><span class="sxs-lookup"><span data-stu-id="21ecb-116">Purchase orders</span></span>  
- <span data-ttu-id="21ecb-117">Kjøpsfakturaer</span><span class="sxs-lookup"><span data-stu-id="21ecb-117">Purchase invoices</span></span>  
- <span data-ttu-id="21ecb-118">Kjøpskladder</span><span class="sxs-lookup"><span data-stu-id="21ecb-118">Purchase journals</span></span>  
- <span data-ttu-id="21ecb-119">Remitteringskladder</span><span class="sxs-lookup"><span data-stu-id="21ecb-119">Remittance journals</span></span>  

> [!NOTE]  
>  <span data-ttu-id="21ecb-120">KID-nummeret kan ikke brukes på kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="21ecb-120">The KID cannot be used for credit memos.</span></span> <span data-ttu-id="21ecb-121">Hvis en kreditnota er en del av betalingen, må fakturaene i den samme betalingen behandles som betalinger uten KID-nummer.</span><span class="sxs-lookup"><span data-stu-id="21ecb-121">If a credit memo is part of the payment, invoices in the same payment must be treated as payments without a KID.</span></span>  

## <a name="see-also"></a><span data-ttu-id="21ecb-122">Se også</span><span class="sxs-lookup"><span data-stu-id="21ecb-122">See Also</span></span>  
 <span data-ttu-id="21ecb-123">[Funksjonalitet som er spesifikk for norske brukere](norway-local-functionality.md) </span><span class="sxs-lookup"><span data-stu-id="21ecb-123">[Norway Local Functionality](norway-local-functionality.md) </span></span>  
 <span data-ttu-id="21ecb-124">[Norsk giro og OCR-B-skrift](norwegian-giro-and-ocr-b-font.md) </span><span class="sxs-lookup"><span data-stu-id="21ecb-124">[Norwegian Giro and OCR-B Font](norwegian-giro-and-ocr-b-font.md) </span></span>  
 <span data-ttu-id="21ecb-125">[Opprette KID-numre på salgsdokumenter](how-to-set-up-kid-numbers-on-sales-documents.md) </span><span class="sxs-lookup"><span data-stu-id="21ecb-125">[Set Up KID Numbers on Sales Documents](how-to-set-up-kid-numbers-on-sales-documents.md) </span></span>  
 <span data-ttu-id="21ecb-126">[Opprette OCR-betalinger](how-to-set-up-ocr-payments.md) </span><span class="sxs-lookup"><span data-stu-id="21ecb-126">[Set Up OCR Payments](how-to-set-up-ocr-payments.md) </span></span>  
 <span data-ttu-id="21ecb-127">[Importere og bokføre OCR-betalinger](how-to-import-and-post-ocr-payments.md) </span><span class="sxs-lookup"><span data-stu-id="21ecb-127">[Import and Post OCR Payments](how-to-import-and-post-ocr-payments.md) </span></span>  
 <span data-ttu-id="21ecb-128">[Elektroniske betalinger til leverandører i Norge](electronic-payments-to-vendors-in-norway.md) </span><span class="sxs-lookup"><span data-stu-id="21ecb-128">[Electronic Payments to Vendors in Norway](electronic-payments-to-vendors-in-norway.md) </span></span>  
 [<span data-ttu-id="21ecb-129">Skrive ut rapporten OCR-kladd - test</span><span class="sxs-lookup"><span data-stu-id="21ecb-129">Print the OCR Journal - Test Report</span></span>](how-to-print-the-ocr-journal-test-report.md)
