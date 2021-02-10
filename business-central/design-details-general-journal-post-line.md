---
title: Designdetaljer – Finanskladd – bokfør linje | Microsoft-dokumentasjon
description: Dette emnet gir innblikk i begrepene og prinsippene som brukes til å utforme funksjonen for bokføring av finanskladdelinjer på nytt i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general journal, posting, codeunit 12
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 56cf606151f687cf48138b3e14758d7febc47db6
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751582"
---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="65068-103">Designdetaljer: Finanskladd – bokfør linje</span><span class="sxs-lookup"><span data-stu-id="65068-103">Design Details: General Journal Post Line</span></span>
<span data-ttu-id="65068-104">Denne dokumentasjonen gir et detaljert teknisk innblikk i begrepene og prinsippene som brukes til å utforme funksjonen for bokføring av finanskladdelinjer på nytt i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="65068-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the general journal posting line feature in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="65068-105">Den nye utformingen forenkler kodeenhet 12 og gjør den enklere å vedlikeholde.</span><span class="sxs-lookup"><span data-stu-id="65068-105">The redesign makes codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="65068-106">Dokumentasjonen begynner med beskrivelse av begrepsmessige oversikter over den nye utformingen.</span><span class="sxs-lookup"><span data-stu-id="65068-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="65068-107">Deretter blir den tekniske arkitekturen forklart for å vise endringene den nye utformingen gir.</span><span class="sxs-lookup"><span data-stu-id="65068-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="65068-108">I denne delen</span><span class="sxs-lookup"><span data-stu-id="65068-108">In This Section</span></span>  
[<span data-ttu-id="65068-109">Oversikt over Finanskladd – bokfør linje</span><span class="sxs-lookup"><span data-stu-id="65068-109">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="65068-110">Designdetaljer: Strukturen til bokføringsgrensesnittet</span><span class="sxs-lookup"><span data-stu-id="65068-110">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="65068-111">Designdetaljer: Strukturen til bokføringsmotoren</span><span class="sxs-lookup"><span data-stu-id="65068-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="65068-112">Endringer i kodeenhet 12: Tilordne globale variabler for Finanskladd – bokfør linje</span><span class="sxs-lookup"><span data-stu-id="65068-112">Codeunit 12 Changes: Mapping Global Variables for General Journal Post Line</span></span>](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)  
[<span data-ttu-id="65068-113">Endringer i kodeenhet 12: Endringer i bokføringsprosedyrene for finans</span><span class="sxs-lookup"><span data-stu-id="65068-113">Codeunit 12 Changes: Changes in General Journal Post Procedures</span></span>](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)  

## <a name="see-also"></a><span data-ttu-id="65068-114">Se også</span><span class="sxs-lookup"><span data-stu-id="65068-114">See Also</span></span>  
[<span data-ttu-id="65068-115">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="65068-115">Working with General Journals</span></span>](ui-work-general-journals.md)
