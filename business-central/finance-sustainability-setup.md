---
title: Bærekraftsoppsett
description: Finn ut hvordan du konfigurerer bærekraftsfunksjoner.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD'
ms.search.form: null
ms.date: 05/08/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="sustainability-setup"></a>Bærekraftsoppsett

Før bærekraftmodulen kan fungere som den skal, må du konfigurere noen grunnleggende kontroller og instruksjoner som er knyttet til hele funksjonaliteten.

Følg denne fremgangsmåten for å konfigurere en bærekraftmodul:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bærekraftsoppsett**, og velg deretter den relaterte koblingen.
2. Konfigurer de obligatoriske feltene som er relatert til bærekraftmodulen, i hurtigfanen **Generelt**.

    | Felt | Beskrivelse |
    |-------|-------------|
    | **Utslippsenhetskode** | Angi enhetskoden som brukes til å registrere utslipp. |
    | **Desimalplasser for utslipp** | Angi antall desimaler som vises for utslippsmengder. Standardinnstillingen *2:5* angir at alle mengder vises med minst to desimaler og maksimalt fem desimaler. Du kan også angi et fast tall. Hvis du for eksempel angir *2*, vises to desimaler for alle mengder. |
    | **Land/område obligatorisk** | Angi om land/område skal være obligatorisk. Brukere kan angi feltet for land/område i kladder selv om du ikke velger dette feltet. Hvis du imidlertid velger det, krever du at brukerne angir feltet for land/område før de bokfører. |
    | **Ansvarssenter obligatorisk** | Angi om ansvarssenteret skal være obligatorisk. Ansvarssenteret kan brukes som et anlegg, slik at du kan måle anleggsbaserte utslipp. Brukere kan angi feltet for ansvarssenter i kladder selv om du ikke velger dette feltet. Hvis du imidlertid velger det, krever du at brukerne angir feltet for ansvarssenter før de bokfører. |
    | **Blokker endring av beregningsgrunnlag hvis det finnes poster** | Angi om endringer i beregningsgrunnlaget (formelen) på kontokategorinivået skal sperres på registreringstidspunktet for bærekraftsposten, etter at formelen allerede er brukt. |
    | **Aktiver bakgrunnsfeilkontroll** | Angi om bakgrunnsfeilkontroll av bærekraftskladdelinjer skal være aktivert. |

    > [!NOTE]
    > Etter at du har aktivert eller deaktivert bakgrunnsfeilkontrollen i kladder, må du logge deg på på nytt før du starter den nye konfigurasjonen.

3. I hurtigfanen **Beregninger** konfigurerer du de obligatoriske feltene som er relatert til formlene som brukes til å beregne utslipp.

    | Felt | Beskrivelse |
    |-------|-------------|
    | **Desimalplasser for drivstoff/elektrisitet** | Angi antall desimaler som skal vises for drivstoff-/elektrisitetsmengder. Standardinnstillingen *2:5* angir at alle mengder vises med minst to desimaler og maksimalt fem desimaler. Du kan også angi et fast tall. Hvis du for eksempel angir *2*, vises to desimaler for alle mengder. |
    | **Desimalplasser for avstand** | Angi antall desimaler som skal vises for avstandsmålinger. Standardinnstillingen *2:5* angir at alle mengder vises med minst to desimaler og maksimalt fem desimaler. Du kan også angi et fast tall. Hvis du for eksempel angir *2*, vises to desimaler for alle mengder. |
    | **Egendefinert antall desimaler for beløp** | Angi antall desimaler som skal vises for egendefinerte mengder. Standardinnstillingen *2:5* angir at alle mengder vises med minst to desimaler og maksimalt fem desimaler. Du kan også angi et fast tall. Hvis du for eksempel angir *2*, vises to desimaler for alle mengder. |

4. I hurtigfanen **Rapportering** fullfører du konfigurasjonen ved å konfigurere feltene som er relatert til rapportering til myndighetene.

    > [!NOTE]
    > I versjon 24.0 støtter ikke [!INCLUDE[prod_short](includes/prod_short.md)] rapportering til noen myndigheter. Feltene som er knyttet til konfigurasjonen av denne funksjonaliteten i hurtigfanen **Rapportering**, er derfor ment for fremtidige rapporteringsfunksjoner. Partnere kan imidlertid også bruke disse feltene i lokaliserte versjoner.

    | Felt | Beskrivelse |
    |-------|-------------|
    | **Enhetskode for utslippsrapportering** | Angi enhetskoden som brukes til å rapportere utslipp, siden du kan bruke en annen enhet når du rapporterer til myndigheter. Dette feltet gjelder ikke for standardrapportene. |
    | **Enhetsfaktor for rapportering** | Angi enhetsfaktoren som brukes til å registrere utslipp hvis du bruker en annen enhet når du rapporterer til myndigheter. |
    | **Avrundingspresisjon for utslipp** | Angi størrelsen på intervallet som brukes under avrunding av utslippsmengder, når du rapporterer til myndigheter. |
    | **Avrundingstype for utslipp** | Angi hvordan programmet avrunder utslippsmengder når du rapporterer til myndigheter. Følgende alternativer er tilgjengelige: **Nærmeste**, **Opp** og **Ned**. |

## <a name="see-also"></a>Se også

[Finans](finance.md)  
[Oversikt over bærekraftsadministrasjon](finance-manage-sustainability.md)  
[Bærekraftskontoplan og finans](finance-sustainability-accounts-ledger.md)  
[Registrer bærekraftsposter](finance-sustainability-journal.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
