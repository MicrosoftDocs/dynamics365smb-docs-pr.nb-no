---
title: "Designdetaljer – Dimensjonsbehandling for kodeenhet 408 | Microsoft-dokumentasjon"
description: "Dimensjonsbehandling for kodeenhet 408 er et funksjonsbibliotek som håndterer vanlige oppgaver som er knyttet til dimensjoner, for eksempel kopiering fra én tabell til en annen eller fra ett dokument til et annet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 95d4afc18b0be620df2f4b2067a093237c7c4df2
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-codeunit-408-dimension-management"></a><span data-ttu-id="ce801-103">Designdetaljer: Dimensjonsbehandling for kodeenhet 408</span><span class="sxs-lookup"><span data-stu-id="ce801-103">Design Details: Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="ce801-104">Dimensjonsbehandling for kodeenhet 408 er et funksjonsbibliotek som håndterer vanlige oppgaver som er knyttet til dimensjoner, for eksempel kopiering fra én tabell til en annen eller fra ett dokument til et annet.</span><span class="sxs-lookup"><span data-stu-id="ce801-104">Codeunit 408 Dimension Management is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span> <span data-ttu-id="ce801-105">Dette emnet viser funksjonene som er endret i Microsoft Dynamics NAV 2013 R2, og angir hva som må gjøres med funksjonene.</span><span class="sxs-lookup"><span data-stu-id="ce801-105">This topic lists the functions that are modified in Microsoft Dynamics NAV 2013 R2 and specifies what has to be done to the functions.</span></span> <span data-ttu-id="ce801-106">Mange funksjoner blir slettet fordi det er ikke nødvendig å kopiere mellom dimensjonstabeller.</span><span class="sxs-lookup"><span data-stu-id="ce801-106">Many functions are deleted because there is no need for copying between dimension tables.</span></span>  

## <a name="modified-functions"></a><span data-ttu-id="ce801-107">Endrede funksjoner</span><span class="sxs-lookup"><span data-stu-id="ce801-107">Modified Functions</span></span>  

|<span data-ttu-id="ce801-108">Funksjonsnavn</span><span class="sxs-lookup"><span data-stu-id="ce801-108">Function Name</span></span>|<span data-ttu-id="ce801-109">Endringsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="ce801-109">Modification Description</span></span>|  
|-------------------|------------------------------|  
|<span data-ttu-id="ce801-110">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="ce801-110">CheckDimSetIDComb</span></span>|<span data-ttu-id="ce801-111">Ny funksjon som erstatter de andre kontrollfunksjonene og bruker en dimensjonssett-ID som argument i stedet for en dimensjonstabell.</span><span class="sxs-lookup"><span data-stu-id="ce801-111">New function that substitutes the other check functions and takes a Dimension Set ID as an argument instead of a dimension table.</span></span>|  
|<span data-ttu-id="ce801-112">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="ce801-112">CheckDimSetIDComb</span></span><br /><br /> <span data-ttu-id="ce801-113">CheckDocDimComb</span><span class="sxs-lookup"><span data-stu-id="ce801-113">CheckDocDimComb</span></span><br /><br /> <span data-ttu-id="ce801-114">CheckServContractDimComb</span><span class="sxs-lookup"><span data-stu-id="ce801-114">CheckServContractDimComb</span></span><br /><br /> <span data-ttu-id="ce801-115">CheckDimBuffer</span><span class="sxs-lookup"><span data-stu-id="ce801-115">CheckDimBuffer</span></span><br /><br /> <span data-ttu-id="ce801-116">CheckDimComb</span><span class="sxs-lookup"><span data-stu-id="ce801-116">CheckDimComb</span></span><br /><br /> <span data-ttu-id="ce801-117">CheckDimValueComb</span><span class="sxs-lookup"><span data-stu-id="ce801-117">CheckDimValueComb</span></span>|<span data-ttu-id="ce801-118">Slett.</span><span class="sxs-lookup"><span data-stu-id="ce801-118">Delete.</span></span> <span data-ttu-id="ce801-119">Alt forbruk må endres til CheckDimSetIDComb.</span><span class="sxs-lookup"><span data-stu-id="ce801-119">All usage should be changed to CheckDimSetIDComb.</span></span>|  
|<span data-ttu-id="ce801-120">GetDefaultDim</span><span class="sxs-lookup"><span data-stu-id="ce801-120">GetDefaultDim</span></span>|<span data-ttu-id="ce801-121">Endre for å returnere en heltallsdimensjons-ID i stedet for et sett med poster.</span><span class="sxs-lookup"><span data-stu-id="ce801-121">Modify to return an integer Dimension Set ID instead of a set of records.</span></span>|  
|<span data-ttu-id="ce801-122">CopyJnlLineDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="ce801-122">CopyJnlLineDimToICJnlDim</span></span><br /><br /> <span data-ttu-id="ce801-123">CopyICJnlDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ce801-123">CopyICJnlDimToJnlLineDim</span></span><br /><br /> <span data-ttu-id="ce801-124">CopyDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-124">CopyDocDimtoICDocDim</span></span><br /><br /> <span data-ttu-id="ce801-125">CopyICDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-125">CopyICDocDimtoICDocDim</span></span>|<span data-ttu-id="ce801-126">Endre slik at den fungerer med DimSetID -> ICJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ce801-126">Modify to work with DimSetID -> ICJnlLineDim</span></span>|  

