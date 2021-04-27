---
title: Opprette KID-numre for salgsdokumenter
description: Kunde-ID (KID) er et kundeidentifikasjonsnummer som inneholder en betalingsreferanse til leverandøren, og sikrer at betalingen bokføres riktig hos leverandøren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8d85edf557e7ff52244859f89b7ec13ae13eaa08
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782197"
---
# <a name="set-up-kid-numbers-on-sales-documents"></a><span data-ttu-id="ed532-103">Opprette KID-numre på salgsdokumenter</span><span class="sxs-lookup"><span data-stu-id="ed532-103">Set Up KID Numbers on Sales Documents</span></span>
<span data-ttu-id="ed532-104">Kunde-ID (KID) er et kundeidentifikasjonsnummer som inneholder en betalingsreferanse til leverandøren, og sikrer at betalingen bokføres riktig hos leverandøren.</span><span class="sxs-lookup"><span data-stu-id="ed532-104">Kunde ID (KID) is a customer identification number that provides a payment reference to the vendor and ensures that the vendor is posting the payment correctly.</span></span> <span data-ttu-id="ed532-105">Du kan opprette KID-numre på salgsdokumenter for å identifisere bilags- og kundeinformasjon ved elektroniske banktransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="ed532-105">You can set up KID numbers on sales documents to identify document and customer information on electronic banking transactions.</span></span>  

## <a name="to-set-up-kid-numbers-on-sales-documents"></a><span data-ttu-id="ed532-106">Slik oppretter du KID-numre på salgsdokumenter</span><span class="sxs-lookup"><span data-stu-id="ed532-106">To set up KID numbers on sales documents</span></span>  

1.  <span data-ttu-id="ed532-107">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](../../media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgsoppsett**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="ed532-107">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ed532-108">I hurtigfanen **Dokumenter** fyller du ut feltene som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="ed532-108">On the **Documents** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="ed532-109">Felt</span><span class="sxs-lookup"><span data-stu-id="ed532-109">Field</span></span>|<span data-ttu-id="ed532-110">Description</span><span class="sxs-lookup"><span data-stu-id="ed532-110">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="ed532-111">**KID-oppsett**</span><span class="sxs-lookup"><span data-stu-id="ed532-111">**KID Setup**</span></span>|<span data-ttu-id="ed532-112">Angir et KID-nummerformat.</span><span class="sxs-lookup"><span data-stu-id="ed532-112">Specifies a KID number format.</span></span>|  
    |<span data-ttu-id="ed532-113">**Bilagsnr.lengde**</span><span class="sxs-lookup"><span data-stu-id="ed532-113">**Document No. length**</span></span>|<span data-ttu-id="ed532-114">Angi hvor mange sifre som skal brukes i bilagsnummeret.</span><span class="sxs-lookup"><span data-stu-id="ed532-114">Enter the number of digits used for the document number.</span></span>|  
    |<span data-ttu-id="ed532-115">**Kundenr.lengde**</span><span class="sxs-lookup"><span data-stu-id="ed532-115">**Customer No. length**</span></span>|<span data-ttu-id="ed532-116">Angi hvor mange sifre som skal brukes i kundenummeret.</span><span class="sxs-lookup"><span data-stu-id="ed532-116">Enter the number of digits used for the customer number.</span></span>|  
    |<span data-ttu-id="ed532-117">**Bruk KID på rentenota**</span><span class="sxs-lookup"><span data-stu-id="ed532-117">**Use KID on Fin. Charge Memo**</span></span>|<span data-ttu-id="ed532-118">Velg å skrive ut KID-numre på rentenotaer.</span><span class="sxs-lookup"><span data-stu-id="ed532-118">Select to print KID numbers on finance charge memos.</span></span> <span data-ttu-id="ed532-119">**Obs!**  Hvis dette alternativet er valgt, må du også velge formatet **Bilagstype + bilagsnr.** i feltet **KID-oppsett**.</span><span class="sxs-lookup"><span data-stu-id="ed532-119">**Note:**  If selected, then you must also select the **Document Type + Document No.** format in the **KID Setup** field.</span></span>|  
    |<span data-ttu-id="ed532-120">**Bruk KID på purring**</span><span class="sxs-lookup"><span data-stu-id="ed532-120">**Use KID on Reminder**</span></span>|<span data-ttu-id="ed532-121">Velg å skrive ut KID-numre på purringer.</span><span class="sxs-lookup"><span data-stu-id="ed532-121">Select to print KID numbers on reminders.</span></span> <span data-ttu-id="ed532-122">**Obs!**  Hvis dette alternativet er valgt, må du også velge formatet **Bilagstype + bilagsnr.** i feltet **KID-oppsett**.</span><span class="sxs-lookup"><span data-stu-id="ed532-122">**Note:**  If selected, then you must also select the **Document Type + Document No.** format in the **KID Setup** field.</span></span>|

3.  <span data-ttu-id="ed532-123">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="ed532-123">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ed532-124">Se også</span><span class="sxs-lookup"><span data-stu-id="ed532-124">See Also</span></span>  
 [<span data-ttu-id="ed532-125">Elektroniske banktjenester i Norge</span><span class="sxs-lookup"><span data-stu-id="ed532-125">Electronic Banking in Norway</span></span>](electronic-banking-in-norway.md) 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]