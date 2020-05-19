---
title: Vis Tabellinformasjon
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/20/2020
ms.author: jswymer
ms.openlocfilehash: de93063a60e6b64405b1491a67489c8bfa4657ad
ms.sourcegitcommit: 99915b493a7e49d12c530f2f9fda1fcedb518b6e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275321"
---
# <a name="viewing-table-information"></a><span data-ttu-id="79df4-102">Vise Tabellinformasjon</span><span class="sxs-lookup"><span data-stu-id="79df4-102">Viewing Table Information</span></span>

<span data-ttu-id="79df4-103">Siden **Informasjon om 8700-tabellen** inneholder informasjon om alle system- og forretningstabeller i en Business Central-løsning.</span><span class="sxs-lookup"><span data-stu-id="79df4-103">The page **8700 Table Information** provides information about all system and business tables in a Business Central solution.</span></span> <span data-ttu-id="79df4-104">Siden viser spesielt informasjon om mengden data som tabellene inneholder.</span><span class="sxs-lookup"><span data-stu-id="79df4-104">In particular, the page displays information about the amount of data the tables contain.</span></span>

<span data-ttu-id="79df4-105">Denne informasjonen er nyttig for å feilsøke ytelsesproblemer, siden dette gir deg muligheten til å se fordelingen av datastørrelsen på tvers av tabeller.</span><span class="sxs-lookup"><span data-stu-id="79df4-105">This information is useful for troubleshooting performance problems, because let's you see the distribution of data size across tables.</span></span>

## <a name="viewing-table-information"></a><span data-ttu-id="79df4-106">Vise tabellinformasjon</span><span class="sxs-lookup"><span data-stu-id="79df4-106">Viewing table information</span></span>

<span data-ttu-id="79df4-107">For å åpne denne siden velger du ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angir **Tabellinformasjon** og velger deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="79df4-107">To open this page, select the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Table Information**, and then choose the related link.</span></span>

<span data-ttu-id="79df4-108">Følgende tabell beskriver opplysningene som er gitt for hver tabell:</span><span class="sxs-lookup"><span data-stu-id="79df4-108">The following table describes the information provided for each table:</span></span>

|<span data-ttu-id="79df4-109">Kolonne</span><span class="sxs-lookup"><span data-stu-id="79df4-109">Column</span></span>|<span data-ttu-id="79df4-110">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="79df4-110">Description</span></span>|
|------|-----------|
|<span data-ttu-id="79df4-111">Selskapsnavn</span><span class="sxs-lookup"><span data-stu-id="79df4-111">Company Name</span></span>|<span data-ttu-id="79df4-112">Navnet på selskapet (hvis noen) som tabellen tilhører.</span><span class="sxs-lookup"><span data-stu-id="79df4-112">The name of the company, if any, that the table belongs to.</span></span>|
|<span data-ttu-id="79df4-113">Tabellnavn</span><span class="sxs-lookup"><span data-stu-id="79df4-113">Table Name</span></span>|<span data-ttu-id="79df4-114">Navnet på tabellen.</span><span class="sxs-lookup"><span data-stu-id="79df4-114">The name of the table.</span></span>|
|<span data-ttu-id="79df4-115">Tabellnr.</span><span class="sxs-lookup"><span data-stu-id="79df4-115">Table No.</span></span>|<span data-ttu-id="79df4-116">ID-en for tabellen</span><span class="sxs-lookup"><span data-stu-id="79df4-116">The ID of the table</span></span>|
|<span data-ttu-id="79df4-117">Antall</span><span class="sxs-lookup"><span data-stu-id="79df4-117">No.</span></span> <span data-ttu-id="79df4-118">poster</span><span class="sxs-lookup"><span data-stu-id="79df4-118">of Records</span></span>|<span data-ttu-id="79df4-119">Totalt antall poster lagret i tabellen.</span><span class="sxs-lookup"><span data-stu-id="79df4-119">The total number of records stored in the table.</span></span>|
|<span data-ttu-id="79df4-120">Poststørrelse</span><span class="sxs-lookup"><span data-stu-id="79df4-120">Record Size</span></span>|<span data-ttu-id="79df4-121">Gjennomsnittlig poststørrelse i kB/post.</span><span class="sxs-lookup"><span data-stu-id="79df4-121">The average record size in KB/record.</span></span> <span data-ttu-id="79df4-122">Verdien beregnes ved å bruke følgende formel: 1024(størrelse)/(antall</span><span class="sxs-lookup"><span data-stu-id="79df4-122">The value is calculated using the following formula: 1024(Size)/(No.</span></span> <span data-ttu-id="79df4-123">poster).</span><span class="sxs-lookup"><span data-stu-id="79df4-123">of Records)\`.</span></span> |

## <a name="see-also"></a><span data-ttu-id="79df4-124">Se også</span><span class="sxs-lookup"><span data-stu-id="79df4-124">See Also</span></span>

[<span data-ttu-id="79df4-125">Kontrollere sider</span><span class="sxs-lookup"><span data-stu-id="79df4-125">Inspecting Pages</span></span>](across-inspect-page.md)  
[<span data-ttu-id="79df4-126">Ytelsesartikler for utviklere</span><span class="sxs-lookup"><span data-stu-id="79df4-126">Performance Articles For Developers</span></span>](/dynamics365/business-central/dev-itpro/performance/performance-developer)  
