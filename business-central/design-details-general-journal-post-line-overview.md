---
title: Oversikt over Finanskladd – bokfør linje | Microsoft-dokumentasjon
description: Dette emnet introduserer endringer i Kodeenhet 12, **Finanskladd – bokfør linje**, som er det store programobjektet for finansbokføring og det eneste stedet å sette inn finansposter, mva-poster og kunde- og leverandørposter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general ledger, post
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 1f6060eb7672b332fb570eb13fe027a3b58e6594
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215256"
---
# <a name="general-journal-post-line-overview"></a><span data-ttu-id="fddea-103">Oversikt over Finanskladd – bokfør linje</span><span class="sxs-lookup"><span data-stu-id="fddea-103">General Journal Post Line Overview</span></span>

<span data-ttu-id="fddea-104">Kodeenhet 12, **Finanskladd – bokfør linje**, er det store programobjektet for finansbokføring og det eneste stedet å sette inn finansposter, mva-poster og kunde- og leverandørposter.</span><span class="sxs-lookup"><span data-stu-id="fddea-104">Codeunit 12, **Gen. Jnl.-Post Line**, is the major application object for general ledger posting and is the only place to insert general ledger, VAT, and customer and vendor ledger entries.</span></span> <span data-ttu-id="fddea-105">Denne kodeenheten brukes også for alle operasjoner med Utlign, Opphev utligning og Tilbakefør.</span><span class="sxs-lookup"><span data-stu-id="fddea-105">This codeunit is also used for all Apply, Unapply and Reverse operations.</span></span>  
  
<span data-ttu-id="fddea-106">I Microsoft Dynamics NAV 2013 R2 ble codeunit utformet på nytt fordi den hadde blitt svært stor, med ca. 7 600 kodelinjer.</span><span class="sxs-lookup"><span data-stu-id="fddea-106">In Microsoft Dynamics NAV 2013 R2, the codeunit was redesigned because it had become very large, with approximately 7,600 code lines.</span></span> <span data-ttu-id="fddea-107">Arkitekturen ble endret, og codeunit er forenklet og gjort enklere å vedlikeholde.</span><span class="sxs-lookup"><span data-stu-id="fddea-107">The architecture was changed and the codeunit has been made simpler and more maintainable.</span></span> <span data-ttu-id="fddea-108">Denne dokumentasjonen beskriver endringene og inneholder informasjon du trenger for å oppgradere.</span><span class="sxs-lookup"><span data-stu-id="fddea-108">This documentation describes the changes and provides information that you will need for upgrade.</span></span>  
  
## <a name="old-architecture"></a><span data-ttu-id="fddea-109">Gammel arkitektur</span><span class="sxs-lookup"><span data-stu-id="fddea-109">Old Architecture</span></span>  
<span data-ttu-id="fddea-110">Den gamle arkitekturen hadde følgende funksjoner:</span><span class="sxs-lookup"><span data-stu-id="fddea-110">The old architecture had the following features:</span></span>  
  
* <span data-ttu-id="fddea-111">Det var omfattende bruk av globale variabler, som øker risikoen for skjulte feil som skyldes bruk av variabler med feil omfang.</span><span class="sxs-lookup"><span data-stu-id="fddea-111">There was extensive use of global variables, which increased the possibility of hidden errors due to use of variables with the wrong scope.</span></span>  
* <span data-ttu-id="fddea-112">Det var mange lange prosedyrer (med flere enn 100 kodelinjer) som også hadde høy syklomatisk kompleksitet (det vil si mange nestede CASE-, REPEAT- og IF-setninger), som gjorde det veldig vanskelig å lese og vedlikeholde koden.</span><span class="sxs-lookup"><span data-stu-id="fddea-112">There were many long procedures (with more than 100 code lines) that also had high cyclomatic complexity (that is, a lot of CASE, REPEAT, IF nested statements), which made the code very difficult to read and maintain.</span></span>  
* <span data-ttu-id="fddea-113">Flere prosedyrer som bare ble brukt lokalt og bare var ment å brukes lokalt, var ikke merket som lokale.</span><span class="sxs-lookup"><span data-stu-id="fddea-113">Several procedures that were only used locally and were only meant to be used locally were not marked as local.</span></span>  
* <span data-ttu-id="fddea-114">De fleste prosedyrene hadde ingen parametere og brukte globale variabler.</span><span class="sxs-lookup"><span data-stu-id="fddea-114">Most procedures had no parameters and used global variables.</span></span> <span data-ttu-id="fddea-115">Noen brukte parametere og overstyrte globale variabler med lokale.</span><span class="sxs-lookup"><span data-stu-id="fddea-115">Some used parameters and overrode global variables with locals.</span></span>  
* <span data-ttu-id="fddea-116">Kodemønstre for å søke i finanskonti og opprette finansposter og mva-poster var ikke standardisert og varierte fra sted til sted.</span><span class="sxs-lookup"><span data-stu-id="fddea-116">Code patterns for searching the general ledger accounts and creating general ledger and VAT entries was not standardized and varied from place to place.</span></span> <span data-ttu-id="fddea-117">I tillegg var det mye duplisering av kode og brutt symmetri mellom kunde- og leverandørkode.</span><span class="sxs-lookup"><span data-stu-id="fddea-117">In addition, there was a lot of code duplication and broken symmetry between customer and vendor code.</span></span>  
* <span data-ttu-id="fddea-118">En stor del av koden i kodeenhet 12, omtrent 30 prosent, er knyttet til kontantrabatt og toleranseberegninger, selv om disse funksjonene ikke er nødvendige i mange land og regioner.</span><span class="sxs-lookup"><span data-stu-id="fddea-118">A large part of the code in codeunit 12, approximately 30 percent, related to payment discount and tolerance calculations, although these features are not needed in many countries or regions.</span></span>  
* <span data-ttu-id="fddea-119">Bokføring, Utlign, Opphev utligning, Tilbakefør, Kontantrabatt, Betalingstoleranse og Valutakursjustering var tilknyttet i kodeenhet 12 ved hjelp av en lang liste med globale variabler.</span><span class="sxs-lookup"><span data-stu-id="fddea-119">Posting, Apply, Unapply, Reverse, Payment Discount and Tolerance, and Exchange Rate Adjustment were married together in codeunit 12 using a long list of global variables.</span></span>  
  
