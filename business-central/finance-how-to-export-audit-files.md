---
title: Revisjonsfileksport
description: 'Denne artikkelen forklarer hvordan du definerer forskjellige eksportformater og deretter bruker dem, basert på revisor- eller myndighetskrav.'
author: altotovi
ms.service: dynamics365-business-central
ms.topic: how-to
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'audit, export, SIE, SAF-T, FAC, GDPdU, file export'
ms.search.form: '5260, 5261, 5264, 5266, 5267, 5270'
ms.date: 04/04/2023
ms.author: altotovi
ms.reviewer: kfend
---

# Revisjonsfileksport

Eksport av bokføringsinformasjon fra systemet er en vanlig forespørsel fra noen lokale myndigheter eller revisorer. Det kan være forskjellige typer formater og obligatorisk informasjon. Oppføringer for eksport er vanligvis finansposter eller merverdiavgiftsposter (mva.). Det er imidlertid noen ganger nødvendig med annen informasjon.

**Revisjonsfileksport** er en forhåndsinstallert utvidelse som gjør det mulig å eksportere forskjellige oppføringer basert på revisor- eller myndighetskrav. Uavhengig av formattypen eller oppføringene kan du bruke utvidelsens funksjonalitet til å kontrollere dataeksportprosessen. Funksjonaliteten har ikke et forhåndsinstallert filformat for eksport. Du må derfor enten installere en app som har et bestemt format (f.eks. SIE, SAF-T eller FAC), eller utvikle din egen.

> [!NOTE]
> Du kan for øyeblikket velge formatet SIE (Sverige), FEC (Frankrike) eller SAF-T som en tilleggsapp. Partnere kan også utvikle et egendefinert format. Antallet tilgjengelige formater økes over tid.

## Konfigurer revisjonsfileksport

