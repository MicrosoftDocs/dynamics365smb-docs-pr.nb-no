---
title: Angi koblingen E-dokumenter med eksterne endepunkter
description: Denne artikkelen forklarer hvordan du konfigurerer funksjonalitet for e-dokumenter når den kobles til eksterne endepunkter.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, access-point, endpoint'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 12/13/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Angi koblingen E-dokumenter med eksterne endepunkter

Denne artikkelen forklarer hvordan du konfigurerer funksjonalitet for e-dokumenter når den kobles til eksterne endepunkter.

Før du bruker funksjonaliteten som er beskrevet i denne artikkelen, må du installere appen **Koblingen E-dokumenter med eksterne endepunkter** appen på toppen av den globale appen **E-dokumentkjerne**. Denne appen kan brukes til standardintegrering med de eksterne (tredjeparts) tilgangspunktene for å automatisere e-dokumentflyten. Fordi denne appen bare representerer noen av de valgte koblingene, er du ikke begrenset til eksisterende integreringer i den. De fleste av koblingene vil være tilgjengelige i AppSource i fremtiden.

## Definer tilkoblingen

For å starte oppsettet følger du fremgangsmåten i [Appen E-dokumentkjerne](finance-how-setup-edocuments.md). Når du har fullført denne fremgangsmåten, går du tilbake til denne artikkelen og fullfører følgende fremgangsmåte:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **E-dokumenttjenester**, og velg deretter den relaterte koblingen.
2. I feltet **Tjenesteintegrering** velger en av integreringskodene som tilbys for oppsettet av endepunktstjeneste.
3. Velg **Oppsett av tjenesteintegrering**.
4. På siden **Eksternt tilkoblingsoppsett for elektronisk dokument** velger du **Be om autorisasjonskode**. Du blir omdirigert til nettsiden for ekstern tjenesteautorisasjon og bedt om påloggingsdetaljer.
5. Kopier autorisasjonskoden til feltet **Angi autorisasjonskode**.
6. Velg **Oppdater tilgangstoken** for å være sikker på at du kan oppdatere tokenet.

    > [!NOTE]
    > Denne forbindelsen krever kommunikasjon med eksterne tjenesteleverandører som kan være gjenstand for tilleggsbetaling og krever kontrakter med dem. For å få all nødvendig legitimasjon må du kontakte tjenesteleverandørene.

7. På siden **Eksternt tilkoblingsoppsett for elektronisk dokument** fyller du ut følgende felter:

    | Feltnavn | Description |
    |---|---|
    | Nettadresse for FileAPI | Angi nettadressen for fil-API-en. |
    | Nettadresse for fildeler | Angi nettadressen for fildelene. |
    | Nettadresse for DocumentAPI | Angi nettadressen for dokumentet-API-en. |
    | Selskaps-ID | Angi selskaps-ID-en. |
    | Sendemodus | Angi sendemodusen. Du kan velge **Produksjon**, **Test** eller **Sertifisering**. |

    > [!NOTE]
    > Spør tjenesteleverandøren om alle de tidligere detaljene for å opprette en forbindelse med tilgangspunktet.

## Konfigurer selskapsopplysninger

Før du begynner å bruke e-dokumenter, må du oppdatere siden **Bedriftsinformasjon** ved å fullføre følgende trinn:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Selskapsopplysninger**, og velg deretter den relaterte koblingen.
2. I tillegg til å fylle ut de vanlige feltene må du også fylle ut følgende felter:

    | Feltnavn | Description |
    |---|---|
    | SWIFT-kode | Angi SWIFT-koden (internasjonal bankidentifiseringskode) til din primære bank. |
    | Bankregistreringsnr. | Angi bankens firesifrede avdelingsnummer. |
    | Organisasjonsnr. mva. | Angi selskapets organisasjonsnummer. |

3. Lukk siden.

## Sett opp kunder til å motta e-dokumenter

Følg følgende fremgangsmåte for å gjøre det mulig for kunder å motta e-dokumentene dine:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kunder** og velger den relaterte koblingen.
2. Åpne kortet **Kunde**.
3. I tillegg til å fylle ut de vanlige feltene spesifisere du kunden i forbindelse med sending av elektroniske dokumenter i feltet **GLN**.
4. Merk av feltet **Bruk GLN i elektroniske dokumenter** for å indikere om det globale lokasjonsnummeret (GLN) brukes som et partsidentifikasjonsnummer i elektroniske dokumenter.
5. Lukk siden.

## Andre oppsett

Før du begynner å jobbe med e-dokumenter, setter du opp **e-dokumentarbeidsflytene** og **dokumentsendingsprofilene** til bruke arbeidsflytene dine. Etter at tjenesteforbindelsen er etablert, kan du begynne å bruke e-dokumentløsningen.

## Tilgjengelige tjenesteleverandører

Microsoft ønsker å oppmuntre tilgangspunktleverandører til å legge til koblingene sine på toppen av rammeverket **E-dokumentkjerne**.

For øyeblikket er Pagero den eneste tilgangspunktleverandøren som dekkes av dette systemet. Microsoft har ingen kontraktsmessig forpliktelse med Pagero. Derfor må du lage en kontrakt med dem for å få all nødvendig legitimasjon.

Vi oppdaterer denne listen etter hvert som vi får nye leverandører av tilgangspunkter for e-dokumentutveksling.

## Se også

[Konfigurere e-dokumenter i Business Central](finance-how-setup-edocuments.md)  
[Konfigurere e-dokumenter i Business Central](finance-how-use-edocuments.md)  
[Utvide e-dokumenter i Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Økonomistyring](finance.md)  
[Fakturer salg](sales-how-invoice-sales.md)  
[Registrere kjøp med kjøpsfakturaer og ordrer](purchasing-how-record-purchases.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
