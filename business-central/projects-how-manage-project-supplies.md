---
title: "Kjøpe varer eller tjenester for et prosjekt og administrere forsyninger | Microsoft-dokumentasjon"
description: "Beskriver hvordan du administrerer forsyninger og innkjøp av materialer og tjenester for prosjekter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, material, purchase
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 95e2a1938585f1ce68e8c1ae51b8a85596fe44e5
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="manage-job-supplies"></a><span data-ttu-id="73689-103">Administrere prosjektforsyninger</span><span class="sxs-lookup"><span data-stu-id="73689-103">Manage Job Supplies</span></span>
<span data-ttu-id="73689-104">Behandling av prosjektforsyninger som varer, tjenester og utgifter inngår i og er en viktig del av alle prosjektutførelser.</span><span class="sxs-lookup"><span data-stu-id="73689-104">Managing project supplies of items, services, and expenses is an integral and critical aspect of the execution of all jobs.</span></span> <span data-ttu-id="73689-105">Du kan bruke lagerantallene eller foreta prosjektspesifikke kjøp ved hjelp av bestillinger eller kjøpsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="73689-105">You can use inventory quantities or make job-specific purchases using purchase orders or purchase invoices.</span></span> <span data-ttu-id="73689-106">En servicejobb på en datamaskin krever for eksempel en ny disk.</span><span class="sxs-lookup"><span data-stu-id="73689-106">For example, a service job on a computer requires a new disk.</span></span> <span data-ttu-id="73689-107">Du oppretter en kjøpsfaktura for å kjøpe en ny disk, og registrerer prosjektet den skal brukes på.</span><span class="sxs-lookup"><span data-stu-id="73689-107">You create a purchase invoice to buy a new disk and record the job that it will be used on.</span></span>

