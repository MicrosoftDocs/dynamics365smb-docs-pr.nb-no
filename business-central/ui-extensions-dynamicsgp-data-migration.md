---
title: "Overføre data fra Dynamics GP med utvidelsen for datamigrering | Microsoft-dokumentasjon"
description: "Bruk utvidelsen Dynamics GP-datamigrering til å overføre kunder, leverandører, lagervarer og konti fra Dynamics GP til Business Central."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 3761bdb0d6b9a51ed309ac4189ff263de76f4679
ms.contentlocale: nb-no
ms.lasthandoff: 05/17/2018

---
# <a name="the-dynamics-gp-data-migration-extension-for-business-central"></a><span data-ttu-id="d1eef-103">Dynamics GP-utvidelse for dataoverføring for Business Central</span><span class="sxs-lookup"><span data-stu-id="d1eef-103">The Dynamics GP Data Migration Extension for Business Central</span></span> 
<span data-ttu-id="d1eef-104">Denne utvidelsen gjør det enkelt å overføre kunder, leverandører og lagervarer og konti fra Dynamics GP til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d1eef-104">This extension makes it easy to migrate customers, vendors, inventory items, and accounts from Dynamics GP to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="d1eef-105">Hvis virksomheten din bruker Dynamics GP i dag, kan du eksportere relevant hovedposter og deretter åpne en assistert oppsettsveiledning for å legge til data i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d1eef-105">If your business uses Dynamics GP today, you can export the relevant master records and then open an assisted setup guide to add the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="d1eef-106">Hvis du vil ha mer informasjon, kan du se [Imporere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md).</span><span class="sxs-lookup"><span data-stu-id="d1eef-106">For more information, see [Importing Business Data from Other Finance Systems](across-import-data-configuration-packages.md).</span></span>

## <a name="exporting-data-from-dynamics-gp"></a><span data-ttu-id="d1eef-107">Eksportere data fra Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="d1eef-107">Exporting Data from Dynamics GP</span></span>
<span data-ttu-id="d1eef-108">Du må ha eksportert noen av eller alle dine eksisterende kunder, leverandører, varer og kontoer til en fil ved hjelp av funksjonen for dataeksport i Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="d1eef-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to a file, using the Dynamics GP functionality for data export.</span></span> <span data-ttu-id="d1eef-109">I forbindelse med [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du eksportere følgende datatyper:</span><span class="sxs-lookup"><span data-stu-id="d1eef-109">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following types of data:</span></span>

* <span data-ttu-id="d1eef-110">Konto</span><span class="sxs-lookup"><span data-stu-id="d1eef-110">Account</span></span>  
* <span data-ttu-id="d1eef-111">Kunde</span><span class="sxs-lookup"><span data-stu-id="d1eef-111">Customer</span></span>  
* <span data-ttu-id="d1eef-112">Element</span><span class="sxs-lookup"><span data-stu-id="d1eef-112">Item</span></span>  
* <span data-ttu-id="d1eef-113">Leverandør</span><span class="sxs-lookup"><span data-stu-id="d1eef-113">Vendor</span></span>  

<span data-ttu-id="d1eef-114">Utvidelsen Dynamics GP-datamigrering automatisk tilordner de eksporterte dataene, slik at dataene er raskt tilgjengelige for deg i det nye selskapet i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d1eef-114">The Dynamics GP Data Migration extension automatically maps the exported data so that your data is quickly available to you in your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="d1eef-115">Under prosessen opprettes understøttende informasjon om oppsettet, for eksempel bokføringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="d1eef-115">During the process, supporting setup information is created, such as posting groups.</span></span> <span data-ttu-id="d1eef-116">Lagervarer skal hentes inn i systemet med FIFO som kostvaluderingsmetode.</span><span class="sxs-lookup"><span data-stu-id="d1eef-116">Inventory items will be brought into the system with FIFO as the cost valuation method.</span></span> <span data-ttu-id="d1eef-117">Kontoene defineres som hovedkontosegmentet fra Dynamics GP med dimensjoner, fordi [!INCLUDE[d365fin](includes/d365fin_long_md.md)] ikke har kontosegmenter.</span><span class="sxs-lookup"><span data-stu-id="d1eef-117">Accounts will be set up as the main account segment from Dynamics GP with dimensions, because [!INCLUDE[d365fin](includes/d365fin_long_md.md)] does not have account segments.</span></span>

## <a name="see-also"></a><span data-ttu-id="d1eef-118">Se også</span><span class="sxs-lookup"><span data-stu-id="d1eef-118">See Also</span></span>
[<span data-ttu-id="d1eef-119">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="d1eef-119">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="d1eef-120">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="d1eef-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

