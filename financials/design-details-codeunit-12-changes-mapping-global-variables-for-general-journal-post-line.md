---
title: "Designdetaljer – Kodeenhet 12: Endringer i tilordning av globale variabler for Finanskladd – bokfør linje | Microsoft-dokumentasjon"
description: "Følgende endringer er implementert i denne versjonen av Finance and Operations, Business edition."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d1199adb2912d88c545cabcc84d5c9bf27b0892a
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---
# <a name="codeunit-12-changes-mapping-global-variables-for-general-journal-post-line"></a>Endringer i kodeenhet 12: Tilordne globale variabler for Finanskladd – bokfør linje
Følgende endringer er implementert i denne versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)].  

|**Microsoft Dynamics NAV 2009 R2**|**Microsoft Dynamics NAV 2013 R2**|**Merknad**|  
|----------------------------------------|----------------------------------------|-----------------|  
|GLSetup@1009 : Post 98;|GLSetup@1009 : Post 98;|Uendret|  
|SalesSetup@1010 : Post 311;||Endret til lokal|  
|PurchSetup@1011 : Post 312;||Endret til lokal|  
|AccountingPeriod@1012 : Post 50;||Endret til lokal|  
|GLAcc@1013 : Post 15;||Endret til lokal|  
|GLEntry@1014 : Post 17;|GlobalGLEntry@1014 : Post 17;|Nytt navn|  
|GLEntryTmp@1015 : MIDLERTIDIG post 17;|TempGLEntryBuf@1010 : MIDLERTIDIG post 17;|Nytt navn|  
|TempGLEntryVAT@1016 : MIDLERTIDIG post 17;|TempGLEntryVAT@1016 : MIDLERTIDIG post 17;|Uendret|  
|OrigGLEntry@1017 : Post 17;||Slettet|  
|VATPostingSetup@1019 : Post 325;||Endret til lokal|  
|Cust@1020 : Post 18;||Endret til lokal|  
|Vend@1021 : Post 23;||Endret til lokal|  
|GenJnlLine@1022 : Post 81;||Endret til lokal|  
|GLReg@1029 : Post 45;|GLReg@1029 : Post 45;|Uendret|  
|CustPostingGr@1030 : Post 92;||Endret til lokal|  
|VendPostingGr@1031 : Post 93;||Endret til lokal|  
|Currency@1032 : Post 4;||Endret til lokal|  
|AddCurrency@1033 : Post 4;|AddCurrency@1033 : Post 4;|Uendret|  
|ApplnCurrency@1034 : Post 4;||Endret til lokal|  
|CurrExchRate@1035 : Post 330;|CurrExchRate@1035 : Post 330;|Uendret|  
|VATEntry@1038 : Post 254;|VATEntry@1038 : Post 254;|Uendret|  
|BankAcc@1039 : Post 270;||Endret til lokal|  
|BankAccLedgEntry@1040 : Post 271;||Endret til lokal|  
|CheckLedgEntry@1041 : Post 272;||Endret til lokal|  
|CheckLedgEntry2@1042 : Post 272;||Endret til lokal|  
|BankAccPostingGr@1043 : Post 277;||Endret til lokal|  
|GenJnlTemplate@1044 : Post 80;||Endret til lokal|  
|TaxJurisdiction@1045 : Post 320;||Endret til lokal|  
|TaxDetail@1046 : Post 322;|TaxDetail@1046 : Post 322;|Uendret|  
|FAGLPostBuf@1047 : MIDLERTIDIG post 5637;||Endret til lokal|  
|UnrealizedCustLedgEntry@1084 : Post 21;|UnrealizedCustLedgEntry@1084 : Post 21;|Uendret|  
|UnrealizedVendLedgEntry@1085 : Post 25;|UnrealizedVendLedgEntry@1085 : Post 25;|Uendret|  
|GLEntryVATEntryLink@1087 : Post 253;|GLEntryVATEntryLink@1087 : Post 253;|Uendret|  
|TempVATEntry@1088 : MIDLERTIDIG post 254;|TempVATEntry@1088 : MIDLERTIDIG post 254;|Uendret|  
|ReversedGLEntryTemp@1089 : MIDLERTIDIG post 17;||Flyttet til kodeenhet 17|  
|CostAccSetup@1092 : Post 1108;||Endret til lokal|  
|GenJnlCheckLine@1048 : Kodeenhet 11;|GenJnlCheckLine@1001 : Kodeenhet 11;|Uendret|  
|ExchAccGLJnlLine@1049 : Kodeenhet 366;||Endret til lokal|  
|FAJnlPostLine@1050 : Kodeenhet 5632;||Endret til lokal|  
|SalesTaxCalculate@1051 : Kodeenhet 398;||Endret til lokal|  
|GenJnlApply@1052 : Kodeenhet 225;||Endret til lokal|  
|DimMgt@1053 : Kodeenhet 408;||Endret til lokal|  
|JobPostLine@1028 : Kodeenhet 1001;||Endret til lokal|  
|TransferGlEntriesToCA@1091 : Kodeenhet 1105;||Endret til lokal|  
||PaymentToleranceMgt@1002 : Kodeenhet 426;|Lagt til|  
||AddCurrencyCode@1117 : Kode[10];|Lagt til|  
|FiscalYearStartDate@1054 : Dato;|FiscalYearStartDate@1011 : Dato;|Uendret|  
|NextEntryNo@1055 : Heltall;|NextEntryNo@1022 : Heltall;|Uendret|  
|BalanceCheckAmount@1056 : Desimal;|BalanceCheckAmount@1056 : Desimal;|Uendret|  
|BalanceCheckAmount2@1057 : Desimal;|BalanceCheckAmount2@1057 : Desimal;|Uendret|  
|BalanceCheckAddCurrAmount@1058 : Desimal;|BalanceCheckAddCurrAmount@1058 : Desimal;|Uendret|  
|BalanceCheckAddCurrAmount2@1059 : Desimal;|BalanceCheckAddCurrAmount2@1059 : Desimal;|Uendret|  
|CurrentBalance@1060 : Desimal;|CurrentBalance@1060 : Desimal;|Uendret|  
|SalesTaxBaseAmount@1061 : Desimal;||Endret til lokal|  
|TotalAddCurrAmount@1062 : Desimal;|TotalAddCurrAmount@1062 : Desimal;|Uendret|  
|TotalAmount@1063 : Desimal;|TotalAmount@1063 : Desimal;|Uendret|  
|UnrealizedRemainingAmountCust@1086 : Desimal;|UnrealizedRemainingAmountCust@1086 : Desimal;|Uendret|  
|UnrealizedRemainingAmountVend@1074 : Desimal;|UnrealizedRemainingAmountVend@1074 : Desimal;|Uendret|  
|NextVATEntryNo@1064 : Heltall;|NextVATEntryNo@1064 : Heltall;|Uendret|  
|FirstNewVATEntryNo@1065 : Heltall;|FirstNewVATEntryNo@1065 : Heltall;|Uendret|  
|NextTransactionNo@1066 : Heltall;|NextTransactionNo@1066 : Heltall;|Uendret|  
|NextConnectionNo@1067 : Heltall;|NextConnectionNo@1067 : Heltall;|Uendret|  
|InsertedTempGLEntryVAT@1068 : Heltall;|InsertedTempGLEntryVAT@1027 : Heltall;|Uendret|  
|LastDocNo@1069 : Kode[20];|LastDocNo@1023 : Kode[20];|Uendret|  
|LastLineNo@1070 : Heltall;||Slettet|  
|LastDate@1071 : Dato;|LastDate@1021 : Dato;|Uendret|  
|LastDocType@1072: ' ,Betaling,Faktura,Kreditnota,Rentenota,Purring';|LastDocType@1025: ' ,Betaling,Faktura,Kreditnota,Rentenota,Purring';|Uendret|  
|NextCheckEntryNo@1073 : Heltall;|NextCheckEntryNo@1028 : Heltall;|Uendret|  
|AddCurrGLEntryVATAmt@1075 : Desimal;|AddCurrGLEntryVATAmt@1017 : Desimal;|Uendret|  
|CurrencyDate@1076 : Dato;|CurrencyDate@1020 : Dato;|Uendret|  
|CurrencyFactor@1077 : Desimal;|CurrencyFactor@1019 : Desimal;|Uendret|  
|UseCurrFactorOnly@1078 : Boolsk;|UseCurrFactorOnly@1078 : Boolsk;|Uendret|  
|NonAddCurrCodeOccured@1079 : Boolsk;|NonAddCurrCodeOccured@1079 : Boolsk;|Uendret|  
|FADimAlreadyChecked@1080 : Boolsk;|FADimAlreadyChecked@1080 : Boolsk;|Uendret|  
|AllApplied@1081 : Boolsk;||Endret til lokal|  
|OverrideDimErr@1018 : Boolsk;|OverrideDimErr@1018 : Boolsk;|Uendret|  
|JobLine@1036 : Boolsk;|JobLine@1036 : Boolsk;|Uendret|  
|Prepayment@1037 : Boolsk;||Slettet|  
|CheckUnrealizedCust@1082 : Boolsk;|CheckUnrealizedCust@1082 : Boolsk;|Uendret|  
|CheckUnrealizedVend@1083 : Boolsk;|CheckUnrealizedVend@1083 : Boolsk;|Uendret|  
|GLEntryNo@1090 : Heltall;|GLEntryNo@1026 : Heltall;|Uendret|  
||GLSetupRead@1015 : Boolsk;|Lagt til|  
||AmountRoundingPrecision@1012 : Desimal;|Lagt til|  
||CrCardTransactionEntryNo@1013 : Heltall;|Lagt til|  

## <a name="see-also"></a>Se også  
 [Designdetaljer – Endringer i kodeenhet 12: Endringer i bokføringsprosedyrene for finans](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)

