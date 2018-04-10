---
title: "Bruke C5-utvidelse for dataoverføring | Microsoft-dokumentasjon"
description: "Bruk denne utvidelsen til å overføre kunder, leverandører, varer og finanskonti fra Microsoft Dynamics C5 2012 til Financials."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 11/21/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 7fe6393ad43dbad032512b2d6d45cc8ee0392236
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---

# <a name="the-c5-data-migration-extension-for-business-central"></a><span data-ttu-id="ed203-103">CS-utvidelse for dataoverføring for Business Central</span><span class="sxs-lookup"><span data-stu-id="ed203-103">The C5 Data Migration Extension for Business Central</span></span>
<span data-ttu-id="ed203-104">Denne utvidelsen gjør det enkelt å overføre kunder, leverandører, varer og konti fra Microsoft Dynamics C5 2012 til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ed203-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="ed203-105">Du kan også overføre historiske poster for finanskonti.</span><span class="sxs-lookup"><span data-stu-id="ed203-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="ed203-106">Selskapet i [!INCLUDE[d365fin](includes/d365fin_md.md)]kan ikke inneholde data.</span><span class="sxs-lookup"><span data-stu-id="ed203-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="ed203-107">I tillegg, når du starter en migrering, bør du ikke opprette kunder, leverandører, varer eller kontoer til migreringen er ferdig.</span><span class="sxs-lookup"><span data-stu-id="ed203-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

##<a name="what-data-is-migrated"></a><span data-ttu-id="ed203-108">Hvilke data overføres?</span><span class="sxs-lookup"><span data-stu-id="ed203-108">What Data is Migrated?</span></span>
<span data-ttu-id="ed203-109">Følgende data overføres for hver enhet:</span><span class="sxs-lookup"><span data-stu-id="ed203-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="ed203-110">**Kunder**</span><span class="sxs-lookup"><span data-stu-id="ed203-110">**Customers**</span></span>
* <span data-ttu-id="ed203-111">Lokasjon</span><span class="sxs-lookup"><span data-stu-id="ed203-111">Location</span></span>
* <span data-ttu-id="ed203-112">Land</span><span class="sxs-lookup"><span data-stu-id="ed203-112">Country</span></span>
* <span data-ttu-id="ed203-113">Dimensjoner for kunde (avdeling, senter, formål)</span><span class="sxs-lookup"><span data-stu-id="ed203-113">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="ed203-114">Leveringsmåte</span><span class="sxs-lookup"><span data-stu-id="ed203-114">Shipment method</span></span>
* <span data-ttu-id="ed203-115">Selger</span><span class="sxs-lookup"><span data-stu-id="ed203-115">Sales Person</span></span>
* <span data-ttu-id="ed203-116">Betalingsbetingelser</span><span class="sxs-lookup"><span data-stu-id="ed203-116">Payment terms</span></span>
* <span data-ttu-id="ed203-117">Betalingsmåte</span><span class="sxs-lookup"><span data-stu-id="ed203-117">Payment method</span></span>
* <span data-ttu-id="ed203-118">Kundeprisgruppe</span><span class="sxs-lookup"><span data-stu-id="ed203-118">Customer price group</span></span>
* <span data-ttu-id="ed203-119">Kundefakturarabatt</span><span class="sxs-lookup"><span data-stu-id="ed203-119">Customer invoice discount</span></span>

