---
title: Forberede kundedatamigrering med maler | Microsoft Docs
description: Finn ut hvordan du bruker konfigurasjonsmaler til å strukturere eksisterende kundedata før du overfører dataene til det nye selskapet i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8f4bd2978652366ecd18109377f4ebeeebfbb4a3
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922345"
---
# <a name="prepare-to-migrate-customer-data-with-templates"></a>Klargjøre for å flytte kundedata med maler

Når du har importert og brukt oppsettsdata i den nye databasen, kan du begynne å overføre kundens eksisterende hoveddata, for eksempel vare- og kundenumre og navn. Hvis du vil forsikre deg om at disse dataene opprettes raskt og nøyaktig i det nye selskapet, bør du bruke maler til å strukturere dataene.  

Du oppretter vanligvis datamaler for følgende hoveddatatabeller:  

- **Kontakt**  
- **Kunde**  
- **Vare**  
- **Leverandør**  

Du kan imidlertid opprette en malstruktur og bruke den på en hvilken som helst tabell i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!TIP]  
> Du kan også bruke datamaler for daglige operasjoner for å opprette nye poster som er basert på maler. Disse datamalene fungerer bare for de støttede hoveddatatabellene. Hvis du vil ha mer informasjon, kan du for eksempel se [Registrere nye varer](inventory-how-register-new-items.md).  

Når du importerer kundedata (for eksempel for varer) fra en fil, vil dataene i de obligatoriske feltene som du har angitt, hentes fra den tilknyttede datamalen. Når du oppretter en ny vare, fyller du bare ut generell informasjon som varenavn, beskrivelse og pris og samler deretter inn resten av dataene for de obligatoriske feltene fra en valgt datamal.

Når du oppretter en ny hoveddatapost, for eksempel et kundekort, er noen av feltene obligatoriske og må fylles ut. Du kan gruppere de fleste obligatoriske felt, for eksempel bokføringgrupper og betalingsbetingelser, for å opprette hoveddataposter enklere og mer stabil. Du kan for eksempel gruppere obligatoriske felt for tabell 18, **Kunde**, som typene **Innland**, **Utland** eller **Eksporter**.

> [!NOTE]
> Felt av typen blob kan ikke eksporteres/importeres i Excel.

## <a name="to-select-a-data-template"></a>Velge en datamal

Når du velger en eksisterende datamal, må du vurdere om malene som du opprettet for det nye selskapet, er tilstrekkelig for kunden. Se gjennom de angitte feltene og verdiene for å avgjøre hvilke maler som passer for et nytt selskap.  

> [!TIP]  
> Du kan også bruke datamaler til raskt å opprette nye poster. Bruk dem til å opprette data raskere og mer nøyaktig. Hvis du vil ha mer informasjon, kan du se [Registrere nye varer](inventory-how-register-new-items.md).

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konfigurasjonsmaler**, og velg deretter den relaterte koblingen.  
2. På siden **Konfigurasjonsmaler** velger du en datamal fra oversikten, og velger deretter **Rediger**-handlingen.  

Hvis standardmalene ikke oppfyller dine behov, kan du opprette nye maler eller legge til felt i en eksisterende mal. Hvis standardmalene er tilstrekkelige, kan du bruke dem til å opprette poster basert på maler for hoveddata.

## <a name="to-create-a-new-data-template"></a>Opprette en ny datamal

Du kan opprette en ny datamal hvis standardmalene ikke oppfyller behovene til det nye selskapet.  

> [!TIP]
> Hvis du oppretter flere, det kan være praktisk å bruke en navnekonvensjon for **Kode**-feltet.

Hver enkelt mal består av et hode og en linje for hvert felt som skal tas med i malen. Når du oppretter en mal, kan du angi hvilke felt som alltid skal gjelde for data av en bestemt type. Du kan for eksempel opprette ulike kundemaler som du vil bruke for ulike kundetyper. Når du oppretter kunden ved hjelp av en mal, kan du bruke maldata for å fylle ut bestemte felt på forhånd.

