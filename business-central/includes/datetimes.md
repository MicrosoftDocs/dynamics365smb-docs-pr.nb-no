---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7ead218d289668d893a659f730a4c64e31195f10
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788571"
---
<span data-ttu-id="8e400-101">Når du angir dato og klokkeslett, som er en dato og klokkeslett kombinert i ett felt, må du angi et mellomrom mellom datoen og klokkeslettet.</span><span class="sxs-lookup"><span data-stu-id="8e400-101">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="8e400-102">Datodelen kan bare inneholde mellomrom i form av det offisielle datoskilletegnet i regioninnstillingene.</span><span class="sxs-lookup"><span data-stu-id="8e400-102">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="8e400-103">Klokkeslettet kan inneholde mellomrom rundt AM/PM-indikatoren i relevante regionale innstillinger.</span><span class="sxs-lookup"><span data-stu-id="8e400-103">The time can contain spaces around the AM/PM indicator in relevant regional settings.</span></span>

<!--It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.-->

<span data-ttu-id="8e400-104">Tabellen nedenfor viser forskjellige måter som du kan angi datoer og klokkeslett på, og hvordan de tolkes.</span><span class="sxs-lookup"><span data-stu-id="8e400-104">The following table lists the various ways in which you can enter datetimes and how they're interpreted.</span></span>  

