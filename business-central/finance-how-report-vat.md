---
title: Sende mva-rapporter til skattemyndighetene | Microsoft-dokumentasjon
description: "Finn ut hvordan du lager rapporter med oversikt over mva fra salg i en periode, eller fra salg og kjøp, og sender inn rapporten til skattemyndighetene."
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, tax, report, EC sales list, statement
ms.date: 07/17/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 975703333b1a675ae78b70d99b1394d370490e9d
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---

# <a name="how-to-report-vat-to-a-tax-authority"></a>Rapportere mva til skattemyndighetene
Dette emnet beskriver rapportene i [!INCLUDE[d365fin](includes/d365fin_md.md)] som du kan bruke til å legge inn informasjon om merverdiavgiftsbeløp (mva) for salg og kjøp til skattemyndighetene i regionen.

Du kan bruke følgende rapporter:

* Den **EU-salg -oversikt** europeisk gruppen (EU) Salgsoversikt viser verdien som er lagt til mva-beløp som du har samlet for salg til mva-registrerte kunder i EU-land.  
* Rapporten **Omsetningsoppgave** inkluderer mva for salg og kjøp for kunder i alle land som bruker mva.

Hvis du vil vise en fullstendig historikk over mva-poster, for hver bokføring som gjelder mva, opprettes en post på siden **mva-poster**. Disse postene brukes til å beregne mva-oppgjørsbeløp, for eksempel betaling eller refusjon, for en bestemt periode. For å rapportere mva-poster, velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Mva-poster**, og velg deretter den relaterte koblingen.

## <a name="about-the-ec-sales-list-report"></a>Om rapporten EU-salg - oversikt
Storbritannia, må alle selskapene som selger varer og tjenester til mva-registrerte kunder, inkludert kunder i andre EU EU-land, sende en elektronisk versjon av rapporten i XML-format gjennom Her Majesty Salgsoversikt europeisk gruppen (EU) Nettstedet for inntekts- og avgiftsmyndighetene (HMRC). Rapporten EU-salg - oversikt fungerer bare for land i EU.

Rapporten inneholder én linje for hver type transaksjon med kunden og viser det totale beløpet for hver type transaksjon. Det finnes tre typer transaksjoner som rapporten kan inneholde:  

* B2B-varer (bedrift-til-bedrift)  
* B2B-tjenester  
* Triangulerte B2B-varer  

B2B-varer og -tjenester angir om du har solgt en vare eller en service, og styres av innstillingen for **EU-tjeneste** i mva-bokføringsoppsettet. Triangulerte B2B-varer angir om du handlet med en tredjepart, og styres av innstillingen for **Trekanthandel** i salgsdokumenter, for eksempel ordrer, fakturaer, kreditnotaer og så videre.  

Når skattemyndigheten har sett gjennom rapporten, sender de en e-postmelding til kontaktpersonen for selskapet. I [!INCLUDE[d365fin](includes/d365fin_md.md)] er kontaktpersonen angitt på siden **Selskapsopplysninger**. Før du sender inn rapporten, kontrollerer du at du har valgt en kontaktperson.

## <a name="about-the-vat-return-report"></a>Om rapporten Omsetningsoppgave
Bruk denne rapporten til å sende inn mva for salg og kjøpsdokumenter, for eksempel innkjøp og ordrer, fakturaer og kreditnotaer. Informasjonen i rapporten vises i samme format som i deklarasjonen fra toll- og avgiftsmyndighetene.  

Mva. beregnes på grunnlag av mva-bokføringsoppsettet og mva-bokføringsgruppene du har definert.

For omsetningsoppgaven kan du angi postene som skal tas med:

* Sende inn bare åpne transaksjoner eller åpne og lukkede. Dette er for eksempel nyttig når du forbereder endelige årlige omsetningsoppgaven.
* Sende inn bare poster fra de angitte periodene, eller også ta med poster fra tidligere perioder. Dette er nyttig hvis du vil oppdatere en omsetningsoppgave du har allerede har sendt, for eksempel hvis en leverandør sender en faktura for sent.    

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Koble til webtjenesten til skattemyndigheten
[!INCLUDE[d365fin](includes/d365fin_md.md)] har tjenestetilkoblinger til nettstedene til skattemyndigheten. Hvis du har Storbritannia, kan du aktivere den **GovTalk** service tilkobling sende EU Salgsoversikt og gå tilbake mva-rapporter elektronisk. Hvis du vil sende rapporten manuelt, er for eksempel ved dataregistrering for skattemyndighetene webområde, ikke nødvendig.   

