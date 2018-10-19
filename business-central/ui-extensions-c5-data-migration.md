---
title: "Bruke C5-utvidelse for dataoverføring | Microsoft-dokumentasjon"
description: "Bruk denne utvidelsen til å overføre kunder, leverandører, varer og finanskonti fra Microsoft Dynamics C5 2012 til Business Central."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: a10c05116e97cdf000bd46258a9d67f4c9910c90
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---

# <a name="the-c5-data-migration-extension"></a><span data-ttu-id="5edee-103">Utvidelsen C5-datamigrering</span><span class="sxs-lookup"><span data-stu-id="5edee-103">The C5 Data Migration Extension</span></span>
<span data-ttu-id="5edee-104">Denne utvidelsen gjør det enkelt å overføre kunder, leverandører, varer og konti fra Microsoft Dynamics C5 2012 til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5edee-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="5edee-105">Du kan også overføre historiske poster for finanskonti.</span><span class="sxs-lookup"><span data-stu-id="5edee-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="5edee-106">Selskapet i [!INCLUDE[d365fin](includes/d365fin_md.md)]kan ikke inneholde data.</span><span class="sxs-lookup"><span data-stu-id="5edee-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="5edee-107">I tillegg, når du starter en migrering, bør du ikke opprette kunder, leverandører, varer eller kontoer til migreringen er ferdig.</span><span class="sxs-lookup"><span data-stu-id="5edee-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="what-data-is-migrated"></a><span data-ttu-id="5edee-108">Hvilke data overføres?</span><span class="sxs-lookup"><span data-stu-id="5edee-108">What Data is Migrated?</span></span>
<span data-ttu-id="5edee-109">Følgende data overføres for hver enhet:</span><span class="sxs-lookup"><span data-stu-id="5edee-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="5edee-110">**Kunder**</span><span class="sxs-lookup"><span data-stu-id="5edee-110">**Customers**</span></span>
* <span data-ttu-id="5edee-111">Kontakter</span><span class="sxs-lookup"><span data-stu-id="5edee-111">Contacts</span></span>  
* <span data-ttu-id="5edee-112">Lokasjon</span><span class="sxs-lookup"><span data-stu-id="5edee-112">Location</span></span>
* <span data-ttu-id="5edee-113">Land</span><span class="sxs-lookup"><span data-stu-id="5edee-113">Country</span></span>
* <span data-ttu-id="5edee-114">Dimensjoner for kunde (avdeling, senter, formål)</span><span class="sxs-lookup"><span data-stu-id="5edee-114">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="5edee-115">Leveringsmåte</span><span class="sxs-lookup"><span data-stu-id="5edee-115">Shipment method</span></span>
* <span data-ttu-id="5edee-116">Selger</span><span class="sxs-lookup"><span data-stu-id="5edee-116">Sales Person</span></span>
* <span data-ttu-id="5edee-117">Betalingsbetingelser</span><span class="sxs-lookup"><span data-stu-id="5edee-117">Payment terms</span></span>
* <span data-ttu-id="5edee-118">Betalingsmåte</span><span class="sxs-lookup"><span data-stu-id="5edee-118">Payment method</span></span>
* <span data-ttu-id="5edee-119">Kundeprisgruppe</span><span class="sxs-lookup"><span data-stu-id="5edee-119">Customer price group</span></span>
* <span data-ttu-id="5edee-120">Kundefakturarabatt</span><span class="sxs-lookup"><span data-stu-id="5edee-120">Customer invoice discount</span></span>

