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
ms.date: 01/09/2019
ms.author: bholtorf
ms.openlocfilehash: ac68f8a4d67224ad55b1c34ff9b2e4ffa2c372aa
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802842"
---
# <a name="the-quickbooks-payroll-file-import-extension"></a><span data-ttu-id="35ba8-103">Utvidelsen QuickBooks Payroll-filimport</span><span class="sxs-lookup"><span data-stu-id="35ba8-103">The QuickBooks Payroll File Import Extension</span></span>
<span data-ttu-id="35ba8-104">Bruk QuickBooks Payroll-filimportutvidelsen til å importere lønnstransaksjoner fra QuickBooks til finanskonti i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="35ba8-104">Use the QuickBooks Payroll File Import extension to import payroll transactions from QuickBooks to general ledger accounts in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="35ba8-105">Dette er for eksempel nyttig når du går fra QuickBooks til [!INCLUDE[d365fin](includes/d365fin_md.md)], eller hvis outsourcer lønn, men også vil holde oversikt over den i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="35ba8-105">For example, this is useful when you are transitioning from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)], or if you outsource your payroll but also want to keep track of it in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="steps-to-import-payroll-data"></a><span data-ttu-id="35ba8-106">Trinn for å importere lønnsdata</span><span class="sxs-lookup"><span data-stu-id="35ba8-106">Steps to Import Payroll Data</span></span>
<span data-ttu-id="35ba8-107">Det første trinnet for deg, eller kanskje regnskapsføreren, er å bruke eksportfunksjonene i QuickBooks til å eksportere lønnsdata til en .IIF-fil.</span><span class="sxs-lookup"><span data-stu-id="35ba8-107">The first step is for you, or maybe your accountant, to use the export features in QuickBooks to export the payroll data to an .IIF file.</span></span> <span data-ttu-id="35ba8-108">Det andre trinnet er å åpne siden **Finanskladder** i [!INCLUDE[d365fin](includes/d365fin_md.md)] og bruke **Importer lønnstransaksjoner**-handling til å importere filen.</span><span class="sxs-lookup"><span data-stu-id="35ba8-108">The second step is to open the **General Journals** page in [!INCLUDE[d365fin](includes/d365fin_md.md)] and use the **Import Payroll Transactions** action to import the file.</span></span> <span data-ttu-id="35ba8-109">I løpet av importprosessen tilordner du finanskontiene fra QuickBooks til tilsvarende finanskonti i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="35ba8-109">During the import process you map the general ledger accounts from QuickBooks to corresponding accounts in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="35ba8-110">Det siste trinnet er å bokføre lønnstransaksjonene i [!INCLUDE[d365fin](includes/d365fin_md.md)] etter kontotilordningen.</span><span class="sxs-lookup"><span data-stu-id="35ba8-110">The final step is to post the payroll transactions in [!INCLUDE[d365fin](includes/d365fin_md.md)] according to the account mapping.</span></span> 

<span data-ttu-id="35ba8-111">Hvis du vil ha mer informasjon, kan du se [Importere lønnstransaksjoner](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="35ba8-111">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="35ba8-112">Se også</span><span class="sxs-lookup"><span data-stu-id="35ba8-112">See Also</span></span>
<span data-ttu-id="35ba8-113">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="35ba8-113">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="35ba8-114">[Finans](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="35ba8-114">[Finance](finance.md)  </span></span>  
<span data-ttu-id="35ba8-115">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="35ba8-115">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>