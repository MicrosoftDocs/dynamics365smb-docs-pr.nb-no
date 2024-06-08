---
title: Tredjeparts kjøpstransaksjoner for EU
description: Dette artikkelemnet forklarer hvordan du definerer og bruker tredjeparts kjøpstransaksjoner for EU.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.form: '50, 51, 52, 187, 317'
ms.search.keywords: 'EU3P, EU 3-P, EU 3-Party'
ms.date: 07/07/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="eu-third-party-purchase-transactions"></a>Tredjeparts kjøpstransaksjoner for EU

Tredjepartshandel for EU skjer når du mottar en kjøpsfaktura fra en kunde i et EU-land/-område, og produktene sendes til et annet EU-land/-område uten at du må angi bostedsland. Transaksjonsbeløpet kan identifiseres og rapporteres separat for å overholde noen EU-lands/-områders mva-rapportering (merverdiavgift) og VIES-krav (VAT Information Exchange System). Microsoft Dynamics 365 Business Central gjør det mulig å definere kjøpstransaksjoner som tredjepartshandel i EU. Bokførte tredjepartstransaksjoner for EU kan filtreres i mva-oppgaver og utelates fra beløpet i kolonnen **Salg til kunde** i rapporten **EU-mva. – brukes ikke i Norge**.

Selv om funksjonen er forhåndsinstallert som en utvidelse, er den ikke aktivert som standard. Følg fremgangsmåten nedenfor for å aktivere funksjonen.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , gå til arbeidsområdet **Funksjonsstyring**, og velg deretter den relaterte koblingen.
2. I listen finner og velger du **Funksjonsoppdatering: Erstatt den eksisterende funksjonaliteten for trekanthandel med den nye utvidelsen Trekanthandel**.
3. Velg **Alle brukere** i kolonnen **Aktivert for**.

## <a name="enable-eu-third-party-trade-functionality-for-a-purchase"></a>Aktiver tredjepartshandelsfunksjonalitet for EU for et kjøp

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Mva-oppsett** og velg den relaterte koblingen.
2. Merk av for **Aktiver trekanthandel** på siden **Mva-oppsett**.

## <a name="use-eu-third-party-trade-functionality"></a>Bruk funksjonalitet for trekanthandel

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Kjøpsfaktura** (eller et annet kjøpsdokument), og velg deretter den relaterte koblingen.
2. Velg en eksisterende kjøpsfaktura, eller velg **Ny** for å opprette en ny.
3. På hurtigfanen **Fakturadetaljer** merker du av for **Trekanthandel**.
4. Velg **OK**.

## <a name="include-or-exclude-eu-third-party-trade-records-on-the-vat-statement"></a>Ta med eller utelat poster for trekanthandel i mva-oppgaven

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Mva-oppgave** og velg den relaterte koblingen.
2. På siden **Mva-oppgave** velger du et av følgende alternativer for å vise poster for trekanthandel ved hjelp av feltet **Filter for trekanthandel**.

    | Alternativ | Description |
    |--------|-------------|
    | Alle | Vis alle poster, uavhengig av om feltet **Trekanthandel** i dokumenter ble merket. |
    | Trekanthandel | Vis bare poster der feltet **Trekanthandel** i dokumenter ble merket. |
    | Ikke trekanthandel | Vis bare poster der feltet **Trekanthandel** i dokumenter ikke ble merket. |


## <a name="see-also"></a>Se også
[Økonomistyring](finance.md)  
[Arbeid med Business Central](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
