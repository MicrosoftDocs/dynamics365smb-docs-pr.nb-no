---
title: Designdetaljer – Finanskladd – bokfør linje | Microsoft-dokumentasjon
description: Dette emnet gir innblikk i begrepene og prinsippene som brukes til å utforme funksjonen for bokføring av finanskladdelinjer på nytt i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general journal, posting, codeunit 12
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 8492c83437be4cd850bafdaaa5dc70d00a075674
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215231"
---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="8d1ce-103">Designdetaljer: Finanskladd – bokfør linje</span><span class="sxs-lookup"><span data-stu-id="8d1ce-103">Design Details: General Journal Post Line</span></span>

<span data-ttu-id="8d1ce-104">Denne dokumentasjonen gir et detaljert teknisk innblikk i begrepene og prinsippene som ble brukt til å utforme funksjonen for bokføring av finanskladdelinjer på nytt i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="8d1ce-104">This documentation provides detailed technical insight into the concepts and principles that were used to redesign the general journal posting line feature in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="8d1ce-105">Den nye utformingen forenklet codeunit 12 og gjør den enklere å vedlikeholde.</span><span class="sxs-lookup"><span data-stu-id="8d1ce-105">The redesign made codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="8d1ce-106">Dokumentasjonen begynner med beskrivelse av begrepsmessige oversikter over den nye utformingen.</span><span class="sxs-lookup"><span data-stu-id="8d1ce-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="8d1ce-107">Deretter blir den tekniske arkitekturen forklart for å vise endringene den nye utformingen gir.</span><span class="sxs-lookup"><span data-stu-id="8d1ce-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="8d1ce-108">Informasjonen i dette avsnittet gjelder for ny design i en tidligere versjon av produktet, Microsoft Dynamics NAV 2013 R2.</span><span class="sxs-lookup"><span data-stu-id="8d1ce-108">The information in this section applies to the redesign in an earlier version of the product, Microsoft Dynamics NAV 2013 R2.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8d1ce-109">I denne delen</span><span class="sxs-lookup"><span data-stu-id="8d1ce-109">In This Section</span></span>

[<span data-ttu-id="8d1ce-110">Oversikt over Finanskladd – bokfør linje</span><span class="sxs-lookup"><span data-stu-id="8d1ce-110">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="8d1ce-111">Designdetaljer: Strukturen til bokføringsgrensesnittet</span><span class="sxs-lookup"><span data-stu-id="8d1ce-111">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="8d1ce-112">Designdetaljer: Strukturen til bokføringsmotoren</span><span class="sxs-lookup"><span data-stu-id="8d1ce-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  

## <a name="see-also"></a><span data-ttu-id="8d1ce-113">Se også</span><span class="sxs-lookup"><span data-stu-id="8d1ce-113">See Also</span></span>

<span data-ttu-id="8d1ce-114">[Arbeid med finanskladder](ui-work-general-journals.md)
[Utformingsdetaljer: Finanskladd – bokfør linje (Dynamics NAV)](/dynamics-nav-app/design-details-general-journal-post-line)</span><span class="sxs-lookup"><span data-stu-id="8d1ce-114">[Working with General Journals](ui-work-general-journals.md)
[Design Details: General Journal Post Line (Dynamics NAV)](/dynamics-nav-app/design-details-general-journal-post-line)</span></span>  

[!INCLUDE[footer-include](includes/footer-banner.md)]