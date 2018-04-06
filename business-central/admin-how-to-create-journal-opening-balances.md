---
title: "Opprette inngående balanser for kladd | Microsoft-dokumentasjon"
description: "Business Central omfatter mange kjørsler som er gitt for å hjelpe i overføringen av eldre kontobalanser til et nylig konfigurert selskap. Du kan enkelt overføre disse dataene med kladdebokføringer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: fc8e8f34220643b7cd3fd357aea3807641cee911
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="create-journal-opening-balances"></a><span data-ttu-id="02ebb-104">Opprette inngående balanser for kladd</span><span class="sxs-lookup"><span data-stu-id="02ebb-104">Create Journal Opening Balances</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="02ebb-105"> omfatter mange kjørsler som er gitt for å hjelpe i overføringen av eldre kontobalanser til et nylig konfigurert selskap.</span><span class="sxs-lookup"><span data-stu-id="02ebb-105"> includes several batch jobs that are provided to help in the transfer of legacy account balances to a newly configured company.</span></span> <span data-ttu-id="02ebb-106">Du kan enkelt overføre disse dataene med kundekladden, leverandørkladden, varekladden eller finanskladden.</span><span class="sxs-lookup"><span data-stu-id="02ebb-106">You can easily transfer this data with the customer journal, the vendor journal, the item journal, or the G/L journal.</span></span>

