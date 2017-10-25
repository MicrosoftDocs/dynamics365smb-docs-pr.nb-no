---
title: Administrere brukere og roller | Microsoft-dokumentasjon
description: "Lær hvordan du administrerer brukere og rollesentre i Dynamics 365 for Financials."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: e8989767618962a2db861b2df60aa03a2ca2b484
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="users-profiles-and-role-centers-in-dynamics-365-for-financials"></a><span data-ttu-id="2af3e-103">Brukere, profiler og rollesentre i Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="2af3e-103">Users, Profiles, and Role Centers in Dynamics 365 for Financials</span></span>
<span data-ttu-id="2af3e-104">Personene i selskapet som har tilgang til [!INCLUDE[d365fin](includes/d365fin_md.md)], er alle tilordnet en *profil* som gir dem tilgang til et *rollesenter\`*.</span><span class="sxs-lookup"><span data-stu-id="2af3e-104">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a *profile* that gives them access to a *Role Center*.</span></span> <span data-ttu-id="2af3e-105">Som en administrator kan du tilordne og endre profiler i [!INCLUDE[d365fin](includes/d365fin_md.md)], og du kan legge til og fjerne brukere som en del av [!INCLUDE[d365fin](includes/d365fin_md.md)]-abonnementet.</span><span class="sxs-lookup"><span data-stu-id="2af3e-105">As an administrator, you can assign and change profiles in [!INCLUDE[d365fin](includes/d365fin_md.md)], and you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="2af3e-106">Legge til brukere</span><span class="sxs-lookup"><span data-stu-id="2af3e-106">Adding Users</span></span>
<span data-ttu-id="2af3e-107">For å legge til brukere i [!INCLUDE[d365fin](includes/d365fin_md.md)] må selskapets Office 365-administrator først opprette brukere i administrasjonssenteret for Office 365.</span><span class="sxs-lookup"><span data-stu-id="2af3e-107">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)], your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="2af3e-108">Hvis du vil ha mer informasjon, kan du se [Administrere brukere og tillatelser](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="2af3e-108">For more information, see [How to: Manage Users and Permissions](ui-how-users-permissions.md).</span></span>  

## <a name="profiles"></a><span data-ttu-id="2af3e-109">Profiler</span><span class="sxs-lookup"><span data-stu-id="2af3e-109">Profiles</span></span>
<span data-ttu-id="2af3e-110">Profiler er samlinger av [!INCLUDE[d365fin](includes/d365fin_md.md)]-brukere som deler samme rollesenter.</span><span class="sxs-lookup"><span data-stu-id="2af3e-110">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same Role Center.</span></span> <span data-ttu-id="2af3e-111">Et rollesenter er en side der du kan plassere forskjellige deler.</span><span class="sxs-lookup"><span data-stu-id="2af3e-111">A Role Center is a type of page on which you can place different parts.</span></span> <span data-ttu-id="2af3e-112">Hver del er en beholder som kan være vert for andre sider eller forhåndsdefinerte systemdeler, for eksempel en Outlook-del eller deler for å legge til oppgaver, varslinger eller notater.</span><span class="sxs-lookup"><span data-stu-id="2af3e-112">Each part is a container in which you can host other pages or pre-defined system parts, such as an Outlook part or parts for adding tasks, notifications, or notes.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2af3e-113">I den nye versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du legge til, endre eller slette profiler.</span><span class="sxs-lookup"><span data-stu-id="2af3e-113">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)], you cannot add, edit, or delete profiles.</span></span>  

## <a name="configuration-and-personalization"></a><span data-ttu-id="2af3e-114">Konfigurasjon og tilpasning</span><span class="sxs-lookup"><span data-stu-id="2af3e-114">Configuration and Personalization</span></span>
<span data-ttu-id="2af3e-115">Begrepet om grensesnittilpasning i [!INCLUDE[d365fin](includes/d365fin_md.md)] er delt i to:</span><span class="sxs-lookup"><span data-stu-id="2af3e-115">The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:</span></span>  

-   <span data-ttu-id="2af3e-116">Konfigurasjon, må utføres av administrator</span><span class="sxs-lookup"><span data-stu-id="2af3e-116">Configuration, performed by the administrator</span></span>  

-   <span data-ttu-id="2af3e-117">Tilpassing, utført av brukere</span><span class="sxs-lookup"><span data-stu-id="2af3e-117">Personalization, performed by users</span></span>  

<span data-ttu-id="2af3e-118">Systemansvarlig konfigurerer brukergrensesnittet for flere brukere ved å tilpasse brukergrensesnittet for en profil som brukerne tilordnes.</span><span class="sxs-lookup"><span data-stu-id="2af3e-118">The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.</span></span>  

<span data-ttu-id="2af3e-119">Brukere tilpasser brukergrensesnittet i sin egen versjon ved å tilpasse brukergrensesnittet når de er logget på sine egne konti.</span><span class="sxs-lookup"><span data-stu-id="2af3e-119">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="2af3e-120">Denne tilpasningen kan slettes av systemansvarlig.</span><span class="sxs-lookup"><span data-stu-id="2af3e-120">This personalization can be deleted by the administrator.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2af3e-121">Se også</span><span class="sxs-lookup"><span data-stu-id="2af3e-121">See Also</span></span>  
[<span data-ttu-id="2af3e-122">Administrere brukere og tillatelser</span><span class="sxs-lookup"><span data-stu-id="2af3e-122">How to: Manage Users and Permissions</span></span>](ui-how-users-permissions.md)  
<!-- [Customize the User Interface](../customize-the-user-interface.md)   
 [Security Overview](../Security%20Overview.md)-->

