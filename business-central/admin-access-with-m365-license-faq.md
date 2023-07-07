---
title: Vanlige spørsmål om tilgang med Microsoft 365-lisenser
description: Få svar på vanlige spørsmål om tilgang til Business Central med Microsoft 365-lisenser.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: faq
ms.date: 11/22/2022
ms.custom: bap-template
---
# <a name="access-with-microsoft-365-licenses-faq"></a>Vanlige spørsmål om tilgang med Microsoft 365-lisenser

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Brukere kan få tilgang til Business Central-data Microsoft Teams ved hjelp av Microsoft 365-lisensen sin. Denne artikkelen svarer på vanlige spørsmål fra administratorer, konsulenter og andre. Utviklere bør se vanlige spørsmål for utviklere. Hvis du har spørsmål om hvordan du integrerer Business Central med Microsoft Teams, går du til [Vanlige spørsmål for Teams](teams-faq.md).

## [Tillatelser](#tab/permissions) 

### <a name="can-i-proactively-configure-different-starting-permissions-for-different-groups-of-users"></a>Kan jeg proaktivt konfigurere forskjellige oppstartstillatelser for ulike brukergrupper?

Ikke for øyeblikket. Business Central tillater bare at det konfigureres én gruppe med tillatelser som er tildelt alle Microsoft 365-brukerne når de logger seg på Business Central for første gang.

### <a name="can-i-proactively-configure-permissions-profiles-and-settings-for-individual-users-before-they-sign-in"></a>Kan jeg konfigurere tillatelser, profiler og innstillinger for individuelle brukere på en proaktiv måte før de logger seg på?

Ja. Det kan gjøres gjennom sikkerhetsgrupper. Ved å bruke en sikkerhetsgruppe i et miljø, definerer du det totale settet med brukere som har tilgang til miljøet. Denne sikkerhetsgruppen kan omfatte brukere med en Business Central-lisens og brukere med en Microsoft 365-lisens. Neste gang du oppdaterer brukere fra Microsoft 365 i **Brukere**-listen, opprettes Microsoft 365-brukeroppføringer. Deretter kan du tildele brukergrupper, tillatelser, profiler og andre innstillinger før de har logget seg på.

### <a name="after-a-user-signs-in-can-i-change-which-objects-they-have-access-to"></a>Når en bruker har logget seg på, kan jeg endre hvilke objekter de har tilgang til?

Ja. Når en bruker har logget seg på for første gang og brukeroppføringen er klargjort, håndterer administratorer disse brukerne på samme måte som alle andre Business Central-brukere. De kan for eksempel legge til eller fjerne tillatelser for ulike objekter. Hvis du endrer tillatelsessettene som er tildelt til Microsoft 365-lisensen på siden for lisenskonfigurasjon, gjelder endringen bare de neste brukerne som logger seg på for første gang.

### <a name="how-do-i-prevent-access-to-sensitive-tables"></a>Hvordan hindrer jeg tilgang til sensitive tabeller?

Business Central tilbyr en kraftig og fleksibel tillatelsesmodell der administratorer kan definere tillatelsessett som gir tilgang til bestemte objekter, forretningsprosesser eller hele roller. Hvis du vil hindre tilgang til sensitive tabeller, kan du opprette egendefinerte tillatelsessett som utelukker tillatelsen til sensitive objekter. Hvis du vil ha mer informasjon om å utelate tillatelser, kan du se [Opprett et tillatelsessett](ui-define-granular-permissions.md).  

### <a name="instead-of-customizing-the-license-configuration-can-i-customize-a-user-group"></a>Kan jeg tilpasse en brukergruppe i stedet for å tilpasse lisenskonfigurasjonen?

Ja. Hvis du legger til tillatelsessett i brukergruppen for interne brukere for Microsoft Teams i Business Central, har det samme nettoresultat som å legge til tillatelsessett i Microsoft 365-lisensen, så lenge Microsoft 365-lisensen fortsetter å tildele til denne brukergruppen. Denne tilnærmingen har den ekstra fordelen at tillatelsessett alltid synkroniseres med medlemmene i gruppen når du endrer brukergruppen.

