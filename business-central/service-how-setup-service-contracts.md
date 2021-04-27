---
title: Definere servicekontrakter | Microsoft-dokumentasjon
description: Finn ut hvordan du definerer servicekontrakter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 216bbd775c66fca619d792ff578d198405fc7612
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781534"
---
# <a name="set-up-service-contracts"></a><span data-ttu-id="6129a-103">Definere servicekontrakter</span><span class="sxs-lookup"><span data-stu-id="6129a-103">Set Up Service Contracts</span></span>
<span data-ttu-id="6129a-104">Før du kan arbeide med kontrakter må du definere følgende:</span><span class="sxs-lookup"><span data-stu-id="6129a-104">Before you can work with contracts, you must set up the following:</span></span> 

* <span data-ttu-id="6129a-105">**Servicekontraktgrupper**, som inneholder servicekontrakter som på én eller annen måte er tilknyttet hverandre.</span><span class="sxs-lookup"><span data-stu-id="6129a-105">**Service contract groups**, which gather service contracts that are related in some way.</span></span>
* <span data-ttu-id="6129a-106">**Kontogrupper for servicekontrakter**, som brukes til å gruppere kontoene for servicekontrakter for servicefakturaer som opprettes for servicekontrakter.</span><span class="sxs-lookup"><span data-stu-id="6129a-106">**Service contract account groups**, which are used to group the service contract accounts together for service invoices created for service contracts.</span></span> <span data-ttu-id="6129a-107">Du kan tilordne disse gruppene til servicekontrakter.</span><span class="sxs-lookup"><span data-stu-id="6129a-107">You assign these groups to service contracts.</span></span>  
* <span data-ttu-id="6129a-108">**Kontraktmaler** som definerer oppsett for kontrakter som omfatter de vanligste opplysningene om servicekontrakter.</span><span class="sxs-lookup"><span data-stu-id="6129a-108">**Contract templates** that define contract layouts of contracts that include the most commonly used service contract details.</span></span> <span data-ttu-id="6129a-109">Når du oppretter servicekontrakttilbud, kan du opprette dem ved hjelp av maler.</span><span class="sxs-lookup"><span data-stu-id="6129a-109">When you create service contract quotes, you can create them by using templates.</span></span> <span data-ttu-id="6129a-110">Når du oppretter et kontrakttilbud, innholdet feltene automatisk innholdet i feltene i malen.</span><span class="sxs-lookup"><span data-stu-id="6129a-110">When you create a contract quote, the fields automatically contain the contents of the template fields.</span></span>
* <span data-ttu-id="6129a-111">**Kundemaler** som lar deg opprette tilbud for kontakter eller potensielle kunder som ikke er registrert som kunder i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="6129a-111">**Customer templates** that let you create quotes for contacts or potential customers who are not registered as customers in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

## <a name="to-set-up-a-service-contract-group"></a><span data-ttu-id="6129a-112">Slik definerer du servicekontraktgrupper</span><span class="sxs-lookup"><span data-stu-id="6129a-112">To set up a service contract group</span></span>  
1. <span data-ttu-id="6129a-113">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicekontraktgrupper**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="6129a-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Contract Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6129a-114">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="6129a-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="6129a-115">Merk av for **Rab. bare på kontr. ordrer** hvis du vil at kontrakt- eller servicerabatter bare skal være gyldige for servicekontraktordrer, for eksempel vedlikehold.</span><span class="sxs-lookup"><span data-stu-id="6129a-115">Choose the **Disc. on Contr. Orders Only** check box if you want contract or service discounts to be valid only for contract service orders, such as maintenance.</span></span>  

## <a name="to-set-up-a-service-contract-account-group"></a><span data-ttu-id="6129a-116">Slik definerer du kontogrupper for servicekontrakter</span><span class="sxs-lookup"><span data-stu-id="6129a-116">To set up a service contract account group</span></span>  
1. <span data-ttu-id="6129a-117">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kontogrp. for servicekontr.**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="6129a-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Serv. Contract Account Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6129a-118">Opprett en ny kontogruppe for servicekontrakter.</span><span class="sxs-lookup"><span data-stu-id="6129a-118">Create a new service contract account group.</span></span>   
3. <span data-ttu-id="6129a-119">Fyll ut feltene **Kode** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="6129a-119">Fill in the **Code** and **Description** fields.</span></span> <span data-ttu-id="6129a-120">Disse feltene beskriver servicekontogruppen.</span><span class="sxs-lookup"><span data-stu-id="6129a-120">These fields describe the service account group.</span></span>  
4. <span data-ttu-id="6129a-121">Fyll ut feltet **Ikke-forh.bet. kontraktkonto**, og velg finanskontonummeret for ikke-forhåndsbetalte konti.</span><span class="sxs-lookup"><span data-stu-id="6129a-121">Fill in the **Non-Prepaid Contract Acc.** field, choose general ledger account number for the non-prepaid account.</span></span>  
5. <span data-ttu-id="6129a-122">I feltet **Ikke-forh.bet. kontraktkonto** velger du finanskontonummeret for forhåndsbetalte konti.</span><span class="sxs-lookup"><span data-stu-id="6129a-122">In the **Prepaid Contract Acc.** field, choose the general ledger account number for the prepaid account.</span></span>  

