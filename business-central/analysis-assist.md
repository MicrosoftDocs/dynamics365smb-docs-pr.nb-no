---
title: Analyser data i lister ved hjelp av Copilot (forhåndsversjon)
description: Lær hvordan du bruker Copilot i Business Central til å analysere data.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/14/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.search.form: '456, 457, 458, 459, 460, 461, 16, 22, 25, 26, 27, 31, 143, 144, 9300, 9301, 9303, 9304, 9305, 9306, 9307, 9309, 9310, 9311'
---
# <a name="analyze-data-in-lists-with-help-from-copilot-preview"></a>Analyser data i lister ved hjelp av Copilot (forhåndsversjon)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Denne artikkelen forklarer hvordan du bruker *analysehjelp* til å analysere data på listesider.

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="about-analysis-assist"></a>Om analysehjelp

Analysehjelp er en Copilot for [analysemodusen](analysis-mode.md) på listesider i Business Central. Analysemodusen gir en interaktiv og allsidig måte å beregne, summere og undersøke data på. Hvis du vil analysere data i analysemodus, oppretter du en *analysefane* der du transformerer dataene for å vise de ønskede samlingene og sammendragene. Du kan for eksempel ordne felter i rader og kolonner, angi filtre, sortere kolonner og pivotere felter. Med analysehjelp oppnår du, i stedet for å gjøre denne oppgaven manuelt, mye av det samme – eller hvertfall som en start – ved å bruke ord. Ved å uttrykke strukturen du vil bruke på naturlig språk, for eksempel «sortere etter antall fra minste til største» eller «vis gjennomsnittskostnad per kategori», bruker analysehjelp kunstig intelligens til å generere et foreslått oppsett i en analysefane.


<!-- 

 However, the data analysis mode requires some understanding of how to structure fields to meet the desired aggregations and summarizations. It requires you to move fields around to the appropriate areas within analysis mode pane which data rows and columns to display, specify filters, sorting, grouping, pivoting and totals. Analysis assist minimizes these requirments by enabling you to express the desired layout in words. , like "group which data rows and columns to display, specify filters, sorting, grouping, pivoting and totals
--> 
## <a name="prerequisites"></a>Forutsetninger

