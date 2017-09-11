---
title: Rapportering av 1099-transaksjoner i USA | Microsoft-dokumentasjon
description: "IRS krever skjemaet 1099-avgiftsskjemaet for betalinger til leverandører, og du kan angi at et kjøpsdokument er 1099-pliktig, og angi 1099-koden for leverandøren."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c20c52927aa979e56aeef7975fbcee1564ca4dd7
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2017

---
# <a name="reporting-transactions-as-1099-liable-in-the-us"></a><span data-ttu-id="b3fe1-103">Rapportere transaksjoner som 1099-pliktige i USA</span><span class="sxs-lookup"><span data-stu-id="b3fe1-103">Reporting Transactions as 1099 Liable in the US</span></span>

<span data-ttu-id="b3fe1-104">IRS (Internal Revenue Service) krever én eller flere versjoner av 1099-avgiftsskjemaet for betalinger til leverandører.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-104">The Internal Revenue Service (IRS) requires one or more versions of the 1099 tax form for payments to vendors.</span></span> <span data-ttu-id="b3fe1-105">Kopier av disse skjemaene må sendes til leverandører årlig på eller før den siste dagen i januar.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-105">Copies of these forms must be sent to vendors annually on or before the last day of January.</span></span> <span data-ttu-id="b3fe1-106">På kjøpsdokumentene kan du angi at dokumentet er 1099-pliktig, og du kan angi 1099-koden for leverandøren.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-106">On your purchase documents, you can specify that the document is 1099 liable, and you can specify the 1099 code for the vendor.</span></span>  

## <a name="1099-codes"></a><span data-ttu-id="b3fe1-107">1099-koder</span><span class="sxs-lookup"><span data-stu-id="b3fe1-107">1099 codes</span></span>
<span data-ttu-id="b3fe1-108">I [!INCLUDE[d365fin](includes/d365fin_md.md)] er de vanligste 1099-kodene allerede definert for deg, slik at du er klar til å generere nødvendige rapporter.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-108">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the most common 1099 codes are already set up for you so you are ready to generate the required reports.</span></span> <span data-ttu-id="b3fe1-109">Kodene er definert i vinduet **IRS 1099-skjemafelt** der du også kan legge til nye 1099-koder.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-109">The codes are defined in the **IRS 1099 Form Box** window where you can also add new 1099 codes.</span></span> <span data-ttu-id="b3fe1-110">For hver avgiftspliktige leverandør kan du deretter angi den aktuelle 1099-koden på i hurtigfanen **Betalinger** på leverandørkortet.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-110">For each tax liable vendor, you can then specify the relevant 1099 code on the **Payments** FastTab on the Vendor card.</span></span>  

<span data-ttu-id="b3fe1-111">Med rapporten **1099-informasjon for leverandør** kan du se gjennom 1099-transaksjoner betalt i løpet av en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-111">With the **Vendor 1099 Information** report, you can review 1099 transactions paid during a specified period.</span></span> <span data-ttu-id="b3fe1-112">På slutten av året kan du skrive ut 1099-transaksjoner på forhåndstrykte skjemaer.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-112">At the end of the year, you can print 1099 transactions on preprinted forms.</span></span>  

## <a name="printing-1099-tax-forms"></a><span data-ttu-id="b3fe1-113">Skriver ut 1099-avgiftsskjemaer</span><span class="sxs-lookup"><span data-stu-id="b3fe1-113">Printing 1099 tax forms</span></span>
<span data-ttu-id="b3fe1-114">Fra den **IRS 1099-skjemaet for** -vinduet, kan du gå til følgende mva-skjemaer:</span><span class="sxs-lookup"><span data-stu-id="b3fe1-114">From the **IRS 1099 Form Box** window, you can access the following tax forms:</span></span>  

* <span data-ttu-id="b3fe1-115">1099-DIV for leverandør</span><span class="sxs-lookup"><span data-stu-id="b3fe1-115">Vendor 1099 Div</span></span>  

  <span data-ttu-id="b3fe1-116">Skriver ut det føderale skjemaet 1099-DIV for utbytte og distribusjon.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-116">Prints the federal form 1099-DIV for dividends and distribution.</span></span> <span data-ttu-id="b3fe1-117">Du kan skrive ut alle eller bestemte 1099-DIV-skjemaer.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-117">You can print all or specific 1099-DIV forms.</span></span> <span data-ttu-id="b3fe1-118">Rapporten bruker kodene som gjelder for beløpsfeltene for DIV-skjemaet fra vinduet **IRS 1099-skjemafelt**.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-118">The report uses the codes that apply to the DIV form amount boxes from the **IRS 1099 Form-Box** window.</span></span>  
* <span data-ttu-id="b3fe1-119">1099-INT for leverandør</span><span class="sxs-lookup"><span data-stu-id="b3fe1-119">Vendor 1099 Int</span></span>  

  <span data-ttu-id="b3fe1-120">Skriver ut det føderale skjemaet 1099-INT for finansinntekter.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-120">Prints the federal form 1099-INT for interest income.</span></span> <span data-ttu-id="b3fe1-121">Du kan skrive ut alle eller bestemte 1099-INT-skjemaer.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-121">You can print all or specific 1099-INT forms.</span></span> <span data-ttu-id="b3fe1-122">Rapporten bruker kodene som gjelder for beløpsfeltene for INT-skjemaet fra vinduet **IRS 1099-skjemafelt**.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-122">The report uses the codes that apply to the INT form amount boxes from the **IRS 1099 Form-Box** window.</span></span>  
