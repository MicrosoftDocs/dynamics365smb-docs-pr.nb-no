---
title: Rapportvalg i Business Central
description: Finn ut mer om hvordan du definerer rapportene du bruker til å skrive ut ulike typer dokumenter i Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ba15a65317ebf52579c285c93dd59eba1b65ae1b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787110"
---
# <a name="report-selection-in-business-central"></a><span data-ttu-id="1191d-103">Rapportvalg i Business Central</span><span class="sxs-lookup"><span data-stu-id="1191d-103">Report Selection in Business Central</span></span>

<span data-ttu-id="1191d-104">Du kan konfigurere standardrapporter som skal brukes til å skrive ut forskjellige salgs- og kjøpsdokumenter, for eksempel ordrer, tilbud/forespørsler, fakturaer og kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="1191d-104">You can set up default reports that will be used to print the various documents for sales and purchases, such as orders, quotes, invoices, and credit memos.</span></span> <span data-ttu-id="1191d-105">Hvis du for eksempel har et bestemt oppsett for salgsfakturaer, kan du angi denne rapporten på siden **Rapportvalg – salg** slik at den blir brukt til å sende eller skrive ut salgsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="1191d-105">For example, if you have a specific layout for sales invoices, you can specify that report in the **Report Selections - Sales** page so that it will be used to send or print sales invoices.</span></span>  

<span data-ttu-id="1191d-106">Siden **Rapportvalg** angir hvilken rapport som skal skrives ut i forskjellige situasjoner.</span><span class="sxs-lookup"><span data-stu-id="1191d-106">The **Report Selections** pages specify which report will be printed in different situations.</span></span> <span data-ttu-id="1191d-107">[!INCLUDE [prod_short](includes/prod_short.md)] inkluderer standardkonfigurasjoner, men du kan selvsagt endre disse standardverdiene.</span><span class="sxs-lookup"><span data-stu-id="1191d-107">[!INCLUDE [prod_short](includes/prod_short.md)] includes default configurations, but of course you can change these defaults.</span></span> <span data-ttu-id="1191d-108">Du kan også legge til rapporter i sidene **Rapportvalg** hvis du for eksempel vil skrive ut mer enn én rapport per dokumenttype.</span><span class="sxs-lookup"><span data-stu-id="1191d-108">You can also add reports to the **Report Selection** pages if you want to print more than one report per document type, for example.</span></span>  

## <a name="available-report-selections"></a><span data-ttu-id="1191d-109">Tilgjengelige rapportvalg</span><span class="sxs-lookup"><span data-stu-id="1191d-109">Available report selections</span></span>

<span data-ttu-id="1191d-110">[!INCLUDE [prod_short](includes/prod_short.md)] inneholder forskjellige sider for **rapportvalg** for forskjellige områder.</span><span class="sxs-lookup"><span data-stu-id="1191d-110">[!INCLUDE [prod_short](includes/prod_short.md)] includes different **Report Selection** pages for different areas.</span></span> <span data-ttu-id="1191d-111">Følgende tabeller beskriver hvor du kan finne informasjon om de forskjellige sidene.</span><span class="sxs-lookup"><span data-stu-id="1191d-111">The following tables describes where you can find information about the different pages.</span></span>  

