---
title: Vise objekter som webtjenester | Microsoft-dokumentasjon
description: Publiser objekter som webtjenester, slik at de umiddelbart blir tilgjengelige for Business Central-løsningen din.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 05/19/2020
ms.author: edupont
ms.openlocfilehash: c9f12f2b15c379ad1f4765f1a20e773150f33b84
ms.sourcegitcommit: d4a77522859c5561c1f3dc43178d45657ffa31b5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/26/2020
ms.locfileid: "3402456"
---
# <a name="publish-a-web-service"></a><span data-ttu-id="e5f0f-103">Publisere en webtjeneste</span><span class="sxs-lookup"><span data-stu-id="e5f0f-103">Publish a Web Service</span></span>

<span data-ttu-id="e5f0f-104">Webtjenester er en lett måte å gjøre programfunksjonalitet tilgjengelig for en rekke eksterne systemer og brukere.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-104">Web services are a lightweight way to make application functionality available to a variety of external systems and users.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="e5f0f-105">inneholder en rekke objekter som vises som webtjenester som standard på grunn av integrering med andre Microsoft-tjenester, men du kan også legge til andre webtjenester.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-105">includes an number of objects that are exposed as web services by default due to integration with other Microsoft services, but you can also add other web services.</span></span>  

<span data-ttu-id="e5f0f-106">Du definerer en webtjeneste i [!INCLUDE[d365fin](includes/d365fin_md.md)]-klienten.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-106">You set up a web service in the [!INCLUDE[d365fin](includes/d365fin_md.md)] client.</span></span> <span data-ttu-id="e5f0f-107">Du må deretter publisere webtjenesten slik at den er tilgjengelig for serviceforespørsler over nettverket.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-107">You must then publish the web service so that it is available to service requests over the network.</span></span> <span data-ttu-id="e5f0f-108">Brukere kan oppdage webtjenester ved å velge en webleser på en server og be om liste over tilgjengelige tjenester.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-108">Users can discover web services by pointing a browser at the server location and requesting a list of available services.</span></span> <span data-ttu-id="e5f0f-109">Når du publiserer en webtjeneste, er den umiddelbart tilgjengelig på nettverket for godkjente brukere.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-109">When you publish a web service, it is immediately available over the network for authenticated users.</span></span> <span data-ttu-id="e5f0f-110">Alle autoriserte brukere har tilgang til metadata for webtjenester, men bare brukere som har tilstrekkelige tillatelser, har tilgang til faktiske data.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-110">All authorized users can access metadata for web services, but only users who have sufficient permissions can access actual data.</span></span>

## <a name="creating-and-publishing-a-web-service"></a><span data-ttu-id="e5f0f-111">Opprette og publisere en webtjeneste</span><span class="sxs-lookup"><span data-stu-id="e5f0f-111">Creating and Publishing a Web Service</span></span>

<span data-ttu-id="e5f0f-112">De følgende trinnene forklarer hvordan du oppretter og publiserer en webtjeneste.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-112">The following steps explain how to create and publish a web service.</span></span>  

### <a name="to-create-and-publish-a-web-service"></a><span data-ttu-id="e5f0f-113">Slik oppretter og publiserer du en webtjeneste</span><span class="sxs-lookup"><span data-stu-id="e5f0f-113">To create and publish a web service</span></span>  

1. <span data-ttu-id="e5f0f-114">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Webtjenester**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e5f0f-115">På siden **Webtjenester** velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-115">On the **Web Services** page, choose **New**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > <span data-ttu-id="e5f0f-116">**Kodeenhet** og **Side** er gyldige typer for SOAP-webtjenester.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-116">**Codeunit** and **Page** are valid types for SOAP web services.</span></span> <span data-ttu-id="e5f0f-117">**Side** og **Spørring** er gyldige typer for OData-webtjenester.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-117">**Page** and **Query** are valid types for OData web services.</span></span>  
    > <span data-ttu-id="e5f0f-118">Hvis databasen inneholder flere selskaper, kan du også velge en objekt-ID som er spesifikk for ett av selskapene.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-118">Also, if the database contains multiple companies, you can choose an object ID that is specific to one of the companies.</span></span>  
    > <span data-ttu-id="e5f0f-119">Tjenestenavnet er synlig for brukere av webtjenesten, og brukes som grunnlag for å identifisere og skjelne webtjenester, så du bør velge et meningsfullt navn.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-119">Finally, the service name is visible to consumers of your web service and is the basis for identifying and distinguishing web services, so you should make the name meaningful.</span></span>

3. <span data-ttu-id="e5f0f-120">Merk avmerkingsboksen i kolonnen **Publisert**.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-120">Select the check box in the **Published** column.</span></span>  

<span data-ttu-id="e5f0f-121">Når du publiserer webtjenesten i feltene **OData URL-adresse** og **SOAP-URL-adresse**, kan du se URL-adressene som er generert for webtjenesten.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-121">When you publish the web service, in the **OData URL** and **SOAP URL** fields, you can see the URLs that are generated for the web service.</span></span> <span data-ttu-id="e5f0f-122">Du kan teste webtjenesten umiddelbart ved å velge koblingene i feltene **OData URL-adresse** og **SOAP-URL-adresse**.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-122">You can test the web service immediately by choosing the links in the **OData URL** and **SOAP URL** fields.</span></span> <span data-ttu-id="e5f0f-123">Du kan eventuelt kopiere feltets verdi, og lagre den for senere bruk.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-123">Optionally, you can copy the value of the field and save it for later use.</span></span>  

