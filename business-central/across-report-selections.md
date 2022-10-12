---
title: Rapportvalg i Business Central
description: Finn ut mer om hvordan du definerer rapportene du bruker til å skrive ut ulike typer dokumenter i Business Central.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.search.form: 306, 307, 347, 385, 524, 865, 5932, 7401, 7355, 99000917
ms.date: 06/09/2022
ms.author: bholtorf
ms.openlocfilehash: fc5bfe8b22d06455379dabd20723fb0ccfe4032b
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607503"
---
# <a name="report-selection-for-documents-in-business-central"></a>Rapportvalg for dokumenter i Business Central

Du kan definere standardrapporter som skal brukes til å skrive ut dokumenter for salg, kjøp og servicedokumenter, for eksempel ordrer, tilbud og fakturaer. Hvis du for eksempel har et bestemt oppsett for salgsfakturaer, kan du angi denne rapporten på siden **Rapportvalg – salg** slik at den blir brukt til å sende eller skrive ut salgsfakturaer.  

## <a name="available-report-selections"></a>Tilgjengelige rapportvalg

Siden **Rapportvalg** angir hvilken rapport som skal skrives ut i forskjellige situasjoner. [!INCLUDE [prod_short](includes/prod_short.md)] gir standardkonfigurasjoner, men du kan endre dem om nødvendig. Du kan også legge til rapporter i sidene **Rapportvalg** hvis du for eksempel vil skrive ut mer enn én rapport per dokumenttype. 

Følgende tabell beskriver hvor du kan finne informasjon om de forskjellige sidene.  

|Område eller oppgave  |Finn ut mer|
|--------------|----------|
|Eksempel på hvordan rapportvalg fungerer (salg)|[Rapportvalg for salgsdokumenter](#example-report-selection-for-sales-documents) finnes nedenfor|
|Standardoppsett for e-poster med salgs- og kjøpsdokumenter  |[Konfigurer gjenbrukbare e-posttekster og -oppsett for salgs- og kjøpsdokumenter](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts) |
|Definer sjekkoppsett     |[Velg et sjekkoppsett](finance-how-define-check-layouts.md) |
|Definer rapporter for mva-rapportering (Tyskland)|[Sette opp rapporter for mva og Intrastat](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> [!INCLUDE [prod_short](includes/prod_short.md)] kan inkludere flere sider for **rapportvalg**, avhengig av lokasjon og bransje. For å kontrollere oppsettet velger du ![Lyspæren som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Rapportvalg** og velg den relevante koblingen.

Standardversjonen av [!INCLUDE [prod_short](includes/prod_short.md)] omfatter følgende sider for **Rapportvalg**:

* **Rapportvalg – salg**  
* **Rapportvalg – kjøp**  
* **Rapportvalg – beholdning**  
* **Rapportvalg – kontantstrøm**  
* **Rapportvalg – lager**  
* **Rapportvalg – bankkonto**  
* **Rapportvalg – prosjekt**  
* **Rapportvalg – service**

## <a name="example-report-selection-for-sales-documents"></a>Eksempel: Rapportvalg for salgsdokumenter

Siden **Rapportvalg – salg** tilbyr standardrapportene som skal brukes i ulike scenarioer for hver av de relaterte dokumenttypene. Velg en dokumenttype i feltet **Bruk**, og legg til eller gå gjennom rapportvalget. Du kan definere mer enn én rapport og angi rekkefølgen rapportene må sendes eller skrives ut i.  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Du kan ikke sende typer dokumenter som e-postvedlegg. For de du kan gjøre det for, inneholder **Rapportvalg**-siden ekstra felt.  

På sidene **Rapportvalg – salg** og **Rapportvalg – kjøp** hjelper følgende felter deg med å konfigurere e-post:

|Feltnavn |Description  |
|-----------|-------------|
|**Bruk for brødtekst i e-post**| Sett inn summert informasjon, for eksempel fakturanummer, forfallsdato eller en kobling til en betalingstjeneste i en e-post.        |
|**Bruk for e-postvedlegg**| Knytt det relaterte dokumentet til e-posten.|
|**Oppsettbeskrivelse for brødtekst i e-post**|Angi oppsett for brødtekst i e-post som skal brukes. Det er vanligvis et egendefinert rapportoppsett. |

## <a name="see-also"></a>Se også

[Definer gjenbrukbare e-posttekster og -oppsett](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts)  
[Velg et sjekkoppsett](finance-how-define-check-layouts.md)  
[Sette opp rapporter for mva og Intrastat (Tyskland)](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[Administrere rapport- og dokumentoppsett](ui-manage-report-layouts.md)  
[Definer dokumentoppsett for kunder og leverandører](ui-define-customer-vendor-document-layouts.md)  
[Konfigurere skrivere](ui-specify-printer-selection-reports.md)  
[Finansrapporter og analyser i Business Central](finance-reports.md)  
[Kunderapporter og analyser av aktiva i Business Central](receivables-reports.md)  
[Leverandørrapporter og analyser av aktiva i Business Central](payables-reports.md)  
[Rapporter og analyser av aktiva i Business Central](fa-reports.md)  
[Prosjektrapporter og analyser i Business Central](project-reports.md)  
[Salgsrapporter og analyser i Business Central](sales-reports.md)  
[Kjøpsrapporter og analyser i Business Central](purchase-reports.md)  
[Lager og lagerrapporter og analyse i Business Central](inventory-WMS-reports.md)  
[Monteringsrapporter og analyser i Business Central](assembly-reports.md)  
[Produksjonsrapporter og analyser i Business Central](production-reports.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
