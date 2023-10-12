---
title: Send dokumenter og e-poster
description: 'Du kan definere innhold som skal settes inn i brødteksten i en e-postmelding, for eksempel en PayPal-kobling. Du kan også legge ved dokumenter i e-postmeldinger.'
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: 'SMTP, mail, Microsoft 365, cover, body, PayPal, layout'
ms.search.form: '41,'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Send dokumenter og e-poster

Du kan enkelt dele informasjon og dokumenter, for eksempel ordrer og bestillinger samt fakturaer, via e-post direkte fra [!INCLUDE[prod_short](includes/prod_short.md)], uten å måtte åpne en e-postapp.  

Du kan sende nesten alle typer dokumenter som PDF-vedlegg. Du kan også definere et rapportoppsett som inneholder informasjon fra dokumentet i e-postteksten, sammen med tekst som gjør e-posten mer brukervennlig, for eksempel en standardhilsen. Hvis du vil ha mer informasjon, kan du se [Administrere rapport- og dokumentoppsett](ui-manage-report-layouts.md).

Når du sender fakturaer, kan du gjøre det enklere for kunder å betale med en betalingstjeneste, for eksempel PayPal, ved automatisk å legge til informasjon og en kobling til tjenesten i e-posten. Hvis du vil ha mer informasjon, kan du se [Aktivere kundebetalinger gjennom betalingstjenester](sales-how-enable-payment-service-extensions.md).

Hvis du vil aktivere e-postmeldinger fra [!INCLUDE[prod_short](includes/prod_short.md)], starter du den assisterte oppsettveiledningen **Konfigurer e-post**. Hvis du vil ha mer informasjon, kan du se [Konfigurer e-post](admin-how-setup-email.md).

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] støtter bare kommunikasjon med utgående e-post. Du kan ikke motta svar innenfra appen.

## Sende dokumenter i e-post

Denne fremgangsmåten beskriver hvordan du knytter en bokført salgsfaktura til en e-postmelding som en PDF-fil, og med dokumentspesifikk e-posttekst. Trinnene er de samme for andre dokumenter.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bokførte salgsfakturaer**, og velg deretter den relaterte koblingen.
2. Velg fakturaen, og velg handlingen **Skriv ut / send** og deretter **Send via e-post**.
3. I feltet **E-post** velger du **Ja (spør om innstillinger)**. Hvis du vil ha mer informasjon, kan du se [Definere en profil for dokumentsending](sales-how-setup-document-send-profiles.md).

    Hvis **E-post**-feltet på siden **Send dokument til** er satt til **Ja (spør om innstillinger)**, vil siden **Send e-post** åpnes forhåndsutfylte med kontaktpersonen i **Til**-feltet og dokumentet vedlagt som en PDF-fil. I **Brødtekst**-feltet kan du angi tekst manuelt eller du kan la feltet fylles ut med en dokumentspesifikk brødtekst for e-post, som du har definert.

4. Velg **OK**-knappen.
5. Angi en gyldig e-postadresse i **Til**-feltet. Standardverdien er kundens e-postadresse.
6. Angi en beskrivende emnetekst i **Emne**-feltet. Standardverdien er kundenavnet og fakturanummeret.
7. Den genererte fakturaen legges som standard ved som en PDF-fil i **Vedlegg**-feltet.
8. Skriv inn en kort melding til mottakeren i **Tekst**-feltet.

    Hvis en dokumentspesifikk tekst i en e-post er konfigurert på siden **Rapportvalg – salg**, fylles **Brødtekst**-feltet ut automatisk. Hvis du vil ha mer informasjon, kan du se [Definer gjenbrukbare e-tekster og oppsett](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts).
9. Velg **OK** for å sende e-postmeldingen.

> [!NOTE]  
> Hvis du ikke vil angi e-postinnstillinger hver gang du sender et dokument via e-post, kan du velge alternativet **Ja (bruk standardinnstillinger)** i **E-post**-feltet på siden **Send dokument til**. I så fall åpnes ikke siden **Send e-post**. Se trinn 4. Hvis du vil ha mer informasjon, kan du se [Definere en profil for dokumentsending](sales-how-setup-document-send-profiles.md).  

## Slik skriver og sender du en e-post

Du kan raskt skrive e-postmeldinger for kontakter, kunder, leverandører, selgere/innkjøpere og bankkontoer direkte fra sidene for disse enhetene. Velg **Behandle** og **Send e-post** for å åpne redigeringsprogrammet for e-post. Når det gjelder bankkonti, er handlingen **Send e-post** under **Handlinger**.

> [!TIP]
> Hvis du ofte sender e-postmeldinger som ligner, eller vil sende en massekommunikasjon, for eksempel for å annonsere en salgskampanje, kan du bruke Word-maler med e-post til å gjøre prosessen raskere. Du kan opprette en mal for en enhet, for eksempel kunder, leverandører og kontakter, som vil generere innholdet i en e-postmelding for deg og til og med tilpasse innholdet for mottakeren basert på data i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Bruk Word-maler til massekommunikasjon](ui-mail-merge.md).  

### Legg ved et dokument i en e-post

Det finnes flere måter å legge ved dokumenter i e-poster på.

Hvis du er tildelt et e-postscenario som gjelder enheten du sender e-postmeldingen til eller dokumentet du sender, kan et vedlegg automatisk legges til meldingen. Dette skyldes at et standardvedlegg er tildelt e-postscenarioet. Du kan slette vedlegget hvis du ikke vil sende det med meldingen. Hvis du vil ha mer informasjon, kan du se [Tilordne e-postscenarioer til e-postkontoer](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts). 

Bruk følgende handlinger for å legge ved en fil i redigeringsprogrammet for e-post:

* Velg **Legg til fil** for å velge en fil.
* Velg **Legg til filer fra standardutvalg** hvis du vil legge til en fil som er tilknyttet e-postscenarioet manuelt.
* Velg **Legg til fil fra kildedokument** for å velge en fil som er knyttet til dokumentet du arbeider med. Filene er enten knyttet til selve dokumentet eller en eller flere av linjene.

## Dokumenter merket som skrevet ut når de sendes

Noen dokumenter i [!INCLUDE[prod_short](includes/prod_short.md)] har et felt som angir hvor mange ganger dokumentet er skrevet ut. Nummeret i dette feltet <!--"that field?" need a name...--> oppdateres også hvis du sender dokumentet via e-post fordi det genereres en PDF-fil for det. Nummeret oppdateres selv om du ikke sender e-posten. <!--guessing this is because emails are technically reports, so the counter bumps up whenever someone creates an email. Need to verify.-->

## Sendte e-poster og e-postutboksen

[!INCLUDE[prod_short](includes/prod_short.md)] lagrer e-postene du sender, på siden **Sendte elementer**. Det gjør at du kan sende e-poster på nytt eller videresende dem til andre. Hvis du ikke finner en e-post i de sendte elementene, ser du etter den på siden **E-postutboks**. 

> [!NOTE]
> Avhengig av utvidelsen som selskapet ditt for e-post, kan administratorer se en liste over meldinger som alle har sendt, men ikke innholdet i meldingene

**E-postutboksen** er stedet der du finner e-postene du har lagret som kladd, og e-postene som ikke kan sendes, for eksempel hvis e-postadressen er ugyldig. For meldinger som ikke er sendt, kan du velge **Vis feil** eller **Undersøk feil** for å feilsøke problemet.  

## Se også

[Administrer rapport- og dokumentoppsett](ui-manage-report-layouts.md)  
[Konfigurere e-post](admin-how-setup-email.md)  
[Fakturer salg](sales-how-invoice-sales.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
