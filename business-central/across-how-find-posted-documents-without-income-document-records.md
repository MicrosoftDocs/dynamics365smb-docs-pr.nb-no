---
title: Søke etter dokumenter uten vedlegg | Microsoft-dokumentasjon
Description: Du kan søke etter finansposter for bokførte kjøps- og salgsdokumenter som ikke har inngående elektroniske dokumenter, for eksempel importerte fakturaer.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e15284452bb80acc329e46df7361ee9dea556996
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754970"
---
# <a name="find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="48543-103">Finne bokførte dokumenter uten innkommende dokumentposter</span><span class="sxs-lookup"><span data-stu-id="48543-103">Find Posted Documents without Incoming Document Records</span></span>
<span data-ttu-id="48543-104">Fra sidene **Kontoplan** og **Finansposter** kan du bruke søkefunksjonen til å finne finansposter for bokførte kjøps- og salgsdokumenter som ikke har innkommende dokumentposter, og deretter sentralt koble eksisterende poster eller opprette nye med vedlagte dokumentfiler.</span><span class="sxs-lookup"><span data-stu-id="48543-104">From the **Chart of Accounts** and **General Ledger Entries** pages, you can use a search function to find general ledger entries for posted purchase and sales documents that do not have incoming document records and then centrally link to existing records or create new ones with attached document files.</span></span>

## <a name="to-find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="48543-105">Slik finner du bokførte dokumenter uten innkommende dokumentposter:</span><span class="sxs-lookup"><span data-stu-id="48543-105">To find posted documents without incoming document records</span></span>
1. <span data-ttu-id="48543-106">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kontoplan**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="48543-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="48543-107">Velg en linje for en finanskonto som du vil vise bokførte kjøps- og salgsdokumenter for uten innkommende dokumentposter, og velg deretter handlingen **Bokførte dokumenter uten inngående dokument**.</span><span class="sxs-lookup"><span data-stu-id="48543-107">Select a line for a G/L account for whose general ledger entries you want to see posted purchase and sales documents without incoming document records, and then choose the **Posted Documents without Incoming Document** action.</span></span>
3. <span data-ttu-id="48543-108">Du kan også velge handlingen **Poster**.</span><span class="sxs-lookup"><span data-stu-id="48543-108">Alternatively, choose the **Ledger Entries** action.</span></span>
4. <span data-ttu-id="48543-109">På siden **Finansposter** velger du handlingen **Bokførte dokumenter uten inngående dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="48543-109">On the **General Ledger Entries** page, choose the **Posted Documents without Incoming Documents** action.</span></span>

<span data-ttu-id="48543-110">Siden **Bokførte dokumenter uten innkommende dokument** åpnes med bokførte kjøps- og salgsdokumenter uten innkommende dokumentposter representert av finansposter på finanskontoen som du åpnet siden for.</span><span class="sxs-lookup"><span data-stu-id="48543-110">The **Posted Documents without Incoming Document** page opens showing posted purchase and sales documents without incoming document records represented by general ledger entries on the G/L account that you opened the page for.</span></span> <span data-ttu-id="48543-111">Siden kan vise maksimalt 1000 linjer.</span><span class="sxs-lookup"><span data-stu-id="48543-111">The page can show a maximum of 1000 lines.</span></span> <span data-ttu-id="48543-112">Som standard inneholder derfor feltet **Datofilter** et filter som begrenser linjene til poster med bokføringsdatoer fra begynnelsen av regnskapsperioden til arbeidsdatoen.</span><span class="sxs-lookup"><span data-stu-id="48543-112">By default, the **Date Filter** field therefore contains a filter that limits the lines to entries with posting dates from the beginning of the accounting period to the work date.</span></span>

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a><span data-ttu-id="48543-113">Slik kobler du dokumenter som blir funnet, til eksisterende innkommende dokumentposter:</span><span class="sxs-lookup"><span data-stu-id="48543-113">To connect found documents to existing incoming document records</span></span>
1. <span data-ttu-id="48543-114">På siden **Bokførte dokumenter uten inngående dokument** velger du linjen for et bokført dokument du vil koble til en eksisterende innkommende dokumentpost, og deretter velger du handlingen **Velg inngående dokument**.</span><span class="sxs-lookup"><span data-stu-id="48543-114">On the **Posted Documents without Incoming Document** page, select the line for a posted document that you want to connect to an existing incoming document record, and then choose the **Select Incoming Document** action.</span></span>
2. <span data-ttu-id="48543-115">På siden **Inngående dokumenter** velger du den innkommende dokumentposten som du vil koble til det bokførte dokumentet som ble funnet, og deretter velger du **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="48543-115">On the **Incoming Documents** page, select the incoming document record that you want to connect to posted document found, and then choose the **OK** button.</span></span>
3. <span data-ttu-id="48543-116">På siden **Bokførte dokumenter uten inngående dokument** er den valgte inngående dokumentposten nå koblet til det bokførte dokumentet, som du kan se i faktaboksen **Filer for inngående dokument**.</span><span class="sxs-lookup"><span data-stu-id="48543-116">On the **Posted Documents without Incoming Document** page, the selected incoming document record is now connected to the posted document, as you can see in the **Incoming Document Files** FactBox.</span></span>

<span data-ttu-id="48543-117">Hvis en relevant innkommende dokumentpost ikke finnes på siden **Inngående dokumenter**, kan du opprette den.</span><span class="sxs-lookup"><span data-stu-id="48543-117">If a relevant incoming document record does not exist on the **Incoming Documents** page, then you can create it.</span></span> <span data-ttu-id="48543-118">Hvis du vil ha mer informasjon, kan du se [Opprette innkommende dokumentposter](across-how-create-income-document-records.md).</span><span class="sxs-lookup"><span data-stu-id="48543-118">For more information, see [Create Incoming Document Records](across-how-create-income-document-records.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="48543-119">Se også</span><span class="sxs-lookup"><span data-stu-id="48543-119">See Also</span></span>
[<span data-ttu-id="48543-120">Behandle inngående dokumenter</span><span class="sxs-lookup"><span data-stu-id="48543-120">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="48543-121">Inngående dokumenter</span><span class="sxs-lookup"><span data-stu-id="48543-121">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="48543-122">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="48543-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="48543-123">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="48543-123">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
