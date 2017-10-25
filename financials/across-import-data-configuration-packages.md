---
title: "Bruke Excel til å importere data til Financials | Microsoft-dokumentasjon"
description: "Bruk standard konfigurasjonspakke til å legge kundedata i Excel og importere dataene tilbake til Dynamics 365 for Financials."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 07/05/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2a38dc36cb9ff609c5582acd489841b20013d4bc
ms.openlocfilehash: 8cf36afea60b089afac8f1c27d126cd19b88ce94
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a><span data-ttu-id="ef7fe-103">Importere data fra eldre regnskapsprogramvare ved hjelp av en konfigurasjonspakke</span><span class="sxs-lookup"><span data-stu-id="ef7fe-103">Importing Data from Legacy Accounting Software using a Configuration Package</span></span>
<span data-ttu-id="ef7fe-104">Du kan importere hoveddata og noen transaksjonsdata fra andre finanssystemer som er basert på standard konfigurasjonspakke i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ef7fe-104">You can import master data and some transactional data from other finance systems based on the default configuration package in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="ef7fe-105">I vinduet **Konfigurasjonspakker** kan du arbeide med pakken for å importere og validere dataene før du bruker pakken.</span><span class="sxs-lookup"><span data-stu-id="ef7fe-105">In the **Configuration Packages** window, you can work with the package to import and validate the data before you apply the package.</span></span>  

<span data-ttu-id="ef7fe-106">Hvis du er kjent med RapidStart-tjenester for Microsoft Dynamics, er du også kjent med konfigurasjonspakker.</span><span class="sxs-lookup"><span data-stu-id="ef7fe-106">If you are familiar with RapidStart Services for Microsoft Dynamics, you are also familiar with configuration packages.</span></span> <span data-ttu-id="ef7fe-107">Standard konfigurasjonspakke støtter de fleste vanlige typer data som du vil importere fra et eldre system.</span><span class="sxs-lookup"><span data-stu-id="ef7fe-107">The default configuration package supports the most common types of data that you want to import from a legacy system.</span></span> <span data-ttu-id="ef7fe-108">I Excel kan du deretter legge til data fra det gamle systemet og konfigurere dem i henhold til forretningslogikken i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ef7fe-108">In Excel, you can then add the data from the legacy system and set it up according to the business logic of the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

> [!TIP]  
>   <span data-ttu-id="ef7fe-109">Du kan også bruke veivisere for datamigrering til å importere data fra QuickBooks eller Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="ef7fe-109">Alternatively, use data migration wizards to import data from QuickBooks or Dynamics GP.</span></span> <span data-ttu-id="ef7fe-110">Hvis du vil ha mer informasjon, kan du se [Datamigrering for QuickBooks](ui-extensions-quickbooks-data-migration.md) eller [Dynamics GP-datamigrering](ui-extensions-dynamicsgp-data-migration.md).</span><span class="sxs-lookup"><span data-stu-id="ef7fe-110">For more information, see [QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md) or [Dynamics GP Data Migration](ui-extensions-dynamicsgp-data-migration.md).</span></span>  

