---
title: Vise objekter som webtjenester | Microsoft-dokumentasjon
description: "Publiserer [!INCLUDE[d365fin](includes/d365fin_md.MD)]-objekter som webtjenester, de er tilgjengelig på nettverket umiddelbart."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 278515fc479a72957fb52dad71ce2f98d354ee32
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-publish-a-web-service"></a><span data-ttu-id="5281b-103">Publisere en webtjeneste</span><span class="sxs-lookup"><span data-stu-id="5281b-103">How to: Publish a Web Service</span></span>
<span data-ttu-id="5281b-104">Webtjenester er en lett måte å gjøre programfunksjonalitet tilgjengelig for en rekke eksterne systemer og brukere.</span><span class="sxs-lookup"><span data-stu-id="5281b-104">Web services are a lightweight way to make application functionality available to a variety of external systems and users.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="5281b-105"> inneholder en rekke objekter som vises som webtjenester som standard på grunn av integrering med andre Microsoft-tjenester, men du kan også legge til andre webtjenester.</span><span class="sxs-lookup"><span data-stu-id="5281b-105"> includes an number of objects that are exposed as web services by default due to integration with other Microsoft services, but you can also add other web services.</span></span>  

<span data-ttu-id="5281b-106">Du kan definere en webtjeneste i Windows-klienten eller i webklienten.</span><span class="sxs-lookup"><span data-stu-id="5281b-106">You can set up a web service in the Windows client or in the Web client.</span></span> <span data-ttu-id="5281b-107">Du må deretter publisere webtjenesten slik at den er tilgjengelig for serviceforespørsler over nettverket.</span><span class="sxs-lookup"><span data-stu-id="5281b-107">You must then publish the web service so that it is available to service requests over the network.</span></span> <span data-ttu-id="5281b-108">Brukere kan oppdage webtjenester ved å velge en webleser på en server og be om liste over tilgjengelige tjenester.</span><span class="sxs-lookup"><span data-stu-id="5281b-108">Users can discover web services by pointing a browser at the server location and requesting a list of available services.</span></span> <span data-ttu-id="5281b-109">Når du publiserer en webtjeneste, er den umiddelbart tilgjengelig på nettverket for godkjente brukere.</span><span class="sxs-lookup"><span data-stu-id="5281b-109">When you publish a web service, it is immediately available over the network for authenticated users.</span></span> <span data-ttu-id="5281b-110">Alle autoriserte brukere har tilgang til metadata for webtjenester, men bare brukere som har tilstrekkelige tillatelser, har tilgang til faktiske data.</span><span class="sxs-lookup"><span data-stu-id="5281b-110">All authorized users can access metadata for web services, but only users who have sufficient permissions can access actual data.</span></span>

## <a name="creating-and-publishing-a-web-service"></a><span data-ttu-id="5281b-111">Opprette og publisere en webtjeneste</span><span class="sxs-lookup"><span data-stu-id="5281b-111">Creating and Publishing a Web Service</span></span>  
 <span data-ttu-id="5281b-112">De følgende trinnene forklarer hvordan du oppretter og publiserer en webtjeneste.</span><span class="sxs-lookup"><span data-stu-id="5281b-112">The following steps explain how to create and publish a web service.</span></span>  

#### <a name="to-create-and-publish-a-web-service"></a><span data-ttu-id="5281b-113">Slik oppretter og publiserer du en webtjeneste</span><span class="sxs-lookup"><span data-stu-id="5281b-113">To create and publish a web service</span></span>  

