---
title: Hent Business Central-tillegget for Outlook
description: Finn ut hvordan du installerer Business Central-tillegget for Outlook for organisasjonen eller for eget bruk.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365, Outlook
ms.search.form: 1831, 1832
ms.date: 08/13/2021
ms.author: jswymer
ms.openlocfilehash: 7fa8eabcffeb19b77c98ed9f9b7036dff6cbbf35
ms.sourcegitcommit: 1508643075dafc25e9c52810a584b8df1d14b1dc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/28/2022
ms.locfileid: "8049598"
---
# <a name="get-the-business-central-add-in-for-outlook"></a>Hent Business Central-tillegget for Outlook

Med [!INCLUDE[prod_short](includes/prod_short.md)] kan du behandle forretningssamhandlinger med kunder og leverandører direkte i Microsoft Outlook. Med [!INCLUDE[prod_short](includes/prod_short.md)] Outlook-tillegget kan du se økonomiske data knyttet til kunder og leverandører. Du kan også opprette og sende økonomiske dokumenter, for eksempel tilbud og fakturaer.  

Du kan få tak i Business Central-tillegget for Outlook installert på to måter, avhengig av hvilken rolle du har i organisasjonen:

- Som en Microsoft 365-administrator bruker du *Sentralisert distribusjon* til å installere tillegget automatisk for hele organisasjonen, grupper eller bestemte brukere.

- Som en hvilken som helst bruker installerer du tillegget for eget bruk, hvis administratoren ikke allerede har distribuert det.

## <a name="about-the-business-central-add-in-for-outlook"></a>Om Business Central-tillegget for Outlook

Business Central-tillegget for Outlook består av to mindre tillegg:

- Innsikt for kontakter

    Dette tillegget gir brukere [!INCLUDE[prod_short](includes/prod_short.md)]-kunde- eller -leverandørinformasjon i e-poster og kalenderavtaler i Outlook. Du kan også opprette og sende [!INCLUDE[prod_short](includes/prod_short.md)]-forretningsdokumenter, for eksempel tilbud og fakturaer, til en kontakt. <!--To support these task, the add-in adds actions to the Outlook ribbon, in the **Business Central** group. --> 

- Dokumentvisning

    Når en e-post henviser til et forretningsdokumentnummer i brødteksten i e-posten, gir dette tillegget en direkte, innebygd kobling fra brødteksten i e-posten til det aktuelle forretningsdokumentet i [!INCLUDE[prod_short](includes/prod_short.md)].

Hvis du vil ha mer informasjon om hva du gjør med tilleggene, kan du se [Bruk av Business Central som innboks for bedriften i Outlook](work-outlook-addin.md).

Hvert tillegg leveres som en XML-fil, kalt et *manifest*, som må installeres i Outlook av alle som ønsker denne funksjonaliteten. Disse filene beskriver hvordan du aktiverer tilleggene og kobler til Business Central når de brukes i Outlook. Arbeid med disse filene utføres vanligvis en administrator. Som vanlig bruker trenger du i de fleste tilfeller ikke å håndtere disse filene direkte. Administratoren konfigurerer tillegget slik at det installeres automatisk, eller du bruker det innebygde assisterte oppsettet til å håndtere installasjonen.

## <a name="deploy-the-add-in-by-using-centralized-deployment-as-an-admin"></a>Distribuer tillegget ved hjelp av sentralisert distribusjon som en administrator

Sentralisert distribusjon er en funksjon i administrasjonssenteret for Microsoft 365 som du bruker til automatisk å installere tillegg i brukernes Office-apper, for eksempel Outlook. Det er den anbefalte måten administratorer kan distribuere for Office-tillegg til brukere og grupper i organisasjonen.

> [!NOTE]
> For Business Central on-premises kan du se [Konfigurer tillegget for Outlook-integrering med Business Central On-Premises](/dynamics365/business-central/dev-itpro/administration/setting-up-office-add-ins-outlook-inbox) i administrasjonsinnholdet (bare engelsk).

### <a name="prerequisites"></a>Forutsetninger

- Et Microsoft 365-abonnement  
- Brukere er tilordnet en Microsoft 365-lisens  
- Microsoft 365-kontoen har rollen *Global administrator* eller *Exchange-administrator*

### <a name="deploy-the-add-in"></a>Distribuer tillegget

1. I Business Central velger du ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Assistert oppsett** og velger den relaterte koblingen.
2. Velg **Outlook-tillegget Sentralisert distribusjon** for å starte veiledningen for assistert oppsett.
3. Gå gjennom første side og velg **Neste** for å åpne siden for å laste ned tilleggene.
4. I **Distribuer**-kolonnen merker du av for tilleggene du vil distribuere, og deretter klikker du på **Last ned og fortsett**.

    En fil med navnet *OutlookAddins.zip* lastes ned på enheten.

5. På dette tidspunktet er du ferdig med arbeidet du må gjøre i Business Central, slik at du kan velge **Ferdig**.

   >[!TIP]
   > Før du velger **Neste**, velger du **Gå til Microsoft 365 (åpnes i et nytt vindu)**-kobling for å åpne og logge på administrasjonssenteret for Microsoft 365 i et nytt nettleservindu. Du må likevel gå til administrasjonssenteret for Microsoft 365 i et senere trinn.