## <a name="to-set-up-a-contract-template"></a><span data-ttu-id="6129a-123">Slik definerer du kontraktmaler</span><span class="sxs-lookup"><span data-stu-id="6129a-123">To set up a contract template</span></span>  
1. <span data-ttu-id="6129a-124">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicekontraktmaler**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="6129a-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Contract Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6129a-125">Opprett en ny servicekontraktmal.</span><span class="sxs-lookup"><span data-stu-id="6129a-125">Create a new service contract template.</span></span>  
3. <span data-ttu-id="6129a-126">I feltet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="6129a-126">In the **No.**</span></span> <span data-ttu-id="6129a-127">-feltet angir du et nummer for kontraktmalen.</span><span class="sxs-lookup"><span data-stu-id="6129a-127">field, enter a number for the contract template.</span></span>  
  
     <span data-ttu-id="6129a-128">Hvis du har definert en nummerserie for kontraktmaler på siden **Serviceoppsett**, kan du eventuelt trykke på Enter-tasten for at programmet skal angi det neste tilgjengelige kontraktmalnummeret.</span><span class="sxs-lookup"><span data-stu-id="6129a-128">Alternatively, if you have set up number series for contract templates on the **Service Mgt. Setup** page, you can press the Enter key to enter the next available contract template number.</span></span> <span data-ttu-id="6129a-129">Fyll eventuelt ut de andre feltene.</span><span class="sxs-lookup"><span data-stu-id="6129a-129">Fill in the other fields if appropriate.</span></span>  
  
4. <span data-ttu-id="6129a-130">I hurtigfanen **Faktura** fyller du ut feltet **Serv.kontr.kontogrp. - kode**, **Fakturaperiode** og så videre.</span><span class="sxs-lookup"><span data-stu-id="6129a-130">On the **Invoice** FastTab, fill in the **Serv. Contract Acc. Group Code** field, the **Invoice Period**, and so on.</span></span> <span data-ttu-id="6129a-131">Fyll eventuelt ut de andre feltene.</span><span class="sxs-lookup"><span data-stu-id="6129a-131">Fill in the other fields if appropriate.</span></span>  
5. <span data-ttu-id="6129a-132">Velg handlingen **Servicerabatter** for å legge til kontraktrabatter.</span><span class="sxs-lookup"><span data-stu-id="6129a-132">Choose the **Service Discounts** action to add contract discounts.</span></span>  

## <a name="to-set-up-a-customer-template"></a><span data-ttu-id="6129a-133">Slik definerer du kundemaler</span><span class="sxs-lookup"><span data-stu-id="6129a-133">To set up a customer template</span></span>  
1. <span data-ttu-id="6129a-134">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kundemaler**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="6129a-134">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6129a-135">Opprett et nytt kundemalkort.</span><span class="sxs-lookup"><span data-stu-id="6129a-135">Create a new customer template card.</span></span>  
3. <span data-ttu-id="6129a-136">På hurtigfanen **Generelt** angir du koden og en beskrivelse for kundemalen i feltene **Kode** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="6129a-136">On the **General** FastTab, enter a code and a description for the customer template in the **Code** and **Description** fields respectively.</span></span> 
4. <span data-ttu-id="6129a-137">Hvis du vil definere søkekriterier, fyller du ut de andre feltene, for eksempel **Lands-/regionkode**, **Distriktskode** og **Språkkode**.</span><span class="sxs-lookup"><span data-stu-id="6129a-137">To define search criteria, fill in the other fields, such as **Country/Region Code**, **Territory Code**, and **Language Code**.</span></span>  
5. <span data-ttu-id="6129a-138">Fyll ut feltene **Bokføringsgruppe - firma** og **Bokføringsgruppe - kunde**.</span><span class="sxs-lookup"><span data-stu-id="6129a-138">Fill in the **Gen. Bus. Posting Group** and **Customer Posting Group** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6129a-139">Se også</span><span class="sxs-lookup"><span data-stu-id="6129a-139">See Also</span></span>
[<span data-ttu-id="6129a-140">Konfigurere servicehåndtering</span><span class="sxs-lookup"><span data-stu-id="6129a-140">Setting Up Service Management</span></span>](service-setup-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]