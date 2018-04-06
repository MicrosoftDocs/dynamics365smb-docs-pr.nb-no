---
title: Definere kontantkunder | Microsoft-dokumentasjon
description: Dette emnet beskriver hvordan du definerer kunder som betaler kontant.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/11/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: a72e6ff0a710f2d555c805e4fa28896683a819e9
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-cash-customers"></a><span data-ttu-id="b6d82-103">Definere kontantkunder</span><span class="sxs-lookup"><span data-stu-id="b6d82-103">Set Up Cash Customers</span></span>
<span data-ttu-id="b6d82-104">Du kan ikke opprette en faktura uten å oppgi et kundenummer.</span><span class="sxs-lookup"><span data-stu-id="b6d82-104">You cannot create an invoice without a customer number.</span></span> <span data-ttu-id="b6d82-105">Dette gjelder også ved kontantsalg og selv om ikke har noe å registrere på en kundekonto.</span><span class="sxs-lookup"><span data-stu-id="b6d82-105">This is true, even if you make a cash sale and do not have anything to record in a customer account.</span></span>  

## <a name="to-set-up-a-cash-customer"></a><span data-ttu-id="b6d82-106">Slik definerer du kontantkunder</span><span class="sxs-lookup"><span data-stu-id="b6d82-106">To set up a cash customer</span></span>  
1.  <span data-ttu-id="b6d82-107">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kunde**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b6d82-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customer**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b6d82-108">Opprett et nytt **kundekort**.</span><span class="sxs-lookup"><span data-stu-id="b6d82-108">Create a new **Customer** card.</span></span> <span data-ttu-id="b6d82-109">Hvis du vil ha mer informasjon, kan du se [Registrere nye kunder](sales-how-register-new-customers.md).</span><span class="sxs-lookup"><span data-stu-id="b6d82-109">For more information, see [Register New Customers](sales-how-register-new-customers.md).</span></span>
3.  <span data-ttu-id="b6d82-110">I feltet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="b6d82-110">In the **No.**</span></span> <span data-ttu-id="b6d82-111">-feltet angir du for eksempel **Kontantsalg**.</span><span class="sxs-lookup"><span data-stu-id="b6d82-111">field, enter **Cash**, for example.</span></span>  
4.  <span data-ttu-id="b6d82-112">I feltet **Navn** angir du for eksempel **Kontantsalg**.</span><span class="sxs-lookup"><span data-stu-id="b6d82-112">In the **Name** field, enter **Cash Sale**, for example.</span></span>  
5.  <span data-ttu-id="b6d82-113">På hurtigfanen **Fakturering** fyller du ut feltene **Bokføringsgruppe** og **Bokføringsgruppe - firma**.</span><span class="sxs-lookup"><span data-stu-id="b6d82-113">On the **Invoicing** FastTab, fill in the **Customer Posting Group** and the **Gen. Bus. Posting Group** fields.</span></span>  

 <span data-ttu-id="b6d82-114">Du har nå definert en kunde som har tilstrekkelig med opplysninger til å kunne faktureres.</span><span class="sxs-lookup"><span data-stu-id="b6d82-114">Now you have set up a customer that contains sufficient information for invoicing.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b6d82-115">Du valgte kanskje en bokføringsgruppe som også brukes ved innenlandsk kredittsalg.</span><span class="sxs-lookup"><span data-stu-id="b6d82-115">You may have chosen a posting group that is also used for domestic credit sales.</span></span> <span data-ttu-id="b6d82-116">Hvis du vil oppdatere separate data for kontantsalg, for eksempel, med en spesiell salgskonto eller samlekonto for kunde, kan du opprette ytterligere en bokføringsgruppe for dette formålet.</span><span class="sxs-lookup"><span data-stu-id="b6d82-116">If you want to maintain separate data on cash sales, for example, with a special sales or receivables account, you can set up an extra posting group for this purpose.</span></span>  
>   
>  <span data-ttu-id="b6d82-117">Du må angi et nummer for bokføringsgruppens samlekonto for kunde, selv om saldoen på denne kontoen alltid vil være 0 etter at du bokfører en faktura.</span><span class="sxs-lookup"><span data-stu-id="b6d82-117">You must enter a number for a receivables account for the posting group, even though the balance in this account will always be 0 after you post an invoice.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b6d82-118">Se også</span><span class="sxs-lookup"><span data-stu-id="b6d82-118">See Also</span></span>
[<span data-ttu-id="b6d82-119">Håndtere fordringer</span><span class="sxs-lookup"><span data-stu-id="b6d82-119">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="b6d82-120">[Registrere nye kunder](sales-how-register-new-customers.md)  </span><span class="sxs-lookup"><span data-stu-id="b6d82-120">[Register New Customers](sales-how-register-new-customers.md)  </span></span>  
[<span data-ttu-id="b6d82-121">Finans</span><span class="sxs-lookup"><span data-stu-id="b6d82-121">Finance</span></span>](finance.md)  


