---
title: Opprette nye selskaper med en automatisk oppsettguide | Microsoft-dokumentasjon
description: Det er enkelt å opprette et nytt, tomt selskap i Business Central. En guide for assistert oppsett hjelper deg gjennom trinnene, og du kan importere forretningsdataene eksisterende.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: company, setup wizard
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fc318d3de70cb56e722bd02c868fc570fb62692b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385052"
---
# <a name="creating-new-companies-in-prod_short"></a><span data-ttu-id="3b9a9-104">Opprette nye seleskaper i [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="3b9a9-104">Creating New Companies in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

<span data-ttu-id="3b9a9-105">I [!INCLUDE[prod_short](includes/prod_short.md)] kalles beholderen for forretningsdataene som hører til en konsern eller juridisk enhet et *selskap*.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-105">In [!INCLUDE[prod_short](includes/prod_short.md)], the container for business data that belongs to a business unit or legal entity is referred to as a *company*.</span></span> <span data-ttu-id="3b9a9-106">Når du registrerer deg for [!INCLUDE[prod_short](includes/prod_short.md)], får du et demoselskap og et tomt selskap, *Mitt selskap*.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-106">When you sign up for [!INCLUDE[prod_short](includes/prod_short.md)], you are given a demonstration company and an empty company, *My Company*.</span></span> <span data-ttu-id="3b9a9-107">Bytte mellom selskaper er enkelt: simpelthen gå til **Mine innstillinger**, og bytt til det andre selskapet.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-107">Switching between the companies is easy: just go to **My Settings** and move to the other company.</span></span> <span data-ttu-id="3b9a9-108">Du kan også opprette nye selskaper i [!INCLUDE[prod_short](includes/prod_short.md)], avhengig av forretningsbehovene.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-108">But you can also create new companies in [!INCLUDE[prod_short](includes/prod_short.md)] depending on your business needs.</span></span> <span data-ttu-id="3b9a9-109">Når du oppretter et nytt selskap, gir en guide for assistert oppsett deg det grunnleggende.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-109">When you create a new company, an assisted setup guide helps you get the basics in place.</span></span> <span data-ttu-id="3b9a9-110">Deretter kan du importere aktuelle data fra det gamle systemet eller et annet selskap i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="3b9a9-110">Then, you can import relevant data from your legacy system or another company in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

## <a name="creating-a-new-company"></a><span data-ttu-id="3b9a9-111">Opprette et nytt selskap</span><span class="sxs-lookup"><span data-stu-id="3b9a9-111">Creating a New Company</span></span>

<span data-ttu-id="3b9a9-112">Hvis du vil legge til et selskap til din [!INCLUDE[prod_short](includes/prod_short.md)], kan du bruke den assisterte oppsettsveiledningen **Opprett nytt selskap** for å komme i gang.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-112">If you decide to add a company to your [!INCLUDE[prod_short](includes/prod_short.md)], you can use the **Create New Company** assisted setup guide to get you started.</span></span> <span data-ttu-id="3b9a9-113">Oppsettsveiviseren er tilgjengelig fra **Selskaper**-siden og fra oppslaget i **Selskap**-feltet på siden **Mine innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-113">The setup wizard is available from the **Companies** page and from the lookup in the **Company** field on the **My Settings** page.</span></span>  

<span data-ttu-id="3b9a9-114">Veiviseren for oppsett har tre maler og et tomt alternativ:</span><span class="sxs-lookup"><span data-stu-id="3b9a9-114">The setup wizard offers three templates and a blank option:</span></span>

- <span data-ttu-id="3b9a9-115">**Evaluering - eksempeldata**</span><span class="sxs-lookup"><span data-stu-id="3b9a9-115">**Evaluation - Sample Data**</span></span>  
    <span data-ttu-id="3b9a9-116">Dette oppretter et selskap som ligner på demoselskapet, med eksempeldata og oppsettsdata.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-116">This creates a company that is similar to the demonstration company with sample data and setup data.</span></span>  
- <span data-ttu-id="3b9a9-117">**Produksjon - bare oppsettsdata**</span><span class="sxs-lookup"><span data-stu-id="3b9a9-117">**Production - Setup Data Only**</span></span>  
    <span data-ttu-id="3b9a9-118">Dette oppretter et selskap som ligner på **Mitt selskap**, med oppsettsdata, men uten eksempeldata.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-118">This creates a company that is similar to **My Company** with setup data but without sample data.</span></span>
