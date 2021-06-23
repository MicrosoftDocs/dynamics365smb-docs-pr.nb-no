---
title: Vanlige spørsmål om Teams
description: Få svar på enkelte vanlige spørsmål om å arbeide med Teams og Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, faq, errors
ms.date: 05/19/2021
ms.author: jswymer
ms.openlocfilehash: f3c9626fa73247b2109e5f179aef405e80b44b07
ms.sourcegitcommit: 5a916b0aa0a2eef0c22b5722a0af041757e6d7c2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/19/2021
ms.locfileid: "6074643"
---
# <a name="teams-faq"></a>Vanlige spørsmål om Teams

[!INCLUDE [online_only](includes/online_only.md)]

Denne artikkelen besvarer noen av spørsmålene du kan ha om å arbeide med Teams og [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="general"></a>[Generelt](#tab/general)

### <a name="how-do-i-sign-in-to-the-prod_shortmd-app-in-teams"></a>Hvordan logger jeg på [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen i Teams?

Når du har installert appen, blir du bedt om å logge på første gang du bruker appen, når du limer inn en [!INCLUDE [prod_short.md](includes/prod_short.md)]-kobling i Teams-chatten, eller når du velger handlingen **Detaljer** på et kort i Teams. Avhengig av Teams-klienten må du kanskje angi legitimasjonen du vil bruke til å få tilgang til [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="how-do-i-sign-out-of-the-prod_shortmd-app-in-teams"></a>Hvordan logger jeg av [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen i Teams?

Hvis du vil logge av gjeldende brukeridentitet i Teams som brukes til å koble til [!INCLUDE [prod_short.md](includes/prod_short.md)], går du til en chatskriveboks, høyreklikker [!INCLUDE [prod_short.md](includes/prod_short.md)]-ikonet nedenfor og velger deretter **Innstillinger**. Når vinduet vises, kontrollerer du din identitet som er logget på, og deretter velger du **Logg av**.

### <a name="does-the-app-for-teams-connect-to-prod_shortmd-on-premises"></a>Kobles appen for Teams til [!INCLUDE [prod_short.md](includes/prod_short.md)] lokalt? 

Antall [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Teams fungerer bare [!INCLUDE [prod_short.md](includes/prod_short.md)] på nettet. Det finnes ingen planer om å støtte [!INCLUDE [prod_short.md](includes/prod_short.md)]-distribusjonstyper som lokal, hybrid sky eller privat sky, som Microsoft ikke er vert for eller administrerer direkte.

### <a name="does-the-app-work-with-multiple-companies-and-environments"></a>Fungerer appen med flere selskaper og miljøer? 

Ja. Hvis du vil søke etter kontakter i et annet selskap, går du til [Innstillinger](across-teams-settings.md). Når [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen utvider en kobling til et kort, må koblingen inneholde miljøet og selskapsnavnene for appen for å samsvare med posten i det riktige selskapet. Du kan lime inn koblinger til alle selskaper og miljøer du har tilgang til, i organisasjonen, og fra [!INCLUDE [prod_short.md](includes/prod_short.md)]-kontoen du brukte til å logge på. Deltakerne på chatten vil se kortet. De kan imidlertid ikke vise kortdetaljene med mindre de har tillatelser til selskapet eller miljøet der den aktuelle posten er lagret.

### <a name="in-which-countries-or-regions-is-the-prod_shortmd-app-available"></a>I hvilke land eller områder er [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen tilgjengelig? 

[!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Teams er ikke begrenset av land eller område. Appen er tilgjengelig i alle markeder som for øyeblikket støttes av Teams-markedsplassen. 

### <a name="does-the-prod_shortmd-app-work-with-any-localization-of-prod_shortmd"></a>Fungerer [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen sammen med en hvilken som helst lokalisering av [!INCLUDE [prod_short.md](includes/prod_short.md)]? 

Ja. Appen er ment å fungere med en hvilken som helst lokalisering av [!INCLUDE [prod_short.md](includes/prod_short.md)], om denne lokaliseringen tilbys direkte fra Microsoft eller via en partner. Hvis du vil ha mer informasjon, kan du se [Land-/områdetilgjengelighet og støttede oversettelser](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).

### <a name="which-languages-does-the-prod_shortmd-app-support"></a><a name="language"></a>Hvilke språk støtter [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen?

To ting avgjør hvilket språk som brukes for kort og kortdetaljer i Teams:

1. Språket ditt i Teams, som du kan se fra kontoinnstillingene i Teams. 
2. Språket ditt i [!INCLUDE [prod_short.md](includes/prod_short.md)], som du kan se i [!INCLUDE [prod_short.md](includes/prod_short.md)]-nettklienten (se [Endre grunnleggende innstilling – språk](ui-change-basic-settings.md#language)).

Tabellen nedenfor inneholder informasjon om hvordan funksjonen er forskjellig for meldingsforfattere og mottakere, avhengig av språkinnstillinger og tilgjengeligheten av språk.

|Hvem|Kort|Kortdetaljer |
|-|----|--------------| 
|Meldingsforfatter |Vises på språket som er angitt for deg i Teams. Hvis [!INCLUDE [prod_short.md](includes/prod_short.md)] ikke tilbyr dette språket, vises kortet på engelsk. |Vises på språket som er angitt for deg i [!INCLUDE [prod_short.md](includes/prod_short.md)].  som kan omfatte språk fra språkapper som tilbys av partnere. |
|Meldingsmottaker |Vises på språket til meldingsforfatteren. |Vises på språket som er angitt for deg i [!INCLUDE [prod_short.md](includes/prod_short.md)]. |

Hvis du vil listen over støttede språk for [!INCLUDE [prod_short.md](includes/prod_short.md)], kan du se [Støttede språk](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json#supported-languages).

### <a name="does-the-prod_shortmd-app-work-with-industry-solutions"></a>Fungerer [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen med bransjeløsninger?

Ja. Men bare noen av funksjonene i appen fungerer med [Innebygde apper](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview):

- Appen fungerer med koblinger basert på mønsteret **\*.bc.dynamics.com** som vanligvis brukes med Bygg inn apper.
- Kontaktsøk er ikke tilgjengelig for Bygg inn apper som erstatter basisprogrammet fra Microsoft.

### <a name="where-can-i-find-teams-integration-inside-the-prod_shortmd-web-client"></a>Hvor finner jeg Teams-integrering i [!INCLUDE [prod_short.md](includes/prod_short.md)]-nettklienten? 

Det finnes for øyeblikket ingen innbygging av Teams-kontroller eller tilgjengelighet av Teams-funksjoner i [!INCLUDE [prod_short.md](includes/prod_short.md)]-nettklienten eller andre klienter.

### <a name="does-prod_shortmd-work-with-the-teams-mobile-app"></a>Fungerer [!INCLUDE [prod_short.md](includes/prod_short.md)] med Teams-mobilappen?

Ja. [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen kan installeres fra Teams-skrivebordsappen eller nettleseren, eller av en administrator for alle brukere. Når den er installert, er [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen automatisk tilgjengelig i Teams for iOS og Android. På mobile enheter kan du bare vise kort som er sendt av andre, tilgangsdetaljer eller åpne kortet til fullskjerm i [!INCLUDE [prod_short.md](includes/prod_short.md)]-mobilappen. Du kan ikke lime inn koblinger som utvides til kort når du skriver meldinger eller søker etter kontakter. Se [Minimumskrav for bruk av Business Central](product-requirements.md) for minimumskrav for mobil.

### <a name="is-the-prod_shortmd-app-for-teams-the-same-as-the-prod_shortmd-app-for-ios-and-android"></a>Er [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Teams det samme som [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for iOS og Android?

Antall Appen for Teams er et tillegg til Microsoft Teams og eksklusivt utformet for samarbeidsfunksjoner som lyses opp i Teams. På den andre siden leverer [!INCLUDE [prod_short.md](includes/prod_short.md)]-mobilappen en flott opplevelse der du kan arbeide med [!INCLUDE [prod_short.md](includes/prod_short.md)]-data på mobile enheter.

Mobilbrukere oppfordres til å installere både mobilappen og appen for Teams for å få mest mulig ut av [!INCLUDE [prod_short.md](includes/prod_short.md)]. Når begge er installert, kan du velge **Eget vindu**-handlingen på et kort i Teams for å åpne kortdetaljene i [!INCLUDE [prod_short.md](includes/prod_short.md)]-mobilappen. Hvis du vil ha informasjon om hvordan du installerer [!INCLUDE [prod_short.md](includes/prod_short.md)] og Teams-mobilappene, kan du se:

- [Få Business Central på mobilenheten din](install-mobile-app.md)
- [Få Teams-mobilapp](https://support.microsoft.com/office/download-the-mobile-app-for-teams-5940ebdc-0082-4fb1-83c4-751edc23dcb5) på Microsoft Kundestøtte

### <a name="does-the-prod_shortmd-app-work-in-all-teams-clients"></a>Fungerer [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen i alle Teams-klienter?

Antall [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Teams støttes ikke når den er installert som en pakke for macOS eller Linux. På disse plattformene kan du få tilgang til Teams ved hjelp av en støttet nettleser i stedet.

Se [Minimumskrav for bruk av Business Central](product-requirements.md#teams) for minimumskrav i [!INCLUDE [prod_short.md](includes/prod_short.md)].

Hvis du vil ha mer informasjon om valg av Teams-klienter og hvordan du installerer dem, kan du se [Få klienter for Microsoft Teams](/microsoftteams/get-clients) i Teams-dokumentasjonen.

### <a name="which-teams-client-is-best-for-prod_shortmd"></a>Hvilke Teams-klienter er best for [!INCLUDE [prod_short.md](includes/prod_short.md)]?

Det er bare små forskjeller og begrensninger mellom Teams-klienter som kan påvirke opplevelsen med [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Teams. Når du velger en Teams-klien, må du vurdere følgende:

- Du får ikke tilgang til kameraet og plasseringen i detaljvinduet i Teams-skrivebordsappen.
- Du kan ikke aktivere telefonnumre fra vinduet Detaljer i Teams for iOS, Teams for Android eller Teams i nettleseren.
- Når du bruker Microsoft Edge med Teams i nettleseren, kan du enkelt arbeide på tvers av flere identiteter og kontoer ved å logge på Teams fra forskjellige profiler. Hvis du finne ut mer å bruke profiler i Microsoft Edge, kan du se [Logg på og opprett flere profiler i Microsoft Edge](https://support.microsoft.com/office/sign-in-and-create-multiple-profiles-in-microsoft-edge-df94e622-2061-49ae-ad1d-6f0e43ce6435) på Microsoft Kundestøtte.

### <a name="what-is-the-best-way-for-me-to-demonstrate-prod_shortmd-and-microsoft-teams-to-prospective-customers"></a>Hva er den beste måten for meg å vise frem [!INCLUDE [prod_short.md](includes/prod_short.md)] og Microsoft Teams til potensielle kunder?

Hvis du er en partner for videresalg, vil du kanskje ha et miljø som du kan vise kundeemner som en del av demonstrasjoner av forhåndssalg. Hvis du vil unngå å påvirke Microsoft Teams i organisasjonen, kan du få en Microsoft 365-demokonto på [https://aka.ms/CDX](https://aka.ms/CDX). Denne kontoen gir deg full kontroll over en uavhengig Azure-organisasjon som inkluderer Microsoft Teams og [!INCLUDE [prod_short.md](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Klargjøre demonstrasjonsmiljøer av Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment).

### <a name="does-the-prod_shortmd-app-for-teams-cater-for-my-customization-and-personalization"></a>Kan [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Teams tilpasses og personaliseres?

[!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Teams kan vise kort for koblinger til kundesider og -tabeller i [!INCLUDE [prod_short.md](includes/prod_short.md)], for eksempel sidene og tabellene som kommer fra tilpassede tillegg eller fra AppSource.

Feltene som vises på et kort i Teams, kan også påvirkes av [!INCLUDE [prod_short.md](includes/prod_short.md)]-tilpasninger som er installert for organisasjonen. Kort tar ikke hensyn til rollespesifikke tilpasninger eller brukertilpasning. Kortdetaljvinduet viser imidlertid postdetaljer slik du ser dem i [!INCLUDE [prod_short.md](includes/prod_short.md)], deriblant alle utvidelser, rolletilpasninger og brukertilpasning.

Når du søker etter kontakter, påvirkes feltene som samsvarer med tabellen **Kontakter** og feltene som vises i søkeresultatene, ikke av egendefineringer eller tilpassinger.

### <a name="how-do-the-permissions-required-by-the-app-affect-my-privacy"></a>Hvordan påvirker tillatelsene som kreves av appen, personvernet mitt?

Før du installerer [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Teams, kan du gå gjennom minimumstillatelsene som kreves for at appen skal fungere. Når du installerer appen, godtar du at appen har tillatelse til å motta meldinger og data som du oppgir, og at Teams har tillatelse til å lagre og behandle disse meldingene.

Enkelte [!INCLUDE [prod_short.md](includes/prod_short.md)]-funksjoner krever også eksterne koblinger eller tilgang til kameraet eller geografisk plassering. La oss for eksempel anta at du vil ta et bilde av en kjøpsfaktura for behandling. [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen bruker ikke disse funksjonene uten ditt samtykke, og de brukes bare av bestemte funksjoner i **Detaljer**-vinduet. Når du bruker en av disse funksjonene for første gang, vises en dialogboks i Teams der du blir bedt om å gi tilgang til de nødvendige enhetsegenskapene.

- På Teams-skrivebordet går du gjennom og justerer apptillatelser fra **Innstillinger**-vinduet. Velg profilbildet ditt øverst i appen, velg **Innstillinger** > **Tillatelser**, og velg deretter [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen.

- For Teams i nettleseren og Teams for iOS eller Android kan du gå gjennom eller endre tillatelsene fra nettleser- eller enhetsinnstillingene.

> [!NOTE]
> Nøyaktig hvilke [!INCLUDE [prod_short.md](includes/prod_short.md)]-funksjoner som ber deg om tillatelser, avhenger av hvilke tilleggsapper og tilpasninger som er brukt i [!INCLUDE [prod_short.md](includes/prod_short.md)]-miljøet du kobler til.

### <a name="where-can-i-learn-about-my-privacy"></a>Hvor kan jeg finne ut mer om personvernet mitt? 

Du kan finne ut mer om hvordan Microsoft håndterer opplysningene dine i [Microsofts personvernerklæringen](https://go.microsoft.com/fwlink/?linkid=2030602). 

Kontakt administratoren for å finne ut hvordan organisasjonen håndterer personvernet til opplysningene dine.

### <a name="how-do-i-uninstall-the-prod_shortmd-app-for-teams"></a>Hvordan avinstallerer jeg [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Teams?

Hvis du vil fjerne appen du installerte selv, kan du gå til en chatmeldingsboks, finne [!INCLUDE [prod_short.md](includes/prod_short.md)]-ikonet under boksen, høyreklikke ikonet og velge **Avinstaller**.  

### <a name="will-microsoft-continue-to-improve-the-prod_shortmd-app-for-teams"></a>Vil Microsoft fortsette å forbedre [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Teams?

Hos Microsoft hører vi konstant på tilbakemelding fra våre mange brukerfellesskap og agerer på de mest populære forslagene. Hvis du vil finne ut hva som skjer videre for [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Teams, kan du se [Dynamics 365-lanseringsplanen](/dynamics365-release-plan/2021wave1/).

Hvis du ønsker ta del i forbedre appen for Teams, eller hvis du har en idé som kan bidra til å forenkle arbeidet eller samarbeidsfunksjonene i Teams, kan du legge til en idé eller stemme på eksisterende idéer på [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

## <a name="searching-for-contacts"></a>[Søke etter kontakter](#tab/contacts)

### <a name="which-tables-does-the-app-search-in"></a>Hvilke tabeller søker i programmet i?

Når du søker etter kontakter fra [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Teams, samsvarer søkebetingelsene med postene i tabellen **Kontakter** i [!INCLUDE [prod_short.md](includes/prod_short.md)]. 

### <a name="which-fields-in-the-contacts-table-can-i-search"></a>Hvilke felt i tabellen Kontakter kan jeg søke i?

Når du skriver inn søkeordene i søkeboksen, sammenlignes vilkårene med de fleste feltene i tabellen **Kontakter**. Feltene inkluderer for eksempel **Nr.**, **Navn**, **Adresse** og **Telefonnr.** eller **Mobiltelefonnr.** og **E-post**. 

Søkeord samsvarer ikke med egendefinerte felter som legges til i tabellen **Kontakter** etter apper og utvidelser.

### <a name="do-search-results-include-companies-and-persons"></a>Inkluderer søkeresultater selskaper og personer?

Ja. I [!INCLUDE [prod_short.md](includes/prod_short.md)] kan kontakter være av typen **Selskap** eller **Person**, der én eller flere personer kan knyttes til et selskap. I søkeresultatene har selskaper og personer ulike ikoner.

### <a name="do-contacts-of-any-business-relationship-appear-in-the-results"></a>Vises det kontakter for forretningsforbindelser i resultatet?

Ja. Noen kontakter kan representere kunder eller leverandører, eller begge deler. Andre kontakter uten definert forretningsforbindelse representerer vanligvis potensielle kunder. Kontakter med andre forretningsforbindelser, inkludert eventuelle egendefinerte relasjoner du har konfigurert i [!INCLUDE [prod_short.md](includes/prod_short.md)], vil også vises i søke resultatene.

### <a name="can-i-look-up-contact-details-during-meetings"></a>Kan jeg slå opp kontaktdetaljer under møter?

Ja. Du kan slå opp kontaktinformasjon, samhandlingslogg og relaterte dokumenter for kunden eller leverandøren under et Teams-møte eller en samtale mens møtet pågår, uten å måtte gå ut av Teams.

Du kan faktisk slå opp kontaktdetaljer fra Teams ved å bruke kommandoboksen. Du kan for eksempel slå opp kontaktdetaljer fra Teams-kalenderen for å gjøre det enklere å arrangere møter.

### <a name="how-do-i-view-my-last-interactions-with-a-contact"></a>Hvordan viser jeg min siste samhandling med en kontakt?

Detaljer-vinduet for en kontakt viser samhandlingsposter. Samhandlingspostene angir historikken for samhandlinger som organisasjonen har hatt med den bestemte kontakten. Samhandlingene kan omfatte e-postmeldinger du har utvekslet, samtaler du har mottatt eller dokumenter du har sendt.

For at samhandlinger skal kunne vises, må [!INCLUDE [prod_short.md](includes/prod_short.md)] være konfigurert for å spore samhandlinger. Hvis du vil finne ut mer om å logge samhandlinger, kan du se [Registrere samhandlinger med kontakter](marketing-interactions.md).

### <a name="how-do-i-register-a-teams-call-or-meeting-as-an-interaction"></a>Hvordan registrerer jeg en Teams-samtale eller et møte som en samhandling?

Fra detaljvinduet til en kontakt finner du handlingen **Opprett samhandling**, og deretter velger du fra innkommende eller utgående samtaler som samhandlingsmaler. Du kan også opprette egendefinerte samhandlingsmaler spesielt for bruk med Teams-samtaler.

### <a name="can-i-call-a-contact-from-the-prod_shortmd-app-for-teams"></a>Kan jeg ringe en kontakt fra [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Teams?

[!INCLUDE [prod_short.md](includes/prod_short.md)] har begrenset integrering med funksjoner for Teams-oppringing. Det er ikke mulig å starte en VOIP-samtale direkte fra vinduet Kontaktkort eller Kontaktopplysninger. Når du viser kontaktopplysninger i appen Teams-skrivebord, kan du imidlertid velge feltet Telefonnummer for å slå nummeret hvis de er konfigurert som standard oppringingsprogram på enheten. Hvis du vil ringe fasttelefon- eller mobiltelefonnumre ved hjelp av PSTN, som er det tradisjonelle telefonsystemet, krever Teams at du har Microsoft 365 Business Voice-appen. Hvis du vil ha mer informasjon, kan du se se [Hva er Microsoft 365 Business Voice?](/MicrosoftTeams/business-voice/whats-business-voice).

### <a name="how-do-i-view-recent-documents-for-a-customer-or-vendor"></a>Hvordan viser jeg nylig brukte dokumenter for en kunde eller leverandør?

[!INCLUDE [prod_short.md](includes/prod_short.md)] relaterer vanligvis en kontakt til en kunde- eller leverandørpost som i sin tur er relatert til forretningstransaksjonsposter, for eksempel salgstilbud eller kjøpsfakturaer. Hvis du vil vise relaterte dokumenter for en kontakt, går du til vinduet Detaljer for kontakten, velger feltverdien **Forretningsforbindelse**, eller bruker handlingene til å gå til den tilknyttede kunden eller leverandøren. På kunde-eller leverandørsiden utvider du faktaboksruten for å vise statistikk for ulike dokumenter som du kan vise detaljer om. Det kan hende at opplevelsen varierer basert på egendefinering og tilpassing.

### <a name="how-do-i-search-for-contacts-using-special-characters"></a>Hvordan søker jeg etter kontakter ved hjelp av spesialtegn?

Du kan angi søkevilkår med nesten alle Unicode-tegn. [!INCLUDE [prod_short.md](includes/prod_short.md)] reserverer imidlertid følgende symboler for andre bruksområder: **=**, **.**, **\**_ og _*@**. Det kan hende du ikke får forventet resultat ved å bruke disse symbolene i søkeordene. Hvis du ikke ser de forventede resultatene, setter du symbolene i søkeordene med enkle anførselstegn, for eksempel **Contoso'='2**.

### <a name="how-can-i-search-contacts-stored-in-a-different-company"></a>Hvordan kan jeg søke etter kontakter som er lagret i et annet selskap?

[!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Teams kan søke etter kunder, leverandører og andre kontakter i ett selskap om gangen.  
Hvis du vil søke etter kontakter som er lagret i et annet [!INCLUDE [prod_short.md](includes/prod_short.md)]-selskap, åpner du [Innstillinger](across-teams-settings.md), og deretter endrer du miljøet og selskapet derfra.

### <a name="are-prod_shortmd-contacts-different-than-the-ones-in-the-teams-contacts-screen"></a>Er [!INCLUDE [prod_short.md](includes/prod_short.md)]-kontakter annerledes enn dem på skjermen for Teams-kontakter?

Ja. Kontakter som er lagret i [!INCLUDE [prod_short.md](includes/prod_short.md)], representerer forretningskontakter som er tilgjengelige for organisasjonen. De er kontakter med et etablert og godt definert forretningsforhold, eller kontakter som representerer potensielle kunder. Disse kontaktene er vanligvis eksterne kontakter. Til sammenligning er kontaktene som vises i samtalelisten i Teams, dine egne kontakter. Disse kontaktene deles ikke nødvendigvis med andre i organisasjonen, og de representerer vanligvis bare kontakter som er interne for organisasjonen.

### <a name="does-prod_shortmd-synchronize-contacts-with-teams"></a>Synkroniserer [!INCLUDE [prod_short.md](includes/prod_short.md)] kontakter med Teams?

Antall Kontakter som er lagret i [!INCLUDE [prod_short.md](includes/prod_short.md)], er atskilt fra kontakter som er lagret i Teams.
Det er for tiden ingen planer om å synkronisere de to listene sammen.

### <a name="what-is-the-minimum-version-of-prod_shortmd-for-contact-search"></a>Hva er minimumsversjonen av [!INCLUDE [prod_short.md](includes/prod_short.md)] for kontaktsøk?

Kontaktsøk krever at du har installert [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Teams-versjon 1.0.4 eller senere, og at du kobler til [!INCLUDE [prod_short.md](includes/prod_short.md)]-miljøer med versjon 18 eller senere.

### <a name="can-i-search-from-my-mobile-device"></a>Kan jeg søke fra min mobile enhet?

Kontaktsøk er ikke tilgjengelig fra Teams for iOS og Teams for Android for øyeblikket.

### <a name="which-permissions-do-i-need-for-contact-search"></a>Hvilke tillatelser trenger jeg for kontaktsøk?

Hvis du vil søke etter kontakter, trenger du tillatelse på objektnivå for tabellen **Kontakter** i [!INCLUDE [prod_short.md](includes/prod_short.md)]-selskapet du søker i. Hvis du vil vise vinduet Detaljer for en kontakt, må du ha minst lesetillatelse til siden **Kontakt** i [!INCLUDE [prod_short.md](includes/prod_short.md)]-selskapet, og andre eventuelle relaterte objekter.

### <a name="can-i-use-contact-search-if-im-a-delegated-admin"></a>Kan jeg bruke kontaktsøk hvis jeg er delegert administrator?

Ja. Du kan også slå opp kontakter og kontaktopplysninger hvis du har en delegert administratorrolle i en organisasjon.

### <a name="is-contact-search-affected-by-api-limits"></a>Påvirkes kontaktsøket av API-begrensninger?

Ja. Søk etter kontakter fra Teams er basert på API-er for [!INCLUDE [prod_short.md](includes/prod_short.md)] v 2.0, og er underlagt eventuelle API-grenser som styrer bruken. Du kan lære mer om begrensningene under [Gjeldende API-begrensninger](/dynamics-nav/api-reference/v2.0/dynamics-current-limits).

### <a name="why-does-it-sometimes-ask-me-to-set-up-the-app"></a>Hvorfor blir jeg noen ganger bedt om å konfigurere appen?

Etter at du har logget på [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Teams for første gang, prøver appen å fastslå det foretrukne selskapet i [!INCLUDE [prod_short.md](includes/prod_short.md)]. Hvis appen ikke kan fastslå selskapet, må du kanskje gå til **Innstillinger** og velge selskapet du vil søke i. Denne situasjonen oppstår for eksempel hvis du har tilgang til flere selskaper på tvers av miljøer i organisasjonen. I dette tilfellet må du velge et selskap før du kan begynne å søke.  

Appen kan også be deg om å gå til **Innstillinger** hvis du ikke har et [!INCLUDE [prod_short.md](includes/prod_short.md)]-abonnement, det ikke finnes noen [!INCLUDE [prod_short.md](includes/prod_short.md)]-miljøer eller kontoen din ikke har en [!INCLUDE [prod_short.md](includes/prod_short.md)]-lisens.

### <a name="id-like-to-search-for-items-or-records-from-other-tables-can-i-do-this-from-teams"></a>Jeg vil gjerne søke etter varer eller poster fra andre tabeller. Kan jeg gjøre dette fra Teams?

Det er ikke mulig å søke i andre tabeller på dette tidspunkt. [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Teams søker bare i kontaktlisten i [!INCLUDE [prod_short.md](includes/prod_short.md)], som kan omfatte leverandører, kunder og andre kontakter.

Hvis du vil at søkefunksjonene skal utvikle seg til å inkludere andre tabeller, oppfordres det til å legge til en idé eller stemme med eksisterende ideer på https://aka.ms/BusinessCentralIdeas.

## <a name="working-with-cards"></a>[Arbeide med kort](#tab/cards)

### <a name="which-types-of-links-does-the-app-support"></a>Hvilke typer koblinger støtter appen?

[!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Teams kan agere på de fleste [!INCLUDE [prod_short.md](includes/prod_short.md)]-nettklientkoblingene. Når koblingen refererer til én post på en side, vil kortet vise felter for den aktuelle posten. De støttede sidetypene omfatter: 

- Kortsider, for eksempel Vare-kortet
- Dokumentsider, for eksempel Ordre-dokument
- ListPlus-sider som representerer en enkelt post som er satt sammen av andre poster, for eksempel oppgave for bankkontoavstemming
- Enkle listesider der en post ikke gir deg mulighet til å drille ned til en egen detaljside, for eksempel listen over postnumre

Når du limer inn en kobling til URL-adressen for den primære nettklienten, for eksempel https://businesscentral.dynamics.com, viser kortet i stedet informasjon som hjelper nye brukere med å få tilgang til [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="how-do-i-delete-a-card-i-sent-to-a-chat"></a>Hvordan sletter jeg et kort jeg har sendt til en chat?

Du kan ikke slette et kort du allerede har sendt til chat. Du kan imidlertid slette hele meldingen som kortet er en del av.

Som forfatter av meldingen kan du slette alle meldinger du har sendt til chat, med en person, gruppe eller kanal, med mindre administratoren har konfigurert policyer som forhindrer at meldinger slettes. Hvis du modererer en kanal som en kanaleier, kan administratoren også ha gitt deg tillatelse til å slette meldinger i kanalen, deriblant meldinger som er sendt av andre brukere.

Når du sletter en melding som inneholder et kort, slettes eller påvirkes ikke noen data i [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="do-cards-always-show-up-to-date-information"></a>Viser kort alltid oppdatert informasjon?

Antall Feltverdiene på et kort i Teams, deriblant bilder, er basert på dataene som er tilgjengelige når kortet ble sendt til chatten. [!INCLUDE [prod_short.md](includes/prod_short.md)]-kort oppdateres ikke automatisk i Teams. 

### <a name="will-others-see-my-card-if-they-dont-have-the-prod_shortmd-app-for-teams"></a>Vil andre se kortet mitt hvis de ikke har [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Teams? 

Når du skriver og sender en melding til chat som inneholder et kort, vil alle brukere se kortet, selv om de ikke har installert [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Teams.

### <a name="how-do-i-find-out-which-company-a-card-in-teams-belongs-to"></a>Hvordan finner jeg ut hvilket selskap et kort i Teams tilhører?

Hvis du arbeider på tvers av [!INCLUDE [prod_short.md](includes/prod_short.md)]-selskaper, må du snakke med systemansvarlig om å aktivere et firmakort for hvert selskap. Når dette alternativet er aktivert, vises dette iøynefallende tipset i alle detaljvinduer i Teams, med selskapet og miljøene som posten tilhører. Hvis du vil vite hvordan du oppretter firmakort, kan du se [Vise et selskapsmerke for rask tilgang til selskapsinformasjon](ui-change-basic-settings.md#badge).

## <a name="working-with-card-details"></a>[Arbeide med kortdetaljer](#tab/carddetails)

### <a name="where-is-the-save-button-in-the-details-window-in-teams"></a>Hvor er Lagre-knappen i detaljvinduet i Teams?

[!INCLUDE [prod_short.md](includes/prod_short.md)] lagrer automatisk endringer du gjør i felter så snart du går ut av feltet. Hvis du vil forlate et felt, klikker/trykker du hvor som helst utenfor feltet eller bruker TAB-tasten til å flytte til det neste feltet. Når data vises i en dialogboks i detaljvinduet, må du kanskje velge **OK** for å [!INCLUDE [prod_short.md](includes/prod_short.md)] lagre endringene.

### <a name="if-i-choose-to-view-details-for-a-card-will-other-users-see-my-details-window"></a>Hvis jeg velger å vise detaljer for et kort, kan andre brukere se detaljvinduet mitt?

Antall Selv om alle i chatten eller på møtet kan vise selve kortet, vises detaljvinduet bare for deg på enheten når du velger **Detaljer**. Andre brukere må velge **Detaljer** hvis de vil se detaljvinduet på enheten sin.

### <a name="can-i-start-a-teams-call-from-the-details-window-in-teams"></a>Kan jeg starte et Teams-anrop fra detaljvinduet i Teams?

Ja. Hvis du bruker Teams-skrivebordsappen, starter du et anrop ved å velge det koblede nummeret for oppringing i et telefonnummerfelt, for eksempel **Mobiltelefonnr.** på **Kontakt**-kortet. Teams må være den angitte oppringingsappen.

Hvis du vil ringe lokale eller internasjonale fasttelefoner og mobiltelefoner, krever Teams at du har en Business Voice-lisens for bedriftsanrop. Du må også konfigurere Teams som anropsløsningen. Hvis du vil finne ut mer, kan du se [Planlegg Teams-taleløsningen](/microsoftteams/cloud-voice-landing-page) i Teams-dokumentasjonen.

### <a name="can-i-print-documents-from-the-details-window-in-teams"></a>Kan jeg skrive ut dokumenter fra detaljvinduet i Teams?

Ja. Du kan skrive ut rapporter og andre dokumenter ved hjelp av standard [!INCLUDE [prod_short.md](includes/prod_short.md)]-utskriftsfunksjoner og alle skyaktiverte skrivere som er konfigurert på siden **Utskriftsbehandling** i [!INCLUDE [prod_short.md](includes/prod_short.md)]. Du kan ikke skrive ut fra Teams til lokale skrivere som er kjent for klientenheten, for eksempel skrivere som du vanligvis skriver ut til fra nettleseren. Du kan derfor ikke skrive ut fra forhåndsvisningsvinduet for rapport, men bare fra forespørselssiden for hovedrapporten, direkte til skyskriverne.

Hvis du vil ha mer informasjon om å konfigurere skyskrivere, kan du se [Konfigurer skrivere](ui-specify-printer-selection-reports.md).

### <a name="can-i-access-the-camera-from-the-details-window-in-teams"></a>Får jeg tilgang til kameraet fra detaljvinduet i Teams?

Ja. Alle [!INCLUDE [prod_short.md](includes/prod_short.md)]-funksjoner i detaljvinduet som bruker kameraet, er tilgjengelig i alle Teams-klientene.

### <a name="can-i-access-my-location-from-the-details-window-in-teams"></a><a name="location"></a>Får jeg tilgang plasseringen min fra detaljvinduet i Teams?

Hvis du bruker funksjonalitet i [!INCLUDE [prod_short.md](includes/prod_short.md)] som har tilgang til gjeldende plasseringskoordinater, for eksempel med kart, må du bruke Teams i nettleseren eller Teams-mobilappen. Plassering er ikke tilgjengelig når du bruker Teams-skrivebordsappen. 

## <a name="collaborating-with-guests"></a>[Samarbeide med gjester ](#tab/collaborating)

### <a name="can-i-share-cards-with-users-outside-my-organization"></a>Kan jeg dele kort med brukere utenfor organisasjonen min?

Ja. Når du skriver og sender en melding som inneholder et kort, vil alle mottakerne i chatten se kortet, selv om de er gjester eller eksterne i organisasjonen. Gjester kan også åpne detaljvinduet hvis de har fått tilgang til dataene i [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="is-the-experience-any-different-for-users-that-are-guests"></a>Er funksjonene annerledes for brukere som er gjester?

Ja. Hvis gjestebrukere inviteres utenfra organisasjonen til å delta i en chat eller en kanal, får de lignende, men ikke identiske funksjoner sammenlignet med brukere i organisasjonen. Når en gjest mottar en melding som inneholder et kort, kan de vise den. Gjester kan også åpne detaljvinduet hvis de har fått tilgang til dataene i [!INCLUDE [prod_short.md](includes/prod_short.md)] og fått tilordnet en [!INCLUDE [prod_short.md](includes/prod_short.md)]-lisens i organisasjonen. Når en gjest skriver en melding, utvides ikke koblinger til deres [!INCLUDE [prod_short.md](includes/prod_short.md)] eller din til kort.

Hvis du vil ha informasjon om andre likheter og forskjeller mellom gjester og teammedlemmer, kan du se [Gjestefunksjoner i Teams](/MicrosoftTeams/guest-experience) i Teams-dokumentasjonen.

### <a name="how-does-a-guest-user-install-the-prod_shortmd-app"></a>Hvordan installerer en gjestebruker [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen? 

Gjester har ikke tilgang til appmarkedsplassen for å installere appene selv. Appen kan imidlertid installeres automatisk, basert på organisasjonens policyer. En annen måte for en gjestebruker å installere [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen på, er når de mottar en chatmelding som inneholder et [!INCLUDE [prod_short.md](includes/prod_short.md)]-kort. I dette tilfellet velger brukeren **Detaljer**-knappen eller menyen på kortet, og deretter installeres [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for bruk i organisasjonen. Når du har installert appen, mottar ikke brukeren automatisk noen tillatelser til å få tilgang til data fra [!INCLUDE [prod_short.md](includes/prod_short.md)].

---

## <a name="see-also"></a>Se også

[Oversikt over [!INCLUDE [prod_short](includes/prod_short.md)] og Microsoft Teams-integrering](across-teams-overview.md)  
[Installer [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Microsoft Teams](across-install-app-for-teams.md)  
[Feilsøke Teams](admin-teams-troubleshooting.md)  
[Utvikle for Teams-integrering](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]