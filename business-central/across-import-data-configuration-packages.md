---
title: "Bruke Excel til å importere data til Business Central | Microsoft-dokumentasjon"
description: "Bruk standard konfigurasjonspakke til å legge kundedata i Excel og importere dataene tilbake til Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: f5ca69c1e542a9b5846c99b03103fd9b2be86499
ms.contentlocale: nb-no
ms.lasthandoff: 11/26/2018

---
# <a name="importing-business-data-from-other-finance-systems"></a><span data-ttu-id="deb97-103">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="deb97-103">Importing Business Data from Other Finance Systems</span></span>
<span data-ttu-id="deb97-104">Når du registrerer deg for [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du velge å opprette et tomt firma, slik at du kan laste opp dine egne data og teste det nye [!INCLUDE[d365fin](includes/d365fin_md.md)]-firmaet.</span><span class="sxs-lookup"><span data-stu-id="deb97-104">When you sign up for [!INCLUDE[d365fin](includes/d365fin_md.md)], you can choose to create an empty company so that you can upload your own data and to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="deb97-105">Avhengig av økonomiløsning som selskapet ditt bruker i dag, kan du overføre informasjon om kunder, leverandører, lager og bankkonti.</span><span class="sxs-lookup"><span data-stu-id="deb97-105">Depending on the finance solution that your business uses today, you can transfer information about customers, vendors, inventory, and bank accounts.</span></span>  

<span data-ttu-id="deb97-106">Fra Rollesenteret kan du starte en assistert oppsettsveiledning som hjelper deg med å overføre forretningsdata fra en Excel-fil eller fra andre formater.</span><span class="sxs-lookup"><span data-stu-id="deb97-106">From the Role Center, you can start an assisted setup guide that helps you transfer the business data from an Excel file or from other formats.</span></span> <span data-ttu-id="deb97-107">Filtypene du kan laste opp, avhenger av utvidelsene som er tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="deb97-107">The type of files you can upload depends on the extensions that are available.</span></span> <span data-ttu-id="deb97-108">Du kan for eksempel overføre opp data fra QuickBooks fordi [!INCLUDE[d365fin](includes/d365fin_md.md)] inneholder en utvidelse som håndterer konverteringen fra QuickBooks.</span><span class="sxs-lookup"><span data-stu-id="deb97-108">For example, you can migrate data from QuickBooks because [!INCLUDE[d365fin](includes/d365fin_md.md)] includes an extension that handles the conversion from QuickBooks.</span></span> <span data-ttu-id="deb97-109">Hvis du vil overføre data fra andre økonomiløsninger, må du kontrollere om en utvidelse er tilgjengelig for denne løsningen eller importere fra Excel.</span><span class="sxs-lookup"><span data-stu-id="deb97-109">If you want to migrate data from other finance solutions, you must either check if an extension is available for that solution or import from Excel.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="deb97-110">inneholder maler for kontoer, kunder, leverandører og lagervarer, som du kan velge å bruke når du importerer dataene.</span><span class="sxs-lookup"><span data-stu-id="deb97-110">includes templates for accounts, customers, vendors, and inventory items that you can choose to apply when you import your data.</span></span>

<span data-ttu-id="deb97-111">Du kan importere hoveddata og noen transaksjonsdata fra andre finanssystemer som er basert på standard konfigurasjonspakke i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="deb97-111">You can import master data and some transactional data from other finance systems based on the default configuration package in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="deb97-112">På siden **Konfigurasjonspakker** kan du arbeide med pakken for å importere og validere dataene før du bruker pakken.</span><span class="sxs-lookup"><span data-stu-id="deb97-112">On the **Configuration Packages** page, you can work with the package to import and validate the data before you apply the package.</span></span>  

> [!TIP]  
> <span data-ttu-id="deb97-113">Du kan også bruke veivisere for datamigrering til å importere data fra QuickBooks eller Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="deb97-113">Alternatively, use data migration wizards to import data from QuickBooks or Dynamics GP.</span></span> <span data-ttu-id="deb97-114">Hvis du vil ha mer informasjon, kan du se [Datamigrering for QuickBooks](ui-extensions-quickbooks-data-migration.md) eller [Dynamics GP-datamigrering](ui-extensions-dynamicsgp-data-migration.md).</span><span class="sxs-lookup"><span data-stu-id="deb97-114">For more information, see [QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md) or [Dynamics GP Data Migration](ui-extensions-dynamicsgp-data-migration.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="deb97-115">For omfattende implementasjonsarbeid kan du bruke RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], et omfattende verktøy for å definere nye løsninger basert på kundens forretningskrav og oppsettsdata.</span><span class="sxs-lookup"><span data-stu-id="deb97-115">For larger implementation work, you can use RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], which is an extensive toolkit for setting up new solutions based on customers' business requirements and setup data.</span></span> <span data-ttu-id="deb97-116">RapidStart Services har dessuten funksjoner for import av forretningsdata.</span><span class="sxs-lookup"><span data-stu-id="deb97-116">RapidStart Services also offers functionality for import of business data.</span></span> <span data-ttu-id="deb97-117">Hvis du vil ha mer informasjon, kan du se [Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span><span class="sxs-lookup"><span data-stu-id="deb97-117">For more information, see [Setting Up a Company With RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span></span>

