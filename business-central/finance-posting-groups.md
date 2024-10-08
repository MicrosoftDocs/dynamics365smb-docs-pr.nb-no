---
title: Konfigurasjon av bokføringsgruppe
description: Finn ut hvordan du bruker bokføringsgrupper for å spare tid og unngå feil når du bokfører transaksjoner.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'posting setup, initialize'
ms.search.form: '312, 313'
ms.date: 08/13/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="set-up-posting-groups"></a>Konfigurer bokføringsgrupper

Bokføringsgrupper tildeler enheter til finanskontoer. Eksempler på enheter er kunder, leverandører, varer, ressurser og salgs- og kjøpsdokumenter. Bokføringsgrupper sparer tid og unngår feil når du bokfører transaksjoner. Transaksjonsverdiene går til kontiene som er angitt i bokføringsgruppen for den bestemte enheten. Det eneste kravet er at du har en kontoplan. Hvis du vil ha mer informasjon, kan du se [Definere kontoplanen](finance-setup-chart-accounts.md).  

Bokføringsgruppene er dekket av tre paraplyer:  

* Generelt

  Definere hvem du selger til og kjøpe fra, og hva du selger og hva du kjøper. Du kan også slå sammen grupper for å angi ting som resultatkontiene bokføres til, eller du kan bruke grupper til å filtrere rapporter.  
* Serienummer

  Bruk salgsdokumenter, i stedet for å bokføre direkte til Finans. Når du oppretter poster i finans, sikrer bokføringsgruppene at tilsvarende poster opprettes i Finans.  
* Avgift

  Definer mva-prosent og beregningstyper som gjelder hvem du selger til og kjøpe fra, og hva du selger og hva du kjøper.

De følgende delene beskriver bokføringsgruppene under hver paraply.  

## <a name="general-posting-groups"></a>Generelle bokføringsgrupper

De følgende tabellene beskriver de generelle bokføringsgruppene.

| Type | Beskrivelse |
| --- | --- |
| Bokføringsgruppe - firma |Tilordne denne gruppen til kunder og leverandører for å angi hvem du selger til, og som du kjøper fra. Definer disse bokføringsgruppene på siden **Bokføringsgrupper – firma**. Når du gjør det, må du tenke på hvor mange grupper du trenger for å bryte ned kjøp og salg. Hvis du for eksempel gruppere kunder og leverandører etter geografisk område, eller ved type virksomhet. |
| Bokføringsgruppe - vare |Tilordne denne gruppen til varer og ressurser til å angi hva du selger, og hva du kjøper. Definer disse bokføringsgruppene på siden **Bokføringsgrupper – vare**. Når du gjør det, bør du vurdere hvor mange grupper du trenger for å bryte ned salg etter produkt (varer og ressurser) og kjøp av varer. Hvis du for eksempel del disse gruppene av råvarer, detaljhandel, ressurser, kapasitet og så videre. |
| Generelle bokføringsoppsett |Kombiner firma- og varebokføringsgrupper, og velg kontoene det skal posteres til. For hver kombinasjon av bokføringsgrupper for firma og vare kan du tilordne et sett med finanskontoer. Du kan eksempel bokføre salget av samme vare til ulike finanskontoer fordi kunder er tildelt til ulike bokføringsgrupper for firma. Definer disse konfigurasjonene på siden **Generelt bokføringsoppsett**. |

## <a name="specific-posting-groups"></a>Spesifikke bokføringsgrupper

Tabellen nedenfor beskriver bokføringsgruppene som er angitt til datatypene.

