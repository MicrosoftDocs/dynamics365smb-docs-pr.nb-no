---
title: Definere dokumentspesifikt innhold for e-post | Microsoft-dokumentasjon
description: Du kan definere innhold som skal settes inn i brødteksten i en e-postmelding, for eksempel en PayPal-kobling. Du kan også legge ved dokumenter i e-postmeldinger.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365, cover, body, PayPal, layout
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: 591ec86980240b8ffcfda0cf51debe571e327299
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803374"
---
# <a name="send-documents-by-email"></a>Sende dokumenter i e-post
For å formidle innholdet i forretningsdokumenter raskt til dine forretningspartnere, for eksempel betalingsinformasjon for salgsdokumenter for kunder, kan du bruke funksjonen Rapportoppsett til å definere dokumentspesifikt innhold som blir satt inn automatisk i brødteksten i e-post. Hvis du vil ha mer informasjon, kan du se [Administrere rapport- og dokumentoppsett](ui-manage-report-layouts.md).

Hvis du vil aktivere e-postmeldinger fra [!INCLUDE[d365fin](includes/d365fin_md.md)], starter du det assisterte oppsettet **Konfigurer e-post** på Rollesenteret.

Du kan sende nesten alle dokumenttyper som vedlegg i e-postmeldinger direkte fra siden som viser dokumentet. I tillegg til vedlegget kan du definere dokumentspesifikke brødtekster for e-post med kjerneinformasjon fra dokumentet, som innledes med standardtekst som hilser e-postmottakeren og introduserer det aktuelle dokumentet. For å tilby kundene å betale for salg med elektroniske betalingstjenester, for eksempel PayPal, kan du også sette inn PayPal-informasjonen og -hyperkoblingen i brødteksten i e-posten.

Fra alle dokumenter som støttes starter du sending i e-post ved å velge handlingen **Send** på bokførte dokumenter, eller handlingen **Bokfør og send** på dokumenter som ikke er bokført.

Hvis **E-post**-feltet på siden **Send dokument til** er satt til **Ja (spør om innstillinger)**, vil siden **Send e-post** åpnes forhåndsutfylte med kontaktpersonen i **Til**-feltet og dokumentet vedlagt som en PDF-fil. I **Brødtekst**-feltet kan du angi tekst manuelt eller du kan la feltet fylles ut med en dokumentspesifikk brødtekst for e-post, som du har definert.

Fremgangsmåten nedenfor beskriver hvordan du konfigurerer rapporten **Salg - faktura** til bruk for dokumentspesifikke brødtekster for e-post når du sender bokførte salgsfakturaer i e-post.

## <a name="to-set-up-a-document-specific-email-body-for-sales-invoices"></a>Konfigurere en dokumentspesifikk brødtekst for e-post for salgsfakturaer
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rapportvalg - salg**, og velg deretter den relaterte koblingen.
2. På siden **Rapportvalg - salg**, i **Bruk**-feltet, velger du **Faktura**.
3. På en ny linje i **-Rapport-ID**-feltet, velger du for eksempel standardrapport 1306.
4. Merk av for **Bruk for brødtekst i e-post**.
5. Velg feltet **Oppsettskode for brødtekst i e-post**, og velg deretter et oppsett fra rullegardinlisten.

    Rapportoppsett definerer stilen og innholdet i selve brødteksten i e-posten, inkludert standardteksten som kommer foran kjerneinformasjonen i dokumentet i brødteksten i e-post. Du kan se alle tilgjengelige rapportoppsett hvis du velger knappen **Velg fra hele listen** i rullegardinlisten.
6. Hvis du vil vise eller redigere oppsettet som brødteksten i e-post er basert på, velger du oppsettet på siden **Egendefinerte rapportoppsett** og velger deretter handlingen **Rediger oppsett**.
7. Hvis du vil tilby kundene å betale for salg med elektroniske, kan du konfigurere de relaterte betalingstjenestene, for eksempel PayPal, og deretter også sette inn PayPal-informasjonen og -hyperkoblingen i brødteksten i e-posten. Hvis du vil ha mer informasjon, kan du se [Aktivere kundebetalinger via PayPal](sales-how-enable-payment-service-extensions.md).
8. Velg **OK**.

Nå når du for eksempel velger **Send**-handlingen på siden **Bokført salgsfaktura**, vil brødteksten i e-posten inneholde dokumentinformasjonen fra rapport 1306 foran standardteksten i henhold til rapportoppsettet du valgte i trinn 5.

Fremgangsmåten nedenfor beskriver hvordan du sender en bokført salgsfaktura som en e-postmelding med dokumentet vedlagt som en PDF-fil og en dokumentspesifikk brødtekst i e-posten.

## <a name="to-send-documents-by-email"></a>Sende dokumenter i e-post
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokførte salgsfakturaer**, og velg deretter den relaterte koblingen.
2. Velg den relevante bokførte salgsfakturaen, og velg deretter handlingen **Send**. Siden **Send dokument til** åpnes.
3. I feltet **E-post** velger du **Ja (spør om innstillinger)**. Hvis du vil ha mer informasjon, kan du se [Definere en profil for dokumentsending](sales-how-setup-document-send-profiles.md).
4. Velg **OK**. Siden **Send e-post** åpnes.
5. Angi en gyldig e-postadresse i **Til**-feltet. Standardverdien er kundens e-postadresse.
6. Angi en beskrivende emnetekst i **Emne**-feltet. Standardverdien er kundenavnet og fakturanummeret.
7. Den genererte fakturaen legges som standard ved som en PDF-fil i **Vedlegg**-feltet. Velg oppslagsknappen for å åpne filen eller legge ved en annen.
8. Skriv inn en kort melding til mottakeren i **Tekst**-feltet.

    Hvis en dokumentspesifikk brødtekst i en e-post er konfigurert på siden **Rapportvalg - salg**, fylles **Brødtekst**-feltet ut automatisk. Hvis du vil ha mer informasjon, kan du se [Konfigurere en dokumentspesifikk brødtekst for e-post for salgsfakturaer](ui-how-send-documents-email.md#to-set-up-a-document-specific-email-body-for-sales-invoices).
9. Velg **OK** for å sende e-postmeldingen.

> [!NOTE]  
>   Hvis du ikke vil angi e-postinnstillinger hver gang du sender et dokument via e-post, kan du velge alternativet **Ja (bruk standardinnstillinger)** i **E-post**-feltet på siden **Send dokument til**. I så fall åpnes ikke siden **Send e-post**. Se trinn 4. Hvis du vil ha mer informasjon, kan du se [Definere en profil for dokumentsending](sales-how-setup-document-send-profiles.md).

## <a name="see-also"></a>Se også
[Administrere rapport- og dokumentoppsett](ui-manage-report-layouts.md)  
[Konfigurere e-post](admin-how-setup-email.md)  
[Fakturere salg](sales-how-invoice-sales.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
