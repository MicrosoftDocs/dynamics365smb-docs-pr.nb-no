---
title: Arbeid med mva. på kjøp og salg
description: 'Dette emnet beskriver de ulike måtene å arbeide med mva. både manuelt og med automatisk oppsett, slik at du kan overholde land-/områdespesifikke forskrifter.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'VAT, sales, purchases'
ms.search.form: '7, 118, 130, 142, 459, 460, 525'
ms.date: 06/16/2021
ms.author: bholtorf
---
# <a name="work-with-vat-on-sales-and-purchases"></a>Arbeid med mva. på kjøp og salg

Hvis landet eller området krever at du beregner og rapporterer merverdiavgift (mva.) i salgs- og kjøpstransaksjoner, kan du definere [!INCLUDE[prod_short](includes/prod_short.md)] for å beregne mva. Hvis du vil ha mer informasjon, kan du se [Definere beregninger og bokføringsmetoder for merverdiavgift](finance-setup-vat.md).

Det er imidlertid enkelte mva-relaterte oppgaver som du kan gjøre manuelt. For eksempel kan det hende du må korrigere et bokført beløpet hvis du oppdager at en leverandør bruker forskjellige Avrundingsmetode.  

> [!TIP]
> Du kan la [!INCLUDE[prod_short](includes/prod_short.md)] bekrefte organisasjonsnumre og andre selskapsopplysninger når du oppretter eller oppdaterer dokumenter. Hvis du vil ha mer informasjon, kan du se [Validering av organisasjonsnumre](finance-how-validate-vat-registration-number.md).

## <a name="calculating-and-displaying-vat-amounts-on-sales-and-purchase-documents"></a>Beregne og vise mva-beløp i salgs- og kjøpsdokumenter

Når du velger et varenummer i **Nr.**- feltet på et salgs- eller kjøpsdokument, fyller [!INCLUDE[prod_short](includes/prod_short.md)] ut feltene **Enhetspris** og **Linjebeløp**. Salgsprisen kommer fra **varekortet** eller fra salgsprisene som er tillatt for varen og kunden. [!INCLUDE[prod_short](includes/prod_short.md)] beregner linjebeløpet bare når du angir en mengde for linjen.  

