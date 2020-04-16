---
title: Opprette en salgsfaktura for prosjekt for å fakturere et prosjekt | Microsoft-dokumentasjon
description: Beskriver hvordan du kan fakturere kunder for prosjektutgifter etter hvert som et prosjekt skrider frem.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 277e5e6cb212202f930ed49012184aa67a23d03f
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191262"
---
# <a name="invoice-jobs"></a><span data-ttu-id="659a4-103">Fakturere prosjekter</span><span class="sxs-lookup"><span data-stu-id="659a4-103">Invoice Jobs</span></span>
<span data-ttu-id="659a4-104">I løpet av prosjektet kan det akkumuleres prosjektkostnader fra ressursforbruk, materiale og prosjektrelaterte kjøp.</span><span class="sxs-lookup"><span data-stu-id="659a4-104">During the project, job costs from resource usage, materials, and job-related purchases can accumulate.</span></span> <span data-ttu-id="659a4-105">Under fremdriften til prosjektet blir disse transaksjonene bokført til prosjektkladden.</span><span class="sxs-lookup"><span data-stu-id="659a4-105">As the job progresses, these transactions get posted to the job journal.</span></span> <span data-ttu-id="659a4-106">Det er viktig at alle kostnader blir registrert i prosjektkladden før du fakturerer kunden.</span><span class="sxs-lookup"><span data-stu-id="659a4-106">It is important that all costs get recorded in the job journal before you invoice the customer.</span></span>

> [!NOTE]
> <span data-ttu-id="659a4-107">Du kan også kjøpe eksterne ressurser som ikke er knyttet til et prosjekt, for eksempel for å fakturere en leverandør for arbeid som er levert.</span><span class="sxs-lookup"><span data-stu-id="659a4-107">You can also purchase external resources unrelated to a job, for example, to invoice a vendor for work delivered.</span></span> <span data-ttu-id="659a4-108">Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="659a4-108">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

<span data-ttu-id="659a4-109">Du kan fakturere hele prosjektet fra siden **Prosjektoppgavelinjer** eller bare fakturere utvalgte fakturerbare linjer fra siden **Planleggingslinjer**.</span><span class="sxs-lookup"><span data-stu-id="659a4-109">You can invoice the whole job from the **Job Task Lines** page or only invoice selected billable lines from the **Planning Lines** page.</span></span> <span data-ttu-id="659a4-110">Fakturering kan utføres etter at prosjektet er fullført, eller ved bestemte intervaller under fremdriften til prosjektet, basert på en faktureringsplan.</span><span class="sxs-lookup"><span data-stu-id="659a4-110">Invoicing can be done after the job is finished or at certain intervals during the job's progress based on an invoicing schedule.</span></span>

> [!NOTE]  
>   <span data-ttu-id="659a4-111">Hvis du velger **Fakturerbar** i feltet **Prosjektlinjetype** i kjøpsdokumentene for prosjektrelaterte kjøp, opprettes prosjektplanleggingslinjer som er klare til å bli fakturert til kunden.</span><span class="sxs-lookup"><span data-stu-id="659a4-111">If you select **Billable** in the **Job Line Type** field on the purchase documents for job-related purchases, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="659a4-112">Hvis du vil ha mer informasjon, kan du se [Administrere prosjektforsyninger](projects-how-manage-project-supplies.md).</span><span class="sxs-lookup"><span data-stu-id="659a4-112">For more information, see [Manage Project Supplies](projects-how-manage-project-supplies.md).</span></span>

## <a name="to-create-and-post-a-job-sales-invoice"></a><span data-ttu-id="659a4-113">Slik oppretter og bokfører du en salgsfaktura for prosjekt</span><span class="sxs-lookup"><span data-stu-id="659a4-113">To create and post a job sales invoice</span></span>
<span data-ttu-id="659a4-114">Du kan opprette en faktura for et prosjekt eller for én eller flere prosjektoppgaver for en kunde enten når arbeidet som skal faktureres, er fullført, eller når faktureringsdatoen som er basert på et faktureringsestimat, er nådd.</span><span class="sxs-lookup"><span data-stu-id="659a4-114">You can create an invoice for a job or for one or more job tasks for a customer when either the work to be invoiced is complete or the date for invoicing based on an invoicing schedule has been reached.</span></span>

