---
title: Se gjennom og tilpasse eksisterende databasedata | Microsoft-dokumentasjon
description: Når du oppretter en konfigurasjonpakke for en løsning, kan du vise og tilpasse de tilgjengelige databasedataene etter kundens behov. Databasetabellen må ha en tilknyttet side.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: admin-how-to-create-custom-company-configuration-packages
ms.openlocfilehash: 95b16dc77bcdb0051447a4f153dd720661c52cf9
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "917939"
---
# <a name="review-and-customize-existing-database-data"></a><span data-ttu-id="1d246-104">Se gjennom og tilpasse eksisterende databasedata</span><span class="sxs-lookup"><span data-stu-id="1d246-104">Review and Customize Existing Database Data</span></span>
<span data-ttu-id="1d246-105">Når du oppretter en konfigurasjonpakke for en løsning, kan du vise og tilpasse de tilgjengelige databasedataene etter kundens behov.</span><span class="sxs-lookup"><span data-stu-id="1d246-105">As you create a configuration package for a solution, you can view and customize the available database data to suit your customer needs.</span></span> <span data-ttu-id="1d246-106">Databasetabellen må ha en tilknyttet side.</span><span class="sxs-lookup"><span data-stu-id="1d246-106">The database table has to have an associated page.</span></span>  

### <a name="to-customize-data-in-the-database"></a><span data-ttu-id="1d246-107">Slik tilpasser du data i databasen:</span><span class="sxs-lookup"><span data-stu-id="1d246-107">To customize data in the database</span></span>  

1.  <span data-ttu-id="1d246-108">Finn tabellene i konfigurasjonsforslaget som inneholder dataene du vil vise eller tilpasse.</span><span class="sxs-lookup"><span data-stu-id="1d246-108">In the configuration worksheet, identify the tables whose data that you want to view or customize.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="1d246-109">Kontroller at hver tabell er tilordnet en side-ID.</span><span class="sxs-lookup"><span data-stu-id="1d246-109">Make sure that each table has a page ID assigned to it.</span></span> <span data-ttu-id="1d246-110">For standard [!INCLUDE[d365fin](includes/d365fin_md.md)]\-tabeller, fylles denne verdien ut automatisk.</span><span class="sxs-lookup"><span data-stu-id="1d246-110">For standard [!INCLUDE[d365fin](includes/d365fin_md.md)] tables, this value is automatically filled in.</span></span> <span data-ttu-id="1d246-111">For egendefinerte tabeller må du oppgi ID\-en.</span><span class="sxs-lookup"><span data-stu-id="1d246-111">For custom tables, you have to provide the ID.</span></span>  

2.  <span data-ttu-id="1d246-112">I fanebladet **Handlinger** under **Vis** velger du **Databasedata**.</span><span class="sxs-lookup"><span data-stu-id="1d246-112">On the **Actions** tab, in the **Show** group, choose **Database Data**.</span></span>  

     <span data-ttu-id="1d246-113">Siden [!INCLUDE[d365fin](includes/d365fin_md.md)] for siden åpnes.</span><span class="sxs-lookup"><span data-stu-id="1d246-113">The [!INCLUDE[d365fin](includes/d365fin_md.md)] page for the page opens.</span></span>  

3.  <span data-ttu-id="1d246-114">Se gjennom informasjonen som er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="1d246-114">Review the available information.</span></span> <span data-ttu-id="1d246-115">Endre den etter behov ved å slette poster som ikke er relevante eller ved å legge til nye.</span><span class="sxs-lookup"><span data-stu-id="1d246-115">Modify it as necessary by deleting records that are not relevant or by adding new ones.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1d246-116">Se også</span><span class="sxs-lookup"><span data-stu-id="1d246-116">See Also</span></span>  
 [<span data-ttu-id="1d246-117">Behandle selskapskonfigurasjon i et forslag</span><span class="sxs-lookup"><span data-stu-id="1d246-117">Manage Company Configuration in a Worksheet</span></span>](admin-how-to-manage-company-configuration-in-a-worksheet.md)
