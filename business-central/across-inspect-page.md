---
title: Kontrollere sider i Business Central
description: Bruk funksjonen for sideinspeksjon til å zoome inn detaljer om sideutformingen og datakilden. Sideinspeksjonsfunksjonen er ideell for feilsøking av problemer med dataene.
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
author: jswymer
ms.date: 10/01/2019
ms.openlocfilehash: 7bc5186103f05ad827d15933f586e2fac9b4a584
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304880"
---
# <a name="inspecting-pages-in-business-central"></a><span data-ttu-id="be733-104">Kontrollere sider i Business Central</span><span class="sxs-lookup"><span data-stu-id="be733-104">Inspecting Pages in Business Central</span></span>

<span data-ttu-id="be733-105">Sideinspeksjonsfunksjonen gjør det mulig å få opplysninger om en side ved å gi innsikt i sideutformingen, de ulike elementene som utgjør siden, og kilden bak dataene som vises.</span><span class="sxs-lookup"><span data-stu-id="be733-105">The page inspection feature enables you to get details about a page, providing insight into the page design, the different elements that comprise the page, and the source behind the data it displays.</span></span> <span data-ttu-id="be733-106">Sideninspeksjon er spesielt utviklet for administratorer, avanserte brukere, støttepersonell og utviklere.</span><span class="sxs-lookup"><span data-stu-id="be733-106">Page inspection is especially designed for administrators, power users, support personnel, and developers.</span></span> <span data-ttu-id="be733-107">Den er ideell for å lære datamodellen bak en side og feilsøking.</span><span class="sxs-lookup"><span data-stu-id="be733-107">It is ideal for learning the data model behind a page and troubleshooting.</span></span> <span data-ttu-id="be733-108">Hvis du har et problem på en side, kan du bruke sideninspeksjon til å få informasjon som kan videresendes til systemansvarlig eller servicepersonell.</span><span class="sxs-lookup"><span data-stu-id="be733-108">For example, if you are experiencing a problem with a page, you could use page inspection to get information to pass on to your system administrator or support personnel.</span></span>

## <a name="working-with-page-inspection"></a><span data-ttu-id="be733-109">Arbeide med sideinspeksjon</span><span class="sxs-lookup"><span data-stu-id="be733-109">Working with Page Inspection</span></span>

<span data-ttu-id="be733-110">Startsideinspeksjonen fra **Hjelp og støtte**-siden.</span><span class="sxs-lookup"><span data-stu-id="be733-110">You start page inspection from the **Help & Support** page.</span></span> <span data-ttu-id="be733-111">Velg spørsmålstegnet øverst til høyre, velg **Hjelp og støtte**, og velg deretter **Undersøk sidene og dataene**.</span><span class="sxs-lookup"><span data-stu-id="be733-111">Choose the question mark in the top right corner, choose **Help & Support**, and then choose **Inspect pages and data**.</span></span> <span data-ttu-id="be733-112">Du kan også bruke hurtigtasten **Ctrl+Alt+F1**.</span><span class="sxs-lookup"><span data-stu-id="be733-112">Or, you can just use the keyboard shortcut **Ctrl+Alt+F1**.</span></span>

<span data-ttu-id="be733-113">Ruten **Sideninspeksjon** åpnes på siden.</span><span class="sxs-lookup"><span data-stu-id="be733-113">The **Page inspection** pane opens on the side.</span></span> <span data-ttu-id="be733-114">Følgende figur viser ruten **Sideninspeksjon** på siden **Ordre**.</span><span class="sxs-lookup"><span data-stu-id="be733-114">The following figure illustrates the **Page Inspection** pane on the **Sales Order** page.</span></span>

![Sideinspeksjon](media/page-inspection-example.png)

<span data-ttu-id="be733-116">Når ruten **Sideinspeksjon** åpnes for første gang, vises informasjon som gjelder hovedobjektet på siden.</span><span class="sxs-lookup"><span data-stu-id="be733-116">When the **Page Inspection** pane first opens, it shows information that pertains to the main page object.</span></span>

