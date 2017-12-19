---
title: Spore brukeraktivitet i en endringsloggen | Microsoft-dokumentasjon
Description: You can activate a user log so that you have a history of any changes made to data in tracked tables.
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: cfe0eed4090ef458e774da8d0bc03910247570d7
ms.openlocfilehash: 9f3db97203e09608ea0776f5571d6179778283b6
ms.contentlocale: nb-no
ms.lasthandoff: 12/14/2017

---
# <a name="logging-changes-in-dynamics-365-business-edition"></a><span data-ttu-id="56ed9-102">Logge endringer i Dynamics 365, Business edition</span><span class="sxs-lookup"><span data-stu-id="56ed9-102">Logging Changes in Dynamics 365, Business edition</span></span> 
<span data-ttu-id="56ed9-103">Du kan aktivere endringsloggen i [!INCLUDE[d365fin](includes/d365fin_md.md)], slik at du har en historikk for aktivitetene.</span><span class="sxs-lookup"><span data-stu-id="56ed9-103">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="56ed9-104">Loggen er basert på endringene som utføres på dataene i tabellene som du vil spore. I endringsloggen er oppføringene ordnet kronologisk og viser endringer som gjøres i feltene i de angitte tabellene.</span><span class="sxs-lookup"><span data-stu-id="56ed9-104">The log is based on changes that are made to data in the tables that you track. In the change log, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="56ed9-105">Endringsloggen samler inn alle endringer som utføres i tabellen.</span><span class="sxs-lookup"><span data-stu-id="56ed9-105">The change log collects all changes that are made to the table.</span></span>  

## <a name="working-with-the-change-log"></a><span data-ttu-id="56ed9-106">Arbeide med endringsloggen</span><span class="sxs-lookup"><span data-stu-id="56ed9-106">Working with the Change Log</span></span>
<span data-ttu-id="56ed9-107">Et vanlig problem i mange finanssystemer er å lokalisere opphavet til feil og endringer i dataene.</span><span class="sxs-lookup"><span data-stu-id="56ed9-107">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="56ed9-108">Det kan være alt fra et uriktig kundetelefonnummer til uriktig bokføring i finanspostene.</span><span class="sxs-lookup"><span data-stu-id="56ed9-108">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="56ed9-109">Ved hjelp av endringsloggen kan du spore alle direkte endringer som brukeren gjør i dataene i databasen.</span><span class="sxs-lookup"><span data-stu-id="56ed9-109">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="56ed9-110">For må angi hver tabell og hvert felt du vil at systemet skal logge. Deretter må du aktivere endringsloggen.</span><span class="sxs-lookup"><span data-stu-id="56ed9-110">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="56ed9-111">Du kan aktivere eller deaktivere endringsloggen i vinduet **Endringsloggoppsett**.</span><span class="sxs-lookup"><span data-stu-id="56ed9-111">You activate and deactivate the change log in the **Change Log Setup** window.</span></span> <span data-ttu-id="56ed9-112">Når du aktiverer eller deaktiverer endringsloggen, logges denne aktiviteten, slik at du alltid kan se hvilken bruker som deaktiverte eller aktiverte endringsloggen.</span><span class="sxs-lookup"><span data-stu-id="56ed9-112">When you activate or deactivate the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span> <span data-ttu-id="56ed9-113">Denne funksjonen kan ikke slås av.</span><span class="sxs-lookup"><span data-stu-id="56ed9-113">This cannot be turned off.</span></span>  

<span data-ttu-id="56ed9-114">I vinduet **Endringsloggoppsett**, hvis du velger **Tabeller**-handlingen, kan du angi hvilke tabeller du vil spore endringer for, og hvilke endringer du vil spore. [!INCLUDE[d365fin](includes/d365fin_md.md)] sporer også flere systemtabeller.</span><span class="sxs-lookup"><span data-stu-id="56ed9-114">In the **Change Log Setup** window, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="56ed9-115">Når du har opprettet endringsloggen, aktivert den og endret data, kan du vise og filtrere endringene i vinduet **Endringsloggposter**.</span><span class="sxs-lookup"><span data-stu-id="56ed9-115">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes in the **Change Log Entries** window.</span></span> <span data-ttu-id="56ed9-116">Hvis du vil slette postene, kan du gjøre det i vinduet **Slett endringsloggposter**, der du kan definere filtre basert på datoene og tidspunktene.</span><span class="sxs-lookup"><span data-stu-id="56ed9-116">If you want to delete entries, you can do that in the **Delete Change Log Entries** window, where you can set filters based on dates and time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="56ed9-117">Se også</span><span class="sxs-lookup"><span data-stu-id="56ed9-117">See Also</span></span>
[<span data-ttu-id="56ed9-118">Endre grunnleggende innstillinger</span><span class="sxs-lookup"><span data-stu-id="56ed9-118">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="56ed9-119">Sortering</span><span class="sxs-lookup"><span data-stu-id="56ed9-119">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="56ed9-120">Bruke Søk etter side eller rapport</span><span class="sxs-lookup"><span data-stu-id="56ed9-120">Using Search for Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="56ed9-121">[Administrere brukere og tillatelser](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="56ed9-121">[How to: Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="56ed9-122">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="56ed9-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

