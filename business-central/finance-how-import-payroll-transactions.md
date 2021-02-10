---
title: Importere lønnstransaksjoner| Microsoft-dokumentasjon
description: Du administrerer lønn ved å importere og bokføre finanstransaksjoner fra lønnssystemet til Finans ved hjelp av en utvidelse for lønn, for eksempel Ceridian eller Quickbooks.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ca36be547224e0d401a05b63452420b88b0b7d1f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746969"
---
# <a name="import-payroll-transactions"></a><span data-ttu-id="12eb4-103">Importer lønnstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="12eb4-103">Import Payroll Transactions</span></span>
<span data-ttu-id="12eb4-104">For å ta høyde for lønnsutbetalinger og relaterte transaksjoner, må du importere og bokføre finansielle transaksjoner som er utført av lønnssystemet til Finans.</span><span class="sxs-lookup"><span data-stu-id="12eb4-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span> <span data-ttu-id="12eb4-105">Hvis du vil gjøre dette, importerer du først filen som du mottar fra lønnssystemet på siden **Finanskladd**.</span><span class="sxs-lookup"><span data-stu-id="12eb4-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** page.</span></span> <span data-ttu-id="12eb4-106">Deretter tilordner du eksterne kontoer i lønnsfilen til de relevante finanskontiene.</span><span class="sxs-lookup"><span data-stu-id="12eb4-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="12eb4-107">Til slutt kan du bokføre lønnstransaksjoner etter kontotilordningen.</span><span class="sxs-lookup"><span data-stu-id="12eb4-107">Lastly, you post the payroll transactions according to the account mapping.</span></span>

> [!NOTE]  
>   <span data-ttu-id="12eb4-108">Hvis du vil bruke denne funksjonaliteten, må det installeres og aktiveres en utvidelse for import av lønn.</span><span class="sxs-lookup"><span data-stu-id="12eb4-108">To use this functionality, an extension for payroll import must be installed and enabled.</span></span> <span data-ttu-id="12eb4-109">Utvidelsene for Ceridian lønn og Quickbooks Payroll-filimport er forhåndsinstallert i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="12eb4-109">The Ceridian Payroll and the Quickbooks Payroll File Import extensions are pre-installed in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="12eb4-110">Hvis du vil ha mer informasjon, kan du se [Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av utvidelser](ui-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="12eb4-110">For more information, see [Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md).</span></span>

## <a name="to-import-a-payroll-file"></a><span data-ttu-id="12eb4-111">Slik importerer du en lønnsfil</span><span class="sxs-lookup"><span data-stu-id="12eb4-111">To import a payroll file</span></span>
1. <span data-ttu-id="12eb4-112">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finanskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="12eb4-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="12eb4-113">I den aktuelle finanskladden velger du handlingen **Importer lønnstransaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="12eb4-113">In the relevant general journal batch, choose the **Import Payroll Transactions** action.</span></span> <span data-ttu-id="12eb4-114">Det åpnes en assistert oppsettsveiledning.</span><span class="sxs-lookup"><span data-stu-id="12eb4-114">An assisted setup guide opens.</span></span>
3. <span data-ttu-id="12eb4-115">Følg trinnene på siden **Importer lønnstransaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="12eb4-115">Follow the steps on the **Import Payroll Transactions** page.</span></span>

    > [!TIP]  
    >   <span data-ttu-id="12eb4-116">I trinnet om hvordan du tilordner de eksterne lønnspostene til finanskontiene, vil tilordningene du gjør, bli husket neste gang de samme postene importeres.</span><span class="sxs-lookup"><span data-stu-id="12eb4-116">In the step about mapping the external payroll records to your G/L accounts, the mappings that you make will be remembered next time the same records are imported.</span></span> <span data-ttu-id="12eb4-117">Dette vil spare deg tid siden du trenger ikke å fylle ut feltet **Kontonummer** i finanskladden hver gang du har importert gjentakende lønnstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="12eb4-117">This will save you time as you do not have to manually fill in the **Account No.** field in the general journal every time you have imported recurring payroll transactions.</span></span>   

    <span data-ttu-id="12eb4-118">Når du velger **OK**-knappen i den assisterte oppsettsveiledningen, fylles siden **Finanskladd** med linjer som representerer transaksjoner der lønnsfilen inneholder og med de aktuelle kontoene som er forhåndsutfylt i **Finanskonto**-feltene i henhold til tilordninger som du har gjort i veiledningen.</span><span class="sxs-lookup"><span data-stu-id="12eb4-118">When you choose the **OK** button in the assisted setup guide, the **General Journal** page is filled with lines representing the transactions that the payroll file contains and with the relevant accounts prefilled in the **G/L Account** fields according to mappings you made in the guide.</span></span>
4. <span data-ttu-id="12eb4-119">Rediger eller bokfør kladdelinjene som for andre transaksjoner i Finans.</span><span class="sxs-lookup"><span data-stu-id="12eb4-119">Edit or post the journal lines as for any other general ledger transactions.</span></span> <span data-ttu-id="12eb4-120">Hvis du vil ha mer informasjon, kan du se [Bokføre transaksjoner direkte i Finans](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="12eb4-120">For more information, see [Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>   

## <a name="see-also"></a><span data-ttu-id="12eb4-121">Se også</span><span class="sxs-lookup"><span data-stu-id="12eb4-121">See Also</span></span>
[<span data-ttu-id="12eb4-122">Finans</span><span class="sxs-lookup"><span data-stu-id="12eb4-122">Finance</span></span>](finance.md)  
<span data-ttu-id="12eb4-123">[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av utvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="12eb4-123">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="12eb4-124">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="12eb4-124">Working with General Journals</span></span>](ui-work-general-journals.md)  
