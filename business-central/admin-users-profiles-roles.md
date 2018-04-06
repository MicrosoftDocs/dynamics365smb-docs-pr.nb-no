---
title: Administrere brukere og roller | Microsoft-dokumentasjon
description: Finn ut hvordan du administrerer brukere og rollesentre i Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/02/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e5efc3536203495dcec1be2f1dc680b35c39d4db
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a><span data-ttu-id="2f768-103">Forstå brukere, profiler og rollesentre</span><span class="sxs-lookup"><span data-stu-id="2f768-103">Understanding Users, Profiles, and Role Centers</span></span>
<span data-ttu-id="2f768-104">Personene i selskapet som har tilgang til [!INCLUDE[d365fin](includes/d365fin_md.md)], er alle tilordnet en *profil* som gir dem tilgang til et *rollesenter*.</span><span class="sxs-lookup"><span data-stu-id="2f768-104">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a *profile* that gives them access to a *Role Center*.</span></span> <span data-ttu-id="2f768-105">Som en administrator kan du tilordne og endre profiler i [!INCLUDE[d365fin](includes/d365fin_md.md)], og du kan legge til og fjerne brukere som en del av [!INCLUDE[d365fin](includes/d365fin_md.md)]-abonnementet.</span><span class="sxs-lookup"><span data-stu-id="2f768-105">As an administrator, you can assign and change profiles in [!INCLUDE[d365fin](includes/d365fin_md.md)], and you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="2f768-106">Legge til brukere</span><span class="sxs-lookup"><span data-stu-id="2f768-106">Adding Users</span></span>
<span data-ttu-id="2f768-107">For å legge til brukere i [!INCLUDE[d365fin](includes/d365fin_md.md)] må selskapets Office 365-administrator først opprette brukere i administrasjonssenteret for Office 365.</span><span class="sxs-lookup"><span data-stu-id="2f768-107">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)], your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="2f768-108">Hvis du vil ha mer informasjon, kan du se [Administrere brukere og tillatelser](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="2f768-108">For more information, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>  

## <a name="profiles"></a><span data-ttu-id="2f768-109">Profiler</span><span class="sxs-lookup"><span data-stu-id="2f768-109">Profiles</span></span>
<span data-ttu-id="2f768-110">Profiler er samlinger av [!INCLUDE[d365fin](includes/d365fin_md.md)]-brukere som deler samme rollesenter.</span><span class="sxs-lookup"><span data-stu-id="2f768-110">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same Role Center.</span></span> <span data-ttu-id="2f768-111">Et rollesenter er en side der du kan plassere forskjellige deler.</span><span class="sxs-lookup"><span data-stu-id="2f768-111">A Role Center is a type of page on which you can place different parts.</span></span> <span data-ttu-id="2f768-112">Hver del er en beholder som kan være vert for andre sider eller forhåndsdefinerte systemdeler, for eksempel en Outlook-del eller deler for å legge til oppgaver, varslinger eller notater.</span><span class="sxs-lookup"><span data-stu-id="2f768-112">Each part is a container in which you can host other pages or pre-defined system parts, such as an Outlook part or parts for adding tasks, notifications, or notes.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2f768-113">I den nye versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du legge til, endre eller slette profiler.</span><span class="sxs-lookup"><span data-stu-id="2f768-113">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)], you cannot add, edit, or delete profiles.</span></span>  

## <a name="configuration-and-personalization"></a><span data-ttu-id="2f768-114">Konfigurasjon og tilpasning</span><span class="sxs-lookup"><span data-stu-id="2f768-114">Configuration and Personalization</span></span>
<span data-ttu-id="2f768-115">Begrepet om grensesnittilpasning i [!INCLUDE[d365fin](includes/d365fin_md.md)] er delt i to:</span><span class="sxs-lookup"><span data-stu-id="2f768-115">The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:</span></span>  

-   <span data-ttu-id="2f768-116">Konfigurasjon, må utføres av administrator</span><span class="sxs-lookup"><span data-stu-id="2f768-116">Configuration, performed by the administrator</span></span>  

-   <span data-ttu-id="2f768-117">Tilpassing, utført av brukere</span><span class="sxs-lookup"><span data-stu-id="2f768-117">Personalization, performed by users</span></span>  

<span data-ttu-id="2f768-118">Systemansvarlig konfigurerer brukergrensesnittet for flere brukere ved å tilpasse brukergrensesnittet for en profil som brukerne tilordnes.</span><span class="sxs-lookup"><span data-stu-id="2f768-118">The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.</span></span>  

<span data-ttu-id="2f768-119">Brukere tilpasser brukergrensesnittet i sin egen versjon ved å tilpasse brukergrensesnittet når de er logget på sine egne konti.</span><span class="sxs-lookup"><span data-stu-id="2f768-119">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="2f768-120">Denne tilpasningen kan slettes av systemansvarlig.</span><span class="sxs-lookup"><span data-stu-id="2f768-120">This personalization can be deleted by the administrator.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2f768-121">Se også</span><span class="sxs-lookup"><span data-stu-id="2f768-121">See Also</span></span>  
[<span data-ttu-id="2f768-122">Administrere brukere og tillatelser</span><span class="sxs-lookup"><span data-stu-id="2f768-122">Managing Users and Permissions</span></span>](ui-how-users-permissions.md)  
<!-- [Customize the User Interface](../customize-the-user-interface.md)   
 [Security Overview](../Security%20Overview.md)-->