<span data-ttu-id="5edee-121">Hvis du overfører konti, overføres også følgende data:</span><span class="sxs-lookup"><span data-stu-id="5edee-121">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="5edee-122">Bokføringsgruppe – kunde</span><span class="sxs-lookup"><span data-stu-id="5edee-122">Customer posting setup</span></span>
* <span data-ttu-id="5edee-123">Finanskladd</span><span class="sxs-lookup"><span data-stu-id="5edee-123">General journal batch</span></span>
* <span data-ttu-id="5edee-124">Åpne transaksjoner (kundeposter)</span><span class="sxs-lookup"><span data-stu-id="5edee-124">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="5edee-125">**Leverandører**</span><span class="sxs-lookup"><span data-stu-id="5edee-125">**Vendors**</span></span>
* <span data-ttu-id="5edee-126">Kontakter</span><span class="sxs-lookup"><span data-stu-id="5edee-126">Contacts</span></span>
* <span data-ttu-id="5edee-127">Lokasjon</span><span class="sxs-lookup"><span data-stu-id="5edee-127">Location</span></span>
* <span data-ttu-id="5edee-128">Land</span><span class="sxs-lookup"><span data-stu-id="5edee-128">Country</span></span>
* <span data-ttu-id="5edee-129">Dimensjoner for leverandør (avdeling, senter, formål)</span><span class="sxs-lookup"><span data-stu-id="5edee-129">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="5edee-130">Fakturarabatt</span><span class="sxs-lookup"><span data-stu-id="5edee-130">Invoice discount</span></span>
* <span data-ttu-id="5edee-131">Leveringsmåte</span><span class="sxs-lookup"><span data-stu-id="5edee-131">Shipment method</span></span>
* <span data-ttu-id="5edee-132">Innkjøper</span><span class="sxs-lookup"><span data-stu-id="5edee-132">Purchaser</span></span>
* <span data-ttu-id="5edee-133">Betalingsbetingelser</span><span class="sxs-lookup"><span data-stu-id="5edee-133">Payment terms</span></span>
* <span data-ttu-id="5edee-134">Betalingsmåte</span><span class="sxs-lookup"><span data-stu-id="5edee-134">Payment method</span></span>
* <span data-ttu-id="5edee-135">Leverandørfakturarabatt</span><span class="sxs-lookup"><span data-stu-id="5edee-135">Vendor invoice discount</span></span>

<span data-ttu-id="5edee-136">Hvis du overfører konti, overføres også følgende data:</span><span class="sxs-lookup"><span data-stu-id="5edee-136">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="5edee-137">Bokføringsgruppe – leverandør</span><span class="sxs-lookup"><span data-stu-id="5edee-137">Vendor posting setup</span></span>
* <span data-ttu-id="5edee-138">Finanskladd</span><span class="sxs-lookup"><span data-stu-id="5edee-138">General journal batch</span></span>
* <span data-ttu-id="5edee-139">Åpne transaksjoner (leverandørposter)</span><span class="sxs-lookup"><span data-stu-id="5edee-139">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="5edee-140">**Varer**</span><span class="sxs-lookup"><span data-stu-id="5edee-140">**Items**</span></span>
* <span data-ttu-id="5edee-141">Lokasjon</span><span class="sxs-lookup"><span data-stu-id="5edee-141">Location</span></span>
* <span data-ttu-id="5edee-142">Land</span><span class="sxs-lookup"><span data-stu-id="5edee-142">Country</span></span>
* <span data-ttu-id="5edee-143">Dimensjoner for vare (avdeling, senter, formål)</span><span class="sxs-lookup"><span data-stu-id="5edee-143">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="5edee-144">Salgslinjerabatter</span><span class="sxs-lookup"><span data-stu-id="5edee-144">Sales line discounts</span></span>
* <span data-ttu-id="5edee-145">Kunderabattgrupper</span><span class="sxs-lookup"><span data-stu-id="5edee-145">Customer discount groups</span></span>
* <span data-ttu-id="5edee-146">Varerabattgrupper</span><span class="sxs-lookup"><span data-stu-id="5edee-146">Item discount groups</span></span>
* <span data-ttu-id="5edee-147">Salgspris</span><span class="sxs-lookup"><span data-stu-id="5edee-147">Sales price</span></span>
* <span data-ttu-id="5edee-148">Tariffnummer</span><span class="sxs-lookup"><span data-stu-id="5edee-148">Tariff number</span></span>
* <span data-ttu-id="5edee-149">Enheter</span><span class="sxs-lookup"><span data-stu-id="5edee-149">Units of measure</span></span>
* <span data-ttu-id="5edee-150">Varesporingskode</span><span class="sxs-lookup"><span data-stu-id="5edee-150">Item tracking code</span></span>
* <span data-ttu-id="5edee-151">Kundeprisgruppe</span><span class="sxs-lookup"><span data-stu-id="5edee-151">Customer price group</span></span>
* <span data-ttu-id="5edee-152">Monteringsstykklister</span><span class="sxs-lookup"><span data-stu-id="5edee-152">Assembly BOMs</span></span>