<span data-ttu-id="73689-108">Hvis kjøpsprosessen ikke krever at den fysiske transaksjonen registreres separat, kan et kjøp behandles i vinduet **Finanskladd for prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="73689-108">If the purchase process does not require that the physical transaction be recorded separately, then a purchase may be processed in the **Job G/L Journal** window.</span></span> <span data-ttu-id="73689-109">Hvis du vil ha mer informasjon, kan du se [Registrere forbruk for prosjekter](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="73689-109">For more information, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

## <a name="to-purchase-items-or-services-for-a-job"></a><span data-ttu-id="73689-110">Slik kjøper du varer eller tjenester for et prosjekt</span><span class="sxs-lookup"><span data-stu-id="73689-110">To purchase items or services for a job</span></span>
<span data-ttu-id="73689-111">Følgende fremgangsmåte viser hvordan du bruker en kjøpsfaktura til å kjøpe produkter for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="73689-111">The following procedure shows how to use a purchase invoice to purchase products for a job.</span></span> <span data-ttu-id="73689-112">Bruk samme fremgangsmåte når du bruker en bestilling.</span><span class="sxs-lookup"><span data-stu-id="73689-112">The same steps apply when using a purchase order.</span></span>  

1. <span data-ttu-id="73689-113">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="73689-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="73689-114">Velg handlingen **Ny** og fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="73689-114">Choose the **New** action and fill in the fields as necessary.</span></span> <span data-ttu-id="73689-115">Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="73689-115">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
3. <span data-ttu-id="73689-116">I feltene **Prosjektnr.** og **Prosjektoppgavenr.** velger du informasjonen på prosjektet som du vil kjøpe varer eller tjenester for.</span><span class="sxs-lookup"><span data-stu-id="73689-116">In the **Job No.** and **Job Task No.** fields, select the information of the job that you want to purchase items or services for.</span></span> <span data-ttu-id="73689-117">Bruk funksjonen **Velg kolonner** hvis feltet ikke er synlig.</span><span class="sxs-lookup"><span data-stu-id="73689-117">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="73689-118">Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet ](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="73689-118">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>

    <span data-ttu-id="73689-119">Verdien du velger i feltet **Prosjektlinjetype**, definerer om en planleggingslinje blir opprettet når du bokfører forbruket for varen.</span><span class="sxs-lookup"><span data-stu-id="73689-119">The value that you select in the **Job Line Type** field defines whether a planning line is created when you post the usage of the item.</span></span> <span data-ttu-id="73689-120">Hvis feltet inneholder **Fakturerbar**, opprettes det prosjektplanleggingslinjer som er klare for å faktureres kunden.</span><span class="sxs-lookup"><span data-stu-id="73689-120">If the field contains **Billable**, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="73689-121">Hvis du vil ha mer informasjon, kan du se [Fakturere prosjekter](projects-how-invoice-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="73689-121">For more information, see [Invoice Jobs](projects-how-invoice-jobs.md).</span></span>
4. <span data-ttu-id="73689-122">Velg handlingen **Bokfør**.</span><span class="sxs-lookup"><span data-stu-id="73689-122">Choose the **Post** action.</span></span>

## <a name="to-view-the-value-of-purchases-for-a-job"></a><span data-ttu-id="73689-123">Slik viser du verdien av kjøp for et prosjekt</span><span class="sxs-lookup"><span data-stu-id="73689-123">To view the value of purchases for a job</span></span>
1. <span data-ttu-id="73689-124">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Jobber**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="73689-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="73689-125">Åpne et aktuelt prosjektkort.</span><span class="sxs-lookup"><span data-stu-id="73689-125">Open a relevant job card.</span></span>

    <span data-ttu-id="73689-126">På hurtigfanen **Oppgaver** viser feltet **Utestående bestillinger** det totale utestående beløpet, i lokal valuta, for lagervarer og tjenester i kjøpsdokumenter for prosjektoppgavelinjen.</span><span class="sxs-lookup"><span data-stu-id="73689-126">On the **Tasks** FastTab, the **Outstanding Orders** field shows the total outstanding amount, in local currency, of inventory items and services on purchase documents for the job task line.</span></span>  

    <span data-ttu-id="73689-127">Feltet **Mottatt, ikke fakturert (beløp)** viser verdien for varer som er levert i kjøpsdokumenter, men som ennå ikke er fakturert.</span><span class="sxs-lookup"><span data-stu-id="73689-127">The **Amt. Rec. Not Invoiced** field shows the value of items delivered on purchase documents, but not yet invoiced.</span></span>  
3. <span data-ttu-id="73689-128">Velg enten feltene for å åpne vinduet **Bestillingslinjer**, der du kan gå gjennom informasjon om de relaterte kjøpsdokumentlinjene, inkludert hvilke varer eller tjenester som er mottatt.</span><span class="sxs-lookup"><span data-stu-id="73689-128">Choose either of the fields to open the **Purchase Lines** window where you can review information about the related purchase document lines, including which items or services have been received.</span></span>

## <a name="to-post-a-job-related-expense"></a><span data-ttu-id="73689-129">Slik bokfører du en prosjektrelatert utgift</span><span class="sxs-lookup"><span data-stu-id="73689-129">To post a job-related expense</span></span>
<span data-ttu-id="73689-130">Hvis du pådrar deg ekstraordinære eller enkeltstående prosjektutgifter, kan du bruke vinduet **Finanskladd for prosjekt** til å bokføre dem direkte til den aktuelle prosjektkontoen.</span><span class="sxs-lookup"><span data-stu-id="73689-130">If you incur extraordinary or one-time job expenses, you can use the **Job G/L Journal** window to post them directly to the relevant job account.</span></span>

1. <span data-ttu-id="73689-131">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finanskladder for prosjekt**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="73689-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="73689-132">Opprett en ny linje, og skriv inn informasjon om utgiften, inkludert informasjon i feltene **Prosjektnr.** og **Prosjektoppgavenr.**</span><span class="sxs-lookup"><span data-stu-id="73689-132">Create a new line and enter information about the expense, including information in the **Job No.** and **Job Task No** fields.</span></span>  
3. <span data-ttu-id="73689-133">Når kladden er fullført, kan du velge handlingen **Bokfør**.</span><span class="sxs-lookup"><span data-stu-id="73689-133">When the journal is complete, choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="73689-134">Se også</span><span class="sxs-lookup"><span data-stu-id="73689-134">See Also</span></span>
[<span data-ttu-id="73689-135">Prosjektstyring</span><span class="sxs-lookup"><span data-stu-id="73689-135">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="73689-136">Finans</span><span class="sxs-lookup"><span data-stu-id="73689-136">Finance</span></span>](finance.md)  
<span data-ttu-id="73689-137">[Innkjøp](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="73689-137">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="73689-138">[Salg](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="73689-138">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="73689-139">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="73689-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

