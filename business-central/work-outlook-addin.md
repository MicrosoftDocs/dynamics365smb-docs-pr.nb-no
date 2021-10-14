---
title: Bruke Business Central med Outlook | Microsoft-dokumentasjon
description: Denne tjenesten er tett integrert med Microsoft 365, slik at du kan behandle alle forretningssamhandlinger og e-postmeldinger med kunder og leverandører direkte i Outlook.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365
ms.date: 08/13/2021
ms.author: jswymer
ms.openlocfilehash: 5de1ae4dc96419d848103a8b4ea9e11113793242
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2021
ms.locfileid: "7589474"
---
# <a name="using-business-central-as-your-business-inbox-in-outlook"></a>Bruke Business Central som forretningsinnboksen i Outlook

[!INCLUDE[prod_short](includes/prod_short.md)] tilbyr et tillegg som lar deg behandle forretningssamhandlinger med kunder og leverandører direkte i Microsoft Outlook. Med [!INCLUDE[prod_short](includes/prod_short.md)]-tillegget for Outlook kan du se økonomiske data relatert til kunder og leverandører, i tillegg til å opprette og sende økonomiske dokumenter, for eksempel tilbud og fakturaer.

[!INCLUDE[prod_short](includes/prod_short.md)]-tillegget består av to separate tillegg som gir følgende funksjoner:

- Innsikt for kontakter

   Dette tillegget lar deg slå opp [!INCLUDE[prod_short](includes/prod_short.md)]-kunde- eller -leverandørinformasjon i e-poster og kalenderavtaler i Outlook. Du kan også opprette og sende [!INCLUDE[prod_short](includes/prod_short.md)]-forretningsdokumenter, for eksempel et tilbud og en faktura, til en kontakt.