<span data-ttu-id="5edee-153">Hvis du overfører konti, overføres også følgende data:</span><span class="sxs-lookup"><span data-stu-id="5edee-153">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="5edee-154">Lagerbokføringsoppsett</span><span class="sxs-lookup"><span data-stu-id="5edee-154">Inventory posting setup</span></span>
* <span data-ttu-id="5edee-155">Generelt bokføringsoppsett</span><span class="sxs-lookup"><span data-stu-id="5edee-155">General posting setup</span></span>
* <span data-ttu-id="5edee-156">Varekladd</span><span class="sxs-lookup"><span data-stu-id="5edee-156">Item journal batch</span></span>
* <span data-ttu-id="5edee-157">Åpne transaksjoner (vareposter)</span><span class="sxs-lookup"><span data-stu-id="5edee-157">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="5edee-158">Hvis det finnes åpne transaksjoner som bruker utenlandske valutaer, overføres også valutakursene for de aktuelle valutaene.</span><span class="sxs-lookup"><span data-stu-id="5edee-158">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="5edee-159">Andre valutakurser overføres ikke.</span><span class="sxs-lookup"><span data-stu-id="5edee-159">Other exchange rates are not migrated.</span></span>

<span data-ttu-id="5edee-160">**Kontoplan**</span><span class="sxs-lookup"><span data-stu-id="5edee-160">**Chart of Accounts**</span></span>  
* <span data-ttu-id="5edee-161">Standarddimensjoner: Avdeling, kostsenter, formål</span><span class="sxs-lookup"><span data-stu-id="5edee-161">Standard dimensions: Department, Cost Center, Purpose</span></span>  
* <span data-ttu-id="5edee-162">Historiske finanstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="5edee-162">Historical G/L transactions</span></span>  

