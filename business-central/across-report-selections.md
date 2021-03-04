---
title: Rapportvalg i Business Central
description: Finn ut mer om hvordan du definerer rapportene du bruker til å skrive ut ulike typer dokumenter i Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.date: 01/18/2021
ms.author: edupont
ms.openlocfilehash: d30baa44894658c03c3deffdf24a7923293b88fd
ms.sourcegitcommit: 32bfc2acaaf3693afc9aeb86feea505fd328caa1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/19/2021
ms.locfileid: "5024640"
---
# <a name="report-selection-in-business-central"></a>Rapportvalg i Business Central

Du kan konfigurere standardrapporter som skal brukes til å skrive ut forskjellige salgs- og kjøpsdokumenter, for eksempel ordrer, tilbud/forespørsler, fakturaer og kreditnotaer. Hvis du for eksempel har et bestemt oppsett for salgsfakturaer, kan du angi denne rapporten på siden **Rapportvalg – salg** slik at den blir brukt til å sende eller skrive ut salgsfakturaer.  

Siden **Rapportvalg** angir hvilken rapport som skal skrives ut i forskjellige situasjoner. [!INCLUDE [prod_short](includes/prod_short.md)] inkluderer standardkonfigurasjoner, men du kan selvsagt endre disse standardverdiene. Du kan også legge til rapporter i sidene **Rapportvalg** hvis du for eksempel vil skrive ut mer enn én rapport per dokumenttype.  

## <a name="available-report-selections"></a>Tilgjengelige rapportvalg

[!INCLUDE [prod_short](includes/prod_short.md)] inneholder forskjellige sider for **rapportvalg** for forskjellige områder. Følgende tabeller beskriver hvor du kan finne informasjon om de forskjellige sidene.  

|Område eller oppgave  |Finn ut mer|
|--------------|----------|
|Eksempel på hvordan rapportvalg fungerer (salg)|[Rapportvalg for salgsdokumenter](#example-report-selection-for-sales-documents)|
|Standardoppsett for e-poster med salgs- og kjøpsdokumenter  |[Konfigurer gjenbrukbare e-posttekster og -oppsett for salgs- og kjøpsdokumenter](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents) |
|Definer sjekkoppsett     |[Velg et sjekkoppsett](finance-how-define-check-layouts.md) |
|Definer rapporter for mva-rapportering (Tyskland)|[Sette opp rapporter for mva og Intrastat](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> [!INCLUDE [prod_short](includes/prod_short.md)] kan inkludere flere sider for **rapportvalg**, avhengig av lokasjon og bransje. Du kan alltid kontrollere oppsettet ved å velge ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rapportvalg** og velge den aktuelle koblingen.

Standardversjonen av [!INCLUDE [prod_short](includes/prod_short.md)] omfatter følgende sider for **rapportvalg**:

* **Rapportvalg – salg**  
* **Rapportvalg – kjøp**  
* **Rapportvalg – beholdning**  
* **Rapportvalg – kontantstrøm**  
* **Rapportvalg – lager**  
* **Rapportvalg – bankkonto**  
* **Purring/rentenota for rapportvalg**  

## <a name="example-report-selection-for-sales-documents"></a>Eksempel: Rapportvalg for salgsdokumenter

Siden **Rapportvalg – salg** definerer standardrapportene som skal brukes i ulike scenarioer for hver av de relaterte dokumenttypene. Velg en dokumenttype i feltet **Bruk**, og legg til eller gå gjennom rapportvalget. Du kan definere mer enn én rapport og rekkefølgen på sekvensen som rapportene må sendes eller skrives ut i.  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Enkelte dokumenttyper kan sendes som e-postvedlegg, og andre kan ikke. Hver **Rapportvalg**-side viser flere felter hvis typen støtter e-post som standard.  

På sidene **Rapportvalg – salg** og **Rapportvalg – kjøp** hjelper følgende felter deg med å konfigurere e-post:

|Feltnavn |Beskrivelse  |
|-----------|-------------|
|**Bruk for brødtekst i e-post**| Angir at sammendragsinformasjon, for eksempel fakturanummer, forfallsdato og kobling til betalingstjeneste, blir satt inn i tekstdelen i e-posten du sender.        |
|**Bruk for e-postvedlegg**| Angir at det relaterte dokumentet blir lagt ved i e-posten.|
|**Oppsettbeskrivelse for brødtekst i e-post**|Angir oppsettet for e-postbrødtekst som brukes, vanligvis et egendefinert rapportoppsett. |

## <a name="see-also"></a>Se også

[Konfigurer gjenbrukbare e-posttekster og -oppsett for salgs- og kjøpsdokumenter](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents)  
[Velg et sjekkoppsett](finance-how-define-check-layouts.md)  
[Sette opp rapporter for mva og Intrastat (Tyskland)](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[Administrere rapport- og dokumentoppsett](ui-manage-report-layouts.md)  
[Definere dokumentoppsett for kunder og leverandører](ui-define-customer-vendor-document-layouts.md)  
[Konfigurere skrivere](ui-specify-printer-selection-reports.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]