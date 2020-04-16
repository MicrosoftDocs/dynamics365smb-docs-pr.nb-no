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
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 2c6600ac7fe9f6e0aa44554883209039faabbd99
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187511"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="52c57-103">Vise og redigere i Excel fra Business Central</span><span class="sxs-lookup"><span data-stu-id="52c57-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="52c57-104">Med sider som viser en oversikt over poster i rader og kolonner, som en liste over kunder, ordrer eller fakturaer, kan du også vise poster ved hjelp av Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="52c57-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="52c57-105">Du har to alternative måter å gjøre dette på.</span><span class="sxs-lookup"><span data-stu-id="52c57-105">To do this, you have two options.</span></span> <span data-ttu-id="52c57-106">Du kan enten velge **Åpne i Excel**-handling eller **Rediger i Excel**-handlingen på siden.</span><span class="sxs-lookup"><span data-stu-id="52c57-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="52c57-107">Forskjellene mellom de to handlingen er følgende:</span><span class="sxs-lookup"><span data-stu-id="52c57-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="52c57-108">Åpne i Excel</span><span class="sxs-lookup"><span data-stu-id="52c57-108">Open in Excel</span></span>

- <span data-ttu-id="52c57-109">Med denne handlingen respekterer Excel filtre på siden som avgrenser postene som vises.</span><span class="sxs-lookup"><span data-stu-id="52c57-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="52c57-110">Dette betyr at Excel-arbeidsboken inneholder de samme radene og kolonnene som vises på siden i [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="52c57-110">This means that the Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="52c57-111">Du kan gjøre endringer i postene i Excel, men du kan ikke publiserer endringene tilbake til [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="52c57-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="52c57-112">Du kan bare lagre endringene til Excel-filen på datamaskinen din.</span><span class="sxs-lookup"><span data-stu-id="52c57-112">You can only save the changes to Excel file on your computer.</span></span>

- <span data-ttu-id="52c57-113">Denne handlingen fungerer både i Windows- og macOS.</span><span class="sxs-lookup"><span data-stu-id="52c57-113">This action works on both on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="52c57-114">For [!INCLUDE[prodshort](includes/prodshort.md)] lokalt er handlingen **Åpne i Excel** tilgjengelig som standard.</span><span class="sxs-lookup"><span data-stu-id="52c57-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="52c57-115">Hvis du konfigurerer [!INCLUDE [prodshort](includes/prodshort.md)] lokalt for redigering av data i Excel, erstattes handlingen **Åpne i Excel** med handlingen **Rediger i Excel**.</span><span class="sxs-lookup"><span data-stu-id="52c57-115">However, if you set up [!INCLUDE [prodshort](includes/prodshort.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="52c57-116">Rediger i Excel</span><span class="sxs-lookup"><span data-stu-id="52c57-116">Edit in Excel</span></span>

- <span data-ttu-id="52c57-117">Med denne handlingen respekterer Excel de fleste filtre på siden som avgrenser postene som vises.</span><span class="sxs-lookup"><span data-stu-id="52c57-117">With this action, Excel respects most filters on the page that limit the records shown.</span></span> <span data-ttu-id="52c57-118">Dette betyr at Excel-arbeidsboken inneholder nesten de samme postene og kolonnene.</span><span class="sxs-lookup"><span data-stu-id="52c57-118">This means that the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="52c57-119">Fordelen med **Rediger i Excel**-handlingen er at den lar deg gjøre endringer i poster i Excel og deretter publiserer endringene tilbake til [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="52c57-119">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="52c57-120">Den fungerer bare i Windows, ikke i macOS.</span><span class="sxs-lookup"><span data-stu-id="52c57-120">It only works on Windows; not macOS.</span></span>

- <span data-ttu-id="52c57-121">Du kan bytte ut selskapet du arbeider med.</span><span class="sxs-lookup"><span data-stu-id="52c57-121">You can switch the company that your are working with.</span></span> <span data-ttu-id="52c57-122">Dette gjør du ved å velge ikonet **Alternativer** under ![Alternativer for Excel-tillegg](media/cogwheel.png "Alternativer for Excel-tillegg") i ruten Excel-tillegg, og deretter velger du selskapet fra **Selskap**-feltet.</span><span class="sxs-lookup"><span data-stu-id="52c57-122">To do this, select the **Options** icon ![Excel add-in options](media/cogwheel.png "Excel add-in options") in the Excel Add-in pane, then select the company from the **Company** field.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="52c57-123">Når du endrer firmaet, må du sørge for at **Miljø**-feltet ikke er tomt.</span><span class="sxs-lookup"><span data-stu-id="52c57-123">When changing the company, make sure that the **Environment** field is not empty.</span></span> <span data-ttu-id="52c57-124">Hvis det er det, setter du det til ett av de tilgjengelige alternativene. Hvis ikke, vil ikke tillegget fungere som det skal.</span><span class="sxs-lookup"><span data-stu-id="52c57-124">If it is, then set it to one of the available options; otherwise, the add-in will not work correctly.</span></span>  

<span data-ttu-id="52c57-125">Excel-tillegget ble forbedret i utgivelsesplan 2 i 2019.</span><span class="sxs-lookup"><span data-stu-id="52c57-125">The Excel Add-in was enhanced in 2019 release wave 2.</span></span> <span data-ttu-id="52c57-126">Hvis du vil ha mer informasjon, se [Forbedringer i Excel-integrasjon](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span><span class="sxs-lookup"><span data-stu-id="52c57-126">For more information, see [Enhancements to Excel integration](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span></span>

> [!NOTE]
> <span data-ttu-id="52c57-127">For [!INCLUDE[prodshort](includes/prodshort.md)] lokalt er handlingen **Rediger i Excel** bare tilgjengelig hvis Excel-tillegget er konfigurert av systemansvarlig, og den er bare tilgjengelig for webklienten.</span><span class="sxs-lookup"><span data-stu-id="52c57-127">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator, and only available for the Web client.</span></span> <span data-ttu-id="52c57-128">For administratorer, hvis du vil vite hvordan du installerer Excel-tilleggskomponenten, se [Definere Excel-tillegget for redigering av Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="52c57-128">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span> <span data-ttu-id="52c57-129">For [!INCLUDE[prodshort](includes/prodshort.md)] lokalt.</span><span class="sxs-lookup"><span data-stu-id="52c57-129">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises.</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="52c57-130">Se forskjellene mellom alternativene</span><span class="sxs-lookup"><span data-stu-id="52c57-130">See the differences between the options</span></span>
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="52c57-131">Se relatert opplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="52c57-131">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="52c57-132">Se også</span><span class="sxs-lookup"><span data-stu-id="52c57-132">See Also</span></span>
[<span data-ttu-id="52c57-133">Arbeide med Business Central</span><span class="sxs-lookup"><span data-stu-id="52c57-133">Working with Business Central</span></span>](ui-work-product.md)  