Hvis du vil at enhetsprisene og linjebeløpene skal inkludere mva., for eksempel hvis du selger til detaljhandelsforbrukere, merker du av for **Priser inkl. mva.** i dokumentet. Hvis du vil ha mer informasjon, kan du se [Inkluder eller ekskluderv mva. i priser og linjebeløp](#including-or-excluding-vat-in-prices-and-line-amounts). 

Du kan beregne og vise mva-beløp i salgs- og kjøpsdokumenter på forskjellig måte, avhengig av hvilken type kunde eller leverandør du handler med. Du kan også endre det beregnede mva-beløpet manuelt, slik at det for eksempel samsvarer mva-beløpet beregnet av leverandøren på en gitt transaksjon.

### <a name="including-or-excluding-vat-in-prices-and-line-amounts"></a>Inkluder eller ekskluder mva. i priser og linjebeløp

Hvis du merker av for **Priser inkl. mva.** i et salgsdokument, oppdateres feltene **Enhetspris** og **Linjebeløp** slik at de inkluderer mva. Som standard er ikke mva. inkludert i disse feltene. Navnene på feltene gjenspeiler om priser er inkludert mva.  

Du kan definere standardinnstillingen for **Priser inkl. mva** for alle salgsdokumenter for en kunde i feltet **Priser inkl. mva.** på **Kunde**-kortet. Du kan også definere at salgspriser skal ha med mva eller ikke. Vanligvis vil priser på varekortet ekskludere mva. 

Tabellen nedenfor inneholder en oversikt over hvordan salgsprisbeløpene beregnes for et salgsdokument når du ikke har definert priser på **Salgspris**-siden:  

|**Feltet Pris inkl. mva. på varekortet**|**Priser inkl. mva.-felt**|**Utført handling**|  
|-----------------------------------------------|----------------------------------------------------|--------------------------|  
|Ikke aktivert|Ikke aktivert|**Salgsprisen** på varekortet kopieres til feltet **Salgspris Ekskl. mva.** på salgslinjene.|  
|Ikke aktivert|Aktivert|Mva-beløpet per enhet beregnes og legges til i **enhetsprisen** på varekortet. Den totale enhetsprisen angis deretter i feltet **Enhetspris inkl. mva.** på salgslinjene.|  
|Aktivert|Ikke aktivert|Mva-beløpet i **Enhetspris**-feltet på **varekortet** beregnes ved hjelp av mva-prosenten som er knyttet til kombinasjonen av mva-bokføringsgruppe for firma (pris) og mva-bokføringsgruppe for vare. **Salgsprisen** på varekortet, redusert med mva-beløpet, angis deretter i feltet **Salgspris Ekskl. mva.** på salgslinjene. Hvis du vil ha mer informasjon, kan du se [Bruk mva-bokføringsgrupper for firma og kundeprisgrupper](finance-work-with-vat.md#using-vat-business-posting-groups-and-customer-price-groups).|  
|Aktivert|Aktivert|**Salgsprisen** på varekortet kopieres til feltet **Salgspris Inkl. mva.** på salgslinjene.|

#### <a name="using-vat-business-posting-groups-and-customer-price-groups"></a>Bruk mva-bokføringsgrupper for firma og kundeprisgrupper

Hvis du vil at priser skal inkludere mva., kan du bruke mva-bokføringsgrupper for firma til å beregne beløpet på bakgrunn av mva-bokføringsoppsettet for gruppen. Hvis du vil ha mer informasjon, kan du se [Definer mva-bokføringsgrupper](finance-setup-vat.md#set-up-vat-business-posting-groups).

Avhengig av hva du vil gjøre, kan du tildele en mva-bokføringsgruppe for firma til kunder eller salgsdokumenter på følgende måter:

* Hvis du vil bruke samme mva-sats for alle kunder, kan du velge en gruppe i feltet **Mva-bokføringsgruppe for firma (pris)** på siden **Salgsoppsett**.
* Hvis du vil bruke en mva-sats for en bestemt kunde, kan du velge en gruppe i feltet **Mva-bokføringsgruppe for firma (pris)** på siden **Kundekort**. 
* Hvis du vil bruke en mva-sats for en bestemt kunde, kan du velge en gruppe i feltet **Mva-bokføringsgruppe for firma (pris)** på siden **Kundeprisgruppe**. Dette er for eksempel nyttig når du vil at en pris skal gjelde alle kunder i et bestemt geografisk område eller en bestemt bransje.
* For alle salgsdokumenter i feltet **Mva-bokføringsgruppe for firma**. Mva-beløpet som er angitt for gruppen, brukes bare for det dokumentet du arbeider på nå.

> [!NOTE]
> Hvis du ikke angir en gruppe i feltet **Mva-bokføringsgruppe for firma (pris)**, er ikke mva. inkludert i priser.

#### <a name="examples"></a>Eksempler

Faktorer som landet eller området du selger til, eller bransjetypen du selger til, kan påvirke det mva-beløpet du må ta med i beregningen. En restaurant kan for eksempel ta 6 % mva for måltider som spise inne, og 17 % for takeaway. For å gjøre det må du opprette en mva-bokføringsgruppe for firma (pris) for internt og en for takeaway.

## <a name="working-with-vat-date"></a>Arbeid med mva-dato

### <a name="vat-date-in-documents"></a>Mva-dato i dokumenter

Når du oppretter nye salgs- eller kjøpsdokumenter, er **mva-datoen** være basert på innstillingen i feltet **Standard mva-dato** på siden **Finansoppsett**. Denne standardverdien kan være den samme som **bokføringsdato** eller **dokumentdato**. Hvis du trenger en annen mva-dato, kan du endre verdien i feltet **Mva-dato** manuelt. Når du bokfører dokumentet, vises **mva-datoen** i bokføringsdokumentet og på mva- og finansposter.

> [!NOTE]
> Hvis feltet **Mva-dato** ikke er tilgjengelig i dokumentene eller kladdene, betyr det at **Ikke bruk mva-datofunksjonalitet** er valgt i feltet **Mva-datobruk** på siden **Finansoppsett**.  

> [!IMPORTANT]
> Hvis du konfigurerer **Kontroller mva-periode** i **Finansoppsettet** som **Blokker bokføring innenfor lukket periode** eller **Blokker bokføring innenfor lukket og varsle for frigitt periode**, kan du bare bokføre dokument eller kladd hvis datoen i feltet **Mva-dato** ikke er i en lukket periode i **Mva-returperioder**. Selv om perioden i **Mva-returperioder** er åpen, kan du få en advarsel basert på **mva-returstatus** og konfigurasjon i **Kontroller mva-periode**.

> [!IMPORTANT]
> Du kan forhindre eller tillate bokføring av **mva-datoen** for et bestemt dataområde ved hjelp av feltene **Tillat bokføring fra** og **Tillat bokføring til** i **Finansoppsett** og i **Brukeroppsett**.  

> [!NOTE]
> Hvis du lar **mva-datoen** være tom, bruker [!INCLUDE [prod_short](includes/prod_short.md)] standardoppsettet fra **Standard mva-dato** i **Finansoppsettet** som en **mva-dato** i den bokførte transaksjonen.  

### <a name="modifying-the-vat-date-in-posted-entries"></a>Endre mva-dato i bokførte poster

Om nødvendig kan du endremva-datoen for bokførte dokumenter. Hvis du vil endre datoen i feltet **Mva-dato** for bokførte dokumenter, må du følge denne fremgangsmåten:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Mva-poster** og velger deretter den relaterte koblingen. 
2. Finn posten med feil mva-dato.  
3. Velg handlingen **Rediger liste**, og angi riktig dato i feltet **Mva-dato**.  
4. Når du lukker siden, endres mva-datoen i relaterte **finansposter** og i det bokførte dokumentet.  

> [!NOTE]
> Du kan bare endre feltet **Mva-dato** i **mva-poster** hvis gjeldende dato ikke befinner seg i en lukket mva-returperiode. Selv om perioden i feltet **Mva-returperioder** er åpen, kan du få en advarsel basert på **mva-returstatus**.  

> [!NOTE]
> Hvis dokumentet har mer enn én **mva-post**, trenger du bare å endre verdien i feltet **Mva-dato** i én post som er knyttet til dokumentet. For å holde poster konsekvente endrer [!INCLUDE[prod_short](includes/prod_short.md)] automatisk mva-datoen i mva-poster som er knyttet til denne transaksjonen. [!INCLUDE [prod_short](includes/prod_short.md)] oppdaterer **mva-datoen** i andre tabeller (finansposter og dokumenter), men bare knyttet til denne transaksjonen.  

## <a name="correcting-vat-amounts-manually-on-sales-and-purchase-documents"></a>Korrigere mva-beløp manuelt i salgs- og kjøpsdokumenter

Du kan korrigere mva-poster som er bokført slik at du kan endre de samlede inngående eller utgående mva-beløpene uten å endre mva-basen. Hvis du for eksempel mottar en faktura fra en leverandør med feil mva-beløp.  

Selv om du kan ha satt opp én eller flere kombinasjoner for å håndtere import-mva, må du definere minst én mva-produktbokføringsgruppe. Du kan for eksempel kalle den **KORRIGER** og bruke den til korreksjonsformål, med mindre du kan bruke den samme finanskontoen i feltet **Inngående mva-konto** på linjen for mva-bokføringsoppsett. Hvis du vil ha mer informasjon, kan du se [Definere beregninger og bokføringsmetoder for merverdiavgift](finance-setup-vat.md).

Når kontantrabatten er tildelt, kan du tilbakestille den delen av kontantrabatten som gjelder mva-beløpet hvis det er beregnet en kontantrabatt på bakgrunn av et fakturabeløp med mva. Merk at du må aktivere feltet **Juster for kontantrabatt** både i finansoppsettet generelt og i mva-bokføringsoppsettet for en bestemt kombinasjon av mva-firmabokføringsgrupper og mva-varebokføringsgrupper.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-sales-documents"></a>Slik oppretter du et system for manuell mva-post i salgsdokumenter
Nedenfor ser du hvordan du aktiverer manuelle mva-endringer på salgsdokumenter. Trinnene ligner på siden **Kjøpsoppsett**.

1. På siden **Finansoppsett** angir du **Maks. tillatte mva-differanse** mellom beløpet som beregnes i programmet, og det manuelle beløpet.  
2. Merk av for **Tillat mva-differanse** på siden **Salgsoppsett**.  

### <a name="to-adjust-vat-for-a-sales-document"></a>Slik justerer du mva for et salgsdokument

1. Åpne den aktuelle ordren.  
2. Velg handlingen **Statistikk**.  
3. På hurtigfanen **Fakturering** velger du verdien i feltet **Ant. mva-linjer**.
4. Rediger **mva-beløp**-feltet.   

> [!NOTE]  
> Det totale mva-beløpet for fakturaen, gruppert etter mva-type, vises på linjene. Du kan justere beløpet manuelt i **Mva-beløp**-feltet på linjene for hver mva-type. Når du endrer **Mva-beløp**-feltet, kontrolleres det at du ikke har endret mva med mer enn beløpet du har angitt som tillatt maksimumsdifferanse. Hvis beløpet er utenfor området for **Maks. tillatte mva-differanse**, vises det en advarsel som angir den maksimale differansen som er tillatt. Du kan ikke fortsette før beløpet er justert innenfor de godkjente parametrene. Klikk **OK** og angi et annet **mva-beløp** som er innenfor det tillatte området. Hvis mva-differansen er lik eller lavere enn tillatt maksimum, deles mva proporsjonelt mellom dokumentlinjene som har samme mva-type.  

## <a name="calculating-vat-manually-using-journals"></a>Beregne mva manuelt ved hjelp av kladder
Du kan også justere mva-beløper i finanskladder, salgskladder og kjøpskladder. Dette kan for eksempel være nødvendig når du angir en leverandørfaktura i kladden og det er en differanse mellom mva-beløpet som er beregnet i [!INCLUDE[prod_short](includes/prod_short.md)], og mva-beløpet på leverandørfakturaen du har mottatt.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-a-general-journals"></a>Slik konfigurerer du systemet for manuell mva-post i en finanskladd.
Du må utføre følgende trinn før du angir mva manuelt i en finanskladd.  

1. På siden **Finansoppsett** angir du **Maks. tillatte mva-differanse** mellom beløpet som beregnes i programmet, og det manuelle beløpet.  
2. På siden **Finanskladdemaler** merker du av for **Tillat mva-differanse** for den relevante kladden.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-a-sales-and-purchase-journals"></a>Slik konfigurerer du systemet for manuell mva-post i salgs- og kjøpskladder

Du må utføre følgende trinn før du angir mva manuelt i en salgs- eller kjøpskladd.

1. På siden **Kjøpsoppsett** merker du av for **Tillat mva-differanse**.  
2. Gjenta trinn 1 for siden **Salgsoppsett**.
3. Når du har fullført oppsettet som er beskrevet ovenfor, kan du justere **Mva-beløp**-feltet på finanskladdelinjen, eller feltet **Motkonto-mva. - beløp** på salgs- eller kjøpskladdelinjen. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer at differansen ikke er større enn den tillatte maksimumsdifferansen.  

> [!NOTE]  
> Hvis differansen er større, vises en advarsel som angir maksimalt differansen som er tillatt. Hvis du vil fortsette, må du justere beløpet. Velg **OK** og angi deretter et beløp som er innenfor det tillatte området. Hvis mva-differansen er lik eller lavere enn tillatt maksimumsdifferanse, viser [!INCLUDE[prod_short](includes/prod_short.md)] differansen i feltet **Mva-differanse**.  

## <a name="posting-import-vat-with-purchase-invoices"></a>Bokføre import-mva med kjøpsfakturaer
I stedet for å bruke kladder til å bokføre en viktig mva-faktura, kan du bruke en kjøpsfaktura.  

### <a name="to-set-up-purchasing-for-posting-import-vat-invoices"></a>Slik definerer du kjøp for bokføring av fakturaer med import-mva.:

1. Opprett et leverandørkort for importmyndigheten som sender deg fakturaen for import-mva. **Bokføringsgruppe - firma** og **Mva-bokføringsgruppe - firma** må være definert på samme måte som finanskontoen for import-mva.  
2. Opprett en **Bokføringsgruppe - vare** for import-mva, og definer en **Std. mva-bokf.gruppe - vare** for import-mva for den tilknyttede **Bokføringsgruppe - vare**.  
3. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kontoplan** og velger deretter den relaterte koblingen.  
4. Velg finanskontoen for import-mva, og velg deretter **Rediger**-handlingen.  
5. På hurtigfanen **Bokføring** velger du oppsettet **Bokføringsgruppe \- vare** for import-mva . [!INCLUDE[prod_short](includes/prod_short.md)] fyller automatisk i feltet **Mva\-bokføringsgruppe \- vare**.  
6. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Generelt bokføringsoppsett**, og velg deretter den relaterte koblingen.  
7. Opprett en kombinasjon av **Bokføringsgruppe - firma** for mva-myndighetene og **Bokføringsgruppe - vare** for import-mva.. For denne nye kombinasjonen velger du finanskontoen for import-mva i **Innkjøpskonto**-feltet.  

### <a name="to-create-a-new-invoice-for-the-import-authority-vendor-once-you-have-completed-the-setup"></a>Slik oppretter du en ny faktura for importmyndighetsleverandøren når du har fullført oppsettet

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.  
2. Opprett en ny kjøpsfaktura.  
3. I feltet **Kjøp fra-leverandørnr.** velger du importmyndighetsleverandøren, og velger deretter **OK**-knappen.  
4. I feltet **Type** på bestillingslinjen velger du **Finanskonto**, og i feltet **Nr.** velger du Importer mva-finanskontoen.  
5. Skriv inn **1** i **Antall**-feltet.  
6. Angi mva-beløpet i feltet **Direkte enhetskost eks. mva**.  
7. Bokfør fakturaen.  

## <a name="processing-certificates-of-supply"></a>Behandle leveringsbekreftelser

Når du selger varer til en kunde i et annet EU-land, må du sende kunden en leveringsbekreftelse som kunden må signere og returnere til deg. Følgende prosedyrer er for behandling av leveringsbekreftelser for følgesedler, men de samme trinnene gjelder for servicefølgesedler for varer og returforsendelser til leverandører.  

### <a name="to-view-certificate-of-supply-details"></a>Slik viser du detaljer om leveringsbekreftelser
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bokførte salgsforsendelser**, og velg deretter den relaterte koblingen.  
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

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bokførte salgsforsendelser**, og velg deretter den relaterte koblingen.  
2. Velg den aktuelle følgeseddelen til en kunde i et annet EU-land eller en annen EU-region.  
3. Velg **Skriv ut mottaksdeklarasjon**.  

> [!NOTE]  
>  Alternativt kan du skrive ut et sertifikat fra siden **Mottaksdeklarasjon**.  

4. Hvis du vil inkludere informasjon fra linjene i leveringsdokumentet i bekreftelsen, kan du merke av for **Skriv ut linjedetaljer**.  
5. Merk av for **Opprett mottaksdeklarasjoner hvis de ikke allerede er opprettet** hvis du vil at [!INCLUDE[prod_short](includes/prod_short.md)] skal opprette bekreftelser for bokførte følgesedler som ikke har slike ved kjøring. Når du merker av for dette alternativet, opprettes nye bekreftelser for alle bokførte følgesedler som ikke har bekreftelser i det merkede området.  
6. Filterinnstillingene er som standard for følgeseddelen du har valgt. Fyll ut filterinformasjonen for å velge en bestemt leveringsbekreftelse du vil skrive ut.  
7. Velg **Skriv ut** på siden **Mottaksdeklarasjon** for å skrive ut rapporten, eller velg **Forhåndsvisning** for å vise den på skjermen.  

> [!Note]  
> Feltet **Status for mottaksdeklarasjon** og feltet **Skrevet ut** er oppdatert for leveringen på siden **Leveringsbekreftelser**.  

8. Send den utskrevne leveringsbekreftelsen til kunden for signatur.  

### <a name="to-update-the-status-of-a-certificate-of-supply-for-a-shipment"></a>Oppdatere statusen til en leveringsbekreftelse for en levering

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bokførte salgsforsendelser**, og velg deretter den relaterte koblingen.  
2. Velg den aktuelle følgeseddelen til en kunde i et annet EU-land eller en annen EU-region.  
3. Velg det aktuelle alternativet i feltet **Status**.  

   Hvis kunden har returnert den signerte leveringsbekreftelsen, velger du **Mottatt**. **Mottaksdato**-feltet er oppdatert. Gjeldende arbeidsdato er som standard angitt for mottaksdatoen.  

   Du kan endre datoen for å gjenspeile datoen da du mottok kundens signerte leveringsbekreftelse. Du kan også legge til en kobling til den signerte bekreftelsen ved hjelp av standard [!INCLUDE[prod_short](includes/prod_short.md)]-kobling.  

   Hvis kunden ikke returnerer den signerte leveringsbekreftelsen, velger du **Ikke mottatt**. Du må deretter sende kunden en ny faktura som inkluderer mva., fordi den opprinnelige fakturaen ikke vil bli godtatt av skattemyndighetene.  

Hvis du vil vise en gruppe av bekreftelser, kan du starte fra **Leveringsbekreftelser**-siden og deretter oppdatere informasjon om status for utestående bekreftelser når du får dem tilbake fra kundene. Dette kan være nyttig når du vil søke etter alle bekreftelser som har en bestemt status, for eksempel **Påkrevd**, som du vil oppdatere til statusen **Ikke mottatt**.  

### <a name="to-update-the-status-of-a-group-of-certificates-of-supply"></a>Oppdatere statusen til en gruppe av leveringsbekreftelser

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Mottaksdeklarasjoner** og velg den relaterte koblingen.  
2. Filtrer **Status**-feltet til ønsket verdi for å opprette listen over bekreftelsene du vil håndtere.  
3. Hvis du vil oppdatere informasjon om status, velger du **Rediger oversikt**.  
4. Velg det aktuelle alternativet i feltet **Status**.  

   Hvis kunden har returnert den signerte leveringsbekreftelsen, velger du **Mottatt**. **Mottaksdato**-feltet er oppdatert. Gjeldende arbeidsdato er som standard angitt for mottaksdatoen.  

   Du kan endre datoen for å gjenspeile datoen da du mottok den signerte leveringsbekreftelsen. Du kan også legge til en kobling til den signerte bekreftelsen ved hjelp av standard [!INCLUDE[prod_short](includes/prod_short.md)]-dokumentkobling.  

> [!NOTE]
> Du kan ikke opprette en ny leveringsbekreftelse i **Leveringsbekreftelse**-siden når du går til det ved hjelp av denne fremgangsmåten. Hvis du vil opprette en bekreftelse for en levering som ikke er konfigurert for å kreve en, åpner du den bokførte følgeseddelen og bruker én av de to fremgangsmåtene som er beskrevet ovenfor:  
>
> * Opprette en leveringsbekreftelse manuelt  
> * Slik skriver du ut en leveringsbekreftelse.

## <a name="see-also"></a>Se også

[Definere beregninger og bokføringsmetoder for merverdiavgift](finance-setup-vat.md)  
[Rapportere mva til skattemyndighetene](finance-how-report-vat.md)  
[Validere et organisasjonsnummer](finance-how-validate-vat-registration-number.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
