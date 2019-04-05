---
title: Betalingsavstemming med Envestnet Yodlee Bank Feeds-utvidelsen | Microsoft-dokumentasjon
description: Beskriver Envestnet Yodlee Bank Feeds-utvidelsen, som kobles til bankkonti slik at du raskt kan avstemme betalinger.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 02/26/2019
ms.author: sgroespe
ms.openlocfilehash: 36400b3265517c29f68f7eb59d17d968334e0fb1
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803752"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="406cc-103">Envestnet Yodlee Bank Feeds-utvidelsen</span><span class="sxs-lookup"><span data-stu-id="406cc-103">The Envestnet Yodlee Bank Feeds Extension</span></span>
<span data-ttu-id="406cc-104">Hvis du vil avstemme raskt betalinger til bankkonti, lar tjenesten Envestnet Yodlee Bank Feeds deg koble systembankkontoen din til nettbankkontoen.</span><span class="sxs-lookup"><span data-stu-id="406cc-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="406cc-105">Dette betyr at det siste bankkontoutdraget automatisk eller manuelt mates inn i avstemmingskladden, noe som sikrer at du alltid behandler de siste betalingene med minimal risiko for feil.</span><span class="sxs-lookup"><span data-stu-id="406cc-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

> [!NOTE]
> <span data-ttu-id="406cc-106">Denne funksjonaliteten støttes bare i den elektroniske versjonen av Business Central.</span><span class="sxs-lookup"><span data-stu-id="406cc-106">This functionality is only supported in the online version of Business Central.</span></span> <span data-ttu-id="406cc-107">Hvis du vil bruke denne funksjonaliteten lokalt, må du hente en cobrand-konto fra Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="406cc-107">To use this functionality on-premise, you must obtain a cobrand account from Envestnet Yodlee.</span></span>

<span data-ttu-id="406cc-108">Envestnet Yodlee Bank Feeds-tjenesten gir følgende fordeler:</span><span class="sxs-lookup"><span data-stu-id="406cc-108">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="406cc-109">Fjerner behovet for manuell registrering.</span><span class="sxs-lookup"><span data-stu-id="406cc-109">Removes the need for manual entry.</span></span>
* <span data-ttu-id="406cc-110">Forbedrer effektivitet og nøyaktighet når du utfører betalingsavstemming.</span><span class="sxs-lookup"><span data-stu-id="406cc-110">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="406cc-111">Støtter et stort antall banker.</span><span class="sxs-lookup"><span data-stu-id="406cc-111">Supports a large number of banks.</span></span>
* <span data-ttu-id="406cc-112">Gir oppdatert informasjon om banktransaksjoner fra [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="406cc-112">Allows up-to-date information about bank transactions from within [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
* <span data-ttu-id="406cc-113">Støtter manuelle og automatiske bankfeeder.</span><span class="sxs-lookup"><span data-stu-id="406cc-113">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="406cc-114">Tillater outsourcing av betalingsavstemming til en regnskapsfører ved å gi tilgang til bankkontoutdrag.</span><span class="sxs-lookup"><span data-stu-id="406cc-114">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

<span data-ttu-id="406cc-115">Hvis du vil ha mer informasjon, kan du se [Konfigurere bankfeedservicen Envestnet Yodlee](bank-how-setup-bank-statement-service.md)</span><span class="sxs-lookup"><span data-stu-id="406cc-115">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="406cc-116">Se også</span><span class="sxs-lookup"><span data-stu-id="406cc-116">See Also</span></span>
<span data-ttu-id="406cc-117">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="406cc-117">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="406cc-118">Utligne betalinger automatisk og avstemme bankkonti</span><span class="sxs-lookup"><span data-stu-id="406cc-118">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="406cc-119">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="406cc-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