> [!NOTE]
> <span data-ttu-id="e5f0f-124">Hvis objektene du eksponerer som nettjenester, ikke må være tilgjengelige fra [!INCLUDE [prodshort](includes/prodshort.md)] online, må du merke av for metodene som vises i koden, som `[Scope('OnPrem')]`.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-124">If the objects that you expose as web services must not be accessible from [!INCLUDE [prodshort](includes/prodshort.md)] online, you must mark the methods exposed in the code as `[Scope('OnPrem')]`.</span></span> <span data-ttu-id="e5f0f-125">Se [Scope-attributtet](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute) hvis du vil ha mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-125">For more information, see [Scope Attribute](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).</span></span>

<span data-ttu-id="e5f0f-126">Når du publiserer en webtjeneste, er den tilgjengelig for eksterne parter.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-126">After you publish a web service, it is available to external parties.</span></span> <span data-ttu-id="e5f0f-127">Du kan kontrollere tilgjengeligheten til denne webtjenesten ved hjelp av en leser, eller du kan velge koblingen i feltene **OData URL-adresse** og **SOAP-URL-adresse** på siden **Webtjenester**.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-127">You can verify the availability of that web service by using a browser, or you can choose the link in the **OData URL** and **SOAP URL** fields on the **Web Services** page.</span></span> <span data-ttu-id="e5f0f-128">Følgende fremgangsmåte viser hvordan du kan kontrollere webtjenestens tilgjengelighet for senere bruk.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-128">The following procedure illustrates how you can verify the availability of the web service for later use.</span></span>  

### <a name="to-verify-the-availability-of-a-web-service"></a><span data-ttu-id="e5f0f-129">Slik kontrollerer du tilgjengeligheten til en webtjeneste</span><span class="sxs-lookup"><span data-stu-id="e5f0f-129">To verify the availability of a web service</span></span>  

1. <span data-ttu-id="e5f0f-130">Angi den aktuelle URL-adressen i nettleseren.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-130">In your browser, enter the relevant URL.</span></span> <span data-ttu-id="e5f0f-131">Tabellen nedenfor viser hvilke typer URL-adresser som du kan angi for ulike webtjenestetyper.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-131">The following table illustrates the types of URLs that you can enter for different web service types.</span></span>  

    > [!div class="mx-tdBreakAll"]
    > |<span data-ttu-id="e5f0f-132">Type</span><span class="sxs-lookup"><span data-stu-id="e5f0f-132">Type</span></span>|<span data-ttu-id="e5f0f-133">Syntaks</span><span class="sxs-lookup"><span data-stu-id="e5f0f-133">Syntax</span></span>|<span data-ttu-id="e5f0f-134">Eksempel</span><span class="sxs-lookup"><span data-stu-id="e5f0f-134">Example</span></span>|
    > |----------------|------|-------|
    > |<span data-ttu-id="e5f0f-135">SOAP</span><span class="sxs-lookup"><span data-stu-id="e5f0f-135">SOAP</span></span>|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/` |`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |<span data-ttu-id="e5f0f-136">OData V4</span><span class="sxs-lookup"><span data-stu-id="e5f0f-136">OData V4</span></span>|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*`|`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    <span data-ttu-id="e5f0f-137">Selskapsnavnet skiller mellom store og små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-137">The company name is case-sensitive.</span></span>|

2. <span data-ttu-id="e5f0f-138">Se gjennom informasjone som vises i webleseren.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-138">Review the information that is displayed in the browser.</span></span> <span data-ttu-id="e5f0f-139">Kontroller at du kan se navnet på webtjenesten som du har opprettet.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-139">Verify that you can see the name of the web service that you have created.</span></span>  

<span data-ttu-id="e5f0f-140">Når du åpner en webtjeneste, og du vil skrive data tilbake til [!INCLUDE[d365fin](includes/d365fin_md.md)], må du angi firmanavnet.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-140">When you access a web service, and you want to write data back to [!INCLUDE[d365fin](includes/d365fin_md.md)], you must specify the company name.</span></span> <span data-ttu-id="e5f0f-141">Du kan angi selskapet som en del av URI-en som vist i eksemplene, eller du kan angi selskapet som en del av spørringsparameterne.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-141">You can specify the company as part of the URI as shown in the examples, or you can specify the company as part of the query parameters.</span></span> <span data-ttu-id="e5f0f-142">Følgende URIer peker for eksempel til den samme OData web-tjenesten, og de er begge gyldige URIer.</span><span class="sxs-lookup"><span data-stu-id="e5f0f-142">For example, the following URIs point to the same OData web service and are both valid URIs.</span></span>  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a><span data-ttu-id="e5f0f-143">Se også</span><span class="sxs-lookup"><span data-stu-id="e5f0f-143">See Also</span></span>

[<span data-ttu-id="e5f0f-144">Administrasjon</span><span class="sxs-lookup"><span data-stu-id="e5f0f-144">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="e5f0f-145">Business Central-webtjenester for utviklere</span><span class="sxs-lookup"><span data-stu-id="e5f0f-145">Business Central Web Services for developers</span></span>](/dynamics365/business-central/dev-itpro/webservices/web-services)  
[<span data-ttu-id="e5f0f-146">OData-forespørselsgrenser</span><span class="sxs-lookup"><span data-stu-id="e5f0f-146">OData request limits</span></span>](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#ODataServices)  
