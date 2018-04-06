---
title: "Designdetaljer – Forsyningsplanlegging | Microsoft-dokumentasjon"
description: Dette emnet gir en oversikt over begrepene og prinsippene som brukes i funksjonene for forsyningsplanlegging i Finance and Operations, Business edition.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, supply, planning, reordering, replenishment
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b8e664be23db7be871e1775a8b98b006218b7404
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-supply-planning"></a><span data-ttu-id="97b28-103">Designdetaljer: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="97b28-103">Design Details: Supply Planning</span></span>
<span data-ttu-id="97b28-104">Denne dokumentasjonen gir et detaljert teknisk innblikk i begrepene og prinsippene som brukes i funksjonene for forsyningsplanlegging i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="97b28-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Supply Planning features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="97b28-105">Den forklarer hvordan planleggingssystemet fungerer, og hvordan du justerer algoritmer for å oppfylle krav i forskjellige miljøer.</span><span class="sxs-lookup"><span data-stu-id="97b28-105">It explains how the planning system works and how to adjust the algorithms to meet planning requirements in different environments.</span></span> <span data-ttu-id="97b28-106">Den introduserer først sentrale løsningskonsepter, og beskriver deretter logikken i den sentrale mekanismen, forsyningsbalansering, før du fortsetter å forklare hvordan lagerplanlegging utføres ved hjelp av gjenbestillingsprinsipper.</span><span class="sxs-lookup"><span data-stu-id="97b28-106">It first introduces central solution concepts and then describes the logic of the central mechanism, supply balancing, before proceeding to explain how inventory planning is performed with the use of reordering policies.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="97b28-107">I denne delen</span><span class="sxs-lookup"><span data-stu-id="97b28-107">In This Section</span></span>  
[<span data-ttu-id="97b28-108">Designdetaljer: Sentrale begreper for planleggingssystemet</span><span class="sxs-lookup"><span data-stu-id="97b28-108">Design Details: Central Concepts of the Planning System</span></span>](design-details-central-concepts-of-the-planning-system.md)  
[<span data-ttu-id="97b28-109">Designdetaljer: Reservasjon, ordresporing og handlingsmeldinger</span><span class="sxs-lookup"><span data-stu-id="97b28-109">Design Details: Reservation, Order Tracking, and Action Messaging</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
[<span data-ttu-id="97b28-110">Designdetaljer: Balansere behov og forsyning</span><span class="sxs-lookup"><span data-stu-id="97b28-110">Design Details: Balancing Demand and Supply</span></span>](design-details-balancing-demand-and-supply.md)  
[<span data-ttu-id="97b28-111">Designdetaljer: Håndtere gjenbestillingsprinsipper</span><span class="sxs-lookup"><span data-stu-id="97b28-111">Design Details: Handling Reordering Policies</span></span>](design-details-handling-reordering-policies.md)  
[<span data-ttu-id="97b28-112">Designdetaljer: Planleggingsparametere</span><span class="sxs-lookup"><span data-stu-id="97b28-112">Design Details: Planning Parameters</span></span>](design-details-planning-parameters.md)  
[<span data-ttu-id="97b28-113">Designdetaljer: Tabell for planleggingstilordning</span><span class="sxs-lookup"><span data-stu-id="97b28-113">Design Details: Planning Assignment Table</span></span>](design-details-planning-assignment-table.md)  
[<span data-ttu-id="97b28-114">Designdetaljer: Behov på tom lokasjon</span><span class="sxs-lookup"><span data-stu-id="97b28-114">Design Details: Demand at Blank Location</span></span>](design-details-demand-at-blank-location.md)  
[<span data-ttu-id="97b28-115">Designdetaljer: Overføringer i planlegging</span><span class="sxs-lookup"><span data-stu-id="97b28-115">Design Details: Transfers in Planning</span></span>](design-details-transfers-in-planning.md)

