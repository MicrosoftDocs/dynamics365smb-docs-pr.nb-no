---
title: Tips og triks - RapidStart Services | Microsoft-dokumentasjon
description: Når du konfigurerer selskaper som bruker RapidStart Services, kan du dra nytte av noen tips og råd for å sikre en problemfri implementering.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d37c15320724412b757225b506fbee8e588164da
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385627"
---
# <a name="tips-and-tricks-rapidstart-services"></a><span data-ttu-id="fa7d5-103">Tips og triks: RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="fa7d5-103">Tips and Tricks: RapidStart Services</span></span>

<span data-ttu-id="fa7d5-104">Når du konfigurerer selskaper som bruker RapidStart Services, kan du dra nytte av noen tips og råd for å sikre en problemfri implementering.</span><span class="sxs-lookup"><span data-stu-id="fa7d5-104">When you configure companies using RapidStart Services, there are some tips and tricks that you can take advantage of to help your implementation go smoothly.</span></span>  

## <a name="take-advantage-of-configuration-templates"></a><span data-ttu-id="fa7d5-105">Dra nytte av konfigurasjonsmaler</span><span class="sxs-lookup"><span data-stu-id="fa7d5-105">Take advantage of configuration templates</span></span>

<span data-ttu-id="fa7d5-106">Konfigurasjonsmaler kan hjelpe deg med å strømlinjeforme implementeringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="fa7d5-106">Configuration templates can help you streamline your implementation process.</span></span> <span data-ttu-id="fa7d5-107">Ved å bruke disse kan du inkludere lignende kunder i segmenter og deretter utvikle en implementeringsprotokoll som behandler alle kunder i et segment på lignende måte.</span><span class="sxs-lookup"><span data-stu-id="fa7d5-107">By using them, you can include similar customers in segments and then develop an implementation protocol that treats all customers in a segment in a similar manner.</span></span> <span data-ttu-id="fa7d5-108">Dermed kan du bruke et forhåndskonfigurasjonsnivå på hvert segment og fortsette med rask implementering.</span><span class="sxs-lookup"><span data-stu-id="fa7d5-108">In that way, you can apply a level of preconfiguration to each segment and continue with a rapid implementation.</span></span>  

## <a name="configuration-questionnaires"></a><span data-ttu-id="fa7d5-109">Konfigurasjonsspørreskjemaer</span><span class="sxs-lookup"><span data-stu-id="fa7d5-109">Configuration questionnaires</span></span>

<span data-ttu-id="fa7d5-110">Du bør vurdere å definere standardsvar for å angi anbefalte fremgangsmåter for å forenkle prosessen med å fylle ut konfigurasjonsspørreskjema.</span><span class="sxs-lookup"><span data-stu-id="fa7d5-110">To aid the process of filling out a configuration questionnaire, consider defining default answers to indicate best practices.</span></span>  

## <a name="batch-creation-of-journal-lines"></a><span data-ttu-id="fa7d5-111">Masseoppretting av kladdelinjer</span><span class="sxs-lookup"><span data-stu-id="fa7d5-111">Batch creation of journal lines</span></span>

<span data-ttu-id="fa7d5-112">Vi anbefaler at du bruker verktøyene for dataflytting til å flytte kladdeposter.</span><span class="sxs-lookup"><span data-stu-id="fa7d5-112">We recommend that you use the data migration tools provided to migrate journal entries.</span></span> <span data-ttu-id="fa7d5-113">Ellers, hvis du bruker en kjørsel for å opprette kladdelinjer, som har et begrenset omfang og bare genererer pre-standardfelt i en kladd.</span><span class="sxs-lookup"><span data-stu-id="fa7d5-113">Otherwise, if you use a batch job to create journal lines, that has a limited scope and only generates pre-default fields into a journal.</span></span> <span data-ttu-id="fa7d5-114">Resten av kladden må deretter fylles ut manuelt.</span><span class="sxs-lookup"><span data-stu-id="fa7d5-114">The rest of the journal then has to be completed manually.</span></span>  

