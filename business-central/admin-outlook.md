---
title: Bruke Business Central med Outlook | Microsoft-dokumentasjon
description: "Denne tjenesten er tett integrert med Office 365, slik at du kan behandle alle forretningssamhandlinger og e-postmeldinger med kunder og leverandører direkte i Outlook."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365
ms.date: 12/10/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: a91f2d34cd023994dcd8eb67a9360d50d2cf3747
ms.contentlocale: nb-no
ms.lasthandoff: 12/11/2018

---
# <a name="using-business-central-as-your-business-inbox-in-outlook"></a>Bruke Business Central som forretningsinnboksen i Outlook
[!INCLUDE[d365fin](includes/d365fin_md.md)] gjør det mulig å behandle forretningssamhandlinger med kunder og leverandører, direkte i Microsoft Outlook. Med [!INCLUDE[d365fin](includes/d365fin_md.md)]-tilleggene for Outlook kan du se økonomiske data relatert til kunder og leverandører, i tillegg til å opprette og sende økonomiske dokumenter, for eksempel tilbud og fakturaer.  

## <a name="getting-the-add-in"></a>Få tillegget
Det er enkelt å begynne med [!INCLUDE[d365fin](includes/d365fin_md.md)]-tillegget til Outlook. I den assisterte oppsettsveiledningen **Konfigurer forretningsinnboksen i Outlook** kan du definere forbindelsen for deg selv eller for organisasjonen. Hvis organisasjonen bruker office 365, må du angi ditt Office 365-navn og -passord. Hvis organisasjonen din ikke bruker Office 365, må du angi opplysninger om hvilken Exchange Server du bruker. [!INCLUDE[d365fin](includes/d365fin_md.md)]-tilleggene legges deretter automatisk til i Outlook.  

Deretter, når du åpner Outlook, vil du se en e-postmelding fra Dynamics 365 Business Central-administratoren. De nye tilleggene blir lagt til Outlook-båndet og i Outlook Web App kan du se tillegget [!INCLUDE[d365fin](includes/d365fin_md.md)] like over eller under brødteksten i e-postmeldingen. Tilleggene oppdateres med jevne mellomrom, og du vil få melding om at en ny versjon er klar for deg i Outlook.  

