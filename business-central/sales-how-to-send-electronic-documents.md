---
title: Sende elektroniske dokumenter
description: Lær hvordan du sender fakturaer elektronisk.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8056aa66531740634fb155e0b3b4419a7f014ffc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778375"
---
# <a name="send-electronic-documents"></a><span data-ttu-id="a9679-103">Sende elektroniske dokumenter</span><span class="sxs-lookup"><span data-stu-id="a9679-103">Send Electronic Documents</span></span>

<span data-ttu-id="a9679-104">Den generelle versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] kan sende elektroniske fakturaer og kreditnotaer i PEPPOL-format, et format som de største leverandørene av dokumentutvekslingstjenester støtter.</span><span class="sxs-lookup"><span data-stu-id="a9679-104">The generic version of [!INCLUDE[prod_short](includes/prod_short.md)] supports sending electronic invoices and credit memos in the PEPPOL format, a format that the largest document exchange service providers support.</span></span> <span data-ttu-id="a9679-105">En leverandør av dokumentutvekslingstjenester fordeler elektroniske dokumenter mellom handelspartnere.</span><span class="sxs-lookup"><span data-stu-id="a9679-105">A document exchange service provider dispatches electronic documents between trading partners.</span></span> <span data-ttu-id="a9679-106">Hvis du vil ha støtte for andre elektroniske dokumentformater, kan du bruke rammeverket for datautveksling.</span><span class="sxs-lookup"><span data-stu-id="a9679-106">To provide support for other electronic document formats, you use the data exchange framework.</span></span>  

 <span data-ttu-id="a9679-107">I den generelle versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] er en dokumentutvekslingstjeneste forhåndskonfigurert og klar til å bli definert for firmaet.</span><span class="sxs-lookup"><span data-stu-id="a9679-107">In the generic version of [!INCLUDE[prod_short](includes/prod_short.md)], a document exchange service is preconfigured and ready to be set up for your company.</span></span> <span data-ttu-id="a9679-108">Hvis du vil ha mer informasjon, kan du se [Konfigurere en dokumentutvekslingstjeneste](across-how-to-set-up-a-document-exchange-service.md).</span><span class="sxs-lookup"><span data-stu-id="a9679-108">For more information, see [Set Up a Document Exchange Service](across-how-to-set-up-a-document-exchange-service.md).</span></span> <span data-ttu-id="a9679-109">I noen tilfeller må du imidlertid installere en app.</span><span class="sxs-lookup"><span data-stu-id="a9679-109">However, in some cases, you must install an app.</span></span> <span data-ttu-id="a9679-110">Hvis du vil ha mer informasjon, se [Vanlige spørsmål om elektronisk fakturering](faq-electronic-invoicing.yml).</span><span class="sxs-lookup"><span data-stu-id="a9679-110">For more information, see [Electronic Invoicing FAQ](faq-electronic-invoicing.yml).</span></span>  

 <span data-ttu-id="a9679-111">Hvis du vil sende en salgsfaktura som et elektronisk PEPPOL-dokument, velger du alternativet **Elektronisk dokument** i dialogboksen **Bokfør og send**.</span><span class="sxs-lookup"><span data-stu-id="a9679-111">To send a sales invoice as an electronic PEPPOL document, you select the **Electronic Document** option in the **Post and Send** dialog box.</span></span> <span data-ttu-id="a9679-112">Du kan også angi kundens standardprofil for dokumentsending fra den dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="a9679-112">You can also set up the customer's default document sending profile from that dialog box.</span></span> <span data-ttu-id="a9679-113">Først må du definere forskjellige hoveddata, for eksempel firmainformasjon, kunder, varer og enheter.</span><span class="sxs-lookup"><span data-stu-id="a9679-113">First, you must set up various master data, such as company information, customers, items, and units of measure.</span></span> <span data-ttu-id="a9679-114">Disse brukes til å identifisere forretningspartnere og elementer ved konvertering av data i feltene [Konfigurere sending og mottak av elektroniske dokumenter](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="a9679-114">These are used to identify the business partners and items when converting data in fields in [Set Up Electronic Document Sending and Receiving](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span></span>  

### <a name="to-send-an-electronic-sales-invoice"></a><span data-ttu-id="a9679-115">Slik sender du en elektronisk salgsfaktura:</span><span class="sxs-lookup"><span data-stu-id="a9679-115">To send an electronic sales invoice</span></span>

1. <span data-ttu-id="a9679-116">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgsfakturaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a9679-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  

2. <span data-ttu-id="a9679-117">Opprett en ny salgsfaktura.</span><span class="sxs-lookup"><span data-stu-id="a9679-117">Create a new sales invoice.</span></span>  

