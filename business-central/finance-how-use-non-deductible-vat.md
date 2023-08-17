---
title: Bruk ikke-fradragsberettiget mva.
description: Denne artikkelen forklarer hvordan du bruker og rapporterer ikke-fradragsberettiget mva.
author: altotovi
ms.author: altotovi
ms.reviewer: null
ms.service: dynamics365-business-central
ms.topic: how-to
ms.search.keywords: 'VAT, non-deductible, return, settlement'
ms.search.form: '50, 51, 52, 161, 187, 317, 403, 6640, 9401'
ms.date: 04/26/2023
ms.custom: bap-template
---

# <a name="use-non-deductible-vat"></a>Bruk ikke-fradragsberettiget mva.

Denne artikkelen forklarer hvordan du bruker og rapporterer ikke-fradragsberettiget mva.

## <a name="create-a-purchase-invoice-with-non-deductible-vat"></a>Opprett en kjøpsfaktura med ikke-fradragsberettiget mva.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 3.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.
2. Velg **Opprett** for å opprette en kjøpsfaktura, og angi passende informasjon i fakturahodet.
3. I delen **Linjer** oppretter du en ny linje av en hvilken som helst type, basert på mva-firmabokføringsgruppen og mva-produktbokføringsgruppen der du konfigurerer ikke-fradragsberettiget mva.
4. Angi passende verdier i feltene **Antall** og **Direkte enhetskost**.

    Hvis du merket av for **Vis ikke-fradragsberettiget mva. i linjer** på siden **Mva-oppsett**, beregnes beløpene i feltene **Ikke-fradragsberettiget mva-grunnlag** og **Ikke-fradragsberettiget mva-beløp** basert på feltet **Ikke-fradragsberettiget mva-prosent** på siden **Mva-bokføringsoppsett**.

5. Bokfør fakturaen.

## <a name="create-a-purchase-order-with-non-deductible-vat"></a>Opprett en bestilling med ikke-fradragsberettiget mva.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 3.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bestillinger**, og velg deretter den relaterte koblingen.
2. Velg **Opprett** for å opprette en bestilling, og angi passende informasjon i dokumenthodet.
3. I delen **Linjer** oppretter du en ny linje av en hvilken som helst type, basert på mva-firmabokføringsgruppen og mva-produktbokføringsgruppen der du konfigurerer ikke-fradragsberettiget mva.
4. Angi passende verdier i feltene **Antall** og **Direkte enhetskost**.

    Hvis du merket av for **Vis ikke-fradragsberettiget mva. i linjer** på siden **Mva-oppsett**, beregnes beløpene i feltene **Ikke-fradragsberettiget mva-grunnlag** og **Ikke-fradragsberettiget mva-beløp** basert på feltet **Ikke-fradragsberettiget mva-prosent** på siden **Mva-bokføringsoppsett**.

5. Bokfør bestillingen.

## <a name="adjust-rounded-vat-amounts-before-document-posting"></a>Juster avrundede mva-beløp før dokumentbokføring

Hvis mva-beløp ikke er avrundet på samme måte i miljøet og i det eksterne regnskapssystemet (det opprinnelige fakturadokumentet), kan du justere mva-beløpet før du bokfører dokumentet. Følg denne fremgangsmåten før du bokfører dokumentet for å utføre denne justeringen.

1. Velg **Statistikk** i handlingsruten.
2. Hvis du arbeider med en kjøpsfaktura, følger du denne fremgangsmåten:

    1. På hurtigfanen **Linjer** velger du mva-beløpet eller ikke-fradragsberettiget mva-beløp.
    2. Angi verdiene du trenger i det opprinnelige dokumentet, og lukk deretter siden **Kjøpsfakturastatistikk**.

3.  Hvis du arbeider med bestillingen, følger du denne fremgangsmåten:

    1. Velg **Antall mva-linjer** på hurtigfanen **Fakturering** for å åpne siden **Mva-beløpslinjer**.
    2. Velg mva-beløpet eller ikke-fradragsberettiget mva-beløp du vil korrigere.
    3. Skriv inn verdiene du trenger fra det opprinnelige dokumentet, lukk siden **Mva-beløpslinjer**, og lukk deretter siden **Bestillingsstatistikk**.

Hvis du vil bruke justeringer av mva-beløp, må du aktivere justeringene. Angi den maksimale mva-differansen som er tillatt, i feltet **Maks. tillatte mva-differanse** på siden **Finansoppsett**. På siden **Kjøpsoppsett** velger du **Tillat mva-differanse**.

Du kan justere verdiene i feltene **Mva-beløp** og **Ikke-fradragsberettiget mva-beløp**. Verdien til feltet **Fradragsberettiget mva-beløp** er resultatet av disse to verdiene. Beløpet du angir i feltet **Ikke-fradragsberettiget mva-beløp**, kan ikke være høyere enn beløpet du angir i feltet **Mva-beløp**. Feltet **Maks tillatte mva-differanse** på siden **Finansoppsett** fungerer uavhengig av fradragsberettigede og ikke-fradragsberettigede mva-beløp på statistikkside når du vil justere mva-beløp.

> [!IMPORTANT]
> Du kan ikke bruke ikke-fradragsberettiget mva. på forskuddsfakturaene.

## <a name="see-also"></a>Se også

[Økonomistyring](finance.md)

[Definer beregninger og bokføringsmetoder for merverdiavgift](finance-setup-vat.md)  

[Konfigurer ikke-fradragsberettiget mva.](finance-setup-nondeductible-vat.md)

[Utformingsdetaljer om ikke-fradragsberettiget mva.](design-details-nondeductible-vat.md)

[Rapporter mva. til skattemyndighetene](finance-how-report-vat.md)

[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
