---
title: Designdetaljer - Kodeeksempler på endrede mønstre i endringer | Microsoft Docs
description: Kodeeksempler viser endrede mønstre i endring og flytting av dimensjonskode for fem ulike scenarier. Det sammenligner kodeeksemplene i tidligere versjoner med kodeeksemplene i Business Central.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-dimension-set-entries
ms.openlocfilehash: d4ed71c8c196ea6beff49f7a40fc1605fe999abd
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303727"
---
# <a name="design-details-code-examples-of-changed-patterns-in-modifications"></a><span data-ttu-id="b8b23-104">Designdetaljer: Kodeeksempler på endrede mønstre i endringer</span><span class="sxs-lookup"><span data-stu-id="b8b23-104">Design Details: Code Examples of Changed Patterns in Modifications</span></span>
<span data-ttu-id="b8b23-105">Dette emnet inneholder kodeeksempler som viser endrede mønstre i endring og flytting av dimensjonskode for fem ulike scenarier.</span><span class="sxs-lookup"><span data-stu-id="b8b23-105">This topic provides code examples to show changed patterns in dimension code modification and migration for five different scenarios.</span></span> <span data-ttu-id="b8b23-106">Det sammenligner kodeeksemplene i tidligere versjoner med kodeeksemplene i Business Central.</span><span class="sxs-lookup"><span data-stu-id="b8b23-106">It compares the code examples in earlier versions to the code examples in Business Central.</span></span>

## <a name="posting-a-journal-line"></a><span data-ttu-id="b8b23-107">Bokføre en kladdelinje</span><span class="sxs-lookup"><span data-stu-id="b8b23-107">Posting a Journal Line</span></span>  
<span data-ttu-id="b8b23-108">Viktige endringer vises slik:</span><span class="sxs-lookup"><span data-stu-id="b8b23-108">Key changes are listed as follows:</span></span>  

- <span data-ttu-id="b8b23-109">Dimensjonstabeller for kladdelinjer blir fjernet.</span><span class="sxs-lookup"><span data-stu-id="b8b23-109">Journal line dimension tables are removed.</span></span>  

- <span data-ttu-id="b8b23-110">En dimensjonssett-ID opprettes i **Dimensjonssett-ID**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b8b23-110">A dimension set ID is created in the **Dimension Set ID** field.</span></span>  

<span data-ttu-id="b8b23-111">**Tidligere versjoner**</span><span class="sxs-lookup"><span data-stu-id="b8b23-111">**Earlier Versions**</span></span>  

```  
ResJnlLine."Qty. per Unit of Measure" :=   
  SalesLine."Qty. per Unit of Measure";  

TempJnlLineDim.DELETEALL;  
TempDocDim.RESET;  
TempDocDim.SETRANGE(  
  "Table ID",DATABASE::"Sales Line");  
TempDocDim.SETRANGE(  
  "Line No.",SalesLine."Line No.");  
DimMgt.CopyDocDimToJnlLineDim(  
  TempDocDim,TempJnlLineDim);  
ResJnlPostLine.RunWithCheck(  
  ResJnlLine,TempJnlLineDim);  

```  

 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  

```  

ResJnlLine."Qty. per Unit of Measure" :=   
  SalesLine."Qty. per Unit of Measure";  

ResJnlLine."Dimension Set ID" :=   
  SalesLine." Dimension Set ID ";  
ResJnlPostLine.Run(ResJnlLine);  

```  

## <a name="posting-a-document"></a><span data-ttu-id="b8b23-112">Bokføre et dokument</span><span class="sxs-lookup"><span data-stu-id="b8b23-112">Posting a Document</span></span>  
 <span data-ttu-id="b8b23-113">Når du bokfører et dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)], trenger du ikke lenger å kopiere dokumentdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="b8b23-113">When you post a document in [!INCLUDE[d365fin](includes/d365fin_md.md)], you no longer have to copy the document dimensions.</span></span>  

 <span data-ttu-id="b8b23-114">**Tidligere versjoner**</span><span class="sxs-lookup"><span data-stu-id="b8b23-114">**Earlier Versions**</span></span>  

```  
DimMgt.MoveOneDocDimToPostedDocDim(  
  TempDocDim,DATABASE::"Sales Line",  
  "Document Type",  
  "No.",  
  SalesShptLine."Line No.",  
  DATABASE::"Sales Shipment Line",  
  SalesShptHeader."No.");  
```  

 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  

```  
SalesShptLine."Dimension Set ID”  
  := SalesLine."Dimension Set ID”  
```  

## <a name="editing-dimensions-from-a-document"></a><span data-ttu-id="b8b23-115">Redigere dimensjoner fra et dokument</span><span class="sxs-lookup"><span data-stu-id="b8b23-115">Editing Dimensions from a Document</span></span>  
 <span data-ttu-id="b8b23-116">Du kan redigere dimensjoner fra et dokument.</span><span class="sxs-lookup"><span data-stu-id="b8b23-116">You can edit dimensions from a document.</span></span> <span data-ttu-id="b8b23-117">Du kan for eksempel redigere en ordrelinje.</span><span class="sxs-lookup"><span data-stu-id="b8b23-117">For example, you can edit a sales order line.</span></span>  

 <span data-ttu-id="b8b23-118">**Tidligere versjoner**</span><span class="sxs-lookup"><span data-stu-id="b8b23-118">**Earlier Versions**</span></span>  

