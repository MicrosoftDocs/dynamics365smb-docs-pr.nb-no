---
title: "Definere og bruke standardlinjer for gjentakende salg og kjøp | Microsoft-dokumentasjon"
description: "Du kan definere salgslinjer og kjøpslinjer du ofte lager, og deretter sette dem inn i salgs- og kjøpsdokumenter for å fylle ut linjene raskt med standardinformasjon."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7c5820db4d8aa65ddeddfd5ee27f0a7e89100abf
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="create-recurring-sales-and-purchase-lines"></a><span data-ttu-id="3253a-103">Opprette gjentakende salgs- og kjøpslinjer</span><span class="sxs-lookup"><span data-stu-id="3253a-103">Create Recurring Sales and Purchase Lines</span></span>
<span data-ttu-id="3253a-104">Hvis du ofte må opprette salgs- og kjøpslinjer med lignende informasjon, kan du definere standardlinjer du deretter kan sette inn på gjentakende salgs- og kjøpsdokumenter, for eksempel for gjentakende etterfyllingsordrer.</span><span class="sxs-lookup"><span data-stu-id="3253a-104">If you often need to create sales and purchase lines with similar information, you can set up standard lines that you can then insert on recurring sales and purchase documents, for example, for recurring replenishment orders.</span></span>  

<span data-ttu-id="3253a-105">Fremgangsmåten nedenfor viser hvordan du arbeider med standardlinjer.</span><span class="sxs-lookup"><span data-stu-id="3253a-105">The following procedure shows how to work with standard sales lines.</span></span> <span data-ttu-id="3253a-106">Det fungerer på en lignende måte som for standard kjøpslinjer.</span><span class="sxs-lookup"><span data-stu-id="3253a-106">It works in a similar way for standard purchase lines.</span></span>  

## <a name="to-set-up-standard-sales-lines"></a><span data-ttu-id="3253a-107">Definere standard salgslinjer</span><span class="sxs-lookup"><span data-stu-id="3253a-107">To set up standard sales lines</span></span>  
1. <span data-ttu-id="3253a-108">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Standard salgskoder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="3253a-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Standard Sales Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3253a-109">I vinduet **Standard salgslinjer** velger du handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="3253a-109">In the **Standard Sales Lines** window, choose the **New** action.</span></span>  
3. <span data-ttu-id="3253a-110">Fyll ut feltene i hurtigfanen **Generelt** etter behov.</span><span class="sxs-lookup"><span data-stu-id="3253a-110">On the **General** FastTab, fill the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="3253a-111">I hurtigfanen **Linjer** angir du informasjon i feltene for å klargjøre salgslinjer som gjenspeiler standardlinjene du forventer å bruke som gjentakende linjer i salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="3253a-111">On the **Lines** FastTab, enter information in the fields to prepare sales lines that reflect the standard lines that you expect to use as recurring lines on sales documents.</span></span>  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a><span data-ttu-id="3253a-112">Sette inn standard salgslinjer på en salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="3253a-112">To insert standard sales lines on a sales invoice</span></span>
1. <span data-ttu-id="3253a-113">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Fakturaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="3253a-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="3253a-114">Åpne salgsfakturaen du vil sette inn én eller flere standard salgslinjer på.</span><span class="sxs-lookup"><span data-stu-id="3253a-114">Open the sales invoice that you want to insert one or more standard sales lines on.</span></span>
3. <span data-ttu-id="3253a-115">Velg handlingen **Hent gjentakende salgslinjer**.</span><span class="sxs-lookup"><span data-stu-id="3253a-115">Choose the **Get Recurring Sales Lines** action.</span></span>
4. <span data-ttu-id="3253a-116">I vinduet **Gjentakende salgslinjer** velger du oppslagsknappen i **Kode**-feltet, og deretter velger du et sett med standard salgslinjer.</span><span class="sxs-lookup"><span data-stu-id="3253a-116">In the **Recurring Sales Lines** window, choose the lookup button in the **Code** field, and then select a set of standard sales lines.</span></span>
5. <span data-ttu-id="3253a-117">Velg **OK** for å sette inn de standard salgslinjene på fakturaen, der du kan bruke informasjonen på nytt som den er eller redigere den.</span><span class="sxs-lookup"><span data-stu-id="3253a-117">Choose the **OK** button to insert the standard sales lines on the invoice, where you can reuse as is or edit the information.</span></span>

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a><span data-ttu-id="3253a-118">Opprette flere salgsfakturaer basert på standard salgslinjer</span><span class="sxs-lookup"><span data-stu-id="3253a-118">To create multiple sales invoices based on standard sales lines</span></span>
<span data-ttu-id="3253a-119">Du kan bruke kjørselen **Opprett gjentak. salgsfakt.** til å opprette salgsfakturaer i henhold til standard salgslinjer som er tilordnet til kundene, og med bokføringsdatoer innenfor gyldig-fra- og gyldig til-datoer du angir i standardsalgskoden.</span><span class="sxs-lookup"><span data-stu-id="3253a-119">You can use the **Create Recurring Sales Inv.** batch job to create sales invoices according to standard sales lines that are assigned to the customers and with posting dates within the valid-from and valid-to dates that you specify on the standard sales code.</span></span>

