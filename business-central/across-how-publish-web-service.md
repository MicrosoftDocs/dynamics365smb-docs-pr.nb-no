---
title: Vise objekter som webtjenester | Microsoft-dokumentasjon
description: Publiser objekter som webtjenester, slik at de umiddelbart blir tilgjengelige for Business Central-løsningen din.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 05a414d6f12243f55105863b66d9b6e759a29189
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305697"
---
# <a name="publish-a-web-service"></a>Publisere en webtjeneste

Webtjenester er en lett måte å gjøre programfunksjonalitet tilgjengelig for en rekke eksterne systemer og brukere. [!INCLUDE[d365fin](includes/d365fin_md.md)] inneholder en rekke objekter som vises som webtjenester som standard på grunn av integrering med andre Microsoft-tjenester, men du kan også legge til andre webtjenester.  

Du definerer en webtjeneste i [!INCLUDE[d365fin](includes/d365fin_md.md)]-klienten. Du må deretter publisere webtjenesten slik at den er tilgjengelig for serviceforespørsler over nettverket. Brukere kan oppdage webtjenester ved å velge en webleser på en server og be om liste over tilgjengelige tjenester. Når du publiserer en webtjeneste, er den umiddelbart tilgjengelig på nettverket for godkjente brukere. Alle autoriserte brukere har tilgang til metadata for webtjenester, men bare brukere som har tilstrekkelige tillatelser, har tilgang til faktiske data.

## <a name="creating-and-publishing-a-web-service"></a>Opprette og publisere en webtjeneste  
De følgende trinnene forklarer hvordan du oppretter og publiserer en webtjeneste.  

### <a name="to-create-and-publish-a-web-service"></a>Slik oppretter og publiserer du en webtjeneste  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Webtjenester**, og velg deretter den relaterte koblingen.  
2. På siden **Webtjenester** velger du **Ny**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > **Kodeenhet** og **Side** er gyldige typer for SOAP-webtjenester. **Side** og **Spørring** er gyldige typer for OData-webtjenester.  
    > Hvis databasen inneholder flere selskaper, kan du også velge en objekt-ID som er spesifikk for ett av selskapene.  
    > Tjenestenavnet er synlig for brukere av webtjenesten, og brukes som grunnlag for å identifisere og skjelne webtjenester, så du bør velge et meningsfullt navn.

3. Merk avmerkingsboksen i kolonnen **Publisert**.  

Når du publiserer webtjenesten i feltene **OData URL-adresse** og **SOAP-URL-adresse**, kan du se URL-adressene som er generert for webtjenesten. Du kan teste webtjenesten umiddelbart ved å velge koblingene i feltene **OData URL-adresse** og **SOAP-URL-adresse**. Du kan eventuelt kopiere feltets verdi, og lagre den for senere bruk.  

> [!IMPORTANT]
> For codeunits som publiseres som en SOAP-webtjeneste, må metodene som vises i codeunits, være merket som `[External]` i koden.

Når du publiserer en webtjeneste, er den tilgjengelig for eksterne parter. Du kan kontrollere tilgjengeligheten til denne webtjenesten ved hjelp av en leser, eller du kan velge koblingen i feltene **OData URL-adresse** og **SOAP-URL-adresse** på siden **Webtjenester**. Følgende fremgangsmåte viser hvordan du kan kontrollere webtjenestens tilgjengelighet for senere bruk.  

### <a name="to-verify-the-availability-of-a-web-service"></a>Slik kontrollerer du tilgjengeligheten til en webtjeneste  

1. Angi den aktuelle URL-adressen i nettleseren. Tabellen nedenfor viser hvilke typer URL-adresser som du kan angi for ulike webtjenestetyper.  

    > [!div class="mx-tdBreakAll"]
    > |Type|Syntaks|Eksempel|
    > |----------------|------|-------|
    > |SOAP |https://api.businesscentral.dynamics.com/*versjon*/*leier*/WS/*Selskapsnavn*/*enhet*/ |`https://api.businesscentral.dynamics.com/v1.0/a10b3ee6-d9a2-42fe-926f-946e23bb8ddd/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |OData V4|https://api.businesscentral.dynamics.com/*versjon*/*leier*/ODataV4/Selskap('*Selskapsnavn*')/*enhet*|`https://api.businesscentral.dynamics.com/v1.0/a10b3ee6-d9a2-42fe-926f-946e23bb8ddd/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    Selskapsnavnet skiller mellom store og små bokstaver.|

2. Se gjennom informasjone som vises i webleseren. Kontroller at du kan se navnet på webtjenesten som du har opprettet.  

Når du åpner en webtjeneste, og du vil skrive data tilbake til [!INCLUDE[d365fin](includes/d365fin_md.md)], må du angi firmanavnet. Du kan angi selskapet som en del av URI-en som vist i eksemplene, eller du kan angi selskapet som en del av spørringsparameterne. Følgende URIer peker for eksempel til den samme OData web-tjenesten, og de er begge gyldige URIer.  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a>Se også

[Administrasjon](admin-setup-and-administration.md)  
[Business Central-webtjenester for utviklere](/dynamics365/business-central/dev-itpro/webservices/web-services)  
