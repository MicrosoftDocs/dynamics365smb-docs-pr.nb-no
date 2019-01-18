---
title: "Søke etter dokumenter uten vedlegg | Microsoft-dokumentasjon"
Description: You can search for general ledger entries for posted purchase and sales documents that do not have incoming electronic documents, such as imported invoices.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 34bbc67c0f2bcc5afe408e75a7d3ceb582160d87
ms.contentlocale: nb-no
ms.lasthandoff: 11/26/2018

---
# <a name="find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="d2e85-102">Finne bokførte dokumenter uten innkommende dokumentposter</span><span class="sxs-lookup"><span data-stu-id="d2e85-102">Find Posted Documents without Incoming Document Records</span></span>
<span data-ttu-id="d2e85-103">Fra sidene **Kontoplan** og **Finansposter** kan du bruke søkefunksjonen til å finne finansposter for bokførte kjøps- og salgsdokumenter som ikke har innkommende dokumentposter, og deretter sentralt koble eksisterende poster eller opprette nye med vedlagte dokumentfiler.</span><span class="sxs-lookup"><span data-stu-id="d2e85-103">From the **Chart of Accounts** and **General Ledger Entries** pages, you can use a search function to find general ledger entries for posted purchase and sales documents that do not have incoming document records and then centrally link to existing records or create new ones with attached document files.</span></span>

## <a name="to-find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="d2e85-104">Slik finner du bokførte dokumenter uten innkommende dokumentposter:</span><span class="sxs-lookup"><span data-stu-id="d2e85-104">To find posted documents without incoming document records</span></span>
1. <span data-ttu-id="d2e85-105">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kontoplan**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="d2e85-105">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="d2e85-106">Velg en linje for en finanskonto som du vil vise bokførte kjøps- og salgsdokumenter for uten innkommende dokumentposter, og velg deretter handlingen **Bokførte dokumenter uten inngående dokument**.</span><span class="sxs-lookup"><span data-stu-id="d2e85-106">Select a line for a G/L account for whose general ledger entries you want to see posted purchase and sales documents without incoming document records, and then choose the **Posted Documents without Incoming Document** action.</span></span>
3. <span data-ttu-id="d2e85-107">Du kan også velge handlingen **Poster**.</span><span class="sxs-lookup"><span data-stu-id="d2e85-107">Alternatively, choose the **Ledger Entries** action.</span></span>
4. <span data-ttu-id="d2e85-108">På siden **Finansposter** velger du handlingen **Bokførte dokumenter uten inngående dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="d2e85-108">On the **General Ledger Entries** page, choose the **Posted Documents without Incoming Documents** action.</span></span>

<span data-ttu-id="d2e85-109">Siden **Bokførte dokumenter uten innkommende dokument** åpnes med bokførte kjøps- og salgsdokumenter uten innkommende dokumentposter representert av finansposter på finanskontoen som du åpnet siden for.</span><span class="sxs-lookup"><span data-stu-id="d2e85-109">The **Posted Documents without Incoming Document** page opens showing posted purchase and sales documents without incoming document records represented by general ledger entries on the G/L account that you opened the page for.</span></span> <span data-ttu-id="d2e85-110">Siden kan vise maksimalt 1000 linjer.</span><span class="sxs-lookup"><span data-stu-id="d2e85-110">The page can show a maximum of 1000 lines.</span></span> <span data-ttu-id="d2e85-111">Som standard inneholder derfor feltet **Datofilter** et filter som begrenser linjene til poster med bokføringsdatoer fra begynnelsen av regnskapsperioden til arbeidsdatoen.</span><span class="sxs-lookup"><span data-stu-id="d2e85-111">By default, the **Date Filter** field therefore contains a filter that limits the lines to entries with posting dates from the beginning of the accounting period to the work date.</span></span>

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a><span data-ttu-id="d2e85-112">Slik kobler du dokumenter som blir funnet, til eksisterende innkommende dokumentposter:</span><span class="sxs-lookup"><span data-stu-id="d2e85-112">To connect found documents to existing incoming document records</span></span>
1. <span data-ttu-id="d2e85-113">På siden **Bokførte dokumenter uten inngående dokument** velger du linjen for et bokført dokument du vil koble til en eksisterende innkommende dokumentpost, og deretter velger du handlingen **Velg inngående dokument**.</span><span class="sxs-lookup"><span data-stu-id="d2e85-113">On the **Posted Documents without Incoming Document** page, select the line for a posted document that you want to connect to an existing incoming document record, and then choose the **Select Incoming Document** action.</span></span>
2. <span data-ttu-id="d2e85-114">På siden **Inngående dokumenter** velger du den innkommende dokumentposten som du vil koble til det bokførte dokumentet som ble funnet, og deretter velger du **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="d2e85-114">On the **Incoming Documents** page, select the incoming document record that you want to connect to posted document found, and then choose the **OK** button.</span></span>
3. <span data-ttu-id="d2e85-115">På siden **Bokførte dokumenter uten inngående dokument** er den valgte inngående dokumentposten nå koblet til det bokførte dokumentet, som du kan se i faktaboksen **Filer for inngående dokument**.</span><span class="sxs-lookup"><span data-stu-id="d2e85-115">On the **Posted Documents without Incoming Document** page, the selected incoming document record is now connected to the posted document, as you can see in the **Incoming Document Files** FactBox.</span></span>

<span data-ttu-id="d2e85-116">Hvis en relevant innkommende dokumentpost ikke finnes på siden **Inngående dokumenter**, kan du opprette den.</span><span class="sxs-lookup"><span data-stu-id="d2e85-116">If a relevant incoming document record does not exist on the **Incoming Documents** page, then you can create it.</span></span> <span data-ttu-id="d2e85-117">Hvis du vil ha mer informasjon, kan du se [Opprette innkommende dokumentposter](across-how-create-income-document-records.md).</span><span class="sxs-lookup"><span data-stu-id="d2e85-117">For more information, see [Create Incoming Document Records](across-how-create-income-document-records.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d2e85-118">Se også</span><span class="sxs-lookup"><span data-stu-id="d2e85-118">See Also</span></span>
[<span data-ttu-id="d2e85-119">Behandle inngående dokumenter</span><span class="sxs-lookup"><span data-stu-id="d2e85-119">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="d2e85-120">Inngående dokumenter</span><span class="sxs-lookup"><span data-stu-id="d2e85-120">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="d2e85-121">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="d2e85-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="d2e85-122">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d2e85-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

