---
title: Opprette servicetilbud | Microsoft-dokumentasjon
description: Du kan bruke siden **Servicetilbud** til å opprette dokumenter der du angir opplysninger om en service, for eksempel reparasjon og vedlikehold, på servicevarer etter forespørsel fra kunde. Du kan bruke et servicetilbud som et foreløpig utkast til en serviceordre, og deretter konvertere tilbudet til en serviceordre.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 44ffab92930237c5496860771f41b4951b15b0ff
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250667"
---
# <a name="create-service-quotes"></a><span data-ttu-id="65487-104">Opprette servicetilbud</span><span class="sxs-lookup"><span data-stu-id="65487-104">Create Service Quotes</span></span>
<span data-ttu-id="65487-105">Du kan betrakte servicetilbud som grunnlag for serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="65487-105">You can think of service quotes as the basis for service orders.</span></span> <span data-ttu-id="65487-106">De er faktisk omtrent like.</span><span class="sxs-lookup"><span data-stu-id="65487-106">In fact, they are almost identical.</span></span> <span data-ttu-id="65487-107">Begge inneholder opplysninger som hvem kunden er, ordretype, varen som trenger service, fakturerings- og leveringsopplysninger og informasjon om det faktiske servicearbeidet.</span><span class="sxs-lookup"><span data-stu-id="65487-107">They both contain information such as who the customer is, the type of order, the item that needs service, billing and shipping information, and information about the actual service work.</span></span>
 
<span data-ttu-id="65487-108">Du kan bruke et servicetilbud som et foreløpig utkast til en serviceordre, og deretter konvertere tilbudet til en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="65487-108">You can use a service quote as a preliminary draft for a service order, and then convert the quote to a service order.</span></span>  
  
## <a name="to-create-a-service-quote"></a><span data-ttu-id="65487-109">Slik oppretter du et servicetilbud</span><span class="sxs-lookup"><span data-stu-id="65487-109">To create a service quote</span></span>  
1. <span data-ttu-id="65487-110">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicetilbud**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="65487-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Quotes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="65487-111">Opprett et nytt servicetilbud.</span><span class="sxs-lookup"><span data-stu-id="65487-111">Create a new service quote.</span></span>  
3. <span data-ttu-id="65487-112">I **Nr.**</span><span class="sxs-lookup"><span data-stu-id="65487-112">In the **No.**</span></span> <span data-ttu-id="65487-113">-feltet angir du et nummer for servicetilbudet.</span><span class="sxs-lookup"><span data-stu-id="65487-113">field, enter a number for the service quote.</span></span> <span data-ttu-id="65487-114">Hvis du har definert en nummerserie for servicetilbud på siden **Serviceoppsett**, kan du eventuelt trykke Enter for å velge det neste tilgjengelige servicetilbudsnummeret.</span><span class="sxs-lookup"><span data-stu-id="65487-114">Alternatively, if you have set up a number series for service quotes on the **Service Mgt. Setup** page, you can press Enter to select the next available service quote number.</span></span>  
4. <span data-ttu-id="65487-115">I feltet **Kundenr.**</span><span class="sxs-lookup"><span data-stu-id="65487-115">In the **Customer No.**</span></span>  <span data-ttu-id="65487-116">-feltet velger du den aktuelle kunden fra listen.</span><span class="sxs-lookup"><span data-stu-id="65487-116">field, select the relevant customer from the list.</span></span>  

  > [!Note]  
  >  <span data-ttu-id="65487-117">Kundefeltene fylles ut automatisk med informasjonen fra **Kunde**-kortet.</span><span class="sxs-lookup"><span data-stu-id="65487-117">The customer fields are filled in automatically with information from the **Customer** card.</span></span> <span data-ttu-id="65487-118">Hvis et **Kunde**-kort ikke finnes for kunden og du har definert en kundemal, kan du opprette kunden fra servicetilbudet.</span><span class="sxs-lookup"><span data-stu-id="65487-118">If a **Customer** card does not exist for the customer, and you have set up a customer template, you can create the customer from the service quote.</span></span> <span data-ttu-id="65487-119">Fyll ut de relevante feltene, og velg deretter handlingen **Opprett kunde**.</span><span class="sxs-lookup"><span data-stu-id="65487-119">Fill in the relevant fields, and then choose the **Create Customer** action.</span></span>  
  
5. <span data-ttu-id="65487-120">Avhengig av innstillingene på hurtigfanen **Obligatoriske felt** på siden **Serviceoppsett** kan det hende du må fylle ut feltet **Serviceordretype** og **Selgerkode**.</span><span class="sxs-lookup"><span data-stu-id="65487-120">Depending on the settings on the **Mandatory Fields** FastTab on the **Service Mgt. Setup** page, you may need to fill in the **Service Order Type** field and the **Salesperson Code** field.</span></span>  
6. <span data-ttu-id="65487-121">Fylle ut servicevarelinjene.</span><span class="sxs-lookup"><span data-stu-id="65487-121">Fill in the service item lines.</span></span>  
7. <span data-ttu-id="65487-122">Registrere beregnet kost i servicelinjene.</span><span class="sxs-lookup"><span data-stu-id="65487-122">Register estimated costs on the service lines.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="65487-123">Se også</span><span class="sxs-lookup"><span data-stu-id="65487-123">See Also</span></span>  
[<span data-ttu-id="65487-124">Opprette serviceordrer</span><span class="sxs-lookup"><span data-stu-id="65487-124">Create Service Orders</span></span>](service-how-to-create-service-orders.md)  
[<span data-ttu-id="65487-125">Arbeide med serviceoppgaver</span><span class="sxs-lookup"><span data-stu-id="65487-125">Work on Service tasks</span></span>](service-how-to-work-on-service-tasks.md)  

 