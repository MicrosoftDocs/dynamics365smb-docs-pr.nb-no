---
title: Vise databaselåser
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 1153ffc97d0f22c889ff23c5a27a8c0446b17018
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196386"
---
# <a name="viewing-database-locks"></a><span data-ttu-id="86d97-102">Visning av databaselåser</span><span class="sxs-lookup"><span data-stu-id="86d97-102">Viewing Database Locks</span></span>

## <a name="about-locks"></a><span data-ttu-id="86d97-103">Om låser</span><span class="sxs-lookup"><span data-stu-id="86d97-103">About Locks</span></span>

<span data-ttu-id="86d97-104">Databaselåsing kontrollerer tilgang for flere brukere til de samme dataene samtidig.</span><span class="sxs-lookup"><span data-stu-id="86d97-104">Database locking controls access by multiple users to the same data at the same time.</span></span> <span data-ttu-id="86d97-105">For å beskytte en transaksjon mot andre transaksjoner som endrer de samme dataene, setter den første transaksjonen en lås på dataene.</span><span class="sxs-lookup"><span data-stu-id="86d97-105">To protect a transaction against other transactions modifying the same data, the first transaction puts a lock on the data.</span></span> <span data-ttu-id="86d97-106">Låsen blir værende til transaksjonen er ferdig.</span><span class="sxs-lookup"><span data-stu-id="86d97-106">The lock remains until the transaction's done.</span></span>

<span data-ttu-id="86d97-107">Brukere kan bli blokkert fra å fullføre transaksjoner for de låste dataene.</span><span class="sxs-lookup"><span data-stu-id="86d97-107">Users may be blocked from completing transactions on the locked data.</span></span> <span data-ttu-id="86d97-108">De får vanligvis en melding som angir låsebetingelsen.</span><span class="sxs-lookup"><span data-stu-id="86d97-108">They'll typically get a message that indicates the lock condition.</span></span>

## <a name="to-view-database-locks"></a><span data-ttu-id="86d97-109">Slik viser du databaselåser</span><span class="sxs-lookup"><span data-stu-id="86d97-109">To view database locks</span></span>

<span data-ttu-id="86d97-110">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Databaselåser**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="86d97-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Database Locks**, and then choose the related link.</span></span>

<span data-ttu-id="86d97-111">Siden **Databaselåser** inneholder et øyeblikksbilde av alle gjeldende databaselåser.</span><span class="sxs-lookup"><span data-stu-id="86d97-111">The **Database Locks** page gives snapshot of all current database locks.</span></span>

<span data-ttu-id="86d97-112">Hvis du vil ha mer informasjon om databaselåsing, kan du se [Overvåke databaselåser](/dynamics365/business-central/a/dev-itpro/administration/monitor-database-locks) i hjelpen for utviklere i Business Central og IT-eksperter.</span><span class="sxs-lookup"><span data-stu-id="86d97-112">For more information about database locking, see [Monitoring Database Locks](/dynamics365/business-central/a/dev-itpro/administration/monitor-database-locks) in the Business Central Developer and IT Pro help.</span></span>

## <a name="see-also"></a><span data-ttu-id="86d97-113">Se også</span><span class="sxs-lookup"><span data-stu-id="86d97-113">See Also</span></span>

[<span data-ttu-id="86d97-114">Overvåke databaselåser</span><span class="sxs-lookup"><span data-stu-id="86d97-114">Monitor Database Locks</span></span>](/dynamics365/business-central/a/dev-itpro/administration/monitor-database-locks) 
