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
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 1a8654b53dec476b175101a4d9c08f15ab3d6d6f
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185375"
---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="7ca62-103">Designdetaljer: Finanskladd – bokfør linje</span><span class="sxs-lookup"><span data-stu-id="7ca62-103">Design Details: General Journal Post Line</span></span>
<span data-ttu-id="7ca62-104">Denne dokumentasjonen gir et detaljert teknisk innblikk i begrepene og prinsippene som brukes til å utforme funksjonen for bokføring av finanskladdelinjer på nytt i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7ca62-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the general journal posting line feature in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="7ca62-105">Den nye utformingen forenkler kodeenhet 12 og gjør den enklere å vedlikeholde.</span><span class="sxs-lookup"><span data-stu-id="7ca62-105">The redesign makes codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="7ca62-106">Dokumentasjonen begynner med beskrivelse av begrepsmessige oversikter over den nye utformingen.</span><span class="sxs-lookup"><span data-stu-id="7ca62-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="7ca62-107">Deretter blir den tekniske arkitekturen forklart for å vise endringene den nye utformingen gir.</span><span class="sxs-lookup"><span data-stu-id="7ca62-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="7ca62-108">I denne delen</span><span class="sxs-lookup"><span data-stu-id="7ca62-108">In This Section</span></span>  
[<span data-ttu-id="7ca62-109">Oversikt over Finanskladd – bokfør linje</span><span class="sxs-lookup"><span data-stu-id="7ca62-109">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="7ca62-110">Designdetaljer: Strukturen til bokføringsgrensesnittet</span><span class="sxs-lookup"><span data-stu-id="7ca62-110">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="7ca62-111">Designdetaljer: Strukturen til bokføringsmotoren</span><span class="sxs-lookup"><span data-stu-id="7ca62-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="7ca62-112">Endringer i kodeenhet 12: Tilordne globale variabler for Finanskladd – bokfør linje</span><span class="sxs-lookup"><span data-stu-id="7ca62-112">Codeunit 12 Changes: Mapping Global Variables for General Journal Post Line</span></span>](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)  
[<span data-ttu-id="7ca62-113">Endringer i kodeenhet 12: Endringer i bokføringsprosedyrene for finans</span><span class="sxs-lookup"><span data-stu-id="7ca62-113">Codeunit 12 Changes: Changes in General Journal Post Procedures</span></span>](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)  

## <a name="see-also"></a><span data-ttu-id="7ca62-114">Se også</span><span class="sxs-lookup"><span data-stu-id="7ca62-114">See Also</span></span>  
[<span data-ttu-id="7ca62-115">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="7ca62-115">Working with General Journals</span></span>](ui-work-general-journals.md)
