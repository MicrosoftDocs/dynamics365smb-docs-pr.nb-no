---
title: Definere webkilder for kontaktselskaper | Microsoft-dokumentasjon
description: Du kan definere Internett-kilder eller webkilder og tilordne dem til et kontaktselskap for å bidra til å identifisere hvor du vil søke etter informasjon om kontaktene.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: aa5998b989d8a3d37f3d7bfcdb348a2c09381168
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "934399"
---
# <a name="set-up-web-sources-for-contact-companies"></a><span data-ttu-id="a7ac1-103">Definere webkilder for kontaktselskaper</span><span class="sxs-lookup"><span data-stu-id="a7ac1-103">Set Up Web Sources for Contact Companies</span></span>
<span data-ttu-id="a7ac1-104">Du kan for eksempel bruke webkilder med kontaktselskaper for å identifisere søkemotorer og webområder på Internett, som du vil bruke til å søke etter informasjon om kontaktene.</span><span class="sxs-lookup"><span data-stu-id="a7ac1-104">You can use web sources with your contact companies to identify, for example, search engines and web sites, on the Internet that you want to use to search for information about the contacts.</span></span> <span data-ttu-id="a7ac1-105">Når du tilordner webkilder, angir du hvilken søkemotor og søkeord programmet skal bruke for å finne de forespurte opplysningene.</span><span class="sxs-lookup"><span data-stu-id="a7ac1-105">When assigning web sources, you specify which search engine and search word the application will use to find the requested information.</span></span>

<span data-ttu-id="a7ac1-106">Bruk av webkilder på kontakter er en totrinnsprosess.</span><span class="sxs-lookup"><span data-stu-id="a7ac1-106">Using web sources on contacts is a two-step process.</span></span> <span data-ttu-id="a7ac1-107">Først må du definere koden for webkilden.</span><span class="sxs-lookup"><span data-stu-id="a7ac1-107">First, you define the web source code.</span></span> <span data-ttu-id="a7ac1-108">Du trenger bare utføre dette trinnet én gang for hver webkilde.</span><span class="sxs-lookup"><span data-stu-id="a7ac1-108">You only have to perform this step one time for each web source.</span></span> <span data-ttu-id="a7ac1-109">Når du har en kode for webkilde, kan du begynne å tilordne koden til kontaktpersoner.</span><span class="sxs-lookup"><span data-stu-id="a7ac1-109">Once you have a web source code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-a-web-source-code"></a><span data-ttu-id="a7ac1-110">Slik definerer du en kode for webkilde</span><span class="sxs-lookup"><span data-stu-id="a7ac1-110">To define a web source code</span></span>
1. <span data-ttu-id="a7ac1-111">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Webkilder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a7ac1-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Sources**, and then choose the related link.</span></span>
2. <span data-ttu-id="a7ac1-112">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a7ac1-112">Choose the **New** actions.</span></span>
3. <span data-ttu-id="a7ac1-113">Fyll ut feltene **Kode**, **Beskrivelse** og **URL**.</span><span class="sxs-lookup"><span data-stu-id="a7ac1-113">Fill in the **Code**, **Description**, and **URL** fields.</span></span>

    <span data-ttu-id="a7ac1-114">Skriv inn %1 i feltet **URL-adresse** for å sette inn en plassholder for et søkeord i nettadressen.</span><span class="sxs-lookup"><span data-stu-id="a7ac1-114">Type %1 in the **URL** field to insert a placeholder for a search word in the URL.</span></span> <span data-ttu-id="a7ac1-115">Når du starter webkilden fra et kontaktkort, erstattes %1 med søkeordet (for eksempel navnet på selskapet) som du angav på siden **Kontaktens webkilder**.</span><span class="sxs-lookup"><span data-stu-id="a7ac1-115">When you launch the web source from a contact, the %1 is replaced with the search word, for example, the name of the company that you have entered on the **Contact Web Sources** page.</span></span>

<span data-ttu-id="a7ac1-116">Gjenta disse trinnene hvis du vil definere flere webkilder.</span><span class="sxs-lookup"><span data-stu-id="a7ac1-116">Repeat these steps to set up as many web sources as you want.</span></span>

## <a name="to-assign-web-sources-to-a-contact-company"></a><span data-ttu-id="a7ac1-117">Slik tilordner du webkilder til et kontaktselskap</span><span class="sxs-lookup"><span data-stu-id="a7ac1-117">To assign web sources to a contact company</span></span>
<span data-ttu-id="a7ac1-118">Når du tilordner webkilder, angir du hvilken søkemotor og søkeord som programmet skal bruke for å finne de forespurte opplysningene.</span><span class="sxs-lookup"><span data-stu-id="a7ac1-118">When assigning web sources, you specify which search engine and search word that the application will use to find the requested information.</span></span>

1. <span data-ttu-id="a7ac1-119">Åpne kontakten.</span><span class="sxs-lookup"><span data-stu-id="a7ac1-119">Open the contact.</span></span>
2. <span data-ttu-id="a7ac1-120">Velg handlingen **Selskap**, og velg deretter handlingen **Webkilder**.</span><span class="sxs-lookup"><span data-stu-id="a7ac1-120">Choose the **Company** action, and then choose the **Web Sources** action.</span></span> <span data-ttu-id="a7ac1-121">Siden **Kontaktens webkilder** åpnes.</span><span class="sxs-lookup"><span data-stu-id="a7ac1-121">The **Contact Web Sources** page opens.</span></span>
3. <span data-ttu-id="a7ac1-122">Velg webkilden du vil tilordne i feltet **Webkilde - kode**.</span><span class="sxs-lookup"><span data-stu-id="a7ac1-122">In the **Web Source Code** field, choose the web source you want to assign.</span></span>
4. <span data-ttu-id="a7ac1-123">I feltet **Søkeord** angir du et søkeord som du vil bruke for å finne opplysningene.</span><span class="sxs-lookup"><span data-stu-id="a7ac1-123">In the **Search Word** field, enter the search word that you want to use to find the information.</span></span>

<span data-ttu-id="a7ac1-124">Gjenta disse trinnene hvis du vil tilordne flere webkilder.</span><span class="sxs-lookup"><span data-stu-id="a7ac1-124">Repeat these steps to assign as many web sources as you want.</span></span>

<span data-ttu-id="a7ac1-125">Ved å følge samme fremgangsmåte kan du også tilordne webkilder på siden **Kontaktoversikt**.</span><span class="sxs-lookup"><span data-stu-id="a7ac1-125">You can also assign web sources from the **Contact List** page by following the same procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="a7ac1-126">Se også</span><span class="sxs-lookup"><span data-stu-id="a7ac1-126">See Also</span></span>
[<span data-ttu-id="a7ac1-127">Opprette kontakter</span><span class="sxs-lookup"><span data-stu-id="a7ac1-127">Creating Contacts</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="a7ac1-128">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a7ac1-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
