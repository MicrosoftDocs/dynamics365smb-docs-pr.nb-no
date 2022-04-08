---
title: Bruke utvidelsen QuickBooks Payroll-filimport | Microsoft-dokumentasjon
description: Dette emnet beskriver hvordan du bruker utvidelsen til å importere lønn og lønnstransaksjoner fra QuickBooks.
services: project-madeira
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: cd715ac63f9ce7068d5b02fce21e294b7a2231cf
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511496"
---
# <a name="the-quickbooks-payroll-file-import-extension"></a>Utvidelsen QuickBooks Payroll-filimport
Bruk QuickBooks Payroll-filimportutvidelsen til å importere lønnstransaksjoner fra QuickBooks til finanskonti i [!INCLUDE[prod_short](includes/prod_short.md)]. Dette er for eksempel nyttig når du går fra QuickBooks til [!INCLUDE[prod_short](includes/prod_short.md)], eller hvis outsourcer lønn, men også vil holde oversikt over den i [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="steps-to-import-payroll-data"></a>Trinn for å importere lønnsdata
Det første trinnet for deg, eller kanskje regnskapsføreren, er å bruke eksportfunksjonene i QuickBooks til å eksportere lønnsdata til en .IIF-fil. Det andre trinnet er å åpne siden **Finanskladder** i [!INCLUDE[prod_short](includes/prod_short.md)] og bruke **Importer lønnstransaksjoner**-handling til å importere filen. I løpet av importprosessen tilordner du finanskontiene fra QuickBooks til tilsvarende finanskonti i [!INCLUDE[prod_short](includes/prod_short.md)]. Det siste trinnet er å bokføre lønnstransaksjonene i [!INCLUDE[prod_short](includes/prod_short.md)] etter kontotilordningen. 

Hvis du vil ha mer informasjon, kan du se [Importere lønnstransaksjoner](finance-how-import-payroll-transactions.md).

## <a name="see-also"></a>Se også
[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av utvidelser](ui-extensions.md)    
[Finans](finance.md)    
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]