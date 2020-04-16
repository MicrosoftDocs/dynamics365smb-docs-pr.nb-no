---
title: Importere betalingsreturdata
description: Mottaks- og avregningsreturer importeres på siden Remitteringsoppdrag - les inn.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: eb2eb1413e71353412f78dc7d2ae878c2e2034e2
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181027"
---
# <a name="import-payment-return-data"></a><span data-ttu-id="14623-103">Importere betalingsreturdata</span><span class="sxs-lookup"><span data-stu-id="14623-103">Import Payment Return Data</span></span>
<span data-ttu-id="14623-104">Mottaks- og avregningsreturer importeres på siden **Remitteringsoppdrag - les inn**.</span><span class="sxs-lookup"><span data-stu-id="14623-104">To import receipt and settlement returns, use the **Rem. payment order – import** page.</span></span> <span data-ttu-id="14623-105">Hvis det oppstår feil under innlesingen av avregningsreturer, kan du vise denne informasjonen på siden **Avregningsopplysninger**.</span><span class="sxs-lookup"><span data-stu-id="14623-105">If any errors are indicated when importing settlement returns, you can view this information on the **Settlement Info** page.</span></span>  

## <a name="to-import-return-data"></a><span data-ttu-id="14623-106">Slik importerer du returdata</span><span class="sxs-lookup"><span data-stu-id="14623-106">To import return data</span></span>  

