---
title: Hjelpefunksjoner
description: Hurtigtaster og andre hjelpefunksjoner.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/26/2020
ms.author: edupont
ms.openlocfilehash: 5636f4b449a944e6b4d67e3dcae9f4c6657e5e06
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757720"
---
# <a name="accessibility-and-keyboard-shortcuts"></a><span data-ttu-id="ba910-103">Tilgjengelighet og hurtigtaster</span><span class="sxs-lookup"><span data-stu-id="ba910-103">Accessibility and Keyboard Shortcuts</span></span>

<span data-ttu-id="ba910-104">Dette emnet inneholder informasjon om funksjonene som gjør [!INCLUDE[prod_short](includes/prod_short.md)] lett tilgjengelig for personer med funksjonshemminger.</span><span class="sxs-lookup"><span data-stu-id="ba910-104">This topic provides information about the features that make [!INCLUDE[prod_short](includes/prod_short.md)] readily available to people with disabilities.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="ba910-105">støtter følgende tilgjengelighetsfunksjoner:</span><span class="sxs-lookup"><span data-stu-id="ba910-105">supports the following accessibility features:</span></span>  

- <span data-ttu-id="ba910-106">Tastatursnarveier</span><span class="sxs-lookup"><span data-stu-id="ba910-106">Keyboard shortcuts</span></span>

    <span data-ttu-id="ba910-107">Hvis du vil ha mer informasjon, kan du se  [Hurtigtaster](keyboard-shortcuts.md)</span><span class="sxs-lookup"><span data-stu-id="ba910-107">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md)</span></span>

- <span data-ttu-id="ba910-108">Navigasjon</span><span class="sxs-lookup"><span data-stu-id="ba910-108">Navigation</span></span>  

- <span data-ttu-id="ba910-109">Overskrifter</span><span class="sxs-lookup"><span data-stu-id="ba910-109">Headings</span></span>  

- <span data-ttu-id="ba910-110">Alternativ tekst for bilder og koblinger</span><span class="sxs-lookup"><span data-stu-id="ba910-110">Alternative text for images and links</span></span>  

- <span data-ttu-id="ba910-111">Støtte for vanlige tekniske hjelpefunksjoner</span><span class="sxs-lookup"><span data-stu-id="ba910-111">Support for common assistive technologies</span></span>  

- <span data-ttu-id="ba910-112">Bruk hurtigtaster til å zoome inn eller ut på en side</span><span class="sxs-lookup"><span data-stu-id="ba910-112">Use keyboard shortcuts to zoom in or out on any page</span></span>

<!-- moved to separate article
##  <a name="Keyboard"></a> Keyboard Shortcuts in the browser
 [!INCLUDE[prod_short](includes/prod_short.md)] supports the keyboard shortcuts that are supported by most web browsers. The keyboard shortcuts described here refer to the U.S. keyboard layout. The layout of the keys on other keyboards may not correspond exactly to the keys on a U.S. keyboard.  

|To do this|Press|  
|----------------|-----------|  
|To move focus to the next or previous control or element on a page, such as buttons, fields, or items in a list.|Tab, Shift+Tab|  
|To enable or access the element or control that is in focus.|Enter|  
|To scroll items up and down in a list.|Up Arrow, Down Arrow|  
|To scroll columns of an item left and right in a list.|Left Arrow, Right Arrow|  
|To open a drop-down list or look up a value for a field.|Alt+Down Arrow|  
|To move focus to the next element outside the list.|Ctrl + Enter|  
|To see the transactions that resulted in a calculated value in a field.|Alt+Right Arrow|  

-->

## <a name="navigation"></a><a name="Navigation"></a> <span data-ttu-id="ba910-113">Navigasjon</span><span class="sxs-lookup"><span data-stu-id="ba910-113">Navigation</span></span>  
 <span data-ttu-id="ba910-114">Du kan gå mellom faneblad og handlinger på båndet, elementer i navigasjonsstolpen og andre kontroller på [!INCLUDE[prod_short](includes/prod_short.md)]-sider og -rapporter med tastaturet.</span><span class="sxs-lookup"><span data-stu-id="ba910-114">You can navigate between the tabs and actions in the ribbon, elements in the navigation bar, and other controls on [!INCLUDE[prod_short](includes/prod_short.md)] pages and reports using the keyboard.</span></span> <span data-ttu-id="ba910-115">Hvis du vil flytte fokus fra én fane, handling eller kontroll til en annen, trykker du på tabulatortasten for å flytte fremover.</span><span class="sxs-lookup"><span data-stu-id="ba910-115">To move the focus from one tab, action, or control to another, press the Tab key to move forward.</span></span> <span data-ttu-id="ba910-116">Trykk på Skift+Tab for å flytte bakover.</span><span class="sxs-lookup"><span data-stu-id="ba910-116">Press Shift+Tab to move backward.</span></span>  

 <span data-ttu-id="ba910-117">Ved hjelp av tabulatorrekkefølgen kan du for eksempel også bytte mellom hovedlesersiden og dialogboksene som ber om bekreftelse, eller påloggingssiden.</span><span class="sxs-lookup"><span data-stu-id="ba910-117">By using the tab order, you can also switch between the main browser page and dialog boxes that request confirmation, for example, or the login page.</span></span>  

