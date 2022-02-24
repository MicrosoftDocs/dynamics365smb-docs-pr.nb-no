---
title: Tilordne tabellene og feltene som skal synkroniseres | Microsoft Docs
description: Lær hvordan du kan tilordne tabeller og felt for å synkronisere data mellom Business Central og Common Data Service.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 04/20/2020
ms.author: bholtorf
ms.openlocfilehash: 0b814c18c328ea0647e38b6a837577b277ca4e63
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/01/2020
ms.locfileid: "3527938"
---
# <a name="mapping-the-tables-and-fields-to-synchronize"></a>Tilordne tabellene og feltene som skal synkroniseres
Det grunnleggende for å synkronisere data i [!INCLUDE[d365fin](includes/d365fin_md.md)] med data i [!INCLUDE[d365fin](includes/cds_long_md.md)] er å tilordne tabellene og feltene som inneholder dataene, til hverandre. Tilordning skjer gjennom integrasjonstabeller. 

## <a name="mapping-integration-tables"></a>Tilordne integrasjonstabeller
En integrasjonstabell er en tabell i [!INCLUDE[d365fin](includes/d365fin_md.md)]-databasen som representerer en enhet, for eksempel en konto, i [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Integrasjonstabeller inneholder felt som samsvarer med feltene i tabellen for [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-enheten. Integrasjonstabellen Konto kobler for eksempel til Kontoer-enheten i [!INCLUDE[cds_short_md](includes/cds_long_md.md)]. Det må være en integrasjonstabelltilordning for hver enhet i [!INCLUDE[cds_short_md](includes/cds_short_md.md)] som du vil synkronisere med data i [!INCLUDE[prodshort](includes/prodshort.md)].

Når du oppretter tilkoblingen mellom appene, definerer [!INCLUDE[d365fin](includes/d365fin_md.md)] enkelte standard tabell- og felttilordninger. Du kan endre tabelltilordningene hvis du vil. Hvis du vil ha mer informasjon, kan du se [Standard enhetstilordning for synkronisering](admin-synchronizing-business-central-and-sales.md#standard-entity-mapping-for-synchronization). Hvis du har endret standardtilordningene og vil tilbakestille endringene, går du til siden **Tilkoblingsoppsett for [!INCLUDE[d365fin](includes/cds_long_md.md)]** og velger **Bruk standard synkroniseringsoppsett**.

> [!Note]
> Hvis du bruker en lokal versjon av [!INCLUDE[d365fin](includes/d365fin_md.md)], er integrasjonstabelltilordningene lagret i tabellen 5335 Tilordninger for integreringstabell, og de kan vises og endres fra side 5335 Tilordninger for integreringstabell. Avanserte tilordninger og synkroniseringsregler er definert i codeunit 5341. 

### <a name="synchronization-rules"></a>Synkroniseringsregler
En integreringstabelltilordning inneholder også regler som styrer hvordan integrasjonssynkroniseringsjobber synkroniserer poster i en [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell og en enhet i [!INCLUDE[d365fin](includes/cds_long_md.md)]. <!--For examples of rules for an integration with Sales, see [Synchronization Rules](admin-synchronizing-business-central-and-sales.md#synchronization-rules). need to verify link -->

## <a name="mapping-integration-fields"></a>Tilordne integreringsfelt
Tilordning av tabeller er bare det første trinnet. Du må også tilordne feltene i tabellene. Integreringsfelttilordninger kobler felt i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller med tilsvarende felt i [!INCLUDE[d365fin](includes/cds_long_md.md)], og avgjør om data skal synkroniseres i hver tabell. Standard tabelltilordning som [!INCLUDE[d365fin](includes/d365fin_md.md)] sørger for, inneholder felttilordninger, men du kan endre dem hvis du vil. Hvis du vil ha mer informasjon, kan du se [Vise enhetstilordninger](admin-synchronizing-business-central-and-sales.md#tip-for-admins-viewing-entity-mappings).

> [!Note]
> Hvis du bruker en lokal versjon av [!INCLUDE[d365fin](includes/d365fin_md.md)], defineres tilordninger for integreringsfelt i tabell 5336 Tilordning for integreringsfelt.

### <a name="handling-differences-in-field-values"></a>Håndtere forskjeller i feltverdier
Noen ganger er verdiene i feltene du vil tilordne, forskjellige. I [!INCLUDE[crm_md](includes/crm_md.md)] er språkkoden for USA for eksempel "U.S.", men i [!INCLUDE[d365fin](includes/d365fin_md.md)] er den "US". Det betyr at du må transformere verdien når du synkroniserer data. Dette skjer gjennom transformeringsregler som du definerer for feltene. Du definerer transformeringsregler på siden **Tilordninger for integreringstabell** ved å velge **Tilordning** og deretter **Felt**. Forhåndsdefinerte regler er angitt, men du kan også opprette dine egne. Hvis du vil ha mer informasjon, kan du se [Transformeringsregler](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

### <a name="handling-missing-option-values-in-mapping"></a>Håndtere manglende alternativverdier i Tilordning
[!INCLUDE[d365fin](includes/cds_long_md.md)] inneholder tre felt som formidler verdier du kan tilordne til [!INCLUDE[d365fin](includes/d365fin_md.md)]-felt av typen **Alternativ** for automatisk synkronisering. Under synkroniseringen ignoreres ikke-tilordnede alternativer, og de manglende alternativene legges til i den relaterte [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen og legges til i systemtabellen **Tilordning av CDS-alternativ** for å håndteres manuelt senere. Det kan for eksempel være å legge til de manglende alternativene i hvert produkt og deretter oppdatere tilordningen. Hvis du vil ha mer informasjon, kan du se [Håndtere manglende alternativverdier](admin-cds-missing-option-values.md).

## <a name="coupling-records"></a>Koblingsposter
Kobling kobler poster i [!INCLUDE[d365fin](includes/cds_long_md.md)] til poster i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Kontoer i [!INCLUDE[d365fin](includes/cds_long_md.md)] er for eksempel vanligvis koblet sammen med kunder i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Kobling av poster gir følgende fordeler:

* Det gjør synkronisering mulig.
* Brukere kan åpne poster i én forretningsapp fra den andre. Dette krever at appene allerede er integrert.

Koblinger kan settes opp automatisk ved hjelp av synkroniseringsjobber eller manuelt ved å redigere posten i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du vil ha mer informasjon, kan du se [Synkronisere data i [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md) og [Sammenkoble og synkronisere poster manuelt](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings).

## <a name="filtering-records"></a>Filtrere poster  
Hvis du ikke vil synkronisere alle postene for en bestemt [!INCLUDE[d365fin](includes/cds_long_md.md)]-enhet eller [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell, kan du sette opp filtre for å begrense postene som synkroniseres. Du definerer filtrene på siden **Tilordninger for integreringstabell**.  

#### <a name="to-filter-records-for-synchronization"></a>Filtrere poster for synkronisering  
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Tilordninger for integreringstabell**, og velg deretter den relaterte koblingen.

2.  For å filtrere [!INCLUDE[d365fin](includes/d365fin_md.md)]-postene angir du **Tabellfilter**-feltet.  

3.  For å filtrere [!INCLUDE[d365fin](includes/cds_long_md.md)]-postene angir du **Integreringstabellfilter**-feltet.  

## <a name="creating-new-records"></a>Opprette nye poster  
Som standard vil bare poster i [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)] som er koblet, synkroniseres av integreringssynkroniseringsjobbene. Du kan definere tabelltilordninger slik at nye poster opprettes i målet (for eksempel [!INCLUDE[d365fin](includes/d365fin_md.md)]) for hver post i kilden (for eksempel [!INCLUDE[d365fin](includes/cds_long_md.md)]) som ikke allerede er koblet.  

SELGERE – Dynamics 365 Sales-synkroniseringsjobben bruker for eksempel tabelltilordningen SELGERE. Synkroniseringsjobben kopierer data fra brukerposter i [!INCLUDE[d365fin](includes/cds_long_md.md)] til selgerposter i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du setter opp tabelltilordningen til å opprette nye poster, for hver bruker i [!INCLUDE[d365fin](includes/cds_long_md.md)] som ikke er allerede koblet til en selger i [!INCLUDE[d365fin](includes/d365fin_md.md)], opprettes en ny selgerpost i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-create-new-records-during-synchronization"></a>Slik oppretter du nye poster under synkronisering  
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Tilordninger for integreringstabell**, og velg deretter den relaterte koblingen.

2.  I tabelltilordningsoppføringen i listen fjerner du **Synkroniser bare koblede poster**-feltet.  

## <a name="using-configuration-templates-on-table-mappings"></a>Bruke konfigurasjonsmaler på tabelltilordninger
Du kan tilordne konfigurasjonsmaler til tabelltilordninger til bruk for nye poster som er opprettet i [!INCLUDE[d365fin](includes/d365fin_md.md)] eller [!INCLUDE[d365fin](includes/cds_long_md.md)]. For hver tabelltilordning kan du angi en konfigurasjonsmal som skal brukes for nye [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster, og en annen mal for å bruke nye [!INCLUDE[d365fin](includes/cds_long_md.md)]-poster.  

Hvis du installerer standard synkroniseringsoppsett, vil to konfigurasjonsmaler vanligvis bli opprettet automatisk og brukes på tabelltilordningen for [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder og [!INCLUDE[crm_md](includes/crm_md.md)]-kontoer: **CDSCUST** og **CDSACCOUNT**.  

-   **CDSCUST** brukes til å opprette og synkronisere nye kunder i [!INCLUDE[d365fin](includes/d365fin_md.md)] basert på en konto i [!INCLUDE[crm_md](includes/crm_md.md)].  

     Denne malen opprettes ved å kopiere en eksisterende konfigurasjonsmal for kunder i programmet. **CDSCUST** opprettes bare hvis det finnes en eksisterende konfigurasjonsmal og **Valutakoden** -feltet i malen er tomt. Hvis et felt i konfigurasjonsmalen inneholder en verdi, brukes verdien i stedet for verdien i det tilordnede feltet for [!INCLUDE[d365fin](includes/cds_long_md.md)]-kontoen. Hvis **Land/region**-feltet i en [!INCLUDE[d365fin](includes/cds_long_md.md)]-konto inneholder *USA*, og **Land/region**-feltet i konfigurasjonsmalen er *GB*, brukes *GB* som **Land/region** for den opprettede kunden i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   **CDSACCOUNT** oppretter og synkroniserer nye kontoer i [!INCLUDE[d365fin](includes/cds_long_md.md)] basert på en konto i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Angi konfigurasjonsmaler på en tabelltilordning  
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Tilordninger for integreringstabell**, og velg deretter den relaterte koblingen.

2.  I tabelltilordningsposten i listen angir du **Malkode for konfigurasjon av tabell**-feltet, velger du konfigurasjonsmalen som skal brukes for nye poster i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

3.  Sett **Malkode for konfigurasjon av int.tab.**-feltet til konfigurasjonsmalen som skal brukes for nye poster i [!INCLUDE[d365fin](includes/cds_long_md.md)].

## <a name="see-also"></a>Se også  
[Om integrering av Dynamics 365 Business Central med [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Synkronisere Business Central og [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)   
[Planlegge en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
