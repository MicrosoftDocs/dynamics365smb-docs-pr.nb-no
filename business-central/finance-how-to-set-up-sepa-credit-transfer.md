---
title: "Definere SEPA-kredittoverføring | Microsoft-dokumentasjon"
description: "Lær hvordan du definerer SEPA-kredittoverføring i Business Central."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sepa, credit, transfer, payment,
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 103ebe376d3384eab119617b903f9a803f248462
ms.contentlocale: nb-no
ms.lasthandoff: 11/26/2018

---
# <a name="set-up-sepa-credit-transfer"></a><span data-ttu-id="3d7a1-103">Definere SEPA-kredittoverføring</span><span class="sxs-lookup"><span data-stu-id="3d7a1-103">Set Up SEPA Credit Transfer</span></span>
<span data-ttu-id="3d7a1-104">Fra siden **Utbetalingskladd** kan du eksportere betalinger til en fil for opplasting til den elektroniske banken for behandling av relaterte pengeoverføringer.</span><span class="sxs-lookup"><span data-stu-id="3d7a1-104">From the **Payment Journal** page, you can export payments to a file for upload to your electronic bank for processing of the related money transfers.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="3d7a1-105">støtter formatet for SEPA-kreidttoverføring, men andre formater for elektroniske betalinger kan være tilgjengelige i ditt land/region.</span><span class="sxs-lookup"><span data-stu-id="3d7a1-105">supports the SEPA Credit Transfer format, but in your country/region, other formats for electronic payments may be available.</span></span>  

<span data-ttu-id="3d7a1-106">Du kan gjøre det mulig å eksportere et bankfilformat som ikke støttes som standard i [!INCLUDE[d365fin](includes/d365fin_md.md)], ved å definere en datautvekslingsdefinisjon ved hjelp av rammeverket for datautveksling.</span><span class="sxs-lookup"><span data-stu-id="3d7a1-106">To enable export of a bank file formats that are not supported out of the box in [!INCLUDE[d365fin](includes/d365fin_md.md)], you can set up a data exchange definition by using the data exchange framework.</span></span> <span data-ttu-id="3d7a1-107">Hvis du vil ha mer informasjon, kan du se [Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md)</span><span class="sxs-lookup"><span data-stu-id="3d7a1-107">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

<span data-ttu-id="3d7a1-108">Før du kan behandle betalingen elektronisk ved å eksportere betalingsfiler i formatet for SEPA-kredittoverføring, må du utføre følgende konfigureringstrinn:</span><span class="sxs-lookup"><span data-stu-id="3d7a1-108">Before you can process payment electronically by exporting payment files in the SEPA Credit Transfer format, you must perform the following setup steps:</span></span>  

* <span data-ttu-id="3d7a1-109">Definer den aktuelle bankkontoen slik at den kan håndtere SEPA-kredittoverføringsformatet.</span><span class="sxs-lookup"><span data-stu-id="3d7a1-109">Set up the bank account in question to handle the SEPA Credit Transfer format</span></span>  
* <span data-ttu-id="3d7a1-110">Definer leverandørkort slik at betalinger behandles ved å eksportere filer i SEPA-kredittoverføringsformatet.</span><span class="sxs-lookup"><span data-stu-id="3d7a1-110">Set up vendor cards to process payments by exporting files in the SEPA Credit Transfer format</span></span>  
* <span data-ttu-id="3d7a1-111">Definer den tilknyttede finanskladden slik at betalingseksport kan utføres fra siden **Utbetalingskladd**.</span><span class="sxs-lookup"><span data-stu-id="3d7a1-111">Set up the related general journal batch to enable payment export from the **Payment Journal** page</span></span>  
* <span data-ttu-id="3d7a1-112">Knytt datautvekslingsdefinisjon for én eller flere betalingstyper til de(n) aktuelle betalingsmåten(e):</span><span class="sxs-lookup"><span data-stu-id="3d7a1-112">Connect the data exchange definition for one or more payment types with the relevant payment method or methods</span></span>  

