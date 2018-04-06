---
title: Konfigurere ny selskaper ved hjelp av en Cmdlet | Microsoft-dokumentasjon
description: "I en rekke scenarier bør du laste ned og importere en konfigurasjonspakke uten å involvere brukerne eller bruke brukergrensesnittet i RapidStart Services. Du kan gjøre dette ved å bruke en Windows PowerShell-cmdlet."
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
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 9d248f2f8676c392451ae4a6f99932145f354f5b
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="configure-new-companies-using-a-cmdlet"></a><span data-ttu-id="6be61-104">Konfigurere ny selskaper ved hjelp av en Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6be61-104">Configure New Companies using a Cmdlet</span></span>
<span data-ttu-id="6be61-105">I en rekke scenarier bør du laste ned og importere en konfigurasjonspakke uten å involvere brukerne eller bruke brukergrensesnittet i RapidStart Services.</span><span class="sxs-lookup"><span data-stu-id="6be61-105">In a number of scenarios, you may want to load and import a configuration package without involving your users or using the RapidStart Services user interface.</span></span> <span data-ttu-id="6be61-106">Du kan gjøre dette ved å bruke en Windows PowerShell-cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6be61-106">You can do so by using a Windows PowerShell cmdlet.</span></span> <span data-ttu-id="6be61-107">Dette kan være nyttig i følgende scenarier:</span><span class="sxs-lookup"><span data-stu-id="6be61-107">Scenarios where this may be useful include:</span></span>  

- <span data-ttu-id="6be61-108">Utføre import på tvers av flere [!INCLUDE[d365fin](includes/d365fin_md.md)]-installasjoner.</span><span class="sxs-lookup"><span data-stu-id="6be61-108">Performing data import across multiple [!INCLUDE[d365fin](includes/d365fin_md.md)] installations.</span></span>
- <span data-ttu-id="6be61-109">Konfigurere flere programområder for flere kunder.</span><span class="sxs-lookup"><span data-stu-id="6be61-109">Configuring additional application areas for multiple customers.</span></span>  

## <a name="to-deploy-a-configuration-package-using-a-cmdlet"></a><span data-ttu-id="6be61-110">Slik distribuerer du en konfigurasjonspakke ved å bruke en cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6be61-110">To deploy a configuration package using a cmdlet</span></span>  

1. <span data-ttu-id="6be61-111">Forberede en pakke RapidStart Services.</span><span class="sxs-lookup"><span data-stu-id="6be61-111">Prepare a RapidStart Services package.</span></span> <span data-ttu-id="6be61-112">Du kan for eksempel opprette en pakke for å importere bestemte verdier og navnene på tabellen og feltene som verdiene skal settes inn i.</span><span class="sxs-lookup"><span data-stu-id="6be61-112">For example, you can create a package to import certain values and the names of the table and the fields to insert these values into.</span></span>  
2. <span data-ttu-id="6be61-113">Plasser pakken på en datamaskin der du vil kjøre cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6be61-113">Place the package on a computer where you will run the cmdlet.</span></span>  
3. <span data-ttu-id="6be61-114">Åpne administrasjonsskallet for [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6be61-114">Open the [!INCLUDE[d365fin](includes/d365fin_md.md)] administration shell.</span></span>  
4. <span data-ttu-id="6be61-115">Angi **Invoke-NAVCodeUnit**, og angi informasjon som ligner følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="6be61-115">Enter **Invoke-NAVCodeUnit**, and specify information similar to the following example.</span></span>  
    ```powershell  
    Invoke-NAVCodeunit -Tenant Default -CompanyName "CRONUS International Ltd." -CodeunitId 8620 -MethodName ImportRapidStartPackage -Argument "C:TEMPRS_CONFIG.rapidstart" -ServerInstance DynamicsNAV71  

    ```
<span data-ttu-id="6be61-116">Cmdleten importerer pakken til hvert selskap.</span><span class="sxs-lookup"><span data-stu-id="6be61-116">The cmdlet imports the package into each company.</span></span> <span data-ttu-id="6be61-117">Brukere kan begynne å bruke den nye funksjonaliteten umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="6be61-117">Users can start to use the new functionality immediately.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6be61-118">Se også</span><span class="sxs-lookup"><span data-stu-id="6be61-118">See Also</span></span>  
[<span data-ttu-id="6be61-119">Konfigurere nye selskaper</span><span class="sxs-lookup"><span data-stu-id="6be61-119">Configure New Companies</span></span>](admin-how-to-configure-new-companies.md)  
[<span data-ttu-id="6be61-120">Bruke konfigurasjoner for nye selskaper</span><span class="sxs-lookup"><span data-stu-id="6be61-120">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="6be61-121">Konfigurere et selskap med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="6be61-121">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="6be61-122">Administrasjon</span><span class="sxs-lookup"><span data-stu-id="6be61-122">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="6be61-123">Microsoft Dynamics NAV Windows PowerShell-cmdleter</span><span class="sxs-lookup"><span data-stu-id="6be61-123">Microsoft Dynamics NAV Windows PowerShell Cmdlets</span></span>](/dynamics-nav/microsoft-dynamics-nav-windows-powershell-cmdlets)

