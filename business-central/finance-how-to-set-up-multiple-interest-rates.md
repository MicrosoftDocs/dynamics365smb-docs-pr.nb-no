---
title: Angi flere rentesatser
description: Du kan beregne rentebelastning med flere rentesatser for en bestemt periode. Renteberegningen fungerer på samme måte for alle rentebelastninger. Det er bare satsen for renten for en bestemt periode som varierer.
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
ms.openlocfilehash: 85e295997089ea10b956fe0a5d087652c190fb44
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802705"
---
# <a name="set-up-multiple-interest-rates"></a><span data-ttu-id="b165f-104">Angi flere rentesatser.</span><span class="sxs-lookup"><span data-stu-id="b165f-104">Set Up Multiple Interest Rates</span></span>
<span data-ttu-id="b165f-105">Flere rentesatser brukes for forskjellige perioder for forsinkede betalinger handelstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="b165f-105">Multiple interest rates are used for different periods for delayed payments in trade transactions.</span></span> <span data-ttu-id="b165f-106">For eksempel angir en offentlig myndighet maksimal rente som kan pålegges for en kunde.</span><span class="sxs-lookup"><span data-stu-id="b165f-106">For example, a government specifies the maximum interest to be levied for a consumer.</span></span> <span data-ttu-id="b165f-107">Denne rentesatsen kan endres to ganger i året, 1. januar og 1. juli.</span><span class="sxs-lookup"><span data-stu-id="b165f-107">This interest rate can be changed twice a year on 01 January and 01 July.</span></span> <span data-ttu-id="b165f-108">Rentesatsen mellom bedrifter (B2B) avtales av partene, og det er ingen begrensning for denne kundegruppen.</span><span class="sxs-lookup"><span data-stu-id="b165f-108">The interest rate between businesses (B2B) is agreed by the parties and there is no limit to that customer group.</span></span> <span data-ttu-id="b165f-109">Annonsert sats er vanligvis 4 % mer enn vanlig bankrente.</span><span class="sxs-lookup"><span data-stu-id="b165f-109">The announced rate is usually four percent more than the normal bank interest.</span></span>

<span data-ttu-id="b165f-110">Når du oppretter rentenotabetingelser og purrebetingelser for straff for forsinket betaling, kan du angi flere rentesatser slik at straffegebyret beregnes fra forskjellige renter i forskjellige perioder.</span><span class="sxs-lookup"><span data-stu-id="b165f-110">When you create finance charge terms and reminder terms, for delayed payment penalty, you can specify multiple interest rates so that the penalty fee is calculated from different interest rates in different periods.</span></span> <span data-ttu-id="b165f-111">Hvis du vil ha mer informasjon, kan du se [Innkreve utestående saldi](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="b165f-111">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>

## <a name="to-set-up-multiple-interest-rates"></a><span data-ttu-id="b165f-112">Angi flere rentesatser</span><span class="sxs-lookup"><span data-stu-id="b165f-112">To set up multiple interest rates</span></span>  
1.  <span data-ttu-id="b165f-113">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rentenotabetingelser**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b165f-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Finance Charge Terms**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b165f-114">På siden **Rentenotabetingelser** velger du den nødvendige rentebetingelsen, og deretter handlingen **Rentesatser**.</span><span class="sxs-lookup"><span data-stu-id="b165f-114">On the **Finance Charge Terms** page, select the required finance term, and then choose the **Interest Rates** action.</span></span>  
3.  <span data-ttu-id="b165f-115">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="b165f-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  <span data-ttu-id="b165f-116">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b165f-116">Choose the **OK** button.</span></span>  
5.  <span data-ttu-id="b165f-117">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Purrebetingelser**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b165f-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Reminder Terms**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="b165f-118">På siden **Purrebetingelser** velger du den nødvendige purrebetingelsen, og deretter handlingen **Nivåer**.</span><span class="sxs-lookup"><span data-stu-id="b165f-118">On the **Reminder Terms** page, select the required reminder term, and then choose the **Levels** action.</span></span>  
7.  <span data-ttu-id="b165f-119">På siden **Purregrader** velger du **Beregn renter**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b165f-119">On the **Reminder Levels** page, select the **Calculate Interest** field.</span></span>  

<span data-ttu-id="b165f-120">Når du utsteder en rentenota, viser den rentebelastningene med flere rentesatser for en bestemt tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="b165f-120">When you issue a finance charge memo, the memo shows the finance charges with multiple interest rates for a specific time period.</span></span> <span data-ttu-id="b165f-121">Notaen inneholder også kontaktdetaljer for kunden, selskapet som utsteder notaen, tilleggsbeløpet og det totale beløpet.</span><span class="sxs-lookup"><span data-stu-id="b165f-121">The memo also contains the contact details of the customer, the company issuing the memo, the additional amount, and the total amount.</span></span> <span data-ttu-id="b165f-122">Åpningsposten på rentenotaen vises med fet skrift.</span><span class="sxs-lookup"><span data-stu-id="b165f-122">The opening entry on the memo is displayed in bold.</span></span> <span data-ttu-id="b165f-123">Rentebelastningen beregnes med flere rentesatser for en bestemt tidsperiode, og skrives ut etter åpningsposten for rentenotaen.</span><span class="sxs-lookup"><span data-stu-id="b165f-123">The finance charges are calculated with multiple interest rates for a specific time period and are printed after the opening entry of the memo.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b165f-124">Se også</span><span class="sxs-lookup"><span data-stu-id="b165f-124">See Also</span></span>  
[<span data-ttu-id="b165f-125">Innkreve utestående saldi</span><span class="sxs-lookup"><span data-stu-id="b165f-125">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="b165f-126">Konfigurere finans</span><span class="sxs-lookup"><span data-stu-id="b165f-126">Setting Up Finance</span></span>](finance-setup-finance.md)