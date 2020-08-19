---
title: Opprette inngående balanser for kladd | Microsoft-dokumentasjon
description: Business Central omfatter mange kjørsler som er gitt for å hjelpe i overføringen av eldre kontobalanser til et nylig konfigurert selskap. Du kan enkelt overføre disse dataene med kladdebokføringer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/14/2020
ms.author: sgroespe
ms.openlocfilehash: 5360b3a8a72387cda8d0e640562a118ca1f20ff4
ms.sourcegitcommit: 89d0ea903f61ab0628f99329c762d9f1619c49a7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/14/2020
ms.locfileid: "3577129"
---
# <a name="create-journal-opening-balances"></a><span data-ttu-id="725c4-104">Opprette inngående balanser for kladd</span><span class="sxs-lookup"><span data-stu-id="725c4-104">Create Journal Opening Balances</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="725c4-105">omfatter mange kjørsler som er gitt for å hjelpe i overføringen av eldre kontobalanser til et nylig konfigurert selskap.</span><span class="sxs-lookup"><span data-stu-id="725c4-105">includes several batch jobs that are provided to help in the transfer of legacy account balances to a newly configured company.</span></span> <span data-ttu-id="725c4-106">Du kan enkelt overføre disse dataene med kundekladden, leverandørkladden, varekladden eller finanskladden.</span><span class="sxs-lookup"><span data-stu-id="725c4-106">You can easily transfer this data with the customer journal, the vendor journal, the item journal, or the G/L journal.</span></span>

