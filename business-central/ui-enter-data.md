---
title: Skrive inn data i felt | Microsoft-dokumentasjon
description: Lære om generelle funksjoner som kan hjelpe deg med å registrere data i feltene.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 00143454cf0b0da9b111f92bcdb7879c7e6743d2
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1252461"
---
# <a name="entering-data"></a><span data-ttu-id="ac29a-103">Skrive inn data</span><span class="sxs-lookup"><span data-stu-id="ac29a-103">Entering Data</span></span>

<span data-ttu-id="ac29a-104">Det finnes mange generelle funksjoner som kan hjelpe deg med å registrere data enklere, raskere og mer nøyaktig.</span><span class="sxs-lookup"><span data-stu-id="ac29a-104">There are many general features that help you enter data easier, faster, and more accurate.</span></span> <span data-ttu-id="ac29a-105">De generelle funksjonene for å skrive inn data beskrives i denne artikkelen.</span><span class="sxs-lookup"><span data-stu-id="ac29a-105">The general features for entering data are described in this article.</span></span>  

<!-- The examples in this article use the demonstration data.-->

## <a name="keyboard-shortcuts"></a><span data-ttu-id="ac29a-106">Hurtigtaster</span><span class="sxs-lookup"><span data-stu-id="ac29a-106">Keyboard Shortcuts</span></span>

<span data-ttu-id="ac29a-107">Det finnes flere tastatursnarveier som lar deg jobbe uten musen og utføre raskere dataregistrering, særlig med oppføringer i stor skala og gjentakende tasteoppgaver.</span><span class="sxs-lookup"><span data-stu-id="ac29a-107">There are several keyboard shortcuts that let you to work "mouse-free" and speed up your data entry, especially with large scale entries and repetitive typing tasks.</span></span>

<span data-ttu-id="ac29a-108">Hvis du vil ha mer informasjon om snarveier, kan du se [Hurtigtaster](keyboard-shortcuts.md).</span><span class="sxs-lookup"><span data-stu-id="ac29a-108">For more information about shortcuts, see [Keyboard Shortcuts](keyboard-shortcuts.md).</span></span> <span data-ttu-id="ac29a-109">Noen av hurtigtastene beskrives i denne artikkelen.</span><span class="sxs-lookup"><span data-stu-id="ac29a-109">A few of the shortcuts are discussed in this article.</span></span>

## <a name="QuickEntry"></a><span data-ttu-id="ac29a-110">Raskere dataregistrering ved hjelp av hurtigoppføring</span><span class="sxs-lookup"><span data-stu-id="ac29a-110">Accelerating Data Entry Using Quick Entry</span></span>

<span data-ttu-id="ac29a-111">Hurtigoppføring er en funksjon som er beregnet på dataregistrering når du bruker tastaturet.</span><span class="sxs-lookup"><span data-stu-id="ac29a-111">Quick Entry is a feature designed for data entry when using the keyboard.</span></span> <span data-ttu-id="ac29a-112">Hurtigoppføring fungerer på felt (som på kortsider) og i lister (rader og kolonner).</span><span class="sxs-lookup"><span data-stu-id="ac29a-112">Quick Entry works on fields (like on card pages) and in lists (rows and columns).</span></span> <span data-ttu-id="ac29a-113">Det er nyttig når du utfører gjentakende skriveoppgaver som krever oppretting av flere poster i rekkefølge, for eksempel en kjørsel for ordrer eller registrering av nye varer.</span><span class="sxs-lookup"><span data-stu-id="ac29a-113">It is beneficial when performing repetitive typing tasks that require creating multiple records in sequence, such as a batch of sales orders or registering new items.</span></span>

<span data-ttu-id="ac29a-114">Det kan være du allerede er kjent med bruk av tabulatortasten for å navigere fra ett felt på en side til neste redigerbare felt.</span><span class="sxs-lookup"><span data-stu-id="ac29a-114">You might already be familiar with using the Tab key to navigate from one field on a page to the next editable field.</span></span> <span data-ttu-id="ac29a-115">En ulempe ved bruk av tabulatoren er at den alltid går fortløpende til neste felt.</span><span class="sxs-lookup"><span data-stu-id="ac29a-115">A disadvantage of using Tab is that it always goes sequentially to the next field.</span></span> <!-- even if the field is non-editable or seldom filled it in.--><span data-ttu-id="ac29a-116">Med Hurtigoppføring kan du endre denne banen.</span><span class="sxs-lookup"><span data-stu-id="ac29a-116">Quick Entry lets you change this path.</span></span> <span data-ttu-id="ac29a-117">Med Hurtigoppføring kan du bruke Enter-tasten til å navigere gjennom feltene du er interessert i, og hoppe over ikke-redigerbare felt og felt du vanligvis ikke fyller ut.</span><span class="sxs-lookup"><span data-stu-id="ac29a-117">With Quick Entry, you use the Enter key to navigate through only those fields that you are interested in, skipping non-editable fields and fields that you typically do not fill in.</span></span> <span data-ttu-id="ac29a-118">Du kan allerede ha oppdaget denne atferden på noen sider.</span><span class="sxs-lookup"><span data-stu-id="ac29a-118">You might have already noticed this behavior on some pages.</span></span> <span data-ttu-id="ac29a-119">Dette er fordi programmet allerede angir hvilke felt som skal tas med når det trykkes på Enter, og hvilke som skal hoppes over.</span><span class="sxs-lookup"><span data-stu-id="ac29a-119">This is because the application already designates which fields to include when pressing Enter and which ones to skip.</span></span> <span data-ttu-id="ac29a-120">Du kan tilpasse Hurtigoppføring ved å tilpasse arbeidsområdet og optimalisere hvordan du registrerer data på hver side.</span><span class="sxs-lookup"><span data-stu-id="ac29a-120">You can customize Quick Entry by personalizing your workspace and optimizing how you enter data on each page.</span></span>

### <a name="how-quick-entry-works"></a><span data-ttu-id="ac29a-121">Hvordan Hurtigoppføring fungerer</span><span class="sxs-lookup"><span data-stu-id="ac29a-121">How Quick Entry Works</span></span>

<span data-ttu-id="ac29a-122">Alle felt kan merkes som *Ta med i hurtigoppføring* eller *Utelat fra hurtigoppføring*.</span><span class="sxs-lookup"><span data-stu-id="ac29a-122">Every field can be marked as either being *included in Quick Entry* or *excluded from Quick Entry*.</span></span> <span data-ttu-id="ac29a-123">Felt som er inkludert i hurtigoppføringen, inkluderes i banen når du trykker på Enter. Felt som er ekskludert fra hurtigoppføringen, inkluderes ikke.</span><span class="sxs-lookup"><span data-stu-id="ac29a-123">Fields that are included in Quick Entry, will be included in the path when you press Enter; fields that are excluded from Quick Entry, will not.</span></span>

