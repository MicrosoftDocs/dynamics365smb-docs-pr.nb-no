---
title: Arbeide med Power BI-rapporter i Business Central | Microsoft Docs
description: 'Få innsikt, forretningsanalyse og KPI-er fra Business Central-dataene med Power BI.'
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 04/01/2021
ms.author: jswymer
---
# <a name="work-with-power-bi-reports-in-include-prodshortincludesprodshortmd" />Arbeid med Power BI-rapporter i [!INCLUDE [prod_short](includes/prod_short.md)]

I denne artikkelen får du grunnleggende informasjon om hvordan du viser Power BI-rapporter i [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="overview" />Oversikt

Power BI-rapporter gir deg innsikt i [!INCLUDE[prod_short](includes/prod_short.md)]. Ulike sider i [!INCLUDE [prod_short](includes/prod_short.md)] inkluderer en Power BI-rapportdel som kan vise Power BI-rapporter. Rollesenteret er en vanlig side der du ser en Power BI-rapportdel. Noen listesider, for eksempel **Varer**, omfatter også en Power BI-del.

[!INCLUDE [prod_short](includes/prod_short.md)] fungerer sammen med Power BI-tjenesten. Rapporter som skal vises i [!INCLUDE [prod_short](includes/prod_short.md)], er lagret i en Power BI-tjeneste. I [!INCLUDE [prod_short](includes/prod_short.md)] kan du bytte rapporten som vises i Power BI-delen, til enhver Power BI-rapport som er tilgjengelig i Power BI-tjenesten. Delene kommer til å være tomme første gang du logger på [!INCLUDE [prod_short](includes/prod_short.md)], og til du kobler til en Power BI-tjeneste, som vist her:

![Power BI-del i Business Central.](./media/power-bi-part.png)

## <a name="get-started" />Kom i gang

### <a name="prerequisites" />Forutsetninger

Hvis du bruker [!INCLUDE[prod_short](includes/prod_short.md)] lokalt, må den aktiveres for Power BI-integrering. Denne oppgaven utføres vanligvis av en administrator. Hvis du vil ha mer informasjon, kan du se [Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] lokalt for Power BI-integrering](admin-powerbi-setup.md#setup).

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] Online er allerede konfigurert for integrering med Power BI.

### <a name="sign-up-power-bi" />Registrer deg for Power BI

