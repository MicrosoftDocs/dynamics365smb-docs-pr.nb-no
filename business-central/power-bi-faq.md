---
title: Vanlige spørsmål om Power BI
description: Få svar på enkelte vanlige spørsmål om å arbeide med Power BI og Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Power BI, reports, faq, errors
ms.date: 04/22/2021
ms.author: jswymer
ms.openlocfilehash: 939b280e631113d3196f6fbbc90d9bf19b9fc408
ms.sourcegitcommit: a76475f124e79440a5bba20577b335c4d50a2d83
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025836"
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

Ikke ennå. Men den nye Power BI-koblingen får støtte for både Business Central-webtjenester og API-sider i juni 2021. Hvis du vil ha mer informasjon, kan du se [Aktivere Power BI-koblingen slik at den fungerer med API-er for Business Central, i stedet for bare webtjenester](/dynamics365-release-plan/2021wave1/smb/dynamics365-business-central/enable-power-bi-connector-work-business-central-apis-instead-web-services-only).

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

<!-- 8 and 9 -->

### <a name="for-embedding-reports-in-business-central-pages-right-now-its-only-possible-to-get-reports-from-my-workspace-in-power-bi-are-there-plans-to-make-it-possible-to-get-them-from-custom-workspaces"></a>Når det gjelder å bygge inn rapporter på Business Central-sider, kan du for øyeblikket bare hente rapporter fra *Mitt arbeidsområde* i Power BI. Har dere planer om å gjøre det mulig å hente dem fra egendefinerte arbeidsområder?

Ja. Vi har planer om å legge til støtte for delte arbeidsområder, men foreløpig har vi ingen timeplan for dette.  

<!-- 10 -->
### <a name="from-power-bi-besides-using-a-query-is-there-another-way-to-get-data-from-business-central-tables-that-dont-have-an-associated-page-for-example-like-the-item-attributes-value-mapping-table"></a>Finnes det en annen metode i Power BI – enn å bruke en spørring – til å hente data fra Business Central-tabeller som ikke har en tilknyttet side? Slik som for eksempel tabellen *Tilordning av verdi for vareattributt*.

Nei. Ikke på dette tidspunktet.

<!-- 12 --> 
### <a name="are-published-queries-faster-to-use-than-published-pages"></a>Går det raskere å bruke publiserte spørringer enn publiserte sider?

Når det gjelder webtjenester, går det vanligvis raskere å bruke publiserte spørringer enn tilsvarende publiserte sider. Årsaken er at spørringer er optimalisert for lesing av data og ikke inneholder kostbare utløsere som OnAfterGetRecord.

Når den nye koblingen er tilgjengelig i juni 2021, oppfordres du til å bruke API-sider i stedet for spørringer som er publisert som webtjenester.

<!-- 13 --> 
### <a name="is-there-a-way-for-an-end-user-to-create-a-web-service-with-a-column-thats-in-a-business-central-table-but-not-a-page-or-will-developer-have-to-create-a-custom-query"></a>Kan en sluttbruker opprette en webtjeneste med en kolonne som er i en Business Central-tabell, men ikke på en side? Eller må utvikleren opprette en egendefinert spørring? 

Ikke ennå. Men når den nye koblingen er tilgjengelig i juni 2021, kan en utvikler lage en ny API-side som oppfyller dette kravet. 

<!-- 28 --> 
### <a name="can-i-connect-power-bi-to-a-read-only-database-server-of-business-central-online"></a>Kan jeg koble Power BI til en skrivebeskyttet databaseserver for Business Central Online? 

Nei. Men vi har denne funksjonen på det langsiktige veikartet vårt. 

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

### <a name="ive-tried-the-preview-of-the-new-connector-which-will-be-live-in-june-2021-i-see-some-values-like-_x0020_-when-connecting-to-api-v20-what-are-these-values"></a>Jeg har prøvd forhåndsversjonen av den nye koblingen som blir tilgjengelig i juni 2021. Jeg ser enkelte verdier som «_x0020_» når jeg kobler til API v2.0. Hva er disse verdiene?

Den kommende versjonen av Power BI-koblingen gjør at du kan koble deg til API-sidene for Business Central, inkludert API v2.0. Disse sidene omfatter enkelte felter basert på [AL Enum-objekter](/dynamics365/business-central/dev-itpro/developer/devenv-extensible-enums). Felter basert på AL-opplistingsobjekter må ha navn som er konsekvente og alltid like, slik at filtre i rapporten alltid fungerer, uansett hvilket språk eller operativsystem du bruker. Derfor blir ikke feltene som er basert på AL-opplistinger, oversatt, og de blir kodet for å unngå ethvert spesialtegn, inkludert mellomrom. Det er særlig når er et tomt alternativ i AL-opplistingsobjektet, at det kodes til «_x0020_». Du kan alltid bruke en transformering på dataene i Power BI hvis du vil vise en annen verdi for disse feltene, for eksempel «Tom».


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