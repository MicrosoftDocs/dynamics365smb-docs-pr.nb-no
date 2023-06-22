---
title: Bruk Power Automate-flyter i Business Central
description: Definer og bruk Power Automate-flyter for å opprette eller endre Business Central-data.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: 'workflow, OData, Power App, SOAP, Power Automate,'
ms.search.form: '1500,'
ms.date: 10/10/2022
ms.custom: bap-template
---
# <a name="use-power-automate-flows-in-includeprodshortincludesprodshortmd" />Bruk Power Automate-flyter i [!INCLUDE[prod_short](includes/prod_short.md)]

Med [!INCLUDE[prod_short](includes/prod_short.md)] får du en lisens til Microsoft Power Automate. Med denne lisensen kan du bruke [!INCLUDE[prod_short](includes/prod_short.md)]-dataene som en del av en arbeidsflyt i Microsoft Power Automate. Du kan opprette flytprosesser og koble dataene fra interne og eksterne kilder gjennom [!INCLUDE [prod_short](includes/prod_short.md)]-koblingen.

Power Automate-flytprosesser utløses av hendelser, for eksempel at en post ble opprettet, endret eller slettet. De kan også kjøres i en brukerdefinert plan eller på forespørsel.

> [!NOTE]
> Administratorer kan begrense tilgangen til Power Automate. Hvis du finner ut at du ikke har tilgang til noen av eller alle funksjonene som er beskrevet i denne artikkelen, kontakter du administratoren. Hvis du vil lære hvordan du kan kontrollere Power Automate-tilgangen som administrator, kan du se [Konfigurer Power Automate-integrering](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup).

<!-- You must have a valid account with both [!INCLUDE[prod_short](includes/prod_short.md)] and Power Automate. --> 

> [!TIP]
> I tillegg til Power Automate kan du bruke godkjenningsarbeidsflytmaler i [!INCLUDE[prod_short](includes/prod_short.md)]. Selv om de er to separate arbeidsflytsystemer, legges en godkjenningsarbeidsflytmal som du oppretter med Power Automate, til i listen over arbeidsflyter i [!INCLUDE[prod_short](includes/prod_short.md)]. Finn ut mer under [Arbeidsflyter](across-workflow.md).

## <a name="about-power-automate-flows" />Om Power Automate-flytprosesser

Power Automate er en tjeneste som hjelper deg med å opprette automatiserte arbeidsflytprosess (eller flytprosesser) mellom apper og tjenester, som [!INCLUDE[prod_short](includes/prod_short.md)]. Power Automate-flytprosesser krever lite eller ingen kodekunnskap. De kan knyttes til et bredt spekter av hendelser og svar, for eksempel:

- oppføringsendringer
- oppdateringer av eksterne filer
- bokførte dokumenter
- Forskjellige Microsoft- og tredjepartstjenester, som Microsoft Outlook, Excel, Dataverse, Teams, SharePoint, Power Apps med mer.

Det finnes tre forskjellige skyflyttyper du kan arbeide med:

|Flyttype|Description|
|---------|-----------|
|Automatisert|Denne flyttypen kjøres automatisk av en hendelse. I [!INCLUDE[prod_short](includes/prod_short.md)] kan en hendelse være når en oppføring eller et dokument opprettes, endres eller slettes. Det kan for eksempel hende at en ny salgsfaktura utløser en flyt for en godkjenningsforespørsel, som kan ha ulike hendelser angitt, avhengig av svaret fra godkjenneren. Et negativt svar sender en varsling og e-post til godkjenningsbestilleren. Et positivt svar oppdaterer samtidig et Excel-regneark som er plassert i en SharePoint-mappe, og sender en oppdatering til en Teams-nettprat. Automatiske flytprosesser kan startes av både interne og eksterne hendelser i [!INCLUDE[prod_short](includes/prod_short.md)].|
|Tidsplanlagt|Denne typen flyt blir også kjørt automatisk, men den kjøres med jevne mellomrom på en planlagt dato og et planlagt tidspunkt. |
|Direkte |Denne flyttypen kjøres etter behov, som krever at brukeren kjører den manuelt fra en knapp eller handling i en annen app eller enhet, i dette tilfellet [!INCLUDE[prod_short](includes/prod_short.md)]-klienten. Direkteflyter fungerer på samme måte som satsvise snarveier, noe som utfører flere lange trinn med noen knappetrykk og startes fra bestemte sider eller tabeller. En flyt kan for eksempel legge til en knapp på handlingsmenyen på **Leverandører**- siden for å sperre betalinger til en leverandør og samtidig sende e-postmeldinger til leverandørens kontakt og innkjøpere, i tillegg til å oppdatere kontakten i Outlook. |

