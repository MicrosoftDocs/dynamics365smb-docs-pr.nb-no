---
title: "Overføre data fra Dynamics GP med utvidelsen for datamigrering | Microsoft-dokumentasjon"
description: "Bruk utvidelsen Dynamics GP-datamigrering til å overføre kunder, leverandører, lagervarer og konti fra Dynamics GP til Finance and Operations, Business edition."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: bfd3ca3e28b6eb3efa2a16cc131b508db6bd1590
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="the-dynamics-gp-data-migration-extension-for-finance-and-operations-business-edition"></a><span data-ttu-id="de2e5-103">Dynamics C5-utvidelse for dataoverføring for Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="de2e5-103">The Dynamics GP Data Migration Extension for Finance and Operations, Business edition</span></span> 
<span data-ttu-id="de2e5-104">Denne utvidelsen gjør det enkelt å overføre kunder, leverandører og lagervarer og konti fra Dynamics GP til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="de2e5-104">This extension makes it easy to migrate customers, vendors, inventory items, and accounts from Dynamics GP to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="de2e5-105">Hvis virksomheten din bruker Dynamics GP i dag, kan du eksportere relevant hovedposter og deretter åpne en assistert oppsettsveiledning for å legge til data i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="de2e5-105">If your business uses Dynamics GP today, you can export the relevant master records and then open an assisted setup guide to add the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="de2e5-106">Hvis du vil ha mer informasjon, kan du se [Overfør forretningsdata fra andre økonomisystemer](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="de2e5-106">For more information, see [Migrate Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-dynamics-gp"></a><span data-ttu-id="de2e5-107">Eksportere data fra Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="de2e5-107">Exporting Data from Dynamics GP</span></span>
<span data-ttu-id="de2e5-108">Du må ha eksportert noen av eller alle dine eksisterende kunder, leverandører, varer og kontoer til en fil ved hjelp av funksjonen for dataeksport i Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="de2e5-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to a file, using the Dynamics GP functionality for data export.</span></span> <span data-ttu-id="de2e5-109">I forbindelse med [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du eksportere følgende datatyper:</span><span class="sxs-lookup"><span data-stu-id="de2e5-109">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following types of data:</span></span>

* <span data-ttu-id="de2e5-110">Konto</span><span class="sxs-lookup"><span data-stu-id="de2e5-110">Account</span></span>  
* <span data-ttu-id="de2e5-111">Kunde</span><span class="sxs-lookup"><span data-stu-id="de2e5-111">Customer</span></span>  
* <span data-ttu-id="de2e5-112">Element</span><span class="sxs-lookup"><span data-stu-id="de2e5-112">Item</span></span>  
* <span data-ttu-id="de2e5-113">Leverandør</span><span class="sxs-lookup"><span data-stu-id="de2e5-113">Vendor</span></span>  

<span data-ttu-id="de2e5-114">Utvidelsen Dynamics GP-datamigrering automatisk tilordner de eksporterte dataene, slik at dataene er raskt tilgjengelige for deg i det nye selskapet i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="de2e5-114">The Dynamics GP Data Migration extension automatically maps the exported data so that your data is quickly available to you in your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="de2e5-115">Under prosessen opprettes understøttende informasjon om oppsettet, for eksempel bokføringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="de2e5-115">During the process, supporting setup information is created, such as posting groups.</span></span> <span data-ttu-id="de2e5-116">Lagervarer skal hentes inn i systemet med FIFO som kostvaluderingsmetode.</span><span class="sxs-lookup"><span data-stu-id="de2e5-116">Inventory items will be brought into the system with FIFO as the cost valuation method.</span></span> <span data-ttu-id="de2e5-117">Kontoene defineres som hovedkontosegmentet fra Dynamics GP med dimensjoner, fordi [!INCLUDE[d365fin](includes/d365fin_long_md.md)] ikke har kontosegmenter.</span><span class="sxs-lookup"><span data-stu-id="de2e5-117">Accounts will be set up as the main account segment from Dynamics GP with dimensions, because [!INCLUDE[d365fin](includes/d365fin_long_md.md)] does not have account segments.</span></span>

## <a name="see-also"></a><span data-ttu-id="de2e5-118">Se også</span><span class="sxs-lookup"><span data-stu-id="de2e5-118">See Also</span></span>
[<span data-ttu-id="de2e5-119">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="de2e5-119">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="de2e5-120">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="de2e5-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

