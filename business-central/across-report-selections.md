---
title: Rapportvalg i Business Central
description: Finn ut mer om hvordan du definerer rapportene du bruker til å skrive ut ulike typer dokumenter i Business Central.
author: edupont04
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.search.form: 306, 307, 347, 385, 524, 865, 5932, 7401, 7355, 99000917
ms.date: 03/11/2022
ms.author: edupont
ms.openlocfilehash: 9106b1ac3f6b179e26c8dfb01212b88e92b694fe
ms.sourcegitcommit: 7b6d70798b4da283d1d3e38a05151df2209c2b72
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/12/2022
ms.locfileid: "8950202"
---
# <a name="report-selection-in-business-central"></a>Rapportvalg i Business Central

Du kan definere standard rapporter som skal brukes til å skrive ut dokumenter for salg og kjøp, for eksempel ordrer, tilbud og fakturaer. Hvis du for eksempel har et bestemt oppsett for salgsfakturaer, kan du angi denne rapporten på siden **Rapportvalg – salg** slik at den blir brukt til å sende eller skrive ut salgsfakturaer.  

Siden **Rapportvalg** angir hvilken rapport som skal skrives ut i forskjellige situasjoner. [!INCLUDE [prod_short](includes/prod_short.md)] gir standardkonfigurasjoner, men du kan endre dem om nødvendig. Du kan også legge til rapporter i sidene **Rapportvalg** hvis du for eksempel vil skrive ut mer enn én rapport per dokumenttype.  

## <a name="available-report-selections"></a>Tilgjengelige rapportvalg

[!INCLUDE [prod_short](includes/prod_short.md)] inneholder forskjellige sider for **rapportvalg** for forskjellige områder. Følgende tabell beskriver hvor du kan finne informasjon om de forskjellige sidene.  

|Område eller oppgave  |Finn ut mer|
|--------------|----------|
|Eksempel på hvordan rapportvalg fungerer (salg)|[Rapportvalg for salgsdokumenter](#example-report-selection-for-sales-documents)|
|Standardoppsett for e-poster med salgs- og kjøpsdokumenter  |[Konfigurer gjenbrukbare e-posttekster og -oppsett for salgs- og kjøpsdokumenter](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts) |
|Definer sjekkoppsett     |[Velg et sjekkoppsett](finance-how-define-check-layouts.md) |
|Definer rapporter for mva-rapportering (Tyskland)|[Sette opp rapporter for mva og Intrastat](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> [!INCLUDE [prod_short](includes/prod_short.md)] kan inkludere flere sider for **rapportvalg**, avhengig av lokasjon og bransje. Du kan alltid kontrollere oppsettet ved å velge ![Lyspæren som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Rapportvalg** og velge den relevante koblingen.

Standardversjonen av [!INCLUDE [prod_short](includes/prod_short.md)] omfatter følgende sider for **rapportvalg**:

* **Rapportvalg – salg**  
* **Rapportvalg – kjøp**  
* **Rapportvalg – beholdning**  
* **Rapportvalg – kontantstrøm**  
* **Rapportvalg – lager**  
* **Rapportvalg – bankkonto**  
* **Purring/rentenota for rapportvalg**  
* **Rapportvalg – prosjekt**  

## <a name="example-report-selection-for-sales-documents"></a>Eksempel: Rapportvalg for salgsdokumenter

Siden **Rapportvalg – salg** definerer standardrapportene som skal brukes i ulike scenarioer for hver av de relaterte dokumenttypene. Velg en dokumenttype i feltet **Bruk**, og legg til eller gå gjennom rapportvalget. Du kan definere mer enn én rapport og rekkefølgen på sekvensen som rapportene må sendes eller skrives ut i.  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Enkelte dokumenttyper kan sendes som e-postvedlegg, og andre kan ikke. Hvis en dokumenttype kan sendes via e-post, inneholder siden for **Rapportvalg** ekstra felter.  

På sidene **Rapportvalg – salg** og **Rapportvalg – kjøp** hjelper følgende felter deg med å konfigurere e-post:

|Feltnavn |Description  |
|-----------|-------------|
|**Bruk for brødtekst i e-post**| Sett inn summert informasjon, for eksempel fakturanummer, forfallsdato og betalingstjenestekobling, i en e-post.        |
|**Bruk for e-postvedlegg**| Knytt det relaterte dokumentet til e-posten.|
|**Oppsettbeskrivelse for brødtekst i e-post**|Angi oppsett for brødtekst i e-post som skal brukes. Oppsettet er vanligvis et egendefinert rapportoppsett. |

## <a name="see-also"></a>Se også

[Definer gjenbrukbare e-posttekster og -oppsett](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts)  
[Velg et sjekkoppsett](finance-how-define-check-layouts.md)  
[Sette opp rapporter for mva og Intrastat (Tyskland)](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[Administrere rapport- og dokumentoppsett](ui-manage-report-layouts.md)  
[Definer dokumentoppsett for kunder og leverandører](ui-define-customer-vendor-document-layouts.md)  
[Konfigurere skrivere](ui-specify-printer-selection-reports.md)  
[Finansrapporter og analyser i Business Central](finance-reports.md)  
[Kunderapporter og -analyser i Business Central](receivables-reports.md) 
[Leverandørrapporter og -analyser i Business Central](payables-reports.md)  
[Rapporter og analyser av aktiva i Business Central](fa-reports.md)  
[Prosjektrapporter og analyser i Business Central](project-reports.md)  
[Salgsrapporter og analyser i Business Central](sales-reports.md)  
[Kjøpsrapporter og analyser i Business Central](purchase-reports.md)  
[Lager og lagerrapporter og analyse i Business Central](inventory-WMS-reports.md)  
[Monteringsrapporter og analyser i Business Central](assembly-reports.md)  
[Produksjonsrapporter og analyser i Business Central](production-reports.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]