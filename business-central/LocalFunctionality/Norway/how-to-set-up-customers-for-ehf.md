---
title: Sette opp kunder for EHF
description: Hvis du vil opprette dokumenter i Elektronisk Handelsformat (EHF) for kunder i offentlig sektor, må du legge til EHF-informasjon for de aktuelle kundene.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9aa7978f54d9d24240ce1bc0d404e75933688d94
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782199"
---
# <a name="set-up-customers-for-ehf"></a><span data-ttu-id="6ee44-103">Sette opp kunder for EHF</span><span class="sxs-lookup"><span data-stu-id="6ee44-103">Set Up Customers for EHF</span></span>
<span data-ttu-id="6ee44-104">Hvis du vil opprette dokumenter i Elektronisk Handelsformat (EHF) for kunder i offentlig sektor, må du legge til EHF-informasjon for de aktuelle kundene.</span><span class="sxs-lookup"><span data-stu-id="6ee44-104">To create Elektronisk Handelsformat (EHF) documents for customers in the public sector, you must add EHF information to the relevant customers.</span></span>  

<span data-ttu-id="6ee44-105">Dette emnet beskriver bare felt som gjelder EHF.</span><span class="sxs-lookup"><span data-stu-id="6ee44-105">This topic only describes fields that apply to EHF.</span></span> <span data-ttu-id="6ee44-106">Hvis du vil ha mer informasjon om hvordan du konfigurerer kunder generelt, se [Registrere nye kunder](../../sales-how-register-new-customers.md).</span><span class="sxs-lookup"><span data-stu-id="6ee44-106">For more information on setting up customers, in general, see [Register New Customers](../../sales-how-register-new-customers.md).</span></span>  

## <a name="to-set-up-a-customer-that-uses-elektronisk-handelsformat"></a><span data-ttu-id="6ee44-107">Slik definerer du en kunde som bruker Elektronisk Handelsformat:</span><span class="sxs-lookup"><span data-stu-id="6ee44-107">To set up a customer that uses Elektronisk Handelsformat</span></span>  

1.  <span data-ttu-id="6ee44-108">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](../../media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="6ee44-108">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="6ee44-109">Åpne kunden du vil aktivere for EHF.</span><span class="sxs-lookup"><span data-stu-id="6ee44-109">Open the customer that you want to enable for EHF.</span></span>  
3.  <span data-ttu-id="6ee44-110">I hurtigfanen **Fakturering** fyller du ut feltene som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="6ee44-110">On the **Invoicing** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="6ee44-111">Felt</span><span class="sxs-lookup"><span data-stu-id="6ee44-111">Field</span></span>|<span data-ttu-id="6ee44-112">Description</span><span class="sxs-lookup"><span data-stu-id="6ee44-112">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="6ee44-113">**GLN**</span><span class="sxs-lookup"><span data-stu-id="6ee44-113">**GLN**</span></span>|<span data-ttu-id="6ee44-114">Påkrevd.</span><span class="sxs-lookup"><span data-stu-id="6ee44-114">Required.</span></span> <span data-ttu-id="6ee44-115">Angi det globale lokasjonsnummeret (GLN) for kunden.</span><span class="sxs-lookup"><span data-stu-id="6ee44-115">Enter the Global Location Number (GLN) for the customer.</span></span>|  
    |<span data-ttu-id="6ee44-116">**Kontokode**</span><span class="sxs-lookup"><span data-stu-id="6ee44-116">**Account Code**</span></span>|<span data-ttu-id="6ee44-117">Angi kontokoden for kunden.</span><span class="sxs-lookup"><span data-stu-id="6ee44-117">Enter the account code for the customer.</span></span><br /><br /> <span data-ttu-id="6ee44-118">Kunder i offentlig sektor gir en kontokode når de plasserer en ordre eller rekvisisjon.</span><span class="sxs-lookup"><span data-stu-id="6ee44-118">Customers in the public sector provide an account code when they place an order or requisition.</span></span> <span data-ttu-id="6ee44-119">Basert på verdien i dette feltet, inkluderes kontokoden i EHF-dokumentene du oppretter i [!INCLUDE[prod_short](../../includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="6ee44-119">Based on the value of this field, the account code is included in the EHF documents that you create in [!INCLUDE[prod_short](../../includes/prod_short.md)].</span></span> <span data-ttu-id="6ee44-120">Se Kontokode for mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="6ee44-120">For more information, see Account Code.</span></span>|  
    |<span data-ttu-id="6ee44-121">**E-faktura**</span><span class="sxs-lookup"><span data-stu-id="6ee44-121">**E-Invoice**</span></span>|<span data-ttu-id="6ee44-122">Merk av for å bruke elektronisk fakturering med kunden.</span><span class="sxs-lookup"><span data-stu-id="6ee44-122">Select the check box to use electronic invoicing with this customer.</span></span>|  
    |<span data-ttu-id="6ee44-123">**Ansvarssenter**</span><span class="sxs-lookup"><span data-stu-id="6ee44-123">**Responsibility Center**</span></span>|<span data-ttu-id="6ee44-124">Kontroller at ansvarssenteret du har valgt, har angitt en lands-/regionkode.</span><span class="sxs-lookup"><span data-stu-id="6ee44-124">Make sure that the Responsibility Center that you have selected has a Country/Region Code specified.</span></span>|  

<span data-ttu-id="6ee44-125">Disse feltene er spesifikke for EHF.</span><span class="sxs-lookup"><span data-stu-id="6ee44-125">These fields are specific to EHF.</span></span> <span data-ttu-id="6ee44-126">Verdiene brukes i alle EHF-dokumenter du oppretter for denne kunden.</span><span class="sxs-lookup"><span data-stu-id="6ee44-126">The values are used in all EHF documents that you create for this customer.</span></span> <span data-ttu-id="6ee44-127">Hvis du vil ha mer informasjon, se [EHF – Elektronisk fakturering i Norge](ehf-electronic-invoicing-in-norway.md).</span><span class="sxs-lookup"><span data-stu-id="6ee44-127">For more information, see [EHF Electronic Invoicing in Norway](ehf-electronic-invoicing-in-norway.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="6ee44-128">Se også</span><span class="sxs-lookup"><span data-stu-id="6ee44-128">See Also</span></span>  
 <span data-ttu-id="6ee44-129">[Opprette elektroniske dokumenter for EHF](how-to-create-electronic-documents-for-ehf.md) </span><span class="sxs-lookup"><span data-stu-id="6ee44-129">[Create Electronic Documents for EHF](how-to-create-electronic-documents-for-ehf.md) </span></span>  
 [<span data-ttu-id="6ee44-130">Angi EHF</span><span class="sxs-lookup"><span data-stu-id="6ee44-130">Set Up EHF</span></span>](how-to-set-up-ehf.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]