---
title: Definere webkilder for kontaktselskaper | Microsoft-dokumentasjon
description: "Du kan definere Internett-kilder eller webkilder og tilordne dem til et kontaktselskap for å bidra til å identifisere hvor du vil søke etter informasjon om kontaktene."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: b8c59f24eae07efe8f2c4ca1e4e22d05fd4f1b1c
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-web-sources-for-contact-companies"></a><span data-ttu-id="675b6-103">Definere webkilder for kontaktselskaper</span><span class="sxs-lookup"><span data-stu-id="675b6-103">Set Up Web Sources for Contact Companies</span></span>
<span data-ttu-id="675b6-104">Du kan for eksempel bruke webkilder med kontaktselskaper for å identifisere søkemotorer og webområder på Internett, som du vil bruke til å søke etter informasjon om kontaktene.</span><span class="sxs-lookup"><span data-stu-id="675b6-104">You can use web sources with your contact companies to identify, for example, search engines and web sites, on the Internet that you want to use to search for information about the contacts.</span></span> <span data-ttu-id="675b6-105">Når du tilordner webkilder, angir du hvilken søkemotor og søkeord programmet skal bruke for å finne de forespurte opplysningene.</span><span class="sxs-lookup"><span data-stu-id="675b6-105">When assigning web sources, you specify which search engine and search word the application will use to find the requested information.</span></span>

<span data-ttu-id="675b6-106">Bruk av webkilder på kontakter er en totrinnsprosess.</span><span class="sxs-lookup"><span data-stu-id="675b6-106">Using web sources on contacts is a two-step process.</span></span> <span data-ttu-id="675b6-107">Først må du definere koden for webkilden.</span><span class="sxs-lookup"><span data-stu-id="675b6-107">First, you define the web source code.</span></span> <span data-ttu-id="675b6-108">Du trenger bare utføre dette trinnet én gang for hver webkilde.</span><span class="sxs-lookup"><span data-stu-id="675b6-108">You only have to perform this step one time for each web source.</span></span> <span data-ttu-id="675b6-109">Når du har en kode for webkilde, kan du begynne å tilordne koden til kontaktpersoner.</span><span class="sxs-lookup"><span data-stu-id="675b6-109">Once you have a web source code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-a-web-source-code"></a><span data-ttu-id="675b6-110">Slik definerer du en kode for webkilde</span><span class="sxs-lookup"><span data-stu-id="675b6-110">To define a web source code</span></span>
1. <span data-ttu-id="675b6-111">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Webkilder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="675b6-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Sources**, and then choose the related link.</span></span>
2. <span data-ttu-id="675b6-112">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="675b6-112">Choose the **New** actions.</span></span>
3. <span data-ttu-id="675b6-113">Fyll ut feltene **Kode**, **Beskrivelse** og **URL**.</span><span class="sxs-lookup"><span data-stu-id="675b6-113">Fill in the **Code**, **Description**, and **URL** fields.</span></span>

    <span data-ttu-id="675b6-114">Skriv inn %1 i feltet **Nettadresse** for å sette inn en plassholder for et søkeord i nettadressen.</span><span class="sxs-lookup"><span data-stu-id="675b6-114">Type %1 in the **URL** field to insert a placeholder for a search word in the URL.</span></span> <span data-ttu-id="675b6-115">Når du starter webkilden fra et kontaktkort, erstattes %1 med søkeordet (for eksempel navnet på selskapet) som du angav i vinduet **Kontaktens webkilder**.</span><span class="sxs-lookup"><span data-stu-id="675b6-115">When you launch the web source from a contact, the %1 is replaced with the search word, for example, the name of the company that you have entered in the **Contact Web Sources** window.</span></span>

<span data-ttu-id="675b6-116">Gjenta disse trinnene hvis du vil definere flere webkilder.</span><span class="sxs-lookup"><span data-stu-id="675b6-116">Repeat these steps to set up as many web sources as you want.</span></span>

## <a name="to-assign-web-sources-to-a-contact-company"></a><span data-ttu-id="675b6-117">Slik tilordner du webkilder til et kontaktselskap</span><span class="sxs-lookup"><span data-stu-id="675b6-117">To assign web sources to a contact company</span></span>
<span data-ttu-id="675b6-118">Når du tilordner webkilder, angir du hvilken søkemotor og søkeord som programmet skal bruke for å finne de forespurte opplysningene.</span><span class="sxs-lookup"><span data-stu-id="675b6-118">When assigning web sources, you specify which search engine and search word that the application will use to find the requested information.</span></span>

1. <span data-ttu-id="675b6-119">Åpne kontakten.</span><span class="sxs-lookup"><span data-stu-id="675b6-119">Open the contact.</span></span>
2. <span data-ttu-id="675b6-120">Velg handlingen **Selskap**, og velg deretter handlingen **Webkilder**.</span><span class="sxs-lookup"><span data-stu-id="675b6-120">Choose the **Company** action, and then choose the **Web Sources** action.</span></span> <span data-ttu-id="675b6-121">Vinduet **Kontaktens webkilder** åpnes.</span><span class="sxs-lookup"><span data-stu-id="675b6-121">The **Contact Web Sources** window opens.</span></span>
3. <span data-ttu-id="675b6-122">Velg webkilden du vil tilordne i feltet **Webkilde - kode**.</span><span class="sxs-lookup"><span data-stu-id="675b6-122">In the **Web Source Code** field, choose the web source you want to assign.</span></span>
4. <span data-ttu-id="675b6-123">I feltet **Søkeord** angir du et søkeord som du vil bruke for å finne opplysningene.</span><span class="sxs-lookup"><span data-stu-id="675b6-123">In the **Search Word** field, enter the search word that you want to use to find the information.</span></span>

<span data-ttu-id="675b6-124">Gjenta disse trinnene hvis du vil tilordne flere webkilder.</span><span class="sxs-lookup"><span data-stu-id="675b6-124">Repeat these steps to assign as many web sources as you want.</span></span>

<span data-ttu-id="675b6-125">Ved å følge samme fremgangsmåte kan du også tilordne webkilder fra vinduet **Kontaktoversikt**.</span><span class="sxs-lookup"><span data-stu-id="675b6-125">You can also assign web sources from the **Contact List** window by following the same procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="675b6-126">Se også</span><span class="sxs-lookup"><span data-stu-id="675b6-126">See Also</span></span>
[<span data-ttu-id="675b6-127">Opprette kontaktselskaper</span><span class="sxs-lookup"><span data-stu-id="675b6-127">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="675b6-128">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="675b6-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

