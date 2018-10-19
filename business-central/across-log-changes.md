---
title: Spore brukeraktivitet i en endringsloggen | Microsoft-dokumentasjon
description: Du kan aktivere en brukerlogg slik at du har en logg over eventuelle endringer i data i sporede tabeller.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: ab9696a3cc14970def764b2741d50dbcd5207460
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="logging-changes-in-business-central"></a><span data-ttu-id="382b0-103">Logge endringer i Business Central</span><span class="sxs-lookup"><span data-stu-id="382b0-103">Logging Changes in Business Central</span></span>
<span data-ttu-id="382b0-104">Du kan aktivere endringsloggen i [!INCLUDE[d365fin](includes/d365fin_md.md)], slik at du har en historikk for aktivitetene.</span><span class="sxs-lookup"><span data-stu-id="382b0-104">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="382b0-105">Loggen er basert på endringene som utføres på dataene i tabellene som du vil spore. I endringsloggen er oppføringene ordnet kronologisk og viser endringer som gjøres i feltene i de angitte tabellene.</span><span class="sxs-lookup"><span data-stu-id="382b0-105">The log is based on changes that are made to data in the tables that you track. In the change log, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="382b0-106">Endringsloggen samler inn alle endringer som utføres i tabellen.</span><span class="sxs-lookup"><span data-stu-id="382b0-106">The change log collects all changes that are made to the table.</span></span>  

## <a name="working-with-the-change-log"></a><span data-ttu-id="382b0-107">Arbeide med endringsloggen</span><span class="sxs-lookup"><span data-stu-id="382b0-107">Working with the Change Log</span></span>
<span data-ttu-id="382b0-108">Et vanlig problem i mange finanssystemer er å lokalisere opphavet til feil og endringer i dataene.</span><span class="sxs-lookup"><span data-stu-id="382b0-108">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="382b0-109">Det kan være alt fra et uriktig kundetelefonnummer til uriktig bokføring i finanspostene.</span><span class="sxs-lookup"><span data-stu-id="382b0-109">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="382b0-110">Ved hjelp av endringsloggen kan du spore alle direkte endringer som brukeren gjør i dataene i databasen.</span><span class="sxs-lookup"><span data-stu-id="382b0-110">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="382b0-111">For må angi hver tabell og hvert felt du vil at systemet skal logge. Deretter må du aktivere endringsloggen.</span><span class="sxs-lookup"><span data-stu-id="382b0-111">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="382b0-112">Du kan aktivere eller deaktivere endringsloggen i vinduet **Endringsloggoppsett**.</span><span class="sxs-lookup"><span data-stu-id="382b0-112">You activate and deactivate the change log in the **Change Log Setup** window.</span></span> <span data-ttu-id="382b0-113">Når du aktiverer eller deaktiverer endringsloggen, logges denne aktiviteten, slik at du alltid kan se hvilken bruker som deaktiverte eller aktiverte endringsloggen.</span><span class="sxs-lookup"><span data-stu-id="382b0-113">When you activate or deactivate the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span> <span data-ttu-id="382b0-114">Denne funksjonen kan ikke slås av.</span><span class="sxs-lookup"><span data-stu-id="382b0-114">This cannot be turned off.</span></span>  

<span data-ttu-id="382b0-115">I vinduet **Endringsloggoppsett**, hvis du velger **Tabeller**-handlingen, kan du angi hvilke tabeller du vil spore endringer for, og hvilke endringer du vil spore. [!INCLUDE[d365fin](includes/d365fin_md.md)] sporer også flere systemtabeller.</span><span class="sxs-lookup"><span data-stu-id="382b0-115">In the **Change Log Setup** window, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="382b0-116">Når du har opprettet endringsloggen, aktivert den og endret data, kan du vise og filtrere endringene i vinduet **Endringsloggposter**.</span><span class="sxs-lookup"><span data-stu-id="382b0-116">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes in the **Change Log Entries** window.</span></span> <span data-ttu-id="382b0-117">Hvis du vil slette postene, kan du gjøre det i vinduet **Slett endringsloggposter**, der du kan definere filtre basert på datoene og tidspunktene.</span><span class="sxs-lookup"><span data-stu-id="382b0-117">If you want to delete entries, you can do that in the **Delete Change Log Entries** window, where you can set filters based on dates and time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="382b0-118">Se også</span><span class="sxs-lookup"><span data-stu-id="382b0-118">See Also</span></span>
[<span data-ttu-id="382b0-119">Endre grunnleggende innstillinger</span><span class="sxs-lookup"><span data-stu-id="382b0-119">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="382b0-120">Sortering</span><span class="sxs-lookup"><span data-stu-id="382b0-120">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="382b0-121">Bruke Søk etter side eller rapport</span><span class="sxs-lookup"><span data-stu-id="382b0-121">Using Search for Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="382b0-122">[Administrere brukere og tillatelser](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="382b0-122">[Managing Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="382b0-123">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="382b0-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

