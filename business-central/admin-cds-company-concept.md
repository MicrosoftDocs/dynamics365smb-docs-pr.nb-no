---
title: Enhetstilordning for selskap og virksomhet | Microsoft Docs
description: Selskaper er både juridiske og forretningsmessige konstruksjoner, og de brukes til å sikre og visualisere forretningsdata.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: CDS, Dataverse, integration, sync
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: c1af1f571170a167d59b20d85010fdd8d70d07cd
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8133995"
---
# <a name="data-ownership-models"></a>Dataeierskapsmodeller


[!INCLUDE[prod_short](includes/cds_long_md.md)] krever at du angir en eier av dataene du lagrer. Hvis du vil ha mer informasjon, kan du se [Tabelltyper](/powerapps/maker/data-platform/types-of-entities) i dokumentasjonen for Power Apps. Når du definerer integreringen mellom [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)], må du velge eierskapet **Bruker eller Team** for poster som synkroniseres. Handlinger som kan utføres på disse postene, kan kontrolleres på et brukernivå. <!--We recommend the Team ownership model because it makes it easier to manage ownership for multiple people.NO LONGER TRUE IN DATAVERSE-->

## <a name="team-ownership"></a>Teameierskap
I [!INCLUDE[prod_short](includes/prod_short.md)] er et selskap en juridisk og forretningsmessig tabell som har metoder for å sikre og visualisere forretningsdata. Brukere arbeider alltid i en bedrifts kontekst. Det nærmeste [!INCLUDE[prod_short](includes/cds_long_md.md)] kommer til dette konseptet, er konserntabellen, som ikke har juridiske eller forretningsmessige konsekvenser.

Ettersom forretningsenheter mangler juridiske og forretningsmessige konsekvenser, kan du ikke gjennomføre en én-til-én-tilordning (1:1) til å synkronisere data mellom et selskap og en forretningsenhet, enten enveis eller toveis. Når du aktiverer synkronisering av et selskap i [!INCLUDE[prod_short](includes/prod_short.md)], skjer følgende i [!INCLUDE[prod_short](includes/cds_long_md.md)] hvis du vil gjøre synkronisering mulig:

