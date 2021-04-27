---
title: Bruke utvidelsen QuickBooks Payroll-filimport | Microsoft-dokumentasjon
description: Dette emnet beskriver hvordan du bruker utvidelsen til å importere lønn og lønnstransaksjoner fra QuickBooks.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 838095fe81af36a421a49f19400b0abd5cdce17b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784768"
---
# <a name="the-quickbooks-payroll-file-import-extension"></a><span data-ttu-id="48c95-103">Utvidelsen QuickBooks Payroll-filimport</span><span class="sxs-lookup"><span data-stu-id="48c95-103">The QuickBooks Payroll File Import Extension</span></span>
<span data-ttu-id="48c95-104">Bruk QuickBooks Payroll-filimportutvidelsen til å importere lønnstransaksjoner fra QuickBooks til finanskonti i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="48c95-104">Use the QuickBooks Payroll File Import extension to import payroll transactions from QuickBooks to general ledger accounts in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="48c95-105">Dette er for eksempel nyttig når du går fra QuickBooks til [!INCLUDE[prod_short](includes/prod_short.md)], eller hvis outsourcer lønn, men også vil holde oversikt over den i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="48c95-105">For example, this is useful when you are transitioning from QuickBooks to [!INCLUDE[prod_short](includes/prod_short.md)], or if you outsource your payroll but also want to keep track of it in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="steps-to-import-payroll-data"></a><span data-ttu-id="48c95-106">Trinn for å importere lønnsdata</span><span class="sxs-lookup"><span data-stu-id="48c95-106">Steps to Import Payroll Data</span></span>
<span data-ttu-id="48c95-107">Det første trinnet for deg, eller kanskje regnskapsføreren, er å bruke eksportfunksjonene i QuickBooks til å eksportere lønnsdata til en .IIF-fil.</span><span class="sxs-lookup"><span data-stu-id="48c95-107">The first step is for you, or maybe your accountant, to use the export features in QuickBooks to export the payroll data to an .IIF file.</span></span> <span data-ttu-id="48c95-108">Det andre trinnet er å åpne siden **Finanskladder** i [!INCLUDE[prod_short](includes/prod_short.md)] og bruke **Importer lønnstransaksjoner**-handling til å importere filen.</span><span class="sxs-lookup"><span data-stu-id="48c95-108">The second step is to open the **General Journals** page in [!INCLUDE[prod_short](includes/prod_short.md)] and use the **Import Payroll Transactions** action to import the file.</span></span> <span data-ttu-id="48c95-109">I løpet av importprosessen tilordner du finanskontiene fra QuickBooks til tilsvarende finanskonti i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="48c95-109">During the import process you map the general ledger accounts from QuickBooks to corresponding accounts in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="48c95-110">Det siste trinnet er å bokføre lønnstransaksjonene i [!INCLUDE[prod_short](includes/prod_short.md)] etter kontotilordningen.</span><span class="sxs-lookup"><span data-stu-id="48c95-110">The final step is to post the payroll transactions in [!INCLUDE[prod_short](includes/prod_short.md)] according to the account mapping.</span></span> 

<span data-ttu-id="48c95-111">Hvis du vil ha mer informasjon, kan du se [Importere lønnstransaksjoner](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="48c95-111">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="48c95-112">Se også</span><span class="sxs-lookup"><span data-stu-id="48c95-112">See Also</span></span>
<span data-ttu-id="48c95-113">[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av utvidelser](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="48c95-113">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="48c95-114">[Finans](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="48c95-114">[Finance](finance.md)  </span></span>  
<span data-ttu-id="48c95-115">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="48c95-115">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]