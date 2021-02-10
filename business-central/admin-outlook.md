---
title: Bruke Business Central med Outlook | Microsoft-dokumentasjon
description: Denne tjenesten er tett integrert med Microsoft 365, slik at du kan behandle alle forretningssamhandlinger og e-postmeldinger med kunder og leverandører direkte i Outlook.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b04a124ea3e55320c1b3f9be37e54898ba3b16d1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752528"
---
# <a name="using-business-central-as-your-business-inbox-in-outlook"></a>Bruke Business Central som forretningsinnboksen i Outlook

[!INCLUDE[prod_short](includes/prod_short.md)] gjør det mulig å behandle forretningssamhandlinger med kunder og leverandører, direkte i Microsoft Outlook. Med [!INCLUDE[prod_short](includes/prod_short.md)]-tilleggene for Outlook kan du se økonomiske data relatert til kunder og leverandører, i tillegg til å opprette og sende økonomiske dokumenter, for eksempel tilbud og fakturaer.  

## <a name="getting-the-add-in"></a>Få tillegget
Det er enkelt å begynne med [!INCLUDE[prod_short](includes/prod_short.md)]-tillegget til Outlook. I den assisterte oppsettsveiledningen **Konfigurer bedriftsinnboksen i Outlook** kan du definere forbindelsen for deg selv eller for organisasjonen hvis organisasjonen bruker Microsoft 365. Angi ganske enkelt Microsoft 365-brukernavnet og -passordet, hvis du blir bedt om det, og fortell oss om du ønsker å motta et eksempel på en e-postmelding. [!INCLUDE[prod_short](includes/prod_short.md)]-tilleggene legges deretter automatisk til i Outlook. Hvis du vil ha mer informasjon, kan du se [Minimumskrav for Outlook](product-requirements.md#outlook).  

Deretter, når du åpner Outlook, vil du se en e-postmelding fra *Dynamics 365 Business Central-admin*. De nye tilleggene blir lagt til Outlook-båndet, og i leseren kan du se tillegget [!INCLUDE[prod_short](includes/prod_short.md)] like over eller under brødteksten i e-postmeldingen. Tilleggene oppdateres med jevne mellomrom, og du vil få melding om at en ny versjon er klar for deg i Outlook.  

> [!TIP]
> Hvis du bruker den nye Outlook på nettet, kan [!INCLUDE[prod_short](includes/prod_short.md)]-tilleggene være skjult under **Flere handlinger**. Hvis du bruker tillegget ofte, kan du feste det slik at det alltid vises umiddelbart. Hvis du vil ha mer informasjon, se [Bruke tillegg i Outlook på Internett](https://support.office.com/article/using-add-ins-in-outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?ns=OLWAO365B&version=16).  

Hvis du arbeider med mer enn ett [!INCLUDE[prod_short](includes/prod_short.md)] selskap, kan du enkelt bytte mellom selskaper i Outlook. Velg **Flere handlinger** på handlingsfeltet til tillegget, og deretter kan du se alternativet for bytte mellom selskaper.  

<!--TEMP-->
> [!NOTE]
> Bytte mellom firmaer krever [!INCLUDE[prod_short](includes/prod_short.md)] 2019 utgivelsesplan 2 eller nyere, som annonsert i [frigivelsesplanen](/dynamics365-release-plan/2019wave2/dynamics365-business-central/switch-between-companies-business-inbox-outlook).

Enkelte selskaper som bruker Microsoft 365, begrenser brukernes tillatelser til å distribuere tillegg. Så du må kontrollere at du har et Microsoft 365-abonnement som inkluderer e-post og lar deg distribuere tillegg. Hvis du vil prøve tillegget likevel, kan du [prøve Microsoft 365 gratis](https://www.microsoft.com/microsoft-365/try).  

## <a name="using-the-contact-insights-add-in"></a>Bruke tillegget Innsikt for kontakter
La oss si at du får en e-post fra en kunde som ønsker å få et tilbud på noen elementer. Du kan åpne [!INCLUDE[prod_short](includes/prod_short.md)]-tillegget direkte i Outlook, som gjenkjenner avsenderen som kunde, og åpner kundekortet for firmaet. Fra dette instrumentbordet kan du se oversiktsinformasjon for kunden, samt vise flere detaljer om bestemte dokumenter. Du kan også vise detaljert informasjon om salgshistorikken for kunden. Hvis det er en ny kontakt, kan du opprette dem som en ny kunde i [!INCLUDE[prod_short](includes/prod_short.md)] uten å forlate Outlook.  

I tillegget kan du opprette et tilbud og sende det tilbake til kunden uten å forlate Outlook. All informasjon du trenger for å sende tilbudet er tilgjengelig i innboksen for virksomheten i Outlook.  
Når du har angitt dataene, kan du publisere tilbudet. Du kan deretter sende det i e-post. [!INCLUDE[prod_short](includes/prod_short.md)] genererer en PDF-fil med tilbudet og legger det ved i e-postmeldingen som du kladder i tillegget.  

På samme måte, hvis du får en e-post fra en leverandør, kan du bruke tillegget til å arbeide med leverandører og kjøpsfakturaer.  

Noen ganger vil du vise flere felt som du kan se i tillegget, for eksempel når du vil fylle ut linjene i en faktura. Hvis du vil gi deg selv litt mer plass å arbeide med, kan du åpne tillegget på en egen side. Det er fortsatt en del av Outlook, men du har mer plass. Når du angir dataene for dokumentet i vinduet, lagres endringene automatisk. Når du er ferdig å skrive inn data for dokumentet, kan du velge **OK**-knappen. Når du velger tilleggsrammen i Outlook, oppdateres dokumentet automatisk med endringene du gjorde i vinduet.  

## <a name="creating-invoices-from-your-meeting-appointments"></a>Opprette fakturaer fra møteavtaler
Noen bedrifter registrere alle fakturerbar avtaler i Outlook-kalenderen. Med [!INCLUDE[prod_short](includes/prod_short.md)] kan du opprette fakturaen for kunden fra kalenderelementet: Åpne avtalen, og du kan åpne [!INCLUDE[prod_short](includes/prod_short.md)]-tillegget, søke etter eksisterende informasjon eller opprette en faktura eller et annet salgsdokument rett.  

## <a name="doing-quick-document-lookup"></a>Utføre hurtig dokumentoppslag
Tillegget for [!INCLUDE[prod_short](includes/prod_short.md)]-dokumentkoblinger gir deg hurtig tilgang til dokumenter som er nevnt i e-postmeldinger. Tillegget er tilgjengelig for en e-postmelding hvis et bilagsnummer gjenkjennes i brødteksten i meldingen. Åpning av tillegget gir hurtig tilgang til dokumentet.  

Hvis du for eksempel mottar en e-postmelding som nevner teksten *S-QUO100*, identifiserer [!INCLUDE[prod_short](includes/prod_short.md)] dette som et tilbud, slik at du kan åpne dokumentet i Outlook. I Outlook velger du **Dokumentkoblinger**-knappen like over brødteksten i e-postmeldingen. I Outlook Web App velger du *S-QUO1001*-teksten i brødteksten i e-postmeldingen.  

I Dokumentkoblinger-tillegget kan du endre og utføre handlinger med dokumentet, på samme måte som i [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="adding-the-add-ins-manually"></a>Legge til tillegg manuelt
I noen tilfeller tilleggene ikke få legges til automatisk i Outlook. Selv om du eller en kollega kjørte assistert installasjonsveiledningen på vegne av selskapet, [!INCLUDE[prod_short](includes/prod_short.md)] kanskje ikke vises i Outlook. Hvis du opplever dette problemet, kan du legge til [!INCLUDE[prod_short](includes/prod_short.md)]-tilleggene manuelt.  

Først må du kontrollere at du har tilgang til tilleggene i Microsoft 365-kontoen. Du kan ganske enkelt åpne din Outlook i en nettleser, åpne en melding, velge **Flere handlinger** (...) øverst i meldingen, og deretter velge **Hent tillegg** nederst i listen. Dette åpner siden **Tillegg for Outlook**, der du kan aktivere [!INCLUDE[prod_short](includes/prod_short.md)] for Outlook. Deretter, når du går tilbake til Outlook, [!INCLUDE[prod_short](includes/prod_short.md)] skal være tilgjengelige.  

På samme måte som i Outlook-skrivebordsklienten kan du bekrefte at [!INCLUDE[prod_short](includes/prod_short.md)] er oppført på siden **Hent tillegg**.  

I begge tilfeller, hvis [!INCLUDE[prod_short](includes/prod_short.md)] fremdeles ikke er tilgjengelig, må du få tilleggsmanifestfilene. Hvis du vil ha mer informasjon, kontakt systemansvarlig for Microsoft 365.

## <a name="using-other-email-accounts"></a>Bruke andre e-postkontoer

Tilleggene er utformet for bruk med Microsoft 365. Hvis du bruker [!INCLUDE[prod_short](includes/prod_short.md)] lokalt, vet administratoren om du kan bruke [!INCLUDE[prod_short](includes/prod_short.md)]-tilleggene i Outlook. Hvis du vil ha mer informasjon, kan du se [Hvilken e-postadresse kan jeg bruke med [!INCLUDE[prod_short](includes/prod_short.md)]?](across-faq.md#email), artikkelen [Funksjoner som krever bestemte forhold](/dynamics365/business-central/dev-itpro/features-not-implemented-on-premises#features-that-require-specific-circumstances?toc=/dynamics365/business-central/toc.json) og delen [Hvorfor fungerer ikke Outlook-tillegget for mine brukere?](/dynamics365/business-central/dev-itpro/faq#why-doesnt-the-outlook-add-in-work-for-my-users?toc=/dynamics365/business-central/toc.json) i Vanlige spørsmål (generelt) i administrasjonsinnholdet.  

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/alternative-interfaces-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Komme i gang](product-get-started.md)  
[Få Business Central på mobilenheten](install-mobile-app.md)  
[Sende dokumenter i e-post](ui-how-send-documents-email.md)  
[Finans](finance.md)  
[Salg](sales-manage-sales.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Minimumskrav for Outlook](product-requirements.md#outlook)  
[Bruke tillegg i Outlook på Internett](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  