<span data-ttu-id="ed203-120">Hvis du overfører konti, overføres også følgende data:</span><span class="sxs-lookup"><span data-stu-id="ed203-120">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="ed203-121">Bokføringsgruppe – kunde</span><span class="sxs-lookup"><span data-stu-id="ed203-121">Customer posting setup</span></span>
* <span data-ttu-id="ed203-122">Finanskladd</span><span class="sxs-lookup"><span data-stu-id="ed203-122">General journal batch</span></span>
* <span data-ttu-id="ed203-123">Åpne transaksjoner (kundeposter)</span><span class="sxs-lookup"><span data-stu-id="ed203-123">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="ed203-124">**Leverandører**</span><span class="sxs-lookup"><span data-stu-id="ed203-124">**Vendors**</span></span>
* <span data-ttu-id="ed203-125">Lokasjon</span><span class="sxs-lookup"><span data-stu-id="ed203-125">Location</span></span>
* <span data-ttu-id="ed203-126">Land</span><span class="sxs-lookup"><span data-stu-id="ed203-126">Country</span></span>
* <span data-ttu-id="ed203-127">Dimensjoner for leverandør (avdeling, senter, formål)</span><span class="sxs-lookup"><span data-stu-id="ed203-127">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="ed203-128">Fakturarabatt</span><span class="sxs-lookup"><span data-stu-id="ed203-128">Invoice discount</span></span>
* <span data-ttu-id="ed203-129">Leveringsmåte</span><span class="sxs-lookup"><span data-stu-id="ed203-129">Shipment method</span></span>
* <span data-ttu-id="ed203-130">Innkjøper</span><span class="sxs-lookup"><span data-stu-id="ed203-130">Purchaser</span></span>
* <span data-ttu-id="ed203-131">Betalingsbetingelser</span><span class="sxs-lookup"><span data-stu-id="ed203-131">Payment terms</span></span>
* <span data-ttu-id="ed203-132">Betalingsmåte</span><span class="sxs-lookup"><span data-stu-id="ed203-132">Payment method</span></span>
* <span data-ttu-id="ed203-133">Leverandørfakturarabatt</span><span class="sxs-lookup"><span data-stu-id="ed203-133">Vendor invoice discount</span></span>

<span data-ttu-id="ed203-134">Hvis du overfører konti, overføres også følgende data:</span><span class="sxs-lookup"><span data-stu-id="ed203-134">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="ed203-135">Bokføringsgruppe – leverandør</span><span class="sxs-lookup"><span data-stu-id="ed203-135">Vendor posting setup</span></span>
* <span data-ttu-id="ed203-136">Finanskladd</span><span class="sxs-lookup"><span data-stu-id="ed203-136">General journal batch</span></span>
* <span data-ttu-id="ed203-137">Åpne transaksjoner (leverandørposter)</span><span class="sxs-lookup"><span data-stu-id="ed203-137">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="ed203-138">**Varer**</span><span class="sxs-lookup"><span data-stu-id="ed203-138">**Items**</span></span>
* <span data-ttu-id="ed203-139">Lokasjon</span><span class="sxs-lookup"><span data-stu-id="ed203-139">Location</span></span>
* <span data-ttu-id="ed203-140">Land</span><span class="sxs-lookup"><span data-stu-id="ed203-140">Country</span></span>
* <span data-ttu-id="ed203-141">Dimensjoner for vare (avdeling, senter, formål)</span><span class="sxs-lookup"><span data-stu-id="ed203-141">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="ed203-142">Salgslinjerabatter</span><span class="sxs-lookup"><span data-stu-id="ed203-142">Sales line discounts</span></span>
* <span data-ttu-id="ed203-143">Kunderabattgrupper</span><span class="sxs-lookup"><span data-stu-id="ed203-143">Customer discount groups</span></span>
* <span data-ttu-id="ed203-144">Varerabattgrupper</span><span class="sxs-lookup"><span data-stu-id="ed203-144">Item discount groups</span></span>
* <span data-ttu-id="ed203-145">Salgspris</span><span class="sxs-lookup"><span data-stu-id="ed203-145">Sales price</span></span>
* <span data-ttu-id="ed203-146">Tariffnummer</span><span class="sxs-lookup"><span data-stu-id="ed203-146">Tariff number</span></span>
* <span data-ttu-id="ed203-147">Enheter</span><span class="sxs-lookup"><span data-stu-id="ed203-147">Units of measure</span></span>
* <span data-ttu-id="ed203-148">Varesporingskode</span><span class="sxs-lookup"><span data-stu-id="ed203-148">Item tracking code</span></span>
* <span data-ttu-id="ed203-149">Kundeprisgruppe</span><span class="sxs-lookup"><span data-stu-id="ed203-149">Customer price group</span></span>

