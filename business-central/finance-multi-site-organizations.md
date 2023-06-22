---
title: Business Central for organisasjoner med flere lokasjoner og internasjonale organisasjoner | Microsoft Docs
description: Business Central har funksjoner som støtter en nav-og-eiker-forretningsmodell.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'hub-and-spoke, multi-site, headquarter, sites'
ms.date: 10/01/2020
ms.author: bholtorf
---

# <a name="business-central-for-multi-site-and-international-organizations" />Business Central for organisasjoner med flere lokasjoner og internasjonale organisasjoner
Organisasjoner med flere lokasjoner bruker ofte en nav-og-eiker-forretningsmodell der et moderselskap, eller hovedkontor, håndterer den generelle driften av virksomheten, mens hver lokasjon fungerer som en frittstående enhet. Lokasjoner er ofte geografisk spredt og har ulike behov for å dele informasjon med moderselskapet. Lokasjoner trenger vanligvis ikke samme grad av kompleksitet og har ofte ikke ressursene til å opprettholde et stort system.

[!INCLUDE[prod_short](includes/prod_short.md)] gir små og mellom store bedrifter en forretningsadministrasjonsløsning som er enkel å bruke og kan opprettholdes med lave eierkostnader.

Denne artikkelen gir en innføring i noen av måtene [!INCLUDE[prod_short](includes/prod_short.md)] støtter en nav-og-eiker-forretningsmodell på.

## <a name="integrating-the-headquarter-company-and-the-sites" />Integrering av moderselskapet og lokasjonene

[!INCLUDE[prod_short](includes/prod_short.md)] kan integreres med moderselskapets regnskapssystem mens det oppfyller de varierte behovene til ulike lokasjoner, uavhengig av størrelse, plassering eller virksomhetstype.

Diagrammet nedenfor er et eksempel på ulike lokasjoner som er integrert med et moderselskap.

![Automatisk generert beskrivelse av diagram.](media/multisite-headquarter-sites.png)

## <a name="meet-the-needs-of-domestic-and-international-sites" />Oppfylle behovene til innenlandske og internasjonale lokasjoner

Forretningsbehov på lokasjoner varierer etter bransje, forretningsmetoder eller relasjonen til moderselskapet. [!INCLUDE[prod_short](includes/prod_short.md)] kan lett tilpasses til og utvides for ulike typer virksomheter og lokasjoner. Microsoft AppSource har en rekke apper fra Microsoft og partnerne våre, og partnere kan raskt implementere [!INCLUDE[prod_short](includes/prod_short.md)] med minimalt avbrudd i den daglige driften.

Når det gjelder flernasjonale organisasjoner, støtter [!INCLUDE[prod_short](includes/prod_short.md)] lokale lovfestede krav og lokal forretningspraksis.

* Når det gjelder nettversjoner, finnes det flere enn [40 lokaliserte landsversjoner](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json) som du kan installere som utvidelser fra Microsoft AppSource.  
* Når det gjelder lokale versjoner, er [landsversjoner](/azure/architecture/solution-ideas/articles/business-central) tilgjengelige som Microsoft-lokaliserte versjoner eller partnerledede tilleggslokaliseringer.

Et nettverk med flere enn 4 000 Microsoft-partnere over hele verden tilbyr lokal ekspertise.

