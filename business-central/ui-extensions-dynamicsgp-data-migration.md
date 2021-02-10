---
title: Overføre data fra Dynamics GP før 15.3 | Microsoft Docs
description: Før 15.3-oppdateringen kunne du bruke utvidelsen Dynamics GP-datamigrering til å overføre kunder, leverandører, lagervarer, finanskonti og åpne transaksjoner med skyldige beløp og tilgodehavender fra Dynamics GP til Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 10/01/2020
ms.author: edupont
ROBOTS: NOINDEX
ms.openlocfilehash: a8f6c35d031cdbe6376ed57ea9ba2e9ce79188b4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757270"
---
# <a name="the-dynamics-gp-data-migration-extension"></a><span data-ttu-id="a7f76-103">Utvidelsen for Dynamics GP datamigrering</span><span class="sxs-lookup"><span data-stu-id="a7f76-103">The Dynamics GP Data Migration Extension</span></span>

> [!NOTE]
> <span data-ttu-id="a7f76-104">Denne utvidelsen er avskrevet i 15.3-oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="a7f76-104">This extension is deprecated in the 15.3 update.</span></span> <span data-ttu-id="a7f76-105">Vi anbefaler at brukere som vil overføre fra Dynamics GP, begynner å bruke veiviseren for **skyoverføring** i stedet.</span><span class="sxs-lookup"><span data-stu-id="a7f76-105">We recommend that users who want to migrate from Dynamics GP start using the **Cloud Migration** wizard instead.</span></span> <span data-ttu-id="a7f76-106">Utvidelsen for **skyoverføring** har mer robust funksjonalitet og henter flere data til Business Central fra Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="a7f76-106">The **Cloud Migration** extension has more robust functionality and brings more data into Business Central from Dynamics GP.</span></span> <span data-ttu-id="a7f76-107">Hvis du vil ha mer informasjon, kan du se [Overføre til Business Central Online fra Dynamics GP](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp) i administrasjonsinnholdet for [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="a7f76-107">For more information, see [Migrate to Business Central Online from Dynamics GP](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp) in the administration content for [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="a7f76-108">Se også</span><span class="sxs-lookup"><span data-stu-id="a7f76-108">See Also</span></span>

[<span data-ttu-id="a7f76-109">Intelligente skyutvidelser for skyoverføring</span><span class="sxs-lookup"><span data-stu-id="a7f76-109">Intelligent Cloud Extensions for Cloud Migration</span></span>](ui-extensions-data-replication.md)  
[<span data-ttu-id="a7f76-110">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="a7f76-110">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="a7f76-111">[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av utvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="a7f76-111">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)</span></span>  
[<span data-ttu-id="a7f76-112">Overføre til Business Central Online fra Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="a7f76-112">Migrate to Business Central Online from Dynamics GP</span></span>](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp)  