* <span data-ttu-id="b3fe1-123">1099-MISC for leverandør – diverse inntekter</span><span class="sxs-lookup"><span data-stu-id="b3fe1-123">Vendor 1099 Misc - Miscellaneous income</span></span>  

  <span data-ttu-id="b3fe1-124">Skriver ut det føderale skjemaet 1099-MISC for diverse inntekter.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-124">Prints the federal form 1099-MISC for miscellaneous income.</span></span> <span data-ttu-id="b3fe1-125">Du kan skrive ut alle eller bestemte 1099-MISC-skjemaer.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-125">You can print all or specific 1099-MISC forms.</span></span> <span data-ttu-id="b3fe1-126">Rapporten bruker kodene som gjelder for beløpsfeltene for MISC-skjemaet fra vinduet **IRS 1099-skjemafelt**.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-126">The report uses the codes that apply to the MISC form amount boxes from the **IRS 1099 Form-Box** window.</span></span>  

<span data-ttu-id="b3fe1-127">Forskriftsmessige endringer som påvirker denne rapporten og tabelldataene håndteres vanligvis under oppdateringer på slutten av året.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-127">Regulatory changes affecting this report and the table data are generally handled in end-of-year updates.</span></span>
<span data-ttu-id="b3fe1-128">Det kan være nyttig å kjøre rapporten **1099-informasjon for leverandør** for å se gjennom dataene før du skriver ut skjemaene.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-128">It may be helpful to run the **Vendor 1099 Information** report to review the data before printing the forms.</span></span>

## <a name="submitting-1099-tax-forms-electronically"></a><span data-ttu-id="b3fe1-129">Innsending av 1099-avgiftsskjemaer elektronisk</span><span class="sxs-lookup"><span data-stu-id="b3fe1-129">Submitting 1099 tax forms electronically</span></span>
<span data-ttu-id="b3fe1-130">Hvis du vil sende 1099-avgiftsskjemaene elektronisk, kan du bruke rapporten **Magnetiske 1099-data for leverandør**.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-130">To submit the 1099 tax forms electronically, use the **Vendor 1099 Magnetic Media** report.</span></span> <span data-ttu-id="b3fe1-131">Angir 1099-skjemaene som kan eksporteres.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-131">Specifies the 1099 forms that can be exported.</span></span> <span data-ttu-id="b3fe1-132">Skjemainformasjonen som eksporteres av denne rapporten, er den samme som rapportene som skriver ut 1099-skjemaer som er beskrevet i det forrige avsnittet.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-132">The form information exported by this report is the same as the reports that print 1099 forms that are described in the previous section.</span></span>  

<span data-ttu-id="b3fe1-133">Rapporten bruker kodene som gjelder for beløpsfeltene for skjemaet fra vinduet **IRS 1099-skjemafelt**.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-133">The report uses the codes that apply to the form amount boxes from the **IRS 1099 Form-Box** window.</span></span> <span data-ttu-id="b3fe1-134">Kodene er tilordnet til skjemafeltene i filoppsettene for denne rapporten, og tabelldataene og rapportversjonen for et bestemt avgiftsår må derfor samsvare.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-134">The codes are mapped to the form boxes in the file layouts of this report, therefore the table data and report version for a particular tax year must be in agreement.</span></span> <span data-ttu-id="b3fe1-135">Hvis eventuelle egendefinerte koder er lagt til i tabellen, må disse tilordnes skjemafeltene i dette objektet.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-135">If any custom codes are added to the table these must be mapped to the form boxes inside this object.</span></span>  

<span data-ttu-id="b3fe1-136">Forskriftsmessige endringer som påvirker denne rapporten og tabelldataene håndteres vanligvis under oppdateringer på slutten av året.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-136">Regulatory changes affecting this report and the table data are generally handled in end-of-year updates.</span></span>
<span data-ttu-id="b3fe1-137">Det kan være nyttig å kjøre rapporten **1099-informasjon for leverandør** for å se gjennom dataene før du genererer den elektroniske filen.</span><span class="sxs-lookup"><span data-stu-id="b3fe1-137">It may be helpful to run the **Vendor 1099 Information** report to review the data before generating the electronic file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b3fe1-138">Se også</span><span class="sxs-lookup"><span data-stu-id="b3fe1-138">See Also</span></span>
[<span data-ttu-id="b3fe1-139">Registrere nye leverandører</span><span class="sxs-lookup"><span data-stu-id="b3fe1-139">How to: Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
[<span data-ttu-id="b3fe1-140">Registrere kjøp</span><span class="sxs-lookup"><span data-stu-id="b3fe1-140">How to: Record Purchase</span></span>](purchasing-how-record-purchases.md)  
<span data-ttu-id="b3fe1-141">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b3fe1-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

