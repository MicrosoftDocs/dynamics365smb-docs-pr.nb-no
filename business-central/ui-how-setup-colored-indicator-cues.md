---
title: Tillpasse visuelle signaler om aktiviteten for et bunke-ikon | Microsoft-dokumentasjon
description: "Definere en farget indikator på en bunkeflis for å gi et tilpasset visuelt signal for aktiviteten for bunke-ikonet."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, customize
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e4ceaeae1a37a521d2d5bd22ab711757283e6321
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-a-colored-indicator-on-cues"></a><span data-ttu-id="5f92b-103">Definere en farget indikator for bunke-ikoner</span><span class="sxs-lookup"><span data-stu-id="5f92b-103">Set Up a Colored Indicator on Cues</span></span>
<span data-ttu-id="5f92b-104">Du kan definere bunke-ikoner som vises i rollesenteret, for å inkludere en indikator som endrer farge basert på dataverdiene i bunke-ikonene.</span><span class="sxs-lookup"><span data-stu-id="5f92b-104">You can set up Cues that appear on the Role Center to include an indicator that changes color based on the data values in the Cues.</span></span>

<span data-ttu-id="5f92b-105">Indikatoren vises som en farget linje langs øverste kant av bunkeflisen.</span><span class="sxs-lookup"><span data-stu-id="5f92b-105">The indicator appears as a colored bar along the top border of the Cue tile.</span></span> <span data-ttu-id="5f92b-106">Den gir et visuelt signal om statusen for aktiviteten for bunke-ikonet, som kan angi fordelaktige eller ufordelaktige tilstander som ber brukeren om å gjøre noe.</span><span class="sxs-lookup"><span data-stu-id="5f92b-106">It provides a visual signal of the status of the Cue's activity, which can indicate favorable or unfavorable conditions to prompt the user to take action.</span></span> <span data-ttu-id="5f92b-107">Hvis det for eksempel vises pågående salgsfakturaer på et bunke-ikon, kan du angi at indikatoren skal være grønn (fordelaktig) når antall pågående salgsfakturaer er under 10, og at den skal være rød (ufordelaktig) når det totale antallet er over 20.</span><span class="sxs-lookup"><span data-stu-id="5f92b-107">For example, if a Cue displays ongoing sales invoices, you can set up the indicator to appear green (favorable) when total number of ongoing sales invoices is below 10, and appears red (unfavorable) when the total is greater than 20.</span></span>

<span data-ttu-id="5f92b-108">Du bruker vinduet **Oppsett for bunke-ikon** til å definere indikatorer for alle bunke-ikonene som er tilgjengelige i selskapsdatabasen.</span><span class="sxs-lookup"><span data-stu-id="5f92b-108">From the **Cue Setup** window, you set up indicators for all the Cues that are available in the company database.</span></span>

<span data-ttu-id="5f92b-109">Hvis du vil definere indikatoren, kan du angi opptil to terskelverdier som definerer tre områder med dataverdier (lav, middels og høy) som du kan bruke en annen farge (eller stil) med.</span><span class="sxs-lookup"><span data-stu-id="5f92b-109">To set up the indicator, you specify up to two threshold values that define three ranges of data values (low, middle, and high) to which you can apply a different color (or style).</span></span>

## <a name="to-set-up-colored-indicators-on-cues"></a><span data-ttu-id="5f92b-110">Slik definerer du fargede indikatorer for bunke-ikoner</span><span class="sxs-lookup"><span data-stu-id="5f92b-110">To set up colored indicators on Cues</span></span>
1. <span data-ttu-id="5f92b-111">Under **Aktiviteter** i rollesenteret velger du **Definer bunke-ikoner**.</span><span class="sxs-lookup"><span data-stu-id="5f92b-111">Under **Activities** on your Role Center, choose **Set Up Cues**.</span></span>  
   <span data-ttu-id="5f92b-112">Vinduet **Oppsett for bunke-ikon** vises.</span><span class="sxs-lookup"><span data-stu-id="5f92b-112">The **Cue Setup** window appears.</span></span> <span data-ttu-id="5f92b-113">Vinduet viser indikatorer som er definert for bunke-ikoner.</span><span class="sxs-lookup"><span data-stu-id="5f92b-113">The window lists the indicators that are currently setup up on Cues.</span></span>
2. <span data-ttu-id="5f92b-114">Hvis du vil endre en indikator, redigerer du feltene og endrer for eksempel verdier for forskjellige terskler.</span><span class="sxs-lookup"><span data-stu-id="5f92b-114">To modify an indicator, edit the fields and modify, for example, the values for the different thresholds.</span></span>  

<span data-ttu-id="5f92b-115">Tabellen nedenfor viser fargene som tilsvarer alternativene i feltene **Stil for nedre område**, **Stil for midterste område** og **Stil for øvre område**.</span><span class="sxs-lookup"><span data-stu-id="5f92b-115">The following table lists the colors that correspond to the options of the **Low Range Style**, **Middle Range Style**, and **High Range Style** fields.</span></span>

| <span data-ttu-id="5f92b-116">Alternativ</span><span class="sxs-lookup"><span data-stu-id="5f92b-116">Option</span></span> | <span data-ttu-id="5f92b-117">Farge</span><span class="sxs-lookup"><span data-stu-id="5f92b-117">Color</span></span> |
| --- | --- |
| <span data-ttu-id="5f92b-118">**Ingen**</span><span class="sxs-lookup"><span data-stu-id="5f92b-118">**None**</span></span> |<span data-ttu-id="5f92b-119">Ingen farge (samme farge som bunkeflisen)</span><span class="sxs-lookup"><span data-stu-id="5f92b-119">No color (same color as the Cue tile)</span></span>|
| <span data-ttu-id="5f92b-120">**Fordelaktig**</span><span class="sxs-lookup"><span data-stu-id="5f92b-120">**Favorable**</span></span> |<span data-ttu-id="5f92b-121">Grønn</span><span class="sxs-lookup"><span data-stu-id="5f92b-121">Green</span></span> |
| <span data-ttu-id="5f92b-122">**Ufordelaktig**</span><span class="sxs-lookup"><span data-stu-id="5f92b-122">**Unfavorable**</span></span> |<span data-ttu-id="5f92b-123">Rød</span><span class="sxs-lookup"><span data-stu-id="5f92b-123">Red</span></span> |
| <span data-ttu-id="5f92b-124">**Tvetydig**</span><span class="sxs-lookup"><span data-stu-id="5f92b-124">**Ambiguous**</span></span> |<span data-ttu-id="5f92b-125">Gul</span><span class="sxs-lookup"><span data-stu-id="5f92b-125">Yellow</span></span> |
| <span data-ttu-id="5f92b-126">**Underordnet**</span><span class="sxs-lookup"><span data-stu-id="5f92b-126">**Subordinate**</span></span> |<span data-ttu-id="5f92b-127">Grå</span><span class="sxs-lookup"><span data-stu-id="5f92b-127">Gray</span></span> |

## <a name="see-also"></a><span data-ttu-id="5f92b-128">Se også</span><span class="sxs-lookup"><span data-stu-id="5f92b-128">See Also</span></span>
<span data-ttu-id="5f92b-129">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5f92b-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

