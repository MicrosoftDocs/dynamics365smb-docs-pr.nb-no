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
ms.date: 04/09/208
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: fa6779ee8fb2bbb453014e32cb7f3cf8dcfa18da
ms.openlocfilehash: 698bde6949c6053501881d07135586810fc81bdd
ms.contentlocale: nb-no
ms.lasthandoff: 04/11/2018

---

# <a name="the-c5-data-migration-extension-for-business-central"></a><span data-ttu-id="fd471-103">CS-utvidelse for dataoverføring for Business Central</span><span class="sxs-lookup"><span data-stu-id="fd471-103">The C5 Data Migration Extension for Business Central</span></span>
<span data-ttu-id="fd471-104">Denne utvidelsen gjør det enkelt å overføre kunder, leverandører, varer og konti fra Microsoft Dynamics C5 2012 til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd471-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="fd471-105">Du kan også overføre historiske poster for finanskonti.</span><span class="sxs-lookup"><span data-stu-id="fd471-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="fd471-106">Selskapet i [!INCLUDE[d365fin](includes/d365fin_md.md)]kan ikke inneholde data.</span><span class="sxs-lookup"><span data-stu-id="fd471-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="fd471-107">I tillegg, når du starter en migrering, bør du ikke opprette kunder, leverandører, varer eller kontoer til migreringen er ferdig.</span><span class="sxs-lookup"><span data-stu-id="fd471-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="what-data-is-migrated"></a><span data-ttu-id="fd471-108">Hvilke data overføres?</span><span class="sxs-lookup"><span data-stu-id="fd471-108">What Data is Migrated?</span></span>
<span data-ttu-id="fd471-109">Følgende data overføres for hver enhet:</span><span class="sxs-lookup"><span data-stu-id="fd471-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="fd471-110">**Kunder**</span><span class="sxs-lookup"><span data-stu-id="fd471-110">**Customers**</span></span>
* <span data-ttu-id="fd471-111">Lokasjon</span><span class="sxs-lookup"><span data-stu-id="fd471-111">Location</span></span>
* <span data-ttu-id="fd471-112">Land</span><span class="sxs-lookup"><span data-stu-id="fd471-112">Country</span></span>
* <span data-ttu-id="fd471-113">Dimensjoner for kunde (avdeling, senter, formål)</span><span class="sxs-lookup"><span data-stu-id="fd471-113">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="fd471-114">Leveringsmåte</span><span class="sxs-lookup"><span data-stu-id="fd471-114">Shipment method</span></span>
* <span data-ttu-id="fd471-115">Selger</span><span class="sxs-lookup"><span data-stu-id="fd471-115">Sales Person</span></span>
* <span data-ttu-id="fd471-116">Betalingsbetingelser</span><span class="sxs-lookup"><span data-stu-id="fd471-116">Payment terms</span></span>
* <span data-ttu-id="fd471-117">Betalingsmåte</span><span class="sxs-lookup"><span data-stu-id="fd471-117">Payment method</span></span>
* <span data-ttu-id="fd471-118">Kundeprisgruppe</span><span class="sxs-lookup"><span data-stu-id="fd471-118">Customer price group</span></span>
* <span data-ttu-id="fd471-119">Kundefakturarabatt</span><span class="sxs-lookup"><span data-stu-id="fd471-119">Customer invoice discount</span></span>

<span data-ttu-id="fd471-120">Hvis du overfører konti, overføres også følgende data:</span><span class="sxs-lookup"><span data-stu-id="fd471-120">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="fd471-121">Bokføringsgruppe – kunde</span><span class="sxs-lookup"><span data-stu-id="fd471-121">Customer posting setup</span></span>
* <span data-ttu-id="fd471-122">Finanskladd</span><span class="sxs-lookup"><span data-stu-id="fd471-122">General journal batch</span></span>
* <span data-ttu-id="fd471-123">Åpne transaksjoner (kundeposter)</span><span class="sxs-lookup"><span data-stu-id="fd471-123">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="fd471-124">**Leverandører**</span><span class="sxs-lookup"><span data-stu-id="fd471-124">**Vendors**</span></span>
* <span data-ttu-id="fd471-125">Lokasjon</span><span class="sxs-lookup"><span data-stu-id="fd471-125">Location</span></span>
* <span data-ttu-id="fd471-126">Land</span><span class="sxs-lookup"><span data-stu-id="fd471-126">Country</span></span>
* <span data-ttu-id="fd471-127">Dimensjoner for leverandør (avdeling, senter, formål)</span><span class="sxs-lookup"><span data-stu-id="fd471-127">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="fd471-128">Fakturarabatt</span><span class="sxs-lookup"><span data-stu-id="fd471-128">Invoice discount</span></span>
* <span data-ttu-id="fd471-129">Leveringsmåte</span><span class="sxs-lookup"><span data-stu-id="fd471-129">Shipment method</span></span>
* <span data-ttu-id="fd471-130">Innkjøper</span><span class="sxs-lookup"><span data-stu-id="fd471-130">Purchaser</span></span>
* <span data-ttu-id="fd471-131">Betalingsbetingelser</span><span class="sxs-lookup"><span data-stu-id="fd471-131">Payment terms</span></span>
* <span data-ttu-id="fd471-132">Betalingsmåte</span><span class="sxs-lookup"><span data-stu-id="fd471-132">Payment method</span></span>
* <span data-ttu-id="fd471-133">Leverandørfakturarabatt</span><span class="sxs-lookup"><span data-stu-id="fd471-133">Vendor invoice discount</span></span>

