---
title: "Feilsøke integrering med Microsoft Flow| Microsoft-dokumentasjon"
description: "Feilsøke hvordan du kan gjøre Business Central-dataene tilgjengelige som en datakilde og angi en OData-URL-adresse til webtjenestene dine for å utvikle automatisk arbeidsflyt."
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 0818550021bf17e5a269d3e11f8db54b9ff80dfa
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="troubleshooting-integration-with-microsoft-flow---request-url-too-long"></a><span data-ttu-id="f8b21-103">Feilsøke integrering med Microsoft Flow – URL-forespørselen er for lang</span><span class="sxs-lookup"><span data-stu-id="f8b21-103">Troubleshooting Integration with Microsoft Flow - Request URL Too Long</span></span>
<span data-ttu-id="f8b21-104">Du kan bruke dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del av en arbeidsflyt i Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="f8b21-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="f8b21-105">Du må ha en gyldig konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] og med Flow.</span><span class="sxs-lookup"><span data-stu-id="f8b21-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

<span data-ttu-id="f8b21-106">Hvis du oppretter en Microsoft Flow ved hjelp av [!INCLUDE[d365fin](includes/d365fin_md.md)]-kontakten, kan du få en feilmelding som angir at den forespurte URL-adressen er for lang når du har opprettet flyten, slik som dette: **RequestUriTooLong**.</span><span class="sxs-lookup"><span data-stu-id="f8b21-106">If you are creating a Microsoft Flow using the [!INCLUDE[d365fin](includes/d365fin_md.md)] connector, you may receive an error message stating that the requsted URL is too long after creating the flow, such as the following: **RequestUriTooLong**.</span></span>

## <a name="cause"></a><span data-ttu-id="f8b21-107">Årsak</span><span class="sxs-lookup"><span data-stu-id="f8b21-107">Cause</span></span>
<span data-ttu-id="f8b21-108">En flyt ser etter endringer i dataene dine, slik at den kan utløses.</span><span class="sxs-lookup"><span data-stu-id="f8b21-108">For a flow to trigger, it looks for changes in your data.</span></span> <span data-ttu-id="f8b21-109">Når du fastslår om dataene er endret, sammenligner koblingene hurtigbufferdata med de nye dataene som forespørres fra kilden.</span><span class="sxs-lookup"><span data-stu-id="f8b21-109">When determining if your data has changed, the connectors compare the cached data to the new data requested from the source.</span></span>  

<span data-ttu-id="f8b21-110">Hvis dataforespørselen oppretter en URL-adresse som er for lang, vil den mislykkes.</span><span class="sxs-lookup"><span data-stu-id="f8b21-110">If the data request creates a URL that is too long, it will fail.</span></span> <span data-ttu-id="f8b21-111">Vanlige årsaker kan være:</span><span class="sxs-lookup"><span data-stu-id="f8b21-111">Common causes may include:</span></span>
- <span data-ttu-id="f8b21-112">Vanligvis kildetabeller med flere enn 250 rader</span><span class="sxs-lookup"><span data-stu-id="f8b21-112">Generally, any source table with over 250 rows</span></span>
- <span data-ttu-id="f8b21-113">Kildetabeller som inneholder flere tusen poster</span><span class="sxs-lookup"><span data-stu-id="f8b21-113">Source tables containing multiple thousands of records</span></span>

## <a name="workaround"></a><span data-ttu-id="f8b21-114">Løsning</span><span class="sxs-lookup"><span data-stu-id="f8b21-114">Workaround</span></span>
<span data-ttu-id="f8b21-115">Følg denne fremgangsmåten for å unngå dette.</span><span class="sxs-lookup"><span data-stu-id="f8b21-115">Follow these steps as a workaround.</span></span>
1. <span data-ttu-id="f8b21-116">Velg å redigere flyten som mislykkes.</span><span class="sxs-lookup"><span data-stu-id="f8b21-116">Choose to edit the flow that is failing.</span></span>
2. <span data-ttu-id="f8b21-117">Vis **Vis avanserte alternativer** på flytutløser.</span><span class="sxs-lookup"><span data-stu-id="f8b21-117">Expand the **Show advanced options** on the flow trigger.</span></span>
3. <span data-ttu-id="f8b21-118">I feltet **Hopp over antall** angir du antall poster som skal utelates.</span><span class="sxs-lookup"><span data-stu-id="f8b21-118">In the **Skip Count** field, enter the number of records to skip.</span></span>  
<span data-ttu-id="f8b21-119">Hvis tabellen du bruker for eksempel har 4 000 poster, angir du 4 000 som antall poster å hoppe over.</span><span class="sxs-lookup"><span data-stu-id="f8b21-119">For example, if the table that you are using as a data source has 4,000 records, enter 4,000 as the number of records to skip.</span></span>
4. <span data-ttu-id="f8b21-120">Oppdater flyten.</span><span class="sxs-lookup"><span data-stu-id="f8b21-120">Update your flow.</span></span>

> [!NOTE]  
> <span data-ttu-id="f8b21-121">Koblingen er for øyeblikket i betaversjon.</span><span class="sxs-lookup"><span data-stu-id="f8b21-121">The connector is currently in Beta.</span></span> <span data-ttu-id="f8b21-122">Oppdateringer for hvordan dataendringer er rettet for fremtidige versjoner.</span><span class="sxs-lookup"><span data-stu-id="f8b21-122">Updates to how data changes are targeted for a future release.</span></span>


## <a name="see-also"></a><span data-ttu-id="f8b21-123">Se også</span><span class="sxs-lookup"><span data-stu-id="f8b21-123">See Also</span></span>
<span data-ttu-id="f8b21-124">[Bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] i en automatisk arbeidsflyt](across-how-use-financials-data-source-flow.md)</span><span class="sxs-lookup"><span data-stu-id="f8b21-124">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow](across-how-use-financials-data-source-flow.md)</span></span>  
[<span data-ttu-id="f8b21-125">Komme i gang</span><span class="sxs-lookup"><span data-stu-id="f8b21-125">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="f8b21-126">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="f8b21-126">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="f8b21-127">[Administrere brukere og tillatelser](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="f8b21-127">[Managing Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="f8b21-128">[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="f8b21-128">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="f8b21-129">Finans</span><span class="sxs-lookup"><span data-stu-id="f8b21-129">Finance</span></span>](finance.md)  

