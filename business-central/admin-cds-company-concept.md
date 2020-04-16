---
title: Enhetstilordning for selskap og virksomhet | Microsoft Docs
description: Selskaper er både juridiske og forretningsmessige konstruksjoner, og de brukes til å sikre og visualisere forretningsdata.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: CDS, Common Data Service, integration, sync
ms.date: 01/17/2020
ms.author: bholtorf
ms.openlocfilehash: ccd371711a53c598279fcc981c5581be5ee9bdaf
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196883"
---
# <a name="data-ownership-models"></a>Dataeierskapsmodeller
[!INCLUDE[d365fin](includes/cds_long_md.md)] krever at du angir en eier av dataene du lagrer. Hvis du vil ha mer informasjon, kan du se [Enhetseierskap](https://docs.microsoft.com/powerapps/maker/common-data-service/types-of-entities#entity-ownership) i dokumentasjonen for Power Apps. Når du definerer integreringen mellom [!INCLUDE[d365fin](includes/cds_long_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)], må du velge én av to eierskapsmodeller for poster som synkroniseres:

* Team 
* Person (bruker)

Handlinger som kan utføres på disse postene, kan kontrolleres på et brukernivå. Hvis du vil ha mer informasjon, kan du se [Enheter for bruker og team](https://docs.microsoft.com/powerapps/developer/common-data-service/user-team-entities). Teameierskapsmodellen anbefales fordi den gjør det enklere å administrere eierskap for flere personer.

## <a name="team-ownership"></a>Teameierskap
I [!INCLUDE[d365fin](includes/d365fin_md.md)] er et selskap en juridisk og forretningsmessig enhet som har metoder for å sikre og visualisere forretningsdata. Brukere arbeider alltid i en bedrifts kontekst. Det nærmeste [!INCLUDE[d365fin](includes/cds_long_md.md)] kommer til dette konseptet, er forretningsenheten, som ikke har juridiske eller forretningsmessige konsekvenser.

Ettersom forretningsenheter mangler juridiske og forretningsmessige konsekvenser, kan du ikke gjennomføre en én-til-én-tilordning (1:1) til å synkronisere data mellom et selskap og en forretningsenhet, enten enveis eller toveis. Når du aktiverer synkronisering av et selskap i [!INCLUDE[d365fin](includes/d365fin_md.md)], skjer følgende i [!INCLUDE[d365fin](includes/cds_long_md.md)] hvis du vil gjøre synkronisering mulig:

* Det opprettes en firmaenhet som tilsvarer firmaenheten i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Navnet på selskapet er suffikset med ID for BC-firma. Det kan for eksempel være Cronus Norge AS (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Det opprettes en standard forretningsenhet som har samme navn som selskapet. Det kan for eksempel være Cronus Norge AS (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Det opprettes egne eierteam med samme navn som selskapet, og knytter det til forretningsenheten. Navnet på teamet har prefikset "BCI-". Det kan for eksempel være BCI – Cronus Norge AS (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Poster som opprettes og synkroniseres til [!INCLUDE[d365fin](includes/cds_long_md.md)], blir tilordnet til teamet BCI-eier som er knyttet til forretningsenheten.

Det følgende bildet viser et eksempel på dette dataoppsettet i [!INCLUDE[d365fin](includes/cds_long_md.md)].

![Rotforretningsenheten er øverst, teamene er i midten, og deretter vises firmaene nederst.](media/cds_bu_team_company.png)

I denne konfigurasjonen eies poster som er knyttet til det amerikanske selskapet Cronus, av et team som er knyttet til <ID>-forretningsenheten for Cronus US i [!INCLUDE[d365fin](includes/cds_long_md.md)]. Brukere som har tilgang til forretningsenheten via en sikkerhetsrolle som er angitt med synlighet på forretningsenhetsnivå i [!INCLUDE[d365fin](includes/cds_long_md.md)], kan nå se de postene. Følgende eksempel viser hvordan du bruker team til å gi tilgang til disse postene.

* Salgssjefrollen er tilordnet til medlemmer av salgsteamet hos Cronus.
* Brukere som har rollen Salgssjef, kan få tilgang til kontoposter for medlemmer av samme konsern.
* Salgsteamet hos Cronus US er knyttet til forretningsenheten for Cronus US som ble nevnt tidligere. Medlemmer av salgsteamet i Cronus US kan se alle forretningsforbindelser som eies av <ID>-brukeren for Cronus US, noe som ville ha kommet fra selskapsenheten for Cronus US i [!INCLUDE[d365fin](includes/d365fin_md.md)].

1:1-tilordningen mellom forretningsenhet, selskap og team er imidlertid bare et utgangspunkt, som vist i følgende bilde.

![Sikkerhetsrollen styrer datasynlighet.](media/cds_bu_team_company_2.png)

I dette eksemplet opprettes det en ny EUR-rotforretningsenhet (Europa) i [!INCLUDE[d365fin](includes/cds_long_md.md)] som den overordnede enheten for både Cronus DE (Tyskland) og Cronus ES (Spania). EUR-forretningsenheten er ikke knyttet til synkronisering. Den kan imidlertid gi medlemmene av EUR-salgsteamet tilgang til å kontodata både i Cronus DE og Cronus ES ved å sette datasynligheten til **Overordnet/Underordnet forretningsenhet** for den tilknyttede sikkerhetsrollen i [!INCLUDE[d365fin](includes/cds_long_md.md)].

Synkronisering bestemmer hvilket team som skal eie poster. Dette styres av feltet **Standard eiende team** i posten BCI – <ID>. Når en post av typen BCI – <ID> aktiveres for synkronisering, opprettes automatisk den tilknyttede forretningsenheten og eierteamet (hvis det ikke allerede finnes), og det angis en verdi i feltet **Standard eiende team**. Når synkronisering er aktivert for en enhet, kan administratorer endre det eiende teamet, men et team må alltid være tilordnet.

> [!NOTE]
> Poster blir skrivebeskyttet etter at et selskap er lagt til og lagret, så sørg for at du velger riktig selskap.

### <a name="choosing-a-different-business-unit"></a>Velge en annen forretningsenhet
Du kan endre valget av forretningsenhet. Hvis du velger en annen enhet, for eksempel en som du opprettet tidligere i CDS, beholder den det opprinnelige navnet. Det vil si at den ikke vil få et suffiks med firma-ID-en. Det opprettes et team som bruker navnekonvensjonen.

## <a name="person-ownership"></a>Personeierskap
Hvis du velger personeierskapsmodellen, må du angi hver selger som skal eie nye poster. Forretningsenheten og teamet opprettes som beskrevet i forrige del.  

## <a name="see-also"></a>Se også
[Om [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-common-data-service.md)