<span data-ttu-id="fd471-134">Hvis du overfører konti, overføres også følgende data:</span><span class="sxs-lookup"><span data-stu-id="fd471-134">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="fd471-135">Bokføringsgruppe – leverandør</span><span class="sxs-lookup"><span data-stu-id="fd471-135">Vendor posting setup</span></span>
* <span data-ttu-id="fd471-136">Finanskladd</span><span class="sxs-lookup"><span data-stu-id="fd471-136">General journal batch</span></span>
* <span data-ttu-id="fd471-137">Åpne transaksjoner (leverandørposter)</span><span class="sxs-lookup"><span data-stu-id="fd471-137">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="fd471-138">**Varer**</span><span class="sxs-lookup"><span data-stu-id="fd471-138">**Items**</span></span>
* <span data-ttu-id="fd471-139">Lokasjon</span><span class="sxs-lookup"><span data-stu-id="fd471-139">Location</span></span>
* <span data-ttu-id="fd471-140">Land</span><span class="sxs-lookup"><span data-stu-id="fd471-140">Country</span></span>
* <span data-ttu-id="fd471-141">Dimensjoner for vare (avdeling, senter, formål)</span><span class="sxs-lookup"><span data-stu-id="fd471-141">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="fd471-142">Salgslinjerabatter</span><span class="sxs-lookup"><span data-stu-id="fd471-142">Sales line discounts</span></span>
* <span data-ttu-id="fd471-143">Kunderabattgrupper</span><span class="sxs-lookup"><span data-stu-id="fd471-143">Customer discount groups</span></span>
* <span data-ttu-id="fd471-144">Varerabattgrupper</span><span class="sxs-lookup"><span data-stu-id="fd471-144">Item discount groups</span></span>
* <span data-ttu-id="fd471-145">Salgspris</span><span class="sxs-lookup"><span data-stu-id="fd471-145">Sales price</span></span>
* <span data-ttu-id="fd471-146">Tariffnummer</span><span class="sxs-lookup"><span data-stu-id="fd471-146">Tariff number</span></span>
* <span data-ttu-id="fd471-147">Enheter</span><span class="sxs-lookup"><span data-stu-id="fd471-147">Units of measure</span></span>
* <span data-ttu-id="fd471-148">Varesporingskode</span><span class="sxs-lookup"><span data-stu-id="fd471-148">Item tracking code</span></span>
* <span data-ttu-id="fd471-149">Kundeprisgruppe</span><span class="sxs-lookup"><span data-stu-id="fd471-149">Customer price group</span></span>

<span data-ttu-id="fd471-150">Hvis du overfører konti, overføres også følgende data:</span><span class="sxs-lookup"><span data-stu-id="fd471-150">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="fd471-151">Lagerbokføringsoppsett</span><span class="sxs-lookup"><span data-stu-id="fd471-151">Inventory posting setup</span></span>
* <span data-ttu-id="fd471-152">Generelt bokføringsoppsett</span><span class="sxs-lookup"><span data-stu-id="fd471-152">General posting setup</span></span>
* <span data-ttu-id="fd471-153">Varekladd</span><span class="sxs-lookup"><span data-stu-id="fd471-153">Item journal batch</span></span>
* <span data-ttu-id="fd471-154">Åpne transaksjoner (vareposter)</span><span class="sxs-lookup"><span data-stu-id="fd471-154">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="fd471-155">Hvis det finnes åpne transaksjoner som bruker utenlandske valutaer, overføres også valutakursene for de aktuelle valutaene.</span><span class="sxs-lookup"><span data-stu-id="fd471-155">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="fd471-156">Andre valutakurser overføres ikke.</span><span class="sxs-lookup"><span data-stu-id="fd471-156">Other exchange rates are not migrated.</span></span>

