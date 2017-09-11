---
title: Angi oppsettet for en sjekk | Microsoft-dokumentasjon
description: "Du kan utforme og skrive ut sjekker i forskjellige formater for å følge standarder."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 06/15/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: a2db2860846cd9b8010222faf580f0c9889e39a4
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-define-check-layouts"></a><span data-ttu-id="e8d3c-103">Definere sjekkoppsett</span><span class="sxs-lookup"><span data-stu-id="e8d3c-103">How to: Define Check Layouts</span></span>
<span data-ttu-id="e8d3c-104">Du kan utforme sjekkene dine slik at de samsvarer med standardene som er angitt av de lokale myndighetene.</span><span class="sxs-lookup"><span data-stu-id="e8d3c-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="e8d3c-105">Sjekkbilder kan skrives ut på engelsk, fransk eller spansk.</span><span class="sxs-lookup"><span data-stu-id="e8d3c-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="e8d3c-106">Sjekkene er utformet for utskrift i sjekkbildeformatene for USA og Canada i formatet sjekk-blankett-sjekk eller blankett-sjekk-blankett.</span><span class="sxs-lookup"><span data-stu-id="e8d3c-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="e8d3c-107">Definere sjekkoppsett</span><span class="sxs-lookup"><span data-stu-id="e8d3c-107">To define check layouts</span></span>
1. <span data-ttu-id="e8d3c-108">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Rapportvalg - bankkonto**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e8d3c-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="e8d3c-109">I **Rapportvalg - bankkonto**</span><span class="sxs-lookup"><span data-stu-id="e8d3c-109">In the **Report Selection - Bank Acc.**</span></span> <span data-ttu-id="e8d3c-110">-vinduet, i feltet **Bruk**, velger du **Sjekk**.</span><span class="sxs-lookup"><span data-stu-id="e8d3c-110">window, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="e8d3c-111">Velg én av følgende rapport-ID-er:</span><span class="sxs-lookup"><span data-stu-id="e8d3c-111">Select one of the following report IDs.</span></span>

| <span data-ttu-id="e8d3c-112">Rapport-ID</span><span class="sxs-lookup"><span data-stu-id="e8d3c-112">Report ID</span></span> | <span data-ttu-id="e8d3c-113">Rapportnavn</span><span class="sxs-lookup"><span data-stu-id="e8d3c-113">Report Name</span></span> | <span data-ttu-id="e8d3c-114">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e8d3c-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e8d3c-115">1401</span><span class="sxs-lookup"><span data-stu-id="e8d3c-115">1401</span></span> |<span data-ttu-id="e8d3c-116">Sjekk</span><span class="sxs-lookup"><span data-stu-id="e8d3c-116">Check</span></span> |<span data-ttu-id="e8d3c-117">Dette er standardrapporten.</span><span class="sxs-lookup"><span data-stu-id="e8d3c-117">This is the default report.</span></span> |
| <span data-ttu-id="e8d3c-118">10401</span><span class="sxs-lookup"><span data-stu-id="e8d3c-118">10401</span></span> |<span data-ttu-id="e8d3c-119">Sjekk (blanket/blankett/sjekk)</span><span class="sxs-lookup"><span data-stu-id="e8d3c-119">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="e8d3c-120">Denne rapporten er utformet for utskrift i formatet blankett/blankett/sjekk.</span><span class="sxs-lookup"><span data-stu-id="e8d3c-120">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="e8d3c-121">10411</span><span class="sxs-lookup"><span data-stu-id="e8d3c-121">10411</span></span> |<span data-ttu-id="e8d3c-122">Sjekk (blanket/sjekk/blankett)</span><span class="sxs-lookup"><span data-stu-id="e8d3c-122">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="e8d3c-123">Denne rapporten er utformet for utskrift i formatet sjekk/blankett/sjekk.</span><span class="sxs-lookup"><span data-stu-id="e8d3c-123">This report is designed to print checks in a check/stub/check format.</span></span> |

<span data-ttu-id="e8d3c-124">Når du har definert sjekkoppsettene, kan du skrive ut sjekker fra vinduet **Betalingskladd**.</span><span class="sxs-lookup"><span data-stu-id="e8d3c-124">When you have set up check layouts, you can print checks from the **Payment Journal** window.</span></span> <span data-ttu-id="e8d3c-125">Hvis du vil ha mer informasjon, kan du se [Arbeide med sjekker](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="e8d3c-125">For more information, see [How to: Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e8d3c-126">Se også</span><span class="sxs-lookup"><span data-stu-id="e8d3c-126">See Also</span></span>
[<span data-ttu-id="e8d3c-127">Administrere skyldige beløp</span><span class="sxs-lookup"><span data-stu-id="e8d3c-127">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="e8d3c-128">[Håndtere bankkonti](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="e8d3c-128">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="e8d3c-129">Fullføre prosesser ved periodens slutt</span><span class="sxs-lookup"><span data-stu-id="e8d3c-129">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="e8d3c-130">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e8d3c-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="e8d3c-131">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="e8d3c-131">General Business Functionality</span></span>](ui-across-business-areas.md)