## <a name="working-with-data-in-excel"></a><span data-ttu-id="ef7fe-111">Arbeide med data i Excel</span><span class="sxs-lookup"><span data-stu-id="ef7fe-111">Working with Data in Excel</span></span>
<span data-ttu-id="ef7fe-112">Når du eksporterer standard konfigurasjonspakke til Excel, inneholder generert arbeidsboken et regneark for hver tabell i pakken.</span><span class="sxs-lookup"><span data-stu-id="ef7fe-112">When you export the default configuration package to Excel, the generated workbook contains a worksheet for each table in the package.</span></span> <span data-ttu-id="ef7fe-113">Du kan forenkle oppgavene ved å bruke verktøyene for XML-manipulering i Excel.</span><span class="sxs-lookup"><span data-stu-id="ef7fe-113">To simplify your tasks, you can take advantage of the XML manipulation tools that are built into Excel.</span></span> <span data-ttu-id="ef7fe-114">Du kan også bruke innebygde Excel-funksjoner for å få hjelp med dataformatering og plassering av data i riktig celle.</span><span class="sxs-lookup"><span data-stu-id="ef7fe-114">You can also use Excel built-in functions to help with data formatting and to put data in the correct cell.</span></span> <span data-ttu-id="ef7fe-115">Du kan for eksempel legge til et tomt regneark og kopiere de gamle dataene til det.</span><span class="sxs-lookup"><span data-stu-id="ef7fe-115">For example, add a blank worksheet and copy the legacy data to it.</span></span> <span data-ttu-id="ef7fe-116">Lag deretter en Excel-formel til å tilordne data i transformasjonsregnearket mellom feltene i det eksporterte regnearket og eldre kundedata.</span><span class="sxs-lookup"><span data-stu-id="ef7fe-116">Then make an Excel formula to map data in the transformation worksheet between the fields in the exported worksheet and customer legacy data.</span></span> <span data-ttu-id="ef7fe-117">Når du har tilordnet alle dataene, kan du kopiere dataområdet til tabellforslaget.</span><span class="sxs-lookup"><span data-stu-id="ef7fe-117">After you have mapped all of the data, copy the range of data onto the table worksheet.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="ef7fe-118">Ikke endre kolonnene i forslagene.</span><span class="sxs-lookup"><span data-stu-id="ef7fe-118">Do not change the columns in the worksheets.</span></span> <span data-ttu-id="ef7fe-119">Hvis du flytter, endrer eller sletter dem, kan ikke regnearket importeres til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ef7fe-119">If they are moved, changed, or deleted, the worksheet cannot be imported into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="tables-in-the-default-configuration-package"></a><span data-ttu-id="ef7fe-120">Tabeller i standard konfigurasjonspakke</span><span class="sxs-lookup"><span data-stu-id="ef7fe-120">Tables in the Default Configuration Package</span></span>
<span data-ttu-id="ef7fe-121">Standard konfigurasjonspakke støtter følgende tabeller:</span><span class="sxs-lookup"><span data-stu-id="ef7fe-121">The default configuration package supports the following tables:</span></span>

