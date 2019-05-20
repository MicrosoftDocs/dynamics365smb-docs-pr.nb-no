---
title: Sende elektroniske dokumenter | Microsoft-dokumentasjon
description: Lær hvordan du sender fakturaer elektronisk.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8cb28db63e977cf02b81daa7043b64838406161f
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251609"
---
# <a name="send-electronic-documents"></a><span data-ttu-id="91b1e-103">Sende elektroniske dokumenter</span><span class="sxs-lookup"><span data-stu-id="91b1e-103">Send Electronic Documents</span></span>
<span data-ttu-id="91b1e-104">Den generelle versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] kan sende elektroniske fakturaer og kreditnotaer i PEPPOL-format, som støttes av de største leverandørene av dokumentutvekslingstjenester.</span><span class="sxs-lookup"><span data-stu-id="91b1e-104">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] supports sending electronic invoices and credit memos in the PEPPOL format, which is supported by the largest document exchange service providers.</span></span> <span data-ttu-id="91b1e-105">En leverandør av dokumentutvekslingstjenester fordeler elektroniske dokumenter mellom handelspartnere.</span><span class="sxs-lookup"><span data-stu-id="91b1e-105">A document exchange service provider dispatches electronic documents between trading partners.</span></span> <span data-ttu-id="91b1e-106">Hvis du vil ha støtte for andre elektroniske dokumentformater, kan du bruke rammeverket for datautveksling.</span><span class="sxs-lookup"><span data-stu-id="91b1e-106">To provide support for other electronic document formats, you use the data exchange framework.</span></span>  

 <span data-ttu-id="91b1e-107">I den generelle versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] er en dokumentutvekslingstjeneste forhåndskonfigurert og klar til å bli definert for firmaet.</span><span class="sxs-lookup"><span data-stu-id="91b1e-107">In the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)], a document exchange service is preconfigured and ready to be set up for your company.</span></span> <span data-ttu-id="91b1e-108">Hvis du vil ha mer informasjon, kan du se [Konfigurere en dokumentutvekslingstjeneste](across-how-to-set-up-a-document-exchange-service.md).</span><span class="sxs-lookup"><span data-stu-id="91b1e-108">For more information, see [Set Up a Document Exchange Service](across-how-to-set-up-a-document-exchange-service.md).</span></span>  

 <span data-ttu-id="91b1e-109">Hvis du vil sende en salgsfaktura som et elektronisk PEPPOL-dokument, velger du alternativet **Elektronisk dokument** i dialogboksen **Bokfør og send**, der du også kan konfigurere kundens standardprofil for dokumentsending.</span><span class="sxs-lookup"><span data-stu-id="91b1e-109">To send a sales invoice as an electronic PEPPOL document, you select the **Electronic Document** option in the **Post and Send** dialog box from where you can also set up the customer’s default document sending profile.</span></span> <span data-ttu-id="91b1e-110">Først må du definere forskjellige hoveddata, for eksempel firmainformasjon, kunder, varer og enheter.</span><span class="sxs-lookup"><span data-stu-id="91b1e-110">First, you must set up various master data, such as company information, customers, items, and units of measure.</span></span> <span data-ttu-id="91b1e-111">Disse brukes til å identifisere forretningspartnere og elementer ved konvertering av data i feltene [Konfigurere sending og mottak av elektroniske dokumenter](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="91b1e-111">These are used to identify the business partners and items when converting data in fields in [Set Up Electronic Document Sending and Receiving](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span></span>  

### <a name="to-send-an-electronic-sales-invoice"></a><span data-ttu-id="91b1e-112">Slik sender du en elektronisk salgsfaktura:</span><span class="sxs-lookup"><span data-stu-id="91b1e-112">To send an electronic sales invoice</span></span>  

1.  <span data-ttu-id="91b1e-113">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Salgsfakturaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="91b1e-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="91b1e-114">Opprett en ny salgsfaktura.</span><span class="sxs-lookup"><span data-stu-id="91b1e-114">Create a new sales invoice.</span></span>  

3.  <span data-ttu-id="91b1e-115">Når salgsfakturaen er klar til fakturering, velger du **Bokfør og send** i **Handlinger**-kategorien i **Bokføring**-gruppen.</span><span class="sxs-lookup"><span data-stu-id="91b1e-115">When the sales invoice is ready to be invoiced, on the **Actions** tab, in the **Posting** group, choose **Post and Send**.</span></span>  

     <span data-ttu-id="91b1e-116">Hvis kundens standard sendingsprofil er **Elektronisk dokument**, vil den vises i dialogboksen **Bokfør og send bekreftelse**, og du trenger bare å velge **Ja**-knappen for å bokføre og sende fakturaen elektronisk i det valgte formatet.</span><span class="sxs-lookup"><span data-stu-id="91b1e-116">If the customer’s default sending profile is **Electronic Document**, then it will be shown in the **Post and Send Confirmation** dialog box and you just have to choose the **Yes** button to post and send the invoice electronically in the selected format.</span></span>  

4.  <span data-ttu-id="91b1e-117">I dialogboksen **Bokfør og send bekreftelse** velger du AssistEdit-knappen til høyre for feltet **Send dokument til**.</span><span class="sxs-lookup"><span data-stu-id="91b1e-117">In the **Post and Send Confirmation** dialog box, choose the AssistEdit button to the right of the **Send Document to** field.</span></span>  

5.  <span data-ttu-id="91b1e-118">I dialogboksen **Send dokument til** i feltet **Elektronisk dokument** velger du **Gjennom dokumentutvekslingstjeneste**.</span><span class="sxs-lookup"><span data-stu-id="91b1e-118">In the **Send Document to** dialog box, in the **Electronic Document** field, choose **Through Document Exchange Service**.</span></span>  

6.  <span data-ttu-id="91b1e-119">I **Format**-feltet velger du **PEPPOL**.</span><span class="sxs-lookup"><span data-stu-id="91b1e-119">In the **Format** field, choose **PEPPOL**.</span></span>  

7.  <span data-ttu-id="91b1e-120">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="91b1e-120">Choose the **OK** button.</span></span> <span data-ttu-id="91b1e-121">Dialogboksen **Bokfør og send bekreftelse** vises.</span><span class="sxs-lookup"><span data-stu-id="91b1e-121">The **Post and Send Confirmation** dialog box appears.</span></span> <span data-ttu-id="91b1e-122">**Elektronisk dokument (PEPPOL)** legges til i **Send dokument til**-feltet.</span><span class="sxs-lookup"><span data-stu-id="91b1e-122">**Electronic Document (PEPPOL)** is added to the **Send Document to** field.</span></span>  

8.  <span data-ttu-id="91b1e-123">Velg **Ja**-knappen.</span><span class="sxs-lookup"><span data-stu-id="91b1e-123">Choose the **Yes** button.</span></span>  

     <span data-ttu-id="91b1e-124">Salgsfakturaen bokføres og sendes til kunden som et elektronisk dokument i formatet PEPPOL.</span><span class="sxs-lookup"><span data-stu-id="91b1e-124">The sales invoice is posted and sent to the customer as an electronic document in the PEPPOL format.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="91b1e-125">Du kan også sende en bokført salgsfaktura som et elektronisk dokument.</span><span class="sxs-lookup"><span data-stu-id="91b1e-125">You can also send a posted sales invoice as an electronic document.</span></span> <span data-ttu-id="91b1e-126">Fremgangsmåten er den samme som beskrevet i dette emnet for ikke-bokførte salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="91b1e-126">The procedure is the same as described in this topic for non-posted sales documents.</span></span> <span data-ttu-id="91b1e-127">På siden **Bokført salgsfaktura** i fanen **Handlinger** i gruppen **Generelt**, velger du **Aktivitetslogg** for å vise statusen for det elektroniske dokumentet.</span><span class="sxs-lookup"><span data-stu-id="91b1e-127">On the **Posted Sales Invoice** page, on the **Actions** tab, in the **General** group, choose **Activity Log** to view the status of the electronic document.</span></span> <span data-ttu-id="91b1e-128">Hvis du vil ha mer informasjon, kan du se **Aktivitetslogg**.</span><span class="sxs-lookup"><span data-stu-id="91b1e-128">For more information, see **Activity Log**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="91b1e-129">Se også</span><span class="sxs-lookup"><span data-stu-id="91b1e-129">See Also</span></span>  
[<span data-ttu-id="91b1e-130">Fakturere salg</span><span class="sxs-lookup"><span data-stu-id="91b1e-130">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="91b1e-131">Definere en profil for dokumentsending</span><span class="sxs-lookup"><span data-stu-id="91b1e-131">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md)  
[<span data-ttu-id="91b1e-132">Konfigurere sending og mottak av elektroniske dokumenter</span><span class="sxs-lookup"><span data-stu-id="91b1e-132">Set Up Electronic Document Sending and Receiving</span></span>](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[<span data-ttu-id="91b1e-133">Konfigurere en dokumentutvekslingstjeneste</span><span class="sxs-lookup"><span data-stu-id="91b1e-133">Set Up a Document Exchange Service</span></span>](across-how-to-set-up-a-document-exchange-service.md)  
[<span data-ttu-id="91b1e-134">Definere datautvekslingsdefinisjoner</span><span class="sxs-lookup"><span data-stu-id="91b1e-134">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="91b1e-135">Utveksle data elektronisk</span><span class="sxs-lookup"><span data-stu-id="91b1e-135">Exchanging Data Electronically</span></span>](across-data-exchange.md)  
[<span data-ttu-id="91b1e-136">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="91b1e-136">General Business Functionality</span></span>](ui-across-business-areas.md)  
