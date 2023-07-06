---
title: Endre grunnleggende innstillinger for gjeldende bruker
description: 'Lær hvordan du endrer enkelte grunnleggende innstillinger i Business Central, for eksempel rolle og rollesenteret, firmaer, arbeidsdatoer og tidssoner.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'change Role Center, notification, change company, change work date, decimal separator'
ms.search.form: '9022, 9019, 9027, 9020, 9026, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 08/31/2022
ms.author: jswymer
---
# <a name="change-basic-settings"></a><a name="change-basic-settings"></a><a name="change-basic-settings"></a>Endre grunnleggende innstillinger

På siden **Mine innstillinger** kan du vise og endre grunnleggende innstillinger for din forekomst av [!INCLUDE[prod_short](includes/prod_short.md)]. Endringene du gjør, påvirker bare ditt arbeidsområde, ikke arbeidsområdene til andre brukere.  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="role"></a><a name="role"></a><a name="role"></a><a name="role-center"></a>Rolle

Rollen fastslår startsiden, som er et startskjermbilde som er tilpasset behovene til en spesifikk rolle i en organisasjon. Avhengig av rollen din, gir startsiden eller rollesenteret deg en oversikt over bedriften, avdelingen eller dine egne oppgaver. Det kan også hjelpe deg med å navigere til daglige oppgaver og finne arbeid som er tilordnet til deg.

* Øverst i navigeringen kan du veksle mellom kunder, leverandører, varer og andre viktige lister med opplysninger. På samme måte kan handlinger la deg opprette oppgaver, for eksempel opprette en ny salgsfaktura direkte fra startsiden.

* I midten finner du **Aktiviteter**-området, som viser gjeldende data og kan velges for å vise mer detaljert informasjon. Sentrale ytelsesindikatorer (KPIer) kan settes opp for å vise et valgt diagram for en visuell fremstilling av for eksempel kontantstrøm eller inntekter og utgifter. Du kan også bygge opp en liste over favorittkunder på hjemmesiden for forretningsforbindelser som du gjør forretninger med ofte eller må vie spesiell oppmerksomhet.

### <a name="change-the-role"></a><a name="change-the-role"></a><a name="change-the-role"></a>Endre rollen

Standardrollen er **Forretningsleder**, men du kan velge en annet rolle for å bruke et rollesenter som passer bedre til dine behov.  

1. I øvre høyre hjørne velger du **Innstillinger**-ikonet ![Innstillinger.](media/ui-experience/settings_icon_small.png "Innstillinger-ikon for rollesenter"), og velg deretter handlingen **Mine innstillinger**.
2. På siden **Mine innstillinger**, i feltet **Rolle**, velger du rollen som du vil angi som standard. Velg for eksempel **Revisor**.
3. Velg **OK**.

## <a name="company"></a><a name="company"></a><a name="company"></a><a name="company"></a>Selskap

Et selskap fungerer som en beholder for data i [!INCLUDE[prod_short](includes/prod_short.md)]. Det kan være flere firmaer i en database, men du kan velge bare ett om gangen. Standardfirma kalles CRONUS og inneholder demonstrasjonsdata bare.

**Selskap**-feltet viser selskapet du arbeider i for øyeblikket, og du kan bruke det til å bytte til et annet selskap. Selskapsnavnet vises alltid øverst i venstre hjørne og fungerer som en handling du kan velge for å gå tilbake til rollesenteret.

> [!TIP]
> Du kan også endre selskapet ved hjelp av bytting av selskap (CRTL + O). Hvis du vil ha mer informasjon om denne funksjonen og andre måter å endre selskap eller miljø på, kan du se [Bytte til et annet selskap eller miljø](ui-organization-switch.md).

Standardfirma kalles CRONUS og inneholder demonstrasjonsdata bare. Du kan opprette et nytt selskap med egendefinerte data. Hvis du vil ha mer informasjon, kan du se [Opprette nye selskaper](about-new-company.md).

<!--
### <a name="to-change-the-company-name"></a><a name="to-change-the-company-name"></a><a name="to-change-the-company-name"></a>To change the company name

The company name is always displayed at the top left corner and works as an action that you can choose to go back to the Role Center. You can change this name on the **Company Information** page.

1. Choose the ![Sprocket icon to open the Settings menu.](media/ui-experience/settings_icon_small.png) icon, and then choose the **Company Information** action.
2. In the **Name** field, enter the new company name.
3. Leave the page. The system restarts and displays the new company in the top-left corner.

### <a name="to-display-a-company-badge-for-quick-access-to-company-information"></a><a name="to-display-a-company-badge-for-quick-access-to-company-information"></a><a name="to-display-a-company-badge-for-quick-access-to-company-information"></a><a name="badge"></a>To display a company badge for quick access to company information