- Analysehjelpfunksjonen er aktivert, og du får tillatelse til å bruke den. Denne oppgaven utføres vanligvis av en administrator. [Finn ut mer om å konfigurere Copilot- og KI-funksjoner](enable-ai.md).
- Visningsspråket i Business Central er satt til et av følgende nasjonale innstillinger på engelsk: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en-ZA. [Finn ut mer om hvordan du endrer språket](ui-change-basic-settings.md#language).
- Business Central-miljøet er i alle land/områder unntatt Canada (denne funksjonen er ennå ikke tilgjengelig i Canada).

<!--
> [!NOTE]
> You may notice some list pages that don't include the **Analyze** switch for changing to the analysis mode. The reason is that developers can disable analysis mode on specific pages by using the [AnalysisModeEnabled property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-analysismodeenabled-property) in AL.-->

## <a name="get-started"></a>Kom i gang

1. Åpne listesiden som du vil analysere.

   Hvis du for eksempel vil arbeide med **Varer**-siden, velger du ikonet ![Forstørrelsesglass som åpner funksjonen Fortell meg.](media/ui-search/search_small.png) og (<kbd>Alt</kbd>+<kbd>Q</kbd>) angir *varer* og velger deretter den relaterte koblingen.

1. Du kan begynne å analysere data med Copilot direkte fra listesiden eller ved først å gå inn i analysemodus. Gjør et av følgende trinn for å komme i gang:

    - I handlingsraden øverst på siden velger du ![Viser kopilotikonet](media/copilot-icon.png) **Copilot** > **Analyser liste**.
    - I handlingsraden øverst på siden velger du ![Viser åpne analysemodus-ikonet](media/analysis-mode-icon.png) **Åpne analysemodus**, og velg ![Viser kopilotikonet](media/copilot-icon.png) **Copilot** > **Opprett ny analyse**.

1. I vinduet **Analyser** med Copilot skriver du inn en beskrivelse av oppsettet du vil bruke. Denne beskrivelsen er kjent som en *spørring*.

    ![Viser analysehjelpen Copilot](media/analysis-assist.png)

    > [!TIP]
    > Hvis du vil ha hjelp til å skrive en melding, velger du ![Viser vis spørring-ikonet](media/prompt-guide-icon.png) **Spørringsveiledning** og velger et av alternativene for å komme i gang. Teksten i hakeparentes `[ ]` vises bare som et eksempel og er ikke inkludert i Copilot-vinduet.

1. Velg **Generer**, og vent deretter mens Copilot genererer oppsettet i den nye analysefanen.
1. Se gjennom resultatene i den nye analysefanen.

   > [!NOTE]
   > Hvis du navigerer bort fra den nye analysefanen (f.eks. går til en annen analysefane eller -side) eller gjør oppsettendringer i fanen (f.eks. sorterer kolonner eller endrer innstillinger i fanene **Kolonner** og **Analysefiltre**), lagres den nye analysefanen automatisk, og Copilot lukkes.

1. Hvis du vil endre den genererte analysen, kan du gjøre et av trinnene:

   - Hvis du vil bygge videre på de forrige instruksjonene, skriver du inn informasjonen i boksen **Legg til flere detaljer om analysen**, og deretter velger du pilen ![Vis justeringspilen](media/analysis-assist-adjust-button.png) **Juster**. Copilot husker de tidligere instruksjonene og bruker dem til å gjøre justeringer.

   - Hvis du vil starte fra bunnen av ved å legge til nye instruksjoner, velger du ![Viser rediger spørring-blyantikonet](media/edit-pencil.png) **Rediger ledetekst:**, legger til detaljene i spørringen og velger deretter **Generer**.

1. Hvis du vil lagre analysefanen, velger du **Behold den**. Hvis du ikke vil lagre den, velger du **Forkast**.

## <a name="prompt-tips-and-examples"></a>Spørringstips og -eksempler

Det er viktig å lage effektive spørringer for Copilot for å få nøyaktige og relevante analyseforslag. Det finnes også måter å minimere tekst du legger til i spørringer for å gjøre det raskere når du skriver. Her er noen tips og retningslinjer etterfulgt av noen eksempler:

- Vær kortfattet og unngå lange setninger eller flere setninger.
- Kontroller at feltnavnene som brukes i spørringene, er omtrent nær de faktiske feltnavnene på siden.
- Bruk naturlig språk, og uttrykk datastrukturen du ønsker på en vennlig og samtalebasert måte.
- Bruk vanlige nøkkelord, uttrykk og begreper som brukes i dataanalyse, som `group by`, `sum`, `sort by` og så videre.
- Hvis det første svaret ikke er det du ønsker, kan du legge til oppfølgingsinstruksjoner eller omformulere den siste instruksjonen.
- Vanlige forkortelser er akseptable.
- Bokstavstørrelse er ikke viktig.

### <a name="examples"></a>Eksempler

Disse følgende spørringseksemplene bruker analysehjelp i **elementlisten**. Varesiden inneholder tre felter som kan summeres for analyse: **Antall på lager**, **Enhetskost**, **Salgspris**.

Spørring: `Show items by brand and unit of measure`

Denne spørringen prøver å vise totaler for alle felter som kan legges sammen, gruppert etter merke og feltet **Lagerenhet**. Men i dette tilfellet samsvarer ikke «merke» med noe feltnavn, så Copilot finner sannsynligvis ikke et samsvarende felt, så det ber deg om å omformulere spørringen og prøve på nytt.

Spørring: `Show items by type and uom`

Denne spørringen vise totaler for alle felter som kan legges sammen, gruppert etter feltet **Type** og feltet **Lagerenhet**. Men i stedet for å skrive ut «måleenhet», brukes forkortelsen `uom`.

Spørring: `Show total quantity per type per UoM`

Denne spørringen oppretter en pivottabell i feltet **Antall på lager** per **lagerenhet** per **type**.

## <a name="see-also"></a>Se også

[Vanlige spørsmål om ansvarlig kunstig intelligens for analysehjelp](faqs-analysis-assist.md)  
[Analyse av ad hoc-data](reports-adhoc-analysis.md)  
