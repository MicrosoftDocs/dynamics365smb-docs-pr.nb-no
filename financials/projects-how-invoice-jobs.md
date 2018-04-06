---
title: "Opprette en salgsfaktura for prosjekt for å fakturere et prosjekt | Microsoft-dokumentasjon"
description: Beskriver hvordan du kan fakturere kunder for prosjektutgifter etter hvert som et prosjekt skrider frem.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4c00ce50f70cbae3ad0557f0703e80f6b115995a
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="invoice-jobs"></a><span data-ttu-id="b8a0d-103">Fakturere prosjekter</span><span class="sxs-lookup"><span data-stu-id="b8a0d-103">Invoice Jobs</span></span>
<span data-ttu-id="b8a0d-104">I løpet av prosjektet kan det akkumuleres prosjektkostnader fra ressursforbruk, materiale og prosjektrelaterte kjøp.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-104">During the project, job costs from resource usage, materials, and job-related purchases can accumulate.</span></span> <span data-ttu-id="b8a0d-105">Under fremdriften til prosjektet blir disse transaksjonene bokført til prosjektkladden.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-105">As the job progresses, these transactions get posted to the job journal.</span></span> <span data-ttu-id="b8a0d-106">Det er viktig at alle kostnader blir registrert i prosjektkladden før du fakturerer kunden.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-106">It is important that all costs get recorded in the job journal before you invoice the customer.</span></span>

<span data-ttu-id="b8a0d-107">Du kan fakturere hele prosjektet fra vinduet **Prosjektoppgavelinjer** eller bare fakturere utvalgte fakturerbare linjer fra vinduet **Planleggingslinjer**.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-107">You can invoice the whole job from the **Job Task Lines** window or only invoice selected billable lines from the **Planning Lines** window.</span></span> <span data-ttu-id="b8a0d-108">Fakturering kan utføres etter at prosjektet er fullført, eller ved bestemte intervaller under fremdriften til prosjektet, basert på en faktureringsplan.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-108">Invoicing can be done after the job is finished or at certain intervals during the job's progress based on an invoicing schedule.</span></span>

> [!NOTE]  
>   <span data-ttu-id="b8a0d-109">Hvis du velger **Fakturerbar** i feltet **Prosjektlinjetype** i kjøpsdokumentene for prosjektrelaterte kjøp, opprettes prosjektplanleggingslinjer som er klare til å bli fakturert til kunden.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-109">If you select **Billable** in the **Job Line Type** field on the purchase documents for job-related purchases, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="b8a0d-110">Hvis du vil ha mer informasjon, kan du se [Administrere prosjektforsyninger](projects-how-manage-project-supplies.md).</span><span class="sxs-lookup"><span data-stu-id="b8a0d-110">For more information, see [Manage Project Supplies](projects-how-manage-project-supplies.md).</span></span>

## <a name="to-create-and-post-a-job-sales-invoice"></a><span data-ttu-id="b8a0d-111">Slik oppretter og bokfører du en salgsfaktura for prosjekt</span><span class="sxs-lookup"><span data-stu-id="b8a0d-111">To create and post a job sales invoice</span></span>
<span data-ttu-id="b8a0d-112">Du kan opprette en faktura for et prosjekt eller for én eller flere prosjektoppgaver for en kunde enten når arbeidet som skal faktureres, er fullført, eller når faktureringsdatoen som er basert på et faktureringsestimat, er nådd.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-112">You can create an invoice for a job or for one or more job tasks for a customer when either the work to be invoiced is complete or the date for invoicing based on an invoicing schedule has been reached.</span></span>

<span data-ttu-id="b8a0d-113">Fra vinduet **Prosjekter** kan du fakturere en kunde ved å velge prosjektet, og deretter velge handlingen **Opprett salgsfaktura for prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-113">From the **Jobs** window, you can invoice a customer by selecting the job, and then choosing the **Create Job Sales Invoice** action.</span></span> <span data-ttu-id="b8a0d-114">Følgende fremgangsmåte viser hvordan du bruker en satsvis jobb til å fakturere flere prosjekter.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-114">The following procedure shows how to use a batch job to invoice multiple jobs.</span></span>  

