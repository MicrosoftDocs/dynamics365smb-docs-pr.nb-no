---
title: Utformingsdetaljer – ikke-fradragsberettiget mva.
description: 'Denne artikkelen gir informasjon om ikke-fradragsberettiget merverdiavgift (mva.) som skal betales av en kjøper, mens som ikke er fradragsberettiget fra innkjøper egen mva-gjeld.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 07/04/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="design-details-non-deductible-vat"></a>Utformingsdetaljer: Ikke-fradragsberettiget mva.

Ikke-fradragsberettiget merverdiavgift (mva.) er merverdiavgiften som skal betales av en kjøper, mens som ikke er fradragsberettiget fra innkjøper egen mva-gjeld. Siden det kan være vanskelig å vite hvor og hvordan varen blir brukt, må du ta kontakt med lokale skattemyndigheter i landet eller området for å finne ut om en angitt prosentandel mva. kan gå til fradrag. Selv om du vet at en bestemt prosentandel av mva. ikke er fradragsberettiget, er det forskjellige modeller for håndtering av ikke-fradragsberettigede beløp siden de er knyttet til **varer** og **aktiva**.

## <a name="prerequisites-for-using-non-deductible-vat"></a>Forutsetninger for bruk av ikke-fradragsberettiget mva.

Følg denne fremgangsmåten for å bruke og bokføre ikke-fradragsberettiget mva.

1. På siden **Mva-oppsett** velger du **Aktiver ikke-fradragsberettiget mva.** for å aktivere funksjonen.
2. På siden **Mva-bokføringsoppsett** velger du hvilke mva-bokføringsgrupper som kan bruke ikke-fradragsberettiget mva.

## <a name="examples"></a>Eksempler

For følgende eksempler er ikke-fradragsberettiget mva. aktivert, og følgende oppsett er fullført:

- Feltet **Mva-varebokføringsgruppe** er satt til **NDVAT**.
- På siden **Mva-bokføringsoppsett**:

    - **NDVAT** er definert som mva-varebokføringsgruppe, og **INNENLANDS** er angitt som mva-firmabokføringsgruppe.
    - Verdien **Mva-type** må være unik.
    - Feltet **Mva-sats** er satt til **25**.
    - Feltet **Tillat ikke-fradragsberettiget mva.** er angitt til **Tillatt**.
    - Feltet **Ikke-fradragsberettiget mva-sats** er angitt til **100**.
    - Feltet **Mva-beregningstype** er satt til **Normal mva.**.
    - Bare utgående mva-konto og inngående mva-konto konfigureres.

Alle eksemplene bruker varer og aktiva der mva-varebokføringsgruppen er **NDVAT**.

### <a name="items"></a>Varer

En ny vare har **NDVAT** angitt som mva-varebokføringsgruppe. I kjøpsdokumentet er **Antall** = **1** og **Direkte enhetskost eks. mva.** = **1 000,00**.

Uansett hvilket alternativ som brukes, vil resultatene i **mva-posten** være like.

| Dokumenttype | Type | Base | Beløp | Ikke-fradragsberettiget mva-grunnlag | Ikke-fradragsberettiget mva-beløp |
|---|---|---|---|---|---|
| Fakturere | Kjøp | 0.00 | 0.00 | 1,000.00 | 250.00 |

Opplysningene vises i **verdipostene**.

> [!NOTE]
> Du kan aktivere feltet **Bruk for varekostnad** på siden **Mva-oppsett**.

#### <a name="use-for-item-cost-isnt-enabled"></a>Bruk for varekost er ikke aktivert

| Vareposttype | Posttype | Kostbeløp (faktisk) | Varepostantall |
|---|---|---|---|
| Kjøp | Direkte kostnad | 1,000.00 | 1 |

#### <a name="use-for-item-cost-is-enabled"></a>Bruk for varekost er aktivert

| Vareposttype | Posttype | Kostbeløp (faktisk) | Varepostantall |
|---|---|---|---|
| Kjøp | Direkte kostnad | 1,250.00 | 1 |

### <a name="fixed-assets"></a>Aktiva

Et nytt objekt har kontoen for anskaffelseskost satt til å bruke **NDVAT** som mva-varebokføringsgruppe. I kjøpsdokumentet er **Antall** = **1** og **Direkte enhetskost eks. mva.** = **1 000,00**.

Uansett hvilket alternativ som brukes, vil resultatene i **mva-posten** være like.

| Dokumenttype | Type | Base | Beløp | Ikke-fradragsberettiget mva-grunnlag | Ikke-fradragsberettiget mva-beløp |
|---|---|---|---|---|---|
| Fakturere | Kjøp | 0.00 | 0.00 | 1,000.00 | 250.00 |

Opplysningene vises i **objektpostene**.

> [!NOTE]
> Du kan aktivere feltet **Bruk for objektkostnad** på siden **Mva-oppsett**.

#### <a name="use-for-fixed-asset-cost-isnt-enabled"></a>Bruk for objektkostnad er ikke aktivert

| Dokumenttype | Aktivabokføringstype | Beløp | Mva-beløp |
|---|---|---|---|
| Fakturere | Anskaffelseskost | 1,000.00 | 250.00 |

#### <a name="use-for-fixed-asset-cost-is-enabled"></a>Bruk for objektkostnad er aktivert

| Dokumenttype | Aktivabokføringstype | Beløp | Mva-beløp |
|---|---|---|---|
| Fakturere | Anskaffelseskost | 1,000.00 | 250.00 |
| Fakturere | Anskaffelseskost | 250.00 | 0.00 |

## <a name="see-also"></a>Se også

[Konfigurer ikke-fradragsberettiget mva.](finance-setup-nondeductible-vat.md)  
[Finans](finance.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