## <a name="headings-in-content"></a><a name="Headings"></a> <span data-ttu-id="ba910-118">Overskrifter i innhold</span><span class="sxs-lookup"><span data-stu-id="ba910-118">Headings in Content</span></span>
 
 <span data-ttu-id="ba910-119">HTML-kilden for [!INCLUDE[prod_short](includes/prod_short.md)]-innhold bruker koder for å hjelpe brukere av hjelpeteknologi til å forstå strukturen og innholdet på siden.</span><span class="sxs-lookup"><span data-stu-id="ba910-119">The HTML source for [!INCLUDE[prod_short](includes/prod_short.md)] content uses tags to help users of assistive technology to understand the structure and content of the page.</span></span> <span data-ttu-id="ba910-120">For eksempel på listesider defineres kolonnene i TH-koder og kolonneoverskriftene defineres med TITTEL-attributtet inni koden.</span><span class="sxs-lookup"><span data-stu-id="ba910-120">For example, on list pages, the columns are defined in TH tags and the column headings are set with TITLE attribute inside the tag.</span></span> <span data-ttu-id="ba910-121">Overskrifter for elementer, for eksempel hurtigfaner faktabokser og felt, inkluderes i overskriftskoder (H1, H2, H3 og H4).</span><span class="sxs-lookup"><span data-stu-id="ba910-121">Captions for elements, such as FastTabs, FactBoxes, and fields are included in heading tags (H1, H2, H3, and H4).</span></span>  

## <a name="image-and-links"></a><a name="Images"></a> <span data-ttu-id="ba910-122">Bilde og koblinger</span><span class="sxs-lookup"><span data-stu-id="ba910-122">Image and Links</span></span>

 <span data-ttu-id="ba910-123">Det angis en beskrivende tekst for bilder med ALT-attributtet inni IMG-koden.</span><span class="sxs-lookup"><span data-stu-id="ba910-123">A descriptive text for images is set with the ALT attribute inside the IMG tag.</span></span> <span data-ttu-id="ba910-124">Det angis en beskrivende tekst for hyperkoblinger med tittelattributtet inni A-koden.</span><span class="sxs-lookup"><span data-stu-id="ba910-124">A descriptive text for hyperlinks is set with the title attribute inside the A tag.</span></span>  

## <a name="assistive-technologies"></a><a name="AssistiveTech"></a> <span data-ttu-id="ba910-125">Hjelpeteknologi</span><span class="sxs-lookup"><span data-stu-id="ba910-125">Assistive Technologies</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="ba910-126">støtter ulike hjelpteknologier, for eksempel høy kontrast, skjermlesere og talegjenkjenningsprogramvare.</span><span class="sxs-lookup"><span data-stu-id="ba910-126">supports various assistive technologies, such as high contrast, screen readers, and voice recognition software.</span></span> <span data-ttu-id="ba910-127">Det kan være at noen hjelpeteknologier ikke fungerer godt med bestemte elementer på [!INCLUDE[prod_short](includes/prod_short.md)]-sider.</span><span class="sxs-lookup"><span data-stu-id="ba910-127">Some assistive technologies may not work well with certain elements in [!INCLUDE[prod_short](includes/prod_short.md)] pages.</span></span>  

## <a name="zoom"></a><a name="zoom"></a> <span data-ttu-id="ba910-128">Zoom</span><span class="sxs-lookup"><span data-stu-id="ba910-128">Zoom</span></span>

<span data-ttu-id="ba910-129">De fleste nettlesere bruker standard tastatursnarveier for å zoome inn og ut på gjeldende side.</span><span class="sxs-lookup"><span data-stu-id="ba910-129">Most browsers use standard keyboard shortcuts to zoom in and out on the current page.</span></span> <span data-ttu-id="ba910-130">Disse hurtigtastene er ikke spesifikke for [!INCLUDE [prod_short](includes/prod_short.md)], men de fungerer når du bruker [!INCLUDE [prod_short](includes/prod_short.md)] i en nettleser.</span><span class="sxs-lookup"><span data-stu-id="ba910-130">These keyboard shortcuts are not specific to [!INCLUDE [prod_short](includes/prod_short.md)], but they work when you use [!INCLUDE [prod_short](includes/prod_short.md)] in a browser.</span></span> <span data-ttu-id="ba910-131">Hvis du vil se en liste over støttede hurtigtaster, kan du se [Hurtigtaster for å zoome inn og ut](keyboard-shortcuts.md#zoomshortcuts).</span><span class="sxs-lookup"><span data-stu-id="ba910-131">For a list of supported keyboard shortcuts, see [Keyboard Shortcuts for Zooming In and Out](keyboard-shortcuts.md#zoomshortcuts).</span></span>  

## <a name="for-more-accessibility-information"></a><span data-ttu-id="ba910-132">For mer informasjon om tilgjengelighet</span><span class="sxs-lookup"><span data-stu-id="ba910-132">For more accessibility information</span></span>

<span data-ttu-id="ba910-133">Du finner mer informasjon om tilgjengelighet med Microsoft-produkter og hjelpeteknologi på nettstedet for [Microsoft Accessibility](https://go.microsoft.com/fwlink/?LinkId=262160).</span><span class="sxs-lookup"><span data-stu-id="ba910-133">You can find additional information about accessibility with Microsoft products and assistive technologies on the [Microsoft Accessibility](https://go.microsoft.com/fwlink/?LinkId=262160) site.</span></span>

## <a name="see-also"></a><span data-ttu-id="ba910-134">Se også</span><span class="sxs-lookup"><span data-stu-id="ba910-134">See Also</span></span>

[<span data-ttu-id="ba910-135">Komme i gang</span><span class="sxs-lookup"><span data-stu-id="ba910-135">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="ba910-136">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ba910-136">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="ba910-137">Vanlige spørsmål</span><span class="sxs-lookup"><span data-stu-id="ba910-137">Frequently Asked Questions</span></span>](across-faq.md)  
