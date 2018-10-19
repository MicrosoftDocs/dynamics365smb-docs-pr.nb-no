---
title: "Definere standardlinjer for gjentakende salg og kjøp | Microsoft-dokumentasjon"
description: "Du kan definere salgslinjer og kjøpslinjer du ofte lager, og deretter sette dem inn i salgs- og kjøpsdokumenter for å fylle ut linjene raskt med standardinformasjon."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: df4f093ded0a55d45c40be15c5888035d6e3b2df
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="create-recurring-sales-and-purchase-lines"></a><span data-ttu-id="6847d-103">Opprette gjentakende salgs- og kjøpslinjer</span><span class="sxs-lookup"><span data-stu-id="6847d-103">Create Recurring Sales and Purchase Lines</span></span>
<span data-ttu-id="6847d-104">Hvis du ofte må opprette salgs- og kjøpslinjer med lignende informasjon, kan du definere standardlinjer du deretter kan sette inn på gjentakende salgs- og kjøpsdokumenter, for eksempel for gjentakende etterfyllingsordrer.</span><span class="sxs-lookup"><span data-stu-id="6847d-104">If you often need to create sales and purchase lines with similar information, you can set up standard lines that you can then insert on recurring sales and purchase documents, for example, for recurring replenishment orders.</span></span>  

<span data-ttu-id="6847d-105">Fremgangsmåten nedenfor viser hvordan du arbeider med standardlinjer.</span><span class="sxs-lookup"><span data-stu-id="6847d-105">The following procedure shows how to work with standard sales lines.</span></span> <span data-ttu-id="6847d-106">Det fungerer på en lignende måte som for standard kjøpslinjer.</span><span class="sxs-lookup"><span data-stu-id="6847d-106">It works in a similar way for standard purchase lines.</span></span>  

## <a name="to-set-up-standard-sales-lines"></a><span data-ttu-id="6847d-107">Definere standard salgslinjer</span><span class="sxs-lookup"><span data-stu-id="6847d-107">To set up standard sales lines</span></span>  
1. <span data-ttu-id="6847d-108">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Standard salgslinjer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="6847d-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Standard Sales Lines**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6847d-109">I vinduet **Standard salgslinjer** velger du handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6847d-109">In the **Standard Sales Lines** window, choose the **New** action.</span></span>  
3. <span data-ttu-id="6847d-110">Fyll ut feltene i hurtigfanen **Generelt** etter behov.</span><span class="sxs-lookup"><span data-stu-id="6847d-110">On the **General** FastTab, fill the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="6847d-111">I hurtigfanen **Linjer** angir du informasjon i feltene for å klargjøre salgslinjer som gjenspeiler standardlinjene du forventer å bruke som gjentakende linjer i salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="6847d-111">On the **Lines** FastTab, enter information in the fields to prepare sales lines that reflect the standard lines that you expect to use as recurring lines on sales documents.</span></span>  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a><span data-ttu-id="6847d-112">Sette inn standard salgslinjer på en salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="6847d-112">To insert standard sales lines on a sales invoice</span></span>
1. <span data-ttu-id="6847d-113">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Fakturaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="6847d-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="6847d-114">Åpne salgsfakturaen du vil sette inn én eller flere standard salgslinjer på.</span><span class="sxs-lookup"><span data-stu-id="6847d-114">Open the sales invoice that you want to insert one or more standard sales lines on.</span></span>
3. <span data-ttu-id="6847d-115">Velg handlingen **Hent gjentakende salgslinjer**.</span><span class="sxs-lookup"><span data-stu-id="6847d-115">Choose the **Get Recurring Sales Lines** action.</span></span>
4. <span data-ttu-id="6847d-116">I vinduet **Gjentakende salgslinjer** velger du oppslagsknappen i **Kode**-feltet, og deretter velger du et sett med standard salgslinjer.</span><span class="sxs-lookup"><span data-stu-id="6847d-116">In the **Recurring Sales Lines** window, choose the lookup button in the **Code** field, and then select a set of standard sales lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6847d-117">For å bruke settet med gjentakende salgslinjer sammen med kjørselen **Opprett gjentakende salgsfakturaer** må du også fylle ut feltene **Gyldig fra-dato** og **Gyldig til-dato** i vinduet **Gjentakende salgslinjer**.</span><span class="sxs-lookup"><span data-stu-id="6847d-117">To use the recurring sales lines set together with the **Create Recurring Sales Invoices** batch job, you must also fill in the **Valid From Date** and **Valid To Date** fields in the **Recurring Sales Lines** window.</span></span> <span data-ttu-id="6847d-118">Hvis du vil ha mer informasjon, kan du se delen "Opprette flere salgsfakturaer basert på standard salgskoder".</span><span class="sxs-lookup"><span data-stu-id="6847d-118">For more information, see the "To create multiple sales invoices based on standard sales lines" section.</span></span>