6. Gå til mappen der OutlookAddins.zip ble lastet ned, og pakk ut filene **Kontaktinnsikt.xml** og **Dokumentvisning.xml** fra .zip-filen til en mappe du velger.

    Hvis du vil ha mer informasjon, kan du se [Pakk og pakk ut filer og mapper](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-8d28fa72-f2f9-712f-67df-f80cf89fd4e5).
7. Logg på administrasjonssenteret for Microsoft 365, og gå til [Integrerte apper](https://go.microsoft.com/fwlink/?linkid=2163967).

8. Velg **Last opp egendefinerte apper**.
9. På siden **Last opp apper som skal distribueres** velger du **Last opp manifestfil (XML) fra enhet** > **Velg fil**.
10. Velg ett av tilleggsfilene du pakket ut tidligere, for eksempel **Kontaktinnsikt.xml**.
11. Følg instruksjonene for å tilordne brukere og distribuere tillegget.
12. Gjenta trinn 9 til 11 for den andre tilleggsfilen hvis du vil.

> [!IMPORTANT]
> Det vises en grønn hake når tillegget er distribuert til administrasjonssenteret. Det kan imidlertid ta opptil 24 timer før brukere ser tillegget i Outlook-appen. Det kan også hende at brukerne må starte Outlook på nytt.

Når du er ferdig, kan du alltids endre distribusjonen i Microsoft 365-administrasjonssenteret, for eksempel tilordne flere brukere. Hvis du vil ha mer informasjon om hvordan du distribuerer tillegg i administrasjonssenteret, kan du se [Distribuer tillegg i administrasjonssenteret](/microsoft-365/admin/manage/manage-deployment-of-add-in).

## <a name="install-the-add-in-for-your-own-use"></a><a name="install"></a>Installer tillegget for eget bruk

Hvis organisasjonen tillater det, kan du installere Business Central-tillegget bare for deg selv. Kontakt administratoren hvis du ikke er sikker.

1. I Business Central går du til ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Hent Outlook-tillegget**. Deretter velger du relatert kobling.
2. Les siden og velg **Neste** når du er klar.
3. Hvis du vil motta en velkomst-e-postmelding fra Business Central med oversikt over bruken av tillegget, aktiverer du **Send eksempel-e-postmelding**.
4. Velg **Fullfør** for å fullføre installasjonen.

Business Central kobles til e-postserveren og installerer tillegget i Outlook. Dette tar ikke lang tid. Du er nå klar til å begynne å bruke tillegget i Outlook.

### <a name="for-business-central-on-premises"></a><a name="onprem"></a>For Business Central lokalt

Hvis du bruker Business Central on-premises, kan det være litt annerledes å installere tillegget.

1. I Business Central går du til ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Hent Outlook-tillegget**. Deretter velger du relatert kobling.
2. Les siden og velg **Neste** når du er klar.
3. Gjør et av følgende, avhengig av hvilken side du ser:

    - Hvis du ser knappen **Installer i min Outlook**, velger du den, og du er ferdig.
    - Hvis du ser **Neste**-knapp, velger du den. På neste side, hvis du vil motta en velkomst-e-postmelding fra Business Central med oversikt over bruken av tillegget, aktiverer du **Send eksempel-e-postmelding**. Deretter klikker du på **Fullfør** og du er ferdig.
    - Hvis du ser **Last ned tillegg**-knappen, velger du det, og deretter går du til neste trinn.
4. Når du velger **Last ned tillegg**, lastes det ned en fil med navnet *OutlookAddins.zip* på enheten. Filen vises øverst i nettleseren.

   Gå til mappen der OutlookAddins.zip ble lastet ned, og pakk ut filene **Kontaktinnsikt.xml** og **Dokumentvisning.xml** fra .zip-filen til en mappe du velger. Hvis du vil ha mer informasjon om hvordan du pakker ut filer, kan du se [Pakk og pakk ut filer og mapper](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-8d28fa72-f2f9-712f-67df-f80cf89fd4e5).

5. Åpne Outlook og velg **Hent tillegg** fra båndet. Hvis du bruker Outlook på nettet, velger du rullegardinmenyen for en ny eller eksisterende e-postmelding, og deretter velger du **Hent tillegg**.
6. Velg **Mine tillegg** > **Legg til et egendefinert tillegg** > **Legg til fra en fil**.
7. Velg en av .xml-filene du pakket ut, for eksempel **Kontaktinnsikt.xml**, og velg deretter **Åpne** > **Installer**.
8. Gjenta trinn 6 og 7 for den andre .xml-filen hvis du lastet den ned.

Du er nå klar til å begynne å bruke tillegget i Outlook.

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/alternative-interfaces-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Få Business Central på mobilenheten](install-mobile-app.md)  
[Send dokumenter i e-post](ui-how-send-documents-email.md)  
[Finans](finance.md)  
[Salg](sales-manage-sales.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Minimumskrav for Outlook](product-requirements.md#outlook)  
[Bruke tillegg i Outlook på Internett](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]