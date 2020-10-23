---
title: Oppgradere en integrasjon med Dynamics 365 Sales
description: Lær hvordan du kan flytte Dynamics 365 Business Central-integrasjonen med Dynamics 365 Sales til den nyeste versjonen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 3bb6b26e011afc515fbd4f492f56b3090c56e860
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922370"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a><span data-ttu-id="6a766-103">Oppgradere en integrasjon med Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="6a766-103">Upgrading an Integration with Dynamics 365 Sales</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="6a766-104">kan integreres med [!INCLUDE[d365fin](includes/cds_long_md.md)], som gjør det enkelt å koble til og synkronisere data med andre Dynamics 365-apper, for eksempel [!INCLUDE[crm_md](includes/crm_md.md)] eller til og med apper du lager selv.</span><span class="sxs-lookup"><span data-stu-id="6a766-104">integrates with [!INCLUDE[d365fin](includes/cds_long_md.md)], which makes it easy to connect and synchronize data with other Dynamics 365 applications, such as [!INCLUDE[crm_md](includes/crm_md.md)], or even apps that you build yourself.</span></span> <span data-ttu-id="6a766-105">Hvis du integrerer for første gang, anbefales det at du gjør det via [!INCLUDE[d365fin](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6a766-105">If you are integrating for the first time, we recommend that you do so through [!INCLUDE[d365fin](includes/cds_long_md.md)].</span></span> <span data-ttu-id="6a766-106">Hvis du vil ha mer informasjon, kan du se [Integrasjon med Common Data Service](admin-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="6a766-106">For more information, see [Integration with Common Data Service](admin-common-data-service.md).</span></span>

<span data-ttu-id="6a766-107">Hvis du allerede har integrert [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du fortsette å synkronisere data ved hjelp av konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="6a766-107">If you have already integrated [!INCLUDE[crm_md](includes/crm_md.md)] with [!INCLUDE[d365fin](includes/d365fin_md.md)], you can continue to synchronize data using your setup.</span></span> <span data-ttu-id="6a766-108">Hvis du imidlertid oppgraderer [!INCLUDE[d365fin](includes/d365fin_md.md)] eller slår av [!INCLUDE[crm_md](includes/crm_md.md)]-integreringen, må du slå den på igjen ved å koble til via [!INCLUDE[d365fin](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6a766-108">However, if you upgrade [!INCLUDE[d365fin](includes/d365fin_md.md)], or turn off your [!INCLUDE[crm_md](includes/crm_md.md)] integration, to turn it on again you must connect through [!INCLUDE[d365fin](includes/cds_long_md.md)].</span></span> 

> [!NOTE]
> <span data-ttu-id="6a766-109">Når du kobler til på nytt via [!INCLUDE[d365fin](includes/cds_long_md.md)], brukes standard synkroniseringsinnstillinger, og eventuelle konfigurasjoner blir overskrevet.</span><span class="sxs-lookup"><span data-stu-id="6a766-109">Reconnecting through [!INCLUDE[d365fin](includes/cds_long_md.md)] will apply default synchronization settings, and will overwrite any configurations you have.</span></span> <span data-ttu-id="6a766-110">Standard tabelltilordninger vil for eksempel bli brukt.</span><span class="sxs-lookup"><span data-stu-id="6a766-110">For example, the default table mappings will be applied.</span></span>

## <a name="to-upgrade-your-connection-to-use-common-data-service"></a><span data-ttu-id="6a766-111">Slik oppgraderer du tilkoblingen for å bruke Common Data Service</span><span class="sxs-lookup"><span data-stu-id="6a766-111">To upgrade your connection to use Common Data Service</span></span>
1. <span data-ttu-id="6a766-112">Åpne siden **Konfigurere Microsoft Dynamics 365-tilkobling** og velg **Aktiver** for å slå av den eksisterende tilkoblingen til [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6a766-112">Open the **Microsoft Dynamics 365 Connection Setup** page, choose the **Enable** toggle to turn off your existing connection to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
2. <span data-ttu-id="6a766-113">Åpne siden **Tilkoblingsoppsett for Common Data Service** og velg **Aktiver** for å slå på tilkoblingen.</span><span class="sxs-lookup"><span data-stu-id="6a766-113">Open the **Common Data Service Connection Setup** page, and choose the **Enable** toggle to turn on the connection.</span></span>
  
   <span data-ttu-id="6a766-114">Når du har aktivert CDS-tilkoblingen, er den grunnleggende løsningen for CDS-integrering for Business Central distribuert til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="6a766-114">After you enable the CDS connection, the Business Central CDS Base Integration Solution is deployed to Common Data Service.</span></span>
3. <span data-ttu-id="6a766-115">Avinstaller løsningen for integrering av Microsoft Dynamics 365 Business Central fra Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="6a766-115">Uninstall the Microsoft Dynamics 365 Business Central Integration solution from your Dynamics 365 Sales.</span></span> <span data-ttu-id="6a766-116">Hvis du vil ha mer informasjon, kan du se [emnet om å avinstallere eller slette en løsning](/powerapps/developer/common-data-service/uninstall-delete-solution).</span><span class="sxs-lookup"><span data-stu-id="6a766-116">For more information, see [Uninstall or delete a solution topic](/powerapps/developer/common-data-service/uninstall-delete-solution).</span></span> 

4. <span data-ttu-id="6a766-117">Åpne siden **Konfigurasjon for Microsoft Dynamics 365-tilkobling**, og aktiver veksleknappen **Aktiver** for å koble til [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6a766-117">On the **Microsoft Dynamics 365 Connection Setup** page, turn on the **Enable** toggle to connect to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
  
   <span data-ttu-id="6a766-118">Når du har aktivert Sales-tilkoblingen, er løsningen for Business Central-integrasjon distribuert til Sales.</span><span class="sxs-lookup"><span data-stu-id="6a766-118">After you enable the Sales connection, the Business Central Integration Solution is deployed to Sales.</span></span> <span data-ttu-id="6a766-119">Dette gjør det mulig å integrere med enheter som er spesifikke for [!INCLUDE[crm_md](includes/crm_md.md)], for eksempel ordrer, tilbud og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="6a766-119">This enables integration with entities that are specific to [!INCLUDE[crm_md](includes/crm_md.md)], such as sales orders, quotes, and invoices.</span></span>
5. <span data-ttu-id="6a766-120">På siden **Tilkoblingsoppsett for Sales** velger du **Bruk standard synkroniseringsoppsett** til å initialisere integrasjonstabelltilordninger for [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6a766-120">On the **Sales Connection Setup** page, choose **Use Default Synchronization Setup** to initialize the integration table mappings for [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="6a766-121">Se også</span><span class="sxs-lookup"><span data-stu-id="6a766-121">See Also</span></span>
[<span data-ttu-id="6a766-122">Integrere med Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="6a766-122">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[<span data-ttu-id="6a766-123">Integrere med Common Data Service</span><span class="sxs-lookup"><span data-stu-id="6a766-123">Integrating with Common Data Service</span></span>](admin-common-data-service.md)