## <a name="migrating-transactions"></a><span data-ttu-id="fa7d5-115">Flytte transaksjoner</span><span class="sxs-lookup"><span data-stu-id="fa7d5-115">Migrating transactions</span></span>

<span data-ttu-id="fa7d5-116">Vi anbefaler at du flytter inngående balanser i følgende rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="fa7d5-116">We recommend that you migrate opening balances in the following order.</span></span> <!--Be aware that you cannot insert ledger entries directly. Instead you must use journals to post the journal lines-->

1. <span data-ttu-id="fa7d5-117">Flytt finanskontoens inngående balanser uten å bruke finanskontoens underliggende poster.</span><span class="sxs-lookup"><span data-stu-id="fa7d5-117">Migrate general ledger opening balances without using the general ledger account subledgers.</span></span> <span data-ttu-id="fa7d5-118">Bruk bestemte motkonti for inngående balanse der én er definert for hvert underregnskap.</span><span class="sxs-lookup"><span data-stu-id="fa7d5-118">Use specific opening balance offsetting accounts, one set up for each subledger.</span></span> <span data-ttu-id="fa7d5-119">Definer motkontoer for å aktivere direkte bokføringer.</span><span class="sxs-lookup"><span data-stu-id="fa7d5-119">Set up the offsetting accounts to enable direct postings.</span></span>  
2. <span data-ttu-id="fa7d5-120">Flytt åpne kundeposter.</span><span class="sxs-lookup"><span data-stu-id="fa7d5-120">Migrate open customer ledger entries.</span></span>  <!--work on these-->
3. <span data-ttu-id="fa7d5-121">Flytte åpne vareposter.</span><span class="sxs-lookup"><span data-stu-id="fa7d5-121">Migrate open item ledger entries.</span></span>  
4. <span data-ttu-id="fa7d5-122">Flytte åpne aktivaposter.</span><span class="sxs-lookup"><span data-stu-id="fa7d5-122">Migrate open fixed asset entries.</span></span>  

## <a name="make-each-package-manageable"></a><span data-ttu-id="fa7d5-123">Gjøre hver pakke håndterbar</span><span class="sxs-lookup"><span data-stu-id="fa7d5-123">Make each package manageable</span></span>

<span data-ttu-id="fa7d5-124">Når du bruker konfigurasjonspakker til å overføre data, deler du dataene inn i separate pakker for å gjøre det enklere å flytte dem.</span><span class="sxs-lookup"><span data-stu-id="fa7d5-124">When you use configuration packages to migrate data, separate the data into separate packages for easier portability.</span></span> <span data-ttu-id="fa7d5-125">Hvis du for eksempel vil overføre 20 år med poster, kan importen ta mange timer og dager.</span><span class="sxs-lookup"><span data-stu-id="fa7d5-125">For example, if you want to migrate 20 years of ledger entries, the import might take many hours and days.</span></span> <span data-ttu-id="fa7d5-126">Du kan i stedet dele inn dataene slik at hver pakke blir mer håndterbar.</span><span class="sxs-lookup"><span data-stu-id="fa7d5-126">Instead, split the data up so that each package becomes more manageable.</span></span> <span data-ttu-id="fa7d5-127">Det er for øyeblikket ingen faste regler for hva som gjør en pakke effektiv, men hvis du får problemer med å importere eller eksportere en pakke, kan du prøve å gjøre den mindre og se om det hjelper.</span><span class="sxs-lookup"><span data-stu-id="fa7d5-127">Currently, there are no firm rules for what makes a package performant, but if you see problems importing or exporting a package, try making it smaller and see if that helps.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fa7d5-128">Se også</span><span class="sxs-lookup"><span data-stu-id="fa7d5-128">See Also</span></span>

[<span data-ttu-id="fa7d5-129">Konfigurere et selskap med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="fa7d5-129">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="fa7d5-130">Administrasjon</span><span class="sxs-lookup"><span data-stu-id="fa7d5-130">Administration</span></span>](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]