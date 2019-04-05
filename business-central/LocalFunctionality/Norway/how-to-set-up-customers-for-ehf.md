---
title: Sette opp kunder for EHF
description: Hvis du vil opprette dokumenter i Elektronisk Handelsformat (EHF) for kunder i offentlig sektor, må du legge til EHF-informasjon for de aktuelle kundene.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 7fae0d71ad9b31d9bf57ed6eab7f0f9fd2c3d000
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "826959"
---
# <a name="set-up-customers-for-ehf"></a><span data-ttu-id="879da-103">Sette opp kunder for EHF</span><span class="sxs-lookup"><span data-stu-id="879da-103">Set Up Customers for EHF</span></span>
<span data-ttu-id="879da-104">Hvis du vil opprette dokumenter i Elektronisk Handelsformat (EHF) for kunder i offentlig sektor, må du legge til EHF-informasjon for de aktuelle kundene.</span><span class="sxs-lookup"><span data-stu-id="879da-104">To create Elektronisk Handelsformat (EHF) documents for customers in the public sector, you must add EHF information to the relevant customers.</span></span>  

<span data-ttu-id="879da-105">Dette emnet beskriver bare felt som gjelder EHF.</span><span class="sxs-lookup"><span data-stu-id="879da-105">This topic only describes fields that apply to EHF.</span></span> <span data-ttu-id="879da-106">Hvis du vil ha mer informasjon om hvordan du konfigurerer kunder generelt, se [Registrere nye kunder](../../sales-how-register-new-customers.md).</span><span class="sxs-lookup"><span data-stu-id="879da-106">For more information on setting up customers, in general, see [Register New Customers](../../sales-how-register-new-customers.md).</span></span>  

## <a name="to-set-up-a-customer-that-uses-elektronisk-handelsformat"></a><span data-ttu-id="879da-107">Slik definerer du en kunde som bruker Elektronisk Handelsformat:</span><span class="sxs-lookup"><span data-stu-id="879da-107">To set up a customer that uses Elektronisk Handelsformat</span></span>  

1.  <span data-ttu-id="879da-108">Velg ikonet ![Søk etter side eller rapport](../../media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kunder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="879da-108">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="879da-109">Åpne kunden du vil aktivere for EHF.</span><span class="sxs-lookup"><span data-stu-id="879da-109">Open the customer that you want to enable for EHF.</span></span>  
3.  <span data-ttu-id="879da-110">I hurtigfanen **Fakturering** fyller du ut feltene som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="879da-110">On the **Invoicing** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="879da-111">Felt</span><span class="sxs-lookup"><span data-stu-id="879da-111">Field</span></span>|<span data-ttu-id="879da-112">Description</span><span class="sxs-lookup"><span data-stu-id="879da-112">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="879da-113">**GLN**</span><span class="sxs-lookup"><span data-stu-id="879da-113">**GLN**</span></span>|<span data-ttu-id="879da-114">Påkrevd.</span><span class="sxs-lookup"><span data-stu-id="879da-114">Required.</span></span> <span data-ttu-id="879da-115">Angi det globale lokasjonsnummeret (GLN) for kunden.</span><span class="sxs-lookup"><span data-stu-id="879da-115">Enter the Global Location Number (GLN) for the customer.</span></span>|  
    |<span data-ttu-id="879da-116">**Kontokode**</span><span class="sxs-lookup"><span data-stu-id="879da-116">**Account Code**</span></span>|<span data-ttu-id="879da-117">Angi kontokoden for kunden.</span><span class="sxs-lookup"><span data-stu-id="879da-117">Enter the account code for the customer.</span></span><br /><br /> <span data-ttu-id="879da-118">Kunder i offentlig sektor gir en kontokode når de plasserer en ordre eller rekvisisjon.</span><span class="sxs-lookup"><span data-stu-id="879da-118">Customers in the public sector provide an account code when they place an order or requisition.</span></span> <span data-ttu-id="879da-119">Basert på verdien i dette feltet, inkluderes kontokoden i EHF-dokumentene du oppretter i [!INCLUDE[d365fin](../../includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="879da-119">Based on the value of this field, the account code is included in the EHF documents that you create in [!INCLUDE[d365fin](../../includes/d365fin_md.md)].</span></span> <span data-ttu-id="879da-120">Se Kontokode for mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="879da-120">For more information, see Account Code.</span></span>|  
    |<span data-ttu-id="879da-121">**E-faktura**</span><span class="sxs-lookup"><span data-stu-id="879da-121">**E-Invoice**</span></span>|<span data-ttu-id="879da-122">Merk av for å bruke elektronisk fakturering med kunden.</span><span class="sxs-lookup"><span data-stu-id="879da-122">Select the check box to use electronic invoicing with this customer.</span></span>|  
    |<span data-ttu-id="879da-123">**Ansvarssenter**</span><span class="sxs-lookup"><span data-stu-id="879da-123">**Responsibility Center**</span></span>|<span data-ttu-id="879da-124">Kontroller at ansvarssenteret du har valgt, har angitt en lands-/regionkode.</span><span class="sxs-lookup"><span data-stu-id="879da-124">Make sure that the Responsibility Center that you have selected has a Country/Region Code specified.</span></span>|  

<span data-ttu-id="879da-125">Disse feltene er spesifikke for EHF.</span><span class="sxs-lookup"><span data-stu-id="879da-125">These fields are specific to EHF.</span></span> <span data-ttu-id="879da-126">Verdiene brukes i alle EHF-dokumenter du oppretter for denne kunden.</span><span class="sxs-lookup"><span data-stu-id="879da-126">The values are used in all EHF documents that you create for this customer.</span></span> <span data-ttu-id="879da-127">Hvis du vil ha mer informasjon, se [EHF – Elektronisk fakturering i Norge](ehf-electronic-invoicing-in-norway.md).</span><span class="sxs-lookup"><span data-stu-id="879da-127">For more information, see [EHF Electronic Invoicing in Norway](ehf-electronic-invoicing-in-norway.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="879da-128">Se også</span><span class="sxs-lookup"><span data-stu-id="879da-128">See Also</span></span>  
 <span data-ttu-id="879da-129">[Opprette elektroniske dokumenter for EHF](how-to-create-electronic-documents-for-ehf.md) </span><span class="sxs-lookup"><span data-stu-id="879da-129">[Create Electronic Documents for EHF](how-to-create-electronic-documents-for-ehf.md) </span></span>  
 [<span data-ttu-id="879da-130">Angi EHF</span><span class="sxs-lookup"><span data-stu-id="879da-130">Set Up EHF</span></span>](how-to-set-up-ehf.md)
