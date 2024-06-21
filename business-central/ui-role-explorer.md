---
title: Utforske og navigere sider og rapporter per rolle
description: 'Du kan få en oversikt over alle forretningsfunksjonene som er tilgjengelige for din rolle, og for andre roller med rolleutforskeren.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'role explorer, find features, navigate'
ms.search.form: 'RoleExplorer, 9020, 9022, 9027, 9024'
ms.date: 08/01/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# <a name="finding-pages-and-reports-with-the-role-explorer"></a>Finne sider og rapporter med rolleutforskeren

Du kan få en oversikt over alle forretningsfunksjonene som er tilgjengelige for din rolle, og for andre roller hvis du går videre. I denne artikkelen omtales funksjonsoversikten som *rolleutforskeren*.

Hvert element i rolleutforskeren er en handling som åpner en side eller rapport. Du kan også bruke rolleutforskeren som en metode for å navigere i [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="open-the-role-explorer"></a>Åpne rolleutforskeren

Du kan åpne rolleutforskeren fra rollesenteret og alle listesider og fra **Fortell meg**-vinduet.

- I rollesenteret eller på en listeside velger du knappen ![Meny-knapp.](media/ui_menu_button.png "Meny-knapp") til høyre for navigasjonsfeltet eller trykker på <kbd>Skift</kbd>+<kbd>F12</kbd>.
- I **Fortell meg**-vinduet velger du **utforsker**-handlingen nederst.

Første gang du åpner rollesenteret, viser det koblinger til de fleste funksjonene som er tilgjengelige for din rolle.

## <a name="open-the-role-explorer-filtered-to-show-reports"></a>Åpne rolleutforskeren filtrert for å vise rapporter

Du kan åpne rolleutforskeren i en visning som er filtrert, for å vise rapporter fra rollesenteret og alle listesider og fra **Fortell meg**-vinduet:

- I rollesenteret eller på en listeside velger du **Alle rapporter**-koblingen på høyre side av navigasjonslinjen.
- I **Fortell meg**-vinduet velger du handlingen **utforske rapporter** nederst.

## <a name="navigate-features"></a>Naviger funksjoner

Handlingene som åpner sider eller rapporter, er ordnet under noder som er oppkalt etter funksjonene eller modulene. Du kan skjule eller utvide hver node enkeltvis eller alle noder samtidig.

- Hvis du vil vise eller skjule en individuell node, velger du noden. Dette gjelder noder på øverste nivå og undernoder.
- Hvis du vil vise/skjule alle noder på øverste nivå på siden, men beholde undernodene som de er, velger du **...** øverst og velger deretter **Vis** eller **Skjul**.
- Hvis du vil vise/skjule alle noder på øverste nivå og alle undernoder under den, velger du **...** øverst og velger deretter **Vis alle** eller **Skjul alle**.

## <a name="search-for-features"></a>Søk etter funksjoner

Du kan raskt finne funksjoner ved å velge **Søk** og deretter skrive inn et ord eller uttrykk for funksjonen du prøver å finne. Rollesenteret uthever all tilsvarende tekst. Hvis en funksjon er skjult i en skjult node, markeres den skjulte noden med en prikk. 

## <a name="explore-other-roles"></a>Utforsk andre roller

Du kan utforske andre roller enn dine egne ved å velge **Utforsk flere roller**. Rollesenteret viser hver rolle under sin egen overskrift, med koblinger til funksjonene i den. Du kan finne og gå til funksjoner på samme måte som når du utforsker rollen.

> [!NOTE]
> Du har bare tilgang til roller som er konfigurert for visning i rolleutforskeren. Hvis en rolle ikke er tilgjengelig, er den sannsynligvis ikke konfigurert for dette. Hvis du vil ha mer informasjon, kan du se [Administrere profiler](admin-users-profiles-roles.md). 

Når du utforsker andre roller, kan du også avgrense utforskeren ved hjelp av handlingene **Rapport og analyse** og **Administrasjon** øverst i rollesenteret.

- **Rapport og analyse** viser bare funksjonene som er kategorisert som rapporterings- og analysefunksjoner.
- **Administrasjon** viser bare funksjonene som er kategorisert som administrasjonsfunksjoner.

> [!TIP]
> For utviklere kategoriserer du sider og rapporter ved å angi [UsageCategory-egenskapen](/dynamics365/business-central/dev-itpro/developer/properties/devenv-usagecategory-property) i objektets Al-kode.
<!--
 
## <a name="role-explorer-actions"></a>Role explorer actions

There a several actions along the top of the role explorer to help you locate features of your role and other roles.

|Action|Description|
|------|------|
|**All**|Shows all features that are related to the role.|
|**Find**|Lets you enter a word or phrase to quickly locate feature names that match.|
|**Explore more roles**|All business features that are available for all roles including your own. When exploring all roles, the other actions work the same way, except for all roles shown. **NOTE:** You can only access roles that are set up to show in role explorer. For more information, see [Manage Profiles](admin-users-profiles-roles.md).  |
|**Report & Analysis**|This action Shows only those features that are categorized as reports and analysis features.|
|**Administration**|Shows only those features that are categorized as administration features.|



<!--
Choose the **Find** action at the top of the role explorer to quickly locate feature names that contain a certain term.

Choose the **Explore more roles** action at the top of the role explorer to get an overview of all business features that are available for all roles including your own.

> [!NOTE]
> Only Role Center actions for profiles where the **Show in Role Explorer** check box is selected will appear on the extended version of the role explorer (shown with the **Explore more roles** action). For more information, see [Manage Profiles](admin-users-profiles-roles.md).
-->

## <a name="expand-and-collapse-nodes-on-the-role-explorer"></a>Vi og skjul noder i rolleutforskeren

Handlingene som åpner sider, er ordnet under noder som er oppkalt etter funksjonene eller modulene. Hver node kan skjules eller utvides enkeltvis, og du kan skjule/utvide alle noder samtidig.

- Hvis du vil vise eller skjule en node, velger du noden. Dette gjelder noder på øverste nivå og undernoder.
- Hvis du vil vise/skjule alle noder på øverste nivå på siden, velger du handlingen **Utvid** eller **Skjul** i øvre høyre hjørne.
- Hvis du vil vise/skjule alle noder på øverste nivå og alle undernoder under den, gjør du ett av følgende:
  - Velg <kbd>Ctrl</kbd>+<kbd>Skift</kbd> mens du velger handlingen **Utvid** eller **Skjul** i øvre høyre hjørne.
  - Velg **...** i øvre høyre hjørne, og velg deretter **Vis alle** eller **Skjul alle**.

## <a name="see-also"></a>Se også

[Finne sider og informasjon med Fortell meg](ui-search.md)  
[Administrere profiler](admin-users-profiles-roles.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
