---
title: Bruke Excel til å importere data til Business Central
description: Bruk standard konfigurasjonspakke til å legge kundedata i Excel og importere dataene tilbake til Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 984186e8bb08cc9e99ab91dbc08f0e85c58e0804
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777951"
---
# <a name="importing-business-data-from-other-finance-systems"></a><span data-ttu-id="d61cf-103">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="d61cf-103">Importing Business Data from Other Finance Systems</span></span>

<span data-ttu-id="d61cf-104">Når du registrerer deg for [!INCLUDE[prod_short](includes/prod_short.md)], kan du velge å opprette et tomt firma, slik at du kan laste opp dine egne data og teste det nye [!INCLUDE[prod_short](includes/prod_short.md)]-firmaet.</span><span class="sxs-lookup"><span data-stu-id="d61cf-104">When you sign up for [!INCLUDE[prod_short](includes/prod_short.md)], you can choose to create an empty company so that you can upload your own data and to test your new [!INCLUDE[prod_short](includes/prod_short.md)] company.</span></span> <span data-ttu-id="d61cf-105">Avhengig av økonomiløsning som selskapet ditt bruker i dag, kan du overføre informasjon om kunder, leverandører, lager og bankkonti.</span><span class="sxs-lookup"><span data-stu-id="d61cf-105">Depending on the finance solution that your business uses today, you can transfer information about customers, vendors, inventory, and bank accounts.</span></span>  

<span data-ttu-id="d61cf-106">Fra Rollesenteret kan du starte en assistert oppsettsveiledning som hjelper deg med å overføre forretningsdata fra en Excel-fil eller fra andre formater.</span><span class="sxs-lookup"><span data-stu-id="d61cf-106">From the Role Center, you can start an assisted setup guide that helps you transfer the business data from an Excel file or from other formats.</span></span> <span data-ttu-id="d61cf-107">Filtypene du kan laste opp, avhenger av utvidelsene som er tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="d61cf-107">The type of files you can upload depends on the extensions that are available.</span></span> <span data-ttu-id="d61cf-108">Du kan for eksempel overføre opp data fra QuickBooks fordi [!INCLUDE[prod_short](includes/prod_short.md)] inneholder en utvidelse som håndterer konverteringen fra QuickBooks.</span><span class="sxs-lookup"><span data-stu-id="d61cf-108">For example, you can migrate data from QuickBooks because [!INCLUDE[prod_short](includes/prod_short.md)] includes an extension that handles the conversion from QuickBooks.</span></span> <span data-ttu-id="d61cf-109">Hvis du vil overføre data fra andre økonomiløsninger, må du kontrollere om en utvidelse er tilgjengelig for denne løsningen eller importere fra Excel.</span><span class="sxs-lookup"><span data-stu-id="d61cf-109">If you want to migrate data from other finance solutions, you must either check if an extension is available for that solution or import from Excel.</span></span>  

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="d61cf-110">inneholder maler for kontoer, kunder, leverandører og lagervarer, som du kan velge å bruke når du importerer dataene.</span><span class="sxs-lookup"><span data-stu-id="d61cf-110">includes templates for accounts, customers, vendors, and inventory items that you can choose to apply when you import your data.</span></span>

<span data-ttu-id="d61cf-111">Du kan importere hoveddata og noen transaksjonsdata fra andre finanssystemer som er basert på standard konfigurasjonspakke i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="d61cf-111">You can import master data and some transactional data from other finance systems based on the default configuration package in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="d61cf-112">På siden **Konfigurasjonspakker** kan du arbeide med pakken for å importere og validere dataene før du bruker pakken.</span><span class="sxs-lookup"><span data-stu-id="d61cf-112">On the **Configuration Packages** page, you can work with the package to import and validate the data before you apply the package.</span></span>  

