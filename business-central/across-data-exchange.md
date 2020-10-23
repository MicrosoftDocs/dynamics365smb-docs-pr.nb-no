---
title: Elektroniske dokumenter i Business Central | Microsoft-dokumentasjon
description: Innføring i å sende og motta elektroniske dokumenter i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8c11553dc3a48a2fdf0df65258914d36f9c2efbd
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914368"
---
# <a name="exchanging-data-electronically"></a><span data-ttu-id="d2770-103">Utveksle data elektronisk</span><span class="sxs-lookup"><span data-stu-id="d2770-103">Exchanging Data Electronically</span></span>
<span data-ttu-id="d2770-104">Du kan bruke rammeverket for datautveksling til å utveksle forretningsdokumenter, bankfiler, valutakurser og andre datafiler med forretningspartnerne.</span><span class="sxs-lookup"><span data-stu-id="d2770-104">You can use the Data Exchange Framework to manage the exchange of business documents, bank files, currency exchange rates, and any other data files with your business partners.</span></span>

<span data-ttu-id="d2770-105">I standardversjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] brukes rammeverket for datautveksling i funksjoner, for eksempel elektroniske dokumenter, import/eksport av bankfiler og oppdatering av valutakurser.</span><span class="sxs-lookup"><span data-stu-id="d2770-105">In the standard version of [!INCLUDE[d365fin](includes/d365fin_md.md)], the Data Exchange Framework is used in features, such as Electronic Documents, Bank File Import/Export, and Currency Exchange Rates Update.</span></span> <span data-ttu-id="d2770-106">Hvis du vil ha mer informasjon, se [Rammeverket for datautveksling](across-about-the-data-exchange-framework.md).</span><span class="sxs-lookup"><span data-stu-id="d2770-106">For more information, see [About the Data Exchange Framework](across-about-the-data-exchange-framework.md).</span></span>

<span data-ttu-id="d2770-107">Som administrator eller Microsoft-partner kan du bruke rammeverket i nye integrasjonsfunksjoner ved å definere hvilke data som skal utveksles, og hvordan.</span><span class="sxs-lookup"><span data-stu-id="d2770-107">As an administrator or Microsoft partner, you can use the framework in new integration features by setting up which data to exchange and how.</span></span> <span data-ttu-id="d2770-108">Hvis du vil ha mer informasjon, kan du se [Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md)</span><span class="sxs-lookup"><span data-stu-id="d2770-108">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>

<span data-ttu-id="d2770-109">Tabellen nedenfor beskriver en sekvens av oppgaver og har koblinger til emnene som beskriver dem.</span><span class="sxs-lookup"><span data-stu-id="d2770-109">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="d2770-110">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="d2770-110">To</span></span>|<span data-ttu-id="d2770-111">Se</span><span class="sxs-lookup"><span data-stu-id="d2770-111">See</span></span>|  
|--------|---------|  
|<span data-ttu-id="d2770-112">Lær hvordan rammeverket for datautveksling fungerer.</span><span class="sxs-lookup"><span data-stu-id="d2770-112">Learn how the Data Exchange Framework works.</span></span>|[<span data-ttu-id="d2770-113">Rammeverket for datautveksling</span><span class="sxs-lookup"><span data-stu-id="d2770-113">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)|  
|<span data-ttu-id="d2770-114">Klargjør for å utveksle data i en fil ved å bruke XML-skjemaet for filen på nytt.</span><span class="sxs-lookup"><span data-stu-id="d2770-114">Prepare to exchange data in a file by reusing the file’s XML schema.</span></span> <span data-ttu-id="d2770-115">Definer datautvekslingsdefinisjoner.</span><span class="sxs-lookup"><span data-stu-id="d2770-115">Set up data exchange definitions.</span></span> <span data-ttu-id="d2770-116">Definer hoveddata for sending av elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="d2770-116">Set up master data for electronic document sending.</span></span> <span data-ttu-id="d2770-117">Definer ulike felt for bankimport/-eksport.</span><span class="sxs-lookup"><span data-stu-id="d2770-117">Set up various bank import/export fields.</span></span>|[<span data-ttu-id="d2770-118">Definere datautveksling</span><span class="sxs-lookup"><span data-stu-id="d2770-118">Setting Up Data Exchange</span></span>](across-set-up-data-exchange.md)|  
|<span data-ttu-id="d2770-119">Basert på datautvekslingsdefinisjoner kan du sende PEPPOL-fakturaer, motta PEPPOL-fakturaer, importere bankkontoutdrag og eksportere bankbetalingsfiler.</span><span class="sxs-lookup"><span data-stu-id="d2770-119">Based on data exchange definitions, send PEPPOL invoices, receive PEPPOL invoices, import bank statements, and export bank payment files.</span></span>|[<span data-ttu-id="d2770-120">Utveksle data</span><span class="sxs-lookup"><span data-stu-id="d2770-120">Exchanging Data</span></span>](across-exchange-data.md)|  

## <a name="see-also"></a><span data-ttu-id="d2770-121">Se også</span><span class="sxs-lookup"><span data-stu-id="d2770-121">See Also</span></span>  
[<span data-ttu-id="d2770-122">Rammeverket for datautveksling</span><span class="sxs-lookup"><span data-stu-id="d2770-122">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)  
[<span data-ttu-id="d2770-123">Bruke XML-skjemaer til å klargjøre datautvekslingsdefinisjoner</span><span class="sxs-lookup"><span data-stu-id="d2770-123">Use XML Schemas to Prepare Data Exchange Definitions</span></span>](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[<span data-ttu-id="d2770-124">Definere datautveksling</span><span class="sxs-lookup"><span data-stu-id="d2770-124">Setting Up Data Exchange</span></span>](across-set-up-data-exchange.md)  
[<span data-ttu-id="d2770-125">Utveksle data</span><span class="sxs-lookup"><span data-stu-id="d2770-125">Exchanging Data</span></span>](across-exchange-data.md)  
[<span data-ttu-id="d2770-126">Inngående dokumenter</span><span class="sxs-lookup"><span data-stu-id="d2770-126">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="d2770-127">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="d2770-127">General Business Functionality</span></span>](ui-across-business-areas.md)
