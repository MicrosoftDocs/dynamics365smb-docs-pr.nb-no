---
title: Bruk dataene til å lage en app | Microsoft-dokumenter
description: Du kan gjøre Business Central-dataene tilgjengelige som en datakilde og angi en OData-URL-adresse til webtjenestene dine for å utvikle en forretningsapp ved hjelp av Power Apps.
author: jswymer
ms.topic: conceptual
ms.service: dynamics365-business-central
ms.search.keywords: 'OData, Power App, SOAP'
ms.date: 05/15/2023
ms.author: jswymer
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a>Koble til Business Central-dataene for å utvikle en forretningsapp ved hjelp av Power Apps

Du kan gjøre [!INCLUDE[prod_short](includes/prod_short.md)]-data tilgjengelige som en datakilde i Power Apps.  

> [!TIP]  
> Business Central tilbyr nå utviklings- og driftsstøtte for Power Platform i AL-Go og eksempler for å komme i gang med å opprette dine egne apper med Power Apps. Disse funksjonene er foreløpig i forhåndsversjon. Hvis du vil ha mer informasjon, kan du gå til [Business Central og Power Apps](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-overview) i hjelpen for utviklere og IT-eksperter.

## <a name="prerequisites"></a>Forutsetninger

Du må ha en gyldig konto med [!INCLUDE[prod_short](includes/prod_short.md)] og med Power Apps.  

## <a name="add--as-a-data-source-in-power-apps"></a>Legge til [!INCLUDE[prod_short](includes/prod_short.md)] som en datakilde i Power Apps

Denne fremgangsmåten legger til en Business Central-tabell, for eksempel kunder eller varer, som datakilden for en Power Apps-app.

1. I nettleseren går du til [powerapps.microsoft.com](https://powerapps.microsoft.com/) og logger deg på.
2. Velg **+ Opprett** i navigasjonsruten til venstre, og velg deretter **Flere data kilder** på siden **Opprett app**.
  
   <!-- This step opens Power Apps canavs. On first sign-in, you must specify the country/region.  -->
3. **Tilkoblinger**-listen viser alle eksisterende datatilkoblinger du har.

   - Hvis det allerede finnes en **Business Central**-tilkobling, merker du den og velger **Opprett**.

   - Hvis du ikke ser en Business Central-tilkobling, velger du **+ Ny tilkobling**, søker etter og velger **Business Central** og velger deretter **Opprett**.

   > [!NOTE]
   > Hvis du vil koble til [!INCLUDE[prod_short](includes/prod_short.md)] lokalt, må du velge **Business Central (lokalt)**-koblingen.  
  
4. Power Apps kobler seg til [!INCLUDE[prod_short](includes/prod_short.md)]. Logg deg på med Business Central-kontonavnet og -passordet. Hvis du ikke er administrator i [!INCLUDE[prod_short](includes/prod_short.md)], må du kanskje logge på med en annen konto.  
5. Når du er pålogget, viser Power Apps en liste over *Miljøer og selskaper* som er tilgjengelige fra [!INCLUDE[prod_short](includes/prod_short.md)]. Velg miljøet og selskapet som inneholder dataene du vil koble til, for ekssempel *PRODUKSJON – Mitt selskap*.  
6. Deretter vises en liste over tabeller som vises som en del av API-et for ditt miljø. Velg tabellen du vil koble til, og velg deretter **Koble til**.

Disse tabellene vises som endepunkter av [!INCLUDE[prod_short](includes/prod_short.md)]-koblingen for Power Apps.  

> [!NOTE]
> Hvis du vil inkludere data fra andre tabeller i [!INCLUDE[prod_short](includes/prod_short.md)] i appen, må du samarbeide med en utvikler for å definere en egendefinert API i [!INCLUDE[prod_short](includes/prod_short.md)].  

Nå har du koblet til [!INCLUDE[prod_short](includes/prod_short.md)]-dataene og er klar til å begynne å bygge din Power App. Du kan alltids legge til flere skjermbilder og koble til flere data. Finn ut mer under [Opprett en lerretsapp fra et eksempel i Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

Når du har utformet og bygd appen, kan du dele den med kollegene dine. Hvis du vil ha mer informasjon, kan du se [Lagre og publisere en lerretsapp i Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

<!--
## <a name="sample-apps-to-get-started"></a>Sample apps to get started

As a preview version, Business Central offers several sample apps that you can use as a starting point for building your own apps that use Business Central data. These sample apps are available in the [Business Central Demos](https://github.com/BusinessCentralDemos) repo on GitHub. For a quick overview on the apps, go to [Power Apps samples for Business Central](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-samples).

## <a name="develop-and-maintain-apps-application-lifecycle-management"></a>Develop and maintain apps application lifecycle management

As an app developer, you may already be familiar with Business Central AL-Go. AL-Go is set of tools on GiHub that enables you to maintain professional DevOps processes for your Business Central AL projects. AL-Go supports source control and activities, like building, testing, and deploying. As a preview, Business Central now offers an Al-Go version that supports for Power Platform solutions. The preview, for example, includes workflows that let you push and pull Power Platfrom changes to and from enviroments. You can access the tools at [https://github.com/BusinessCentralDemos/AL-Go-PTE](https://github.com/BusinessCentralDemos/AL-Go-PTE). For more information, see [Application lifecycle management for Power Apps in Business Central](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-alm).-->

## <a name="see-also"></a>Se også

[Opprette en lerretsapp fra en mal i Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Importer forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Komme i gang med å utvikle tilkoblingsapper for Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
