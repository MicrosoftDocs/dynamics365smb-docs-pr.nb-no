---
title: Klargjøre en konfigurasjonspakke | Microsoft-dokumentasjon
description: Finn ut nå hvordan du konfigurerer en RapidStart-konfigurasjonspakke som kan hjelpe deg med å sette opp nye selskaper basert på eksisterende data.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/06/2020
ms.author: sgroespe
ms.openlocfilehash: f2550f9df9e2eda87e2f5b3de9f6be00d4758b7a
ms.sourcegitcommit: 7d05fc049d81cae9b2b711101cdaea037b7ba61f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2020
ms.locfileid: "3535975"
---
# <a name="prepare-a-configuration-package"></a>Klargjøre en konfigurasjonspakke

Når du konfigurerer et nytt selskap basert på en konfigurasjonspakke, gjenkjennes og behandles tabellrelasjoner. Dataene importeres og brukes i riktig rekkefølge. Dimensjonstabeller importeres også hvis de er inkludert i konfigurasjonspakken. Hvis du vil ha mer informasjon, kan du se [Slik importerer du kundedata](admin-migrate-customer-data.md#to-import-customer-data).  

For å hjelpe kunden med å bruke konfigurasjonspakken kan du legge til et spørreskjema eller et sett av spørreskjemaer i pakken. Spørreskjemaet kan hjelpe kunden med å forstå de forskjellige oppsettsalternativene. Spørreskjemaer opprettes vanligvis for hovedoppsettstabellene når kunder vil ha ytterligere veiledning om hvordan de velger en riktig innstilling. Hvis du vil ha mer informasjon, kan du se [Samle oppsettsverdier for kunde](admin-gather-customer-setup-values.md).

## <a name="before-you-create-a-configuration-package"></a>Før du oppretter en konfigurasjonspakke

Det er noen ting du bør vurdere før du oppretter en konfigurasjonspakke, fordi de vil påvirke deg eller kundens mulighet til å importere den.  

### <a name="tables-that-contain-posted-entries"></a>Tabeller som inneholder bokførte poster

Du kan ikke importere data til tabeller som inneholder bokførte poster, for eksempel tabellene for kunde-, leverandør- og vareposter, så du bør ikke ta med disse dataene i konfigurasjonspakken. Du kan legge til oppføringer i disse tabellene når du har importert konfigurasjonspakken ved hjelp av journaler for å bokføre postene. Hvis du vil ha mer informasjon, kan du se [Bokføre dokumenter og kladder](ui-post-documents-journals.md).

### <a name="licensing"></a>Lisensiering

Lisensen må inkludere tabellene du oppdaterer. Hvis du er usikker, kan siden **Konfigurasjonsforslag** hjelpe. Hvis lisensen inkluderer tabellen, er det merket av for **Lisensiert tabell**.  

### <a name="permissions"></a>Tillatelser

Prosessen med å opprette og importere en konfigurasjonspakke omfatter følgende effektive tillatelser for alle tabellene i pakken:  

- Brukeren som eksporterer data for konfigurasjonspakken, må ha effektive **Lese**-tillatelser.
- Brukeren som importerer data for konfigurasjonspakken, må ha effektive **Sett inn** og **Endre**-tillatelser.

### <a name="database-schema"></a>Databaseskjema

Når du eksportere og importere konfigurasjonspakker mellom to firmadatabaser, må databasene har samme skjema for å sikre at alle dataene overføres. Dette betyr at databasene bør ha den samme tabell- og feltstruktur, der tabellene har samme primærnøkler og felt har samme IDer og datatyper.  

Du kan importere en konfigurasjonspakke som har blitt eksportert fra en database, som har et annet skjema enn måldatabasen. Tabeller eller felt i konfigurasjonpakken som ikke finnes i måldatabasen, blir imidlertid ikke importert. Tabeller med forskjellige primærnøkler og felt med ulike datatyper, blir heller ikke importert. Hvis konfigurasjonspakken inneholder en tabell, for eksempel **50000-kunden**, som har primærnøkkelen **Kode20**, og databasen du importerer pakken til, som inneholder tabellen **Bankkonto for 50000-kunde**, som har primærnøkkelen **Kode20 + Kode20**, importeres ikke dataene.  

## <a name="to-create-a-configuration-package"></a>Slik oppretter du en konfigurasjonspakke:

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konfigurasjonspakker**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. På hurtigfanen **Generelt** fyller du ut feltene riktig. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Hvis du vil utelate konfigurasjonsspørreskjemaene, konfigurasjonsmalene og konfigurasjonforslagstabellene fra pakken, merker du av for **Utelat konfigurasjonstabeller**. Ellers vil disse tabellene automatisk legges til i listen over pakketabeller når du eksporterer pakken.  
5. Velg handlingen **Hent tabeller**. Kjørselssiden **Hent pakketabeller** åpnes.  
6. Velg feltet **Velg tabeller**. Siden **Konfig. valg** åpnes.  
7. Velg handlingen **Merk alt** for å legge til alle tabeller i pakken, eller du merker avmerkingsboksen **Valgt** for hver tabell i listen som du vil legge til.
8. Velg **OK**-knappen. Antall tabeller du har valgt, er angitt i feltet **Velg tabeller**. Angi flere alternativer, og velg deretter **OK**-knappen. [!INCLUDE[d365fin](includes/d365fin_md.md)] tabeller legges til i linjene på **Konfig.pakke**-siden.  

    > [!NOTE]  
    >  Du kan også gjøre dette i konfigurasjonsforslaget. Velg tabellene du vil inkludere i pakken, og velg deretter handlingen **Tilordne pakke**.

9. Hvis du vil velge feltene du vil inkludere fra en tabell, merker du tabellen og velger deretter handlingen **Felt** i fanen **Linjer**.
Angi hvilke felt som er inkludert i pakken. Alle feltene er inkludert som standard.

    - Hvis du bare vil velge felt du vil inkludere, velger du handlingen **Fjern inkludert**. Hvis du vil legge til alle felt, velger du handlingen **Sett inkludert**.  
    - Hvis du vil angi at feltdataene ikke skal valideres, fjerner du merket for **Valider felt** for feltet.  

10. Finn ut om du har introdusert mulige feil ved å velge handlingen **Valider pakke**. Dette kan skje når du ikke tar med tabeller som konfigurasjonen avhenger av.  
11. Velg **OK**-knappen.  

Når du har fornyet listen over felt som skal inkluderes fra en tabell, kan du se resultatene i Excel.  

### <a name="to-filter-and-review-your-dataset"></a>Slik filtrerer du og ser gjennom datasett:

1. Når du skal filtrere et bestemt sett med poster som skal tas med i pakken, velger du handlingen **Filtre** og angir deretter filterverdiene du vil bruke i fanen **Linjer**.  
2. På pakkekortet, i fanen **Linjer**, velger du handlingen **Eksporter til Excel**.  
3. Bekreft meldingene som gjør det mulig å eksportere data til Excel. Den navngitte XLSX-filen åpnes. Se gjennom poster som er eksportert.  
4. Lukk Excel.  

### <a name="to-include-a-template-for-application-to-a-table"></a>Slik inkluderer du en mal for bruk i en tabell:

For enkelte tabeller, for eksempel en tabell som inneholder hoveddata, kan du angi en mal som skal brukes på dataene. Malen kan inneholde de obligatoriske feltene som du vil bruke på alle hoveddata, og som du ikke vil skal variere. Du kan for eksempel opprette en mal som kan brukes med kundedata. Malen kan inneholde alle nødvendige felt, som gjør at import av standardisert informasjon blir konsekvent. Informasjonen som ikke kan standardiseres, for eksempel kundenavn, behandles når du importerer kundedata. Hvis du vil ha mer informasjon, kan du se [Klargjøre for å flytte kundedata med maler](admin-use-templates-to-prepare-customer-data-for-migration.md).  

1. Velg en tabell, og velg deretter **Datamal**-feltet på siden **Konfigurer pakkekort**. Det vises en liste over maler i tabellen som vises.
2. Velg en mal og deretter **OK**.  

Når pakken er fullført, følger du prosedyren nedenfor for å lagre pakken som en fil. Deretter kan du gi pakken til en kunde eller partner for bruk.

### <a name="to-save-and-export-a-configuration-package"></a>Lagre og eksportere en konfigurasjonspakke

- På siden **Konfigurer pakkekort** velger du handlingen **Eksporter pakke**.  

Pakken opprettes i en .rapidstart-fil, som leverer innholdet i pakken i et komprimert format. Konfigurasjonspørreskjemaer, konfigurasjonsmaler og konfigurasjonsforslaget legges til i pakken automatisk med mindre du spesifikt bestemmer deg for å utelukke dem.  

Du kan lagre filen med et navn som gir mening for deg, men du kan ikke endre filtypen for filen. Den må være .rapidstart.  

### <a name="to-copy-a-configuration-package"></a>Slik konfigurerer du en konfigurasjonspakke:

Når du har opprettet en pakke som dekker de fleste behovene, kan du bruke den som grunnlag for å opprette lignende pakker. Dette kan forkorte implementeringstiden og forbedrer gjentakelse for RapidStart Services.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konfigurasjonspakker**, og velg deretter den relaterte koblingen.  
2. Velg en pakke fra listen, og velg deretter handlingen **Kopier pakke**.  
3. Angi en kode for den nye pakken i feltet **Ny pakkekode**.  
4. Merk av for **Kopier Data** hvis du også vil kopiere databasedata fra den eksisterende pakken.  
5. Velg **OK**-knappen.

## <a name="to-customize-a-configuration-package"></a>Tilpasse en konfigurasjonspakke

Bruk konfigurasjonsforslaget til å samle inn og kategorisere informasjon du vil bruke til å konfigurere et nytt selskap, og til å ordne tabeller på en logisk måte. Formatering i forslaget er basert på et enkelt hierarki: områder inneholder grupper, som i sin tur inneholder tabeller. Områder og grupper er valgfrie, men nødvendige for å vise en oversikt over konfigurasjonsprosessen i rollesenteret for RapidStart Services.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konfigurasjonsforslag**, og velg deretter den relaterte koblingen.  
2. Velg **Område** i **Linjetype**-feltet. Skriv inn et beskrivende navn i **Navn**-feltet.  
3. Velg **Gruppe** i **Linjetype**-feltet. Skriv inn et beskrivende navn i **Navn**-feltet.  
4. Velg **Tabell** i **Linjetype**-feltet. Velg tabellen du vil ta med i forslaget, i **Tabell-ID**-feltet.  

Nå kan du tilordne tabeller til spesifikk konfigurasjonspakker som du har opprettet eller planlegger å opprette. Hvis du vil ha mer informasjon, se [Slik tilordner du en tabell til en konfigurasjonspakke](admin-how-to-prepare-a-configuration-package.md#to-assign-a-table-to-a-configuration-package).

## <a name="to-work-with-promoted-tables"></a>Slik arbeider du med forfremmede tabeller:

1. Merk av for **Forfremmet tabell** for å indikere en tabell som ofte blir brukt av en vanlig kunde under oppsettprosessen , for eksempel **Finanskonto**-tabellen. Når en tabell har denne angivelsen, kan en kunde enkelt filtrere forslaget for å vise bare listen over forfremmede tabeller som krever oppmerksomhet.  
2. Hvis du vil vise den filtrerte visningen, velger du handlingen **Bare forfremmet**. Listen over tabeller inneholder bare tabeller som har avmerkingsboksen merket.  

## <a name="to-assign-a-table-to-a-configuration-package"></a>Slik tilordner du en tabell til en konfigurasjonspakke:

Når du har definert tabellene du vil skal behandles som en del av konfigurasjonen, kan du enkelt tilordne tabellene til konfigurasjonspakker. Du kan tilordne en tabell til bare én pakke. I fremgangsmåten nedenfor tilordner du pakken i konfigurasjonsforslaget.  

> [!NOTE]  
> Du kan også opprette en pakke direkte, og legge til tabeller i den. Hvis du vil ha mer informasjon, se [Slik oppretter du en konfigurasjonspakke](admin-how-to-prepare-a-configuration-package.md#to-create-a-configuration-package).

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konfigurasjonsforslag**, og velg deretter den relaterte koblingen.
2. Velg en linje eller gruppe med linjer i konfigurasjonsforslaget som du vil tilordne til konfigurasjonspakke, og velg deretter handlingen **Tilordne pakke**.  
3. Velg en pakke fra listen, eller velg handlingen **Ny** for å opprette en ny pakke, og velg deretter **OK**.  

    Hvis en tabell ikke allerede er inkludert i pakken, legges den til. Pakkekodefeltet på forslagslinjen fylles ut med koden for pakken som tabellen er tilordnet.  
4. Hvis du velger en eksisterende pakke, kan du se hvor mange tabeller som allerede er i pakken, ved å se gjennom informasjonen i **Antall tabeller**-feltet.

## <a name="to-review-or-customize-existing-database-data"></a>Se gjennom eller tilpasse eksisterende databasedata

Når du oppretter en konfigurasjonpakke for en løsning, kan du vise og tilpasse de tilgjengelige databasedataene etter kundens behov. Databasetabellen må ha en tilknyttet side.  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konfigurasjonsforslag**, og velg deretter den relaterte koblingen.
2. Finn tabellene i konfigurasjonsforslaget som inneholder dataene du vil vise eller tilpasse.  

    > [!NOTE]  
    >  Kontroller at hver tabell er tilordnet en side-ID. For standard [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller, fylles denne verdien ut automatisk. For egendefinerte tabeller må du angi ID-en.

3. Velg handlingen **Databasedata**. Siden for den relaterte siden åpnes.
4. Se gjennom informasjonen som er tilgjengelig. Endre den etter behov ved å slette poster som ikke er relevante eller ved å legge til nye.  

## <a name="to-copy-data-from-a-test-environment-to-a-production-environment"></a>Kopiere data fra et testmiljø til et produksjonsmiljø

Når du har sett gjennom og testet all oppsettsinformasjon, kan du fortsette med å kopiere dataene til ditt produksjonsmiljø. Du oppretter et nytt selskap i samme database.

1. Åpne og start det nye selskapet.  
2. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konfigurasjonsforslag**, og velg deretter den relaterte koblingen.  
3. Velg handlingen **Kopier data fra selskap**.  
4. Velg **Kopier fra**-feltet på siden **Kopier selskapsdata**. **Selskaper**-siden åpnes.  
5. Velg selskapet du vil kopiere data fra, og velg deretter **OK**. En liste over tabellene som er valgt i konfigurasjonsforslaget, åpnes. Det er bare tabeller som inneholder poster som er inkludert i denne listen.
6. Velg tabellene du vil kopiere data fra, og velg deretter handlingen **Kopier Data**. Klikk **OK** på siden **Kopier selskapsdata**.  

## <a name="see-also"></a>Se også

[Klargjøre for å flytte kundedata med maler](admin-use-templates-to-prepare-customer-data-for-migration.md)  
[Samle oppsettsverdier for kunde](admin-gather-customer-setup-values.md)  
[Definere selskapskonfigurasjon](admin-set-up-company-configuration.md)  
[Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administrasjon](admin-setup-and-administration.md)  
