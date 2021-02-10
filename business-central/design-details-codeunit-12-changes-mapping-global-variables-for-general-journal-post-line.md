---
title: Endringer i tilordning av globale variabler for bokføring i codeunit 12
description: I tidligere versjoner ble codeunit 12 endret for å bidra til å forbedre ytelsen i bokføringen fra finanskladden. Finn ut mer om endringene i de globale variablene.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/28/2020
ms.author: edupont
ms.openlocfilehash: 0fc79ba982e17b9295f0f611ca34b4eb615001f3
ms.sourcegitcommit: a95681db16e81af109b34f8e5d88028c1552c6a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/03/2020
ms.locfileid: "4367762"
---
# <a name="historical-changes-to-codeunit-12-mapping-global-variables-for-general-journal-post-line"></a>Historiske endringer i Codeunit 12: Tilordne globale variabler for Finanskladd – bokfør linje

Følgende endringer er implementert i versjoner av [!INCLUDE [navnow_md](includes/navnow_md.md)].  

|**Microsoft Dynamics NAV 2009 R2**|**Microsoft Dynamics NAV 2013 R2**|**Merknad**|  
|----------------------------------------|----------------------------------------|-----------------|  
|GLSetup@1009 : Record 98;|GLSetup@1009 : Record 98;|Uendret|  
|SalesSetup@1010 : Record 311;||Endret til lokal|  
|PurchSetup@1011 : Record 312;||Endret til lokal|  
|AccountingPeriod@1012 : Record 50;||Endret til lokal|  
|GLAcc@1013 : Record 15;||Endret til lokal|  
|GLEntry@1014 : Record 17;|GlobalGLEntry@1014 : Record 17;|Nytt navn|  
|GLEntryTmp@1015 : TEMPORARY Record 17;|TempGLEntryBuf@1010 : TEMPORARY Record 17;|Nytt navn|  
|TempGLEntryVAT@1016 : TEMPORARY Record 17;|TempGLEntryVAT@1016 : TEMPORARY Record 17;|Uendret|  
|OrigGLEntry@1017 : Record 17;||Slettet|  
|VATPostingSetup@1019 : Record 325;||Endret til lokal|  
|Cust@1020 : Record 18;||Endret til lokal|  
|Vend@1021 : Record 23;||Endret til lokal|  
|GenJnlLine@1022 : Record 81;||Endret til lokal|  
|GLReg@1029 : Record 45;|GLReg@1029 : Record 45;|Uendret|  
|CustPostingGr@1030 : Record 92;||Endret til lokal|  
|VendPostingGr@1031 : Record 93;||Endret til lokal|  
|Currency@1032 : Record 4;||Endret til lokal|  
|AddCurrency@1033 : Record 4;|AddCurrency@1033 : Record 4;|Uendret|  
|ApplnCurrency@1034 : Record 4;||Endret til lokal|  
|CurrExchRate@1035 : Record 330;|CurrExchRate@1035 : Record 330;|Uendret|  
|VATEntry@1038 : Record 254;|VATEntry@1038 : Record 254;|Uendret|  
|BankAcc@1039 : Record 270;||Endret til lokal|  
|BankAccLedgEntry@1040 : Record 271;||Endret til lokal|  
|CheckLedgEntry@1041 : Record 272;||Endret til lokal|  
|CheckLedgEntry2@1042 : Record 272;||Endret til lokal|  
|BankAccPostingGr@1043 : Record 277;||Endret til lokal|  
|GenJnlTemplate@1044 : Record 80;||Endret til lokal|  
|TaxJurisdiction@1045 : Record 320;||Endret til lokal|  
|TaxDetail@1046 : Record 322;|TaxDetail@1046 : Record 322;|Uendret|  
|FAGLPostBuf@1047 : TEMPORARY Record 5637;||Endret til lokal|  
|UnrealizedCustLedgEntry@1084 : Record 21;|UnrealizedCustLedgEntry@1084 : Record 21;|Uendret|  
|UnrealizedVendLedgEntry@1085 : Record 25;|UnrealizedVendLedgEntry@1085 : Record 25;|Uendret|  
|GLEntryVATEntryLink@1087 : Record 253;|GLEntryVATEntryLink@1087 : Record 253;|Uendret|  
|TempVATEntry@1088 : TEMPORARY Record 254;|TempVATEntry@1088 : TEMPORARY Record 254;|Uendret|  
|ReversedGLEntryTemp@1089 : TEMPORARY Record 17;||Flyttet til kodeenhet 17|  
|CostAccSetup@1092 : Record 1108;||Endret til lokal|  
|GenJnlCheckLine@1048 : Codeunit 11;|GenJnlCheckLine@1001 : Codeunit 11;|Uendret|  
|ExchAccGLJnlLine@1049 : Codeunit 366;||Endret til lokal|  
|FAJnlPostLine@1050 : Codeunit 5632;||Endret til lokal|  
|SalesTaxCalculate@1051 : Codeunit 398;||Endret til lokal|  
|GenJnlApply@1052 : Codeunit 225;||Endret til lokal|  
|DimMgt@1053 : Codeunit 408;||Endret til lokal|  
|JobPostLine@1028 : Codeunit 1001;||Endret til lokal|  
|TransferGlEntriesToCA@1091 : Codeunit 1105;||Endret til lokal|  
||PaymentToleranceMgt@1002 : Codeunit 426;|Lagt til|  
||AddCurrencyCode@1117 : Code[10];|Lagt til|  
|FiscalYearStartDate@1054 : Date;|FiscalYearStartDate@1011 : Date;|Uendret|  
|NextEntryNo@1055 : Integer;|NextEntryNo@1022 : Integer;|Uendret|  
|BalanceCheckAmount@1056 : Decimal;|BalanceCheckAmount@1056 : Decimal;|Uendret|  
|BalanceCheckAmount2@1057 : Decimal;|BalanceCheckAmount2@1057 : Decimal;|Uendret|  
|BalanceCheckAddCurrAmount@1058 : Decimal;|BalanceCheckAddCurrAmount@1058 : Decimal;|Uendret|  
|BalanceCheckAddCurrAmount2@1059 : Decimal;|BalanceCheckAddCurrAmount2@1059 : Decimal;|Uendret|  
|CurrentBalance@1060 : Decimal;|CurrentBalance@1060 : Decimal;|Uendret|  
|SalesTaxBaseAmount@1061 : Decimal;||Endret til lokal|  
|TotalAddCurrAmount@1062 : Decimal;|TotalAddCurrAmount@1062 : Decimal;|Uendret|  
|TotalAmount@1063 : Decimal;|TotalAmount@1063 : Decimal;|Uendret|  
|UnrealizedRemainingAmountCust@1086 : Decimal;|UnrealizedRemainingAmountCust@1086 : Decimal;|Uendret|  
|UnrealizedRemainingAmountVend@1074 : Decimal;|UnrealizedRemainingAmountVend@1074 : Decimal;|Uendret|  
|NextVATEntryNo@1064 : Integer;|NextVATEntryNo@1064 : Integer;|Uendret|  
|FirstNewVATEntryNo@1065 : Integer;|FirstNewVATEntryNo@1065 : Integer;|Uendret|  
|NextTransactionNo@1066 : Integer;|NextTransactionNo@1066 : Integer;|Uendret|  
|NextConnectionNo@1067 : Integer;|NextConnectionNo@1067 : Integer;|Uendret|  
|InsertedTempGLEntryVAT@1068 : Integer;|InsertedTempGLEntryVAT@1027 : Integer;|Uendret|  
|LastDocNo@1069 : Code[20];|LastDocNo@1023 : Code[20];|Uendret|  
|LastLineNo@1070 : Integer;||Slettet|  
|LastDate@1071 : Date;|LastDate@1021 : Date;|Uendret|  
|LastDocType@1072 : ' ,Payment,Invoice,Credit Memo,Finance Charge Memo,Reminder';|LastDocType@1025 : ' ,Payment,Invoice,Credit Memo,Finance Charge Memo,Reminder';|Uendret|  
|NextCheckEntryNo@1073 : Integer;|NextCheckEntryNo@1028 : Integer;|Uendret|  
|AddCurrGLEntryVATAmt@1075 : Decimal;|AddCurrGLEntryVATAmt@1017 : Decimal;|Uendret|  
|CurrencyDate@1076 : Date;|CurrencyDate@1020 : Date;|Uendret|  
|CurrencyFactor@1077 : Decimal;|CurrencyFactor@1019 : Decimal;|Uendret|  
|UseCurrFactorOnly@1078 : Boolean;|UseCurrFactorOnly@1078 : Boolean;|Uendret|  
|NonAddCurrCodeOccured@1079 : Boolean;|NonAddCurrCodeOccured@1079 : Boolean;|Uendret|  
|FADimAlreadyChecked@1080 : Boolean;|FADimAlreadyChecked@1080 : Boolean;|Uendret|  
|AllApplied@1081 : Boolean;||Endret til lokal|  
|OverrideDimErr@1018 : Boolean;|OverrideDimErr@1018 : Boolean;|Uendret|  
|JobLine@1036 : Boolean;|JobLine@1036 : Boolean;|Uendret|  
|Prepayment@1037 : Boolean;||Slettet|  
|CheckUnrealizedCust@1082 : Boolean;|CheckUnrealizedCust@1082 : Boolean;|Uendret|  
|CheckUnrealizedVend@1083 : Boolean;|CheckUnrealizedVend@1083 : Boolean;|Uendret|  
|GLEntryNo@1090 : Integer;|GLEntryNo@1026 : Integer;|Uendret|  
||GLSetupRead@1015 : Boolean;|Lagt til|  
||AmountRoundingPrecision@1012 : Decimal;|Lagt til|  
||CrCardTransactionEntryNo@1013 : Integer;|Lagt til|  

## <a name="see-also"></a>Se også  
 [Designdetaljer – Endringer i kodeenhet 12: Endringer i bokføringsprosedyrene for finans](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)
