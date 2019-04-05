---
title: Arbeide med mva på kjøp og salg | Microsoft-dokumentasjon
description: Dette emnet beskriver hvordan du utfører oppgaver som å korrigere bokført mav i EU-land/regioner, hver salgs- og kjøpstransaksjon er underlagt mva-beregninger. Dette emnet beskriver hvordan.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, sales, purchases,
ms.date: 10/01/2018
ms.author: bholtorf
ms.openlocfilehash: 9d6f3cf74582283e633d9c3347def5289aeb8f88
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803262"
---
# <a name="work-with-vat-on-sales-and-purchases"></a>Arbeide med mva på kjøp og salg
Hvis landet eller regionen din krever at du beregner merverdiavgift (mva) i salgs- og kjøpstransaksjoner, slik at du kan rapportere beløpene til en skattemyndighet, kan du sette opp [!INCLUDE[d365fin](includes/d365fin_md.md)] til å beregne mva automatisk på salgs- og kjøpsdokumenter. Hvis du vil ha mer informasjon, kan du se [Definere beregninger og bokføringsmetoder for merverdiavgift](finance-setup-vat.md).

Det er imidlertid enkelte mva-relaterte oppgaver som du kan gjøre manuelt. For eksempel kan det hende du må korrigere et bokført beløpet hvis du oppdager at en leverandør bruker forskjellige Avrundingsmetode.

## <a name="calculating-and-displaying-vat-amounts-in-sales-and-purchase-documents"></a>Beregne og vise mva-beløp i salgs- og kjøpsdokumenter  
Du kan beregne og vise mva-beløp i salgs- og kjøpsdokumenter på forskjellig måte, avhengig av hvilken type kunde eller leverandør du handler med. Du kan også overstyre det beregnede mva-beløpet, slik at det tilsvarer med mva-beløpet leverandøren har beregnet for en gitt transaksjon.  

### <a name="unit-price-and-line-amount-includingexcluding-vat-on-sales-documents"></a>Salgspris og linjebeløp med/uten mva på salgsdokumenter  
Når du velger et varenummer i **Nr.**- feltet i et salgsdokument, blir også **Salgspris**-feltet fylt ut i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Salgsprisen kommer fra **varekortet** eller fra salgsprisene som er tillatt for varen og kunden. [!INCLUDE[d365fin](includes/d365fin_md.md)] beregner **linjebeløpet** bare når du angir en mengde for linjen.  

Hvis du selger til detaljistkunder, vil du kanskje at priser på salgsdokumenter skal inkludere mva. Dette gjør du ved å merke av for **Priser inkl. mva.** for dokumentet.  

### <a name="including-or-excluding-vat-on-prices"></a>Med eller uten mva i priser
Hvis det er merket av for **Priser inkl. mva.** i et salgsdokument, oppdateres feltene **Salgspris** og **Linjebeløp** slik at de inkluderer mva, og feltnavnene vil også gjenspeile dette. Som standard er mva ikke inkludert i disse feltene.  

Hvis dette feltet ikke er valgt, blir feltene **Salgspris** og **Linjebeløp** fylt ut uten mva, og feltnavnene vil gjenspeile dette.  

Du kan definere standardinnstillingen for **Priser inkl. mva** for alle salgsdokumenter for en kunde i feltet **Priser inkl. mva.** på **Kunde**-kortet. Du kan også definere at salgspriser skal ha med mva eller ikke. Salgspriser på varekortet vil vanligvis være prisen uten mva. Informasjonen fra feltet **Pris inkl. mva.** på **Vare**-kortet brukes til å fastsette salgsprisbeløpet for salgsdokumenter.  

Tabellen nedenfor inneholder en oversikt over hvordan salgsprisbeløpene beregnes for et salgsdokument når du ikke har definert priser på **Salgspris**-siden:  

