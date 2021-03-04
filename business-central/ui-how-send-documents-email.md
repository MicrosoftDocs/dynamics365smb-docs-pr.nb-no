---
title: Definere dokumentspesifikt innhold for e-post | Microsoft-dokumentasjon
description: Du kan definere innhold som skal settes inn i brødteksten i en e-postmelding, for eksempel en PayPal-kobling. Du kan også legge ved dokumenter i e-postmeldinger.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365, cover, body, PayPal, layout
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f318825b87b0c9aa51ef8493ba89a74a02384b73
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756870"
---
# <a name="send-documents-and-emails"></a>Send dokumenter og e-poster
Du kan enkelt dele informasjon og dokumenter, for eksempel ordrer og bestillinger samt fakturaer, via e-post direkte fra [!INCLUDE[prod_short](includes/prod_short.md)]], uten å måtte åpne en e-postapp. 

Du kan sende nesten alle typer dokumenter som PDF-vedlegg. Du kan også definere et rapportoppsett som inneholder informasjon fra dokumentet i e-postteksten, sammen med tekst som gjør e-posten mer brukervennlig, for eksempel en standardhilsen. Hvis du vil ha mer informasjon, kan du se [Administrere rapport- og dokumentoppsett](ui-manage-report-layouts.md). <!--this topic does not mention how to set up a layout for email. Need to investigate.-->

Når du sender fakturaer, kan du gjøre det enklere for kunder å betale med en betalingstjeneste, for eksempel PayPal, ved automatisk å legge til informasjon og en kobling til tjenesten i e-posten. Hvis du vil ha mer informasjon, kan du se [Aktivere kundebetalinger gjennom betalingstjenester](sales-how-enable-payment-service-extensions.md).

Hvis du vil aktivere e-postmeldinger fra [!INCLUDE[prod_short](includes/prod_short.md)], starter du den assisterte oppsettveiledningen **Konfigurer e-post**. Hvis du vil ha mer informasjon, kan du se [Konfigurer e-post](admin-how-setup-email.md).

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)]] støtter bare kommunikasjon med utgående e-post. Du kan ikke motta svar innenfra appen.

## <a name="to-send-documents-by-email"></a>Sende dokumenter i e-post
Denne fremgangsmåten beskriver hvordan du knytter en bokført salgsfaktura til en e-postmelding som en PDF-fil, og med dokumentspesifikk e-posttekst. <!--update this-->

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokførte salgsfakturaer**, og velg deretter den relaterte koblingen.
2. Velg fakturaen, og velg deretter handlingen **Skriv ut / send**.
3. I feltet **E-post** velger du **Ja (spør om innstillinger)**. Hvis du vil ha mer informasjon, kan du se [Definere en profil for dokumentsending](sales-how-setup-document-send-profiles.md).
    
    Hvis **E-post**-feltet på siden **Send dokument til** er satt til **Ja (spør om innstillinger)**, vil siden **Send e-post** åpnes forhåndsutfylte med kontaktpersonen i **Til**-feltet og dokumentet vedlagt som en PDF-fil. I **Brødtekst**-feltet kan du angi tekst manuelt eller du kan la feltet fylles ut med en dokumentspesifikk brødtekst for e-post, som du har definert.

4. Velg **OK**-knappen.
5. Angi en gyldig e-postadresse i **Til**-feltet. Standardverdien er kundens e-postadresse.
6. Angi en beskrivende emnetekst i **Emne**-feltet. Standardverdien er kundenavnet og fakturanummeret.
7. Den genererte fakturaen legges som standard ved som en PDF-fil i **Vedlegg**-feltet.
8. Skriv inn en kort melding til mottakeren i **Tekst**-feltet.

    Hvis en dokumentspesifikk tekst i en e-post er konfigurert på siden **Rapportvalg – salg**, fylles **Brødtekst**-feltet ut automatisk. Hvis du vil ha mer informasjon, kan du se [Konfigurer gjenbrukbare e-posttekster og -oppsett for salgs- og kjøpsdokumenter](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents).
9. Velg **OK** for å sende e-postmeldingen.

> [!NOTE]  
> Hvis du ikke vil angi e-postinnstillinger hver gang du sender et dokument via e-post, kan du velge alternativet **Ja (bruk standardinnstillinger)** i **E-post**-feltet på siden **Send dokument til**. I så fall åpnes ikke siden **Send e-post**. Se trinn 4. Hvis du vil ha mer informasjon, kan du se [Definere en profil for dokumentsending](sales-how-setup-document-send-profiles.md).  

## <a name="to-compose-and-send-an-email"></a>Slik skriver og sender du en e-post
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **E-postkonti**, og velg deretter den relaterte koblingen.
2. Velg kontoen du vil sende e-posten fra, og velg deretter handlingen **Skriv e-post**.

## <a name="documents-marked-as-printed-when-they-are-sent"></a>Dokumenter merket som skrevet ut når de sendes
Noen dokumenter i [!INCLUDE[prod_short](includes/prod_short.md)] har et felt som angir hvor mange ganger dokumentet er skrevet ut. Nummeret i dette feltet <!--"that field?" need a name...--> oppdateres også hvis du sender dokumentet via e-post fordi det genereres en PDF-fil for det. Nummeret oppdateres selv om du ikke sender e-posten. <!--guessing this is because emails are technically reports, so the counter bumps up whenever someone creates an email. Need to verify.-->

## <a name="sent-emails-and-your-email-outbox"></a>Sendte e-poster og e-postutboksen
[!INCLUDE[prod_short](includes/prod_short.md)]] lagrer e-postene du sender, på siden **Sendte elementer**. Det gjør at du kan sende e-poster på nytt eller videresende dem til andre. Hvis du ikke finner en e-post i de sendte elementene, ser du etter den på siden **E-postutboks**. 

> [!NOTE]
> Avhengig av utvidelsen som selskapet ditt for e-post, kan administratorer se en liste over meldinger som alle har sendt, men ikke innholdet i meldingene

**E-postutboksen** er stedet der du finner e-postene du har lagret som kladd, og e-postene som ikke kan sendes, for eksempel hvis e-postadressen er ugyldig. For meldinger som ikke er sendt, kan du velge **Vis feil** eller **Undersøk feil** for å feilsøke problemet.

## <a name="see-also"></a>Se også
[Administrere rapport- og dokumentoppsett](ui-manage-report-layouts.md)  
[Konfigurere e-post](admin-how-setup-email.md)  
[Fakturere salg](sales-how-invoice-sales.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]