---
title: Angi oppsettet for en sjekk | Microsoft-dokumentasjon
description: Du kan utforme og skrive ut sjekker i forskjellige formater for å følge standarder.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: eace865bc70f56206d478f8e8d38fd217133925e
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "935261"
---
# <a name="define-check-layouts"></a><span data-ttu-id="f41d8-103">Definere sjekkoppsett</span><span class="sxs-lookup"><span data-stu-id="f41d8-103">Define Check Layouts</span></span>
<span data-ttu-id="f41d8-104">Du kan utforme sjekkene dine slik at de samsvarer med standardene som er angitt av de lokale myndighetene.</span><span class="sxs-lookup"><span data-stu-id="f41d8-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="f41d8-105">Sjekkbilder kan skrives ut på engelsk, fransk eller spansk.</span><span class="sxs-lookup"><span data-stu-id="f41d8-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="f41d8-106">Sjekkene er utformet for utskrift i sjekkbildeformatene for USA og Canada i formatet sjekk-blankett-sjekk eller blankett-sjekk-blankett.</span><span class="sxs-lookup"><span data-stu-id="f41d8-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="f41d8-107">Definere sjekkoppsett</span><span class="sxs-lookup"><span data-stu-id="f41d8-107">To define check layouts</span></span>
1. <span data-ttu-id="f41d8-108">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rapportvalg – bankkonto**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="f41d8-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="f41d8-109">På siden **Rapportvalg - bankkonto**, i **Bruk**-feltet, velger du **Sjekk**.</span><span class="sxs-lookup"><span data-stu-id="f41d8-109">On the **Report Selection - Bank Acc.** page, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="f41d8-110">Velg én av følgende rapport-ID-er:</span><span class="sxs-lookup"><span data-stu-id="f41d8-110">Select one of the following report IDs.</span></span>

| <span data-ttu-id="f41d8-111">Rapport-ID</span><span class="sxs-lookup"><span data-stu-id="f41d8-111">Report ID</span></span> | <span data-ttu-id="f41d8-112">Rapportnavn</span><span class="sxs-lookup"><span data-stu-id="f41d8-112">Report Name</span></span> | <span data-ttu-id="f41d8-113">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f41d8-113">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f41d8-114">1401</span><span class="sxs-lookup"><span data-stu-id="f41d8-114">1401</span></span> |<span data-ttu-id="f41d8-115">Sjekk</span><span class="sxs-lookup"><span data-stu-id="f41d8-115">Check</span></span> |<span data-ttu-id="f41d8-116">Dette er standardrapporten.</span><span class="sxs-lookup"><span data-stu-id="f41d8-116">This is the default report.</span></span> |
| <span data-ttu-id="f41d8-117">10401</span><span class="sxs-lookup"><span data-stu-id="f41d8-117">10401</span></span> |<span data-ttu-id="f41d8-118">Sjekk (blanket/blankett/sjekk)</span><span class="sxs-lookup"><span data-stu-id="f41d8-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="f41d8-119">Denne rapporten er utformet for utskrift i formatet blankett/blankett/sjekk.</span><span class="sxs-lookup"><span data-stu-id="f41d8-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="f41d8-120">10411</span><span class="sxs-lookup"><span data-stu-id="f41d8-120">10411</span></span> |<span data-ttu-id="f41d8-121">Sjekk (blanket/sjekk/blankett)</span><span class="sxs-lookup"><span data-stu-id="f41d8-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="f41d8-122">Denne rapporten er utformet for utskrift i formatet sjekk/blankett/sjekk.</span><span class="sxs-lookup"><span data-stu-id="f41d8-122">This report is designed to print checks in a check/stub/check format.</span></span> |

<span data-ttu-id="f41d8-123">Når du har definert sjekkoppsettene, kan du skrive ut sjekker fra siden **Betalingskladd**.</span><span class="sxs-lookup"><span data-stu-id="f41d8-123">When you have set up check layouts, you can print checks from the **Payment Journal** page.</span></span> <span data-ttu-id="f41d8-124">Hvis du vil ha mer informasjon, kan du se [Arbeide med sjekker](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="f41d8-124">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f41d8-125">Se også</span><span class="sxs-lookup"><span data-stu-id="f41d8-125">See Also</span></span>
[<span data-ttu-id="f41d8-126">Administrere skyldige beløp</span><span class="sxs-lookup"><span data-stu-id="f41d8-126">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="f41d8-127">[Håndtere bankkonti](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="f41d8-127">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="f41d8-128">Fullføre prosesser ved periodens slutt</span><span class="sxs-lookup"><span data-stu-id="f41d8-128">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="f41d8-129">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f41d8-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="f41d8-130">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="f41d8-130">General Business Functionality</span></span>](ui-across-business-areas.md)
