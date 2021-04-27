---
title: Begrense og tillate bruk av en post | Microsoft-dokumentasjon
description: Hvis du vil hindre at en post brukes i bestemte aktiviteter, for eksempel før oppføringen er godkjent, kan du innlemme to arbeidsflytsvar i en arbeidsflyt som styrer bruken av posten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: bbb22a00e878e8c4d75cb5fcdbcc27a28d9d22a4
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783994"
---
# <a name="restrict-and-allow-usage-of-a-record"></a><span data-ttu-id="0bc3c-103">Begrense og tillate bruk av en post</span><span class="sxs-lookup"><span data-stu-id="0bc3c-103">Restrict and Allow Usage of a Record</span></span>
<span data-ttu-id="0bc3c-104">Hvis du vil hindre at en post brukes i bestemte aktiviteter, for eksempel før oppføringen er godkjent, kan du innlemme to arbeidsflytsvar i en arbeidsflyt som styrer bruken av posten.</span><span class="sxs-lookup"><span data-stu-id="0bc3c-104">If you want to restrict a record from being used in certain activities, for example, until the record has been approved, you can incorporate two workflow responses in a workflow that controls the usage of the record.</span></span> <span data-ttu-id="0bc3c-105">Ett arbeidsflytsvar vil begrense bruken av posten som definert av arbeidsflythendelsen og -betingelsene.</span><span class="sxs-lookup"><span data-stu-id="0bc3c-105">One workflow response will restrict usage of the record as defined by the workflow event and conditions.</span></span> <span data-ttu-id="0bc3c-106">Et nytt arbeidsflytsvar vil tillate bruken av posten som definert av arbeidsflythendelsen og -betingelsene.</span><span class="sxs-lookup"><span data-stu-id="0bc3c-106">Another workflow response will allow usage of the record as defined by the workflow event and conditions.</span></span> <span data-ttu-id="0bc3c-107">Det finnes to svar i den generelle versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] for dette formålet: **Begrens bruk av en post.**</span><span class="sxs-lookup"><span data-stu-id="0bc3c-107">Two responses exist in the generic version of [!INCLUDE[prod_short](includes/prod_short.md)] for this purpose: **Restrict usage of a record.**</span></span> <span data-ttu-id="0bc3c-108">og **Tillat bruk av en post.**.</span><span class="sxs-lookup"><span data-stu-id="0bc3c-108">and **Allow usage of a record.**.</span></span>

> [!NOTE]  
>  <span data-ttu-id="0bc3c-109">Den generelle versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] tilbyr støtte for å forhindre at en post posteres, eksporteres som en betaling og skrives ut som en sjekk.</span><span class="sxs-lookup"><span data-stu-id="0bc3c-109">The generic version of [!INCLUDE[prod_short](includes/prod_short.md)] offers support for restricting a record from being posted, from being exported as a payment, and from being printed as a check.</span></span> <span data-ttu-id="0bc3c-110">For å støtte andre begrensninger må Microsoft-partneren tilpasse programkoden.</span><span class="sxs-lookup"><span data-stu-id="0bc3c-110">To support other restrictions, a Microsoft partner must customize the application code.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0bc3c-111">Arbeidsflytfunksjonaliteten for å begrense poster fra å brukes, er ikke relatert til funksjonaliteten for å blokkere vare, kunde og leverandørposter fra å bli bokført.</span><span class="sxs-lookup"><span data-stu-id="0bc3c-111">The workflow functionality to restrict and allow records from being used is not related to the functionality to block item, customer, and vendor records from being posted.</span></span>

