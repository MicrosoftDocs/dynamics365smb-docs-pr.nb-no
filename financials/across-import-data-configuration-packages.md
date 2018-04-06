---
title: "Bruke Excel til å importere data til Financials | Microsoft-dokumentasjon"
description: "Bruk standard konfigurasjonspakke til å legge kundedata i Excel og importere dataene tilbake til Finance and Operations, Business edition."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 03/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 591d8100100ee717a932d188a87545fe4098a001
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a><span data-ttu-id="c5121-103">Importere data fra eldre regnskapsprogramvare ved hjelp av en konfigurasjonspakke</span><span class="sxs-lookup"><span data-stu-id="c5121-103">Importing Data from Legacy Accounting Software using a Configuration Package</span></span>
<span data-ttu-id="c5121-104">Du kan importere hoveddata og noen transaksjonsdata fra andre finanssystemer som er basert på standard konfigurasjonspakke i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c5121-104">You can import master data and some transactional data from other finance systems based on the default configuration package in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="c5121-105">I vinduet **Konfigurasjonspakker** kan du arbeide med pakken for å importere og validere dataene før du bruker pakken.</span><span class="sxs-lookup"><span data-stu-id="c5121-105">In the **Configuration Packages** window, you can work with the package to import and validate the data before you apply the package.</span></span>  

> [!NOTE]  
> <span data-ttu-id="c5121-106">Konfigurasjonpakker er en del av RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], et omfattende verktøy for å definere nye løsninger basert på kundens forretningskrav og oppsettsdata.</span><span class="sxs-lookup"><span data-stu-id="c5121-106">Configuration packages are part of RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], an extensive toolkit for setting up new solutions based on customers' business requirements and setup data.</span></span> <span data-ttu-id="c5121-107">RapidStart Services har dessuten funksjoner for import av eldre data.</span><span class="sxs-lookup"><span data-stu-id="c5121-107">RapidStart Services also offers functionality for import of legacy data.</span></span> <span data-ttu-id="c5121-108">Hvis du vil ha mer informasjon, kan du se [Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span><span class="sxs-lookup"><span data-stu-id="c5121-108">For more information, see [Setting Up a Company With RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span></span>

> [!TIP]  
>   <span data-ttu-id="c5121-109">Du kan også bruke veivisere for datamigrering til å importere data fra QuickBooks eller Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="c5121-109">Alternatively, use data migration wizards to import data from QuickBooks or Dynamics GP.</span></span> <span data-ttu-id="c5121-110">Hvis du vil ha mer informasjon, kan du se [Datamigrering for QuickBooks](ui-extensions-quickbooks-data-migration.md) eller [Dynamics GP-datamigrering](ui-extensions-dynamicsgp-data-migration.md).</span><span class="sxs-lookup"><span data-stu-id="c5121-110">For more information, see [QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md) or [Dynamics GP Data Migration](ui-extensions-dynamicsgp-data-migration.md).</span></span>  

