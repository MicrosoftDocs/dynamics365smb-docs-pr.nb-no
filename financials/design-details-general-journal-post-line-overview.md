---
title: "Oversikt over Finanskladd – bokfør linje | Microsoft-dokumentasjon"
description: "Dette emnet introduserer endringer i Kodeenhet 12, **Finanskladd - bokfør linje**, som er det store programobjektet for finansbokføring og det eneste stedet å sette inn finansposter, mva-poster og kunde- og leverandørposter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general ledger, post
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 77fa52505dc586dc11ca89e53f6eec75042d3606
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="general-journal-post-line-overview"></a><span data-ttu-id="44019-103">Oversikt over Finanskladd – bokfør linje</span><span class="sxs-lookup"><span data-stu-id="44019-103">General Journal Post Line Overview</span></span>
<span data-ttu-id="44019-104">Kodeenhet 12, **Finanskladd – bokfør linje**, er det store programobjektet for finansbokføring og det eneste stedet å sette inn finansposter, mva-poster og kunde- og leverandørposter.</span><span class="sxs-lookup"><span data-stu-id="44019-104">Codeunit 12, **Gen. Jnl.-Post Line**, is the major application object for general ledger posting and is the only place to insert general ledger, VAT, and customer and vendor ledger entries.</span></span> <span data-ttu-id="44019-105">Denne kodeenheten brukes også for alle operasjoner med Utlign, Opphev utligning og Tilbakefør.</span><span class="sxs-lookup"><span data-stu-id="44019-105">This codeunit is also used for all Apply, Unapply and Reverse operations.</span></span>  
  
<span data-ttu-id="44019-106">Selv om kodeenheten har blitt forbedret i hver utgivelse over de siste ti årene, har arkitekturen i hovedsak vært den samme.</span><span class="sxs-lookup"><span data-stu-id="44019-106">While the codeunit has been improved in each release over the last ten years, its architecture remained essentially unchanged.</span></span> <span data-ttu-id="44019-107">Kodeenheten ble svært stor, med omtrent 7 600 kodelinjer.</span><span class="sxs-lookup"><span data-stu-id="44019-107">The codeunit became very large, with approximately 7,600 code lines.</span></span> <span data-ttu-id="44019-108">I denne utgivelsen av [!INCLUDE[d365fin](includes/d365fin_md.md)] er arkitekturen endret, og kodeenheten er forenklet og gjort enklere å vedlikeholde.</span><span class="sxs-lookup"><span data-stu-id="44019-108">With this release of [!INCLUDE[d365fin](includes/d365fin_md.md)], the architecture is changed and the codeunit has been made simpler and more maintainable.</span></span> <span data-ttu-id="44019-109">Denne dokumentasjonen beskriver endringene og inneholder informasjon du trenger for å oppgradere.</span><span class="sxs-lookup"><span data-stu-id="44019-109">This documentation introduces the changes and provides information that you will need for upgrade.</span></span>  
  
## <a name="old-architecture"></a><span data-ttu-id="44019-110">Gammel arkitektur</span><span class="sxs-lookup"><span data-stu-id="44019-110">Old Architecture</span></span>  
<span data-ttu-id="44019-111">Den gamle arkitekturen hadde følgende funksjoner:</span><span class="sxs-lookup"><span data-stu-id="44019-111">The old architecture had the following features:</span></span>  
  
