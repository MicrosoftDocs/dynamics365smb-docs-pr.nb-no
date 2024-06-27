---
title: Skriv ut en lagerplukkliste fra ordre
description: 'Du kan skrive ut en plukkliste for lager direkte fra en ordre, salg, faktura og andre utgående salgsdokumenter.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 02/07/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Skriv ut plukklisten

Du kan skrive ut en plukkliste for lager direkte fra en ordre og andre dokumenter som igangsetter leveringen av varer.

Denne rapporten brukes vanligvis i selskaper uten egen funksjonalitet for lagerstyring, slik at en lagerarbeider kan vise eller skrive ut plukklisten fra det tilknyttede salgsdokumentet. I selskaper med høyere volum eller mer komplekse prosesser, planlegges levering og plukking og utføres i egne lagerdokumenter. Finn ut mer under [Utgående lagerflyt](design-details-outbound-warehouse-flow.md).

## Skrive ut en plukkliste fra en ordre

Følgende fremgangsmåte er basert på en ordre. Fremgangsmåten er de samme for alle andre dokumenter som kan brukes til å starte levering av varer, for eksempel en overføringsordre.

1. Velg ikonet ![Søk etter side eller rapport.](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.  
2. Åpne ordren du vil plukke varer for.  
3. Velg **Rapport**-handlingen, og velg deretter **Plukklisten etter ordre**-handlingen.  
4. Velg **Skriv ut** for å skrive ut plukklisten, eller velg **Forhåndsvisning** for å vise den på skjermen.

Du kan også lagre plukklisten som et dokument, for eksempel for å sende til noen, eller legge til som et vedlegg i ordren. Finn ut mer under [Behandle vedlegg, koblinger og merknader på kort og dokumenter](ui-how-add-link-to-record.md).

> [!NOTE]
> Hvis du brukte **Utfold stykkliste**-funksjonen på ordren, vises bare komponentene for den tilknyttede monteringsvaren i rapporten. Finn ut mer under [Arbeid med stykklister](inventory-how-work-BOMs.md).

## Se også

[Lager](inventory-manage-inventory.md)  
[Utgående lagerflyt](design-details-outbound-warehouse-flow.md)
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
