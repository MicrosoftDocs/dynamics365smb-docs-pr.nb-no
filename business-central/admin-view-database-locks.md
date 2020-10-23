---
title: Vise databaselåser
description: Lær hvordan du kan vise informasjon om en databaselås rett fra klientgrensesnittet i Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 6880ffa9a2ab42c1af7c22f9cace64697c9f905b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922320"
---
# <a name="viewing-database-locks"></a><span data-ttu-id="e2cf1-103">Visning av databaselåser</span><span class="sxs-lookup"><span data-stu-id="e2cf1-103">Viewing Database Locks</span></span>

<span data-ttu-id="e2cf1-104">Databaselåsing kontrollerer tilgang for flere brukere til de samme dataene samtidig.</span><span class="sxs-lookup"><span data-stu-id="e2cf1-104">Database locking controls access by multiple users to the same data at the same time.</span></span> <span data-ttu-id="e2cf1-105">For å beskytte en transaksjon mot andre transaksjoner som endrer de samme dataene, setter den første transaksjonen en lås på dataene.</span><span class="sxs-lookup"><span data-stu-id="e2cf1-105">To protect a transaction against other transactions modifying the same data, the first transaction puts a lock on the data.</span></span> <span data-ttu-id="e2cf1-106">Låsen blir værende til transaksjonen er ferdig.</span><span class="sxs-lookup"><span data-stu-id="e2cf1-106">The lock remains until the transaction's done.</span></span>

<span data-ttu-id="e2cf1-107">Brukere kan bli blokkert fra å fullføre transaksjoner for de låste dataene.</span><span class="sxs-lookup"><span data-stu-id="e2cf1-107">Users may be blocked from completing transactions on the locked data.</span></span> <span data-ttu-id="e2cf1-108">De får vanligvis en melding som angir låsebetingelsen.</span><span class="sxs-lookup"><span data-stu-id="e2cf1-108">They'll typically get a message that indicates the lock condition.</span></span>

## <a name="to-view-database-locks"></a><span data-ttu-id="e2cf1-109">Slik viser du databaselåser</span><span class="sxs-lookup"><span data-stu-id="e2cf1-109">To view database locks</span></span>

<span data-ttu-id="e2cf1-110">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Databaselåser**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e2cf1-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Database Locks**, and then choose the related link.</span></span>

<span data-ttu-id="e2cf1-111">Siden **Databaselåser** inneholder et øyeblikksbilde av alle gjeldende databaselåser.</span><span class="sxs-lookup"><span data-stu-id="e2cf1-111">The **Database Locks** page gives snapshot of all current database locks.</span></span>

<span data-ttu-id="e2cf1-112">Hvis du vil ha mer informasjon om databaselåsing, kan du se [Overvåke databaselåser](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) i hjelpen for utviklere i Business Central og IT-eksperter.</span><span class="sxs-lookup"><span data-stu-id="e2cf1-112">For more information about database locking, see [Monitoring Database Locks](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) in the Business Central Developer and IT Pro help.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2cf1-113">Se også</span><span class="sxs-lookup"><span data-stu-id="e2cf1-113">See Also</span></span>

[<span data-ttu-id="e2cf1-114">Overvåke databaselåser</span><span class="sxs-lookup"><span data-stu-id="e2cf1-114">Monitor Database Locks</span></span>](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 