1.  <span data-ttu-id="5281b-114">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Webtjenester**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="5281b-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Web Services**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="5281b-115">På siden **Webtjenester** velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5281b-115">In the **Web Services** page, choose **New**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    >  <span data-ttu-id="5281b-116">**Kodeenhet** og **Side** er gyldige typer for SOAP-webtjenester.</span><span class="sxs-lookup"><span data-stu-id="5281b-116">**Codeunit** and **Page** are valid types for SOAP web services.</span></span> <span data-ttu-id="5281b-117">**Side** og **Spørring** er gyldige typer for OData-webtjenester.</span><span class="sxs-lookup"><span data-stu-id="5281b-117">**Page** and **Query** are valid types for OData web services.</span></span>  
    <span data-ttu-id="5281b-118">Hvis databasen inneholder flere selskaper, kan du også velge en objekt-ID som er spesifikk for ett av selskapene.</span><span class="sxs-lookup"><span data-stu-id="5281b-118">Also, if the database contains multiple companies, you can choose an object ID that is specific to one of the companies.</span></span>  
    <span data-ttu-id="5281b-119">Tjenestenavnet er synlig for brukere av webtjenesten, og brukes som grunnlag for å identifisere og skjelne webtjenester, så du bør velge et meningsfullt navn.</span><span class="sxs-lookup"><span data-stu-id="5281b-119">Finally, the service name is visible to consumers of your web service and is the basis for identifying and distinguishing web services, so you should make the name meaningful.</span></span>

3.  <span data-ttu-id="5281b-120">Merk avmerkingsboksen i kolonnen **Publisert**.</span><span class="sxs-lookup"><span data-stu-id="5281b-120">Select the check box in the **Published** column.</span></span>  

     <span data-ttu-id="5281b-121">Når du publiserer webtjenesten i feltene **OData URL-adresse** og **SOAP-URL-adresse**, kan du se URL-adressene som er generert for webtjenesten.</span><span class="sxs-lookup"><span data-stu-id="5281b-121">When you publish the web service, in the **OData URL** and **SOAP URL** fields, you can see the URLs that are generated for the web service.</span></span> <span data-ttu-id="5281b-122">Du kan teste webtjenesten umiddelbart ved å velge koblingene i feltene **OData URL-adresse** og **SOAP-URL-adresse**.</span><span class="sxs-lookup"><span data-stu-id="5281b-122">You can test the web service immediately by choosing the links in the **OData URL** and **SOAP URL** fields.</span></span> <span data-ttu-id="5281b-123">Du kan eventuelt kopiere feltets verdi, og lagre den for senere bruk.</span><span class="sxs-lookup"><span data-stu-id="5281b-123">Optionally, you can copy the value of the field and save it for later use.</span></span>  

<span data-ttu-id="5281b-124">Når du publiserer en webtjeneste, er den tilgjengelig for eksterne parter.</span><span class="sxs-lookup"><span data-stu-id="5281b-124">After you publish a web service, it is available to external parties.</span></span> <span data-ttu-id="5281b-125">Du kan kontrollere tilgjengeligheten til denne webtjenesten ved hjelp av en leser, eller du kan velge koblingen i feltene **OData URL-adresse** og **SOAP-URL-adresse** i vinduet **Webtjenester**.</span><span class="sxs-lookup"><span data-stu-id="5281b-125">You can verify the availability of that web service by using a browser, or you can choose the link in the **OData URL** and **SOAP URL** fields in the **Web Services** window.</span></span> <span data-ttu-id="5281b-126">Følgende fremgangsmåte viser hvordan du kan kontrollere webtjenestens tilgjengelighet for senere bruk.</span><span class="sxs-lookup"><span data-stu-id="5281b-126">The following procedure illustrates how you can verify the availability of the web service for later use.</span></span>  

#### <a name="to-verify-the-availability-of-a-web-service"></a><span data-ttu-id="5281b-127">Slik kontrollerer du tilgjengeligheten til en webtjeneste</span><span class="sxs-lookup"><span data-stu-id="5281b-127">To verify the availability of a web service</span></span>  