## <a name="working-with-data-in-excel"></a><span data-ttu-id="c5121-111">Arbeide med data i Excel</span><span class="sxs-lookup"><span data-stu-id="c5121-111">Working with Data in Excel</span></span>
<span data-ttu-id="c5121-112">Når du eksporterer standard konfigurasjonspakke til Excel, inneholder generert arbeidsboken et regneark for hver tabell i pakken.</span><span class="sxs-lookup"><span data-stu-id="c5121-112">When you export the default configuration package to Excel, the generated workbook contains a worksheet for each table in the package.</span></span> <span data-ttu-id="c5121-113">Du kan forenkle oppgavene ved å bruke verktøyene for XML-manipulering i Excel.</span><span class="sxs-lookup"><span data-stu-id="c5121-113">To simplify your tasks, you can take advantage of the XML manipulation tools that are built into Excel.</span></span> <span data-ttu-id="c5121-114">Du kan også bruke innebygde Excel-funksjoner for å få hjelp med dataformatering og plassering av data i riktig celle.</span><span class="sxs-lookup"><span data-stu-id="c5121-114">You can also use Excel built-in functions to help with data formatting and to put data in the correct cell.</span></span> <span data-ttu-id="c5121-115">Du kan for eksempel legge til et tomt regneark og kopiere de gamle dataene til det.</span><span class="sxs-lookup"><span data-stu-id="c5121-115">For example, add a blank worksheet and copy the legacy data to it.</span></span> <span data-ttu-id="c5121-116">Lag deretter en Excel-formel til å tilordne data i transformasjonsregnearket mellom feltene i det eksporterte regnearket og eldre kundedata.</span><span class="sxs-lookup"><span data-stu-id="c5121-116">Then make an Excel formula to map data in the transformation worksheet between the fields in the exported worksheet and customer legacy data.</span></span> <span data-ttu-id="c5121-117">Når du har tilordnet alle dataene, kan du kopiere dataområdet til tabellforslaget.</span><span class="sxs-lookup"><span data-stu-id="c5121-117">After you have mapped all of the data, copy the range of data onto the table worksheet.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="c5121-118">Ikke endre kolonnene i forslagene.</span><span class="sxs-lookup"><span data-stu-id="c5121-118">Do not change the columns in the worksheets.</span></span> <span data-ttu-id="c5121-119">Hvis du flytter, endrer eller sletter dem, kan ikke regnearket importeres til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c5121-119">If they are moved, changed, or deleted, the worksheet cannot be imported into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="tables-in-the-default-configuration-package"></a><span data-ttu-id="c5121-120">Tabeller i standard konfigurasjonspakke</span><span class="sxs-lookup"><span data-stu-id="c5121-120">Tables in the Default Configuration Package</span></span>
<span data-ttu-id="c5121-121">Standard konfigurasjonspakke støtter følgende tabeller:</span><span class="sxs-lookup"><span data-stu-id="c5121-121">The default configuration package supports the following tables:</span></span>

