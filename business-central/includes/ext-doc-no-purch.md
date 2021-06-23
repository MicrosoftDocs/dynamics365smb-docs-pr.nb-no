---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: 59376b96dcd6f755040b07784ceca53e157bcf14
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115982"
---
<span data-ttu-id="4ee61-101">I kjøpsdokumenter og kladder kan du angi et dokumentnummer som viser til leverandørens nummereringssystem.</span><span class="sxs-lookup"><span data-stu-id="4ee61-101">On purchase documents and journals, you can specify a document number that refers to the vendor's numbering system.</span></span> <span data-ttu-id="4ee61-102">Bruk dette feltet til å registrere nummeret som leverandøren har knyttet til ordren, fakturaen eller kreditnotaen.</span><span class="sxs-lookup"><span data-stu-id="4ee61-102">Use this field to record the number that the vendor assigned to the order, invoice, or credit memo.</span></span> <span data-ttu-id="4ee61-103">Du kan deretter bruke nummeret senere hvis du trenger å søke etter den bokførte oppføring ved hjelp av dette nummeret.</span><span class="sxs-lookup"><span data-stu-id="4ee61-103">You can then use the number later if, for some reason, you need to search for the posted entry using this number.</span></span>

<span data-ttu-id="4ee61-104">Feltet **Obligatorisk nr. for eksternt dokument** i feltet **Kjøpsoppsett** angir om det er obligatorisk å angi et eksternt dokumentnummer i følgende situasjoner:</span><span class="sxs-lookup"><span data-stu-id="4ee61-104">The **Ext. Doc. No. Mandatory** field in the **Purchases & Payables Setup** page specifies whether it is mandatory to enter an external document number in the following situations:</span></span>

* <span data-ttu-id="4ee61-105">I feltet **Leverandørs fakturanr.**, feltet **Leverandørs bestillingsnr.**</span><span class="sxs-lookup"><span data-stu-id="4ee61-105">In the **Vendor Invoice No.** field, **Vendor Order No.**</span></span> <span data-ttu-id="4ee61-106">, eller feltet **Leverandørs kreditnotanr.**</span><span class="sxs-lookup"><span data-stu-id="4ee61-106">field, or the **Vendor Cr. Memo No.**</span></span> <span data-ttu-id="4ee61-107">i et bestillingshode</span><span class="sxs-lookup"><span data-stu-id="4ee61-107">field on a purchase header</span></span>

* <span data-ttu-id="4ee61-108">I feltet **Eksternt dokumentnr.** på en finanskladdelinje der innholdet i feltet **Bilagstype** er angitt til *Faktura*, *Kreditnota* eller *Rentenota*, og innholdet i feltet **Kontotype** er angitt til *Leverandør*.</span><span class="sxs-lookup"><span data-stu-id="4ee61-108">In the **External Document No.** field on a general journal line, where the **Document Type** field is set to *Invoice*, *Credit Memo*, or *Finance Charge Memo*, and the **Account Type** field is set to *Vendor*.</span></span>

<span data-ttu-id="4ee61-109">Hvis du velger dette feltet, vil det ikke være mulig å bokføre en faktura, en kreditnota eller den type finanskladdelinje som er beskrevet ovenfor, uten at et eksternt dokumentnummer er fylt ut.</span><span class="sxs-lookup"><span data-stu-id="4ee61-109">If you select this field, it will not be possible to post an invoice, a credit memo, or the type of general journal line described above without an external document number.</span></span>

<span data-ttu-id="4ee61-110">Det eksterne dokumentnummeret inkluderes i bokførte dokumenter der du kan søke etter det aktuelle nummeret.</span><span class="sxs-lookup"><span data-stu-id="4ee61-110">The external document number is included in posted documents where you can search by the relevant number.</span></span> <span data-ttu-id="4ee61-111">Du kan også søke ved hjelp av det eksterne dokumentnummeret når du navigerer i leverandørposter.</span><span class="sxs-lookup"><span data-stu-id="4ee61-111">You can also search using the external document number when navigating on vendor ledger entries.</span></span>

<span data-ttu-id="4ee61-112">En annen måte å håndtere eksterne dokumentnumre på, er å bruke feltet **Deres referanse**.</span><span class="sxs-lookup"><span data-stu-id="4ee61-112">A different way to handle external document numbers is to use the **Your Reference** field.</span></span> <span data-ttu-id="4ee61-113">Hvis du bruker feltet **Deres referanse**, inkluderes nummeret i bokførte dokumenter, og du kan søke etter det på samme måte som for verdier fra feltet **Eksternt dokumentnr.**.</span><span class="sxs-lookup"><span data-stu-id="4ee61-113">If you use the **Your Reference** field, the number will be included in posted documents, and you can search by it in the same way as for values from **External Document No.** fields.</span></span> <span data-ttu-id="4ee61-114">Men feltet er ikke tilgjengelig på kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="4ee61-114">But the field is not available on journal lines.</span></span>