> [!Note]
> <span data-ttu-id="5edee-163">Historiske finanstransaksjoner behandles på en litt annen måte.</span><span class="sxs-lookup"><span data-stu-id="5edee-163">Historical G/L transactions are treated a little differently.</span></span> <span data-ttu-id="5edee-164">Når du overfører data, angir du parameteren **Inneværende periode**.</span><span class="sxs-lookup"><span data-stu-id="5edee-164">When you migrate data you set a **Current Period** parameter.</span></span> <span data-ttu-id="5edee-165">Denne parameteren angir hvordan finanstransaksjoner behandles.</span><span class="sxs-lookup"><span data-stu-id="5edee-165">This parameter specifies how to process G/L transactions.</span></span> <span data-ttu-id="5edee-166">Transaksjoner etter denne datoen overføres individuelt.</span><span class="sxs-lookup"><span data-stu-id="5edee-166">Transactions after this date are migrated individually.</span></span> <span data-ttu-id="5edee-167">Transaksjoner før denne datoen samles per konto og overføres som et enkelt beløp.</span><span class="sxs-lookup"><span data-stu-id="5edee-167">Transactions before this date are aggregated per account and migrated as a single amount.</span></span> <span data-ttu-id="5edee-168">La oss for eksempel si at det finnes transaksjoner i 2015, 2016, 2017, 2018, og du angir 1. januar 2017 i feltet Innværende periode.</span><span class="sxs-lookup"><span data-stu-id="5edee-168">For example, let's say there are transactions in 2015, 2016, 2017, 2018, and you specify January 01, 2017 in the Current Period field.</span></span> <span data-ttu-id="5edee-169">For hver konto samles beløpene for transaksjonene på eller før 31. desember 2106 i én finanskladdlinje for hver finanskonto.</span><span class="sxs-lookup"><span data-stu-id="5edee-169">For each account, amounts for transactions on or before December 31, 2106, will be aggregated in a single general journal line for each G/L account.</span></span> <span data-ttu-id="5edee-170">Alle transaksjoner etter denne datoen overføres individuelt.</span><span class="sxs-lookup"><span data-stu-id="5edee-170">All trascations after this date will be migrated individually.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="5edee-171">Migrere data</span><span class="sxs-lookup"><span data-stu-id="5edee-171">To migrate data</span></span>
<span data-ttu-id="5edee-172">Det tar kun noen få trinn å eksportere data fra C5 og importere dataen inn i [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="5edee-172">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="5edee-173">I C5 bruker du **Eksportere databasen**-funksjonen for å eksportere dataene.</span><span class="sxs-lookup"><span data-stu-id="5edee-173">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="5edee-174">Deretter sender du eksportmappen til en komprimert (pakket) mappe.</span><span class="sxs-lookup"><span data-stu-id="5edee-174">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="5edee-175">I [!INCLUDE[d365fin](includes/d365fin_md.md)] velger du ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Datamigrering** og deretter velge **Datamigrering**.</span><span class="sxs-lookup"><span data-stu-id="5edee-175">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="5edee-176">Fullfør trinnene i den assisterte oppsettsveiledningen.</span><span class="sxs-lookup"><span data-stu-id="5edee-176">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="5edee-177">Pass på at du velger **Importer fra Microsoft Dynamcis C5 2012** som datakilde.</span><span class="sxs-lookup"><span data-stu-id="5edee-177">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note]
> <span data-ttu-id="5edee-178">Firmaer legger ofte til felt for å tilpasse C5 til deres bestemte bransjer.</span><span class="sxs-lookup"><span data-stu-id="5edee-178">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="5edee-179">flytter ikke data fra egendefinerte felt.</span><span class="sxs-lookup"><span data-stu-id="5edee-179">does not migrate data from custom fields.</span></span> <span data-ttu-id="5edee-180">Migreringen mislykkes også hvis du har flere enn 10 egendefinerte felt.</span><span class="sxs-lookup"><span data-stu-id="5edee-180">Also, migration will fail if you have more than 10 custom fields.</span></span>

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="5edee-181">Se statusen for migreringen</span><span class="sxs-lookup"><span data-stu-id="5edee-181">Viewing the Status of the Migration</span></span>
<span data-ttu-id="5edee-182">Bruk vinduet **Oversikt over datamigrering** for å overvåke migreringen.</span><span class="sxs-lookup"><span data-stu-id="5edee-182">Use the **Data Migration Overview** window to monitor the success of the migration.</span></span> <span data-ttu-id="5edee-183">Siden viser informasjon om hvor mange enheter som er inkludert i migreringen, status til migreringen, antall varer som er migrert, og om migreringen var vellykket.</span><span class="sxs-lookup"><span data-stu-id="5edee-183">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="5edee-184">Den viser også antall feil, gir deg mulighet til å undersøke hva som gikk feil, og gjør det enkelt å gå til enheten for å løse problemene.</span><span class="sxs-lookup"><span data-stu-id="5edee-184">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="5edee-185">Hvis du vil ha mer informasjon, kan du se neste avsnitt i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="5edee-185">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="5edee-186">Mens du venter på resultatet av overføringen, må du oppdatere siden for å vise resultatet.</span><span class="sxs-lookup"><span data-stu-id="5edee-186">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="how-to-avoid-double-posting"></a><span data-ttu-id="5edee-187">Slik unngår du dobbel bokføring</span><span class="sxs-lookup"><span data-stu-id="5edee-187">How to Avoid Double-Posting</span></span>
<span data-ttu-id="5edee-188">For å unngå dobbel bokføring i Finans brukes følgende balansekonti for åpne transaksjoner:</span><span class="sxs-lookup"><span data-stu-id="5edee-188">To help avoid double-posting to the general ledger, the following balance accounts are used for open transactions:</span></span>  