<span data-ttu-id="0bc3c-112">Følgende fremgangsmåte beskriver hvordan du begrenser bestillinger fra å posteres før de er godkjent.</span><span class="sxs-lookup"><span data-stu-id="0bc3c-112">The following procedure describes how to restrict purchase orders from being posted until they have been approved.</span></span> <span data-ttu-id="0bc3c-113">Den nye arbeidsflyten skal baseres på den eksisterende arbeidsmalen for arbeidsflyt for kjøpsfakturagodkjenning.</span><span class="sxs-lookup"><span data-stu-id="0bc3c-113">The new workflow will be based on the existing Purchase Invoice Approval Workflow workflow template.</span></span>  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a><span data-ttu-id="0bc3c-114">Slik oppretter du et arbeidsflyttrinn som begrenser postering av ikke-godkjente bestillinger:</span><span class="sxs-lookup"><span data-stu-id="0bc3c-114">To create a workflow step that restricts posting of unapproved purchase orders</span></span>  
1. <span data-ttu-id="0bc3c-115">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Arbeidsflyter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0bc3c-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0bc3c-116">På **Arbeidsflyter**-siden oppretter du en ny arbeidsflyt kalt Arbeidsflyt for bestillingsgodkjenning.</span><span class="sxs-lookup"><span data-stu-id="0bc3c-116">On the **Workflows** page, create a new workflow named Purchase Order Approval Workflow.</span></span> <span data-ttu-id="0bc3c-117">Hvis du vil ha mer informasjon, kan du se [Opprette arbeidsflyter](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="0bc3c-117">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  
3. <span data-ttu-id="0bc3c-118">Velg handlingen **Kopier fra arbeidsflytmal**.</span><span class="sxs-lookup"><span data-stu-id="0bc3c-118">Choose the **Copy From Workflow Template** action.</span></span>  
4. <span data-ttu-id="0bc3c-119">Velg **Arbeidsflytkode for kilde**-feltet og velg deretter arbeidsmalen Arbeidsflyt for kjøpsfakturagodkjenning på **Arbeidsflytmaler**-siden.</span><span class="sxs-lookup"><span data-stu-id="0bc3c-119">Choose the **Source Workflow Code** field, and then, on the **Workflow Templates** page, choose the Purchase Invoice Approval Workflow workflow template.</span></span>  

     <span data-ttu-id="0bc3c-120">Legg merke til at de to første trinnene i arbeidsflyten er om å begrense og deretter tillate bruk av kjøpsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="0bc3c-120">Notice that the first two workflow steps are about restricting and then allowing usage of purchase invoices.</span></span> <span data-ttu-id="0bc3c-121">Fortsette å endre hendelsensbetingelsen på det første trinnet i den nye arbeidsflyten for å angi at den gjelder for bestillinger.</span><span class="sxs-lookup"><span data-stu-id="0bc3c-121">Proceed to change the event condition on the first step of the new workflow to specify that it applies to purchase orders.</span></span>  
5. <span data-ttu-id="0bc3c-122">I hurtigfanen **Arbeidsflyttrinn** velger du **Hendelsesvilkår**-feltet, og deretter velger du **Ordre** for **Dokumenttype**.</span><span class="sxs-lookup"><span data-stu-id="0bc3c-122">On the **Workflow Steps** FastTab, choose the **Event Conditions** field, and then, for the **Document Type** filter, select **Order**.</span></span>  
6. <span data-ttu-id="0bc3c-123">Fortsette med å redigere, slette eller legge til andre trinn i arbeidsflyten for å tilpasse til en forretningsprosess som begynner ved å forhindre at ikke-godkjente bestillinger posteres.</span><span class="sxs-lookup"><span data-stu-id="0bc3c-123">Proceed to edit, delete, or add other workflow steps to fit a business process that begins by restricting unapproved purchase orders from being posted.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0bc3c-124">Se også</span><span class="sxs-lookup"><span data-stu-id="0bc3c-124">See Also</span></span>  
<span data-ttu-id="0bc3c-125">[Opprette arbeidsflyter](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="0bc3c-125">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
[<span data-ttu-id="0bc3c-126">Arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="0bc3c-126">Workflow</span></span>](across-workflow.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]