---
title: Definere koder for forretningsforbindelse for kontakter | Microsoft-dokumentasjon
description: Bruk forretningsforbindelser i Business Central til å hjelpe til med markedsføring, og til å angi hvilket forretningsforhold du har til prospekter, klienter og kunder, for eksempel en bank eller serviceleverandør.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 10/01/2019
ms.author: jswymer
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: 6c20dbd1eaa60037f33aee35701c5baa224fbc1c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2309391"
---
# <a name="setting-up-business-relations-on-contacts"></a><span data-ttu-id="e7d57-103">Definere forretningsforbindelser for kontakter</span><span class="sxs-lookup"><span data-stu-id="e7d57-103">Setting Up Business Relations on Contacts</span></span>
<span data-ttu-id="e7d57-104">Du kan bruke forretningsforbindelser til å angi hvilket forretningsforhold du har til kontaktene, for eksempel prospekter, banker, konsulenter, serviceleverandører og så videre.</span><span class="sxs-lookup"><span data-stu-id="e7d57-104">You can use business relations to indicate the business relationship you have with your contacts, for example, a prospect, bank, consultant, service supplier, and so on.</span></span>

<span data-ttu-id="e7d57-105">Bruk av forretningsforbindelser på kontakter er en totrinnsprosess.</span><span class="sxs-lookup"><span data-stu-id="e7d57-105">Using business relations on contacts is a two-step process.</span></span> <span data-ttu-id="e7d57-106">Først må definere du koden for forretningsforbindelsen.</span><span class="sxs-lookup"><span data-stu-id="e7d57-106">First, you define the business relation code.</span></span> <span data-ttu-id="e7d57-107">Du trenger bare utføre dette trinnet én gang for hver forretningsforbindelse.</span><span class="sxs-lookup"><span data-stu-id="e7d57-107">You only have to perform this step one time for each business relation.</span></span> <span data-ttu-id="e7d57-108">Når du har en kode for forretningsforbindelse, kan du begynne å tilordne koden til kontaktselskaper.</span><span class="sxs-lookup"><span data-stu-id="e7d57-108">Once you have a business relation code, you can start to assign the code to contact companies.</span></span>

> [!NOTE]  
>   <span data-ttu-id="e7d57-109">Hvis du planlegger å synkronisere kontaktene med leverandører, kunder eller bankkonti i andre deler av programmet, bør du definere en forretningsforbindelse for disse.</span><span class="sxs-lookup"><span data-stu-id="e7d57-109">If you plan to synchronize your contacts with vendors, customers, or bank accounts in other parts of the application, you may want to set up a business relation for them.</span></span>

## <a name="to-define-a-business-relation-code"></a><span data-ttu-id="e7d57-110">Definere en kode for forretningsforbindelse</span><span class="sxs-lookup"><span data-stu-id="e7d57-110">To define a business relation code</span></span>
<span data-ttu-id="e7d57-111">Koden for forretningsforbindelsen definerer en kategori eller type for forretningsforbindelsen, for eksempel BANK eller Juridisk.</span><span class="sxs-lookup"><span data-stu-id="e7d57-111">The business relation code defines a category or type of the business relationship, such as BANK or Law.</span></span> <span data-ttu-id="e7d57-112">Du kan ha flere forretningsforbindelseskoder.</span><span class="sxs-lookup"><span data-stu-id="e7d57-112">You can have several business relation codes.</span></span> <span data-ttu-id="e7d57-113">Hvis du vil definere forretningsforbindelsen, bruker du siden **Forretningsforbindelser**.</span><span class="sxs-lookup"><span data-stu-id="e7d57-113">To define the business relation, you use the **Business Relations** page.</span></span>

1. <span data-ttu-id="e7d57-114">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Forretningsforbindelser**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e7d57-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Business Relations**, and then choose the related link.</span></span>
2. <span data-ttu-id="e7d57-115">Velg handlingen **Ny**, og fyll ut en kode og en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="e7d57-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="e7d57-116">Koden kan bestå av opptil 11 tegn, og kan inneholde en kombinasjon av tall og bokstaver.</span><span class="sxs-lookup"><span data-stu-id="e7d57-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="AssignBusRelContact"></a> <span data-ttu-id="e7d57-117">Tilordne forretningsforbindelser til en kontakt</span><span class="sxs-lookup"><span data-stu-id="e7d57-117">To assign business relations to a contact</span></span>
<span data-ttu-id="e7d57-118">Du kan ikke tilordne forretningsforbindelser til en kontaktperson, bare selskaper.</span><span class="sxs-lookup"><span data-stu-id="e7d57-118">You cannot assign business relations to a contact person - only companies.</span></span>

1. <span data-ttu-id="e7d57-119">Åpne kontakten.</span><span class="sxs-lookup"><span data-stu-id="e7d57-119">Open the contact.</span></span>
2. <span data-ttu-id="e7d57-120">Velg handlingen **Selskap**, og deretter handlingen **Forretningsforbindelser**.</span><span class="sxs-lookup"><span data-stu-id="e7d57-120">Choose the **Company** action, and then the **Business Relations** action.</span></span>

    <span data-ttu-id="e7d57-121">Siden **Kontaktens forretn.forbind.** åpnes.</span><span class="sxs-lookup"><span data-stu-id="e7d57-121">The **Contact Business Relations** page opens.</span></span>
3. <span data-ttu-id="e7d57-122">Velg forretningsforbindelsen du vil tilordne, i feltet **Forretn.forbindelseskode**.</span><span class="sxs-lookup"><span data-stu-id="e7d57-122">In the **Business Relation Code** field, select the business relation you want to assign.</span></span>

<span data-ttu-id="e7d57-123">Gjenta disse trinnene hvis du vil tilordne flere forretningsforbindelser.</span><span class="sxs-lookup"><span data-stu-id="e7d57-123">Repeat these steps to assign as many business relations as you want.</span></span> <span data-ttu-id="e7d57-124">Du kan også tilordne forretningsforbindelser fra kontaktlisten ved å følge samme fremgangsmåte.</span><span class="sxs-lookup"><span data-stu-id="e7d57-124">You can also assign business relations from the contact list by following the same procedure.</span></span>

<span data-ttu-id="e7d57-125">Antall forretningsforbindelser du har tilordnet kontakten, vises i feltet **Ant. forretningsforbindelser** i inndelingen **Segmentering** på siden **Kontakt**.</span><span class="sxs-lookup"><span data-stu-id="e7d57-125">The number of business relations you have assigned to the contact is displayed in the **No. of Business Relations** field in the **Segmentation** section on the **Contact** page.</span></span>

<span data-ttu-id="e7d57-126">Når du har tilordnet forretningsforbindelser til kontaktene, kan du bruke disse opplysningene til å velge kontakter for segmentene.</span><span class="sxs-lookup"><span data-stu-id="e7d57-126">After you have assigned business relations to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="e7d57-127">Hvis du vil ha mer informasjon, kan du se [Legge til kontakter i segmenter](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="e7d57-127">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e7d57-128">Se også</span><span class="sxs-lookup"><span data-stu-id="e7d57-128">See Also</span></span>
<span data-ttu-id="e7d57-129">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e7d57-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
