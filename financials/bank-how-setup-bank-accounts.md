---
title: Opprette bankkonti | Microsoft-dokumentasjon
description: Du kan avstemme bankkonti i Financials med kontoutdrag fra banken.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: f46e95e24ef39a93bc93cfda1b9c575b07273566
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-set-up-bank-accounts"></a><span data-ttu-id="88e2b-103">Opprette bankkonti</span><span class="sxs-lookup"><span data-stu-id="88e2b-103">How to: Set Up Bank Accounts</span></span>
<span data-ttu-id="88e2b-104">Du bruker bankkonti i [!INCLUDE[d365fin](includes/d365fin_md.md)] til å holde orden på banktransaksjonene dine.</span><span class="sxs-lookup"><span data-stu-id="88e2b-104">You use bank accounts in the [!INCLUDE[d365fin](includes/d365fin_md.md)] to keep track of your banking transactions.</span></span> <span data-ttu-id="88e2b-105">Konti kan utstedes i norske kroner eller i fremmed valuta.</span><span class="sxs-lookup"><span data-stu-id="88e2b-105">Accounts can be denominated in your local currency or in a foreign currency.</span></span> <span data-ttu-id="88e2b-106">Når du har opprettet bankkonti, kan du bruke mulighetene for utskriving av sjekker (gjelder ikke Norge).</span><span class="sxs-lookup"><span data-stu-id="88e2b-106">After you have set up bank accounts, you can also use the check printing option.</span></span>

## <a name="to-set-up-bank-accounts"></a><span data-ttu-id="88e2b-107">Slik setter du opp bankkonti</span><span class="sxs-lookup"><span data-stu-id="88e2b-107">To set up bank accounts</span></span>
1. <span data-ttu-id="88e2b-108">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Bankkonti**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="88e2b-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="88e2b-109">I vinduet **Bankkonti** velger du handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="88e2b-109">In the **Bank Accounts** window, choose the **New** action.</span></span>
3. <span data-ttu-id="88e2b-110">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="88e2b-110">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a><span data-ttu-id="88e2b-111">Opprette din bankkonto for import eller eksport av bankfilene</span><span class="sxs-lookup"><span data-stu-id="88e2b-111">To set up your bank account for import or export of bank files</span></span>
<span data-ttu-id="88e2b-112">Felt i hurtigafnen **Overføring** i vinduet **Bankkontokort** er relatert til import og eksport av bankfeeder og filer.</span><span class="sxs-lookup"><span data-stu-id="88e2b-112">Fields on the **Transfer** FastTab in the **Bank Account Card** window are related to import and export of bank feeds and files.</span></span> <span data-ttu-id="88e2b-113">Hvis du vil ha mer informasjon, kan du se [Konfigurere konverteringstjenesten for bankdata](bank-how-setup-bank-data-conversion-service.md) og [Kofigurere Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="88e2b-113">For more information, see [How to: Set Up the Bank Data Conversion Service](bank-how-setup-bank-data-conversion-service.md) and [How to: Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

1. <span data-ttu-id="88e2b-114">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Bankkonti**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="88e2b-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="88e2b-115">Åpne kortet for en bankkonto som du vil eksportere eller importere bankfiler for.</span><span class="sxs-lookup"><span data-stu-id="88e2b-115">Open the card for a bank account that you will export or import bank files for.</span></span>
3. <span data-ttu-id="88e2b-116">Fyll ut feltene på hurtigfanen **Overføring** etter behov.</span><span class="sxs-lookup"><span data-stu-id="88e2b-116">On the **Transfer** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="88e2b-117">Andre fileksporttjenester og formater krever ulike oppsettsverdier i vinduet **Bankkort**.</span><span class="sxs-lookup"><span data-stu-id="88e2b-117">Different file export services and their formats require different setup values in the **Bank Account Card** window.</span></span> <span data-ttu-id="88e2b-118">Du blir informert om feil eller manglende oppsettsverdier når du prøver å eksportere filen.</span><span class="sxs-lookup"><span data-stu-id="88e2b-118">You will be informed about wrong or missing setup values as you try to export the file.</span></span> <span data-ttu-id="88e2b-119">Les derfor de korte beskrivelsene av feltene nøye, eller se relaterte fremgangsmåteeemner.</span><span class="sxs-lookup"><span data-stu-id="88e2b-119">So read the short descriptions of the fields carefully or refer to the related procedure topics.</span></span> <span data-ttu-id="88e2b-120">Hvis du for eksempel eksporterer en betalingsfil for Nord-Amerika elektronisk pengeoverføring (EFT) krever at både **Nr. for siste remitteringsmelding**</span><span class="sxs-lookup"><span data-stu-id="88e2b-120">For example, exporting a payment file for North American electronic funds transfer (EFT) requires that both the **Last Remittance Advice No.**</span></span> <span data-ttu-id="88e2b-121">og **Transittnr.**</span><span class="sxs-lookup"><span data-stu-id="88e2b-121">field and the **Transit No.**</span></span> <span data-ttu-id="88e2b-122">er fylt ut.</span><span class="sxs-lookup"><span data-stu-id="88e2b-122">field are filled in.</span></span> <span data-ttu-id="88e2b-123">Hvis du vil ha mer informasjon, kan du se [Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="88e2b-123">For more information, see [How to: Export Payments to a Bank File](payables-how-export-payments-bank-file.md).</span></span>

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a><span data-ttu-id="88e2b-124">Opprette dine leverandørbankkonti for import eller eksport av bankfilene</span><span class="sxs-lookup"><span data-stu-id="88e2b-124">To set up vendor bank accounts for export of bank files</span></span>
<span data-ttu-id="88e2b-125">Felt i hurtigafnen **Overføring** i vinduet **Leverandørs bankkort** er relatert til eksport av bankfeeder og filer.</span><span class="sxs-lookup"><span data-stu-id="88e2b-125">Fields on the **Transfer** FastTab in the **Vendor Bank Account Card** window are related to export of bank feeds and files.</span></span> <span data-ttu-id="88e2b-126">Hvis du vil ha mer informasjon, kan du se [Konfigurere tjeneste for konvertering av bankdata](bank-how-setup-bank-data-conversion-service.md) og [Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="88e2b-126">For more information, see [How to: Set Up the Bank Data Conversion Service](bank-how-setup-bank-data-conversion-service.md) and [How to: Export Payments to a Bank File](payables-how-export-payments-bank-file.md).</span></span>

1. <span data-ttu-id="88e2b-127">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Leverandører**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="88e2b-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="88e2b-128">Åpne kortet for en leverandør med en bankkonto som du vil eksportere betalingsbankfiler til.</span><span class="sxs-lookup"><span data-stu-id="88e2b-128">Open the card for a vendor whose bank account you will export payment bank files to.</span></span>
3. <span data-ttu-id="88e2b-129">Velg **Bankkonti**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="88e2b-129">Choose the **Bank Accounts** action.</span></span>
3. <span data-ttu-id="88e2b-130">I vinduet **Leverandørs bankkort**, i hurtigfanen **Overføring**, fyller du ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="88e2b-130">In the **Vendor Bank Account Card** window, on the **Transfer** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="88e2b-131">Se også</span><span class="sxs-lookup"><span data-stu-id="88e2b-131">See Also</span></span>
[<span data-ttu-id="88e2b-132">Konfigurere banktjenester</span><span class="sxs-lookup"><span data-stu-id="88e2b-132">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="88e2b-133">Håndtere bankkonti</span><span class="sxs-lookup"><span data-stu-id="88e2b-133">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
<span data-ttu-id="88e2b-134">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="88e2b-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

