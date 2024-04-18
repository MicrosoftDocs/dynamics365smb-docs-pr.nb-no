---
title: Bærekraftsoppsett
description: Finn ut hvordan du konfigurerer bærekraftsfunksjoner.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD'
ms.search.form: null
ms.date: 04/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Bærekraftsoppsett  

Hvis bærekraftmodulen skal fungere skikkelig, må du først sette opp noen grunnleggende kontroller og instruksjoner knyttet til hele funksjonaliteten.  

Følg denne fremgangsmåten for å sette opp en bærekraftmodul:  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Bærekraftsoppsett** og velger den relaterte koblingen.  
2. På hurtigfanen **Generelt** konfigurerer du de obligatoriske feltene som er relatert til denne modulen:   

|  Felt  |  Description  |  
|--------|--------------| 
| **Utslippsenhetskode** | Angir enhetskoden som brukes til å registrere utslipp. |
| **Desimalplasser for utslipp** | Angir antall desimaler som vises for utslippsmengder. Standardinnstillingen 2:5 angir at alle beløp vises med minimum 2 desimaler og maksimalt 5 desimaler. Du kan også angi et fast tall, for eksempel 2, som også betyr at beløpene vises med to desimaler. |
| **Land/område obligatorisk** | Angir om land/område er obligatorisk. Du kan bruke dette feltet i kladder uten å konfigurere dette, men du kan velge det hvis du vil tvinge brukere til å fylle ut feltet før bokføring. |
| **Ansvarssenter obligatorisk** | Angir om ansvarssenter er obligatorisk, da ansvarssenteret kan brukes som et anlegg for måling av anleggsbaserte utslipp. Du kan bruke dette feltet i kladder uten å konfigurere dette, men du kan velge det hvis du vil tvinge brukere til å fylle ut feltet før bokføring. |
| **Blokker endring av beregningsgrunnlag hvis det finnes poster** | Angir om endringen av beregningsgrunnlaget i kontokategorien er sperret på tidspunktet for bærekraftsposten, noe som betyr at denne formelen allerede er brukt. |
| **Aktiver bakgrunnsfeilkontroll** | Angir om bakgrunnsfeilkontroll av bærekraftskladdelinjer er aktivert. |

3.  På hurtigfanen **Beregninger** konfigurerer du obligatoriske felter relatert til formlene som brukes til å beregne utslipp:  

|  Felt  |  Description  |  
|--------|--------------| 
| **Desimalplasser for drivstoff/elektrisitet** | Angir antall desimaler som vises for brensel-/elektrisitetsmengder. Standardinnstillingen 2:5 angir at alle beløp vises med minimum 2 desimaler og maksimalt 5 desimaler. Du kan også angi et fast tall, for eksempel 2, som også betyr at beløpene vises med to desimaler. |
| **Desimalplasser for avstand** | Angir antall desimaler som vises for avstandsmålinger. Standardinnstillingen 2:5 angir at alle beløp vises med minimum 2 desimaler og maksimalt 5 desimaler. Du kan også angi et fast tall, for eksempel 2, som også betyr at beløpene vises med to desimaler. |
| **Egendefinert antall desimaler for beløp** | Angir antall desimaler som vises for egendefinerte mengder. Standardinnstillingen 2:5 angir at alle beløp vises med minimum 2 desimaler og maksimalt 5 desimaler. Du kan også angi et fast tall, for eksempel 2, som også betyr at beløpene vises med to desimaler. |

4.  Fullfør oppsettet på hurtigfanen **Rapportering** relatert til rapportering til myndigheter:   

|  Felt  |  Description  |  
|--------|--------------| 
| **Enhetskode for utslippsrapportering** | Angir enhetskoden som brukes til å rapportere utslipp, siden du kan bruke forskjellige enheter når du rapporterer til myndigheter. Dette feltet gjelder ikke for standardrapportene. |
| **Enhetsfaktor for rapportering** | Angir enhetsfaktoren som brukes til å registrere utslipp hvis du bruker forskjellige enheter når du rapporterer til myndigheter. |
| **Avrundingspresisjon for utslipp** | Angir størrelsen på intervallet som skal brukes når du avrunder utslippsbeløp mens du rapporterer til myndigheter. |
| **Avrundingstype for utslipp** | Angir hvordan programmet avrunder en utslippsmengde under rapportering til myndighetene, ved hjelp av alternativene Nærmeste, Opp eller Ned. |

>[!NOTE]
> I versjon 24.0 støtter ikke [!INCLUDE[prod_short](includes/prod_short.md)] rapportering til noen myndighet. Felt som er relatert til konfigurasjon i hurtigfanen **Rapportering**, blir brukt for fremtidige rapporteringsfunksjoner, men det kan også brukes av partnere i lokaliserte versjoner.

## Se også  
[Finans](finance.md)    
[Oversikt over bærekraftsbehandling](finance-manage-sustainability.md)
[Bærekraftskontoplan og finans](finance-sustainability-accounts-ledger.md)
[Slik registrerer du utslipp](finance-sustainability-journal.md)
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
