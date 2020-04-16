---
title: Oppgradere en integrasjon med Dynamics 365 Sales | Microsoft Docs
description: Lær hvordan du klargjør Dynamics 365 Business Central for integrering med Dynamics 365 Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 95098397bd9554be6c993b6107963eba9a99c067
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196880"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a><span data-ttu-id="50066-103">Oppgradere en integrasjon med Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="50066-103">Upgrading an Integration with Dynamics 365 Sales</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="50066-104">kan også integreres med [!INCLUDE[d365fin](includes/cds_long_md.md)], som gjør det enkelt å koble til og synkronisere data med andre Dynamics 365-apper, for eksempel [!INCLUDE[crm_md](includes/crm_md.md)] eller til og med apper du lager selv.</span><span class="sxs-lookup"><span data-stu-id="50066-104">also integrates with [!INCLUDE[d365fin](includes/cds_long_md.md)], which makes it easy to connect and synchronize data with other Dynamics 365 applications, such as [!INCLUDE[crm_md](includes/crm_md.md)], or even apps that you build yourself.</span></span> <span data-ttu-id="50066-105">Hvis du integrerer for første gang, anbefales det at du gjør det via [!INCLUDE[d365fin](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="50066-105">If you are integrating for the first time, we recommend that you do so through [!INCLUDE[d365fin](includes/cds_long_md.md)].</span></span> <span data-ttu-id="50066-106">Hvis du vil ha mer informasjon, kan du se [Integrasjon med Common Data Service](admin-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="50066-106">For more information, see [Integration with Common Data Service](admin-common-data-service.md).</span></span>

<span data-ttu-id="50066-107">Hvis du allerede har integrert [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du fortsette å synkronisere data ved hjelp av konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="50066-107">If you have already integrated [!INCLUDE[crm_md](includes/crm_md.md)] with [!INCLUDE[d365fin](includes/d365fin_md.md)], you can continue to synchronize data using your setup.</span></span> <span data-ttu-id="50066-108">Hvis du imidlertid oppgraderer [!INCLUDE[d365fin](includes/d365fin_md.md)] eller slår av [!INCLUDE[crm_md](includes/crm_md.md)]-integreringen, må du slå den på igjen ved å koble til via [!INCLUDE[d365fin](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="50066-108">However, if you upgrade [!INCLUDE[d365fin](includes/d365fin_md.md)], or turn off your [!INCLUDE[crm_md](includes/crm_md.md)] integration, to turn it on again you must connect through [!INCLUDE[d365fin](includes/cds_long_md.md)].</span></span> 

> [!NOTE]
> <span data-ttu-id="50066-109">Når du kobler til på nytt via [!INCLUDE[d365fin](includes/cds_long_md.md)], brukes standard synkroniseringsinnstillinger, og eventuelle konfigurasjoner blir overskrevet.</span><span class="sxs-lookup"><span data-stu-id="50066-109">Reconnecting through [!INCLUDE[d365fin](includes/cds_long_md.md)] will apply default synchronization settings, and will overwrite any configurations you have.</span></span> <span data-ttu-id="50066-110">Standard tabelltilordninger vil for eksempel bli brukt.</span><span class="sxs-lookup"><span data-stu-id="50066-110">For example, the default table mappings will be applied.</span></span>

## <a name="to-upgrade-your-connection-to-use-common-data-service"></a><span data-ttu-id="50066-111">Slik oppgraderer du tilkoblingen for å bruke Common Data Service</span><span class="sxs-lookup"><span data-stu-id="50066-111">To upgrade your connection to use Common Data Service</span></span>
1. <span data-ttu-id="50066-112">Åpne siden **Konfigurere Microsoft Dynamics 365-tilkobling** og velg **Aktiver** for å slå av den eksisterende tilkoblingen til [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="50066-112">Open the **Microsoft Dynamics 365 Connection Setup** page, choose the **Enable** toggle to turn off your existing connection to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
2. <span data-ttu-id="50066-113">Åpne siden **Tilkoblingsoppsett for Common Data Service** og velg **Aktiver** for å slå på tilkoblingen.</span><span class="sxs-lookup"><span data-stu-id="50066-113">Open the **Common Data Service Connection Setup** page, and choose the **Enable** toggle to turn on the connection.</span></span>
3. <span data-ttu-id="50066-114">Når du har aktivert CDS-tilkoblingen, er den grunnleggende løsningen for CDS-integrering for Business Central distribuert til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="50066-114">After you enable the CDS connection, the Business Central CDS Base Integration Solution is deployed to Common Data Service.</span></span>
4. <span data-ttu-id="50066-115">Åpne siden Konfigurere Microsoft Dynamics 365-tilkobling og velg Aktiver for å slå på tilkoblingen til [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="50066-115">On the Microsoft Dynamics 365 Connection Setup page, choose the Enable toggle to turn on the connection to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
5. <span data-ttu-id="50066-116">Når du har aktivert Sales-tilkoblingen, er løsningen for Business Central-integrasjon distribuert til Sales.</span><span class="sxs-lookup"><span data-stu-id="50066-116">After you enable the Sales connection, the Business Central Integration Solution is deployed to Sales.</span></span> <span data-ttu-id="50066-117">Dette gjør det mulig å integrere med enheter som er spesifikke for [!INCLUDE[crm_md](includes/crm_md.md)], for eksempel ordrer, tilbud og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="50066-117">This enables integration with entities that are specific to [!INCLUDE[crm_md](includes/crm_md.md)], such as sales orders, quotes, and invoices.</span></span>
6. <span data-ttu-id="50066-118">På siden **Tilkoblingsoppsett for Sales** velger du **Bruk standard synkroniseringsoppsett** til å initialisere integrasjonstabelltilordninger for [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="50066-118">On the **Sales Connection Setup** page, choose **Use Default Synchronization Setup** to initialize the integration table mappings for [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
7. <span data-ttu-id="50066-119">Velg deretter **Distribuer integreringsløsning på nytt** for å installere og konfigurere den oppgraderte løsningen for Business Central-integrasjon.</span><span class="sxs-lookup"><span data-stu-id="50066-119">Now choose **Redeploy Integration Solution** to install and configure the upgraded Business Central Integration Solution.</span></span>

## <a name="see-also"></a><span data-ttu-id="50066-120">Se også</span><span class="sxs-lookup"><span data-stu-id="50066-120">See Also</span></span>
[<span data-ttu-id="50066-121">Integrere med Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="50066-121">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[<span data-ttu-id="50066-122">Integrere med Common Data Service</span><span class="sxs-lookup"><span data-stu-id="50066-122">Integrating with Common Data Service</span></span>](admin-common-data-service.md)