<span data-ttu-id="3253a-120">I vinduet **Gjentakende salgslinjer** kan du også angi en Direct Debit-betalingsmåte og en Direct Debit-belastningsfullmakt.</span><span class="sxs-lookup"><span data-stu-id="3253a-120">In the **Recurring Sales Lines** window, you can also specify a direct-debit payment method and a direct-debit mandate.</span></span> <span data-ttu-id="3253a-121">Salgsfakturaene som er opprettet med den satsvise jobben **Opprett gjentak. salgsfakt.**, vil dermed inneholde informasjon som kreves for å kreve inn betaling for salgsfakturaer med SEPA direct debit.</span><span class="sxs-lookup"><span data-stu-id="3253a-121">The sales invoices that are created with the **Create Recurring Sales Inv.** batch job will then include information required to collect payment for the sales invoices with SEPA direct debit.</span></span> <span data-ttu-id="3253a-122">Hvis du vil ha mer informasjon, kan du se [Innkreve betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md).</span><span class="sxs-lookup"><span data-stu-id="3253a-122">For more information, see [Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md).</span></span>

1. <span data-ttu-id="3253a-123">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Opprett gjentakende salgsfakturaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="3253a-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Create Recurring Sales Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="3253a-124">Fyll ut feltene i vinduet **Opprett gjentak. salgsfakt.** etter behov.</span><span class="sxs-lookup"><span data-stu-id="3253a-124">In the **Create Recurring Sales Inv.** window, fill in the fields as necessary.</span></span>
3. <span data-ttu-id="3253a-125">I vinduet **Kode** angir du koden for standard salgslinjer som er tilordnet en kunde du vil opprette salgsfakturaer for.</span><span class="sxs-lookup"><span data-stu-id="3253a-125">In the **Code** field, enter the code for standard sales lines assigned to a customer that you want to create sales invoices for.</span></span>
4. <span data-ttu-id="3253a-126">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3253a-126">Choose the **OK** button.</span></span>

<span data-ttu-id="3253a-127">Salgsfakturaer blir opprettet for kunder med angitt standard kundesalgskode og eventuell angitt avtalegiroinformasjon, for bokføring på den angitte datoen.</span><span class="sxs-lookup"><span data-stu-id="3253a-127">Sales invoices are created for the customers with the specified standard customer sales code, and any specified direct-debit information, for posting on the specified date.</span></span>

## <a name="see-also"></a><span data-ttu-id="3253a-128">Se også</span><span class="sxs-lookup"><span data-stu-id="3253a-128">See Also</span></span>  
[<span data-ttu-id="3253a-129">Salg</span><span class="sxs-lookup"><span data-stu-id="3253a-129">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="3253a-130">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3253a-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