### <a name="new-architecture"></a><span data-ttu-id="fddea-120">Ny arkitektur</span><span class="sxs-lookup"><span data-stu-id="fddea-120">New Architecture</span></span>  
<span data-ttu-id="fddea-121">Kodeenhet 12 har fått følgende forbedringer i [!INCLUDE[prod_short](includes/prod_short.md)]:</span><span class="sxs-lookup"><span data-stu-id="fddea-121">In [!INCLUDE[prod_short](includes/prod_short.md)], codeunit 12 has had the following improvements:</span></span>  
  
* <span data-ttu-id="fddea-122">Kodeenhet 12 er refaktorert til mindre prosedyrer (alle er færre enn 100 kodelinjer).</span><span class="sxs-lookup"><span data-stu-id="fddea-122">Codeunit 12 has been refactored into smaller procedures (all less than 100 code lines).</span></span>  
* <span data-ttu-id="fddea-123">Standardiserte mønstre for søk i finanskonti er implementert ved hjelp av hjelperfunksjoner fra Bokføringsgruppe-tabeller.</span><span class="sxs-lookup"><span data-stu-id="fddea-123">Standardized patterns for the search of general ledger accounts have been implemented by using helper functions from Posting Group tables.</span></span>  
* <span data-ttu-id="fddea-124">Et rammeverk for bokføringsmotor er implementert for å behandle starten og slutten på transaksjoner og isolere opprettelsen av finansposter og mva-poster, innsamlingen av mva-justering og beregningen av flere valutabeløp.</span><span class="sxs-lookup"><span data-stu-id="fddea-124">A Posting Engine Framework has been implemented to manage the start and finish of transactions and to isolate the creation to general ledger and VAT entries, the collection of VAT adjustment, and the calculation of additional currency amounts.</span></span>  
* <span data-ttu-id="fddea-125">Duplisering av kode er eliminert.</span><span class="sxs-lookup"><span data-stu-id="fddea-125">Code duplication has been eliminated.</span></span>  
* <span data-ttu-id="fddea-126">Mange hjelperfunksjoner er overført til tilsvarende tabeller for kunde- og leverandørposter.</span><span class="sxs-lookup"><span data-stu-id="fddea-126">Many helper functions have been transferred to corresponding customer and vendor ledger entry tables.</span></span>  
* <span data-ttu-id="fddea-127">Bruken av globale variabler er minimert, slik at hver prosedyre bruker parametere og kapsler inn sin egen programlogikk.</span><span class="sxs-lookup"><span data-stu-id="fddea-127">The use of global variables has been minimized, so that each procedure uses parameters and encapsulates its own application logic.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fddea-128">Se også</span><span class="sxs-lookup"><span data-stu-id="fddea-128">See Also</span></span>

[<span data-ttu-id="fddea-129">Designdetaljer: Strukturen til bokføringsgrensesnittet</span><span class="sxs-lookup"><span data-stu-id="fddea-129">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="fddea-130">Designdetaljer: Strukturen til bokføringsmotoren</span><span class="sxs-lookup"><span data-stu-id="fddea-130">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="fddea-131">Designdetaljer: Finanskladd – bokfør linje (Dynamics NAV)</span><span class="sxs-lookup"><span data-stu-id="fddea-131">Design Details: General Journal Post Line (Dynamics NAV)</span></span>](/dynamics-nav-app/design-details-general-journal-post-line)  


[!INCLUDE[footer-include](includes/footer-banner.md)]