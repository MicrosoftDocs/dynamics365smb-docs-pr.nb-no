---
title: Arbeid med innkommende dokumenter
description: 'Du kan behandle innkommende eksterne forretningsdokumenter, for eksempel kvitteringer eller PDF-filer, behandle OCR-oppgaver og konvertere filer til elektroniske dokumenter og poster.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# Inngående dokumenter

Eksterne forretningsdokumenter kan komme til selskapet ditt som et e-postvedlegg eller en kopi som du skanner til fil. Dette scenarioet er vanlig for kjøp, hvor slike innkommende dokumentfiler representerer kvitteringer for utgifter eller små innkjøp.

På siden **Inngående dokumenter** kan du bruke forskjellige funksjoner til å se gjennom utgiftskvitteringer, behandle OCR-oppgaver og konvertere inngående dokumentfiler, manuelt eller automatisk, til de aktuelle dokumentene eller kladdelinjene. De eksterne filene kan tilknyttes på et hvilket som helst tidspunkt i prosessen, inkludert bokførte dokumenter og resulterende leverandør, kunde- og finansposter.

## Bruksscenario

Du kan registrere filer eller papirkopier som er mottatt fra handelspartnerne, i [!INCLUDE[prod_short](includes/prod_short.md)] og opprette en dokumentpost. Det kan for eksempel være en kjøps- eller salgsfaktura, en kreditnota eller en kladdelinje.

Last opp de mottatte filene, eller bruk enhetskameraet til å ta et bilde – og opprett poster som skal representere de eksterne dokumentene. Med PDF- eller bildefiler som representerer innkommende dokumenter, kan du også få en ekstern OCR-tjeneste (optisk tegngjenkjenning) til å generere elektroniske dokumenter som deretter kan konverteres til poster i [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> OCR-funksjonen tilbys av eksterne leverandører. Velg en tjenestepakke som passer for organisasjonen og/eller landet/området. Finn tjenester som er kompatible med [!INCLUDE[prod_short](includes/prod_short.md)] og detaljer om tilgjengelige funksjoner ved [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

Når du for eksempel mottar en faktura i PDF-format fra leverandøren, kan du sende den til OCR-tjenesten fra siden **Inngående dokumenter**. Noen OCR-leverandører har også muligheten til å behandle filer videresendt til en egen e-postadresse, som deretter oppretter en relatert, innkommende dokumentpost automatisk. Etter noen sekunder vil du motta filen tilbake fra OCR-tjenesten som en elektronisk faktura som kan konverteres til en kjøpsfaktura for leverandøren.

> [!TIP]
> Opprett innkommende dokumentposter i [!INCLUDE[prod_short](includes/prod_short.md)] direkte fra e-poster sendt av leverandører ved hjelp av Outlook-tillegget. Hvis du vil ha mer informasjon, kan du se [Bruk Business Central som innboks for virksomheten i Outlook](work-outlook-addin.md).

## Funksjoner for innkommende dokument

Prosessen for inngående dokumenter kan bestå av følgende hovedaktiviteter:

* Registrere de eksterne dokumentene i [!INCLUDE[prod_short](includes/prod_short.md)] ved å opprette linjer på siden **Inngående dokumenter** på én av følgende måter:
  * Manuelt, fra en PC eller en mobilenhet, på en av følgende måter:
    * Bruk **Opprett fra fil**-knappen, last opp en fil, og fyll deretter ut aktuelle felter på siden **Innkommende dokument**.
    * Bruk **Ny**-knappen, og fyll deretter ut aktuelle felter på siden **Innkommende dokument**, og legg manuelt ved den relaterte filen.
    * Fra et nettverk eller en telefon kan du bruke **Opprett fra kamera**-knappen til å opprette en ny innkommende dokumentpost ved å bruke enhetens innebygde kamera.
  * Automatisk, ved å motta dokumentet fra OCR-tjenesten som et elektronisk dokument etter at du har lastet opp eller sendt den relaterte PDF- eller bildefilen til en OCR-tjeneste. Hurtigfanen **Økonomisk informasjon** fylles ut automatisk på siden **Inngående dokument**.
* Bruk en ekstern OCR-tjeneste til å konvertere PDF- eller bildefiler til elektroniske dokumenter som kan konverteres til dokumentposter i [!INCLUDE[prod_short](includes/prod_short.md)].
* Opprett nye dokumenter eller finanskladdelinje for inngående dokumentposter ved å skrive inn informasjonen mens du leser den fra inngående dokumentfiler.
* Knytte inngående dokumentfiler til salgs- og kjøpsdokumenter med en hvilken som helst status, inkludert til leverandør, kunde- og finansposter som resultat av bokføring.
* Vise innkommende dokumentposter og tilhørende vedlegg fra alle kjøps- og salgsdokument eller oppføringer, eller søke etter alle finansposter uten innkommende dokumentposter fra siden **Kontoplan**.

> [!NOTE]
> Filer som er knyttet til kort og dokumenter på fanen **Vedlegg**, tas ikke med på siden **Innkommende dokumenter**. Se [Behandle vedlegg, koblinger og merknader på kort og dokumenter](ui-how-add-link-to-record.md) hvis du vil ha mer informasjon.

| Til | Se |
| --- | --- |
| Definere funksjonen for **innkommende dokumenter** og OCR-tjenesten. |[Konfigurere inngående dokumenter](across-how-setup-income-documents.md) |
| Opprett poster for inngående dokument manuelt eller automatisk ved for eksempel å ta et bilde av en papirkvittering. |[Opprette innkommende dokumentposter](across-how-create-income-document-records.md) |
| Bruk for eksempel en OCR-tjeneste til å gjøre om PDF- og bildefiler til elektroniske dokumenter som kan konverteres til kjøpsfakturaer i [!INCLUDE[prod_short](includes/prod_short.md)]. Lære opp OCR-tjenesten for å unngå feil i neste gang den behandler liknende data. |[Bruke OCR til å konvertere PDF- og bildefiler til elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md) |
| Tilknytte eller fjerne inngående dokumentposter for alle ikke-bokførte salgs- eller kjøpsdokumenter og til en hvilken som helst kunde, leverandør eller finanspost fra dokumentet eller posten. |[Opprette innkommende dokumentposter direkte fra dokumenter og poster](across-how-connect-disconnect-income-document-records.md) |
| Fra sidene **Kontoplan** og **Finansposter** bruker du søkefunksjonen til å finne finansposter for bokførte dokumenter som ikke har innkommende dokumentposter, og deretter sentralt koble eksisterende poster eller opprette nye med vedlagte dokumentfiler. |[Finne bokførte dokumenter uten innkommende dokumentposter](across-how-find-posted-documents-without-income-document-records.md) |
| Få en bedre oversikt ved å sette inngående dokumentposter til *Behandlet* for å fjerne dem fra standardvisningen. |[Håndter mange inngående dokumentposter](across-how-manage-many-income-document-records.md) |

## Se relatert [Microsoft-opplæring](/training/modules/incoming-documents-dynamics-365-business-central/)

## Se også

[Innkjøp](purchasing-manage-purchasing.md)  
[Redigering av bokførte dokumenter](across-edit-posted-document.md)  
[Utveksle data elektronisk](across-data-exchange.md)  
[Business Central og OneDrive for Business-integrering](across-onedrive-overview.md)  
[Bruk Business Central som forretningsinnboks i Outlook](work-outlook-addin.md)  
[Send dokumenter og e-poster](ui-how-send-documents-email.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