### <a name="to-set-up-a-bank-account-for-sepa-credit-transfer"></a><span data-ttu-id="3d7a1-113">Slik oppretter du en bankkonto for SEPA-kredittoverføring:</span><span class="sxs-lookup"><span data-stu-id="3d7a1-113">To set up a bank account for SEPA Credit Transfer</span></span>  
1. <span data-ttu-id="3d7a1-114">Skriv inn **Bankkontoer** i **Søk**-boksen, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="3d7a1-114">In the **Search** box, enter **Bank Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3d7a1-115">Åpne kortet for bankkontoen som du vil eksportere betalingsfiler fra, i formatet for SEPA-kredittoverføring.</span><span class="sxs-lookup"><span data-stu-id="3d7a1-115">Open the card of the bank account from which you will export payment files in the SEPA Credit Transfer format.</span></span>  
3. <span data-ttu-id="3d7a1-116">På hurtigfanen **Overfør** i feltet **Betalingseksportformat** velger du **SEPADD**.</span><span class="sxs-lookup"><span data-stu-id="3d7a1-116">On the **Transfer** FastTab, in the **Payment Export Format** field, choose **SEPADD**.</span></span>  
4. <span data-ttu-id="3d7a1-117">I feltet **SEPA CT-mld., ID-nr-serie** velger du en nummerserie med numre som tilordnes til bokføringer av SEPA-kredittoverføringer.</span><span class="sxs-lookup"><span data-stu-id="3d7a1-117">In the **SEPA CT Msg. ID No. Series** field, choose a number series from which numbers are assigned to SEPA credit transfer entries.</span></span>  
5. <span data-ttu-id="3d7a1-118">Kontroller at **IBAN**-feltet er utfylt.</span><span class="sxs-lookup"><span data-stu-id="3d7a1-118">Make sure the **IBAN** field is filled.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="3d7a1-119">**EUR** må angis i **Valutakode**-feltet fordi SEPA-kredittoverføringer bare kan foretas i euro.</span><span class="sxs-lookup"><span data-stu-id="3d7a1-119">The **Currency Code** field must be set to **EUR**, because SEPA credit transfers can only be made in the EURO currency.</span></span>  

### <a name="to-set-up-a-vendor-card-for-sepa-credit-transfer"></a><span data-ttu-id="3d7a1-120">Slik oppretter du et leverandørkort for SEPA-kredittoverføring:</span><span class="sxs-lookup"><span data-stu-id="3d7a1-120">To set up a vendor card for SEPA Credit Transfer</span></span>  
1. <span data-ttu-id="3d7a1-121">Skriv inn **Leverandører** i **Søk**-boksen, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="3d7a1-121">In the **Search** box, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3d7a1-122">Åpne kortet for leverandøren som du vil betale elektronisk, ved å eksportere betalingsfiler i formatet for SEPA-kredittoverføring.</span><span class="sxs-lookup"><span data-stu-id="3d7a1-122">Open the card of the vendor whom you will pay electronically by export payment files in the SEPA Credit Transfer format.</span></span>  
3. <span data-ttu-id="3d7a1-123">Velg **BANK** i hurtigfanen **Betaling** i feltet **Betalingsmåte - kode**.</span><span class="sxs-lookup"><span data-stu-id="3d7a1-123">On the **Payment** FastTab, in the **Payment Method Code** field, choose **BANK**.</span></span>  
4. <span data-ttu-id="3d7a1-124">I feltet **Foretrukket bankkonto** velger du banken som pengene skal overføres til når den behandles av den elektroniske banken.</span><span class="sxs-lookup"><span data-stu-id="3d7a1-124">In the **Preferred Bank Account** field, choose the bank to which the money will be transferred when it is processed by your electronic bank.</span></span>  

     <span data-ttu-id="3d7a1-125">Verdien i feltet **Foretrukket bankkonto** overføres til feltet **Mottakerbankkonto** på siden **Utbetalingskladd**.</span><span class="sxs-lookup"><span data-stu-id="3d7a1-125">The value in the **Preferred Bank Account** field is copied to the **Recipient Bank Account** field on the **Payment Journal** page.</span></span>  

