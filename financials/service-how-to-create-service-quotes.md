---
title: Opprette servicetilbud | Microsoft-dokumentasjon
description: "Du kan bruke vinduet **Servicetilbud** til å opprette dokumenter der du angir opplysninger om en service, for eksempel reparasjon og vedlikehold, på servicevarer etter forespørsel fra kunde. Du kan bruke et servicetilbud som et foreløpig utkast til en serviceordre, og deretter konvertere tilbudet til en serviceordre."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d5348e7b15eb0337f2a5f829c871dadcf3133b86
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-service-quotes"></a><span data-ttu-id="4eaf8-104">Opprette servicetilbud</span><span class="sxs-lookup"><span data-stu-id="4eaf8-104">How to: Create Service Quotes</span></span>
<span data-ttu-id="4eaf8-105">Du kan betrakte servicetilbud som grunnlag for serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="4eaf8-105">You can think of service quotes as the basis for service orders.</span></span> <span data-ttu-id="4eaf8-106">De er faktisk omtrent like.</span><span class="sxs-lookup"><span data-stu-id="4eaf8-106">In fact, they are almost identical.</span></span> <span data-ttu-id="4eaf8-107">Begge inneholder opplysninger som hvem kunden er, ordretype, varen som trenger service, fakturerings- og leveringsopplysninger og informasjon om det faktiske servicearbeidet.</span><span class="sxs-lookup"><span data-stu-id="4eaf8-107">They both contain information such as who the customer is, the type of order, the item that needs service, billing and shipping information, and information about the actual service work.</span></span>
 
<span data-ttu-id="4eaf8-108">Du kan bruke et servicetilbud som et foreløpig utkast til en serviceordre, og deretter konvertere tilbudet til en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="4eaf8-108">You can use a service quote as a preliminary draft for a service order, and then convert the quote to a service order.</span></span>  
  
## <a name="to-create-a-service-quote"></a><span data-ttu-id="4eaf8-109">Slik oppretter du et servicetilbud</span><span class="sxs-lookup"><span data-stu-id="4eaf8-109">To create a service quote</span></span>  
1. <span data-ttu-id="4eaf8-110">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Servicetilbud**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="4eaf8-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Quotes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4eaf8-111">Opprett et nytt servicetilbud.</span><span class="sxs-lookup"><span data-stu-id="4eaf8-111">Create a new service quote.</span></span>  
3. <span data-ttu-id="4eaf8-112">I **Nr.**</span><span class="sxs-lookup"><span data-stu-id="4eaf8-112">In the **No.**</span></span> <span data-ttu-id="4eaf8-113">-feltet angir du et nummer for servicetilbudet.</span><span class="sxs-lookup"><span data-stu-id="4eaf8-113">field, enter a number for the service quote.</span></span> <span data-ttu-id="4eaf8-114">Hvis du har definert en nummerserie for servicetilbud i vinduet **Serviceoppsett**, kan du eventuelt trykke Enter for å velge det neste tilgjengelige servicetilbudsnummeret.</span><span class="sxs-lookup"><span data-stu-id="4eaf8-114">Alternatively, if you have set up a number series for service quotes in the **Service Mgt. Setup** window, you can press Enter to select the next available service quote number.</span></span>  
4. <span data-ttu-id="4eaf8-115">I feltet **Kundenr.**</span><span class="sxs-lookup"><span data-stu-id="4eaf8-115">In the **Customer No.**</span></span>  <span data-ttu-id="4eaf8-116">-feltet velger du den aktuelle kunden fra listen.</span><span class="sxs-lookup"><span data-stu-id="4eaf8-116">field, select the relevant customer from the list.</span></span>  

  > [!Note]  
  >  <span data-ttu-id="4eaf8-117">Kundefeltene fylles ut automatisk med informasjonen fra **Kunde**-kortet.</span><span class="sxs-lookup"><span data-stu-id="4eaf8-117">The customer fields are filled in automatically with information from the **Customer** card.</span></span> <span data-ttu-id="4eaf8-118">Hvis et **Kunde**-kort ikke finnes for kunden og du har definert en kundemal, kan du opprette kunden fra servicetilbudet.</span><span class="sxs-lookup"><span data-stu-id="4eaf8-118">If a **Customer** card does not exist for the customer, and you have set up a customer template, you can create the customer from the service quote.</span></span> <span data-ttu-id="4eaf8-119">Fyll ut de relevante feltene, og velg deretter handlingen **Opprett kunde**.</span><span class="sxs-lookup"><span data-stu-id="4eaf8-119">Fill in the relevant fields, and then choose the **Create Customer** action.</span></span>  
  
5. <span data-ttu-id="4eaf8-120">Avhengig av innstillingene på hurtigfanen **Obligatoriske felt** i vinduet **Serviceoppsett** kan det hende du må fylle ut feltet **Serviceordretype** og **Selgerkode**.</span><span class="sxs-lookup"><span data-stu-id="4eaf8-120">Depending on the settings on the **Mandatory Fields** FastTab in the **Service Mgt. Setup** window, you may need to fill in the **Service Order Type** field and the **Salesperson Code** field.</span></span>  
6. <span data-ttu-id="4eaf8-121">Fylle ut servicevarelinjene.</span><span class="sxs-lookup"><span data-stu-id="4eaf8-121">Fill in the service item lines.</span></span>  
7. <span data-ttu-id="4eaf8-122">Registrere beregnet kost i servicelinjene.</span><span class="sxs-lookup"><span data-stu-id="4eaf8-122">Register estimated costs on the service lines.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4eaf8-123">Se også</span><span class="sxs-lookup"><span data-stu-id="4eaf8-123">See Also</span></span>  
[<span data-ttu-id="4eaf8-124">Opprette serviceordrer</span><span class="sxs-lookup"><span data-stu-id="4eaf8-124">How to: Create Service Orders</span></span>](service-how-to-create-service-orders.md)  
[<span data-ttu-id="4eaf8-125">Arbeide med serviceoppgaver</span><span class="sxs-lookup"><span data-stu-id="4eaf8-125">How to: Work on Service tasks</span></span>](service-how-to-work-on-service-tasks.md)  

 