## <a name="deleted-functions"></a><span data-ttu-id="ce801-127">Slettede funksjoner</span><span class="sxs-lookup"><span data-stu-id="ce801-127">Deleted Functions</span></span>  
 <span data-ttu-id="ce801-128">Funksjoner som er slettet fra kodeenhet 408 i forbindelse med funksjonen Dimensjonssettposter, er oppført nedenfor.</span><span class="sxs-lookup"><span data-stu-id="ce801-128">Functions that are deleted from codeunit 408 in connection with the Dimension Set Entries feature are listed below.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="ce801-129">Under oppgraderingen av programkode fra Microsoft Dynamics NAV 2009 eller tidligere versjoner til Microsoft Dynamics NAV 2016 er følgende funksjoner ikke tilgjengelige i Microsoft Dynamics NAV 2016.</span><span class="sxs-lookup"><span data-stu-id="ce801-129">During the upgrade of application code from Microsoft Dynamics NAV 2009 or earlier versions to Microsoft Dynamics NAV 2016, the following functions are not available in Microsoft Dynamics NAV 2016.</span></span> <span data-ttu-id="ce801-130">Hvis du har tilpasninger som bruker en eller flere av funksjonene, må du oppgradere koden i henhold til dette.</span><span class="sxs-lookup"><span data-stu-id="ce801-130">If you have customizations that use one or more of the functions, you must upgrade that code accordingly.</span></span>

 <span data-ttu-id="ce801-131">InsertJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ce801-131">InsertJnlLineDim</span></span>  

 <span data-ttu-id="ce801-132">UpdateJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="ce801-132">UpdateJnlLineDefaultDim</span></span>  

 <span data-ttu-id="ce801-133">GetJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="ce801-133">GetJnlLineDefaultDim</span></span>  

 <span data-ttu-id="ce801-134">GetPreviousDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="ce801-134">GetPreviousDocDefaultDim</span></span>  

 <span data-ttu-id="ce801-135">GetPreviousProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="ce801-135">GetPreviousProdDocDefaultDim</span></span>  

 <span data-ttu-id="ce801-136">InsertDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-136">InsertDocDim</span></span>  

 <span data-ttu-id="ce801-137">UpdateDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="ce801-137">UpdateDocDefaultDim</span></span>  

 <span data-ttu-id="ce801-138">ExtractDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="ce801-138">ExtractDocDefaultDim</span></span>  

 <span data-ttu-id="ce801-139">InsertProdDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-139">InsertProdDocDim</span></span>  

 <span data-ttu-id="ce801-140">UpdateProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="ce801-140">UpdateProdDocDefaultDim</span></span>  

 <span data-ttu-id="ce801-141">InsertServContractDim</span><span class="sxs-lookup"><span data-stu-id="ce801-141">InsertServContractDim</span></span>  

 <span data-ttu-id="ce801-142">UpdateServcontractDim</span><span class="sxs-lookup"><span data-stu-id="ce801-142">UpdateServcontractDim</span></span>  

 <span data-ttu-id="ce801-143">UpdateDefaultDimNewDimValue</span><span class="sxs-lookup"><span data-stu-id="ce801-143">UpdateDefaultDimNewDimValue</span></span>  

 <span data-ttu-id="ce801-144">GetDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-144">GetDocDim</span></span>  

 <span data-ttu-id="ce801-145">GetProdDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-145">GetProdDocDim</span></span>  

 <span data-ttu-id="ce801-146">TypeToTableID1</span><span class="sxs-lookup"><span data-stu-id="ce801-146">TypeToTableID1</span></span>  

 <span data-ttu-id="ce801-147">TypeToTableID2</span><span class="sxs-lookup"><span data-stu-id="ce801-147">TypeToTableID2</span></span>  

 <span data-ttu-id="ce801-148">TypeToTableID3</span><span class="sxs-lookup"><span data-stu-id="ce801-148">TypeToTableID3</span></span>  

 <span data-ttu-id="ce801-149">TypeToTableID4</span><span class="sxs-lookup"><span data-stu-id="ce801-149">TypeToTableID4</span></span>  

 <span data-ttu-id="ce801-150">TypeToTableID5</span><span class="sxs-lookup"><span data-stu-id="ce801-150">TypeToTableID5</span></span>  

 <span data-ttu-id="ce801-151">DeleteJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ce801-151">DeleteJnlLineDim</span></span>  

 <span data-ttu-id="ce801-152">DeleteDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-152">DeleteDocDim</span></span>  

 <span data-ttu-id="ce801-153">DeletePostedDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-153">DeletePostedDocDim</span></span>  

 <span data-ttu-id="ce801-154">DeleteProdDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-154">DeleteProdDocDim</span></span>  

 <span data-ttu-id="ce801-155">DeleteServContractDim</span><span class="sxs-lookup"><span data-stu-id="ce801-155">DeleteServContractDim</span></span>  

 <span data-ttu-id="ce801-156">ShowJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ce801-156">ShowJnlLineDim</span></span>  

 <span data-ttu-id="ce801-157">SaveJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ce801-157">SaveJnlLineDim</span></span>  

 <span data-ttu-id="ce801-158">ShowJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="ce801-158">ShowJnlLineNewDim</span></span>  

 <span data-ttu-id="ce801-159">SaveJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="ce801-159">SaveJnlLineNewDim</span></span>  

 <span data-ttu-id="ce801-160">ShowDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-160">ShowDocDim</span></span>  

 <span data-ttu-id="ce801-161">SaveDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-161">SaveDocDim</span></span>  

 <span data-ttu-id="ce801-162">ShowProdDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-162">ShowProdDocDim</span></span>  

 <span data-ttu-id="ce801-163">SaveProdDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-163">SaveProdDocDim</span></span>  

 <span data-ttu-id="ce801-164">ShowTempDim</span><span class="sxs-lookup"><span data-stu-id="ce801-164">ShowTempDim</span></span>  

 <span data-ttu-id="ce801-165">SaveTempDim</span><span class="sxs-lookup"><span data-stu-id="ce801-165">SaveTempDim</span></span>  

 <span data-ttu-id="ce801-166">ShowTempNewDim</span><span class="sxs-lookup"><span data-stu-id="ce801-166">ShowTempNewDim</span></span>  

 <span data-ttu-id="ce801-167">SaveTempNewDim</span><span class="sxs-lookup"><span data-stu-id="ce801-167">SaveTempNewDim</span></span>  

 <span data-ttu-id="ce801-168">SaveServContractDim</span><span class="sxs-lookup"><span data-stu-id="ce801-168">SaveServContractDim</span></span>  

 <span data-ttu-id="ce801-169">MoveJnlLineDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="ce801-169">MoveJnlLineDimToLedgEntryDim</span></span>  

 <span data-ttu-id="ce801-170">MoveDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-170">MoveDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="ce801-171">MoveOneDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-171">MoveOneDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="ce801-172">MoveLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ce801-172">MoveLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="ce801-173">MoveDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ce801-173">MoveDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="ce801-174">MoveDimBufToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="ce801-174">MoveDimBufToLedgEntryDim</span></span>  

 <span data-ttu-id="ce801-175">MoveDimBufToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-175">MoveDimBufToPostedDocDim</span></span>  

 <span data-ttu-id="ce801-176">MoveDimBufToGLBudgetDim</span><span class="sxs-lookup"><span data-stu-id="ce801-176">MoveDimBufToGLBudgetDim</span></span>  

 <span data-ttu-id="ce801-177">CopyJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ce801-177">CopyJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="ce801-178">CopyLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ce801-178">CopyLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="ce801-179">CopyDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-179">CopyDocDimToDocDim</span></span>  

 <span data-ttu-id="ce801-180">CopyPostedDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-180">CopyPostedDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="ce801-181">CopyDocDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ce801-181">CopyDocDimToJnlLineDim</span></span>  

 <span data-ttu-id="ce801-182">CopyDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ce801-182">CopyDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="ce801-183">CopyDimBufToDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-183">CopyDimBufToDocDim</span></span>  

 <span data-ttu-id="ce801-184">CopySCDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-184">CopySCDimToDocDim</span></span>  

 <span data-ttu-id="ce801-185">MoveDocDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="ce801-185">MoveDocDimToLedgEntryDim</span></span>  

 <span data-ttu-id="ce801-186">MoveDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-186">MoveDocDimToDocDim</span></span>  

 <span data-ttu-id="ce801-187">MoveDocDimArchvToDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-187">MoveDocDimArchvToDocDim</span></span>  

 <span data-ttu-id="ce801-188">MoveLedgEntryDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-188">MoveLedgEntryDimToDocDim</span></span>  

 <span data-ttu-id="ce801-189">MoveProdDocDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-189">MoveProdDocDimToProdDocDim</span></span>  

 <span data-ttu-id="ce801-190">MoveJnlLineDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-190">MoveJnlLineDimToProdDocDim</span></span>  

 <span data-ttu-id="ce801-191">MoveJnlLineDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-191">MoveJnlLineDimToDocDim</span></span>  

 <span data-ttu-id="ce801-192">MoveJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="ce801-192">MoveJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="ce801-193">CopyLedgEntryDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="ce801-193">CopyLedgEntryDimToLedgEntryDim</span></span>  

 <span data-ttu-id="ce801-194">MoveTempFromDimToTempToDim</span><span class="sxs-lookup"><span data-stu-id="ce801-194">MoveTempFromDimToTempToDim</span></span>  

 <span data-ttu-id="ce801-195">TransferTempToDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="ce801-195">TransferTempToDimToDocDim</span></span>  

 <span data-ttu-id="ce801-196">MoveJnlLineDimToBuf</span><span class="sxs-lookup"><span data-stu-id="ce801-196">MoveJnlLineDimToBuf</span></span>  

 <span data-ttu-id="ce801-197">CopyICJnlDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="ce801-197">CopyICJnlDimToICJnlDim</span></span>  

 <span data-ttu-id="ce801-198">TestDimValue</span><span class="sxs-lookup"><span data-stu-id="ce801-198">TestDimValue</span></span>  

 <span data-ttu-id="ce801-199">TestNewDimValue</span><span class="sxs-lookup"><span data-stu-id="ce801-199">TestNewDimValue</span></span>  

 <span data-ttu-id="ce801-200">MoveDimBufToItemBudgetDim.</span><span class="sxs-lookup"><span data-stu-id="ce801-200">MoveDimBufToItemBudgetDim.</span></span> <span data-ttu-id="ce801-201">(Slett fordi ItemBudgetDim-tabellen er slettet.)</span><span class="sxs-lookup"><span data-stu-id="ce801-201">(Delete because the ItemBudgetDim Table is deleted.)</span></span>  

 <span data-ttu-id="ce801-202">GetServContractDim</span><span class="sxs-lookup"><span data-stu-id="ce801-202">GetServContractDim</span></span>  

 <span data-ttu-id="ce801-203">MoveTempDimToBuf</span><span class="sxs-lookup"><span data-stu-id="ce801-203">MoveTempDimToBuf</span></span>  

 <span data-ttu-id="ce801-204">UpdateSCInvLineDim</span><span class="sxs-lookup"><span data-stu-id="ce801-204">UpdateSCInvLineDim</span></span>  

 <span data-ttu-id="ce801-205">CopyJnlLineDimToBuffer</span><span class="sxs-lookup"><span data-stu-id="ce801-205">CopyJnlLineDimToBuffer</span></span>  

 <span data-ttu-id="ce801-206">UpdateDocDefaultDim2</span><span class="sxs-lookup"><span data-stu-id="ce801-206">UpdateDocDefaultDim2</span></span>  

## <a name="see-also"></a><span data-ttu-id="ce801-207">Se også</span><span class="sxs-lookup"><span data-stu-id="ce801-207">See Also</span></span>
 <span data-ttu-id="ce801-208">[Designdetaljer: Dimensjonssettposter](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="ce801-208">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="ce801-209">[Designdetaljer: Oversikt over dimensjonssettposter](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="ce801-209">[Design Details: Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 <span data-ttu-id="ce801-210">[Designdetaljer: Søke etter dimensjonskombinasjoner](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="ce801-210">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
 <span data-ttu-id="ce801-211">[Designdetaljer: Tabellstruktur](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="ce801-211">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
 [<span data-ttu-id="ce801-212">Designdetaljer: Kodeeksempler på endrede mønstre i endringer</span><span class="sxs-lookup"><span data-stu-id="ce801-212">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)

