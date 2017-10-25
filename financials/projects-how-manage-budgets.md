---
title: Definere og administrere et budsjett for et prosjekt | Microsoft-dokumentasjon
description: "Beskriver hvordan du planlegger ressurser og prognose, og styrer prosjektkostnader ved å definere et budsjett for hvert prosjekt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project budget, forecast
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 0e480c67ddb2acd5e98799c98cb1cd9d972889df
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-manage-job-budgets"></a><span data-ttu-id="a2235-103">Administrere prosjektbudsjetter</span><span class="sxs-lookup"><span data-stu-id="a2235-103">How to: Manage Job Budgets</span></span>
<span data-ttu-id="a2235-104">Du kan opprette et budsjett for hvert prosjekt.</span><span class="sxs-lookup"><span data-stu-id="a2235-104">You can set up a budget for each job.</span></span> <span data-ttu-id="a2235-105">Budsjettet brukes til å planlegge ressursene du tildeler til et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="a2235-105">The budget is used to plan the resources that you allocate to a job.</span></span> <span data-ttu-id="a2235-106">Budsjettet kan enten være generelt med få poster, eller det kan inneholde mange poster som er oppdelt i aktivitetsnivåer.</span><span class="sxs-lookup"><span data-stu-id="a2235-106">The budget can be either general with few entries or it can contain more entries that are divided into activity levels.</span></span> <span data-ttu-id="a2235-107">Deretter kan du sammenligne de budsjetterte beløpene med det faktiske forbruket slik det er registrert i prosjektkladden.</span><span class="sxs-lookup"><span data-stu-id="a2235-107">You can then compare the budgeted amounts with the actual usage as recorded in the job journal.</span></span> <span data-ttu-id="a2235-108">Ved å overvåke forskjeller mellom faktisk bruk og budsjettert bruk kan du kontrollere et pågående prosjekt og forbedre kvaliteten på fremtidige prosjekter ved å redusere risikoen for å underestimere kostnader.</span><span class="sxs-lookup"><span data-stu-id="a2235-108">By monitoring differences between actual usage and budgeted usage, you can control an ongoing project and improve the quality of future jobs by reducing the risk of underestimating costs.</span></span>