### <a name="to-set-the-payment-journal-up-to-export-payment-files"></a><span data-ttu-id="3d7a1-126">Slik definerer du utbetalingskladden for eksport av betalingsfiler:</span><span class="sxs-lookup"><span data-stu-id="3d7a1-126">To set the payment journal up to export payment files</span></span>  
1. <span data-ttu-id="3d7a1-127">Skriv inn **Utbetalingskladder** i **Søk**-boksen, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="3d7a1-127">In the **Search** box, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3d7a1-128">Åpne utbetalingskladden du bruker til å behandle betalinger med, ved å eksportere filer i formatet for SEPA-kredittoverføring.</span><span class="sxs-lookup"><span data-stu-id="3d7a1-128">Open the payment journal that you use to process payments by exporting files in the SEPA Credit Transfer format.</span></span>  
3. <span data-ttu-id="3d7a1-129">Velg rulle\-gardinknappen i **Bunkenavn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3d7a1-129">In the **Batch Name** field, choose the drop\-down button.</span></span>  
4. <span data-ttu-id="3d7a1-130">Velg **Rediger oversikt** under **Behandle** på fanebladet **Hjem** på siden **Finanskladder**.</span><span class="sxs-lookup"><span data-stu-id="3d7a1-130">On the **General Journal Batches** page, on the **Home** tab, in the **Manage** group, choose **Edit List**.</span></span>  
5. <span data-ttu-id="3d7a1-131">På linjen for utbetalingskladden du vil bruke til å eksportere betalinger, merker du av for **Tillat betalingseksport**.</span><span class="sxs-lookup"><span data-stu-id="3d7a1-131">On the line for the payment journal that you will use to export payments, select the **Allow Payment Export** check box.</span></span>  

### <a name="to-connect-the-data-exchange-definition-for-one-or-more-payment-types-with-the-relevant-payment-method-or-methods"></a><span data-ttu-id="3d7a1-132">Slik knytter du datautvekslingsdefinisjon for én eller flere betalingstyper til de(n) aktuelle betalingsmåten(e):</span><span class="sxs-lookup"><span data-stu-id="3d7a1-132">To connect the data exchange definition for one or more payment types with the relevant payment method or methods</span></span>  
1. <span data-ttu-id="3d7a1-133">Skriv inn **Betalingsmåter** i **Søk**-boksen, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="3d7a1-133">In the **Search** box, enter **Payment Methods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3d7a1-134">På siden **Betalingsmåter** velger du betalingsmåten som brukes til å eksportere betalinger fra, og deretter velger du feltet **Definisjon av betalingseksportlinje**.</span><span class="sxs-lookup"><span data-stu-id="3d7a1-134">On the **Payment Methods** page, select the payment method that is used to export payments from, and then choose the **Pmt. Export Line Definition** field.</span></span>  
3. <span data-ttu-id="3d7a1-135">På siden **Definisjoner av betalingseksportlinje** velger du koden du angav i **Kode**-feltet på hurtigfanen **Linjedefinisjoner** i trinn 4 i delen "Slik beskriver du formateringen av linjer og kolonner i filen" i fremgangsmåten [Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="3d7a1-135">On the **Pmt. Export Line Definitions** page, select the code that you specified in the **Code** field on the **Line Definitions** FastTab in step 4 in the “To describe the formatting of lines and columns in the file” section in the [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md) procedure.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3d7a1-136">Se også</span><span class="sxs-lookup"><span data-stu-id="3d7a1-136">See Also</span></span>  
[<span data-ttu-id="3d7a1-137">Innkreve betalinger med SEPA Direct Debit</span><span class="sxs-lookup"><span data-stu-id="3d7a1-137">Collecting Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="3d7a1-138">Definere datautvekslingsdefinisjoner</span><span class="sxs-lookup"><span data-stu-id="3d7a1-138">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="3d7a1-139">Opprette gjentakende salgs- og kjøpslinjer</span><span class="sxs-lookup"><span data-stu-id="3d7a1-139">Create Recurring Sales and Purchase Lines</span></span>](sales-how-work-standard-lines.md)  
[<span data-ttu-id="3d7a1-140">Utveksle data elektronisk</span><span class="sxs-lookup"><span data-stu-id="3d7a1-140">Exchanging Data Electronically</span></span>](across-data-exchange.md)  