- Dokumentvisning

   Når et forretningsdokumentnummer sendes i en e-post, gir dette tillegget en direkte kobling fra brødteksten i e-posten til det aktuelle forretningsdokumentet i [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="get-started"></a>Kom i gang

1. Det første du gjør, er å få [!INCLUDE[prod_short](includes/prod_short.md)]-tillegget installert i Outlook. Administratoren har kanskje allerede installert tillegget for deg. Hvis du ikke er sikker, kontakter du administratoren eller ser neste trinn for å kontrollere om det er installert.

    Hvis tillegget ikke er installert for deg, kan du se [Installer tillegget for eget bruk](admin-outlook.md#install). 

2. Når tillegget er installert, får du tilgang til **[!INCLUDE[prod_short](includes/prod_short.md)]**-tillegget fra en ny eller eksisterende e-postmelding eller kalenderavtale i Outlook.

    Begynn med å logge på Outlook og åpne en e-postmelding. Hvis du bruker Outlook-appen, går du til båndet og ser etter **[!INCLUDE[prod_short](includes/prod_short.md)]**.  Hvis du bruker Outlook på nettet, kan du se etter ![Ikon for Business Central-tillegget i Outlook.](media/outlook-business-central-icon.png) øverst eller nederst i e-postmeldingen eller gå til flere handlinger ![Vis flere handlinger for en e-post i Outlook.](media/outlook-more-actions-button.png) .

    ![Få tilgang til Business Central-tillegg for Outlook.](media/outlook-business-central-addin.png)

   Hvis du har installert tillegget på egen hånd og valgte å få en eksempel-e-post, kan du se etter velkomst-e-posten i innboksen. Denne e-posten inneholder informasjon som hjelper deg med å komme i gang.

Første gang du bruker tillegget, kan det hende du blir bedt om å logge på i [!INCLUDE[prod_short](includes/prod_short.md)]-ruten. I dette tilfellet velger du **Logg på nå** og følger instruksjonene for å logge på Business Central med kontoen din på skjermen.

> [!TIP]
> Hvis du bruker den nye Outlook på nettet, kan du feste **[!INCLUDE[prod_short](includes/prod_short.md)]** slik at det alltid vises umiddelbart, i stedet for å måtte gå til knappen flere handlinger, slik at det blir enklere å se kontaktinnsikter mens du blar gjennom forskjellige e-postmeldinger.

Hvis du vil ha mer informasjon, se [Bruke tillegg i Outlook på Internett](https://support.office.com/article/using-add-ins-in-outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?ns=OLWAO365B&version=16).  

## <a name="work-with-contacts-and-documents-using-the-contact-insights-add-in"></a>Arbeid med kontakter og dokumenter ved hjelp av Kontaktinnsikt-tillegget

La oss si at du får en e-post fra en kunde som ønsker å få et tilbud på noen elementer. Du kan åpne [!INCLUDE[prod_short](includes/prod_short.md)]-tillegget direkte i Outlook, som gjenkjenner avsenderen som kunde, og åpner kundekortet for firmaet. Fra dette instrumentbordet ser du oversiktsinformasjon for kunden og kan drille ned for flere detaljer om bestemte dokumenter. Du kan også vise detaljert informasjon om salgshistorikken for kunden. Hvis det er en ny kontakt, kan du opprette dem som en ny kunde i [!INCLUDE[prod_short](includes/prod_short.md)] uten å forlate Outlook.  

I tillegget kan du opprette et tilbud og sende det tilbake til kunden uten å forlate Outlook. All informasjon du trenger for å sende tilbudet er tilgjengelig i innboksen for virksomheten i Outlook. Når du har angitt dataene, kan du publisere tilbudet og sende det på e-post. [!INCLUDE[prod_short](includes/prod_short.md)] genererer en PDF-fil med tilbudet og legger det ved i e-postmeldingen som du kladder i tillegget.  

På samme måte, hvis du får en e-post fra en leverandør, kan du bruke tillegget til å arbeide med leverandører og kjøpsfakturaer.  

Noen ganger vil du vise flere felt som du kan se i tillegget, for eksempel når du vil fylle ut linjene i en faktura. Hvis du vil gi deg selv litt mer plass å arbeide med, kan du åpne tillegget på en egen side. Det er fortsatt en del av Outlook, men du har mer plass. Når du angir dataene for dokumentet i vinduet, lagres endringene automatisk. Delene nedenfor leder deg gjennom noen grunnleggende oppgaver for å gi deg en generell forståelse av hvordan du bruker det.

> [!TIP]
> Oppgavene forklarer hvordan du bruker tillegget fra en e-postmelding. Men du kan gjøre det samme fra en kalenderavtale i Outlook.

### <a name="look-up-a-business-contact-when-composing-an-email"></a>Slå opp en forretningskontakt når du skriver en e-post

1. Opprett en ny e-postmelding.
2. På båndet går du til **[!INCLUDE[prod_short](includes/prod_short.md)]** og velger **Kontaktinnsikt**. Hvis du bruker Outlook på nettet, går du nederst i meldingen og velger ![Ikon for Business Central-tillegget i Outlook.](media/outlook-business-central-icon.png) > **Kontaktinnsikt**.
3. I **[!INCLUDE[prod_short](includes/prod_short.md)]**-tilleggsruten som åpnes, søker du etter og velger kontakten du vil ha.

    En oversikt over kontaktene vises i ruten, og kontakten legges til i **Til**-linjen i e-posten.

### <a name="view-and-change-the-contact-details-or-switch-company"></a>Vis og endre kontaktdetaljer eller bytte firma

Handlingslinjen øverst i [!INCLUDE[prod_short](includes/prod_short.md)]-tilleggsruten inneholder flere handlinger som gjør at du kan gå dypere inn i detaljene om kontakten og endre ting.

![Handlingslinje for Business Central-tillegg for Outlook.](media/outlook-addin-action-bar.png)

Du kan for eksempel åpne de fullstendige kontaktopplysningene slik de vises i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du arbeider med mer enn ett [!INCLUDE[prod_short](includes/prod_short.md)] selskap, kan du enkelt bytte mellom selskaper.

### <a name="track-incoming-documents"></a>Spor innkommende dokumenter 

Kanskje du bruker listen **Innkommende dokumenter** i [!INCLUDE[prod_short](includes/prod_short.md)] til å spore dokumenter for behandling av leverandører som sender til deg, for eksempel en kjøpsfaktura som må betales. Hvis du gjør det, kan du enkelt opprette Innkommende dokument-poster fra Outlook-tillegget og inkludere e-postvedleggene.

1. Når du mottar en e-post fra en leverandør som har et vedlegg, velger du ![Ikon for Business Central-tillegget i Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]**  > **Kontaktinnsikt**. 

2. På handlingslinjen i tillegget velger du **Vis flere handlinger**, og deretter velger du **Send til innkommende dokumenter ...**. 

### <a name="create-and-send-new-document-to-a-contact"></a>Opprett og send nytt dokument til en kontakt

1. På båndet eller nederst i e-postmeldingen velger du ![Ikon for Business Central-tillegg i Outlook.](media/outlook-business-central-icon.png) **[!INCLUDE[prod_short](includes/prod_short.md)]** > **Nytt**, og deretter velger du dokumenttypen du vil opprette, for eksempel **Tilbud**.
2. Gjør endringer i dokumentet i **[!INCLUDE[prod_short](includes/prod_short.md)]**-tilleggsruten.
3. Når dokumentet er klart for sending til kontakten, velger du **Vis flere handlinger** på handlingslinjen , og deretter velger du handlingen **Send per e-post**.

## <a name="view-a-document-from-an-email-using-the-document-view-add-in"></a>Vis et dokument fra en e-post ved hjelp av tillegget Dokumentvisning

Om det er en e-postmelding du har sendt eller mottatt, kan du bruke et hvilket som helst [!INCLUDE[prod_short](includes/prod_short.md)]-dokument, for eksempel tilbudet, direkte i Outlook. Derfra kan du gjøre endringer og navigere til beslektet informasjon, på samme måte som i [!INCLUDE[prod_short](includes/prod_short.md)].

Hvis du bruker Outlook-appen, velger du bare **Dokumentkobling** øverst i e-postmeldingen. For Outlook på nettet kan du se etter dokumentreferansekoblingen i e-postmeldingen. Teksten på referansekoblingen vil inneholde dokumentnummeret, som er basert på nummerserien som brukes i [!INCLUDE[prod_short](includes/prod_short.md)]. Koblingen for et tilbud kan for eksempel være noe som **Tilbud S-QUO1000**.

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