1.  <span data-ttu-id="14623-107">Velg ikonet ![Søk etter side eller rapport](../../media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Remitteringsoppdrag - les inn**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="14623-107">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Rem. payment order – import**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="14623-108">I hurtigfanen **Alternativer** fyller du ut feltene som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="14623-108">On the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="14623-109">Felt</span><span class="sxs-lookup"><span data-stu-id="14623-109">Field</span></span>|<span data-ttu-id="14623-110">Description</span><span class="sxs-lookup"><span data-stu-id="14623-110">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="14623-111">**Oppdragsbemerkning**</span><span class="sxs-lookup"><span data-stu-id="14623-111">**Payment order note**</span></span>|<span data-ttu-id="14623-112">Skriv inn en bemerkning som overføres til oppdraget.</span><span class="sxs-lookup"><span data-stu-id="14623-112">Enter a note that is transferred to the payment order.</span></span>|  
    |<span data-ttu-id="14623-113">**Kontrollkjørsel**</span><span class="sxs-lookup"><span data-stu-id="14623-113">**ControlBatch**</span></span>|<span data-ttu-id="14623-114">Merk av her for å verifisere returfilene på forhånd, for å sjekke om importen kan utføres.</span><span class="sxs-lookup"><span data-stu-id="14623-114">Select the check box to verify return files in advance to ensure if the import can be made.</span></span> <span data-ttu-id="14623-115">Returdata importeres ikke.</span><span class="sxs-lookup"><span data-stu-id="14623-115">Return data is not imported.</span></span>|  
    |<span data-ttu-id="14623-116">**Returfiler**</span><span class="sxs-lookup"><span data-stu-id="14623-116">**Return files**</span></span>|<span data-ttu-id="14623-117">Angir hvor mange returfiler som er funnet og lest inn.</span><span class="sxs-lookup"><span data-stu-id="14623-117">Specifies how many return files are found and imported.</span></span>|  

3.  <span data-ttu-id="14623-118">Velg **Returfiler**-knappen for å vise returfilene.</span><span class="sxs-lookup"><span data-stu-id="14623-118">Choose the **Return Files** button to display the return files.</span></span>  
4.  <span data-ttu-id="14623-119">På siden **Returfiler** velger du **Importer** ved siden av hver fil som skal importeres.</span><span class="sxs-lookup"><span data-stu-id="14623-119">On the **Return Files** page, select the **Import** option next to each file to be imported.</span></span> <span data-ttu-id="14623-120">Hvis alternativet ikke er merket, blir ikke filen importert.</span><span class="sxs-lookup"><span data-stu-id="14623-120">If the option is cleared, the file will not be imported.</span></span>  
5.  <span data-ttu-id="14623-121">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="14623-121">Choose the **OK** button.</span></span>  

## <a name="to-view-settlement-information"></a><span data-ttu-id="14623-122">Slik viser du avregningsopplysninger</span><span class="sxs-lookup"><span data-stu-id="14623-122">To view settlement information</span></span>  

1.  <span data-ttu-id="14623-123">Velg ikonet ![Søk etter side eller rapport](../../media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Avregningsopplysninger**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="14623-123">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Settlement Info**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="14623-124">I hurtigfanen **Generelt** viser du feltene som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="14623-124">On the **General** FastTab, view the fields as described in the following table.</span></span>  

    |<span data-ttu-id="14623-125">Felt</span><span class="sxs-lookup"><span data-stu-id="14623-125">Field</span></span>|<span data-ttu-id="14623-126">Description</span><span class="sxs-lookup"><span data-stu-id="14623-126">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="14623-127">**Remittering effektueringsref.**</span><span class="sxs-lookup"><span data-stu-id="14623-127">**Remittance Handling Ref.**</span></span>|<span data-ttu-id="14623-128">Viser referansen som banken angir for betalinger utland.</span><span class="sxs-lookup"><span data-stu-id="14623-128">Shows the reference that the bank enters for foreign payments.</span></span>|  
    |<span data-ttu-id="14623-129">**Remittering advarsel**</span><span class="sxs-lookup"><span data-stu-id="14623-129">**Remittance Warning**</span></span>|<span data-ttu-id="14623-130">Hvis dette alternativet er valgt, inneholder kladdelinjen en advarsel.</span><span class="sxs-lookup"><span data-stu-id="14623-130">If selected, the journal line contains a warning.</span></span>|  
    |<span data-ttu-id="14623-131">**Remittering advarseltekst**</span><span class="sxs-lookup"><span data-stu-id="14623-131">**Remittance Warning Text**</span></span>|<span data-ttu-id="14623-132">Viser beskrivelsen av advarselen, hvis relevant.</span><span class="sxs-lookup"><span data-stu-id="14623-132">Shows the description of the warning, if applicable.</span></span>|  

3.  <span data-ttu-id="14623-133">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="14623-133">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="14623-134">Se også</span><span class="sxs-lookup"><span data-stu-id="14623-134">See Also</span></span>  
 <span data-ttu-id="14623-135">[Elektroniske betalinger til leverandører i Norge](electronic-payments-to-vendors-in-norway.md) </span><span class="sxs-lookup"><span data-stu-id="14623-135">[Electronic Payments to Vendors in Norway](electronic-payments-to-vendors-in-norway.md) </span></span>  
 <span data-ttu-id="14623-136">[Sette opp remitteringsavtaler](how-to-set-up-remittance-agreements.md) </span><span class="sxs-lookup"><span data-stu-id="14623-136">[Set Up Remittance Agreements](how-to-set-up-remittance-agreements.md) </span></span>  
 <span data-ttu-id="14623-137">[Opprette remitteringskontoer](how-to-create-remittance-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="14623-137">[Create Remittance Accounts](how-to-create-remittance-accounts.md) </span></span>  
 <span data-ttu-id="14623-138">[Angi leverandører for remittering](how-to-set-up-vendors-for-remittance.md) </span><span class="sxs-lookup"><span data-stu-id="14623-138">[Set Up Vendors for Remittance](how-to-set-up-vendors-for-remittance.md) </span></span>  
 <span data-ttu-id="14623-139">[Mottakerreferansekoder](recipient-reference-codes.md) </span><span class="sxs-lookup"><span data-stu-id="14623-139">[Recipient Reference Codes](recipient-reference-codes.md) </span></span>  
 <span data-ttu-id="14623-140">[Opprette remitteringsforslag](how-to-create-remittance-suggestions.md) </span><span class="sxs-lookup"><span data-stu-id="14623-140">[Create Remittance Suggestions](how-to-create-remittance-suggestions.md) </span></span>  
 <span data-ttu-id="14623-141">[Opprette manuelle remitteringsoppdrag](how-to-create-manual-remittance-payments.md) </span><span class="sxs-lookup"><span data-stu-id="14623-141">[Create Manual Remittance Payments](how-to-create-manual-remittance-payments.md) </span></span>  
 <span data-ttu-id="14623-142">[Definere betalingslinjeinformasjon](how-to-set-up-payment-line-information.md) </span><span class="sxs-lookup"><span data-stu-id="14623-142">[Set Up Payment Line Information](how-to-set-up-payment-line-information.md) </span></span>  
 <span data-ttu-id="14623-143">[Kontrollere remitteringsoppdrag](how-to-test-remittance-payments.md) </span><span class="sxs-lookup"><span data-stu-id="14623-143">[Test Remittance Payments](how-to-test-remittance-payments.md) </span></span>  
 <span data-ttu-id="14623-144">[Eksportere remitteringsoppdrag](how-to-export-remittance-payments.md) </span><span class="sxs-lookup"><span data-stu-id="14623-144">[Export Remittance Payments](how-to-export-remittance-payments.md) </span></span>  
 <span data-ttu-id="14623-145">[Typer betalingsreturfiler](types-of-payment-returns-files.md) </span><span class="sxs-lookup"><span data-stu-id="14623-145">[Types of Payment Returns Files](types-of-payment-returns-files.md) </span></span>  
 <span data-ttu-id="14623-146">[Slette remitteringsoppdrag](how-to-delete-remittance-payment-orders.md) </span><span class="sxs-lookup"><span data-stu-id="14623-146">[Delete Remittance Payment Orders](how-to-delete-remittance-payment-orders.md) </span></span>  
 <span data-ttu-id="14623-147">[Remitteringsfeil](remittance-errors.md) </span><span class="sxs-lookup"><span data-stu-id="14623-147">[Remittance Errors](remittance-errors.md) </span></span>  
 <span data-ttu-id="14623-148">[Vise remitteringsfeilkoder](how-to-view-remittance-error-codes.md) </span><span class="sxs-lookup"><span data-stu-id="14623-148">[View Remittance Error Codes](how-to-view-remittance-error-codes.md) </span></span>  
 [<span data-ttu-id="14623-149">Annullere betalinger</span><span class="sxs-lookup"><span data-stu-id="14623-149">Cancel Payments</span></span>](how-to-cancel-payments.md)
