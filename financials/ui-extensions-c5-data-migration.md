---
title: Bruke C5 Data Migration-utvidelsen | Microsoft-dokumentasjon
description: "Bruk denne utvidelsen til å overføre kunder, leverandører, varer og finanskonti fra Microsoft Dynamics C5 2012 til Financials."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 09/26/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 2d7d533662936116ffa40ded07b68e845fed810b
ms.contentlocale: nb-no
ms.lasthandoff: 11/10/2017

---

# <a name="the-c5-data-migration-extension-for-dynamics-365-for-finance-and-operations-business-edition"></a><span data-ttu-id="6c6b9-103">C5 Data Migration-utvidelsen for Dynamics 365 for Finance and Operations, Business Edition</span><span class="sxs-lookup"><span data-stu-id="6c6b9-103">The C5 Data Migration Extension for Dynamics 365 for Finance and Operations, Business Edition</span></span>
<span data-ttu-id="6c6b9-104">Denne utvidelsen gjør det enkelt å overføre kunder, leverandører, varer og konti fra Microsoft Dynamics C5 2012 til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6c6b9-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
  
> [!Note] 
> <span data-ttu-id="6c6b9-105">Selskapet i [!INCLUDE[d365fin](includes/d365fin_md.md)]kan ikke inneholde data.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-105">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="6c6b9-106">I tillegg, når du starter en migrering, bør du ikke opprette kunder, leverandører, varer eller kontoer til migreringen er ferdig.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-106">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="6c6b9-107">Migrere data</span><span class="sxs-lookup"><span data-stu-id="6c6b9-107">To migrate data</span></span>
<span data-ttu-id="6c6b9-108">Det tar kun noen få trinn å eksportere data fra C5 og importere dataen inn i [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="6c6b9-108">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  
  
1. <span data-ttu-id="6c6b9-109">I C5 bruker du **Eksportere databasen**-funksjonen for å eksportere dataene.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-109">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="6c6b9-110">Deretter sender du eksportmappen til en komprimert (pakket) mappe.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-110">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="6c6b9-111">I [!INCLUDE[d365fin](includes/d365fin_md.md)] velger du ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), så velger du **Datamigrering**, og så  **Datamigrering**.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-111">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="6c6b9-112">Fullfør trinnene i den assisterte oppsettsveiledningen.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-112">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="6c6b9-113">Pass på at du velger **Importer fra Microsoft Dynamcis C5 2012** som datakilde.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-113">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note] 
> <span data-ttu-id="6c6b9-114">Firmaer legger ofte til felt for å tilpasse C5 til deres bestemte bransjer.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-114">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="6c6b9-115"> flytter ikke data fra egendefinerte felt.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-115"> does not migrate data from custom fields.</span></span> <span data-ttu-id="6c6b9-116">Migreringen mislykkes også hvis du har flere enn 10 egendefinerte felt.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-116">Also, migration will fail if you have more than 10 custom fields.</span></span> 

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="6c6b9-117">Se statusen for migreringen</span><span class="sxs-lookup"><span data-stu-id="6c6b9-117">Viewing the Status of the Migration</span></span>
<span data-ttu-id="6c6b9-118">Bruk siden **Oversikt over datamigrering** for å overvåke migreringen.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-118">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="6c6b9-119">Siden viser informasjon om hvor mange enheter som er inkludert i migreringen, status til migreringen, antall varer som er migrert, og om migreringen var vellykket.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-119">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="6c6b9-120">Den viser også antall feil, gir deg mulighet til å undersøke hva som gikk feil, og gjør det enkelt å gå til enheten for å løse problemene.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-120">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="6c6b9-121">Hvis du vil ha mer informasjon, kan du se neste avsnitt i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-121">For more information, see the next section in this topic.</span></span> 

> [!Note] 
> <span data-ttu-id="6c6b9-122">Mens du venter på resultatet av overføringen, må du oppdatere siden for å vise resultatet.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-122">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="correcting-errors"></a><span data-ttu-id="6c6b9-123">Feilkorrigering</span><span class="sxs-lookup"><span data-stu-id="6c6b9-123">Correcting Errors</span></span>
<span data-ttu-id="6c6b9-124">Hvis det oppstår en feil, viser **Status**-feltet **Fullført med feil**, og **Feilantall** viser hvor mange feil som oppsto.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-124">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="6c6b9-125">For å se en oversikt over feilene, kan du åpne siden **Datamigreringsfeil** ved å velge:</span><span class="sxs-lookup"><span data-stu-id="6c6b9-125">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>