### <a name="when-a-business-central-user-shares-a-record-in-teams-do-they-grant-new-permissions"></a>Når en Business Central-bruker deler en post i Teams, gir de nye tillatelser?

Nei. Denne handlingen er ikke den samme som å dele en kobling til et SharePoint-dokument der personen som deler dokumentet, kan velge å gi tilgang til andre. I Business Central kan bare administratorer konfigurere og tildele tillatelser. Når det sammenlignes med å dele SharePoint-dokumenter, er det tilsvarende det å velge alternativet Del til personer med eksisterende tilgang.

### <a name="does-this-feature-support-row-level-security"></a>Støtter denne funksjonen sikkerhet på radnivå?

Ja. Selv om en person som åpner en post i Teams med Microsoft 365-lisens, kan ha de riktige tillatelsene for tabell og sideobjekt, brukes tillatelser på radnivå hvis den er implementert for denne tabellen.  

### <a name="if-i-configure-permissions-that-include-write-access-will-users-be-able-to-write-in-teams"></a>Hvis jeg konfigurerer tillatelser som omfatter skrivetilgang, kan brukere skrive i Teams?

Hvis du konfigurerer Business Central til å tildele et tillatelsessett som omfatter sett inn, endre eller slette tilgang til et eller flere objekter, kan brukere med tillatelsessettet fremdeles ikke skrive i Teams når de bare har en Microsoft 365-lisens. Business Central-tjenesten fremtvinger skrivebeskyttet tilgang uansett hvilken sett inn-, endre- eller slettetillatelse du tildeler.  

Selv om Business Central gir dette beskyttelsesnivået, anbefaler vi likevel at du unngår tillatelsessett med skrivetilgang. Hvis du gjør det, unngår du problemer senere når brukerne endrer rolle eller skaffer seg nye lisenser.  

## [Oppsett og konfigurasjon](#tab/setup)

### <a name="why-is-the-setting-to-enable-access-not-available-for-my-environment"></a>Hvorfor er innstillingen for å aktivere tilgang ikke tilgjengelig for miljøet mitt?

Aktivering av tilgang med Microsoft 365-lisenser er bare tilgjengelig for Business Central-miljøer med plattformversjon 21.1 eller nyere. Når miljøet oppgraderes til denne minimumsversjonen, blir innstillingen automatisk tilgjengelig. Hvis du vil kontrollere versjonen av miljøet ditt, går du til siden for miljødetaljer for miljøet i administrasjonssenteret for Business Central. Du kan eventuelt logge deg på miljøet og gå til **Hjelp og kundestøtte**-siden fra **Hjelp**-menyen.

### <a name="can-i-access-business-central-on-premises-with-microsoft-365-licenses"></a>Kan jeg åpne Business Central lokalt med Microsoft 365-lisenser?

Nei, det støttes ikke. Business Central viser en feil når brukerne prøver å få tilgang til lokale Business Central-poster i Teams.

### <a name="what-is-the-employee-profile"></a>Hva er ansattprofilen?

**Ansattprofilen** som vises på listesiden **Profiler (roller)** ble innført med oppdatering 21.1. Standardprofilen tildeles brukere som har tilgang til Business Central med Microsoft 365-lisensen sin. Denne profilen er ment for personer i en organisasjon som ikke har en bestemt rolle i Business Central, og som bare trenger å vise data som er delt med dem.

### <a name="what-is-the-teams-users-user-group"></a>Hva er Teams-brukergruppen?

Gruppen **Interne Microsoft Teams-brukere** som vises på siden **Brukergrupper**, ble innført med oppdatering 21.1. Denne gruppen er standard brukergruppe tildelt brukere som har tilgang til Business Central med Microsoft 365-lisensen sin. Brukergruppen er beregnet på personer i den samme organisasjonen der Business Central er vert for samarbeid i Microsoft Teams.  

