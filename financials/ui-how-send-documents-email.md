---
title: Sende dokumenter i e-post| Microsoft-dokumentasjon
description: Sende dokumenter i e-post
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365, cover, body, PayPal, layout
ms.date: 03/30/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: f6d234e40cf01be46d601c92c680e90c71424be0
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-send-documents-by-email"></a>Sende dokumenter i e-post
For å formidle innholdet i forretningsdokumenter raskt til dine forretningspartnere, for eksempel betalingsinformasjon for salgsdokumenter for kunder, kan du bruke funksjonen Rapportoppsett til å definere dokumentspesifikt innhold som blir satt inn automatisk i brødteksten i e-post. Hvis du vil ha mer informasjon, kan du se [Administrere rapport- og dokumentoppsett](ui-manage-report-layouts.md).

Hvis du vil aktivere e-postmeldinger fra [!INCLUDE[d365fin](includes/d365fin_md.md)], starter du det assisterte oppsettet **Konfigurer e-post** på Hjem-siden.

Du kan sende nesten alle dokumenttyper som vedlegg i e-postmeldinger direkte fra vinduet som viser dokumentet. I tillegg til vedlegget kan du definere dokumentspesifikke brødtekster for e-post med kjerneinformasjon fra dokumentet, som innledes med standardtekst som hilser e-postmottakeren og introduserer det aktuelle dokumentet. For å tilby kundene å betale for salg med elektroniske betalingstjenester, for eksempel PayPal, kan du også sette inn PayPal-informasjonen og -hyperkoblingen i brødteksten i e-posten.

Fra alle dokumenter som støttes starter du sending i e-post ved å velge handlingen **Send** på bokførte dokumenter, eller handlingen **Bokfør og send** på dokumenter som ikke er bokført.

Hvis **E-post**-feltet i vinduet **Send dokument til** er satt til **Ja (spør om innstillinger)**, vil vinduet **Send e-post** åpnes forhåndsutfylte med kontaktpersonen i **Til**-feltet og dokumentet vedlagt som en PDF-fil. I **Brødtekst**-feltet kan du angi tekst manuelt eller du kan la feltet fylles ut med en dokumentspesifikk brødtekst for e-post, som du har definert.

Fremgangsmåten nedenfor beskriver hvordan du konfigurerer rapporten **Salg - faktura** til bruk for dokumentspesifikke brødtekster for e-post når du sender bokførte salgsfakturaer i e-post.

## <a name="to-set-up-a-document-specific-email-body-for-sales-invoices"></a>Konfigurere en dokumentspesifikk brødtekst for e-post for salgsfakturaer
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Rapportvalg - salg**, og deretter velger du den beslektede koblingen.
2. I vinduet **Rapportvalg - salg**, i **Bruk**-feltet, velger du **Faktura**.
3. På en ny linje i **-Rapport-ID**-feltet, velger du for eksempel standardrapport 1306.
4. Merk av for **Bruk for brødtekst i e-post**.
5. Velg feltet **Oppsettskode for brødtekst i e-post**, og velg deretter et oppsett fra rullegardinlisten.

    Rapportoppsett definerer stilen og innholdet i selve brødteksten i e-posten, inkludert standardteksten som kommer foran kjerneinformasjonen i dokumentet i brødteksten i e-post. Du kan se alle tilgjengelige rapportoppsett hvis du velger knappen **Velg fra hele listen** i rullegardinlisten.
6. Hvis du vil vise eller redigere oppsettet som brødteksten i e-post er basert på, velger du oppsettet i vinduet **Egendefinerte rapportoppsett** og velger deretter handlingen **Rediger oppsett**.
7. Hvis du vil tilby kundene å betale for salg med elektroniske, kan du konfigurere de relaterte betalingstjenestene, for eksempel PayPal, og deretter også sette inn PayPal-informasjonen og -hyperkoblingen i brødteksten i e-posten. Hvis du vil ha mer informasjon, kan du se [Aktivere kundebetalinger via PayPal](sales-how-enable-payment-service-extensions.md).
8. Velg **OK**-knappen.

Nå når du for eksempel velger **Send**-handlingen i vinduet **Bokført salgsfaktura**, vil brødteksten i e-posten inneholde dokumentinformasjonen fra rapport 1306 foran standardteksten i henhold til rapportoppsettet du valgte i trinn 5.

Fremgangsmåten nedenfor beskriver hvordan du sender en bokført salgsfaktura som en e-postmelding med dokumentet vedlagt som en PDF-fil og en dokumentspesifikk brødtekst i e-posten.

## <a name="to-send-documents-by-email"></a>Sende dokumenter i e-post
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Bokførte salgsfakturaer**, og deretter velger du den beslektede koblingen.
2. Velg den relevante bokførte salgsfakturaen, og velg deretter handlingen **Send**. Vinduet **Send dokument til** åpnes.
3. I feltet **E-post** velger du **Ja (spør om innstillinger)**. Hvis du vil ha mer informasjon, kan du se [Definere en profil for dokumentsending](sales-how-setup-document-send-profiles.md).
4. Velg **OK**-knappen. Vinduet **Send e-post** åpnes.
5. Angi en gyldig e-postadresse i **Til**-feltet. Standardverdien er kundens e-postadresse.
6. Angi en beskrivende emnetekst i **Emne**-feltet. Standardverdien er kundenavnet og fakturanummeret.
7. Den genererte fakturaen legges som standard ved som en PDF-fil i **Vedlegg**-feltet. Velg oppslagsknappen for å åpne filen eller legge ved en annen.
8. Skriv inn en kort melding til mottakeren i **Tekst**-feltet.

    Hvis en dokumentspesifikk brødtekst i e-post er konfigurert i vinduet **Rapportvalg - salg**, fylles **Brødtekst**-feltet ut automatisk. Hvis du vil ha mer informasjon, kan du se avsnittet "Konfigurere en dokumentspesifikk brødtekst for e-post for salgsfakturaer" i dette emnet.
9. Velg **OK**-knappen for å sende e-postmeldingen.

**Merk**: Hvis du ikke vil angi postinnstillinger hver gang du sender et dokument i e-post, kan du velge alternativet **Ja (bruk standardinnstillinger)** i **E-post-feltet** i vinduet **Send dokument til**. I så fall åpnes ikke vinduet **Send e-post**. Se trinn 4. Hvis du vil ha mer informasjon, kan du se [Definere en profil for dokumentsending](sales-how-setup-document-send-profiles.md).

## <a name="see-also"></a>Se også
[Administrere rapport- og dokumentoppsett](ui-manage-report-layouts.md)  
[Konfigurere e-post](madeira-how-setup-email.md)  
[Fakturere salg](sales-how-invoice-sales.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