1.  <span data-ttu-id="5281b-128">Angi den aktuelle URL-adressen i nettleseren.</span><span class="sxs-lookup"><span data-stu-id="5281b-128">In your browser, enter the relevant URL.</span></span> <span data-ttu-id="5281b-129">Tabellen nedenfor viser hvilke typer URL-adresser som du kan angi.</span><span class="sxs-lookup"><span data-stu-id="5281b-129">The following table illustrates the types of URLs that you can enter.</span></span> <span data-ttu-id="5281b-130">Bruk følgende format for din URI for SOAP-webtjenester.</span><span class="sxs-lookup"><span data-stu-id="5281b-130">For SOAP web services, use the following format for your URI.</span></span>  

    <table>
    <tr>
    <th><span data-ttu-id="5281b-131">Webtjenestetype</span><span class="sxs-lookup"><span data-stu-id="5281b-131">Web service type</span></span></th>
    <th><span data-ttu-id="5281b-132">Syntaks</span><span class="sxs-lookup"><span data-stu-id="5281b-132">Syntax</span></span></th>
    <th><span data-ttu-id="5281b-133">Eksempel</span><span class="sxs-lookup"><span data-stu-id="5281b-133">Example</span></span></th>
    </tr>
    <tr>
    <td><span data-ttu-id="5281b-134">SOAP</span><span class="sxs-lookup"><span data-stu-id="5281b-134">SOAP</span></span></td>
    <td><span data-ttu-id="5281b-135">https://*Server*:*SOAPWebServicePort*/*ServerInstance*/WS/*CompanyName*/salesDocuments/</span><span class="sxs-lookup"><span data-stu-id="5281b-135">https://*Server*:*SOAPWebServicePort*/*ServerInstance*/WS/*CompanyName*/salesDocuments/</span></span></td>
    <td><span data-ttu-id="5281b-136">https://mycompany.financials.dynamics.com:7047/MS/WS/MyCompany/Page/salesDocuments?tenant=mycompany.financials.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="5281b-136">https://mycompany.financials.dynamics.com:7047/MS/WS/MyCompany/Page/salesDocuments?tenant=mycompany.financials.dynamics.com</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="5281b-137">OData</span><span class="sxs-lookup"><span data-stu-id="5281b-137">OData</span></span></td>
    <td><span data-ttu-id="5281b-138">https://*Server*:*ODataWebServicePort*/*ServerInstance*/OData/Company('*CompanyName*')</span><span class="sxs-lookup"><span data-stu-id="5281b-138">https://*Server*:*ODataWebServicePort*/*ServerInstance*/OData/Company('*CompanyName*')</span></span></td>
    <td><span data-ttu-id="5281b-139">https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="5281b-139">https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com</span></span>

         The company name is case-sensitive.</td>
    </tr>
    </table>

2.  <span data-ttu-id="5281b-140">Se gjennom informasjone som vises i webleseren.</span><span class="sxs-lookup"><span data-stu-id="5281b-140">Review the information that is displayed in the browser.</span></span> <span data-ttu-id="5281b-141">Kontroller at du kan se navnet på webtjenesten som du har opprettet.</span><span class="sxs-lookup"><span data-stu-id="5281b-141">Verify that you can see the name of the web service that you have created.</span></span>  

 <span data-ttu-id="5281b-142">Når du åpner en webtjeneste, og du vil skrive data tilbake til [!INCLUDE[d365fin](includes/d365fin_md.md)], må du angi firmanavnet.</span><span class="sxs-lookup"><span data-stu-id="5281b-142">When you access a web service, and you want to write data back to [!INCLUDE[d365fin](includes/d365fin_md.md)], you must specify the company name.</span></span> <span data-ttu-id="5281b-143">Du kan angi selskapet som en del av URI-en som vist i eksemplene, eller du kan angi selskapet som en del av spørringsparameterne.</span><span class="sxs-lookup"><span data-stu-id="5281b-143">You can specify the company as part of the URI as shown in the examples, or you can specify the company as part of the query parameters.</span></span> <span data-ttu-id="5281b-144">Følgende URIer peker for eksempel til den samme OData web-tjenesten, og de er begge gyldige URIer.</span><span class="sxs-lookup"><span data-stu-id="5281b-144">For example, the following URIs point to the same OData web service and are both valid URIs.</span></span>  

```  
https://localhost:7048/server/OData/Company('CRONUS International Ltd.')/Customer  
```  

```  
https://localhost:7048/server/OData/Customer?company='CRONUS International Ltd.'  
```  

## <a name="see-also"></a><span data-ttu-id="5281b-145">Se også</span><span class="sxs-lookup"><span data-stu-id="5281b-145">See Also</span></span>  
[<span data-ttu-id="5281b-146">Oppsett og administrasjon i Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="5281b-146">Setup and Administration in Dynamics 365 for Financials</span></span>](admin-setup-and-administration.md)  

