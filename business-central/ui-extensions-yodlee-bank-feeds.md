---
title: Betalingsavstemming med Envestnet Yodlee Bank Feeds-utvidelsen
description: Beskriver Envestnet Yodlee Bank Feeds-utvidelsen, som kobles til bankkonti, slik at du raskt kan avstemme betalinger.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 946958669f4554869e171286927bf498fe62a7ed
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5394027"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="dec95-103">Envestnet Yodlee Bank Feeds-utvidelsen</span><span class="sxs-lookup"><span data-stu-id="dec95-103">The Envestnet Yodlee Bank Feeds Extension</span></span>

<span data-ttu-id="dec95-104">Hvis du raskt vil avstemme betalinger til bankkonti, lar tjenesten Envestnet Yodlee Bank Feeds deg koble systembankkontoen din til nettbankkontoen.</span><span class="sxs-lookup"><span data-stu-id="dec95-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="dec95-105">Dette betyr at det siste bankkontoutdraget automatisk eller manuelt mates inn i avstemmingskladden, noe som sikrer at du alltid behandler de siste betalingene med minimal risiko for feil.</span><span class="sxs-lookup"><span data-stu-id="dec95-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

<span data-ttu-id="dec95-106">Envestnet Yodlee Bank Feeds-tjenesten støttes bare i USA og Canada.</span><span class="sxs-lookup"><span data-stu-id="dec95-106">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>

> [!NOTE]
> <span data-ttu-id="dec95-107">Envestnet Yodlee Bank Feeds-tjenesten støttes bare i den elektroniske versjonen av Business Central.</span><span class="sxs-lookup"><span data-stu-id="dec95-107">The Envestnet Yodlee Bank Feeds service is only supported in the online version of Business Central.</span></span> <span data-ttu-id="dec95-108">Hvis du vil bruke denne funksjonaliteten lokalt, må du hente en cobrand-konto fra Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="dec95-108">To use this functionality on-premises, you must obtain a cobrand account from Envestnet Yodlee.</span></span><br /><br />
> <span data-ttu-id="dec95-109">Envestnet Yodlee Bank Feeds-tjenesten støttes bare i USA og Canada.</span><span class="sxs-lookup"><span data-stu-id="dec95-109">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>
> <span data-ttu-id="dec95-110">Det er bare banker som befinner seg i disse landene, som støttes, selv om banker fra andre land kan vises i vinduet for valg av bank Envestnet Yodlee Bank Feeds i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="dec95-110">Only banks residing in these countries are supported, even though banks from other countries may appear in the Envestnet Yodlee Bank Feeds bank selection window in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dec95-111">På grunn av det nye direktivet for betalingstjenester i Europa (PSD2), vil du ikke lenger kunne importere bankkontoutdrag fra banker i Stobritannia i [!INCLUDE[prod_short](includes/prod_short.md)] etter 14. september 2019.</span><span class="sxs-lookup"><span data-stu-id="dec95-111">Due to the new Payment Services Directive in Europe (PSD2), after September 14, 2019, you will no longer be able to automatically import bank statements from banks in the United Kingdom into [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="dec95-112">Vi undersøker muligheten for å tilby denne funksjonen igjen senere.</span><span class="sxs-lookup"><span data-stu-id="dec95-112">We are looking into the possibility of offering this feature again in the future.</span></span>

<span data-ttu-id="dec95-113">Envestnet Yodlee Bank Feeds-tjenesten gir følgende fordeler:</span><span class="sxs-lookup"><span data-stu-id="dec95-113">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="dec95-114">Fjerner behovet for manuell registrering.</span><span class="sxs-lookup"><span data-stu-id="dec95-114">Removes the need for manual entry.</span></span>
* <span data-ttu-id="dec95-115">Forbedrer effektivitet og nøyaktighet når du utfører betalingsavstemming.</span><span class="sxs-lookup"><span data-stu-id="dec95-115">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="dec95-116">Støtter et stort antall banker.</span><span class="sxs-lookup"><span data-stu-id="dec95-116">Supports a large number of banks.</span></span>
* <span data-ttu-id="dec95-117">Gir oppdatert informasjon om banktransaksjoner fra [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="dec95-117">Allows up-to-date information about bank transactions from within [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>
* <span data-ttu-id="dec95-118">Støtter manuelle og automatiske bankfeeder.</span><span class="sxs-lookup"><span data-stu-id="dec95-118">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="dec95-119">Tillater outsourcing av betalingsavstemming til en regnskapsfører ved å gi tilgang til bankkontoutdrag.</span><span class="sxs-lookup"><span data-stu-id="dec95-119">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

## <a name="available-bank-feeds"></a><span data-ttu-id="dec95-120">Tilgjengelige bankfeeder</span><span class="sxs-lookup"><span data-stu-id="dec95-120">Available Bank Feeds</span></span>
<span data-ttu-id="dec95-121">Du kan kontrollere om en bank er støttet, ved å definere og koble til Envestnet Yodlee Bank Feeds-tjenesten.</span><span class="sxs-lookup"><span data-stu-id="dec95-121">You can check whether a bank is supported by setting up and connecting to the Envestnet Yodlee Bank Feeds service.</span></span> <span data-ttu-id="dec95-122">Banken vil vises i oversikten hvis den støttes av Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="dec95-122">The bank will appear on the list if it is supported by Envestnet Yodlee.</span></span>

<span data-ttu-id="dec95-123">Hvis du vil ha mer informasjon, kan du se [Konfigurere Envestnet Yodlee Bank Feeds-tjenesten](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="dec95-123">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="dec95-124">Se også</span><span class="sxs-lookup"><span data-stu-id="dec95-124">See Also</span></span>
<span data-ttu-id="dec95-125">[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av utvidelser](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="dec95-125">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="dec95-126">Utligne betalinger automatisk og avstemme bankkonti</span><span class="sxs-lookup"><span data-stu-id="dec95-126">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="dec95-127">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dec95-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]