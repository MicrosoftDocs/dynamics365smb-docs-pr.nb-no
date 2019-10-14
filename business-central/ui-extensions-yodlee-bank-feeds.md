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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: d79ef7c076ec3a529aeb0c679b8b61658ef65af5
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315351"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="bd47a-103">Envestnet Yodlee Bank Feeds-utvidelsen</span><span class="sxs-lookup"><span data-stu-id="bd47a-103">The Envestnet Yodlee Bank Feeds Extension</span></span>
<span data-ttu-id="bd47a-104">Hvis du raskt vil avstemme betalinger til bankkonti, lar tjenesten Envestnet Yodlee Bank Feeds deg koble systembankkontoen din til nettbankkontoen.</span><span class="sxs-lookup"><span data-stu-id="bd47a-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="bd47a-105">Dette betyr at det siste bankkontoutdraget automatisk eller manuelt mates inn i avstemmingskladden, noe som sikrer at du alltid behandler de siste betalingene med minimal risiko for feil.</span><span class="sxs-lookup"><span data-stu-id="bd47a-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

<span data-ttu-id="bd47a-106">Envestnet Yodlee Bank Feeds-tjenesten støttes bare i USA og Canada.</span><span class="sxs-lookup"><span data-stu-id="bd47a-106">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>

> [!NOTE]
> <span data-ttu-id="bd47a-107">Denne funksjonaliteten støttes bare i den elektroniske versjonen av Business Central.</span><span class="sxs-lookup"><span data-stu-id="bd47a-107">This functionality is only supported in the online version of Business Central.</span></span> <span data-ttu-id="bd47a-108">Hvis du vil bruke denne funksjonaliteten lokalt, må du hente en cobrand-konto fra Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="bd47a-108">To use this functionality on-premise, you must obtain a cobrand account from Envestnet Yodlee.</span></span><br /><br />

> [!IMPORTANT]
> <span data-ttu-id="bd47a-109">På grunn av det nye direktivet for betalingstjenester i Europa (PSD2), vil du ikke lenger kunne importere bankkontoutdrag fra banker i Stobritannia i [!INCLUDE[d365fin](includes/d365fin_md.md)] etter 14. september 2019.</span><span class="sxs-lookup"><span data-stu-id="bd47a-109">Due to the new Payment Services Directive in Europe (PSD2), after September 14, 2019, you will no longer be able to automatically import bank statements from banks in the United Kingdom into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="bd47a-110">Vi undersøker muligheten for å tilby denne funksjonen igjen senere.</span><span class="sxs-lookup"><span data-stu-id="bd47a-110">We are looking into the possibility of offering this feature again in the future.</span></span>

<span data-ttu-id="bd47a-111">Envestnet Yodlee Bank Feeds-tjenesten gir følgende fordeler:</span><span class="sxs-lookup"><span data-stu-id="bd47a-111">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="bd47a-112">Fjerner behovet for manuell registrering.</span><span class="sxs-lookup"><span data-stu-id="bd47a-112">Removes the need for manual entry.</span></span>
* <span data-ttu-id="bd47a-113">Forbedrer effektivitet og nøyaktighet når du utfører betalingsavstemming.</span><span class="sxs-lookup"><span data-stu-id="bd47a-113">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="bd47a-114">Støtter et stort antall banker.</span><span class="sxs-lookup"><span data-stu-id="bd47a-114">Supports a large number of banks.</span></span>
* <span data-ttu-id="bd47a-115">Gir oppdatert informasjon om banktransaksjoner fra [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="bd47a-115">Allows up-to-date information about bank transactions from within [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
* <span data-ttu-id="bd47a-116">Støtter manuelle og automatiske bankfeeder.</span><span class="sxs-lookup"><span data-stu-id="bd47a-116">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="bd47a-117">Tillater outsourcing av betalingsavstemming til en regnskapsfører ved å gi tilgang til bankkontoutdrag.</span><span class="sxs-lookup"><span data-stu-id="bd47a-117">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

<span data-ttu-id="bd47a-118">Hvis du vil ha mer informasjon, kan du se [Konfigurere Envestnet Yodlee Bank Feeds-tjenesten](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="bd47a-118">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="bd47a-119">Se også</span><span class="sxs-lookup"><span data-stu-id="bd47a-119">See Also</span></span>
<span data-ttu-id="bd47a-120">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="bd47a-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="bd47a-121">Utligne betalinger automatisk og avstemme bankkonti</span><span class="sxs-lookup"><span data-stu-id="bd47a-121">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="bd47a-122">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bd47a-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