|Type | Beskrivelse |
| --- | --- |
| Bokføringsgrupper - kunde |Definere konti som skal brukes når du bokfører transaksjoner for kortsiktige fordringer. Hvis du bruker lager med kundekonto, fastsettes hvilke kontoer salgsordrelinjene bokføres til, av den generelle bokføringsgruppen for firma som er tilordnet kunden, og den generelle bokføringsgruppen for vare som er tilordnet lagervaren. Se *Bokføringsgrupper – firma* og *Bokføringsgrupper – vare* under delen [Generelle bokføringsgrupper](#general-posting-groups). Definer disse bokføringsgruppene på siden **Bokføringsgrupper – kunde**. |
| Bokføringsgrupper - leverandør |Definere hvor du vil bokføre transaksjoner for leverandørkonto, gebyr og kontantrabattkontiene. Dette ligner på kundebokføringsgrupper. Definer disse bokføringsgruppene på siden **Bokføringsgrupper – leverandør**. |
| Bokføringsgrupper - lager |Definer lagerbokføringsgrupper, som du deretter tilordner til relevante varekontor på siden **Lagerbokføringsoppsett**. Hvis du gjør dette når du bokfører poster som er knyttet til en vare, utføres det en bokføring i finanskontoen som er opprettet for kombinasjonen av lagerbokføringsgruppe og lokasjon som er knyttet til varen. Bokføringsgrupper for lager gir også et godt utgangspunkt for organisering av lageret, slik at du kan skille varer ved hjelp av bokføringsgruppene når du genererer rapporter. Definer disse bokføringsgruppene på siden **Bokføringsgrupper – lager**. |
| Bokføringsgrupper - bank |Definer finanskontiene som bankkontooppføringene bokføres til. Dette kan for eksempel forenkle prosessene i transaksjonssporing og avstemming av bankkontoer. Definer disse bokføringsgruppene på siden **Bokføringsgrupper – bank**. Vi anbefaler at disse finanskontiene har feltet **Direkte bokføring** satt til *Nei*. |
| Bokføringsgrupper - aktiva |Definer kontoer for diverse typer utgifter og kostnader, for eksempel anskaffelseskost, akkumulerte avskrivningsbeløp, anskaffelseskost ved salg, akkumulert avskrivning ved salg, vinning ved salg, tap ved salg, vedlikeholdsutgifter og avskrivningsutgifter. Definer disse bokføringsgruppene på siden **Bokføringsgrupper – aktiva**. |

### <a name="allow-substitute-customer-or-vendor-posting-groups-on-documents"></a>Tillat erstatning av kunde- eller leverandørbokføringsgrupper i dokumenter

Du kan la andre velge andre kunde- og leverandørbokføringsgrupper enn standardgruppene når de arbeider med salgs- eller kjøpsdokumenter og -kladder.

Hvis du vil tillate endringer i bokføringsgrupper for kunde, velger du **Tillat flere bokføringsgrupper** på sidene **Salgsoppsett** og **Serviceoppsett**, og siden **Kjøpsoppsett** for endringer i bokføringsgruppe for leverandør.

På sidene **Bokføringsgrupper – kunde** eller **Bokføringsgrupper – leverandør** kan du angi bokføringsgruppene som skal tillates, som erstatninger ved å velge **Erstatninger**. Ved å erstatte bokføringsgrupper kan du erstatte standard kunde- eller leverandørbokføringsgrupper som er angitt for en kunde eller leverandør.

Når du har definert dette, kan du velge blant de tillatte erstatningsbokføringsgruppene og endre kunde- eller leverandørbokføringsgruppen når du bokfører salgs- eller kjøpsdokumenter og -kladder. De erstattende kunde- eller leverandørbokføringsgruppene kopieres til bokførte dokumenter og kladder, og finansposter bokføres til finanskontoene som er angitt for erstatninger.

Når det gjelder for eksempel en faktura og betaling som bokføres med ulike kunde- eller leverandørbokføringsgrupper (ulike finanskontoer), overfører [!INCLUDE[prod_short](includes/prod_short.md)] beløpene mellom finanskontoene slik at de kan balanseres.

## <a name="tax-posting-groups"></a>Avgiftsbokføringsgrupper

De følgende tabellene beskriver de avgiftsrelaterte bokføringsgruppene.

| Type | Beskrivelse |
| --- | --- |
| Mva-bokføringsgrupper - firma |Finn ut hvordan du kan beregne og postere merverdiavgift for kunder og leverandører. Definer disse bokføringsgruppene på siden **Mva-bokføringsgrupper – firma**. Når du gjør, tenker på hvor mange grupper trenger du. Det kan for eksempel avhenge av faktorer som lokal lovgivning og om du handler både innen- og utenlands. |
| Mva-bokføringsgrupper - vare |Angi mva-beregninger som trengs for typen varer eller ressurser du kjøper eller selger. |
| Mva-bokføringsoppsett |Kombiner mva-bokføringsgrupper for bedrifter og mva-bokføringsgrupper for varer. Når du fyller ut en kladdelinje, bestillingslinje eller salgslinje, skal vi se på kombinasjon til å identifisere konti som skal brukes. |

Hvis landet/området ditt bruker merverdiavgift (mva), kan du se [Definer beregninger og bokføringsmetoder for merverdiavgift](finance-setup-vat.md).  

## <a name="example-of-linking-posting-groups"></a>Eksempel på kobling av bokføringsgruppe

Her er et scenario.  

Disse bokføringsgruppene er valgt på kundekortet:  

* Firmabokføringsgruppe
* Kundebokføringsgruppe  

Disse bokføringsgruppene er valgt på varekortet:  

* Generell produktbokføringsgruppe  
* Bokføringsgruppe - lager  

Når du oppretter et salgsdokument, bruker salgshodet informasjonen fra kundekortet, og salgslinjene bruker informasjonen fra varekortet.  

* Bokføringen av inntekter (resultat) fastsettes av kombinasjonen av bokføringsgruppen for firma og bokføringsgruppen for vare.  
* Bokføringen av kortsiktige fordringer (balanse) fastsettes av bokføringsgruppen for kunde.  
* Lagerbokføringen (balanse) fastsettes av bokføringsgruppen for lager.  
* Bokføringen av solgte varers kost (resultat) fastsettes av kombinasjonen av bokføringsgruppen for firma og bokføringsgruppen for vare.  

Oppsettet bestemmer når postering skjer. Hvis du for eksempel berørt tidsberegning av når du gjør periodiske aktiviteter, for eksempel bokføre lagerkostnaden eller justere kostverdi-vareposter.

## <a name="copy-posting-setup-lines"></a>Kopier linjer for bokføringsoppsett

Jo flere bokføringsgrupper for vare og firma du har, jo flere linjer ser du på siden **Generelt bokføringsoppsett**. Selv om det kan være mange ulike kombinasjoner av bokføringsgrupper for firma og vare, kan de ulike kombinasjonene likevel bokføre til de samme finanskontoene. Du kan begrense mengden manuell registrering ved kopiere finanskontoene fra en eksisterende linje på siden **Generelt bokføringsoppsett**.

## <a name="set-up-posting-groups-on-the-go"></a>Definere bokføringsgrupper på farten

[!INCLUDE[prod_short](includes/prod_short.md)] kan vise varslinger om manglende finanskonti i ulike oppsett for bokføringsgrupper, slik at brukere kan komme raskere i gang. Hvis du vil ha disse varslene, må du kontrollere at varselet **Finanskonto mangler i bokføringsgruppe eller oppsett** er valgt på **Mine varsler**-siden, som du får tilgang til fra feltet **Endre når jeg mottar varsler** på siden **Mine innstillinger**.  

Dermed får du et varsel når du arbeider med et dokument som bruker en bokføringsgruppe, eller et oppsett som mangler en nødvendig finanskonto. Velg koblingen i varslingen for å åpne en side der du kan gjøre de aktuelle endringene, forutsatt at du har tillatelse til å gjøre dem.  

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] oppretter en plassholderbokføringsgruppe eller et plassholderoppsett, slik at det kan sende deg direkte til bokføringsgruppen eller oppsettet som mangler en finanskonto. Bokføringsgrupper og oppsett gjør at regnskapsføreren kan styre hvordan poster bokføres i Finans, så slik just-in-time-opprettelse av bokføringsgrupper og oppsett er kanskje ikke tillatt i organisasjonen din.  
>
> I dette tilfellet deaktiverer du varselet *Finanskonto mangler i bokføringsgruppe eller oppsett*, og deretter arbeider du med regnskapsføreren for å foreta relevante endringer i bokføringsgruppen, oppsettet eller dokumentet. Dette er et viktig trinn fordi etter at dokumenter er bokført, kan du ikke slette uriktig brukte bokføringsgrupper eller oppsett fordi finansposter er opprettet for dem.