## <a name="importing-data-from-configuration-packages"></a><span data-ttu-id="deb97-118">Importere data fra konfigurasjonspakker</span><span class="sxs-lookup"><span data-stu-id="deb97-118">Importing Data from Configuration Packages</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="deb97-119">inkluderer en konfigurasjonspakke som du kan eksportere til Excel og definere dataene der.</span><span class="sxs-lookup"><span data-stu-id="deb97-119">includes a configuration package that you can export to Excel and set up your data there.</span></span> <span data-ttu-id="deb97-120">Deretter kan du importere dataene fra Excel på nytt.</span><span class="sxs-lookup"><span data-stu-id="deb97-120">Then, you can import the data from Excel again.</span></span> <span data-ttu-id="deb97-121">Pakken består av 27 tabeller, inkludert hoveddata som kunder, leverandører, varer, og kontoer, andre grunnleggende oppsettstabeller, for eksempel frakt og transaksjonerstabeller, som salgshode og linjer.</span><span class="sxs-lookup"><span data-stu-id="deb97-121">The package consists of 27 tables, including master data such as customers, vendors, items, and accounts, other basic setup tables such as shipping methods, and transactions tables such as sales header and lines.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="deb97-122">Arbeide med konfigurasjonspakker er avanserte funksjoner, og vi anbefaler at du kontakter systemansvarlig.</span><span class="sxs-lookup"><span data-stu-id="deb97-122">Working with configuration packages is advanced functionality, and we recommend that you contact your administrator.</span></span> <span data-ttu-id="deb97-123">For mer informasjon, se [Importere data fra eldre regnskapsprogramvare ved hjelp av en konfigurasjonspakke](across-import-data-configuration-packages.md).</span><span class="sxs-lookup"><span data-stu-id="deb97-123">For more information, see [Importing Data from Legacy Accounting Software using a Configuration Package](across-import-data-configuration-packages.md).</span></span>

## <a name="working-with-data-in-excel"></a><span data-ttu-id="deb97-124">Arbeide med data i Excel</span><span class="sxs-lookup"><span data-stu-id="deb97-124">Working with Data in Excel</span></span>
<span data-ttu-id="deb97-125">Når du eksporterer standard konfigurasjonspakke til Excel, inneholder generert arbeidsboken et regneark for hver tabell i pakken.</span><span class="sxs-lookup"><span data-stu-id="deb97-125">When you export the default configuration package to Excel, the generated workbook contains a worksheet for each table in the package.</span></span> <span data-ttu-id="deb97-126">Du kan forenkle oppgavene ved å bruke verktøyene for XML-manipulering i Excel.</span><span class="sxs-lookup"><span data-stu-id="deb97-126">To simplify your tasks, you can take advantage of the XML manipulation tools that are built into Excel.</span></span> <span data-ttu-id="deb97-127">Du kan også bruke innebygde Excel-funksjoner for å få hjelp med dataformatering og plassering av data i riktig celle.</span><span class="sxs-lookup"><span data-stu-id="deb97-127">You can also use Excel built-in functions to help with data formatting and to put data in the correct cell.</span></span> <span data-ttu-id="deb97-128">Du kan for eksempel legge til et tomt regneark og kopiere de gamle dataene til det.</span><span class="sxs-lookup"><span data-stu-id="deb97-128">For example, add a blank worksheet and copy the legacy data to it.</span></span> <span data-ttu-id="deb97-129">Lag deretter en Excel-formel til å tilordne data i transformasjonsregnearket mellom feltene i det eksporterte regnearket og eldre kundedata.</span><span class="sxs-lookup"><span data-stu-id="deb97-129">Then make an Excel formula to map data in the transformation worksheet between the fields in the exported worksheet and customer legacy data.</span></span> <span data-ttu-id="deb97-130">Når du har tilordnet alle dataene, kan du kopiere dataområdet til tabellforslaget.</span><span class="sxs-lookup"><span data-stu-id="deb97-130">After you have mapped all of the data, copy the range of data onto the table worksheet.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="deb97-131">Ikke endre kolonnene i forslagene.</span><span class="sxs-lookup"><span data-stu-id="deb97-131">Do not change the columns in the worksheets.</span></span> <span data-ttu-id="deb97-132">Hvis du flytter, endrer eller sletter dem, kan ikke regnearket importeres til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="deb97-132">If they are moved, changed, or deleted, the worksheet cannot be imported into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="tables-in-the-default-configuration-package"></a><span data-ttu-id="deb97-133">Tabeller i standard konfigurasjonspakke</span><span class="sxs-lookup"><span data-stu-id="deb97-133">Tables in the Default Configuration Package</span></span>
<span data-ttu-id="deb97-134">Standard konfigurasjonspakke støtter følgende tabeller:</span><span class="sxs-lookup"><span data-stu-id="deb97-134">The default configuration package supports the following tables:</span></span>

