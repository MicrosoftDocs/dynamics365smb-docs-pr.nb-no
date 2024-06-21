---
title: Bytte til et annet selskap eller miljø
description: 'Hvis du arbeider for flere organisasjoner, kan du raskt bytte mellom miljøet og selskapene.'
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'environments, companies, tenants, organization'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 04/24/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="switching-to-another-company-or-environment"></a>Bytte til et annet selskap eller miljø

[!INCLUDE [prod_short](includes/prod_short.md)] er tilgjengelig i mange forskjellige land/områder og støtter mange forskjellige typer organisasjoner. Organisasjonen kan velge å organisere arbeidet i [!INCLUDE [prod_short](includes/prod_short.md)] i flere *selskaper* og *miljøer*. Denne artikkelen hjelper deg med å forstå viktige forskjeller og hvordan du arbeider på tvers av dem.

## <a name="about-companies-and-environments"></a>Om selskaper og miljøer

[!INCLUDE [company_environment](includes/company_environment.md)]

> [!TIP]
> Hvis du ofte bytter mellom selskaper eller arbeider med [!INCLUDE[prod_short](includes/prod_short.md)] fra en annen app, som Microsoft Teams, kan det være lett å miste oversikten over hvor du er. For å hjelpe deg med å holde oversikt kan du legge til et merke som viser selskapsnavnet, slik at du raskt kan kontrollere at du er på riktig sted. Hvis du vil ha mer informasjon, kan du se [Vis et selskapsmerke](admin-company-information.md#badge).
> 
> Avhengig av hvilken nettleser du har, kan du også feste de forskjellige selskapene til favoritterstolpen.  

<!--
[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]-->

## <a name="features-for-switching-company-or-environment"></a>Funksjoner for å bytte selskap eller miljø

Det finnes noen funksjoner du kan bruke til å bytte mellom selskap eller miljø mens du arbeider. Tabellen nedenfor sammenligner funksjonene i funksjonen, som forklares nærmere i delene nedenfor.

|Funksjon|Bytt selskap|Bytt miljø|Bytt i ny nettleserfane| Tilgjengelig lokalt|
|-------|--------------|------------------|-------------------------|----------------------|
|[Bytting av selskap](#use-the-company-switcher)|![avmerking](media/check.png "avmerking")|![avmerking](media/check.png "avmerking")|![avmerking](media/check.png "avmerking")|![avmerking](media/check.png "avmerking")|
|[Appstartprogram](#use-the-app-launcher)||![avmerking](media/check.png "avmerking")|![avmerking](media/check.png "avmerking")||
|[Mine innstillinger](#use-my-settings)|![avmerking](media/check.png "avmerking")|||![avmerking](media/check.png "avmerking")|
|[Selskapssenter](#use-company-hub)|![avmerking](media/check.png "avmerking")|![avmerking](media/check.png "avmerking")|![avmerking](media/check.png "avmerking")||

## <a name="use-the-company-switcher"></a>Bruk bytting av selskap

Bruk av bytting av selskap er sannsynligvis den raskeste og mest allsidige måten å bytte selskap på. Bytting av selskap er en rute som er lett tilgjengelig fra alle sider. Ruten gir en oversikt over alle selskapene i alle miljøer du har tilgang til, og lar deg bytte direkte til en av dem – enten i samme nettleserfane eller i en ny en. Det er spesielt nyttig når du arbeider i mange selskaper på tvers av forskjellige miljøer.

1. I øvre høyre hjørne vises enten standard selskapsikon, som ![startprogram for selskap-ikon.](media/ui-experience/company-icon.png "Viser ikonet for bytting av selskap som brukes når det er et enkelt miljø") og ![company-icon-mult-env](media/ui-experience/company-icon-multi-env.png "Viser ikonet for bytting av selskap som brukes når det er flere miljøer") eller et [egendefinert merke](admin-company-information.md#badge) for selskapet du arbeider med. Velg ikonet for å åpne ruten for bytting av selskap.

   :::image type="content" source="media/ui-experience/company-switch-2.png" alt-text="Viser ikonet for bytting av selskap i overskriften til Business Central-klienten.":::  

   > [!TIP]
   > Du kan også bruke <kbd>CRTL</kbd>+<kbd>O</kbd>-hurtigtasten til å åpne ruten.
2. I ruten **Tilgjengelige selskaper** velger du selskapet du vil bytte til, velger pilen **Bytt** og velger et av følgende alternativer:

   |Alternativ|Description|
   |------|-----------|
   |Bytt|Åpner rollesenteret for valgt selskap i samme nettleserfane som du arbeider med. Selskapet blir standardselskapet som åpnes i Business Central, til du bytter igjen eller endrer selskapet ved hjelp av **Mine innstillinger**. |
   |Åpne i ny fane|Åpner rollesenteret for valgt selskap i en ny nettleser fane, og holder det opprinnelige selskapet åpent i den andre fanen.|
   |Åpne i ny fane og gå til samme side|Dette alternativet er bare aktivt på listesider, for eksempel kunder, salgsordrer eller varer. Den åpner samme liste, men for det valgte selskapet, i en ny nettleserfane. |

> [!TIP]
> Velg <kbd>F5</kbd> for å oppdatere listen over miljøer og selskaper.

## <a name="use-the-app-launcher"></a>Bruk startprogrammet for appen

Når du er logget på [!INCLUDE[prod_short](includes/prod_short.md)], er miljøene du har tilgang til, tilgjengelige i Microsoft 365.  

1. Velg **Appstarter**-ikonet ![Appstarter.](media/app-launcher-icon.png "Appstarteren gir tilgang til flere funksjoner").
2. I ruten som åpnes ser du etter og velger [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du ikke ser [!INCLUDE[prod_short](includes/prod_short.md)], velger du **Alle apper**, og deretter angir du **Business Central** i **Søk**-boksen.

   :::image type="content" source="media/app-launcher-bc-tile.png" alt-text="Microsoft 365-appstarteren viser Business Central-flisen.":::  

3. Hvis det er mer enn ett miljø, blir du bedt om å velge miljøet du vil ha tilgang til.

> [!NOTE]
> Startprogrammet for apper er ikke tilgjengelig hvis du er logget på Business Central som gjest.

<!--
The following image shows tiles for accessing production and sandbox environments on the Dynamics 365 Home page.

:::image type="content" source="media/app-picker-environments.png" alt-text="The Dynamics 365 Home page showing production and sandbox environments.":::
-->
## <a name="use-my-settings"></a>Bruk Mine innstillinger

Når du er logget på [!INCLUDE[prod_short](includes/prod_short.md)], kan du raskt bytte til et annet selskap i samme miljø. Når du har byttet, blir selskapet du velger standardselskap og åpnes neste gang du logger på.

1. I øvre høyre hjørne velger du **Innstillinger**-ikonet ![Innstillinger.](media/ui-experience/settings_icon_small.png "Innstillinger-ikon for rollesenter"), og velg deretter handlingen **Mine innstillinger**.

    > [!TIP]
    > Du kan også bruke hurtigtasten <kbd>Alt</kbd>+<kbd>T</kbd> til å åpne siden Mine innstillinger på en rask måte.

2. Velg selskap på **Mine innstillinger**-siden i **Selskap**-feltet.  
3. Velg **OK**-knappen.

> [!TIP]
> En god måte å gå direkte til standardselskapet på når du logger på, og unngå å måtte angi et miljø, er å legge til nettadressen i listen over favoritter etter at du har logget på.

## <a name="use-company-hub"></a>Bruk selskapssenter

*Selskapssenter* er et meget spesialisert rollesenter som gir en økonomisk oversikt over selskaper og miljøer. Selskapssenteret er tilgjengelig som en [utvidelse](ui-extensions-company-hub.md) og gir et instrumentbord med oppsummeringsdata for hvert selskap du har tilgang til. Startsiden viser finansielle KPI-er og en direkte kobling til de enkelte miljøene og selskapene. Hvis du vil ha mer informasjon, kan du se [Administrere arbeid på tvers av flere selskaper i selskapshuben](company-hub.md).

[![Viser siden for selskapssenteret som viser alle selskaper.](media/company-hub.png)](media/company-hub.png#lightbox)  

## <a name="see-also"></a>Se også

[Opprette nye seleskaper i [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md)  
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Miljøer og selskaper (bare på engelsk)](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology)  
[Selskapsinformasjon](admin-company-information.md)  
[Administrasjonssenter for Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
