---
title: Vise og redigere i Excel fra Business Central
description: Lær om hvordan du åpner sidene i Microsoft Excel fra Business Central for bedre dataanalyser.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 7e3abf36444c4701229ffaac7ceade11bb1879cc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786935"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="3a2ce-103">Vise og redigere i Excel fra Business Central</span><span class="sxs-lookup"><span data-stu-id="3a2ce-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="3a2ce-104">Med sider som viser en oversikt over poster i rader og kolonner, som en liste over kunder, ordrer eller fakturaer, kan du også vise poster ved hjelp av Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="3a2ce-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="3a2ce-105">Du har to alternative måter å gjøre dette på.</span><span class="sxs-lookup"><span data-stu-id="3a2ce-105">To do this, you have two options.</span></span> <span data-ttu-id="3a2ce-106">Du kan enten velge **Åpne i Excel**-handling eller **Rediger i Excel**-handlingen på siden.</span><span class="sxs-lookup"><span data-stu-id="3a2ce-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="3a2ce-107">Forskjellene mellom de to handlingen er følgende:</span><span class="sxs-lookup"><span data-stu-id="3a2ce-107">The differences between the two actions are as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="3a2ce-108">Åpne i Excel</span><span class="sxs-lookup"><span data-stu-id="3a2ce-108">Open in Excel</span></span>

- <span data-ttu-id="3a2ce-109">Med denne handlingen respekterer Excel filtre på siden som avgrenser postene som vises.</span><span class="sxs-lookup"><span data-stu-id="3a2ce-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="3a2ce-110">Excel-arbeidsboken inneholder de samme radene og kolonnene som vises på siden i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="3a2ce-110">The Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