<span data-ttu-id="ed203-150">Hvis du overfører konti, overføres også følgende data:</span><span class="sxs-lookup"><span data-stu-id="ed203-150">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="ed203-151">Lagerbokføringsoppsett</span><span class="sxs-lookup"><span data-stu-id="ed203-151">Inventory posting setup</span></span>
* <span data-ttu-id="ed203-152">Generelt bokføringsoppsett</span><span class="sxs-lookup"><span data-stu-id="ed203-152">General posting setup</span></span>
* <span data-ttu-id="ed203-153">Varekladd</span><span class="sxs-lookup"><span data-stu-id="ed203-153">Item journal batch</span></span>
* <span data-ttu-id="ed203-154">Åpne transaksjoner (vareposter)</span><span class="sxs-lookup"><span data-stu-id="ed203-154">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="ed203-155">Hvis det finnes åpne transaksjoner som bruker utenlandske valutaer, overføres også valutakursene for de aktuelle valutaene.</span><span class="sxs-lookup"><span data-stu-id="ed203-155">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="ed203-156">Andre valutakurser overføres ikke.</span><span class="sxs-lookup"><span data-stu-id="ed203-156">Other exchange rates are not migrated.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="ed203-157">Migrere data</span><span class="sxs-lookup"><span data-stu-id="ed203-157">To migrate data</span></span>
<span data-ttu-id="ed203-158">Det tar kun noen få trinn å eksportere data fra C5 og importere dataen inn i [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="ed203-158">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="ed203-159">I C5 bruker du **Eksportere databasen**-funksjonen for å eksportere dataene.</span><span class="sxs-lookup"><span data-stu-id="ed203-159">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="ed203-160">Deretter sender du eksportmappen til en komprimert (pakket) mappe.</span><span class="sxs-lookup"><span data-stu-id="ed203-160">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="ed203-161">I [!INCLUDE[d365fin](includes/d365fin_md.md)] velger du ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), så velger du **Datamigrering**, og så  **Datamigrering**.</span><span class="sxs-lookup"><span data-stu-id="ed203-161">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="ed203-162">Fullfør trinnene i den assisterte oppsettsveiledningen.</span><span class="sxs-lookup"><span data-stu-id="ed203-162">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="ed203-163">Pass på at du velger **Importer fra Microsoft Dynamcis C5 2012** som datakilde.</span><span class="sxs-lookup"><span data-stu-id="ed203-163">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note]
> <span data-ttu-id="ed203-164">Firmaer legger ofte til felt for å tilpasse C5 til deres bestemte bransjer.</span><span class="sxs-lookup"><span data-stu-id="ed203-164">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="ed203-165"> flytter ikke data fra egendefinerte felt.</span><span class="sxs-lookup"><span data-stu-id="ed203-165"> does not migrate data from custom fields.</span></span> <span data-ttu-id="ed203-166">Migreringen mislykkes også hvis du har flere enn 10 egendefinerte felt.</span><span class="sxs-lookup"><span data-stu-id="ed203-166">Also, migration will fail if you have more than 10 custom fields.</span></span>

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="ed203-167">Se statusen for migreringen</span><span class="sxs-lookup"><span data-stu-id="ed203-167">Viewing the Status of the Migration</span></span>
<span data-ttu-id="ed203-168">Bruk siden **Oversikt over datamigrering** for å overvåke migreringen.</span><span class="sxs-lookup"><span data-stu-id="ed203-168">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="ed203-169">Siden viser informasjon om hvor mange enheter som er inkludert i migreringen, status til migreringen, antall varer som er migrert, og om migreringen var vellykket.</span><span class="sxs-lookup"><span data-stu-id="ed203-169">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="ed203-170">Den viser også antall feil, gir deg mulighet til å undersøke hva som gikk feil, og gjør det enkelt å gå til enheten for å løse problemene.</span><span class="sxs-lookup"><span data-stu-id="ed203-170">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="ed203-171">Hvis du vil ha mer informasjon, kan du se neste avsnitt i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="ed203-171">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="ed203-172">Mens du venter på resultatet av overføringen, må du oppdatere siden for å vise resultatet.</span><span class="sxs-lookup"><span data-stu-id="ed203-172">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="correcting-errors"></a><span data-ttu-id="ed203-173">Feilkorrigering</span><span class="sxs-lookup"><span data-stu-id="ed203-173">Correcting Errors</span></span>
<span data-ttu-id="ed203-174">Hvis det oppstår en feil, viser **Status**-feltet **Fullført med feil**, og **Feilantall** viser hvor mange feil som oppsto.</span><span class="sxs-lookup"><span data-stu-id="ed203-174">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="ed203-175">For å se en oversikt over feilene, kan du åpne siden **Datamigreringsfeil** ved å velge:</span><span class="sxs-lookup"><span data-stu-id="ed203-175">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>  

