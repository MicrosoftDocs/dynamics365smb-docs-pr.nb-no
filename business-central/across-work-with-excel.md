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
ms.date: 07/03/2020
ms.author: jswymer
ms.openlocfilehash: f782b3ce19baa29d9268f3fdf742d2aa6112957f
ms.sourcegitcommit: 506a433298fc3629231cfa98f64a2d1428094fde
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/03/2020
ms.locfileid: "3534597"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="8efaf-103">Vise og redigere i Excel fra Business Central</span><span class="sxs-lookup"><span data-stu-id="8efaf-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="8efaf-104">Med sider som viser en oversikt over poster i rader og kolonner, som en liste over kunder, ordrer eller fakturaer, kan du også vise poster ved hjelp av Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="8efaf-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="8efaf-105">Du har to alternative måter å gjøre dette på.</span><span class="sxs-lookup"><span data-stu-id="8efaf-105">To do this, you have two options.</span></span> <span data-ttu-id="8efaf-106">Du kan enten velge **Åpne i Excel**-handling eller **Rediger i Excel**-handlingen på siden.</span><span class="sxs-lookup"><span data-stu-id="8efaf-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="8efaf-107">Forskjellene mellom de to handlingen er følgende:</span><span class="sxs-lookup"><span data-stu-id="8efaf-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="8efaf-108">Åpne i Excel</span><span class="sxs-lookup"><span data-stu-id="8efaf-108">Open in Excel</span></span>

- <span data-ttu-id="8efaf-109">Med denne handlingen respekterer Excel filtre på siden som avgrenser postene som vises.</span><span class="sxs-lookup"><span data-stu-id="8efaf-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="8efaf-110">Dette betyr at Excel-arbeidsboken inneholder de samme radene og kolonnene som vises på siden i [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="8efaf-110">This means that the Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="8efaf-111">Du kan gjøre endringer i postene i Excel, men du kan ikke publiserer endringene tilbake til [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="8efaf-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="8efaf-112">Du kan bare lagre endringene til Excel-filen på datamaskinen din.</span><span class="sxs-lookup"><span data-stu-id="8efaf-112">You can only save the changes to Excel file on your computer.</span></span>

- <span data-ttu-id="8efaf-113">Denne handlingen fungerer både i Windows- og macOS.</span><span class="sxs-lookup"><span data-stu-id="8efaf-113">This action works on both on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="8efaf-114">For [!INCLUDE[prodshort](includes/prodshort.md)] lokalt er handlingen **Åpne i Excel** tilgjengelig som standard.</span><span class="sxs-lookup"><span data-stu-id="8efaf-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="8efaf-115">Hvis du konfigurerer [!INCLUDE[prodshort](includes/prodshort.md)] lokalt for redigering av data i Excel, erstattes handlingen **Åpne i Excel** med handlingen **Rediger i Excel**.</span><span class="sxs-lookup"><span data-stu-id="8efaf-115">However, if you set up [!INCLUDE[prodshort](includes/prodshort.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="8efaf-116">Rediger i Excel</span><span class="sxs-lookup"><span data-stu-id="8efaf-116">Edit in Excel</span></span>

- <span data-ttu-id="8efaf-117">Med denne handlingen respekterer Excel de fleste filtre på siden som avgrenser postene som vises.</span><span class="sxs-lookup"><span data-stu-id="8efaf-117">With this action, Excel respects most filters on the page that limit the records shown.</span></span> <span data-ttu-id="8efaf-118">Dette betyr at Excel-arbeidsboken inneholder nesten de samme postene og kolonnene.</span><span class="sxs-lookup"><span data-stu-id="8efaf-118">This means that the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="8efaf-119">Fordelen med **Rediger i Excel**-handlingen er at den lar deg gjøre endringer i poster i Excel og deretter publiserer endringene tilbake til [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="8efaf-119">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="8efaf-120">Den fungerer bare i Windows, ikke i macOS.</span><span class="sxs-lookup"><span data-stu-id="8efaf-120">It only works on Windows; not macOS.</span></span>

- <span data-ttu-id="8efaf-121">Du kan bytte ut selskapet du arbeider med.</span><span class="sxs-lookup"><span data-stu-id="8efaf-121">You can switch the company that your are working with.</span></span> <span data-ttu-id="8efaf-122">Dette gjør du ved å velge ikonet **Alternativer** under ![Alternativer for Excel-tillegg](media/cogwheel.png "Alternativer for Excel-tillegg") i ruten Excel-tillegg, og deretter velger du selskapet fra **Selskap**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8efaf-122">To do this, select the **Options** icon ![Excel add-in options](media/cogwheel.png "Excel add-in options") in the Excel Add-in pane, then select the company from the **Company** field.</span></span>  

    > [!IMPORTANT]
    > <span data-ttu-id="8efaf-123">Når du endrer firmaet, må du sørge for at **Miljø**-feltet ikke er tomt.</span><span class="sxs-lookup"><span data-stu-id="8efaf-123">When changing the company, make sure that the **Environment** field is not empty.</span></span> <span data-ttu-id="8efaf-124">Hvis det er det, setter du det til ett av de tilgjengelige alternativene. Hvis ikke, vil ikke tillegget fungere som det skal.</span><span class="sxs-lookup"><span data-stu-id="8efaf-124">If it is, then set it to one of the available options; otherwise, the add-in will not work correctly.</span></span>  

<span data-ttu-id="8efaf-125">Hvis du gjør endringer i tillegget, må du laste det inn på nytt for å oppdatere tilkoblingen.</span><span class="sxs-lookup"><span data-stu-id="8efaf-125">If you make changes to the add-in, you must reload it in order to update the connection.</span></span> <span data-ttu-id="8efaf-126">Du kan laste inn på nytt ved å bruke menyen for ![tillegg i Excel](media/excel-addin-menu.png "Meny for Excel-tillegg") øverst til høyre for tillegget.</span><span class="sxs-lookup"><span data-stu-id="8efaf-126">To reload, use the ![Excel add-in menu](media/excel-addin-menu.png "Excel add-in menu") menu in the top-right corner of the add-in.</span></span>

> [!NOTE]
> <span data-ttu-id="8efaf-127">For [!INCLUDE[prodshort](includes/prodshort.md)] lokalt er handlingen **Rediger i Excel** bare tilgjengelig hvis Excel-tillegget er konfigurert av systemansvarlig, og den er bare tilgjengelig for webklienten.</span><span class="sxs-lookup"><span data-stu-id="8efaf-127">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator, and only available for the Web client.</span></span> <span data-ttu-id="8efaf-128">For administratorer, hvis du vil vite hvordan du installerer Excel-tilleggskomponenten, se [Definere Excel-tillegget for redigering av Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="8efaf-128">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="8efaf-129">Se forskjellene mellom alternativene</span><span class="sxs-lookup"><span data-stu-id="8efaf-129">See the differences between the options</span></span>
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="8efaf-130">Se relatert opplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="8efaf-130">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="8efaf-131">Se også</span><span class="sxs-lookup"><span data-stu-id="8efaf-131">See Also</span></span>

[<span data-ttu-id="8efaf-132">Arbeide med Business Central</span><span class="sxs-lookup"><span data-stu-id="8efaf-132">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="8efaf-133">Forbedringer i Excel-integrasjon i 2019 Release Wave 2</span><span class="sxs-lookup"><span data-stu-id="8efaf-133">Enhancements to Excel integration in 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  
