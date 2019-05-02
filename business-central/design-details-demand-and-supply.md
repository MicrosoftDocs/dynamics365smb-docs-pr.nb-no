---
title: Designdetaljer – Behov og forsyning | Microsoft-dokumentasjon
description: Behov er det vanlige uttrykket som brukes for alle typer bruttobehov, for eksempel en salgsordre og komponentbehov fra en produksjonsordre. I tillegg tillater programmet mer tekniske typer behov, for eksempel negativ beholdning og bestillingsreturer.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: ad6684bb1fefe10fc965c3c8a7780c6aa8a9d685
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803477"
---
# <a name="design-details-demand-and-supply"></a><span data-ttu-id="76fec-104">Designdetaljer: Behov og forsyning</span><span class="sxs-lookup"><span data-stu-id="76fec-104">Design Details: Demand and Supply</span></span>
<span data-ttu-id="76fec-105">Behov er det vanlige uttrykket som brukes for alle typer bruttobehov, for eksempel en salgsordre og komponentbehov fra en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="76fec-105">Demand is the common term used for any kind of gross demand, such as a sales order and component need from a production order.</span></span> <span data-ttu-id="76fec-106">I tillegg tillater programmet mer tekniske typer behov, for eksempel negativ beholdning og bestillingsreturer.</span><span class="sxs-lookup"><span data-stu-id="76fec-106">In addition, the program allows more technical types of demand, such as negative inventory and purchase returns.</span></span>  

 <span data-ttu-id="76fec-107">Forsyning er den vanlige betegnelsen som brukes om alle typer positive eller inngående antall, for eksempel beholdning, kjøp, montering, produksjon eller inngående overføringer.</span><span class="sxs-lookup"><span data-stu-id="76fec-107">Supply is the common term used for any kind of positive or inbound quantity, such as inventory, purchases, assembly, production, or inbound transfers.</span></span> <span data-ttu-id="76fec-108">I tillegg kan en ordreretur også representere forsyning.</span><span class="sxs-lookup"><span data-stu-id="76fec-108">In addition, a sales return may also represent supply.</span></span>  

 <span data-ttu-id="76fec-109">For å sortere ut de mange kildene til behov og forsyning organiserer planleggingssystemet dem på to tidslinjer kalt beholdningsprofiler.</span><span class="sxs-lookup"><span data-stu-id="76fec-109">To sort out the many sources of demand and supply, the planning system organizes them on two time lines called inventory profiles.</span></span> <span data-ttu-id="76fec-110">Én profil inneholder behovshendelser, og den andre inneholder tilsvarende forsyningshendelser.</span><span class="sxs-lookup"><span data-stu-id="76fec-110">One profile holds demand events, and the other holds the corresponding supply events.</span></span> <span data-ttu-id="76fec-111">Hver hendelse representerer én ordrenettverksenhet, for eksempel en salgsordrelinje, en varepost eller en produksjonsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="76fec-111">Each event represents one order network entity, such as a sales order line, an item ledger entry, or a production order line.</span></span>  

 <span data-ttu-id="76fec-112">Når du beholdningsprofiler lastes inn, balanseres de ulike settene med behov/forsyning for å gi en forsyningsplan som oppfyller de angitte målene.</span><span class="sxs-lookup"><span data-stu-id="76fec-112">When inventory profiles are loaded, the different demand-supply sets are balanced to output a supply plan that fulfills the listed goals.</span></span>  

 <span data-ttu-id="76fec-113">Planleggingsparametre og lagernivåer er henholdsvis andre typer behov og forsyning som gjennomgå integrert balansering for å etterfylle lagervarer.</span><span class="sxs-lookup"><span data-stu-id="76fec-113">Planning parameters and inventory levels are other types of demand and supply respectively, which undergo integrated balancing to replenish stock items.</span></span> <span data-ttu-id="76fec-114">Hvis du vil ha mer informasjon, se [Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md).</span><span class="sxs-lookup"><span data-stu-id="76fec-114">For more information, see [Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="76fec-115">Se også</span><span class="sxs-lookup"><span data-stu-id="76fec-115">See Also</span></span>  
 <span data-ttu-id="76fec-116">[Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="76fec-116">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
 <span data-ttu-id="76fec-117">[Designdetaljer: Sentrale begreper for planleggingssystemet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="76fec-117">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
 [<span data-ttu-id="76fec-118">Designdetaljer: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="76fec-118">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)