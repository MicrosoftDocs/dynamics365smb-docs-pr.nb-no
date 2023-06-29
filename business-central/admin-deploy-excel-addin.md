---
title: Hent Business Central-tillegget for Excel
description: Finn ut hvordan du henter Business Central-tillegget for Excel til brukere.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.search.form: 1480
ms.search.keywords: 'Excel, add-in, centralized deployment, M365 admin center, individual acquisition, appsource'
ms.date: 10/07/2021
ms.author: jswymer
---
# <a name="get-the-business-central-add-in-for-excel"></a><a name="get-the-business-central-add-in-for-excel"></a>Hent Business Central-tillegget for Excel

[!INCLUDE[prod_short](includes/prod_short.md)] inneholder et tillegg for Excel som lar brukere velge en **Rediger i Excel**-handling på bestemte sider for å åpne dataene i et Excel-regneark. Denne handlingen er forskjellig fra handlingen **Åpne i Excel** fordi den gjør det mulig for brukere å foreta endringer i Excel, og deretter publiserer endringene tilbake til [!INCLUDE[prod_short](includes/prod_short.md)]

## <a name="overview"></a><a name="overview"></a>Oversikt

### <a name="about-the-add-in"></a><a name="about-the-add-in"></a>Om tillegget

Tillegget kalles **Microsoft Dynamics Office-tillegg** og er tilgjengelig for installasjon fra [Office Store (AppSource)](https://appsource.microsoft.com/). Når tillegget er installert, er handlingen **Rediger i Excel** tilgjengelig på de fleste listedelsidene fra **Del**-ikonet ![Del en side i en annen app.](media/share-icon.png). Hvis du vil ha mer informasjon om å bruke tillegget, kan du se [Vis og rediger i Excel fra Business Central](across-work-with-excel.md).

> [!NOTE]
> Tillegget fungerer bare i Windows, ikke i macOS.

### <a name="about-deployment-as-an-admin"></a><a name="about-deployment-as-an-admin"></a>Om distribusjon som administrator

Med [!INCLUDE[prod_short](includes/prod_short.md)] online finnes det noen distribusjonsalternativer for å distribuere tillegget til brukerne. Ett alternativ er *individuell anskaffelse*, der du lar brukerne installere tillegget selv. Med dette alternativet må brukere ha tilgang til å laste ned filer fra Office Store. Et annet alternativ er å konfigurere *sentralisert distribusjon* i administrasjonssenteret for Microsoft 365 for automatisk å distribuere tillegget til hele organisasjonen, grupper eller bestemte brukere. Sentralisert distribusjon gjør det mulig å distribuere tillegget til brukerne hvis organisasjonen ikke gir brukere tilgang til Office Store.

For sluttbrukeren er installasjonsopplevelsen forskjellig for de to distribusjonsscenarioene:

- Første gang brukerne velger **Rediger i Excel**-handlingen, vil ruten **Nytt Office-tillegg** åpnes i Excel. Hvis du vil installere tillegget, velger brukeren **Klarer dette tillegget**, noe som installerer tillegget direkte fra Office Store. Brukere kan deretter logge på [!INCLUDE[prod_short](includes/prod_short.md)] ved å bruke brukernavn og passord.

- Ved sentralisert distribusjon velger førstegangsbrukere handlingen **Rediger i Excel**, og tillegget installeres automatisk i Excel fra sentralisert distribusjon, ikke Office Store. Det eneste brukerne må gjøre, er å logge seg på [!INCLUDE[prod_short](includes/prod_short.md)]

Med begge disse distribusjonsalternativene konfigureres tillegget automatisk for å koble til [!INCLUDE[prod_short](includes/prod_short.md)]. Et tredje distribusjonsalternativ, som er manuell installasjon av tillegget direkte fra Excel. Med dette alternativet må brukerne konfigurere tillegget for å koble til [!INCLUDE[prod_short](includes/prod_short.md)]

### <a name="switching-from-individual-acquisition-to-centralized-deployment-or-the-other-way-around"></a><a name="switching-from-individual-acquisition-to-centralized-deployment-or-the-other-way-around"></a><a name="switch"></a>Bytt fra individuell anskaffelse til sentralisert distribusjon, eller omvendt

Når du bytter fra individuell anskaffelse av tillegget til sentralisert distribusjon, eller omvendt, blir Excel-filer som brukere opprettet før overgangen, påvirket. Etter overgangen kan brukerne fremdeles åpne Excel-regneark som tidligere ble opprettet med handlingen **Rediger i Excel**, eller opprettet manuelt ved å konfigurere Excel-tillegget. Men de kan ikke oppdatere dataene i filen fra Business Central- eller push-oppdateringer til Business Central

Denne tilstanden skyldes at alle Excel-filer er tilordnet et ID for tillegg. I overgangen til eller fra sentralisert distribusjon, tilordnes en annen ID, slik at den tidligere ID-en blir blokkert.

## <a name="preparation-on-premises-only"></a><a name="preparation-on-premises-only"></a>Klargjøring (bare lokalt)

[!INCLUDE[prod_short](includes/prod_short.md)] on-premises krever at miljøet er konfigurert for tillegget. Hvis ikke vil ikke handlingen **Rediger i Excel** være tilgjengelig for brukerne. Hvis du vil ha mer informasjon, kan du se [Konfigurer Excel-tillegget for redigering av Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin) i hjelpen for utviklere og IT-eksperter.

## <a name="deploy-the-add-in-by-using-centralized-deployment"></a><a name="deploy-the-add-in-by-using-centralized-deployment"></a>Distribuer tillegget ved hjelp av sentralisert distribusjon

Sentralisert distribusjon er en funksjon i administrasjonssenteret for Microsoft 365 som du bruker til automatisk å installere tillegg i brukernes Office-apper, for eksempel Excel. For å hjelpe deg med sentralisert distribusjon må [!INCLUDE[prod_short](includes/prod_short.md)] inkludere det assisterte oppsettet **Excel-tillegget Sentralisert distribusjon**.

### <a name="before-you-begin"></a><a name="before-you-begin"></a>Før du starter

- Hvis du vil vite mer om hvordan du hindrer at brukere laster ned fra Office Store, kan du se [Behandle tillegg i administrasjonssenteret](/microsoft-365/admin/manage/manage-addins-in-the-admin-center).
- Kontrollere at sentralisert distribusjon vil fungere for organisasjonen. Hvis du vil ha mer informasjon, kan du se [Fastslå om sentralisert distribusjon av tillegg fungerer for organisasjonen](/microsoft-365/admin/manage/centralized-deployment-of-add-ins)
- Hvis du går over fra individuell anskaffelse, kan du se [Bytt fra individuell anskaffelse til sentralisert distribusjon](#switch)

> [!NOTE]
> Aktivering av sentralisert distribusjon påvirker funksjoner som bruker Excel-tillegget, for eksempel handlingen **Rediger i Excel**. Den påvirker ikke andre Excel-relaterte funksjoner og eller tillatelser tilordnet brukere i [!INCLUDE[prod_short](includes/prod_short.md)]

### <a name="set-up-centralized-deployment-of-the-add-in"></a><a name="set-up-centralized-deployment-of-the-add-in"></a>Konfigurer sentral. distribusjon for tillegget

Du arbeider i både [!INCLUDE[prod_short](includes/prod_short.md)] og administrasjonssenteret for Microsoft 365.

1. I [!INCLUDE[prod_short](includes/prod_short.md)] velger du ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Excel-tillegget Sentralisert distribusjon**. Deretter velger du relatert kobling.
2. Les informasjonen på siden **Oppsett av Excel-tillegg for Business Central**, og velg **Neste**.
3. Logg deg på [administrasjonssenteret for Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2163967), og gå til **Integrerte apper**<!--**Add-ins**-->.

    Fullfør følgende fremgangsmåte for å konfigurere tillegget for å distribuere fra Office Store: 
    1. Velg **Hent apper** for å åpne Office Store (AppSource). <!--**Deploy Add-in** 5. In the **Deploy a new add-in**, select **Choose from the store**.-->
    2. Søk etter **Microsoft Dynamics Office-tillegg**, og velg deretter **Få det nå**. <!--On the **Select add-in** page, search for and select **Microsoft Dynamics Office Add-in** > **Add** > **Continue**.-->
    3. På siden **Legg til brukere** angir du brukerne du vil distribuere tillegget for, og deretter velger du **Neste**.<!--On the **Configure add-in**, specify the users that you want to deploy the add-in for.-->
    4. Gå gjennom **Godta tillatelsesforespørsler** og velg **Neste** > **Fullfør distribusjon**.
    5. Vent til det grønne avmerkingsmerket ved siden av **Distribuert** vises for tillegget, og velg deretter **Ferdig**. <!--Select **Deploy** and wait til successful, then **Next** > **Continue**.-->

       Tillegget vises på siden **Tillegg**. Hvis du vil ha mer informasjon om hvordan du distribuerer tillegg i administrasjonssenteret for Microsoft 365, kan du se [Distribuer tillegg i administrasjonssenteret](/power-platform/admin/use-service-admin-role-manage-tenant?azure-portal=true).
4. Gå tilbake til det assisterte oppsettet **Excel-tillegget Sentralisert distribusjon** i [!INCLUDE[prod_short](includes/prod_short.md)] og velg **Neste**.
5. Aktiver **Bruk av sentralisert distribusjon** og velg **Fullfør**.

    Hvis du ikke slår på denne bryteren, henter [!INCLUDE[prod_short](includes/prod_short.md)] tillegget direkte fra Office Store.

Når du er ferdig, kan du alltids endre distribusjonen i Microsoft 365-administrasjonssenteret, for eksempel tilordne flere brukere. Hvis du vil ha mer informasjon om hvordan du distribuerer tillegg i administrasjonssenteret, kan du se [Distribuer tillegg i administrasjonssenteret](/power-platform/admin/use-service-admin-role-manage-tenant?azure-portal=true).

> [!IMPORTANT]
> Hvis du har mer enn ett miljø, må du kjøre det assisterte oppsettet **Excel-tillegget Sentralisert distribusjon** for hvert miljø der du vil bruke sentralisert distribusjon. Du trenger imidlertid ikke konfigurere den sentraliserte distribusjonen i Microsoft 365 på nytt. Det eneste du må gjøre, er å slå på bryteren **Bruk sentralisert distribusjon** i det assisterte oppsettet. 

> [!NOTE]
> Det kan ta opptil 24 timer før tillegget blir distribuert automatisk i Excel til brukere.

## <a name="individual-acquisition-install-the-add-in-manually-for-your-own-use"></a><a name="individual-acquisition-install-the-add-in-manually-for-your-own-use"></a><a name="install"></a>Individuell anskaffelse: Installer tillegget manuelt for egen bruk

Når du åpner Excel fra Business Central, vil tillegget i de fleste tilfeller enten bli installert automatisk, eller du blir bedt om å installere det. Det kan imidlertid finnes tilfeller der du må installere tillegget manuelt.

1. Åpne Excel og åpne deretter en Excel-arbeidsbok.
2. Velg **Tillegg** > **Hent tillegg** på menyen **Sett inn**
3. Gå til **Administrert av administrator** og se etter **Microsoft Dynamics Office-tillegg**. Hvis du ser det der, merker du det og velger **Legg til**. Hvis du ikke ser det, går du til **Store**, søker etter *Microsoft Dynamics Office-tillegg* og følger instruksjonene på skjermen for å legge det til.

Når tillegget er installert, vises det som et panel i Excel. Nå konfigurerer du tilkoblingen.

### <a name="configure-the-business-central-connection"></a><a name="configure-the-business-central-connection"></a>Konfigurer Business Central-tilkoblingen

Hvis en bruker ikke kan koble til automatisk, kan du fjerne blokkeringen ved å be dem følge denne fremgangsmåten:

1. I **Microsoft Dynamics**-tilleggsruten i Excel velger du **Legg til serverinformasjon**. Hvis du ikke ser den, velger du ikonet ![Flere alternativer-knappen i Excel.](media/cogwheel.png) øverst for å åpne dialogboksen for alternativer. 
2. For [!INCLUDE[prod_short](includes/prod_short.md)] online angir du **URL-adresse for server** til `https://exceladdinprovider.smb.dynamics.com`. For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises angir du URL-adressen til nettklienten, for eksempel `https://myBCserver/190`.
3. Velg **OK** og bekreft deretter at appen lastes på nytt.
4. Logg på Business Central med brukernavn og passord når du blir bedt om det.
5. Du kan også velge miljøet og selskapet som du vil koble til.

Tillegget er nå tilkoblet [!INCLUDE [prod_short](includes/prod_short.md)], og du kan redigere data og publisere endringene i [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="prepare-devices-and-network-for-the-excel-add-in"></a><a name="prepare-devices-and-network-for-the-excel-add-in"></a>Klargjør enheter og nettverk for Excel-tillegget

Nettverkstjenester som proxyer eller brannmurer må tillate ruting mellom hver klientenhet der tillegget er installert og mange serviceendepunkter. Se [Klargjør nettverket for Excel-tillegget](/dynamics365/business-central/dev-itpro/administration/configuring-network-for-addins) for en liste over endepunkter.

## <a name="troubleshooting"></a><a name="troubleshooting"></a>Feilsøking

Noen ganger støter brukere på problemer med Excel-tillegget. Denne delen inneholder noen tips for hvordan du kan oppheve blokkeringen av brukere i visse tilfeller.

|Problem  |Løsning eller midlertidig løsning  |Kommentarer  |
|---------|---------|---------|
|Tillegget starter ikke <br><br>Brukeren får for eksempel meldingen Advarsel om tillegg: Dette tillegget er ikke lenger tilgjengelig. når vedkommende prøver å bruke tillegget. Dette problemet kan oppstå hvis sentralisert distribusjon er riktig konfigurert, men brukeren har ikke fått tildelt tilgang.|Kontroller om tillegget er distribuert sentralt. Du kan eventuelt kontrollere om brukeren er blokkert fra å installere det lokalt. | Administratoren kan konfigurere Office slik at brukere ikke kan hente tillegg. I slike tilfeller må administratoren distribuere tillegget sentralt. Hvis du vil ha mer informasjon, kan du se [Distribuer tillegg i administrasjonssenteret](/microsoft-365/admin/manage/manage-deployment-of-add-ins?view=o365-worldwide&preserve-view=true).|
|Data blir ikke lastet inn i Excel|Test tilkoblingen ved å åpne en annen liste i Excel fra [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan eventuelt åpne arbeidsboken i Excel i en nettleser.|Hvis brukeren har angitt et selskapsnavn som inneholder spesialtegn, kan ikke tillegget kobles til. |
|Data kan ikke publiseres tilbake til [!INCLUDE [prod_short](includes/prod_short.md)].|Test tilkoblingen ved å åpne arbeidsboken i Excel i en nettleser. |Noen ganger kan en utvidelse blokkere publiseringsjobben. Hvis siden er utvidet eller tilpasset, fjerner du utvidelsene og prøver på nytt.|
|Datoene er feil  |Excel kan vise klokkeslett og datoer i et annet format enn [!INCLUDE [prod_short](includes/prod_short.md)]. Denne betingelsen gjør dem ikke feil, og dataene i [!INCLUDE [prod_short](includes/prod_short.md)] blir ikke forstyrret.|         |
|For enkelte listesider vil redigering av flere linjer i Excel konsekvent forårsake feil. Denne betingelsen kan oppstå hvis OData-oppkall inkluderer FlowFields og felter utenfor repeater-kontrollen.|På siden **Nettjenester** merker du av for **Utelat ikke-redigerbare FlowFields** og **Utelat felter utenfor repeater** for den publiserte siden. Hvis du merker av i disse avmerkingsboksene, utelates ikke-redigerbare FlowFields og felt fra beregningen av eTag. |Disse avmerkingsboksene er skjult som standard. Hvis du vil se dem på siden **Nettjenester**, bruker du [tilpasning](/dynamics365/business-central/ui-personalization-user). |
|Brukere kan ikke lenger logge seg på tillegget. Når de prøver å logge seg på, stopper prosessen uten å fullføres.| Dette problemet kan skyldes en oppdatering som vi gjorde med tillegget, en gang i juli 2022. Hvis du vil ha mer informasjon og en feilretting, kan du se [Endre konfigurasjonen for Excel-tillegget for å støtte oppdateringen fra juli 2022](/dynamics365/business-central/dev-itpro/administration/update-excel-addin-configuration).|Gjelder bare lokal versjon av [!INCLUDE [prod_short](includes/prod_short.md)]|

<!--
## <a name="deploy-the-excel-add-in-for-business-central-online"></a><a name="deploy-the-excel-add-in-for-business-central-online"></a>Deploy the Excel add-in for Business Central online

For [!INCLUDE [prod_short](includes/prod_short.md)] online, the administrator can deploy the add-in for all users. But users can also install the add-in themselves, provided they have permission to configure their Office experience.  

> [!TIP]
> In some organizations, administrators cannot deploy add-ins centrally. For more information, see [Determine if Centralized Deployment of add-ins works for your organization](/microsoft-365/admin/manage/centralized-deployment-of-add-ins?view=o365-worldwide&preserve-view=true).

### <a name="to-deploy-the-excel-add-in-for-all-users"></a><a name="to-deploy-the-excel-add-in-for-all-users"></a>To deploy the Excel add-in for all users

1. As the administrator, sign in to the Microsoft commercial website and find the add-in at [https://appsource.microsoft.com/product/office/WA104379629](https://appsource.microsoft.com/product/office/WA104379629).
2. Choose the **Get it now** button.

    You'll be redirected to the Microsoft 365 admin center.
3. In the left panel, go to **Settings**, and then choose **Add-ins**.
4. In the **Configure add-in** pane, specify which users to grant access to the add-in.
5. Save your changes.


### <a name="to-add-the-excel-add-in-locally"></a><a name="to-add-the-excel-add-in-locally"></a>To add the Excel add-in locally

1. Open Excel, and then open any Excel workbook.
2. On the **Insert** menu, choose **Office Add-ins**, and then choose **Admin managed** or **Store** as appropriate.
3. Search for *Dynamics Office Add-In*, and then install the add-in.

When the add-in is installed, it shows up as a panel in Excel. Next, you must configure the connection.

> [!TIP]
> If the workbook is not automatically saved to the user's OneDrive, then recommend them to save all workbooks that they export from [!INCLUDE [prod_short](includes/prod_short.md)].When they open the workbook again, the connection is still available, so they do not have to configure the connection again.

> [!NOTE]
> In certain deployments, the administrator must configure network access to unblock the Excel add-in. For more information, see [Preparing Your Network for the Excel Add-In](configuring-network-for-addins.md).-->

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a><a name="see-also"></a>Se også

[Analyser årsregnskap i Microsoft Excel](finance-analyze-excel.md)  
[Arbeid med Business Central](ui-work-product.md)  
[Forbedringer i Excel-integrasjon i 2019 Release Wave 2](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
