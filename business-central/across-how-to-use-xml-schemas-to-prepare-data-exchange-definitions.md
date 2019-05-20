---
title: Opprette XML-porter på XML-skjemaer | Microsoft-dokumentasjon
description: Bruk XML-skjemaer til å konfigurere rammeverket for dokumentutveksling.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: bac8d19bd48d9b7ad981c75dc54b155c8fe765a5
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245053"
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a><span data-ttu-id="bf3e2-103">Bruke XML-skjemaer til å klargjøre datautvekslingsdefinisjoner</span><span class="sxs-lookup"><span data-stu-id="bf3e2-103">Use XML Schemas to Prepare Data Exchange Definitions</span></span>
<span data-ttu-id="bf3e2-104">Du kan gjøre det mulig å importere/eksportere data i XML-filer via rammeverket for datautveksling [!INCLUDE[d365fin](includes/d365fin_md.md)] ved å bruke XML-skjemaer til å definere hvilke dataelementer du vil utveksle med [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="bf3e2-104">To enable import/export of data in XML files through the data exchange framework in [!INCLUDE[d365fin](includes/d365fin_md.md)], you can use XML schemas to define which data elements you want to exchange with [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="bf3e2-105">Du kan gjøre dette på siden **Visningsprogram for XML-skjema** ved å laste inn XML-skjemafilen, velge de aktuelle dataelementene og deretter initialisere en datautvekslingsdefinisjon eller en XMLport.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-105">You perform this work on the **XML Schema Viewer** page by loading the XML schema file, selecting the relevant data elements, and then initializing either a data exchange definition or an XMLport.</span></span>  

 <span data-ttu-id="bf3e2-106">Når du har angitt hvilke dataelementer som skal inkluderes basert på XML-skjemaet, kan du bruke handlingen **Generer XMLport** til å opprette XMLport-objektet.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-106">When you have defined which data elements to include based on the XML schema, you can use the **Generate XMLport** action to create the XMLport object.</span></span>  

 <span data-ttu-id="bf3e2-107">Du kan eventuelt bruke handlingen **Generer datautvekslingsdefinisjon** for å initialisere en datautvekslingsdefinisjon basert på de valgte dataelementene, som du deretter fullfører i rammeverket for datautveksling.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-107">Alternatively, you can use the **Generate Data Exchange Definition** action to initialize a data exchange definition based on the selected data elements, which you then complete in the Data Exchange Framework.</span></span> <span data-ttu-id="bf3e2-108">Dermed opprettes en post på siden **Definisjoner av bokføringsutveksling**, der du fortsetter ved å definere hvilke felt i [!INCLUDE[d365fin](includes/d365fin_md.md)] som elementene i filen skal tilordnes til.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-108">This creates a record on the **Posting Exchange Definition** page where you continue by defining which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="bf3e2-109">Hvis du vil ha mer informasjon, kan du se [Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md)</span><span class="sxs-lookup"><span data-stu-id="bf3e2-109">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

 <span data-ttu-id="bf3e2-110">Dette emnet inneholder følgende fremgangsmåter:</span><span class="sxs-lookup"><span data-stu-id="bf3e2-110">This topic contains the following procedures:</span></span>  

-   <span data-ttu-id="bf3e2-111">Slik laster du inn en XML-skjemafil:</span><span class="sxs-lookup"><span data-stu-id="bf3e2-111">To load an XML schema file</span></span>  

-   <span data-ttu-id="bf3e2-112">Slik velger eller fjerner du noder i et XML-skjema:</span><span class="sxs-lookup"><span data-stu-id="bf3e2-112">To select or clear nodes in an XML schema</span></span>  

-   <span data-ttu-id="bf3e2-113">Slik genererer du en datautvekslingsdefinisjon som er basert på et XML-skjema:</span><span class="sxs-lookup"><span data-stu-id="bf3e2-113">To generate a data exchange definition that is based on an XML schema</span></span>  

-   <span data-ttu-id="bf3e2-114">Slik genererer du en XMLport for filen som er basert på et XML-skjema</span><span class="sxs-lookup"><span data-stu-id="bf3e2-114">To generate an XMLport for the file that is based on an XML schema</span></span>  

-   <span data-ttu-id="bf3e2-115">Slik importerer du en XMLport til Object Designer</span><span class="sxs-lookup"><span data-stu-id="bf3e2-115">To import an XMLport into the Object Designer</span></span>  

### <a name="to-load-an-xml-schema-file"></a><span data-ttu-id="bf3e2-116">Slik laster du inn en XML-skjemafil:</span><span class="sxs-lookup"><span data-stu-id="bf3e2-116">To load an XML schema file</span></span>  

1.  <span data-ttu-id="bf3e2-117">Kontroller at den aktuelle XML-skjemafilen er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-117">Make sure that the relevant XML schema file is available.</span></span> <span data-ttu-id="bf3e2-118">Filtypen er XSD.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-118">The file extension is .xsd.</span></span>  

2.  <span data-ttu-id="bf3e2-119">Skriv inn **XML-skjemaer** i **Søk**-boksen, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-119">In the **Search** box, enter **XML Schemas**, and then choose the related link.</span></span>  

3.  <span data-ttu-id="bf3e2-120">I fanen **Hjem** under **Ny** velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-120">On the **Home** tab, in the **New** group, choose **New**.</span></span>  

4.  <span data-ttu-id="bf3e2-121">Fyll ut feltene som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-121">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="bf3e2-122">Felt</span><span class="sxs-lookup"><span data-stu-id="bf3e2-122">Field</span></span>|<span data-ttu-id="bf3e2-123">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="bf3e2-123">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="bf3e2-124">**Kode**</span><span class="sxs-lookup"><span data-stu-id="bf3e2-124">**Code**</span></span>|<span data-ttu-id="bf3e2-125">Angi en kode som identifiserer XML-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-125">Specify a code to identify the XML schema.</span></span>|  
    |<span data-ttu-id="bf3e2-126">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="bf3e2-126">**Description**</span></span>|<span data-ttu-id="bf3e2-127">Angi en beskrivelse av XML-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-127">Specify a description of the XML schema.</span></span>|  

     <span data-ttu-id="bf3e2-128">Feltet **Målnavneområde** angir eventuelle navneområder i XML-skjemafilen som er lastet inn for linjen.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-128">The **Target Namespace** field specifies any namespace in the XML schema file that has been loaded for the line.</span></span>  

5.  <span data-ttu-id="bf3e2-129">Velg **Last inn skjema** under **Prosess** i fanebladet **Hjem**, og velg deretter XML-skjemafilen.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-129">On the **Home** tab, in the **Process** group, choose **Load Schema**, and then select the XML schema file.</span></span>  

     <span data-ttu-id="bf3e2-130">Når filen er lastet inn, fylles resten av feltene på linjen med informasjon fra filen, og det merkes av for **Skjemaet er lastet inn**.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-130">When the file is loaded, the rest of the fields on the line are filled with information from the file, and the **Schema is Loaded** check box is selected.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="bf3e2-131">Treet i det innlastede XML-skjemaet er skjult som standard.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-131">The tree of the loaded XML schema is collapsed by default.</span></span> <span data-ttu-id="bf3e2-132">Du utvider hver node ved å velge **+**-knappen på noden.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-132">You expand each node by choosing the **+** button on the node.</span></span> <span data-ttu-id="bf3e2-133">Hvis du vil utvide alle noder, velger du **Utvid alle** på båndet.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-133">To expand all nodes, choose **Expand All** on the ribbon.</span></span>  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a><span data-ttu-id="bf3e2-134">Slik velger eller fjerner du noder i et XML-skjema:</span><span class="sxs-lookup"><span data-stu-id="bf3e2-134">To select or clear nodes in an XML schema</span></span>  

1.  <span data-ttu-id="bf3e2-135">Skriv inn **Visningsprogram for XML-skjema** i **Søk**-boksen, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-135">In the **Search** box, enter **XML Schema Viewer**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="bf3e2-136">Fyll ut feltene i hodet som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-136">Fill the fields on the header as described in the following table.</span></span>  

    |<span data-ttu-id="bf3e2-137">Felt</span><span class="sxs-lookup"><span data-stu-id="bf3e2-137">Field</span></span>|<span data-ttu-id="bf3e2-138">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="bf3e2-138">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="bf3e2-139">**XML-skjemakode**</span><span class="sxs-lookup"><span data-stu-id="bf3e2-139">**XML Schema Code**</span></span>|<span data-ttu-id="bf3e2-140">Angi XML-skjemafilen du lastet inn i trinn 5 under "Slik laster du inn en XML-skjemafil".</span><span class="sxs-lookup"><span data-stu-id="bf3e2-140">Specify the XML schema file that you loaded in step 5 in the “To load an XML schema file” section.</span></span>|  
    |<span data-ttu-id="bf3e2-141">**Ny XMLport nr.**</span><span class="sxs-lookup"><span data-stu-id="bf3e2-141">**New XMLport No.**</span></span>|<span data-ttu-id="bf3e2-142">Angi nummeret på XMLport som opprettes fra dette XML-skjemaet når du velger handlingen **Generer XMLport**.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-142">Specify the number of the XMLport that is created from this XML schema when you choose the **Generate XMLport** action.</span></span>|  

     <span data-ttu-id="bf3e2-143">Linjene er nå fylt med noder som representerer alle elementene i XML-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-143">The lines are now filled with nodes representing all elements in the XML schema.</span></span> <span data-ttu-id="bf3e2-144">Noder for elementer som er obligatoriske i henhold til XML-skjemaet blir valgt som standard.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-144">Nodes for elements that are mandatory according to the XML schema are selected by default.</span></span>  

3.  <span data-ttu-id="bf3e2-145">På den første linjen i **Nodenavn**-kolonnen viser du **Dokument**-noden, og deretter viser du gradvis de underliggende nodene som du vil se gjennom.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-145">On the first line, in the **Node Name** column, expand the **Document** node, and then gradually expand underlying nodes that you want to review.</span></span>  

     <span data-ttu-id="bf3e2-146">Du kan også høyreklikke en node, og deretter velge **Vis alle**.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-146">Alternatively, right-click on a node and then choose **Expand All**.</span></span>  

4.  <span data-ttu-id="bf3e2-147">I kategorien **Hjem** i **Vis**-gruppen velger du én av følgende handlinger for å endre hvilke noder som skal vises.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-147">On the **Home** tab, in the **View** group, choose either of the following actions to change which nodes are displayed.</span></span>  

    |<span data-ttu-id="bf3e2-148">**Handling**</span><span class="sxs-lookup"><span data-stu-id="bf3e2-148">**Action**</span></span>|<span data-ttu-id="bf3e2-149">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="bf3e2-149">Description</span></span>|  
    |----------------|---------------------------------------|  
    |<span data-ttu-id="bf3e2-150">**Vis alle**</span><span class="sxs-lookup"><span data-stu-id="bf3e2-150">**Show All**</span></span>|<span data-ttu-id="bf3e2-151">Alle noder vises.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-151">All nodes are shown.</span></span>|  
    |<span data-ttu-id="bf3e2-152">**Skjul ikke-obligatorisk**</span><span class="sxs-lookup"><span data-stu-id="bf3e2-152">**Hide Non-Mandatory**</span></span>|<span data-ttu-id="bf3e2-153">Det vises bare noder som representerer elementer som er nødvendig i henhold til XML-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-153">Only nodes representing elements that are required according to the XML schema are shown.</span></span> <span data-ttu-id="bf3e2-154">Disse nodene er vanligvis angitt med **1** i feltet **MinOccurs**.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-154">These nodes are typically indicated by a **1** in the **MinOccurs** field.</span></span><br /><br /> <span data-ttu-id="bf3e2-155">Velg **Vis alle** for å reversere visningen.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-155">Choose **Show All** to reverse the view.</span></span>|  
    |<span data-ttu-id="bf3e2-156">**Skjul ikke-valgt**</span><span class="sxs-lookup"><span data-stu-id="bf3e2-156">**Hide Non-Selected**</span></span>|<span data-ttu-id="bf3e2-157">Det vises bare noder der det er merket av for **Valgt**.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-157">Only nodes where the **Selected** check box is selected are shown.</span></span><br /><br /> <span data-ttu-id="bf3e2-158">Velg **Vis alle** for å reversere visningen.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-158">Choose **Show All** to reverse the view.</span></span>|  

5.  <span data-ttu-id="bf3e2-159">I fanen **Hjem** under **Behandle** velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-159">On the **Home** tab, in the **Manage** group, choose **Edit**.</span></span>  

6.  <span data-ttu-id="bf3e2-160">I avmerkingsboksen **Valgt** angir du for hver node om du vil at elementet skal støttes i datautvekslingsdefinisjonen for den relaterte SEPA-bankfilen.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-160">In the **Selected** check box, specify for each node if you want the element to be supported in the data exchange definition for the related SEPA bank file.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="bf3e2-161">Når du merker en obligatorisk underordnet node, merkes også alle overordnede noder ovenfor.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-161">When you select a mandatory child node, all parent nodes above it are also selected.</span></span>  

7.  <span data-ttu-id="bf3e2-162">Velg handlingen **Merk alle obligatoriske elementer** for å merke på nytt alle noder som representerer elementer som er obligatoriske i henhold til XML-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-162">Choose the **Select All Mandatory Elements** action to reselect all nodes that represent elements that are mandatory according to the XML schema.</span></span>  

8.  <span data-ttu-id="bf3e2-163">Velg handlingen **Fjern all merking** for å fjerne all merking.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-163">Choose the **Deselect All** action to clear all selections.</span></span>  

     <span data-ttu-id="bf3e2-164">**Valg**-feltet angir at noden har to eller flere likestilte noder som fungerer som alternativer.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-164">The **Choice** field specifies that the node has two or more sibling nodes that function as options.</span></span>  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a><span data-ttu-id="bf3e2-165">Slik genererer du en datautvekslingsdefinisjon som er basert på et XML-skjema:</span><span class="sxs-lookup"><span data-stu-id="bf3e2-165">To generate a data exchange definition that is based on an XML schema</span></span>  

1.  <span data-ttu-id="bf3e2-166">Skriv inn **XML-skjemaer** i **Søk**-boksen, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-166">In the **Search** box, enter  **XML Schemas**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="bf3e2-167">Velg det aktuelle XML-skjemaet, og velg deretter **Åpne XML-skjemavisning** under **Prosess** i fanebladet **Hjem**.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-167">Select the relevant XML schema, and then on the on the **Home** tab, in the **Process** group, choose **Open XML Schema Viewer**.</span></span>  

3.  <span data-ttu-id="bf3e2-168">Kontroller at de aktuelle nodene er valgt.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-168">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="bf3e2-169">Hvis du vil ha mer informasjon, kan du se avsnittet "Slik velger eller fjerner du noder i et XML-skjema".</span><span class="sxs-lookup"><span data-stu-id="bf3e2-169">For more information, see the “To select or clear nodes in an XML schema” section.</span></span>  

4.  <span data-ttu-id="bf3e2-170">På siden **Visningsprogram for XML-skjema**, på **Hjem**-fanen, i **Prosess**-gruppen velger du **Generer datautvekslingsdefinisjon**.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-170">On the **XML Schema Viewer** page, on the **Home** tab, in the **Process** group, choose **Generate Data Exchange Definition**.</span></span>  

 <span data-ttu-id="bf3e2-171">En datautvekslingsdefinisjon opprettes på siden **Definisjoner av bokføringsutveksling**, som du kan fullføre ved å angi hvilke elementer som er tilordnet hvilke felt i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="bf3e2-171">A data exchange definition is created on the **Posting Exchange Definition** page, which you can complete by specifying which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="bf3e2-172">Hvis du vil ha mer informasjon, kan du se [Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md)</span><span class="sxs-lookup"><span data-stu-id="bf3e2-172">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="bf3e2-173">Du kan også bruke **Hent filstruktur**-funksjonen fra siden **Definisjoner av bokføringsutveksling**, som bruker funksjonaliteten på siden **Visningsprogram for XML-skjema** til å forhåndsutfylle hurtigfanen **Kolonnedefinisjoner**.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-173">You can also use the **Get File Structure** function from the **Posting Exchange Definition** page, which uses the functionality of the **XML Schema Viewer** page to prefill the **Column Definitions** TastTab.</span></span>  

### <a name="to-generate-an-xmlport-that-is-based-on-an-xml-schema"></a><span data-ttu-id="bf3e2-174">Slik genererer du en XMLport som er basert på et XML-skjema</span><span class="sxs-lookup"><span data-stu-id="bf3e2-174">To generate an XMLport that is based on an XML schema</span></span>  

1.  <span data-ttu-id="bf3e2-175">Skriv inn **XML-skjemaer** i **Søk**-boksen, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-175">In the **Search** box, enter  **XML Schemas**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="bf3e2-176">Velg det aktuelle XML-skjemaet, og velg deretter **Åpne XML-skjemavisning** under **Prosess** i fanebladet **Hjem**.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-176">Select the relevant XML schema, and then on the on the **Home** tab, in the **Process** group, choose **Open XML Schema Viewer**.</span></span>  

3.  <span data-ttu-id="bf3e2-177">I feltet **Ny XMLport nr.**</span><span class="sxs-lookup"><span data-stu-id="bf3e2-177">In the **New XMLport No.**</span></span> <span data-ttu-id="bf3e2-178">angir du nummeret som det nye XMLport-objektet blir gitt når det genereres.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-178">field, specify the number that the new XMLport object will be given when it is generated.</span></span>  

4.  <span data-ttu-id="bf3e2-179">Kontroller at de aktuelle nodene er valgt.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-179">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="bf3e2-180">Hvis du vil ha mer informasjon, kan du se avsnittet "Slik velger eller fjerner du noder i et XML-skjema".</span><span class="sxs-lookup"><span data-stu-id="bf3e2-180">For more information, see the “To select or clear nodes in an XML schema” section.</span></span>  

5.  <span data-ttu-id="bf3e2-181">I kategorien **Hjem** i **Prosess**-gruppen velger du **Generer XMLport**, og deretter lagrer du objektet som en TXT-fil på ønsket plassering.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-181">On the **Home** tab, in the **Process** group, choose **Generate XMLport**, and then save the object as a .txt file in an appropriate location.</span></span>  

6. <span data-ttu-id="bf3e2-182">Importer den nye XMLport i [!INCLUDE[d365fin](includes/d365fin_md.md)]-utviklingsmiljøet, og kompiler den.</span><span class="sxs-lookup"><span data-stu-id="bf3e2-182">Import the new XMLport into the [!INCLUDE[d365fin](includes/d365fin_md.md)] development environment and compile it.</span></span>

## <a name="see-also"></a><span data-ttu-id="bf3e2-183">Se også</span><span class="sxs-lookup"><span data-stu-id="bf3e2-183">See Also</span></span>  
<span data-ttu-id="bf3e2-184">[Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md) </span><span class="sxs-lookup"><span data-stu-id="bf3e2-184">[Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md) </span></span>  
<span data-ttu-id="bf3e2-185">[Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md) </span><span class="sxs-lookup"><span data-stu-id="bf3e2-185">[Export Payments to a Bank File](payables-how-export-payments-bank-file.md) </span></span>  
<span data-ttu-id="bf3e2-186">[Innkreve betalinger med SEPA direct debit](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="bf3e2-186">[Collect Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
[<span data-ttu-id="bf3e2-187">Rammeverket for datautveksling</span><span class="sxs-lookup"><span data-stu-id="bf3e2-187">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)
