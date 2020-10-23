---
title: Opprette KID-numre for salgsdokumenter
description: Kunde-ID (KID) er et kundeidentifikasjonsnummer som inneholder en betalingsreferanse til leverandøren, og sikrer at betalingen bokføres riktig hos leverandøren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d98bdfadd8c3a9438b1dae01bb8232932f12e7d4
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919769"
---
# <a name="set-up-kid-numbers-on-sales-documents"></a><span data-ttu-id="64211-103">Opprette KID-numre på salgsdokumenter</span><span class="sxs-lookup"><span data-stu-id="64211-103">Set Up KID Numbers on Sales Documents</span></span>
<span data-ttu-id="64211-104">Kunde-ID (KID) er et kundeidentifikasjonsnummer som inneholder en betalingsreferanse til leverandøren, og sikrer at betalingen bokføres riktig hos leverandøren.</span><span class="sxs-lookup"><span data-stu-id="64211-104">Kunde ID (KID) is a customer identification number that provides a payment reference to the vendor and ensures that the vendor is posting the payment correctly.</span></span> <span data-ttu-id="64211-105">Du kan opprette KID-numre på salgsdokumenter for å identifisere bilags- og kundeinformasjon ved elektroniske banktransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="64211-105">You can set up KID numbers on sales documents to identify document and customer information on electronic banking transactions.</span></span>  

## <a name="to-set-up-kid-numbers-on-sales-documents"></a><span data-ttu-id="64211-106">Slik oppretter du KID-numre på salgsdokumenter</span><span class="sxs-lookup"><span data-stu-id="64211-106">To set up KID numbers on sales documents</span></span>  

1.  <span data-ttu-id="64211-107">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](../../media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgsoppsett**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="64211-107">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="64211-108">I hurtigfanen **Dokumenter** fyller du ut feltene som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="64211-108">On the **Documents** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="64211-109">Felt</span><span class="sxs-lookup"><span data-stu-id="64211-109">Field</span></span>|<span data-ttu-id="64211-110">Description</span><span class="sxs-lookup"><span data-stu-id="64211-110">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="64211-111">**KID-oppsett**</span><span class="sxs-lookup"><span data-stu-id="64211-111">**KID Setup**</span></span>|<span data-ttu-id="64211-112">Angir et KID-nummerformat.</span><span class="sxs-lookup"><span data-stu-id="64211-112">Specifies a KID number format.</span></span>|  
    |<span data-ttu-id="64211-113">**Bilagsnr.lengde**</span><span class="sxs-lookup"><span data-stu-id="64211-113">**Document No. length**</span></span>|<span data-ttu-id="64211-114">Angi hvor mange sifre som skal brukes i bilagsnummeret.</span><span class="sxs-lookup"><span data-stu-id="64211-114">Enter the number of digits used for the document number.</span></span>|  
    |<span data-ttu-id="64211-115">**Kundenr.lengde**</span><span class="sxs-lookup"><span data-stu-id="64211-115">**Customer No. length**</span></span>|<span data-ttu-id="64211-116">Angi hvor mange sifre som skal brukes i kundenummeret.</span><span class="sxs-lookup"><span data-stu-id="64211-116">Enter the number of digits used for the customer number.</span></span>|  
    |<span data-ttu-id="64211-117">**Bruk KID på rentenota**</span><span class="sxs-lookup"><span data-stu-id="64211-117">**Use KID on Fin. Charge Memo**</span></span>|<span data-ttu-id="64211-118">Velg å skrive ut KID-numre på rentenotaer.</span><span class="sxs-lookup"><span data-stu-id="64211-118">Select to print KID numbers on finance charge memos.</span></span> <span data-ttu-id="64211-119">**Obs!**  Hvis dette alternativet er valgt, må du også velge formatet **Bilagstype + bilagsnr.** i feltet **KID-oppsett**.</span><span class="sxs-lookup"><span data-stu-id="64211-119">**Note:**  If selected, then you must also select the **Document Type + Document No.** format in the **KID Setup** field.</span></span>|  
    |<span data-ttu-id="64211-120">**Bruk KID på purring**</span><span class="sxs-lookup"><span data-stu-id="64211-120">**Use KID on Reminder**</span></span>|<span data-ttu-id="64211-121">Velg å skrive ut KID-numre på purringer.</span><span class="sxs-lookup"><span data-stu-id="64211-121">Select to print KID numbers on reminders.</span></span> <span data-ttu-id="64211-122">**Obs!**  Hvis dette alternativet er valgt, må du også velge formatet **Bilagstype + bilagsnr.** i feltet **KID-oppsett**.</span><span class="sxs-lookup"><span data-stu-id="64211-122">**Note:**  If selected, then you must also select the **Document Type + Document No.** format in the **KID Setup** field.</span></span>|

3.  <span data-ttu-id="64211-123">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="64211-123">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="64211-124">Se også</span><span class="sxs-lookup"><span data-stu-id="64211-124">See Also</span></span>  
 [<span data-ttu-id="64211-125">Elektroniske banktjenester i Norge</span><span class="sxs-lookup"><span data-stu-id="64211-125">Electronic Banking in Norway</span></span>](electronic-banking-in-norway.md) 
