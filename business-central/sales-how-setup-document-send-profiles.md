---
title: Definere foretrukne metoder for å sende salgsdokumenter | Microsoft-dokumentasjon
description: Beskriver hvordan du konfigurerer kundens foretrukne sendemetode for salgsdokumenter, for eksempel e-post, PDF-fil, elektronisk dokument og så videre.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: email, PDF, electronic document
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1ec87cbf0885b392dc92bbd9a25fca81db38c5a1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758145"
---
# <a name="set-up-document-sending-profiles"></a><span data-ttu-id="5289b-103">Definere en profil for dokumentsending</span><span class="sxs-lookup"><span data-stu-id="5289b-103">Set Up Document Sending Profiles</span></span>
<span data-ttu-id="5289b-104">Du kan definere hver kunde med en foretrukket metode for sending av salgsdokumenter, slik at du ikke trenger å velge et alternativ for sending hver gang du velger handlingen **Bokfør og send**.</span><span class="sxs-lookup"><span data-stu-id="5289b-104">You can set each customer up with a preferred method of sending sales documents, so that you do not have to select a sending option every time you choose the **Post and Send** action.</span></span>

<span data-ttu-id="5289b-105">På siden **Profiler for dokumentsending** definerer du ulike sendingsprofiler som du kan velge fra feltet **Profil for dokumentsending** på et kundekort.</span><span class="sxs-lookup"><span data-stu-id="5289b-105">On the **Document Sending Profiles** page, you set up different sending profiles that you can select from in the **Document Sending Profile** field on a customer card.</span></span> <span data-ttu-id="5289b-106">Du kan merke av for **Standard** for å angi at profilen for dokumentsending er standardprofilen for alle kunder, bortsett fra kunder der feltet **Profil for dokumentsending** er fylt ut med en annen sendingsprofil.</span><span class="sxs-lookup"><span data-stu-id="5289b-106">You can select the **Default** check box to specify that the document sending profile is the default profile for all customers, except for customers where the **Document Sending Profile** field is filled with another sending profile.</span></span>

<span data-ttu-id="5289b-107">Når du velger handlingen **Bokfør og send** i et salgsdokument, viser dialogboksen **Bokfør og send bekreftelse** sendingsprofilen som brukes, enten den som er satt opp for kunden, eller standarden for alle kunder.</span><span class="sxs-lookup"><span data-stu-id="5289b-107">When you choose the **Post and Send** action on a sales document, the **Post and Send Confirmation** dialog box shows the sending profile used, either the one set up for the customer or the default for all customers.</span></span> <span data-ttu-id="5289b-108">I dialogboksen kan du endre sendingsprofilen for salgsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="5289b-108">In the dialog box, you can change the sending profile for the sales document.</span></span> <span data-ttu-id="5289b-109">Hvis du vil ha mer informasjon, kan du se [Fakturere salg](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="5289b-109">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHH?rel=0]

## <a name="to-set-up-a-document-sending-profile"></a><span data-ttu-id="5289b-110">Slik definerer du en profil for dokumentsending:</span><span class="sxs-lookup"><span data-stu-id="5289b-110">To set up a document sending profile</span></span>
1. <span data-ttu-id="5289b-111">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Profiler for dokumentsending**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="5289b-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Document Sending Profiles**, and then choose the related link.</span></span>
2. <span data-ttu-id="5289b-112">På siden **Profiler for dokumentsending** velger du handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5289b-112">On the **Document Sending Profiles** page, choose the **New** action.</span></span>
3. <span data-ttu-id="5289b-113">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="5289b-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a><span data-ttu-id="5289b-114">Slik angir du en sendingsprofil på et kundekort:</span><span class="sxs-lookup"><span data-stu-id="5289b-114">To specify a sending profile on a customer card</span></span>
1. <span data-ttu-id="5289b-115">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="5289b-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="5289b-116">Åpne kortet til kunden som du vil definere en sendingsprofil for.</span><span class="sxs-lookup"><span data-stu-id="5289b-116">Open the card of the customer who you want to set up a sending profile for.</span></span>
3. <span data-ttu-id="5289b-117">Velg en profil i feltet i feltet **Profiler for dokumentsending**, som du har satt opp som beskrevet i forrige fremgangsmåte.</span><span class="sxs-lookup"><span data-stu-id="5289b-117">In the **Document Sending Profile** field, select a profile that you have set up as described in the previous procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="5289b-118">Se også</span><span class="sxs-lookup"><span data-stu-id="5289b-118">See Also</span></span>
[<span data-ttu-id="5289b-119">Sette opp salg</span><span class="sxs-lookup"><span data-stu-id="5289b-119">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="5289b-120">Salg</span><span class="sxs-lookup"><span data-stu-id="5289b-120">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="5289b-121">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5289b-121">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
