---
title: Definere aktiva | Microsoft-dokumentasjon
description: "Få informasjon om sekvensen av oppgaver du må gjøre for å definere aktiva, for eksempel maskiner eller bygninger."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9dea8be0f5b0200f97082dc25dbaa2483ad6c735
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-fixed-assets"></a><span data-ttu-id="f6923-103">Definere aktiva</span><span class="sxs-lookup"><span data-stu-id="f6923-103">Setting Up Fixed Assets</span></span>
<span data-ttu-id="f6923-104">Før du kan arbeide med aktiva, må du definere et par ting:</span><span class="sxs-lookup"><span data-stu-id="f6923-104">Before you can work with Fixed Assets, you need to define a few things:</span></span>  

* <span data-ttu-id="f6923-105">Hvordan du forsikrer, vedlikeholder og avskriver aktiva.</span><span class="sxs-lookup"><span data-stu-id="f6923-105">How you insure, maintain, and depreciate fixed assets.</span></span>  
* <span data-ttu-id="f6923-106">Hvordan du registrerer kostnader og andre verdier i finans.</span><span class="sxs-lookup"><span data-stu-id="f6923-106">How you record costs and other values in the general ledger.</span></span>  

<span data-ttu-id="f6923-107">Tabellen nedenfor inneholder koblinger til mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="f6923-107">The table below has links to more information.</span></span> <span data-ttu-id="f6923-108">Når du definerer disse tingene, kan du starte forskjellige aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="f6923-108">After you set those things up, you can start various activities.</span></span> <span data-ttu-id="f6923-109">Hvis du vil ha mer informasjon, kan du se [Aktiva](fa-manage.md).</span><span class="sxs-lookup"><span data-stu-id="f6923-109">For more information, see [Fixed Assets](fa-manage.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="f6923-110">Du kan registrere aktivatransaksjoner i vinduet **Aktivafinanskladd** eller **Aktivakladd**, avhengig av om transaksjonene er for finansrapportering eller intern håndtering.</span><span class="sxs-lookup"><span data-stu-id="f6923-110">You can record fixed asset transactions in the **Fixed Asset G/L Journal** or **Fixed Asset Journal** windows, depending on whether the transactions are for financial reporting or for internal management.</span></span> <span data-ttu-id="f6923-111">Hjelp for aktiva beskriver bare hvordan du bruker **Aktiva finanskladd**-vinduet.</span><span class="sxs-lookup"><span data-stu-id="f6923-111">Help for Fixed Assets only describes how to use the **Fixed Asset G/L Journal** window.</span></span>  

<span data-ttu-id="f6923-112">Når du aktiverer et aktiva i delen **Finansintegrasjon** i **Avskrivningstablåkort**-vinduet, vil **Aktivafinanskladd**-vinduet brukes til å bokføre transaksjoner for aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="f6923-112">When you enable a fixed asset activity in the **G/L Integration** section in the **Depreciation Book Card** window, the **Fixed Asset G/L Journal** window is used to post transactions for the activity.</span></span>

> [!NOTE]  
>  <span data-ttu-id="f6923-113">Denne funksjonen krever at opplevelsen er satt til **Suite**.</span><span class="sxs-lookup"><span data-stu-id="f6923-113">This functionality requires that the experience is set to **Suite**.</span></span> <span data-ttu-id="f6923-114">Hvis du vil ha mer informasjon, kan du se [Tilpasse Financials-opplevelsen](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="f6923-114">For more information, see [Customizing Your Financials Experience](ui-experiences.md).</span></span>  

<span data-ttu-id="f6923-115">Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.</span><span class="sxs-lookup"><span data-stu-id="f6923-115">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

| <span data-ttu-id="f6923-116">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="f6923-116">To</span></span> | <span data-ttu-id="f6923-117">Se</span><span class="sxs-lookup"><span data-stu-id="f6923-117">See</span></span> |
| --- | --- |
| <span data-ttu-id="f6923-118">Definere standard finanskonti, fordelingsnøkler, kladdemaler og kladder for aktivabokføring, og definere aktivaklasser og underklasser, for eksempel materielle og immaterielle.</span><span class="sxs-lookup"><span data-stu-id="f6923-118">Set up default G/L accounts, allocation keys, journal templates and batches for fixed asset posting, and set up fixed asset classes and subclasses, such as Tangible and Intangible.</span></span> |[<span data-ttu-id="f6923-119">Definere generell aktivainformasjon</span><span class="sxs-lookup"><span data-stu-id="f6923-119">How to: Set Up General Fixed Assets Information</span></span>](fa-how-setup-general.md) |
| <span data-ttu-id="f6923-120">Opprette avskrivningstablåer, definere diverse avskrivningsmetoder, integrere med Finans, og gjøre det mulig å duplisere poster i flere avskrivningstablåer.</span><span class="sxs-lookup"><span data-stu-id="f6923-120">Create depreciation books, define various depreciation methods, integrate with the general ledger, and enable duplication of entries in several depreciation books.</span></span> |[<span data-ttu-id="f6923-121">Definere avskrivning av aktiva</span><span class="sxs-lookup"><span data-stu-id="f6923-121">How to: Set Up Fixed Asset Depreciation</span></span>](fa-how-setup-depreciation.md) |
| <span data-ttu-id="f6923-122">Aktivere forsikring av aktiva, definere generelle forsikringsopplysninger, et forsikringskort per polise, og forberede kladder for bokføring av forsikringskostnader.</span><span class="sxs-lookup"><span data-stu-id="f6923-122">Enable insurance of fixed assets, set up general insurance information, an insurance card per policy, and prepare journals to post insurance costs.</span></span> |[<span data-ttu-id="f6923-123">Definere aktivaforsikring</span><span class="sxs-lookup"><span data-stu-id="f6923-123">How to: Set Up Fixed Asset Insurance</span></span>](fa-how-setup-insurance.md) |
| <span data-ttu-id="f6923-124">Aktivere vedlikehold av aktiva, definere generell vedlikeholdsinformasjon, definere kontoer for postering av vedlikehold, og definere typer av vedlikeholdsarbeid.</span><span class="sxs-lookup"><span data-stu-id="f6923-124">Enable maintenance of fixed assets, set up general maintenance information, set up maintenance posting accounts, and define types of maintenance work.</span></span> |[<span data-ttu-id="f6923-125">Definere vedlikehold av aktiva</span><span class="sxs-lookup"><span data-stu-id="f6923-125">How to: Set Up Fixed Asset Maintenance</span></span>](fa-how-setup-maintenance.md) |
| <span data-ttu-id="f6923-126">Lær mer om ulike avskrivningsmetoder for aktiva.</span><span class="sxs-lookup"><span data-stu-id="f6923-126">Learn about different fixed asset depreciation methods.</span></span> |[<span data-ttu-id="f6923-127">Avskrivningsmetoder</span><span class="sxs-lookup"><span data-stu-id="f6923-127">Depreciation Methods</span></span>](fa-depreciation-methods.md) |

## <a name="see-also"></a><span data-ttu-id="f6923-128">Se også</span><span class="sxs-lookup"><span data-stu-id="f6923-128">See Also</span></span>
[<span data-ttu-id="f6923-129">Aktiva</span><span class="sxs-lookup"><span data-stu-id="f6923-129">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="f6923-130">Finans</span><span class="sxs-lookup"><span data-stu-id="f6923-130">Finance</span></span>](finance.md)  
<span data-ttu-id="f6923-131">[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="f6923-131">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="f6923-132">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f6923-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

