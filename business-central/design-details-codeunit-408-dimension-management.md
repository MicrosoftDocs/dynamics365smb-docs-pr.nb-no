---
title: Designdetaljer – Dimensjonsbehandling for kodeenhet 408 | Microsoft-dokumentasjon
description: Dimensjonsbehandling for kodeenhet 408 er et funksjonsbibliotek som håndterer vanlige oppgaver som er knyttet til dimensjoner, for eksempel kopiering fra én tabell til en annen eller fra ett dokument til et annet.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-dimension-set-entries
ms.openlocfilehash: f725e5baea27b47399a50d041757fde83657673c
ms.sourcegitcommit: 1fa3d33db7bc71e3a27c826308a80ff24a436a72
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/30/2019
ms.locfileid: "1970973"
---
# <a name="design-details-codeunit-408-dimension-management"></a><span data-ttu-id="0ef18-103">Designdetaljer: Dimensjonsbehandling for kodeenhet 408</span><span class="sxs-lookup"><span data-stu-id="0ef18-103">Design Details: Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="0ef18-104">Dimensjonsbehandling for kodeenhet 408 er et funksjonsbibliotek som håndterer vanlige oppgaver som er knyttet til dimensjoner, for eksempel kopiering fra én tabell til en annen eller fra ett dokument til et annet.</span><span class="sxs-lookup"><span data-stu-id="0ef18-104">Codeunit 408 Dimension Management is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span> <span data-ttu-id="0ef18-105">Dette emnet viser funksjonene som er endret i Microsoft Dynamics NAV 2013 R2, og angir hva som må gjøres med funksjonene.</span><span class="sxs-lookup"><span data-stu-id="0ef18-105">This topic lists the functions that are modified in Microsoft Dynamics NAV 2013 R2 and specifies what has to be done to the functions.</span></span> <span data-ttu-id="0ef18-106">Mange funksjoner blir slettet fordi det er ikke nødvendig å kopiere mellom dimensjonstabeller.</span><span class="sxs-lookup"><span data-stu-id="0ef18-106">Many functions are deleted because there is no need for copying between dimension tables.</span></span>  

## <a name="modified-functions"></a><span data-ttu-id="0ef18-107">Endrede funksjoner</span><span class="sxs-lookup"><span data-stu-id="0ef18-107">Modified Functions</span></span>  

|<span data-ttu-id="0ef18-108">Funksjonsnavn</span><span class="sxs-lookup"><span data-stu-id="0ef18-108">Function Name</span></span>|<span data-ttu-id="0ef18-109">Endringsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="0ef18-109">Modification Description</span></span>|  
|-------------------|------------------------------|  
|<span data-ttu-id="0ef18-110">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="0ef18-110">CheckDimSetIDComb</span></span>|<span data-ttu-id="0ef18-111">Ny funksjon som erstatter de andre kontrollfunksjonene og bruker en dimensjonssett-ID som argument i stedet for en dimensjonstabell.</span><span class="sxs-lookup"><span data-stu-id="0ef18-111">New function that substitutes the other check functions and takes a Dimension Set ID as an argument instead of a dimension table.</span></span>|  
|<span data-ttu-id="0ef18-112">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="0ef18-112">CheckDimSetIDComb</span></span><br /><br /> <span data-ttu-id="0ef18-113">CheckDocDimComb</span><span class="sxs-lookup"><span data-stu-id="0ef18-113">CheckDocDimComb</span></span><br /><br /> <span data-ttu-id="0ef18-114">CheckServContractDimComb</span><span class="sxs-lookup"><span data-stu-id="0ef18-114">CheckServContractDimComb</span></span><br /><br /> <span data-ttu-id="0ef18-115">CheckDimBuffer</span><span class="sxs-lookup"><span data-stu-id="0ef18-115">CheckDimBuffer</span></span><br /><br /> <span data-ttu-id="0ef18-116">CheckDimComb</span><span class="sxs-lookup"><span data-stu-id="0ef18-116">CheckDimComb</span></span><br /><br /> <span data-ttu-id="0ef18-117">CheckDimValueComb</span><span class="sxs-lookup"><span data-stu-id="0ef18-117">CheckDimValueComb</span></span>|<span data-ttu-id="0ef18-118">Slett.</span><span class="sxs-lookup"><span data-stu-id="0ef18-118">Delete.</span></span> <span data-ttu-id="0ef18-119">Alt forbruk må endres til CheckDimSetIDComb.</span><span class="sxs-lookup"><span data-stu-id="0ef18-119">All usage should be changed to CheckDimSetIDComb.</span></span>|  
|<span data-ttu-id="0ef18-120">GetDefaultDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-120">GetDefaultDim</span></span>|<span data-ttu-id="0ef18-121">Endre for å returnere en heltallsdimensjons-ID i stedet for et sett med poster.</span><span class="sxs-lookup"><span data-stu-id="0ef18-121">Modify to return an integer Dimension Set ID instead of a set of records.</span></span>|  
|<span data-ttu-id="0ef18-122">CopyJnlLineDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-122">CopyJnlLineDimToICJnlDim</span></span><br /><br /> <span data-ttu-id="0ef18-123">CopyICJnlDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-123">CopyICJnlDimToJnlLineDim</span></span><br /><br /> <span data-ttu-id="0ef18-124">CopyDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-124">CopyDocDimtoICDocDim</span></span><br /><br /> <span data-ttu-id="0ef18-125">CopyICDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-125">CopyICDocDimtoICDocDim</span></span>|<span data-ttu-id="0ef18-126">Endre slik at den fungerer med DimSetID -> ICJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-126">Modify to work with DimSetID -> ICJnlLineDim</span></span>|  

