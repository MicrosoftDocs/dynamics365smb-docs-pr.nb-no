---
title: "Vanlige spørsmål om Fortell meg | Microsoft-dokumentasjon"
description: "Denne artikkelen gir svar på spørsmål som våre kunder og partnere ofte stiller om Fortell meg."
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 70ab7fb07cda5ce9d86b3f39dd14321829e85a52
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="tell-me-faq"></a><span data-ttu-id="0fe19-103">Vanlige spørsmål om Fortell meg</span><span class="sxs-lookup"><span data-stu-id="0fe19-103">Tell Me FAQ</span></span>
<span data-ttu-id="0fe19-104">Dette emnet gir svar på spørsmål som våre avanserte brukere ofte spør om den nye Fortell meg-funksjonen, som har erstattet den tidligere sidesøkefunksjonen, kalt for **Søk etter side eller rapport**.</span><span class="sxs-lookup"><span data-stu-id="0fe19-104">This topic answers questions that our advanced users often ask about the new Tell Me feature, which has replaced the previous Page Search feature known as **Find Pages and Reports**.</span></span>

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a><span data-ttu-id="0fe19-105">Kan alle handlinger fra den gjeldende siden oppdages i Fortell meg?</span><span class="sxs-lookup"><span data-stu-id="0fe19-105">Are all actions from my current page discoverable in Tell Me?</span></span>
<span data-ttu-id="0fe19-106">Nei.</span><span class="sxs-lookup"><span data-stu-id="0fe19-106">No.</span></span> <span data-ttu-id="0fe19-107">Handlinger i deler, for eksempel salgslinjer eller faktabokser, vises ikke i Fortell meg.</span><span class="sxs-lookup"><span data-stu-id="0fe19-107">Actions in parts, such as the Sales Lines part or FactBoxes, are not displayed in Tell Me.</span></span>

### <a name="are-the-results-in-tell-me-filtered-by-permissions"></a><span data-ttu-id="0fe19-108">Er resultatene i Fortell meg filtrert etter tillatelser?</span><span class="sxs-lookup"><span data-stu-id="0fe19-108">Are the results in Tell Me filtered by permissions?</span></span>
<span data-ttu-id="0fe19-109">Hvis brukeren ikke har AccessByPermissions, vises ikke handlinger.</span><span class="sxs-lookup"><span data-stu-id="0fe19-109">If the user does not have AccessByPermissions then actions are not displayed.</span></span> <span data-ttu-id="0fe19-110">Sider og rapporter vises i resultatet, men krever at brukeren har tillatelse til å få tilgang til dem.</span><span class="sxs-lookup"><span data-stu-id="0fe19-110">However, pages and reports appear in the results but require that the user has permission to access them.</span></span> <span data-ttu-id="0fe19-111">En melding vises hvis brukeren ikke har tillatelse til å vise objektet.</span><span class="sxs-lookup"><span data-stu-id="0fe19-111">A message will display if the user does not have permission to view the object.</span></span>

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a><span data-ttu-id="0fe19-112">Viser Fortell meg innhold fra tilpasninger eller installerte tredjeparts utvidelser?</span><span class="sxs-lookup"><span data-stu-id="0fe19-112">Does Tell Me display content from my customizations or installed third-party extensions?</span></span>
<span data-ttu-id="0fe19-113">Handlinger, sider og rapporter som kommer fra utvidelser, hentes av Fortell meg, men ikke egendefinert hjelp.</span><span class="sxs-lookup"><span data-stu-id="0fe19-113">Actions, pages, and reports that originate from extensions are picked up by Tell Me, but custom help documentation is not.</span></span> <span data-ttu-id="0fe19-114">For teknisk informasjon om hvordan du gjør det mulig å oppdage egendefinerte sider og rapporter, kan du se [Legge til sider og rapporter i Søk](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).</span><span class="sxs-lookup"><span data-stu-id="0fe19-114">For technical information about how to make custom pages and reports discoverable, see [Adding Pages and Reports to Search](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).</span></span>

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a><span data-ttu-id="0fe19-115">Hva gjør dette forskjellig fra det som tidligere ble kalt for Sidesøk?</span><span class="sxs-lookup"><span data-stu-id="0fe19-115">What makes this different from what was previously known as Page Search?</span></span>
<span data-ttu-id="0fe19-116">Sidesøk har utviklet seg til Fortell meg for å hjelpe deg med å arbeide raskt.</span><span class="sxs-lookup"><span data-stu-id="0fe19-116">Page Search has evolved into Tell Me to help you get work done quickly.</span></span> <span data-ttu-id="0fe19-117">Sidesøk kunne bare hjelpe deg med å navigere til sider eller rapporter.</span><span class="sxs-lookup"><span data-stu-id="0fe19-117">Page Search could only help you navigate to pages or reports.</span></span> <span data-ttu-id="0fe19-118">På et teknisk nivå er Fortell meg ikke lenger basert på det eldre MenuSuite-konseptet.</span><span class="sxs-lookup"><span data-stu-id="0fe19-118">At a technical level, Tell Me is no longer based on the legacy MenuSuite concept.</span></span>

