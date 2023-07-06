---
title: Kom i gang med å opprette oppsett
description: 'Finn ut hvordan du lager oppsett for å tilpasse utseendet på en rapport når den vises, skrives ut eller lagres.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 03/23/2022
ms.author: jswymer
---
# <a name="get-started-creating-report-layouts"></a><a name="get-started-creating-report-layouts"></a><a name="get-started-creating-report-layouts"></a>Kom i gang med å opprette rapportoppsett

Business Central leveres med mange innebygde oppsett som du kan bruke i rapportene. Andre oppsett kan ha blitt lagt til som en del av andre utvidelser. Men det er også mulig å opprette dine egne rapporter enten fra grunnen av eller basert på et eksisterende oppsett.

> [!IMPORTANT]
> Du kan også bruke rapportoppsett til å legge til innhold i e-postmeldinger. Rapportoppsett kan for eksempel spare tid og bidra til å sikre konsekvens ved å bruke det samme innholdet på nytt når du kommuniserer med kundene. Hvis du vil bruke egendefinerte rapportoppsett med e-post, må filtypen for oppsettet være Word. Du kan ikke bruke filtypen RDLC. Hvis du vil ha mer informasjon, kan du se [Definer gjenbrukbare e-tekster og oppsett](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts). 

## <a name="overview"></a><a name="overview"></a><a name="overview"></a>Oversikt

Når du arbeider med rapportoppsett, hjelper det å tenke på oppsettet som en fil som er importert og tildelt en rapport. Uavhengig av type oppsett er måten du administrerer oppsett for Business Central på, den samme. Vanligvis arbeider du på siden **Rapportoppsett**. Hovedforskjellen er hvordan du utformer oppsettet, som gjøres ved hjelp av approgramvaren som er laget i utformingen, for eksempel Word, Excel eller SQL Server Report Builder.

Med dette konseptet i tankene. Det finnes hovedsakelig tre eller fire oppgaver involvert i konfigurasjonen av et oppsett i en rapport:

1. Angi typen oppsett.
2. Eksporter en kopi av et eksisterende oppsett for å bruke det som utgangspunkt.
3. Gjør endringer i oppsettsfilen i det aktuelle programmet.
4. Legg til den nye oppsettsfilen i rapporten.

