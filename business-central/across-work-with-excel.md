---
title: Vise og redigere i Excel fra Business Central | Microsoft-dokumenter
description: "Lær om hvordan du åpner sidene i Microsoft Excel fra Business Central for bedre dataanalyser."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 12/07/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 5d6d2d9527e81a92987f6b8fcdbe8e087c3c537a
ms.openlocfilehash: 27c137ea6309d40cddc94bc676ec7ea27d5c01fa
ms.contentlocale: nb-no
ms.lasthandoff: 01/22/2019

---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="3e234-103">Vise og redigere i Excel fra Business Central</span><span class="sxs-lookup"><span data-stu-id="3e234-103">Viewing and Editing in Excel From Business Central</span></span> 

<span data-ttu-id="3e234-104">Med sider som viser en oversikt over poster i rader og kolonner, som en liste over kunder, ordrer eller fakturaer, kan du også vise poster ved hjelp av Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="3e234-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="3e234-105">Du har to alternative måter å gjøre dette på.</span><span class="sxs-lookup"><span data-stu-id="3e234-105">To do this, you have two options.</span></span> <span data-ttu-id="3e234-106">Du kan enten velge **Åpne i Excel**-handling eller **Rediger i Excel**-handlingen på siden.</span><span class="sxs-lookup"><span data-stu-id="3e234-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="3e234-107">Forskjellene mellom de to handlingen er følgende:</span><span class="sxs-lookup"><span data-stu-id="3e234-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="3e234-108">Åpne i Excel</span><span class="sxs-lookup"><span data-stu-id="3e234-108">Open in Excel</span></span>

-    <span data-ttu-id="3e234-109">Med denne handlingen respekterer Excel filtre på siden som avgrenser postene som vises.</span><span class="sxs-lookup"><span data-stu-id="3e234-109">With this action, Excel respects any filters on the page the limit the records shown.</span></span> <span data-ttu-id="3e234-110">Dette betyr at Excel-arbeidsboken inneholder de samme radene og kolonnene som vises på siden i [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="3e234-110">This means that the Excel workbook will contain the same rows and columns that appear on the the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

-    <span data-ttu-id="3e234-111">Du kan gjøre endringer i postene i Excel, men du kan ikke publiserer endringene tilbake til [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="3e234-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="3e234-112">Du kan bare lagre endringene til Excel-filen på datamaskinen din.</span><span class="sxs-lookup"><span data-stu-id="3e234-112">You can only save the changes to Excel file on your computer.</span></span> 

-    <span data-ttu-id="3e234-113">Denne handlingen fungerer både i Windows- og macOS.</span><span class="sxs-lookup"><span data-stu-id="3e234-113">This action works on both on Windows and macOS.</span></span> 

>[!NOTE]
><span data-ttu-id="3e234-114">For lokal [!INCLUDE[prodshort](includes/prodshort.md)] er **Åpne i Excel**-handlingen ikke tilgjengelig hvis **Rediger i Excel**-handlingen er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="3e234-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is not available if the **Edit in Excel** action is.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="3e234-115">Rediger i Excel</span><span class="sxs-lookup"><span data-stu-id="3e234-115">Edit in Excel</span></span>

-    <span data-ttu-id="3e234-116">Med denne handlingen respekterer ikke Excel-arbeidsboken filtre på siden som avgrenser postene som vises.</span><span class="sxs-lookup"><span data-stu-id="3e234-116">With this action, the Excel workbook does not respect filters on the page the limit the records shown.</span></span> <span data-ttu-id="3e234-117">Dette betyr at Excel-arbeidsboken inneholder alle tilgjengelige poster og kolonner, uavhengig av hva som vises på siden.</span><span class="sxs-lookup"><span data-stu-id="3e234-117">This means that the Excel workbook will contain all the available records and columns, regardless of what is shown on the page.</span></span> 

-    <span data-ttu-id="3e234-118">Fordelen med **Rediger i Excel**-handlingen er at den lar deg gjøre endringer i poster i Excel og deretter publiserer endringene tilbake til [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="3e234-118">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

-    <span data-ttu-id="3e234-119">Den fungerer bare i Windows, ikke i macOS.</span><span class="sxs-lookup"><span data-stu-id="3e234-119">It only works on Windows; not macOS.</span></span>

>[!NOTE]
><span data-ttu-id="3e234-120">For lokal [!INCLUDE[prodshort](includes/prodshort.md)] er **Rediger i Excel**-handlingen bare tilgjengelig hvis Excel-tillegget er installert av systemansvarlig.</span><span class="sxs-lookup"><span data-stu-id="3e234-120">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been installed by your administrator.</span></span> <span data-ttu-id="3e234-121">For administratorer, hvis du vil vite hvordan du installerer Excel-tilleggskomponenten, se [Definere Excel-tillegget](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="3e234-121">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

## <a name="see-also"></a><span data-ttu-id="3e234-122">Se også</span><span class="sxs-lookup"><span data-stu-id="3e234-122">See Also</span></span>

[<span data-ttu-id="3e234-123">Arbeide med Business Central</span><span class="sxs-lookup"><span data-stu-id="3e234-123">Working with Business Central</span></span>](ui-work-product.md)  