<span data-ttu-id="659a4-115">Fra siden **Prosjekter** kan du fakturere en kunde ved å velge prosjektet, og deretter velge handlingen **Opprett salgsfaktura for prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="659a4-115">From the **Jobs** page, you can invoice a customer by selecting the job, and then choosing the **Create Job Sales Invoice** action.</span></span> <span data-ttu-id="659a4-116">Følgende fremgangsmåte viser hvordan du bruker en satsvis jobb til å fakturere flere prosjekter.</span><span class="sxs-lookup"><span data-stu-id="659a4-116">The following procedure shows how to use a batch job to invoice multiple jobs.</span></span>  

1. <span data-ttu-id="659a4-117">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Opprett salgsfaktura for prosjekt**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="659a4-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Create Sales Invoice**, and then choose the related link.</span></span>  
2. <span data-ttu-id="659a4-118">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="659a4-118">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="659a4-119">Angi filtre hvis du vil begrense prosjektene som kjørselen skal behandle.</span><span class="sxs-lookup"><span data-stu-id="659a4-119">Set filters if you want to limit the jobs that the batch job will process.</span></span>
4. <span data-ttu-id="659a4-120">Velg **OK** for å opprette fakturaene.</span><span class="sxs-lookup"><span data-stu-id="659a4-120">Choose the **OK** button to create the invoices.</span></span>  

## <a name="to-create-multiple-job-sales-invoices-from-job-planning-lines"></a><span data-ttu-id="659a4-121">Slik oppretter du flere prosjektsalgsfakturaer fra prosjektplanleggingslinjer</span><span class="sxs-lookup"><span data-stu-id="659a4-121">To create multiple job sales invoices from job planning lines</span></span>
<span data-ttu-id="659a4-122">Du kan opprette en faktura fra en prosjektplanleggingslinje og samtidig angi antallet for varen, ressursen eller finanskontoen som du vil fakturere.</span><span class="sxs-lookup"><span data-stu-id="659a4-122">You can create an invoice from a job planning lines, and indicate at that time the quantity of the item, resource, or general ledger account that you want to invoice.</span></span>

1. <span data-ttu-id="659a4-123">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Prosjekter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="659a4-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="659a4-124">Åpne et relevant prosjekt.</span><span class="sxs-lookup"><span data-stu-id="659a4-124">Open a relevant job.</span></span>
3. <span data-ttu-id="659a4-125">Velg en prosjektoppgave der feltet **Prosjektoppgavetype** inneholder **Bokføring**, og velg deretter handlingen **Prosjektplanleggingslinjer**.</span><span class="sxs-lookup"><span data-stu-id="659a4-125">Select a job task for which the **Job Task Type** field contains **Posting**, and then choose the **Job Planning Lines** action.</span></span>  
4. <span data-ttu-id="659a4-126">På en prosjektplanleggingslinjer, i feltet **Ant. som skal overføres til faktura** angir du antallet av varen, ressursen, finanskontotypen du vil fakturere.</span><span class="sxs-lookup"><span data-stu-id="659a4-126">On a job planning line, in the **Qty. To Transfer to Invoice** field, enter the quantity of the item, resource, general ledger account type that you want to invoice.</span></span>  
5. <span data-ttu-id="659a4-127">Velg handlingen **Opprett salgsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="659a4-127">Choose the **Create Sales Invoice** action.</span></span>
6. <span data-ttu-id="659a4-128">På siden **Opprett salgsfaktura for prosjekt** skriver du inn bokføringsdatoen og om du vil opprette en ny faktura eller føye til denne fakturaen til en eksisterende.</span><span class="sxs-lookup"><span data-stu-id="659a4-128">On the **Job Create Sales Invoice** page, enter the posting date and whether you want to create a new invoice or append this invoice to an existing one.</span></span>
7. <span data-ttu-id="659a4-129">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="659a4-129">Choose the **OK** button.</span></span>  

    <span data-ttu-id="659a4-130">Du kan se antallet i feltet **Ant. overført til faktura** på prosjektplanleggingslinjen.</span><span class="sxs-lookup"><span data-stu-id="659a4-130">On the job planning line, in the **Qty. Transferred to Invoice** field, you can see the quantity.</span></span>
8. <span data-ttu-id="659a4-131">På siden **Prosjektplanleggingslinjer** velger du handlingen **Salgsfakturaer/kreditnotaer**.</span><span class="sxs-lookup"><span data-stu-id="659a4-131">On the **Job Planning Lines** page, choose the **Sales Invoices/Credit Memos** action.</span></span>

    <span data-ttu-id="659a4-132">Siden **Salgsfaktura** åpnes og viser antallet du har overført til fakturaen.</span><span class="sxs-lookup"><span data-stu-id="659a4-132">The **Sales Invoice** page opens, showing the quantity that you have transferred to the invoice.</span></span>  
