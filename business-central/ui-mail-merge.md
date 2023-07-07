---
title: Bruk Word-maler til massekommunikasjon
description: Word-maler kan gjøre det enkelt å opprette dokumenter som er tilpasset for bestemte enheter.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/01/2023
ms.custom: bap-template
ms.search.forms: '9989, 13,'
---

# <a name="use-word-templates-for-bulk-communication"></a>Bruk Word-maler til massekommunikasjon

Microsoft Word-maler kan gjøre det enklere å massekommunisere på trykk eller e-post med enheter som kontakter, kunder og leverandører. Du kan for eksempel opprette:

* Brosjyrer for å varsle kunder om en salgskampanje
* Brev for å informere leverandører om en ny innkjøpspolicy
* Invitasjoner til å tiltrekke kontakter til et kommende arrangement

> [!NOTE]
> Når du konfigurerer Word-maler, må du bruke en enhet med Microsoft Word 2019 eller nyere og Windows-operativsystemet installert.

## <a name="set-up-the-source-of-data"></a>Sett opp datakilden

Bruk enheter i [!INCLUDE[prod_short](includes/prod_short.md)] som datakilde for malen, og legg til flettefelt for å tilpasse dokumenter for hver enhet. Flettefeltene kommer fra enheten i [!INCLUDE[prod_short](includes/prod_short.md)]. Når du bruker en Word-mal på en enhet, settes det inn data fra flettefeltene i dokumentet.

På siden **Word-maler** kan du gjøre følgende når du oppretter en ny mal i en veiledning for assistert oppsett:

