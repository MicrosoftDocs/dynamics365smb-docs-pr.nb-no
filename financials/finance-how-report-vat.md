---
title: Behandle mva-rapportering til skattemyndighetene | Microsoft-dokumentasjon
description: Finn ut hvordan du lager en rapport med oversikt over mva fra salg i en periode, og sender inn rapporten til skattemyndighetene.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, tax, report, EC sales list, statement
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9b0db56fc08881a94b1f80bafed32d7bcbc24fd8
ms.contentlocale: nb-no
ms.lasthandoff: 07/07/2017


---

# <a name="how-to-report-vat-to-tax-authorities"></a>Rapportere mva til skattemyndighetene
Rapporten med oversikt over EU-salg inneholder mva-beløpene (merverdiavgift) du har innkrevd for salg i EU, slik at du kan sende inn mva-beløpene til webtjenesten til en skattemyndighet.

> [!NOTE]  
>   I Storbritannia må alle selskaper som selger mer enn en bestemt verdi hvert år til kunder i EU-medlemsland, sende inn en elektronisk versjon av rapporten med oversikt over EU-salg i XML-format via nettstedet Her Majesty's Revenue and Customs (HMRC) i Storbritannia.

Rapporten EU-salg - oversikt fungerer bare for land i EU. Den inneholder for eksempel ikke mva for salg til land som Kina eller USA.

For å kunne rapportere mva til skattemyndighetene elektronisk, må du koble [!INCLUDE[d365fin](includes/d365fin_md.md)]til webtjenesten til skattemyndigheten. Dette krever at du oppretter en konto hos skattemyndigheten. Når du har en konto, kan du aktivere en tjenestetilkobling vi gir i [!INCLUDE[d365fin](includes/d365fin_md.md)]. I Storbritannia kan du for eksempel bruke tjenestetilkoblingen **GovTalk**.

Rapporten inneholder én linje for hver type transaksjon med kunden og viser det totale beløpet for hver type transaksjon. Det finnes tre typer transaksjoner som rapporten kan inneholde:  
  
* B2B-varer (bedrift-til-bedrift)  
* B2B-tjenester  
* Triangulerte B2B-varer  
  
B2B-varer og -tjenester angir om du har solgt en vare eller en service, og styres av innstillingen for **EU-tjeneste** i mva-bokføringsoppsettet. Triangulerte B2B-varer angir om du handlet med en tredjepart, og styres av innstillingen for **Trekanthandel** i salgsdokumenter, for eksempel ordrer, fakturaer, kreditnotaer og så videre.  
  
Når du har sendt inn rapporten, overvåker [!INCLUDE[d365fin](includes/d365fin_md.md)] tjenesten og holder en oversikt over kommunikasjonen din. **Status**-feltet angir hvor rapporten er i prosessen. Når myndighetene behandler rapporten, endres for eksempel statusen til **Vellykket**. Hvis skattemyndigheten finner feil i rapporten du har sendt inn, blir statusen for rapporten **Mislyktes**. Du kan vise feilene under **Feil og advarsler**, rette dem og deretter sende inn rapporten på nytt. Hvis du vil se en oversikt over alle rapportene for EU-salg - oversikt, går du til siden **Rapporter for EU-salg - oversikt**.  
  
> [!NOTE]  
>   Hvis du bruker en annen metode til å sende inn rapporten, for eksempel ved å eksportere XML-filen og laste den opp til nettstedet til en skattemyndighet, kan du etterpå velge **Merk som Sendt** for å lukke rapporteringsperioden. Når du merker rapporten som frigitt, kan den ikke redigeres. Hvis du må endre rapporten etter at du har merket den som frigitt, må du åpne den på nytt. 
  
Når skattemyndigheten har sett gjennom rapporten, sender de en e-postmelding til kontaktpersonen for selskapet. I [!INCLUDE[d365fin](includes/d365fin_md.md)] er kontaktpersonen angitt på siden **Selskapsopplysninger**. Før du sender inn rapporten, kontrollerer du at du har valgt en kontaktperson.