Enkelte selskaper bruker Office 365, begrense brukernes tillatelser til å distribuere tillegg. Så du må kontrollere at du har et Office 365-abonnement som inkluderer e-post og lar deg distribuere tillegg. Hvis du vil prøve tillegget likevel, kan du [prøve Office 365 gratis](https://products.office.com/try).  

## <a name="using-the-contact-insights-add-in"></a>Bruke tillegget Innsikt for kontakter
La oss si at du får en e-post fra en kunde som ønsker å få et tilbud på noen elementer. Du kan åpne [!INCLUDE[d365fin](includes/d365fin_md.md)]-tillegget direkte i Outlook, som gjenkjenner avsenderen som kunde, og åpner kundekortet for hans firma. Fra dette instrumentbordet kan du se oversiktsinformasjon for kunden, samt vise flere detaljer om bestemte dokumenter. Du kan også vise detaljert informasjon om salgshistorikken for kunden. Hvis det er en ny kunde, kan du opprette dem som en ny kunde i [!INCLUDE[d365fin](includes/d365fin_md.md)] uten å forlate Outlook.  

I tillegget kan du opprette et tilbud og sende det tilbake til kunden uten å forlate Outlook. All informasjon du trenger for å sende tilbudet er tilgjengelig i innboksen for virksomheten i Outlook.  
Når du har angitt dataene, kan du publisere tilbudet. Du kan deretter sende det i e-post. [!INCLUDE[d365fin](includes/d365fin_md.md)] genererer en PDF-fil med tilbudet og legger det ved i e-postmeldingen som du kladder i tillegget.  

På samme måte, hvis du får en e-post fra en leverandør, kan du bruke tillegget til å arbeide med leverandører og kjøpsfakturaer.  

Noen ganger vil du vise flere felt som du kan se i tillegget, for eksempel når du vil fylle ut linjene i en faktura. Hvis du vil gi deg selv litt mer plass å arbeide med, kan du åpne tillegget på en egen side. Det er fortsatt en del av Outlook, men du har mer plass. Når du angir dataene for dokumentet i vinduet, lagres endringene automatisk. Når du er ferdig å skrive inn data for dokumentet, kan du velge **OK**-knappen. Når du velger tilleggsrammen i Outlook, oppdateres dokumentet automatisk med endringene du gjorde i vinduet.  

## <a name="creating-invoices-from-your-meeting-appointments"></a>Opprette fakturaer fra møteavtaler
Noen bedrifter registrere alle fakturerbar avtaler i Outlook-kalenderen. Med [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du opprette fakturaen for kunden fra kalenderelementet: Åpne avtalen, og du kan åpne [!INCLUDE[d365fin](includes/d365fin_md.md)]-tillegget, søke etter eksisterende informasjon eller opprette en faktura eller et annet salgsdokument rett.  

## <a name="doing-quick-document-lookup"></a>Utføre hurtig dokumentoppslag
Tillegget for [!INCLUDE[d365fin](includes/d365fin_md.md)]-dokumentkoblinger gir deg hurtig tilgang til dokumenter som er nevnt i e-postmeldinger. Tillegget er tilgjengelig for en e-postmelding hvis et bilagsnummer gjenkjennes i brødteksten i meldingen. Åpning av tillegget gir hurtig tilgang til dokumentet.  

Hvis du for eksempel mottar en e-postmelding som nevner teksten *S-QUO100*, identifiserer [!INCLUDE[d365fin](includes/d365fin_md.md)] dette som et tilbud, slik at du kan åpne dokumentet i Outlook. I Outlook velger du **Dokumentkoblinger**-knappen like over brødteksten i e-postmeldingen. I Outlook Web App velger du *S-QUO1001*-teksten i brødteksten i e-postmeldingen.  

I Dokumentkoblinger-tillegget kan du endre og utføre handlinger med dokumentet, på samme måte som i [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="adding-the-add-ins-manually"></a>Legge til tillegg manuelt
I noen tilfeller tilleggene ikke få legges til automatisk i Outlook. Selv om du eller en kollega kjørte assistert installasjonsveiledningen på vegne av selskapet, [!INCLUDE[d365fin](includes/d365fin_md.md)] kanskje ikke vises i Outlook. Hvis du opplever dette problemet, kan du legge til [!INCLUDE[d365fin](includes/d365fin_md.md)]-tilleggene manuelt.  

Først må du kontrollere at du har tilgang til tilleggene i Office 365-kontoen. Åpne ganske enkelt Outlook Web Access i en webleser, og legg deretter til `/owa/#path=/options/manageapps` i URL-adressen i adresselinjen. Dette åpner siden **Administrer tillegg**, der du kan aktivere [!INCLUDE[d365fin](includes/d365fin_md.md)] for Outlook. Deretter, når du går tilbake til Outlook, [!INCLUDE[d365fin](includes/d365fin_md.md)] skal være tilgjengelige.  

På samme måte i Outlook-skrivebordsklient, kan du bekrefte at [!INCLUDE[d365fin](includes/d365fin_md.md)] er oppført på siden **Administrer tillegg**.  

I begge tilfeller, hvis [!INCLUDE[d365fin](includes/d365fin_md.md)] fremdeles ikke er tilgjengelig, må du få tilleggsmanifestfilene. Hvis du vil ha mer informasjon, kontakt systemansvarlig for Office 365.

## <a name="see-also"></a>Se også

[Komme i gang](product-get-started.md)  
[Få Business Central på mobilenheten](install-mobile-app.md)  
[Sende dokumenter i e-post](ui-how-send-documents-email.md)  
[Finans](finance.md)  
[Salg](sales-manage-sales.md)  
[Innkjøp](purchasing-manage-purchasing.md)  