> [!TIP]  
> <span data-ttu-id="d61cf-113">Vi anbefaler at du bruker veivisere for datamigrering til å importere data fra Dynamics GP, Dynamics NAV eller QuickBooks.</span><span class="sxs-lookup"><span data-stu-id="d61cf-113">We recommend that you use data migration wizards to import data from Dynamics GP, Dynamics NAV, or QuickBooks.</span></span> <span data-ttu-id="d61cf-114">Hvis du vil ha mer informasjon, kan du se [Overføre lokale data til Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) i administrasjonsinnholdet eller [Datamigrering for QuickBooks](ui-extensions-quickbooks-data-migration.md).</span><span class="sxs-lookup"><span data-stu-id="d61cf-114">For more information, see [Migrating On-Premises Data to Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) in the administration content, or [QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="d61cf-115">For omfattende implementasjonsarbeid kan du bruke RapidStart Services for [!INCLUDE[prod_short](includes/prod_short.md)], et omfattende verktøy for å definere nye løsninger basert på kundens forretningskrav og oppsettsdata.</span><span class="sxs-lookup"><span data-stu-id="d61cf-115">For larger implementation work, you can use RapidStart Services for [!INCLUDE[prod_short](includes/prod_short.md)], which is an extensive toolkit for setting up new solutions based on customers' business requirements and setup data.</span></span> <span data-ttu-id="d61cf-116">RapidStart Services har dessuten funksjoner for import av forretningsdata.</span><span class="sxs-lookup"><span data-stu-id="d61cf-116">RapidStart Services also offers functionality for import of business data.</span></span> <span data-ttu-id="d61cf-117">Hvis du vil ha mer informasjon, kan du se [Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span><span class="sxs-lookup"><span data-stu-id="d61cf-117">For more information, see [Setting Up a Company With RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span></span>

<span data-ttu-id="d61cf-118">For å importere varebilder kan du bruke en egen funksjon på siden **Lageroppsett**.</span><span class="sxs-lookup"><span data-stu-id="d61cf-118">To import item pictures, you can use a dedicated function on the **Inventory Setup** page.</span></span> <span data-ttu-id="d61cf-119">Hvis du vil ha mer informasjon, se [Importere flere varebilder](inventory-how-import-item-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="d61cf-119">For more information, see [Import Multiple Item Pictures](inventory-how-import-item-pictures.md).</span></span>

## <a name="importing-data-from-configuration-packages"></a><span data-ttu-id="d61cf-120">Importere data fra konfigurasjonspakker</span><span class="sxs-lookup"><span data-stu-id="d61cf-120">Importing Data from Configuration Packages</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="d61cf-121">inkluderer en konfigurasjonspakke som du kan eksportere til Excel og definere dataene der.</span><span class="sxs-lookup"><span data-stu-id="d61cf-121">includes a configuration package that you can export to Excel and set up your data there.</span></span> <span data-ttu-id="d61cf-122">Deretter kan du importere dataene fra Excel på nytt.</span><span class="sxs-lookup"><span data-stu-id="d61cf-122">Then, you can import the data from Excel again.</span></span> <span data-ttu-id="d61cf-123">Pakken består av 27 tabeller, inkludert hoveddata som kunder, leverandører, varer, og kontoer, andre grunnleggende oppsettstabeller, for eksempel frakt og transaksjonerstabeller, som salgshode og linjer.</span><span class="sxs-lookup"><span data-stu-id="d61cf-123">The package consists of 27 tables, including master data such as customers, vendors, items, and accounts, other basic setup tables such as shipping methods, and transactions tables such as sales header and lines.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="d61cf-124">Arbeide med konfigurasjonspakker er avanserte funksjoner, og vi anbefaler at du kontakter systemansvarlig.</span><span class="sxs-lookup"><span data-stu-id="d61cf-124">Working with configuration packages is advanced functionality, and we recommend that you contact your administrator.</span></span> <span data-ttu-id="d61cf-125">For mer informasjon, se [Importere data fra eldre regnskapsprogramvare ved hjelp av en konfigurasjonspakke](across-import-data-configuration-packages.md).</span><span class="sxs-lookup"><span data-stu-id="d61cf-125">For more information, see [Importing Data from Legacy Accounting Software using a Configuration Package](across-import-data-configuration-packages.md).</span></span>

## <a name="working-with-data-in-excel"></a><span data-ttu-id="d61cf-126">Arbeide med data i Excel</span><span class="sxs-lookup"><span data-stu-id="d61cf-126">Working with Data in Excel</span></span>
<span data-ttu-id="d61cf-127">Når du eksporterer standard konfigurasjonspakke til Excel, inneholder generert arbeidsboken et regneark for hver tabell i pakken.</span><span class="sxs-lookup"><span data-stu-id="d61cf-127">When you export the default configuration package to Excel, the generated workbook contains a worksheet for each table in the package.</span></span> <span data-ttu-id="d61cf-128">Du kan forenkle oppgavene ved å bruke verktøyene for XML-manipulering i Excel.</span><span class="sxs-lookup"><span data-stu-id="d61cf-128">To simplify your tasks, you can take advantage of the XML manipulation tools that are built into Excel.</span></span> <span data-ttu-id="d61cf-129">Du kan også bruke innebygde Excel-funksjoner for å få hjelp med dataformatering og plassering av data i riktig celle.</span><span class="sxs-lookup"><span data-stu-id="d61cf-129">You can also use Excel built-in functions to help with data formatting and to put data in the correct cell.</span></span> <span data-ttu-id="d61cf-130">Du kan for eksempel legge til et tomt regneark og kopiere de gamle dataene til det.</span><span class="sxs-lookup"><span data-stu-id="d61cf-130">For example, add a blank worksheet and copy the legacy data to it.</span></span> <span data-ttu-id="d61cf-131">Lag deretter en Excel-formel til å tilordne data i transformasjonsregnearket mellom feltene i det eksporterte regnearket og eldre kundedata.</span><span class="sxs-lookup"><span data-stu-id="d61cf-131">Then make an Excel formula to map data in the transformation worksheet between the fields in the exported worksheet and customer legacy data.</span></span> <span data-ttu-id="d61cf-132">Når du har tilordnet alle dataene, kan du kopiere dataområdet til tabellforslaget.</span><span class="sxs-lookup"><span data-stu-id="d61cf-132">After you have mapped all of the data, copy the range of data onto the table worksheet.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="d61cf-133">Ikke endre kolonnene i forslagene.</span><span class="sxs-lookup"><span data-stu-id="d61cf-133">Do not change the columns in the worksheets.</span></span> <span data-ttu-id="d61cf-134">Hvis du flytter, endrer eller sletter dem, kan ikke regnearket importeres til [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="d61cf-134">If they are moved, changed, or deleted, the worksheet cannot be imported into [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="d61cf-135">Felt av typen blob kan ikke eksporteres/importeres i Excel.</span><span class="sxs-lookup"><span data-stu-id="d61cf-135">Fields of type Blob cannot be exported/imported using Excel.</span></span>

## <a name="tables-in-the-default-configuration-package"></a><span data-ttu-id="d61cf-136">Tabeller i standard konfigurasjonspakke</span><span class="sxs-lookup"><span data-stu-id="d61cf-136">Tables in the Default Configuration Package</span></span>
<span data-ttu-id="d61cf-137">Standard konfigurasjonspakke støtter følgende tabeller:</span><span class="sxs-lookup"><span data-stu-id="d61cf-137">The default configuration package supports the following tables:</span></span>

-   <span data-ttu-id="d61cf-138">Betalingsbetingelser</span><span class="sxs-lookup"><span data-stu-id="d61cf-138">Payment Terms</span></span>
-   <span data-ttu-id="d61cf-139">Kundeprisgruppe</span><span class="sxs-lookup"><span data-stu-id="d61cf-139">Customer Price Group</span></span>
-   <span data-ttu-id="d61cf-140">Leveringsmåte</span><span class="sxs-lookup"><span data-stu-id="d61cf-140">Shipment Method</span></span>
-   <span data-ttu-id="d61cf-141">Selger/innkjøper</span><span class="sxs-lookup"><span data-stu-id="d61cf-141">Salesperson/Purchaser</span></span>
-   <span data-ttu-id="d61cf-142">Lokasjon</span><span class="sxs-lookup"><span data-stu-id="d61cf-142">Location</span></span>
-   <span data-ttu-id="d61cf-143">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="d61cf-143">GL Account</span></span>
-   <span data-ttu-id="d61cf-144">Kunde</span><span class="sxs-lookup"><span data-stu-id="d61cf-144">Customer</span></span>
-   <span data-ttu-id="d61cf-145">Leverandør</span><span class="sxs-lookup"><span data-stu-id="d61cf-145">Vendor</span></span>
-   <span data-ttu-id="d61cf-146">Element</span><span class="sxs-lookup"><span data-stu-id="d61cf-146">Item</span></span>
-   <span data-ttu-id="d61cf-147">Salgshode</span><span class="sxs-lookup"><span data-stu-id="d61cf-147">Sales Header</span></span>
-   <span data-ttu-id="d61cf-148">Salgslinje</span><span class="sxs-lookup"><span data-stu-id="d61cf-148">Sales Line</span></span>
-   <span data-ttu-id="d61cf-149">Bestillingshode</span><span class="sxs-lookup"><span data-stu-id="d61cf-149">Purchase Header</span></span>
-   <span data-ttu-id="d61cf-150">Bestillingslinje</span><span class="sxs-lookup"><span data-stu-id="d61cf-150">Purchase Line</span></span>
-   <span data-ttu-id="d61cf-151">Finans-</span><span class="sxs-lookup"><span data-stu-id="d61cf-151">Gen.</span></span> <span data-ttu-id="d61cf-152">kladdelinje</span><span class="sxs-lookup"><span data-stu-id="d61cf-152">Journal Line</span></span>
-   <span data-ttu-id="d61cf-153">Varekladdelinje</span><span class="sxs-lookup"><span data-stu-id="d61cf-153">Item Journal Line</span></span>
-   <span data-ttu-id="d61cf-154">Bokføringsgruppe - kunde</span><span class="sxs-lookup"><span data-stu-id="d61cf-154">Customer Posting Group</span></span>
-   <span data-ttu-id="d61cf-155">Bokføringsgruppe - leverandør</span><span class="sxs-lookup"><span data-stu-id="d61cf-155">Vendor Posting Group</span></span>
-   <span data-ttu-id="d61cf-156">Bokføringsgruppe - lager</span><span class="sxs-lookup"><span data-stu-id="d61cf-156">Inventory Posting Group</span></span>
-   <span data-ttu-id="d61cf-157">Enht.</span><span class="sxs-lookup"><span data-stu-id="d61cf-157">Unit of Measure</span></span>
-   <span data-ttu-id="d61cf-158">Finans-</span><span class="sxs-lookup"><span data-stu-id="d61cf-158">Gen.</span></span> <span data-ttu-id="d61cf-159">- firma</span><span class="sxs-lookup"><span data-stu-id="d61cf-159">Business Posting Group</span></span>
-   <span data-ttu-id="d61cf-160">Finans-</span><span class="sxs-lookup"><span data-stu-id="d61cf-160">Gen.</span></span> <span data-ttu-id="d61cf-161">- vare</span><span class="sxs-lookup"><span data-stu-id="d61cf-161">Product Posting Group</span></span>
-   <span data-ttu-id="d61cf-162">Generelt bokføringsoppsett</span><span class="sxs-lookup"><span data-stu-id="d61cf-162">General Posting Setup</span></span>
-   <span data-ttu-id="d61cf-163">Distrikt</span><span class="sxs-lookup"><span data-stu-id="d61cf-163">Territory</span></span>
-   <span data-ttu-id="d61cf-164">Varekategori</span><span class="sxs-lookup"><span data-stu-id="d61cf-164">Item Category</span></span>
-   <span data-ttu-id="d61cf-165">Salgspris</span><span class="sxs-lookup"><span data-stu-id="d61cf-165">Sales Price</span></span>
-   <span data-ttu-id="d61cf-166">Kjøpspris</span><span class="sxs-lookup"><span data-stu-id="d61cf-166">Purchase Price</span></span>

## <a name="see-also"></a><span data-ttu-id="d61cf-167">Se også</span><span class="sxs-lookup"><span data-stu-id="d61cf-167">See Also</span></span>
[<span data-ttu-id="d61cf-168">Konfigurere et selskap med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="d61cf-168">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="d61cf-169">Overføre lokale data til Business Central Online</span><span class="sxs-lookup"><span data-stu-id="d61cf-169">Migrating On-Premises Data to Business Central Online</span></span>](/dynamics365/business-central/dev-itpro/administration/migrate-data)  
[<span data-ttu-id="d61cf-170">Datamigrering for QuickBooks</span><span class="sxs-lookup"><span data-stu-id="d61cf-170">QuickBooks Data Migration</span></span>](ui-extensions-quickbooks-data-migration.md)  
[<span data-ttu-id="d61cf-171">Importere flere varebilder</span><span class="sxs-lookup"><span data-stu-id="d61cf-171">Import Multiple Item Pictures</span></span>](inventory-how-import-item-pictures.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]