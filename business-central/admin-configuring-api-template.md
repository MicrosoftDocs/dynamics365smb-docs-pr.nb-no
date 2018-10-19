---
title: Konfigurere API-maler | Microsoft Docs
description: "Beskrive trinnene du må gå gjennom for å konfigurere API-maler for Dynamics 365 Business Central."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API templates, configuring templates
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 2dfa62c765a653986de2069ef26e454928d68ee3
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---

# <a name="configuring-api-templates"></a><span data-ttu-id="058e7-103">Konfigurere API-maler</span><span class="sxs-lookup"><span data-stu-id="058e7-103">Configuring API Templates</span></span>
<span data-ttu-id="058e7-104">API-biblioteket for [!INCLUDE[d365fin_md](includes/d365fin_md.md)] gir en forenklet visning av de underliggende enhetene.</span><span class="sxs-lookup"><span data-stu-id="058e7-104">The API library for [!INCLUDE[d365fin_md](includes/d365fin_md.md)] provides a simplified representation of the underlying entities.</span></span> <span data-ttu-id="058e7-105">Alle egenskapene i programmet vises ikke via det tilknyttede API-et.</span><span class="sxs-lookup"><span data-stu-id="058e7-105">All the properties in the application are not exposed through the associated API.</span></span> <span data-ttu-id="058e7-106">I **API-oppsett**-vinduet kan du definere maler som brukes til å fylle ut tomme egenskaper på en enhet når du oppretter en POST-handling gjennom API-et.</span><span class="sxs-lookup"><span data-stu-id="058e7-106">The **API Setup** window allows you to define templates that are used to populate empty properties on an entity when you create a POST action through the API.</span></span> 

<span data-ttu-id="058e7-107">Hvis for eksempel en konfigurasjonsmal er definert for vareenheten, når en ny varepost opprettes gjennom vare-API-et, blir egenskaper for den nye varen som ikke er definert i API-kallet, fylt ut fra den valgte malen.</span><span class="sxs-lookup"><span data-stu-id="058e7-107">For example, if a configuration template is defined for the item entity, when a new item record is created through the items API, any properties for the new item that are not defined in the API call will be populated from the selected template.</span></span> <span data-ttu-id="058e7-108">Hvis for eksempel ingen verdi er definert for **Bokføringsgruppe - vare**-feltet gjennom API-et, men en verdi er definert i den valgte malen, brukes bokføringsgruppeverdien som er definert i malen, for den nye varen.</span><span class="sxs-lookup"><span data-stu-id="058e7-108">If, for example, no value is defined for the **Gen. Prod. Posting Group** field through the API, but a value is defined in the selected template, then the posting group value defined in the template will be applied to the new item.</span></span> 

## <a name="setting-up-the-entity-template"></a><span data-ttu-id="058e7-109">Definere enhetsmalen</span><span class="sxs-lookup"><span data-stu-id="058e7-109">Setting up the Entity Template</span></span>
<span data-ttu-id="058e7-110">Hvis du vil bruke maler med API-biblioteket, må du først konfigurere og definere egenskaper for malene.</span><span class="sxs-lookup"><span data-stu-id="058e7-110">To use templates with the API library, you must first set up and define properties for the templates.</span></span> <span data-ttu-id="058e7-111">Du kan sette opp malene i vinduet **Konfigurasjonsmaler**.</span><span class="sxs-lookup"><span data-stu-id="058e7-111">You can set up these templates in the **Configuration Templates** window.</span></span> <span data-ttu-id="058e7-112">Hvis du vil ha mer informasjon, kan du se [Klargjøre for å flytte kundedata](admin-use-templates-to-prepare-customer-data-for-migration.md).</span><span class="sxs-lookup"><span data-stu-id="058e7-112">For more information, see [Prepare to Migrate Customer Data](admin-use-templates-to-prepare-customer-data-for-migration.md).</span></span> 

## <a name="assign-the-template-to-an-api"></a><span data-ttu-id="058e7-113">Tilordne malen til et API</span><span class="sxs-lookup"><span data-stu-id="058e7-113">Assign the template to an API</span></span>

<span data-ttu-id="058e7-114">Hvis du vil tilordne en mal til et API, må du gå gjennom fremgangsmåten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="058e7-114">To assign a template to an API, you must go through the following steps.</span></span>

