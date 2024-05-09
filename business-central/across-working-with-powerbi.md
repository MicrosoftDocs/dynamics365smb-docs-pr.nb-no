---
title: Arbeide med Power BI-rapporter i Business Central | Microsoft Docs
description: 'Få innsikt, forretningsanalyse og KPI-er fra Business Central-dataene med Power BI.'
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 04/24/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Arbeid med Power BI-rapporter i [!INCLUDE [prod_short](includes/prod_short.md)]

I denne artikkelen får du grunnleggende informasjon om å arbeide med rapporter. Dette inkluderer visning av Power BI-rapporter i [!INCLUDE [prod_short](includes/prod_short.md)] (inkludert målstyringer og instrumentbord) og redigering av Power BI-rapporter som bruker [!INCLUDE [prod_short](includes/prod_short.md)] som datakilde. Artikkelen tar for seg noen aspekter som hjelper deg å komme i gang som [!INCLUDE[prod_short](includes/prod_short.md)]-bruker. Når det gjelder generelle retningslinjer og instruksjoner for hvordan du bruker Power BI, kan du se [Power BI-dokumentasjon for forbrukere](/power-bi/consumer).

## Oversikt

Power BI-rapporter gir deg innsikt i [!INCLUDE[prod_short](includes/prod_short.md)]. Ulike sider i [!INCLUDE [prod_short](includes/prod_short.md)] inkluderer en Power BI-rapportdel som kan vise Power BI-rapporter. Rollesenteret er en vanlig side der du ser en Power BI-rapportdel. Noen listesider, for eksempel **Varer**, omfatter også en Power BI-del.

[!INCLUDE [prod_short](includes/prod_short.md)] fungerer sammen med Power BI-tjenesten. Rapporter som skal vises i [!INCLUDE [prod_short](includes/prod_short.md)], er lagret i en Power BI-tjeneste. I [!INCLUDE [prod_short](includes/prod_short.md)] kan du bytte rapporten som vises i Power BI-delen, til enhver Power BI-rapport som er tilgjengelig i Power BI-tjenesten. Delene kommer til å være tomme første gang du logger på [!INCLUDE [prod_short](includes/prod_short.md)], og til du kobler til en Power BI-tjeneste, som vist her:

![Power BI-del i Business Central.](./media/power-bi-part.png)

## Kom i gang

> [!NOTE]
> [!INCLUDE [prod_short](includes/prod_short.md)] Online er allerede konfigurert for integrering med Power BI.

### Registrer deg for Power BI