<span data-ttu-id="fd471-157">**Kontoplan**</span><span class="sxs-lookup"><span data-stu-id="fd471-157">**Chart of Accounts**</span></span>  
* <span data-ttu-id="fd471-158">Standarddimensjoner: Avdeling, kostsenter, formål</span><span class="sxs-lookup"><span data-stu-id="fd471-158">Standard dimensions: Department, Cost Center, Purpose</span></span>  
* <span data-ttu-id="fd471-159">Historiske finanstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="fd471-159">Historical G/L transactions</span></span>  

> [!Note]
> <span data-ttu-id="fd471-160">Historiske finanstransaksjoner behandles på en litt annen måte.</span><span class="sxs-lookup"><span data-stu-id="fd471-160">Historical G/L transactions are treated a little differently.</span></span> <span data-ttu-id="fd471-161">Når du overfører data, angir du parameteren **Inneværende periode**.</span><span class="sxs-lookup"><span data-stu-id="fd471-161">When you migrate data you set a **Current Period** parameter.</span></span> <span data-ttu-id="fd471-162">Denne parameteren angir hvordan finanstransaksjoner behandles.</span><span class="sxs-lookup"><span data-stu-id="fd471-162">This parameter specifies how to process G/L transactions.</span></span> <span data-ttu-id="fd471-163">Transaksjoner etter denne datoen overføres individuelt.</span><span class="sxs-lookup"><span data-stu-id="fd471-163">Transactions after this date are migrated individually.</span></span> <span data-ttu-id="fd471-164">Transaksjoner før denne datoen samles per konto og overføres som et enkelt beløp.</span><span class="sxs-lookup"><span data-stu-id="fd471-164">Transactions before this date are aggregated per account and migrated as a single amount.</span></span> <span data-ttu-id="fd471-165">La oss for eksempel si at det finnes transaksjoner i 2015, 2016, 2017, 2018, og du angir 1. januar 2017 i feltet Innværende periode.</span><span class="sxs-lookup"><span data-stu-id="fd471-165">For example, let's say there are transactions in 2015, 2016, 2017, 2018, and you specify January 01, 2017 in the Current Period field.</span></span> <span data-ttu-id="fd471-166">For hver konto samles beløpene for transaksjonene på eller før 31. desember 2106 i én finanskladdlinje for hver finanskonto.</span><span class="sxs-lookup"><span data-stu-id="fd471-166">For each account, amounts for transactions on or before December 31, 2106, will be aggregated in a single general journal line for each G/L account.</span></span> <span data-ttu-id="fd471-167">Alle transaksjoner etter denne datoen overføres individuelt.</span><span class="sxs-lookup"><span data-stu-id="fd471-167">All trascations after this date will be migrated individually.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="fd471-168">Migrere data</span><span class="sxs-lookup"><span data-stu-id="fd471-168">To migrate data</span></span>
<span data-ttu-id="fd471-169">Det tar kun noen få trinn å eksportere data fra C5 og importere dataen inn i [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="fd471-169">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="fd471-170">I C5 bruker du **Eksportere databasen**-funksjonen for å eksportere dataene.</span><span class="sxs-lookup"><span data-stu-id="fd471-170">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="fd471-171">Deretter sender du eksportmappen til en komprimert (pakket) mappe.</span><span class="sxs-lookup"><span data-stu-id="fd471-171">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="fd471-172">I [!INCLUDE[d365fin](includes/d365fin_md.md)] velger du ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), så velger du **Datamigrering**, og så  **Datamigrering**.</span><span class="sxs-lookup"><span data-stu-id="fd471-172">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="fd471-173">Fullfør trinnene i den assisterte oppsettsveiledningen.</span><span class="sxs-lookup"><span data-stu-id="fd471-173">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="fd471-174">Pass på at du velger **Importer fra Microsoft Dynamcis C5 2012** som datakilde.</span><span class="sxs-lookup"><span data-stu-id="fd471-174">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note]
> <span data-ttu-id="fd471-175">Firmaer legger ofte til felt for å tilpasse C5 til deres bestemte bransjer.</span><span class="sxs-lookup"><span data-stu-id="fd471-175">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="fd471-176"> flytter ikke data fra egendefinerte felt.</span><span class="sxs-lookup"><span data-stu-id="fd471-176"> does not migrate data from custom fields.</span></span> <span data-ttu-id="fd471-177">Migreringen mislykkes også hvis du har flere enn 10 egendefinerte felt.</span><span class="sxs-lookup"><span data-stu-id="fd471-177">Also, migration will fail if you have more than 10 custom fields.</span></span>

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="fd471-178">Se statusen for migreringen</span><span class="sxs-lookup"><span data-stu-id="fd471-178">Viewing the Status of the Migration</span></span>
<span data-ttu-id="fd471-179">Bruk siden **Oversikt over datamigrering** for å overvåke migreringen.</span><span class="sxs-lookup"><span data-stu-id="fd471-179">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="fd471-180">Siden viser informasjon om hvor mange enheter som er inkludert i migreringen, status til migreringen, antall varer som er migrert, og om migreringen var vellykket.</span><span class="sxs-lookup"><span data-stu-id="fd471-180">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="fd471-181">Den viser også antall feil, gir deg mulighet til å undersøke hva som gikk feil, og gjør det enkelt å gå til enheten for å løse problemene.</span><span class="sxs-lookup"><span data-stu-id="fd471-181">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="fd471-182">Hvis du vil ha mer informasjon, kan du se neste avsnitt i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="fd471-182">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="fd471-183">Mens du venter på resultatet av overføringen, må du oppdatere siden for å vise resultatet.</span><span class="sxs-lookup"><span data-stu-id="fd471-183">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="how-to-avoid-double-posting"></a><span data-ttu-id="fd471-184">Slik unngår du dobbel bokføring</span><span class="sxs-lookup"><span data-stu-id="fd471-184">How to Avoid Double-Posting</span></span>
<span data-ttu-id="fd471-185">For å unngå dobbel bokføring i Finans brukes følgende balansekonti for åpne transaksjoner:</span><span class="sxs-lookup"><span data-stu-id="fd471-185">To help avoid double-posting to the general ledger, the following balance accounts are used for open transactions:</span></span>  
  
