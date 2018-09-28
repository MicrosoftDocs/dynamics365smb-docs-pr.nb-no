---
title: "Designdetaljer – Dimensjonssettposter | Microsoft-dokumentasjon"
description: "Denne dokumentasjonen gir et detaljert teknisk innblikk i begrepene og prinsippene som brukes til å utforme funksjonen for lagring og bokføring av dimensjonsposter på nytt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, dimensions, codeunit
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 5563241784aaf8bfa1a29f8568411be657647cf7
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-dimension-set-entries"></a><span data-ttu-id="e2456-103">Designdetaljer: Dimensjonssettposter</span><span class="sxs-lookup"><span data-stu-id="e2456-103">Design Details: Dimension Set Entries</span></span>
<span data-ttu-id="e2456-104">Denne dokumentasjonen gir et detaljert teknisk innblikk i begrepene og prinsippene som brukes til å utforme funksjonen for lagring og bokføring av dimensjonsposter på nytt i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e2456-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the dimension entry storing and posting feature in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="e2456-105">Dokumentasjonen begynner med beskrivelse av begrepsmessige oversikter over den nye utformingen.</span><span class="sxs-lookup"><span data-stu-id="e2456-105">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="e2456-106">Deretter blir den tekniske arkitekturen forklart for å vise hvordan den nye utformingen er utført.</span><span class="sxs-lookup"><span data-stu-id="e2456-106">Then it explains the technical architecture to show how the redesign is made.</span></span> <span data-ttu-id="e2456-107">Til slutt inneholder det kodeeksempler for å gjøre deg klar for overføring og oppgradering av dimensjonskode.</span><span class="sxs-lookup"><span data-stu-id="e2456-107">Finally, it provides code examples to prepare you for dimension code migration and upgrade.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="e2456-108">I denne delen</span><span class="sxs-lookup"><span data-stu-id="e2456-108">In This Section</span></span>  
[<span data-ttu-id="e2456-109">Dimensjonssettposter – oversikt</span><span class="sxs-lookup"><span data-stu-id="e2456-109">Dimension Set Entries Overview</span></span>](design-details-dimension-set-entries-overview.md)  
[<span data-ttu-id="e2456-110">Designdetaljer: Søke etter dimensjonskombinasjoner</span><span class="sxs-lookup"><span data-stu-id="e2456-110">Design Details: Searching for Dimension Combinations</span></span>](design-details-searching-for-dimension-combinations.md)  
[<span data-ttu-id="e2456-111">Designdetaljer: Tabellstruktur</span><span class="sxs-lookup"><span data-stu-id="e2456-111">Design Details: Table Structure</span></span>](design-details-table-structure.md)  
[<span data-ttu-id="e2456-112">Designdetaljer: Dimensjonsbehandling for kodeenhet 408</span><span class="sxs-lookup"><span data-stu-id="e2456-112">Design Details: Codeunit 408 Dimension Management</span></span>](design-details-codeunit-408-dimension-management.md)  
[<span data-ttu-id="e2456-113">Designdetaljer: Kodeeksempler på endrede mønstre i endringer</span><span class="sxs-lookup"><span data-stu-id="e2456-113">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)