<span data-ttu-id="ac29a-124">Når du er ferdig med å registrere data i et felt, kan du ganske enkelt trykke Enter for å bekrefte endringene og gå til neste felt.</span><span class="sxs-lookup"><span data-stu-id="ac29a-124">When you are finished entering data in a field, you simply press Enter to confirm the changes and go to the next field.</span></span> <span data-ttu-id="ac29a-125">Hvis du vil reversere retningen og gå til forrige felt, trykker du på Skift+Enter.</span><span class="sxs-lookup"><span data-stu-id="ac29a-125">If you want to reverse direction, and go the previous field, press Shift+Enter.</span></span> <span data-ttu-id="ac29a-126">Hvis du vil ha mer informasjon om snarveier, kan du se [Hurtigreferanse for tastatursnarveier](keyboard-shortcuts.md#QuickEntry).</span><span class="sxs-lookup"><span data-stu-id="ac29a-126">For more information about shortcuts, see [Quick Entry keyboard shortcuts](keyboard-shortcuts.md#QuickEntry).</span></span>

#### <a name="tips-and-tricks"></a><span data-ttu-id="ac29a-127">Tips og triks</span><span class="sxs-lookup"><span data-stu-id="ac29a-127">Tips and tricks</span></span>
<span data-ttu-id="ac29a-128">Nedenfor finner du nyttig informasjon om hvordan du bruker Hurtigoppføring.</span><span class="sxs-lookup"><span data-stu-id="ac29a-128">The following provides some useful information about using Quick Entry.</span></span>

- <span data-ttu-id="ac29a-129">Funksjonen er tilgjengelig for alle redigerbare felt.</span><span class="sxs-lookup"><span data-stu-id="ac29a-129">It is available for any editable fields.</span></span>
- <span data-ttu-id="ac29a-130">Den fungerer også i kolonner og rader.</span><span class="sxs-lookup"><span data-stu-id="ac29a-130">It also works across columns and rows.</span></span>
- <span data-ttu-id="ac29a-131">Den hindrer ikke tilgang til andre elementer på en side, for eksempel handlinger.</span><span class="sxs-lookup"><span data-stu-id="ac29a-131">It does not prevent accessing other elements of a page, such as actions.</span></span> <span data-ttu-id="ac29a-132">Disse er fortsatt tilgjengelige ved hjelp av tabulatoren og Skift+Tab.</span><span class="sxs-lookup"><span data-stu-id="ac29a-132">These are still accessible by using Tab and Shift+Tab.</span></span>  
- <span data-ttu-id="ac29a-133">Hurtigfaner trenger ikke å utvides for at Hurtigoppføring skal fungere.</span><span class="sxs-lookup"><span data-stu-id="ac29a-133">FastTabs do not have to be expanded for Quick Entry to work.</span></span> <span data-ttu-id="ac29a-134">Hvis det neste Hurtigoppføring-feltet befinner seg i en skjult hurtigfane, vil denne hurtigfanen utvides automatisk og fokusere på det valgte feltet.</span><span class="sxs-lookup"><span data-stu-id="ac29a-134">If the next Quick Entry field is located in a collapsed FastTab, that FastTab will automatically expand and focus on the designated field.</span></span>
- <span data-ttu-id="ac29a-135">Hurtigoppføring fungerer uavhengig av om felt er obligatoriske.</span><span class="sxs-lookup"><span data-stu-id="ac29a-135">Quick Entry works irrespective of whether fields are mandatory.</span></span> <span data-ttu-id="ac29a-136">Derfor er det lurt å sikre at obligatoriske felt er inkludert i Hurtigoppføring.</span><span class="sxs-lookup"><span data-stu-id="ac29a-136">So it is a good idea to ensure that mandatory fields are included in Quick Entry.</span></span>
- <span data-ttu-id="ac29a-137">Som standard inkluderes de fleste feltene automatisk i Hurtigoppføring.</span><span class="sxs-lookup"><span data-stu-id="ac29a-137">By default, most fields are automatically included in Quick Entry.</span></span> <span data-ttu-id="ac29a-138">Så i starten vil oppgaven din sannsynligvis eksludere felt fra Hurtigoppføring.</span><span class="sxs-lookup"><span data-stu-id="ac29a-138">So initially your task will most likely be excluding fields from Quick Entry.</span></span>

### <a name="how-to-change-quick-entry-fields"></a><span data-ttu-id="ac29a-139">Endre Hurtigoppføring-felt</span><span class="sxs-lookup"><span data-stu-id="ac29a-139">How to Change Quick Entry Fields</span></span>

<span data-ttu-id="ac29a-140">Hvis du vil endre hvilke felt som inkluderes i eller utelates fra Hurtigoppføring på en side, kan du bruke tilpasning.</span><span class="sxs-lookup"><span data-stu-id="ac29a-140">To change which fields are included in or excluded from Quick Entry on a page, you use personalization.</span></span>

1. <span data-ttu-id="ac29a-141">Start tilpasningen ved å velge ikonet ![Innstillinger](media/ui-experience/settings_icon_small.png "Innstillinger-ikonet for rollesenteret"), og klikk deretter **Tilpass**.</span><span class="sxs-lookup"><span data-stu-id="ac29a-141">Start personalization by selecting the ![Settings](media/ui-experience/settings_icon_small.png "Settings icon for role center") icon, and then **Personalize**.</span></span>
2. <span data-ttu-id="ac29a-142">Velg et felt som du vil endre, eller velg tilsvarende kolonneoverskrift i lister, og velg deretter **Ta med i hurtigoppføring** eller **Utelat fra hurtigoppføring**.</span><span class="sxs-lookup"><span data-stu-id="ac29a-142">Select a field that you want change, or in lists, select the corresponding column heading, and then choose either **Include in Quick Entry** or **Exclude from Quick Entry**.</span></span>

<span data-ttu-id="ac29a-143">Hvis du vil ha mer informasjon om tilpasning, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="ac29a-143">For more information about personalization, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="ac29a-144">Obligatoriske felt</span><span class="sxs-lookup"><span data-stu-id="ac29a-144">Mandatory Fields</span></span>

<span data-ttu-id="ac29a-145">Når du angir data på sider, merkes bestemte felt med en rød stjerne.</span><span class="sxs-lookup"><span data-stu-id="ac29a-145">When you enter data on pages, certain fields are marked with a red asterisk.</span></span> <span data-ttu-id="ac29a-146">Den røde stjernen betyr at feltet må fylles ut for å fullføre en bestemt prosess som bruker feltet, for eksempel bokføre en transaksjon som bruker verdien i feltet.</span><span class="sxs-lookup"><span data-stu-id="ac29a-146">The red asterisk means that the field must be filled to complete a certain process that uses the field, such as posting a transaction that uses the value in the field.</span></span>  

<span data-ttu-id="ac29a-147">Selv om feltet inneholder en rød stjerne, er du ikke nødt til å fylle ut feltet før du går videre til andre felt eller lukker siden.</span><span class="sxs-lookup"><span data-stu-id="ac29a-147">Even though the field contains a red asterisk, you are not forced to fill the field before you continue to other fields or close the page.</span></span> <span data-ttu-id="ac29a-148">Stjernen bare fungerer som en påminnelse om at du vil bli blokkert fra å fullføre en bestemt prosess.</span><span class="sxs-lookup"><span data-stu-id="ac29a-148">The red asterisk only serves as a reminder that you will be blocked from completing a certain process.</span></span>  

## <a name="finding-data-as-you-type"></a><span data-ttu-id="ac29a-149">Finne data mens du skriver</span><span class="sxs-lookup"><span data-stu-id="ac29a-149">Finding Data As You Type</span></span>

 <span data-ttu-id="ac29a-150">Når du begynner å skrive inn tegn i et felt, åpnes en rullegardinliste med mulige feltverdier.</span><span class="sxs-lookup"><span data-stu-id="ac29a-150">When you start to type characters in a field, a drop-down list is displayed and shows possible field values.</span></span> <span data-ttu-id="ac29a-151">Innholdet i listen endres etter hvert som du skriver inn flere tegn, og du kan velge ønsket verdi når den vises.</span><span class="sxs-lookup"><span data-stu-id="ac29a-151">The list changes as you type more characters, and you can select the correct value when it is displayed.</span></span>  

 <span data-ttu-id="ac29a-152">Mange felt har en pil-ned-knapp som du kan velge.</span><span class="sxs-lookup"><span data-stu-id="ac29a-152">Many fields have a down arrow button that you can choose.</span></span> <span data-ttu-id="ac29a-153">Du velger pilen for å få frem en liste over data som kan settes inn i feltet.</span><span class="sxs-lookup"><span data-stu-id="ac29a-153">You choose the arrow to get a list of data that is available to enter in the field.</span></span> <span data-ttu-id="ac29a-154">Knappen har to funksjoner, avhengig av felttype:</span><span class="sxs-lookup"><span data-stu-id="ac29a-154">The button has two functions depending on the type of field:</span></span>  

-   <span data-ttu-id="ac29a-155">Oppslag - viser informasjon fra en annen tabell som du kan sette inn i feltet.</span><span class="sxs-lookup"><span data-stu-id="ac29a-155">Lookup - Displays information from another table that you can enter in the field.</span></span> <span data-ttu-id="ac29a-156">Du kan velge én datadel om gangen.</span><span class="sxs-lookup"><span data-stu-id="ac29a-156">You can select one piece of data at a time.</span></span>  

-   <span data-ttu-id="ac29a-157">Rullegardin - viser settet med alternativer som finnes for feltet.</span><span class="sxs-lookup"><span data-stu-id="ac29a-157">Drop-down - Displays the set of options that exist for the field.</span></span> <span data-ttu-id="ac29a-158">Du kan bare velge ett av alternativene.</span><span class="sxs-lookup"><span data-stu-id="ac29a-158">You can select only one of the options.</span></span>  

## <a name="copying-and-pasting-fields-and-lines"></a><span data-ttu-id="ac29a-159">Kopiere og lime inn felt og linjer</span><span class="sxs-lookup"><span data-stu-id="ac29a-159">Copying and Pasting Fields and Lines</span></span>

<span data-ttu-id="ac29a-160">Du kan kopiere en eller flere rader fra en oversikt eller ett enkelt felt på en side og deretter lime inn det du kopierte, på samme side, en annen side eller et eksternt dokument (som Microsoft Excel og Outlook-e-post).</span><span class="sxs-lookup"><span data-stu-id="ac29a-160">You can copy one or more rows from a list or a single field on a page, and then paste what you copied into the same page, another page, or an external document (like Microsoft Excel and Outlook email).</span></span> <span data-ttu-id="ac29a-161">Kort sagt, for å kopiere trykker du CTRL+C (cmd+C i macOS) på tastaturet.</span><span class="sxs-lookup"><span data-stu-id="ac29a-161">In short, to copy, you press CTRL+C (cmd+C in macOS) on your keyboard.</span></span> <span data-ttu-id="ac29a-162">For å lime inn trykker du CTRL+V (cmd+V i macOS).</span><span class="sxs-lookup"><span data-stu-id="ac29a-162">To paste, you press CTRL+V (cmd+V in macOS).</span></span>

<span data-ttu-id="ac29a-163">Trykk på F8 i listen for å kopiere feltet i den samme kolonnen i raden over, og lim det inn i den gjeldende raden.</span><span class="sxs-lookup"><span data-stu-id="ac29a-163">In a list, to copy the field in the same column of the row above, and paste it into the current row, just press F8.</span></span>

<span data-ttu-id="ac29a-164">Hvis du vil ha mer informasjon, kan du se [Kopiere og lime inn i Business Central](ui-copy-paste.md).</span><span class="sxs-lookup"><span data-stu-id="ac29a-164">For more information, see [Copying and Pasting in Business Central](ui-copy-paste.md).</span></span>

## <a name="Focus"></a><span data-ttu-id="ac29a-165">Fokusere på linjeelementer</span><span class="sxs-lookup"><span data-stu-id="ac29a-165">Focusing on Line Items</span></span>

<span data-ttu-id="ac29a-166">Når du arbeider med dokumenter som inkluderer en linjeelementdel, som en ordre- eller fakturaside, kan du bytte visningen slik at fokus endres til bare linjeelementene, og hovedsakelig utvide linjeelementdelen, slik at den opptar så godt som hele arbeidsområdet og skjuler andre deler av siden bortsett fra handlingsområdet øverst.</span><span class="sxs-lookup"><span data-stu-id="ac29a-166">When working on documents that include a line items part, like a sales order or invoice page, you can switch your view to focus only on the line items, essentially expanding the line items part so that it occupies pretty much the entire workspace - hiding other parts of the page except the actions area at the top.</span></span> <span data-ttu-id="ac29a-167">Dette gir deg bedre oversikt over linjelementene og gir mer plass til å arbeide med dem.</span><span class="sxs-lookup"><span data-stu-id="ac29a-167">This gives you a better overview of the lines items, and provides more room to work on them.</span></span> <span data-ttu-id="ac29a-168">Dette er særlig nyttig når du arbeider med store linjeelementlister og rask dataregistrering er ønskelig.</span><span class="sxs-lookup"><span data-stu-id="ac29a-168">This is particularly beneficial when working with large line item lists and fast data entry is desired.</span></span>

<span data-ttu-id="ac29a-169">En annen fordel er at det også gir deg avanserte filtreringsmuligheter, som i andre oversikter, så sporing og søk gjennom linjeelementer blir enda enklere.</span><span class="sxs-lookup"><span data-stu-id="ac29a-169">Another advantage is that it also provides advanced filtering capability, like on other lists, so browsing and searching through line items becomes even easier.</span></span>

### <a name="switch-the-focus-on-and-off"></a><span data-ttu-id="ac29a-170">Bytte fokus på og av</span><span class="sxs-lookup"><span data-stu-id="ac29a-170">Switch the Focus On and Off</span></span>

<span data-ttu-id="ac29a-171">Når du skal fokusere på linjeelementer, velger du hvor som helst i linjeelementdelen og velger deretter ![Fokusmodusikon](media/focus-mode.png "Fokusmodusikon") øverst til høyre, eller trykk på Ctrl+Skift+F12.</span><span class="sxs-lookup"><span data-stu-id="ac29a-171">To focus on lines items, select anywhere in the line item part, and then choose ![Focus Mode icon](media/focus-mode.png "Focus mode icon") in the upper right corner or press Ctrl+Shift+F12.</span></span>

<span data-ttu-id="ac29a-172">Hvis du vil gå tilbake til den normale visningen, kan du velge ![Fokusmodusikon](media/focus-mode.png "Fokusmodusikon"), eller trykk på Ctrl+Skift+F12 på nytt.</span><span class="sxs-lookup"><span data-stu-id="ac29a-172">To switch back to the normal view, choose ![Focus Mode icon](media/focus-mode.png "Focus mode icon") or press Ctrl+Shift+F12 again.</span></span>

### <a name="filtering-the-line-items"></a><span data-ttu-id="ac29a-173">Filtrere linjeelementer</span><span class="sxs-lookup"><span data-stu-id="ac29a-173">Filtering the Line Items</span></span>

<span data-ttu-id="ac29a-174">For å starte filtreringen kan du velge ![Filtreringsruteikon](media/open-filter-pane-icon.png "Filtreringsruteikon") øverst i oversikten eller trykke på **Skift+F3** for å åpne filtreringsruten.</span><span class="sxs-lookup"><span data-stu-id="ac29a-174">To start filtering, select ![Filter pane icon](media/open-filter-pane-icon.png "Filter pane icon") at the top of the list or press **Shift+F3** to open the filter pane.</span></span> <span data-ttu-id="ac29a-175">Du arbeider med filtreringsruten som i andre oversikter.</span><span class="sxs-lookup"><span data-stu-id="ac29a-175">You work with the filter pane as you do on any other list.</span></span> <span data-ttu-id="ac29a-176">Hvis du vil ha mer informasjon, kan du se [Filtrering](ui-enter-criteria-filters.md#Filtering).</span><span class="sxs-lookup"><span data-stu-id="ac29a-176">For more information, see [Filtering](ui-enter-criteria-filters.md#Filtering).</span></span>

<span data-ttu-id="ac29a-177">Filtrere er spesielt nyttig når du viser og analysere lengre dokumenter.</span><span class="sxs-lookup"><span data-stu-id="ac29a-177">Filtering is especially helpful when viewing and analysing longer documents.</span></span> <span data-ttu-id="ac29a-178">Tenk deg at du åpner en bokført salgsfaktura og filtrerer linjeelementene for å vise alle linjeelementer som har en individuell rabatt på mer enn 5 %, eller filtrer for å vise bare sykkeltilbehør med "pro" i navnet.</span><span class="sxs-lookup"><span data-stu-id="ac29a-178">For example, imagine you open a posted sales invoice and filter the line items to display all line items that have an individual discount above 5%, or filter to display only bike accessories with 'pro' in the name.</span></span>

## <a name="entering-quantities-by-calculation"></a><span data-ttu-id="ac29a-179">Angi antall ved beregning</span><span class="sxs-lookup"><span data-stu-id="ac29a-179">Entering Quantities by Calculation</span></span>

<span data-ttu-id="ac29a-180">Når du setter inn tall i antallfelt, for eksempel **Antall**-feltet på en varekladdlinje, kan du angi formelen i stedet for summen.</span><span class="sxs-lookup"><span data-stu-id="ac29a-180">When entering numbers into quantity fields, such as the **Quantity** field on an item journal line, you can enter the formula instead of the sum quantity.</span></span>  

### <a name="examples"></a><span data-ttu-id="ac29a-181">Eksempler</span><span class="sxs-lookup"><span data-stu-id="ac29a-181">Examples</span></span>  

-   <span data-ttu-id="ac29a-182">Hvis du skriver inn 19+19, beregnes feltet til 38.</span><span class="sxs-lookup"><span data-stu-id="ac29a-182">If you enter 19+19, the field is calculated to 38.</span></span>  

-   <span data-ttu-id="ac29a-183">Hvis du skriver inn 41-9, beregnes feltet til 32.</span><span class="sxs-lookup"><span data-stu-id="ac29a-183">If you enter 41-9, the field is calculated to 32.</span></span>  

-   <span data-ttu-id="ac29a-184">Hvis du skriver inn 12\*4, beregnes feltet til 48.</span><span class="sxs-lookup"><span data-stu-id="ac29a-184">If you enter 12\*4, the field is calculated to 48.</span></span>  

-   <span data-ttu-id="ac29a-185">Hvis du skriver inn 12/4, beregnes feltet til 3.</span><span class="sxs-lookup"><span data-stu-id="ac29a-185">If you enter 12/4, the field is calculated to 3.</span></span>  

## <a name="entering-negative-numbers"></a><span data-ttu-id="ac29a-186">Skrive inn negative tall</span><span class="sxs-lookup"><span data-stu-id="ac29a-186">Entering Negative Numbers</span></span>

<span data-ttu-id="ac29a-187">Du kan angi negative tall på to måter.</span><span class="sxs-lookup"><span data-stu-id="ac29a-187">You can enter negative numbers in two ways.</span></span> <span data-ttu-id="ac29a-188">Tallet -20,5 kan angis som:</span><span class="sxs-lookup"><span data-stu-id="ac29a-188">The number -20.5 can be entered as:</span></span>  

-   <span data-ttu-id="ac29a-189">-20,5</span><span class="sxs-lookup"><span data-stu-id="ac29a-189">-20.5</span></span>  

    <span data-ttu-id="ac29a-190">eller</span><span class="sxs-lookup"><span data-stu-id="ac29a-190">or</span></span>
-   <span data-ttu-id="ac29a-191">20,5-</span><span class="sxs-lookup"><span data-stu-id="ac29a-191">20.5-</span></span>  

 <span data-ttu-id="ac29a-192">I begge tilfeller registreres beløpet som -20,5.</span><span class="sxs-lookup"><span data-stu-id="ac29a-192">In both cases, the amount will be recorded in as -20.5.</span></span>  

 <span data-ttu-id="ac29a-193">Hvis det siste tegnet i uttrykket er en **++** eller en **--**, blir hele uttrykket registrert med dette tegnet.</span><span class="sxs-lookup"><span data-stu-id="ac29a-193">If the last character of the expression is a **+** or a **-**, the entire expression will be recorded with that sign.</span></span> <span data-ttu-id="ac29a-194">Eksempel: **10-20+** resulterer i 10 og ikke -10.</span><span class="sxs-lookup"><span data-stu-id="ac29a-194">An example, **10-20+** will result in 10 and not -10.</span></span>  

## <a name="entering-dates-and-times"></a><span data-ttu-id="ac29a-195">Angi datoer og klokkeslett</span><span class="sxs-lookup"><span data-stu-id="ac29a-195">Entering Dates and Times</span></span>

<span data-ttu-id="ac29a-196">Du kan sette inn datoer og klokkeslett i alle felt som er spesifikt tilordnet til datoer (datofelt).</span><span class="sxs-lookup"><span data-stu-id="ac29a-196">You can enter dates and times in all the fields that are specifically assigned to dates (date fields).</span></span> <span data-ttu-id="ac29a-197">Datoene kan skrives inn med eller uten skilletegn.</span><span class="sxs-lookup"><span data-stu-id="ac29a-197">You can enter dates with or without separators.</span></span>

> [!NOTE]  
> <span data-ttu-id="ac29a-198">Hvordan du angir dato og klokkeslett på, avhenger av dine **Område**-innstillinger.</span><span class="sxs-lookup"><span data-stu-id="ac29a-198">How you enter dates and times depends on your **Region** settings.</span></span> <span data-ttu-id="ac29a-199">Hvis du vil ha mer informasjon, kan du se [Endre grunnleggende innstillinger](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="ac29a-199">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>  

### <a name="entering-dates"></a><span data-ttu-id="ac29a-200">Sette inn datoer</span><span class="sxs-lookup"><span data-stu-id="ac29a-200">Entering Dates</span></span>

<span data-ttu-id="ac29a-201">For datofelt kan du bruke datavelgeren, som lar deg velge en dato fra en kalender, eller du kan angi datoer manuelt.</span><span class="sxs-lookup"><span data-stu-id="ac29a-201">For date fields, you can either use the data picker, which lets you select a date from a calender, or you can enter dates manually.</span></span> <span data-ttu-id="ac29a-202">Denne delen inneholder en kort oversikt over hvordan du angir datoer.</span><span class="sxs-lookup"><span data-stu-id="ac29a-202">This section provides a brief overview of how to enter dates.</span></span> <span data-ttu-id="ac29a-203">Hvis du vil ha mer informasjon, se [Arbeide med datoer og klokkeslett i kalenderen](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="ac29a-203">For more details, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

<span data-ttu-id="ac29a-204">For manuell datoregistrering kan du angi to, fire, seks eller åtte tall:</span><span class="sxs-lookup"><span data-stu-id="ac29a-204">For manually date entry, you can enter two, four, six, or eight digits:</span></span>  

-   <span data-ttu-id="ac29a-205">Hvis du bare skriver inn to tall, tolkes disse som dagen, og måneden og året for arbeidsdatoen legges til.</span><span class="sxs-lookup"><span data-stu-id="ac29a-205">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>  

-   <span data-ttu-id="ac29a-206">Hvis du skriver inn fire tall, tolkes disse som dagen og måneden, og året for arbeidsdatoen legges til.</span><span class="sxs-lookup"><span data-stu-id="ac29a-206">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span>  

-   <span data-ttu-id="ac29a-207">Hvis datoen du vil angi ligger i intervallet 01.01.1930 til og med 31.12.2029, kan du angi året med to eller fire sifre.</span><span class="sxs-lookup"><span data-stu-id="ac29a-207">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>  

<span data-ttu-id="ac29a-208">Du kan også angi en dato som en ukedag etterfulgt av et ukenummer og, hvis du vil, et år (for eksempel Man25 eller man25 betyr mandag i uke 25).</span><span class="sxs-lookup"><span data-stu-id="ac29a-208">You can also enter a date as a weekday followed by a week number and, optionally, a year (for example, Mon25 or mon25 means Monday in week 25).</span></span>  

<span data-ttu-id="ac29a-209">I stedet for å skrive inn en bestemt dato kan du skrive inn én av disse kodene.</span><span class="sxs-lookup"><span data-stu-id="ac29a-209">Instead of entering a specific date, you can enter one of these codes.</span></span>  

|<span data-ttu-id="ac29a-210"> - kode</span><span class="sxs-lookup"><span data-stu-id="ac29a-210">Code</span></span>|<span data-ttu-id="ac29a-211">Resultat</span><span class="sxs-lookup"><span data-stu-id="ac29a-211">Result</span></span>|  
|--------------|----------------|  
|<span data-ttu-id="ac29a-212">i</span><span class="sxs-lookup"><span data-stu-id="ac29a-212">t</span></span>|<span data-ttu-id="ac29a-213">Dette angir dagens dato (systemdatoen for datamaskinen).</span><span class="sxs-lookup"><span data-stu-id="ac29a-213">This specifies today's date (the system date for the computer).</span></span>|  
|<span data-ttu-id="ac29a-214">P</span><span class="sxs-lookup"><span data-stu-id="ac29a-214">p</span></span>|<span data-ttu-id="ac29a-215">Dette angir en regnskapsperiode der `p` betyr at den første regnskapsperioden, `p2` betyr den andre andre regnskapsperioden og så videre.</span><span class="sxs-lookup"><span data-stu-id="ac29a-215">This specifies an accounting period´, where `p`means the first accounting period, `p2` means the second accountin period, and so on.</span></span> |
|<span data-ttu-id="ac29a-216">a</span><span class="sxs-lookup"><span data-stu-id="ac29a-216">w</span></span>|<span data-ttu-id="ac29a-217">Dette angir arbeidsdatoen som er satt opp i programmet.</span><span class="sxs-lookup"><span data-stu-id="ac29a-217">This specifies the work date that is setup in the application.</span></span> <span data-ttu-id="ac29a-218">Du kan endre arbeidsdatoen ved å se [Endre grunnleggende innstillinger](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="ac29a-218">To change the work date, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span> <span data-ttu-id="ac29a-219">Hvis du har mange transaksjoner å utføre på en dato som ikke er dagens dato, er det en fordel å bruke arbeidsdatoen.</span><span class="sxs-lookup"><span data-stu-id="ac29a-219">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>|
|<span data-ttu-id="ac29a-220">c</span><span class="sxs-lookup"><span data-stu-id="ac29a-220">c</span></span>|<span data-ttu-id="ac29a-221">Dette angir at datoen etter `c` er en avslutningsdato, for eksempel `C123101`.</span><span class="sxs-lookup"><span data-stu-id="ac29a-221">This specifies that the date after `c`is a closing date, for example `C123101`.</span></span>|  

## <a name="entering-times"></a><span data-ttu-id="ac29a-222">Angi klokkeslett</span><span class="sxs-lookup"><span data-stu-id="ac29a-222">Entering Times</span></span>

<span data-ttu-id="ac29a-223">Et vilkårlig skilletegn kan settes inn mellom tidsinndelingene, men det er ikke obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="ac29a-223">When you enter times, you can insert any separator sign that you want between the units, but it is not required.</span></span> <span data-ttu-id="ac29a-224">Du behøver ikke å skrive inn minutter eller sekunder.</span><span class="sxs-lookup"><span data-stu-id="ac29a-224">You do not have to write minutes, seconds, or AM/PM.</span></span>  

<span data-ttu-id="ac29a-225">Tabellen nedenfor viser en oversikt over ulike måter å angi tidsinnstillinger på, og hvordan de tolkes.</span><span class="sxs-lookup"><span data-stu-id="ac29a-225">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span>  

|<span data-ttu-id="ac29a-226">Angivelse</span><span class="sxs-lookup"><span data-stu-id="ac29a-226">Entry</span></span>|<span data-ttu-id="ac29a-227">Tolkning</span><span class="sxs-lookup"><span data-stu-id="ac29a-227">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="ac29a-228">5</span><span class="sxs-lookup"><span data-stu-id="ac29a-228">5</span></span>|<span data-ttu-id="ac29a-229">05:00:00</span><span class="sxs-lookup"><span data-stu-id="ac29a-229">05:00:00</span></span>|  
|<span data-ttu-id="ac29a-230">5:30</span><span class="sxs-lookup"><span data-stu-id="ac29a-230">5:30</span></span>|<span data-ttu-id="ac29a-231">05:30:00</span><span class="sxs-lookup"><span data-stu-id="ac29a-231">05:30:00</span></span>|  
|<span data-ttu-id="ac29a-232">0530</span><span class="sxs-lookup"><span data-stu-id="ac29a-232">0530</span></span>|<span data-ttu-id="ac29a-233">05:30:00</span><span class="sxs-lookup"><span data-stu-id="ac29a-233">05:30:00</span></span>|  
|<span data-ttu-id="ac29a-234">5:30:5</span><span class="sxs-lookup"><span data-stu-id="ac29a-234">5:30:5</span></span>|<span data-ttu-id="ac29a-235">05:30:05</span><span class="sxs-lookup"><span data-stu-id="ac29a-235">05:30:05</span></span>|  
|<span data-ttu-id="ac29a-236">053005</span><span class="sxs-lookup"><span data-stu-id="ac29a-236">053005</span></span>|<span data-ttu-id="ac29a-237">05:30:05</span><span class="sxs-lookup"><span data-stu-id="ac29a-237">05:30:05</span></span>|  
|<span data-ttu-id="ac29a-238">5:30:5,50</span><span class="sxs-lookup"><span data-stu-id="ac29a-238">5:30:5,50</span></span>|<span data-ttu-id="ac29a-239">05:30:05.5</span><span class="sxs-lookup"><span data-stu-id="ac29a-239">05:30:05.5</span></span>|  
|<span data-ttu-id="ac29a-240">053005050</span><span class="sxs-lookup"><span data-stu-id="ac29a-240">053005050</span></span>|<span data-ttu-id="ac29a-241">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="ac29a-241">05:30:05.05</span></span>|  

 <span data-ttu-id="ac29a-242">Du må angi to sifre for hver tidsenhet dersom du ikke setter inn et skilletegn.</span><span class="sxs-lookup"><span data-stu-id="ac29a-242">You must enter two digits for each unit of time if you do not enter a separator.</span></span>  

## <a name="entering-datetimes"></a><span data-ttu-id="ac29a-243">Angi datoer og klokkeslett</span><span class="sxs-lookup"><span data-stu-id="ac29a-243">Entering Datetimes</span></span>

<span data-ttu-id="ac29a-244">Når du angir dato og klokkeslett, må du sette inn et mellomrom mellom datoen og klokkeslettet.</span><span class="sxs-lookup"><span data-stu-id="ac29a-244">When you enter datetimes you must enter a space between the date and the time.</span></span>  

<span data-ttu-id="ac29a-245">Tabellen nedenfor viser de forskjellige måtene du kan angi dato og klokkeslett på, og hvordan de tolkes.</span><span class="sxs-lookup"><span data-stu-id="ac29a-245">The following table lists the various ways in which you can enter datetimes and how they are interpreted.</span></span>  

|<span data-ttu-id="ac29a-246">Post</span><span class="sxs-lookup"><span data-stu-id="ac29a-246">Entry</span></span>|<span data-ttu-id="ac29a-247">Tolkning</span><span class="sxs-lookup"><span data-stu-id="ac29a-247">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="ac29a-248">131202 132455</span><span class="sxs-lookup"><span data-stu-id="ac29a-248">131202 132455</span></span>|<span data-ttu-id="ac29a-249">13.12.02 13.24.55</span><span class="sxs-lookup"><span data-stu-id="ac29a-249">13-12-02 13:24:55</span></span>|  
|<span data-ttu-id="ac29a-250">1.12.02 10</span><span class="sxs-lookup"><span data-stu-id="ac29a-250">1-12-02 10</span></span>|<span data-ttu-id="ac29a-251">01.12.02 10:00:00</span><span class="sxs-lookup"><span data-stu-id="ac29a-251">01-12-02 10:00:00</span></span>|  
|<span data-ttu-id="ac29a-252">1.12.02 5</span><span class="sxs-lookup"><span data-stu-id="ac29a-252">1.12.02 5</span></span>|<span data-ttu-id="ac29a-253">12.01.02 05:00:00</span><span class="sxs-lookup"><span data-stu-id="ac29a-253">01-12-02 05:00:00</span></span>|  
|<span data-ttu-id="ac29a-254">1.12.02</span><span class="sxs-lookup"><span data-stu-id="ac29a-254">1.12.02</span></span>|<span data-ttu-id="ac29a-255">01.12.02 00.00.00</span><span class="sxs-lookup"><span data-stu-id="ac29a-255">01-12-02 00:00:00</span></span>|  
|<span data-ttu-id="ac29a-256">11 12</span><span class="sxs-lookup"><span data-stu-id="ac29a-256">11 12</span></span>|<span data-ttu-id="ac29a-257">11 - inneværende måned - inneværende år 12.00.00</span><span class="sxs-lookup"><span data-stu-id="ac29a-257">11-current month-current year 12:00:00</span></span>|  
|<span data-ttu-id="ac29a-258">1112 12</span><span class="sxs-lookup"><span data-stu-id="ac29a-258">1112 12</span></span>|<span data-ttu-id="ac29a-259">11-12 - inneværende år 12.00.00</span><span class="sxs-lookup"><span data-stu-id="ac29a-259">11-12-current year 12:00:00</span></span>|  
|<span data-ttu-id="ac29a-260">t eller i dag</span><span class="sxs-lookup"><span data-stu-id="ac29a-260">t or today</span></span>|<span data-ttu-id="ac29a-261">dagens dato 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ac29a-261">today's date 00:00:00</span></span>|  
|<span data-ttu-id="ac29a-262">klokkeslett</span><span class="sxs-lookup"><span data-stu-id="ac29a-262">t time</span></span>|<span data-ttu-id="ac29a-263">dagens dato og klokkeslett</span><span class="sxs-lookup"><span data-stu-id="ac29a-263">today's date actual time</span></span>|  
|<span data-ttu-id="ac29a-264">k 10.30</span><span class="sxs-lookup"><span data-stu-id="ac29a-264">t 10:30</span></span>|<span data-ttu-id="ac29a-265">dagens dato 10:30:00</span><span class="sxs-lookup"><span data-stu-id="ac29a-265">today's date 10:30:00</span></span>|  
|<span data-ttu-id="ac29a-266">k 3.3.3</span><span class="sxs-lookup"><span data-stu-id="ac29a-266">t 3:3:3</span></span>|<span data-ttu-id="ac29a-267">dagens dato 03.03.03</span><span class="sxs-lookup"><span data-stu-id="ac29a-267">today's date 03:03:03</span></span>|  
|<span data-ttu-id="ac29a-268">a eller arbeidsdag</span><span class="sxs-lookup"><span data-stu-id="ac29a-268">w or workdate</span></span>|<span data-ttu-id="ac29a-269">arbeidsdatoen 00.00.00</span><span class="sxs-lookup"><span data-stu-id="ac29a-269">the working date 00:00:00</span></span>|  
|<span data-ttu-id="ac29a-270">m eller mandag</span><span class="sxs-lookup"><span data-stu-id="ac29a-270">m or Monday</span></span>|<span data-ttu-id="ac29a-271">mandag i inneværende uke 00.00.00</span><span class="sxs-lookup"><span data-stu-id="ac29a-271">Monday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="ac29a-272">ti eller tirsdag</span><span class="sxs-lookup"><span data-stu-id="ac29a-272">tu or Tuesday</span></span>|<span data-ttu-id="ac29a-273">tirsdag i inneværende uke 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ac29a-273">Tuesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="ac29a-274">o eller onsdag</span><span class="sxs-lookup"><span data-stu-id="ac29a-274">we or Wednesday</span></span>|<span data-ttu-id="ac29a-275">onsdag i inneværende uke 00.00.00</span><span class="sxs-lookup"><span data-stu-id="ac29a-275">Wednesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="ac29a-276">to eller torsdag</span><span class="sxs-lookup"><span data-stu-id="ac29a-276">th or Thursday</span></span>|<span data-ttu-id="ac29a-277">torsdag i inneværende uke 00.00.00</span><span class="sxs-lookup"><span data-stu-id="ac29a-277">Thursday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="ac29a-278">f eller fredag</span><span class="sxs-lookup"><span data-stu-id="ac29a-278">f or Friday</span></span>|<span data-ttu-id="ac29a-279">fredag i inneværende uke 00.00.00</span><span class="sxs-lookup"><span data-stu-id="ac29a-279">Friday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="ac29a-280">l eller lørdag</span><span class="sxs-lookup"><span data-stu-id="ac29a-280">s or Saturday</span></span>|<span data-ttu-id="ac29a-281">lørdag i inneværende uke 00.00.00</span><span class="sxs-lookup"><span data-stu-id="ac29a-281">Saturday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="ac29a-282">s eller søndag</span><span class="sxs-lookup"><span data-stu-id="ac29a-282">su or Sunday</span></span>|<span data-ttu-id="ac29a-283">søndag i inneværende uke 00.00.00</span><span class="sxs-lookup"><span data-stu-id="ac29a-283">Sunday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="ac29a-284">ti 10.30</span><span class="sxs-lookup"><span data-stu-id="ac29a-284">tu 10:30</span></span>|<span data-ttu-id="ac29a-285">tirsdag i inneværende uke 10:30:00</span><span class="sxs-lookup"><span data-stu-id="ac29a-285">Tuesday of the current week 10:30:00</span></span>|  
|<span data-ttu-id="ac29a-286">ti 3.3.3</span><span class="sxs-lookup"><span data-stu-id="ac29a-286">tu 3:3:3</span></span>|<span data-ttu-id="ac29a-287">tirsdag i inneværende uke 03.03.03</span><span class="sxs-lookup"><span data-stu-id="ac29a-287">Tuesday of the current week 03:03:03</span></span>|  

## <a name="entering-duration"></a><span data-ttu-id="ac29a-288">Angi varighet</span><span class="sxs-lookup"><span data-stu-id="ac29a-288">Entering Duration</span></span>

<span data-ttu-id="ac29a-289">Du angir en varighet som et tall etterfulgt av enheten.</span><span class="sxs-lookup"><span data-stu-id="ac29a-289">You enter a duration as a number followed by its unit of measure.</span></span>  

<span data-ttu-id="ac29a-290">Her er noen eksempler.</span><span class="sxs-lookup"><span data-stu-id="ac29a-290">Here are some examples.</span></span>  

|<span data-ttu-id="ac29a-291">Varighet</span><span class="sxs-lookup"><span data-stu-id="ac29a-291">Duration</span></span>|<span data-ttu-id="ac29a-292">Enhtet\*\*</span><span class="sxs-lookup"><span data-stu-id="ac29a-292">Unit of measure\*\*</span></span>|  
|------------------|-------------------------|  
|<span data-ttu-id="ac29a-293">2t</span><span class="sxs-lookup"><span data-stu-id="ac29a-293">2h</span></span>|<span data-ttu-id="ac29a-294">2 timer</span><span class="sxs-lookup"><span data-stu-id="ac29a-294">2 hrs</span></span>|  
|<span data-ttu-id="ac29a-295">6t 30 m</span><span class="sxs-lookup"><span data-stu-id="ac29a-295">6h 30 m</span></span>|<span data-ttu-id="ac29a-296">6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="ac29a-296">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="ac29a-297">6,5t</span><span class="sxs-lookup"><span data-stu-id="ac29a-297">6.5h</span></span>|<span data-ttu-id="ac29a-298">6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="ac29a-298">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="ac29a-299">90m</span><span class="sxs-lookup"><span data-stu-id="ac29a-299">90m</span></span>|<span data-ttu-id="ac29a-300">1 t 30 min</span><span class="sxs-lookup"><span data-stu-id="ac29a-300">1 hr 30 mins</span></span>|  
|<span data-ttu-id="ac29a-301">2d 6t 30m</span><span class="sxs-lookup"><span data-stu-id="ac29a-301">2d 6h 30m</span></span>|<span data-ttu-id="ac29a-302">2 dager 6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="ac29a-302">2 days 6 hrs 30 mins</span></span>|  
|<span data-ttu-id="ac29a-303">2d 6t 30m 56s 600ms</span><span class="sxs-lookup"><span data-stu-id="ac29a-303">2d 6h 30m 56s 600ms</span></span>|<span data-ttu-id="ac29a-304">2 dager 6 timer 30 min 56 sek 600 msek</span><span class="sxs-lookup"><span data-stu-id="ac29a-304">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|  

 <span data-ttu-id="ac29a-305">Du kan også angi et tall, og det blir automatisk konvertert til et tidsintervall.</span><span class="sxs-lookup"><span data-stu-id="ac29a-305">You can also enter a number and it is automatically converted to a duration.</span></span> <span data-ttu-id="ac29a-306">Tallet du angir, konverteres i henhold til standardenheten som er angitt for feltet Varighet.</span><span class="sxs-lookup"><span data-stu-id="ac29a-306">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>  

 <span data-ttu-id="ac29a-307">Hvis du vil se hvilken enhet som er brukt i et varighetsfelt, kan du angi et tall og se hvilken enhet programmet er konvertert det til.</span><span class="sxs-lookup"><span data-stu-id="ac29a-307">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>  

 <span data-ttu-id="ac29a-308">Tallet 5 konverteres til 5 timer hvis enheten er timer.</span><span class="sxs-lookup"><span data-stu-id="ac29a-308">The number 5 is converted to 5 hrs, if the unit of measure is hours.</span></span>  

<!--OnPrem  ##  <a name="BKMK_SettingDateRanges"></a> Setting Date Ranges  
 You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges.  

|**Meaning**|**Sample expression**|**Entries included**|  
|-----------------|---------------------------|--------------------------|  
|**Equal to**|12 15 00|Only those posted on 12 15 00.|  
|**Interval**|12 15 00..01 15 01<br /><br /> ..12 15 00|Those posted on dates between and including 12 15 00 and 01 15 01.<br /><br /> Those posted on 12 15 00 or earlier.|  
|**Either/or**|12 15 00&#124;12 16 00|Those posted on either 12 15 00 or 12 16 00. If there are entries posted on both days, they will all be displayed.|  

 You can also combine the various format types.  

|**Sample expression**|**Entries included**|  
|---------------------------|--------------------------|  
|12 15 00&#124;12 01 00..12 10 00|Entries posted either on 12 15 00 or on dates between and including 12 01 00 and 12 10 00.|  
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|

## Using Date Formulas

 A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.  

> [!NOTE]  
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, if you enter 1W, for example, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter 6D or 1W-1D.  

 Here are some examples of how date formulas can be used:  

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.  

-   The date formula in the Grace Period field for a specified reminder level determines the period of time that must pass from the due date (or from the date of the previous reminder) before a reminder will be created.  

-   The date formula in the Due Date Calculation field determines how to calculate the due date on the reminder.  

 The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.  

|||  
|-|-|  
|C|Current|  
|D|Day(s)|  
|W|Week(s)|  
|M|Month(s)|  
|Q|Quarter(s)|  
|Y|Year(s)|  

 You can construct a date formula in three ways.  

 The following example shows how current plus a time unit.  

|||  
|-|-|  
|CW|Current week|  
|CM|Current month|  

 The following example shows how a number and a time unit. A number cannot be larger than 9999.  

|||  
|-|-|  
|10D|10 days from today|  
|2W|2 weeks from today|  

 The following example shows how a time unit and a number.  

|||  
|-|-|  
|D10|The next 10th day of a month|  
|WD4|The next 4th day of a week (Thursday)|  

 The following example shows how you can combine these three forms as needed.  

|||  
|-|-|  
|CM+10D|Current month + 10 days|  

 The following example shows how you can use a minus sign to indicate a date in the past.  

|||  
|-|-|  
|-1Y|1 year ago from today|

[!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->

## <a name="see-also"></a><span data-ttu-id="ac29a-309">Se også</span><span class="sxs-lookup"><span data-stu-id="ac29a-309">See Also</span></span>  
 [<span data-ttu-id="ac29a-310">Sortere, søke etter og filtrere oversikter</span><span class="sxs-lookup"><span data-stu-id="ac29a-310">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
 <span data-ttu-id="ac29a-311">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ac29a-311">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
