---
title: Konfigurer tilgang med Microsoft 365-lisenser
description: En veiledning for hvordan administratorer kan konfigurere tilgang til Business Central med Microsoft 365-lisenser.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 09/28/2023
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
ms.search.form: '9061,'
---
# <a name="set-up-business-central-access-in-teams-with-microsoft-365-licenses"></a>Konfigurer Business Central-tilgang i Teams med Microsoft 365-lisenser

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Administratorer må fullføre flere aktiviteter før brukerne kan få tilgang til [!INCLUDE [prod_short](includes/prod_short.md)] med Microsoft 365-lisensen. Trinnene nedenfor representerer minimumsoppsettet som kreves for å starte. Hvis du vil vite mer om tilgang med Microsoft 365-lisenser, går du til [Business Central-tilgang med Microsoft 365-lisenser](admin-access-with-m365-license.md).

## <a name="guidelines"></a>Retningslinjer

Konfigurering av tilgang med Microsoft 365-lisenser omfatter følgende oppgaver:

|Trinn|Oppgave|Obligatorisk|
|-|-|-|
|1|[Konfigurer hvilke Business Central-data de Microsoft 365-lisensierte brukerne har tillatelse til å vise](#configure-permissions)|![avmerking](media/check.png "avmerking")|
|2|[Aktiver tilgang med Microsoft 365-lisenser i Business Central-miljøet](#enable-access-with-microsoft-365-licenses)|![avmerking](media/check.png "avmerking")|
|3|[Tildel sikkerhetsgruppe til miljøet](#choose-who-gets-access-by-using-security-group)|
|4|[Distribuer Business Central-appen for Teams til brukere](#deploy-the-business-central-app-for-teams)|![avmerking](media/check.png "avmerking")|
|5|[Test oppsettet](#test-your-setup)||

> [!TIP]
> Med unntak av den siste oppgaven, kan du fullføre oppgavene i en hvilken som helst rekkefølge. Du kan utføre oppgaver separat, som beskrevet i delene nedenfor, ved å følge eller bruke veiledningen for assistert oppsett for **Tilgang med Microsoft 365-lisenser** for å forklare dem.
>
> Hvis du vil kjøre veiledningen med assistert oppsett, gjør du følgende:
>
> 1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Assistert oppsett** og velger den relaterte koblingen.
> 2. Gå til delen **Gjør mer med Business Central** på siden **Assistert oppsett**, og velg **Tilgang med Microsoft 365-lisenser**.
> 3. Følg instruksjonene.  

## <a name="configure-permissions"></a>Konfigurer tillatelser

[!INCLUDE [prod_short](includes/prod_short.md)] er sikret etter utforming og minimerer risikoen ved å gi ingen tillatelser til Microsoft 365-brukere som standard. Administratorer må konfigurere objekttillatelser som bestemmer hvilke tabeller, sider og rapporter som kan åpnes i Teams med bare en Microsoft 365-lisens. Disse tillatelsene er starttillatelsene som tildeles når en bruker logger seg på for første gang med Microsoft 365-lisensen. 

Slik konfigurerer du oppstartstillatelser:

1. I [!INCLUDE [prod_short](includes/prod_short.md)] søker du etter **Lisenskonfigurasjon**.
2. Velg Microsoft 365-lisensen.
3. Velg redigeringsikonet ![Redigeringsikon](media/edit-pencil.png) øverst på **Microsoft 365**-lisensiden, og aktiver deretter **Tilpass tillatelser**. 
4. I delen **Egendefinerte tillatelsessett** legger du til de riktige tillatelsessettene og velger om de skal gjelde ett selskap eller alle selskaper i miljøet.

Med denne konfigurasjonen legges brukere med bare en Microsoft 365-lisens til i listen **Brukere** når de åpner [!INCLUDE [prod_short](includes/prod_short.md)] for første gang. Hvis du vil ha mer informasjon om brukere, kan du gå til [Opprett brukere i henhold til lisenser](ui-how-users-permissions.md).

> [!NOTE]
> Når du synkroniserer listen over brukere i [!INCLUDE [prod_short](includes/prod_short.md)] med brukere i Microsoft 365, legges bare brukere som har en [!INCLUDE [prod_short](includes/prod_short.md)]-lisens, til i listen over brukere for [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis du vil ha mer administrativ kontroll over tillatelser og profiler, kan du tildele en sikkerhetsgruppe til miljøet. Når miljøer er sikret med en sikkerhetsgruppe og aktiverer tilgang med Microsoft 365-lisenser, omfatter **Oppdater brukere fra Microsoft 365**-handlingen på siden **Brukere** også brukere som bare har en Microsoft 365-lisens. Hvis du vil ha mer informasjon om å sikre miljøer, kan du se [Administrer tilgang med Microsoft Entra-grupper](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups) i hjelpen for utviklere og IT-eksperter.

> [!TIP]
> Ser du etter en raskere måte å komme i gang på når du prøver denne funksjonen i en sandkasse eller et evalueringsselskap? Tildel tillatelsessettet **D365 lese** som gir tillatelse til de fleste objektene.  

Når du arbeider med flere miljøer, må lisenskonfigurasjonen brukes for hvert miljø, og de kan være forskjellige i alle miljøene.

Finn ut mer under [Tildel tillatelser til brukere og grupper](ui-define-granular-permissions.md) og [Opprett tillatelsessett](/dynamics365/business-central/dev-itpro/developer/devenv-permissionset-composing)

## <a name="enable-access-with-microsoft-365-licenses"></a>Aktiver tilgang med Microsoft 365-lisenser

Tilgang med Microsoft 365-lisenser er som standard deaktivert. Tilgang må aktiveres for hvert miljø uavhengig, noe som gir administratorer mulighet til å styre og tillate utrulling på tvers av organisasjonen. Du aktiverer tilgang ved hjelp av [!INCLUDE [prod_short](includes/prod_short.md)]-administrasjonssenteret: 

1. Øverst til høyre velger du **Innstillinger** ![Innstillinger.](media/ui-experience/settings_icon_small.png "Innstillinger-ikon for rollesenter"). > **Administrasjonssenter**.  
2. I administrasjonssenteret velger du **Miljøer**, og deretter velger du miljøet du vil endre lisenstilgang for. 
3. På siden **Miljødetaljer** velger du **Endre** for innstillingen **Tilgang med Microsoft 365-lisens**.
4. I ruten **Microsoft 365-lisenser** slår du på bryteren. 
5. Velg **Lagre** når du er ferdig og godta bekreftelsen. Endringene trer i kraft umiddelbart.

## <a name="choose-who-gets-access-by-using-security-group"></a>Velg hvem som får tilgang ved hjelp av sikkerhetsgruppe

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

I Business Central-administrasjonssenteret kan et miljø tildeles til en eller flere sikkerhetsgrupper for å kontrollere tilgang. Du kan tildele en Microsoft Entra-gruppe til miljøet. Ved å tildele en Microsoft Entra-gruppe til et miljø får bare direkte og indirekte medlemmer i gruppen tilgang til miljøet. Indirekte medlemmer er brukere i en annen gruppe, som selv er medlem av gruppen som er tildelt til miljøet. Selv om alle lisensierte brukere i Microsoft Entra ID blir lagt til i miljøet når det synkroniseres med Microsoft 365, kan bare gruppemedlemmer logge seg på. Hvis du vil ha mer informasjon, kan du gå til [Administrer tilgang med Microsoft Entra-grupper](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups) i hjelpen for utviklere og IT-eksperter.

## <a name="deploy-the-business-central-app-for-teams"></a>Distribuer Business Central-appen for Teams

Hvis [!INCLUDE [prod_short](includes/prod_short.md)]-lisensinnehavere skal dele data i Teams og for Microsoft 365-lisensinnehavere å få tilgang til disse dataene, må [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Teams være installert. Selv om brukerne kan installere appen selv, anbefales det at administratorer bruker sentralisert distribusjon. Med sentralisert distribusjon kan du rulle ut appen til en større målgruppe på tvers av organisasjonen og minimere individuell brukerinnsats. 

Hvis du vil finne ut mer om hvordan du kan distribuere [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Teams, kan du se [Installer Business Central-appen ved hjelp av sentralisert distribusjon](admin-teams-integration.md#installing-the-business-central-app-by-using-centralized-deployment).

> [!NOTE]
> Hvis du har kjørt sentralisert distribusjon tidligere og bare har distribuert appen til sikkerhetsgruppen for lisensierte [!INCLUDE [prod_short](includes/prod_short.md)]-brukere, må du kjøre den på nytt for å distribuere til flere grupper eller hele organisasjonen, avhengig av hvordan du konfigurerer tilgang.

> [!TIP]
> Ser du etter en raskere måte å komme i gang på når du prøver denne funksjonen? Testbrukere kan installere appen på [aka.ms/BCgetTeamsApp](https://aka.ms/BCgetTeamsApp).

## <a name="test-your-setup"></a>Test oppsettet

Hvis du vil kontrollere at oppsettet er klart for produksjon, kan du bruke følgende fremgangsmåte til å påse at alt fungerer som det skal.

1. Opprett eller identifiser to testbrukere (A og B).

   - Testbruker A må ha en [!INCLUDE [prod_short](includes/prod_short.md)]-lisens og Microsoft 365-lisens med tilgang til Teams.
   - Testbruker B må bare ha en Microsoft 365-lisens for tilgang til Teams.

2. Logg deg på [!INCLUDE [prod_short](includes/prod_short.md)]-nettklienten som testbruker A.

   1. Åpne en post som testbruker B skal ha tilgang til, for eksempel et **varekort** i riktig selskap og miljø.
   2. Velg **Del** ![!Del til andre apper-handling på sider.](media/share-icon.png) > **Del til Teams** for å åpne vinduet Del til Teams.
   3. I feltet **Del til** legger du til testbruker B som mottaker.
   4. Vent til koblingen er utvidet til et kort, og velg Del.

3. Logg seg på Microsoft Teams som testbruker B.

   1. Velg Nettprat og åpne samtalen med testbruker A.
   2. Velg Detaljer-knappen på kortet i meldingen som sendes av testbruker A. Hvis [!INCLUDE [prod_short](includes/prod_short.md)]-klienten vises og er skrivebeskyttet, er oppsettet vellykket.

> [!TIP]
> Noe gikk galt. Sjekk [Feilsøk tilgang med Microsoft 365-lisenser](admin-access-with-m365-license-troubleshooting.md).

## <a name="see-also"></a>Se også

[Oversikt over Business Central-tilgang med Microsoft 365-lisenser](admin-access-with-m365-license.md#minimum-requirements)  
[Feilsøk tilgang med Microsoft 365-lisenser](admin-access-with-m365-license-troubleshooting.md)  
[Business Central og Microsoft Teams-integrering](across-teams-overview.md)  
