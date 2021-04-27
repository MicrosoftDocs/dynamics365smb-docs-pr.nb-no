---
title: Vise objekter som webtjenester
description: Publiser objekter som webtjenester, slik at de umiddelbart blir tilgjengelige for Business Central-løsningen din.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 59b6febc147687e88f11423b4ad317ab6ee5a408
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775950"
---
# <a name="publish-a-web-service"></a><span data-ttu-id="bfb87-103">Publisere en webtjeneste</span><span class="sxs-lookup"><span data-stu-id="bfb87-103">Publish a Web Service</span></span>

<span data-ttu-id="bfb87-104">Webtjenester er en lett måte å gjøre programfunksjonalitet tilgjengelig for forskjellige eksterne systemer og brukere.</span><span class="sxs-lookup"><span data-stu-id="bfb87-104">Web services are a lightweight way to make application functionality available to different kinds of external systems and users.</span></span> <span data-ttu-id="bfb87-105">Som standard viser [!INCLUDE[prod_short](includes/prod_short.md)] flere objekter som webtjenester for bedre integrasjon med andre Microsoft-tjenester.</span><span class="sxs-lookup"><span data-stu-id="bfb87-105">By default, [!INCLUDE[prod_short](includes/prod_short.md)] exposes a number of objects as web services for better integration with other Microsoft services.</span></span> <span data-ttu-id="bfb87-106">Du kan legge til andre webtjenester etter behov.</span><span class="sxs-lookup"><span data-stu-id="bfb87-106">You can add other web services as your business requires.</span></span>  

<span data-ttu-id="bfb87-107">Sett opp en webtjeneste i [!INCLUDE[prod_short](includes/prod_short.md)], og publiser deretter webtjenesten slik at den er tilgjengelig for godkjente brukere.</span><span class="sxs-lookup"><span data-stu-id="bfb87-107">Set up a web service in [!INCLUDE[prod_short](includes/prod_short.md)], and then publish the web service so that it is available to authenticated users.</span></span> <span data-ttu-id="bfb87-108">Alle autoriserte brukere har tilgang til metadata for webtjenester, men bare brukere som har tilstrekkelige tillatelser, har tilgang til faktiske data.</span><span class="sxs-lookup"><span data-stu-id="bfb87-108">All authorized users can access metadata for web services, but only users who have sufficient permissions can access actual data.</span></span>  

## <a name="creating-and-publishing-a-web-service"></a><span data-ttu-id="bfb87-109">Opprette og publisere en webtjeneste</span><span class="sxs-lookup"><span data-stu-id="bfb87-109">Creating and Publishing a Web Service</span></span>

<span data-ttu-id="bfb87-110">De følgende trinnene forklarer hvordan du oppretter og publiserer en webtjeneste.</span><span class="sxs-lookup"><span data-stu-id="bfb87-110">The following steps explain how to create and publish a web service.</span></span>  

### <a name="to-create-and-publish-a-web-service"></a><span data-ttu-id="bfb87-111">Slik oppretter og publiserer du en webtjeneste</span><span class="sxs-lookup"><span data-stu-id="bfb87-111">To create and publish a web service</span></span>  

1. <span data-ttu-id="bfb87-112">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Webtjenester**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="bfb87-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bfb87-113">På siden **Webtjenester** velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="bfb87-113">On the **Web Services** page, choose **New**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > <span data-ttu-id="bfb87-114">**Kodeenhet** og **Side** er gyldige typer for SOAP-webtjenester.</span><span class="sxs-lookup"><span data-stu-id="bfb87-114">**Codeunit** and **Page** are valid types for SOAP web services.</span></span> <span data-ttu-id="bfb87-115">**Side** og **Spørring** er gyldige typer for OData-webtjenester.</span><span class="sxs-lookup"><span data-stu-id="bfb87-115">**Page** and **Query** are valid types for OData web services.</span></span> <span data-ttu-id="bfb87-116">Fra og med versjon 16.3 er **Codeunit** også en gyldig type for OData v4-webtjenester, men ingen URL-adresse vises i brukergrensesnittet.</span><span class="sxs-lookup"><span data-stu-id="bfb87-116">Starting with version 16.3, **Codeunit** is also a valid type for OData v4 web services, but then no URL is shown in the user interface.</span></span> <span data-ttu-id="bfb87-117">Hvis databasen inneholder flere selskaper, kan du også velge en objekt-ID som er spesifikk for ett av selskapene.</span><span class="sxs-lookup"><span data-stu-id="bfb87-117">Also, if the database contains multiple companies, you can choose an object ID that is specific to one of the companies.</span></span>  
    > <span data-ttu-id="bfb87-118">Tjenestenavnet er synlig for brukere av webtjenesten, og brukes som grunnlag for å identifisere og skjelne webtjenester, så du bør velge et meningsfullt navn.</span><span class="sxs-lookup"><span data-stu-id="bfb87-118">Finally, the service name is visible to consumers of your web service and is the basis for identifying and distinguishing web services, so you should make the name meaningful.</span></span>

