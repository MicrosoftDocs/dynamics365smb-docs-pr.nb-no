---
title: Vise og redigere i Excel fra Business Central | Microsoft-dokumenter
description: Lær om hvordan du åpner sidene i Microsoft Excel fra Business Central for bedre dataanalyser.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 01/13/2020
ms.author: jswymer
ms.openlocfilehash: 9fd5c6c242932d75addcfa5c1811bdd1aff99a94
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/14/2020
ms.locfileid: "2953052"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="c784d-103">Vise og redigere i Excel fra Business Central</span><span class="sxs-lookup"><span data-stu-id="c784d-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="c784d-104">Med sider som viser en oversikt over poster i rader og kolonner, som en liste over kunder, ordrer eller fakturaer, kan du også vise poster ved hjelp av Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="c784d-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="c784d-105">Du har to alternative måter å gjøre dette på.</span><span class="sxs-lookup"><span data-stu-id="c784d-105">To do this, you have two options.</span></span> <span data-ttu-id="c784d-106">Du kan enten velge **Åpne i Excel**-handling eller **Rediger i Excel**-handlingen på siden.</span><span class="sxs-lookup"><span data-stu-id="c784d-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="c784d-107">Forskjellene mellom de to handlingen er følgende:</span><span class="sxs-lookup"><span data-stu-id="c784d-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="c784d-108">Åpne i Excel</span><span class="sxs-lookup"><span data-stu-id="c784d-108">Open in Excel</span></span>

- <span data-ttu-id="c784d-109">Med denne handlingen respekterer Excel filtre på siden som avgrenser postene som vises.</span><span class="sxs-lookup"><span data-stu-id="c784d-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="c784d-110">Dette betyr at Excel-arbeidsboken inneholder de samme radene og kolonnene som vises på siden i [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="c784d-110">This means that the Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="c784d-111">Du kan gjøre endringer i postene i Excel, men du kan ikke publiserer endringene tilbake til [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="c784d-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="c784d-112">Du kan bare lagre endringene til Excel-filen på datamaskinen din.</span><span class="sxs-lookup"><span data-stu-id="c784d-112">You can only save the changes to Excel file on your computer.</span></span>

- <span data-ttu-id="c784d-113">Denne handlingen fungerer både i Windows- og macOS.</span><span class="sxs-lookup"><span data-stu-id="c784d-113">This action works on both on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="c784d-114">For [!INCLUDE[prodshort](includes/prodshort.md)] lokalt er handlingen **Åpne i Excel** tilgjengelig som standard.</span><span class="sxs-lookup"><span data-stu-id="c784d-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="c784d-115">Hvis du konfigurerer [!INCLUDE [prodshort](includes/prodshort.md)] lokalt for redigering av data i Excel, erstattes handlingen **Åpne i Excel** med handlingen **Rediger i Excel**.</span><span class="sxs-lookup"><span data-stu-id="c784d-115">However, if you set up [!INCLUDE [prodshort](includes/prodshort.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="c784d-116">Rediger i Excel</span><span class="sxs-lookup"><span data-stu-id="c784d-116">Edit in Excel</span></span>

- <span data-ttu-id="c784d-117">Med denne handlingen respekterer Excel de fleste filtre på siden som avgrenser postene som vises.</span><span class="sxs-lookup"><span data-stu-id="c784d-117">With this action, Excel respects most filters on the page that limit the records shown.</span></span> <span data-ttu-id="c784d-118">Dette betyr at Excel-arbeidsboken inneholder nesten de samme postene og kolonnene.</span><span class="sxs-lookup"><span data-stu-id="c784d-118">This means that the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="c784d-119">Fordelen med **Rediger i Excel**-handlingen er at den lar deg gjøre endringer i poster i Excel og deretter publiserer endringene tilbake til [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="c784d-119">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="c784d-120">Den fungerer bare i Windows, ikke i macOS.</span><span class="sxs-lookup"><span data-stu-id="c784d-120">It only works on Windows; not macOS.</span></span>

<span data-ttu-id="c784d-121">Dette ble forbedret i 2019 Release Wave 2.</span><span class="sxs-lookup"><span data-stu-id="c784d-121">This was enhanced in 2019 release wave 2.</span></span> <span data-ttu-id="c784d-122">Hvis du vil ha mer informasjon, se [Forbedringer i Excel-integrasjon](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span><span class="sxs-lookup"><span data-stu-id="c784d-122">For more information, see [Enhancements to Excel integration](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span></span>

> [!NOTE]
> <span data-ttu-id="c784d-123">For lokal [!INCLUDE[prodshort](includes/prodshort.md)] er **Rediger i Excel**-handlingen bare tilgjengelig hvis Excel-tillegget er konfigurert av systemansvarlig.</span><span class="sxs-lookup"><span data-stu-id="c784d-123">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator.</span></span> <span data-ttu-id="c784d-124">For administratorer, hvis du vil vite hvordan du installerer Excel-tilleggskomponenten, se [Definere Excel-tillegget for redigering av Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="c784d-124">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

> [!NOTE]
> <span data-ttu-id="c784d-125">For [!INCLUDE[prodshort](includes/prodshort.md)] lokalt er denne funksjonen bare tilgjengelig for webklienten.</span><span class="sxs-lookup"><span data-stu-id="c784d-125">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, this feature is only available for the Web client.</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="c784d-126">Se forskjellene mellom alternativene</span><span class="sxs-lookup"><span data-stu-id="c784d-126">See the differences between the options</span></span>
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learnlearnmodulesconfigure-powerbi-excel-dynamics-365-business-centralindex"></a><span data-ttu-id="c784d-127">Se relatert opplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="c784d-127">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="c784d-128">Se også</span><span class="sxs-lookup"><span data-stu-id="c784d-128">See Also</span></span>
[<span data-ttu-id="c784d-129">Arbeide med Business Central</span><span class="sxs-lookup"><span data-stu-id="c784d-129">Working with Business Central</span></span>](ui-work-product.md)  
