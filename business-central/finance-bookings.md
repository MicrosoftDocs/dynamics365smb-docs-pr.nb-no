---
title: Fakturere bestillinger i Business Central | Microsoft-dokumentasjon
description: Finn ut hvordan du kan foreta massefakturering fra Microsoft Bookings i Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: invoicing, bookings
ms.date: 06/14/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 56a41a81bee7084d0f624e6ce9bc4a7138e77ff0
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="bulk-invoicing-for-microsoft-bookings-in-included365finincludesd365finmdmd"></a><span data-ttu-id="b2e53-103">Massefakturering for Microsoft Bookings i [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="b2e53-103">Bulk Invoicing for Microsoft Bookings in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
<span data-ttu-id="b2e53-104">Hvis selskapet ditt bruker Bookings-appen i Office 365, kan du foreta massefakturering for avtaler.</span><span class="sxs-lookup"><span data-stu-id="b2e53-104">If your company uses the Bookings app in Office 365, you can do bulk invoicing for appointments.</span></span> <span data-ttu-id="b2e53-105">Siden **Ufakturerte Bookings** i [!INCLUDE[d365fin](includes/d365fin_md.md)] gir en oversikt over selskapets fullførte bestillinger.</span><span class="sxs-lookup"><span data-stu-id="b2e53-105">The **Uninvoiced Bookings** page in [!INCLUDE[d365fin](includes/d365fin_md.md)] provides a list of the company's completed bookings.</span></span> <span data-ttu-id="b2e53-106">På denne siden kan du raskt velge avtalene du vil fakturere, og opprette fakturakladder for de leverte tjenestene.</span><span class="sxs-lookup"><span data-stu-id="b2e53-106">In this page you can quickly select the appointments that you want to invoice and create draft invoices for the services provided.</span></span>  

## <a name="connect-to-bookings"></a><span data-ttu-id="b2e53-107">Koble til Bookings</span><span class="sxs-lookup"><span data-stu-id="b2e53-107">Connect to Bookings</span></span>
<span data-ttu-id="b2e53-108">For å kunne koble [!INCLUDE[d365fin](includes/d365fin_md.md)] til Bookings må du angi Bookings-firmaet, hva som skal synkroniseres med Bookings, hvor ofte du vil synkronisere, og hvilke maler som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="b2e53-108">To connect your [!INCLUDE[d365fin](includes/d365fin_md.md)] with Bookings, you must specify your Bookings company, what to synchronize with Bookings, how often to synchronize, and which templates to use.</span></span> <span data-ttu-id="b2e53-109">Du definerer denne informasjonen på siden **Oppsett for synkronisering av Bookings**, som du kan åpne fra siden **Konfigurasjon av Exchange-synkronisering**, som du finner via [Søk](ui-search.md).</span><span class="sxs-lookup"><span data-stu-id="b2e53-109">You set up this information in the **Booking Sync. Setup** page, which you can launch from the **Exchange Sync. Setup** page, which you can find through [Search](ui-search.md).</span></span>  

<span data-ttu-id="b2e53-110">Hvis du for eksempel vil synkronisere kunder mellom Bookings og [!INCLUDE[d365fin](includes/d365fin_md.md)], må du angi standardmalen som skal brukes til å legge til nye kunder i [!INCLUDE[d365fin](includes/d365fin_md.md)], basert på kundene i Bookings-firmaet ditt.</span><span class="sxs-lookup"><span data-stu-id="b2e53-110">For example, if you want to synchronize customers between Bookings and [!INCLUDE[d365fin](includes/d365fin_md.md)], you must specify the default template to use to add new customers in [!INCLUDE[d365fin](includes/d365fin_md.md)] based on the customers in your Bookings company.</span></span>  

## <a name="invoice-appointments"></a><span data-ttu-id="b2e53-111">Fakturaavtaler</span><span class="sxs-lookup"><span data-stu-id="b2e53-111">Invoice Appointments</span></span>
<span data-ttu-id="b2e53-112">Når tiden er inne for å sende fakturaer for de fullførte bestillingene, går du til siden **Ufakturerte Bookings**.</span><span class="sxs-lookup"><span data-stu-id="b2e53-112">When it is time to send invoices for the completed bookings, you go to the **Uninvoiced Bookings** page.</span></span> <span data-ttu-id="b2e53-113">Listen er lang eller kort avhengig av hvor ofte informasjonen synkroniseres.</span><span class="sxs-lookup"><span data-stu-id="b2e53-113">Depending on how often the information is synchronized, the list is long or short.</span></span> <span data-ttu-id="b2e53-114">Du kan opprette fakturaer for alle bestillingene i listen eller én bestilling om gangen.</span><span class="sxs-lookup"><span data-stu-id="b2e53-114">You can create invoices for all bookings in the list or one booking at a time.</span></span> <span data-ttu-id="b2e53-115">Du kan velge én eller flere poster i listen og fakturere bare disse.</span><span class="sxs-lookup"><span data-stu-id="b2e53-115">You can select one or more entries in the list and invoice those only.</span></span>  

<span data-ttu-id="b2e53-116">Støtten for fakturering av avtaler fra Bookings er enklere enn den mer fullstendige arbeidsflyten der du arbeider med tilbud, ordrer og salgsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="b2e53-116">The support for invoicing appointments from Bookings is simpler than the fuller workflow of working with sales quotes, sales orders, and sales invoices.</span></span> <span data-ttu-id="b2e53-117">Hvis du vil ha mer informasjon, kan du se [Fakturere salg](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="b2e53-117">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span> <span data-ttu-id="b2e53-118">Du kan velge å selge tjenestene ved å bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] eller velge å bruke Bookings, avhengig av forretningsbehovene dine.</span><span class="sxs-lookup"><span data-stu-id="b2e53-118">You can choose to sell your services using [!INCLUDE[d365fin](includes/d365fin_md.md)] or choose to use Bookings, depending on your business needs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b2e53-119">Se også</span><span class="sxs-lookup"><span data-stu-id="b2e53-119">See Also</span></span>
[<span data-ttu-id="b2e53-120">Finans</span><span class="sxs-lookup"><span data-stu-id="b2e53-120">Finance</span></span>](finance.md)  
[<span data-ttu-id="b2e53-121">Fakturere salg</span><span class="sxs-lookup"><span data-stu-id="b2e53-121">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="b2e53-122">Sette opp salg</span><span class="sxs-lookup"><span data-stu-id="b2e53-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="b2e53-123">Microsoft Bookings</span><span class="sxs-lookup"><span data-stu-id="b2e53-123">Microsoft Bookings</span></span>](https://products.office.com/en-us/business/scheduling-and-booking-app)  

