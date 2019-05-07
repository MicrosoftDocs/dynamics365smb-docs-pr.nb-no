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
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: fc14d11bf75ea39553c1ed04986273903874a0e1
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "915433"
---
# <a name="auditing-changes-in-business-central"></a><span data-ttu-id="af149-103">Revidere endringer i Business Central</span><span class="sxs-lookup"><span data-stu-id="af149-103">Auditing Changes in Business Central</span></span>

<span data-ttu-id="af149-104">Du kan aktivere endringsloggen i [!INCLUDE[d365fin](includes/d365fin_md.md)], slik at du har en historikk for aktivitetene.</span><span class="sxs-lookup"><span data-stu-id="af149-104">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="af149-105">Loggen er basert på endringene som utføres på dataene i tabellene som du vil spore. På siden **Endringsloggposter** er oppføringene ordnet kronologisk og viser endringer som gjøres i feltene i de angitte tabellene.</span><span class="sxs-lookup"><span data-stu-id="af149-105">The log is based on changes that are made to data in the tables that you track. On the **Change Log Entries** page, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="af149-106">Endringsloggen samler inn alle endringer som utføres i tabellen.</span><span class="sxs-lookup"><span data-stu-id="af149-106">The change log collects all changes that are made to the table.</span></span>

> [!Important]
> <span data-ttu-id="af149-107">En brukers endringer vises ikke i **Endringsloggposter** før brukerøkten startes på nytt, som skjer i følgende tilfeller:</span><span class="sxs-lookup"><span data-stu-id="af149-107">A user's changes are not visible in the **Change Log Entries** until the user's session is restarted, which happens in the following cases:</span></span>
<br />
> * <span data-ttu-id="af149-108">Økten har utløpt og ble oppdatert.</span><span class="sxs-lookup"><span data-stu-id="af149-108">The session expired and was refreshed.</span></span>
> * <span data-ttu-id="af149-109">Brukeren har valgt et annet selskap eller rollesenter.</span><span class="sxs-lookup"><span data-stu-id="af149-109">The user selected another company or Role Center.</span></span>
> * <span data-ttu-id="af149-110">Brukeren logget ut og inn igjen.</span><span class="sxs-lookup"><span data-stu-id="af149-110">The user signed out and back in.</span></span>

## <a name="working-with-the-change-log"></a><span data-ttu-id="af149-111">Arbeide med endringsloggen</span><span class="sxs-lookup"><span data-stu-id="af149-111">Working with the Change Log</span></span>

<span data-ttu-id="af149-112">Et vanlig problem i mange finanssystemer er å lokalisere opphavet til feil og endringer i dataene.</span><span class="sxs-lookup"><span data-stu-id="af149-112">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="af149-113">Det kan være alt fra et uriktig kundetelefonnummer til uriktig bokføring i finanspostene.</span><span class="sxs-lookup"><span data-stu-id="af149-113">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="af149-114">Ved hjelp av endringsloggen kan du spore alle direkte endringer som brukeren gjør i dataene i databasen.</span><span class="sxs-lookup"><span data-stu-id="af149-114">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="af149-115">For må angi hver tabell og hvert felt du vil at systemet skal logge. Deretter må du aktivere endringsloggen.</span><span class="sxs-lookup"><span data-stu-id="af149-115">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="af149-116">Du kan aktivere eller deaktivere endringsloggen på siden **Endringsloggoppsett**.</span><span class="sxs-lookup"><span data-stu-id="af149-116">You activate and deactivate the change log on the **Change Log Setup** page.</span></span> <span data-ttu-id="af149-117">Når en bruker aktiverer eller deaktiverer endringsloggen, logges denne aktiviteten, slik at du alltid kan se hvilken bruker som deaktiverte eller aktiverte endringsloggen.</span><span class="sxs-lookup"><span data-stu-id="af149-117">When a user activates or deactivates the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span>

<span data-ttu-id="af149-118">På siden **Endringsloggoppsett**, hvis du velger **Tabeller**-handlingen, kan du angi hvilke tabeller du vil spore endringer for, og hvilke endringer du vil spore. [!INCLUDE[d365fin](includes/d365fin_md.md)] sporer også flere systemtabeller.</span><span class="sxs-lookup"><span data-stu-id="af149-118">On the **Change Log Setup** page, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="af149-119">Når du har opprettet endringsloggen, aktivert den og endret data, kan du vise og filtrere endringene på siden **Endringsloggposter**.</span><span class="sxs-lookup"><span data-stu-id="af149-119">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes on the **Change Log Entries** page.</span></span> <span data-ttu-id="af149-120">Hvis du vil slette postene, kan du gjøre det på siden **Slett endringsloggposter**, der du kan definere filtre basert på datoene og tidspunktene.</span><span class="sxs-lookup"><span data-stu-id="af149-120">If you want to delete entries, you can do that on the **Delete Change Log Entries** page, where you can set filters based on dates and time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="af149-121">Se også</span><span class="sxs-lookup"><span data-stu-id="af149-121">See Also</span></span>
[<span data-ttu-id="af149-122">Endre grunnleggende innstillinger</span><span class="sxs-lookup"><span data-stu-id="af149-122">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="af149-123">Sortering</span><span class="sxs-lookup"><span data-stu-id="af149-123">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="af149-124">Bruke Fortell meg til å finne funksjoner og informasjon</span><span class="sxs-lookup"><span data-stu-id="af149-124">Using Tell Me to Find Features and Information</span></span>](ui-search.md)  
<span data-ttu-id="af149-125">[Administrere brukere og tillatelser](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="af149-125">[Managing Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="af149-126">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="af149-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