<span data-ttu-id="a2235-109">Følgende fremgangsmåte beskriver hvordan du kan beregne budsjetterte kostnader under planleggingen.</span><span class="sxs-lookup"><span data-stu-id="a2235-109">The following procedure describes how to estimate budgeted costs during planning.</span></span> <span data-ttu-id="a2235-110">Hvis du vil ha informasjon om registrering av budsjetterte sammenlignet med faktiske prosjektpriser og kostnader, kan du se [Registrere forbruk for prosjekter](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="a2235-110">For information about recording budgeted versus actual job prices and costs, see [How to: Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>  

## <span data-ttu-id="a2235-111"><a name="JobBudgetCosts"></a> Slik estimerer du budsjetterte kostnader for et prosjekt</span><span class="sxs-lookup"><span data-stu-id="a2235-111"><a name="JobBudgetCosts"></a> To estimate the budgeted costs for a job</span></span>
<span data-ttu-id="a2235-112">Når en kunde vil vite prisen på et prosjekt som faktureres basert på forbruk, må du fastsette de budsjetterte kostbeløpene for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="a2235-112">When a customer wants to know the price of a job that will be invoiced based on usage, you must have to determine the budgeted costs for the job.</span></span> <span data-ttu-id="a2235-113">Du bruker vinduet **Prosjektoppgavelinjer** til å gjøre dette.</span><span class="sxs-lookup"><span data-stu-id="a2235-113">You use the **Job Task Lines** window to do this.</span></span>

1. <span data-ttu-id="a2235-114">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Prosjekter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a2235-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a2235-115">Åpne et relevant prosjekt.</span><span class="sxs-lookup"><span data-stu-id="a2235-115">Open a relevant job.</span></span>
3. <span data-ttu-id="a2235-116">Merk en oppgavelinje for bokføring, og velg deretter handlingen **Prosjektplanleggingslinjer**.</span><span class="sxs-lookup"><span data-stu-id="a2235-116">Select a task line of type Posting, and then choose the **Job Planning Lines** action.</span></span>
4. <span data-ttu-id="a2235-117">Fyll ut feltene etter behov på en ny linje.</span><span class="sxs-lookup"><span data-stu-id="a2235-117">On a new line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

<span data-ttu-id="a2235-118">Se følgende informasjon for feltet **Linjetype**.</span><span class="sxs-lookup"><span data-stu-id="a2235-118">For the **Line Type** field, refer to the following information.</span></span>  

| <span data-ttu-id="a2235-119">Linjetype</span><span class="sxs-lookup"><span data-stu-id="a2235-119">Line Type</span></span> | <span data-ttu-id="a2235-120">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a2235-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="a2235-121">**Både Budsjett og Fakturerbar**</span><span class="sxs-lookup"><span data-stu-id="a2235-121">**Both Budget and Billable**</span></span> |<span data-ttu-id="a2235-122">Kost- og prisbeløpene som er angitt på planleggingslinjen, er budsjettert kost for den bestemte planleggingslinjen.</span><span class="sxs-lookup"><span data-stu-id="a2235-122">The cost and price amounts entered on the planning line are the budgeted costs for the particular planning line.</span></span> <span data-ttu-id="a2235-123">Prisbeløpet vil bli fakturert.</span><span class="sxs-lookup"><span data-stu-id="a2235-123">The price amount will be invoiced.</span></span> |
| <span data-ttu-id="a2235-124">**Budsjett**</span><span class="sxs-lookup"><span data-stu-id="a2235-124">**Budget**</span></span> |<span data-ttu-id="a2235-125">Kunden belastes ikke for forbruk.</span><span class="sxs-lookup"><span data-stu-id="a2235-125">The customer is not charged for usage.</span></span> <span data-ttu-id="a2235-126">Forbruk overføres ikke til en faktura, men brukes likevel i VIA-beregningen.</span><span class="sxs-lookup"><span data-stu-id="a2235-126">Usage is not transferred to an invoice, but will still be used in the calculation of WIP.</span></span> |
| <span data-ttu-id="a2235-127">**Fakturerbar**</span><span class="sxs-lookup"><span data-stu-id="a2235-127">**Billable**</span></span> |<span data-ttu-id="a2235-128">Kunden belastes for forbruk.</span><span class="sxs-lookup"><span data-stu-id="a2235-128">The customer is charged for usage.</span></span> <span data-ttu-id="a2235-129">Forbruk overføres til fakturaen basert på antallet angitt i feltet Ant. som skal overføres til faktura.</span><span class="sxs-lookup"><span data-stu-id="a2235-129">Usage is transferred to the invoice, based on the quantity specified in the Qty. to Transfer to Invoice field.</span></span> |

> [!NOTE]  
>   <span data-ttu-id="a2235-130">Feltet **Planleggingsdato** for planleggingslinjen inneholder datoen da forbruk som er knyttet til planleggingslinjen, er forventet å fullføres.</span><span class="sxs-lookup"><span data-stu-id="a2235-130">The **Planning Date** field for the planning line contains the date when usage related to the planning line is expected to be completed.</span></span> <span data-ttu-id="a2235-131">Det er også datoen da planleggingslinjen kan overføres til en salgsfaktura og bokføres.</span><span class="sxs-lookup"><span data-stu-id="a2235-131">It is also the date when the planning line may be transferred to a sales invoice and posted.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="a2235-132">Når du fyller ut feltet **Antall**, blir all informasjon om totalpris og totalkostnad beregnet og fylt ut for denne planleggingslinjen.</span><span class="sxs-lookup"><span data-stu-id="a2235-132">When you fill in the **Quantity** field, all total price and total cost information will be calculated and filled in for that planning line.</span></span> <span data-ttu-id="a2235-133">Du kan redigere dem når som helst.</span><span class="sxs-lookup"><span data-stu-id="a2235-133">You can edit them at any time.</span></span>

<span data-ttu-id="a2235-134">I vinduet **Prosjektkort** kan du nå se en oversikt over totalt budsjetterte kostnader, budsjettert pris, fakturerbar kostnad og fakturerbar pris for hver oppgave.</span><span class="sxs-lookup"><span data-stu-id="a2235-134">In the **Job Card** window, you can now see a summary of the total budgeted costs, budgeted price, billable cost and billable price for each task.</span></span>

<span data-ttu-id="a2235-135">Hvis du vil ha informasjon om registrering av budsjetterte sammenlignet med faktiske prosjektpriser og kostnader, kan du se [Registrere forbruk for prosjekter](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="a2235-135">For information about recording budgeted versus actual job prices and costs, see [How to: Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a2235-136">Se også</span><span class="sxs-lookup"><span data-stu-id="a2235-136">See Also</span></span>
[<span data-ttu-id="a2235-137">Prosjektstyring</span><span class="sxs-lookup"><span data-stu-id="a2235-137">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="a2235-138">Finans</span><span class="sxs-lookup"><span data-stu-id="a2235-138">Finance</span></span>](finance.md)  
<span data-ttu-id="a2235-139">[Innkjøp](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="a2235-139">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="a2235-140">[Salg](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="a2235-140">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="a2235-141">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a2235-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