For å kunne rapportere mva til skattemyndighetene elektronisk, må du koble [!INCLUDE[d365fin](includes/d365fin_md.md)]til webtjenesten til skattemyndigheten. Dette krever at du oppretter en konto hos skattemyndigheten. Når du har en konto, kan du aktivere en tjenestetilkobling vi gir i [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Tjenestetilkoblinger**, og velg deretter den aktuelle koblingen.
2. Fyll ut de obligatoriske feltene. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    >   Det er lurt å teste tilkoblingen. Du gjør dette ved å merke av for **Testmodus** og deretter forberede og sende mva-rapporten som beskrevet i delen _Forberede og sende inn en omsetningsoppgave_. I testmodus tester tjenesten om skattemyndighetene kan motta rapporten, og statusen for rapporten angir om testinnsendingen var vellykket. Det er viktig å huske at dette ikke er en faktisk innsending. Hvis du vil faktisk sende inn rapporten, må du fjerne merket for **Testmodus** og deretter gjenta innsendingsprosessen.

## <a name="to-set-up-vat-reports-in-included365finincludesd365finmdmd"></a>Slik setter du opp omsetningsoppgaver i [!INCLUDE[d365fin](includes/d365fin_md.md)]
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Mva-rapportoppsett**, og velg deretter den relaterte koblingen.  
2. Hvis du vil at brukere skal kunne endre rapporten og sende den inn på nytt, merker du av for **Endre sendte rapporter**.  
3. Velg nummerserien som skal brukes for hver rapport.  

## <a name="to-prepare-and-submit-a-vat-report"></a>Slik forbereder du og sender inn en omsetningsoppgave
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **EU-salg - oversikt** eller **Omsetningsoppgave**, og velg deretter den relaterte koblingen.  
2. Velg **Ny**, og fyll deretter ut de obligatoriske feltene. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Du genererer innholdet i rapporten ved å velge handlingen **Foreslå linjer**.  

    > [!NOTE]  
    >   For rapporten EU-salg - oversikt kan du gå gjennom transaksjonene som er inkludert i rapportlinjene, før du sender rapporten. Velg linjen for å gjøre dette, og velg deretter handlingen **Vis mva-poster**.  
4. Du validerer og klargjør rapporten for innsending ved å velge handlingen **Frigi**.  

    >  [!NOTE]  
    >   [!INCLUDE[d365fin](includes/d365fin_md.md)] validerer om rapporten er riktig definert. Hvis valideringen mislykkes, vises feilene under **Feil og advarsler**, slik at du vet hva du må løse. Vanligvis, hvis meldingen er om en manglende innstilling i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du klikke meldingen for å åpne siden som inneholder informasjon for å korrigere.  
5. Du sender inn rapporten ved å velge handlingen **Send**.  

Når du har sendt inn rapporten, overvåker [!INCLUDE[d365fin](includes/d365fin_md.md)] tjenesten og holder en oversikt over kommunikasjonen din. **Status**-feltet angir hvor rapporten er i prosessen. Når myndighetene behandler rapporten, endres for eksempel statusen til **Vellykket**. Hvis skattemyndigheten finner feil i rapporten du har sendt inn, blir statusen for rapporten **Mislyktes**. Du kan vise feilene under **Feil og advarsler**, rette dem og deretter sende inn rapporten på nytt. Hvis du vil se en oversikt over alle rapportene for EU-salg - oversikt, går du til siden **Rapporter for EU-salg - oversikt**.  

## <a name="viewing-communications-with-your-tax-authority"></a>Vise kommunikasjon med skattemyndigheten
I enkelte land utveksler du meldinger med skattemyndigheten når du sender inn rapporter. Du kan vise den første og siste meldingen du har sendt eller mottatt, ved å velge handlingene **Last ned sendingsmelding** og **Last ned svarmelding**.  

## <a name="submitting-vat-reports-manually"></a>Sende inn mva-rapporter manuelt
Hvis du bruker en annen metode til å sende inn rapporten, for eksempel ved å eksportere XML-filen og laste den opp til nettstedet til en skattemyndighet, kan du etterpå velge **Merk som Sendt** for å lukke rapporteringsperioden. Når du merker rapporten som frigitt, kan den ikke redigeres. Hvis du må endre rapporten etter at du har merket den som frigitt, må du åpne den på nytt.

## <a name="vat-settlement"></a>Mva-oppgjør
Du må jevnlig remittere netto mva til skattemyndighetene. Hvis du må gjøre opp mva ofte, kan du kjøre kjørselen **Beregn og bokfør mva-oppgjør** for å lukke åpne mva-poster og overføre inngående og utgående mva-beløp til kontoen for mva-oppgjør.

Når du overfører mva-beløp til oppgjørskontoen, krediteres kontoen for inngående mva., og kontoen for utgående mva. debiteres med beløpene som er beregnet for den angitte perioden. Nettobeløpet krediteres mva-oppgjørskontoen, eller debiteres hvis det inngående mva-beløpet er størst. Du kan bokføre oppgjøret umiddelbart eller skrive ut en testrapport først.

>    [!NOTE]  
>    Når du bruker kjørselen **Beregn og bokfør mva-oppgjør**, hvis du ikke angir en **Mva-bokføringsgruppe - firma** og en **Mva-bokføringsgruppe - vare**, inkluderes poster som har alle firma-og varebokføringsgrupper.

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
[Definere beregninger og bokføringsmetoder for merverdiavgift](finance-setup-vat.md)  
[Arbeide med mva på kjøp og salg](finance-work-with-vat.md)  
[Sette opp salg](sales-setup-sales.md)  
[Fakturere salg](sales-setup-sales.md)  