### <a name="do-users-that-only-have-a-microsoft-365-license-show-up-in-the-users-list-in-business-central"></a>Vises brukere som bare har en Microsoft 365-lisens, i brukerlisten i Business Central?

Ja. Hvis du bruker sikkerhetsgrupper i miljøer, vises disse brukerne i brukerlisten etter at du har brukt handlingen Oppdater brukere fra Microsoft 365 fra **brukerlisten**. Hvis du ikke bruker sikkerhetsgrupper, vises brukerposter i brukerlisten etter første gang de har tilgang til en Business Central-oppføring.

### <a name="does-this-feature-work-for-embed-isv-solutions"></a>Fungerer denne funksjonen for å bygge inn ISV-løsninger?

Ja. Brukere med bare en Microsoft 365-lisens kan også få tilgang til poster i miljøer som kjører under domenet *.bc.dynamics.com.

## [Lisensiering](#tab/license)

### <a name="can-a-customer-use-this-feature-if-they-dont-have-business-central"></a>Kan en kunde bruke denne funksjonen hvis de ikke har Business Central?

Tilgang til Business Central med en Microsoft 365-lisens er beregnet på organisasjoner som allerede abonnerer på Business Central, og som driver et eller flere Business Central-miljøer med lisensierte Business Central-brukere. Den gir ingen ny funksjonalitet eller brukerrettigheter til Microsoft 365-kunder som ikke har en Business Central-plan.

### <a name="how-does-this-help-me-manage-subscription-costs-in-my-organization"></a>Hvordan kan dette hjelpe meg å administrere abonnementskostnader i organisasjonen min?

For å oppnå best mulig produktivitet og effektivisere driften kjøper SMB-er ofte Dynamics 365 Business Central sammen med Microsoft 365. Da mottar de fleste av dem en Microsoft 365-lisens, men bare bestemte roller eller personer mottar en Business Central-lisens. Business Central gir lisensieringsfleksibilitet slik at kundene bare betaler for det de trenger:

- For brukere som trenger full tilgang til Business Central, tildeles vanligvis en Business Central Essentials- eller Business Central Premium-lisens. 
- Brukere som trenger begrenset skrivetilgang, er vanligvis tildelt en Business Central Team Member-lisens.
- Alle andre ansatte i organisasjonen som bare trenger å lese forretningsdata som er delt med dem, kan gjøre dette hvis de har en Microsoft 365-lisens. De trenger ikke å tildeles en Team Member-lisens. Andre lisensalternativer er tilgjengelige. Hvis du vil ha mer informasjon, kan du laste ned og lese [lisensveiledningen for Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).

### <a name="is-this-100-free-of-charge"></a>Er dette 100 % kostnadsfritt?
 
Nei. Tilgang til Business Central-data i Microsoft Teams krever at hver bruker enten har en Business Central-lisens eller en Microsoft 365-lisens fra listen over støttede planer.

### <a name="does-this-work-with-microsoft-365-trials-and-business-central-trials"></a>Fungerer dette med prøveversjoner av Microsoft 365 og Business Central?