-   <span data-ttu-id="ef7fe-122">Betalingsbetingelser</span><span class="sxs-lookup"><span data-stu-id="ef7fe-122">Payment Terms</span></span>
-   <span data-ttu-id="ef7fe-123">Kundeprisgruppe</span><span class="sxs-lookup"><span data-stu-id="ef7fe-123">Customer Price Group</span></span>
-   <span data-ttu-id="ef7fe-124">Leveringsmåte</span><span class="sxs-lookup"><span data-stu-id="ef7fe-124">Shipment Method</span></span>
-   <span data-ttu-id="ef7fe-125">Selger/innkjøper</span><span class="sxs-lookup"><span data-stu-id="ef7fe-125">Salesperson/Purchaser</span></span>
-   <span data-ttu-id="ef7fe-126">Lokasjon</span><span class="sxs-lookup"><span data-stu-id="ef7fe-126">Location</span></span>
-   <span data-ttu-id="ef7fe-127">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="ef7fe-127">GL Account</span></span>
-   <span data-ttu-id="ef7fe-128">Kunde</span><span class="sxs-lookup"><span data-stu-id="ef7fe-128">Customer</span></span>
-   <span data-ttu-id="ef7fe-129">Leverandør</span><span class="sxs-lookup"><span data-stu-id="ef7fe-129">Vendor</span></span>
-   <span data-ttu-id="ef7fe-130">Element</span><span class="sxs-lookup"><span data-stu-id="ef7fe-130">Item</span></span>
-   <span data-ttu-id="ef7fe-131">Salgshode</span><span class="sxs-lookup"><span data-stu-id="ef7fe-131">Sales Header</span></span>
-   <span data-ttu-id="ef7fe-132">Salgslinje</span><span class="sxs-lookup"><span data-stu-id="ef7fe-132">Sales Line</span></span>
-   <span data-ttu-id="ef7fe-133">Bestillingshode</span><span class="sxs-lookup"><span data-stu-id="ef7fe-133">Purchase Header</span></span>
-   <span data-ttu-id="ef7fe-134">Bestillingslinje</span><span class="sxs-lookup"><span data-stu-id="ef7fe-134">Purchase Line</span></span>
-   <span data-ttu-id="ef7fe-135">Finanskladdelinje</span><span class="sxs-lookup"><span data-stu-id="ef7fe-135">Gen. Journal Line</span></span>
-   <span data-ttu-id="ef7fe-136">Varekladdelinje</span><span class="sxs-lookup"><span data-stu-id="ef7fe-136">Item Journal Line</span></span>
-   <span data-ttu-id="ef7fe-137">Bokføringsgruppe - kunde</span><span class="sxs-lookup"><span data-stu-id="ef7fe-137">Customer Posting Group</span></span>
-   <span data-ttu-id="ef7fe-138">Bokføringsgruppe - leverandør</span><span class="sxs-lookup"><span data-stu-id="ef7fe-138">Vendor Posting Group</span></span>
-   <span data-ttu-id="ef7fe-139">Bokføringsgruppe - lager</span><span class="sxs-lookup"><span data-stu-id="ef7fe-139">Inventory Posting Group</span></span>
-   <span data-ttu-id="ef7fe-140">Enht.</span><span class="sxs-lookup"><span data-stu-id="ef7fe-140">Unit of Measure</span></span>
-   <span data-ttu-id="ef7fe-141">Bokføringsgruppe - firma</span><span class="sxs-lookup"><span data-stu-id="ef7fe-141">Gen. Business Posting Group</span></span>
-   <span data-ttu-id="ef7fe-142">Bokføringsgruppe - vare</span><span class="sxs-lookup"><span data-stu-id="ef7fe-142">Gen. Product Posting Group</span></span>
-   <span data-ttu-id="ef7fe-143">Generelt bokføringsoppsett</span><span class="sxs-lookup"><span data-stu-id="ef7fe-143">General Posting Setup</span></span>
-   <span data-ttu-id="ef7fe-144">Distrikt</span><span class="sxs-lookup"><span data-stu-id="ef7fe-144">Territory</span></span>
-   <span data-ttu-id="ef7fe-145">Varekategori</span><span class="sxs-lookup"><span data-stu-id="ef7fe-145">Item Category</span></span>
-   <span data-ttu-id="ef7fe-146">Salgspris</span><span class="sxs-lookup"><span data-stu-id="ef7fe-146">Sales Price</span></span>
-   <span data-ttu-id="ef7fe-147">Kjøpspris</span><span class="sxs-lookup"><span data-stu-id="ef7fe-147">Purchase Price</span></span>

## <a name="importing-customer-data"></a><span data-ttu-id="ef7fe-148">Importere kundedata</span><span class="sxs-lookup"><span data-stu-id="ef7fe-148">Importing Customer Data</span></span>
<span data-ttu-id="ef7fe-149">Når kundedataene er angitt i Excel, importerer du dataee til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ef7fe-149">After the customer data has been entered in Excel, you import the data into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="ef7fe-150">I vinduet **Konfigurasjonspakker** importerer du data fra Excel-filen, og du kan bekrefte at dataene er i samsvar med [!INCLUDE[d365fin](includes/d365fin_md.md)] før du installerer pakken.</span><span class="sxs-lookup"><span data-stu-id="ef7fe-150">In the **Configuration Packages** window, you import the data from the Excel file, and you can validate that the data is consistent with [!INCLUDE[d365fin](includes/d365fin_md.md)] before you apply the package.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef7fe-151">Se også</span><span class="sxs-lookup"><span data-stu-id="ef7fe-151">See Also</span></span>
[<span data-ttu-id="ef7fe-152">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="ef7fe-152">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
[<span data-ttu-id="ef7fe-153">Datamigrering for QuickBooks</span><span class="sxs-lookup"><span data-stu-id="ef7fe-153">QuickBooks Data Migration</span></span>](ui-extensions-quickbooks-data-migration.md)  
[<span data-ttu-id="ef7fe-154">Dynamics GP-datamigrering</span><span class="sxs-lookup"><span data-stu-id="ef7fe-154">Dynamics GP Data Migration</span></span>](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

