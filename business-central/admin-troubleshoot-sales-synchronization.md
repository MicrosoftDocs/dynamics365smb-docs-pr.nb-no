---
title: Feilsøke synkroniseringsfeil | Microsoft Docs
description: Gir veiledning for identifisering og løsing av synkroniseringsfeil.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2019
ms.author: bholtorf
ms.openlocfilehash: bb6d0837f91240eb31abc7c02895cf2da420bf7d
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726793"
---
# <a name="troubleshooting-synchronization-errors"></a><span data-ttu-id="b1d62-103">Feilsøke synkroniseringsfeil</span><span class="sxs-lookup"><span data-stu-id="b1d62-103">Troubleshooting Synchronization Errors</span></span>
<span data-ttu-id="b1d62-104">Mange bevegelige deler er involvert i integrasjon av [!INCLUDE[d365fin](includes/d365fin_md.md)] med [!INCLUDE[crm_md](includes/crm_md.md)], og noen ganger går det galt.</span><span class="sxs-lookup"><span data-stu-id="b1d62-104">There are lots of moving parts involved in integrating [!INCLUDE[d365fin](includes/d365fin_md.md)] with [!INCLUDE[crm_md](includes/crm_md.md)], and sometimes things go wrong.</span></span> <span data-ttu-id="b1d62-105">I dette emnet omtales noen av de typiske feilene som oppstår, og det oppgis noen punkter for hvordan de skal løses.</span><span class="sxs-lookup"><span data-stu-id="b1d62-105">This topic points out some of the typical errors that occur and gives some pointers for how to fix them.</span></span>

<span data-ttu-id="b1d62-106">Feil oppstår ofte enten på grunn av noe en bruker har gjort med koblede poster eller fordi noe er galt med hvordan integrasjonen er satt opp.</span><span class="sxs-lookup"><span data-stu-id="b1d62-106">Errors often occur either because of something that a user has done to coupled records or something is wrong with how the integration is set up.</span></span> <span data-ttu-id="b1d62-107">Ved feil relatert til koblede poster kan brukere løse disse selv.</span><span class="sxs-lookup"><span data-stu-id="b1d62-107">For errors related to coupled records, users can resolve those themselves.</span></span> <span data-ttu-id="b1d62-108">Disse feilene skyldes handlinger som sletting av en post i én bedriftsapp, men ikke i begge bedriftsappene, og påfølgende synkronisering.</span><span class="sxs-lookup"><span data-stu-id="b1d62-108">These errors are caused by actions such as deleting a record in one, but not both, business apps and then synchronizing.</span></span> <span data-ttu-id="b1d62-109">Hvis du vil ha mer informasjon, kan du se [Vise statusen for en synkronisering](admin-how-to-view-synchronization-status.md).</span><span class="sxs-lookup"><span data-stu-id="b1d62-109">For more information, see [View the Status of a Synchronization](admin-how-to-view-synchronization-status.md).</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

<span data-ttu-id="b1d62-110">Feil som er relatert til hvordan integrasjonen er satt opp, må vanligvis håndteres av en administrator.</span><span class="sxs-lookup"><span data-stu-id="b1d62-110">Errors that are related to how the integration is set up typically require an administrator's attention.</span></span> <span data-ttu-id="b1d62-111">Du kan se disse feilene på siden **Synkroniseringsfeil ved integrasjon**.</span><span class="sxs-lookup"><span data-stu-id="b1d62-111">You can view these errors on the **Integration Synchronization Errors** page.</span></span> <span data-ttu-id="b1d62-112">Eksempler på noen vanlige problemer er:</span><span class="sxs-lookup"><span data-stu-id="b1d62-112">Examples of some typical issues include:</span></span>  
  