1. Velg en eller flere enheter som skal brukes som datakilde. Hvis du for eksempel vil opprette en brosjyre for en salgskampanje, har du sannsynligvis valgt Kunde-enheten som kilde.
2. Velg andre enheter som ekstra datakilder. Lær mer under [Legg til poster som er relatert til eller ikke relatert til kildeenheten](#add-entries-that-are-related-or-unrelated-to-the-source-entity).
3. Last ned en tom mal. Du kan sette opp malen i Word med en gang, eller du kan laste opp den tomme malen og fullføre veiledningen. Når malen er klar, bruker du **Last opp**-handlingen på siden **Word-maler** til å erstatte den tomme malen med den ferdige malen. Finn ut mer under [Definer malen i Word](#set-up-the-template-in-word).
4. Last opp malen du har forberedt.
5. Angi en kode og et navn som identifiserer malen.

Når du laster ned en mal, får du en ZIP-fil som inneholder to filer.

|Fil  |Beskrivelse  |
|---------|---------|
|DataSource.xlsx     | Datakildefilen inneholder feltene du kan bruke i malen. Ikke rediger datakildefilen. Du kan bare bruke Word-maler og datakildefiler du laster ned, og du må lagre filene på samme sted.     |
|Word-mal     | En DOCX-fil som skal brukes som mal.        |

Hvis du vil lære om hvordan du oppretter en mal i Word, kan du gå til [Definer malen i Word](#set-up-the-template-in-word).

## <a name="add-entries-that-are-related-or-unrelated-to-the-source-entity"></a>Legg til poster som er relatert til eller ikke relatert til kildeenheten

Du kan også slå sammen data fra andre enheter. Hvis du vil legge til andre enheter som datakilder, bruker du en av følgende handlinger på siden **Word-maler** eller når du bruker veiledningen for assistert oppsett:

|Handling  |Beskrivelse  |
|---------|---------|
|**Legg til relatert enhet**  | Bruk data fra enheter som er knyttet til kildeenheten. For Kunde-enheten kan du for eksempel også slå sammen data fra Kontakt-enheten. Enheter er relatert når et felt på en enhet henviser til en annen. Et felt på Kunde-enheten henviser til et felt på Kontakt-enheten, så de er relatert. Det delte feltet er ofte en identifikator, for eksempel navn, kode eller ID.        |
|**Legg til ikke-relatert enhet**| Bruk data fra enheter som ikke er knyttet til kildeenheten. Du oppretter for eksempel en mal for Kunde-enheten. Du kan legge til Selskapsopplysninger-enheten slik at du kan ta med kontaktopplysningene. En viktig fordel er at hvis du endrer kontaktopplysninger, oppdateres de automatisk i malen. Når du har lagt til en ikke-relatert enhet, kan du legge til enheter som er relatert til den.         |

For urelaterte poster velger du en bestemt post. Ettersom du bare kan legge til en enhet én gang, må du slette enheten og legge den til på nytt med den nye posten for å bruke en annen post.

Du kan opprette et hierarki over enheter, både relaterte og ikke relaterte. Relasjonen vises som en trestruktur. Feltet **Enhetsrelasjon** viser også informasjon om relasjonen. For ikke-relaterte enheter viser feltet posten som oppretter relasjonen.

Når du legger til enheter, bruker du feltet **Feltprefiks** til å angi et prefiks for feltnavnene. Senere, når du legger til felter i malen, kan prefikset hjelpe deg med å skille mellom felter fra kildeenheten og andre enheter.

### <a name="select-the-fields-to-include"></a>Velg feltene som skal inkluderes

For hver enhet kan du angi hvilke felter som skal være tilgjengelige for malen. Velg antallet i kolonnen **Antall valgte felter** for å få tilgang til en liste over tilgjengelige felter. På siden **Feltutvalg** bruker du avmerkingsboksen **Inkluder** til å angi feltene. For enkelte enheter er felter som vanligvis brukes i virksomheter, inkludert som standard. Du kan redigere listen, for eksempel for å fjerne standardfeltene. Endringene gjelder bare malen du arbeider på.

> [!NOTE]
> Totalt antall felter du kan legge til fra alle enheter er 250.

> [!NOTE]
> Du eller Microsoft-partneren kan legge til egendefinerte felter i enheter. Når du gjør dette, prefikser vi navnet på feltene med **BEREGN** og gi dem felttypen **Beregnet**. Felttypen kalles beregnet for å angi at feltet kan vise forskjellige typer verdier, for eksempel tekst, tall, datoer og så videre.

## <a name="to-create-a-word-template-in-business-central"></a>Slik oppretter du en Word-mal i Business Central

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Word-maler**, og velg deretter den relaterte koblingen.
2. Velg **Ny**, **Opprett en mal**, og følg deretter instruksjonene i veiledningen for assistert oppsett. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Du kan også opprette en mal direkte fra siden for en enhet ved å velge handlingen **Bruk Word-mal** for å åpne veiledningen for assistert oppsett og deretter **Ny mal**. Når du gjør dette, velges datakilden basert på enhetstypen.

## <a name="set-up-the-template-in-word"></a>Definer malen i Word

Når du definerer en mal i Word, kan du legge til flettefelt ved å velge **Sett inn flettefelt** i fanen **Masseutsendelser**. Flettefeltene kommer fra datakildefilen du lastet ned for enheten. De fungerer som plassholdere som forteller Word hvor i dokumentet det skal plasseres informasjon om enheten.

:::image type="content" source="media/word-tmpl-merge-field.PNG" alt-text="Legg til flettefelt i Microsoft Word":::

## <a name="apply-a-template"></a>Bruk en mal

Når Word-malen er klar, kan du velge **Bruk** på siden **Word-maler** for å generere dokumentene. Når du bruker en Word-mal på en enhet, settes det inn data fra flettefeltene i dokumentet. Du kan enten opprette ett dokument som inneholder inndelinger for hver enkelt enhet, eller velge **Del opp** for å opprette et nytt dokument for hver enhet.

Du kan bruke handlingen **Bruk Word-maler** til å bruke maler på en eller flere av samme type enhet, som kunde, direkte i konteksten til siden for enheten. For eksempel sidene **Kunde** eller **Leverandør**.

## <a name="use-word-templates-with-email"></a>Bruk Word-maler med e-post

Du kan bruke Word-maler til å legge til innhold i e-postmeldinger. Når du skriver en e-postmelding, kan du velge handlingen **Bruk Word-mal** for å bruke innholdet i en mal på meldingen. Du må ha opprettet maler for enheten. Du kan bruke én mal om gangen, og når du bytter mellom maler, endres meldingen for å gjenspeile innholdet fra den valgte malen.

I tillegg kan du bruke handlingen **Legg til fil fra Word-mal** til å knytte innholdet i malen til e-postmeldingen som en fil. Filen bruker formatet som er angitt for utdataene i malen.

:::image type="content" source="media/email-word-tmpl.PNG" alt-text="Alternativer for bruk av innhold fra en Word-mal i en e-post":::

## <a name="edit-a-word-template"></a>Rediger en Word-mal

Du kan gjøre følgende endringer i Word-maler:

* Hvis du vil redigere brødteksten eller flette feltene som er inkludert i malen, bruker du handlingen **Last ned**, gjør endringene og bruker **Last opp**-handlingen
* Hvis du vil endre datakildene, bruker du handlingen **Rediger relaterte enheter**
* Hvis du vil erstatte Word-malen med en ny mal, bruker du **Last opp**-handlingen
* Slett malen

## <a name="see-also"></a>Se også

[Administrer rapport- og dokumentoppsett](ui-manage-report-layouts.md)  
[Konfigurer e-post](admin-how-setup-email.md)  
