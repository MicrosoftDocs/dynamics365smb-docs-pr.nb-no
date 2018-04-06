---
title: "Designdetaljer – Finanskladd – bokfør linje | Microsoft-dokumentasjon"
description: "Dette emnet gir et innblikk i begrepene og prinsippene som brukes til å utforme funksjonen for bokføring av finanskladdelinjer på nytt i Finance and Operations, Business edition."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general journal, posting, codeunit 12
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2d26d477b6223d6e53745a8dfd65844a1c3f5e5a
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="79bbd-103">Designdetaljer: Finanskladd – bokfør linje</span><span class="sxs-lookup"><span data-stu-id="79bbd-103">Design Details: General Journal Post Line</span></span>
<span data-ttu-id="79bbd-104">Denne dokumentasjonen gir et detaljert teknisk innblikk i begrepene og prinsippene som brukes til å utforme funksjonen for bokføring av finanskladdelinjer på nytt i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="79bbd-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the general journal posting line feature in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="79bbd-105">Den nye utformingen forenkler kodeenhet 12 og gjør den enklere å vedlikeholde.</span><span class="sxs-lookup"><span data-stu-id="79bbd-105">The redesign makes codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="79bbd-106">Dokumentasjonen begynner med beskrivelse av begrepsmessige oversikter over den nye utformingen.</span><span class="sxs-lookup"><span data-stu-id="79bbd-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="79bbd-107">Deretter blir den tekniske arkitekturen forklart for å vise endringene den nye utformingen gir.</span><span class="sxs-lookup"><span data-stu-id="79bbd-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="79bbd-108">I denne delen</span><span class="sxs-lookup"><span data-stu-id="79bbd-108">In This Section</span></span>  
[<span data-ttu-id="79bbd-109">Oversikt over Finanskladd – bokfør linje</span><span class="sxs-lookup"><span data-stu-id="79bbd-109">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="79bbd-110">Designdetaljer: Strukturen til bokføringsgrensesnittet</span><span class="sxs-lookup"><span data-stu-id="79bbd-110">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="79bbd-111">Designdetaljer: Strukturen til bokføringsmotoren</span><span class="sxs-lookup"><span data-stu-id="79bbd-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="79bbd-112">Endringer i kodeenhet 12: Tilordne globale variabler for Finanskladd – bokfør linje</span><span class="sxs-lookup"><span data-stu-id="79bbd-112">Codeunit 12 Changes: Mapping Global Variables for General Journal Post Line</span></span>](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)  
[<span data-ttu-id="79bbd-113">Endringer i kodeenhet 12: Endringer i bokføringsprosedyrene for finans</span><span class="sxs-lookup"><span data-stu-id="79bbd-113">Codeunit 12 Changes: Changes in General Journal Post Procedures</span></span>](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)  

## <a name="see-also"></a><span data-ttu-id="79bbd-114">Se også</span><span class="sxs-lookup"><span data-stu-id="79bbd-114">See Also</span></span>  
[<span data-ttu-id="79bbd-115">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="79bbd-115">Working with General Journals</span></span>](ui-work-general-journals.md)