|<span data-ttu-id="1191d-112">Område eller oppgave</span><span class="sxs-lookup"><span data-stu-id="1191d-112">Area or task</span></span>  |<span data-ttu-id="1191d-113">Finn ut mer</span><span class="sxs-lookup"><span data-stu-id="1191d-113">Learn more</span></span>|
|--------------|----------|
|<span data-ttu-id="1191d-114">Eksempel på hvordan rapportvalg fungerer (salg)</span><span class="sxs-lookup"><span data-stu-id="1191d-114">Example of how report selection works (Sales)</span></span>|[<span data-ttu-id="1191d-115">Rapportvalg for salgsdokumenter</span><span class="sxs-lookup"><span data-stu-id="1191d-115">Report selection for sales documents</span></span>](#example-report-selection-for-sales-documents)|
|<span data-ttu-id="1191d-116">Standardoppsett for e-poster med salgs- og kjøpsdokumenter</span><span class="sxs-lookup"><span data-stu-id="1191d-116">Default layout for emails with sales and purchase documents</span></span>  |[<span data-ttu-id="1191d-117">Konfigurer gjenbrukbare e-posttekster og -oppsett for salgs- og kjøpsdokumenter</span><span class="sxs-lookup"><span data-stu-id="1191d-117">Set Up Reusable Email Texts and Layouts for Sales and Purchase Documents</span></span>](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents) |
|<span data-ttu-id="1191d-118">Definer sjekkoppsett</span><span class="sxs-lookup"><span data-stu-id="1191d-118">Define check layouts</span></span>     |[<span data-ttu-id="1191d-119">Velg et sjekkoppsett</span><span class="sxs-lookup"><span data-stu-id="1191d-119">Select a Check Layout</span></span>](finance-how-define-check-layouts.md) |
|<span data-ttu-id="1191d-120">Definer rapporter for mva-rapportering (Tyskland)</span><span class="sxs-lookup"><span data-stu-id="1191d-120">Define reports for VAT reporting (Germany)</span></span>|[<span data-ttu-id="1191d-121">Sette opp rapporter for mva og Intrastat</span><span class="sxs-lookup"><span data-stu-id="1191d-121">Set Up Reports for VAT and Intrastat</span></span>](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> <span data-ttu-id="1191d-122">[!INCLUDE [prod_short](includes/prod_short.md)] kan inkludere flere sider for **rapportvalg**, avhengig av lokasjon og bransje.</span><span class="sxs-lookup"><span data-stu-id="1191d-122">Your [!INCLUDE [prod_short](includes/prod_short.md)] can include additional **Report Selection** pages, depending on your location and industry, for example.</span></span> <span data-ttu-id="1191d-123">Du kan alltid kontrollere oppsettet ved å velge ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rapportvalg** og velge den aktuelle koblingen.</span><span class="sxs-lookup"><span data-stu-id="1191d-123">You can always check your setup by choosing the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, entering **Report Selections**, and then choose the relevant link.</span></span>

<span data-ttu-id="1191d-124">Standardversjonen av [!INCLUDE [prod_short](includes/prod_short.md)] omfatter følgende sider for **rapportvalg**:</span><span class="sxs-lookup"><span data-stu-id="1191d-124">The default version of [!INCLUDE [prod_short](includes/prod_short.md)] includes the following **Report Section** pages:</span></span>

* <span data-ttu-id="1191d-125">**Rapportvalg – salg**</span><span class="sxs-lookup"><span data-stu-id="1191d-125">**Report Selection - Sales**</span></span>  
* <span data-ttu-id="1191d-126">**Rapportvalg – kjøp**</span><span class="sxs-lookup"><span data-stu-id="1191d-126">**Report Selection - Purchase**</span></span>  
* <span data-ttu-id="1191d-127">**Rapportvalg – beholdning**</span><span class="sxs-lookup"><span data-stu-id="1191d-127">**Report Selection - Inventory**</span></span>  
* <span data-ttu-id="1191d-128">**Rapportvalg – kontantstrøm**</span><span class="sxs-lookup"><span data-stu-id="1191d-128">**Report Selection - Cash Flow**</span></span>  
* <span data-ttu-id="1191d-129">**Rapportvalg – lager**</span><span class="sxs-lookup"><span data-stu-id="1191d-129">**Report Selection - Warehouse**</span></span>  
* <span data-ttu-id="1191d-130">**Rapportvalg – bankkonto**</span><span class="sxs-lookup"><span data-stu-id="1191d-130">**Report Selection - Bank Account**</span></span>  
* <span data-ttu-id="1191d-131">**Purring/rentenota for rapportvalg**</span><span class="sxs-lookup"><span data-stu-id="1191d-131">**Report Selections Reminder/Finance Charge**</span></span>  

## <a name="example-report-selection-for-sales-documents"></a><span data-ttu-id="1191d-132">Eksempel: Rapportvalg for salgsdokumenter</span><span class="sxs-lookup"><span data-stu-id="1191d-132">Example: Report selection for sales documents</span></span>

<span data-ttu-id="1191d-133">Siden **Rapportvalg – salg** definerer standardrapportene som skal brukes i ulike scenarioer for hver av de relaterte dokumenttypene.</span><span class="sxs-lookup"><span data-stu-id="1191d-133">The **Report Selection - Sales** page defines the default reports to use in different scenarios for each related document type.</span></span> <span data-ttu-id="1191d-134">Velg en dokumenttype i feltet **Bruk**, og legg til eller gå gjennom rapportvalget.</span><span class="sxs-lookup"><span data-stu-id="1191d-134">Choose a document type in the **Usage** field, and then add or review the report selection.</span></span> <span data-ttu-id="1191d-135">Du kan definere mer enn én rapport og rekkefølgen på sekvensen som rapportene må sendes eller skrives ut i.</span><span class="sxs-lookup"><span data-stu-id="1191d-135">You can set up more than one report and the order of sequence that the reports must be sent or printed in.</span></span>  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="1191d-136">Enkelte dokumenttyper kan sendes som e-postvedlegg, og andre kan ikke.</span><span class="sxs-lookup"><span data-stu-id="1191d-136">Some types of document can be sent as email attachments, and others cannot.</span></span> <span data-ttu-id="1191d-137">Hver **Rapportvalg**-side viser flere felter hvis typen støtter e-post som standard.</span><span class="sxs-lookup"><span data-stu-id="1191d-137">Each **Report Selection** page shows additional fields if the type support email out of the box.</span></span>  

<span data-ttu-id="1191d-138">På sidene **Rapportvalg – salg** og **Rapportvalg – kjøp** hjelper følgende felter deg med å konfigurere e-post:</span><span class="sxs-lookup"><span data-stu-id="1191d-138">For example, in the **Report Selection - Sales** and **Report Selection - Purchase** pages, the following fields help you set up emailing:</span></span>

|<span data-ttu-id="1191d-139">Feltnavn</span><span class="sxs-lookup"><span data-stu-id="1191d-139">Field name</span></span> |<span data-ttu-id="1191d-140">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="1191d-140">Description</span></span>  |
|-----------|-------------|
|<span data-ttu-id="1191d-141">**Bruk for brødtekst i e-post**</span><span class="sxs-lookup"><span data-stu-id="1191d-141">**Use for Email Body**</span></span>| <span data-ttu-id="1191d-142">Angir at sammendragsinformasjon, for eksempel fakturanummer, forfallsdato og kobling til betalingstjeneste, blir satt inn i tekstdelen i e-posten du sender.</span><span class="sxs-lookup"><span data-stu-id="1191d-142">Specifies that summarized information, such as invoice number, due date, and payment service link, will be inserted in the body of the email that you send.</span></span>        |
|<span data-ttu-id="1191d-143">**Bruk for e-postvedlegg**</span><span class="sxs-lookup"><span data-stu-id="1191d-143">**Use for Email Attachment**</span></span>| <span data-ttu-id="1191d-144">Angir at det relaterte dokumentet blir lagt ved i e-posten.</span><span class="sxs-lookup"><span data-stu-id="1191d-144">Specifies that the related document will be attached to the email.</span></span>|
|<span data-ttu-id="1191d-145">**Oppsettbeskrivelse for brødtekst i e-post**</span><span class="sxs-lookup"><span data-stu-id="1191d-145">**Email Body Layout Description**</span></span>|<span data-ttu-id="1191d-146">Angir oppsettet for e-postbrødtekst som brukes, vanligvis et egendefinert rapportoppsett.</span><span class="sxs-lookup"><span data-stu-id="1191d-146">Specifies the email body layout that is used, typically a custom report layout.</span></span> |

## <a name="see-also"></a><span data-ttu-id="1191d-147">Se også</span><span class="sxs-lookup"><span data-stu-id="1191d-147">See also</span></span>

[<span data-ttu-id="1191d-148">Konfigurer gjenbrukbare e-posttekster og -oppsett for salgs- og kjøpsdokumenter</span><span class="sxs-lookup"><span data-stu-id="1191d-148">Set Up Reusable Email Texts and Layouts for Sales and Purchase Documents</span></span>](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents)  
[<span data-ttu-id="1191d-149">Velg et sjekkoppsett</span><span class="sxs-lookup"><span data-stu-id="1191d-149">Select a Check Layout</span></span>](finance-how-define-check-layouts.md)  
[<span data-ttu-id="1191d-150">Sette opp rapporter for mva og Intrastat (Tyskland)</span><span class="sxs-lookup"><span data-stu-id="1191d-150">Set Up Reports for VAT and Intrastat (Germany)</span></span>](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[<span data-ttu-id="1191d-151">Administrere rapport- og dokumentoppsett</span><span class="sxs-lookup"><span data-stu-id="1191d-151">Managing Report and Document Layouts</span></span>](ui-manage-report-layouts.md)  
[<span data-ttu-id="1191d-152">Definere dokumentoppsett for kunder og leverandører</span><span class="sxs-lookup"><span data-stu-id="1191d-152">Define Document Layouts for Customers and Vendors</span></span>](ui-define-customer-vendor-document-layouts.md)  
[<span data-ttu-id="1191d-153">Konfigurere skrivere</span><span class="sxs-lookup"><span data-stu-id="1191d-153">Set Up Printers</span></span>](ui-specify-printer-selection-reports.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]