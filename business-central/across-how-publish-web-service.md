---
title: Vise objekter som webtjenester | Microsoft-dokumentasjon
description: "Publiser objekter som webtjenester slik at de blir umiddelbart tilgjengelige på nettverket."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: bb9623c00aa038b387179d46e6eb8a869552569e
ms.contentlocale: nb-no
ms.lasthandoff: 11/26/2018

---
# <a name="publish-a-web-service"></a>Publisere en webtjeneste

Webtjenester er en lett måte å gjøre programfunksjonalitet tilgjengelig for en rekke eksterne systemer og brukere. [!INCLUDE[d365fin](includes/d365fin_md.md)] inneholder en rekke objekter som vises som webtjenester som standard på grunn av integrering med andre Microsoft-tjenester, men du kan også legge til andre webtjenester.  

Du kan definere en webtjeneste i Windows-klienten eller i webklienten. Du må deretter publisere webtjenesten slik at den er tilgjengelig for serviceforespørsler over nettverket. Brukere kan oppdage webtjenester ved å velge en webleser på en server og be om liste over tilgjengelige tjenester. Når du publiserer en webtjeneste, er den umiddelbart tilgjengelig på nettverket for godkjente brukere. Alle autoriserte brukere har tilgang til metadata for webtjenester, men bare brukere som har tilstrekkelige tillatelser, har tilgang til faktiske data.

## <a name="creating-and-publishing-a-web-service"></a>Opprette og publisere en webtjeneste  
De følgende trinnene forklarer hvordan du oppretter og publiserer en webtjeneste.  

### <a name="to-create-and-publish-a-web-service"></a>Slik oppretter og publiserer du en webtjeneste  

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Webtjenester**, og velg deretter den relaterte koblingen.  
2.  På siden **Webtjenester** velger du **Ny**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    >  **Kodeenhet** og **Side** er gyldige typer for SOAP-webtjenester. **Side** og **Spørring** er gyldige typer for OData-webtjenester.  
    Hvis databasen inneholder flere selskaper, kan du også velge en objekt-ID som er spesifikk for ett av selskapene.  
    Tjenestenavnet er synlig for brukere av webtjenesten, og brukes som grunnlag for å identifisere og skjelne webtjenester, så du bør velge et meningsfullt navn.

3.  Merk avmerkingsboksen i kolonnen **Publisert**.  

Når du publiserer webtjenesten i feltene **OData URL-adresse** og **SOAP-URL-adresse**, kan du se URL-adressene som er generert for webtjenesten. Du kan teste webtjenesten umiddelbart ved å velge koblingene i feltene **OData URL-adresse** og **SOAP-URL-adresse**. Du kan eventuelt kopiere feltets verdi, og lagre den for senere bruk.  

Når du publiserer en webtjeneste, er den tilgjengelig for eksterne parter. Du kan kontrollere tilgjengeligheten til denne webtjenesten ved hjelp av en leser, eller du kan velge koblingen i feltene **OData URL-adresse** og **SOAP-URL-adresse** på siden **Webtjenester**. Følgende fremgangsmåte viser hvordan du kan kontrollere webtjenestens tilgjengelighet for senere bruk.  

### <a name="to-verify-the-availability-of-a-web-service"></a>Slik kontrollerer du tilgjengeligheten til en webtjeneste  

1.  Angi den aktuelle URL-adressen i nettleseren. Tabellen nedenfor viser hvilke typer URL-adresser som du kan angi for ulike webtjenestetyper.  
> [!div class="mx-tdBreakAll"]
> |Type|Syntaks|Eksempel|
> |----------------|------|-------|
> |SOAP |https://*Server*:*SOAPWebServicePort*/*ServerInstance*/WS/*CompanyName*/salesDocuments/ |https://mycompany.financials.dynamics.com:7047/MS/WS/MyCompany/Page/salesDocuments?tenant=mycompany.financials.dynamics.com |
> |OData |https://*Server*:*ODataWebServicePort*/*ServerInstance*/OData/Company('*CompanyName*')|[https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com](https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com) <br />    Selskapsnavnet skiller mellom store og små bokstaver.|

2.  Se gjennom informasjone som vises i webleseren. Kontroller at du kan se navnet på webtjenesten som du har opprettet.  

Når du åpner en webtjeneste, og du vil skrive data tilbake til [!INCLUDE[d365fin](includes/d365fin_md.md)], må du angi firmanavnet. Du kan angi selskapet som en del av URI-en som vist i eksemplene, eller du kan angi selskapet som en del av spørringsparameterne. Følgende URIer peker for eksempel til den samme OData web-tjenesten, og de er begge gyldige URIer.  

```  
https://localhost:7048/server/OData/Company('CRONUS International Ltd.')/Customer  
```  

```  
https://localhost:7048/server/OData/Customer?company='CRONUS International Ltd.'  
```  

## <a name="see-also"></a>Se også  
[Administrasjon](admin-setup-and-administration.md)  

