---
title: Arbeide med smarte varsler og angi når du ser dem | Microsoft-dokumentasjon
description: Du kan motta varsler som informerer deg om statusendringer eller hendelser, for eksempel en forfalt saldo eller lav beholdning.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 45916dc92513a223ca74cb3d76629fb36b8afa39
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3189510"
---
# <a name="manage-notifications"></a><span data-ttu-id="cff5a-103">Behandle varsler</span><span class="sxs-lookup"><span data-stu-id="cff5a-103">Manage Notifications</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="cff5a-104">kan hjelpe deg å arbeide smartere ved å varsle deg om bestemte hendelser eller endringer i status, når du for eksempel er i ferd med fakturere en kunde som har en forfalt saldo, eller den disponible beholdningen er lavere enn antallet du vil selge.</span><span class="sxs-lookup"><span data-stu-id="cff5a-104">can help you work smarter by notifying you about certain events or changes in status, such as when you are about to invoice a customer who has an overdue balance, or the available inventory is lower than the quantity you are about to sell, for example.</span></span> <span data-ttu-id="cff5a-105">Disse meldingene vises som diskrete tips i forbindelse med oppgaven du utfører, og du kan velge å ignorere varselet eller vise detaljer om problemet.</span><span class="sxs-lookup"><span data-stu-id="cff5a-105">These notifications are shown as discreet tips in the context of the task you are doing, and you can choose to ignore the notification or to see details about the issue.</span></span>  

<span data-ttu-id="cff5a-106">Hvis du velger å vise detaljer for et varsel, kan du iverksette tiltak for å løse problemet, for eksempel kontakte kunden, kjøper mer inn på lager og så videre.</span><span class="sxs-lookup"><span data-stu-id="cff5a-106">If you choose to see details for a notification, you can take action to resolve the issue, such as contacting the customer, buying more inventory, and so on.</span></span> <span data-ttu-id="cff5a-107">Du velger selv hva du gjør, og [!INCLUDE[d365fin](includes/d365fin_md.md)] gir deg råd og anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="cff5a-107">It's your choice what to do, and [!INCLUDE[d365fin](includes/d365fin_md.md)] gives you advice and recommendations.</span></span>  

<span data-ttu-id="cff5a-108">Varsler hjelper utrente brukere å fullføre ukjente oppgaver og reduserer ikke produktiviteten til mer erfarne brukere.</span><span class="sxs-lookup"><span data-stu-id="cff5a-108">Notifications can help untrained users complete unfamiliar tasks, and do not reduce productivity for the more trained user.</span></span>  

## <a name="to-turn-notifications-on-or-off-and-control-when-they-are-sent"></a><span data-ttu-id="cff5a-109">Aktivere eller deaktivere varslinger og kontrollere når de sendes</span><span class="sxs-lookup"><span data-stu-id="cff5a-109">To turn notifications on or off, and control when they are sent</span></span>

<span data-ttu-id="cff5a-110">Når du først starter med [!INCLUDE[d365fin](includes/d365fin_md.md)], er alle meldinger slått på, men du kan slå dem på eller av, for eksempel, hvis du ikke er interessert i en bestemt hendelse eller status.</span><span class="sxs-lookup"><span data-stu-id="cff5a-110">When you first start with [!INCLUDE[d365fin](includes/d365fin_md.md)] all notifications are turned on, but you can turn them on or off, for example, if you aren't interested in a certain event or status.</span></span>  

<span data-ttu-id="cff5a-111">I tillegg kan noen meldinger du angi betingelsene som de ble sendt.</span><span class="sxs-lookup"><span data-stu-id="cff5a-111">Additionally, some notifications let you specify the conditions under which they are sent.</span></span> <span data-ttu-id="cff5a-112">For eksempel hvis du ønsker å bli varslet når lageret er lite, men bare for varer kjøper du fra en bestemt leverandør.</span><span class="sxs-lookup"><span data-stu-id="cff5a-112">For example, if you want to be notified when inventory is running low, but only for items you buy from a certain vendor.</span></span>  

<span data-ttu-id="cff5a-113">Slå av varsler på eller av, og angi betingelser, gjelder bare for deg.</span><span class="sxs-lookup"><span data-stu-id="cff5a-113">Turning notifications on or off, and specifying conditions, applies only to you.</span></span>  

1. <span data-ttu-id="cff5a-114">I øvre høyre hjørne velger du **Innstillinger**-ikonet ![Innstillinger](media/ui-experience/settings_icon_small.png "Innstillinger-ikon for rollesenter"), og velg deretter handlingen **Mine innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="cff5a-114">In the top right corner, choose the **Settings** icon ![Settings](media/ui-experience/settings_icon_small.png "Settings icon for role center"), and then choose the **My Settings** action.</span></span>  
2. <span data-ttu-id="cff5a-115">På siden **Mine innstillinger**, i feltet **Varsler**, velger du *Endre når jeg mottar varsler*.</span><span class="sxs-lookup"><span data-stu-id="cff5a-115">On the **My Settings** page, in the **Notifications** field, choose the *Change when I receive notifications.*</span></span> <span data-ttu-id="cff5a-116">kobling.</span><span class="sxs-lookup"><span data-stu-id="cff5a-116">link.</span></span>  
3. <span data-ttu-id="cff5a-117">På siden som vises, aktiverer eller deaktiverer du et varsel ved å merke av for eller fjerne merket for **Aktivert**.</span><span class="sxs-lookup"><span data-stu-id="cff5a-117">In the page that appears, turn on or turn off a notification by selecting or clearing the **Enabled** check box.</span></span>  
4. <span data-ttu-id="cff5a-118">Hvis du vil angi vilkårene som utløser et varsel, kan du velge koblingen **Vis filterdetaljer**, og deretter fyller du ut feltene.</span><span class="sxs-lookup"><span data-stu-id="cff5a-118">To specify conditions that trigger a notification, choose the **View filter details** link, and then fill in the fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cff5a-119">Se også</span><span class="sxs-lookup"><span data-stu-id="cff5a-119">See Also</span></span>

<span data-ttu-id="cff5a-120">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cff5a-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