- <span data-ttu-id="3b9a9-119">**Avansert evaluering - fullført eksempeldata** - dette oppretter et selskap med oppsettdata og fullfør eksempeldata for alle funksjoner, inkludert produksjons- og servicehåndtering</span><span class="sxs-lookup"><span data-stu-id="3b9a9-119">**Advanced Evaluation - Complete Sample Data** This creates a company with setup data and complete sample data for all features, including Manufacturing and Service Management.</span></span>
- <span data-ttu-id="3b9a9-120">**Opprett nytt- ingen data**</span><span class="sxs-lookup"><span data-stu-id="3b9a9-120">**Create New - No Data**</span></span>  
    <span data-ttu-id="3b9a9-121">Dette oppretter et tomt selskap uten oppsettsdata.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-121">This creates a blank company without setup data.</span></span>  

<span data-ttu-id="3b9a9-122">Hvis du ønsker å begynne med et nytt selskap, må du velge **Produksjon - Bare oppsettsdata** og deretter importere egne forretningsdata, for eksempel kunder, varer og leverandører.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-122">If you want to get started easily with a new company, choose **Production - Setup Data Only** and then import your own business data, such as customers, items, and vendors.</span></span> <span data-ttu-id="3b9a9-123">Velg **Ny**-malen hvis du vil definere alt fra begynnelsen.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-123">Choose the **New** template if you want to set everything up from scratch.</span></span> <span data-ttu-id="3b9a9-124">I så fall kan du bruke veiviseren **Selskapsoppsett** med assistert oppsettsveiledning for å komme i gang med grunnleggende oppsettsdata.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-124">In that case, you can use the **Company Setup** assisted setup guide to help you get started with essential setup data.</span></span>  

> [!NOTE]  
> <span data-ttu-id="3b9a9-125">Når du oppretter et nytt selskap, tar litt tid før du kan bruke det i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="3b9a9-125">When you create a new company, it takes a few minutes before you can access it in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="3b9a9-126">Statusen for oppsettet på siden **Selskaper** viser når det nye selskapet er klart.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-126">The setup status on the **Companies** page shows when the new company is ready for you.</span></span> <span data-ttu-id="3b9a9-127">Deretter du kan bytte til et nytt selskap ved hjelp av **Mine innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-127">Then, you can switch to the new company by using **My Settings**.</span></span>  

<span data-ttu-id="3b9a9-128">Du kan opprette så mange nye selskaper under 30 dagers prøveperioden, men de er bare tilgjengelige under prøveperioden.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-128">During your 30 day trial, you can create any number of new companies, but they will only be available during your trial.</span></span> <span data-ttu-id="3b9a9-129">Ta kontakt med din [!INCLUDE[prod_short](includes/prod_short.md)]-partner for mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-129">For more information, contact your [!INCLUDE[prod_short](includes/prod_short.md)] partner.</span></span>  

## <a name="copying-a-company"></a><span data-ttu-id="3b9a9-130">Kopiere et selskap</span><span class="sxs-lookup"><span data-stu-id="3b9a9-130">Copying a company</span></span>

<span data-ttu-id="3b9a9-131">På siden **Selskaper** kan du bruke **Kopier**-handlingen til å opprette et annet selskap basert på innholdet i et eksisterende selskap.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-131">On the **Companies** page, you can use the **Copy** action to create a second company based on the contents of an existing company.</span></span> <span data-ttu-id="3b9a9-132">Dette er for eksempel nyttig når du vil teste et selskap uten å forstyrre produksjonsdata.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-132">This is useful, for example, when you want to test a company without disrupting production data.</span></span>

> [!Important]
> <span data-ttu-id="3b9a9-133">Denne funksjonen kan ikke brukes til å ta en sikkerhetskopi av et selskap.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-133">This function cannot be used to take a backup of a company.</span></span> <span data-ttu-id="3b9a9-134">Å ta en sikkerhetskopi av selskapet begynner ved å eksportere databasen som en bacpac-fil.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-134">Taking a company backup begins by exporting the database as a .bacpac file.</span></span> <span data-ttu-id="3b9a9-135">Hvis du vil ha mer informasjon, kan du se [Eksportere databaser](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export) i hjelpen for utvikling og administrasjon.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-135">For more information, see [Exporting Databases](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export) in the development and administration help.</span></span>

## <a name="company-setup"></a><span data-ttu-id="3b9a9-136">Selskapsoppsett</span><span class="sxs-lookup"><span data-stu-id="3b9a9-136">Company Setup</span></span>

