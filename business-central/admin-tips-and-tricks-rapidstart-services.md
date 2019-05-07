---
title: Tips og råd - RapidStart Services | Microsoft-dokumentasjon
description: Når du konfigurerer selskaper som bruker RapidStart Services, kan du dra nytte av noen tips og råd for å sikre en problemfri implementering.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6a10ab0d2e4658eba4824e44527d45cbf0f33dd8
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "936915"
---
# <a name="tips-and-tricks-rapidstart-services"></a><span data-ttu-id="8dfcf-103">Tips og råd: RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="8dfcf-103">Tips and Tricks: RapidStart Services</span></span>
<span data-ttu-id="8dfcf-104">Når du konfigurerer selskaper som bruker RapidStart Services, kan du dra nytte av noen tips og råd for å sikre en problemfri implementering.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-104">When you configure companies using RapidStart Services, there are some tips and tricks that you can take advantage of to help your implementation go smoothly.</span></span>  

## <a name="take-advantage-of-configuration-templates"></a><span data-ttu-id="8dfcf-105">Dra nytte av konfigurasjonsmaler</span><span class="sxs-lookup"><span data-stu-id="8dfcf-105">Take advantage of configuration templates</span></span>  
<span data-ttu-id="8dfcf-106">Konfigurasjonsmaler kan hjelpe deg med å strømlinjeforme implementeringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-106">Configuration templates can help you streamline your implementation process.</span></span> <span data-ttu-id="8dfcf-107">Ved å bruke disse kan du inkludere lignende kunder i segmenter og deretter utvikle en implementeringsprotokoll som behandler alle kunder i et segment på lignende måte.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-107">By using them, you can include similar customers in segments and then develop an implementation protocol that treats all customers in a segment in a similar manner.</span></span> <span data-ttu-id="8dfcf-108">Dermed kan du bruke et forhåndskonfigurasjonsnivå på hvert segment og fortsette med rask implementering.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-108">In that way, you can apply a level of preconfiguration to each segment and continue with a rapid implementation.</span></span>  

## <a name="configuration-questionnaires"></a><span data-ttu-id="8dfcf-109">Konfigurasjonsspørreskjemaer</span><span class="sxs-lookup"><span data-stu-id="8dfcf-109">Configuration questionnaires</span></span>  
<span data-ttu-id="8dfcf-110">Du bør vurdere å definere standardsvar for å angi anbefalte fremgangsmåter for å forenkle prosessen med å fylle ut konfigurasjonsspørreskjema.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-110">To aid the process of filling out a configuration questionnaire, consider defining default answers to indicate best practices.</span></span>  

## <a name="batch-creation-of-journal-lines"></a><span data-ttu-id="8dfcf-111">Masseoppretting av kladdelinjer</span><span class="sxs-lookup"><span data-stu-id="8dfcf-111">Batch creation of journal lines</span></span>  
<span data-ttu-id="8dfcf-112">Vi anbefaler at du bruker verktøyene for dataflytting til å flytte kladdeposter.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-112">We recommend that you use the data migration tools provided to migrate journal entries.</span></span> <span data-ttu-id="8dfcf-113">Ellers, hvis du bruker en kjørsel for å opprette kladdelinjer, som har et begrenset omfang og bare genererer pre-standardfelt i en kladd.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-113">Otherwise, if you use a batch job to create journal lines, that has a limited scope and only generates pre-default fields into a journal.</span></span> <span data-ttu-id="8dfcf-114">Resten av kladden må deretter fylles ut manuelt.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-114">The rest of the journal then has to be completed manually.</span></span>  

## <a name="migrating-transactions"></a><span data-ttu-id="8dfcf-115">Flytte transaksjoner</span><span class="sxs-lookup"><span data-stu-id="8dfcf-115">Migrating transactions</span></span>  
<span data-ttu-id="8dfcf-116">Vi anbefaler at du flytter inngående balanser i følgende rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-116">We recommend that you migrate opening balances in the following order.</span></span>  

1.  <span data-ttu-id="8dfcf-117">Flytt finanskontoens inngående balanser uten å bruke finanskontoens underliggende poster.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-117">Migrate general ledger opening balances without using the general ledger account subledgers.</span></span> <span data-ttu-id="8dfcf-118">Bruk bestemte motkonti for inngående balanse der én er definert for hvert underregnskap.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-118">Use specific opening balance offsetting accounts, one set up for each subledger.</span></span> <span data-ttu-id="8dfcf-119">Definer motkontoer for å aktivere direkte bokføringer.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-119">Set up the offsetting accounts to enable direct postings.</span></span>  
2.  <span data-ttu-id="8dfcf-120">Flytt åpne kundeposter.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-120">Migrate open customer ledger entries.</span></span>  
3.  <span data-ttu-id="8dfcf-121">Flytte åpne vareposter.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-121">Migrate open item ledger entries.</span></span>  
4.  <span data-ttu-id="8dfcf-122">Flytte åpne aktivaposter.</span><span class="sxs-lookup"><span data-stu-id="8dfcf-122">Migrate open fixed asset entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8dfcf-123">Se også</span><span class="sxs-lookup"><span data-stu-id="8dfcf-123">See Also</span></span>  
[<span data-ttu-id="8dfcf-124">Konfigurere et selskap med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="8dfcf-124">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="8dfcf-125">Administrasjon</span><span class="sxs-lookup"><span data-stu-id="8dfcf-125">Administration</span></span>](admin-setup-and-administration.md)