* <span data-ttu-id="5edee-189">Vi bruker leverandørgjeldskonto for leverandører fra leverandørbokføringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="5edee-189">For vendors, we use the A/P account from the vendor posting group.</span></span>  
* <span data-ttu-id="5edee-190">Vi bruker kundefordringskonto for kunder fra kundebokføringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="5edee-190">For customers, we use the A/R account from the customer posting group.</span></span>  
* <span data-ttu-id="5edee-191">For varer oppretter vi et generelt bokføringsoppsett, der justeringskontoen er kontoen som er angitt som lagerkonto i lagerbokføringsoppsettet.</span><span class="sxs-lookup"><span data-stu-id="5edee-191">For items, we create a general posting setup where the adjustment account is the account specified as the inventory account on the inventory posting setup.</span></span>  

## <a name="correcting-errors"></a><span data-ttu-id="5edee-192">Feilkorrigering</span><span class="sxs-lookup"><span data-stu-id="5edee-192">Correcting Errors</span></span>
<span data-ttu-id="5edee-193">Hvis det oppstår en feil, viser **Status**-feltet **Fullført med feil**, og **Feilantall** viser hvor mange feil som oppsto.</span><span class="sxs-lookup"><span data-stu-id="5edee-193">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="5edee-194">For å se en oversikt over feilene, kan du åpne vinduet **Datamigreringsfeil** ved å velge:</span><span class="sxs-lookup"><span data-stu-id="5edee-194">To view a list of the errors, you can open the **Data Migration Errors** window by choosing:</span></span>  

* <span data-ttu-id="5edee-195">Tallet i feltet **Feilantall** for enheten.</span><span class="sxs-lookup"><span data-stu-id="5edee-195">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="5edee-196">Enheten og velg deretter handlingen **Vis feil**.</span><span class="sxs-lookup"><span data-stu-id="5edee-196">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="5edee-197">For å korrigere en feil kan du velge en feilmelding i vinduet **Datamigreringsfeil**, og deretter velge **Rediger post** for å vise de migrerte dataene for enheten.</span><span class="sxs-lookup"><span data-stu-id="5edee-197">In the **Data Migration Errors** window, to fix an error you can choose an error message, and then choose **Edit Record** to view the migrated data for the entity.</span></span> <span data-ttu-id="5edee-198">Hvis du har flere feil som må løses, kan du velge **Massereparasjon av feil** for å redigere enhetene i en liste.</span><span class="sxs-lookup"><span data-stu-id="5edee-198">If you have several errors to fix, you can choose **Bulk-Fix Errors** to edit the entities in a list.</span></span> <span data-ttu-id="5edee-199">Du må fortsatt åpne enkeltposter hvis årsaken til feilen blr forårsaket av en relatert post.</span><span class="sxs-lookup"><span data-stu-id="5edee-199">You still need to open individual records if the error was caused by a related entry though.</span></span> <span data-ttu-id="5edee-200">For eksempel overføres en leverandør ikke hvis en e-postadresse til en av kontaktene har ugyldig format.</span><span class="sxs-lookup"><span data-stu-id="5edee-200">For example, a vendor will not be migrated if an email address one of their contacts has an invalid format.</span></span>

