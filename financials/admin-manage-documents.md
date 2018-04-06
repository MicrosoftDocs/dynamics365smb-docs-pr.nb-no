---
title: Administrere, slette eller komprimere dokumenter | Microsoft-dokumentasjon
description: Behold dine historiske data, eller slett dem.
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 60438f0b6f0d5da60925b5b9c309cc359a8422e3
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="manage-documents"></a><span data-ttu-id="558d7-103">Administrere dokumenter</span><span class="sxs-lookup"><span data-stu-id="558d7-103">Manage Documents</span></span>
<span data-ttu-id="558d7-104">En sentral rolle, for eksempel programadministrator, må regelmessig håndtere oppsamlede historiske dokumenter ved å slette eller komprimere dem.</span><span class="sxs-lookup"><span data-stu-id="558d7-104">A central role, such as the application administrator, must regularly deal with accumulating historic documents by deleting or compressing them.</span></span>  

## <a name="delete-documents"></a><span data-ttu-id="558d7-105">Slette dokumenter</span><span class="sxs-lookup"><span data-stu-id="558d7-105">Delete Documents</span></span>
<span data-ttu-id="558d7-106">I enkelte situasjoner kan det hende du må slette fakturerte bestillinger som ikke allerede er slettet.</span><span class="sxs-lookup"><span data-stu-id="558d7-106">In certain situations, you may need to delete invoiced purchase orders that have not been deleted.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="558d7-107"> kontrollerer at de slettede bestillingene er fullstendig fakturert.</span><span class="sxs-lookup"><span data-stu-id="558d7-107"> checks that you have fully invoiced the deleted purchase orders.</span></span> <span data-ttu-id="558d7-108">Du kan ikke slette bestillinger som ikke er fullstendig fakturert og mottatt.</span><span class="sxs-lookup"><span data-stu-id="558d7-108">You cannot delete orders that you have not fully invoiced and received.</span></span>  

<span data-ttu-id="558d7-109">Ordrereturer slettes vanligvis etter at de er fakturert.</span><span class="sxs-lookup"><span data-stu-id="558d7-109">Return orders are usually deleted after they are invoiced.</span></span> <span data-ttu-id="558d7-110">Når du bokfører en faktura, overføres den til vinduet **Bokført kjøpskreditnota**.</span><span class="sxs-lookup"><span data-stu-id="558d7-110">When you post an invoice, it is transferred to the **Posted Purchase Credit Memo** window.</span></span> <span data-ttu-id="558d7-111">Hvis du merket av for **Returforsendelse i kreditnota** i **Kjøpsoppsett**-vinduet, overføres fakturaen til vinduet **Bokført returforsendelse**.</span><span class="sxs-lookup"><span data-stu-id="558d7-111">If you selected the **Return Shipment on Credit Memo** check box in the **Purchases & Payable Setup** window, then the invoice is transferred to the **Posted Return Shipment** window.</span></span> <span data-ttu-id="558d7-112">Du kan slette dokumentene ved hjelp av kjørselen **Slett fakturerte best.returer**.</span><span class="sxs-lookup"><span data-stu-id="558d7-112">You can delete the documents using the **Delete Invd Purch. Ret. Orders** batch job.</span></span> <span data-ttu-id="558d7-113">Før du sletter, kontrollerer kjørselen om bestillingsreturer er fullstendig levert og fakturert.</span><span class="sxs-lookup"><span data-stu-id="558d7-113">Before deleting, the batch job checks if the purchase return orders are fully shipped and invoiced.</span></span>  

<span data-ttu-id="558d7-114">Rammebestillinger slettes ikke når du har behandlet og fakturert alle de relaterte bestillingene.</span><span class="sxs-lookup"><span data-stu-id="558d7-114">Blanket purchase orders are not deleted after you have processed and invoiced all the related purchase orders.</span></span> <span data-ttu-id="558d7-115">Du kan slette rammebestillinger med kjørselen **Slett fakturerte rammebestillinger**.</span><span class="sxs-lookup"><span data-stu-id="558d7-115">You can delete blanket orders with the **Delete Invoiced Blanket Purchase Orders** batch job.</span></span>  

<span data-ttu-id="558d7-116">Fakturerte serviceordrer slettes vanligvis automatisk etter at de er fullstendig fakturert.</span><span class="sxs-lookup"><span data-stu-id="558d7-116">Invoiced service orders are usually deleted automatically after having been fully invoiced.</span></span> <span data-ttu-id="558d7-117">Når en faktura bokføres, opprettes en tilhørende post i vinduet **Bokførte servicefakturaer**.</span><span class="sxs-lookup"><span data-stu-id="558d7-117">When an invoice is posted, a corresponding entry is created in the **Posted Service Invoices** window.</span></span> <span data-ttu-id="558d7-118">Det bokførte dokumentet kan vises i vinduet **Bokført servicefaktura**.</span><span class="sxs-lookup"><span data-stu-id="558d7-118">The posted document can be viewed in the **Posted Service Invoice** window.</span></span>  

<span data-ttu-id="558d7-119">Serviceordrer slettes ikke automatisk hvis det totale antallet i ordren ikke er bokført fra selve serviceordren, men fra **Servicefaktura**-vinduet.</span><span class="sxs-lookup"><span data-stu-id="558d7-119">Service orders are not deleted automatically, however, if the total quantity on the order has been posted not from the service order itself, but from the **Service Invoice** window.</span></span> <span data-ttu-id="558d7-120">Da må du kanskje slette fakturerte ordrer som ikke er slettet.</span><span class="sxs-lookup"><span data-stu-id="558d7-120">Then you may need to delete invoiced orders that were not deleted.</span></span> <span data-ttu-id="558d7-121">Du kan gjøre dette ved hjelp av kjørselen **Slett fakturerte serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="558d7-121">You can do this by running the **Delete Invoiced Service Orders** batch job.</span></span>  

## <a name="see-also"></a><span data-ttu-id="558d7-122">Se også</span><span class="sxs-lookup"><span data-stu-id="558d7-122">See Also</span></span>  
[<span data-ttu-id="558d7-123">Oppsett og administrasjon i Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="558d7-123">Setup and Administration in Finance and Operations, Business edition</span></span>](admin-setup-and-administration.md)  