- <span data-ttu-id="3a2ce-111">Du kan gjøre endringer i postene i Excel, men du kan ikke publiserer endringene tilbake til [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="3a2ce-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="3a2ce-112">Du kan bare lagre endringene til Excel-filen på datamaskinen din.</span><span class="sxs-lookup"><span data-stu-id="3a2ce-112">You can only save the changes to Excel file on your computer.</span></span>

- <span data-ttu-id="3a2ce-113">Denne handlingen fungerer både i Windows- og macOS.</span><span class="sxs-lookup"><span data-stu-id="3a2ce-113">This action works on both on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="3a2ce-114">For [!INCLUDE[prod_short](includes/prod_short.md)] lokalt er handlingen **Åpne i Excel** tilgjengelig som standard.</span><span class="sxs-lookup"><span data-stu-id="3a2ce-114">For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="3a2ce-115">Hvis du konfigurerer [!INCLUDE[prod_short](includes/prod_short.md)] lokalt for redigering av data i Excel, erstattes handlingen **Åpne i Excel** med handlingen **Rediger i Excel**.</span><span class="sxs-lookup"><span data-stu-id="3a2ce-115">However, if you set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="3a2ce-116">Rediger i Excel</span><span class="sxs-lookup"><span data-stu-id="3a2ce-116">Edit in Excel</span></span>

- <span data-ttu-id="3a2ce-117">Med denne handlingen respekterer Excel de fleste filtre på siden som begrenser postene som vises, slik at Excel-arbeidsboken vil inneholde nesten de samme postene og kolonnene.</span><span class="sxs-lookup"><span data-stu-id="3a2ce-117">With this action, Excel respects most filters on the page that limit the records shown, so the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="3a2ce-118">Fordelen med **Rediger i Excel**-handlingen er at den lar deg gjøre endringer i poster i Excel og deretter publiserer endringene tilbake til [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="3a2ce-118">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

- <span data-ttu-id="3a2ce-119">Den fungerer bare i Windows, ikke i macOS.</span><span class="sxs-lookup"><span data-stu-id="3a2ce-119">It only works on Windows; not macOS.</span></span>

- <span data-ttu-id="3a2ce-120">Du kan bytte ut selskapet du arbeider med.</span><span class="sxs-lookup"><span data-stu-id="3a2ce-120">You can switch the company that you are working with.</span></span> <span data-ttu-id="3a2ce-121">Du bytter selskap ved å velge ikonet **Alternativer** under ![Alternativer for Excel-tillegg](media/cogwheel.png "Alternativer for Excel-tillegg") i ruten Excel-tillegg, og deretter velger du selskapet fra **Selskap**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3a2ce-121">To switch company, select the **Options** icon ![Excel add-in options](media/cogwheel.png "Excel add-in options") in the Excel Add-in pane, then select the company from the **Company** field.</span></span>  

    > [!IMPORTANT]
    > <span data-ttu-id="3a2ce-122">Når du endrer firmaet, må du sørge for at **Miljø**-feltet ikke er tomt.</span><span class="sxs-lookup"><span data-stu-id="3a2ce-122">When changing the company, make sure that the **Environment** field is not empty.</span></span> <span data-ttu-id="3a2ce-123">Hvis det er det, setter du det til ett av de tilgjengelige alternativene. Hvis ikke, vil ikke tillegget fungere som det skal.</span><span class="sxs-lookup"><span data-stu-id="3a2ce-123">If it is, then set it to one of the available options; otherwise, the add-in will not work correctly.</span></span>  

<span data-ttu-id="3a2ce-124">Hvis du gjør endringer i tillegget, må du laste det inn på nytt for å oppdatere tilkoblingen.</span><span class="sxs-lookup"><span data-stu-id="3a2ce-124">If you make changes to the add-in, you must reload it to update the connection.</span></span> <span data-ttu-id="3a2ce-125">Du kan laste inn på nytt ved å bruke menyen for ![tillegg i Excel](media/excel-addin-menu.png "Meny for Excel-tillegg") øverst til høyre for tillegget.</span><span class="sxs-lookup"><span data-stu-id="3a2ce-125">To reload, use the ![Excel add-in menu](media/excel-addin-menu.png "Excel add-in menu") menu in the top-right corner of the add-in.</span></span> <span data-ttu-id="3a2ce-126">Hvis du ikke kan laste inn tillegget, kontakter du systemansvarlig.</span><span class="sxs-lookup"><span data-stu-id="3a2ce-126">If you cannot load the add-in, talk to your administrator.</span></span> <span data-ttu-id="3a2ce-127">Hvis du er administrator, kan du se [Konfigurere Excel-tillegget for redigering av Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="3a2ce-127">If you are the administrator, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

> [!NOTE]
> <span data-ttu-id="3a2ce-128">For [!INCLUDE[prod_short](includes/prod_short.md)] lokalt er handlingen **Rediger i Excel** bare tilgjengelig hvis Excel-tillegget er konfigurert av systemansvarlig, og den er bare tilgjengelig for webklienten.</span><span class="sxs-lookup"><span data-stu-id="3a2ce-128">For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator, and only available for the Web client.</span></span> <span data-ttu-id="3a2ce-129">For administratorer, hvis du vil vite hvordan du installerer Excel-tilleggskomponenten, se [Definere Excel-tillegget for redigering av Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="3a2ce-129">For administrators, if you want to learn how to install the Excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="3a2ce-130">Se forskjellene mellom alternativene</span><span class="sxs-lookup"><span data-stu-id="3a2ce-130">See the differences between the options</span></span>
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="3a2ce-131">Se relatert opplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="3a2ce-131">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="3a2ce-132">Se også</span><span class="sxs-lookup"><span data-stu-id="3a2ce-132">See Also</span></span>

[<span data-ttu-id="3a2ce-133">Analysere årsregnskap i Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="3a2ce-133">Analyzing Financial Statements in Microsoft Excel</span></span>](finance-analyze-excel.md)  
[<span data-ttu-id="3a2ce-134">Arbeide med Business Central</span><span class="sxs-lookup"><span data-stu-id="3a2ce-134">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="3a2ce-135">Forbedringer i Excel-integrasjon i 2019 Release Wave 2</span><span class="sxs-lookup"><span data-stu-id="3a2ce-135">Enhancements to Excel integration in 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]