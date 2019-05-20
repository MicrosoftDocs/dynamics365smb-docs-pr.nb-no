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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 337f1e679ba2f0b1fcfc0ceb8b3f0ea45ca86ecc
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242996"
---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="69164-103">Designdetaljer: Finanskladd – bokfør linje</span><span class="sxs-lookup"><span data-stu-id="69164-103">Design Details: General Journal Post Line</span></span>
<span data-ttu-id="69164-104">Denne dokumentasjonen gir et detaljert teknisk innblikk i begrepene og prinsippene som brukes til å utforme funksjonen for bokføring av finanskladdelinjer på nytt i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="69164-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the general journal posting line feature in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="69164-105">Den nye utformingen forenkler kodeenhet 12 og gjør den enklere å vedlikeholde.</span><span class="sxs-lookup"><span data-stu-id="69164-105">The redesign makes codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="69164-106">Dokumentasjonen begynner med beskrivelse av begrepsmessige oversikter over den nye utformingen.</span><span class="sxs-lookup"><span data-stu-id="69164-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="69164-107">Deretter blir den tekniske arkitekturen forklart for å vise endringene den nye utformingen gir.</span><span class="sxs-lookup"><span data-stu-id="69164-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="69164-108">I denne delen</span><span class="sxs-lookup"><span data-stu-id="69164-108">In This Section</span></span>  
[<span data-ttu-id="69164-109">Oversikt over Finanskladd – bokfør linje</span><span class="sxs-lookup"><span data-stu-id="69164-109">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="69164-110">Designdetaljer: Strukturen til bokføringsgrensesnittet</span><span class="sxs-lookup"><span data-stu-id="69164-110">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="69164-111">Designdetaljer: Strukturen til bokføringsmotoren</span><span class="sxs-lookup"><span data-stu-id="69164-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="69164-112">Endringer i kodeenhet 12: Tilordne globale variabler for Finanskladd – bokfør linje</span><span class="sxs-lookup"><span data-stu-id="69164-112">Codeunit 12 Changes: Mapping Global Variables for General Journal Post Line</span></span>](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)  
[<span data-ttu-id="69164-113">Endringer i kodeenhet 12: Endringer i bokføringsprosedyrene for finans</span><span class="sxs-lookup"><span data-stu-id="69164-113">Codeunit 12 Changes: Changes in General Journal Post Procedures</span></span>](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)  

## <a name="see-also"></a><span data-ttu-id="69164-114">Se også</span><span class="sxs-lookup"><span data-stu-id="69164-114">See Also</span></span>  
[<span data-ttu-id="69164-115">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="69164-115">Working with General Journals</span></span>](ui-work-general-journals.md)