Bruk feltet **Sperret** på siden **Generelt bokføringsoppsett** til å hindre at brukere ved en feiltakelse bruker et oppsett som ikke lenger er relevant for nye bokføringer. 

## <a name="access-all-fields-and-accounts-when-you-set-up-a-posting-group"></a>Åpne alle felter og kontoer når du definerer en bokføringsgruppe

Bokføringsgrupper kan være kompliserte å definere. Fordi noen kontotyper ikke brukes ofte, viser ikke [!INCLUDE [prod_short](includes/prod_short.md)] dem som kolonner på linjene. For å gjøre det litt enklere å velge riktige kontoer filtrerer [!INCLUDE [prod_short](includes/prod_short.md)] kontoene du kan velge i feltoppslag. 

Hvis du vil ha tilgang til alle kontoene på linjene og i feltoppslagene, er det et par innstillinger som kan hjelpe:

* Hvis du vil vise alle kontoer som kolonner på linjene, aktiverer du vekslebryteren **Vis alle kontoer**.
* Hvis du vil ha tilgang til alle kontoer i feltoppslag på individuelle linjer, merker du av for **Vis alle kontoer ved oppslag**.

> [!NOTE]
> Vekslebryteren **Vis alle kontoer** ser kanskje ikke ut til å fungere på siden **Generelt bokføringsoppsett**. Det er fordi [!INCLUDE [prod_short](includes/prod_short.md)] alltid viser alle kontoer som kolonner på linjene på denne siden.

## <a name="troubleshooting-posting-group-errors"></a>Feilsøking av feil med bokføringsgruppe

Bokføringsgrupper er en av de mer avanserte konseptene som skal konfigureres i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis de ikke er konfigurer riktig, kan det oppstå feil når du bokfører dokumenter eller kladdelinjer. Disse feilene oppstår for eksempel vanligvis av en feil i forbindelse med hvordan finanskonti tilordnes, eller hvordan bokføringsgrupper kombineres.

Når noe er feil, viser [!INCLUDE[prod_short](includes/prod_short.md)] siden **Feilmeldinger**. Siden **Feilmeldinger** kan gjøre det enklere å identifisere og løse problemet. Siden gir en beskrivelse av feilen som henviser til bokføringsgruppeoppsettet som krever oppmerksomhet. Meldingen kan for eksempel være «Konto for salgsforskudd mangler i et generelt bokføringsoppsett». Det finnes også en kobling for å åpne siden som er kilden til problemet, slik at du raskt kan løse det.  

> [!NOTE]
> Feilbehandlingen som er beskrevet ovenfor, er ikke tilgjengelig for vare, ressurs, ansatt og aktivakladder, eller for finanskontoer som er lagt til i lokale versjoner av bokføringsgrupper.

## <a name="see-also"></a>Se også

[Finans og kontoplanen](finance-general-ledger.md)    
[Definere Finance](finance-setup-finance.md)    
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