* <span data-ttu-id="ed203-176">Tallet i feltet **Feilantall** for enheten.</span><span class="sxs-lookup"><span data-stu-id="ed203-176">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="ed203-177">Enheten og velg deretter handlingen **Vis feil**.</span><span class="sxs-lookup"><span data-stu-id="ed203-177">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="ed203-178">For å korrigere en feil kan du velge en feilmelding på siden **Datamigreringsfeil**, og deretter velge **Rediger post** for å åpne en side som inneholder den migrerte dataen til enheten.</span><span class="sxs-lookup"><span data-stu-id="ed203-178">On the **Data Migration Errors** page, to fix an error you can choose an error message, then choose **Edit Record** to open a page that shows the migrated data for the entity.</span></span> <span data-ttu-id="ed203-179">Etter at du har korrigert én eller flere feil, kan du velge **Migrer** for å migrere enheten du har korrigert, uten å starte hele migrerringen på nytt.</span><span class="sxs-lookup"><span data-stu-id="ed203-179">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="ed203-180">Hvis du har korrigert én eller flere feil, kan du bruke funksjonen **Velg mer** for å velge flere linjer til som skal migreres.</span><span class="sxs-lookup"><span data-stu-id="ed203-180">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="ed203-181">Hvis det finnes feil som ikke er viktige å korrigere, kan du velge dem og så velge **Hopp over valg**.</span><span class="sxs-lookup"><span data-stu-id="ed203-181">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="ed203-182">Hvis du har varer som er inkludert i en stykkliste, må du kanskje migrere mer enn én gang hvis den opprinnelige varen ikke er opprettet før variantene som refererer til den.</span><span class="sxs-lookup"><span data-stu-id="ed203-182">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="ed203-183">Hvis en varevariant opprettes først, kan referansen til den opprinnelige varen føre til en feilmelding.</span><span class="sxs-lookup"><span data-stu-id="ed203-183">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="ed203-184">Kontrollere dataene etter migrering</span><span class="sxs-lookup"><span data-stu-id="ed203-184">Verifying Data After Migrating</span></span>
<span data-ttu-id="ed203-185">Du kan kontrollere at dataene er overført riktig ved å se på følgende sider i C5 og [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ed203-185">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="ed203-186">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="ed203-186">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]|
|-----|-----|
|<span data-ttu-id="ed203-187">Kundeposter</span><span class="sxs-lookup"><span data-stu-id="ed203-187">Customer Entries</span></span>| <span data-ttu-id="ed203-188">Finanskladder</span><span class="sxs-lookup"><span data-stu-id="ed203-188">General Journals</span></span>|
|<span data-ttu-id="ed203-189">Leverandørposter</span><span class="sxs-lookup"><span data-stu-id="ed203-189">Vendor Entries</span></span>| <span data-ttu-id="ed203-190">Finanskladder</span><span class="sxs-lookup"><span data-stu-id="ed203-190">General Journals</span></span>|
|<span data-ttu-id="ed203-191">Vareposter</span><span class="sxs-lookup"><span data-stu-id="ed203-191">Item Entries</span></span>| <span data-ttu-id="ed203-192">Varekladder</span><span class="sxs-lookup"><span data-stu-id="ed203-192">Item Journals</span></span>|

<span data-ttu-id="ed203-193">I [!INCLUDE[d365fin](includes/d365fin_md.md)]er navnet på kladden for de migrerte dataene **C5MIGRATE**.</span><span class="sxs-lookup"><span data-stu-id="ed203-193">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the batch for the migrated data is named **C5MIGRATE**.</span></span>

## <a name="stopping-data-migration"></a><span data-ttu-id="ed203-194">Stoppe datamigrering</span><span class="sxs-lookup"><span data-stu-id="ed203-194">Stopping Data Migration</span></span>
<span data-ttu-id="ed203-195">Du kan stoppe datamigreringen ved å velge **Stopp alle migreringer**.</span><span class="sxs-lookup"><span data-stu-id="ed203-195">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="ed203-196">Hvis du gjør dette, blir alle ventende migreringer også stoppet.</span><span class="sxs-lookup"><span data-stu-id="ed203-196">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed203-197">Se også</span><span class="sxs-lookup"><span data-stu-id="ed203-197">See Also</span></span>
<span data-ttu-id="ed203-198">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="ed203-198">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="ed203-199">Komme i gang</span><span class="sxs-lookup"><span data-stu-id="ed203-199">Getting Started</span></span>](product-get-started.md) 

