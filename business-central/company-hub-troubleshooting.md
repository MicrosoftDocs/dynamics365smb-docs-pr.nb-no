---
title: Feilsøke selskapshuben
description: Lær å omgå problemer i selskapshuben i Dynamics 365 Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3f348de3e8116efd789f85f1b011ecc7013bf2b1
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927706"
---
# <a name="troubleshooting-your-company-hub"></a><span data-ttu-id="f38a5-103">Feilsøke selskapshuben</span><span class="sxs-lookup"><span data-stu-id="f38a5-103">Troubleshooting Your Company Hub</span></span>

<span data-ttu-id="f38a5-104">Det er lett nok å legge til selskaper i instrumentbordet for selskapshuben, men denne artikkelen tar opp problemer du kan møte underveis.</span><span class="sxs-lookup"><span data-stu-id="f38a5-104">Adding companies to the company hub dashboard is easy enough, but this article addresses issues that you may have on the way.</span></span>  

## <a name="check-errors"></a><span data-ttu-id="f38a5-105">Sjekk feil</span><span class="sxs-lookup"><span data-stu-id="f38a5-105">Check errors</span></span>

<span data-ttu-id="f38a5-106">Bruk handlingen **Sjekk feil** til å vise en liste over nylige feil.</span><span class="sxs-lookup"><span data-stu-id="f38a5-106">Use the **Check Errors** action to view a list of recent errors.</span></span> <span data-ttu-id="f38a5-107">Du kan vise flere detaljer for hver feil, og du kan rydde i loggen ved å slette eldre oppføringer.</span><span class="sxs-lookup"><span data-stu-id="f38a5-107">You can see additional details for each error, and you can clean up the log by deleting older entries.</span></span>  

## <a name="connection-failed"></a><span data-ttu-id="f38a5-108">Tilkobling mislyktes</span><span class="sxs-lookup"><span data-stu-id="f38a5-108">Connection failed</span></span>

<span data-ttu-id="f38a5-109">Det kan være et par årsaker til at du ikke kan koble til et selskap, inkludert følgende:</span><span class="sxs-lookup"><span data-stu-id="f38a5-109">There can be a couple of reasons why you cannot connect to a company, including the following:</span></span>

- <span data-ttu-id="f38a5-110">URL-adressen i feltet **Miljøkobling** er ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="f38a5-110">The URL in the **Environment Link** field is not valid</span></span>  

  <span data-ttu-id="f38a5-111">Gå til siden **Miljøkoblinger**, åpne miljøet du ikke kan koble til, og velg deretter **Test tilkoblingen**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="f38a5-111">Go to the **Environment Links** page, open the environment that you cannot connect to, and then choose the **Test the connection** action.</span></span>  
- <span data-ttu-id="f38a5-112">Klientens selskapet er frakoblet for øyeblikket, for eksempel hvis det blir oppgradert</span><span class="sxs-lookup"><span data-stu-id="f38a5-112">The client's company is currently offline, for example if it being upgraded</span></span>

  <span data-ttu-id="f38a5-113">På instrumentpanelet velger du **Verktøy**-menyelementet, og deretter **Sjekk feil**.</span><span class="sxs-lookup"><span data-stu-id="f38a5-113">In your dashboard, choose the **Tools** menu item, and then choose **Check Errors**.</span></span> <span data-ttu-id="f38a5-114">Dermed åpnes en liste med tekniske opplysninger, så du vil kanskje kontakte systemansvarlig hvis du ser feil.</span><span class="sxs-lookup"><span data-stu-id="f38a5-114">This opens a list with technical details, so you might want to contact your administrator if you're seeing errors.</span></span> <span data-ttu-id="f38a5-115">Feilmeldingen «*Serveren har avvist klientlegitimasjonen*» antyder at du ikke har tilgang.</span><span class="sxs-lookup"><span data-stu-id="f38a5-115">For example, the error message "*The server has rejected the client credentials*" suggests that you do not have access.</span></span>  
- <span data-ttu-id="f38a5-116">Du har ikke tilgang til alle selskaper i miljøet du prøver å koble til</span><span class="sxs-lookup"><span data-stu-id="f38a5-116">You do not have access to all companies in the environment that you are trying to connect to</span></span>

  <span data-ttu-id="f38a5-117">I [!INCLUDE [prodshort](includes/prodshort.md)] kan en organisasjon ha flere forretningsenheter som kalles selskaper, og du har kanskje ikke tilgang til alle selskapene.</span><span class="sxs-lookup"><span data-stu-id="f38a5-117">In [!INCLUDE [prodshort](includes/prodshort.md)], an organization can have multiple business units called companies, and you might not have access to all companies.</span></span> <span data-ttu-id="f38a5-118">Kontakt administratoren eller klienten for å sikre at du har tilgang til selskapene som du må arbeide i.</span><span class="sxs-lookup"><span data-stu-id="f38a5-118">Work with your administrator or client to make sure that you have access to the companies that you have to work in.</span></span>  

## <a name="data-does-not-refresh"></a><span data-ttu-id="f38a5-119">Data blir ikke oppdatert</span><span class="sxs-lookup"><span data-stu-id="f38a5-119">Data does not refresh</span></span>

<span data-ttu-id="f38a5-120">Når du legger til et selskap eller ber om en oppdatering av dataene, henter [!INCLUDE [prodshort](includes/prodshort.md)] dataene.</span><span class="sxs-lookup"><span data-stu-id="f38a5-120">When you add a company or request a refresh of the data, [!INCLUDE [prodshort](includes/prodshort.md)] fetches the data.</span></span> <span data-ttu-id="f38a5-121">Men du må oppdatere siden selv, for eksempel velge handlingen **Last inn alle selskaper på nytt**, oppdatere lesersiden, navigere fra instrumentbordet og deretter tilbake igjen, eller lignende.</span><span class="sxs-lookup"><span data-stu-id="f38a5-121">But you must refresh the page yourself, such as choosing the **Reload all companies** action, refresh the browser page, navigate away from the dashboard and then back again, or similar.</span></span>  

<span data-ttu-id="f38a5-122">Hvis du har lagt til et selskap, men det vises ikke i oversikten, kan du også bruke handlingen **Last inn alle selskaper på nytt** for å oppdatere oversikten.</span><span class="sxs-lookup"><span data-stu-id="f38a5-122">If you've added a company but it is not displaying in the list, you can also use the **Reload all companies** action to update the list.</span></span>

## <a name="see-also"></a><span data-ttu-id="f38a5-123">Se også</span><span class="sxs-lookup"><span data-stu-id="f38a5-123">See also</span></span>

[<span data-ttu-id="f38a5-124">Administrere arbeid på tvers av flere selskaper i selskapshuben</span><span class="sxs-lookup"><span data-stu-id="f38a5-124">Manage Work across Multiple Companies in the Company Hub</span></span>](company-hub.md)  
[<span data-ttu-id="f38a5-125">Legge til selskaper i selskapshuben</span><span class="sxs-lookup"><span data-stu-id="f38a5-125">Add companies to your company hub</span></span>](company-hub-add-company.md)  
[<span data-ttu-id="f38a5-126">Regnskapsføreropplevelser i Business Central</span><span class="sxs-lookup"><span data-stu-id="f38a5-126">Accountant Experiences in Business Central</span></span>](finance-accounting.md)  