1. <span data-ttu-id="058e7-115">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **API-oppsett**, og velg den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="058e7-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **API Setup**, and choose the related link.</span></span>
2. <span data-ttu-id="058e7-116">Velg **Ny**, og velg deretter **Rekkefølge**-verdien for posten.</span><span class="sxs-lookup"><span data-stu-id="058e7-116">Choose **New**, and then choose the **Order** value for the record.</span></span>  
<span data-ttu-id="058e7-117">Hvis det er mer enn én mal som er valgt for et API (side-ID), brukes malene i rekkefølgen som er definert i **Rekkefølge**-kolonnen.</span><span class="sxs-lookup"><span data-stu-id="058e7-117">If there is more than one template selected for an API (Page ID), the templates are applied in the order defined in the **Order** column.</span></span>   
<span data-ttu-id="058e7-118">Når hver mal er brukt, brukes bare feltverdiene som er definert i malen, på felt som ikke allerede har fått en verdi definert, enten eksplisitt i API-et eller i en mal som er brukt tidligere i rekkefølgen.</span><span class="sxs-lookup"><span data-stu-id="058e7-118">When each template is applied, field values defined in the template are only applied to fields that have not already had a value defined, either explicitly in the API, or in a previously applied template in the order.</span></span> 
3. <span data-ttu-id="058e7-119">Velg en verdi for **Side-ID**.</span><span class="sxs-lookup"><span data-stu-id="058e7-119">Select a **Page ID** value.</span></span>  
<span data-ttu-id="058e7-120">Dette er siden for API-et som malen skal brukes på.</span><span class="sxs-lookup"><span data-stu-id="058e7-120">This is the page for the API to which the template will be applied.</span></span> <span data-ttu-id="058e7-121">**Side-ID**-oppslaget gir en oversikt over alle API-er som er tilgjengelige i biblioteket.</span><span class="sxs-lookup"><span data-stu-id="058e7-121">The **Page ID** lookup provides a list of all APIs available in the library.</span></span>
4. <span data-ttu-id="058e7-122">Velg en verdi i **Malkode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="058e7-122">Select a value in the **Template Code** field.</span></span>  
<span data-ttu-id="058e7-123">Malkoden er koden for malen som ble definert i **Konfigurasjonsmaler**-vinduet.</span><span class="sxs-lookup"><span data-stu-id="058e7-123">The template code is the code for the template that was defined in the **Configuration Templates** window.</span></span> <span data-ttu-id="058e7-124">Malverdiene som er definert, brukes på API-et.</span><span class="sxs-lookup"><span data-stu-id="058e7-124">The template values defined are applied to the API.</span></span> 
5. <span data-ttu-id="058e7-125">I feltet **Betingelser** angir du hvilken mal som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="058e7-125">In the **Conditions** field, specify which template should be applied.</span></span>  
<span data-ttu-id="058e7-126">Den definerte malen brukes på en ny post som er opprettet gjennom API-et, hvis, og bare hvis, betingelsene som er definert i **Betingelser**-feltet er oppfylt av verdiene som allerede er definert for den nye forekomsten av enheten.</span><span class="sxs-lookup"><span data-stu-id="058e7-126">The defined template is applied to a new record created through the API if, and only if, the conditions defined in the **Conditions** field are met by the values already defined for the new instance of the entity.</span></span>

## <a name="see-also"></a><span data-ttu-id="058e7-127">Se også</span><span class="sxs-lookup"><span data-stu-id="058e7-127">See Also</span></span>
[<span data-ttu-id="058e7-128">API-dokumentasjon</span><span class="sxs-lookup"><span data-stu-id="058e7-128">API Documentation</span></span>](/dynamics-nav/fin-graph)  
<span data-ttu-id="058e7-129">[Utvikle tilkoblingsapper for [!INCLUDE[d365fin_md](includes/d365fin_md.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)</span><span class="sxs-lookup"><span data-stu-id="058e7-129">[Developing Connect Apps for [!INCLUDE[d365fin_md](includes/d365fin_md.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)</span></span>  
[<span data-ttu-id="058e7-130">Aktivere API-ene</span><span class="sxs-lookup"><span data-stu-id="058e7-130">Enabling the APIs</span></span>](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[<span data-ttu-id="058e7-131">Endepunkt for API-ene</span><span class="sxs-lookup"><span data-stu-id="058e7-131">Endpoints for the APIs</span></span>](/dynamics-nav/endpoints-apis-for-dynamics)  
[<span data-ttu-id="058e7-132">Konfigurere et selskap med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="058e7-132">Setting Up a Company with RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="058e7-133">Administrasjon</span><span class="sxs-lookup"><span data-stu-id="058e7-133">Administration</span></span>](admin-setup-and-administration.md)
