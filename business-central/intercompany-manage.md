---
title: Behandle konserninterne transaksjoner
description: Med de konserninterne funksjonene kan du forenkle forretningsprosesser og transaksjoner mellom selskaper i samme organisasjon.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bhielse
ms.topic: conceptual
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '605,'
ms.service: dynamics-365-business-central
---
# <a name="managing-intercompany-transactions"></a>Behandle konserninterne transaksjoner

Bedrifter med mer enn én juridisk enhet med separate regnskapsfunksjoner, kan dra nytte av konserninterne transaksjoner. Det kan for eksempel være nyttig for selskaper som har datterselskaper i flere internasjonale markeder eller områder. Eller en organisasjonen kan ha flere selskaper, men mangle samme antall regnskapsteam og administrative team. Med konserninterne transaksjoner kan du forenkle og tilpasse forretningsprosesser og transaksjoner mellom selskaper i det konserninterne partnerskapet.

Når du har angitt kunde- og leverandørrelasjonen for konserninterne transaksjoner, angir partnerne informasjon én gang i salgs- og kjøpsdokumenter. Et tilsvarende dokument opprettes i den andre partneren som er involvert i transaksjonen. Tildeling av kontoplanen og dimensjonene hjelper deg med å sikre at informasjonen vises på riktige steder.  

Det er fire hovedfordeler med de konserninterne funksjonene:  

* Økt produktivitet som et resultat av spart tid og forenklede transaksjoner  
* Redusert antall feil med engangsregistrering av informasjon og systemomfattende, automatiske oppdateringer  
* Fullstendig sporing og full synlighet i forretningsaktiviteter og transaksjonslogger  
* Effektive, kostnadsbesparende transaksjoner med partner- og datterselskaper  

## <a name="streamline-the-flow-of-business-activities"></a>Effektiv flyt av forretningsaktiviteter

Med konserninterne transaksjoner kan du distribuere salgs- og kjøpsdokumenter og finansposter til alle satellittkontorer, salgskontorer eller datterselskaper. Distribusjon av transaksjoner sparer tid og øker effektiviteten i hele organisasjonen ved å redusere dataregistreringen. Det kutter ned på behovet for å sende, motta, skrive ut og arkivere salgs- og kjøpsdokumenter.  

Du har full kontroll over alle transaksjonsdokumenter. Du kan for eksempel avvise et dokument som sendes til deg, og bruke handlingene **Tilbakefør kladdebokføringer** og **Angre mottak/leveringer** for å korrigere. Og når du foretar et kjøp fra et partner- eller datterselskap, kan du oppdatere bestillingen så lenge salgsselskapet ikke har sendt varene ennå.  

Når du angir en transaksjon, trenger du ikke å angi kontoene som skal brukes. Du velger bare den konserninterne partneren. De konserninterne funksjonene oppretter finanskladdelinjer som balanserer bøkene i begge selskapene som er involvert i transaksjonen. I Kundekonto og Leverandørkonto kan du tilordne en konsernintern partnerkode til hvilken som helst kunde eller leverandør. Fra nå av produserer alle ordrer og fakturaer for transaksjoner mellom disse selskapene tilsvarende dokumenter i partnerselskapet. Resultatet er riktig balanserte kontoer.  

Konsernintern fokuserer på salgs- og kjøpsdokumenter og finanskladdelinjer og tillater transaksjoner mellom flere [!INCLUDE [prod_short](includes/prod_short.md)]-databaser. Eksempel:

* I forskjellige land/områder
* Flere valutaer
* Ulike kontoplaner
* Ulike dimensjoner
* Ulike varenumre  

Konserninterne transaksjoner bruker flere typer poster og dokumenter:  

* Finanskladdeposter
* Bestillinger og ordrer
* Kjøps- og salgsfakturaer
* Kreditnotaer
* Ordrereturer

Når du definerer konserninterne transaksjoner, oppretter du en liste over konserninterne partnere, en konsernintern kontoplan og konserninterne dimensjoner. Etterpå kan du opprette transaksjoner i konserninterne finanskladder.

> [!NOTE]
> Finanskladden alene inkluderer ikke valutaer. Det konverterer alle beløp til lokal valuta ved nåværende valutakurs.

Når du har definert forretningspartnerne som kunder og leverandører og tildeler konserninterne partnerkoder til dem, kan de utveksle konserninterne kjøps- og salgsdokumenter, inkludert varer og varegebyrer. 

> [!NOTE]
> Selskaper kan ikke bruke konsernintern til å utveksle alle typer data. Kjøpsfakturaer sendes ikke til forretningspartnere gjennom konserninterne prosesser. Salgsfakturaer som sendes via konserninterne prosesser, blir imidlertid opprettet som kjøpsfakturaer i mottaksselskapet.

Konsolidere økonomisk data kan være aktuelt for konserninterne prosesser. Hvis du vil ha mer informasjon, se [Konsolidere finansielle data fra flere selskap](finance-consolidated-company-reporting.md).

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til artiklene som beskriver dem.

|Hvis du vil |Se|
|---|---|
|Opprett konserninterne leverandører og kunder som partnere, og definer en konsernintern kontoplan.|[Oppsett av konserninternt](intercompany-how-setup.md)|
|Bruk konserninterne dokumenter eller kladder til å bokføre transaksjoner med de konserninterne partnerne.|[Arbeide med konserninterne dokumenter og kladder](intercompany-how-work-documents-journals.md)|
|Organisere og behandle inngående og utgående transaksjoner som du kan utveksle med de konserninterne partnerne.|[Administrere den konserninterne innboksen og utboksen](intercompany-how-manage-intercompany-inbox.md)|
|Bruk konserninterne transaksjoner til å fordele kost mellom partnerselskaper.|[Fordel kost til konserninterne partnere](intercompany-allocate-costs.md)|

## <a name="see-also"></a>Se også

[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Arbeid med finanskladder](ui-work-general-journals.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
