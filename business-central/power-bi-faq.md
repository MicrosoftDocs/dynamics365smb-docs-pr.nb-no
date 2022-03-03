---
title: Vanlige spørsmål om Power BI
description: Få svar på enkelte vanlige spørsmål om å arbeide med Power BI og Business Central.
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Power BI, reports, faq, errors
ms.date: 04/22/2021
ms.author: jswymer
ms.openlocfilehash: 1c0a19a9739ab537b6a5df562484d2d9d6f8e3a6
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8137656"
---
# <a name="power-bi--faq"></a>Vanlige spørsmål om Power BI

Denne artikkelen besvarer noen av spørsmålene du kan ha om å arbeide med Power BI og [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="general"></a>[Generelt](#tab/general)
<!-- 26 -->
### <a name="ive-selected-a-report-for-my-role-center-in-business-central-if-i-later-make-changes-to-the-reports-visuals-online-will-the-role-center-automatically-update-to-my-changes"></a>Jeg har valgt en rapport for rollesenteret mitt i Business Central. Blir rollesenteret oppdatert automatisk slik at endringene mine gjenspeiles hvis jeg senere endrer de visuelle elementene i rapporten på nettet?

Ja, fordi rapportene bygges inn fra Power BI.

<!-- 3 -->
### <a name="are-the-business-central-apps-for-power-bi-available-in-languages-other-than-english"></a>Er Business Central-appene for Power BI tilgjengelige på andre språk enn engelsk?

Nei. Disse appene er for øyeblikket bare tilgjengelige på engelsk.

<!-- 24 -->
### <a name="once-a-report-is-published-on-mypowerbicomworkspace-can-i-download-its-pbix"></a>Når en rapport er publisert på arbeidsområdet mitt på powerbi.com, kan jeg laste ned PBIX-filen for den? 

Ja. Hvis du vil ha mer informasjon, kan du se [Laste ned en rapport fra Power BI-tjenesten til Power BI Desktop](/power-bi/create-reports/service-export-to-pbix).  

<!-- 27 -->
### <a name="can-i-download-the-apps-as-pbix-files"></a>Kan jeg laste ned appene som PBIX-filer? 

Nei. Vi tilbyr for øyeblikket ikke nedlasting av PBIX-filer for de offisielle Power BI-appene, fordi de er publisert på AppSource.

## <a name="license"></a>[Lisens](#tab/license)

<!-- 14 -->
### <a name="do-i-need-a-power-bi-pro-license-to-publish-reports"></a>Må jeg ha en Power BI Pro-lisens for å kunne publisere rapporter? 

<!-- todo What does " or for every user that consults the published report" mean? fixed -->
Nei. En Pro-lisens er ikke nødvendig for å publisere rapporter. Power BI-standardlisensen (gratis) er nok. Hvis du vil ha mer informasjon, kan du se [Power BI-lisensiering](admin-powerbi-setup.md#license).

<!-- 15 -->
### <a name="is-there-anything-i-cant-do-with-the-free-license"></a>Er det noe jeg ikke kan gjøre med gratislisensen?

Du kan ikke dele rapporter eller installere Business Central-appene for Power BI. Bortsett fra dette kan du opprette nesten alle varianter av diagrammer og rapporter med gratislisensen.

<!-- 16 -->
### <a name="if-someone-shares-a-report-with-another-person-then-that-person-needs-a-pro-license-to-see-the-report-are-there-plans-to-make-this-capability-possible-with-the-free-license"></a>Hvis noen deler en rapport med en annen person, må denne personen ha en Pro-lisens for å kunne se rapporten. Har dere planer om å gjøre denne funksjonen tilgjengelig med gratislisensen?

Vi har ikke kontroll over dette kravet. Dette kravet stilles av Power BI. Hvis du vil ha mer informasjon, kan du se [Dele Power BI-instrumentbord og -rapporter med kolleger og andre](/power-bi/collaborate-share/service-share-dashboards).  

## <a name="designer"></a>[Utforming](#tab/designer)

<!-- 7 -->
### <a name="does-the-connector-work-with-api-pages"></a>Fungerer koblingen med API-sider?

Ja. Fra og med juni 2021 støtter den nye Power BI-koblingen både Business Central-nettjenester og API-sider. Hvis du vil ha mer informasjon, kan du se [Aktivere Power BI-koblingen slik at den fungerer med API-er for Business Central, i stedet for bare webtjenester](/dynamics365-release-plan/2021wave1/smb/dynamics365-business-central/enable-power-bi-connector-work-business-central-apis-instead-web-services-only).

### <a name="can-i-build-a-power-bi-report-using-the-sales-invoice-lines-or-journal-lines-apis"></a>Kan jeg bygge en Power BI-rapport ved hjelp av API-ene Salgsfakturalinjer eller Kladdelinjer?

De mest brukte linjepostene er tilgjengelige i [Business Central-API-ene v2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/)). Du kan dermed bruke dem til å bygge opp rapporter i Power BI ved å merke dem i **Dynamics 365 Business Central**-koblingen. API-ene for **linjer** er imidlertid utformet for bare å brukes sammen med enkelte svært spesifikke filtre, og fungerer kanskje ikke i ditt scenario. Du kan få feilmeldingen som ligner: Du må angi en ID eller en dokument-ID for å hente linjene. Du løser dette problemet ved å gjøre følgende når du henter data fra Business Central for rapporten i Power BI Desktop:

1. I stedet for å inkludere datakilden for linjeenheten, legger du til den overordnede datakilden. Du kan for eksempel legge til **salgsfaktura** i stedet for **salgsfakturalinjer**.
2. Velg **Transformer data** på Power BI Desktop-handlingslinjen.
3. Velg spørringen du nettopp la til, for eksempel **Salgsfakturaer**.
4. Bruke alle nødvendige filtreringer på postene for å redusere antall poster som lastes inn i rapporten.
5. Rull mot høyre til du finner en kolonne som heter linjer, for eksempel **SalesInvoiceLines**.
6. Velg Vis-knappen i kolonneoverskriften ved siden av kolonnenavnet.

   :::image type="content" source="media/saleinvoicelines.png" alt-text="Viser SalesInvoiceLines-kolonnen i Power BI Desktop.":::
<!-- 11 --> 
### <a name="is-it-possible-to-choose-which-business-central-environment-to-get-data-from-for-power-bi-for-example-like-a-sandbox-or-production-environment"></a>Går det an å velge hvilket Business Central-miljø du kan hente data fra, for Power BI, for eksempel et sandkasse- eller produksjonsmiljø? 

Ja. Dette er enkelt å velge. Når du kobler deg til Business Central med koblingen, må du velge miljøet og selskapsnavnet.

<!-- 6 --> 
### <a name="can-i-merge-data-from-several-production-environments-of-the-same-tenant"></a>Kan jeg slå sammen data fra flere produksjonsmiljøer for samme leier?

Ja. I Power BI kjører du bare Hent data-operasjonen på nytt og velger ønsket miljø.

<!-- 25 -->
### <a name="which-pages-in-business-central-have-the-power-bi-report-part"></a>Hvilke sider i Business Central er delen Power BI-rapport på?  

Det er for øyeblikket noen få utvalgte sider som har en faktaboks med delen **Power BI-rapporter** for visning av en rapport. 

Delen **Power BI-rapporter** på listesider filtreres for å vise rapporter som gjelder data i listen. Her er listetypesidene som omfatter delen **Power BI-rapporter**:

|Side-ID|Name|
|-------|----|
|22|Kundeoversikt|
|27|Leverandøroversikt|
|31|Vareoversikt|
|9305|Ordreoversikt|
|9308|Kjøpsfakturaer|

Her er andre sider som inneholder den større, ikke-filtrerte delen **Power BI-rapporter**:

|Side-ID|Name|
|-------|----|
|1156|Opplysninger om selskap|
|4013|Intelligent skyinnsikt |
|9006|Rollesenter for ordrebehandler|
|9008|Rollesenter for grunnleggende lager|
|9010|Rollesenter for produksjonsplanlegger|
|9015|Rollesenter for jobbprosjektleder|
|9016|Rollesenter for serviceordrefordeler|
|9022|Rollesenter for forretningsleder|
|9024|Rollesenter for sikkerhetsadministrator|
|9026|Rollesenter for sjef for salg og relasjoner|
|9027|Rollesenter for regnskapsfører|

> [!TIP]
> Vi har for øyeblikket ingen planer om å legge den til på alle listesider. Du kan imidlertid lage en enkel sideutvidelse som legger til delen **Power BI-rapporter** i en faktaboks. Hvis du vil ha mer informasjon, kan du se [Legge til deler for Power BI-rapport på sider](/dynamics365/business-central/dev-itpro/developer/devenv-power-bi-report-parts) i hjelpen for utviklere og IT-eksperter.

<!-- 5 -->
### <a name="is-there-any-way-to-filter-a-dataset-from-business-central-before-i-pull-it-into-power-bi-instead-of-applying-filters-afterwards"></a>Går det an å filtrere et datasett fra Business Central *før* jeg henter det inn i Power BI, i stedet for å bruke filtre etterpå?

Den enkleste måten å filtrere større datasett på er å angi et filter for Power BI-rapporten ved å redigere Power Query-formelen direkte. De fleste filtrene du angir på denne måten, sendes videre til Business Central via spørringsdelegering. Se [Trinnvis oppdatering for datasett](/power-bi/admin/service-premium-incremental-refresh).

Det er for øyeblikket ingen måte å angi et filter for webtjenestedataene fra Business Central. Hvis programmet må angi et filter fra Business Central, må du opprette en egendefinert Business Central-app for dette formålet.

<!-- 10 -->
### <a name="from-power-bi-besides-using-a-query-is-there-another-way-to-get-data-from-business-central-tables-that-dont-have-an-associated-page-for-example-like-the-item-attributes-value-mapping-table"></a>Finnes det en annen metode i Power BI – enn å bruke en spørring – til å hente data fra Business Central-tabeller som ikke har en tilknyttet side? Slik som for eksempel tabellen *Tilordning av verdi for vareattributt*.

Nei. Ikke på dette tidspunktet.

<!-- 12 --> 
### <a name="are-published-queries-faster-to-use-than-published-pages"></a>Går det raskere å bruke publiserte spørringer enn publiserte sider?

Når det gjelder webtjenester, går det vanligvis raskere å bruke publiserte spørringer enn tilsvarende publiserte sider. Årsaken er at spørringer er optimalisert for lesing av data og ikke inneholder kostbare utløsere som OnAfterGetRecord.

Nettjenester er basert på sider eller spørringer som er bygd for tilgang fra nettet, og som vanligvis ikke er optimalisert for tilgang fra eksterne tjenester. Selv om Business Central-koblingen fortsatt støtter henting av data fra nettjenester, oppfordrer vi deg til å bruke API-sider i stedet for nettjenester når det er mulig.

<!-- 13 --> 
### <a name="is-there-a-way-for-an-end-user-to-create-a-web-service-with-a-column-thats-in-a-business-central-table-but-not-a-page-or-will-the-developer-have-to-create-a-custom-query"></a>Kan en sluttbruker opprette en webtjeneste med en kolonne som er i en Business Central-tabell, men ikke på en side? Eller må utvikleren opprette en egendefinert spørring? 

Det er for øyeblikket ikke mulig å legge til et nytt felt i en nettjeneste. API-sider gir deg full fleksibilitet på sidestrukturen, slik at en utvikler kan opprette en ny API-side som oppfyller dette kravet. 

<!-- 28 --> 
### <a name="can-i-connect-power-bi-to-a-read-only-database-server-of-business-central-online"></a>Kan jeg koble Power BI til en skrivebeskyttet databaseserver for Business Central Online? 

Denne funksjonaliteten blir snart tilgjengelig. Fra og med februar 2022 prøver nye rapporter du oppretter basert på Business Central Online-data, automatisk å koble seg til en skrivebeskyttet databasereplika. Dermed oppdateres rapportene raskere, og det vil ha mindre innvirkning på ytelsene hvis du bruker Business Central mens en rapport oppdateres. Vi anbefaler likevel at du planlegger rapportene slik at de oppdateres utenom vanlige arbeidstider, når det er mulig.

Hvis du har gamle rapporter basert på Business Central-data, kobler de ikke til den skrivebeskyttede databasereplikaen.

### <a name="ive-tried-the-preview-of-the-new-connector-for-the-february-2022-update-when-i-connect-to-my-custom-business-central-api-page-i-get-the-error-cannot-insert-a-record-current-connection-intent-is-read-only-how-can-i-fix-it"></a><a name="databasemods"></a>Jeg har prøvd å forhåndsvise den nye koblingen til oppdateringen for februar 2022. Når jeg kobler til en egendefinert Business Central API-side, får jeg feilmeldingen «Kan ikke sette inn en post. Nåværende tilkoblingshensikt er skrivebeskyttet.» Hvordan kan jeg løse det?

Med den nye koblingen vil nye rapporter som bruker Business Central-data, bli koblet til en skrivebeskyttet replika av Business Central-databasen som standard. Denne endringen gir en ytelsesforbedring. I sjeldne tilfeller kan det imidlertid føre til feilen. Denne feilen oppstår vanligvis fordi den egendefinerte API-en gjør endringer i Business Central-poster mens Power BI prøver å hente dataene. Særlig skjer det som en del av AL-utløserne: OnInit, OnOpenPage, OnFindRecord, OnNextRecord, OnAfterGetRecord og OnAfterGetCurrRecord.

Du løser dette problemet ved å tvinge Business Central-koblingen til å tillate dette problemet ved å se [Bygg Power BI-rapporter for å vise Business Central-data – løs problemer](across-how-use-financials-data-source-powerbi.md#fixing-problems).

<!--
In general, we recommend avoiding any database modifications in API pages when they're opening or loading records, because they cause performance issues and might cause your report refresh to fail. In some cases, you might still need to make a database modification when your custom API page opens or loads records. You can force the Business Central connector to allow this behavior. Do the following steps when getting data from Business Central for the report in Power BI Desktop:

1. Start Power BI Desktop.
2. In the ribbon, select **Get Data** > **Online Services**.
3. In the **Online Services** pane, select **Dynamics 365 Business Central**, then **Connect**.
4. In the **Navigator** window, select the API endpoint that you want to load data from.
5. In the preview pane on the right, you'll see the following error:

   *Dynamics365BusinessCentral: Request failed: The remote server returned an error: (400) Bad Request. (Cannot insert a record. Current connection intent is Read-Only. CorrelationId: [...])".*

6.  Select **Transform Data** instead of **Load** as you might normally do.
7. In **Power Query Editor**, select **Advanced Editor** from the ribbon.
8.  Replace the following line:

   ```
   Source = Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, null),
   ```

   with the line:

   ```
   Source = Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, [UseReadOnlyReplica = false]),
   ```

9.  Select **Done**.
10. Select **Close & Apply** from the ribbon to save the changes and close Power Query Editor.

-->
### <a name="how-do-i-change-or-clear-the-user-account-im-currently-using-to-connect-to-business-central-from-power-bi-desktop"></a><a name="perms"></a>Hvordan endrer eller tømmer jeg brukerkontoen jeg for øyeblikket bruker til koble til Business Central fra Power BI Desktop?

Gjør ett av følgende i Power BI Desktop:

1. Velg **Alternativer og innstillinger** > **Datakildeinnstillinger** på Fil-menyen.
2. Velg **Dynamics Business Central** i oversikten, og velg deretter **Slett tillatelser** > **Slett**.

Neste gang du kobler til Business Central for å hente data, blir du bedt om å logge på.

## <a name="performance"></a>[Ytelse](#tab/performance)

<!-- 17 -->

### <a name="is-it-faster-to-get-data-using-api-pages-than-using-web-services"></a>Går det raskere å hente data ved å bruke API-sider enn å bruke webtjenester?

Ja. Testene våre viser at API-sider er opptil 25 % mer effektive enn webtjenester.

<!-- 18 -->
### <a name="are-there-plans-to-have-a-mirror-on-the-azure-sql-database-instance-which-i-can-connect-to-directly"></a>Har dere planer om å ha et speil for Azure SQL-databaseforekomsten som jeg kan koble direkte til?

Nei. Ikke på dette tidspunktet. Du kan bare kommunisere med Business Central via API-er.

<!-- 19 -->
### <a name="loading-data-from-business-central-web-services-seems-slow-is-there-any-way-to-get-data-directly-from-the-sql-database-table"></a>Det går tregt å laste inn data fra Business Central-webtjenester. Går det an å hente data direkte fra SQL-databasetabellen?

Nei. Det går ikke an å få tilgang til databasen direkte, men det hjelper mye å bytte til API-sider (når den nye koblingen blir tilgjengelig).

## <a name="advanced"></a>[Avansert](#tab/advanced)
<!-- 1 -->

### <a name="are-there-plans-for-the-power-bi-connector-to-support-the-incremental-refresh-features-in-the-power-bi-service"></a>Kommer Power BI-koblingen til å støtte funksjonene for trinnvis oppdatering i Power BI-tjenesten?

Ja. Vi har dette på veikartet vårt.

<!-- 2 -->
### <a name="if-a-business-central-on-premises-solution-doesnt-have-internet-access-can-i-still-use-power-bi"></a>Hvis en lokal Business Central-løsning ikke har tilgang til Internett, kan jeg likevel bruke Power BI?
<!-- todo: please explain this one-->

Ja. I dette tilfellet kan du bruke Power BI Desktop lokalt og koble til Business Central lokalt. Når du er tilkoblet, kan du opprette og vise rapporter, men bare ikke publisere dem på Power BI-tjenesten. 
<!-- 20 -->
### <a name="are-there-any-plans-to-make-it-possible-to-replicate-business-central-online-databases-so-theyre-accessible-for-read-only-sql-queries-this-capability-would-support-incremental-refresh-and-be-a-lot-faster-than-apis-or-web-services"></a>Har dere planer om å gjøre det mulig å replikere Business Central Online-databaser slik at de er tilgjengelige for skrivebeskyttede SQL-spørringer? Denne funksjonen hadde støttet trinnvis oppdatering og vært mye raskere enn API-er eller webtjenester.

<!-- todo: what does "BC-Saas-DB-replicated DB accessible" mean? fixe-->
Ja. Vi har denne funksjonen på det langsiktige veikartet vårt. 

<!-- 21 -->
### <a name="if-i-use-azure-data-factory-to-get-data-from-business-central-and-consume-it-on-power-bi-will-that-help-in-increase-in-performance"></a>Hvis jeg bruker Azure Data Factory til å hente data fra Business Central og bruke dem i Power BI, bidrar dette til å øke ytelsen? 

Ja. Dette avanserte scenarioet bidrar til å holde Business Central effektivt fordi datatilgangen skjer via Azure Data Factory.

<!-- 22 -->
### <a name="are-there-any-plans-to-support-power-bi-deployment-pipelines-or-a-way-to-build-deployment-pipelines-for-pbi-reports-similar-to-extensions-or-maybe-even-a-simple-api-in-the-business-admin-center"></a>Har dere planer om å støtte Power BI-distribusjonspipeliner eller en måte å bygge distribusjonspipeliner for PBI-rapporter på, slik som for utvidelser? Eller kanskje til og med en enkel API i administrasjonssenteret for Business? 

Vi undersøker muligheter for denne funksjonen. Power BI har omfattende API-er for styring av rapportdistribusjoner. Hvis du vil ha mer informasjon, kan du se [Innføring i distribusjonspipeliner](/power-bi/create-reports/deployment-pipelines-overview).

### <a name="when-i-get-data-from-business-central-to-use-in-my-power-bi-reports-i-see-some-values-like-_x0020_-what-are-these-values"></a>Når jeg får data fra Business Central som skal brukes i Power BI-rapportene mine, ser jeg noen verdier som _x0020_. Hva er disse verdiene?

Enkelte API-sider, inkludert de fleste API v 2.0-sider, har felter basert på [AL-opplistingsobjekter](/dynamics365/business-central/dev-itpro/developer/devenv-extensible-enums). Felter basert på AL-opplistingsobjekter må ha navn som er konsekvente og alltid like, slik at filtre i rapporten alltid fungerer, uansett hvilket språk eller operativsystem du bruker. Derfor blir ikke feltene som er basert på AL-opplistinger, oversatt, og de blir kodet for å unngå ethvert spesialtegn, inkludert mellomrom. Det er særlig når er et tomt alternativ i AL-opplistingsobjektet, at det kodes til «_x0020_». Du kan alltid bruke en transformering på dataene i Power BI hvis du vil vise en annen verdi for disse feltene, for eksempel «Tom».


---

## <a name="see-also"></a>Se også

[Power BI-lisensiering](admin-powerbi-setup.md#license)
[Innføring i Business Central og Power BI](admin-powerbi.md)  
[Oversikt over Power BI-integrering](admin-powerbi-overview.md)  
[Aktivere Power BI i Business Central](admin-powerbi-setup.md)  
[Arbeide med Power BI-rapporter i Business Central](across-working-with-powerbi.md)  
[Arbeide med Business Central-data i Power BI](across-working-with-business-central-in-powerbi.md)  
[Bygge Power BI-rapporter for å vise Business Central-data](across-how-use-financials-data-source-powerbi.md)    
[Power BI-dokumentasjon](/power-bi/)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
