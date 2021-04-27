---
title: Vis Tabellinformasjon
description: Lær hvordan du kan vise informasjon om databasetabellene rett fra klientgrensesnittet i Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 7a01143dd7928d5996c1620676a758ea634bdf5d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776894"
---
# <a name="viewing-table-information"></a><span data-ttu-id="6e088-103">Vise Tabellinformasjon</span><span class="sxs-lookup"><span data-stu-id="6e088-103">Viewing Table Information</span></span>

<span data-ttu-id="6e088-104">Siden **Informasjon om 8700-tabellen** inneholder informasjon om alle system- og forretningstabeller i en Business Central-løsning.</span><span class="sxs-lookup"><span data-stu-id="6e088-104">The page **8700 Table Information** provides information about all system and business tables in a Business Central solution.</span></span> <span data-ttu-id="6e088-105">Siden viser spesielt informasjon om mengden data som tabellene inneholder.</span><span class="sxs-lookup"><span data-stu-id="6e088-105">In particular, the page displays information about the amount of data the tables contain.</span></span>

<span data-ttu-id="6e088-106">Denne informasjonen er nyttig for å feilsøke ytelsesproblemer, siden dette gir deg muligheten til å se fordelingen av datastørrelsen på tvers av tabeller.</span><span class="sxs-lookup"><span data-stu-id="6e088-106">This information is useful for troubleshooting performance problems, because let's you see the distribution of data size across tables.</span></span>

## <a name="viewing-table-information"></a><span data-ttu-id="6e088-107">Vise tabellinformasjon</span><span class="sxs-lookup"><span data-stu-id="6e088-107">Viewing table information</span></span>

<span data-ttu-id="6e088-108">For å åpne denne siden velger du ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angir **Tabellinformasjon** og velger deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="6e088-108">To open this page, select the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Table Information**, and then choose the related link.</span></span>

<span data-ttu-id="6e088-109">Følgende tabell beskriver opplysningene som er gitt for hver tabell:</span><span class="sxs-lookup"><span data-stu-id="6e088-109">The following table describes the information provided for each table:</span></span>

|<span data-ttu-id="6e088-110">Kolonne</span><span class="sxs-lookup"><span data-stu-id="6e088-110">Column</span></span>|<span data-ttu-id="6e088-111">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="6e088-111">Description</span></span>|
|------|-----------|
|<span data-ttu-id="6e088-112">Selskapsnavn</span><span class="sxs-lookup"><span data-stu-id="6e088-112">Company Name</span></span>|<span data-ttu-id="6e088-113">Navnet på selskapet (hvis noen) som tabellen tilhører.</span><span class="sxs-lookup"><span data-stu-id="6e088-113">The name of the company, if any, that the table belongs to.</span></span>|
|<span data-ttu-id="6e088-114">Tabellnavn</span><span class="sxs-lookup"><span data-stu-id="6e088-114">Table Name</span></span>|<span data-ttu-id="6e088-115">Navnet på tabellen.</span><span class="sxs-lookup"><span data-stu-id="6e088-115">The name of the table.</span></span>|
|<span data-ttu-id="6e088-116">Tabellnr.</span><span class="sxs-lookup"><span data-stu-id="6e088-116">Table No.</span></span>|<span data-ttu-id="6e088-117">ID-en for tabellen</span><span class="sxs-lookup"><span data-stu-id="6e088-117">The ID of the table</span></span>|
|<span data-ttu-id="6e088-118">Antall</span><span class="sxs-lookup"><span data-stu-id="6e088-118">No.</span></span> <span data-ttu-id="6e088-119">poster</span><span class="sxs-lookup"><span data-stu-id="6e088-119">of Records</span></span>|<span data-ttu-id="6e088-120">Totalt antall poster lagret i tabellen.</span><span class="sxs-lookup"><span data-stu-id="6e088-120">The total number of records stored in the table.</span></span>|
|<span data-ttu-id="6e088-121">Poststørrelse</span><span class="sxs-lookup"><span data-stu-id="6e088-121">Record Size</span></span>|<span data-ttu-id="6e088-122">Gjennomsnittlig poststørrelse i kB/post.</span><span class="sxs-lookup"><span data-stu-id="6e088-122">The average record size in KB/record.</span></span> <span data-ttu-id="6e088-123">Verdien beregnes ved hjelp av følgende formel: 1024 (størrelse)/(antall</span><span class="sxs-lookup"><span data-stu-id="6e088-123">The value is calculated using the following formula: 1024(Size)/(No.</span></span> <span data-ttu-id="6e088-124">poster).</span><span class="sxs-lookup"><span data-stu-id="6e088-124">of Records)\`.</span></span> |

## <a name="see-also"></a><span data-ttu-id="6e088-125">Se også</span><span class="sxs-lookup"><span data-stu-id="6e088-125">See Also</span></span>

[<span data-ttu-id="6e088-126">Kontrollere sider</span><span class="sxs-lookup"><span data-stu-id="6e088-126">Inspecting Pages</span></span>](across-inspect-page.md)  
[<span data-ttu-id="6e088-127">Ytelsesartikler for utviklere</span><span class="sxs-lookup"><span data-stu-id="6e088-127">Performance Articles For Developers</span></span>](/dynamics365/business-central/dev-itpro/performance/performance-developer)  


[!INCLUDE[footer-include](includes/footer-banner.md)]