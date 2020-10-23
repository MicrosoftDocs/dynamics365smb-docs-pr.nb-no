---
title: Vis Tabellinformasjon
description: Lær hvordan du kan vise informasjon om databasetabellene rett fra klientgrensesnittet i Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 72e220aa310515c665ce85bd43f4ebd3aac157d0
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922270"
---
# <a name="viewing-table-information"></a><span data-ttu-id="85d61-103">Vise Tabellinformasjon</span><span class="sxs-lookup"><span data-stu-id="85d61-103">Viewing Table Information</span></span>

<span data-ttu-id="85d61-104">Siden **Informasjon om 8700-tabellen** inneholder informasjon om alle system- og forretningstabeller i en Business Central-løsning.</span><span class="sxs-lookup"><span data-stu-id="85d61-104">The page **8700 Table Information** provides information about all system and business tables in a Business Central solution.</span></span> <span data-ttu-id="85d61-105">Siden viser spesielt informasjon om mengden data som tabellene inneholder.</span><span class="sxs-lookup"><span data-stu-id="85d61-105">In particular, the page displays information about the amount of data the tables contain.</span></span>

<span data-ttu-id="85d61-106">Denne informasjonen er nyttig for å feilsøke ytelsesproblemer, siden dette gir deg muligheten til å se fordelingen av datastørrelsen på tvers av tabeller.</span><span class="sxs-lookup"><span data-stu-id="85d61-106">This information is useful for troubleshooting performance problems, because let's you see the distribution of data size across tables.</span></span>

## <a name="viewing-table-information"></a><span data-ttu-id="85d61-107">Vise tabellinformasjon</span><span class="sxs-lookup"><span data-stu-id="85d61-107">Viewing table information</span></span>

<span data-ttu-id="85d61-108">For å åpne denne siden velger du ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angir **Tabellinformasjon** og velger deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="85d61-108">To open this page, select the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Table Information**, and then choose the related link.</span></span>

<span data-ttu-id="85d61-109">Følgende tabell beskriver opplysningene som er gitt for hver tabell:</span><span class="sxs-lookup"><span data-stu-id="85d61-109">The following table describes the information provided for each table:</span></span>

|<span data-ttu-id="85d61-110">Kolonne</span><span class="sxs-lookup"><span data-stu-id="85d61-110">Column</span></span>|<span data-ttu-id="85d61-111">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="85d61-111">Description</span></span>|
|------|-----------|
|<span data-ttu-id="85d61-112">Selskapsnavn</span><span class="sxs-lookup"><span data-stu-id="85d61-112">Company Name</span></span>|<span data-ttu-id="85d61-113">Navnet på selskapet (hvis noen) som tabellen tilhører.</span><span class="sxs-lookup"><span data-stu-id="85d61-113">The name of the company, if any, that the table belongs to.</span></span>|
|<span data-ttu-id="85d61-114">Tabellnavn</span><span class="sxs-lookup"><span data-stu-id="85d61-114">Table Name</span></span>|<span data-ttu-id="85d61-115">Navnet på tabellen.</span><span class="sxs-lookup"><span data-stu-id="85d61-115">The name of the table.</span></span>|
|<span data-ttu-id="85d61-116">Tabellnr.</span><span class="sxs-lookup"><span data-stu-id="85d61-116">Table No.</span></span>|<span data-ttu-id="85d61-117">ID-en for tabellen</span><span class="sxs-lookup"><span data-stu-id="85d61-117">The ID of the table</span></span>|
|<span data-ttu-id="85d61-118">Antall</span><span class="sxs-lookup"><span data-stu-id="85d61-118">No.</span></span> <span data-ttu-id="85d61-119">poster</span><span class="sxs-lookup"><span data-stu-id="85d61-119">of Records</span></span>|<span data-ttu-id="85d61-120">Totalt antall poster lagret i tabellen.</span><span class="sxs-lookup"><span data-stu-id="85d61-120">The total number of records stored in the table.</span></span>|
|<span data-ttu-id="85d61-121">Poststørrelse</span><span class="sxs-lookup"><span data-stu-id="85d61-121">Record Size</span></span>|<span data-ttu-id="85d61-122">Gjennomsnittlig poststørrelse i kB/post.</span><span class="sxs-lookup"><span data-stu-id="85d61-122">The average record size in KB/record.</span></span> <span data-ttu-id="85d61-123">Verdien beregnes ved hjelp av følgende formel: 1024 (størrelse)/(antall</span><span class="sxs-lookup"><span data-stu-id="85d61-123">The value is calculated using the following formula: 1024(Size)/(No.</span></span> <span data-ttu-id="85d61-124">poster).</span><span class="sxs-lookup"><span data-stu-id="85d61-124">of Records)\`.</span></span> |

## <a name="see-also"></a><span data-ttu-id="85d61-125">Se også</span><span class="sxs-lookup"><span data-stu-id="85d61-125">See Also</span></span>

[<span data-ttu-id="85d61-126">Kontrollere sider</span><span class="sxs-lookup"><span data-stu-id="85d61-126">Inspecting Pages</span></span>](across-inspect-page.md)  
[<span data-ttu-id="85d61-127">Ytelsesartikler for utviklere</span><span class="sxs-lookup"><span data-stu-id="85d61-127">Performance Articles For Developers</span></span>](/dynamics365/business-central/dev-itpro/performance/performance-developer)  