5. <span data-ttu-id="6847d-119">Velg **OK** for å sette inn de standard salgslinjene på fakturaen, der du kan bruke informasjonen på nytt som den er eller redigere den.</span><span class="sxs-lookup"><span data-stu-id="6847d-119">Choose the **OK** button to insert the standard sales lines on the invoice where you can reuse them as is or edit the information.</span></span>

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a><span data-ttu-id="6847d-120">Opprette flere salgsfakturaer basert på standard salgslinjer</span><span class="sxs-lookup"><span data-stu-id="6847d-120">To create multiple sales invoices based on standard sales lines</span></span>
<span data-ttu-id="6847d-121">Du kan bruke kjørselen **Opprett gjentakende salgsfakturaer** til å opprette salgsfakturaer i henhold til standard salgslinjer som er tilordnet til kundene, og med bokføringsdatoer innenfor gyldig-fra- og gyldig til-datoer du angir på standardsalgslinjene.</span><span class="sxs-lookup"><span data-stu-id="6847d-121">You can use the **Create Recurring Sales Invoices** batch job to create sales invoices according to standard sales lines that are assigned to the customers and with posting dates within the valid-from and valid-to dates that you specify on the standard sales lines.</span></span>

> [!NOTE]
> <span data-ttu-id="6847d-122">I vinduet **Gjentakende salgslinjer** kan du også angi en Direct Debit-betalingsmåte og en Direct Debit-belastningsfullmakt.</span><span class="sxs-lookup"><span data-stu-id="6847d-122">In the **Recurring Sales Lines** window, you can also specify a direct-debit payment method and a direct-debit mandate.</span></span> <span data-ttu-id="6847d-123">Salgsfakturaene som er opprettet med den satsvise jobben **Opprett gjentak. salgsfakt.**, vil dermed inneholde informasjon som kreves for å kreve inn betaling for salgsfakturaer med SEPA direct debit.</span><span class="sxs-lookup"><span data-stu-id="6847d-123">The sales invoices that are created with the **Create Recurring Sales Inv.** batch job will then include information required to collect payment for the sales invoices with SEPA direct debit.</span></span> <span data-ttu-id="6847d-124">Hvis du vil ha mer informasjon, kan du se [Innkreve betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md).</span><span class="sxs-lookup"><span data-stu-id="6847d-124">For more information, see [Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md).</span></span>

1. <span data-ttu-id="6847d-125">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Opprett gjentakende salgsfakturaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="6847d-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Create Recurring Sales Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="6847d-126">Fyll ut feltene i vinduet **Opprett gjentakende salgsfakturaer** etter behov.</span><span class="sxs-lookup"><span data-stu-id="6847d-126">In the **Create Recurring Sales Invoices** window, fill in the fields as necessary.</span></span>
3. <span data-ttu-id="6847d-127">I filterfeltet **Kode** angir du koden for standard salgslinjer som er tilordnet en kunde du vil opprette salgsfakturaer for.</span><span class="sxs-lookup"><span data-stu-id="6847d-127">In the **Code** filter field, enter the code for standard sales lines that are assigned to a customer that you want to create sales invoices for.</span></span>
4. <span data-ttu-id="6847d-128">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6847d-128">Choose the **OK** button.</span></span>

<span data-ttu-id="6847d-129">Salgsfakturaer blir opprettet for kunder med angitt standard kundesalgskode og eventuell angitt avtalegiroinformasjon, for bokføring på den angitte datoen.</span><span class="sxs-lookup"><span data-stu-id="6847d-129">Sales invoices are created for the customers with the specified standard customer sales code, and any specified direct-debit information, for posting on the specified date.</span></span>

## <a name="see-also"></a><span data-ttu-id="6847d-130">Se også</span><span class="sxs-lookup"><span data-stu-id="6847d-130">See Also</span></span>  
[<span data-ttu-id="6847d-131">Salg</span><span class="sxs-lookup"><span data-stu-id="6847d-131">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="6847d-132">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6847d-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

