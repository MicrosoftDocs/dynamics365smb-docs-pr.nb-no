---
title: Advarsler og feilmeldinger
description: Lær hvordan du kan feilsøke og finne løsninger på feilmeldinger når du arbeider i Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: af846556e09a2c1246e5c6769399d2c9d545e4a8
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115618"
---
# <a name="warnings-and-error-messages-in-dynamics-365-business-central"></a><span data-ttu-id="da9e1-103">Advarsler og feilmeldinger i Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="da9e1-103">Warnings and Error Messages in Dynamics 365 Business Central</span></span>

<span data-ttu-id="da9e1-104">I løpet av arbeidsdagen kan du se meldinger i [!INCLUDE [prod_short](includes/prod_short.md)] om at noe gikk galt, eller at det ikke er mulig å bokføre noe, for eksempel.</span><span class="sxs-lookup"><span data-stu-id="da9e1-104">During your work day, you might see notifications in [!INCLUDE [prod_short](includes/prod_short.md)] that something went wrong, or that it was not possible to post something, for example.</span></span> <span data-ttu-id="da9e1-105">I mange tilfeller gjør meldingen det enkelt å løse eller tilbakestille eventuelle endringer du har gjort.</span><span class="sxs-lookup"><span data-stu-id="da9e1-105">In many cases, the notification makes it easy to resolve the matter, or to roll back any changes that you made.</span></span> <span data-ttu-id="da9e1-106">I andre tilfeller har du kanskje ikke de opplysningene du trenger for å fjerne blokkeringen.</span><span class="sxs-lookup"><span data-stu-id="da9e1-106">In other cases, you might not have have the information that you need to get unblocked.</span></span> <span data-ttu-id="da9e1-107">Denne artikkelen inneholder tips for hvordan du går frem.</span><span class="sxs-lookup"><span data-stu-id="da9e1-107">This article provides tips on how to make progress.</span></span>  

## <a name="in-product-user-assistance"></a><span data-ttu-id="da9e1-108">Innebygd brukerstøtte</span><span class="sxs-lookup"><span data-stu-id="da9e1-108">In-product user assistance</span></span>

<span data-ttu-id="da9e1-109">Standardversjonen av [!INCLUDE [prod_short](includes/prod_short.md)] omfatter beskrivelser for de fleste feltene, kolonnene og handlingene du får tilgang til når du velger navnet.</span><span class="sxs-lookup"><span data-stu-id="da9e1-109">The default version of [!INCLUDE [prod_short](includes/prod_short.md)] includes descriptions for most fields, columns, and actions that can be accessed when you choose the name.</span></span> <span data-ttu-id="da9e1-110">I kombinasjon med læringstips for viktige sider, beskrivende tekster og instruksjonstekster, er disse verktøytipsene, eller bildeforklaringene, vår nåværende implementering av *innebygd brukerstøtte*, som er et viktig prinsipp i dagens programvaredesign.</span><span class="sxs-lookup"><span data-stu-id="da9e1-110">In combination with teaching tips for important pages, descriptive captions, and instructional text, these tooltips, or callouts, are our current implementation of *embedded user assistance*, which is an important principle in today's world of software design.</span></span>  

<span data-ttu-id="da9e1-111">Hvis du har spørsmål om et felt eller et annet element i brukergrensesnittet, velger du navnet, og du får frem en kort beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="da9e1-111">If you have a question about a field or another element of the user interface, choose the name, and a short description will appear.</span></span> <span data-ttu-id="da9e1-112">Velg *Lær mer*-koblingen hvis det ikke er nok.</span><span class="sxs-lookup"><span data-stu-id="da9e1-112">Choose the *Learn more* link if that is not enough.</span></span>  