* <span data-ttu-id="b1d62-113">Tillatelsene og rollene som er tilordnet til brukere, er ikke korrekte.</span><span class="sxs-lookup"><span data-stu-id="b1d62-113">The permissions and roles assigned to users are not correct.</span></span>  
* <span data-ttu-id="b1d62-114">Administratorkontoen ble angitt som integrasjonsbrukeren.</span><span class="sxs-lookup"><span data-stu-id="b1d62-114">The administrator account was specified as the integration user.</span></span>  
* <span data-ttu-id="b1d62-115">Integrasjonsbrukerens passord er satt til å kreve en endring når brukeren logger seg på.</span><span class="sxs-lookup"><span data-stu-id="b1d62-115">The integration user’s password is set to require a change when the user signs in.</span></span>  
* <span data-ttu-id="b1d62-116">Valutakursene for valutaer er ikke angitt i én av appene.</span><span class="sxs-lookup"><span data-stu-id="b1d62-116">The exchange rates for currencies are not specified in one or the other app.</span></span>  
  
<span data-ttu-id="b1d62-117">Du må løse feilene manuelt, men siden hjelper deg på noen måter.</span><span class="sxs-lookup"><span data-stu-id="b1d62-117">You must manually resolve the errors, but there are a few ways in which the page helps you.</span></span> <span data-ttu-id="b1d62-118">Eksempel:</span><span class="sxs-lookup"><span data-stu-id="b1d62-118">For example:</span></span>  

* <span data-ttu-id="b1d62-119">Feltene **Kilde** og **Destinasjon** kan inneholde koblinger til posten der feilen ble funnet.</span><span class="sxs-lookup"><span data-stu-id="b1d62-119">The **Source** and **Destination** fields may contain links to the record where the error was found.</span></span> <span data-ttu-id="b1d62-120">Klikk på koblingen for å åpne posten og undersøke feilen.</span><span class="sxs-lookup"><span data-stu-id="b1d62-120">Click the link to open the record and investigate the error.</span></span>  
* <span data-ttu-id="b1d62-121">Handlingene **Slett oppføringer eldre enn 7 dager** og **Slett alle oppføringer** rydder opp i listen.</span><span class="sxs-lookup"><span data-stu-id="b1d62-121">The **Delete Entries Older than 7 Days** and the **Delete All Entries** actions will clean up the list.</span></span> <span data-ttu-id="b1d62-122">Vanligvis bruker du disse handlingene etter at du har løst årsaken til en feil som påvirker mange poster.</span><span class="sxs-lookup"><span data-stu-id="b1d62-122">Typically, you use these actions after you have resolved the cause of an error that affects many records.</span></span> <span data-ttu-id="b1d62-123">Du må imidlertid være forsiktig.</span><span class="sxs-lookup"><span data-stu-id="b1d62-123">Use caution, however.</span></span> <span data-ttu-id="b1d62-124">Disse handlingene kan slette feil som fremdeles er relevante.</span><span class="sxs-lookup"><span data-stu-id="b1d62-124">These actions might delete errors that are still relevant.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1d62-125">Se også</span><span class="sxs-lookup"><span data-stu-id="b1d62-125">See Also</span></span>
<span data-ttu-id="b1d62-126">[Integrere med [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)</span><span class="sxs-lookup"><span data-stu-id="b1d62-126">[Integrating with [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)</span></span>  
<span data-ttu-id="b1d62-127">[Sette opp brukerkontoer for integrasjon med [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)</span><span class="sxs-lookup"><span data-stu-id="b1d62-127">[Setting Up User Accounts for Integrating with [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)</span></span>  
<span data-ttu-id="b1d62-128">[Sette opp en tilkobling til [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)</span><span class="sxs-lookup"><span data-stu-id="b1d62-128">[Set Up a Connection to [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)</span></span>  
[<span data-ttu-id="b1d62-129">Sammenkoble og synkronisere poster manuelt</span><span class="sxs-lookup"><span data-stu-id="b1d62-129">Couple and Synchronize Records Manually</span></span>](admin-how-to-couple-and-synchronize-records-manually.md)  
[<span data-ttu-id="b1d62-130">Vise statusen for en synkronisering</span><span class="sxs-lookup"><span data-stu-id="b1d62-130">View the Status of a Synchronization</span></span>](admin-how-to-view-synchronization-status.md)  