<!--> [!NOTE]  
>   Rapporten EU-salg - oversikt kan inneholde opptil 1 000 linjer. Hvis du har flere linjer, må du sende inn enda en rapport. -->

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Koble til webtjenesten til skattemyndigheten
[!INCLUDE[d365fin](includes/d365fin_md.md)] har tjenestetilkoblinger som kobler til nettstedene til skattemyndigheten. Hvis du for eksempel holder til i Storbritannia, må du aktivere tjenestetilkoblingen **GovTalk**.  

1. I feltet **Søk etter side eller rapport** angir du **Tjenestetilkoblinger**, og deretter velger du den aktuelle koblingen. <!-- remember to get the updated text for this-->  
2. Fyll ut de obligatoriske feltene.  

## <a name="to-set-up-the-ec-sales-list-report"></a>Definere rapporten EU-salg - oversikt
1. I feltet **Søk etter side eller rapport** angir du **Mva-rapportoppsett**, og deretter velger du den relaterte koblingen.  
2. Hvis du vil at brukere skal kunne endre rapporten og sende den inn på nytt, merker du av for **Endre sendte rapporter**.  
3. Angi nummerserien som skal brukes for rapporter for EU-salg - oversikt.  

## <a name="to-prepare-and-submit-the-ec-sales-list-report"></a>Lage og sende inn rapporten EU-salg - oversikt
1. I feltet **Søk etter side eller rapport** angir du **EU-salg - oversikt**, og deretter velger du den relaterte koblingen.  
2. Velg **Ny**, og fyll deretter ut de obligatoriske feltene.  
3. Du genererer innholdet i rapporten ved å velge handlingen **Foreslå linjer**.  

    > [!NOTE]  
>   Du kan se gjennom transaksjonene på linjen før du sender inn rapporten. Velg linjen for å gjøre dette, og velg deretter handlingen **Vis mva-poster**.  
4. Du klargjør rapporten for innsending ved å velge handlingen **Frigi**.  
5. Du sender inn rapporten ved å velge handlingen **Send**.  
  
[!INCLUDE[d365fin](includes/d365fin_md.md)] validerer om rapporten er riktig definert. Hvis valideringen mislykkes, vises feilene under **Feil og advarsler**, slik at du kan foreta de nødvendige endringene.

## <a name="viewing-communications-with-your-tax-authority"></a>Vise kommunikasjon med skattemyndigheten
I enkelte land utveksler du meldinger med skattemyndigheten når du sender inn rapporter. Du kan vise den første og siste meldingen du har sendt eller mottatt, ved å velge handlingene **Last ned sendingsmelding** og **Last ned svarmelding**.  

## <a name="configuring-your-own-vat-reports"></a>Konfigurere dine egne mva-rapporter
Du kan bruke rapporten EU-salg - oversikt som den er, men du kan også lage dine egne rapporter. Dette krever at du lager noen kodeenheter. Hvis du vil ha hjelp med dette, kan du kontakte en Microsoft-partner.  
    
Tabellen nedenfor beskriver kodeenhetene du må lage for rapporten.

| Kodeenhet | Det den må gjøre |
|----|-----|
|Foreslå linjer| Hente informasjon fra tabellen Mva-poster og vise den på linjer i mva-rapporten.|
|Innhold | Styre formatet på rapporten, for eksempel om det er XML eller JSON. Formatet som skal brukes, er avhengig av kravene som gjelder i webtjenesten til skattemyndighetene. |
|Innsending | Styre hvordan og når du sender inn rapporten, basert på kravene til skattemyndigheten. |
|Svarbehandler | Håndtere returer fra skattemyndighetene. Den kan for eksempel sende en e-postmelding til kontaktpersonen i selskapet ditt. |
|Annuller | Sende en annullering av en mva-rapport ble sendt inn til skattemyndigheten tidligere. |

> [!NOTE]  
>   Når du lager kodeenheter for rapporten, må du være oppmerksom på verdien i feltet **Versjon av mva-rapport**. Dette feltet må gjenspeile versjonen av rapporten som skattemyndigheten krever eller krevde. Du kan for eksempel angi **2017** i feltet for å angi at rapporten følger kravene som var gjeldende for dette året. For å finne nåværende versjon kontakter du skattemyndigheten.  

## <a name="see-also"></a>Se også 
[Konfigurere mva](finance-setup-vat.md)  
[Definere salg](sales-setup-sales.md)  
[Fakturere salg](sales-setup-sales.md)  

