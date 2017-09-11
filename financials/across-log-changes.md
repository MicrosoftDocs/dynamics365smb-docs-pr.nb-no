---
title: Spore brukeraktivitet i en endringsloggen | Microsoft-dokumentasjon
Description: Du kan aktivere en brukerlogg slik at du har en logg over eventuelle endringer i data i sporede tabeller.
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
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c27c63ae26f2f97dd15d31978b967f6a08dd55b7
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2017


---
# <a name="logging-changes-in-dynamics-365-for-financials"></a><span data-ttu-id="ffb61-103">Logging av endringer i Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="ffb61-103">Logging Changes in Dynamics 365 for Financials</span></span>
<span data-ttu-id="ffb61-104">Du kan aktivere endringsloggen i [!INCLUDE[d365fin](includes/d365fin_md.md)], slik at du har en historikk for aktivitetene.</span><span class="sxs-lookup"><span data-stu-id="ffb61-104">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="ffb61-105">Endringsloggen er basert på endringer som gjøres med dataene i tabellene som du vil spore.</span><span class="sxs-lookup"><span data-stu-id="ffb61-105">The log is based on changes that are made to data in the tables that you track.</span></span> <span data-ttu-id="ffb61-106">I endringsloggen er postene sortert kronologisk, og de viser endringer som er gjort i feltene i de angitte tabellene.</span><span class="sxs-lookup"><span data-stu-id="ffb61-106">In the change log, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="ffb61-107">Endringsloggen samler inn alle endringer som utføres i tabellen.</span><span class="sxs-lookup"><span data-stu-id="ffb61-107">The change log collects all changes that are made to the table.</span></span>  

## <a name="working-with-the-change-log"></a><span data-ttu-id="ffb61-108">Arbeide med endringsloggen</span><span class="sxs-lookup"><span data-stu-id="ffb61-108">Working with the change log</span></span>
<span data-ttu-id="ffb61-109">Et vanlig problem i mange finanssystemer er å lokalisere opphavet til feil og endringer i dataene.</span><span class="sxs-lookup"><span data-stu-id="ffb61-109">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="ffb61-110">Det kan være alt fra et uriktig kundetelefonnummer til uriktig bokføring i finanspostene.</span><span class="sxs-lookup"><span data-stu-id="ffb61-110">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="ffb61-111">Ved hjelp av endringsloggen kan du spore alle direkte endringer som brukeren gjør i dataene i databasen.</span><span class="sxs-lookup"><span data-stu-id="ffb61-111">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="ffb61-112">For må angi hver tabell og hvert felt du vil at systemet skal logge. Deretter må du aktivere endringsloggen.</span><span class="sxs-lookup"><span data-stu-id="ffb61-112">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="ffb61-113">Du kan aktivere eller deaktivere endringsloggen i vinduet **Endringsloggoppsett**.</span><span class="sxs-lookup"><span data-stu-id="ffb61-113">You activate and deactivate the change log in the **Change Log Setup** window.</span></span> <span data-ttu-id="ffb61-114">Når du aktiverer eller deaktiverer endringsloggen, logges denne aktiviteten, slik at du alltid kan se hvilken bruker som deaktiverte eller aktiverte endringsloggen.</span><span class="sxs-lookup"><span data-stu-id="ffb61-114">When you activate or deactivate the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span> <span data-ttu-id="ffb61-115">Denne funksjonen kan ikke slås av.</span><span class="sxs-lookup"><span data-stu-id="ffb61-115">This cannot be turned off.</span></span>  

<span data-ttu-id="ffb61-116">I vinduet **Endringsloggoppsett**, hvis du velger **Tabeller**-handlingen, kan du angi hvilke tabeller du vil spore endringer for, og hvilke endringer du vil spore.</span><span class="sxs-lookup"><span data-stu-id="ffb61-116">In the **Change Log Setup** window, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="ffb61-117"> sporer også en rekke systemtabeller.</span><span class="sxs-lookup"><span data-stu-id="ffb61-117"> also tracks a number of system tables.</span></span>

<span data-ttu-id="ffb61-118">Når du har opprettet endringsloggen, aktivert den og endret data, kan du vise og filtrere endringene i vinduet **Endringsloggposter**.</span><span class="sxs-lookup"><span data-stu-id="ffb61-118">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes in the **Change Log Entries** window.</span></span> <span data-ttu-id="ffb61-119">Hvis du vil slette postene, kan du gjøre det i vinduet **Slett endringsloggposter**, der du kan definere filtre basert på datoene og tidspunktene.</span><span class="sxs-lookup"><span data-stu-id="ffb61-119">If you want to delete entries, you can do that in the **Delete Change Log Entries** window, where you can set filters based on dates and time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ffb61-120">Se også</span><span class="sxs-lookup"><span data-stu-id="ffb61-120">See Also</span></span>
[<span data-ttu-id="ffb61-121">Endre grunnleggende innstillinger</span><span class="sxs-lookup"><span data-stu-id="ffb61-121">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="ffb61-122">Sortering</span><span class="sxs-lookup"><span data-stu-id="ffb61-122">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="ffb61-123">Bruke Søk etter side eller rapport</span><span class="sxs-lookup"><span data-stu-id="ffb61-123">Using Search for Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="ffb61-124">[Administrere brukere og tillatelser](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="ffb61-124">[How to: Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="ffb61-125">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ffb61-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