You can add a customized badge in the top-right corner, which you can choose to quickly view company name and tenant information in a pop-up box. The company badge is also useful when [!INCLUDE[prod_short](includes/prod_short.md)] is embedded in another application, like Microsoft Teams or in some other web application. In these cases, because the [!INCLUDE[web_client](includes/web_client.md)] displays less surrounding contextual information, the company badge serves as the only way to determine which company or environment a record belongs to.

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Company Information**, and then choose the related link.
2. On the **Company Badge** FastTab, fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

> [!NOTE]
> If a company badge is defined, then you cannot change the company name as described in [To change the company name](ui-change-basic-settings.md#to-change-the-company-name)-->

## <a name="work-date"></a><a name="work-date"></a><a name="work-date"></a><a name="work-date"></a>Arbeidsdato

Den mest brukte arbeidsdatoen er i dag. Du må kanskje endre arbeidsdatoen midlertidig for å utføre oppgaver, for eksempel å fylle ut transaksjoner for en dato som ikke er i dag.

> [!TIP]  
> I alle dataofelt skriver du inn **i** for å raskt angi i dag, og **a** for å raskt angi arbeidsdato, som er verdien i feltet **Arbeidsdato** på siden **Mine innstillinger**.

> [!IMPORTANT]  
> Når du endrer arbeidsdatoen, og hvis du logger ut eller bytter til et annet selskap, reverteres arbeidsdataene til standard arbeidsdato. Så neste gang du logger deg på eller bytter tilbake til det opprinnelige selskapet, må du kanskje angi arbeidsdatoen på nytt.

### <a name="work-date-indication"></a><a name="work-date-indication"></a><a name="work-date-indication"></a>Arbeidsdatoindikasjon

Arbeidsdatoen er viktig på sider som kan redigeres. Når arbeidsdatoen ikke er satt til dagens dato på en redigerbar side, vises to typer indikatorer på siden:

* Det vises en påminnelse øverst på siden som forteller deg hva arbeidsdatoen er satt til. Påminnelsen gir en direkte kobling til arbeidsdatoinnstillingen på siden **Mine innstillinger**, slik at du kan endre datoen hvis du vil. Fra purringen kan du også velge å lukke påminnelsen for resten av økten. Med mindre du endrer arbeidsdatoen til "i dag", vil påminnelsen vises neste gang du logger på.

* Hvis du lukker purringen, vises arbeidsdatoen vises i tittelen på siden.  

Hvis arbeidsdatoen ikke er angitt til gjeldende dag (i dag), vil gjeldende arbeidsdato vises øverst til venstre på alle sider der kan du redigere data.

## <a name="region"></a><a name="region"></a><a name="region"></a><a name="region"></a> Region

**Område**-innstillingen bestemmer hvordan datoer, klokkeslett, numre og valutaer vises eller formateres. Det bestemmer også hvilket tegn som brukes som desimalskilletegn når du bruker et numerisk tastatur til å angi data. Lær mer under [Angi data](ui-enter-data.md#decimal).

## <a name="language"></a><a name="language"></a><a name="language"></a><a name="language"></a> Språk

Endre visningsspråket. Dette feltet vises bare når det er mer enn ett språk som kan velges.

Det første språket bestemmes enten av systemansvarlig eller leserinnstillingene når du registrerer deg for [!INCLUDE[prod_short](includes/prod_short.md)]. Språket som du har angitt, vil bli brukt på alle enhetene du logger på fra, for eksempel telefon eller nettbrett.

Flere språk for [!INCLUDE[prod_short](includes/prod_short.md)] kan installeres fra AppSource. Alle støttede visningsspråk vises i listen. Systemansvarlig må installere den relevante språkappen på leieren før brukere kan bytte til det nye språket i [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="time-zone"></a><a name="time-zone"></a><a name="time-zone"></a>Tidssone

Definerer tidssonen du befinner deg i. Når du logger på [!INCLUDE [prod_short](includes/prod_short.md)] første gang, angis tidssonen basert på selskapets adresse. Endre den hvis den ikke stemmer med den fysiske plasseringen din.  

## <a name="notifications"></a><a name="notifications"></a><a name="notifications"></a>Varslinger

Velg koblingen *Endre når jeg mottar varslinger* for å vise eller endre varslingene som du får om bestemte hendelser eller statusendringer, når du for eksempel er i ferd med fakturere en kunde som har en forfalt saldo, eller den disponible beholdningen er lavere enn antallet du vil selge. Lær mer under [Administrer varslinger](ui-smart-notifications.md).

## <a name="teaching-tips"></a><a name="teaching-tips"></a><a name="teaching-tips"></a>Læringstips

[!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)]

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/personalize-ui-dynamics-365-business-central/index)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
[Opprette nye selskaper](about-new-company.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
