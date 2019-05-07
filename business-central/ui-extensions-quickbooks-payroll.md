---
title: Bruke utvidelsen QuickBooks Payroll-filimport | Microsoft-dokumentasjon
description: Dette emnet beskriver hvordan du bruker utvidelsen til å importere lønn og lønnstransaksjoner fra QuickBooks.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: c7ac2a17ecc0c2a33ea166968f577ca46e8282ed
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "920538"
---
# <a name="the-quickbooks-payroll-file-import-extension"></a>Utvidelsen QuickBooks Payroll-filimport
Bruk QuickBooks Payroll-filimportutvidelsen til å importere lønnstransaksjoner fra QuickBooks til finanskonti i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dette er for eksempel nyttig når du går fra QuickBooks til [!INCLUDE[d365fin](includes/d365fin_md.md)], eller hvis outsourcer lønn, men også vil holde oversikt over den i [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="steps-to-import-payroll-data"></a>Trinn for å importere lønnsdata
Det første trinnet for deg, eller kanskje regnskapsføreren, er å bruke eksportfunksjonene i QuickBooks til å eksportere lønnsdata til en .IIF-fil. Det andre trinnet er å åpne siden **Finanskladder** i [!INCLUDE[d365fin](includes/d365fin_md.md)] og bruke **Importer lønnstransaksjoner**-handling til å importere filen. I løpet av importprosessen tilordner du finanskontiene fra QuickBooks til tilsvarende finanskonti i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det siste trinnet er å bokføre lønnstransaksjonene i [!INCLUDE[d365fin](includes/d365fin_md.md)] etter kontotilordningen. 

Hvis du vil ha mer informasjon, kan du se [Importere lønnstransaksjoner](finance-how-import-payroll-transactions.md).

## <a name="see-also"></a>Se også
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)    
[Finans](finance.md)    
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