Ja. Hvis en bruker er tildelt en Microsoft 365-lisens fra en prøve versjon av en plan som støttes, har de også tilgang til Business Central-poster i Teams. Det er da mulig for kundene å prøve Microsoft-produktivitetsapper og -forretningsapper som arbeider sammen, og gjør at selgere og konsulenter hos partnere enkelt kan demonstrere denne funksjonen. Partnere kan for eksempel klargjøre sine egne Azure AD-leiere fra [https://aka.ms/CDX](https://aka.ms/CDX) som omfatter Microsoft 365-prøveversjoner og Business Central-prøveversjoner for å demonstrere Business Central.

### <a name="the-list-of-licenses-in-business-central-shows-a-microsoft-365-license-whats-that"></a>Listen over lisenser i Business Central viser en Microsoft 365-lisens. Hva er det?

Siden **Lisenskonfigurasjon** i Business Central viser de ulike typene lisenser som kan gi tilgang til Business Central-tjenesten. I versjon 21 la Microsoft til Microsoft 365 i denne listen som en ny måte å få tilgang til Business Central på. Denne listen over lisenser innebærer ikke at organisasjonen har kjøpt abonnementer på noen av disse lisensene, eller at organisasjonen har aktivert tilgang gjennom de lisensene.

### <a name="do-i-need-to-acquire-a-new-type-of-microsoft-365-license-for-this-feature-to-work"></a>Må jeg anskaffe en ny type Microsoft 365-lisens for at denne funksjonen skal fungere?

Microsoft har ikke opprettet nye lisenser eller nye planer for å drive denne funksjonen. Denne funksjonen er fullstendig avhengig av eksisterende Microsoft 365-planer og -lisenser. Hvis du allerede abonnerer på en av de støttede Microsoft 365-planene, har du allerede denne nye bruksrettigheten. Hvis du ikke abonnerer på Microsoft 365 i dag, kan du registrere deg for Microsoft 365 Business Premium eller lignende planer her. 

### <a name="how-do-i-find-out-which-users-have-only-a-microsoft-365-license"></a>Hvordan finner jeg ut hvilke brukere som bare har en Microsoft 365-lisens?

Det finnes flere måter. I administrasjonssenteret for Microsoft 365 går du til listen **Aktive brukere** i og ser kolonnen **Lisenser**. I Business Central går du til **Brukere**-listen, velger en av brukerne og viser faktaboksen **Lisenser**.  

### <a name="how-do-i-filter-the-users-list-in-business-central-to-see-users-that-only-have-a-microsoft-365-license"></a>Hvordan filtrerer jeg brukerlisten i Business Central for å se brukere som bare har en Microsoft 365-lisens?

Denne oppgaven er for tiden ikke mulig ved å bruke en filter- eller listevisning. Du kan imidlertid velge en bruker i listen og vise faktaboksen Lisenser som bare omfatter Microsoft 365, hvis brukeren bare har en Microsoft 365-lisens.

### <a name="what-about-users-that-have-both-a-microsoft-365-license-and-a-business-central-license"></a>Hva med brukere som både har en Microsoft 365-lisens og en Business Central-lisens?

Når flere lisenser er tildelt til en bruker, vinner større lisensbruksrettighetene over mindre lisensbruksrettigheter ved tilgang til Business Central. I dette tilfellet gir Business Central-lisensen brukeren tilgang til flere brukerrettigheter. Dermed kan brukerne lese og skrive Business Central-poster i Teams og få tilgang til Business Central-nettklienten i nettleseren, på samme måte som andre Business Central-lisenshavere. Hvis bestemte tillatelsessett er konfigurert for Microsoft 365-lisensen, får brukeren de konfigurerte tillatelsessettene kombinert med tillatelsessettene fra Business Central-lisensen, eller som allerede er tildelt til brukeren.

### <a name="is-this-licensing-related-to-the-business-central-team-member-license"></a>Er denne lisensieringen knyttet til Business Central Team Member-lisensen?

Det er ingen forbindelse mellom Business Central Team Member-lisenser og tilgang til Business Central i Microsoft Teams ved å bruke Microsoft 365-lisenser. Selv om Microsoft Teams og dokumentasjonen henviser til personer i en gruppe som *gruppemedlemmer*, er det et samlebegrep for en gruppe Microsoft Teams-brukere. Det henviser ikke til Business Central-lisenser.

### <a name="does-business-central-enforce-any-of-the-constraints"></a>Håndhever Business Central noen av begrensningene?

Ja, alle plattformbegrensninger og minimumskrav, inkludert lisenskrav, håndheves av Business Central-plattformen. Dette veileder brukere med bestemte feilmeldinger for å hjelpe dem med å feilsøke oppsettet og forhindre misbruk. Hvis for eksempel en bruker som bare har en Microsoft 365-lisens, prøver å få tilgang til Business Central-nettklienten i nettleseren, blir tilgang nektet og det vises en veiledende feilmelding. 

## [Forbruk](#tab/usage)
 
### <a name="can-i-access-records-on-teams-for-ios-and-teams-for-android"></a>Får jeg tilgang til poster på Teams for iOS og Teams for Android?

For øyeblikket er det ikke mulig å få tilgang til Business Central-data på Teams-mobilversjonen med bare en Microsoft 365-lisens. Microsoft arbeider med å aktivere denne funksjonen om kort tid. 

### <a name="how-do-users-change-their-personal-settings-in-my-settings"></a>Hvordan endrer brukerne sine personlige innstillinger i Mine innstillinger?

Når en bruker får tilgang til Business Central for første gang ved hjelp av bare Microsoft 365-lisensen, angis brukerinnstillinger som språk, tidssone og regionale innstillinger automatisk basert på operativsystemets eller nettleserens innstillinger. Administratorer kan endre disse innstillingene fra Business Central for hver bruker. 

### <a name="what-determines-the-choice-of-language-when-you-sign-in-for-the-first-time"></a>Hvilket bestemmer valget av språk når du logger deg på første gang?

Språket du ser i Business Central, er angitt basert på ulike faktorer, inkludert Teams-klienten som du åpner Business Central med den første gangen. For Teams-skrivebordsappen, Teams for iOS og Teams for Android brukes operativsystemets språk. For Teams for nettet brukes nettleserspråket. I alle tilfeller vurderes ikke Teams-språket. 

### <a name="why-cant-i-activate-some-of-the-colored-links-in-tabs-and-card-details"></a>Hvorfor kan jeg ikke aktivere noen av de fargede koblingene i faner og kortdetaljer?

Handlingsrettede koblinger på Business Central-sider vises ofte som fete hyperkoblinger som kan aktiveres eller kjøre operasjoner. På et teknisk nivå implementeres disse koblingene vanligvis som feltverdier uten tekst som utløser en kode, og der valg av stil ofte gjenspeiler statusen. Når brukere får tilgang til Business Central-sider med Microsoft 365-lisensen, er koblingene utformet som om de er handlingsrettet. Men de kan ikke aktiveres fordi denne lisensen ikke tilbyr bruksrettigheter til å kjøre handlinger.  

### <a name="why-cant-i-activate-page-notification-actions"></a>Hvorfor kan jeg ikke aktivere sidevarslingshandlinger?

Kontekstavhengige varsler som vises på sider, er ofte sammen med handlingsrettede koblinger. Når brukere får tilgang til Business Central-sider med Microsoft 365-lisensen, vises disse koblingene, men de kan ikke aktiveres fordi denne lisensen ikke tilbyr bruksrettigheter til å kjøre handlinger. På et teknisk nivå implementeres disse koblingene som handlinger.

### <a name="can-microsoft-365-users-remove-tabs"></a>Kan Microsoft 365-brukere fjerne faner?

Ja. Alle i nettpraten eller kanalen kan fjerne faner som er opprettet av andre. Når du fjerner en fane, fjernes eller påvirkes ikke data i Business Central, men fanen blir fjernet for alle brukere i nettpraten eller kanalen.

### <a name="if-i-cant-filter-will-i-still-see-a-filtered-list-that-was-created-by-others"></a>Hvis jeg ikke kan filtrere, kan jeg fortsatt se en filtrert liste som ble opprettet av andre?

Brukere som har tilgang til Business Central med Microsoft 365-lisensen, har ikke bruksrettighetene til å filtrere ved hjelp av filtreringsruten eller bruke listevisninger. Hvis en annen bruker har opprettet en fane som inneholder en filtrert listeside, ser Microsoft 365-brukerne også filtrene som er brukt i fanen.

---

## <a name="see-also"></a>Se også

[Oversikt over Business Central-tilgang med Microsoft 365-lisenser](admin-access-with-m365-license.md#minimum-requirements)  
[Konfigurer tilgang med Microsoft 365-lisenser](admin-access-with-m365-license-setup.md)  