```  
Table 37, function ShowDimensions:  
TESTFIELD("Document No.");  
TESTFIELD("Line No.");  
DocDim.SETRANGE("Table ID",DATABASE::"Sales Line");  
DocDim.SETRANGE("Document Type","Document Type");  
DocDim.SETRANGE("Document No.","Document No.");  
DocDim.SETRANGE("Line No.","Line No.");  
DocDimensions.SETTABLEVIEW(DocDim);  
DocDimensions.RUNMODAL;  
```  

 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  

```  
Table 37, function ShowDimensions:  
"Dimension ID" :=   
  DimSetEntry.EditDimensionSet(  
    "Dimension ID");  
```  

## <a name="showing-dimensions-from-posted-entries"></a><span data-ttu-id="b8b23-119">Vise dimensjoner fra bokførte poster</span><span class="sxs-lookup"><span data-stu-id="b8b23-119">Showing Dimensions from Posted Entries</span></span>  
 <span data-ttu-id="b8b23-120">Du kan vise dimensjoner fra bokførte poster, for eksempel følgeseddellinjer.</span><span class="sxs-lookup"><span data-stu-id="b8b23-120">You can show dimensions from posted entries, such as sales shipment lines.</span></span>  

 <span data-ttu-id="b8b23-121">**Tidligere versjoner**</span><span class="sxs-lookup"><span data-stu-id="b8b23-121">**Earlier Versions**</span></span>  

```  
Table 111, function ShowDimensions:  
TESTFIELD("No.");  
TESTFIELD("Line No.");  
PostedDocDim.SETRANGE(  
  "Table ID",DATABASE::"Sales Shipment Line");  
PostedDocDim.SETRANGE(  
  "Document No.","Document No.");  
PostedDocDim.SETRANGE("Line No.","Line No.");  
PostedDocDimensions.SETTABLEVIEW(PostedDocDim);  
PostedDocDimensions.RUNMODAL;  
```  

 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  

```  
Table 111, function ShowDimensions:  
DimSetEntry.ShowDimensionSet(  
  "Dimension ID");  
```  

## <a name="getting-default-dimensions-for-a-document"></a><span data-ttu-id="b8b23-122">Hente standarddimensjoner for et dokument</span><span class="sxs-lookup"><span data-stu-id="b8b23-122">Getting Default Dimensions for a Document</span></span>  
 <span data-ttu-id="b8b23-123">Du kan hente standarddimensjoner for et dokument, for eksempel en ordrelinje.</span><span class="sxs-lookup"><span data-stu-id="b8b23-123">You can get default dimensions for a document, such as a sales order line.</span></span>  

 <span data-ttu-id="b8b23-124">**Tidligere versjoner**</span><span class="sxs-lookup"><span data-stu-id="b8b23-124">**Earlier Versions**</span></span>  

```  
Table 37, function CreateDim()  
SourceCodeSetup.GET;  
TableID[1] := Type1;  
No[1] := No1;  
TableID[2] := Type2;  
No[2] := No2;  
TableID[3] := Type3;  
No[3] := No3;  
"Shortcut Dimension 1 Code" := '';  
"Shortcut Dimension 2 Code" := '';  
DimMgt.GetPreviousDocDefaultDim(  
  DATABASE::"Sales Header","Document Type",  
  "Document No.",0,  
  DATABASE::Customer,  
  "Shortcut Dimension 1 Code",  
  "Shortcut Dimension 2 Code");  
DimMgt.GetDefaultDim(  
  TableID,No,SourceCodeSetup.Sales,  
  "Shortcut Dimension 1 Code",  
  "Shortcut Dimension 2 Code");  
IF "Line No." <> 0 THEN  
  DimMgt.UpdateDocDefaultDim(  
    DATABASE::"Sales Line","Document Type",  
    "Document No.","Line No.",  
    "Shortcut Dimension 1 Code",  
    "Shortcut Dimension 2 Code");  
```  

 **[!INCLUDE[d365fin](includes/d365fin_md.md)]**  

```  
Table 37, function CreateDim()  
SourceCodeSetup.GET;  
TableID[1] := Type1;  
No[1] := No1;  
TableID[2] := Type2;  
No[2] := No2;  
TableID[3] := Type3;  
No[3] := No3;  
"Shortcut Dimension 1 Code" := '';  
"Shortcut Dimension 2 Code" := '';  
GetSalesHeader;  
"Dimension ID" :=  
  DimMgt.GetDefaultDimID(  
    TableID,No,SourceCodeSetup.Sales,  
    "Shortcut Dimension 1 Code",  
    "Shortcut Dimension 2 Code",  
    SalesHeader."Dimension ID",  
    DATABASE::"Sales Header");

```  

## <a name="see-also"></a><span data-ttu-id="b8b23-125">Se også</span><span class="sxs-lookup"><span data-stu-id="b8b23-125">See Also</span></span>  
<span data-ttu-id="b8b23-126">[Designdetaljer: Dimensjonssettposter](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="b8b23-126">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
[<span data-ttu-id="b8b23-127">Designdetaljer: Tabellstruktur</span><span class="sxs-lookup"><span data-stu-id="b8b23-127">Design Details: Table Structure</span></span>](design-details-table-structure.md)   