* <span data-ttu-id="44019-112">Det var omfattende bruk av globale variabler, som øker risikoen for skjulte feil som skyldes bruk av variabler med feil omfang.</span><span class="sxs-lookup"><span data-stu-id="44019-112">There was extensive use of global variables, which increased the possibility of hidden errors due to use of variables with the wrong scope.</span></span>  
* <span data-ttu-id="44019-113">Det var mange lange prosedyrer (med flere enn 100 kodelinjer) som også hadde høy syklomatisk kompleksitet (det vil si mange nestede CASE-, REPEAT- og IF-setninger), som gjorde det veldig vanskelig å lese og vedlikeholde koden.</span><span class="sxs-lookup"><span data-stu-id="44019-113">There were many long procedures (with more than 100 code lines) that also had high cyclomatic complexity (that is, a lot of CASE, REPEAT, IF nested statements), which made the code very difficult to read and maintain.</span></span>  
* <span data-ttu-id="44019-114">Flere prosedyrer som bare ble brukt lokalt og bare var ment å brukes lokalt, var ikke merket som lokale.</span><span class="sxs-lookup"><span data-stu-id="44019-114">Several procedures that were only used locally and were only meant to be used locally were not marked as local.</span></span>  
* <span data-ttu-id="44019-115">De fleste prosedyrene hadde ingen parametere og brukte globale variabler.</span><span class="sxs-lookup"><span data-stu-id="44019-115">Most procedures had no parameters and used global variables.</span></span> <span data-ttu-id="44019-116">Noen brukte parametere og overstyrte globale variabler med lokale.</span><span class="sxs-lookup"><span data-stu-id="44019-116">Some used parameters and overrode global variables with locals.</span></span>  
* <span data-ttu-id="44019-117">Kodemønstre for å søke i finanskonti og opprette finansposter og mva-poster var ikke standardisert og varierte fra sted til sted.</span><span class="sxs-lookup"><span data-stu-id="44019-117">Code patterns for searching the general ledger accounts and creating general ledger and VAT entries was not standardized and varied from place to place.</span></span> <span data-ttu-id="44019-118">I tillegg var det mye duplisering av kode og brutt symmetri mellom kunde- og leverandørkode.</span><span class="sxs-lookup"><span data-stu-id="44019-118">In addition, there was a lot of code duplication and broken symmetry between customer and vendor code.</span></span>  
* <span data-ttu-id="44019-119">En stor del av koden i kodeenhet 12, omtrent 30 prosent, er knyttet til kontantrabatt og toleranseberegninger, selv om disse funksjonene ikke er nødvendige i mange land og regioner.</span><span class="sxs-lookup"><span data-stu-id="44019-119">A large part of the code in codeunit 12, approximately 30 percent, related to payment discount and tolerance calculations, although these features are not needed in many countries or regions.</span></span>  
* <span data-ttu-id="44019-120">Bokføring, Utlign, Opphev utligning, Tilbakefør, Kontantrabatt, Betalingstoleranse og Valutakursjustering var tilknyttet i kodeenhet 12 ved hjelp av en lang liste med globale variabler.</span><span class="sxs-lookup"><span data-stu-id="44019-120">Posting, Apply, Unapply, Reverse, Payment Discount and Tolerance, and Exchange Rate Adjustment were married together in codeunit 12 using a long list of global variables.</span></span>  
  
### <a name="new-architecture"></a><span data-ttu-id="44019-121">Ny arkitektur</span><span class="sxs-lookup"><span data-stu-id="44019-121">New Architecture</span></span>  
<span data-ttu-id="44019-122">Kodeenhet 12 har fått følgende forbedringer i [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="44019-122">In [!INCLUDE[d365fin](includes/d365fin_md.md)], codeunit 12 has had the following improvements:</span></span>  
  
* <span data-ttu-id="44019-123">Kodeenhet 12 er refaktorert til mindre prosedyrer (alle er færre enn 100 kodelinjer).</span><span class="sxs-lookup"><span data-stu-id="44019-123">Codeunit 12 has been refactored into smaller procedures (all less than 100 code lines).</span></span>  
* <span data-ttu-id="44019-124">Standardiserte mønstre for søk i finanskonti er implementert ved hjelp av hjelperfunksjoner fra Bokføringsgruppe-tabeller.</span><span class="sxs-lookup"><span data-stu-id="44019-124">Standardized patterns for the search of general ledger accounts have been implemented by using helper functions from Posting Group tables.</span></span>  
* <span data-ttu-id="44019-125">Et rammeverk for bokføringsmotor er implementert for å behandle starten og slutten på transaksjoner og isolere opprettelsen av finansposter og mva-poster, innsamlingen av mva-justering og beregningen av flere valutabeløp.</span><span class="sxs-lookup"><span data-stu-id="44019-125">A Posting Engine Framework has been implemented to manage the start and finish of transactions and to isolate the creation to general ledger and VAT entries, the collection of VAT adjustment, and the calculation of additional currency amounts.</span></span>  
* <span data-ttu-id="44019-126">Duplisering av kode er eliminert.</span><span class="sxs-lookup"><span data-stu-id="44019-126">Code duplication has been eliminated.</span></span>  
* <span data-ttu-id="44019-127">Mange hjelperfunksjoner er overført til tilsvarende tabeller for kunde- og leverandørposter.</span><span class="sxs-lookup"><span data-stu-id="44019-127">Many helper functions have been transferred to corresponding customer and vendor ledger entry tables.</span></span>  
* <span data-ttu-id="44019-128">Bruken av globale variabler er minimert, slik at hver prosedyre bruker parametere og kapsler inn sin egen programlogikk.</span><span class="sxs-lookup"><span data-stu-id="44019-128">The use of global variables has been minimized, so that each procedure uses parameters and encapsulates its own application logic.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="44019-129">Se også</span><span class="sxs-lookup"><span data-stu-id="44019-129">See Also</span></span>  
<span data-ttu-id="44019-130">[Designdetaljer: Strukturen til bokføringsgrensesnittet](design-details-posting-interface-structure.md) </span><span class="sxs-lookup"><span data-stu-id="44019-130">[Design Details: Posting Interface Structure](design-details-posting-interface-structure.md) </span></span>  
[<span data-ttu-id="44019-131">Designdetaljer: Strukturen til bokføringsmotoren</span><span class="sxs-lookup"><span data-stu-id="44019-131">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)