<span data-ttu-id="5edee-201">Etter at du har korrigert én eller flere feil, kan du velge **Migrer** for å migrere enheten du har korrigert, uten å starte hele migrerringen på nytt.</span><span class="sxs-lookup"><span data-stu-id="5edee-201">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="5edee-202">Hvis du har korrigert én eller flere feil, kan du bruke funksjonen **Velg mer** for å velge flere linjer til som skal migreres.</span><span class="sxs-lookup"><span data-stu-id="5edee-202">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="5edee-203">Hvis det finnes feil som ikke er viktige å korrigere, kan du velge dem og så velge **Hopp over valg**.</span><span class="sxs-lookup"><span data-stu-id="5edee-203">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="5edee-204">Hvis du har varer som er inkludert i en stykkliste, må du kanskje migrere mer enn én gang hvis den opprinnelige varen ikke er opprettet før variantene som refererer til den.</span><span class="sxs-lookup"><span data-stu-id="5edee-204">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="5edee-205">Hvis en varevariant opprettes først, kan referansen til den opprinnelige varen føre til en feilmelding.</span><span class="sxs-lookup"><span data-stu-id="5edee-205">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="5edee-206">Kontrollere dataene etter migrering</span><span class="sxs-lookup"><span data-stu-id="5edee-206">Verifying Data After Migrating</span></span>
<span data-ttu-id="5edee-207">Du kan kontrollere at dataene er overført riktig ved å se på følgende sider i C5 og [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5edee-207">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="5edee-208">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="5edee-208">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]| <span data-ttu-id="5edee-209">Kjørsel som skal brukes</span><span class="sxs-lookup"><span data-stu-id="5edee-209">Batch Job to Use</span></span> |
|-----|-----|-----|
|<span data-ttu-id="5edee-210">Kundeposter</span><span class="sxs-lookup"><span data-stu-id="5edee-210">Customer Entries</span></span>| <span data-ttu-id="5edee-211">Finanskladder</span><span class="sxs-lookup"><span data-stu-id="5edee-211">General Journals</span></span>| <span data-ttu-id="5edee-212">CUSTMIGR</span><span class="sxs-lookup"><span data-stu-id="5edee-212">CUSTMIGR</span></span> |
|<span data-ttu-id="5edee-213">Leverandørposter</span><span class="sxs-lookup"><span data-stu-id="5edee-213">Vendor Entries</span></span>| <span data-ttu-id="5edee-214">Finanskladder</span><span class="sxs-lookup"><span data-stu-id="5edee-214">General Journals</span></span>| <span data-ttu-id="5edee-215">VENDMIGR</span><span class="sxs-lookup"><span data-stu-id="5edee-215">VENDMIGR</span></span>|
|<span data-ttu-id="5edee-216">Vareposter</span><span class="sxs-lookup"><span data-stu-id="5edee-216">Item Entries</span></span>| <span data-ttu-id="5edee-217">Varekladder</span><span class="sxs-lookup"><span data-stu-id="5edee-217">Item Journals</span></span>| <span data-ttu-id="5edee-218">ITEMMIGR</span><span class="sxs-lookup"><span data-stu-id="5edee-218">ITEMMIGR</span></span> |
|<span data-ttu-id="5edee-219">Finansposter</span><span class="sxs-lookup"><span data-stu-id="5edee-219">G/L Entries</span></span>| <span data-ttu-id="5edee-220">Finanskladder</span><span class="sxs-lookup"><span data-stu-id="5edee-220">General Journals</span></span>| <span data-ttu-id="5edee-221">GLACMIGR</span><span class="sxs-lookup"><span data-stu-id="5edee-221">GLACMIGR</span></span> |

## <a name="stopping-data-migration"></a><span data-ttu-id="5edee-222">Stoppe datamigrering</span><span class="sxs-lookup"><span data-stu-id="5edee-222">Stopping Data Migration</span></span>
<span data-ttu-id="5edee-223">Du kan stoppe datamigreringen ved å velge **Stopp alle migreringer**.</span><span class="sxs-lookup"><span data-stu-id="5edee-223">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="5edee-224">Hvis du gjør dette, blir alle ventende migreringer også stoppet.</span><span class="sxs-lookup"><span data-stu-id="5edee-224">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="5edee-225">Se også</span><span class="sxs-lookup"><span data-stu-id="5edee-225">See Also</span></span>
<span data-ttu-id="5edee-226">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="5edee-226">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="5edee-227">Komme i gang</span><span class="sxs-lookup"><span data-stu-id="5edee-227">Getting Started</span></span>](product-get-started.md)

