---
title: Betalingsavstemming med Envestnet Yodlee Bank Feeds-utvidelsen | Microsoft Docs
description: Beskriver Envestnet Yodlee Bank Feeds-utvidelsen, som kobles til bankkonti, slik at du raskt kan avstemme betalinger.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3107c42fd584a58fc13ad2bfeacea0ed14e28de7
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3918591"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="958ea-103">Envestnet Yodlee Bank Feeds-utvidelsen</span><span class="sxs-lookup"><span data-stu-id="958ea-103">The Envestnet Yodlee Bank Feeds Extension</span></span>
<span data-ttu-id="958ea-104">Hvis du raskt vil avstemme betalinger til bankkonti, lar tjenesten Envestnet Yodlee Bank Feeds deg koble systembankkontoen din til nettbankkontoen.</span><span class="sxs-lookup"><span data-stu-id="958ea-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="958ea-105">Dette betyr at det siste bankkontoutdraget automatisk eller manuelt mates inn i avstemmingskladden, noe som sikrer at du alltid behandler de siste betalingene med minimal risiko for feil.</span><span class="sxs-lookup"><span data-stu-id="958ea-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

<span data-ttu-id="958ea-106">Envestnet Yodlee Bank Feeds-tjenesten støttes bare i USA og Canada.</span><span class="sxs-lookup"><span data-stu-id="958ea-106">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>

> [!NOTE]
> <span data-ttu-id="958ea-107">Envestnet Yodlee Bank Feeds-tjenesten støttes bare i den elektroniske versjonen av Business Central.</span><span class="sxs-lookup"><span data-stu-id="958ea-107">The Envestnet Yodlee Bank Feeds service is only supported in the online version of Business Central.</span></span> <span data-ttu-id="958ea-108">Hvis du vil bruke denne funksjonaliteten lokalt, må du hente en cobrand-konto fra Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="958ea-108">To use this functionality on-premises, you must obtain a cobrand account from Envestnet Yodlee.</span></span><br /><br />
> <span data-ttu-id="958ea-109">Envestnet Yodlee Bank Feeds-tjenesten støttes bare i USA og Canada.</span><span class="sxs-lookup"><span data-stu-id="958ea-109">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>
> <span data-ttu-id="958ea-110">Det er bare banker som befinner seg i disse landene, som støttes, selv om banker fra andre land kan vises i vinduet for valg av bank Envestnet Yodlee Bank Feeds i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="958ea-110">Only banks residing in these countries are supported, even though banks from other countries may appear in the Envestnet Yodlee Bank Feeds bank selection window in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

> [!IMPORTANT]
> <span data-ttu-id="958ea-111">På grunn av det nye direktivet for betalingstjenester i Europa (PSD2), vil du ikke lenger kunne importere bankkontoutdrag fra banker i Stobritannia i [!INCLUDE[d365fin](includes/d365fin_md.md)] etter 14. september 2019.</span><span class="sxs-lookup"><span data-stu-id="958ea-111">Due to the new Payment Services Directive in Europe (PSD2), after September 14, 2019, you will no longer be able to automatically import bank statements from banks in the United Kingdom into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="958ea-112">Vi undersøker muligheten for å tilby denne funksjonen igjen senere.</span><span class="sxs-lookup"><span data-stu-id="958ea-112">We are looking into the possibility of offering this feature again in the future.</span></span>

<span data-ttu-id="958ea-113">Envestnet Yodlee Bank Feeds-tjenesten gir følgende fordeler:</span><span class="sxs-lookup"><span data-stu-id="958ea-113">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="958ea-114">Fjerner behovet for manuell registrering.</span><span class="sxs-lookup"><span data-stu-id="958ea-114">Removes the need for manual entry.</span></span>
* <span data-ttu-id="958ea-115">Forbedrer effektivitet og nøyaktighet når du utfører betalingsavstemming.</span><span class="sxs-lookup"><span data-stu-id="958ea-115">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="958ea-116">Støtter et stort antall banker.</span><span class="sxs-lookup"><span data-stu-id="958ea-116">Supports a large number of banks.</span></span>
* <span data-ttu-id="958ea-117">Gir oppdatert informasjon om banktransaksjoner fra [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="958ea-117">Allows up-to-date information about bank transactions from within [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
* <span data-ttu-id="958ea-118">Støtter manuelle og automatiske bankfeeder.</span><span class="sxs-lookup"><span data-stu-id="958ea-118">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="958ea-119">Tillater outsourcing av betalingsavstemming til en regnskapsfører ved å gi tilgang til bankkontoutdrag.</span><span class="sxs-lookup"><span data-stu-id="958ea-119">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

## <a name="available-bank-feeds"></a><span data-ttu-id="958ea-120">Tilgjengelige bankfeeder</span><span class="sxs-lookup"><span data-stu-id="958ea-120">Available Bank Feeds</span></span>
<span data-ttu-id="958ea-121">Du kan kontrollere om en bank er støttet, ved å definere og koble til Envestnet Yodlee Bank Feeds-tjenesten.</span><span class="sxs-lookup"><span data-stu-id="958ea-121">You can check whether a bank is supported by setting up and connecting to the Envestnet Yodlee Bank Feeds service.</span></span> <span data-ttu-id="958ea-122">Banken vil vises i oversikten hvis den støttes av Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="958ea-122">The bank will appear on the list if it is supported by Envestnet Yodlee.</span></span>

<span data-ttu-id="958ea-123">Hvis du vil ha mer informasjon, kan du se [Konfigurere Envestnet Yodlee Bank Feeds-tjenesten](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="958ea-123">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="958ea-124">Se også</span><span class="sxs-lookup"><span data-stu-id="958ea-124">See Also</span></span>
<span data-ttu-id="958ea-125">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="958ea-125">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="958ea-126">Utligne betalinger automatisk og avstemme bankkonti</span><span class="sxs-lookup"><span data-stu-id="958ea-126">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="958ea-127">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="958ea-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