| **Forretningsbehov** | **Hvordan Business Central støtter det** | **Finn ut mer** |
|-------------------------|-------------------------|-------------------------|
| Skreddersy systemet til virksomheten. | Få et system som er utformet for mellomstore bedrifter fra starten av. | [Oversikt](https://dynamics.microsoft.com/business-central/overview/) |
| Følg forskriftsmessig og lokal praksis. | Følg lokale lovfestede krav og lokal forretningspraksis. | [Lokal funksjonalitet](about-localization.md) |
| Få tilgang til flere selskaper fra én side. | Få rask tilgang til ethvert Business Central-selskap i organisasjonen. | [Selskapshub](ui-extensions-company-hub.md) |
| Håndter flere språk og valutaer. | Støtte for flere språk og valutaer bidrar til å oppfylle lokale behov. | [Funksjoner for flere språk](about-locale-language.md)<br></br>[Funksjoner for flere valutaer](finance-how-setup-additional-currencies.md) |


## <a name="consolidate-financial-data" />Konsolidere økonomiske data

Et kjerneaspekt ved nav-og-eiker-forretningsmodellen er at moderselskapet og lokasjonene kan utveksle økonomiske data, selv når moderselskapet og lokasjonene bruker ulike systemer, regnskapsstrukturer, språk og valutaer.

| **Forretningsbehov** | **Hvordan Business Central støtter det** | **Finn ut mer** |
|-------------------------|-------------------------|-------------------------|
| Konsolider økonomiske data fra lokasjoner. | Konsolider årsregnskap for lokasjoner, uansett om de kjører Business Central eller et annet program, i én forretningsenhet (selskap). | [Konsolidere finansielle data fra flere selskaper](finance-consolidated-company-reporting.md) |
| Integrer regnskapsstrukturer. | Overfør konsolideringsdata fra ulike regnskapsstrukturer til din egen. Innebygd filformat for F&O (tilgjengelig i lanseringsbølge 2 for 2020) | [Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)<br></br>[Klargjøre finanskonti for konsolidering](finance-consolidated-company-reporting-setup.md#glacc) |
| Bruk flere valutaer. | Bidra til å sikre at årsregnskaper i ulike valutaer er nøyaktige og bruker riktige valutakurser. | [Oppdatere valutakurser](finance-how-update-currencies.md) |

## <a name="share-business-insight-with-integrated-analytics" />Dele forretningsinnsikt med integrert analyse

Rett inn organisasjonen etter forretningsmålene ved å sørge for en felles forståelse av virkeligheten. Integrert analyse kan hjelpe personer å basere beslutningene på de samme faktaene.

| **Forretningsbehov** | **Hvordan Business Central støtter det** | **Finn ut mer** |
|-------------------------|-------------------------|-------------------------|
| Del innsikt med lokasjoner uten omfattende IT-støtte. | Opprett KPI-er og instrumentbord for forretningsanalyse i Power BI basert på dataene. | [Arbeid med Business Central-data i Power BI](across-working-with-business-central-in-powerbi.md) |
| Utvikle egendefinerte finansrapporter. | Generer parameterbaserte finansrapporter. | [Forretningsintelligens](bi.md) |
| Bli enige om faktaene. | Generer, vis og del rapporter med interne og eksterne interessenter. | [Finansrapporter](finance-reports.md) |
| Analyser data i Excel. | Undersøk faktaene, feilsøk og foreta adhocanalyser i Microsoft Excel. | [Analysere årsregnskaper i Excel](finance-analyze-excel.md) |


## <a name="exchange-data-using-apis-and-xmlports" />Utveksle data ved hjelp av API-er og XMLport-er

API-er og XMLport-er gjør det enklere å koble sammen forekomster av [!INCLUDE[prod_short](includes/prod_short.md)], inkludert de som er tilpasset for hver lokasjon.

| **Forretningsbehov** | **Hvordan Business Central støtter det** | **Finn ut mer** |
|-------------------------|-------------------------|-------------------------|
| Koble sammen egendefinerte versjoner mellom lokasjoner og moderselskapet. | API-sider kan vise alle representasjoner av en enhet, inkludert tilpassingene. | [Aktivere API-er for Business Central](/dynamics-nav/enabling-apis-for-dynamics-nav) |
| Versjonskontroll og sikkerhet. | API-er bruker ODataV4, som gir versjonskontroll, og webhooks og endringssporing. | [Sikkerhet og beskyttelse](/dynamics365/business-central/dev-itpro/security/security-and-protection) |
| Bokfør og importer XML-dokumenter. | Kodeenheter kan vises som ubundne handlinger for å støtte bokføring og inntak av XML-dokumenter. XMLport-er kan brukes ved behandling av XML-dokumenter. Ubundne handlinger kan også generere et XML- eller JSON-dokument. | [XMLport-objekter](/dynamics365/business-central/dev-itpro/developer/devenv-xmlport-object) |
| Gjør vedlikehold enklere via elektronisk datautveksling. | Det går an å legge til en elektronisk datautvekslingsløsning som fungerer som et integreringslag mellom moderselskapet og lokasjonene. | [Rammeverket for datautveksling](across-about-the-data-exchange-framework.md) |
| Utveksle data mellom ulike systemer. | Bruk XMLport-er til å opprette XML-dokumenter, som deretter kan utveksles mellom et moderselskap som bruker ett system og lokasjoner som bruker Business Central. | [Oversikt over XMLport](/dynamics365/business-central/dev-itpro/developer/devenv-xmlport-overview) |
| Iverksett komplekse datautvekslinger. | Bruk en kombinasjon av XMLport-er med Business Central og Microsoft BizTalk Server til å oppfylle unike behov på lokasjonene.</br>Når det gjelder komplekse behov, bruker du en elektronisk datautvekslingsløsning basert på BizTalk Server og Commerce Gateway i Business Central sammen med XMLport-ene. | [Arbeid med rapporter, satsvise jobber og XMLport-er](ui-work-report.md) |
| Koble til tredjepartsløsninger og -tjenester. | API-er oppretter en punkt-til-punkt-forbindelse mellom Business Central og tredjepartsløsninger og -tjenester. | [API v2.0](/dynamics-nav/api-reference/v2.0/) |


## <a name="promote-an-efficient-intercompany-supply-chain" />Fremme en effektiv konsernintern forsyningskjede

Lokasjoner må ofte ha tilgang til forsyningskjeden og kunne håndtere visse aspekter ved den. Lokasjoner kan for eksempel bruke samme leverandør, men håndtere aktiva og fysiske lokasjoner separat.

| **Forretningsbehov** | **Hvordan Business Central støtter det** | **Finn ut mer** |
|-------------------------|-------------------------|-------------------------|
| Behandle transaksjoner mellom avdelinger som vanlige salgs- og kjøpstransaksjoner. | Bruk konsernintern bokføring til å opprette salgs- og kjøpsdokumenter og finansposter for hele arbeidsflyter, og for flere selskaper om gangen for å unngå registrering av dupliserte data. | [Behandle konserninterne transaksjoner](intercompany-manage.md) |
| Bruk papirløse fremgangsmåter. | Unngå kostnadene ved å sende, motta og skrive ut dokumenter. | [Inngående dokumenter](across-income-documents.md)<br><br> [Behandle vedlegg, koblinger og merknader på kort og dokumenter](ui-how-add-link-to-record.md) |

## <a name="respond-quickly-to-new-business-conditions" />Reagere raskt på nye forretningsforhold

Moderselskapet må kunne reagere raskt på forretningsendringer på hver lokasjon. Power Automate kan sammen med [!INCLUDE[prod_short](includes/prod_short.md)] fungere som en forvarselsmekanisme.

![Et skjermbilde av en automatisk generert beskrivelse av et innlegg på sosiale medier,](media/multisite-apps.png)

| **Forretningsbehov** | **Hvordan Business Central støtter det** | **Finn ut mer** |
|-------------------------|-------------------------|-------------------------|
| Generer e-postvarsler automatisk. | Konfigurer varsler i Power Automate som genererer e-postmeldinger med informasjon om kritiske forretningsforhold på lokasjoner eller hos forsyningskjedepartnere. | [Business Central og Power BI](admin-powerbi.md) |
| Bruk standard eller egendefinerte varsler. | Bruk tolv ulike maler som er inkludert for Business Central, eller konfigurer dine egne varsler som er tilpasset virksomheten. | [Bruk Business Central i en automatisk arbeidsflyt](across-how-use-financials-data-source-flow.md) |

## <a name="see-also" />Se også
[Administrasjon av Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
