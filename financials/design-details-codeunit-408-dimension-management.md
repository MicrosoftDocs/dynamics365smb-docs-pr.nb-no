---
title: "Designdetaljer – Dimensjonsbehandling for kodeenhet 408 | Microsoft-dokumentasjon"
description: "Dimensjonsbehandling for kodeenhet 408 er et funksjonsbibliotek som håndterer vanlige oppgaver som er knyttet til dimensjoner, for eksempel kopiering fra én tabell til en annen eller fra ett dokument til et annet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 32f67c058570f03d4aa1c84d9bb32289b1f07bec
ms.contentlocale: nb-no
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-codeunit-408-dimension-management"></a>Designdetaljer: Dimensjonsbehandling for kodeenhet 408
Dimensjonsbehandling for kodeenhet 408 er et funksjonsbibliotek som håndterer vanlige oppgaver som er knyttet til dimensjoner, for eksempel kopiering fra én tabell til en annen eller fra ett dokument til et annet. Dette emnet viser funksjonene som er endret i Microsoft Dynamics NAV 2013 R2, og angir hva som må gjøres med funksjonene. Mange funksjoner blir slettet fordi det er ikke nødvendig å kopiere mellom dimensjonstabeller.  

## <a name="modified-functions"></a>Endrede funksjoner  

|Funksjonsnavn|Endringsbeskrivelse|  
|-------------------|------------------------------|  
|CheckDimSetIDComb|Ny funksjon som erstatter de andre kontrollfunksjonene og bruker en dimensjonssett-ID som argument i stedet for en dimensjonstabell.|  
|CheckDimSetIDComb<br /><br /> CheckDocDimComb<br /><br /> CheckServContractDimComb<br /><br /> CheckDimBuffer<br /><br /> CheckDimComb<br /><br /> CheckDimValueComb|Slett. Alt forbruk må endres til CheckDimSetIDComb.|  
|GetDefaultDim|Endre for å returnere en heltallsdimensjons-ID i stedet for et sett med poster.|  
|CopyJnlLineDimToICJnlDim<br /><br /> CopyICJnlDimToJnlLineDim<br /><br /> CopyDocDimtoICDocDim<br /><br /> CopyICDocDimtoICDocDim|Endre slik at den fungerer med DimSetID -> ICJnlLineDim|  

## <a name="deleted-functions"></a>Slettede funksjoner  
 Funksjoner som er slettet fra kodeenhet 408 i forbindelse med funksjonen Dimensjonssettposter, er oppført nedenfor.  

> [!CAUTION]  
>  Under oppgraderingen av programkode fra Microsoft Dynamics NAV 2009 eller tidligere versjoner til Microsoft Dynamics NAV 2016 er følgende funksjoner ikke tilgjengelige i Microsoft Dynamics NAV 2016. Hvis du har tilpasninger som bruker en eller flere av funksjonene, må du oppgradere koden i henhold til dette.

 InsertJnlLineDim  

 UpdateJnlLineDefaultDim  

 GetJnlLineDefaultDim  

 GetPreviousDocDefaultDim  

 GetPreviousProdDocDefaultDim  

 InsertDocDim  

 UpdateDocDefaultDim  

 ExtractDocDefaultDim  

 InsertProdDocDim  

 UpdateProdDocDefaultDim  

 InsertServContractDim  

 UpdateServcontractDim  

 UpdateDefaultDimNewDimValue  

 GetDocDim  

 GetProdDocDim  

 TypeToTableID1  

 TypeToTableID2  

 TypeToTableID3  

 TypeToTableID4  

 TypeToTableID5  

 DeleteJnlLineDim  

 DeleteDocDim  

 DeletePostedDocDim  

 DeleteProdDocDim  

 DeleteServContractDim  

 ShowJnlLineDim  

 SaveJnlLineDim  

 ShowJnlLineNewDim  

 SaveJnlLineNewDim  

 ShowDocDim  

 SaveDocDim  

 ShowProdDocDim  

 SaveProdDocDim  

 ShowTempDim  

 SaveTempDim  

 ShowTempNewDim  

 SaveTempNewDim  

 SaveServContractDim  

 MoveJnlLineDimToLedgEntryDim  

 MoveDocDimToPostedDocDim  

 MoveOneDocDimToPostedDocDim  

 MoveLedgEntryDimToJnlLineDim  

 MoveDimBufToJnlLineDim  

 MoveDimBufToLedgEntryDim  

 MoveDimBufToPostedDocDim  

 MoveDimBufToGLBudgetDim  

 CopyJnlLineDimToJnlLineDim  

 CopyLedgEntryDimToJnlLineDim  

 CopyDocDimToDocDim  

 CopyPostedDocDimToPostedDocDim  

 CopyDocDimToJnlLineDim  

 CopyDimBufToJnlLineDim  

 CopyDimBufToDocDim  

 CopySCDimToDocDim  

 MoveDocDimToLedgEntryDim  

 MoveDocDimToDocDim  

 MoveDocDimArchvToDocDim  

 MoveLedgEntryDimToDocDim  

 MoveProdDocDimToProdDocDim  

 MoveJnlLineDimToProdDocDim  

 MoveJnlLineDimToDocDim  

 MoveJnlLineDimToJnlLineDim  

 CopyLedgEntryDimToLedgEntryDim  

 MoveTempFromDimToTempToDim  

 TransferTempToDimToDocDim  

 MoveJnlLineDimToBuf  

 CopyICJnlDimToICJnlDim  

 TestDimValue  

 TestNewDimValue  

 MoveDimBufToItemBudgetDim. (Slett fordi ItemBudgetDim-tabellen er slettet.)  

 GetServContractDim  

 MoveTempDimToBuf  

 UpdateSCInvLineDim  

 CopyJnlLineDimToBuffer  

 UpdateDocDefaultDim2  

## <a name="see-also"></a>Se også
 [Designdetaljer: Dimensjonssettposter](design-details-dimension-set-entries.md)   
 [Designdetaljer: Oversikt over dimensjonssettposter](design-details-dimension-set-entries-overview.md)   
 [Designdetaljer: Søke etter dimensjonskombinasjoner](design-details-searching-for-dimension-combinations.md)   
 [Designdetaljer: Tabellstruktur](design-details-table-structure.md)   
 [Designdetaljer: Kodeeksempler på endrede mønstre i endringer](design-details-code-examples-of-changed-patterns-in-modifications.md)

