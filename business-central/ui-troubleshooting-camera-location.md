---
title: 'Feilsøking: Få tilgang til kamera og plassering'
description: Denne artikkelen beskriver hvordan du feilsøker tilgang til kamera- og plasseringsinformasjon i Business Central.
author: blrobl
ms.author: t-blrobl
ms.date: 10/01/2020
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
ms.openlocfilehash: a29b2ea19d812d60d2824c131e311c34d74612af
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760219"
---
# <a name="troubleshooting-accessing-camera-and-location"></a><span data-ttu-id="27016-103">Feilsøking: Få tilgang til kamera og plassering</span><span class="sxs-lookup"><span data-stu-id="27016-103">Troubleshooting: Accessing Camera and Location</span></span>

<span data-ttu-id="27016-104">Du kan oppleve problemer når du prøver å få til gang til kamera- og plasseringsinformasjon for en enhet fra [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="27016-104">You might come across some issues when trying to access the camera and location information of a device from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="27016-105">Nedenfor finner du mulige årsaker til disse problemene og hvordan du omgår dem.</span><span class="sxs-lookup"><span data-stu-id="27016-105">You can find the possible causes behind these problems and how to work around them listed below.</span></span>

## <a name="device-must-have-camera-and-location-capabilities"></a><span data-ttu-id="27016-106">Enheten må ha kamera- og plasseringsegenskaper</span><span class="sxs-lookup"><span data-stu-id="27016-106">Device must have Camera and Location Capabilities</span></span>

<span data-ttu-id="27016-107">For å få tilgang til kameraet eller en brukers plassering fra en enheten må enheten henholdsvis ha et fysisk kamera eller muligheten til å hente plasseringsinformasjon.</span><span class="sxs-lookup"><span data-stu-id="27016-107">In order to access the camera or a user's location from a device, the device must have a physical camera or the capability to retrieve location information, respectively.</span></span>

<span data-ttu-id="27016-108">Hvis enheten har kamera- og plasseringsegenskaper, men du fremdeles har problemer, kan det hende at enkelte driver trenger oppdatering eller ny installasjon.</span><span class="sxs-lookup"><span data-stu-id="27016-108">If your device has camera and location capabilities but you still encounter problems, it is possible that some drivers need updating or reinstalling.</span></span> <span data-ttu-id="27016-109">Selv om du er usikker, anbefaler vi alltid at du oppdaterer enheten operativsystem, drivere og nettleser til den nyeste versjonen for den beste opplevelsen.</span><span class="sxs-lookup"><span data-stu-id="27016-109">Even if you are unsure, we always recommend you update your device operating system, drivers, and browser to the latest version for the best experience.</span></span>

## <a name="access-permissions-not-enabled"></a><span data-ttu-id="27016-110">Tilgangstillatelser ikke aktivert</span><span class="sxs-lookup"><span data-stu-id="27016-110">Access Permissions not Enabled</span></span>

<span data-ttu-id="27016-111">Du må aktivere generell tilgang til kamera og plassering fra enhetens personverninnstillinger og uttrykkelig tillate at [!INCLUDE[prod_short](includes/prod_short.md)] får tilgang til dem.</span><span class="sxs-lookup"><span data-stu-id="27016-111">You must enable general access to camera and location from your device's privacy settings and explicitly give permission to  [!INCLUDE[prod_short](includes/prod_short.md)] to access them.</span></span> <span data-ttu-id="27016-112">For å se eller endre tillatelser for en enhet som kjører i Windows, går du for eksempel til **Innstillinger**, velger **Personvern** og **Apptillatelser**.</span><span class="sxs-lookup"><span data-stu-id="27016-112">For example, to see or change permissions for a device running on Windows, go to **Settings**, choose **Privacy**, and then **App permissions**.</span></span> 

<span data-ttu-id="27016-113">For mobile enheter må du gi kamera- og plasseringstilgangstillatelser til [!INCLUDE[prod_short](includes/prod_short.md)]-mobilappen.</span><span class="sxs-lookup"><span data-stu-id="27016-113">For mobile devices, you must give camera and location access permissions to the [!INCLUDE[prod_short](includes/prod_short.md)] Mobile App.</span></span> <span data-ttu-id="27016-114">For å gjøre det for en iOS-enhet går du til **Innstillinger**, velger **Personvern** og **Kamera** eller **Plassering**.</span><span class="sxs-lookup"><span data-stu-id="27016-114">To do so for an iOS device, go to **Settings**, choose **Privacy**, and then **Camera** or **Location**.</span></span> <span data-ttu-id="27016-115">For å gjøre det for Android-enheter går du til **Innstillinger**, velger **Apper og varsler**, **Avansert**, **Tillatelsesbehandling** og **Kamera** eller **Plassering**.</span><span class="sxs-lookup"><span data-stu-id="27016-115">For Android devices go to **Settings**, choose **Apps & Notifications**, **Advanced**, **Permission Manager**, and then **Camera** or **Location**.</span></span>

<span data-ttu-id="27016-116">Hvis du bruker [!INCLUDE[prod_short](includes/prod_short.md)] i en nettleser, må du i tillegg gi [!INCLUDE[prod_short](includes/prod_short.md)]-nettstedet tillatelse til å få tilgang til kamera- eller plasseringsinformasjon.</span><span class="sxs-lookup"><span data-stu-id="27016-116">In addition, if you are using [!INCLUDE[prod_short](includes/prod_short.md)] in a browser, you must also grant the [!INCLUDE[prod_short](includes/prod_short.md)] site permission to access the camera or location information.</span></span> <span data-ttu-id="27016-117">For å se eller endre et nettsteds tillatelser i Microsoft Edge-nettleseren går du til **Innstillinger**, **Nettstedstillatelser** og **Kamera** eller **Plassering**.</span><span class="sxs-lookup"><span data-stu-id="27016-117">To see or change a site's permissions in the Microsoft Edge browser, go to **Settings**, choose **Site Permissions**, and then **Camera** or **Location**.</span></span> <span data-ttu-id="27016-118">Vær oppmerksom på at dette kan være annerledes for andre nettlesere.</span><span class="sxs-lookup"><span data-stu-id="27016-118">Note that this might be different for other browsers.</span></span>

<span data-ttu-id="27016-119">Som standard vil enheten eller nettleseren vise en forespørsel om tilgang til disse egenskapene når brukeren aktiverer dem for første gang.</span><span class="sxs-lookup"><span data-stu-id="27016-119">By default, the device or browser will pop up a request to access these capabilities when the user activates them for the first time.</span></span>

> [!NOTE]  
> <span data-ttu-id="27016-120">Enkelte eldre nettlesere gir ikke tilgang til kamera og plassering.</span><span class="sxs-lookup"><span data-stu-id="27016-120">Some old browsers do not grant access to camera and location.</span></span> <span data-ttu-id="27016-121">Kamera er for eksempel ikke tilgjengelig i Internet Explorer eller den gamle Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="27016-121">For example, camera is not available in Internet Explorer or the legacy Edge browser.</span></span>

## <a name="web-client-connection-not-secure"></a><span data-ttu-id="27016-122">Nettklienttilkobling ikke sikker</span><span class="sxs-lookup"><span data-stu-id="27016-122">Web Client Connection not Secure</span></span>

<span data-ttu-id="27016-123">Kamera- og plasseringsegenskaper er bare tilgjengelig når du har tilgang til nettklienten via SSL-sikrede HTTP-tilkobling ved å bruke URI-skjemaet `https://`.</span><span class="sxs-lookup"><span data-stu-id="27016-123">The camera and location capabilities are only available when accessing the Web Client through SSL secured HTTP connections, using the `https://` URI scheme.</span></span> 

<span data-ttu-id="27016-124">Det eneste unntaket er å koble til `http://localhost`, som brukes til formål for utvikling og testing.</span><span class="sxs-lookup"><span data-stu-id="27016-124">The only exception is connecting to `http://localhost`, used for development and test purposes.</span></span>


## <a name="working-with-virtualization-technologies"></a><span data-ttu-id="27016-125">Arbeide med visualiseringsteknologier</span><span class="sxs-lookup"><span data-stu-id="27016-125">Working with Virtualization Technologies</span></span>

<span data-ttu-id="27016-126">Når du kobler til [!INCLUDE[prod_short](includes/prod_short.md)] via Eksternt skrivebord eller en annen virtualisering, kan det hende tilgang til kamera og plassering ikke er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="27016-126">When connecting to [!INCLUDE[prod_short](includes/prod_short.md)] through Remote Desktop or another virtualization, the access to camera or location might not be available.</span></span> <span data-ttu-id="27016-127">I dette tilfellet bruker du det fysiske systemet i stedet.</span><span class="sxs-lookup"><span data-stu-id="27016-127">If this is the case, use the physical system instead.</span></span>

## <a name="antivirus-software"></a><span data-ttu-id="27016-128">Antivirusprogramvare</span><span class="sxs-lookup"><span data-stu-id="27016-128">Antivirus Software</span></span>
<span data-ttu-id="27016-129">Enkelte antivirusprogramvarer blokkerer tilgang til kamera og plassering som standard.</span><span class="sxs-lookup"><span data-stu-id="27016-129">Some antivirus software block access to camera and location by default.</span></span> <span data-ttu-id="27016-130">Husk å sjekke innstillingene for antivirusprogramvaren.</span><span class="sxs-lookup"><span data-stu-id="27016-130">Remember to check your antivirus software settings.</span></span>

## <a name="see-also"></a><span data-ttu-id="27016-131">Se også</span><span class="sxs-lookup"><span data-stu-id="27016-131">See Also</span></span>
[<span data-ttu-id="27016-132">Implementere kameraet i AL</span><span class="sxs-lookup"><span data-stu-id="27016-132">Implementing the Camera in AL</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-implement-camera-al)  
[<span data-ttu-id="27016-133">Implementere plasseringen i AL</span><span class="sxs-lookup"><span data-stu-id="27016-133">Implementing the Location in AL</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-implement-location-al)
