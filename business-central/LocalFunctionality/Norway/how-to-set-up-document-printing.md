---
title: Definere dokumentutskrift
description: I Business Central kan du skrive ut salgsrapportene som bruker de nødvendige girospesifikasjonene, ved bruk av forskjellige papirtyper og -skuffer.
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
ms.openlocfilehash: 1d708dd032551bccfdbf98d5186498e988ed3e99
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "826955"
---
# <a name="set-up-document-printing"></a><span data-ttu-id="57d34-103">Definere dokumentutskrift</span><span class="sxs-lookup"><span data-stu-id="57d34-103">Set Up Document Printing</span></span>
<span data-ttu-id="57d34-104">I [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kan du skrive ut salgsrapportene som bruker de nødvendige girospesifikasjonene, ved bruk av forskjellige papirtyper og -skuffer.</span><span class="sxs-lookup"><span data-stu-id="57d34-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can print the sales reports that use the required giro specifications by using different paper types and paper trays.</span></span>  

<span data-ttu-id="57d34-105">Du må vurdere hvordan skriveren og skriverdriveren tolker denne informasjonen når du bruker skuffnumre og papirkilder for norske salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="57d34-105">When you use tray numbers and paper sources for Norwegian sales documents, you must consider how the printer and printer driver interpret this information.</span></span> <span data-ttu-id="57d34-106">Du må kanskje angi andre skuffnumre for din spesifikke skriver.</span><span class="sxs-lookup"><span data-stu-id="57d34-106">You may have to specify other tray numbers for your specific printer.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="57d34-107">KID-informasjon skrives også ut der giroopplysningene skrives ut.</span><span class="sxs-lookup"><span data-stu-id="57d34-107">KID information will also print where the giro information is printed.</span></span>  

<span data-ttu-id="57d34-108">Følgende dokumenter krever en utskrevet giro:</span><span class="sxs-lookup"><span data-stu-id="57d34-108">The following documents require a printed giro:</span></span>  

- <span data-ttu-id="57d34-109">Fakturaer</span><span class="sxs-lookup"><span data-stu-id="57d34-109">Invoices</span></span>  
- <span data-ttu-id="57d34-110">Kreditnotaer</span><span class="sxs-lookup"><span data-stu-id="57d34-110">Credit memos</span></span>  
- <span data-ttu-id="57d34-111">Rentenotaer</span><span class="sxs-lookup"><span data-stu-id="57d34-111">Finance charge memos</span></span>  
- <span data-ttu-id="57d34-112">Purringer</span><span class="sxs-lookup"><span data-stu-id="57d34-112">Reminders</span></span>  

<span data-ttu-id="57d34-113">Den norske versjonen av [!INCLUDE[d365fin](../../includes/d365fin_md.md)] inneholder følgende sett med salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="57d34-113">The Norwegian version of [!INCLUDE[d365fin](../../includes/d365fin_md.md)] contains the following sets of sales documents.</span></span>  

|<span data-ttu-id="57d34-114">**Valg**</span><span class="sxs-lookup"><span data-stu-id="57d34-114">**Set**</span></span>|<span data-ttu-id="57d34-115">Description</span><span class="sxs-lookup"><span data-stu-id="57d34-115">Description</span></span>|  
|-------------|---------------------------------------|  
|<span data-ttu-id="57d34-116">1</span><span class="sxs-lookup"><span data-stu-id="57d34-116">1</span></span>|<span data-ttu-id="57d34-117">Standard [!INCLUDE[d365fin](../../includes/d365fin_md.md)]-dokumenter.</span><span class="sxs-lookup"><span data-stu-id="57d34-117">The standard [!INCLUDE[d365fin](../../includes/d365fin_md.md)] documents.</span></span> <span data-ttu-id="57d34-118">Ingen giroinformasjon skrives ut.</span><span class="sxs-lookup"><span data-stu-id="57d34-118">No giro information is printed.</span></span>|  
|<span data-ttu-id="57d34-119">2</span><span class="sxs-lookup"><span data-stu-id="57d34-119">2</span></span>|<span data-ttu-id="57d34-120">Giroen skrives ut på hver side.</span><span class="sxs-lookup"><span data-stu-id="57d34-120">The giro is printed on every page.</span></span> <span data-ttu-id="57d34-121">Den siste siden skriver ut girosummen.</span><span class="sxs-lookup"><span data-stu-id="57d34-121">The last page prints the giro total.</span></span>|  

## <a name="to-set-up-paper-trays"></a><span data-ttu-id="57d34-122">Slik definerer du papirskuffer:</span><span class="sxs-lookup"><span data-stu-id="57d34-122">To set up paper trays</span></span>  

1.  <span data-ttu-id="57d34-123">Velg ikonet ![Søk etter side eller rapport](../../media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Skrivervalg**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="57d34-123">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Printer Selections**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="57d34-124">Velg rapporten.</span><span class="sxs-lookup"><span data-stu-id="57d34-124">Select the report.</span></span>  
3.  <span data-ttu-id="57d34-125">Velg handlingen **Salgsdok.arkskuff - oppsett**.</span><span class="sxs-lookup"><span data-stu-id="57d34-125">Choose the **Sales Document Paper Tray Setup** action.</span></span>  
4.  <span data-ttu-id="57d34-126">Velg en papirkilde i **Første side - papirkilde**-feltet.</span><span class="sxs-lookup"><span data-stu-id="57d34-126">Select a paper source from the **First Page - Paper Source** field.</span></span>  
5.  <span data-ttu-id="57d34-127">Feltet **Første side - skuffnr.** viser automatisk den valgte papirkilden.</span><span class="sxs-lookup"><span data-stu-id="57d34-127">The **First Page – Tray Number** field will automatically display the selected paper source.</span></span> <span data-ttu-id="57d34-128">Du kan også angi et skuffnummer manuelt.</span><span class="sxs-lookup"><span data-stu-id="57d34-128">You can also manually enter a tray number.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="57d34-129">Ikke alle skrivere har samme papirkildenavn.</span><span class="sxs-lookup"><span data-stu-id="57d34-129">Not all printers will have the same paper source names.</span></span> <span data-ttu-id="57d34-130">Du kan angi et nummer i feltet **Skuffnr.**.</span><span class="sxs-lookup"><span data-stu-id="57d34-130">You can specify a number in the **Tray Number** field.</span></span> <span data-ttu-id="57d34-131">Nummeret kan tilsvare en papirkilde.</span><span class="sxs-lookup"><span data-stu-id="57d34-131">The number may correspond to a paper source.</span></span> <span data-ttu-id="57d34-132">Du finner nummeret som en bestemt skriver bruker, i den tekniske dokumentasjonen for skriveren.</span><span class="sxs-lookup"><span data-stu-id="57d34-132">To find the number that a specific printer is using, see the technical documentation for the printer.</span></span>  

    <span data-ttu-id="57d34-133">Feltet **Andre sider** og **Giroside** defineres på samme måte.</span><span class="sxs-lookup"><span data-stu-id="57d34-133">The **Other Pages** and **Giro Page** fields are set up the same way.</span></span>  

6.  <span data-ttu-id="57d34-134">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="57d34-134">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="57d34-135">Se også</span><span class="sxs-lookup"><span data-stu-id="57d34-135">See Also</span></span>  
  <span data-ttu-id="57d34-136">[Norsk giro og OCR-B-skrift](norwegian-giro-and-ocr-b-font.md) </span><span class="sxs-lookup"><span data-stu-id="57d34-136">[Norwegian Giro and OCR-B Font](norwegian-giro-and-ocr-b-font.md) </span></span>  
 [<span data-ttu-id="57d34-137">Opprette KID-numre på salgsdokumenter</span><span class="sxs-lookup"><span data-stu-id="57d34-137">Set Up KID Numbers on Sales Documents</span></span>](how-to-set-up-kid-numbers-on-sales-documents.md)