### <a name="i-use-on-premises-included365finincludesd365finmdmd-does-that-include-tell-me"></a><span data-ttu-id="0fe19-119">Jeg bruker lokal [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="0fe19-119">I use on-premises [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="0fe19-120">Inkluderer dette Fortell meg?</span><span class="sxs-lookup"><span data-stu-id="0fe19-120">Does that include Tell Me?</span></span>
<span data-ttu-id="0fe19-121">Du kan bruke Fortell meg i den lokale webklienten til å finne handlinger, sider og rapporter, men ikke dokumentasjon.</span><span class="sxs-lookup"><span data-stu-id="0fe19-121">You can use Tell Me in the on-premises Web Client to find actions, pages, and reports, but not documentation.</span></span> <span data-ttu-id="0fe19-122">Brukere som kobler til [!INCLUDE[d365fin](includes/d365fin_md.md)] fra Dynamics NAV-klienten fortsetter å bruke Sidesøk.</span><span class="sxs-lookup"><span data-stu-id="0fe19-122">Users connecting to [!INCLUDE[d365fin](includes/d365fin_md.md)] from the Dynamics NAV client continue to use Page Search.</span></span>

### <a name="is-tell-me-available-for-all-form-factors"></a><span data-ttu-id="0fe19-123">Er Fortell meg tilgjengelig for alle skjemafaktorer?</span><span class="sxs-lookup"><span data-stu-id="0fe19-123">Is Tell Me available for all form factors?</span></span>
<span data-ttu-id="0fe19-124">Fortell meg er bare tilgjengelig i webklienten eller Windows-apper for stasjonær datamaskin.</span><span class="sxs-lookup"><span data-stu-id="0fe19-124">Tell Me is only available in the Web Client or Windows desktop app.</span></span>

### <a name="are-the-documentation-results-available-in-any-language"></a><span data-ttu-id="0fe19-125">Er dokumentasjonsresultatene tilgjengelige på alle språk?</span><span class="sxs-lookup"><span data-stu-id="0fe19-125">Are the documentation results available in any language?</span></span>
<span data-ttu-id="0fe19-126">Hjelpeartiklene vises på språket du har angitt i **Mine innstillinger** hvis hjelp er tilgjengelig på dette språket.</span><span class="sxs-lookup"><span data-stu-id="0fe19-126">The help articles display in the language you have specified in **My Settings**, if help is available in that language.</span></span>

## <a name="see-also"></a><span data-ttu-id="0fe19-127">Se også</span><span class="sxs-lookup"><span data-stu-id="0fe19-127">See Also</span></span>  
[<span data-ttu-id="0fe19-128">Finne funksjoner og informasjon</span><span class="sxs-lookup"><span data-stu-id="0fe19-128">Finding Features and Information</span></span>](ui-search.md)

