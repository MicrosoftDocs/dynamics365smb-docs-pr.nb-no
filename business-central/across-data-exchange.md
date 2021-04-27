---
title: Elektroniske dokumenter i Business Central | Microsoft-dokumentasjon
description: Innføring i å sende og motta elektroniske dokumenter i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d3eaa3ba03b661675a659fb78a3f6ec9dec08e52
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776250"
---
# <a name="exchanging-data-electronically"></a><span data-ttu-id="9cf16-103">Utveksle data elektronisk</span><span class="sxs-lookup"><span data-stu-id="9cf16-103">Exchanging Data Electronically</span></span>
<span data-ttu-id="9cf16-104">Du kan bruke rammeverket for datautveksling til å utveksle forretningsdokumenter, bankfiler, valutakurser og andre datafiler med forretningspartnerne.</span><span class="sxs-lookup"><span data-stu-id="9cf16-104">You can use the Data Exchange Framework to manage the exchange of business documents, bank files, currency exchange rates, and any other data files with your business partners.</span></span>

<span data-ttu-id="9cf16-105">I standardversjonen av [!INCLUDE[prod_short](includes/prod_short.md)] brukes rammeverket for datautveksling i funksjoner, for eksempel elektroniske dokumenter, import/eksport av bankfiler og oppdatering av valutakurser.</span><span class="sxs-lookup"><span data-stu-id="9cf16-105">In the standard version of [!INCLUDE[prod_short](includes/prod_short.md)], the Data Exchange Framework is used in features, such as Electronic Documents, Bank File Import/Export, and Currency Exchange Rates Update.</span></span> <span data-ttu-id="9cf16-106">Hvis du vil ha mer informasjon, se [Rammeverket for datautveksling](across-about-the-data-exchange-framework.md).</span><span class="sxs-lookup"><span data-stu-id="9cf16-106">For more information, see [About the Data Exchange Framework](across-about-the-data-exchange-framework.md).</span></span>

<span data-ttu-id="9cf16-107">Som administrator eller Microsoft-partner kan du bruke rammeverket i nye integrasjonsfunksjoner ved å definere hvilke data som skal utveksles, og hvordan.</span><span class="sxs-lookup"><span data-stu-id="9cf16-107">As an administrator or Microsoft partner, you can use the framework in new integration features by setting up which data to exchange and how.</span></span> <span data-ttu-id="9cf16-108">Hvis du vil ha mer informasjon, kan du se [Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md)</span><span class="sxs-lookup"><span data-stu-id="9cf16-108">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>

<span data-ttu-id="9cf16-109">Tabellen nedenfor beskriver en sekvens av oppgaver og har koblinger til emnene som beskriver dem.</span><span class="sxs-lookup"><span data-stu-id="9cf16-109">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="9cf16-110">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="9cf16-110">To</span></span>|<span data-ttu-id="9cf16-111">Se</span><span class="sxs-lookup"><span data-stu-id="9cf16-111">See</span></span>|  
|--------|---------|  
|<span data-ttu-id="9cf16-112">Lær hvordan rammeverket for datautveksling fungerer.</span><span class="sxs-lookup"><span data-stu-id="9cf16-112">Learn how the Data Exchange Framework works.</span></span>|[<span data-ttu-id="9cf16-113">Rammeverket for datautveksling</span><span class="sxs-lookup"><span data-stu-id="9cf16-113">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)|  
|<span data-ttu-id="9cf16-114">Klargjør for å utveksle data i en fil ved å bruke XML-skjemaet for filen på nytt.</span><span class="sxs-lookup"><span data-stu-id="9cf16-114">Prepare to exchange data in a file by reusing the file’s XML schema.</span></span> <span data-ttu-id="9cf16-115">Definer datautvekslingsdefinisjoner.</span><span class="sxs-lookup"><span data-stu-id="9cf16-115">Set up data exchange definitions.</span></span> <span data-ttu-id="9cf16-116">Definer hoveddata for sending av elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="9cf16-116">Set up master data for electronic document sending.</span></span> <span data-ttu-id="9cf16-117">Definer ulike felt for bankimport/-eksport.</span><span class="sxs-lookup"><span data-stu-id="9cf16-117">Set up various bank import/export fields.</span></span>|[<span data-ttu-id="9cf16-118">Definere datautveksling</span><span class="sxs-lookup"><span data-stu-id="9cf16-118">Setting Up Data Exchange</span></span>](across-set-up-data-exchange.md)|  
|<span data-ttu-id="9cf16-119">Basert på datautvekslingsdefinisjoner kan du sende PEPPOL-fakturaer, motta PEPPOL-fakturaer, importere bankkontoutdrag og eksportere bankbetalingsfiler.</span><span class="sxs-lookup"><span data-stu-id="9cf16-119">Based on data exchange definitions, send PEPPOL invoices, receive PEPPOL invoices, import bank statements, and export bank payment files.</span></span>|[<span data-ttu-id="9cf16-120">Utveksle data</span><span class="sxs-lookup"><span data-stu-id="9cf16-120">Exchanging Data</span></span>](across-exchange-data.md)|  

## <a name="see-also"></a><span data-ttu-id="9cf16-121">Se også</span><span class="sxs-lookup"><span data-stu-id="9cf16-121">See Also</span></span>  
[<span data-ttu-id="9cf16-122">Rammeverket for datautveksling</span><span class="sxs-lookup"><span data-stu-id="9cf16-122">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)  
[<span data-ttu-id="9cf16-123">Bruke XML-skjemaer til å klargjøre datautvekslingsdefinisjoner</span><span class="sxs-lookup"><span data-stu-id="9cf16-123">Use XML Schemas to Prepare Data Exchange Definitions</span></span>](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[<span data-ttu-id="9cf16-124">Definere datautveksling</span><span class="sxs-lookup"><span data-stu-id="9cf16-124">Setting Up Data Exchange</span></span>](across-set-up-data-exchange.md)  
[<span data-ttu-id="9cf16-125">Utveksle data</span><span class="sxs-lookup"><span data-stu-id="9cf16-125">Exchanging Data</span></span>](across-exchange-data.md)  
[<span data-ttu-id="9cf16-126">Inngående dokumenter</span><span class="sxs-lookup"><span data-stu-id="9cf16-126">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="9cf16-127">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="9cf16-127">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]