9. <span data-ttu-id="659a4-133">Gjør flere endringer, og velg deretter handlingen **Bokfør**.</span><span class="sxs-lookup"><span data-stu-id="659a4-133">Make any additional changes, and then choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="659a4-134">Fremgangsmåten ovenfor er identisk for å opprette, gå gjennom og bokføre en prosjektrelatert salgskreditnota.</span><span class="sxs-lookup"><span data-stu-id="659a4-134">The above procedure is similar for creating, reviewing, and posting a job-related sales credit memo.</span></span>

## <a name="to-calculate-and-post-job-completion-entries"></a><span data-ttu-id="659a4-135">Slik beregner og bokfører du prosjektferdiggjørelsesposter</span><span class="sxs-lookup"><span data-stu-id="659a4-135">To calculate and post job completion entries</span></span>
<span data-ttu-id="659a4-136">Når du har fullført alle aktiviteter for et prosjekt, inkludert bokføring og fakturering, må du oppdatere prosjektet for å sette **Status** til **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="659a4-136">When you have completed all activities for a job, including usage posting and invoicing, you must update the job to have a **Status** of **Completed**.</span></span> <span data-ttu-id="659a4-137">Deretter må du reversere alle VIA-er som er bokført i finans.</span><span class="sxs-lookup"><span data-stu-id="659a4-137">Then, you must reverse any WIP that has been posted to the general ledger.</span></span>

1. <span data-ttu-id="659a4-138">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Prosjekter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="659a4-138">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="659a4-139">Merk et åpent prosjekt, og velg handlingen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="659a4-139">Select an open job, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="659a4-140">I feltet **Status** velger du **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="659a4-140">In the **Status** field, select **Completed**.</span></span>
4. <span data-ttu-id="659a4-141">Følg hjelpetrinnene for å beregne og bokføre VIA.</span><span class="sxs-lookup"><span data-stu-id="659a4-141">Follow the assistance steps to calculate and post WIP.</span></span> <span data-ttu-id="659a4-142">Alternativt følger du trinn 5 og 6 hvis du vil gjøre dette manuelt.</span><span class="sxs-lookup"><span data-stu-id="659a4-142">Alternatively, follows steps 5 and 6 to do so manually.</span></span>  
5. <span data-ttu-id="659a4-143">Velg handlingen **Beregn VIA**.</span><span class="sxs-lookup"><span data-stu-id="659a4-143">Choose the **Calculate WIP** action.</span></span>
6. <span data-ttu-id="659a4-144">På siden **Beregn VIA for prosjekt** fyller du ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="659a4-144">On the **Job Calculate WIP** page, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="659a4-145">VIA-postene for prosjekt du oppretter ved å kjøre kjørselen, vil ha en avmerking i **Prosjekt ferdig**-boksen for å angi at de er ferdiggjørelsesposter.</span><span class="sxs-lookup"><span data-stu-id="659a4-145">The job WIP entries created by running the batch job will have the **Job Complete** check box selected to show that they are completion entries.</span></span>  
7. <span data-ttu-id="659a4-146">Velg handlingen **Bokfør VIA i Finans for prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="659a4-146">Choose the **Job Post WIP to G/L** action.</span></span>
8. <span data-ttu-id="659a4-147">Fyll ut feltene etter behov på siden **Bokfør VIA i Finans for prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="659a4-147">On the **Job Post WIP to G/L** page, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="659a4-148">VIA-finanspostene for prosjekt som du oppretter ved å kjøre kjørselen, vil ha en avmerking i **Prosjekt ferdig**-boksen for å angi at de er ferdiggjørelsesposter.</span><span class="sxs-lookup"><span data-stu-id="659a4-148">The job WIP general ledger entries created by running the batch job will have the **Job Complete** check box selected to show they are completion entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="659a4-149">Se også</span><span class="sxs-lookup"><span data-stu-id="659a4-149">See Also</span></span>
[<span data-ttu-id="659a4-150">Administrere prosjekter</span><span class="sxs-lookup"><span data-stu-id="659a4-150">Managing Projects</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="659a4-151">Finans</span><span class="sxs-lookup"><span data-stu-id="659a4-151">Finance</span></span>](finance.md)  
<span data-ttu-id="659a4-152">[Innkjøp](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="659a4-152">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="659a4-153">[Salg](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="659a4-153">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="659a4-154">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="659a4-154">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
