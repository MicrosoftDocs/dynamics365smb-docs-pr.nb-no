---
title: Definere og administrere et budsjett for et prosjekt | Microsoft-dokumentasjon
description: Beskriver hvordan du planlegger ressurser og prognose, og styrer prosjektkostnader ved å definere et budsjett for hvert prosjekt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project budget, forecast
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e8de8d35ee036d2819ba40b1fdf50b6d5ed2dab5
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3913174"
---
# <a name="manage-job-budgets"></a><span data-ttu-id="76721-103">Administrere prosjektbudsjetter</span><span class="sxs-lookup"><span data-stu-id="76721-103">Manage Job Budgets</span></span>
<span data-ttu-id="76721-104">Du kan opprette et budsjett for hvert prosjekt.</span><span class="sxs-lookup"><span data-stu-id="76721-104">You can set up a budget for each job.</span></span> <span data-ttu-id="76721-105">Budsjettet brukes til å planlegge ressursene du tildeler til et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="76721-105">The budget is used to plan the resources that you allocate to a job.</span></span> <span data-ttu-id="76721-106">Budsjettet kan enten være generelt med få poster, eller det kan inneholde mange poster som er oppdelt i aktivitetsnivåer.</span><span class="sxs-lookup"><span data-stu-id="76721-106">The budget can be either general with few entries or it can contain more entries that are divided into activity levels.</span></span> <span data-ttu-id="76721-107">Deretter kan du sammenligne de budsjetterte beløpene med det faktiske forbruket slik det er registrert i prosjektkladden.</span><span class="sxs-lookup"><span data-stu-id="76721-107">You can then compare the budgeted amounts with the actual usage as recorded in the job journal.</span></span> <span data-ttu-id="76721-108">Ved å overvåke forskjeller mellom faktisk bruk og budsjettert bruk kan du kontrollere et pågående prosjekt og forbedre kvaliteten på fremtidige prosjekter ved å redusere risikoen for å underestimere kostnader.</span><span class="sxs-lookup"><span data-stu-id="76721-108">By monitoring differences between actual usage and budgeted usage, you can control an ongoing project and improve the quality of future jobs by reducing the risk of underestimating costs.</span></span>

