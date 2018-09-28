---
title: Definere aktiva | Microsoft-dokumentasjon
description: "Få informasjon om sekvensen av oppgaver du må gjøre for å definere aktiva, for eksempel maskiner eller bygninger."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: b7efd55ab57f3af627635ffc28fc3e3f31a0251b
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="setting-up-fixed-assets"></a><span data-ttu-id="cc111-103">Definere aktiva</span><span class="sxs-lookup"><span data-stu-id="cc111-103">Setting Up Fixed Assets</span></span>
<span data-ttu-id="cc111-104">Før du kan arbeide med aktiva, må du definere et par ting:</span><span class="sxs-lookup"><span data-stu-id="cc111-104">Before you can work with Fixed Assets, you need to define a few things:</span></span>  

* <span data-ttu-id="cc111-105">Hvordan du forsikrer, vedlikeholder og avskriver aktiva.</span><span class="sxs-lookup"><span data-stu-id="cc111-105">How you insure, maintain, and depreciate fixed assets.</span></span>  
* <span data-ttu-id="cc111-106">Hvordan du registrerer kostnader og andre verdier i finans.</span><span class="sxs-lookup"><span data-stu-id="cc111-106">How you record costs and other values in the general ledger.</span></span>  

<span data-ttu-id="cc111-107">Tabellen nedenfor inneholder koblinger til mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="cc111-107">The table below has links to more information.</span></span> <span data-ttu-id="cc111-108">Når du definerer disse tingene, kan du starte forskjellige aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="cc111-108">After you set those things up, you can start various activities.</span></span> <span data-ttu-id="cc111-109">Hvis du vil ha mer informasjon, kan du se [Aktiva](fa-manage.md).</span><span class="sxs-lookup"><span data-stu-id="cc111-109">For more information, see [Fixed Assets](fa-manage.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="cc111-110">Du kan registrere aktivatransaksjoner i vinduet **Aktivafinanskladd** eller **Aktivakladd**, avhengig av om transaksjonene er for finansrapportering eller intern håndtering.</span><span class="sxs-lookup"><span data-stu-id="cc111-110">You can record fixed asset transactions in the **Fixed Asset G/L Journal** or **Fixed Asset Journal** windows, depending on whether the transactions are for financial reporting or for internal management.</span></span> <span data-ttu-id="cc111-111">Hjelp for aktiva beskriver bare hvordan du bruker **Aktiva finanskladd**-vinduet.</span><span class="sxs-lookup"><span data-stu-id="cc111-111">Help for Fixed Assets only describes how to use the **Fixed Asset G/L Journal** window.</span></span>  

<span data-ttu-id="cc111-112">Når du aktiverer et aktiva i delen **Finansintegrasjon** i **Avskrivningstablåkort**-vinduet, vil **Aktivafinanskladd**-vinduet brukes til å bokføre transaksjoner for aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="cc111-112">When you enable a fixed asset activity in the **G/L Integration** section in the **Depreciation Book Card** window, the **Fixed Asset G/L Journal** window is used to post transactions for the activity.</span></span>

<span data-ttu-id="cc111-113">Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.</span><span class="sxs-lookup"><span data-stu-id="cc111-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

| <span data-ttu-id="cc111-114">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="cc111-114">To</span></span> | <span data-ttu-id="cc111-115">Se</span><span class="sxs-lookup"><span data-stu-id="cc111-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="cc111-116">Definere standard finanskonti, fordelingsnøkler, kladdemaler og kladder for aktivabokføring, og definere aktivaklasser og underklasser, for eksempel materielle og immaterielle.</span><span class="sxs-lookup"><span data-stu-id="cc111-116">Set up default G/L accounts, allocation keys, journal templates and batches for fixed asset posting, and set up fixed asset classes and subclasses, such as Tangible and Intangible.</span></span> |[<span data-ttu-id="cc111-117">Definere generell aktivainformasjon</span><span class="sxs-lookup"><span data-stu-id="cc111-117">Set Up General Fixed Assets Information</span></span>](fa-how-setup-general.md) |
| <span data-ttu-id="cc111-118">Opprette avskrivningstablåer, definere diverse avskrivningsmetoder, integrere med Finans, og gjøre det mulig å duplisere poster i flere avskrivningstablåer.</span><span class="sxs-lookup"><span data-stu-id="cc111-118">Create depreciation books, define various depreciation methods, integrate with the general ledger, and enable duplication of entries in several depreciation books.</span></span> |[<span data-ttu-id="cc111-119">Definere avskrivning for aktiva</span><span class="sxs-lookup"><span data-stu-id="cc111-119">Set Up Fixed Asset Depreciation</span></span>](fa-how-setup-depreciation.md) |
| <span data-ttu-id="cc111-120">Aktivere forsikring av aktiva, definere generelle forsikringsopplysninger, et forsikringskort per polise, og forberede kladder for bokføring av forsikringskostnader.</span><span class="sxs-lookup"><span data-stu-id="cc111-120">Enable insurance of fixed assets, set up general insurance information, an insurance card per policy, and prepare journals to post insurance costs.</span></span> |[<span data-ttu-id="cc111-121">Definere aktivaforsikring</span><span class="sxs-lookup"><span data-stu-id="cc111-121">Set Up Fixed Asset Insurance</span></span>](fa-how-setup-insurance.md) |
| <span data-ttu-id="cc111-122">Aktivere vedlikehold av aktiva, definere generell vedlikeholdsinformasjon, definere kontoer for postering av vedlikehold, og definere typer av vedlikeholdsarbeid.</span><span class="sxs-lookup"><span data-stu-id="cc111-122">Enable maintenance of fixed assets, set up general maintenance information, set up maintenance posting accounts, and define types of maintenance work.</span></span> |[<span data-ttu-id="cc111-123">Definere aktivavedlikehold</span><span class="sxs-lookup"><span data-stu-id="cc111-123">Set Up Fixed Asset Maintenance</span></span>](fa-how-setup-maintenance.md) |
| <span data-ttu-id="cc111-124">Lær mer om ulike avskrivningsmetoder for aktiva.</span><span class="sxs-lookup"><span data-stu-id="cc111-124">Learn about different fixed asset depreciation methods.</span></span> |[<span data-ttu-id="cc111-125">Avskrivningsmetoder</span><span class="sxs-lookup"><span data-stu-id="cc111-125">Depreciation Methods</span></span>](fa-depreciation-methods.md) |

## <a name="see-also"></a><span data-ttu-id="cc111-126">Se også</span><span class="sxs-lookup"><span data-stu-id="cc111-126">See Also</span></span>
[<span data-ttu-id="cc111-127">Anleggsmidler</span><span class="sxs-lookup"><span data-stu-id="cc111-127">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="cc111-128">Finans</span><span class="sxs-lookup"><span data-stu-id="cc111-128">Finance</span></span>](finance.md)  
[<span data-ttu-id="cc111-129">Komme i gang</span><span class="sxs-lookup"><span data-stu-id="cc111-129">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="cc111-130">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cc111-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