Før du kan bruke Power BI med [!INCLUDE[prod_short](includes/prod_short.md)], må du registrere deg for Power BI-tjenesten. Hvis du ikke allerede har registrert deg, går du til [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Når du registrerer deg, bruker du e-postadressen og passordet for jobben din.

Når du har en Power BI-konto, kan du logge deg på på [https://powerbi.microsoft.com/](https://powerbi.microsoft.com/).

Power BI-tjenesten er vert for alle rapportene som er tilgjengelige for deg. Hvis du vil se en rapport i det personlige arbeidsområdet, velger du **Mitt arbeidsområde**  >  **Rapporter**. Deretter velger du bare rapporten du vil vise. Hvis du har tilgang til et eller flere delte Power BI-arbeidsområder, kan du også se rapporter i disse arbeidsområdene.

Med [!INCLUDE[prod_short](includes/prod_short.md)] Online får du automatisk et sett med standardrapporter på arbeidsområdet. Hvis du vil opprette egne rapporter, kan du bruke Power BI Desktop til å opprette dem og deretter publisere dem på arbeidsområdet ditt. Hvis du vil ha mer informasjon, kan du se [Komme i gang med å bygge rapporter i Power BI Desktop for å vise [!INCLUDE [prod_long](includes/prod_long.md)]-data](across-how-use-financials-data-source-powerbi.md).

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

## <a name="connect"></a>Koble til Power BI – bare én gang

Når du logger på [!INCLUDE [prod_short](includes/prod_short.md)] første gang, ser du sannsynligvis en tom Power BI-del (som vist i forrige figur) på ulike sider. Det første du må gjøre, er å koble til Power BI-kontoen. Når du er tilkoblet, kan du se rapporter. Du trenger bare å utføre dette trinnet én gang.

1. Velg koblingen **Komme i gang med Power BI** i delen **Power BI-rapporter**.
2. Det assisterte oppsettet **Oppsett Power BI-rapporter i Business Central** starter. Velg **Neste** for å fortsette.
3. På siden **Kontroller Power BI-lisensen**. Gjør ett av følgende:

    - Hvis du ennå ikke har registrert deg for Power BI, velger du [Gå til startsiden for Power BI](https://powerbi.microsoft.com). Registrer deg for en konto, og kom deretter tilbake til [!INCLUDE[prod_short](includes/prod_short.md)] og fullfør oppsettet.

    - Hvis du allerede har en lisens, velger du **Neste**.
4. På neste siden skal [!INCLUDE[prod_short](includes/prod_short.md)] laste opp en demorapport til Power BI. Dette trinnet kan ta noen minutter, så det gjøres i bakgrunnen. Velg **Neste** og deretter **Fullfør** for å fullføre oppsettet.

Tilkoblingsprosessen starter. Under prosessen kommuniserer [!INCLUDE [prod_short](includes/prod_short.md)] med Power BI-tjenesten for å finne ut om du har en gyldig Power BI-konto og -lisens. Når lisensen er kontrollert, vises standard Power BI-rapportvisninger på siden. Hvis en rapport ikke vises, kan du velge en rapport fra delen.

> [!TIP]
> Med [!INCLUDE [prod_short](includes/prod_short.md)] Online laster dette trinnet automatisk opp Power BI-rapporter som brukes i [!INCLUDE [prod_short](includes/prod_short.md)], til Power BI-arbeidsområdet.

<!--#### From [!INCLUDE [prod_short](includes/prod_short.md)] on-premises

Connecting to Power BI from [!INCLUDE [prod_short](includes/prod_short.md)] is similar to online. However, you might be prompted on the **MICROSOFT ENTRA SERVICE PERMISSIONS** page to grant access to Power BI Services. To grant access, select **Authorize Azure Services**, and then **Accept**.

Once connected, you can select a report from the Power BI part on pages.-->

## Arbeid med Power BI-rapporter

### Få de nyeste dataene

Hver Power BI-rapport er basert på et datasett som henter data fra [!INCLUDE[prod_short](includes/prod_short.md)]-kildene. Du må sørge for at dataene i Power BI-rapportene er oppdatert med dataene i [!INCLUDE[prod_short](includes/prod_short.md)]. Dette begrepet omtales som *oppdatering*.  Det kan hende at oppdatering ikke skjer automatisk, avhengig av hvordan organisasjonen har konfigurert Power BI. Du kan oppdatere data på to måter: manuelt eller ved å planlegge en oppdatering. Manuell oppdatering utføres etter behov. Planlagt oppdatering lar deg oppdatere automatisk ved angitte tidsintervaller.

#### Oppdatere manuelt

Fra Power BI på nettet velger du **Flere alternativer (...)** ved siden av datasettet under **Datasett** i navigasjonsruten, og velger deretter **Oppdater nå**.

#### Planlegge en oppdatering

Fra Power BI på nettet velger du Flere alternativer (...) ved siden av datasettet under Datasett i navigasjonsruten, og velg deretter **Planlegg oppdatering**. Fyll inn informasjonen under **Planlegg oppdatering**, og velg **Bruk**.

Hvis du vil ha mer informasjon, kan du se [Konfigurere planlagt oppdatering](/power-bi/connect-data/refresh-scheduled-refresh)

### Vise rapporter på listesider

[!INCLUDE[prod_long](includes/prod_long.md)] omfatter en Power BI-faktaboks på flere viktige listesider. Denne faktaboksen gir ytterligere innsikt i dataene i listen. Når du flytter mellom radene i listen, er oppdateres og filtreres rapporten for den valgte posten.

Hvis du vil vite hvordan du oppretter rapporter for listesider, kan du se [Opprette Power BI-rapporter for visning av listedata i [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

> [!TIP]
> Hvis faktaboksen for Power BI ikke vises, kan den være skjult i arbeidsområdet ved hjelp av personalisering. Velg ![Innstillinger.](media/ui-experience/settings_icon_small.png "Innstillinger-ikon for rollesenter"). og velg deretter **Tilpass**-handlingen. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).
>
> Hvis du har en eldre versjon av Business Central, går du til handlingslinjen, velge **Handlinger** > **Vis** > **Vis/Skjul Power BI-rapporter**.

### Bytte rapporter

En Power BI-del på en side kan vise enhver Power BI-rapport som er tilgjengelig for deg. Hvis du vil bytte til visning av en annen rapport, velger du **Velg rapport**-handlingen fra rullegardinkommandolisten øverst i delen.  

Siden **Valg av Power BI-rapporter** viser en oversikt over alle Power BI-rapportene du har tilgang til. Denne listen er hentet fra alle dine egne arbeidsområder eller arbeidsområder som er delt med deg i Power BI-tjenesten. Velg **Aktiver**-boksen for hver rapport du vil vise på siden, og velg deretter **OK**. Du kommer tilbake til siden, og den siste rapporten du aktiverte, vises. Ved hjelp av rullegardinkommandolisten bruker du kommandoene **Forrige** og **Neste** til å navigere mellom rapporter.  

### Hente flere rapporter

Hvis du ikke ser noen rapporter på siden **Valg av Power BI-rapporter** eller ikke ser ønsket rapport, velger du **Hent rapporter**. Med denne handlingen kan du se etter rapporter fra to plasseringer: *Min organisasjon* eller *Tjenester*.

- Velg **Min organisasjon** for å gå til Power BI-tjenestene. Herfra kan du vise rapportene i organisasjonen som du har fått tilgang til å vise. Deretter kan du legge dem til i arbeidsområdet.
- Velg **Tjenester** for å gå til Microsoft AppSource, der du kan installere Power BI-apper.  

> [!TIP]
> Hvis du har Power BI Desktop, kan du også opprette nye Power BI-rapporter. Når disse rapportene er publisert på Power BI-arbeidsområdet, vises de deretter på siden **Valg av Power BI-rapporter**.  

### Behandle og endre rapporter

Du kan foreta endringer i en rapport i Power BI-delen. Endringene du foretar, publiseres deretter i Power BI-tjenesten. Hvis rapporten deles med andre brukere, ser de også endringene, med mindre du lagrer endringene i en ny rapport.

Hvis du vil endre en rapport, velger du **Behandle rapport**-handlingen fra rullegardinkommandolisten i Power BI-delen. Begynn deretter å gjøre endringer. Når du er ferdig å gjøre endringer, velger du **Fil** > **Lagre**. Hvis det er en delt rapport og du ikke vil foreta endringen for alle brukere, velger du **Lagre som** for å unngå å foreta denne endringen for alle brukerne.

Når du går tilbake til rollesenteret, vises den oppdaterte rapporten. Hvis du brukte **Lagre som**, må du velge **Velg rapport** og deretter aktivere den nye rapporten for å se den.

> [!NOTE]
> Denne funksjonen er ikke tilgjengelig for [!INCLUDE [prod_short](includes/prod_short.md)] lokalt.

### <a name="upload"></a>Laste opp rapporter

Power BI-rapporter kan distribueres mellom brukere som PBIX-filer. Hvis du har PBIX-filer, kan du laste opp og dele dem med alle brukere av [!INCLUDE [prod_short](includes/prod_short.md)]. Rapportene deles i hvert selskap i [!INCLUDE [prod_short](includes/prod_short.md)].  

For å laste opp en rapport velger du handlingen **Last opp rapport** fra rullegardinkommandolisten i delen **Power BI-rapporter**. Finn deretter PBIX-filen som definerer rapportene du vil dele. Du kan endre standardnavnet på filen.  

Når rapporten lastes opp til Power BI-arbeidsområdet ditt, lastes den også automatisk opp til andre brukeres Power BI-arbeidsområder.

> [!NOTE]
> Du må ha SUPER-brukertillatelser i [!INCLUDE[prod_short](includes/prod_short.md)] for å kunne laste opp en rapport via [!INCLUDE[prod_short](includes/prod_short.md)]. Du trenger ingen spesiell tillatelse for å laste opp rapporter til arbeidsområdet via Power BI-tjenesten.

## <a name="upload"></a>Laste opp rapporter fra filer

Power BI-rapporter kan distribueres mellom brukere som PBIX-filer. Hvis du har en PBIX-fil, kan du laste opp filen til et arbeidsområde. Gjør følgende for å laste opp en rapport:

1. Velg **Hent data** i det nye arbeidsområdet.

2. Velg **Hent** i Filer-boksen.

3. Velg **Lokal fil**, gå til plasseringen der du lagret filen, og velg **Åpne**.

Hvis du vil ha mer informasjon, kan du se [Laste opp rapporten til tjenesten](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

<!--
> [!NOTE]
> Uploading a report requires that you have a [Premium capacity](/power-bi/service-premium-what-is) work space. For more information, see [Managing Premium capacities](/power-bi/admin/service-premium-capacity-manage). -->

> [!TIP]
> Hvis du bruker [!INCLUDE[prod_short](includes/prod_short.md)] Online, kan du også laste opp en rapport fra [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Arbeid med Power BI-rapporter i [!INCLUDE [prod_short](includes/prod_short.md)] – last opp rapporter](across-working-with-powerbi.md#upload).

## <a name="share"></a>Dele rapporter med andre

Når rapporten er i arbeidsområdet ditt, kan du dele den med andre i organisasjonen.

Hvis du vil dele en rapport, velger du **Del** i en liste over rapporter eller i en åpen rapport. I **Del rapport**-ruten angir du de fullstendige e-postadressene til enkeltpersonene eller distribusjonsgruppene du vil dele med. Følg instruksjonene på skjermen for å fullføre delingen. Hvis du vil ha mer informasjon, kan du se [Dele et instrumentbord eller en rapport](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

> [!NOTE]
> Det kreves at både du og personene du deler rapporten med, har [Power BI Pro-lisens](/power-bi/service-features-license-type). Eller må innholdet være i en [Premium-kapasitet](/power-bi/service-premium-what-is). Hvis du vil ha mer informasjon, kan du se [Måter å dele arbeidet på i Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).

## Løse problemer

Hvis noe går galt, vil denne delen imidlertid gi en løsning for de vanligste problemene.  

### Du har ikke en Power BI-konto

En Power BI-konto er ikke opprettet. For å kunne få en gyldig Power BI-konto må du ha en lisens, og du må ha logget på Power BI tidligere for å opprette et Power BI-arbeidsområde.

### Melding: Det finnes ingen aktiverte rapporter. Klikk Velg rapport for å se en liste over rapporter du kan vise.

Denne meldingen vises hvis standardrapporten ikke kan distribueres til Power BI-arbeidsområdet. Eller den ble distribuert, men ikke oppdatert. Naviger til rapporten i Power BI-arbeidsområdet, velg **Datasett** og **Innstillinger**, og oppdater deretter legitimasjonen manuelt. Når datasettet er oppdatert, går du tilbake til [!INCLUDE[prod_short](includes/prod_short.md)] og velger rapporten fra **Velg rapporter**-siden manuelt.

#### Du kan ikke se en rapport på Velg rapport-siden på en listeside

Dette skjer sannsynligvis fordi navnet på rapporten ikke inneholder navnet på listesiden. Fjern filteret for å få en fullstendig liste over tilgjengelige Power BI-rapporter.

## Se også

[Business Central og Power BI](admin-powerbi.md)    
[Bygg Power BI-rapporter for å vise [!INCLUDE [prod_long](includes/prod_long.md)]-data](across-how-use-financials-data-source-powerbi.md)    
[Oversikt over komponent og arkitektur for Power BI-integrering for [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)    
[Koble deg til Power BI fra [!INCLUDE [prod_short](includes/prod_short.md)] lokalt](across-working-with-business-central-in-powerbi.md)    
[Power BI for forbrukere](/power-bi/consumer/end-user-consumer)     
[Nytt utseende på Power BI-tjenesten](/power-bi/service-new-look)    
[Hurtigstart: Koble til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)    
[Power BI-dokumentasjon](/power-bi/)    
[Forretningsintelligens](bi.md)    
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)    
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)    
[Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)    
[Bruk [!INCLUDE[prod_short](includes/prod_short.md)] som en Power BI-datakilde](across-how-use-financials-data-source-powerapps.md)    
[Bruk [!INCLUDE[prod_short](includes/prod_short.md)] som en Power Apps-datakilde](across-how-use-financials-data-source-powerapps.md)    
[Bruk [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]
