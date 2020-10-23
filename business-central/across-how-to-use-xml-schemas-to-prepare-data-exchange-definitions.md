---
title: Bruke XML-skjemaer til å klargjøre datautvekslingsdefinisjoner
description: Bruk XML-skjemaer til å konfigurere rammeverket for dokumentutveksling.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d2e600f3b2da20540e224cb1405a50adc4a31f25
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924956"
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a><span data-ttu-id="d9bc9-103">Bruke XML-skjemaer til å klargjøre datautvekslingsdefinisjoner</span><span class="sxs-lookup"><span data-stu-id="d9bc9-103">Use XML Schemas to Prepare Data Exchange Definitions</span></span>

<span data-ttu-id="d9bc9-104">Du kan gjøre det mulig å importere/eksportere data i XML-filer via rammeverket for datautveksling [!INCLUDE[d365fin](includes/d365fin_md.md)] ved å bruke XML-skjemaer til å definere hvilke dataelementer du vil utveksle med [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d9bc9-104">To enable import/export of data in XML files through the data exchange framework in [!INCLUDE[d365fin](includes/d365fin_md.md)], you can use XML schemas to define which data elements you want to exchange with [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="d9bc9-105">Du kan gjøre dette på siden **Visningsprogram for XML-skjema** ved å laste inn XML-skjemafilen, velge de aktuelle dataelementene og deretter initialisere en datautvekslingsdefinisjon.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-105">You perform this work on the **XML Schema Viewer** page by loading the XML schema file, selecting the relevant data elements, and then initializing a data exchange definition.</span></span>  

 <span data-ttu-id="d9bc9-106">Når du har definert hvilke dataelementer du vil ta med basert på XML-skjemaet, kan du bruke handlingen **Generer datautvekslingsdefinisjon** til å initialisere en datautvekslingsdefinisjon basert på de valgte dataelementene, som du deretter fullfører i rammeverket for datautveksling.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-106">When you have defined which data elements to include based on the XML schema, you can use the **Generate Data Exchange Definition** action to initialize a data exchange definition based on the selected data elements, which you then complete in the Data Exchange Framework.</span></span> <span data-ttu-id="d9bc9-107">Dermed opprettes en post på siden **Definisjoner av bokføringsutveksling**, der du fortsetter ved å definere hvilke felt i [!INCLUDE[d365fin](includes/d365fin_md.md)] som elementene i filen skal tilordnes til.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-107">This creates a record on the **Posting Exchange Definition** page where you continue by defining which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="d9bc9-108">Hvis du vil ha mer informasjon, kan du se [Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md)</span><span class="sxs-lookup"><span data-stu-id="d9bc9-108">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

 <span data-ttu-id="d9bc9-109">Dette emnet inneholder følgende fremgangsmåter:</span><span class="sxs-lookup"><span data-stu-id="d9bc9-109">This topic contains the following procedures:</span></span>  

- <span data-ttu-id="d9bc9-110">Slik laster du inn en XML-skjemafil:</span><span class="sxs-lookup"><span data-stu-id="d9bc9-110">To load an XML schema file</span></span>  

- <span data-ttu-id="d9bc9-111">Slik velger eller fjerner du noder i et XML-skjema:</span><span class="sxs-lookup"><span data-stu-id="d9bc9-111">To select or clear nodes in an XML schema</span></span>  

- <span data-ttu-id="d9bc9-112">Slik genererer du en datautvekslingsdefinisjon som er basert på et XML-skjema:</span><span class="sxs-lookup"><span data-stu-id="d9bc9-112">To generate a data exchange definition that is based on an XML schema</span></span>  

## <a name="to-load-an-xml-schema-file"></a><span data-ttu-id="d9bc9-113">Slik laster du inn en XML-skjemafil:</span><span class="sxs-lookup"><span data-stu-id="d9bc9-113">To load an XML schema file</span></span>

1. <span data-ttu-id="d9bc9-114">Kontroller at den aktuelle XML-skjemafilen er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-114">Make sure that the relevant XML schema file is available.</span></span> <span data-ttu-id="d9bc9-115">Filtypen er XSD.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-115">The file extension is .xsd.</span></span>  

2. <span data-ttu-id="d9bc9-116">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **XML-skjemaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schemas**, and then choose the related link.</span></span>  

3. <span data-ttu-id="d9bc9-117">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-117">Choose the **New** action.</span></span>  

4. <span data-ttu-id="d9bc9-118">Fyll ut feltene som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-118">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="d9bc9-119">Felt</span><span class="sxs-lookup"><span data-stu-id="d9bc9-119">Field</span></span>|<span data-ttu-id="d9bc9-120">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d9bc9-120">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="d9bc9-121">**Kode**</span><span class="sxs-lookup"><span data-stu-id="d9bc9-121">**Code**</span></span>|<span data-ttu-id="d9bc9-122">Angi en kode som identifiserer XML-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-122">Specify a code to identify the XML schema.</span></span>|  
    |<span data-ttu-id="d9bc9-123">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="d9bc9-123">**Description**</span></span>|<span data-ttu-id="d9bc9-124">Angi en beskrivelse av XML-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-124">Specify a description of the XML schema.</span></span>|  

     <span data-ttu-id="d9bc9-125">Feltet **Målnavneområde** angir eventuelle navneområder i XML-skjemafilen som er lastet inn for linjen.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-125">The **Target Namespace** field specifies any namespace in the XML schema file that has been loaded for the line.</span></span>  

5. <span data-ttu-id="d9bc9-126">Velg **Last inn skjema**-handlingen, og velg deretter XML-skjemafilen.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-126">Choose the **Load Schema** action, and then select the XML schema file.</span></span>  

     <span data-ttu-id="d9bc9-127">Når filen er lastet inn, fylles resten av feltene på linjen med informasjon fra filen, og det merkes av for **Skjemaet er lastet inn**.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-127">When the file is loaded, the rest of the fields on the line are filled with information from the file, and the **Schema is Loaded** check box is selected.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="d9bc9-128">Treet i det innlastede XML-skjemaet er skjult som standard.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-128">The tree of the loaded XML schema is collapsed by default.</span></span> <span data-ttu-id="d9bc9-129">Du utvider hver node ved å velge **+**-knappen på noden.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-129">You expand each node by choosing the **+** button on the node.</span></span> <span data-ttu-id="d9bc9-130">Hvis du vil utvide alle noder, velger du **Utvid alle** på båndet.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-130">To expand all nodes, choose **Expand All** on the ribbon.</span></span>  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a><span data-ttu-id="d9bc9-131">Slik velger eller fjerner du noder i et XML-skjema:</span><span class="sxs-lookup"><span data-stu-id="d9bc9-131">To select or clear nodes in an XML schema</span></span>  

1. <span data-ttu-id="d9bc9-132">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Visningsprogram for XML-skjema**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schema Viewer**, and then choose the related link.</span></span>  

2. <span data-ttu-id="d9bc9-133">Fyll ut feltene i hodet som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-133">Fill the fields on the header as described in the following table.</span></span>  

    |<span data-ttu-id="d9bc9-134">Felt</span><span class="sxs-lookup"><span data-stu-id="d9bc9-134">Field</span></span>|<span data-ttu-id="d9bc9-135">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d9bc9-135">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="d9bc9-136">**XML-skjemakode**</span><span class="sxs-lookup"><span data-stu-id="d9bc9-136">**XML Schema Code**</span></span>|<span data-ttu-id="d9bc9-137">Angi XML-skjemafilen du lastet inn i trinn 5 under «Slik laster du inn en XML-skjemafil».</span><span class="sxs-lookup"><span data-stu-id="d9bc9-137">Specify the XML schema file that you loaded in step 5 in the "To load an XML schema file" section.</span></span>|  
    |<span data-ttu-id="d9bc9-138">**Ny XMLport nr.**</span><span class="sxs-lookup"><span data-stu-id="d9bc9-138">**New XMLport No.**</span></span>|<span data-ttu-id="d9bc9-139">Angi nummeret på XMLport som opprettes fra dette XML-skjemaet når du velger handlingen **Generer XMLport**.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-139">Specify the number of the XMLport that is created from this XML schema when you choose the **Generate XMLport** action.</span></span>|  

     <span data-ttu-id="d9bc9-140">Linjene er nå fylt med noder som representerer alle elementene i XML-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-140">The lines are now filled with nodes representing all elements in the XML schema.</span></span> <span data-ttu-id="d9bc9-141">Noder for elementer som er obligatoriske i henhold til XML-skjemaet blir valgt som standard.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-141">Nodes for elements that are mandatory according to the XML schema are selected by default.</span></span>  

3. <span data-ttu-id="d9bc9-142">På den første linjen i **Nodenavn**-kolonnen viser du **Dokument**-noden, og deretter viser du gradvis de underliggende nodene som du vil se gjennom.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-142">On the first line, in the **Node Name** column, expand the **Document** node, and then gradually expand underlying nodes that you want to review.</span></span>  

     <span data-ttu-id="d9bc9-143">Du kan også høyreklikke en node, og deretter velge **Vis alle**.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-143">Alternatively, right-click on a node and then choose **Expand All**.</span></span>  

4. <span data-ttu-id="d9bc9-144">Velg én av følgende handlinger for å endre hvilke noder som skal vises.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-144">Choose either of the following actions to change which nodes are displayed.</span></span>  

    |<span data-ttu-id="d9bc9-145">**Handling**</span><span class="sxs-lookup"><span data-stu-id="d9bc9-145">**Action**</span></span>|<span data-ttu-id="d9bc9-146">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d9bc9-146">Description</span></span>|  
    |----------------|---------------------------------------|  
    |<span data-ttu-id="d9bc9-147">**Vis alle**</span><span class="sxs-lookup"><span data-stu-id="d9bc9-147">**Show All**</span></span>|<span data-ttu-id="d9bc9-148">Alle noder vises.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-148">All nodes are shown.</span></span>|  
    |<span data-ttu-id="d9bc9-149">**Skjul ikke-obligatorisk**</span><span class="sxs-lookup"><span data-stu-id="d9bc9-149">**Hide Non-Mandatory**</span></span>|<span data-ttu-id="d9bc9-150">Det vises bare noder som representerer elementer som er nødvendig i henhold til XML-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-150">Only nodes representing elements that are required according to the XML schema are shown.</span></span> <span data-ttu-id="d9bc9-151">Disse nodene er vanligvis angitt med **1** i feltet **MinOccurs**.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-151">These nodes are typically indicated by a **1** in the **MinOccurs** field.</span></span><br /><br /> <span data-ttu-id="d9bc9-152">Velg **Vis alle** for å reversere visningen.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-152">Choose **Show All** to reverse the view.</span></span>|  
    |<span data-ttu-id="d9bc9-153">**Skjul ikke-valgt**</span><span class="sxs-lookup"><span data-stu-id="d9bc9-153">**Hide Non-Selected**</span></span>|<span data-ttu-id="d9bc9-154">Det vises bare noder der det er merket av for **Valgt**.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-154">Only nodes where the **Selected** check box is selected are shown.</span></span><br /><br /> <span data-ttu-id="d9bc9-155">Velg **Vis alle** for å reversere visningen.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-155">Choose **Show All** to reverse the view.</span></span>|  

5. <span data-ttu-id="d9bc9-156">Velg handlingen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-156">Choose the **Edit** action.</span></span>  

6. <span data-ttu-id="d9bc9-157">I avmerkingsboksen **Valgt** angir du for hver node om du vil at elementet skal støttes i datautvekslingsdefinisjonen for den relaterte SEPA-bankfilen.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-157">In the **Selected** check box, specify for each node if you want the element to be supported in the data exchange definition for the related SEPA bank file.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="d9bc9-158">Når du merker en obligatorisk underordnet node, merkes også alle overordnede noder ovenfor.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-158">When you select a mandatory child node, all parent nodes above it are also selected.</span></span>  

7. <span data-ttu-id="d9bc9-159">Velg handlingen **Merk alle obligatoriske elementer** for å merke på nytt alle noder som representerer elementer som er obligatoriske i henhold til XML-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-159">Choose the **Select All Mandatory Elements** action to reselect all nodes that represent elements that are mandatory according to the XML schema.</span></span>  

8. <span data-ttu-id="d9bc9-160">Velg handlingen **Fjern all merking** for å fjerne all merking.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-160">Choose the **Deselect All** action to clear all selections.</span></span>  

     <span data-ttu-id="d9bc9-161">**Valg**-feltet angir at noden har to eller flere likestilte noder som fungerer som alternativer.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-161">The **Choice** field specifies that the node has two or more sibling nodes that function as options.</span></span>  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a><span data-ttu-id="d9bc9-162">Slik genererer du en datautvekslingsdefinisjon som er basert på et XML-skjema:</span><span class="sxs-lookup"><span data-stu-id="d9bc9-162">To generate a data exchange definition that is based on an XML schema</span></span>  

1. <span data-ttu-id="d9bc9-163">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **XML-skjemaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-163">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter  **XML Schemas**, and then choose the related link.</span></span>  

2. <span data-ttu-id="d9bc9-164">Velg det relevante XML-skjemaet, og velg deretter handlingen **Åpne XML-skjemavisning**.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-164">Select the relevant XML schema, and then choose the **Open XML Schema Viewer** action.</span></span>  

3. <span data-ttu-id="d9bc9-165">Kontroller at de aktuelle nodene er valgt.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-165">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="d9bc9-166">Hvis du vil ha mer informasjon, kan du se avsnittet «Slik velger eller fjerner du noder i et XML-skjema».</span><span class="sxs-lookup"><span data-stu-id="d9bc9-166">For more information, see the "To select or clear nodes in an XML schema" section.</span></span>  

4. <span data-ttu-id="d9bc9-167">På siden **Visningsprogram for XML-skjema** velger du handlingen **Generer datautvekslingsdefinisjon**.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-167">On the **XML Schema Viewer** page, choose the **Generate Data Exchange Definition** action.</span></span>  

 <span data-ttu-id="d9bc9-168">En datautvekslingsdefinisjon opprettes på siden **Definisjoner av bokføringsutveksling**, som du kan fullføre ved å angi hvilke elementer som er tilordnet hvilke felt i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d9bc9-168">A data exchange definition is created on the **Posting Exchange Definition** page, which you can complete by specifying which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="d9bc9-169">Hvis du vil ha mer informasjon, kan du se [Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md)</span><span class="sxs-lookup"><span data-stu-id="d9bc9-169">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="d9bc9-170">Du kan også bruke **Hent filstruktur**-funksjonen fra siden **Definisjoner av bokføringsutveksling**, som bruker funksjonaliteten på siden **Visningsprogram for XML-skjema** til å forhåndsutfylle hurtigfanen **Kolonnedefinisjoner**.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-170">You can also use the **Get File Structure** function from the **Posting Exchange Definition** page, which uses the functionality of the **XML Schema Viewer** page to prefill the **Column Definitions** TastTab.</span></span>  

> [!NOTE]
> <span data-ttu-id="d9bc9-171">I lanseringsbølge 1 for 2019 og tidligere versjoner kunne du generere en XMLport som var basert på skjemaet, og deretter importere den til løsningen.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-171">In 2019 release wave 1 and earlier versions, you could generate an XMLport that was based on the schema and then import that into your solution.</span></span> <span data-ttu-id="d9bc9-172">Denne støttes ikke lenger.</span><span class="sxs-lookup"><span data-stu-id="d9bc9-172">This is no longer supported.</span></span>

## <a name="see-also"></a><span data-ttu-id="d9bc9-173">Se også</span><span class="sxs-lookup"><span data-stu-id="d9bc9-173">See Also</span></span>

[<span data-ttu-id="d9bc9-174">Definere datautvekslingsdefinisjoner</span><span class="sxs-lookup"><span data-stu-id="d9bc9-174">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="d9bc9-175">Eksportere betalinger til en bankfil</span><span class="sxs-lookup"><span data-stu-id="d9bc9-175">Export Payments to a Bank File</span></span>](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[<span data-ttu-id="d9bc9-176">Innkreve betalinger med SEPA direct debit</span><span class="sxs-lookup"><span data-stu-id="d9bc9-176">Collect Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="d9bc9-177">Rammeverket for datautveksling</span><span class="sxs-lookup"><span data-stu-id="d9bc9-177">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)  