1. Velg søkeknappen ![Forstørrelsesglass som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Oppsett av revisjonsfileksport** og velg deretter relatert kobling.
2. Følg denne fremgangsmåten på siden **Oppsett av revisjonsfileksport**:

    1. På hurtigfanen **Generelt** i feltet **Eksportformatkode for revisjonsfil** angir du koden for standard eksportformat for revisjonsfil. Bare formater som ble aktivert da et bestemt filformat ble installert fra Funksjonsstyring, og de som ble lagt til som egendefinert format, er tilgjengelige.
    2. På hurtigfanen **Datakvalitet** merker du av for **Kontroller selskapsopplysninger** for å bli varslet om selskapsopplysningsfelter som ikke er definert riktig.
    3. Merk av for **Kontroller kunde** for å bli varslet om felter som ikke er konfigurert riktig for bestemte kunder.
    4. Merk av for **Kontroller leverandør** for å bli varslet om felter som ikke er konfigurert riktig for bestemte leverandører.
    5. Merk av for **Kontroller bankkonto** for å bli varslet om felter som ikke er konfigurert riktig for bestemte bankkontoer.
    6. Merk av for **Kontroll postnummer** for å bli varslet om et postnummer som ikke er definert riktig.
    7. Merk av for **Kontroller adresse** for å bli varslet når en adresse ikke er definert riktig.
    8. I feltet **Standard postnummer** angir du postnummeret som skal brukes hvis det ikke er angitt noe postnummer på kunde- eller leverandørkortet.

3. Velg søkeknappen ![Forstørrelsesglass som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Oppsett av eksportformat for revisjonsfil** og velg deretter relatert kobling.
4. Følg denne fremgangsmåten på siden **Oppsett av eksportformat for revisjonsfil**:

    1. Velg eksportformatet for revisjonsfil du vil konfigurere. Bare formater som ble aktivert da et bestemt filformat ble installert fra Funksjonsstyring, og de som ble lagt til som egendefinert format, er tilgjengelige.
    2. I feltet **Navn på revisjonsfil** angir du standard filnavn eller filnavnmalen for revisjonsfilen du vil eksportere.
    3. Merk av for **Arkiver til ZIP** for å pakke eksporterte filer automatisk.

## Angi finanskontotildelingen for revisjonsfileksport

De fleste formater som kreves av myndighetene for finanskontoer, krever en bestemt standard kontoplan. Etter at du har konfigurert finanskontoene, baseres derfor den eksporterte filen på tildelingene. Du kan bruke flere tildelinger i systemet.

Følg denne fremgangsmåten for å angi finanskontotildelingen for revisjonsfileksport.

1. Velg søkeknappen ![Forstørrelsesglass som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finanskontotildeling** og velg deretter relatert kobling.
2. På siden **Finanstildeling** velger **Opprett** for å opprette en tildeling.
3. I feltet **Kode** angir du tildelingskoden som representerer rapporteringsperioden.
4. I feltet **Standard kontotype** velger du typen standard finanskontoer.
5. I feltet **Eksportformat for revisjonsfil** angir du eksportformatet for revisjonsfilen som standard finanskontoer er koblet til.
6. I feltet **Periodetype** angir systemet en regnskapsperiode eller en egendefinert periodetype som har fleksibel startdato og -tidspunkt basert på hva du har valgt. Hvis du velger en bestemt regnskapsperiode, blir feltet satt til **Regnskapsperiode**. Hvis ikke blir den satt til **Dataområde**.
7. I feltet **Regnskapsperiode** angir du startdatoen for regnskapsperioden som skal brukes som rapporteringsperiode, hvis du vil at de skal være like.
8. Hvis du angir feltet **Regnskapsperiode**, angis feltene **Startdato** og **Sluttdato** automatisk på bakgrunn av den angitte perioden. Hvis ikke kan du manuelt angi start- og sluttdato for rapporteringen.
9. Hvis du allerede har lagt til en standard kontoplan, følger du denne fremgangsmåten:

    1. I feltet **Standard kontokategorinr.** angir du kategorien for standardkonto eller grupperingskode som brukes til tildeling.
    2. I feltet **Standard kontonr.** angir du kategorien for standard kontokode eller grupperingskode som brukes til tildeling.

10. Merk av for **Ta med inngående saldo** for å vurdere den inngående saldoen for finanskontoen av typen **saldokonto** i stedet for bevegelsen i rapporteringsperioden.
11. Hvis du vil tildelingen, gjør du følgende:

    1. Hvis du vil generere linjer på siden **Finanskontotildeling** basert på en eksisterende kontoplan, velger du **Start kilde for tildeling**. Hvis du vil kopiere finanskontotildelingen fra en annen tildelingskode, velger du **Kopier fra en annen tildeling**. Når du er ferdig med å opprette linjer, er alle finanskontoer som har bokførte poster, merket med grønt.
    2. Hvis du vil merke bare finanskontoer som har oppføringer, velger du **Oppdater tilgjengelighet for finanspost**. Hvis alternativet **Ta med inngående saldo** er aktivert, vurderes alle bokførte finansposter for beregning. Ellers vurderes bare finansposter i rapporteringsperioden.

## Eksporter revisjonsfilen

1. Velg søkeknappen ![Forstørrelsesglass som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Eksportdokumenter for revisjonsfil** og velg deretter relatert kobling.
2. Velg **Opprett** på siden **Eksportdokumenter for revisjonsfil**.
3. Følg denne Fremgangs måten på hurtigfanen **Generelt**:

    1. Velg formatet som brukes til å eksportere revisjonsfilen, i feltet **Eksportformat for revisjonsfil**.
    2. I feltet **Kode for finanskontotildeling** velger du koden for finanskontotildelingen for rapporteringsperioden.
    3. Merk av for **Del etter måned** hvis du kan generere flere revisjonsfiler per måned.
    4. Merk av for **Del etter dato** hvis du kan generere flere revisjonsfiler per dag.
    5. Skriv inn merknaden du vil ha med i hodet på revisjonsfilen, i feltet **Hodemerknad**.
    6. I feltet **Kontakt** angir du kontakten som eksporteres til hodet til revisjonsfilen.
    7. Merk av for **Opprett flere ZIP-filer** for å generere flere ZIP-filer.

        > [!IMPORTANT]
        > Merk bare av for dette alternativet hvis du tidligere har installert noen av formatappene eller opprettet en egen app. Hvis du installerer et eller flere av de spesifikke formatene, legges det sannsynlig til felter og funksjoner i funksjonaliteten **Revisjonsfileksport**, basert på formatkravene.

4. Følg denne Fremgangs måten på hurtigfanen **Behandling**:

    1. Merk av for **Parallell behandling** hvis du vil at revisjonsfilgenerering skal bli behandlet av parallelle bakgrunnsjobber. Fjern avmerkingen for å eksportere data i nåværende økt.
    2. Hvis du merket av for **Parallell behandling** i feltet **Maks antall prosjekter**, angir du det maksimale antall bakgrunnsprosjekter som kan kjøres samtidig.
    3. I feltet **Tidligste startdato/-klokkeslett** angir du tidligste dato og klokkeslett for når bakgrunnsprosjektet skal kjøres. Hvis du kjører prosessen ved å velge **Start**, kan du spore statusen i hurtigfanene **Behandling** og **Linjer**.

5. Når du er ferdig, velger du **Last ned som fil** for å laste ned revisjonsfilen for den valgte linjen.

> [!IMPORTANT]
> Hvis du har flere poster som skal eksporteres, anbefaler vi ikke at du eksporterer dem i nåværende økt på grunn av mulige ytelsesproblemer. Vi anbefaler i stedet å bruke parallell behandling på fridager eller utenom arbeidstid.

## Se også
[Økonomistyring](finance.md)  
[Forstå Finans og kontoplanen](finance-general-ledger.md)  
[Arbeid med dimensjoner](finance-dimensions.md)  
[Arbeid med Business Central](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