1. <span data-ttu-id="b8a0d-115">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Opprett salgsfaktura for prosjekt**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Job Create Sales Invoice**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b8a0d-116">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-116">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="b8a0d-117">Angi filtre hvis du vil begrense prosjektene som kjørselen skal behandle.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-117">Set filters if you want to limit the jobs that the batch job will process.</span></span>
4. <span data-ttu-id="b8a0d-118">Velg **OK** for å opprette fakturaene.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-118">Choose the **OK** button to create the invoices.</span></span>  

## <a name="to-create-multiple-job-sales-invoices-from-job-planning-lines"></a><span data-ttu-id="b8a0d-119">Slik oppretter du flere prosjektsalgsfakturaer fra prosjektplanleggingslinjer</span><span class="sxs-lookup"><span data-stu-id="b8a0d-119">To create multiple job sales invoices from job planning lines</span></span>
<span data-ttu-id="b8a0d-120">Du kan opprette en faktura fra en prosjektplanleggingslinje og samtidig angi antallet for varen, ressursen eller finanskontoen som du vil fakturere.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-120">You can create an invoice from a job planning lines, and indicate at that time the quantity of the item, resource, or general ledger account that you want to invoice.</span></span>

1. <span data-ttu-id="b8a0d-121">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Prosjekter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="b8a0d-122">Åpne et relevant prosjekt.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-122">Open a relevant job.</span></span>
3. <span data-ttu-id="b8a0d-123">Velg en prosjektoppgave der feltet **Prosjektoppgavetype** inneholder **Bokføring**, og velg deretter handlingen **Prosjektplanleggingslinjer**.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-123">Select a job task for which the **Job Task Type** field contains **Posting**, and then choose the **Job Planning Lines** action.</span></span>  
4. <span data-ttu-id="b8a0d-124">På en prosjektplanleggingslinjer, i feltet **Ant. som skal overføres til faktura** angir du antallet av varen, ressursen, finanskontotypen du vil fakturere.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-124">On a job planning line, in the **Qty. To Transfer to Invoice** field, enter the quantity of the item, resource, general ledger account type that you want to invoice.</span></span>  
5. <span data-ttu-id="b8a0d-125">Velg handlingen **Opprett salgsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-125">Choose the **Create Sales Invoice** action.</span></span>
6. <span data-ttu-id="b8a0d-126">I vinduet **Opprett salgsfaktura for prosjekt** skriver du inn bokføringsdatoen og om du vil opprette en ny faktura eller føye til denne fakturaen til en eksisterende.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-126">In the **Job Create Sales Invoice** window, enter the posting date and whether you want to create a new invoice or append this invoice to an existing one.</span></span>
7. <span data-ttu-id="b8a0d-127">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-127">Choose the **OK** button.</span></span>  

    <span data-ttu-id="b8a0d-128">Du kan se antallet i feltet **Ant. overført til faktura** på prosjektplanleggingslinjen.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-128">On the job planning line, in the **Qty. Transferred to Invoice** field, you can see the quantity.</span></span>
8. <span data-ttu-id="b8a0d-129">I vinduet **Prosjektplanleggingslinjer** velger du handlingen **Salgsfakturaer/kreditnotaer**.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-129">In the **Job Planning Lines** window, choose the **Sales Invoices/Credit Memos** action.</span></span>

    <span data-ttu-id="b8a0d-130">Vinduet **Salgsfaktura** åpnes og viser antallet du har overført til fakturaen.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-130">The **Sales Invoice** window opens, showing the quantity that you have transferred to the invoice.</span></span>  