* Det opprettes en selskapstabell som tilsvarer selskapstabellen i [!INCLUDE[prod_short](includes/prod_short.md)]. Navnet på selskapet er suffikset med ID for BC-firma. Det kan for eksempel være Cronus Norge AS (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Det opprettes en standard forretningsenhet som har samme navn som selskapet. Det kan for eksempel være Cronus Norge AS (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Det opprettes egne eierteam med samme navn som selskapet, og knytter det til forretningsenheten. Navnet på teamet har prefikset "BCI-". Det kan for eksempel være BCI – Cronus Norge AS (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Poster som opprettes og synkroniseres til [!INCLUDE[prod_short](includes/cds_long_md.md)], blir tilordnet til teamet BCI-eier som er knyttet til forretningsenheten.

> [!NOTE]
> Hvis du gir nytt navn til et selskap i [!INCLUDE[prod_short](includes/prod_short.md)], oppdateres ikke navnene på selskapet, bedriften og teamet vi oppretter automatisk i [!INCLUDE[prod_short](includes/cds_long_md.md)]. Siden bare selskaps-ID-en brukes til integrasjon, påvirker ikke dette synkroniseringen. Hvis du vil at navnene skal samsvare, må du oppdatere selskapet, forretningsenheten og teamet i [!INCLUDE[prod_short](includes/cds_long_md.md)].

Det følgende bildet viser et eksempel på dette dataoppsettet i [!INCLUDE[prod_short](includes/cds_long_md.md)].

![Rotforretningsenheten er øverst, teamene er i midten, og deretter vises firmaene nederst.](media/cds_bu_team_company.png)

I denne konfigurasjonen eies poster som er knyttet til det amerikanske selskapet Cronus, av et team som er knyttet til forretningsenheten for Cronus US i [!INCLUDE[prod_short](includes/cds_long_md.md)]. Brukere som har tilgang til forretningsenheten via en sikkerhetsrolle som er angitt med synlighet på forretningsenhetsnivå i [!INCLUDE[prod_short](includes/cds_long_md.md)], kan nå se de postene. Følgende eksempel viser hvordan du bruker team til å gi tilgang til disse postene.

* Salgssjefrollen er tilordnet til medlemmer av salgsteamet hos Cronus.
* Brukere som har rollen Salgssjef, kan få tilgang til kontoposter for medlemmer av samme konsern.
* Salgsteamet hos Cronus US er knyttet til forretningsenheten for Cronus US som ble nevnt tidligere. Medlemmer av salgsteamet i Cronus US kan se alle forretningsforbindelser som eies av brukeren for Cronus US, noe som ville ha kommet fra selskapstabellen for Cronus US i [!INCLUDE[prod_short](includes/prod_short.md)].

1:1-tilordningen mellom forretningsenhet, selskap og team er imidlertid bare et utgangspunkt, som vist i følgende bilde.

![Sikkerhetsrollen styrer datasynlighet.](media/cds_bu_team_company_2.png)

I dette eksemplet opprettes det en ny EUR-rotforretningsenhet (Europa) i [!INCLUDE[prod_short](includes/cds_long_md.md)] som den overordnede enheten for både Cronus DE (Tyskland) og Cronus ES (Spania). EUR-forretningsenheten er ikke knyttet til synkronisering. Den kan imidlertid gi medlemmene av EUR-salgsteamet tilgang til å kontodata både i Cronus DE og Cronus ES ved å sette datasynligheten til **Overordnet/Underordnet forretningsenhet** for den tilknyttede sikkerhetsrollen i [!INCLUDE[prod_short](includes/cds_long_md.md)].

Synkronisering bestemmer hvilket team som skal eie poster. Dette styres av feltet **Standard eiende team** i raden BCI. Når en post av typen BCI aktiveres for synkronisering, opprettes automatisk den tilknyttede forretningsenheten og eierteamet (hvis det ikke allerede finnes), og det angis en verdi i feltet **Standard eiende team**. Når synkronisering er aktivert for en tabell, kan administratorer endre det eiende teamet, men et team må alltid være tilordnet.

> [!NOTE]
> Poster blir skrivebeskyttet etter at et selskap er lagt til og lagret, så sørg for at du velger riktig selskap.

## <a name="choosing-a-different-business-unit"></a>Velge en annen forretningsenhet
Du kan endre valgt forretningsenhet hvis du bruker Team-eierskapsmodellen. Hvis du bruker Person-eierskapsmodellen, blir standard forretningsenhet alltid valgt. 

Hvis du velger en annen forretningsenhet, for eksempel et som du opprettet tidligere i [!INCLUDE[prod_short](includes/cds_long_md.md)], beholder den det opprinnelige navnet. Det vil si at den ikke vil få et suffiks med firma-ID-en. Det opprettes et team som bruker navnekonvensjonen.

Når du endrer en forretningsenhet, kan du bare velge de konsernene som er ett nivå under rotforretningsenheten.

## <a name="person-ownership"></a>Personeierskap
Hvis du velger personeierskapsmodellen, må du angi hver selger som skal eie nye poster. Forretningsenheten og teamet opprettes som beskrevet i delen [Teameierskap](admin-cds-company-concept.md#team-ownership).

Standard forretningsenhet brukes når Person-eierskapsmodellen er valgt, og du kan ikke velge en annen forretningsenhet. Teamet som er knyttet til standard forretningsenhet, vil eie poster for vanlige tabeller, for eksempel produkttabellen, som ikke er knyttet til bestemte selgere.

Når du kobler selgere i [!INCLUDE[prod_short](includes/prod_short.md)] med brukere i [!INCLUDE[prod_short](includes/cds_long_md.md)], vil [!INCLUDE[prod_short](includes/prod_short.md)] legge til brukeren i standardgruppen i [!INCLUDE[prod_short](includes/cds_long_md.md)]. Du kan bekrefte at brukerne er lagt til ved å se på kolonnen **Standard teammedlem** på **Brukere - Common Data Service**-siden. Hvis brukeren ikke er lagt til, kan du legge dem til manuelt ved å bruke handlingen **Legg til koblede brukere i Team**. Hvis du vil ha mer informasjon, kan du se [Synkronisere data i Business Central med Dataverse](admin-synchronizing-business-central-and-sales.md).

## <a name="see-also"></a>Se også
[Om [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-common-data-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]