> [!IMPORTANT]
> Du kan ikke endre eller erstatte et utvidelsesoppsett, som er et oppsett som kommer fra en utvidelse. Du kan bare endre eller erstatte brukerdefinerte oppsett. På siden **Rapportoppsett** kan du se om oppsett er et utvidelsesoppsett eller et brukerdefinert oppsett ved å se på kolonnen **Utvidelse**. Et utvidelsesoppsett vil vise informasjon om kildeutvidelsen i kolonnen. **Utvidelse**-kolonnen vil være tom for et brukerdefinert oppsett.
>
> Hvis du vil vite mer om forskjellen mellom utvidelsesoppsett og brukerdefinerte oppsett, kan du se [Oppsettskilde](ui-manage-report-layouts.md#layout-sources).

## <a name="get-started"></a><a name="get-started"></a><a name="get-started"></a>Kom i gang

Avhengig av hva situasjonen er, varierer de faktiske aktivitetene. Bruk følgende tabell for å komme i gang.

|Hva vil du gjøre?|Se ...|
|-----------------------|------|
|Finn ut hva er den beste oppsettstypen som skal brukes i min situasjon|[Bestem hvilken type oppsett du vil bruke](#decide)|
|Opprett et nytt oppsett for en rapport som er basert på et eksisterende oppsett, og beholder det eksisterende oppsettet.|[Opprett et nytt oppsett](#create)|
|Gjør endringer i et eksisterende oppsett som brukes i en rapport|[Endre et oppsett](#modify)|
|Jeg har en ny versjon av en oppsettsfil for en rapport. Jeg vil erstatte den eksisterende oppsettsfilen.|[Erstatt et oppsett](#replace)|
|Bytt det gjeldende oppsettet som brukes av en rapport, til et annet oppsett|[Definer oppsettet som brukes av en rapport](ui-set-report-layout.md)|
|Endre navn og beskrivelse for et oppsett|[Gi et oppsett nytt navn](#rename)|

## <a name="decide-what-type-of-layout-you-want"></a><a name="decide-what-type-of-layout-you-want"></a><a name="decide-what-type-of-layout-you-want"></a><a name="decide"></a>Bestem hvilken type oppsett du vil bruke

Det første når du oppretter et oppsett, er å bestemme hvilken [type oppsett](ui-manage-report-layouts.md#layout-types) du vil bruke. Du kan velge enten Word, Excel eller RDLC. Oppsettstypen varierer avhengig av hvordan du vil at den genererte rapporten skal se ut. Det avhenger dessuten av hva slags programvare du trenger for å opprette oppsett, for eksempel Word, Excel og SQL Server Report Builder.

<!--
* The process for setting up Word, Excel, and RDLC layouts on reports is the same. The main difference is in the way you modify the layouts. Excel and Word layouts are typically easier to create and modify than RDLC layouts because you use Word and Excel. RDLC report layouts are modified by using SQL Server Report builder, which targets more advanced users.-->

* Excel-oppsett er vanligvis de enkleste å opprette og endre fordi funksjonene for å summere data, legge til grafikk og stil, er vanlige Excel-funksjoner.

* Ikke alle rapporter og dokumenter har et datasett som er optimalisert for bruk med et oppsett i Excel. Aggregasjoner og sammensatte beregninger fungerer for eksempel best med RDLC- eller Word-oppsett. Dette gjelder også dokumenter.

* Hvis du bare gjør endringer i stilene som skrifttype, størrelse og farger, er et Word-oppsett også et godt valg.

* Det er mer avansert enn med Excel å legge til datafelter eller omorganisere datafelter i Word eller RDLC.

* Word- og RDLC-oppsett er gode å bruke for rapporter som etter hvert skal skrives ut.  

* Generelle utformingskonsepter for Word og RDLC oppsett er like. Hver type har imidlertid visse utformingsfunksjoner som påvirker hvordan den genererte rapporten vises i [!INCLUDE[prod_short](includes/prod_short.md)]. Den samme rapporten kan gi ulike utseender ved å bruke Word-oppsettet sammenlignet med RDLC-oppsettet.

## <a name="create-a-new-layout"></a><a name="create-a-new-layout"></a><a name="create-a-new-layout"></a><a name="create"></a>Opprett et nytt oppsett

Du kan opprette et nytt oppsett for et eksisterende oppsett på to måter. En måte er å lagre det eksisterende oppsettet på en kopi. Den andre måten er å eksportere det eksisterende oppsettet.

## [Kopiering](#tab/copy)

Kopiering er en rask måte å opprette et nytt oppsett som er det samme som et eksisterende oppsett. Når du har opprettet kopien, kan du gjøre endringer ved å eksportere oppsettet. 

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Velg oppsettet du vil ha en kopi av, for det nye oppsettet, og klikk deretter på **Rediger info**-handlingen.

    Hvis du har valgt et utvidelsesoppsett, blir du spurt om du vil redigere en kopi. Velg **Ja** for å fortsette.

    > [!TIP]
    > Du kan finne oppsettet ved å bruke **søkefeltet**, **filtreringsruten** og kolonnesorteringen.
3. Endre **oppsettnavnet**.
4. Slå **Lagre endringer til kopi** til **På** og velg **OK**

   Det nye oppsettet vises på siden **Rapportoppsett**.
5. Hvis du vil foreta endringer i den nye utformingen, kan du se [Endre et eksisterende oppsett](#modify).

### [Eksport/import](#tab/export)

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Velg oppsettet du vil ha en kopi av, for det nye oppsettet, og klikk deretter på **Eksporter oppsett**-handlingen.

   Oppsettsfilen lastes ned til enheten. 

    > [!TIP]
    > Du kan finne oppsettet ved å bruke **søkefeltet**, **filtreringsruten** og kolonnesorteringen.

3. Åpne oppsettsfilen i det aktuelle programmet, som Word (for en DOCX-fil) eller Excel (for en XLSX-fil).

   Hvis du vil ha mer informasjon, kan du se:

   * [Arbeid med Word-oppsett](ui-how-add-fields-word-report-layout.md)
   * [Arbeid med Excel-oppsett](ui-excel-report-layouts.md)
   * [Arbeid med RDLC-oppsett](ui-rdlc-report-layouts.md)

   Gjør endringer i filen og lagre den.

4. Velg handlingen **Nytt oppsett** tilbake på siden **Rapportoppsett**.
5. Fyll ut følgende felter:

   |Felt|Beskrivelse|Obligatorisk|
   |-----|-----------|---------|
   |Rapport-ID|Angi ID-en som er tildelt rapporten|ja|
   |Navn på oppsett| Skriv inn et kort beskrivelsesnavn for oppsettet slik at du lett kan identifisere det.|ja|
   |Beskrivelse| Skriv inn mer detaljert informasjon om oppsett. |nei|
   |Formatalternativer|Angi at dette feltet skal være identisk med typen oppsett, for eksempel Word, Excel eller RDLC.|ja|

6. Velg **OK** og gjør deretter et av følgende for å laste opp oppsettfilen for rapporten:

   [!INCLUDE[file-upload](includes/file-upload.md)]

   Den valgte filen lastes opp til oppsettet, og du går tilbake til siden **Rapportoppsett**.

Hvis du vil se hvordan rapporten ser ut med det nye oppsettet, velger du oppsettet i listen, og deretter velger du **Kjør rapport**.

---

## <a name="modify-a-layout"></a><a name="modify-a-layout"></a><a name="modify-a-layout"></a><a name="modify"></a>Endre et oppsett

Følg denne fremgangsmåten for å endre et eksisterende brukerdefinert oppsett.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Velg oppsettet du vil endre, og velg deretter **Eksporter oppsett**-handlingen.

   Oppsettsfilen lastes ned til enheten. 

   > [!TIP]
   > Du kan finne oppsettet ved å bruke **søkefeltet**, **filtreringsruten** og kolonnesorteringen.

3. Åpne oppsettsfilen i det aktuelle programmet, som Word (for en DOCX-fil) eller Excel (for en XLSX-fil).

   Hvis du vil ha mer informasjon, kan du se:

   * [Arbeid med Word-oppsett](ui-how-add-fields-word-report-layout.md)
   * [Arbeid med Excel-oppsett](ui-excel-report-layouts.md)
   * [Arbeid med RDLC-oppsett](ui-rdlc-report-layouts.md)

   Gjør endringer i filen og lagre den.

4. Tilbake på siden **Rapportoppsett** velger du det eksisterende oppsettet, og deretter velger du **Erstatt oppsett**-handlingen.
5. Velg **OK** > **Velg** for å åpne filutforsker på enheten.
6. Finn og velg Excel-filen, og velg deretter **Åpne**.

   Den valgte filen lastes opp til oppsettet, og du går tilbake til siden **Rapportoppsett**.
7. Hvis du vil se hvordan rapporten ser ut med det nye oppsettet, velger du oppsettet i listen, og deretter velger du **Kjør rapport**.

## <a name="replace-a-layout"></a><a name="replace-a-layout"></a><a name="replace-a-layout"></a><a name="replace"></a>Erstatt et oppsett

Følg denne fremgangsmåten hvis du vil erstatte den eksisterende, brukerdefinerte oppsettsfilen med en ny fil.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Velg det eksisterende oppsettet, og velg deretter **Erstatt oppsett**-handlingen.
3. Velg **OK** > **Velg** for å åpne filutforsker på enheten.
4. Finn og velg Excel-filen, og velg deretter **Åpne**.

   Den valgte filen lastes opp til oppsettet, og du går tilbake til siden **Rapportoppsett**.
5. Hvis du vil se hvordan rapporten ser ut med det nye oppsettet, velger du oppsettet i listen, og deretter velger du **Kjør rapport**.

## <a name="rename-a-layout"></a><a name="rename-a-layout"></a><a name="rename-a-layout"></a><a name="rename"></a>Gi et oppsett nytt navn

Følg denne fremgangsmåten hvis du vil endre navnet og beskrivelsen for et brukerdefinert oppsett.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Velg oppsettet du vil gi nytt navn, og velg deretter **Rediger info**-handlingen.

    > [!TIP]
    > Du kan finne oppsettet ved å bruke **søkefeltet**, **filtreringsruten** og kolonnesorteringen.
3. Endre **oppsettsnavnet** og velg deretter **OK**.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Håndtere rapportoppsett](ui-manage-report-layouts.md)  
[Arbeid med Word-oppsett](ui-how-add-fields-word-report-layout.md)  
[Arbeid med Excel-oppsett](ui-excel-report-layouts.md)  
[Arbeide med rapporter, satsvise jobber og XMLport-er](ui-work-report.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