9. <span data-ttu-id="b8a0d-131">Gjør flere endringer, og velg deretter handlingen **Bokfør**.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-131">Make any additional changes, and then choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="b8a0d-132">Fremgangsmåten ovenfor er identisk for å opprette, gå gjennom og bokføre en prosjektrelatert salgskreditnota.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-132">The above procedure is similar for creating, reviewing, and posting a job-related sales credit memo.</span></span>

## <a name="to-calculate-and-post-job-completion-entries"></a><span data-ttu-id="b8a0d-133">Slik beregner og bokfører du prosjektferdiggjørelsesposter</span><span class="sxs-lookup"><span data-stu-id="b8a0d-133">To calculate and post job completion entries</span></span>
<span data-ttu-id="b8a0d-134">Når du har fullført alle aktiviteter for et prosjekt, inkludert bokføring og fakturering, må du oppdatere prosjektet for å sette **Status** til **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-134">When you have completed all activities for a job, including usage posting and invoicing, you must update the job to have a **Status** of **Completed**.</span></span> <span data-ttu-id="b8a0d-135">Deretter må du reversere alle VIA-er som er bokført i finans.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-135">Then, you must reverse any WIP that has been posted to the general ledger.</span></span>

1. <span data-ttu-id="b8a0d-136">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Prosjekter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b8a0d-137">Merk et åpent prosjekt, og velg handlingen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-137">Select an open job, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="b8a0d-138">I feltet **Status** velger du **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-138">In the **Status** field, select **Completed**.</span></span>
4. <span data-ttu-id="b8a0d-139">Følg hjelpetrinnene for å beregne og bokføre VIA.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-139">Follow the assistance steps to calculate and post WIP.</span></span> <span data-ttu-id="b8a0d-140">Alternativt følger du trinn 5 og 6 hvis du vil gjøre dette manuelt.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-140">Alternatively, follows steps 5 and 6 to do so manually.</span></span>  
5. <span data-ttu-id="b8a0d-141">Velg handlingen **Beregn VIA**.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-141">Choose the **Calculate WIP** action.</span></span>
6. <span data-ttu-id="b8a0d-142">I vinduet **Beregn VIA for prosjekt** fyller du ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-142">In the **Job Calculate WIP** window, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="b8a0d-143">VIA-postene for prosjekt du oppretter ved å kjøre kjørselen, vil ha en avmerking i **Prosjekt ferdig**-boksen for å angi at de er ferdiggjørelsesposter.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-143">The job WIP entries created by running the batch job will have the **Job Complete** check box selected to show that they are completion entries.</span></span>  
7. <span data-ttu-id="b8a0d-144">Velg handlingen **Bokfør VIA i Finans for prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-144">Choose the **Job Post WIP to G/L** action.</span></span>
8. <span data-ttu-id="b8a0d-145">Fyll ut feltene etter behov i vinduet **Bokfør VIA i Finans for prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-145">In the **Job Post WIP to G/L** window, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="b8a0d-146">VIA-finanspostene for prosjekt som du oppretter ved å kjøre kjørselen, vil ha en avmerking i **Prosjekt ferdig**-boksen for å angi at de er ferdiggjørelsesposter.</span><span class="sxs-lookup"><span data-stu-id="b8a0d-146">The job WIP general ledger entries created by running the batch job will have the **Job Complete** check box selected to show they are completion entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="b8a0d-147">Se også</span><span class="sxs-lookup"><span data-stu-id="b8a0d-147">See Also</span></span>
[<span data-ttu-id="b8a0d-148">Administrere prosjekter</span><span class="sxs-lookup"><span data-stu-id="b8a0d-148">Managing Projects</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="b8a0d-149">Finans</span><span class="sxs-lookup"><span data-stu-id="b8a0d-149">Finance</span></span>](finance.md)  
<span data-ttu-id="b8a0d-150">[Innkjøp](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="b8a0d-150">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="b8a0d-151">[Salg](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="b8a0d-151">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="b8a0d-152">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b8a0d-152">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