|**Feltet Pris inkl. mva. på varekortet**|**Feltet Priser inkl. mva. i salgshodet**|**Utført handling**|  
|-----------------------------------------------|----------------------------------------------------|--------------------------|  
|Ingen avmerking|Ingen avmerking|**Salgsprisen** på varekortet kopieres til feltet **Salgspris Ekskl. mva.** på salgslinjene.|  
|Ingen avmerking|Avmerking|Mva-beløpet per enhet beregnes og legges til i **enhetsprisen** på varekortet. Den totale salgsprisen angis deretter i feltet **Salgspris Inkl. mva.** på salgslinjene.|  
|Avmerking|Ingen avmerking|Mva-beløpet i **Salgspris**på varekortet beregnes ved hjelp av mva-prosenten som er knyttet til kombinasjonen av mva-bokføringsgruppe for firma (pris) og mva-bokføringsgruppe for vare. **Salgsprisen** på varekortet, redusert med mva-beløpet, angis deretter i feltet **Salgspris Ekskl. mva.** på salgslinjene.|  
|Avmerking|Avmerking|**Salgsprisen** på varekortet kopieres til feltet **Salgspris Inkl. mva.** på salgslinjene.|

## <a name="correcting-vat-amounts-manually-in-sales-and-purchase-documents"></a>Korrigere mva-beløp manuelt i salgs- og kjøpsdokumenter  
Du kan foreta korrigeringer i bokførte mva-poster. Dette gjør at du kan endre de totale mva-beløpene for salg eller kjøp uten å endre mva-grunnlaget. Dette kan være nødvendig hvis du for eksempel mottar en faktura fra en leverandør som har beregnet mva. feil.  

Selv om du kan ha satt opp én eller flere kombinasjoner for å håndtere import-mva, må du definere minst én mva-produktbokføringsgruppe. Du kan for eksempel kalle den **KORRIGER** og bruke den til korreksjonsformål, med mindre du kan bruke den samme finanskontoen i feltet **Inngående mva-konto** på linjen for mva-bokføringsoppsett. Hvis du vil ha mer informasjon, kan du se [Definere beregninger og bokføringsmetoder for merverdiavgift](finance-setup-vat.md).

Når kontantrabatten er tildelt, kan du tilbakestille den delen av kontantrabatten som gjelder mva-beløpet hvis det er beregnet en kontantrabatt på bakgrunn av et fakturabeløp med mva. Merk at du må aktivere feltet **Juster for kontantrabatt** både i finansoppsettet generelt og i mva-bokføringsoppsettet for en bestemt kombinasjon av mva-firmabokføringsgrupper og mva-varebokføringsgrupper.  

#### <a name="to-manually-enter-vat-in-sales-documents"></a>Slik angir du mva manuelt i salgsdokumenter  
1. På siden **Finansoppsett** angir du **Maks. tillatte mva-differanse** mellom beløpet som beregnes i programmet, og det manuelle beløpet.  
2. Merk av for **Tillat mva-differanse** på siden **Salgsoppsett**.  

#### <a name="to-adjust-vat-for-a-sales-document"></a>Slik justerer du mva for et salgsdokument  
1. Åpne den aktuelle ordren.  
2. Velg handlingen **Statistikk**.  
3. Velg hurtigfanen **Fakturering**.  
  
    > [!NOTE]  
    >  Det totale mva-beløpet for fakturaen, gruppert etter mva-type, vises på linjene. Du kan justere beløpet manuelt i **Mva-beløp**-feltet på linjene for hver mva-type. Når du endrer **Mva-beløp**-feltet, kontrolleres det at du ikke har endret mva med mer enn beløpet du har angitt som tillatt maksimumsdifferanse. Hvis beløpet er utenfor området for **Maks. tillatte mva-differanse**, vises det en advarsel som angir den maksimale differansen som er tillatt. Du kan ikke fortsette før beløpet er justert innenfor de godkjente parametrene. Klikk **OK** og angi et annet **mva-beløp** som er innenfor det tillatte området. Hvis mva-differansen er lik eller lavere enn tillatt maksimum, deles mva proporsjonelt mellom dokumentlinjene som har samme mva-type.  

