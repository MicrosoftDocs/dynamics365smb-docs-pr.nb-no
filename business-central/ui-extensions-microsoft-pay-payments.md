---
title: Microsoft Pay-standard | Microsoft-dokumentasjon
description: Gir informasjon om Microsoft Pay-utvidelsen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 748316c411c4b04947685c6053e9c53aa9102c35
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747571"
---
# <a name="the-microsoft-pay-extension"></a><span data-ttu-id="88b61-103">Microsoft Pay-utvidelsen</span><span class="sxs-lookup"><span data-stu-id="88b61-103">The Microsoft Pay Extension</span></span>

> [!IMPORTANT]
> <span data-ttu-id="88b61-104">Fra og med 8. februar 2020 vil endringer i Microsoft Pay-tjenesten påvirke Microsoft Pay-filtypen i Microsoft [!INCLUDE[prod_short](includes/prod_long.md)].</span><span class="sxs-lookup"><span data-stu-id="88b61-104">Effective February 8 2020, changes in the Microsoft Pay service will affect the Microsoft Pay extension in Microsoft [!INCLUDE[prod_short](includes/prod_long.md)].</span></span> <span data-ttu-id="88b61-105">På grunn av endringene vil **Betal nå**-betalingskoblinger som Microsoft Pay-utvidelsen genererer for fakturaer i [!INCLUDE[prod_short](includes/prod_short.md)], ikke åpne Microsoft Pay etter 8. februar.</span><span class="sxs-lookup"><span data-stu-id="88b61-105">Due to the changes, after February 8, the **Pay now** payment links that the Microsoft Pay extension generates for invoices in [!INCLUDE[prod_short](includes/prod_short.md)] will not open Microsoft Pay.</span></span> <span data-ttu-id="88b61-106">Kunder som bruker utvidelsen, bør endre oppsettet for Betalingstjenester for å begynne å bruke PayPal-utvidelsen i stedet.</span><span class="sxs-lookup"><span data-stu-id="88b61-106">Customers who are using the extension should change their Payment Services setup to start using the PayPal extension instead.</span></span><br /></br>
>
> <span data-ttu-id="88b61-107">Fra 8. januar vises det et varsel i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="88b61-107">From January 8, we will display a notification in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="88b61-108">Varselet vil inneholde en kobling til innstillingene du må endre, og til mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="88b61-108">The notification will contain a link to the settings that you need to change and to more information.</span></span> <span data-ttu-id="88b61-109">Etter 8. februar vil Microsoft Pay-utvidelsen ikke lenger være tilgjengelig i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="88b61-109">After February 8, the Microsoft Pay extension will no longer be available in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span><br /></br>
>
> <span data-ttu-id="88b61-110">Endringene påvirker følgende versjoner av Business Central:</span><span class="sxs-lookup"><span data-stu-id="88b61-110">The changes impact the following versions of Business Central:</span></span>
> - <span data-ttu-id="88b61-111">Microsoft Dynamics 365 Business Central, oktober 2018</span><span class="sxs-lookup"><span data-stu-id="88b61-111">Microsoft Dynamics 365 Business Central October 2018</span></span>
> - <span data-ttu-id="88b61-112">Microsoft Dynamics 365 Business Central, april 2019</span><span class="sxs-lookup"><span data-stu-id="88b61-112">Microsoft Dynamics 365 Business Central April 2019</span></span>
> - <span data-ttu-id="88b61-113">Microsoft Dynamics 365 Business Central 2019, utgivelsesplan 2</span><span class="sxs-lookup"><span data-stu-id="88b61-113">Microsoft Dynamics 365 Business Central 2019 Release Wave 2</span></span>

<span data-ttu-id="88b61-114">Kundene krever kontinuerlig bedre kundeservice, både når det gjelder produktkvalitet, men også når det gjelder leverings- og betalingstjenester.</span><span class="sxs-lookup"><span data-stu-id="88b61-114">Customers continuously require higher customer service, both in terms of the quality of product but also in terms of delivery and payment services.</span></span> <span data-ttu-id="88b61-115">Microsoft Pay-tjenesten hjelper deg med å forbedre din kundeservice.</span><span class="sxs-lookup"><span data-stu-id="88b61-115">The Microsoft Pay service helps you increase your customer service.</span></span>