|<span data-ttu-id="8e400-105">Angivelse</span><span class="sxs-lookup"><span data-stu-id="8e400-105">Entry</span></span>|<span data-ttu-id="8e400-106">Tolkning</span><span class="sxs-lookup"><span data-stu-id="8e400-106">Interpretation</span></span>|
|---------------|------------------------|
|<span data-ttu-id="8e400-107">08-01-2022 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="8e400-107">08-01-2022 05:48:12 PM</span></span>|<span data-ttu-id="8e400-108">08\-01\-2022 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="8e400-108">08\-01\-2022 05:48:12 PM</span></span>|
|<span data-ttu-id="8e400-109">131222 132455</span><span class="sxs-lookup"><span data-stu-id="8e400-109">131222 132455</span></span>|<span data-ttu-id="8e400-110">13-12-22 13:24:55</span><span class="sxs-lookup"><span data-stu-id="8e400-110">13-12-22 13:24:55</span></span>|
|<span data-ttu-id="8e400-111">1-12-22 10</span><span class="sxs-lookup"><span data-stu-id="8e400-111">1-12-22 10</span></span>|<span data-ttu-id="8e400-112">01-12-22 10:00:00</span><span class="sxs-lookup"><span data-stu-id="8e400-112">01-12-22 10:00:00</span></span>|
|<span data-ttu-id="8e400-113">1.12.22 5</span><span class="sxs-lookup"><span data-stu-id="8e400-113">1.12.22 5</span></span>|<span data-ttu-id="8e400-114">01-12-22 05:00:00</span><span class="sxs-lookup"><span data-stu-id="8e400-114">01-12-22 05:00:00</span></span>|
|<span data-ttu-id="8e400-115">1.12.22</span><span class="sxs-lookup"><span data-stu-id="8e400-115">1.12.22</span></span>|<span data-ttu-id="8e400-116">01-12-22 00:00:00</span><span class="sxs-lookup"><span data-stu-id="8e400-116">01-12-22 00:00:00</span></span>|
|<span data-ttu-id="8e400-117">11 12</span><span class="sxs-lookup"><span data-stu-id="8e400-117">11 12</span></span>|<span data-ttu-id="8e400-118">11.nneværende måned.inneværende år 12.00.00</span><span class="sxs-lookup"><span data-stu-id="8e400-118">11-current month-current year 12:00:00</span></span>|
|<span data-ttu-id="8e400-119">1112 12</span><span class="sxs-lookup"><span data-stu-id="8e400-119">1112 12</span></span>|<span data-ttu-id="8e400-120">11.12.inneværende år 12.00.00</span><span class="sxs-lookup"><span data-stu-id="8e400-120">11-12-current year 12:00:00</span></span>|
|<span data-ttu-id="8e400-121">d eller i dag</span><span class="sxs-lookup"><span data-stu-id="8e400-121">t or today</span></span>|<span data-ttu-id="8e400-122">dagens dato 00:00:00</span><span class="sxs-lookup"><span data-stu-id="8e400-122">today's date 00:00:00</span></span>|
|<span data-ttu-id="8e400-123">d klokkeslett</span><span class="sxs-lookup"><span data-stu-id="8e400-123">t time</span></span>|<span data-ttu-id="8e400-124">dagens dato og klokkeslett</span><span class="sxs-lookup"><span data-stu-id="8e400-124">today's date actual time</span></span>|
|<span data-ttu-id="8e400-125">d 10.30</span><span class="sxs-lookup"><span data-stu-id="8e400-125">t 10:30</span></span>|<span data-ttu-id="8e400-126">dagens dato 10:30:00</span><span class="sxs-lookup"><span data-stu-id="8e400-126">today's date 10:30:00</span></span>|
|<span data-ttu-id="8e400-127">d 3.3.3</span><span class="sxs-lookup"><span data-stu-id="8e400-127">t 3:3:3</span></span>|<span data-ttu-id="8e400-128">dagens dato 03.03.03</span><span class="sxs-lookup"><span data-stu-id="8e400-128">today's date 03:03:03</span></span>|
|<span data-ttu-id="8e400-129">a eller arbeidsdag</span><span class="sxs-lookup"><span data-stu-id="8e400-129">w or workdate</span></span>|<span data-ttu-id="8e400-130">arbeidsdatoen 00.00.00</span><span class="sxs-lookup"><span data-stu-id="8e400-130">the working date 00:00:00</span></span>|
|<span data-ttu-id="8e400-131">m eller mandag</span><span class="sxs-lookup"><span data-stu-id="8e400-131">m or Monday</span></span>|<span data-ttu-id="8e400-132">mandag i inneværende uke 00.00.00</span><span class="sxs-lookup"><span data-stu-id="8e400-132">Monday of the current week 00:00:00</span></span>|
|<span data-ttu-id="8e400-133">ti eller tirsdag</span><span class="sxs-lookup"><span data-stu-id="8e400-133">tu or Tuesday</span></span>|<span data-ttu-id="8e400-134">tirsdag i inneværende uke 00:00:00</span><span class="sxs-lookup"><span data-stu-id="8e400-134">Tuesday of the current week 00:00:00</span></span>|
|<span data-ttu-id="8e400-135">o eller onsdag</span><span class="sxs-lookup"><span data-stu-id="8e400-135">we or Wednesday</span></span>|<span data-ttu-id="8e400-136">onsdag i inneværende uke 00.00.00</span><span class="sxs-lookup"><span data-stu-id="8e400-136">Wednesday of the current week 00:00:00</span></span>|
|<span data-ttu-id="8e400-137">to eller torsdag</span><span class="sxs-lookup"><span data-stu-id="8e400-137">th or Thursday</span></span>|<span data-ttu-id="8e400-138">torsdag i inneværende uke 00.00.00</span><span class="sxs-lookup"><span data-stu-id="8e400-138">Thursday of the current week 00:00:00</span></span>|
|<span data-ttu-id="8e400-139">f eller fredag</span><span class="sxs-lookup"><span data-stu-id="8e400-139">f or Friday</span></span>|<span data-ttu-id="8e400-140">fredag i inneværende uke 00.00.00</span><span class="sxs-lookup"><span data-stu-id="8e400-140">Friday of the current week 00:00:00</span></span>|
|<span data-ttu-id="8e400-141">l eller lørdag</span><span class="sxs-lookup"><span data-stu-id="8e400-141">s or Saturday</span></span>|<span data-ttu-id="8e400-142">lørdag i inneværende uke 00.00.00</span><span class="sxs-lookup"><span data-stu-id="8e400-142">Saturday of the current week 00:00:00</span></span>|
|<span data-ttu-id="8e400-143">s eller søndag</span><span class="sxs-lookup"><span data-stu-id="8e400-143">su or Sunday</span></span>|<span data-ttu-id="8e400-144">søndag i inneværende uke 00.00.00</span><span class="sxs-lookup"><span data-stu-id="8e400-144">Sunday of the current week 00:00:00</span></span>|
|<span data-ttu-id="8e400-145">ti 10.30</span><span class="sxs-lookup"><span data-stu-id="8e400-145">tu 10:30</span></span>|<span data-ttu-id="8e400-146">tirsdag i inneværende uke 10:30:00</span><span class="sxs-lookup"><span data-stu-id="8e400-146">Tuesday of the current week 10:30:00</span></span>|
|<span data-ttu-id="8e400-147">ti 3.3.3</span><span class="sxs-lookup"><span data-stu-id="8e400-147">tu 3:3:3</span></span>|<span data-ttu-id="8e400-148">tirsdag i inneværende uke 03.03.03</span><span class="sxs-lookup"><span data-stu-id="8e400-148">Tuesday of the current week 03:03:03</span></span>|
|<span data-ttu-id="8e400-149">t23 t</span><span class="sxs-lookup"><span data-stu-id="8e400-149">t23 t</span></span>|<span data-ttu-id="8e400-150">Tirsdag i uke 23 i arbeidsdatoåret, gjeldende klokkeslett</span><span class="sxs-lookup"><span data-stu-id="8e400-150">Tuesday of week 23 of the work date year, current time of day</span></span>|
|<span data-ttu-id="8e400-151">t23</span><span class="sxs-lookup"><span data-stu-id="8e400-151">t23</span></span>|<span data-ttu-id="8e400-152">Tirsdag i uke 23 i arbeidsdatoåret</span><span class="sxs-lookup"><span data-stu-id="8e400-152">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="8e400-153">t 23</span><span class="sxs-lookup"><span data-stu-id="8e400-153">t 23</span></span>|<span data-ttu-id="8e400-154">I dag 23:00:00</span><span class="sxs-lookup"><span data-stu-id="8e400-154">Today 23:00:00</span></span>|
|<span data-ttu-id="8e400-155">t-1</span><span class="sxs-lookup"><span data-stu-id="8e400-155">t-1</span></span>|<span data-ttu-id="8e400-156">Tirsdag i uke 1 i arbeidsdatoåret</span><span class="sxs-lookup"><span data-stu-id="8e400-156">Tuesday of week 1 of the work date year</span></span>|


