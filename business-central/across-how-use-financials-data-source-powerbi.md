---
title: Bygge rapporter i Power BI Desktop for å vise Business Central-data
description: 'Gjør dataene tilgjengelige som en datakilde i Power BI, og bygg kraftige rapporter om status for din bedrift.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'business intelligence, KPI, Odata, Power App, SOAP, analysis'
ms.date: 06/12/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# <a name="building-power-bi-reports-to-display--data"></a>Bygg Power BI-rapporter for å vise [!INCLUDE [prod_long](includes/prod_long.md)]-data

Gjør [!INCLUDE[prod_long](includes/prod_long.md)]-dataene tilgjengelige som en datakilde i Power BI Desktop, og bygg kraftige rapporter om status for din bedrift.

Denne artikkelen beskriver hvordan du kommer i gang med Power BI Desktop for å opprette rapporter som viser [!INCLUDE[prod_long](includes/prod_long.md)]-data. Når du har opprettet rapporter, kan du publisere dem i Power BI-tjenesten eller dele dem med alle brukerne i organisasjonen. Når rapportene er i Power BI-tjenesten, kan brukerne som er konfigurert for den, vise rapportene i [!INCLUDE[prod_long](includes/prod_long.md)].

## <a name="get-ready"></a>Gjøre deg klar

