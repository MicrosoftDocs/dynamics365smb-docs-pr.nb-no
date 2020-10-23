---
title: Importere og bokføre OCR-betalinger
description: Før du kan motta OCR-betalinger (optisk tegngjenkjenning), må du gjøre noen forberedelser.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9eaeb9a3c8d1f22b96fb328fb7a8cbc2787dd620
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919783"
---
# <a name="import-and-post-ocr-payments"></a><span data-ttu-id="12380-103">Importere og bokføre OCR-betalinger</span><span class="sxs-lookup"><span data-stu-id="12380-103">Import and Post OCR Payments</span></span>
<span data-ttu-id="12380-104">Før du kan motta OCR-betalinger (optisk tegngjenkjenning), må du gjøre følgende forberedelser:</span><span class="sxs-lookup"><span data-stu-id="12380-104">Before you can receive optical character recognition (OCR) payments, you must make the following preparations:</span></span>  

- <span data-ttu-id="12380-105">Opprette en innbetalingskladdemal for å balansere OCR-transaksjoner i henhold til bilagsnummeret i stedet for bilagstypen.</span><span class="sxs-lookup"><span data-stu-id="12380-105">Set up a cash receipt journal template to balance OCR transactions according to the document number, instead of the document type.</span></span>  
- <span data-ttu-id="12380-106">Lese inn og bokføre OCR-betalingsfiler i en innbetalingskladd.</span><span class="sxs-lookup"><span data-stu-id="12380-106">Import and post the OCR payment files to a cash receipt journal.</span></span>  

## <a name="to-import-ocr-payments"></a><span data-ttu-id="12380-107">Slik leser du inn OCR-betalinger</span><span class="sxs-lookup"><span data-stu-id="12380-107">To import OCR payments</span></span>  

1.  <span data-ttu-id="12380-108">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](../../media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Innbetalingskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="12380-108">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cash Receipt Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="12380-109">Velg en kladd i feltet **Bunkenavn**.</span><span class="sxs-lookup"><span data-stu-id="12380-109">In the **Batch Name** field, select a journal batch.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="12380-110">OCR-betalinger kan bare bokføres i en innbetalingskladd som ikke benytter en motkonto i feltet **Motkontonr.** på linjen Innbetalingskladd.</span><span class="sxs-lookup"><span data-stu-id="12380-110">OCR payments can only be posted to a cash receipt journal that does not use a balance account in the **Bal. Account No.** field on the cash receipt journal line.</span></span>  

3.  <span data-ttu-id="12380-111">Velg handlingen **Importer betalinger**.</span><span class="sxs-lookup"><span data-stu-id="12380-111">Choose the **Import Payments** action.</span></span>  
4.  <span data-ttu-id="12380-112">På siden **OCR-betaling - BBS** fyller du ut feltene som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="12380-112">On the **OCR Payment-BBS** page, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="12380-113">Felt</span><span class="sxs-lookup"><span data-stu-id="12380-113">Field</span></span>|<span data-ttu-id="12380-114">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="12380-114">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="12380-115">**Filnavn**</span><span class="sxs-lookup"><span data-stu-id="12380-115">**File Name**</span></span>|<span data-ttu-id="12380-116">Skriv inn hele banen til importfilen.</span><span class="sxs-lookup"><span data-stu-id="12380-116">Enter the full path of the import file.</span></span>|  

5.  <span data-ttu-id="12380-117">Velg **OK** for å lese inn betalingsfilen i kladden.</span><span class="sxs-lookup"><span data-stu-id="12380-117">Choose the **OK** button to import the payment file to the journal.</span></span>  

## <a name="to-post-ocr-payments"></a><span data-ttu-id="12380-118">Slik bokfører du OCR-betalinger</span><span class="sxs-lookup"><span data-stu-id="12380-118">To post OCR payments</span></span>  

1.  <span data-ttu-id="12380-119">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](../../media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Innbetalingskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="12380-119">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cash Receipt Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="12380-120">Velg handlingen **Bokfør**.</span><span class="sxs-lookup"><span data-stu-id="12380-120">Choose the **Post** action.</span></span>  

<span data-ttu-id="12380-121">OCR-betalingsfilene bokføres i innbetalingskladden.</span><span class="sxs-lookup"><span data-stu-id="12380-121">The OCR payment files are posted to the cash receipt journal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="12380-122">Se også</span><span class="sxs-lookup"><span data-stu-id="12380-122">See Also</span></span>  
 <span data-ttu-id="12380-123">[Elektroniske banktjenester i Norge](electronic-banking-in-norway.md) </span><span class="sxs-lookup"><span data-stu-id="12380-123">[Electronic Banking in Norway](electronic-banking-in-norway.md) </span></span>  
 <span data-ttu-id="12380-124">[Opprette KID-numre på salgsdokumenter](how-to-set-up-kid-numbers-on-sales-documents.md) </span><span class="sxs-lookup"><span data-stu-id="12380-124">[Set Up KID Numbers on Sales Documents](how-to-set-up-kid-numbers-on-sales-documents.md) </span></span>  
 <span data-ttu-id="12380-125">[Opprette OCR-betalinger](how-to-set-up-ocr-payments.md) </span><span class="sxs-lookup"><span data-stu-id="12380-125">[Set Up OCR Payments](how-to-set-up-ocr-payments.md) </span></span>  
 <span data-ttu-id="12380-126">[Arbeide med finanskladder](../../ui-work-general-journals.md) </span><span class="sxs-lookup"><span data-stu-id="12380-126">[Work With General Journals](../../ui-work-general-journals.md) </span></span>  
 [<span data-ttu-id="12380-127">Skrive ut rapporten OCR-kladd - test</span><span class="sxs-lookup"><span data-stu-id="12380-127">Print the OCR Journal - Test Report</span></span>](how-to-print-the-ocr-journal-test-report.md)
