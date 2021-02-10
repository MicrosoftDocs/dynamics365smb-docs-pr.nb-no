---
title: Administrere databasetilgangsformål i Business Central | Microsoft Docs
description: Endre databasetilgangsformålet for rapporter, API-sider og spørringer.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 6d79f5b2851df85ea9f19faeeb941eccfd1b397b
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752828"
---
# <a name="managing-database-access-intent"></a><span data-ttu-id="f7b1c-103">Administrere databasetilgangsformål</span><span class="sxs-lookup"><span data-stu-id="f7b1c-103">Managing Database Access Intent</span></span> 

<span data-ttu-id="f7b1c-104">Som superbruker eller administrator kan du endre databasetilgangsformålet i rapporter, sider av typen API og spørringer for å forbedre tjenestens ytelse.</span><span class="sxs-lookup"><span data-stu-id="f7b1c-104">As a super user or administrator, you can change the database access intent on reports, pages of the type API, and queries to improve performance of the service.</span></span>

## <a name="overview"></a><span data-ttu-id="f7b1c-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="f7b1c-105">Overview</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="f7b1c-106">kan konfigureres til å bruke skrivebeskyttede replikaer for den primære (lese-skrive) databasen.</span><span class="sxs-lookup"><span data-stu-id="f7b1c-106">can be set up to use read-only replicas of the primary (read-write) database.</span></span> <span data-ttu-id="f7b1c-107">Når du bruker databasereplikaen, reduseres belastningen på den primære databasen.</span><span class="sxs-lookup"><span data-stu-id="f7b1c-107">Using the database replica reduces the load on the primary database.</span></span> <span data-ttu-id="f7b1c-108">I noen tilfeller vil det også forbedre ytelsen ved visning av data i klienten.</span><span class="sxs-lookup"><span data-stu-id="f7b1c-108">In some cases, it will also improve the performance when viewing data in the client.</span></span> <span data-ttu-id="f7b1c-109">Replikaer er nyttige for objekter, for eksempel rapporter, spørringer og API-sider, som brukes til å vise data, og som ikke endrer data.</span><span class="sxs-lookup"><span data-stu-id="f7b1c-109">Replicas are beneficial for objects, like reports, queries, and API pages, that are used for viewing data only, not modifying data.</span></span>

