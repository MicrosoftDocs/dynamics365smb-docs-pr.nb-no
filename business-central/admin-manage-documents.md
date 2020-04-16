---
title: Administrere, slette eller komprimere dokumenter | Microsoft-dokumentasjon
description: Behold dine historiske data, eller slett dem.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 54cccb9df4daee3ad0811139dc2180d8a3072deb
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3186959"
---
# <a name="manage-documents"></a><span data-ttu-id="3bf49-103">Administrere dokumenter</span><span class="sxs-lookup"><span data-stu-id="3bf49-103">Manage Documents</span></span>
<span data-ttu-id="3bf49-104">En sentral rolle, for eksempel programadministrator, må regelmessig håndtere oppsamlede historiske dokumenter ved å slette eller komprimere dem.</span><span class="sxs-lookup"><span data-stu-id="3bf49-104">A central role, such as the application administrator, must regularly deal with accumulating historic documents by deleting or compressing them.</span></span>  

## <a name="delete-documents"></a><span data-ttu-id="3bf49-105">Slette dokumenter</span><span class="sxs-lookup"><span data-stu-id="3bf49-105">Delete Documents</span></span>
<span data-ttu-id="3bf49-106">I enkelte situasjoner kan det hende du må slette fakturerte bestillinger som ikke allerede er slettet.</span><span class="sxs-lookup"><span data-stu-id="3bf49-106">In certain situations, you may need to delete invoiced purchase orders that have not been deleted.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="3bf49-107">kontrollerer at de slettede bestillingene er fullstendig fakturert.</span><span class="sxs-lookup"><span data-stu-id="3bf49-107">checks that you have fully invoiced the deleted purchase orders.</span></span> <span data-ttu-id="3bf49-108">Du kan ikke slette bestillinger som ikke er fullstendig fakturert og mottatt.</span><span class="sxs-lookup"><span data-stu-id="3bf49-108">You cannot delete orders that you have not fully invoiced and received.</span></span>  

<span data-ttu-id="3bf49-109">Ordrereturer slettes vanligvis etter at de er fakturert.</span><span class="sxs-lookup"><span data-stu-id="3bf49-109">Return orders are usually deleted after they are invoiced.</span></span> <span data-ttu-id="3bf49-110">Når du bokfører en faktura, overføres den til siden **Bokført kjøpskreditnota**.</span><span class="sxs-lookup"><span data-stu-id="3bf49-110">When you post an invoice, it is transferred to the **Posted Purchase Credit Memo** page.</span></span> <span data-ttu-id="3bf49-111">Hvis du merket av for **Returforsendelse i kreditnota** på **Kjøpsoppsett**-siden, overføres fakturaen til siden **Bokført returforsendelse**.</span><span class="sxs-lookup"><span data-stu-id="3bf49-111">If you selected the **Return Shipment on Credit Memo** check box on the **Purchases & Payable Setup** page, then the invoice is transferred to the **Posted Return Shipment** page.</span></span> <span data-ttu-id="3bf49-112">Du kan slette dokumentene ved hjelp av kjørselen **Slett fakturerte best.returer**.</span><span class="sxs-lookup"><span data-stu-id="3bf49-112">You can delete the documents using the **Delete Invd Purch. Ret. Orders** batch job.</span></span> <span data-ttu-id="3bf49-113">Før du sletter, kontrollerer kjørselen om bestillingsreturer er fullstendig levert og fakturert.</span><span class="sxs-lookup"><span data-stu-id="3bf49-113">Before deleting, the batch job checks if the purchase return orders are fully shipped and invoiced.</span></span>  

<span data-ttu-id="3bf49-114">Rammebestillinger slettes ikke når du har behandlet og fakturert alle de relaterte bestillingene.</span><span class="sxs-lookup"><span data-stu-id="3bf49-114">Blanket purchase orders are not deleted after you have processed and invoiced all the related purchase orders.</span></span> <span data-ttu-id="3bf49-115">Du kan slette rammebestillinger med kjørselen **Slett fakturerte rammebestillinger**.</span><span class="sxs-lookup"><span data-stu-id="3bf49-115">You can delete blanket orders with the **Delete Invoiced Blanket Purchase Orders** batch job.</span></span>  

<span data-ttu-id="3bf49-116">Fakturerte serviceordrer slettes vanligvis automatisk etter at de er fullstendig fakturert.</span><span class="sxs-lookup"><span data-stu-id="3bf49-116">Invoiced service orders are usually deleted automatically after having been fully invoiced.</span></span> <span data-ttu-id="3bf49-117">Når en faktura bokføres, opprettes en tilhørende post på siden **Bokførte servicefakturaer**.</span><span class="sxs-lookup"><span data-stu-id="3bf49-117">When an invoice is posted, a corresponding entry is created on the **Posted Service Invoices** page.</span></span> <span data-ttu-id="3bf49-118">Det bokførte dokumentet kan vises på siden **Bokført servicefaktura**.</span><span class="sxs-lookup"><span data-stu-id="3bf49-118">The posted document can be viewed on the **Posted Service Invoice** page.</span></span>  

<span data-ttu-id="3bf49-119">Serviceordrer slettes ikke automatisk hvis det totale antallet i ordren ikke er bokført fra selve serviceordren, men fra **Servicefaktura**-siden.</span><span class="sxs-lookup"><span data-stu-id="3bf49-119">Service orders are not deleted automatically, however, if the total quantity on the order has been posted not from the service order itself, but from the **Service Invoice** page.</span></span> <span data-ttu-id="3bf49-120">Da må du kanskje slette fakturerte ordrer som ikke er slettet.</span><span class="sxs-lookup"><span data-stu-id="3bf49-120">Then you may need to delete invoiced orders that were not deleted.</span></span> <span data-ttu-id="3bf49-121">Du kan gjøre dette ved hjelp av kjørselen **Slett fakturerte serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="3bf49-121">You can do this by running the **Delete Invoiced Service Orders** batch job.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3bf49-122">Se også</span><span class="sxs-lookup"><span data-stu-id="3bf49-122">See Also</span></span>  
[<span data-ttu-id="3bf49-123">Administrasjon</span><span class="sxs-lookup"><span data-stu-id="3bf49-123">Administration</span></span>](admin-setup-and-administration.md)  