<span data-ttu-id="88b61-116">Microsoft Pay-utvidelsen legger til en Microsoft Pay-kobling i salgsdokumenter slik at kundene kan enkelt betale med Microsoft Pay.</span><span class="sxs-lookup"><span data-stu-id="88b61-116">The Microsoft Pay extension adds a Microsoft Pay link to your sales documents so customers can easily pay using Microsoft Pay.</span></span> <span data-ttu-id="88b61-117">Du kan sende dokumenter via e-post for å gi bedre kundeservice og korte ned tiden det tar for kundens betalinger å komme inn på bankkontoen din.</span><span class="sxs-lookup"><span data-stu-id="88b61-117">Then you can send the documents by email to provide higher customer service and shorten the time it takes for customers’ payments to arrive on your bank account.</span></span>

<span data-ttu-id="88b61-118">Microsoft Pay-utvidelsen gir følgende fordeler:</span><span class="sxs-lookup"><span data-stu-id="88b61-118">The Microsoft Pay extension provides the following benefits:</span></span>
- <span data-ttu-id="88b61-119">Kundebetalinger kommer raskere inn på bankkontoen din.</span><span class="sxs-lookup"><span data-stu-id="88b61-119">Customer payments appear faster on your bank account.</span></span>
- <span data-ttu-id="88b61-120">Kunder har flere måter å betale fakturaer på.</span><span class="sxs-lookup"><span data-stu-id="88b61-120">Customers have more ways to pay invoices.</span></span>
- <span data-ttu-id="88b61-121">Microsoft Pay tilbyr en pålitelig betalingstjeneste, som kunder som foretrekker i stedet for å angi opplysninger om kredittkort på ukjente nettsteder.</span><span class="sxs-lookup"><span data-stu-id="88b61-121">Microsoft Pay offers a trustworthy payment service, which customers prefer to entering credit card information on unknown web sites.</span></span>
- <span data-ttu-id="88b61-122">Microsoft Pay tilbyr flere måter for å håndtere betalinger, inkludert behandling av kredittkortbetaling som PayPal og Stripe.</span><span class="sxs-lookup"><span data-stu-id="88b61-122">Microsoft Pay offers multiple ways of handling payments, including credit card processing, such as PayPal and Stripe.</span></span>
- <span data-ttu-id="88b61-123">Microsoft Pay-koblingen kan inkluderes automatisk på alle fakturadokumenter eller av brukeren.</span><span class="sxs-lookup"><span data-stu-id="88b61-123">The Microsoft Pay link can be embedded automatically on every invoice document or by the user.</span></span>
- <span data-ttu-id="88b61-124">Ettersom denne funksjonen er bygd som en utvidelse, får du full kontroll og kan aktivere den når og hvis forretningsprosessene trenger dette.</span><span class="sxs-lookup"><span data-stu-id="88b61-124">Because this functionality is built as an extension, it gives you full control to enable it when and if your business processes require it.</span></span>

<span data-ttu-id="88b61-125">Aktiverer utvidelser for betaling-tjenesten er gratis i [!INCLUDE[prod_short](includes/prod_short.md)], men du må kontakte tjenesten for å få en konto.</span><span class="sxs-lookup"><span data-stu-id="88b61-125">Enabling payment service extensions is free in [!INCLUDE[prod_short](includes/prod_short.md)], however, you will need to contact the payment service to get an account.</span></span> <span data-ttu-id="88b61-126">Hvis du vil ha mer informasjon, kan du se [Aktivere kundebetalinger gjennom betalingstjenester](sales-how-enable-payment-service-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="88b61-126">For more information, see [Enable Customer Payment Through Payment Services](sales-how-enable-payment-service-extensions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="88b61-127">Se også</span><span class="sxs-lookup"><span data-stu-id="88b61-127">See Also</span></span>
<span data-ttu-id="88b61-128">[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av utvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="88b61-128">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="88b61-129">Sette opp salg</span><span class="sxs-lookup"><span data-stu-id="88b61-129">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="88b61-130">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="88b61-130">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