* <span data-ttu-id="6c6b9-126">Tallet i feltet **Feilantall** for enheten.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-126">The number in the **Error Count** field for the entity.</span></span> 
* <span data-ttu-id="6c6b9-127">Enheten og velg deretter handlingen **Vis feil**.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-127">The entity, and then the **Show Errors** action.</span></span> 

<span data-ttu-id="6c6b9-128">For å korrigere en feil kan du velge en feilmelding på siden **Datamigreringsfeil**, og deretter velge **Rediger post** for å åpne en side som inneholder den migrerte dataen til enheten.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-128">On the **Data Migration Errors** page, to fix an error you can choose an error message, then choose **Edit Record** to open a page that shows the migrated data for the entity.</span></span> <span data-ttu-id="6c6b9-129">Etter at du har korrigert én eller flere feil, kan du velge **Migrer** for å migrere enheten du har korrigert, uten å starte hele migrerringen på nytt.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-129">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="6c6b9-130">Hvis du har korrigert én eller flere feil, kan du bruke funksjonen **Velg mer** for å velge flere linjer til som skal migreres.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-130">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="6c6b9-131">Hvis det finnes feil som ikke er viktige å korrigere, kan du velge dem og så velge **Hopp over valg**.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-131">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="6c6b9-132">Hvis du har varer som er inkludert i en stykkliste, må du kanskje migrere mer enn én gang hvis den opprinnelige varen ikke er opprettet før variantene som refererer til den.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-132">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="6c6b9-133">Hvis en varevariant opprettes først, kan referansen til den opprinnelige varen føre til en feilmelding.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-133">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="6c6b9-134">Kontrollere dataene etter migrering</span><span class="sxs-lookup"><span data-stu-id="6c6b9-134">Verifying Data After Migrating</span></span> 
<span data-ttu-id="6c6b9-135">Hvis du vil kontrollere at dataene migrert riktig, kan du se på følgende sider i C5 og [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6c6b9-135">If you want to verify that your data migrated correctly, you can look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="6c6b9-136">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="6c6b9-136">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]|
|-----|-----|
|<span data-ttu-id="6c6b9-137">Kundeposter</span><span class="sxs-lookup"><span data-stu-id="6c6b9-137">Customer Entries</span></span>| <span data-ttu-id="6c6b9-138">Finanskladder</span><span class="sxs-lookup"><span data-stu-id="6c6b9-138">General Journals</span></span>|
|<span data-ttu-id="6c6b9-139">Leverandørposter</span><span class="sxs-lookup"><span data-stu-id="6c6b9-139">Vendor Entries</span></span>| <span data-ttu-id="6c6b9-140">Finanskladder</span><span class="sxs-lookup"><span data-stu-id="6c6b9-140">General Journals</span></span>|
|<span data-ttu-id="6c6b9-141">Vareposter</span><span class="sxs-lookup"><span data-stu-id="6c6b9-141">Item Entries</span></span>| <span data-ttu-id="6c6b9-142">Varekladder</span><span class="sxs-lookup"><span data-stu-id="6c6b9-142">Item Journals</span></span>|

<span data-ttu-id="6c6b9-143">I [!INCLUDE[d365fin](includes/d365fin_md.md)]er navnet på kladden for de migrerte dataene **C5MIGRATE**.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-143">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the batch for the migrated data is named **C5MIGRATE**.</span></span> 

## <a name="stopping-data-migration"></a><span data-ttu-id="6c6b9-144">Stoppe datamigrering</span><span class="sxs-lookup"><span data-stu-id="6c6b9-144">Stopping Data Migration</span></span>
<span data-ttu-id="6c6b9-145">Du kan stoppe datamigreringen ved å velge **Stopp alle migreringer**.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-145">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="6c6b9-146">Hvis du gjør dette, blir alle ventende migreringer også stoppet.</span><span class="sxs-lookup"><span data-stu-id="6c6b9-146">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c6b9-147">Se også</span><span class="sxs-lookup"><span data-stu-id="6c6b9-147">See Also</span></span>
<span data-ttu-id="6c6b9-148">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="6c6b9-148">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="6c6b9-149">[Velkommen til [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="6c6b9-149">[Welcome to [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span></span>  

