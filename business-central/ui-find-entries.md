---
title: Søke etter relaterte poster for dokumenter
description: 'Lær hvordan du finner dokumenter, forretningskontakter og vareposter som er knyttet til hverandre.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: find
ms.search.form: 344
ms.date: 05/23/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Søke etter relaterte poster for dokumenter

Finn ut hvordan du finner dokumenter og poster som er knyttet til hverandre basert på felles informasjon, for eksempel:

- Bilagsnummer eller bokføringsdato.
- Forretningskontakttype, nummer eller eksternt dokumentnummer.
- Vareserienummer eller partinummer.

Denne funksjonen er svært nyttig for å finne postene som resulterer fra bestemte transaksjoner. Når du søker ved hjelp av bilagsnummer, kan du skrive ut oversikten fra **Bilagsposter**-rapporten.

## Kom i gang

Funksjonen Finn poster er lett tilgjengelig fra nesten alle sider ved å trykke på tastene <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>Q</kbd>. Fra sider som spesifikt viser bokførte dokumenter eller bokførte dokumentposter, både for lister og kort, kan du også åpne funksjonen ved å velge handlingen **Søk etter poster**.

Siden **Søk etter poster** inkluderer alle relaterte dokumenter og poster basert på bilagsnr. og bokføringsdato. Siden er delt inn i tre deler:

- Den øverste delen viser felt og handlinger som du bruker til å filtrere søket.
- Den midterste delen viser relaterte dokumenter basert på søket.
- Den nederste delen viser informasjon om kildedokumentet som ble funnet ved å søke.

## Søke etter poster

Du kan søke etter oppføringer basert på informasjon om enten dokumentet, forretningskontakten eller varereferansen. I den øverste delen velger du et av følgende alternativer, avhengig av hvilken type informasjon du har:

|Handling|Description|
|------|-----------|
| **Søk etter dokumenter** | Vis poster basert på et bestemt bilagsnummer eller en bestemt bokføringsdato. |
| **Søk etter forretningskontakter** | Vis poster basert på en bestemt kontakttype, kontaktnummer eller eksternt dokumentnummer. Med dette siste alternativet kan du søke etter leverandør- eller kundedokumenter ved hjelp av nummeret som er tildelt kontakten. |
| **Søk etter varereferanser** | Vis poster basert på serienummer eller partinummer. Du kan angi partinummeret eller serienummeret, eller filtrere på partinummeret eller serienummeret du vil søke etter. Denne handlingen er nyttig hvis du vil se hvor et bestemt varesporingsnummer er brukt, hvilken leverandør det kom fra, eller hvilken kunde det ble solgt til. |

Når du har gjort et valg, angir du relevant søkeinformasjon i feltene øverst på siden. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Når du er ferdig, velger du **Søk** for å starte søket. Hvis du endrer noen av filtrene, må du velge **Søk** på nytt.

> [!TIP]
> Hvis du vil ha et par eksempler på hvordan du bruker **Søk etter poster**, kan du se [Spore varesporede varer](inventory-how-to-trace-item-tracked-items.md) og [Gjennomgang: spore serie-/partinumre](walkthrough-tracing-serial-lot-numbers.md).

## Se også

[Vare varesporede varer](inventory-how-to-trace-item-tracked-items.md)  
[Finn bokførte dokumenter uten inngående dokumentposter](across-how-find-posted-documents-without-income-document-records.md)  
[Tilgjengelighet og hurtigtaster](ui-accessibility.md)  
[Arbeid med Business Central](ui-work-product.md)  
[Legg til en sidehandling i rollesenteret](ui-bookmarks.md)  
[Finn sider og informasjon med Fortell meg](ui-search.md)  
[Finn sider med rolleutforskeren](ui-role-explorer.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