## <a name="power-automate-features" />Power Automate-funksjoner

Du kan utforske alle Power Automate-flytprosesser som er tilgjengelige for deg, ved å logge deg på [Power Automate](https://powerautomate.com) og velge **Mine flytprosesser** fra navigasjonsfeltet til venstre. Her finner du alle flytprosesser du allerede har opprettet selv, og flytprosesser som deles med deg av en administrator eller en kollega.

- Direkteflyter gjøres også tilgjengelig for kjøring direkte fra de fleste liste-, kort- og dokumentsidene i [!INCLUDE[prod_short](includes/prod_short.md)]. Du finner direkteflytene i handlingsgruppen **Automatiser** i handlingslinjen på sider. Du kan kjøre en flyt ved å merke den og følge instruksjonene som vises. Finn ut mer i delene som følger.
 
- Med automatiserte flytprosesser i [!INCLUDE[prod_short](includes/prod_short.md)] tregner du ikke å gjøre noe med mindre du vil endre dem eller slå dem av. Hvis ikke fungerer de når de utløses. 
<!--

## <a name="automated-flows" />Automated flows

With Power Automate, you can create business flows directly in-house and rely on citizen developers. Automated workflows can be started by both internal and external events in [!INCLUDE[prod_short](includes/prod_short.md)], and also be set to run periodically. Learn more and get instructions on how to create flows in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

-->

## <a name="run-instant-flows" />Kjør direkteflytprosesser

Direkteflytprosesser åpnes i [!INCLUDE [prod_short](includes/prod_short.md)] på nettet slik at du kan forbli innenfor konteksten til forretningsprosessen du holdt på med. Du kan kjøre en direkteflyt fra de fleste lister, kort eller dokumenter.

1. Velg **Automatiser** på handlingsraden, og velg deretter en flyt fra listen over tilgjengelige flytprosesser under **Power Automate**-handlingen

    :::image type="content" source="media/power-automate-action-intro.png" alt-text="Viser handlingen Automatiser på handlingsraden med utvidede handlinger.":::

    På noen sider er **Automatiser** nestet under **Flere alternativer (...)**. 
2. Fyll ut de nødvendige feltene i ruten **Kjør flyt**, og velg deretter **Fortsett** for å kjøre flyten.

> [!NOTE]
> Første gang du bruker elementet **Automatiser**, kan det hende du bare ser handlingen **Kom i gang med Power Automate**. Du ser denne handlingen fordi du ikke har godtatt personvernerklæringen for Microsoft Power Automate. Du fortsetter ved å velge **Kom i gang med Power Automate** og følge instruksjonene for å godta eller ikke godta.  
>
> :::image type="content" source="media/power-automate-action.png" alt-text="Viser elementet Automatiser på handlingsraden.":::

<!--

[!INCLUDE [prod_short](includes/prod_short.md)] can run a Power Automate flow from most list, card, and document pages. Once the admin has connected [!INCLUDE [prod_short](includes/prod_short.md)] with Power Automate, you'll see any flows your organization has added when you choose the **Automate** action on the relevant pages. Instant flows are run without leaving [!INCLUDE [prod_short](includes/prod_short.md)]. Learn more in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

These instant flows open on a page inside [!INCLUDE [prod_short](includes/prod_short.md)] online so you can remain within the context of the business process you were in the middle of. Choose the **Automate** action—on some pages nested under the **More Options** menu—choose the **Power Automate** menu item, then choose the relevant link to trigger the workflow. The connection to Power Automate is already set up for you.

Most flows require you to fill in a field or two before you choose the **Run flow** action.

> [!TIP]
> If you don't see an **Automate** action, then your [!INCLUDE [prod_short](includes/prod_short.md)] probably hasn't yet been set up to use Power Automate. Learn more from your admin.-->

## <a name="create-edit-and-manage-flows" />Opprett, rediger og administrer flytprosesser

Oppretting av nye flytprosesser, endring og administrering av eksisterende (som å slå dem av eller på) kan utføres direkte i Power Automate. Du kan imidlertid starte noen av disse oppgavene fra [!INCLUDE[prod_short](includes/prod_short.md)]:

- Hvis du vil opprette en direkteflyt fra en liste-, kort- eller dokumentside, velger du **Automatiser** > **Opprett en flyt**.
- Du åpner Power Automate fra en liste-, kort- eller dokumentside ved å velge **Automatiser** > **Administrer flytprosesser**.
<!--- To create new flows or manage existing flows from inside [!INCLUDE[prod_short](includes/prod_short.md)], got to the **Manage Power Automate Flows** page.-->

Disse oppgavene gjøres vanligvis av en administrator eller superbruker. Oppgavene krever omfattende kunnskap om forretningsprosessene i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil lære mer, kan du utforske [Power Automate-integrering](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-overview), [Definer direkteflyter](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows) og [Administrer Power Automate-flyter](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows).
<!-- 

## <a name="add-more-automated-flows-and-instant-flows" />Add more automated flows and instant flows

You can create flows through the [powerautomate.microsoft.com](https://powerautomate.microsoft.com) website. However, if your admin has switched on the capability to run Power Automate flows from inside [!INCLUDE [prod_short](includes/prod_short.md)] online, you can start the process of building a flow from the **Automate** action on the relevant pages, which can be found under the **More Options** menu depending on the page. Then choose the **Power Automate** menu item, and then choose the **Create a flow** action. Power Automate then opens in a new browser tab, and you're signed in automatically.

You can find sample templates to adapt to your company and all available trigger events, using both [!INCLUDE [prod_short](includes/prod_short.md)] and external tools, by choosing the **Connectors** menu on the Power Automate website. Learn more about available templates and triggers in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

## <a name="create-and-manage-power-automate-flows" />Create and manage Power Automate flows

You can create new flows or manage existing Power Automate flows in [!INCLUDE [prod_short](includes/prod_short.md)] on the **Manage Power Automate Flows** page. Learn more in the [Manage Power Automate Flows](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows) article in the administration content.

<!--
You can also manage available Power Automate workflows on the **Workflows** page in [!INCLUDE[prod_short](includes/prod_short.md)]. The page lists both the built-in approval and Power Automate workflows, with options for the latter to enable/disable, delete, and view the workflow on the Power Automate website.-->

## <a name="see-related-microsoft-trainingtrainingmodulesuse-power-automate" />Se relatert [Microsoft-opplæring](/training/modules/use-power-automate/)

## <a name="see-also" />Se også

[Feilsøk automatiserte arbeidsflyter for [!INCLUDE[prod_short](includes/prod_short.md)]](across-flow-troubleshoot.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Arbeidsflyter](across-workflow.md)  
[Importer forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Tildel tillatelser til brukere og grupper](ui-define-granular-permissions.md)  
[Konfigurer [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finans](finance.md)  
[Administrer Power Automate-flyter](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  
[Konfigurer automatiserte arbeidsflyter](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Slå på direkteflyter](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
a
