---
title: Angi oppsettet for en sjekk | Microsoft-dokumentasjon
description: Du kan utforme og skrive ut sjekker i forskjellige formater for å følge standarder.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 06/24/2019
ms.author: edupont
ms.openlocfilehash: 6ba5b6f0f91e207ec8ffedf5b45003a5787b9e0f
ms.sourcegitcommit: 0854c074b500c3031eaf86fde9d452f93f238081
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/24/2019
ms.locfileid: "1701132"
---
# <a name="select-a-check-layout"></a><span data-ttu-id="b112b-103">Velg et sjekkoppsett</span><span class="sxs-lookup"><span data-stu-id="b112b-103">Select a Check Layout</span></span>
<span data-ttu-id="b112b-104">Du kan utforme sjekkene dine slik at de samsvarer med standardene som er angitt av de lokale myndighetene.</span><span class="sxs-lookup"><span data-stu-id="b112b-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="b112b-105">Sjekkbilder kan skrives ut på engelsk, fransk eller spansk.</span><span class="sxs-lookup"><span data-stu-id="b112b-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="b112b-106">Sjekkene er utformet for utskrift i sjekkbildeformatene for USA og Canada i formatet sjekk-blankett-sjekk eller blankett-sjekk-blankett.</span><span class="sxs-lookup"><span data-stu-id="b112b-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-select-a-check-layout"></a><span data-ttu-id="b112b-107">Slik velger du et sjekkoppsett</span><span class="sxs-lookup"><span data-stu-id="b112b-107">To select a check layout</span></span>
1. <span data-ttu-id="b112b-108">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rapportvalg – bankkonto**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b112b-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="b112b-109">På siden **Rapportvalg - bankkonto**, i **Bruk**-feltet, velger du **Sjekk**.</span><span class="sxs-lookup"><span data-stu-id="b112b-109">On the **Report Selection - Bank Acc.** page, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="b112b-110">Velg én av følgende rapport-ID-er:</span><span class="sxs-lookup"><span data-stu-id="b112b-110">Select one of the following report IDs.</span></span>

| <span data-ttu-id="b112b-111">Rapport-ID</span><span class="sxs-lookup"><span data-stu-id="b112b-111">Report ID</span></span> | <span data-ttu-id="b112b-112">Rapportnavn</span><span class="sxs-lookup"><span data-stu-id="b112b-112">Report Name</span></span> | <span data-ttu-id="b112b-113">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="b112b-113">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="b112b-114">1401</span><span class="sxs-lookup"><span data-stu-id="b112b-114">1401</span></span> |<span data-ttu-id="b112b-115">Sjekk</span><span class="sxs-lookup"><span data-stu-id="b112b-115">Check</span></span> |<span data-ttu-id="b112b-116">Dette er standardrapporten.</span><span class="sxs-lookup"><span data-stu-id="b112b-116">This is the default report.</span></span> |
| <span data-ttu-id="b112b-117">10411</span><span class="sxs-lookup"><span data-stu-id="b112b-117">10411</span></span> |<span data-ttu-id="b112b-118">Sjekk (blanket/blankett/sjekk)</span><span class="sxs-lookup"><span data-stu-id="b112b-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="b112b-119">Denne rapporten er utformet for utskrift i formatet blankett/blankett/sjekk.</span><span class="sxs-lookup"><span data-stu-id="b112b-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="b112b-120">10412</span><span class="sxs-lookup"><span data-stu-id="b112b-120">10412</span></span> |<span data-ttu-id="b112b-121">Sjekk (blanket/sjekk/blankett)</span><span class="sxs-lookup"><span data-stu-id="b112b-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="b112b-122">Denne rapporten er utformet for utskrift i formatet blankett/sjekk/blankett.</span><span class="sxs-lookup"><span data-stu-id="b112b-122">This report is designed to print checks in a stub/check/stub format.</span></span> |
| <span data-ttu-id="b112b-123">10413</span><span class="sxs-lookup"><span data-stu-id="b112b-123">10413</span></span> |<span data-ttu-id="b112b-124">Tre sjekker side</span><span class="sxs-lookup"><span data-stu-id="b112b-124">Three Checks per Page</span></span> |<span data-ttu-id="b112b-125">Denne rapporten er utformet for å skrive ut tre sjekker på hver side.</span><span class="sxs-lookup"><span data-stu-id="b112b-125">This report is designed to print three checks on each page.</span></span> |

<span data-ttu-id="b112b-126">Når du har definert sjekkoppsettene, kan du skrive ut sjekker fra siden **Betalingskladd**.</span><span class="sxs-lookup"><span data-stu-id="b112b-126">When you have set up check layouts, you can print checks from the **Payment Journal** page.</span></span> <span data-ttu-id="b112b-127">Hvis du vil ha mer informasjon, kan du se [Arbeide med sjekker](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="b112b-127">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

<span data-ttu-id="b112b-128">Hvis du vil endre en av disse standardsjekkoppsettene, bruker du Word- eller RDLC-integrasjonen til å gjøre dette.</span><span class="sxs-lookup"><span data-stu-id="b112b-128">To change one of these default check layouts, use either the Word or the RDLC integration to do so.</span></span> <span data-ttu-id="b112b-129">Hvis du vil ha mer informasjon, kan du se [Opprette og endre et egendefinert rapportoppsett eller dokumentoppsett](ui-how-create-custom-report-layout.md).</span><span class="sxs-lookup"><span data-stu-id="b112b-129">For more information, see [Create and Modify a Custom Report or Document Layout](ui-how-create-custom-report-layout.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b112b-130">Se også</span><span class="sxs-lookup"><span data-stu-id="b112b-130">See Also</span></span>
[<span data-ttu-id="b112b-131">Opprette og endre et egendefinert rapportoppsett eller dokumentoppsett</span><span class="sxs-lookup"><span data-stu-id="b112b-131">Create and Modify a Custom Report or Document Layout</span></span>](ui-how-create-custom-report-layout.md)  
[<span data-ttu-id="b112b-132">Administrere skyldige beløp</span><span class="sxs-lookup"><span data-stu-id="b112b-132">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="b112b-133">[Håndtere bankkonti](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="b112b-133">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="b112b-134">Fullføre prosesser ved periodens slutt</span><span class="sxs-lookup"><span data-stu-id="b112b-134">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="b112b-135">[Arbeide med [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b112b-135">[Working with [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="b112b-136">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="b112b-136">General Business Functionality</span></span>](ui-across-business-areas.md)
