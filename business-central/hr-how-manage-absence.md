---
title: Håndtere ansattes fravær
description: Beskriver hvordan du registrerer de ansattes fravær og analyserer fraværsstatistikk ved hjelp av sidene for fraværsregistrering og ansattes fravær.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '5200, 5201, 5204, 5206, 5208, 5209, 5211, 5212'
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="manage-employee-absence"></a>Håndtere ansattes fravær
For å kunne håndtere fraværet til en ansatt må du registrere fraværet på siden **Fraværsregistrering**. Det kan deretter vises på forskjellige måter for analyse og rapportering.

Du kan vise ansattes fravær på to forskjellige sider:

* På siden **Fraværsregistrering** der du registrerer alle ansattes fravær med en linje for hvert fravær.
* På siden **Ansattes fravær** der fraværene for bare én ansatt vises. Dette er informasjonen du registrerte på siden **Fraværsregistrering**, filtrert etter den bestemte ansatte.

Hvis du skal ha nytte av statistikken, bør du alltid bruke samme enhet (time eller dag) når du registrerer fraværet til de ansatte.

## <a name="to-register-employee-absence"></a>Slik registrerer du ansattes fravær
Du kan registrere fraværet daglig eller etter et annet intervall som oppfyller behovene i organisasjonen.

1. I øvre høyre hjørne velger du ikonet **Søk etter side eller rapport**, angir **Fraværsregistrering** og velger deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. Fyll ut en linje for hvert ansattfravær du vil registrere.
4. Lukk siden.

    > [!Tip]
    > Hvis du skal ha nytte av statistikken, må du alltid bruke samme enhet, time eller dag, når du registrerer fraværet til de ansatte.

## <a name="to-view-an-individual-employees-absence"></a>Slik viser du fraværet til én ansatt
1. I øvre høyre hjørne velger du ikonet **Søk etter side eller rapport**, angir **Ansatte** og velger deretter den relaterte koblingen.
2. Velg den aktuelle ansatte, og velg deretter handlingen **Fravær**.

    Siden **Ansattes fravær** åpnes og viser samlet fravær og når fraværet begynte og sluttet.

## <a name="to-view-an-employees-absence-by-categories"></a>Slik viser du fraværet til en ansatt etter kategorier
1. I øvre høyre hjørne velger du ikonet **Søk etter side eller rapport**, angir **Ansatte** og velger deretter den relaterte koblingen.
2. Velg den aktuelle ansatte, og velg deretter handlingen **Fravær per kategori**.
3. På siden **Ansattes fravær per kategori** fyller du ut filterfeltene etter behov, og deretter velger du handlingen **Vis matrise**.

    Siden **Ansattes fravær per kat. - matrise** åpnes og viser alt fravær, inndelt etter fraværsårsak.

## <a name="to-view-all-employee-absences-by-category"></a>Slik viser du alt ansattfravær etter kategori:
1. I øvre høyre hjørne velger du ikonet **Søk etter side eller rapport**, angir **Fraværsregistrering** og velger deretter den relaterte koblingen.
2. På siden **Fraværsregistrering** velger handlingen du **Oversikt per kategori**.
3. På siden **Fravær per kategori - oversikt** angir du et filter i **Filter - ansattnr.**, slik at du kan vise fraværet til en bestemt ansatt eller en definert gruppe av ansatte.
4. Velg handlingen **Vis matrise**.

    Siden **Matrise for fraværsoversikt etter kategorier** åpnes og viser fraværet til alle de ansatte, inndelt etter ulike fraværsårsaker.

## <a name="to-view-all-employee-absences-by-period"></a>Slik viser du alt ansattfravær etter periode:
1. I øvre høyre hjørne velger du ikonet **Søk etter side eller rapport**, angir **Fraværsregistrering** og velger deretter den relaterte koblingen.
   På siden **Fraværsregistrering** velger handlingen du **Oversikt per periode**.
2. På siden **Fraværsovers. per periode** angir du et filter i feltet **Filter årsak til fravær**, slik at du kan vise ansattfravær med bestemte årsaker.
3. Velg handlingen **Vis matrise**.

    Siden **Fraværsovers. per periode - matrise** åpnes og viser fraværet til ansatte, inndelt etter perioder.

## <a name="see-also"></a>Se også
[Administrere personale](hr-manage-human-resources.md)  
[Finans](finance.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