<span data-ttu-id="3b9a9-137">Når du logger deg på et nytt selskap, kjøres veiviseren **Selskapsoppsett** automatisk og hjelper deg med å komme i gang.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-137">When you sign in to a new company, the **Company Setup** wizard runs automatically and helps you get started.</span></span> <span data-ttu-id="3b9a9-138">Du blir bedt om informasjon om selskapet, for eksempel adressen, bankdetaljer og lagerkostmetoden.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-138">You will be asked for information about your business, such as the address, bank details, and inventory costing method.</span></span> <span data-ttu-id="3b9a9-139">Vi ber om opplysningene fordi de brukes som grunnlag for mange områder i [!INCLUDE[prod_short](includes/prod_short.md)], som du ikke kan definere senere manuelt.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-139">We ask for this information because it is used as a basis for many areas in [!INCLUDE[prod_short](includes/prod_short.md)] that you will then not have to set up manually later.</span></span>  

<span data-ttu-id="3b9a9-140">For eksempel firmaadressen er inkludert i fakturaer og andre dokumenter, bankinformasjonen brukes i betalinger og kostmetoden brukes til å beregne priser og lagerverdisetting.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-140">For example, your company address is included in invoices and other documents, your bank information is used in payments, and the costing method is used to calculate prices as well as inventory valuation.</span></span>  

<span data-ttu-id="3b9a9-141">Når du har det grunnleggende på plass, kan du definere gjenstående kjerneområder.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-141">Once you have the basics in place, you can set up remaining core areas.</span></span> <span data-ttu-id="3b9a9-142">Deretter er du klar til å legge til forretningsdataene, for eksempel kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-142">Then, you are ready to add business data, such as customers and vendors.</span></span> <span data-ttu-id="3b9a9-143">Hvis du vil ha mer informasjon, kan du se [Definere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).</span><span class="sxs-lookup"><span data-stu-id="3b9a9-143">For more information, see [Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).</span></span>  

## <a name="companies-and-environments"></a><span data-ttu-id="3b9a9-144">Selskaper og miljøer</span><span class="sxs-lookup"><span data-stu-id="3b9a9-144">Companies and Environments</span></span>

[!INCLUDE [company_environment](includes/company_environment.md)]

<span data-ttu-id="3b9a9-145">Hvis du vil ha mer informasjon, kan du se [Bytte til et annet selskap eller miljø](ui-organization-switch.md).</span><span class="sxs-lookup"><span data-stu-id="3b9a9-145">For more information, see [Switching to Another Company or Environment](ui-organization-switch.md).</span></span> 

## <a name="changing-a-companys-name"></a><span data-ttu-id="3b9a9-146">Endre et selskaps navn</span><span class="sxs-lookup"><span data-stu-id="3b9a9-146">Changing a Company's Name</span></span>

<span data-ttu-id="3b9a9-147">Når et selskap er opprettet, kan du ikke endre navnet på det.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-147">Once a company has been created, you can't change it's name.</span></span> <span data-ttu-id="3b9a9-148">Du kan imidlertid endre **visningsnavnet**, som er tekst som skal vises for selskapet i programmet.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-148">But you can change its **Display Name**, which is text that will be shown for the company throughout the application.</span></span>  

> [!TIP]
> <span data-ttu-id="3b9a9-149">Du kan gi et selskap nytt navn hvis du bruker [!INCLUDE[prod_short](includes/prod_short.md)] lokalt.</span><span class="sxs-lookup"><span data-stu-id="3b9a9-149">You can rename a company if you're using [!INCLUDE[prod_short](includes/prod_short.md)] on-premises.</span></span>

## <a name="see-also"></a><span data-ttu-id="3b9a9-150">Se også</span><span class="sxs-lookup"><span data-stu-id="3b9a9-150">See Also</span></span>

[<span data-ttu-id="3b9a9-151">Tilpasse Business Central</span><span class="sxs-lookup"><span data-stu-id="3b9a9-151">Customizing Business Central</span></span>](ui-customizing-overview.md)  
<span data-ttu-id="3b9a9-152">[Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="3b9a9-152">[Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span></span>  
[<span data-ttu-id="3b9a9-153">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="3b9a9-153">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="3b9a9-154">Endre grunnleggende innstillinger</span><span class="sxs-lookup"><span data-stu-id="3b9a9-154">Change Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="3b9a9-155">Komme i gang</span><span class="sxs-lookup"><span data-stu-id="3b9a9-155">Getting Started</span></span>](product-get-started.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]