<span data-ttu-id="02ebb-107">Det første trinnet er å opprette en konfigurasjonspakke som inneholder oppsettstabellene for disse kladdene.</span><span class="sxs-lookup"><span data-stu-id="02ebb-107">The first step is to create a configuration package that includes the setup tables for those journals.</span></span> <span data-ttu-id="02ebb-108">Følgende fremgangsmåte forutsetter at dette trinnet er fullført.</span><span class="sxs-lookup"><span data-stu-id="02ebb-108">The following procedure assumes that this step is completed.</span></span> <span data-ttu-id="02ebb-109">Du finner mer informasjon under [Definere selskapskonfigurasjon](admin-set-up-company-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="02ebb-109">For more information, see [Set Up Company Configuration](admin-set-up-company-configuration.md).</span></span> <span data-ttu-id="02ebb-110">Denne fremgangsmåten beskriver de påfølgende trinnene, blant annet å bruke pakken som er levert av en partner.</span><span class="sxs-lookup"><span data-stu-id="02ebb-110">This procedure describes the subsequent steps, which include applying the package that is provided by a partner.</span></span>  

<span data-ttu-id="02ebb-111">Før du kan begynne, kontrollerer du at du er på rollesentersiden for RapidStart Services-implementereren, som gir riktig kontekst for konfigurasjonsarbeidet.</span><span class="sxs-lookup"><span data-stu-id="02ebb-111">Before you start, make sure that you are on the RapidStart Services Implementer Role Center page as it provides the correct context for your configuration work.</span></span> <span data-ttu-id="02ebb-112">Hvis du vil ha mer informasjon, kan du se [Endre grunnleggende innstillinger](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="02ebb-112">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a><span data-ttu-id="02ebb-113">Slik utligner du poster i en kladd mot et nytt selskap:</span><span class="sxs-lookup"><span data-stu-id="02ebb-113">To apply the entries in a journal to a new company</span></span>  
1. <span data-ttu-id="02ebb-114">Konfigurer og bruk en konfigurasjonspakke for det.</span><span class="sxs-lookup"><span data-stu-id="02ebb-114">Configure a new company and apply a configuration package to it.</span></span> <span data-ttu-id="02ebb-115">Hvis du vil ha mer informasjon, kan du se [Konfigurere et selskap med RapidStart-veiviseren](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="02ebb-115">For more information, see [Configure a Company with the RapidStart Wizard](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span></span>  

    <span data-ttu-id="02ebb-116">Det nye selskapet inneholder ikke informasjon om inngående balanser for kladd.</span><span class="sxs-lookup"><span data-stu-id="02ebb-116">The new company does not contain information about journal opening balances.</span></span>  

2. <span data-ttu-id="02ebb-117">Åpne konfigurasjonsforslaget og importer eksisterende data om kunder, varer, leverandører og finans.</span><span class="sxs-lookup"><span data-stu-id="02ebb-117">Open the configuration worksheet and import existing data about customers, items, vendors, and the general ledger.</span></span> <span data-ttu-id="02ebb-118">Hvis du vil ha mer informasjon, kan du se [Flytte kundedata](admin-migrate-customer-data.md).</span><span class="sxs-lookup"><span data-stu-id="02ebb-118">For more information, see [Migrate Customer Data](admin-migrate-customer-data.md).</span></span>  
3. <span data-ttu-id="02ebb-119">Velg for eksempel handlingen **Opprett finanskladdelinjer**.</span><span class="sxs-lookup"><span data-stu-id="02ebb-119">Choose, for example, the **Create G/L Journal Lines** action.</span></span>  
4. <span data-ttu-id="02ebb-120">Fyll ut det som er aktuelt i hurtigfanen **Alternativer**, og angi filtre etter behov.</span><span class="sxs-lookup"><span data-stu-id="02ebb-120">Fill in the **Options** FastTab as appropriate, and set filters as needed.</span></span> <span data-ttu-id="02ebb-121">Skriv for eksempel inn et navn i **Kladdemal**-feltet.</span><span class="sxs-lookup"><span data-stu-id="02ebb-121">For example, in the **Journal Template** field, enter a name.</span></span>  
5. <span data-ttu-id="02ebb-122">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="02ebb-122">Choose the **OK** button.</span></span> <span data-ttu-id="02ebb-123">Nå er postene i kladden, men beløpene er tomme.</span><span class="sxs-lookup"><span data-stu-id="02ebb-123">The records are now in the journal, but the amounts are empty.</span></span>  
6. <span data-ttu-id="02ebb-124">Eksporter kladdetabellen til Excel, og angi informasjon om bokføring og motkonto fra eldre data manuelt.</span><span class="sxs-lookup"><span data-stu-id="02ebb-124">Export the journal table to Excel and manually enter the posting and balancing account information from the legacy data.</span></span>
7. <span data-ttu-id="02ebb-125">Importere og bruke tabellinformasjon for det nye selskapet.</span><span class="sxs-lookup"><span data-stu-id="02ebb-125">Import and apply the table information into the new company.</span></span> <span data-ttu-id="02ebb-126">Kladdelinjene er klare for bokføring.</span><span class="sxs-lookup"><span data-stu-id="02ebb-126">The journal lines are ready for posting.</span></span>  
8. <span data-ttu-id="02ebb-127">Velg kladdelinjetabellen i konfigurasjonsforslaget, og velg deretter handlingen **Databasedata**.</span><span class="sxs-lookup"><span data-stu-id="02ebb-127">In the configuration worksheet, select the journal line table, and then choose the **Database Data** action.</span></span>  
9. <span data-ttu-id="02ebb-128">Se gjennom informasjonen, og velg deretter **Bokfør**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="02ebb-128">Review the information, and then choose the **Post** action.</span></span>  
10. <span data-ttu-id="02ebb-129">Gjenta trinnene for å importere og bokføre eventuelle åpningssaldoer.</span><span class="sxs-lookup"><span data-stu-id="02ebb-129">Repeat the steps to import and post any other opening balances.</span></span>  

## <a name="see-also"></a><span data-ttu-id="02ebb-130">Se også</span><span class="sxs-lookup"><span data-stu-id="02ebb-130">See Also</span></span>  
[<span data-ttu-id="02ebb-131">Bruke konfigurasjoner for nye selskaper</span><span class="sxs-lookup"><span data-stu-id="02ebb-131">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="02ebb-132">Konfigurere et selskap med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="02ebb-132">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="02ebb-133">Administrasjon</span><span class="sxs-lookup"><span data-stu-id="02ebb-133">Administration</span></span>](admin-setup-and-administration.md)