<span data-ttu-id="f7b1c-110">Når objekter kjøres, bestemmer databasetilgangsformålet om det skal brukes en skrivebeskyttet replika, hvis en slik er tilgjengelig, eller den primære databasen.</span><span class="sxs-lookup"><span data-stu-id="f7b1c-110">When objects run, the database access intent determines whether to use a read-only replica, if one is available, or the primary database.</span></span> <span data-ttu-id="f7b1c-111">Rapporter, API-sider og spørringer er utviklet med et forhåndsdefinert databasetilgangsformål (se [Egenskapen DatabaseAccessIntent](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).</span><span class="sxs-lookup"><span data-stu-id="f7b1c-111">Reports, API pages, and queries are developed with a predefined database access intent (see [DatabaseAccessIntent property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).</span></span>

<span data-ttu-id="f7b1c-112">Siden **Liste over databasetilgangsformål** gjør det mulig å overstyre det forhåndsdefinerte databasetilgangsformålet for objekter når de kjøres.</span><span class="sxs-lookup"><span data-stu-id="f7b1c-112">The **Database Access Intent List** page lets you override the predefined database access intent for objects when they're run.</span></span>

<span data-ttu-id="f7b1c-113">I databasevilkårene kalles denne funksjonen vanligvis *leseutskalering*. Hvis du vil ha mer informasjon om leseutskalering og datatilgangsformål i [!INCLUDE[prod_short](includes/prod_short.md)], kan du se [Bruke leseutskalering for bedre ytelse](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) i [!INCLUDE[prod_short](includes/prod_short.md)] Developer og hjelpen for administrasjon.</span><span class="sxs-lookup"><span data-stu-id="f7b1c-113">In database terms, this feature is commonly known as *read scale-out*. For more information about read-scale out and data access intent in [!INCLUDE[prod_short](includes/prod_short.md)], see [Utilizing Read Scale-Out for Better Performance](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) in the [!INCLUDE[prod_short](includes/prod_short.md)] Developer and Administration help.</span></span>

## <a name="to-change-the-database-access-intent"></a><span data-ttu-id="f7b1c-114">Slik endrer du databasetilgangsformålet</span><span class="sxs-lookup"><span data-stu-id="f7b1c-114">To change the database access intent</span></span>

1. <span data-ttu-id="f7b1c-115">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Liste over databasetilgangsformål**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="f7b1c-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Database Access Intent List**, and then choose the related link.</span></span>

    <span data-ttu-id="f7b1c-116">Siden viser alle rapporter, sider og spørringer.</span><span class="sxs-lookup"><span data-stu-id="f7b1c-116">The page lists all reports, pages, and queries.</span></span> <span data-ttu-id="f7b1c-117">Kolonnen **Tilgangsformål** inneholder én av følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="f7b1c-117">The **Access Intent** column includes one of the following values:</span></span>

    |<span data-ttu-id="f7b1c-118">**Innstilling**</span><span class="sxs-lookup"><span data-stu-id="f7b1c-118">**Setting**</span></span>|<span data-ttu-id="f7b1c-119">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="f7b1c-119">**Description**</span></span>|  
    |------------|-------------|  
    |<span data-ttu-id="f7b1c-120">**Standard**</span><span class="sxs-lookup"><span data-stu-id="f7b1c-120">**Default**</span></span>|<span data-ttu-id="f7b1c-121">Angir at objektet bruker det forhåndsdefinerte databasetilgangsformålet.</span><span class="sxs-lookup"><span data-stu-id="f7b1c-121">Indicates that the object uses the predefined database access intent.</span></span>|
    |<span data-ttu-id="f7b1c-122">**Tillat skriving**</span><span class="sxs-lookup"><span data-stu-id="f7b1c-122">**Allow Write**</span></span>|<span data-ttu-id="f7b1c-123">Angir at objektet skal bruke den primære databasen, slik at brukeren kan endre data.</span><span class="sxs-lookup"><span data-stu-id="f7b1c-123">Sets the object to use the primary database, allowing the user to modify data.</span></span>|
    |<span data-ttu-id="f7b1c-124">**Skrivebeskyttet**</span><span class="sxs-lookup"><span data-stu-id="f7b1c-124">**Read Only**</span></span>|<span data-ttu-id="f7b1c-125">Angir at objektet skal bruke databasereplikaen, noe som betyr at brukeren bare kan vise data og ikke endre data.</span><span class="sxs-lookup"><span data-stu-id="f7b1c-125">Sets the object to use the database replica, which means that the user can only view data, not change data.</span></span>|

2. <span data-ttu-id="f7b1c-126">Velg handlingen **Rediger oversikt**.</span><span class="sxs-lookup"><span data-stu-id="f7b1c-126">Choose the **Edit List** action.</span></span>

3. <span data-ttu-id="f7b1c-127">På siden **Rediger – Liste over databasetilgangsformål** endrer du verdien i feltet **Tilgangsformål** for objektene.</span><span class="sxs-lookup"><span data-stu-id="f7b1c-127">On the **Edit - Database Access Intent List** page, change the **Access Intent** field for the objects.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f7b1c-128">Hvis et objekt som kan redigeres, for eksempel kundekortet, er satt til **Skrivebeskyttet**, vil den primære databasen fortsatt brukes, uavhengig av tilgangsformålet. Dermed kan brukere foreta endringer som normalt.</span><span class="sxs-lookup"><span data-stu-id="f7b1c-128">If an object that is editable, like the Customer Card, is set to **Read Only**, the primary database will still be used, regardless of the access intent, allowing users to make changes as normal.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="f7b1c-129">Se relatert opplæring på [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="f7b1c-129">See Related Training at [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="f7b1c-130">Se også</span><span class="sxs-lookup"><span data-stu-id="f7b1c-130">See Also</span></span>
[<span data-ttu-id="f7b1c-131">Forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="f7b1c-131">Business Functionality</span></span>](across-business-functionality.md)  
[<span data-ttu-id="f7b1c-132">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="f7b1c-132">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="f7b1c-133">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f7b1c-133">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="f7b1c-134">Komme i gang</span><span class="sxs-lookup"><span data-stu-id="f7b1c-134">Getting Started</span></span>](product-get-started.md)    

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
