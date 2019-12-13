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
ms.date: 10/24/2019
ms.author: jswymer
ms.openlocfilehash: 99fe339426b755b70983d8ec9345858357043347
ms.sourcegitcommit: 893e13fa75b2d04dedd4a29abda216e3e54b24ae
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/15/2019
ms.locfileid: "2808748"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="192d2-103">Vise og redigere i Excel fra Business Central</span><span class="sxs-lookup"><span data-stu-id="192d2-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="192d2-104">Med sider som viser en oversikt over poster i rader og kolonner, som en liste over kunder, ordrer eller fakturaer, kan du også vise poster ved hjelp av Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="192d2-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="192d2-105">Du har to alternative måter å gjøre dette på.</span><span class="sxs-lookup"><span data-stu-id="192d2-105">To do this, you have two options.</span></span> <span data-ttu-id="192d2-106">Du kan enten velge **Åpne i Excel**-handling eller **Rediger i Excel**-handlingen på siden.</span><span class="sxs-lookup"><span data-stu-id="192d2-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="192d2-107">Forskjellene mellom de to handlingen er følgende:</span><span class="sxs-lookup"><span data-stu-id="192d2-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="192d2-108">Åpne i Excel</span><span class="sxs-lookup"><span data-stu-id="192d2-108">Open in Excel</span></span>

- <span data-ttu-id="192d2-109">Med denne handlingen respekterer Excel filtre på siden som avgrenser postene som vises.</span><span class="sxs-lookup"><span data-stu-id="192d2-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="192d2-110">Dette betyr at Excel-arbeidsboken inneholder de samme radene og kolonnene som vises på siden i [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="192d2-110">This means that the Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="192d2-111">Du kan gjøre endringer i postene i Excel, men du kan ikke publiserer endringene tilbake til [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="192d2-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="192d2-112">Du kan bare lagre endringene til Excel-filen på datamaskinen din.</span><span class="sxs-lookup"><span data-stu-id="192d2-112">You can only save the changes to Excel file on your computer.</span></span> 

- <span data-ttu-id="192d2-113">Denne handlingen fungerer både i Windows- og macOS.</span><span class="sxs-lookup"><span data-stu-id="192d2-113">This action works on both on Windows and macOS.</span></span> 

> [!NOTE]
> <span data-ttu-id="192d2-114">For [!INCLUDE[prodshort](includes/prodshort.md)] lokalt er handlingen **Åpne i Excel** tilgjengelig som standard.</span><span class="sxs-lookup"><span data-stu-id="192d2-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="192d2-115">Hvis du konfigurerer [!INCLUDE [prodshort](includes/prodshort.md)] lokalt for redigering av data i Excel, erstattes handlingen **Åpne i Excel** med handlingen **Rediger i Excel**.</span><span class="sxs-lookup"><span data-stu-id="192d2-115">However, if you set up [!INCLUDE [prodshort](includes/prodshort.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="192d2-116">Rediger i Excel</span><span class="sxs-lookup"><span data-stu-id="192d2-116">Edit in Excel</span></span>

- <span data-ttu-id="192d2-117">Med denne handlingen respekterer Excel de fleste filtre på siden som avgrenser postene som vises.</span><span class="sxs-lookup"><span data-stu-id="192d2-117">With this action, Excel respects most filters on the page that limit the records shown.</span></span> <span data-ttu-id="192d2-118">Dette betyr at Excel-arbeidsboken inneholder nesten de samme postene og kolonnene.</span><span class="sxs-lookup"><span data-stu-id="192d2-118">This means that the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="192d2-119">Fordelen med **Rediger i Excel**-handlingen er at den lar deg gjøre endringer i poster i Excel og deretter publiserer endringene tilbake til [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="192d2-119">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="192d2-120">Den fungerer bare i Windows, ikke i macOS.</span><span class="sxs-lookup"><span data-stu-id="192d2-120">It only works on Windows; not macOS.</span></span>

<span data-ttu-id="192d2-121">Dette ble forbedret i 2019 Release Wave 2.</span><span class="sxs-lookup"><span data-stu-id="192d2-121">This was enhanced in 2019 release wave 2.</span></span> <span data-ttu-id="192d2-122">Hvis du vil ha mer informasjon, se [Forbedringer i Excel-integrasjon](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span><span class="sxs-lookup"><span data-stu-id="192d2-122">For more information, see [Enhancements to Excel integration](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span></span>

> [!NOTE]
> <span data-ttu-id="192d2-123">For lokal [!INCLUDE[prodshort](includes/prodshort.md)] er **Rediger i Excel**-handlingen bare tilgjengelig hvis Excel-tillegget er konfigurert av systemansvarlig.</span><span class="sxs-lookup"><span data-stu-id="192d2-123">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator.</span></span> <span data-ttu-id="192d2-124">For administratorer, hvis du vil vite hvordan du installerer Excel-tilleggskomponenten, se [Definere Excel-tillegget for redigering av Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="192d2-124">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

> [!NOTE]
> <span data-ttu-id="192d2-125">For [!INCLUDE[prodshort](includes/prodshort.md)] lokalt er denne funksjonen bare tilgjengelig for webklienten.</span><span class="sxs-lookup"><span data-stu-id="192d2-125">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, this feature is only available for the Web client.</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="192d2-126">Se forskjellene mellom alternativene</span><span class="sxs-lookup"><span data-stu-id="192d2-126">See the differences between the options</span></span> 
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-also"></a><span data-ttu-id="192d2-127">Se også</span><span class="sxs-lookup"><span data-stu-id="192d2-127">See Also</span></span>
[<span data-ttu-id="192d2-128">Arbeide med Business Central</span><span class="sxs-lookup"><span data-stu-id="192d2-128">Working with Business Central</span></span>](ui-work-product.md)  