## <a name="deleted-functions"></a><span data-ttu-id="0ef18-127">Slettede funksjoner</span><span class="sxs-lookup"><span data-stu-id="0ef18-127">Deleted Functions</span></span>  
 <span data-ttu-id="0ef18-128">Funksjoner som er slettet fra kodeenhet 408 i forbindelse med funksjonen Dimensjonssettposter, er oppført nedenfor.</span><span class="sxs-lookup"><span data-stu-id="0ef18-128">Functions that are deleted from codeunit 408 in connection with the Dimension Set Entries feature are listed below.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="0ef18-129">Under oppgraderingen av programkode fra Microsoft Dynamics NAV 2009 eller tidligere versjoner til Microsoft Dynamics NAV 2016 er følgende funksjoner ikke tilgjengelige i Microsoft Dynamics NAV 2016.</span><span class="sxs-lookup"><span data-stu-id="0ef18-129">During the upgrade of application code from Microsoft Dynamics NAV 2009 or earlier versions to Microsoft Dynamics NAV 2016, the following functions are not available in Microsoft Dynamics NAV 2016.</span></span> <span data-ttu-id="0ef18-130">Hvis du har tilpasninger som bruker en eller flere av funksjonene, må du oppgradere koden i henhold til dette.</span><span class="sxs-lookup"><span data-stu-id="0ef18-130">If you have customizations that use one or more of the functions, you must upgrade that code accordingly.</span></span>

 <span data-ttu-id="0ef18-131">InsertJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-131">InsertJnlLineDim</span></span>  

 <span data-ttu-id="0ef18-132">UpdateJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-132">UpdateJnlLineDefaultDim</span></span>  

 <span data-ttu-id="0ef18-133">GetJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-133">GetJnlLineDefaultDim</span></span>  

 <span data-ttu-id="0ef18-134">GetPreviousDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-134">GetPreviousDocDefaultDim</span></span>  

 <span data-ttu-id="0ef18-135">GetPreviousProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-135">GetPreviousProdDocDefaultDim</span></span>  

 <span data-ttu-id="0ef18-136">InsertDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-136">InsertDocDim</span></span>  

 <span data-ttu-id="0ef18-137">UpdateDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-137">UpdateDocDefaultDim</span></span>  

 <span data-ttu-id="0ef18-138">ExtractDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-138">ExtractDocDefaultDim</span></span>  

 <span data-ttu-id="0ef18-139">InsertProdDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-139">InsertProdDocDim</span></span>  

 <span data-ttu-id="0ef18-140">UpdateProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-140">UpdateProdDocDefaultDim</span></span>  

 <span data-ttu-id="0ef18-141">InsertServContractDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-141">InsertServContractDim</span></span>  

 <span data-ttu-id="0ef18-142">UpdateServcontractDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-142">UpdateServcontractDim</span></span>  

 <span data-ttu-id="0ef18-143">UpdateDefaultDimNewDimValue</span><span class="sxs-lookup"><span data-stu-id="0ef18-143">UpdateDefaultDimNewDimValue</span></span>  

 <span data-ttu-id="0ef18-144">GetDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-144">GetDocDim</span></span>  

 <span data-ttu-id="0ef18-145">GetProdDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-145">GetProdDocDim</span></span>  

 <span data-ttu-id="0ef18-146">TypeToTableID1</span><span class="sxs-lookup"><span data-stu-id="0ef18-146">TypeToTableID1</span></span>  

 <span data-ttu-id="0ef18-147">TypeToTableID2</span><span class="sxs-lookup"><span data-stu-id="0ef18-147">TypeToTableID2</span></span>  

 <span data-ttu-id="0ef18-148">TypeToTableID3</span><span class="sxs-lookup"><span data-stu-id="0ef18-148">TypeToTableID3</span></span>  

 <span data-ttu-id="0ef18-149">TypeToTableID4</span><span class="sxs-lookup"><span data-stu-id="0ef18-149">TypeToTableID4</span></span>  

 <span data-ttu-id="0ef18-150">TypeToTableID5</span><span class="sxs-lookup"><span data-stu-id="0ef18-150">TypeToTableID5</span></span>  

 <span data-ttu-id="0ef18-151">DeleteJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-151">DeleteJnlLineDim</span></span>  

 <span data-ttu-id="0ef18-152">DeleteDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-152">DeleteDocDim</span></span>  

 <span data-ttu-id="0ef18-153">DeletePostedDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-153">DeletePostedDocDim</span></span>  

 <span data-ttu-id="0ef18-154">DeleteProdDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-154">DeleteProdDocDim</span></span>  

 <span data-ttu-id="0ef18-155">DeleteServContractDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-155">DeleteServContractDim</span></span>  

 <span data-ttu-id="0ef18-156">ShowJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-156">ShowJnlLineDim</span></span>  

 <span data-ttu-id="0ef18-157">SaveJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-157">SaveJnlLineDim</span></span>  

 <span data-ttu-id="0ef18-158">ShowJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-158">ShowJnlLineNewDim</span></span>  

 <span data-ttu-id="0ef18-159">SaveJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-159">SaveJnlLineNewDim</span></span>  

 <span data-ttu-id="0ef18-160">ShowDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-160">ShowDocDim</span></span>  

 <span data-ttu-id="0ef18-161">SaveDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-161">SaveDocDim</span></span>  

 <span data-ttu-id="0ef18-162">ShowProdDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-162">ShowProdDocDim</span></span>  

 <span data-ttu-id="0ef18-163">SaveProdDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-163">SaveProdDocDim</span></span>  

 <span data-ttu-id="0ef18-164">ShowTempDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-164">ShowTempDim</span></span>  

 <span data-ttu-id="0ef18-165">SaveTempDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-165">SaveTempDim</span></span>  

 <span data-ttu-id="0ef18-166">ShowTempNewDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-166">ShowTempNewDim</span></span>  

 <span data-ttu-id="0ef18-167">SaveTempNewDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-167">SaveTempNewDim</span></span>  

 <span data-ttu-id="0ef18-168">SaveServContractDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-168">SaveServContractDim</span></span>  

 <span data-ttu-id="0ef18-169">MoveJnlLineDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-169">MoveJnlLineDimToLedgEntryDim</span></span>  

 <span data-ttu-id="0ef18-170">MoveDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-170">MoveDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="0ef18-171">MoveOneDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-171">MoveOneDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="0ef18-172">MoveLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-172">MoveLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="0ef18-173">MoveDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-173">MoveDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="0ef18-174">MoveDimBufToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-174">MoveDimBufToLedgEntryDim</span></span>  

 <span data-ttu-id="0ef18-175">MoveDimBufToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-175">MoveDimBufToPostedDocDim</span></span>  

 <span data-ttu-id="0ef18-176">MoveDimBufToGLBudgetDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-176">MoveDimBufToGLBudgetDim</span></span>  

 <span data-ttu-id="0ef18-177">CopyJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-177">CopyJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="0ef18-178">CopyLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-178">CopyLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="0ef18-179">CopyDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-179">CopyDocDimToDocDim</span></span>  

 <span data-ttu-id="0ef18-180">CopyPostedDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-180">CopyPostedDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="0ef18-181">CopyDocDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-181">CopyDocDimToJnlLineDim</span></span>  

 <span data-ttu-id="0ef18-182">CopyDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-182">CopyDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="0ef18-183">CopyDimBufToDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-183">CopyDimBufToDocDim</span></span>  

 <span data-ttu-id="0ef18-184">CopySCDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-184">CopySCDimToDocDim</span></span>  

 <span data-ttu-id="0ef18-185">MoveDocDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-185">MoveDocDimToLedgEntryDim</span></span>  

 <span data-ttu-id="0ef18-186">MoveDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-186">MoveDocDimToDocDim</span></span>  

 <span data-ttu-id="0ef18-187">MoveDocDimArchvToDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-187">MoveDocDimArchvToDocDim</span></span>  

 <span data-ttu-id="0ef18-188">MoveLedgEntryDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-188">MoveLedgEntryDimToDocDim</span></span>  

 <span data-ttu-id="0ef18-189">MoveProdDocDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-189">MoveProdDocDimToProdDocDim</span></span>  

 <span data-ttu-id="0ef18-190">MoveJnlLineDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-190">MoveJnlLineDimToProdDocDim</span></span>  

 <span data-ttu-id="0ef18-191">MoveJnlLineDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-191">MoveJnlLineDimToDocDim</span></span>  

 <span data-ttu-id="0ef18-192">MoveJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-192">MoveJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="0ef18-193">CopyLedgEntryDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-193">CopyLedgEntryDimToLedgEntryDim</span></span>  

 <span data-ttu-id="0ef18-194">MoveTempFromDimToTempToDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-194">MoveTempFromDimToTempToDim</span></span>  

 <span data-ttu-id="0ef18-195">TransferTempToDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-195">TransferTempToDimToDocDim</span></span>  

 <span data-ttu-id="0ef18-196">MoveJnlLineDimToBuf</span><span class="sxs-lookup"><span data-stu-id="0ef18-196">MoveJnlLineDimToBuf</span></span>  

 <span data-ttu-id="0ef18-197">CopyICJnlDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-197">CopyICJnlDimToICJnlDim</span></span>  

 <span data-ttu-id="0ef18-198">TestDimValue</span><span class="sxs-lookup"><span data-stu-id="0ef18-198">TestDimValue</span></span>  

 <span data-ttu-id="0ef18-199">TestNewDimValue</span><span class="sxs-lookup"><span data-stu-id="0ef18-199">TestNewDimValue</span></span>  

 <span data-ttu-id="0ef18-200">MoveDimBufToItemBudgetDim.</span><span class="sxs-lookup"><span data-stu-id="0ef18-200">MoveDimBufToItemBudgetDim.</span></span> <span data-ttu-id="0ef18-201">(Slett fordi ItemBudgetDim-tabellen er slettet.)</span><span class="sxs-lookup"><span data-stu-id="0ef18-201">(Delete because the ItemBudgetDim Table is deleted.)</span></span>  

 <span data-ttu-id="0ef18-202">GetServContractDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-202">GetServContractDim</span></span>  

 <span data-ttu-id="0ef18-203">MoveTempDimToBuf</span><span class="sxs-lookup"><span data-stu-id="0ef18-203">MoveTempDimToBuf</span></span>  

 <span data-ttu-id="0ef18-204">UpdateSCInvLineDim</span><span class="sxs-lookup"><span data-stu-id="0ef18-204">UpdateSCInvLineDim</span></span>  

 <span data-ttu-id="0ef18-205">CopyJnlLineDimToBuffer</span><span class="sxs-lookup"><span data-stu-id="0ef18-205">CopyJnlLineDimToBuffer</span></span>  

 <span data-ttu-id="0ef18-206">UpdateDocDefaultDim2</span><span class="sxs-lookup"><span data-stu-id="0ef18-206">UpdateDocDefaultDim2</span></span>  

## <a name="see-also"></a><span data-ttu-id="0ef18-207">Se også</span><span class="sxs-lookup"><span data-stu-id="0ef18-207">See Also</span></span>
 <span data-ttu-id="0ef18-208">[Designdetaljer: Dimensjonssettposter](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="0ef18-208">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="0ef18-209">[Designdetaljer: Oversikt over dimensjonssettposter](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="0ef18-209">[Design Details: Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 <span data-ttu-id="0ef18-210">[Designdetaljer: Søke etter dimensjonskombinasjoner](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="0ef18-210">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
 [<span data-ttu-id="0ef18-211">Designdetaljer: Tabellstruktur</span><span class="sxs-lookup"><span data-stu-id="0ef18-211">Design Details: Table Structure</span></span>](design-details-table-structure.md)   
 