3. <span data-ttu-id="bfb87-119">Merk avmerkingsboksen i kolonnen **Publisert**.</span><span class="sxs-lookup"><span data-stu-id="bfb87-119">Select the check box in the **Published** column.</span></span>  

<span data-ttu-id="bfb87-120">Når du publiserer webtjenesten, viser feltene **OData-URL-adresse** og **SOAP-URL-adresse** de nye URL-adressene.</span><span class="sxs-lookup"><span data-stu-id="bfb87-120">When you publish the web service, the **OData URL** and **SOAP URL** fields show the new URLs.</span></span> <span data-ttu-id="bfb87-121">For codeunits som vises som OData v4-ubundne handlinger, vises imidlertid ikke URL-feltene.</span><span class="sxs-lookup"><span data-stu-id="bfb87-121">However, for codeunits that are exposed as OData v4 unbound actions, the URL fields are not shown.</span></span>  

<span data-ttu-id="bfb87-122">Du kan teste webtjenesten umiddelbart ved å velge koblingene i feltene **OData URL-adresse** og **SOAP-URL-adresse**.</span><span class="sxs-lookup"><span data-stu-id="bfb87-122">You can test the web service immediately by choosing the links in the **OData URL** and **SOAP URL** fields.</span></span> <span data-ttu-id="bfb87-123">Kopier eventuelt feltets verdi, og lagre den for senere bruk.</span><span class="sxs-lookup"><span data-stu-id="bfb87-123">Optionally, copy the value of the field and save it for later use.</span></span> <span data-ttu-id="bfb87-124">Hvis du vil teste codeunits som vises som OData v4-ubundne handlinger, følger du instruksjonene i delen [Verifisere tilgjengelighet for webtjeneste](/dynamics365/business-central/dev-itpro/developer/devenv-creating-and-interacting-with-odatav4-unbound-action#verifying-web-service-availability) i innholdet for utviklere.</span><span class="sxs-lookup"><span data-stu-id="bfb87-124">To test codeunits that are exposed as OData v4 unbound actions, follow the instructions in the [Verifying web service availability](/dynamics365/business-central/dev-itpro/developer/devenv-creating-and-interacting-with-odatav4-unbound-action#verifying-web-service-availability) section in the developer content.</span></span>

> [!NOTE]
> <span data-ttu-id="bfb87-125">Hvis objektene du eksponerer som nettjenester, ikke må være tilgjengelige fra [!INCLUDE[prod_short](includes/prod_short.md)] online, må du merke av for metodene som vises i koden, som `[Scope('OnPrem')]`.</span><span class="sxs-lookup"><span data-stu-id="bfb87-125">If the objects that you expose as web services must not be accessible from [!INCLUDE[prod_short](includes/prod_short.md)] online, you must mark the methods exposed in the code as `[Scope('OnPrem')]`.</span></span> <span data-ttu-id="bfb87-126">Se [Scope-attributtet](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute) hvis du vil ha mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="bfb87-126">For more information, see [Scope Attribute](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).</span></span>

<span data-ttu-id="bfb87-127">Når du publiserer en webtjeneste, er den tilgjengelig for eksterne parter.</span><span class="sxs-lookup"><span data-stu-id="bfb87-127">After you publish a web service, it is available to external parties.</span></span> <span data-ttu-id="bfb87-128">Du kan kontrollere tilgjengeligheten til denne webtjenesten ved hjelp av en leser, eller velge koblingen i feltene **OData URL-adresse** og **SOAP-URL-adresse** på siden **Webtjenester**.</span><span class="sxs-lookup"><span data-stu-id="bfb87-128">You can verify the availability of that web service by using a browser, or choose the link in the **OData URL** and **SOAP URL** fields on the **Web Services** page.</span></span> <span data-ttu-id="bfb87-129">Følgende fremgangsmåte viser hvordan du kan kontrollere webtjenestens tilgjengelighet for senere bruk.</span><span class="sxs-lookup"><span data-stu-id="bfb87-129">The following procedure illustrates how you can verify the availability of the web service for later use.</span></span>  

### <a name="to-verify-the-availability-of-a-web-service"></a><span data-ttu-id="bfb87-130">Slik kontrollerer du tilgjengeligheten til en webtjeneste</span><span class="sxs-lookup"><span data-stu-id="bfb87-130">To verify the availability of a web service</span></span>  

1. <span data-ttu-id="bfb87-131">Angi den aktuelle URL-adressen i nettleseren.</span><span class="sxs-lookup"><span data-stu-id="bfb87-131">In your browser, enter the relevant URL.</span></span> <span data-ttu-id="bfb87-132">Tabellen nedenfor viser hvilke typer URL-adresser som du kan angi for ulike webtjenestetyper.</span><span class="sxs-lookup"><span data-stu-id="bfb87-132">The following table illustrates the types of URLs that you can enter for different web service types.</span></span>  

    > [!div class="mx-tdBreakAll"]
    > |<span data-ttu-id="bfb87-133">Type</span><span class="sxs-lookup"><span data-stu-id="bfb87-133">Type</span></span>|<span data-ttu-id="bfb87-134">Syntaks</span><span class="sxs-lookup"><span data-stu-id="bfb87-134">Syntax</span></span>|<span data-ttu-id="bfb87-135">Eksempel</span><span class="sxs-lookup"><span data-stu-id="bfb87-135">Example</span></span>|
    > |----------------|------|-------|
    > |<span data-ttu-id="bfb87-136">SOAP</span><span class="sxs-lookup"><span data-stu-id="bfb87-136">SOAP</span></span>|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/` |`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |<span data-ttu-id="bfb87-137">OData V4</span><span class="sxs-lookup"><span data-stu-id="bfb87-137">OData V4</span></span>|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*`|`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    <span data-ttu-id="bfb87-138">Selskapsnavnet skiller mellom store og små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="bfb87-138">The company name is case-sensitive.</span></span>|

2. <span data-ttu-id="bfb87-139">Se gjennom informasjone som vises i webleseren.</span><span class="sxs-lookup"><span data-stu-id="bfb87-139">Review the information that is displayed in the browser.</span></span> <span data-ttu-id="bfb87-140">Kontroller at du kan se navnet på webtjenesten som du har opprettet.</span><span class="sxs-lookup"><span data-stu-id="bfb87-140">Verify that you can see the name of the web service that you have created.</span></span>  

<span data-ttu-id="bfb87-141">Når du åpner en webtjeneste, og du vil skrive data tilbake til [!INCLUDE[prod_short](includes/prod_short.md)], må du angi firmanavnet.</span><span class="sxs-lookup"><span data-stu-id="bfb87-141">When you access a web service, and you want to write data back to [!INCLUDE[prod_short](includes/prod_short.md)], you must specify the company name.</span></span> <span data-ttu-id="bfb87-142">Du kan angi selskapet som en del av URI-en som vist i eksemplene, eller angi selskapet som en del av spørringsparameterne.</span><span class="sxs-lookup"><span data-stu-id="bfb87-142">You can specify the company as part of the URI as shown in the examples; alternatively, specify the company as part of the query parameters.</span></span> <span data-ttu-id="bfb87-143">Følgende URIer peker for eksempel til den samme OData web-tjenesten, og de er begge gyldige URIer.</span><span class="sxs-lookup"><span data-stu-id="bfb87-143">For example, the following URIs point to the same OData web service and are both valid URIs.</span></span>  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a><span data-ttu-id="bfb87-144">Se også</span><span class="sxs-lookup"><span data-stu-id="bfb87-144">See Also</span></span>

[<span data-ttu-id="bfb87-145">Administrasjon</span><span class="sxs-lookup"><span data-stu-id="bfb87-145">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="bfb87-146">Business Central-webtjenester for utviklere</span><span class="sxs-lookup"><span data-stu-id="bfb87-146">Business Central Web Services for developers</span></span>](/dynamics365/business-central/dev-itpro/webservices/web-services)  
[<span data-ttu-id="bfb87-147">OData-forespørselsgrenser</span><span class="sxs-lookup"><span data-stu-id="bfb87-147">OData request limits</span></span>](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#ODataServices)  


[!INCLUDE[footer-include](includes/footer-banner.md)]