---
title: Oversikt over oppgaver for å definere kjøp | Microsoft-dokumentasjon
description: Beskriver oppgaver for å definere selskapets innkjøpspolicyer og definere kjøpsprosessene.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement, supply, vendor order
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 219c1fcf1d4929a548f9a8d5849dde77f1c0b24a
ms.sourcegitcommit: 32bfc2acaaf3693afc9aeb86feea505fd328caa1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/19/2021
ms.locfileid: "5024590"
---
# <a name="setting-up-purchasing"></a><span data-ttu-id="d33b3-103">Definere kjøp</span><span class="sxs-lookup"><span data-stu-id="d33b3-103">Setting Up Purchasing</span></span>
<span data-ttu-id="d33b3-104">Før du kan håndtere kjøpsprosesser, må du konfigurere regler og verdier som definerer selskapets kjøpsprinsipper.</span><span class="sxs-lookup"><span data-stu-id="d33b3-104">Before you can manage purchase processes, you must configure the rules and values that define the company's purchase policies.</span></span>

<span data-ttu-id="d33b3-105">Du må definere det generelle oppsettet, for eksempel hvilke kjøpsdokumenter som kreves, og hvordan verdiene i dem skal bokføres.</span><span class="sxs-lookup"><span data-stu-id="d33b3-105">You must define the general setup, such as which purchase documents are required and how their values are posted.</span></span> <span data-ttu-id="d33b3-106">Dette generelle oppsettet foretas vanligvis én gang under den første implementeringen.</span><span class="sxs-lookup"><span data-stu-id="d33b3-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="d33b3-107">En egen rekke oppgaver relatert til registrering av nye leverandører er å registrere alle spesialpris eller rabattavtaler som du har med hver leverandør.</span><span class="sxs-lookup"><span data-stu-id="d33b3-107">A separate series of tasks related to registering new vendors is to record any special price or discount agreements that you have with each vendor.</span></span>

<span data-ttu-id="d33b3-108">Finansrelatert kjøpsoppsett, for eksempel betalingsmåte og valutaer, beskrives i avsnittet Finansoppsett.</span><span class="sxs-lookup"><span data-stu-id="d33b3-108">Finance-related purchase setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="d33b3-109">Hvis du vil ha mer informasjon, kan du se [Konfigurere finans](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="d33b3-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="d33b3-110">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="d33b3-110">To</span></span> | <span data-ttu-id="d33b3-111">Se</span><span class="sxs-lookup"><span data-stu-id="d33b3-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="d33b3-112">Opprett et leverandørkort for hver leverandør som du kjøper fra.</span><span class="sxs-lookup"><span data-stu-id="d33b3-112">Create a vendor card for each vendor that you purchase from</span></span>|[<span data-ttu-id="d33b3-113">Registrere nye leverandører</span><span class="sxs-lookup"><span data-stu-id="d33b3-113">Register New Vendors</span></span>](purchasing-how-register-new-vendors.md) |
| <span data-ttu-id="d33b3-114">Angi de forskjellige rabattene og spesialprisene som leverandør gir deg avhengig av vare, antall og/eller dato.</span><span class="sxs-lookup"><span data-stu-id="d33b3-114">Enter the different discounts and special prices that vendors grant you depending on item, quantities, and/or date</span></span> |[<span data-ttu-id="d33b3-115">Registrere avtaler om kjøpspris, rabatt og betaling</span><span class="sxs-lookup"><span data-stu-id="d33b3-115">Record Purchase Price, Discount, and Payment Agreements</span></span>](purchasing-how-record-purchase-price-discount-payment-agreements.md) |
| <span data-ttu-id="d33b3-116">Prioritere leverandører</span><span class="sxs-lookup"><span data-stu-id="d33b3-116">Prioritize vendors</span></span> |[<span data-ttu-id="d33b3-117">Prioritere leverandører</span><span class="sxs-lookup"><span data-stu-id="d33b3-117">Prioritize Vendors</span></span>](purchasing-how-prioritize-vendors.md) |
| <span data-ttu-id="d33b3-118">Definere innkjøpere</span><span class="sxs-lookup"><span data-stu-id="d33b3-118">Set up purchasers</span></span> |[<span data-ttu-id="d33b3-119">Definere innkjøpere</span><span class="sxs-lookup"><span data-stu-id="d33b3-119">Set Up Purchasers</span></span>](purchasing-how-setup-purchasers.md) |
|<span data-ttu-id="d33b3-120">Angi standardrapporter som skal brukes for ulike dokumenttyper.</span><span class="sxs-lookup"><span data-stu-id="d33b3-120">Specify default reports to be used for different document types.</span></span>|[<span data-ttu-id="d33b3-121">Rapportvalg i Business Central</span><span class="sxs-lookup"><span data-stu-id="d33b3-121">Report Selection in Business Central</span></span>](across-report-selections.md)|

> [!TIP]
> <span data-ttu-id="d33b3-122">Avhengig av den geografiske plasseringen din kan enkelte sider inneholde felt som ikke er beskrevet i artiklene som er oppført her, fordi de gjelder for lokale funksjoner eller tilpasninger.</span><span class="sxs-lookup"><span data-stu-id="d33b3-122">Depending on your geographical location, some pages can contain fields that are not described in the articles that are listed here because they apply to local functionality or customizations.</span></span> [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="d33b3-123">Se relatert opplæring på [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="d33b3-123">See Related Training at [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="d33b3-124">Se også</span><span class="sxs-lookup"><span data-stu-id="d33b3-124">See Also</span></span>

[<span data-ttu-id="d33b3-125">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="d33b3-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="d33b3-126">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d33b3-126">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
