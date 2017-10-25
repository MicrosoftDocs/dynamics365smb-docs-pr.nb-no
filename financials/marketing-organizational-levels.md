---
title: "Definere organisasjonsnivåer for kontaktpersoner | Microsoft-dokumentasjon"
description: "Du kan definere et organisasjonsnivå og tilordne det til kontakten for å angi hvilken stilling de har i selskapet sitt, for eksempel en stilling i toppledelsen."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d101076c8a51b1c7a79606d207f79a826c89bf29
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-organizational-levels-for-contact-persons"></a><span data-ttu-id="e514f-103">Definere organisasjonsnivåer for kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="e514f-103">How to: Set Up Organizational Levels for Contact Persons</span></span>
<span data-ttu-id="e514f-104">Du kan bruke organisasjonsnivåer på kontaktene for å angi hvilken stilling de har i selskapet, for eksempel en stilling i toppledelsen.</span><span class="sxs-lookup"><span data-stu-id="e514f-104">You can use organizational levels on your contacts to specify which position they have in the company, for example, top management.</span></span> <span data-ttu-id="e514f-105">Du kan bruke denne informasjonen når du oppgir opplysninger om kontaktene.</span><span class="sxs-lookup"><span data-stu-id="e514f-105">You can use this information when entering information about your contacts.</span></span>

<span data-ttu-id="e514f-106">Bruk av organisasjonsnivåer på kontakter er en totrinnsprosess.</span><span class="sxs-lookup"><span data-stu-id="e514f-106">Using organizational levels on contacts is a two-step process.</span></span> <span data-ttu-id="e514f-107">Først må du definere koden for organisasjonsnivået.</span><span class="sxs-lookup"><span data-stu-id="e514f-107">First, you define the organizational level code.</span></span> <span data-ttu-id="e514f-108">Du trenger bare utføre dette trinnet én gang for hvert organisasjonsnivå.</span><span class="sxs-lookup"><span data-stu-id="e514f-108">You only have to perform this step one time for each organizational level.</span></span> <span data-ttu-id="e514f-109">Når du har en kode for organisasjonsnivå, kan du begynne å tilordne koden til kontaktpersoner.</span><span class="sxs-lookup"><span data-stu-id="e514f-109">Once you have an organizational level code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-an-organizational-level-code"></a><span data-ttu-id="e514f-110">Slik definerer du en kode for organisasjonsnivå</span><span class="sxs-lookup"><span data-stu-id="e514f-110">To define an organizational level code</span></span>
<span data-ttu-id="e514f-111">Koden for organisasjonsnivå definerer jobbtype eller -kategori for organisasjonsnivået, for eksempel ADMDIR eller ØKDIR.</span><span class="sxs-lookup"><span data-stu-id="e514f-111">The organizational level code defines the type or category of the organizational level, such a CEO  or CFO.</span></span> <span data-ttu-id="e514f-112">Du kan ha flere koder for organisasjonsnivå.</span><span class="sxs-lookup"><span data-stu-id="e514f-112">You can have several organizational level codes.</span></span> <span data-ttu-id="e514f-113">Hvis du vil definere organisasjonsnivået, bruker du vinduet **Organisasjonsnivåer**.</span><span class="sxs-lookup"><span data-stu-id="e514f-113">To define the organizational level, you use the **Organizational Levels** window.</span></span>

1. <span data-ttu-id="e514f-114">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Organisasjonsnivåer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e514f-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Organizational Levels**, and then choose the related link.</span></span>
2. <span data-ttu-id="e514f-115">Velg handlingen **Ny**, og fyll ut en kode og en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="e514f-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="e514f-116">Koden kan bestå av opptil 11 tegn, og kan inneholde en kombinasjon av tall og bokstaver.</span><span class="sxs-lookup"><span data-stu-id="e514f-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="to-assign-organizational-levels-to-a-contact-person"></a><span data-ttu-id="e514f-117">Slik tilordner du organisasjonsnivåer til en kontaktperson</span><span class="sxs-lookup"><span data-stu-id="e514f-117">To assign organizational levels to a contact person</span></span>
<span data-ttu-id="e514f-118">Du kan bare tilordne organisasjonsnivåer til kontaktpersoner, ikke selskaper.</span><span class="sxs-lookup"><span data-stu-id="e514f-118">You can assign organizational levels to contact persons only, not contact companies.</span></span> <span data-ttu-id="e514f-119">Du kan bare tilordne ett organisasjonsnivå til hver enkelt kontakt.</span><span class="sxs-lookup"><span data-stu-id="e514f-119">You can only assign one organizational level to each contact.</span></span>

1. <span data-ttu-id="e514f-120">Åpne kontakten.</span><span class="sxs-lookup"><span data-stu-id="e514f-120">Open the contact.</span></span>
2. <span data-ttu-id="e514f-121">I feltet **Organisasjonsnivåer** velger du koden du vil tilordne.</span><span class="sxs-lookup"><span data-stu-id="e514f-121">In the **Organizational Levels** field, select the code you want to assign.</span></span>

<span data-ttu-id="e514f-122">Når du har tildelt organisasjonsnivåer til kontaktene, kan du bruke disse opplysningene til å opprette segmenter.</span><span class="sxs-lookup"><span data-stu-id="e514f-122">After you have assigned organizational levels to your contacts, you can use this information to create segments.</span></span>

<span data-ttu-id="e514f-123">Når du har tilordnet ansvarsområder til kontaktene, kan du bruke disse opplysningene til å velge kontakter for segmentene.</span><span class="sxs-lookup"><span data-stu-id="e514f-123">After you have assigned job responsibilities to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="e514f-124">Hvis du vil ha mer informasjon, kan du se [Legge til kontakter i segmenter](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="e514f-124">For more information, see [How to: Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e514f-125">Se også</span><span class="sxs-lookup"><span data-stu-id="e514f-125">See Also</span></span>
[<span data-ttu-id="e514f-126">Opprette kontaktselskaper</span><span class="sxs-lookup"><span data-stu-id="e514f-126">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="e514f-127">Opprette kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="e514f-127">Creating Contact Persons</span></span>](marketing-create-contact-persons.md)  
<span data-ttu-id="e514f-128">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e514f-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

