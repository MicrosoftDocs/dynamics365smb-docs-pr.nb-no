---
title: Opprette brukere i henhold til lisenser
description: Beskriver hvordan du legger til brukere i Business Central Online eller lokalt basert på lisenser.
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'access, right, security'
ms.search.form: '119, 6300, 6301, 6302, 8930, 9800, 9807, 9808, 9830, 9831, 9838, 9818, 9062, 9061, 9069, 9173'
ms.date: 03/24/2023
ms.author: jswymer
ms.reviewer: jswymer
---
# <a name="create-users-according-to-licenses"></a>Opprette brukere i henhold til lisenser

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Denne artikkelen beskriver hvordan administratorer oppretter brukere og definerer hvem som kan logge seg på [!INCLUDE[prod_short](includes/prod_short.md)]. Du finner også ut hvordan du tildeler tillatelser til ulike brukere i henhold til produktlisensene dine.

Når du oppretter brukere i [!INCLUDE[prod_short](includes/prod_short.md)], gir du tillatelser til dem gjennom tillatelsessett. Du kan også organisere brukere i brukergrupper. Brukergrupper gjør det enklere å behandle tillatelser og andre innstillinger for flere brukere samtidig. Hvis du vil ha mer informasjon, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md).  

Hvis du vil ha mer informasjon om de ulike typene lisenser og hvordan lisensiering fungerer i [!INCLUDE[prod_short](includes/prod_short.md)], kan du se [Laste ned lisensieringsveiledningen for Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> Prosessen med å behandle brukere og lisenser varierer avhengig av om [!INCLUDE[prod_short](includes/prod_short.md)] er distribuert elektronisk eller lokalt. For [!INCLUDE [prod_short](includes/prod_short.md)] online må du legge til brukere fra Microsoft 365. I lokale distribusjoner kan du opprette, redigere og slette brukere direkte.  

## <a name="manage-users-and-licenses-in-online-tenants"></a>Behandle brukere og lisenser i nettleietakere

Brukerkontoer i [!INCLUDE[prod_short](includes/prod_short.md)] må først opprettes i administrasjonssenteret for Microsoft 365. Disse brukerkontoene er ikke eksklusive for Business Central. Hvis du abonnerer på andre planer, kan de brukes til å logge på andre programmer, for eksempel Power BI. Hvis du vil ha mer informasjon om hvordan du oppretter brukere i administrasjonssenteret for Microsoft 365, går du til [Legg til brukere i administrasjonssenteret for Microsoft](/microsoft-365/admin/add-users/add-users).

Abonnementet på [!INCLUDE[prod_short](includes/prod_short.md)] på nettet definerer hvor mange [!INCLUDE[prod_short](includes/prod_short.md)]-brukerlisenser du er tillatt. Brukere legges til i leietakeren din i Microsoft Partner Center, vanligvis av Microsoft-partneren. Hvis du vil ha mer informasjon, kan du se [Administrasjon av Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

Du tildeler lisenser til brukere i henhold til arbeidet hver bruker skal gjøre i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan tildele lisenser på flere måter:

- Selskapets Microsoft 365-administrator kan gjøre dette i [administrasjonssenteret for Microsoft 365](https://admin.microsoft.com). Hvis du vil ha mer informasjon, kan du se [Legge til brukere individuelt eller gruppevis i Microsoft 365](/microsoft-365/admin/add-users/add-users).  
- En Microsoft-partner kan tilordne lisenser i administrasjonssenteret for Microsoft 365 eller i Microsoft Partner Center. Hvis du vil ha mer informasjon, se [Brukerbehandlingoppgaver for kundekonti](/partner-center/assign-licenses-to-users) i hjelpen for Microsoft Partner Center.

Hvis du vil ha mer informasjon, kan du se [Administrasjon av Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) i hjelpen for administrasjon.

Når brukerkontoer er opprettet i administrasjonssenteret for Microsoft 365, kan du importere dem til Business Central på to måter:

- En brukerkonto importeres automatisk når brukeren logger seg på [!INCLUDE [prod_short](includes/prod_short.md)] for første gang.

- Administratoren kan importere brukere ved å velge handlingen **Oppdater brukere fra Microsoft 365** på **Brukere* -siden.

Begge måtene har sine egne fordeler, og du kan bruke dem samtidig. Med hver fremgangsmåte kan administratorer proaktivt konfigurere [!INCLUDE [prod_short](includes/prod_short.md)] for å tildele oppstartstillatelsene, brukergruppene og brukerprofilene. Hvis du bruker handlingen **Oppdater brukere fra Microsoft 365**, får administratorer mer kontroll til å justere tillatelser, brukergrupper og profiler. Det er en ideell måte når du setter opp [!INCLUDE [prod_short](includes/prod_short.md)] for første gang, før noen brukere logger seg på, eller når du legger til en ny brukergruppe.

> [!NOTE]
> Når du har lagt til brukere i Microsoft 365-administrasjonssenteret, anbefaler vi at du oppdaterer bruker opplysningene i [!INCLUDE[prod_short](includes/prod_short.md)] så raskt som mulig. Det er enkelt å holde brukerinformasjon oppdatert, og det bidrar til å sikre at personer alltid kan logge seg på. Se [Slik legger du til brukere eller oppdaterer brukerinformasjon og lisenstilordninger i Business Central](#adduser) for mer informasjon.<br>
>
> Det er spesielt viktig å oppdatere brukerinformasjon hvis du har egendefinerte tillatelsessett for lisensen. Hvis en ny bruker prøver å logge seg på [!INCLUDE[prod_short](includes/prod_short.md)] før du har lagt til vedkommende, er det ikke sikkert de kan logges seg på. Hvis du vil ha mer informasjon, kan du se [Konfigurer tillatelser basert på lisenser](#licensespermissions).
>
> Brukere som opplever dette problemet, blir ikke faktisk sperret. De kan enten bruke handlingen **Gå tilbake til startsiden** eller ganske enkelt logge seg på igjen for å løse problemet.

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]

Hvis du vil ha mer informasjon, kan du se [Delegert administratortilgang til Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin).  

### <a name="configure-permissions-based-on-licenses"></a><a name="licensespermissions"></a>Konfigurer tillatelser basert på lisenser

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

Administratorer kan konfigurere tillatelsessett og brukergrupper for hver lisens.<!--Note to translators: The names in *italics* or capitalized in this section must not be translated.-->  

Den vanligste lisensen, *Dynamics 365 Business Central Team Member*, har for eksempel følgende tillatelsessett som standard:

- D365 LESE
- D365-TEAMMEDLEM
- REDIGER I EXCEL – VIS
- EKSPORTER RAPPORT EXCEL
- LOKAL

Andre tillatelsessett legges til automatisk basert på brukergruppene som er tildelt lisensen. Når du oppretter en ny bruker basert på denne lisensen, tildeler [!INCLUDE[prod_short](includes/prod_short.md)] tillatelsessettene som kommer fra brukergruppene og tillatelsessettene fra lisensen. De samme oppstartstillatelsene tildeles brukeren hvis brukerkontoen ble opprettet automatisk i [!INCLUDE[prod_short](includes/prod_short.md)], eller hvis administratoren brukte handlingen **Oppdater brukere fra Microsoft 365** på siden **Brukere**.

Hvis denne standarddefinisjonen ikke er riktig oppsett for et bestemt miljø, kan administratoren endre konfigurasjonen. Egendefinerte tillatelser vil imidlertid bare påvirke nye brukere som er tildelt lisensen. Tillatelser for eksisterende brukere som er tildelt lisensen, påvirkes ikke.  

1. Logg deg på [!INCLUDE[prod_short](includes/prod_short.md)] ved å bruke en administratorkonto.  
2. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lisenskonfigurasjon**, og velg deretter den relaterte koblingen.  

    <!--Alternatively, if you're already in the **Users** page, you can run the **Update Users from Microsoft 365** guide, and then, on the first page of the guide, choose the **Configure permissions per license** link.-->  
3. Velg lisensen du vil tilpasse, på siden **Lisenskonfigurasjon**, og velg deretter handlingen **Konfigurer**.  
4. Velg feltet **Tilpass tillatelser** for å aktivere tilpasning, og foreta deretter de aktuelle endringene.  

    I vårt eksempel vil administratoren fjerne tillatelsen til å redigere i Excel, og vedkommende fjerner derfor brukergruppen for *Excel-eksporthandling* fra teammedlemslisensen. Videre får ikke nye brukere som er tildelt teammedlemslisensen, mulighet til å eksportere data til Excel. Hvis organisasjonen ombestemmer seg, kan de gå tilbake til siden **Lisenskonfigurasjon** og slå av tilpasningen for denne lisenstypen.  

> [!IMPORTANT]
> Denne tilpasningen av tillatelser trer bare i kraft for nye brukere som du tildeler den aktuelle lisensen til. Eksisterende brukere oppdateres ikke. Vi anbefaler at du tilpasser tillatelsene før du begynner å tildeler brukerlisenser i Microsoft 365-administrasjonssenteret.

### <a name="to-add-users-or-update-user-information-and-license-assignments-in-business-central"></a><a name="adduser"></a>Slik legger du til brukere eller oppdaterer brukerinformasjon og lisenstilordninger i Business Central

Når du har lagt til brukere eller endret brukerinformasjon i administrasjonssenteret for Microsoft 365, kan du raskt importere brukerinformasjonen til [!INCLUDE[prod_short](includes/prod_short.md)]. Importen omfatter lisenstildelinger.  

1. Logg deg på [!INCLUDE[prod_short](includes/prod_short.md)] ved å bruke en administratorkonto.
2. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukere**, og velg deretter den relaterte koblingen.  
3. Velg **Oppdater brukere fra Microsoft 365**.

> [!IMPORTANT]  
> Kjøring av synkronisering av brukere fra Microsoft 365 ved å bruke veiledningen **Oppdater brukere fra Microsoft 365**, krever SUPER-tillatelsessettet.

> [!NOTE]
> Veiledningen **Oppdater brukere fra Microsoft 365** oppdaterer ikke brukere som ikke er tildelt en lisens, for eksempel en bruker som er global administrator og Dynamics 365-administrator. Disse brukerne oppdateres neste gang de logger seg på miljøet.

Det neste trinnet for nylig opprettede brukere er å tildele brukergrupper og -tillatelser. Gå til [Tildel tillatelser til brukere og grupper](ui-define-granular-permissions.md) for informasjon. Hvis du oppdaterer en bruker og oppdateringen omfatter en lisensendring, blir brukerne tildelt til den aktuelle brukergruppen, og tilhørende tillatelsessett blir oppdatert. Hvis du vil ha mer informasjon, kan du se [Administrere tillatelser gjennom brukergrupper](ui-define-granular-permissions.md).  

> [!NOTE]
> Alle brukere i et miljø må tilordnes til den samme lisensen, enten Essentials eller Premium. Gå til nettstedet for [Business Central](https://dynamics.microsoft.com/business-central/overview/) hvis du vil ha mer informasjon om lisensiering.

Hvis du vil ha mer informasjon om å synkronisere brukerinformasjon med Microsoft 365, går du til delen [Synkronisering med Microsoft 365](#m365).

> [!NOTE]
> Hvis du bruker en ekstern regnskapsfører til å administrere regnskap og finansrapportering, kan du invitere regnskapsføreren til [!INCLUDE[prod_short](includes/prod_short.md)], slik at vedkommende kan arbeide med regnskapsdataene. Hvis du vil ha mer informasjon, kan du se [Invitere den eksterne regnskapsføreren til Business Central](finance-accounting.md#inviteaccountant).

### <a name="to-remove-a-users-access-to-the-system"></a>Fjerne en brukers tilgang til systemet

Du kan fjerne en brukers tilgang til [!INCLUDE[prod_short](includes/prod_short.md)] på nettet. Alle referanser til brukeren beholdes. Brukeren kan imidlertid ikke logge seg på og aktive økter for brukeren stoppes.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukere**, og velg deretter den relaterte koblingen.
2. Åpne siden **Brukerkort** for den aktuelle brukeren, og velg deretter **Deaktivert** i feltet **Status**.
3. Hvis du vil gi brukeren tilgang igjen, setter du verdien for feltet **Status** til **Aktivert**.

Du kan også fjerne lisensen fra en bruker i administrasjonssenteret for Microsoft 365. Brukeren kan da ikke logge på. Hvis du vil ha mer informasjon, kan du se [Fjerne lisenser fra brukere](/microsoft-365/admin/manage/remove-licenses-from-users).

### <a name="synchronization-with-microsoft-365"></a><a name="m365"></a>Synkronisere med Microsoft 365

Når du tilordner en lisens for [!INCLUDE[prod_short](includes/prod_short.md)] til en bruker i Microsoft 365, kan du opprette brukeren i [!INCLUDE[prod_short](includes/prod_short.md)] på to måter.  

- Administratoren kan legge til brukeren ved å velge **Oppdater brukere fra Microsoft 365**-handlingen på **Brukere**-siden som beskrevet i delen [Slik legger du til en bruker eller oppdaterer brukerinformasjon i Business Central](#adduser).
- Lisensinformasjonen blir oppdatert automatisk når brukeren logger på første gang.

I begge tilfeller brukes flere innstillinger automatisk. Disse innstillingene er oppført i andre og tredje kolonne i tabellen nedenfor.

Hvis du endrer brukerinformasjon i Microsoft 365, kan du oppdatere [!INCLUDE[prod_short](includes/prod_short.md)] for å gjenspeile endringen. Avhengig av hva du vil oppdatere, kan du bruke én av handlingene på **Brukere**-siden. Handlingene beskrives i de to siste kolonnene i tabellen nedenfor.

|Hva skjer når:|Første bruker, første pålogging|Oppdater brukere fra Microsoft 365|Gjenopprett brukerens standardbrukergrupper|
|-|-|-|-|
|Omfang:|Gjeldende bruker|Flere valgte brukere|Enkeltvalgt bruker (bortsett fra gjeldende)|
|Opprett den nye brukeren, og tilordne SUPER-tillatelsessett.<br /><br /><!--Platform-->|**X**|**X** | | 
|Oppdater brukeren basert på informasjon i Microsoft 365: status, fullt navn, kontaktens e-post, godkjennings-e-post.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|
|Synkroniser brukerplaner (lisenser) med lisenser og roller tilordnet i Microsoft 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**|**X**|
|Legg til brukeren i brukergrupper i henhold til gjeldende brukerplaner. Fjern tillatelsessettet SUPER for alle andre brukere enn den første brukeren som skal logge på, samt [administratorer](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Det må være minst en forekomst av tillatelsessettet SUPER.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**|**X**<br /><br />Fjerner manuelt tilordnede brukergrupper og tillatelser.|

Brukere kan få tilgang til [!INCLUDE[prod_short](includes/prod_short.md)]-poster i Teams ved hjelp av bare Microsoft 365-lisensen sin. Når tilgang er aktivert for et miljø, inkluderer ikke synkronisering ved hjelp av handlingen **Oppdater brukere fra Microsoft 365**, brukere som bare har en Microsoft 365-lisens. Hvis du vil inkludere disse brukerne i synkroniseringen, må du først oppdatere miljøinnstillinger ved å tildele en sikkerhetsgruppe som inneholder brukere med en [!INCLUDE[prod_short](includes/prod_short.md)]-lisens og brukere som bare har en Microsoft 365-lisens.

Finn ut mer om å sikre tilgang til miljøer ved hjelp av sikkerhetsgrupper under [Administrer tilgang ved hjelp av Microsoft Entra-grupper](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups).

Få en oversikt over tilgang til [!INCLUDE[prod_short](includes/prod_short.md)] i Teams med Microsoft 365-lisenser under [administratortilgang-med-m365-lisens](admin-access-with-m365-license.md).

## <a name="manage-users-and-licenses-in-on-premises-deployments"></a>Behandle brukere og lisenser i lokale distribusjoner

For lokale distribusjoner er antallet brukerlisenser angitt i lisensfilen (.bclicense eller .flf). Når en administrator eller Microsoft-partner laster opp lisensfilen, kan de angi hvilke brukere som kan logge på [!INCLUDE[prod_short](includes/prod_short.md)].

Ved distribusjon på stedet oppretter, redigerer og sletter administratoren brukere direkte fra **Brukere**-siden.

### <a name="to-edit-or-delete-a-user-in-an-on-premises-deployment"></a>Slik redigerer eller sletter du en bruker i en lokal distribusjon

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukere**, og velg deretter den relaterte koblingen.
2. Velg brukeren du vil redigere, og velg deretter **Rediger**-handlingen.
3. På siden **Brukerkort** endrer du informasjonen etter behov.  
4. Hvis du vil slette en bruker, velger du brukeren du vil slette, og deretter velger du handlingen **Slett**.

> [!NOTE]
> For lokale distribusjoner kan en administrator angi hvordan brukerlegitimasjoner skal godkjennes i [!INCLUDE[server](includes/server.md)]-forekomsten. Når du oppretter en bruker, angir du legitimasjonstypen du bruker.
>
> Hvis du vil ha mer informasjon, kan du se [Godkjenning og legitimasjonstyper](/dynamics365/business-central/dev-itpro/administration/users-credential-types) i administrasjonshjelpen for [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-also"></a>Se også

[Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md)  
[Administrere profiler](admin-users-profiles-roles.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Administrasjon](admin-setup-and-administration.md)  
[Lisensiering i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing)  
[Legge til brukere i Microsoft 365 for business](/microsoft-365/admin/add-users/add-users)  
[Sikkerhet og beskyttelse i Business Central (administrasjonsinnhold)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  
[Tilpass en telemetri-ID til brukere](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights#assign-a-telemetry-id-to-users)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
