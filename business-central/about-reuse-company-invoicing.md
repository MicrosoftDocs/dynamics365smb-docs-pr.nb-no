---
title: Bruke fakturering og Business Central | Microsoft-dokumentasjon
description: "Løsning for å få tilgang til Microsoft Invoicing når du har registrert deg for Dynamics 365 Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 917887deae163a76b233e1635344e537806f6215
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="using-the-same-office-365-account-in-included365finincludesd365finlongmdmd-and-microsoft-invoicing"></a><span data-ttu-id="25be9-103">Bruke samme Office 365-konto i [!INCLUDE[d365fin](includes/d365fin_long_md.md)] og Microsoft Invoicing</span><span class="sxs-lookup"><span data-stu-id="25be9-103">Using the same Office 365 Account in [!INCLUDE[d365fin](includes/d365fin_long_md.md)] and Microsoft Invoicing</span></span>
<span data-ttu-id="25be9-104">Når du registrerer deg for en prøveversjon med [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du flytte over til en 30 dager evalueringsfase, du kan du starte et abonnement eller du kan slutte å bruke [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="25be9-104">When you sign up for a trial with [!INCLUDE[d365fin](includes/d365fin_md.md)], you can move to a 30-day evaluation phase, you can start a subscription, or you can stop using [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="25be9-105">I alle tilfellene, hvis du logger på Office-portalen, kan du se en rute som kalles **Business Center** og klikke den.</span><span class="sxs-lookup"><span data-stu-id="25be9-105">In all cases, if you log into the Office Portal, you might see a tile called **Business center** and click it.</span></span> <span data-ttu-id="25be9-106">Dette er en del av Office 365 Business Premium-abonnementet, så ikke alle ser denne ruten i Office-portalen.</span><span class="sxs-lookup"><span data-stu-id="25be9-106">This is part of the Office 365 Business Premium subscription, so not everyone will see that tile in the Office Portal.</span></span>  

<span data-ttu-id="25be9-107">Hvis du ikke har tilgang til forretningssenteret, ser du en del kalt **Fakturering**.</span><span class="sxs-lookup"><span data-stu-id="25be9-107">If you do access the Business center, you will see a section called **Invoicing**.</span></span> <span data-ttu-id="25be9-108">Hvis du åpner denne delen, vises en melding om at du ikke har tilgang til Microsoft Invoicing fordi kontoen brukes i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="25be9-108">If you access that section, you will see a message that you cannot access Microsoft Invoicing because your account is used in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="25be9-109">Det vises en lignende melding hvis du installerer mobilappen for fakturering.</span><span class="sxs-lookup"><span data-stu-id="25be9-109">You see a similar message if you install the mobile app for Invoicing.</span></span>  

## <a name="workaround"></a><span data-ttu-id="25be9-110">Løsning</span><span class="sxs-lookup"><span data-stu-id="25be9-110">Workaround</span></span>
<span data-ttu-id="25be9-111">Fakturering og [!INCLUDE[d365fin](includes/d365fin_md.md)] har en delt plattform.</span><span class="sxs-lookup"><span data-stu-id="25be9-111">Invoicing and [!INCLUDE[d365fin](includes/d365fin_md.md)] have a shared platform.</span></span> <span data-ttu-id="25be9-112">Dette innebærer at du gjenkjennes som en eksisterende bruker av [!INCLUDE[d365fin](includes/d365fin_md.md)] når du klikker på fakturering i forretningssenteret.</span><span class="sxs-lookup"><span data-stu-id="25be9-112">That means that you are recognized as an existing user of [!INCLUDE[d365fin](includes/d365fin_md.md)] when you click Invoicing in the Business center.</span></span> <span data-ttu-id="25be9-113">Årsaken er at fakturering ikke kan bruke det samme selskapet som [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="25be9-113">The reason is that Invoicing cannot use the same company as [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="25be9-114">Så du må logge på [!INCLUDE[d365fin](includes/d365fin_md.md)] og gi nytt navn til det eksisterende selskapet ditt, og deretter opprette et nytt selskap som du deretter kan bruke i fakturering.</span><span class="sxs-lookup"><span data-stu-id="25be9-114">So you will have to log into [!INCLUDE[d365fin](includes/d365fin_md.md)] and rename your existing company, and then create a new company that you can then use in Invoicing.</span></span> <span data-ttu-id="25be9-115">Ingen data flyttes eller overskrives i denne løsningen.</span><span class="sxs-lookup"><span data-stu-id="25be9-115">No data is moved or overwritten during this workaround.</span></span>

### <a name="to-rename-your-company"></a><span data-ttu-id="25be9-116">Slik endrer du navn på selskapet</span><span class="sxs-lookup"><span data-stu-id="25be9-116">To rename your company</span></span>
1.  <span data-ttu-id="25be9-117">Logg på [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="25be9-117">Sign in to your [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
2.  <span data-ttu-id="25be9-118">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Selskaper**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="25be9-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Companies**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="25be9-119">I **Selskaper**-vinduet velger du **Rediger oversikt**-knappen.</span><span class="sxs-lookup"><span data-stu-id="25be9-119">In the **Companies** window, choose the **Edit List** button.</span></span>  
4.  <span data-ttu-id="25be9-120">Endre navnet i *Mitt selskap*-posten til et annet navn.</span><span class="sxs-lookup"><span data-stu-id="25be9-120">Change the name of the *My Company* entry to something else.</span></span>  

    <span data-ttu-id="25be9-121">Vent noen minutter.</span><span class="sxs-lookup"><span data-stu-id="25be9-121">Wait a number of minutes.</span></span> <span data-ttu-id="25be9-122">Vi kan foreta flere endringer i den underliggende databasen, og det tar litt tid.</span><span class="sxs-lookup"><span data-stu-id="25be9-122">We’ll be making a number of changes in the underlying database, and that takes a while.</span></span>
5.  <span data-ttu-id="25be9-123">Når systemet er klart igjen, velger du **Opprett et nytt selskap**-knappen.</span><span class="sxs-lookup"><span data-stu-id="25be9-123">When the system is ready again, choose the **Create New Company** button.</span></span>  
6.  <span data-ttu-id="25be9-124">I dialogboksen som vises, angir du navnet som *Mitt selskap*, og velger **Produksjon - Bare oppsettsdata**-alternativet.</span><span class="sxs-lookup"><span data-stu-id="25be9-124">In the dialog that appears, specify the name as *My Company*, and choose the **Production – Setup Data Only** option.</span></span>  

<span data-ttu-id="25be9-125">Dette tar også flere minutter.</span><span class="sxs-lookup"><span data-stu-id="25be9-125">This again takes a number of minutes.</span></span> <span data-ttu-id="25be9-126">Når prosessen er fullført, får du tilgang til fakturering som en del av Office 365 Business Premium-opplevelsen.</span><span class="sxs-lookup"><span data-stu-id="25be9-126">When the process completes, you will be able to access Invoicing as part of your Office 365 Business Premium experience.</span></span>  

### <a name="what-about-my-data"></a><span data-ttu-id="25be9-127">Hva med dataene mine?</span><span class="sxs-lookup"><span data-stu-id="25be9-127">What about my data?</span></span>
<span data-ttu-id="25be9-128">Når du endrer navn på det opprinnelige Mitt selskap, får databasetabellene som lagrer dine eksisterende [!INCLUDE[d365fin](includes/d365fin_md.md)]-data nye navn, men selve dataene røres ikke.</span><span class="sxs-lookup"><span data-stu-id="25be9-128">When you rename the original My Company, the database tables that store your existing [!INCLUDE[d365fin](includes/d365fin_md.md)] data are renamed, but the data itself is not touched.</span></span>  

<span data-ttu-id="25be9-129">Hvis du bruker både fakturering og [!INCLUDE[d365fin](includes/d365fin_md.md)], lagres dataene i to forskjellige beholdere (de to selskapene).</span><span class="sxs-lookup"><span data-stu-id="25be9-129">If you use both Invoicing and [!INCLUDE[d365fin](includes/d365fin_md.md)], the data is stored in two different containers (the two companies).</span></span> <span data-ttu-id="25be9-130">Ingenting deles, slik at du må administrere kunder og varer i begge selskapene.</span><span class="sxs-lookup"><span data-stu-id="25be9-130">Nothing is shared, so you'll have to manage customers and items in both companies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="25be9-131">Se også</span><span class="sxs-lookup"><span data-stu-id="25be9-131">See Also</span></span>
[<span data-ttu-id="25be9-132">Vanlige spørsmål</span><span class="sxs-lookup"><span data-stu-id="25be9-132">Frequently Asked Questions</span></span>](across-faq.md)  
[<span data-ttu-id="25be9-133">Administrasjon</span><span class="sxs-lookup"><span data-stu-id="25be9-133">Administration</span></span>](admin-setup-and-administration.md)  