<span data-ttu-id="725c4-107">Det første trinnet er å opprette en konfigurasjonspakke som inneholder oppsettstabellene for disse kladdene.</span><span class="sxs-lookup"><span data-stu-id="725c4-107">The first step is to create a configuration package that includes the setup tables for those journals.</span></span> <span data-ttu-id="725c4-108">Følgende fremgangsmåte forutsetter at dette trinnet er fullført.</span><span class="sxs-lookup"><span data-stu-id="725c4-108">The following procedure assumes that this step is completed.</span></span> <span data-ttu-id="725c4-109">Du finner mer informasjon under [Definere selskapskonfigurasjon](admin-set-up-company-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="725c4-109">For more information, see [Set Up Company Configuration](admin-set-up-company-configuration.md).</span></span> <span data-ttu-id="725c4-110">Denne fremgangsmåten beskriver de påfølgende trinnene, blant annet å bruke pakken som er levert av en partner.</span><span class="sxs-lookup"><span data-stu-id="725c4-110">This procedure describes the subsequent steps, which include applying the package that is provided by a partner.</span></span>  

<span data-ttu-id="725c4-111">Før du begynner, må du kontrollere at du bruker rollesentersiden for administrasjon, fordi denne gir riktig kontekst for konfigurasjonsarbeidet.</span><span class="sxs-lookup"><span data-stu-id="725c4-111">Before you start, make sure that you are using the Administration Role Center page because it provides the correct context for your configuration work.</span></span> <span data-ttu-id="725c4-112">Hvis du vil ha mer informasjon, kan du se [Endre grunnleggende innstillinger](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="725c4-112">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a><span data-ttu-id="725c4-113">Slik utligner du poster i en kladd mot et nytt selskap:</span><span class="sxs-lookup"><span data-stu-id="725c4-113">To apply the entries in a journal to a new company</span></span>

1. <span data-ttu-id="725c4-114">Konfigurer og bruk en konfigurasjonspakke for det.</span><span class="sxs-lookup"><span data-stu-id="725c4-114">Configure a new company and apply a configuration package to it.</span></span> <span data-ttu-id="725c4-115">Hvis du vil ha mer informasjon, kan du se [Konfigurere et selskap med RapidStart-veiviseren](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="725c4-115">For more information, see [Configure a Company with the RapidStart Wizard](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span></span>  

    <span data-ttu-id="725c4-116">Det nye selskapet inneholder ikke informasjon om inngående balanser for kladd.</span><span class="sxs-lookup"><span data-stu-id="725c4-116">The new company does not contain information about journal opening balances.</span></span>  

2. <span data-ttu-id="725c4-117">Åpne konfigurasjonsforslaget og importer eksisterende data om kunder, varer, leverandører og finans.</span><span class="sxs-lookup"><span data-stu-id="725c4-117">Open the configuration worksheet and import existing data about customers, items, vendors, and the general ledger.</span></span> <span data-ttu-id="725c4-118">Hvis du vil ha mer informasjon, kan du se [Flytte kundedata](admin-migrate-customer-data.md).</span><span class="sxs-lookup"><span data-stu-id="725c4-118">For more information, see [Migrate Customer Data](admin-migrate-customer-data.md).</span></span>  

    <span data-ttu-id="725c4-119">Nå er hoveddata på plass.</span><span class="sxs-lookup"><span data-stu-id="725c4-119">Now you have master data in place.</span></span> <span data-ttu-id="725c4-120">Deretter legger du til åpningssaldoer.</span><span class="sxs-lookup"><span data-stu-id="725c4-120">Next, you add the opening balances.</span></span> <span data-ttu-id="725c4-121">Trinnene nedenfor beskriver hvordan du oppretter kladdelinjer finanskonti, men det samme gjelder for oppretting av kladdelinjer for kunder, leverandører og varer.</span><span class="sxs-lookup"><span data-stu-id="725c4-121">The following steps describe how to create journal lines for G/L accounts, but the same apply to creating journal lines for customers, vendors, and items.</span></span>  
3. <span data-ttu-id="725c4-122">Velg handlingen **Opprett finanskladdelinjer**.</span><span class="sxs-lookup"><span data-stu-id="725c4-122">Choose the **Create G/L Acct. Journal Lines** action.</span></span>  
4. <span data-ttu-id="725c4-123">Fyll ut det som er aktuelt i hurtigfanen **Alternativer**, og angi filtre etter behov.</span><span class="sxs-lookup"><span data-stu-id="725c4-123">Fill in the **Options** FastTab as appropriate, and set filters as needed.</span></span> <span data-ttu-id="725c4-124">Skriv for eksempel inn et navn i **Kladdemal**-feltet.</span><span class="sxs-lookup"><span data-stu-id="725c4-124">For example, in the **Journal Template** field, enter a name.</span></span>  
5. <span data-ttu-id="725c4-125">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="725c4-125">Choose the **OK** button.</span></span> <span data-ttu-id="725c4-126">Nå er postene i kladden, men beløpene er tomme.</span><span class="sxs-lookup"><span data-stu-id="725c4-126">The records are now in the journal, but the amounts are empty.</span></span>  
6. <span data-ttu-id="725c4-127">Eksporter kladdetabellen til Excel, og angi informasjon om bokføring og motkonto fra eldre data manuelt.</span><span class="sxs-lookup"><span data-stu-id="725c4-127">Export the journal table to Excel and manually enter the posting and balancing account information from the legacy data.</span></span>
7. <span data-ttu-id="725c4-128">Importere og bruke tabellinformasjon for det nye selskapet.</span><span class="sxs-lookup"><span data-stu-id="725c4-128">Import and apply the table information into the new company.</span></span> <span data-ttu-id="725c4-129">Kladdelinjene er klare for bokføring.</span><span class="sxs-lookup"><span data-stu-id="725c4-129">The journal lines are ready for posting.</span></span>  
8. <span data-ttu-id="725c4-130">Velg kladdelinjetabellen i konfigurasjonsforslaget, og velg deretter handlingen **Databasedata**.</span><span class="sxs-lookup"><span data-stu-id="725c4-130">In the configuration worksheet, select the journal line table, and then choose the **Database Data** action.</span></span>  
9. <span data-ttu-id="725c4-131">Se gjennom informasjonen, og velg deretter **Bokfør**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="725c4-131">Review the information, and then choose the **Post** action.</span></span>  
10. <span data-ttu-id="725c4-132">Gjenta trinnene for å importere og bokføre eventuelle åpningssaldoer.</span><span class="sxs-lookup"><span data-stu-id="725c4-132">Repeat the steps to import and post any other opening balances.</span></span>  

> [!TIP]
> <span data-ttu-id="725c4-133">Du kan bruke de samme kjørslene til å legge til åpningssaldoer når du registrerer en ny kunde eller leverandør som du har gjort forretninger med før, men som ikke er registrert i [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="725c4-133">You can use the same batch jobs to add opening balances whenever you register a new customer or vendor that you have done business with before but not registered in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="725c4-134">Bare søk etter den aktuelle oppgaven, og velg deretter den relevante koblingen.</span><span class="sxs-lookup"><span data-stu-id="725c4-134">Just search for the relevant task, and then choose the relevant link.</span></span>

## <a name="see-also"></a><span data-ttu-id="725c4-135">Se også</span><span class="sxs-lookup"><span data-stu-id="725c4-135">See Also</span></span>

[<span data-ttu-id="725c4-136">Bruke konfigurasjoner for nye selskaper</span><span class="sxs-lookup"><span data-stu-id="725c4-136">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="725c4-137">Konfigurere et selskap med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="725c4-137">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="725c4-138">Administrasjon</span><span class="sxs-lookup"><span data-stu-id="725c4-138">Administration</span></span>](admin-setup-and-administration.md)  
