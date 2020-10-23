---
title: Definere kontantkunder | Microsoft-dokumentasjon
description: Dette emnet beskriver hvordan du definerer kunder som betaler kontant.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a4f73de177129f5bc33808e6acf74bd273ae0d33
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915563"
---
# <a name="set-up-cash-customers"></a><span data-ttu-id="4c1e9-103">Definere kontantkunder</span><span class="sxs-lookup"><span data-stu-id="4c1e9-103">Set Up Cash Customers</span></span>
<span data-ttu-id="4c1e9-104">Du kan ikke opprette en faktura uten å oppgi et kundenummer.</span><span class="sxs-lookup"><span data-stu-id="4c1e9-104">You cannot create an invoice without a customer number.</span></span> <span data-ttu-id="4c1e9-105">Dette gjelder også ved kontantsalg og selv om ikke har noe å registrere på en kundekonto.</span><span class="sxs-lookup"><span data-stu-id="4c1e9-105">This is true, even if you make a cash sale and do not have anything to record in a customer account.</span></span>  

## <a name="to-set-up-a-cash-customer"></a><span data-ttu-id="4c1e9-106">Slik definerer du kontantkunder</span><span class="sxs-lookup"><span data-stu-id="4c1e9-106">To set up a cash customer</span></span>  
1.  <span data-ttu-id="4c1e9-107">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunde**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="4c1e9-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4c1e9-108">Opprett et nytt **kundekort**.</span><span class="sxs-lookup"><span data-stu-id="4c1e9-108">Create a new **Customer** card.</span></span> <span data-ttu-id="4c1e9-109">Hvis du vil ha mer informasjon, kan du se [Registrere nye kunder](sales-how-register-new-customers.md).</span><span class="sxs-lookup"><span data-stu-id="4c1e9-109">For more information, see [Register New Customers](sales-how-register-new-customers.md).</span></span>
3.  <span data-ttu-id="4c1e9-110">I feltet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="4c1e9-110">In the **No.**</span></span> <span data-ttu-id="4c1e9-111">-feltet angir du for eksempel **Kontantsalg**.</span><span class="sxs-lookup"><span data-stu-id="4c1e9-111">field, enter **Cash**, for example.</span></span>  
4.  <span data-ttu-id="4c1e9-112">I feltet **Navn** angir du for eksempel **Kontantsalg**.</span><span class="sxs-lookup"><span data-stu-id="4c1e9-112">In the **Name** field, enter **Cash Sale**, for example.</span></span>  
5.  <span data-ttu-id="4c1e9-113">På hurtigfanen **Fakturering** fyller du ut feltene **Bokføringsgruppe** og **Bokføringsgruppe - firma**.</span><span class="sxs-lookup"><span data-stu-id="4c1e9-113">On the **Invoicing** FastTab, fill in the **Customer Posting Group** and the **Gen. Bus. Posting Group** fields.</span></span>  

 <span data-ttu-id="4c1e9-114">Du har nå definert en kunde som har tilstrekkelig med opplysninger til å kunne faktureres.</span><span class="sxs-lookup"><span data-stu-id="4c1e9-114">Now you have set up a customer that contains sufficient information for invoicing.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="4c1e9-115">Du valgte kanskje en bokføringsgruppe som også brukes ved innenlandsk kredittsalg.</span><span class="sxs-lookup"><span data-stu-id="4c1e9-115">You may have chosen a posting group that is also used for domestic credit sales.</span></span> <span data-ttu-id="4c1e9-116">Hvis du vil oppdatere separate data for kontantsalg, for eksempel, med en spesiell salgskonto eller samlekonto for kunde, kan du opprette ytterligere en bokføringsgruppe for dette formålet.</span><span class="sxs-lookup"><span data-stu-id="4c1e9-116">If you want to maintain separate data on cash sales, for example, with a special sales or receivables account, you can set up an extra posting group for this purpose.</span></span>  
>   
>  <span data-ttu-id="4c1e9-117">Du må angi et nummer for bokføringsgruppens samlekonto for kunde, selv om saldoen på denne kontoen alltid vil være 0 etter at du bokfører en faktura.</span><span class="sxs-lookup"><span data-stu-id="4c1e9-117">You must enter a number for a receivables account for the posting group, even though the balance in this account will always be 0 after you post an invoice.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4c1e9-118">Se også</span><span class="sxs-lookup"><span data-stu-id="4c1e9-118">See Also</span></span>
[<span data-ttu-id="4c1e9-119">Håndtere fordringer</span><span class="sxs-lookup"><span data-stu-id="4c1e9-119">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="4c1e9-120">[Registrere nye kunder](sales-how-register-new-customers.md)  </span><span class="sxs-lookup"><span data-stu-id="4c1e9-120">[Register New Customers](sales-how-register-new-customers.md)  </span></span>  
[<span data-ttu-id="4c1e9-121">Finans</span><span class="sxs-lookup"><span data-stu-id="4c1e9-121">Finance</span></span>](finance.md)  