-   <span data-ttu-id="c5121-122">Betalingsbetingelser</span><span class="sxs-lookup"><span data-stu-id="c5121-122">Payment Terms</span></span>
-   <span data-ttu-id="c5121-123">Kundeprisgruppe</span><span class="sxs-lookup"><span data-stu-id="c5121-123">Customer Price Group</span></span>
-   <span data-ttu-id="c5121-124">Leveringsmåte</span><span class="sxs-lookup"><span data-stu-id="c5121-124">Shipment Method</span></span>
-   <span data-ttu-id="c5121-125">Selger/innkjøper</span><span class="sxs-lookup"><span data-stu-id="c5121-125">Salesperson/Purchaser</span></span>
-   <span data-ttu-id="c5121-126">Lokasjon</span><span class="sxs-lookup"><span data-stu-id="c5121-126">Location</span></span>
-   <span data-ttu-id="c5121-127">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="c5121-127">GL Account</span></span>
-   <span data-ttu-id="c5121-128">Kunde</span><span class="sxs-lookup"><span data-stu-id="c5121-128">Customer</span></span>
-   <span data-ttu-id="c5121-129">Leverandør</span><span class="sxs-lookup"><span data-stu-id="c5121-129">Vendor</span></span>
-   <span data-ttu-id="c5121-130">Element</span><span class="sxs-lookup"><span data-stu-id="c5121-130">Item</span></span>
-   <span data-ttu-id="c5121-131">Salgshode</span><span class="sxs-lookup"><span data-stu-id="c5121-131">Sales Header</span></span>
-   <span data-ttu-id="c5121-132">Salgslinje</span><span class="sxs-lookup"><span data-stu-id="c5121-132">Sales Line</span></span>
-   <span data-ttu-id="c5121-133">Bestillingshode</span><span class="sxs-lookup"><span data-stu-id="c5121-133">Purchase Header</span></span>
-   <span data-ttu-id="c5121-134">Bestillingslinje</span><span class="sxs-lookup"><span data-stu-id="c5121-134">Purchase Line</span></span>
-   <span data-ttu-id="c5121-135">Finanskladdelinje</span><span class="sxs-lookup"><span data-stu-id="c5121-135">Gen. Journal Line</span></span>
-   <span data-ttu-id="c5121-136">Varekladdelinje</span><span class="sxs-lookup"><span data-stu-id="c5121-136">Item Journal Line</span></span>
-   <span data-ttu-id="c5121-137">Bokføringsgruppe - kunde</span><span class="sxs-lookup"><span data-stu-id="c5121-137">Customer Posting Group</span></span>
-   <span data-ttu-id="c5121-138">Bokføringsgruppe - leverandør</span><span class="sxs-lookup"><span data-stu-id="c5121-138">Vendor Posting Group</span></span>
-   <span data-ttu-id="c5121-139">Bokføringsgruppe - lager</span><span class="sxs-lookup"><span data-stu-id="c5121-139">Inventory Posting Group</span></span>
-   <span data-ttu-id="c5121-140">Enht.</span><span class="sxs-lookup"><span data-stu-id="c5121-140">Unit of Measure</span></span>
-   <span data-ttu-id="c5121-141">Bokføringsgruppe - firma</span><span class="sxs-lookup"><span data-stu-id="c5121-141">Gen. Business Posting Group</span></span>
-   <span data-ttu-id="c5121-142">Bokføringsgruppe - vare</span><span class="sxs-lookup"><span data-stu-id="c5121-142">Gen. Product Posting Group</span></span>
-   <span data-ttu-id="c5121-143">Generelt bokføringsoppsett</span><span class="sxs-lookup"><span data-stu-id="c5121-143">General Posting Setup</span></span>
-   <span data-ttu-id="c5121-144">Distrikt</span><span class="sxs-lookup"><span data-stu-id="c5121-144">Territory</span></span>
-   <span data-ttu-id="c5121-145">Varekategori</span><span class="sxs-lookup"><span data-stu-id="c5121-145">Item Category</span></span>
-   <span data-ttu-id="c5121-146">Salgspris</span><span class="sxs-lookup"><span data-stu-id="c5121-146">Sales Price</span></span>
-   <span data-ttu-id="c5121-147">Kjøpspris</span><span class="sxs-lookup"><span data-stu-id="c5121-147">Purchase Price</span></span>

## <a name="importing-customer-data"></a><span data-ttu-id="c5121-148">Importere kundedata</span><span class="sxs-lookup"><span data-stu-id="c5121-148">Importing Customer Data</span></span>
<span data-ttu-id="c5121-149">Når kundedataene er angitt i Excel, importerer du dataee til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c5121-149">After the customer data has been entered in Excel, you import the data into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="c5121-150">I vinduet **Konfigurasjonspakker** importerer du data fra Excel-filen, og du kan bekrefte at dataene er i samsvar med [!INCLUDE[d365fin](includes/d365fin_md.md)] før du installerer pakken.</span><span class="sxs-lookup"><span data-stu-id="c5121-150">In the **Configuration Packages** window, you import the data from the Excel file, and you can validate that the data is consistent with [!INCLUDE[d365fin](includes/d365fin_md.md)] before you apply the package.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5121-151">Se også</span><span class="sxs-lookup"><span data-stu-id="c5121-151">See Also</span></span>
[<span data-ttu-id="c5121-152">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="c5121-152">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
[<span data-ttu-id="c5121-153">Konfigurere et selskap med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="c5121-153">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="c5121-154">Datamigrering for QuickBooks</span><span class="sxs-lookup"><span data-stu-id="c5121-154">QuickBooks Data Migration</span></span>](ui-extensions-quickbooks-data-migration.md)  
[<span data-ttu-id="c5121-155">Dynamics GP-datamigrering</span><span class="sxs-lookup"><span data-stu-id="c5121-155">Dynamics GP Data Migration</span></span>](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

