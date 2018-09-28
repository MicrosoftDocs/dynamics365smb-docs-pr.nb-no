---
title: "Designdetaljer – Behov og forsyning | Microsoft-dokumentasjon"
description: Dette emnet introduserer konseptet med behov, som er det vanlige uttrykket som brukes for alle typer bruttobehov, for eksempel en salgsordre og komponentbehov fra en produksjonsordre.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8cf7ffe90ccaf32258b4a51fb12f93a8df8ba7eb
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-demand-and-supply"></a><span data-ttu-id="8ef64-103">Designdetaljer: Behov og forsyning</span><span class="sxs-lookup"><span data-stu-id="8ef64-103">Design Details: Demand and Supply</span></span>
<span data-ttu-id="8ef64-104">Behov er det vanlige uttrykket som brukes for alle typer bruttobehov, for eksempel en salgsordre og komponentbehov fra en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="8ef64-104">Demand is the common term used for any kind of gross demand, such as a sales order and component need from a production order.</span></span> <span data-ttu-id="8ef64-105">I tillegg tillater programmet mer tekniske typer behov, for eksempel negativ beholdning og bestillingsreturer.</span><span class="sxs-lookup"><span data-stu-id="8ef64-105">In addition, the program allows more technical types of demand, such as negative inventory and purchase returns.</span></span>  
  
<span data-ttu-id="8ef64-106">Forsyning er den vanlige betegnelsen som brukes om alle typer positive eller inngående antall, for eksempel beholdning, kjøp, montering, produksjon eller inngående overføringer.</span><span class="sxs-lookup"><span data-stu-id="8ef64-106">Supply is the common term used for any kind of positive or inbound quantity, such as inventory, purchases, assembly, production, or inbound transfers.</span></span> <span data-ttu-id="8ef64-107">I tillegg kan en ordreretur også representere forsyning.</span><span class="sxs-lookup"><span data-stu-id="8ef64-107">In addition, a sales return may also represent supply.</span></span>  
  
<span data-ttu-id="8ef64-108">For å sortere ut de mange kildene til behov og forsyning organiserer planleggingssystemet dem på to tidslinjer kalt beholdningsprofiler.</span><span class="sxs-lookup"><span data-stu-id="8ef64-108">To sort out the many sources of demand and supply, the planning system organizes them on two time lines called inventory profiles.</span></span> <span data-ttu-id="8ef64-109">Én profil inneholder behovshendelser, og den andre inneholder tilsvarende forsyningshendelser.</span><span class="sxs-lookup"><span data-stu-id="8ef64-109">One profile holds demand events, and the other holds the corresponding supply events.</span></span> <span data-ttu-id="8ef64-110">Hver hendelse representerer én ordrenettverksenhet, for eksempel en salgsordrelinje, en varepost eller en produksjonsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="8ef64-110">Each event represents one order network entity, such as a sales order line, an item ledger entry, or a production order line.</span></span>  
  
<span data-ttu-id="8ef64-111">Når du beholdningsprofiler lastes inn, balanseres de ulike settene med behov/forsyning for å gi en forsyningsplan som oppfyller de angitte målene.</span><span class="sxs-lookup"><span data-stu-id="8ef64-111">When inventory profiles are loaded, the different demand-supply sets are balanced to output a supply plan that fulfills the listed goals.</span></span>  
  
<span data-ttu-id="8ef64-112">Planleggingsparametre og lagernivåer er henholdsvis andre typer behov og forsyning som gjennomgå integrert balansering for å etterfylle lagervarer.</span><span class="sxs-lookup"><span data-stu-id="8ef64-112">Planning parameters and inventory levels are other types of demand and supply respectively, which undergo integrated balancing to replenish stock items.</span></span> <span data-ttu-id="8ef64-113">Hvis du vil ha mer informasjon, se [Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md).</span><span class="sxs-lookup"><span data-stu-id="8ef64-113">For more information, see [Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8ef64-114">Se også</span><span class="sxs-lookup"><span data-stu-id="8ef64-114">See Also</span></span>  
<span data-ttu-id="8ef64-115">[Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="8ef64-115">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="8ef64-116">[Designdetaljer: Sentrale begreper for planleggingssystemet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="8ef64-116">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="8ef64-117">Designdetaljer: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="8ef64-117">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
