---
title: Tilordne og håndtere oppgaver | Microsoft-dokumentasjon
description: Lære hvordan du tilordner oppgaver til brukere, inkludert din regnskapsfører i Business Central
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: tasks, work
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 5befadf7a162cc2094fbb1ef426e25d02d50e856
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241171"
---
# <a name="define-user-tasks"></a><span data-ttu-id="d3cb2-103">Definere brukeroppgaver</span><span class="sxs-lookup"><span data-stu-id="d3cb2-103">Define User Tasks</span></span>
<span data-ttu-id="d3cb2-104">I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du opprette oppgaver for å holde orden på arbeid.</span><span class="sxs-lookup"><span data-stu-id="d3cb2-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], you can create tasks to remind you of work to be done.</span></span> <span data-ttu-id="d3cb2-105">Du kan opprette oppgaver selv, men du kan også tilordne aktiviteter til andre eller bli tilordnet til en aktivitet av andre i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="d3cb2-105">You can create tasks for yourself, but you can also assign tasks to others or be assigned a task by someone else in your organization.</span></span>  

## <a name="managing-user-tasks"></a><span data-ttu-id="d3cb2-106">Administrere brukeroppgaver</span><span class="sxs-lookup"><span data-stu-id="d3cb2-106">Managing User Tasks</span></span>
<span data-ttu-id="d3cb2-107">**Brukeroppgaver**-siden viser alle oppgaver, og du kan opprette og tilordne nye aktiviteter enkel måte.</span><span class="sxs-lookup"><span data-stu-id="d3cb2-107">The **User Tasks** page shows all tasks, and you can easily create and assign new tasks.</span></span> <span data-ttu-id="d3cb2-108">Når du oppretter en oppgave, kan du angi start- og forfallsdato, og du kan legge til en kobling til siden i [!INCLUDE[d365fin](includes/d365fin_md.md)] hvor oppgaven må utføres.</span><span class="sxs-lookup"><span data-stu-id="d3cb2-108">When you create a task, you can specify the start date and due date, and you can add a link to the page in [!INCLUDE[d365fin](includes/d365fin_md.md)] where the user must do the work.</span></span>  

<span data-ttu-id="d3cb2-109">Du kan for eksempel opprette en oppgave for deg selv for å vise alle bokførte salgsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="d3cb2-109">For example, you can create a task for yourself to view all posted sales invoices.</span></span> <span data-ttu-id="d3cb2-110">I så fall knytter du oppgaven til side 143, bokførte salgsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="d3cb2-110">In that case, you link the task to page 143, Posted Sales Invoices.</span></span>  

<span data-ttu-id="d3cb2-111">![Eksempel på en brukeroppgave](media/across-user-tasks/sample-user-task.png "Eksempel på en brukeroppgave")</span><span class="sxs-lookup"><span data-stu-id="d3cb2-111">![Example of a User Task](media/across-user-tasks/sample-user-task.png "Example of a user task")</span></span>

> [!TIP]  
>  <span data-ttu-id="d3cb2-112">Bruk oppslag i **Side**-feltet og bruk deretter **Søk etter en side eller rapport**-feltet for å finne siden du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="d3cb2-112">Use the look-up in the **Page** field and then use the **Search for Page or Report** field to find the page that you want.</span></span> <span data-ttu-id="d3cb2-113">Hvis du vil ha mer informasjon, se [Søke etter en side eller rapport](ui-search.md).</span><span class="sxs-lookup"><span data-stu-id="d3cb2-113">For more information, see [Searching for a Page or Report](ui-search.md).</span></span>  

### <a name="picking-up-user-tasks"></a><span data-ttu-id="d3cb2-114">Plukke opp brukeroppgaver</span><span class="sxs-lookup"><span data-stu-id="d3cb2-114">Picking Up User Tasks</span></span>
<span data-ttu-id="d3cb2-115">I rollesentrene for forretningsleder og regnskapsfører viser en rute ventende oppgaver som er tilordnet denne brukeren.</span><span class="sxs-lookup"><span data-stu-id="d3cb2-115">In the Business Manager, Bookkeeper, and Accountant Role Centers, a tile shows pending tasks that are assigned to that user.</span></span> <span data-ttu-id="d3cb2-116">For å plukke opp en oppgave, velger du den ganske enkelt fra listen over ventende brukeroppgaver.</span><span class="sxs-lookup"><span data-stu-id="d3cb2-116">To pick up a task, simply choose it from the list of pending user tasks.</span></span> <span data-ttu-id="d3cb2-117">I båndet åpner **Gå til oppgaveelement**-koblingen siden der du kan gjøre oppgaven.</span><span class="sxs-lookup"><span data-stu-id="d3cb2-117">In the ribbon, the link **Go to Task Item** opens the page where you can do the work.</span></span>  

<span data-ttu-id="d3cb2-118">Når du har fullført en oppgave, merker du den som fullført.</span><span class="sxs-lookup"><span data-stu-id="d3cb2-118">When you have completed a task, simply mark it as completed.</span></span>  

### <a name="deleting-user-tasks"></a><span data-ttu-id="d3cb2-119">Slett brukeroppgaver</span><span class="sxs-lookup"><span data-stu-id="d3cb2-119">Deleting User Tasks</span></span>
<span data-ttu-id="d3cb2-120">Hvis du vil slette alle eller noen brukeroppgaver samlet, kan du bruke **Slett brukeroppgaver**-rapporten.</span><span class="sxs-lookup"><span data-stu-id="d3cb2-120">If you want to bulk delete all or some user tasks, you can use the **Delete User Tasks** report.</span></span> <span data-ttu-id="d3cb2-121">På forespørselssiden kan du angi filtre som bestemmer hvilke aktiviteter som må slettes.</span><span class="sxs-lookup"><span data-stu-id="d3cb2-121">In the request page, you can set filters to determine which tasks must be deleted.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d3cb2-122">Se også</span><span class="sxs-lookup"><span data-stu-id="d3cb2-122">See Also</span></span>
[<span data-ttu-id="d3cb2-123">Søke etter en side eller rapport</span><span class="sxs-lookup"><span data-stu-id="d3cb2-123">Searching for a Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="d3cb2-124">[Regnskapsføreropplevelser i [!INCLUDE[d365fin](includes/d365fin_md.md)]](finance-accounting.md)</span><span class="sxs-lookup"><span data-stu-id="d3cb2-124">[Accountant Experiences in [!INCLUDE[d365fin](includes/d365fin_md.md)]](finance-accounting.md)</span></span>  
