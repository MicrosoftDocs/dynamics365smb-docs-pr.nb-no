---
title: Definere postgrupper for kontakter | Microsoft-dokumentasjon
description: "Du kan bruke postgrupper til å identifisere grupper med kontakter du vil skal motta samme informasjon, for eksempel for en markedsføringskampanje."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 92173c1df5f105ad9156c34ab7050ef1546127bc
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-mailing-groups-for-contacts"></a><span data-ttu-id="f96ff-103">Definere postgrupper for kontakter</span><span class="sxs-lookup"><span data-stu-id="f96ff-103">Set Up Mailing Groups for Contacts</span></span>
<span data-ttu-id="f96ff-104">Du kan bruke postgrupper til å identifisere grupper av kontakter som du ønsker skal motta like opplysninger.</span><span class="sxs-lookup"><span data-stu-id="f96ff-104">You can use mailing groups to identify groups of contacts that you want to receive the same information.</span></span> <span data-ttu-id="f96ff-105">Du kan for eksempel definere en postgruppe for kontaktene du vil sende en melding om kontorflytting til, eller en annen gruppe for sending av julegavene.</span><span class="sxs-lookup"><span data-stu-id="f96ff-105">For example, you can set up a mailing group for the contacts that you want to send a notification of an office move, or another group for sending holiday gifts.</span></span>

<span data-ttu-id="f96ff-106">Bruk av postgrupper på kontakter er en totrinnsprosess.</span><span class="sxs-lookup"><span data-stu-id="f96ff-106">Using mailing groups on contacts is a two-step process.</span></span> <span data-ttu-id="f96ff-107">Først må definere du koden for postgruppen.</span><span class="sxs-lookup"><span data-stu-id="f96ff-107">First, you define the mailing group code.</span></span> <span data-ttu-id="f96ff-108">Du trenger bare utføre dette trinnet én gang for hver postgruppe.</span><span class="sxs-lookup"><span data-stu-id="f96ff-108">You only have to perform this step one time for each mailing group.</span></span> <span data-ttu-id="f96ff-109">Når du har en kode for postgruppe, kan du begynne å tilordne koden til kontaktselskaper.</span><span class="sxs-lookup"><span data-stu-id="f96ff-109">Once you have a mailing group code, you can start to assign the code to contact companies.</span></span>

## <a name="to-define-mailing-group-codes"></a><span data-ttu-id="f96ff-110">Definere postgruppekoder</span><span class="sxs-lookup"><span data-stu-id="f96ff-110">To define mailing group codes</span></span>
<span data-ttu-id="f96ff-111">Koden for postgruppen definerer typen eller kategori for gruppen, for eksempel FLYTTE for kontorflytting eller GAVE julegave.</span><span class="sxs-lookup"><span data-stu-id="f96ff-111">The mailing group code defines the type or category of the group, such as MOVE for office move, or GIFT for holiday gift.</span></span> <span data-ttu-id="f96ff-112">Du kan ha flere koder for bransjegruppe.</span><span class="sxs-lookup"><span data-stu-id="f96ff-112">You can have several industry group codes.</span></span> <span data-ttu-id="f96ff-113">Hvis du vil definere bransjegrupper, bruker du vinduet **Postgrupper**.</span><span class="sxs-lookup"><span data-stu-id="f96ff-113">To define the industry groups, you use the **Mailing Groups** window.</span></span>

1. <span data-ttu-id="f96ff-114">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Postgrupper**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="f96ff-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Mailing Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="f96ff-115">Velg handlingen **Ny**, og fyll ut en kode og en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f96ff-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="f96ff-116">Koden kan bestå av opptil 11 tegn, og kan inneholde en kombinasjon av tall og bokstaver.</span><span class="sxs-lookup"><span data-stu-id="f96ff-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="AssignMailGroupContact"></a> <span data-ttu-id="f96ff-117">Slik tilordner du postgrupper til en kontakt</span><span class="sxs-lookup"><span data-stu-id="f96ff-117">To assign mailing groups to a contact</span></span>
1. <span data-ttu-id="f96ff-118">Åpne kontakten.</span><span class="sxs-lookup"><span data-stu-id="f96ff-118">Open the contact.</span></span>
2. <span data-ttu-id="f96ff-119">Velg handlingen **Postgrupper**.</span><span class="sxs-lookup"><span data-stu-id="f96ff-119">Choose the **Mailing Groups** action.</span></span> <span data-ttu-id="f96ff-120">Vinduet **Kontaktens postgrupper** åpnes.</span><span class="sxs-lookup"><span data-stu-id="f96ff-120">The **Contact Mailing Groups** window opens.</span></span>
3. <span data-ttu-id="f96ff-121">Velg postgruppen du vil tilordne, i feltet **Postgruppekode**.</span><span class="sxs-lookup"><span data-stu-id="f96ff-121">In the **Mailing Groups Code** field, select the mailing group that you want to assign.</span></span>

<span data-ttu-id="f96ff-122">Gjenta disse trinnene hvis du vil tilordne flere postgrupper.</span><span class="sxs-lookup"><span data-stu-id="f96ff-122">Repeat these steps to assign as many mailing groups as you want.</span></span> <span data-ttu-id="f96ff-123">Ved å følge samme fremgangsmåte kan du også tilordne postgrupper fra kontaktlisten.</span><span class="sxs-lookup"><span data-stu-id="f96ff-123">You can also assign mailing groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="f96ff-124">Antallet postgrupper du har tilordnet kontakten, vises i feltet **Ant. postgrupper** i inndelingen **Segmentering** i vinduet **Kontakt**.</span><span class="sxs-lookup"><span data-stu-id="f96ff-124">The number of mailing groups you have assigned to the contact is displayed in the **No. of Mailing Groups** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="f96ff-125">Når du har tilordnet postgrupper til kontaktene, kan du bruke disse opplysningene til å velge kontakter for segmentene.</span><span class="sxs-lookup"><span data-stu-id="f96ff-125">After you have assigned mailing groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="f96ff-126">Hvis du vil ha mer informasjon, kan du se [Legge til kontakter i segmenter](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="f96ff-126">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f96ff-127">Se også</span><span class="sxs-lookup"><span data-stu-id="f96ff-127">See Also</span></span>
[<span data-ttu-id="f96ff-128">Opprette kontaktselskaper</span><span class="sxs-lookup"><span data-stu-id="f96ff-128">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="f96ff-129">Opprette kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="f96ff-129">Creating Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="f96ff-130">Arbeide med Financials</span><span class="sxs-lookup"><span data-stu-id="f96ff-130">Working with Financials</span></span>](ui-work-product.md)

