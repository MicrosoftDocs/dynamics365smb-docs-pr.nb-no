---
title: Konfigurer digitale bilag
description: Denne artikkelen forklarer hvordan du setter opp og bruker digitale bilag i Microsoft Dynamics 365 Business Central.
author: altotovi
ms.author: altotovi
ms.reviewer: null
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.search.keywords: 'digital voucher, voucher, attachment, setup'
ms.search.form: '5579, 5582, 5587'
ms.date: 11/17/2023
ms.custom: bap-template
---

# <a name="set-up-digital-vouchers"></a>Konfigurer digitale bilag

Administratorer kan bruke funksjonalitet for digitale bilag for å kreve at dokumenter legges ved spesifikke transaksjoner når de bokføres. Derfor tillater denne funksjonaliteten en kildedrevet tilnærming og gir et bedre revisjonsspor. Ulike typer bruk kan konfigureres for dette formålet, avhengig av dokumentene eller journaltypene.

Begrepet *digitalt bilag* viser til en digital eller elektronisk form for et tradisjonelt bilag i regnskap. Et bilag er et dokument som brukes til å støtte og godkjenne økonomiske transaksjoner. I regnskap fungerer et bilag vanligvis som bevis på en utgift eller en mottak av midler. Bilaget kan inneholde detaljer som datoen for transaksjonen, en beskrivelse, beløpet og eventuelle autorisasjonssignaturer.

> [!IMPORTANT]
> I enkelte land og områder kan du være begrenset fra å konfigurere noen alternativer, fordi spesifikke oppsett kan være pålagt av juridiske krav. Hvis du møter disse begrensningene, kan du se etter en detaljert forklaring på dokumentasjonssiden for ditt land eller område.

## <a name="enable-digital-vouchers"></a>Aktiver digitale bilag

Følg denne fremgangsmåten for å aktivere funksjonalitet for digitale bilag.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 3.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Oppsett for digitalt bilag**, og velg deretter den relaterte koblingen.
2. Merk av for **Aktivert**.

## <a name="set-up-digital-vouchers-1"></a>Konfigurer digitale bilag

Du kan bruke forskjellige oppsett for følgende dokumenter og journaler.

| Posttype | Beskrivelse |
|------------|-------------|
| Salgsdokument | Angir bokføringer som er fullført fra salgsdokumenter. |
| Kjøpsdokument | Angir bokføringer som er fullført fra kjøpsdokumenter. |
| Kassakladd | Angir bokføringer som er fullført fra finanskladden for alle kontotyper bortsett fra de som er relatert til kunde og leverandør. Hvis du velger en av disse kontotypene, endrer du kontroll over bokføringsprosessen. Hvis du velger **Kunde** som kontotype, sjekker systemet ditt oppsett som er relatert til salgskladden. Hvis du velger **Leverandør** som kontotype, sjekker systemet ditt oppsett som er relatert til kjøpskladden. |
| Salgskladd | Angir bokføringene som fullføres fra salgskladden og finanskladden der **Kunde** er valgt som kontotype. |
| Kjøpskladd | Angir bokføringene som fullføres fra kjøpskladden og finanskladden der **Leverandør** er valgt som kontotype. |

Følg denne fremgangsmåten for å definere hvordan organisasjonen din bruker digitale bilag.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 3.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Oppføringsoppsett for digitalt bilag**, og velg deretter den relaterte koblingen. Alternativt på siden **Oppsett av digitalt bilag** velger du **Oppføringsoppsett**.
2. I **Oppføringstype**-kolonnen velger du et alternativ.
3. I **Kontrolltype**-kolonnen velger du et håndhevelsesalternativ. Hvis du velger **Ingen**, kan du bokføre valgt type oppføring uten digitalt bilag. Hvis du velger **Vedlegg**, må oppføringen inneholde et vedlegg. Hvis du velger **Vedlegg eller merknad**, kan du inkludere et vedlegg eller en merknad for oppføringen. 
4. Merk av for **Generer automatisk** for å generere det digitale bilaget automatisk. Hvis du for eksempel ikke vil legge til en salgsfaktura manuelt i transaksjonen, merker du av i denne avmerkingsboksen. Deretter må du bare bokføre dokumentet. Systemet oppretter automatisk dokumentet, basert på rapportoppsettet ditt og legger det ved transaksjonen.
5. Merk av for **Hopp over hvis lagt til manuelt** hvis du ikke vil legge til et automatisk generert digitalt bilag hvis brukeren allerede har lagt til et manuelt vedlegg.

### <a name="use-source-codes-for-setup"></a>Bruk kildespor for oppsett

For å bruke håndheving for kladder, men ikke for alle transaksjonstyper, kobler du til det spesifikke kildesporet for å identifisere oppføringstypen i finanskladden, salgskladden eller kjøpskladden.

Følg denne fremgangsmåten for å konfigurere spesifikke kildespor for digitale bilag.

1. På siden **Oppføringsoppsett av digitalt bilag** velger du **Kildespor**.
2. På siden **Kildespor for bilagsoppføring** velger du kildesporene du vil konfigurere.
3. Lukk siden.

## <a name="use-the-functionality"></a>Bruk funksjonaliteten

Åpne et kjøps- eller salgsdokument, og skriv inn informasjon i de obligatoriske feltene. Før du bokfører dokumentet, må du følge denne fremgangsmåten for å legge ved et digital bilag.

1. I faktaboksen **Innkommende dokumentfiler** velger du **Legg ved fil**.
2. Dra en fil direkte til siden **Sett inn fil**, eller bla til filen fra denne siden.

Dokumentet legges ved i faktaboksen **Innkommende dokumentfiler**. For hver linje kan du finne dokumentnavn og -type.

Hvis du ved et uhell legger ved feil bilag, følger du denne fremgangsmåten for å slette den før du bokfører dokumentet.

1. I faktaboksen **Innkommende dokumentfiler** fra dokumentlinjen velger du **Innkommende dokument**.
2. På siden **Innkommende dokument** velger du **Slett**.

> [!NOTE]
> Hvis vedlegg av et digitalt bilag er konfigurert som obligatorisk, og du prøver å bokføre dokumenter eller kladder uten å legge ved et bilag, hindrer systemet deg i å bokføre. Du får følgende feilmelding: Ikke mulig å bokføre uten å legge ved det digitale bilaget.

### <a name="find-attached-vouchers-in-transactions"></a>Finn vedlagte bilag i transaksjoner

Du kan finne det vedlagte bilaget fra det bokførte dokumentet eller fra siden **Finanskladder** ved å se i faktaboksen **Innkommende dokumentfiler**.

Du kan ikke slette et vedlagt dokument etter bokføringen er fullført. Du kan imidlertid legge til flere vedlegg etter at bokføringen er fullført.

## <a name="see-also"></a>Se også

[Økonomistyring](finance.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
