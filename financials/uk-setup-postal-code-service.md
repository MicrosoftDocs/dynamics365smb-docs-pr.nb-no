---
title: Konfigurere GetAddress.io UK Postcodes-utvidelsen | Microsoft-dokumentasjon
description: "Beskriver de generelle funksjonene du bruker til å arbeide med data i Financials, for eksempel angi verdier, sortere data og bytte visninger."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: getaddress.io, postcodes, extension
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c5a99f7a90b2f832bba3eb088d0faa7514c14708
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-the-getaddressio-uk-postcodes-extension"></a><span data-ttu-id="9867b-103">Konfigurere GetAddress.io UK Postcodes-utvidelsen</span><span class="sxs-lookup"><span data-stu-id="9867b-103">How to: Set Up the GetAddress.io UK Postcodes Extension</span></span>
<span data-ttu-id="9867b-104">Denne utvidelsen gjør det enkelt å angi adressene i Storbritannia for enheter som kunder, kontakter, ansatte, leverandører, bankkonti og så videre.</span><span class="sxs-lookup"><span data-stu-id="9867b-104">This extension makes it easy to enter addresses in the UK for entities like customers, contacts, employees, vendors, bank accounts, and so on.</span></span> 

<span data-ttu-id="9867b-105">GetAddress.io UK Postcodes-utvidelsen bruker getAddress API til å finne adresser i postnumre i Storbritannia.</span><span class="sxs-lookup"><span data-stu-id="9867b-105">The GetAddress.io UK Postcodes extension uses the getAddress API to find addresses in postcodes in the UK.</span></span> <span data-ttu-id="9867b-106">Hvis du vil bruke utvidelsen, må du få en plan og en API-nøkkel for getAddress API.</span><span class="sxs-lookup"><span data-stu-id="9867b-106">To use the extension, you need to get a plan and an API Key for the getAddress API.</span></span> <span data-ttu-id="9867b-107">Det er enkelt, og vi hjelper deg med å gjøre det når du setter opp GetAddress.io UK Postcodes-utvidelsen.</span><span class="sxs-lookup"><span data-stu-id="9867b-107">That's easy, and we help you do that when you set up the GetAddress.io UK Postcodes extension.</span></span> <span data-ttu-id="9867b-108">Planer er basert på bruk eller det som noen ganger blir referert til som samtaler.</span><span class="sxs-lookup"><span data-stu-id="9867b-108">Plans are based on use, or what's sometimes referred to as calls.</span></span> <span data-ttu-id="9867b-109">En samtale, i dette tilfellet er når [!INCLUDE[d365fin](includes/d365fin_md.md)] viser en liste over adresser i et postnummer.</span><span class="sxs-lookup"><span data-stu-id="9867b-109">A call, in this case, is when [!INCLUDE[d365fin](includes/d365fin_md.md)] displays a list of addresses in a postcode.</span></span> <span data-ttu-id="9867b-110">Avhengig av hvor ofte du legger til adresser, velger du planen som passer best for deg.</span><span class="sxs-lookup"><span data-stu-id="9867b-110">Depending on how often you add addresses, choose the plan that is best for you.</span></span> <span data-ttu-id="9867b-111">Hvis du velger **Få API-nøkkel** på siden, bruker du **Ledig**-planen, som lar deg legge til 20 adresser per dag, og som er gyldig i 30 dager.</span><span class="sxs-lookup"><span data-stu-id="9867b-111">If you just choose **Get API Key** in the page, you'll use the **Free** plan, which lets you add 20 addresses per day, and is valid for 30 days.</span></span> 

##<a name="to-set-up-the-getaddressio-uk-postcodes-extension"></a><span data-ttu-id="9867b-112">Konfigurere GetAddress.io UK Postcodes-utvidelsen</span><span class="sxs-lookup"><span data-stu-id="9867b-112">To set up the GetAddress.io UK Postcodes extension</span></span> 
1. <span data-ttu-id="9867b-113">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Tjenestetilkoblinger**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="9867b-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Connections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9867b-114">I vinduet **Tjenestetilkoblinger** velger du **UK Postcode Service**.</span><span class="sxs-lookup"><span data-stu-id="9867b-114">In the **Service Connections** window, choose **UK Postcode Service**.</span></span>
3. <span data-ttu-id="9867b-115">På siden **Konfigurasjon av postnummerleverandør** velger du **Deaktivert**.</span><span class="sxs-lookup"><span data-stu-id="9867b-115">In the **Postcode provider configuration** page, choose **Disabled**.</span></span>
4. <span data-ttu-id="9867b-116">I vinduet **Valg av postnummertjeneste** velger du **GetAddress.io**.</span><span class="sxs-lookup"><span data-stu-id="9867b-116">In the **Postal code service selection** window, choose **GetAddress.io**.</span></span>
5. <span data-ttu-id="9867b-117">I vinduet **GetAddress.io Config** velger du **Få API-nøkkel** for å åpne **Planer**-siden på nettstedet for getAddress API.</span><span class="sxs-lookup"><span data-stu-id="9867b-117">In the **GetAddress.io Config** window, choose **Get API Key** to open the **Plans** page on the website for the getAddress API.</span></span>  

    > [!NOTE]  
>   <span data-ttu-id="9867b-118">Du må kanskje tillate popup-vinduer i nettleseren.</span><span class="sxs-lookup"><span data-stu-id="9867b-118">You might need to allow pop-ups in your browser.</span></span>
6. <span data-ttu-id="9867b-119">Kjøp en plan, eller velg bare **Få API-nøkkel**, og angi e-postadressen din.</span><span class="sxs-lookup"><span data-stu-id="9867b-119">Purchase a plan, or just choose **Get API Key**, and then provide your email address.</span></span>
7. <span data-ttu-id="9867b-120">Åpne e-postmeldingen fra getAddress.io, og kopier API-nøkkelen.</span><span class="sxs-lookup"><span data-stu-id="9867b-120">Open the email from getAddress.io, and copy the API key.</span></span> <span data-ttu-id="9867b-121">Nøkkelen er under overskriften **Din API-nøkkel**.</span><span class="sxs-lookup"><span data-stu-id="9867b-121">The key is under the **Your API Key** heading.</span></span>
8. <span data-ttu-id="9867b-122">I vinduet **GetAddress.io Config** limer du inn API-nøkkelen i feltet **API-nøkkel** og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="9867b-122">In the **GetAddress.io Config** window, paste the API key in the **API Key** field, and then choose **OK**.</span></span>
9. <span data-ttu-id="9867b-123">På siden **Tjenestetilkoblinger** må du kontrollere at feltet **Adresseleverandør** viser **GetAddress.io**.</span><span class="sxs-lookup"><span data-stu-id="9867b-123">In the **Service Connections** page, verify that the **Address Provider** field shows **GetAddress.io**.</span></span> <span data-ttu-id="9867b-124">I så fall er tjenesten aktivert.</span><span class="sxs-lookup"><span data-stu-id="9867b-124">If it does, the service is enabled.</span></span>

## <a name="see-also"></a><span data-ttu-id="9867b-125">Se også</span><span class="sxs-lookup"><span data-stu-id="9867b-125">See Also</span></span>
<span data-ttu-id="9867b-126">[GetAddress.io UK Postcodes](ui-extensions-getaddressio.md)
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="9867b-126">[GetAddress.io UK Postcodes](ui-extensions-getaddressio.md)
[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="9867b-127">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9867b-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