<span data-ttu-id="da9e1-113">Hvis du vil ha mer informasjon, kan du se [Brukerstøttemodell for Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/user-assistance) i administrasjonsinnholdet for [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="da9e1-113">For more information, see [Dynamics 365 Business Central User Assistance Model](/dynamics365/business-central/dev-itpro/user-assistance) in the administration content for [!INCLUDE [prod_short](includes/prod_short.md)].</span></span>  

## <a name="help-and-support-page"></a><span data-ttu-id="da9e1-114">Hjelp og støtte-siden</span><span class="sxs-lookup"><span data-stu-id="da9e1-114">Help and Support page</span></span>

<span data-ttu-id="da9e1-115">I [!INCLUDE[prod_short](includes/prod_short.md)] gir Hjelp-menyelementet (spørsmålstegnet øverst til høyre) tilgang til **Hjelp og støtte**-siden, der du finner koblinger til ressurser som kan hjelpe deg med å finne svar på spørsmålene dine.</span><span class="sxs-lookup"><span data-stu-id="da9e1-115">In [!INCLUDE[prod_short](includes/prod_short.md)], the Help menu item (the question mark in the top right corner) gives you access to the **Help and Support** page, where you can find links to resources that can help you find answers to your questions.</span></span> <span data-ttu-id="da9e1-116">Hvis du vil ha mer informasjon, kan du se [Ressurser for hjelp og støtte](product-help-and-support.md).</span><span class="sxs-lookup"><span data-stu-id="da9e1-116">For more information, see [Resources for Help and Support](product-help-and-support.md).</span></span>  

## <a name="help-others"></a><span data-ttu-id="da9e1-117">Hjelpe andre</span><span class="sxs-lookup"><span data-stu-id="da9e1-117">Help others</span></span>

<span data-ttu-id="da9e1-118">Hvis du er administrator eller en superbruker, kan du hjelpe andre ved å slå opp feilmeldinger på siden **Feilmeldingsregister** eller i administrasjonssenteret.</span><span class="sxs-lookup"><span data-stu-id="da9e1-118">If you are an administrator or superuser, you can help others by looking up error messages in the **Error Message Register** page or in the administration center.</span></span> <span data-ttu-id="da9e1-119">I mange tilfeller handler advarselen eller feilmeldingen om installasjoner eller mangel på tillatelser og lignende som superbrukeren eller administratoren enkelt kan hjelpe med.</span><span class="sxs-lookup"><span data-stu-id="da9e1-119">In many cases, the warning or error message is about setup or lack of permission and similar issues that the superuser or administrator can easily help with.</span></span> <span data-ttu-id="da9e1-120">I andre tilfeller kan det hende du må sjekke sider for å finne årsaken.</span><span class="sxs-lookup"><span data-stu-id="da9e1-120">In other cases, you might have to inspect pages to identify the cause.</span></span> <span data-ttu-id="da9e1-121">Hvis du vil ha mer informasjon, kan du se [Finne teknisk informasjon](/dynamics365/business-central/dev-itpro/administration/manage-technical-support#finding-technical-information) i administrasjonsinnholdet for [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="da9e1-121">For more information, see [Finding technical information](/dynamics365/business-central/dev-itpro/administration/manage-technical-support#finding-technical-information) in the administration content for [!INCLUDE [prod_short](includes/prod_short.md)].</span></span>  

## <a name="see-also"></a><span data-ttu-id="da9e1-122">Se også</span><span class="sxs-lookup"><span data-stu-id="da9e1-122">See Also</span></span>

[<span data-ttu-id="da9e1-123">Ressurser for hjelp og støtte</span><span class="sxs-lookup"><span data-stu-id="da9e1-123">Resources for Help and Support</span></span>](product-help-and-support.md)  
[<span data-ttu-id="da9e1-124">Vanlige spørsmål</span><span class="sxs-lookup"><span data-stu-id="da9e1-124">Frequently Asked Questions</span></span>](across-faq.yml)  
[<span data-ttu-id="da9e1-125">Vanlige spørsmål om Fortell meg</span><span class="sxs-lookup"><span data-stu-id="da9e1-125">Tell Me FAQ</span></span>](ui-search-faq.md)  
[<span data-ttu-id="da9e1-126">Vanlige spørsmål om søk og filtrering</span><span class="sxs-lookup"><span data-stu-id="da9e1-126">Searching and Filtering FAQ</span></span>](ui-search-filter-faq.yml)  
[<span data-ttu-id="da9e1-127">Vanlige spørsmål om kopiere og lime inn</span><span class="sxs-lookup"><span data-stu-id="da9e1-127">Copy and Paste FAQ</span></span>](faq-copy-paste.yml)  
[<span data-ttu-id="da9e1-128">Endre grunnleggende innstillinger</span><span class="sxs-lookup"><span data-stu-id="da9e1-128">Change Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="da9e1-129">Bli klar til å gjøre forretninger</span><span class="sxs-lookup"><span data-stu-id="da9e1-129">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]