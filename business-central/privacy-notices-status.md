---
title: Status for personvernerklæringer i Business Central
description: En oversikt over siden Status for personvernerklæringer i Business Central
author: brentholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: null
ms.search.form: 1565
audience: null
ms.author: bholtorf
ms.date: 07/21/2022
---

# Status for personvernerklæringer i [!INCLUDE[prod_long](includes/prod_long.md)]

Denne artikkelen drøfter hva en personvernerklæring er, og forklarer formålet med siden **Status for personvernerklæringer** i [!INCLUDE[prod_short](includes/prod_short.md)]. Du vil også lære hvordan administratorer kan bruke denne siden.

## Personvernerklæring

En personvernerklæring angir datainnsamlingen, databehandlingen og datapersonvernerklæringene fulgt av organisasjonens databehandler. Det er et dokument som beskriver hvilke data som samles inn, og hvordan brukerens data behandles, hvordan de lagres og hvem som skal kontaktes hvis en bruker ønsker å stille et spørsmål om dataene sine. 

## Siden Status for personvernerklæringer

Hvis brukerne vil integrere dataene med Microsoft Exchange, Microsoft OneDrive og Microsoft Teams i [!INCLUDE[prod_short](includes/prod_short.md)], må de godta personvernerklæringen for hver enhet. Eller en administrator kan godkjenne personvernerklæringene på deres vegne. Administratorer kan se statusen for personvernerklæringer på siden **Status for personvernerklæringer**. Du kan finne siden **Status for personvernerklæringer** i [!INCLUDE[prod_short](includes/prod_short.md)] ved å skrive inn navnet på siden i søkefeltet.  

På denne siden finner du en tabell med godkjenningsalternativer for alle tjenestene nevnt ovenfor. 

| Kolonne | Description |
| ----------- | ----------- | 
| **Navn på integrering** | Navnet på tjenesten som Microsoft OneDrive. |
| **Godta for alle** | En administrator godkjenner personvernerklæringen for alle brukere. |
| **Ikke godta for alle** | En administrator godkjenner ikke personvernerklæringen for alle brukere. |
| **La brukeren bestemme** | Brukerne bestemmer seg for å godkjenne personvernerklæringen for tjenesten eller ikke. |

> [!NOTE]
> Du kan bare se statusen for personvernerklæringer på hovedsiden **Status for personvernerklæringer**. Hvis du vil redigere svarene, går du til **Rediger listen** på handlingslinjen på siden der alternativene nå er uthevet, og ikke nedtonet.

## Godkjenninger av personvernerklæring

Administratorer kan se individuelle godkjenninger og administrere dem på undersiden **Godkjenninger for personvernerklæring**. Gå til *handlingslinjen* på siden **Handlinger for personvernerklæringer**, under *Handlinger*, for å finne alternativet *Vis individuelle godkjenninger*. Dette alternativet går til siden **Godkjenninger for personvernerklæring**.<br>

På denne siden finner du en tabell med godkjenningsalternativer. 

| Kolonne | Description |
| ----------- | ----------- | 
| **Navn på integrering** | Navnet på tjenesten som Microsoft OneDrive. |
| **Brukernavn** | Brukeren som innehar denne godkjenningen. Hvis *organisasjonen* er skrevet i brukernavnkolonnen, tilhører godkjenningen hele organisasjonen. 
| **Godta** | Brukeren godkjenner personvernerklæringen. |
| **Ikke godta** | Brukeren godkjenner ikke personvernerklæringen. |
| **Brukernavn for godkjenner** | Den som godkjenner personvernerklæringen. |

## Se også

[Samsvarsoversikt  ](/dynamics365/business-central/compliance/compliance-overview)  
[Svar på forespørsler om personopplysninger  ](/dynamics365/business-central/admin-responding-to-requests-about-personal-data)  
[Personvernerklæring og vilkår for bruk ](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-checklist-i-privacypolicy-termsofuse)  
[Dataoppbevaringspolicyer](/dynamics365-release-plan/2020wave2/smb/dynamics365-business-central/define-retention-policies) 