-   <span data-ttu-id="deb97-135">Betalingsbetingelser</span><span class="sxs-lookup"><span data-stu-id="deb97-135">Payment Terms</span></span>
-   <span data-ttu-id="deb97-136">Kundeprisgruppe</span><span class="sxs-lookup"><span data-stu-id="deb97-136">Customer Price Group</span></span>
-   <span data-ttu-id="deb97-137">Leveringsmåte</span><span class="sxs-lookup"><span data-stu-id="deb97-137">Shipment Method</span></span>
-   <span data-ttu-id="deb97-138">Selger/innkjøper</span><span class="sxs-lookup"><span data-stu-id="deb97-138">Salesperson/Purchaser</span></span>
-   <span data-ttu-id="deb97-139">Lokasjon</span><span class="sxs-lookup"><span data-stu-id="deb97-139">Location</span></span>
-   <span data-ttu-id="deb97-140">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="deb97-140">GL Account</span></span>
-   <span data-ttu-id="deb97-141">Kunde</span><span class="sxs-lookup"><span data-stu-id="deb97-141">Customer</span></span>
-   <span data-ttu-id="deb97-142">Leverandør</span><span class="sxs-lookup"><span data-stu-id="deb97-142">Vendor</span></span>
-   <span data-ttu-id="deb97-143">Element</span><span class="sxs-lookup"><span data-stu-id="deb97-143">Item</span></span>
-   <span data-ttu-id="deb97-144">Salgshode</span><span class="sxs-lookup"><span data-stu-id="deb97-144">Sales Header</span></span>
-   <span data-ttu-id="deb97-145">Salgslinje</span><span class="sxs-lookup"><span data-stu-id="deb97-145">Sales Line</span></span>
-   <span data-ttu-id="deb97-146">Bestillingshode</span><span class="sxs-lookup"><span data-stu-id="deb97-146">Purchase Header</span></span>
-   <span data-ttu-id="deb97-147">Bestillingslinje</span><span class="sxs-lookup"><span data-stu-id="deb97-147">Purchase Line</span></span>
-   <span data-ttu-id="deb97-148">Finanskladdelinje</span><span class="sxs-lookup"><span data-stu-id="deb97-148">Gen. Journal Line</span></span>
-   <span data-ttu-id="deb97-149">Varekladdelinje</span><span class="sxs-lookup"><span data-stu-id="deb97-149">Item Journal Line</span></span>
-   <span data-ttu-id="deb97-150">Bokføringsgruppe - kunde</span><span class="sxs-lookup"><span data-stu-id="deb97-150">Customer Posting Group</span></span>
-   <span data-ttu-id="deb97-151">Bokføringsgruppe - leverandør</span><span class="sxs-lookup"><span data-stu-id="deb97-151">Vendor Posting Group</span></span>
-   <span data-ttu-id="deb97-152">Bokføringsgruppe - lager</span><span class="sxs-lookup"><span data-stu-id="deb97-152">Inventory Posting Group</span></span>
-   <span data-ttu-id="deb97-153">Enht.</span><span class="sxs-lookup"><span data-stu-id="deb97-153">Unit of Measure</span></span>
-   <span data-ttu-id="deb97-154">Bokføringsgruppe - firma</span><span class="sxs-lookup"><span data-stu-id="deb97-154">Gen. Business Posting Group</span></span>
-   <span data-ttu-id="deb97-155">Bokføringsgruppe - vare</span><span class="sxs-lookup"><span data-stu-id="deb97-155">Gen. Product Posting Group</span></span>
-   <span data-ttu-id="deb97-156">Generelt bokføringsoppsett</span><span class="sxs-lookup"><span data-stu-id="deb97-156">General Posting Setup</span></span>
-   <span data-ttu-id="deb97-157">Distrikt</span><span class="sxs-lookup"><span data-stu-id="deb97-157">Territory</span></span>
-   <span data-ttu-id="deb97-158">Varekategori</span><span class="sxs-lookup"><span data-stu-id="deb97-158">Item Category</span></span>
-   <span data-ttu-id="deb97-159">Salgspris</span><span class="sxs-lookup"><span data-stu-id="deb97-159">Sales Price</span></span>
-   <span data-ttu-id="deb97-160">Kjøpspris</span><span class="sxs-lookup"><span data-stu-id="deb97-160">Purchase Price</span></span>

## <a name="see-also"></a><span data-ttu-id="deb97-161">Se også</span><span class="sxs-lookup"><span data-stu-id="deb97-161">See Also</span></span>
[<span data-ttu-id="deb97-162">Konfigurere et selskap med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="deb97-162">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="deb97-163">Datamigrering for QuickBooks</span><span class="sxs-lookup"><span data-stu-id="deb97-163">QuickBooks Data Migration</span></span>](ui-extensions-quickbooks-data-migration.md)  
[<span data-ttu-id="deb97-164">Dynamics GP-datamigrering</span><span class="sxs-lookup"><span data-stu-id="deb97-164">Dynamics GP Data Migration</span></span>](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

