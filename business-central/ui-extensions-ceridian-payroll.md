---
title: Importere lønnsdata ved hjelp av Ceridian lønn-utvidelsen | Microsoft-dokumentasjon
description: Bruk denne utvidelsen til å importere lønnstransaksjoner fra tjenestene Ceridian HR/Payroll (USA) og Ceridian PowerPay (Canada).
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 29dfaaa1cefe2bdc55fd68b1efd752be2c11cbc8
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912356"
---
# <a name="the-ceridian-payroll-extension"></a><span data-ttu-id="243ab-103">Ceridian lønn-utvidelsen</span><span class="sxs-lookup"><span data-stu-id="243ab-103">The Ceridian Payroll Extension</span></span>
<span data-ttu-id="243ab-104">For å ta høyde for lønnsutbetalinger og relaterte transaksjoner, må du importere og bokføre finansielle transaksjoner som er utført av lønnssystemet til Finans.</span><span class="sxs-lookup"><span data-stu-id="243ab-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span>

<span data-ttu-id="243ab-105">Hvis du vil gjøre dette, importerer du først filen som du mottar fra lønnssystemet på siden **Finanskladd**.</span><span class="sxs-lookup"><span data-stu-id="243ab-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** page.</span></span> <span data-ttu-id="243ab-106">Deretter tilordner du eksterne kontoer i lønnsfilen til de relevante finanskontiene.</span><span class="sxs-lookup"><span data-stu-id="243ab-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="243ab-107">Til slutt kan du bokføre lønnstransaksjoner etter kontotilordningen.</span><span class="sxs-lookup"><span data-stu-id="243ab-107">Lastly, you post the payroll transactions according to the account mapping.</span></span> <span data-ttu-id="243ab-108">Hvis du vil ha mer informasjon, kan du se [Importere lønnstransaksjoner](finance-how-import-payroll-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="243ab-108">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

<span data-ttu-id="243ab-109">Ceridian lønn-utvidselen lar deg importere lønnstransaksjoner fra Ceridian HR/Payroll (US) og Ceridian PowerPay (Canada).</span><span class="sxs-lookup"><span data-stu-id="243ab-109">The Ceridian Payroll extension allows you to import payroll transactions from the Ceridian HR/Payroll (US) and Ceridian PowerPay (Canada) services.</span></span>

## <a name="see-also"></a><span data-ttu-id="243ab-110">Se også</span><span class="sxs-lookup"><span data-stu-id="243ab-110">See Also</span></span>
<span data-ttu-id="243ab-111">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="243ab-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="243ab-112">[Finans](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="243ab-112">[Finance](finance.md)  </span></span>  
<span data-ttu-id="243ab-113">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="243ab-113">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