<span data-ttu-id="be733-117">Du kan tastaturet eller pekeenheten til å flytte fokus til forskjellige elementer på siden.</span><span class="sxs-lookup"><span data-stu-id="be733-117">Use the keyboard or pointing device to move focus to different elements on the page.</span></span> <span data-ttu-id="be733-118">Når du velger en faktaboks eller en del på hovedsiden, markeres rammeområdet med en kant, og **Sidenspeksjon**-ruten viser informasjon om det valgte elementet.</span><span class="sxs-lookup"><span data-stu-id="be733-118">When you select a FactBox or a part on the main page, the bounding area is highlighted by a border, and the **Page Inspection** pane shows information about the selected element.</span></span> <span data-ttu-id="be733-119">Den forrige figuren viser opplysninger om listedelen på siden **Ordre**.</span><span class="sxs-lookup"><span data-stu-id="be733-119">For example, the previous figure shows information about the list part in the **Sales Order** page.</span></span> <span data-ttu-id="be733-120">Når du går til andre sider i programmet, vil ruten **Sideinspeksjon** automatisk oppdateres med sideinformasjon når du flytter.</span><span class="sxs-lookup"><span data-stu-id="be733-120">As you navigate to other pages in the application, the **Page Inspection** pane will automatically update with page information as you move along.</span></span>

<span data-ttu-id="be733-121">Hvis du vil ha mer informasjon om hva som vises i sideinspeksjonen, kan du se [Inspisere og feilsøke sider](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages) i hjelpen for utviklere og IT-eksperter for Business Central.</span><span class="sxs-lookup"><span data-stu-id="be733-121">For more information about what is shown in page inspection, see [Inspecting and Troubleshooting Pages](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages) in the Business Central Developer and IT Pro help.</span></span>

<span data-ttu-id="be733-122">Hvis du ikke ser opplysningene du forventer å se i ruten **Sideinspeksjon**, har du trolig ikke den nødvendige tillatelsen, som beskrevet i neste del.</span><span class="sxs-lookup"><span data-stu-id="be733-122">If you do not see the details that you expect to see in the **Page Inspection** pane, you probably do not have the required permissions, as described in the next section.</span></span>

## <a name="controlling-access-to-page-inspection-details"></a><span data-ttu-id="be733-123">Kontrollere tilgang til sideinspeksjonsinformasjon</span><span class="sxs-lookup"><span data-stu-id="be733-123">Controlling Access to Page Inspection Details</span></span>

<span data-ttu-id="be733-124">Som administrator kan du kontrollere tilgang til alle opplysninger som vises i ruten **Sideinspeksjon**, ved å konfigurere brukernes tillatelser.</span><span class="sxs-lookup"><span data-stu-id="be733-124">As an administrator, you can control access to the full details that are shown in the **Page Inspection** pane by configuring the permissions that users have.</span></span> <span data-ttu-id="be733-125">For å gi en brukertillatelse til alle opplysninger, kan du gi brukere **Kjør**-tilgang for **System**-objekt **5330**.</span><span class="sxs-lookup"><span data-stu-id="be733-125">To grant a user permission to the full details, give users **Execute** permission on the **System** object **5330**.</span></span> <span data-ttu-id="be733-126">Du kan gi tillatelse ved hjelp av et tillatelsessett (som for eksempel **D365-feilsøking**) eller en brukergruppe (som for eksempel **D365-feilsøking**).</span><span class="sxs-lookup"><span data-stu-id="be733-126">You can grant this permission by using a permission set (such as **D365 Troubleshoot**) or a user group (such as **D365 Troubleshoot**).</span></span> <span data-ttu-id="be733-127">Hvis du vil ha mer informasjon om tillatelser, kan du se [Administrere brukere og tillatelser](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="be733-127">For more information about permissions, see [Manage Users and Permissions](ui-how-users-permissions.md).</span></span>

<span data-ttu-id="be733-128">Brukere som ikke har tilgang til **Systemobjekt 5330**, har fremdeles tilgang til **Sideinspeksjon**-ruten, men de ser bare **Side**- og **Tabell**-feltene, som viser grunnleggende informasjon som kan de kan sende videre til støttegruppen.</span><span class="sxs-lookup"><span data-stu-id="be733-128">Users who are not granted permissions on **System object 5330** can still access the **Page Inspection** pane, but they will only see the **Page** and **Table** fields, which display basic details that they can pass on to their support team.</span></span>

## <a name="see-also"></a><span data-ttu-id="be733-129">Se også</span><span class="sxs-lookup"><span data-stu-id="be733-129">See Also</span></span>

<span data-ttu-id="be733-130">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="be733-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
