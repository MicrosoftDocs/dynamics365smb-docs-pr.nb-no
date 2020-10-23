---
title: Bruke én mva-kode i kladder
description: I Norge kan du bruke funksjonen for én mva-kode i en kladd, slik at du kan bokføre mva ved hjelp av ett enkelt felt, Mva-kode.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b11a8353616063fa8ee76e19bf698a7ee1b3c84b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3921346"
---
# <a name="use-one-vat-code-in-journals"></a><span data-ttu-id="89d11-103">Bruke én mva-kode i kladder</span><span class="sxs-lookup"><span data-stu-id="89d11-103">Use One VAT Code in Journals</span></span>
<span data-ttu-id="89d11-104">I Norge kan du bruke funksjonen for én mva-kode i en kladd, slik at du kan bokføre mva ved hjelp av ett enkelt felt, **Mva-kode**.</span><span class="sxs-lookup"><span data-stu-id="89d11-104">In Norway, you can use the feature one VAT code in a journal, so that you can post VAT by using a single field, **VAT Code**.</span></span> <span data-ttu-id="89d11-105">Når én mva-kode er konfigurert, er dette en rask måte å fylle ut mva-felt som brukes ofte.</span><span class="sxs-lookup"><span data-stu-id="89d11-105">After it is set up, the one VAT code is a quick way to fill in the commonly used VAT fields.</span></span>  

<span data-ttu-id="89d11-106">For å angi mva-koden for bestillinger og ordrer, må de tilsvarende mva-bokføringsgruppene for firma og mva-bokføringsgruppene for varer defineres.</span><span class="sxs-lookup"><span data-stu-id="89d11-106">To set up the VAT code for purchase orders and sales orders, the corresponding VAT business posting groups and the VAT product posting groups have to be defined.</span></span>  

<span data-ttu-id="89d11-107">Mva-satsen beregnes fra kombinasjonen av mva-firmabokføringsgrupper, kjøperinformasjon og mva-varebokføringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="89d11-107">The VAT rate is calculated from the combination of VAT business posting groups, buyer information, and VAT product posting groups.</span></span>  

## <a name="to-create-a-vat-code"></a><span data-ttu-id="89d11-108">Slik oppretter du en mva-kode:</span><span class="sxs-lookup"><span data-stu-id="89d11-108">To create a VAT code</span></span>  

1.  <span data-ttu-id="89d11-109">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](../../media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **VAT-koder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="89d11-109">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **VAT Codes**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="89d11-110">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="89d11-110">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="89d11-111">Angi opplysninger i feltet **Kode**, **Bokføringstype** og **Beskrivelse** for hver mva-kode.</span><span class="sxs-lookup"><span data-stu-id="89d11-111">Enter information in the **Code**, **General Posting Type**, and **Description** fields for each VAT code.</span></span>  
4.  <span data-ttu-id="89d11-112">Velg **OK**-knappen for å lukke siden **Mva-koder**.</span><span class="sxs-lookup"><span data-stu-id="89d11-112">Choose the **OK** button to close the **VAT Codes** page.</span></span>  

 <span data-ttu-id="89d11-113">Fremgangsmåten nedenfor beskriver mva-bokføringsoppsettet.</span><span class="sxs-lookup"><span data-stu-id="89d11-113">he following procedure explains the VAT posting setup.</span></span>  

## <a name="to-set-up-vat-posting"></a><span data-ttu-id="89d11-114">Slik definerer du mva-bokføring:</span><span class="sxs-lookup"><span data-stu-id="89d11-114">To set up VAT posting</span></span>  

1.  <span data-ttu-id="89d11-115">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](../../media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Mva-bokføringsoppsett**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="89d11-115">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **VAT Posting Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="89d11-116">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="89d11-116">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="89d11-117">I kortet **Mva-bokføringsoppsett** må du fylle ut følgende felt:</span><span class="sxs-lookup"><span data-stu-id="89d11-117">In the **VAT Posting Setup** card, fill in the following fields:</span></span>  

    - <span data-ttu-id="89d11-118">**Mva-bokføringsgruppe - firma**</span><span class="sxs-lookup"><span data-stu-id="89d11-118">**VAT Business Posting Group**</span></span>  
    - <span data-ttu-id="89d11-119">**Mva-bokføringsgruppe - vare**</span><span class="sxs-lookup"><span data-stu-id="89d11-119">**VAT Product Posting Group**</span></span>  
    - <span data-ttu-id="89d11-120">**Mva-type**</span><span class="sxs-lookup"><span data-stu-id="89d11-120">**VAT Identifier**</span></span>  
    - <span data-ttu-id="89d11-121">**Mva-prosent**</span><span class="sxs-lookup"><span data-stu-id="89d11-121">**VAT Percentage**</span></span>  
    - <span data-ttu-id="89d11-122">**Utgående mva-konto**</span><span class="sxs-lookup"><span data-stu-id="89d11-122">**Sales VAT Account**</span></span>  
    - <span data-ttu-id="89d11-123">**Inngående mva-konto**</span><span class="sxs-lookup"><span data-stu-id="89d11-123">**Purchase VAT Account**</span></span>  

4.  <span data-ttu-id="89d11-124">I feltet **Mva-kode** velger du en kode fra listen.</span><span class="sxs-lookup"><span data-stu-id="89d11-124">In the **VAT Code** field, select a code from the list.</span></span>  

<span data-ttu-id="89d11-125">Nå når du bokfører et dokument i finanskladden og lukker det, brukes informasjonen som er angitt i **Mva-bokføringsoppsett**-kortet.</span><span class="sxs-lookup"><span data-stu-id="89d11-125">Now, when you post a document in the general journal and close it, the information specified in the **VAT Posting Setup** card is applied.</span></span>  

<span data-ttu-id="89d11-126">For eksempel: mva-satsen som er bokført i kladden, defineres av oppsettet du har angitt på **Mva-bokføringsoppsett**-siden.</span><span class="sxs-lookup"><span data-stu-id="89d11-126">For example, the VAT rate posted in the journal is defined by the setup that you have specified on the **VAT Posting Setup** page.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="89d11-127">Feltet **Mva-kode** og **Motkonto-mva. - kode** er lagt til i kladden.</span><span class="sxs-lookup"><span data-stu-id="89d11-127">The **VAT Code** and the **Bal. VAT Code**  fields have been added to the journal.</span></span> <span data-ttu-id="89d11-128">**Motkonto-mva. - kode** er mva-koden som brukes til å beregne motkontoen.</span><span class="sxs-lookup"><span data-stu-id="89d11-128">The **Bal. VAT Code** is the VAT code that is used to calculate the balancing account.</span></span>  
>   
>  <span data-ttu-id="89d11-129">Det gjøres ingen endringer i bokføringen.</span><span class="sxs-lookup"><span data-stu-id="89d11-129">No changes are made to the posting.</span></span>  

## <a name="see-also"></a><span data-ttu-id="89d11-130">Se også</span><span class="sxs-lookup"><span data-stu-id="89d11-130">See Also</span></span>  
 [<span data-ttu-id="89d11-131">Norske mva-koder</span><span class="sxs-lookup"><span data-stu-id="89d11-131">Norwegian VAT Codes</span></span>](norwegian-vat-codes.md)