### <a name="to-copy-an-existing-data-template"></a>Kopiere en eksisterende datamal

Du kan raskt opprette en ny datamal ved å kopiere informasjon fra en eksisterende datamal, som du deretter kan redigere.

1. Åpne siden **Konfigurasjonsmaler**.
2. Velg handlingen **Ny**.
3. Fyll ut **Kode**-feltet.
4. Velg handlingen **Kopier konfigurasjonsmal**.
5. På siden **Konfigurasjonsmaler** velger du en eksisterende mal for kopiering, og velger deretter **OK**-knappen.

Tabell-ID-en, tabellnavnet og linjene i den eksisterende datamalen settes inn i den nye malen.

### <a name="to-create-a-data-template-header-manually"></a>Opprette et datamalhode manuelt

1. Åpne siden **Konfigurasjonsmaler**.
2. Velg handlingen **Ny**.
3. Fyll ut **Kode**-feltet.
4. Angi tabellen som denne malen skal brukes på, i **Tabell-ID**-feltet. **Tabellnavn**-feltet fylles automatisk ut når **Tabell-ID**-feltet er angitt.

### <a name="to-create-a-data-template-line-manually"></a>Opprette en datamallinje manuelt

1. På den første linjen velger du **Feltnavn**-feltet. **Feltoversikt**-siden viser listen over felt i tabellen.
2. Velg et felt og deretter **OK**-knappen. Feltet **Felttekst** er fylt ut med feltnavnet.
3. Angi en aktuell verdi i **Standardverdi**-feltet. I noen tilfeller vil du kanskje bruke en verdi som ikke finnes i databasen. I dette tilfellet kan du merke av for **Hopp over relasjonskontroll**, slik at du kan bruke data uten å få feil.

    > [!TIP]  
    > Siden **Standardverdi**-feltet ikke har et oppslag for tilsvarende [!INCLUDE[d365fin](includes/d365fin_md.md)]-feltalternativer, kopierer du verdien du vil bruke fra den tilknyttede siden og limer den inn i malen.

4. Merk av for **Obligatorisk** hvis brukere må fylle ut det aktuelle feltet.

    > [!NOTE]
    > Avmerkingsboksen er kun veiledende. Ingen forretningslogikk fremtvinges. Brukere kan for eksempel ikke bokføre en faktura hvis det ikke er definert bokføringsgrupper. Du kan merke av for **Obligatorisk** for disse feltene slik at brukeren fyller dem ut, og dermed unngå en bokføringsfeil senere.
5. Angi informasjon om feltet etter behov i **Referanse**-feltet.
6. Velg **OK**.

## <a name="to-export-to-a-template-in-excel"></a>Slik eksporterer du til en mal i Excel:

Du kan opprette en Excel-arbeidsbok som skal fungere som en mal som er basert på strukturen i en eksisterende databasetabell. Deretter kan du bruke malen til å samle kundedata i et konsekvent format for senere import til [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konfigurasjonsforslag**, og velg deretter den relaterte koblingen.
2. Legg til en tabell i listen, eller velg en eksisterende tabell. Hvis du vil ha mer informasjon, se [Behandle selskapskonfigurasjon i et forslag](admin-how-to-manage-company-configuration-in-a-worksheet.md).
3. Velg handlingen **Vis felt** for å definere feltene fra tabellen som du vil inkludere i malen.
4. Velg **Eksporter til mal**-handlingen.
5. Gi Excel-filen navn og lagre den. Excel-arbeidsboken åpnes automatisk.

Du kan nå angi kundedata i Excel-regnearket. Hvis du har eksportert flere tabeller, er hver tabell på sitt et eget regneark. Lagre arbeidsboken før du fortsetter med neste fremgangsmåte.

> [!NOTE]  
> Følgende feil kan oppstå hvis du kjører en engelsk versjon av Excel når de regionale innstillingene er konfigurert for et annet språk enn engelsk: Gammelt format eller ugyldig typebibliotek. Når du skal rette denne feilen, må du passe på at språkpakken for andre språk enn engelsk er installert.

## <a name="to-import-from-a-template-in-excel"></a>Slik importerer du fra en mal i Excel:

1. På siden **Konfigurasjonsforslag** velger du **Importer fra mal**-handlingen.
2. Gå til malforslaget du har opprettet, og velg deretter **Åpne**-handlingen.
3. Hvis du vil legge til samlede kundedata i databasen, kan du velge **Bruk data**-handlingen.

Når du bruker data fra en Excel-mal i en tabell som også har en tilknyttet konfigurasjonsmal i konfigurasjonspakken, vil standard feltverdier fra konfigurasjonsmalen også tas i bruk.

Enhver post der dataene er brukt på denne måten, er fullført fordi den består av data som er angitt av en bruker i Excel, i tillegg til standardverdiene som er angitt av konfigurasjonsmalen.

> [!NOTE]
> Hvis dataene i tabellene i konfigurasjonspakken inneholder datoer, for eksempel bokføringsdatoer på fakturaer, tas datoene med i tidssonen som er angitt i [!INCLUDE[d365fin](includes/d365fin_md.md)]. 

## <a name="to-create-a-record-from-a-configuration-template"></a>Slik oppretter du en post fra en konfigurasjonsmal:

Du kan bruke strukturen i data som datamalene inneholder, til å enkeltvis konvertere informasjonen til poster i databasen. Hvis du vil gjøre dette, bruker du funksjonen **Opprett forekomst**. Dette er en miniatyrversjon av dataoverføringsprosessen og kan være nyttig for prototypeutvikling eller håndtering av mindre dataopprettingsoppgaver.  

Trinnene nedenfor viser hvordan du oppretter et varekort fra en varedatamal. Du kan opprette en post fra en hvilken som helst datamal ved å bruke den samme fremgangsmåten.  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konfigurasjonsmaler**, og velg deretter den relaterte koblingen.  
2. Velg **Vare**-malen, og velg deretter handlingen **Rediger**. Hvis du vil ha mer informasjon, se [Slik oppretter du en datamal](admin-use-templates-to-prepare-customer-data-for-migration.md#to-create-a-new-data-template).
3. Velg handlingen **Opprett forekomst**. Et varekort opprettes.  
4. Velg **OK**.  
5. For å gå gjennom det nye varekortet velger du ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angir **Varer**, og velger deretter den relaterte koblingen.  
6. Åpne det nye varekortet.  
7. Utvid ulike hurtigfaner, og kontroller at informasjonen er opprettet på riktig måte på dem.  

## <a name="to-use-a-configuration-template-on-a-record"></a>Slik bruker du en konfigurasjonsmal på en post:

Du kan bruke en datamal for en hvilken som helst post i [!INCLUDE[d365fin](includes/d365fin_md.md)] og bruke denne teknikken til å endre eller modifisere en post. Når du gjør dette, skriver du imidlertid over eksisterende verdier i posten med de som er i malen. Du bør derfor være forsiktig når du bruker en mal i eksisterende poster.

> [!WARNING]  
> **Bruk mal**-funksjonen overskriver eksisterende data i en post. Hvis denne funksjonen brukes i flytting av hoveddata, overskriver den de importerte dataene når du oppretter poster.

Følgende fremgangsmåte er basert på et nytt kundekort.  

1. Opprett en kunde. Hvis du vil ha mer informasjon, kan du se [Registrere nye kunder](sales-how-register-new-customers.md).
2. På siden **Kundekort** velger du handlingen **Bruk mal**.  
3. På siden **Kundemaler** velger du en av malene, og deretter velger du **OK**-knappen.  

Standardverdiene fra den valgte kundemalen settes inn på kundekortet.

## <a name="see-also"></a>Se også

[Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administrasjon](admin-setup-and-administration.md)  
[Registrere nye kunder](sales-how-register-new-customers.md)  
