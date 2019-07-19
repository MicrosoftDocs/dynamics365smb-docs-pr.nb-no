---
title: Bruke rollesenteret for RapidStart Services-implementerer | Microsoft-dokumentasjon
description: Når du bruker RapidStart Services, anbefaler vi at du sporer arbeidet og bruker rollesenteret for RapidStart Services-implementereren som gir riktig kontekst for konfigurasjonsarbeidet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: /dynamics365/business-central/admin-set-up-company-configuration
ROBOTS: NOINDEX
ms.openlocfilehash: e1cfcc47d5fb1112c4422be93ab49a345e9a30ec
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726908"
---
# <a name="use-the-rapidstart-services-implementer-role-center"></a><span data-ttu-id="b8259-103">Bruke rollesenteret for RapidStart Services-implementerer</span><span class="sxs-lookup"><span data-stu-id="b8259-103">Use the RapidStart Services Implementer Role Center</span></span>
<span data-ttu-id="b8259-104">Når du bruker RapidStart Services, anbefaler vi at du bruker rollesenteret for RapidStart Services-implementereren som gir riktig kontekst for konfigurasjonsarbeidet.</span><span class="sxs-lookup"><span data-stu-id="b8259-104">When you use RapidStart Services, we recommend that you use the RapidStart Services Implementer Role Center as it provides the correct context for your configuration work.</span></span> <span data-ttu-id="b8259-105">Hvis du vil ha mer informasjon, kan du se [Endre rollesenter](ui-change-basic-settings.md#to-change-role-center).</span><span class="sxs-lookup"><span data-stu-id="b8259-105">For more information, see [To change Role Center](ui-change-basic-settings.md#to-change-role-center).</span></span>

<span data-ttu-id="b8259-106">Når du fortsetter arbeidet, kan du tilordne hver tabell statusen som gjenspeiler hvor du er i prosessen.</span><span class="sxs-lookup"><span data-stu-id="b8259-106">As you continue with your work, you can assign each table the status that reflects where you are in the process.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="b8259-107">holder deretter orden på tabellstatusen i **Aktiviteter**-delen i rollesenteret.</span><span class="sxs-lookup"><span data-stu-id="b8259-107">then keeps track of the table status in the **Activities** part on the Role Center.</span></span>  

<span data-ttu-id="b8259-108">Når du legger til en tabell i konfigurasjonsforslaget, er statusen angitt til tom som standard.</span><span class="sxs-lookup"><span data-stu-id="b8259-108">By default, when you add a table to the configuration worksheet, its status is set to blank.</span></span> <span data-ttu-id="b8259-109">Dette betyr at konfigurasjonen av tabellen ikke har begynt.</span><span class="sxs-lookup"><span data-stu-id="b8259-109">This means that configuration of the table has not begun.</span></span> <span data-ttu-id="b8259-110">Dette gjenspeiles i **Ikke startet**-antallet i **Aktiviteter**-flisen.</span><span class="sxs-lookup"><span data-stu-id="b8259-110">This is reflected in the **Not Started** count in the **Activities** tile.</span></span>  

## <a name="to-update-the-status-of-a-configuration-table"></a><span data-ttu-id="b8259-111">Slik oppdaterer du statusen for en konfigurasjonstabell:</span><span class="sxs-lookup"><span data-stu-id="b8259-111">To update the status of a configuration table</span></span>  
1.  <span data-ttu-id="b8259-112">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konfigurasjonsforslag**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b8259-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Configuration Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b8259-113">Velg handlingen **Rediger oversikt**.</span><span class="sxs-lookup"><span data-stu-id="b8259-113">Choose the **Edit List** action.</span></span>  
3.  <span data-ttu-id="b8259-114">Velg en tabell og velg den aktuelle statusen i **Status**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b8259-114">Select a table, and in the **Status** field, choose the appropriate status.</span></span>  
4.  <span data-ttu-id="b8259-115">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="b8259-115">Choose the **OK** button.</span></span>  

<span data-ttu-id="b8259-116">Når du går tilbake til rollesenteret, oppdateres flisene i **Aktiviteter**-delen for å gjenspeile endringene.</span><span class="sxs-lookup"><span data-stu-id="b8259-116">When you return to the Role Center, the tiles in the **Activities** part are updated to reflect your changes.</span></span>  

## <a name="to-track-the-status-of-a-configuration-project"></a><span data-ttu-id="b8259-117">Slik sporer du statusen for et konfigurasjonsprosjekt:</span><span class="sxs-lookup"><span data-stu-id="b8259-117">To track the status of a configuration project</span></span>  
- <span data-ttu-id="b8259-118">Åpne rollesenteret for RapidStart Services.</span><span class="sxs-lookup"><span data-stu-id="b8259-118">Open the RapidStart Services Role Center.</span></span>  

<span data-ttu-id="b8259-119">I **Konfigurasjonsområder**-delen vises fullføringsstatistikken for områder og grupper du har definert i konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="b8259-119">In the **Configuration Areas** part, completion statistics are shown for the areas and groups that you have set up.</span></span> <span data-ttu-id="b8259-120">Hvis du ikke har definert noen grupper eller områder, er det ikke data i denne delen.</span><span class="sxs-lookup"><span data-stu-id="b8259-120">If you have not set up any groups or areas, this part has no data.</span></span>  

## <a name="to-see-a-filtered-view-of-table-status"></a><span data-ttu-id="b8259-121">Vise en filtrert visning av tabellstatus</span><span class="sxs-lookup"><span data-stu-id="b8259-121">To see a filtered view of table status</span></span>  
1. <span data-ttu-id="b8259-122">Velg handlingen **Tabeller**.</span><span class="sxs-lookup"><span data-stu-id="b8259-122">Choose the **Tables** action.</span></span>  
2. <span data-ttu-id="b8259-123">Velg den aktuelle filtrerte visningen.</span><span class="sxs-lookup"><span data-stu-id="b8259-123">Select the appropriate filtered view.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b8259-124">Se også</span><span class="sxs-lookup"><span data-stu-id="b8259-124">See Also</span></span>  
[<span data-ttu-id="b8259-125">Konfigurere et selskap med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="b8259-125">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="b8259-126">Administrasjon</span><span class="sxs-lookup"><span data-stu-id="b8259-126">Administration</span></span>](admin-setup-and-administration.md)