## <a name="calculating-vat-manually-using-journals"></a>Beregne mva manuelt ved hjelp av kladder  
Du kan også justere mva-beløper i finanskladder, salgskladder og kjøpskladder. Dette kan for eksempel være nødvendig når du angir en leverandørfaktura i kladden og det er en differanse mellom mva-beløpet som er beregnet i [!INCLUDE[d365fin](includes/d365fin_md.md)], og mva-beløpet på leverandørfakturaen du har mottatt.  

#### <a name="before-you-manually-enter-vat-on-a-general-journal"></a>Før du angir mva manuelt i en finanskladd  
1. På siden **Finansoppsett** angir du **Maks. tillatte mva-differanse** mellom beløpet som beregnes i programmet, og det manuelle beløpet.  
2. På siden **Finanskladdemaler** merker du av for **Tillat mva-differanse** for den relevante kladden.  

#### <a name="before-you-manually-enter-vat-on-sales-and-purchase-journals"></a>Før du kan angi mva manuelt i salgs- og kjøpskladder  
1. På siden **Kjøpsoppsett** merker du av for **Tillat mva-differanse**.  
2. Når du har fullført oppsettet som er beskrevet ovenfor, kan du justere **Mva-beløp**-feltet på finanskladdelinjen, eller feltet **Motkonto-mva. - beløp** på salgs- eller kjøpskladdelinjen. [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerer at differansen ikke er større enn den tillatte maksimumsdifferansen.  
  
    > [!NOTE]  
    > Hvis differansen er større, vises en advarsel som angir maksimalt differansen som er tillatt. Hvis du vil fortsette, må du justere beløpet. Velg **OK** og angi deretter et beløp som er innenfor det tillatte området. Hvis mva-differansen er lik eller lavere enn tillatt maksimumsdifferanse, viser [!INCLUDE[d365fin](includes/d365fin_md.md)] differansen i feltet **Mva-differanse**.  

## <a name="to-post-import-vat-with-purchase-invoices"></a>Slik bokfører du import-mva med kjøpsfakturaer
I stedet for å bruke en kladd til å bokføre en viktig mva-faktura, kan du bruke en kjøpsfaktura.  

### <a name="to-set-up-purchasing-for-posting-import-vat-invoices"></a>Slik definerer du kjøp for bokføring av fakturaer med import-mva.:  
1. Opprett et leverandørkort for importmyndigheten som sender deg fakturaen for import-mva. **Bokføringsgruppe - firma** og **Mva-bokføringsgruppe - firma** må være definert på samme måte som finanskontoen for import-mva.  
2. Opprett en **Bokføringsgruppe - vare** for import-mva, og definer en **Std. mva-bokf.gruppe - vare** for import-mva for den tilknyttede **Bokføringsgruppe - vare**.  
3. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kontoplan**, og velg deretter den relaterte koblingen.  
4. Velg finanskontoen for import-mva og velg deretter **Rediger** under **Behandle** i fanebladet **Hjem**.  
5. På hurtigfanen **Bokføring** velger du oppsettet **Bokføringsgruppe \- vare** for import-mva . [!INCLUDE[d365fin](includes/d365fin_md.md)] fyller automatisk i feltet **Mva\-bokføringsgruppe \- vare**.  
6. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Generelt bokføringsoppsett**, og velg deretter den relaterte koblingen.  
7. Opprett en kombinasjon av **Bokføringsgruppe - firma** for mva-myndighetene og **Bokføringsgruppe - vare** for import-mva.. For denne nye kombinasjonen velger du finanskontoen for import-mva i **Innkjøpskonto**-feltet.  

### <a name="to-create-a-new-invoice-for-the-import-authority-vendor-once-you-have-completed-the-setup"></a>Slik oppretter du en ny faktura for importmyndighetsleverandøren når du har fullført oppsettet  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.  
2. Opprett en ny kjøpsfaktura.  
3. I feltet **Kjøp fra-leverandørnr.** velger du importmyndighetsleverandøren, og velger deretter **OK**-knappen.  
4. I feltet **Type** på bestillingslinjen velger du **Finanskonto**, og i feltet **Nr.** velger du Importer mva-finanskontoen.  
5. Skriv inn **1** i **Antall**-feltet.  
6. Angi mva-beløpet i feltet **Direkte enhetskost eks. mva**.  
7. Bokfør fakturaen.  

## <a name="to-process-certificates-of-supply"></a>Slik behandler du leveringsbekreftelser
Når du selger varer til en kunde i et annet EU-land, må du sende kunden en leveringsbekreftelse som kunden må signere og returnere til deg. Følgende prosedyrer er for behandling av leveringsbekreftelser for følgesedler, men de samme trinnene gjelder for servicefølgesedler for varer og returforsendelser til leverandører.  

### <a name="to-view-certificate-of-supply-details"></a>Slik viser du detaljer om leveringsbekreftelser  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokførte følgesedler**, og velg deretter den relaterte koblingen.  
2. Velg den aktuelle følgeseddelen til en kunde i et annet EU-land eller en annen EU-region.  
3. Velg **Detaljer om mottaksdeklarasjon**.  
4. Hvis det er merket av for **Leveringsbekreftelse er obligatorisk** for mva-bokføringsgruppedefinisjonen som er konfigurert for kunden, er som standard **Obligatorisk** angitt i **Status**-feltet. Du kan oppdatere feltet for å angi om kunden har returnert bekreftelsen.  

    > [!Note]  
    >  Hvis det ikke er merket av for **Leveringsbekreftelse er obligatorisk** i mva-bokføringsgruppedefinisjonen, opprettes det en post, og **Ikke i bruk** angis i **Status**-feltet. Du kan oppdatere feltet for å gjenspeile den riktige statusinformasjonen. Du kan manuelt endre statusen fra **Ikke i bruk** til **Påkrevd** og fra **Påkrevd** til **Ikke i bruk** etter behov.  

   Når du oppdaterer **Status**-feltet til **Påkrevet**, **Mottatt** eller **Ikke mottatt**, opprettes det en bekreftelse.  
  
    > [!TIP]  
    >  Du kan bruke **Leveringsbekreftelser**-siden for å få en oversikt over statusen for alle bokførte leveringer som det er opprettet en leveringsbekreftelse for.  

5. Velg **Skriv ut mottaksdeklarasjon**.  
  
    > [!Note]  
    >  Du kan forhåndsvise eller skrive ut dokumentet. Når du velger **Skriv ut leveringsbekreftelse** og skriver ut dokumentet, blir det merket av for **Skrevet ut** automatisk. Hvis den ikke allerede er angitt, oppdateres statusen for bekreftelsen til **Påkrevd**. Om nødvendig inkluderer du den utskrevne bekreftelsen med leveringen.  

### <a name="to-print-a-certificate-of-supply"></a>Slik skriver du ut en leveringsbekreftelse  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokførte følgesedler**, og velg deretter den relaterte koblingen.  
2. Velg den aktuelle følgeseddelen til en kunde i et annet EU-land eller en annen EU-region.  
3. Velg **Skriv ut mottaksdeklarasjon**.  

    > [!NOTE]  
    >  Alternativt kan du skrive ut et sertifikat fra siden **Mottaksdeklarasjon**.  

4. Hvis du vil inkludere informasjon fra linjene i leveringsdokumentet i bekreftelsen, kan du merke av for **Skriv ut linjedetaljer**.  
5. Merk av for **Opprett mottaksdeklarasjoner hvis de ikke allerede er opprettet** hvis du vil at [!INCLUDE[d365fin](includes/d365fin_md.md)] skal opprette bekreftelser for bokførte følgesedler som ikke har slike ved kjøring. Når du merker av for dette alternativet, opprettes nye bekreftelser for alle bokførte følgesedler som ikke har bekreftelser i det merkede området.  
6. Filterinnstillingene er som standard for følgeseddelen du har valgt. Fyll ut filterinformasjonen for å velge en bestemt leveringsbekreftelse du vil skrive ut.  
7. Velg **Skriv ut** på siden **Mottaksdeklarasjon** for å skrive ut rapporten, eller velg **Forhåndsvisning** for å vise den på skjermen.  

    > [!Note]  
    > Feltet **Status for mottaksdeklarasjon** og feltet **Skrevet ut** er oppdatert for leveringen på siden **Leveringsbekreftelser**.  

8. Send den utskrevne leveringsbekreftelsen til kunden for signatur.  

### <a name="to-update-the-status-of-a-certificate-of-supply-for-a-shipment"></a>Oppdatere statusen til en leveringsbekreftelse for en levering  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokførte følgesedler**, og velg deretter den relaterte koblingen.  
2. Velg den aktuelle følgeseddelen til en kunde i et annet EU-land eller en annen EU-region.  
3. Velg det aktuelle alternativet i feltet **Status**.  

   Hvis kunden har returnert den signerte leveringsbekreftelsen, velger du **Mottatt**. **Mottaksdato**-feltet er oppdatert. Gjeldende arbeidsdato er som standard angitt for mottaksdatoen.  

   Du kan endre datoen for å gjenspeile datoen da du mottok kundens signerte leveringsbekreftelse. Du kan også legge til en kobling til den signerte bekreftelsen ved hjelp av standard [!INCLUDE[d365fin](includes/d365fin_md.md)]\-kobling.  

   Hvis kunden ikke returnerer den signerte leveringsbekreftelsen, velger du **Ikke mottatt**. Du må deretter sende kunden en ny faktura som inkluderer mva., fordi den opprinnelige fakturaen ikke vil bli godtatt av skattemyndighetene.  

Hvis du vil vise en gruppe av bekreftelser, kan du starte fra **Leveringsbekreftelser**-siden og deretter oppdatere informasjon om status for utestående bekreftelser når du får dem tilbake fra kundene. Dette kan være nyttig når du vil søke etter alle bekreftelser som har en bestemt status, for eksempel **Påkrevd**, som du vil oppdatere til statusen **Ikke mottatt**.  

### <a name="to-update-the-status-of-a-group-of-certificates-of-supply"></a>Oppdatere statusen til en gruppe av leveringsbekreftelser  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Mottaksdeklarasjoner**, og velg deretter den relaterte koblingen.  
2. Filtrer **Status**-feltet til ønsket verdi for å opprette listen over bekreftelsene du vil håndtere.  
3. Hvis du vil oppdatere informasjon om status, velger du **Rediger oversikt**.  
4. Velg det aktuelle alternativet i feltet **Status**.  

   Hvis kunden har returnert den signerte leveringsbekreftelsen, velger du **Mottatt**. **Mottaksdato**-feltet er oppdatert. Gjeldende arbeidsdato er som standard angitt for mottaksdatoen.  

   Du kan endre datoen for å gjenspeile datoen da du mottok den signerte leveringsbekreftelsen. Du kan også legge til en kobling til den signerte bekreftelsen ved hjelp av standard [!INCLUDE[d365fin](includes/d365fin_md.md)]-dokumentkobling.  

    > [!NOTE]  
    >  Du kan ikke opprette en ny leveringsbekreftelse i **Leveringsbekreftelse**-siden når du går til det ved hjelp av denne fremgangsmåten. Hvis du vil opprette en bekreftelse for en levering som ikke er konfigurert for å kreve en, åpner du den bokførte følgeseddelen og bruker én av de to fremgangsmåtene som er beskrevet ovenfor:  
    >   
    > * Opprette en leveringsbekreftelse manuelt  
    > * Slik skriver du ut en leveringsbekreftelse.

## <a name="see-also"></a>Se også  
[Definere beregninger og bokføringsmetoder for merverdiavgift](finance-setup-vat.md)   
[Rapportere mva til skattemyndighetene](finance-how-report-vat.md)   
