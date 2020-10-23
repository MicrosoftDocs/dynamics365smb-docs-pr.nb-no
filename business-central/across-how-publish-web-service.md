---
title: Vise objekter som webtjenester
description: Publiser objekter som webtjenester, slik at de umiddelbart blir tilgjengelige for Business Central-løsningen din.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 10/08/2020
ms.author: edupont
ms.openlocfilehash: 658816cfb65580404bc8ef10472a5b62c6815c9e
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989491"
---
# <a name="publish-a-web-service"></a>Publisere en webtjeneste

Webtjenester er en lett måte å gjøre programfunksjonalitet tilgjengelig for forskjellige eksterne systemer og brukere. Som standard viser [!INCLUDE[d365fin](includes/d365fin_md.md)] flere objekter som webtjenester for bedre integrasjon med andre Microsoft-tjenester. Du kan legge til andre webtjenester etter behov.  

Sett opp en webtjeneste i [!INCLUDE[d365fin](includes/d365fin_md.md)], og publiser deretter webtjenesten slik at den er tilgjengelig for godkjente brukere. Alle autoriserte brukere har tilgang til metadata for webtjenester, men bare brukere som har tilstrekkelige tillatelser, har tilgang til faktiske data.  

## <a name="creating-and-publishing-a-web-service"></a>Opprette og publisere en webtjeneste

De følgende trinnene forklarer hvordan du oppretter og publiserer en webtjeneste.  

### <a name="to-create-and-publish-a-web-service"></a>Slik oppretter og publiserer du en webtjeneste  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Webtjenester**, og velg deretter den relaterte koblingen.  
2. På siden **Webtjenester** velger du **Ny**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > **Kodeenhet** og **Side** er gyldige typer for SOAP-webtjenester. **Side** og **Spørring** er gyldige typer for OData-webtjenester. Fra og med versjon 16.3 er **Codeunit** også en gyldig type for OData v4-webtjenester, men ingen URL-adresse vises i brukergrensesnittet. Hvis databasen inneholder flere selskaper, kan du også velge en objekt-ID som er spesifikk for ett av selskapene.  
    > Tjenestenavnet er synlig for brukere av webtjenesten, og brukes som grunnlag for å identifisere og skjelne webtjenester, så du bør velge et meningsfullt navn.

3. Merk avmerkingsboksen i kolonnen **Publisert**.  

Når du publiserer webtjenesten, viser feltene **OData-URL-adresse** og **SOAP-URL-adresse** de nye URL-adressene. For codeunits som vises som OData v4-ubundne handlinger, vises imidlertid ikke URL-feltene.  

Du kan teste webtjenesten umiddelbart ved å velge koblingene i feltene **OData URL-adresse** og **SOAP-URL-adresse**. Kopier eventuelt feltets verdi, og lagre den for senere bruk. Hvis du vil teste codeunits som vises som OData v4-ubundne handlinger, følger du instruksjonene i delen [Verifisere tilgjengelighet for webtjeneste](/dynamics365/business-central/dev-itpro/developer/devenv-creating-and-interacting-with-odatav4-unbound-action#verifying-web-service-availability) i innholdet for utviklere.

> [!NOTE]
> Hvis objektene du eksponerer som nettjenester, ikke må være tilgjengelige fra [!INCLUDE[prodshort](includes/prodshort.md)] online, må du merke av for metodene som vises i koden, som `[Scope('OnPrem')]`. Se [Scope-attributtet](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute) hvis du vil ha mer informasjon.

Når du publiserer en webtjeneste, er den tilgjengelig for eksterne parter. Du kan kontrollere tilgjengeligheten til denne webtjenesten ved hjelp av en leser, eller velge koblingen i feltene **OData URL-adresse** og **SOAP-URL-adresse** på siden **Webtjenester**. Følgende fremgangsmåte viser hvordan du kan kontrollere webtjenestens tilgjengelighet for senere bruk.  

### <a name="to-verify-the-availability-of-a-web-service"></a>Slik kontrollerer du tilgjengeligheten til en webtjeneste  

1. Angi den aktuelle URL-adressen i nettleseren. Tabellen nedenfor viser hvilke typer URL-adresser som du kan angi for ulike webtjenestetyper.  

    > [!div class="mx-tdBreakAll"]
    > |Type|Syntaks|Eksempel|
    > |----------------|------|-------|
    > |SOAP|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/` |`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |OData V4|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*`|`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    Selskapsnavnet skiller mellom store og små bokstaver.|

2. Se gjennom informasjone som vises i webleseren. Kontroller at du kan se navnet på webtjenesten som du har opprettet.  

Når du åpner en webtjeneste, og du vil skrive data tilbake til [!INCLUDE[d365fin](includes/d365fin_md.md)], må du angi firmanavnet. Du kan angi selskapet som en del av URI-en som vist i eksemplene, eller angi selskapet som en del av spørringsparameterne. Følgende URIer peker for eksempel til den samme OData web-tjenesten, og de er begge gyldige URIer.  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a>Se også

[Administrasjon](admin-setup-and-administration.md)  
[Business Central-webtjenester for utviklere](/dynamics365/business-central/dev-itpro/webservices/web-services)  
[OData-forespørselsgrenser](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#ODataServices)  