- Registrer deg for Power BI-tjenesten.

  Hvis du ikke har registrert deg, går du til [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Når du registrerer deg, bruker du e-postadressen og passordet for jobben din.

- Last ned [Power BI Desktop](https://powerbi.microsoft.com/desktop/).

  Power BI Desktop er et gratis program du kan installere på den lokale datamaskinen. Hvis du vil ha mer informasjon, kan du se [Hurtigstart: Koble til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).

- Kontroller at dataene du vil ha med i rapporten er tilgjengelig som en API-side eller er publisert som en nettjeneste. Hvis du vil ha mer informasjon, kan du se [Eksponere data via API-sider eller OData-nettjenester](admin-powerbi-setup.md#exposedata).

<!--- For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, get the following information:

  - The OData URL for [!INCLUDE[prod_short](includes/prod_short.md)].
  
    Typically, this URL has the format `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, for example, `https://localhost:7048/BC190/ODataV4`. If you have a multi-tenant deployment, include the tenant in the URL, for example, `https://localhost:7048/BC190/ODataV4?tenant=tenant1`.
  - A user name and web service access key of a [!INCLUDE[prod_short](includes/prod_short.md)] account.

    To get data from [!INCLUDE[prod_short](includes/prod_short.md)], Power BI uses basic authentication. So, you'll need a user name and web service access key to connect. The account might be your own user account, or your organization may have specific account for this purpose.-->

- Last ned [!INCLUDE [prod_short](includes/prod_short.md)]-rapporttemaet (valgfritt).

  Hvis du vil ha mer informasjon, kan du se [Bruk [!INCLUDE [prod_short](includes/prod_short.md)]-rapporttemaet](#theme) i denne artikkelen.

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

## <a name="add--as-a-data-source-in-power-bi-desktop"></a><a name="getdata"></a>Legge til [!INCLUDE[prod_short](includes/prod_short.md)] som en datakilde i Power BI Desktop

Den første oppgaven i opprettelse av rapporter, er å legge til [!INCLUDE[prod_short](includes/prod_short.md)] som en datakilde i Power BI Desktop. Når den er tilkoblet, kan du begynne å bygge rapporten.

1. Start Power BI Desktop.
2. Velg **Hent data**.

    Hvis du ikke ser **Hent data**, velger du **Fil**-menyen og deretter **Hent data**.
3. På **Hent data**-siden velger du **Online Services**.
4. I **Online Services**-ruten gjør du ett av følgende:

    - Hvis du vil koble til [!INCLUDE [prod_short](includes/prod_short.md)] online, velger du **Dynamics 365 Business Central** og deretter **Koble til**.
    <!--- To connect to  [!INCLUDE [prod_short](includes/prod_short.md)] on-premises, select **Dynamics 365 Business Central (on-premises)**, then **Connect**.-->

5. Logg på [!INCLUDE [prod_short](includes/prod_short.md)] (bare én gang).

    Hvis du ikke er logget på [!INCLUDE [prod_short](includes/prod_short.md)] fra Power BI Desktop, blir du bedt om å logge på.

    - For [!INCLUDE [prod_short](includes/prod_short.md)] Online velger du **Logg på** og deretter den relevante kontoen. Bruk den samme kontoen du bruker til å logge på [!INCLUDE [prod_short](includes/prod_short.md)]. Velg **Koble til** når du er ferdig.

    <!--- For [!INCLUDE [prod_short](includes/prod_short.md)] on-premises, first enter the OData URL for [!INCLUDE[prod_short](includes/prod_short.md)], then select **OK**. When prompted, enter the user name and password of the account to use for connecting to [!INCLUDE[prod_short](includes/prod_short.md)]. In the **Password** box, enter the web service access key. When done, select **Connect**.-->

    > [!NOTE]  
    > Når du er koblet til [!INCLUDE[prod_short](includes/prod_short.md)], blir du ikke bedt på nytt om å logge på. [Hvordan endrer eller tømmer jeg kontoen jeg for øyeblikket bruker til koble til Business Central fra Power BI Desktop?](/dynamics365/business-central/power-bi-faq?tabs=designer#perms)

6. Når du er tilkoblet, kontakter Power BI [!INCLUDE [prod_short](includes/prod_short.md)]-tjenesten. **Navigatør**-vinduet viser datakildene som er tilgjengelige for bygging av rapporter. Velg en mappe for å utvide den og se de tilgjengelige datakildene.

   Disse datakildene representerer alle nettjenestene og API-sidene som er publisert for [!INCLUDE [prod_short](includes/prod_short.md)], gruppert etter miljøer og selskaper. Med [!INCLUDE [prod_short](includes/prod_short.md)] online har **Navigatør** følgende struktur:

    - **Miljønavn**
      - **Selskapsnavn**
        - **Avanserte API-er**

          Denne mappen viser avanserte API-sider som er publisert av Microsoft, som [Automatiserings-API-er for Business Central](/dynamics365/business-central/dev-itpro/administration/itpro-introduction-to-automation-apis) og [tilpassede API-sider for Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api). Egendefinerte API-sider grupperes ytterligere i mapper i henhold til egenskapene [APIPublisher](/dynamics365/business-central/dev-itpro/developer/properties/devenv-apipublisher-property)/[APIGroup](/dynamics365/business-central/dev-itpro/developer/properties/devenv-apigroup-property) for kildekoden for API-siden.

        - **Standard API-er v 2.0**

          Denne mappen inneholder en oversikt over API-sidene som vises av [Business Central API v2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/).

        - **Nettjenester \(eldre)**

          Denne mappen inneholder en oversikt over sider, codeunit og spørringer som er publisert som nettjenester i Business Central.

    <!--
    > [!NOTE]
    > The structure for Business Central on-premises is different because it doesn't support API pages.-->

7. Velg datakilden eller -kildene du vil legge til datamodellen, og velg deretter **Last inn**-knappen.
8. Hvis du senere vil legge til flere Business Central-data, kan du gjenta trinnene ovenfor.

Når dataene er lastet inn, kan du se dem i høyre navigering på siden. Nå har du koblet til [!INCLUDE[prod_short](includes/prod_short.md)]-dataene, og du kan begynne å bygge Power BI-rapporten.  

> [!TIP]
> Hvis du vil ha mer informasjon om hvordan du bruker Power BI Desktop, kan du se [Kom i gang med Power BI Desktop](/power-bi/fundamentals/desktop-getting-started).

## <a name="creating-accessible-reports"></a>Opprette tilgjengelige rapporter

Det er viktig å gjøre rapportene brukbare for så mange som mulig. Prøv å utforme rapporter slik at de ikke må tilpasses for å oppfylle bestemte behov for ulike brukere. Kontroller at utformingen lar brukere dra nytte av standard hjelpeteknologier, for eksempel skjermlesere. Power BI omfatter ulike tilgjengelighetsfunksjoner, verktøy og retningslinjer som kan hjelpe deg å oppnå dette. Hvis du vil ha mer informasjon, kan du se [Utforme Power BI-rapporter for tilgjengelighet](/power-bi/create-reports/desktop-accessibility-creating-reports) i dokumentasjonen for Power BI.

## <a name="creating-reports-to-display-data-associated-with-a-list"></a>Opprette rapporter for å vise data tilknyttet en liste

Du kan opprette rapporter som vises i en faktaboks på en [!INCLUDE [prod_short](includes/prod_short.md)]-listeside. Rapportene kan inneholde data om posten som er valgt i listen. Du oppretter disse rapportene på lignende måte som andre rapporter, men det er enkelte ting du må gjøre for å sikre at rapportene vises som forventet. Hvis du vil ha mer informasjon, kan du se [Opprette Power BI-rapporter for visning av listedata i [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

## <a name="using-the--report-theme-optional"></a><a name="theme"></a>Bruke [!INCLUDE [prod_short](includes/prod_short.md)]-rapporttemaet (valgfritt)

Før du bygger rapporten, anbefales det at du laster ned og importerer [!INCLUDE [prod_short](includes/prod_short.md)]-teamfilen. Temafilen oppretter en fargepalett, slik at du kan lage rapporter med samme fargestil som [!INCLUDE [prod_short](includes/prod_short.md)]-appene uten å måtte definere egendefinerte farger for hver visualisering.

> [!NOTE]
> Denne oppgaven er valgfri. Du kan alltids opprette rapportene og deretter laste ned og bruke stilmalen senere.

### <a name="download-the-theme"></a>Laste ned temaet

Temafilen er tilgjengelig som en JSON-fil i temagalleriet i Microsoft Power BI-fellesskapet. Hvis du vil laste ned temafilen, gjør du følgende:

1. Gå til [Temagalleriet i Microsoft Power BI-fellesskapet for Microsoft Dynamics 365 Business Central](https://community.powerbi.com/t5/Themes-Gallery/Microsoft-Dynamics-365-Business-Central/m-p/385875).
2. Velg nedlastingsvedlegget **Microsoft Dynamics Business Central.json**.

### <a name="import-the-theme-on-a-report"></a>Importere temaet i en rapport

Etter at du har lastet ned [!INCLUDE [prod_short](includes/prod_short.md)]-rapporttemaet, kan du importere det til rapportene. Du importerer temaet ved å velge **Vis** > **Temaer** > **Bla gjennom etter temaer**. Hvis du vil ha mer informasjon, kan du se [Power BI Desktop – importere egendefinerte rapporttemaer](/power-bi/create-reports/desktop-report-themes#import-custom-report-theme-files).

## <a name="publish-reports"></a>Publisere rapporter

Når du har opprettet eller endret en rapport, kan du publisere den i Power BI-tjenesten og dele den med andre i organisasjonen. Når du har publisert en rapport, er den tilgjengelig i Power BI. Rapporten blir også tilgjengelig for valg i [!INCLUDE[prod_short](includes/prod_short.md)].

Du publiserer en rapport ved å velge **Publiser** i **Hjem**-fanen på båndet eller **Fil**-menyen. Hvis du er logget på Power BI-tjenesten, publiseres rapporten til denne tjenesten. Hvis ikke blir du bedt om å logge på. 

## <a name="distribute-or-share-a-report"></a>Distribuere eller dele en rapport

Du kan sende rapporter til kolleger og andre på et par ulike måter:

- Distribuer rapporter som PBIX-filer.

    Rapporter lagres på datamaskinen som PBIX-filer. Du kan distribuere PBIX-rapportfilen til brukere, slik som alle andre filer. Deretter kan brukerne laste opp filen til Power BI-tjenesten. Se [Laste opp rapporter fra filer](across-working-with-powerbi.md#upload).

    > [!NOTE]
    > Når du distribuerer rapporter på denne måten, betyr det at data for rapporter oppdateres individuelt av hver bruker. Denne situasjonen kan påvirke ytelsen til [!INCLUDE[prod_short](includes/prod_short.md)].

- Del rapporter fra Power BI-tjenesten.

    Hvis du har en Power BI Pro-lisens, kan du dele rapporten med andre direkte fra Power BI-tjenesten. Hvis du vil ha mer informasjon, kan du se [Power BI – dele et instrumentbord eller en rapport](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

## <a name="how-to-develop-cross-company-or-cross-environment-power-bi-reports"></a>Slik utvikler du Power BI-rapporter på tvers av firmaer eller miljøgrupper

Alle [!INCLUDE[prod_short](includes/prod_short.md)] API-endepunktene har prefikset `https://api.businesscentral.dynamics.com/v2.0/<environment_name>/api/v2.0`, etterfulgt av `/companies({company_id})/accounts({id})` (her bruker vi API-en `accounts` som en illustrasjon). Du kan bruke denne strukturen til å opprette PowerQuery-spørringer som laster inn data for flere selskaper eller flere miljøer, hvis brukeren som leser data, har tilgang til dem.

Hvis du vil konfigurere en spørring for å laste inn data for flere selskaper, gjør du følgende:

1. Ta PowerQuery-spørringen som laster inn data for ett enkelt selskap. Konverter den til en egendefinert Power Query-funksjon som bruker selskaps-ID-en (eller kanskje miljønavnet) som parametere. Hvis du vil vite mer, kan du gå til [Bruke egendefinerte Power Query-funksjoner](/power-query/custom-function).
1. Bruk nå den nye egendefinerte funksjonen i en PowerQuery-spørring, der du tilordner funksjonen over en liste over selskaper og deretter fletter datasettene ved hjelp av funksjonen [Table.Combine](/powerquery-m/table-combine) i Power Query.

## <a name="fixing-problems"></a>Løse problemer

### <a name="cant-insert-a-record-current-connection-intent-is-read-only-error-connecting-to-custom-api-page"></a>«Kan ikke sette inn en post. Nåværende tilkoblingshensikt er skrivebeskyttet.» feil under tilkobling til egendefinert API-side

> **GJELDER:** Business Central Online

Fra og med februar 2022 blir nye rapporter som bruker [!INCLUDE [prod_short](includes/prod_short.md)]-data, koblet til en skrivebeskyttet replika av [!INCLUDE [prod_short](includes/prod_short.md)]-databasen som standard. I sjeldne tilfeller, avhengig av sideutformingen, kan du få en feilmelding når du prøver å koble deg til og hente data fra siden.

1. Start Power BI Desktop.
2. På båndet velger du **Hent data** > **Online Services**.
3. I ruten **Online Services** velger du **Dynamics 365 Business Central** og deretter **Koble til**.
4. Velg API-endepunktet du vil laste inn data fra, i vinduet **Navigatør**.
5. Forhåndsvisningsruten viser følgende feil:

   *Dynamics365BusinessCentral: forespørsel mislyktes: den eksterne serveren returnerte en feil: (400) Ugyldig forespørsel. (Kan ikke sette inn en post. Nåværende tilkoblingshensikt er skrivebeskyttet. CorrelationId: [...])".*

6. Velg **Transformer data** i stedet for **Last inn** som du normalt ville gjort.
7. Velg **Avansert redigering** fra båndet i **Power Query-redigeringsprogram**.
8. På linjen som begynner med **Kilde =**, erstatter du følgende tekst:

   ```
   Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, null)
   ```

   med:

   ```
   Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, [UseReadOnlyReplica = false])
   ```

9. Velg **Ferdig**.
10. Velg **Lukk og bruk** fra båndet til å lagre endringene og lukk Power Query-redigeringsprogrammet.

## <a name="see-also"></a>Se også

[Aktiver forretningsdata for Power BI](admin-powerbi-setup.md)  
[Forretningsintelligens](bi.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finans](finance.md)  
[Hurtigstart: Koble til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