* <span data-ttu-id="fd471-186">Vi bruker leverandørgjeldskonto for leverandører fra leverandørbokføringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="fd471-186">For vendors, we use the A/P account from the vendor posting group.</span></span>  
* <span data-ttu-id="fd471-187">Vi bruker kundefordringskonto for kunder fra kundebokføringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="fd471-187">For customers, we use the A/R account from the customer posting group.</span></span>  
* <span data-ttu-id="fd471-188">For varer oppretter vi et generelt bokføringsoppsett, der justeringskontoen er kontoen som er angitt som lagerkonto i lagerbokføringsoppsettet.</span><span class="sxs-lookup"><span data-stu-id="fd471-188">For items, we create a general posting setup where the adjustment account is the account specified as the inventory account on the inventory posting setup.</span></span>  

## <a name="correcting-errors"></a><span data-ttu-id="fd471-189">Feilkorrigering</span><span class="sxs-lookup"><span data-stu-id="fd471-189">Correcting Errors</span></span>
<span data-ttu-id="fd471-190">Hvis det oppstår en feil, viser **Status**-feltet **Fullført med feil**, og **Feilantall** viser hvor mange feil som oppsto.</span><span class="sxs-lookup"><span data-stu-id="fd471-190">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="fd471-191">For å se en oversikt over feilene, kan du åpne siden **Datamigreringsfeil** ved å velge:</span><span class="sxs-lookup"><span data-stu-id="fd471-191">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>  