3. <span data-ttu-id="a9679-118">Når salgsfakturalinjene er klare til å bli fakturert, kan du velge handlingen **Bokfør og send**.</span><span class="sxs-lookup"><span data-stu-id="a9679-118">When the sales invoice is ready to be invoiced, choose the **Post and Send** action.</span></span>  

     <span data-ttu-id="a9679-119">Hvis kundens standard sendeprofil er **Elektronisk dokument**, vil den vises i dialogboksen **Legg inn og send bekreftelse**.</span><span class="sxs-lookup"><span data-stu-id="a9679-119">If the customer's default sending profile is **Electronic Document**, then it will be shown in the **Post and Send Confirmation** dialog box.</span></span> <span data-ttu-id="a9679-120">På denne måten må du bare velge **Ja** for å bokføre og sende fakturaen elektronisk i det valgte formatet.</span><span class="sxs-lookup"><span data-stu-id="a9679-120">This way, you just have to choose the **Yes** button to post and send the invoice electronically in the selected format.</span></span>  

4. <span data-ttu-id="a9679-121">I dialogboksen **Bokfør og send bekreftelse** velger du AssistEdit-knappen til høyre for feltet **Send dokument til**.</span><span class="sxs-lookup"><span data-stu-id="a9679-121">In the **Post and Send Confirmation** dialog box, choose the AssistEdit button to the right of the **Send Document to** field.</span></span>  

5. <span data-ttu-id="a9679-122">I dialogboksen **Send dokument til** i feltet **Elektronisk dokument** velger du **Gjennom dokumentutvekslingstjeneste**.</span><span class="sxs-lookup"><span data-stu-id="a9679-122">In the **Send Document to** dialog box, in the **Electronic Document** field, choose **Through Document Exchange Service**.</span></span>  

6. <span data-ttu-id="a9679-123">I **Format**-feltet velger du **PEPPOL**.</span><span class="sxs-lookup"><span data-stu-id="a9679-123">In the **Format** field, choose **PEPPOL**.</span></span>  

7. <span data-ttu-id="a9679-124">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="a9679-124">Choose the **OK** button.</span></span> <span data-ttu-id="a9679-125">Dialogboksen **Bokfør og send bekreftelse** vises.</span><span class="sxs-lookup"><span data-stu-id="a9679-125">The **Post and Send Confirmation** dialog box appears.</span></span> <span data-ttu-id="a9679-126">**Elektronisk dokument (PEPPOL)** legges til i **Send dokument til**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a9679-126">**Electronic Document (PEPPOL)** is added to the **Send Document to** field.</span></span>  

8. <span data-ttu-id="a9679-127">Velg **Ja**-knappen.</span><span class="sxs-lookup"><span data-stu-id="a9679-127">Choose the **Yes** button.</span></span>  

     <span data-ttu-id="a9679-128">Salgsfakturaen bokføres og sendes til kunden i formatet PEPPOL.</span><span class="sxs-lookup"><span data-stu-id="a9679-128">The sales invoice is posted and sent to the customer in the PEPPOL format.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="a9679-129">Du kan også sende en bokført salgsfaktura som et elektronisk dokument.</span><span class="sxs-lookup"><span data-stu-id="a9679-129">You can also send a posted sales invoice as an electronic document.</span></span> <span data-ttu-id="a9679-130">Fremgangsmåten er den samme som beskrevet i dette emnet for ikke-bokførte salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="a9679-130">The procedure is the same as described in this topic for non-posted sales documents.</span></span> <span data-ttu-id="a9679-131">På siden **Bokført salgsfaktura** velger du **Aktivitetslogg**-handlingen for å vise statusen for det elektroniske dokumentet.</span><span class="sxs-lookup"><span data-stu-id="a9679-131">On the **Posted Sales Invoice** page, choose the **Activity Log** action to view the status of the electronic document.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="a9679-132">Se relatert opplæring på [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="a9679-132">See Related Training at [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="a9679-133">Se også</span><span class="sxs-lookup"><span data-stu-id="a9679-133">See Also</span></span>

[<span data-ttu-id="a9679-134">Fakturere salg</span><span class="sxs-lookup"><span data-stu-id="a9679-134">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="a9679-135">Definere en profil for dokumentsending</span><span class="sxs-lookup"><span data-stu-id="a9679-135">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md)  
[<span data-ttu-id="a9679-136">Konfigurere sending og mottak av elektroniske dokumenter</span><span class="sxs-lookup"><span data-stu-id="a9679-136">Set Up Electronic Document Sending and Receiving</span></span>](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[<span data-ttu-id="a9679-137">Konfigurere en dokumentutvekslingstjeneste</span><span class="sxs-lookup"><span data-stu-id="a9679-137">Set Up a Document Exchange Service</span></span>](across-how-to-set-up-a-document-exchange-service.md)  
[<span data-ttu-id="a9679-138">Definere datautvekslingsdefinisjoner</span><span class="sxs-lookup"><span data-stu-id="a9679-138">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="a9679-139">Utveksle data elektronisk</span><span class="sxs-lookup"><span data-stu-id="a9679-139">Exchanging Data Electronically</span></span>](across-data-exchange.md)  
[<span data-ttu-id="a9679-140">Vanlige spørsmål om elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="a9679-140">Electronic Invoicing FAQ</span></span>](faq-electronic-invoicing.yml)  
[<span data-ttu-id="a9679-141">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="a9679-141">General Business Functionality</span></span>](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]