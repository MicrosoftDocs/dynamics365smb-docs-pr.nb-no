---
title: 'Designdetaljer – Kodeenhet 12: Endringer i bokføringsprosedyrene for finans | Microsoft-dokumentasjon'
description: Følgende endringer er implementert i denne versjonen av Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 42e3c3da8c9ea32467f2259c7d29d224427535c6
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185783"
---
# <a name="codeunit-12-changes-changes-in-general-journal-post-procedures"></a>Endringer i kodeenhet 12: Endringer i bokføringsprosedyrene for finans
Følgende endringer er implementert i denne versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)].  

|**Microsoft Dynamics NAV 2009 R2**|**Microsoft Dynamics NAV 2013 R2**|**Merknad**|  
|----------------------------------------|----------------------------------------|-----------------|  
|GetGLReg|GetGLReg|Oppdatert|  
|RunWithCheck|RunWithCheck|Oppdatert|  
|RunWithoutCheck|RunWithoutCheck|Oppdatert|  
|Kode|Kode|Oppdatert|  
||PostGenJnlLine|Lagt til|  
||InitAmounts|Lagt til|  
||InitLastDocDate|Lagt til|  
|InitVAT|InitVAT|Oppdatert|  
|PostVAT|PostVAT|Oppdatert|  
|InsertVAT|InsertVAT|Oppdatert|  
|SummarizeVAT|SummarizeVAT|Oppdatert|  
|InsertSummarizedVAT|InsertSummarizedVAT|Oppdatert|  
|PostGLAcc|PostGLAcc|Oppdatert|  
|PostCust|PostCust|Oppdatert|  
|PostVend|PostVend|Oppdatert|  
|PostBankAcc|PostBankAcc|Oppdatert|  
|PostFixedAsset|PostFixedAsset|Oppdatert|  
|PostICPartner|PostICPartner|Oppdatert|  
|InitCodeUnit|StartPosting|Oppdatert|  
||ContinuePosting|Lagt til|  
|FinishCodeunit|FinishPosting|Oppdatert|  
||PostUnrealizedVAT|Lagt til|  
||CheckPostUnrealizedVAT|Lagt til|  
||ExchangeAccounts|Lagt til|  
|InitGLEntry|InitGLEntry|Oppdatert|  
||InitGLEntryVAT|Lagt til|  
||InitGLEntryVATCopy|Lagt til|  
|InsertGLEntry|InsertGLEntry|Oppdatert|  
||CreateGLEntry|Lagt til|  
||CreateGLEntryBalAcc|Lagt til|  
||CreateGLEntryVAT|Lagt til|  
||CreateGLEntryVATCollectAdj|Lagt til|  
||CreateGLEntryFromVATEntry|Lagt til|  
||UpdateCheckAmounts|Lagt til|  
|ApplyCustLedgEntry|ApplyCustLedgEntry|Oppdatert|  
||CalcPmtDiscPossible|Lagt til|  
||CalcPmtTolerancePossible|Lagt til|  
|CalcPmtTolerance|CalcPmtTolerance|Oppdatert|  
|CalcPmtDisc|CalcPmtDisc|Oppdatert|  
|CalcPmtDiscIfAdjVAT|CalcPmtDiscIfAdjVAT|Oppdatert|  
|CalcPmtDiscTolerance|CalcPmtDiscTolerance|Oppdatert|  
||CalcPmtDiscVATBases|Lagt til|  
||CalcPmtDiscVATAmounts|Lagt til|  
||InsertPmtDiscVATForVATEntry|Lagt til|  
||InsertPmtDiscVATForGLEntry|Lagt til|  
|CalcCurrencyApplnRounding|CalcCurrencyApplnRounding|Oppdatert|  
|FindAmtForAppln|FindAmtForAppln|Oppdatert|  
|CalcCurrencyUnrealizedGainLoss|CalcCurrencyUnrealizedGainLoss|Oppdatert|  
|CalcCurrencyRealizedGainLoss|CalcCurrencyRealizedGainLoss|Oppdatert|  
|CalcApplication|CalcApplication|Oppdatert|  
|CalcRemainingPmtDisc|CalcRemainingPmtDisc|Flyttet til kodeenhet 426 Administrasjon av betalingstoleranse|  
|CalcAmtLCYAdjustment|CalcAmtLCYAdjustment|Lagt til|  
|InitNewCVLedgEntry|InitFromGenJnlLine|Flyttet til tabell 383 Buffer for detaljert KL-post|  
|InitOldCVLedgEntry|CopyFromCVLedgEntryBuf|Flyttet til tabell 383 Buffer for detaljert KL-post|  
|InsertDtldCVLedgEntry|InsertDtldCVLedgEntry|Flyttet til tabell 383 Buffer for detaljert KL-post|  
||InitBankAccLedgEntry|Lagt til|  
||InitCheckLedgEntry|Lagt til|  
||InitCustLedgEntry|Lagt til|  
||InitVendLedgEntry|Lagt til|  
||InsertDtldCustLedgEntry|Lagt til|  
||InsertDtldVendLedgEntry|Lagt til|  
|CustUnrealizedVAT|CustUnrealizedVAT|Oppdatert|  
|CustPostApplyCustLedgEntry|CustPostApplyCustLedgEntry|Oppdatert|  
||PrepareTempCustLedgEntry|Lagt til|  
|UnapplyCustLedgEntry|UnapplyCustLedgEntry|Oppdatert|  
|TransferCustLedgEntry|CopyFromGenJnlLine|Flyttet til tabell 21 Kundepost|  
|PostDtldCustLedgEntries|PostDtldCustLedgEntries|Oppdatert|  
||PostDtldCustLedgEntry|Lagt til|  
||PostDtldCustLedgEntryUnapply|Lagt til|  
||GetDtldCustLedgEntryAccNo|Lagt til|  
|ZeroTransNoDtldCustLedgEntries|SetZeroTransNo|Flyttet til tabell 379 Detaljert kundepost|  
|AutoEntrForDtldCustLedgEntries||Refaktorert til PostDtldCustLedgEntryUnapply|  
|CustUpdateDebitCredit|UpdateDebitCredit|Flyttet til tabell 379 Detaljert kundepost|  
|ApplyVendLedgEntry|ApplyVendLedgEntry|Oppdatert|  
||PrepareTempVendLedgEntry|Lagt til|  
|VendPostApplyVendLedgEntry|VendPostApplyVendLedgEntry|Oppdatert|  
|UnapplyVendLedgEntry|UnapplyVendLedgEntry|Oppdatert|  
|TransferVendLedgEntry|CopyFromGenJnlLine|Flyttet til tabell 25 Leverandørpost|  
|PostDtldVendLedgEntries|PostDtldVendLedgEntries|Oppdatert|  
||PostDtldVendLedgEntry|Lagt til|  
||PostDtldVendLedgEntryUnapply|Lagt til|  
||GetDtldVendLedgEntryAccNo|Lagt til|  
||PostDtldCVLedgEntry|Lagt til|  
||PostDtldCustVATAdjustment|Lagt til|  
||PostDtldVendVATAdjustment|Lagt til|  
|ZeroTransNoDtldVendLedgEntries|SetZeroTransNo|Flyttet til tabell 380 Detaljert leverandørpost|  
|AutoEntrForDtldVendLedgEntries||Refaktorert til PostDtldVendLedgEntryUnapply|  
|VendUpdateDebitCredit|UpdateDebitCredit|Flyttet til tabell 380 Detaljert leverandørpost|  
|VendUnrealizedVAT|VendUnrealizedVAT|Oppdatert|  
||PostUnrealVATEntry|Lagt til|  
||PostApply|Lagt til|  
|PostUnrealVATByUnapply|PostUnrealVATByUnapply|Oppdatert|  
||PostUnapply|Lagt til|  
||InsertDtldCustLedgEntryUnapply|Lagt til|  
||InsertDtldVendLedgEntryUnapply|Lagt til|  
||InsertTempVATEntry|Lagt til|  
||ProcessTempVATEntry|Lagt til|  
||UpdateCustLedgEntry|Lagt til|  
||UpdateVendLedgEntry|Lagt til|  
|UpdateCalcInterest|UpdateCalcInterest|Oppdatert|  
|UpdateCalcInterest2|UpdateCalcInterest2|Oppdatert|  
|GLCalcAddCurrency|GLCalcAddCurrency|Oppdatert|  
|HandleAddCurrResidualGLEntry|HandleAddCurrResidualGLEntry|Oppdatert|  
|CalcLCYToAddCurr|CalcLCYToAddCurr|Oppdatert|  
|CalcAddCurrFactor||Slettet|  
|GetCurrencyExchRate|GetCurrencyExchRate|Oppdatert|  
|ExchAmount|ExchangeAmount|Flyttet til tabell 330 Valutakurs|  
|ExchangeAmtLCYToFCY2|ExchangeAmtLCYToFCY2|Oppdatert|  
|CalcAddCurrForUnapplication|CalcAddCurrForUnapplication|Oppdatert|  
|CheckNonAddCurrCodeOccurred|CheckNonAddCurrCodeOccurred|Oppdatert|  
|CheckCalcPmtDisc||Flyttet til kodeenhet 426 Administrasjon av betalingstoleranse|  
|CheckCalcPmtDiscCVCust||Flyttet til kodeenhet 426 Administrasjon av betalingstoleranse|  
|CheckCalcPmtDiscCust||Flyttet til kodeenhet 426 Administrasjon av betalingstoleranse|  
|CheckCalcPmtDiscGenJnlCust||Flyttet til kodeenhet 426 Administrasjon av betalingstoleranse|  
|CheckCalcPmtDiscCVVend||Flyttet til kodeenhet 426 Administrasjon av betalingstoleranse|  
|CheckCalcPmtDiscVend||Flyttet til kodeenhet 426 Administrasjon av betalingstoleranse|  
|CheckCalcPmtDiscGenJnlVend||Flyttet til kodeenhet 426 Administrasjon av betalingstoleranse|  
|Reverse|Reverse|Flyttet til codeunit 17 Finanskladd – bokfør tilbakeført|  
|ReverseCustLedgEntry|ReverseCustLedgEntry|Flyttet til codeunit 17 Finanskladd – bokfør tilbakeført|  
|ReverseVendLedgEntry|ReverseVendLedgEntry|Flyttet til codeunit 17 Finanskladd – bokfør tilbakeført|  
|ReverseBankAccLedgEntry|ReverseBankAccLedgEntry|Flyttet til codeunit 17 Finanskladd – bokfør tilbakeført|  
|ReverseVAT|ReverseVAT|Flyttet til codeunit 17 Finanskladd – bokfør tilbakeført|  
|SetReversalDescription|SetReversalDescription|Flyttet til codeunit 17 Finanskladd – bokfør tilbakeført|  
|ApplyCustLedgEntryByReversal|ApplyCustLedgEntryByReversal|Flyttet til codeunit 17 Finanskladd – bokfør tilbakeført|  
|ApplyVendLedgEntryByReversal|ApplyVendLedgEntryByReversal|Flyttet til codeunit 17 Finanskladd – bokfør tilbakeført|  
|PostPmtDiscountVATByUnapply|PostPmtDiscountVATByUnapply|Flyttet til codeunit 17 Finanskladd – bokfør tilbakeført|  
||CheckDimComb|Lagt til i codeunit 17 Finanskladd – bokfør tilbakeført|  
||CopyCustLedgEntry|Lagt til i codeunit 17 Finanskladd – bokfør tilbakeført|  
||CopyVendLedgEntry|Lagt til i codeunit 17 Finanskladd – bokfør tilbakeført|  
||CopyBankAccLedgEntry|Lagt til i codeunit 17 Finanskladd – bokfør tilbakeført|  
|HandlDtlAddjustment|HandleDtldAdjustment|Oppdatert|  
|CollectAddjustment|CollectAdjustment|Oppdatert|  
|SetOverDimErr|SetOverDimErr|Oppdatert|  
|PostJob|PostJob|Oppdatert|  
|InsertVATEntriesFromTemp|InsertVATEntriesFromTemp|Oppdatert|  
|CaptureOrRefundCreditCardPmnt|CaptureOrRefundCreditCardPmnt|Oppdatert|  
|UpdateDOPaymentTransactEntry|UpdateDOPaymentTransactEntry|Oppdatert|  
|ABSMin|ABSMin|Oppdatert|  
|GetApplnRoundPrecision|GetApplnRoundPrecision|Oppdatert|  
|CheckDimValueForDisposal|CheckDimValueForDisposal|Oppdatert|  
|CalculateCurrentBalance|CalculateCurrentBalance|Oppdatert|  
|IncludeVATAmount||Flyttet til tabell 81 kladdelinje|  
|CalcVATAmountFromVATEntry|CalcVATAmountFromVATEntry|Oppdatert|  
||TotalVATAmountOnJnlLines|Lagt til|  
||SetGLRegReverse|Lagt til|  
||GetGLSetup|Lagt til|  
||ReadGLSetup|Lagt til|  
||CheckSalesExtDocNo|Lagt til|  
||CheckPurchExtDocNo|Lagt til|  
||CheckGLAccDimError|Lagt til|  
||GetCurrency|Lagt til|  
||PostDtldAdjustment|Lagt til|  
||GetNextEntryNo|Lagt til|  
||GetNextTransactionNo|Lagt til|  
||GetNextVATEntryNo|Lagt til|  
||IncrNextVATEntryNo|Lagt til|  
||IsNotPayment|Lagt til|  
||IsTempGLEntryBufEmpty|Lagt til|  
||IsVATAdjustment|Lagt til|  
||IsVATExcluded|Lagt til|  
||UpdateDimensions|Lagt til|  
||UpdateDimensionsFromCustLedgEntry|Lagt til|  
||UpdateDimensionsFromVendLedgEntry|Lagt til|  
||UpdateTotalAmounts|Lagt til|  
||CreateGLEntriesForTotalAmounts|Lagt til|  

## <a name="see-also"></a>Se også  
 [Designdetaljer – Kodeenhet 12: Tilordne globale variabler for Finanskladd – bokfør linje](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)
