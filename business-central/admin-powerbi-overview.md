---
title: Oversikt over komponent og arkitektur for Power BI-integrering for Business Central | Microsoft Docs
description: Få informasjon om de ulike aspektene ved Power BI-integrering med Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: overview
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 04/26/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Oversikt over komponent og arkitektur for -integrering for Power BI

I denne artikkelen får du informasjon om de forskjellige aspektene ved Power BI-integrering med [!INCLUDE[prod_short](includes/prod_short.md)] for å gjøre det enklere å forstå hvordan du implementerer og bruker den.

## Komponenter

Tabellen nedenfor beskriver de hovedkomponentene som er involvert i Power BI-integrering.

|Komponent|Beskrivelse|
|---------|-----------|
|Power BI|En skybasert tjeneste for drifting og administrasjon av rapporter.|
|Power BI Desktop|Et redigeringsverktøy du bruker til å bygge rapporter og instrumentbord, og gjør at du kan kjøre rapporter. Det er tilgjengelig som en gratis nedlasting i Microsoft Store og installeres lokalt.|
|[!INCLUDE[prod_short](includes/prod_short.md)]|Online eller lokal løsning med koblinger som er eksponert for Power BI, og kan bygge inn en Power BI-del.|

## Hva som er tilgjengelig fra begynnelsen

Tabellen nedenfor beskriver tilgjengelige funksjoner.

|Funksjon|Støtte for [!INCLUDE[prod_short](includes/prod_short.md)] Online eller lokalt|
|-------|---------------------|
|Power BI-koblinger|Begge deler. Ulike koblinger for Online og lokalt. Samme kobling brukes for Power BI Desktop og Power BI-tjeneste. |
|Innebygd opplevelse for visning av en gitt rapport i en faktaboks i [!INCLUDE[prod_short](includes/prod_short.md)]|Begge deler. Må konfigureres for å kunne vise rapporter for den lokale versjonen.|
|Power BI-rapportadministrasjon fra [!INCLUDE[prod_short](includes/prod_short.md)]|Online|
|Standard Power BI-rapporter for rollesentre distribueres til Power BI|Online|
|Power BI-apper i Microsoft AppSource|Online|

## Arkitektur

[!INCLUDE[prod_short](includes/prod_short.md)] integreres med Power BI via en kobling som bruker OData. Datakilden for Power BI-rapporter eksponeres som API-sider og OData-nettjenester.

:::image type="content" source="./media/power-bi-architecture.svg" alt-text="Alternativ bildetekst." lightbox="./media/power-bi-architecture.svg":::

Fra og med februar 2022 blir Power BI-rapporter for [!INCLUDE[prod_short](includes/prod_short.md)] online hentet fra en sekundær, skrivebeskyttet databasereplika. Databasereplika er en del av funksjonen for å [lese skalering](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) i [!INCLUDE[prod_short](includes/prod_short.md)] online. Denne konfigurasjonen frigjør hoveddatabasen for transaksjoner, noe som forbedrer ytelsen i systemet. Å koble til den skrivebeskyttede database replikaen er en vesentlig del av Business Central Online-koblingen og krever ingen ekstra oppsett av deg. Alle nye rapporter kobler bare til den skrivebeskyttede databasereplikaen som standard. Gamle rapporter vil fortsatt bruke hoveddatabasen. Hvis du vil ha mer informasjon, kan du se [plan for lanseringsbølge 2 for 2021 for Business Central](/dynamics365-release-plan/2021wave2/smb/dynamics365-business-central/use-secondary-read-only-database-power-bi-reporting).

## Generell flyt

Diagrammet nedenfor viser den grunnleggende arbeidsflyten for brukere når du kobler [!INCLUDE[prod_short](includes/prod_short.md)] til Power BI.

![Power BI-arbeidsflyt for integrering med Business Central.](./media/power-bi-flow-v2.svg)

1. Brukeren registrerer seg for en Power BI-konto.
2. Brukeren kobler seg til Power BI fra [!INCLUDE[prod_short](includes/prod_short.md)].
3. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer lisensen.
4. [!INCLUDE[prod_short](includes/prod_short.md)] distribuerer standardrapporter til Power BI-tjenesten. Dette trinnet skjer bare for [!INCLUDE[prod_short](includes/prod_short.md)] Online.
5. [!INCLUDE[prod_short](includes/prod_short.md)] gjør rapporter i Power BI tilgjengelige for valg i [!INCLUDE[prod_short](includes/prod_short.md)]. Standardrapporter vises automatisk i Power BI-deler.
6. Brukeren oppretter en rapport i Power BI Desktop.
7. Brukeren publiserer rapporten til Power BI-tjenesten. Rapportene blir deretter tilgjengelige for valg i [!INCLUDE[prod_short](includes/prod_short.md)].

## Se også

[Business Central og Power BI](admin-powerbi.md)  
[Power BI for forbrukere](/power-bi/consumer/end-user-consumer)  
[Nytt utseende på Power BI-tjenesten](/power-bi/service-new-look)  
[Hurtigstart: Koble til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI-dokumentasjon](/power-bi/)  
[Forretningsintelligens](bi.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Importer forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Bruk [!INCLUDE[prod_short](includes/prod_short.md)] som en Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Bruk [!INCLUDE[prod_short](includes/prod_short.md)] som en Power Apps-datakilde](across-how-use-financials-data-source-powerapps.md)  
[Bruk [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
