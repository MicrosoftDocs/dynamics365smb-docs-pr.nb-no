---
title: Oppgradere en integrasjon med Dynamics 365 Sales
description: Lær hvordan du kan flytte Dynamics 365 Business Central-integrasjonen med Dynamics 365 Sales til den nyeste versjonen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 4e3b79d6245a0f1b8277c94faa58c24edc66662e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777019"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a><span data-ttu-id="818e1-103">Oppgradere en integrasjon med Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="818e1-103">Upgrading an Integration with Dynamics 365 Sales</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="818e1-104">kan integreres med [!INCLUDE[prod_short](includes/cds_long_md.md)], som gjør det enkelt å koble til og synkronisere data med andre Dynamics 365-apper, for eksempel [!INCLUDE[crm_md](includes/crm_md.md)] eller til og med apper du lager selv.</span><span class="sxs-lookup"><span data-stu-id="818e1-104">integrates with [!INCLUDE[prod_short](includes/cds_long_md.md)], which makes it easy to connect and synchronize data with other Dynamics 365 applications, such as [!INCLUDE[crm_md](includes/crm_md.md)], or even apps that you build yourself.</span></span> <span data-ttu-id="818e1-105">Hvis du integrerer for første gang, anbefales det at du gjør det via [!INCLUDE[prod_short](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="818e1-105">If you are integrating for the first time, we recommend that you do so through [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> <span data-ttu-id="818e1-106">Hvis du vil ha mer informasjon, kan du se [Integrasjon med Dataverse](admin-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="818e1-106">For more information, see [Integration with Dataverse](admin-common-data-service.md).</span></span>

<span data-ttu-id="818e1-107">Hvis du allerede har integrert [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[prod_short](includes/prod_short.md)], kan du fortsette å synkronisere data ved hjelp av konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="818e1-107">If you have already integrated [!INCLUDE[crm_md](includes/crm_md.md)] with [!INCLUDE[prod_short](includes/prod_short.md)], you can continue to synchronize data using your setup.</span></span> <span data-ttu-id="818e1-108">Hvis du imidlertid oppgraderer [!INCLUDE[prod_short](includes/prod_short.md)] eller slår av [!INCLUDE[crm_md](includes/crm_md.md)]-integreringen, må du slå den på igjen ved å koble til via [!INCLUDE[prod_short](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="818e1-108">However, if you upgrade [!INCLUDE[prod_short](includes/prod_short.md)], or turn off your [!INCLUDE[crm_md](includes/crm_md.md)] integration, to turn it on again you must connect through [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> 

> [!NOTE]
> <span data-ttu-id="818e1-109">Når du kobler til på nytt via [!INCLUDE[prod_short](includes/cds_long_md.md)], brukes standard synkroniseringsinnstillinger, og eventuelle konfigurasjoner blir overskrevet.</span><span class="sxs-lookup"><span data-stu-id="818e1-109">Reconnecting through [!INCLUDE[prod_short](includes/cds_long_md.md)] will apply default synchronization settings, and will overwrite any configurations you have.</span></span> <span data-ttu-id="818e1-110">Standard tabelltilordninger vil for eksempel bli brukt.</span><span class="sxs-lookup"><span data-stu-id="818e1-110">For example, the default table mappings will be applied.</span></span>

## <a name="to-upgrade-your-connection-to-use-dataverse"></a><span data-ttu-id="818e1-111">Slik oppgraderer du tilkoblingen for å bruke Dataverse</span><span class="sxs-lookup"><span data-stu-id="818e1-111">To upgrade your connection to use Dataverse</span></span>
1. <span data-ttu-id="818e1-112">Åpne siden **Tilkoblingsoppsett for Microsoft Dynamics 365**, og deaktiver vekslebryteren **Aktivert** for å koble fra [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="818e1-112">Open the **Microsoft Dynamics 365 Connection Setup** page, and then turn off the **Enabled** toggle to disconnect from [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
2. <span data-ttu-id="818e1-113">Åpne siden **Tilkoblingsoppsett for Dataverse** og velg **Aktivert** for å aktivere tilkoblingen til [!INCLUDE[prod_short](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="818e1-113">Open the **Dataverse Connection Setup** page, and choose the **Enabled** toggle to turn on the connection to [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span>
  
   > [!NOTE]
   > <span data-ttu-id="818e1-114">Når du har aktivert tilkoblingen, er Business Central-integreringsløsningen distribuert til Dataverse.</span><span class="sxs-lookup"><span data-stu-id="818e1-114">After you enable the connection, the Business Central Integration Solution is deployed to Dataverse.</span></span>
3. <span data-ttu-id="818e1-115">Velg **Distribuer integreringsløsning på nytt** for å installere Business Central-integreringsløsningen på nytt.</span><span class="sxs-lookup"><span data-stu-id="818e1-115">Choose **Redeploy Integration Solution** to reinstall the Business Central Integration Solution.</span></span>
4. <span data-ttu-id="818e1-116">Åpne siden **Konfigurasjon for Microsoft Dynamics 365-tilkobling**, og aktiver veksleknappen **Aktivert** for å koble til [!INCLUDE[crm_md](includes/crm_md.md)] på nytt.</span><span class="sxs-lookup"><span data-stu-id="818e1-116">On the **Microsoft Dynamics 365 Connection Setup** page, turn on the **Enabled** toggle to reconnect to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
  
   > [!NOTE]
   > <span data-ttu-id="818e1-117">Når du har aktivert tilkoblingen, er Business Central-integreringsløsningen distribuert til [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="818e1-117">After you enable the connection, the Business Central Integration Solution is deployed to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="818e1-118">Dette gjør det mulig å integrere med tabeller som er spesifikke for [!INCLUDE[crm_md](includes/crm_md.md)], for eksempel ordrer, tilbud og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="818e1-118">This enables integration with tables that are specific to [!INCLUDE[crm_md](includes/crm_md.md)], such as sales orders, quotes, and invoices.</span></span>
5. <span data-ttu-id="818e1-119">Velg **Distribuer integreringsløsning på nytt** for å installere Business Central-integreringsløsningen på nytt.</span><span class="sxs-lookup"><span data-stu-id="818e1-119">Choose **Redeploy Integration Solution** to reinstall the Business Central Integration Solution.</span></span>
6. <span data-ttu-id="818e1-120">På siden **Tilkoblingsoppsett for Sales** velger du **Bruk standard synkroniseringsoppsett** til å initialisere integrasjonstabelltilordninger for [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="818e1-120">On the **Sales Connection Setup** page, choose **Use Default Synchronization Setup** to initialize the integration table mappings for [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="818e1-121">Se også</span><span class="sxs-lookup"><span data-stu-id="818e1-121">See Also</span></span>
[<span data-ttu-id="818e1-122">Integrere med Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="818e1-122">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[<span data-ttu-id="818e1-123">Integrere med Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="818e1-123">Integrating with Microsoft Dataverse</span></span>](admin-common-data-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]