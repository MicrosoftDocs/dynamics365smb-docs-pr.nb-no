---
title: Definer ikke-fradragsberettiget mva
description: Denne artikkelen forklarer hvordan du konfigurerer ikke-fradragsberettiget mva i Microsoft Dynamics 365 Business Central.
author: altotovi
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.search.keywords: 'VAT, non-deductible, setup'
ms.search.form: '187, 472, 473'
ms.date: 08/13/2024
ms.custom: bap-template
ms.reviewer: bholtorf
---

# <a name="set-up-nondeductible-vat"></a>Definer ikke-fradragsberettiget mva

Ikke-fradragsberettiget merverdiavgift (mva) er merverdiavgiften som skal betales av en kjøper, men som ikke er fradragsberettiget fra innkjøper egen mva-gjeld. Selskaper kan vanligvis gjenopprette mva. på kjøp av varer og tjenester som er knyttet til forretningsaktivitetene. I enkelte situasjoner påløper det mva. som ikke er fradragsberettiget, for bedrifter. Disse situasjonene er vanligvis knyttet til de lokale bestemmelsene og kan variere blant land/områder. Modellen for bruk av ikke-fradragsberettiget eller delvis fradragsberettiget mva. er imidlertid lik. Du kan bruke forholdsmessig mva. til å beregne mva. når fradragsberettiget og ikke-fradragsberettiget mva. forekommer.

Vanligvis kan ikke mva. trekkes fra for enkelte kjøp på grunn av følgende faktorer:

- **Typen varer eller tjenester som er kjøpt** – mva. er helt eller delvis ikke-fradragsberettiget ifølge loven om varer som biler, mobiltelefoner og mat som kjøpes på restauranter.
- **Delvis fradragsberettiget proporsjonal mva.** – Mva. er proporsjonal i henhold til forholdet mellom salgsoperasjonene som mva. skyldes for, og alle utførte operasjoner. Mva. som overskrider dette forholdet, kan ikke trekkes fra.

Siden det kan være vanskelig å vite hvor og hvordan en vare brukes, bør du kontakte de lokale skattemyndighetene i landet/området ditt. De kan hjelpe deg med å avgjøre om du kan trekke fra en bestemt prosentandel av mva., basert på historiske data.

> [!IMPORTANT]
> Denne globale funksjonen er tilgjengelig i alle land med aktivert mva. **unntatt for Belgia, Italia og Norge**. Disse lokaliseringene har allerede eksisterende lokal funksjon og vil oppgraderes senere. Ikke kjør denne funksjonen i disse landene, fordi oppgraderingsprosedyren finnes ikke.

## <a name="use-nondeductible-vat"></a>Bruk ikke-fradragsberettiget mva

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 3.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Mva-oppsett** og velg den relaterte koblingen.
2. Merk av for **Aktiver ikke-fradragsberettiget mva.**.

    > [!IMPORTANT]
    > Når du har aktivert ikke-fradragsberettiget mva., kan du ikke deaktivere den fordi funksjonen kan inkludere endringer i data og kan starte en oppgradering av noen databasetabeller. Microsoft anbefaler på det sterkeste at du først aktiverer og tester denne funksjonen i sandkassemiljøet før du aktiverer den i produksjonsmiljøet.

3. Konfigurer hvordan [!INCLUDE [prod_short](includes/prod_short.md)] skal behandle ikke-fradragsberettigede mva-verdier.

    1. I feltet **Bruk for varekostnad** angir du om ikke-fradragsberettiget mva. skal legges til i varekostnaden når du kjøper varer. Ellers vil ikke-fradragsberettiget mva. få innvirkning på varekostnaden, og hele beløpet registreres bare på finansnivå.
    2. Velg avmerkingsboksen **Bruk for objektkostnad** for å legge til den ikke-fradragsberettigede mva. i objektkostnaden når du kjøper nye objekter. Ellers vil ikke-fradragsberettiget mva. få innvirkning på objektkostnaden, og hele beløpet registreres bare på finansnivå.
    3. Velg avmerkingsboksen **Bruk for prosjektkostnad** for å angi at ikke-fradragsberettiget mva. skal legges til i prosjektkostnaden når du kjøper varer for prosjektet. Ellers vil ikke-fradragsberettiget mva. få innvirkning på prosjektkostnaden, og hele beløpet registreres bare på finansnivå.
    4. Merk av for **Vis ikke-fradragsberettiget mva. i linjer** for å angi at ikke-fradragsberettiget mva. skal vises på dokumentlinjesider for enklere redigering av mva-beløp.

## <a name="use-the-nondeductible-vat-percentage"></a>Bruk den ikke-fradragsberettigede mva-prosenten

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 3.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Mva-bokføringsoppsett**, og velg deretter den relaterte koblingen.
2. På siden **Mva-bokføringsoppsett** angir du feltene som beskrevet i tabellen nedenfor.

    | Felt | Description |
    |-------|-------------|
    | **Tillat ikke-fradragsberettiget mva.** | Angi om ikke-fradragsberettiget mva. vurderes for nåværende kombinasjon av mva-firmabokføringsgruppe og mva-produktbokføringsgruppe. |
    | **ikke-fradragsberettiget mva. %** | Angi prosentandelen av transaksjonsbeløpet som mva. ikke brukes på. |
    | **Ikke-fradragsberettiget inngående mva-konto** | Angi kontoen som er knyttet til mva-beløpet som ikke er fratrukket på grunn av typen varer eller tjenester som er kjøpt. |

    > [!NOTE]
    > Hvis du vil ha finansposter som bruker den dedikerte kontoen i stedet for salgs-/kjøpskontoen, kan du enten la feltet **Ikke-fradragsberettiget mva-konto** være tomt eller angi feltet **Finanskonto**.

3. Velg **OK**.

> [!NOTE]
> Du kan ikke bruke urealisert mva. sammen med ikke-fradragsberettiget mva.
>
> Ikke bruk den samme **mva-type** for både normal mva. der feltet **Ikke-fradragsberettiget mva-prosent** er satt til **0** (null) og normal mva., der feltet **Ikke-fradragsberettiget mva-prosent** er satt til en verdi som ikke er null. Ellers beregnes ikke det totale mva-beløpet som ikke er fradragsberettiget mva., på riktig måte.

## <a name="see-also"></a>Se også

[Økonomistyring](finance.md)  
[Utformingsdetaljer: Ikke-fradragsberettiget mva](design-details-nondeductible-vat.md)  
[Bruk ikke-fradragsberettiget mva](finance-how-use-non-deductible-vat.md)  
[Definer beregninger og bokføringsmetoder for merverdiavgift](finance-setup-vat.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
