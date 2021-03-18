---
title: Oversikt over oppgaver for å definere kjøp | Microsoft-dokumentasjon
description: Beskriver oppgaver for å definere selskapets innkjøpspolicyer og definere kjøpsprosessene.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement, supply, vendor order
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f16e82531825ccb0350b45bf4be20c3f8b5b9914
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383836"
---
# <a name="setting-up-purchasing"></a><span data-ttu-id="2ae65-103">Definere kjøp</span><span class="sxs-lookup"><span data-stu-id="2ae65-103">Setting Up Purchasing</span></span>
<span data-ttu-id="2ae65-104">Før du kan håndtere kjøpsprosesser, må du konfigurere regler og verdier som definerer selskapets kjøpsprinsipper.</span><span class="sxs-lookup"><span data-stu-id="2ae65-104">Before you can manage purchase processes, you must configure the rules and values that define the company's purchase policies.</span></span>

<span data-ttu-id="2ae65-105">Du må definere det generelle oppsettet, for eksempel hvilke kjøpsdokumenter som kreves, og hvordan verdiene i dem skal bokføres.</span><span class="sxs-lookup"><span data-stu-id="2ae65-105">You must define the general setup, such as which purchase documents are required and how their values are posted.</span></span> <span data-ttu-id="2ae65-106">Dette generelle oppsettet foretas vanligvis én gang under den første implementeringen.</span><span class="sxs-lookup"><span data-stu-id="2ae65-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="2ae65-107">En egen rekke oppgaver relatert til registrering av nye leverandører er å registrere alle spesialpris eller rabattavtaler som du har med hver leverandør.</span><span class="sxs-lookup"><span data-stu-id="2ae65-107">A separate series of tasks related to registering new vendors is to record any special price or discount agreements that you have with each vendor.</span></span>

<span data-ttu-id="2ae65-108">Finansrelatert kjøpsoppsett, for eksempel betalingsmåte og valutaer, beskrives i avsnittet Finansoppsett.</span><span class="sxs-lookup"><span data-stu-id="2ae65-108">Finance-related purchase setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="2ae65-109">Hvis du vil ha mer informasjon, kan du se [Konfigurere finans](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="2ae65-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="2ae65-110">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="2ae65-110">To</span></span> | <span data-ttu-id="2ae65-111">Se</span><span class="sxs-lookup"><span data-stu-id="2ae65-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="2ae65-112">Opprett et leverandørkort for hver leverandør som du kjøper fra.</span><span class="sxs-lookup"><span data-stu-id="2ae65-112">Create a vendor card for each vendor that you purchase from</span></span>|[<span data-ttu-id="2ae65-113">Registrere nye leverandører</span><span class="sxs-lookup"><span data-stu-id="2ae65-113">Register New Vendors</span></span>](purchasing-how-register-new-vendors.md) |
| <span data-ttu-id="2ae65-114">Angi de forskjellige rabattene og spesialprisene som leverandør gir deg avhengig av vare, antall og/eller dato.</span><span class="sxs-lookup"><span data-stu-id="2ae65-114">Enter the different discounts and special prices that vendors grant you depending on item, quantities, and/or date</span></span> |[<span data-ttu-id="2ae65-115">Registrere avtaler om kjøpspris, rabatt og betaling</span><span class="sxs-lookup"><span data-stu-id="2ae65-115">Record Purchase Price, Discount, and Payment Agreements</span></span>](purchasing-how-record-purchase-price-discount-payment-agreements.md) |
| <span data-ttu-id="2ae65-116">Prioritere leverandører</span><span class="sxs-lookup"><span data-stu-id="2ae65-116">Prioritize vendors</span></span> |[<span data-ttu-id="2ae65-117">Prioritere leverandører</span><span class="sxs-lookup"><span data-stu-id="2ae65-117">Prioritize Vendors</span></span>](purchasing-how-prioritize-vendors.md) |
| <span data-ttu-id="2ae65-118">Definere innkjøpere</span><span class="sxs-lookup"><span data-stu-id="2ae65-118">Set up purchasers</span></span> |[<span data-ttu-id="2ae65-119">Definere innkjøpere</span><span class="sxs-lookup"><span data-stu-id="2ae65-119">Set Up Purchasers</span></span>](purchasing-how-setup-purchasers.md) |
|<span data-ttu-id="2ae65-120">Angi standardrapporter som skal brukes for ulike dokumenttyper.</span><span class="sxs-lookup"><span data-stu-id="2ae65-120">Specify default reports to be used for different document types.</span></span>|[<span data-ttu-id="2ae65-121">Rapportvalg i Business Central</span><span class="sxs-lookup"><span data-stu-id="2ae65-121">Report Selection in Business Central</span></span>](across-report-selections.md)|

> [!TIP]
> <span data-ttu-id="2ae65-122">Avhengig av den geografiske plasseringen din kan enkelte sider inneholde felt som ikke er beskrevet i artiklene som er oppført her, fordi de gjelder for lokale funksjoner eller tilpasninger.</span><span class="sxs-lookup"><span data-stu-id="2ae65-122">Depending on your geographical location, some pages can contain fields that are not described in the articles that are listed here because they apply to local functionality or customizations.</span></span> [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="2ae65-123">Se relatert opplæring på [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="2ae65-123">See Related Training at [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="2ae65-124">Se også</span><span class="sxs-lookup"><span data-stu-id="2ae65-124">See Also</span></span>

[<span data-ttu-id="2ae65-125">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="2ae65-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="2ae65-126">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2ae65-126">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]