* <span data-ttu-id="fd471-192">Tallet i feltet **Feilantall** for enheten.</span><span class="sxs-lookup"><span data-stu-id="fd471-192">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="fd471-193">Enheten og velg deretter handlingen **Vis feil**.</span><span class="sxs-lookup"><span data-stu-id="fd471-193">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="fd471-194">For å korrigere en feil kan du velge en feilmelding på siden **Datamigreringsfeil**, og deretter velge **Rediger post** for å åpne en side som inneholder den migrerte dataen til enheten.</span><span class="sxs-lookup"><span data-stu-id="fd471-194">On the **Data Migration Errors** page, to fix an error you can choose an error message, then choose **Edit Record** to open a page that shows the migrated data for the entity.</span></span> <span data-ttu-id="fd471-195">Etter at du har korrigert én eller flere feil, kan du velge **Migrer** for å migrere enheten du har korrigert, uten å starte hele migrerringen på nytt.</span><span class="sxs-lookup"><span data-stu-id="fd471-195">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="fd471-196">Hvis du har korrigert én eller flere feil, kan du bruke funksjonen **Velg mer** for å velge flere linjer til som skal migreres.</span><span class="sxs-lookup"><span data-stu-id="fd471-196">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="fd471-197">Hvis det finnes feil som ikke er viktige å korrigere, kan du velge dem og så velge **Hopp over valg**.</span><span class="sxs-lookup"><span data-stu-id="fd471-197">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="fd471-198">Hvis du har varer som er inkludert i en stykkliste, må du kanskje migrere mer enn én gang hvis den opprinnelige varen ikke er opprettet før variantene som refererer til den.</span><span class="sxs-lookup"><span data-stu-id="fd471-198">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="fd471-199">Hvis en varevariant opprettes først, kan referansen til den opprinnelige varen føre til en feilmelding.</span><span class="sxs-lookup"><span data-stu-id="fd471-199">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="fd471-200">Kontrollere dataene etter migrering</span><span class="sxs-lookup"><span data-stu-id="fd471-200">Verifying Data After Migrating</span></span>
<span data-ttu-id="fd471-201">Du kan kontrollere at dataene er overført riktig ved å se på følgende sider i C5 og [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fd471-201">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="fd471-202">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="fd471-202">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]| <span data-ttu-id="fd471-203">Kjørsel som skal brukes</span><span class="sxs-lookup"><span data-stu-id="fd471-203">Batch Job to Use</span></span> |
|-----|-----|-----|
|<span data-ttu-id="fd471-204">Kundeposter</span><span class="sxs-lookup"><span data-stu-id="fd471-204">Customer Entries</span></span>| <span data-ttu-id="fd471-205">Finanskladder</span><span class="sxs-lookup"><span data-stu-id="fd471-205">General Journals</span></span>| <span data-ttu-id="fd471-206">CUSTMIGR</span><span class="sxs-lookup"><span data-stu-id="fd471-206">CUSTMIGR</span></span> |
|<span data-ttu-id="fd471-207">Leverandørposter</span><span class="sxs-lookup"><span data-stu-id="fd471-207">Vendor Entries</span></span>| <span data-ttu-id="fd471-208">Finanskladder</span><span class="sxs-lookup"><span data-stu-id="fd471-208">General Journals</span></span>| <span data-ttu-id="fd471-209">VENDMIGR</span><span class="sxs-lookup"><span data-stu-id="fd471-209">VENDMIGR</span></span>|
|<span data-ttu-id="fd471-210">Vareposter</span><span class="sxs-lookup"><span data-stu-id="fd471-210">Item Entries</span></span>| <span data-ttu-id="fd471-211">Varekladder</span><span class="sxs-lookup"><span data-stu-id="fd471-211">Item Journals</span></span>| <span data-ttu-id="fd471-212">ITEMMIGR</span><span class="sxs-lookup"><span data-stu-id="fd471-212">ITEMMIGR</span></span> |
|<span data-ttu-id="fd471-213">Finansposter</span><span class="sxs-lookup"><span data-stu-id="fd471-213">G/L Entries</span></span>| <span data-ttu-id="fd471-214">Finanskladder</span><span class="sxs-lookup"><span data-stu-id="fd471-214">General Journals</span></span>| <span data-ttu-id="fd471-215">GLACMIGR</span><span class="sxs-lookup"><span data-stu-id="fd471-215">GLACMIGR</span></span> |

## <a name="stopping-data-migration"></a><span data-ttu-id="fd471-216">Stoppe datamigrering</span><span class="sxs-lookup"><span data-stu-id="fd471-216">Stopping Data Migration</span></span>
<span data-ttu-id="fd471-217">Du kan stoppe datamigreringen ved å velge **Stopp alle migreringer**.</span><span class="sxs-lookup"><span data-stu-id="fd471-217">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="fd471-218">Hvis du gjør dette, blir alle ventende migreringer også stoppet.</span><span class="sxs-lookup"><span data-stu-id="fd471-218">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd471-219">Se også</span><span class="sxs-lookup"><span data-stu-id="fd471-219">See Also</span></span>
<span data-ttu-id="fd471-220">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="fd471-220">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="fd471-221">Komme i gang</span><span class="sxs-lookup"><span data-stu-id="fd471-221">Getting Started</span></span>](product-get-started.md) 