<span data-ttu-id="76721-109">Følgende fremgangsmåte beskriver hvordan du kan beregne budsjetterte kostnader under planleggingen.</span><span class="sxs-lookup"><span data-stu-id="76721-109">The following procedure describes how to estimate budgeted costs during planning.</span></span> <span data-ttu-id="76721-110">Hvis du vil ha informasjon om registrering av budsjetterte sammenlignet med faktiske prosjektpriser og kostnader, kan du se [Registrere forbruk for prosjekter](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="76721-110">For information about recording budgeted versus actual job prices and costs, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>  

## <a name="to-estimate-the-budgeted-costs-for-a-job"></a><a name="JobBudgetCosts"></a> <span data-ttu-id="76721-111">Slik estimerer du budsjetterte kostnader for et prosjekt</span><span class="sxs-lookup"><span data-stu-id="76721-111">To estimate the budgeted costs for a job</span></span>
<span data-ttu-id="76721-112">Når en kunde vil vite prisen på et prosjekt som faktureres basert på forbruk, må du fastsette de budsjetterte kostbeløpene for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="76721-112">When a customer wants to know the price of a job that will be invoiced based on usage, you must have to determine the budgeted costs for the job.</span></span> <span data-ttu-id="76721-113">Du bruker siden **Prosjektoppgavelinjer** til å gjøre dette.</span><span class="sxs-lookup"><span data-stu-id="76721-113">You use the **Job Task Lines** page to do this.</span></span>

1. <span data-ttu-id="76721-114">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Prosjekter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="76721-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="76721-115">Åpne et relevant prosjekt.</span><span class="sxs-lookup"><span data-stu-id="76721-115">Open a relevant job.</span></span>
3. <span data-ttu-id="76721-116">Merk en oppgavelinje for bokføring, og velg deretter handlingen **Prosjektplanleggingslinjer**.</span><span class="sxs-lookup"><span data-stu-id="76721-116">Select a task line of type Posting, and then choose the **Job Planning Lines** action.</span></span>
4. <span data-ttu-id="76721-117">Fyll ut feltene etter behov på en ny linje.</span><span class="sxs-lookup"><span data-stu-id="76721-117">On a new line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

<span data-ttu-id="76721-118">Se følgende informasjon for feltet **Linjetype**.</span><span class="sxs-lookup"><span data-stu-id="76721-118">For the **Line Type** field, refer to the following information.</span></span>  

| <span data-ttu-id="76721-119">Linjetype</span><span class="sxs-lookup"><span data-stu-id="76721-119">Line Type</span></span> | <span data-ttu-id="76721-120">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="76721-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="76721-121">**Både Budsjett og Fakturerbar**</span><span class="sxs-lookup"><span data-stu-id="76721-121">**Both Budget and Billable**</span></span> |<span data-ttu-id="76721-122">Kost- og prisbeløpene som er angitt på planleggingslinjen, er budsjettert kost for den bestemte planleggingslinjen.</span><span class="sxs-lookup"><span data-stu-id="76721-122">The cost and price amounts entered on the planning line are the budgeted costs for the particular planning line.</span></span> <span data-ttu-id="76721-123">Prisbeløpet vil bli fakturert.</span><span class="sxs-lookup"><span data-stu-id="76721-123">The price amount will be invoiced.</span></span> |
| <span data-ttu-id="76721-124">**Budsjett**</span><span class="sxs-lookup"><span data-stu-id="76721-124">**Budget**</span></span> |<span data-ttu-id="76721-125">Kunden belastes ikke for forbruk.</span><span class="sxs-lookup"><span data-stu-id="76721-125">The customer is not charged for usage.</span></span> <span data-ttu-id="76721-126">Forbruk overføres ikke til en faktura, men brukes likevel i VIA-beregningen.</span><span class="sxs-lookup"><span data-stu-id="76721-126">Usage is not transferred to an invoice, but will still be used in the calculation of WIP.</span></span> |
| <span data-ttu-id="76721-127">**Fakturerbar**</span><span class="sxs-lookup"><span data-stu-id="76721-127">**Billable**</span></span> |<span data-ttu-id="76721-128">Kunden belastes for forbruk.</span><span class="sxs-lookup"><span data-stu-id="76721-128">The customer is charged for usage.</span></span> <span data-ttu-id="76721-129">Forbruk overføres til fakturaen basert på antallet angitt i feltet Ant. som skal overføres til faktura.</span><span class="sxs-lookup"><span data-stu-id="76721-129">Usage is transferred to the invoice, based on the quantity specified in the Qty. to Transfer to Invoice field.</span></span> |

> [!NOTE]  
> <span data-ttu-id="76721-130">Feltet **Planlagt lev.dato** for planleggingslinjen inneholder datoen da forbruk som er knyttet til planleggingslinjen, er forventet å fullføres.</span><span class="sxs-lookup"><span data-stu-id="76721-130">The **Planned Delivery Date** field for the planning line contains the date when usage related to the planning line is expected to be completed.</span></span> <span data-ttu-id="76721-131">Det er også datoen da planleggingslinjen kan overføres til en salgsfaktura og bokføres.</span><span class="sxs-lookup"><span data-stu-id="76721-131">It is also the date when the planning line may be transferred to a sales invoice and posted.</span></span> <br /><br /> <span data-ttu-id="76721-132">I den underliggende prosjektoppgaven på siden **Prosjektkort** inneholder **Startdato**- og **Sluttdato**-feltene verdien av feltet **Planlagt leveringsdato** i de første og siste prosjektplanleggingslinjer på den tilhørende **Prosjektplanleggingslinjer**-siden.</span><span class="sxs-lookup"><span data-stu-id="76721-132">On the underlying job task on the **Job Card** page, the **Start Date** and **End Date** fields respectively contain the value of the **Planned Delivery Date** field on the earliest and latest job planning lines in the related **Job Planning Lines** page.</span></span>

> [!NOTE]  
>   <span data-ttu-id="76721-133">Når du fyller ut feltet **Antall**, blir all informasjon om totalpris og totalkostnad beregnet og fylt ut for denne planleggingslinjen.</span><span class="sxs-lookup"><span data-stu-id="76721-133">When you fill in the **Quantity** field, all total price and total cost information will be calculated and filled in for that planning line.</span></span> <span data-ttu-id="76721-134">Du kan redigere dem når som helst.</span><span class="sxs-lookup"><span data-stu-id="76721-134">You can edit them at any time.</span></span>

<span data-ttu-id="76721-135">På siden **Prosjektkort** kan du nå se en oversikt over totalt budsjetterte kostnader, budsjettert pris, fakturerbar kostnad og fakturerbar pris for hver oppgave.</span><span class="sxs-lookup"><span data-stu-id="76721-135">On the **Job Card** page, you can now see a summary of the total budgeted costs, budgeted price, billable cost and billable price for each task.</span></span>

<span data-ttu-id="76721-136">Hvis du vil ha informasjon om registrering av budsjetterte sammenlignet med faktiske prosjektpriser og kostnader, kan du se [Registrere forbruk for prosjekter](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="76721-136">For information about recording budgeted versus actual job prices and costs, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="76721-137">Se også</span><span class="sxs-lookup"><span data-stu-id="76721-137">See Also</span></span>
[<span data-ttu-id="76721-138">Prosjektstyring</span><span class="sxs-lookup"><span data-stu-id="76721-138">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="76721-139">Finans</span><span class="sxs-lookup"><span data-stu-id="76721-139">Finance</span></span>](finance.md)  
<span data-ttu-id="76721-140">[Innkjøp](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="76721-140">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="76721-141">[Salg](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="76721-141">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="76721-142">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="76721-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
