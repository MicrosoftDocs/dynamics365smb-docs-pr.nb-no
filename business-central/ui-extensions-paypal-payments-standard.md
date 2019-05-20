---
title: Bruke PayPal Payments Standard-utvidelsen | Microsoft-dokumentasjon
description: Beskriver hvordan du bruker utvidelsen til å gjøre det mulig for kunder å betale med PayPal.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: f715108b17d355084fee7983e106cd33dd476906
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1249770"
---
# <a name="the-paypal-payments-standard-extension"></a><span data-ttu-id="4ce44-103">PayPal Payments Standard-utvidelsen</span><span class="sxs-lookup"><span data-stu-id="4ce44-103">The PayPal Payments Standard Extension</span></span>
<span data-ttu-id="4ce44-104">Kundene krever kontinuerlig bedre kundeservice, både når det gjelder produktkvalitet, men også når det gjelder leverings- og betalingsalternativer.</span><span class="sxs-lookup"><span data-stu-id="4ce44-104">Customers continuously require higher customer service, both in terms of product quality but also in terms of delivery and payment options.</span></span> <span data-ttu-id="4ce44-105">PayPal Payments Standard-tjenesten hjelper deg med å forbedre din kundeservice.</span><span class="sxs-lookup"><span data-stu-id="4ce44-105">The PayPal Payments Standard service helps you increase your customer service.</span></span>

<span data-ttu-id="4ce44-106">Som et alternativ til å samle inn betalinger via bankoverføring eller kredittkort, kan du tilby kundene å betale du gjennom sin PayPal-konto.</span><span class="sxs-lookup"><span data-stu-id="4ce44-106">As an alternative to collecting payments through bank transfer or credit cards, you can offer your customers to pay you through their PayPal account.</span></span> <span data-ttu-id="4ce44-107">Når du sender en salgsfaktura eller ordre i e-post, er det en PayPal-kobling i brødteksten i e-posten og i det vedlagte PDF-dokumentet.</span><span class="sxs-lookup"><span data-stu-id="4ce44-107">When you send a sales invoice or sales order by email, there is a PayPal link in the email body and in the attached PDF document.</span></span> <span data-ttu-id="4ce44-108">Når kunden velger PayPal-koblingen, vises tjenestesiden deres for PayPal-kontoen med betalingsdetaljer for salget.</span><span class="sxs-lookup"><span data-stu-id="4ce44-108">When the customer chooses the link, the service page for their PayPal account appears showing the payment details for the sale.</span></span> <span data-ttu-id="4ce44-109">Kunden kan deretter betale fakturaen på samme måte som andre PayPal-betalinger.</span><span class="sxs-lookup"><span data-stu-id="4ce44-109">The customer can then pay the invoice as any other PayPal payment.</span></span>

<span data-ttu-id="4ce44-110">PayPal Payments Standard-tjenesten gir følgende fordeler:</span><span class="sxs-lookup"><span data-stu-id="4ce44-110">The PayPal Payments Standard service provides the following benefits:</span></span>

* <span data-ttu-id="4ce44-111">Kundebetalinger kommer raskere inn på bankkontoen din.</span><span class="sxs-lookup"><span data-stu-id="4ce44-111">Customer payments arrive faster in your bank account.</span></span>
* <span data-ttu-id="4ce44-112">Kunder har flere måter å betale fakturaer på.</span><span class="sxs-lookup"><span data-stu-id="4ce44-112">Customers have more ways to pay invoices.</span></span>
* <span data-ttu-id="4ce44-113">PayPal tilbyr en pålitelig betalingstjeneste, som kunder som foretrekker i stedet for å angi opplysninger om kredittkort på nettsteder.</span><span class="sxs-lookup"><span data-stu-id="4ce44-113">PayPal offers a trustworthy payment service, which customers prefer to entering credit card information on web sites.</span></span>
* <span data-ttu-id="4ce44-114">PayPal tilbyr flere måter for å håndtere betalinger, inkludert behandling av kredittkortbetaling, PayPal-kontoer og andre kilder.</span><span class="sxs-lookup"><span data-stu-id="4ce44-114">PayPal offers multiple ways of handling payments, including credit card processing, PayPal accounts, and other sources.</span></span>
* <span data-ttu-id="4ce44-115">PayPal-kobling kan legges til automatisk i salgsdokumenter eller manuelt av brukeren.</span><span class="sxs-lookup"><span data-stu-id="4ce44-115">The PayPal link can be added automatically to sales documents or manually by the user.</span></span>
* <span data-ttu-id="4ce44-116">PayPal Payments Standard-tjenesten omfatter ikke månedlige avgifter eller etableringsgebyrer.</span><span class="sxs-lookup"><span data-stu-id="4ce44-116">The PayPal Payments Standard service does not involve monthly fees or setup fees.</span></span>
* <span data-ttu-id="4ce44-117">Fordi det er en utvidelse kan du enkelt aktivere PayPal Payments Standard-tjenesten når og hvis bedriften din har bruk for den.</span><span class="sxs-lookup"><span data-stu-id="4ce44-117">Because it is an extension, you can easily enable the PayPal Payment Standard service when and if your business requires it.</span></span>  

<span data-ttu-id="4ce44-118">Hvis du vil ha mer informasjon, kan du se [Aktivere kundebetaling via PayPal](sales-how-enable-payment-service-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="4ce44-118">For more information, see [Enable Customer Payment Through PayPal](sales-how-enable-payment-service-extensions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="4ce44-119">Se også</span><span class="sxs-lookup"><span data-stu-id="4ce44-119">See Also</span></span>
<span data-ttu-id="4ce44-120">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="4ce44-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="4ce44-121">Sette opp salg</span><span class="sxs-lookup"><span data-stu-id="4ce44-121">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="4ce44-122">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4ce44-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