Før du kan bruke Power BI med [!INCLUDE[prod_short](includes/prod_short.md)], må du registrere deg for Power BI-tjenesten. Hvis du ikke allerede har registrert deg, går du til [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Når du registrerer deg, bruker du e-postadressen og passordet for jobben din.

## <a name="a-nameconnectaconnect-to-power-bi---one-time-only" /><a name="connect"></a>Koble til Power BI – bare én gang

Når du logger på [!INCLUDE [prod_short](includes/prod_short.md)] første gang, ser du sannsynligvis en tom Power BI-del (som vist i forrige figur) på ulike sider. Det første du må gjøre, er å koble til Power BI-kontoen. Når du er tilkoblet, kan du se rapporter. Du trenger bare å utføre dette trinnet én gang.

1. Velg koblingen **Komme i gang med Power BI** i delen **Power BI-rapporter**.
2. Det assisterte oppsettet **Oppsett Power BI-rapporter i Business Central** starter. Velg **Neste** for å fortsette.
3. På siden **Kontroller Power BI-lisensen**. Gjør ett av følgende:

    - Hvis du ennå ikke har registrert deg for Power BI, velger du [Gå til startsiden for Power BI](https://powerbi.microsoft.com). Registrer deg for en konto, og kom deretter tilbake til [!INCLUDE[prod_short](includes/prod_short.md)] og fullfør oppsettet.

    - Hvis du allerede har en lisens, velger du **Neste**.
4. På neste siden skal [!INCLUDE[prod_short](includes/prod_short.md)] laste opp en demorapport til Power BI. Dette trinnet kan ta noen minutter, så det gjøres i bakgrunnen. Velg **Neste** og deretter **Fullfør** for å fullføre oppsettet.

Tilkoblingsprosessen starter. Under prosessen kommuniserer [!INCLUDE [prod_short](includes/prod_short.md)] med Power BI-tjenesten for å finne ut om du har en gyldig Power BI-konto og -lisens. Når lisensen er kontrollert, vises standard Power BI-rapportvisninger på siden. Hvis en rapport ikke vises, kan du velge en rapport fra delen.

> [!TIP]
> Med [!INCLUDE [prod_short](includes/prod_short.md)] Online blir Power BI-rapporter som brukes i [!INCLUDE [prod_short](includes/prod_short.md)], lastet opp automatisk til Power BI-arbeidsområdet i dette trinnet.

#### <a name="from-include-prodshortincludesprodshortmd-on-premises" />Fra [!INCLUDE [prod_short](includes/prod_short.md)] lokalt

Tilkoblingen til Power BI fra [!INCLUDE [prod_short](includes/prod_short.md)] er lignende den i Online. Du kan imidlertid bli bedt om å gi tilgang til Power BI-tjenester på siden **TILLATELSER FOR AZURE ACTIVE DIRECTORY-TJENESTEN**. Du gir tilgang ved å velge **Autoriser Azure-tjenester** og deretter **Godta**.

Når du er tilkoblet, kan du velge en rapport fra Power BI-delen på sider.

## <a name="work-with-power-bi-reports" />Arbeid med Power BI-rapporter

### <a name="show-reports-on-list-pages" />Vise rapporter på listesider

[!INCLUDE[prod_long](includes/prod_long.md)] omfatter en Power BI-faktaboks på flere viktige listesider. Denne faktaboksen gir ytterligere innsikt i dataene i listen. Når du flytter mellom radene i listen, er oppdateres og filtreres rapporten for den valgte posten.

Hvis du vil vite hvordan du oppretter rapporter for listesider, kan du se [Opprette Power BI-rapporter for visning av listedata i [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

> [!TIP]
> Hvis faktaboksen for Power BI ikke vises, kan den være skjult i arbeidsområdet ved hjelp av personalisering. Velg ![Innstillinger.](media/ui-experience/settings_icon_small.png "Innstillinger-ikon for rollesenter"). og velg deretter **Tilpass**-handlingen. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).
>
> Hvis du har en eldre versjon av Business Central, går du til handlingslinjen, velge **Handlinger** > **Vis** > **Vis/Skjul Power BI-rapporter**.

### <a name="switch-reports" />Bytte rapporter

En Power BI-del på en side kan vise enhver Power BI-rapport som er tilgjengelig for deg. Hvis du vil bytte til visning av en annen rapport, velger du **Velg rapport**-handlingen fra rullegardinkommandolisten øverst i delen.  

Siden **Valg av Power BI-rapporter** viser en oversikt over alle Power BI-rapportene du har tilgang til. Denne listen er hentet fra alle dine egne arbeidsområder eller arbeidsområder som er delt med deg i Power BI-tjenesten. Velg **Aktiver**-boksen for hver rapport du vil vise på siden, og velg deretter **OK**. Du kommer tilbake til siden, og den siste rapporten du aktiverte, vises. Ved hjelp av rullegardinkommandolisten bruker du kommandoene **Forrige** og **Neste** til å navigere mellom rapporter.  

### <a name="get-more-reports" />Hente flere rapporter

Hvis du ikke ser noen rapporter på siden **Valg av Power BI-rapporter** eller ikke ser ønsket rapport, velger du **Hent rapporter**. Med denne handlingen kan du se etter rapporter fra to plasseringer: *Min organisasjon* eller *Tjenester*.

- Velg **Min organisasjon** for å gå til Power BI-tjenestene. Herfra kan du vise rapportene i organisasjonen som du har fått tilgang til å vise. Deretter kan du legge dem til i arbeidsområdet.
- Velg **Tjenester** for å gå til Microsoft AppSource, der du kan installere Power BI-apper.  

> [!TIP]
> Hvis du har Power BI Desktop, kan du også opprette nye Power BI-rapporter. Når disse rapportene er publisert på Power BI-arbeidsområdet, vises de deretter på siden **Valg av Power BI-rapporter**.  

### <a name="manage-and-modify-reports" />Behandle og endre rapporter

Du kan foreta endringer i en rapport i Power BI-delen. Endringene du foretar, publiseres deretter i Power BI-tjenesten. Hvis rapporten deles med andre brukere, ser de også endringene, med mindre du lagrer endringene i en ny rapport.

Hvis du vil endre en rapport, velger du **Behandle rapport**-handlingen fra rullegardinkommandolisten i Power BI-delen. Begynn deretter å gjøre endringer. Når du er ferdig å gjøre endringer, velger du **Fil** > **Lagre**. Hvis det er en delt rapport og du ikke vil foreta endringen for alle brukere, velger du **Lagre som** for å unngå å foreta denne endringen for alle brukerne.

Når du går tilbake til rollesenteret, vises den oppdaterte rapporten. Hvis du brukte **Lagre som**, må du velge **Velg rapport** og deretter aktivere den nye rapporten for å se den.

> [!NOTE]
> Denne funksjonen er ikke tilgjengelig for [!INCLUDE [prod_short](includes/prod_short.md)] lokalt.

### <a name="a-nameuploadaupload-reports" /><a name="upload"></a>Laste opp rapporter

Power BI-rapporter kan distribueres mellom brukere som PBIX-filer. Hvis du har PBIX-filer, kan du laste opp og dele dem med alle brukere av [!INCLUDE [prod_short](includes/prod_short.md)]. Rapportene deles i hvert selskap i [!INCLUDE [prod_short](includes/prod_short.md)].  

For å laste opp en rapport velger du handlingen **Last opp rapport** fra rullegardinkommandolisten i delen **Power BI-rapporter**. Finn deretter PBIX-filen som definerer rapportene du vil dele. Du kan endre standardnavnet på filen.  

Når rapporten lastes opp til Power BI-arbeidsområdet ditt, lastes den også automatisk opp til andre brukeres Power BI-arbeidsområder.

> [!NOTE]
> Du må ha SUPER-brukertillatelser i [!INCLUDE[prod_short](includes/prod_short.md)] for å kunne laste opp en rapport. Du kan i tillegg ikke laste opp rapporter med [!INCLUDE [prod_short](includes/prod_short.md)] lokalt. Med den lokale versjonen laster du opp rapporter direkte til Power BI-arbeidsområdet. Hvis du vil ha mer informasjon, kan du se [Arbeid med [!INCLUDE [prod_short](includes/prod_short.md)]-data i Power BI](across-working-with-business-central-in-powerbi.md).

## <a name="fixing-problems" />Løse problemer

Hvis noe går galt, vil denne delen imidlertid gi en løsning for de vanligste problemene.  

### <a name="you-dont-have-a-power-bi-account" />Du har ikke en Power BI-konto

En Power BI-konto er ikke opprettet. For å kunne få en gyldig Power BI-konto må du ha en lisens, og du må ha logget på Power BI tidligere for å opprette et Power BI-arbeidsområde.

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display" />Melding: Det finnes ingen aktiverte rapporter. Klikk Velg rapport for å se en liste over rapporter du kan vise.

Denne meldingen vises hvis standardrapporten ikke kan distribueres til Power BI-arbeidsområdet. Eller den ble distribuert, men ikke oppdatert. Naviger til rapporten i Power BI-arbeidsområdet, velg **Datasett** og **Innstillinger**, og oppdater deretter legitimasjonen manuelt. Når datasettet er oppdatert, går du tilbake til [!INCLUDE[prod_short](includes/prod_short.md)] og velger rapporten fra **Velg rapporter**-siden manuelt.

#### <a name="you-cant-see-a-report-on-the-select-report-page-on-a-list-page" />Du kan ikke se en rapport på Velg rapport-siden på en listeside

Dette skjer sannsynligvis fordi navnet på rapporten ikke inneholder navnet på listesiden. Fjern filteret for å få en fullstendig liste over tilgjengelige Power BI-rapporter.

## <a name="see-related-microsoft-trainingtrainingmodulesconfigure-powerbi-excel-dynamics--business-centralindex" />Se relatert [Microsoft-opplæring](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also" />Se også

[Business Central og Power BI](admin-powerbi.md)  
[Bygg Power BI-rapporter for å vise [!INCLUDE [prod_long](includes/prod_long.md)]-data](across-how-use-financials-data-source-powerbi.md)  
[Oversikt over komponent og arkitektur for Power BI-integrering for [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Arbeid med [!INCLUDE [prod_short](includes/prod_short.md)]-data i Power BI](across-working-with-business-central-in-powerbi.md)  
[Power BI for forbrukere](/power-bi/consumer/end-user-consumer)  
[Nytt utseende på Power BI-tjenesten](/power-bi/service-new-look)  
[Hurtigstart: Koble til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI-dokumentasjon](/power-bi/)  
[Forretningsintelligens](bi.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Importer forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Bruk [!INCLUDE[prod_short](includes/prod_short.md)] som en Power Apps-datakilde](across-how-use-financials-data-source-powerapps.md)  
[Bruk [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]
