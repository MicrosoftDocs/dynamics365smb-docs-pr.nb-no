---
title: Håndtere endringer i mva-satser
description: Lær hvordan du bruker verktøyet for endring av mva-satser for Dynamics 365 Business Central for å endre mva-satser basert på lokal lovgivning.
author: andregu
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.reviewer: edupont
ms.workload: na
ms.search.keywords: VAT, VAT rate, posting, tax, value-added tax
ms.search.form: 550,
ms.date: 06/16/2021
ms.author: andregu
ms.openlocfilehash: e021a2950d3441f481c63771250c44b874f92cda
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/14/2022
ms.locfileid: "7970547"
---
# <a name="managing-vat-rate-changes"></a>Håndtere endringer i mva-satser

MVA-satser kan endres avhengig av lokal lovgivning. Eventuelle endringer i mva påvirker dataene i [!INCLUDE[prod_short](includes/prod_short.md)] om mva-satsen reduseres, økes eller fjernes. Mva er knyttet til mange enheter i [!INCLUDE[prod_short](includes/prod_short.md)], for eksempel kunder, leverandører, varer, ressurser, varegebyrer og finanskonti. Endringer i mva-satser skjer vanligvis på en bestemt dato, og fra hvilket punkt må du ha endret mva-oppsettet, bokføringsgruppene og så videre, for å sikre at nye ordrer og bestillinger opprettes med den nye mva-satsen.

## <a name="changing-vat-rates"></a>Endre mva-satser

Den optimale fremgangsmåten for å håndtere en endring i mva-satser er å bokføre og lukke åpne ordrer og andre dokumenter før endringsdatoen for mva-sats for å sikre at disse ikke påvirkes av endringen. Dette er den ryddigste tilnærmingen som gjør at du kan opprette nye ordrer og dokumenter med den nye mva-satsen.

Fremgangsmåten nedenfor anbefales når du skal håndtere en endring av mva-sats

1. Bokfør og lukk åpne ordrer, kladder og andre dokumenter fullstendig før endringsdatoen. Du kan vente til etter endringsdatoen så lenge du ikke legger til nye linjer og kontrollerer at ikrafttredelsesdatoen kommer før endringsdatoen.  
2. Opprett det nye mva-oppsettet.  
3. Utfør endring av mva på enheter (relevante kunder, leverandører, varer og så videre).  
4. På endringsdatoen for mva-satsen oppretter du nye dokumenter som vil bruke den nye satsen.  


> [!NOTE]  
> Verktøyet for endring av mva-satser oppdateres. Funksjonaliteten som er nevnt nedenfor, er kanskje ikke i samsvar med funksjonaliteten i ditt miljø. Oppdateringen vil finne sted før 1. juli 2020 og ikke vil være en vanlig månedlig oppdatering. I stedet vil alle miljøer bli oppdatert automatisk (hurtigreparasjon). Når denne oppdateringen er fullført, vil ikke meldingen lenger vises.  

## <a name="the-vat-rate-change-tool"></a>Bruke verktøyet for endring av mva-sats

Verktøyet for endring av mva-sats kan til en viss grad hjelpe med konvertering av mva-satser på hoveddata, kladder og ordrer. Dette er nyttig hvis du vil konvertere mva på hoveddata på en enklere måte, eller hvis du har ordrer som du ikke kan lukke før endringsdatoen og som skal behandles over en lengre tidsperiode, som krysser endringsdatoen for mva-satsen. Det finnes bestemte gjeldende begrensninger i verktøyet for endring av mva-satser.

## <a name="understanding-the-vat-rate-conversion-process-and-limitations"></a>Forstå prosesser og begrensninger for konvertering av mva-sats

Verktøyet for endring av mva-sats utfører mva-satskonverteringer for hoveddata, kladder og ordrer på forskjellige måter. Valgte hoveddata og kladder blir oppdatert med den nye varebokføringsgruppen eller mva-varebokføringsgruppen. Hvis en ordre er fullstendig eller delvis levert, beholder de leverte varene gjeldende varebokføringsgruppe eller mva-varebokføringsgruppe. En ny ordrelinje blir opprettet for usendte varer og oppdatert for å justere gjeldende og nye mva- eller varebokføringsgrupper. I tillegg oppdateres varegebyrtilordninger, konfigurasjonsmaler for varer, reservasjoner og varesporingsinformasjon i henhold til dette. 

På ordrelinjer oppdateres salgsprisen for alle linjer av typen vare og ressurs, hvis det brukes priser inkl. mva. for varen. For andre linjetyper er det mulig å bestemme om salgsprisen skal oppdateres eller ikke.

Det er et par ting verktøyet ikke konverterer:

* Ordrer eller bestillinger og fakturaer der leveringer er bokført. Disse dokumentene bokføres med den gjeldende mva-satsen.  
* Dokumenter som har bokførte forskuddsfakturaer. Du har for eksempel foretatt eller mottatt forskuddsbetaling på fakturaer som ikke ble fullført før du brukte verktøyet for endring av mva-sats. I dette tilfellet blir det en forskjell mellom mva. som er forfalt og mva. som er betalt i forskuddsbetalingene, når fakturaen er fullført. Verktøyet for endring av mva-sats vil hoppe over disse dokumentene, og du må oppdatere dem manuelt.  
* Ordrer eller bestillinger med lagerintegrasjon hvis de er delvis levert eller mottatt.  
* Direkte leveringer.
* Spesialbestillinger. 
* Monteringsordrer.
* Servicekontrakter.  
* Kreditnotaer.
* Ordreretur.
* Priser på varer (hoveddata)
* Priser på salgspriser (hoveddata)
* Mva-bokføringsgrupper for kunder og leverandører.

### <a name="to-prepare-vat-rate-change-conversions"></a>Klargjøre konverteringer av mva-satsendring

Før du konfigurerer verktøyet for mva-satsendring, må du gjøre følgende forberedelser.

* Hvis du har transaksjoner som bruker forskjellige satser, må du dele dem inn i ulike grupper ved å opprette nye finanskonti for hver sats, eller ved å bruke datafiltre til å gruppere transaksjoner i henhold til sats.  
* Hvis du oppretter nye finanskonti, må du opprette nye generelle bokføringsgrupper.  
* Hvis du vil redusere antall dokumenter som konverteres, må du bokføre så mange dokumenter som mulig og redusere ikke-bokførte dokumenter til et minimum.  
* Sikkerhetskopiere data.

### <a name="to-set-up-the-vat-rate-change-tool"></a>Slik konfigurerer du verktøyet for endring av mva-sats:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Oppsett for endring av mva-sats**, og velg deretter den relaterte koblingen.  
2. På hurtigfanene **Hoveddata**, **Kladder** og **dokumenter** velger du en bokføringsgruppeverdi fra alternativlisten over nødvendige felt. For hver gruppe kan du velge om du vil konvertere mva-bokføringsgrupper for varer eller varebokføringsgrupper, eller konvertere begge verdier hvis de er tilgjengelige i hoveddataelementet. For enkelte områder kan du også angi et filter for å konvertere bare et delsett med verdier, for eksempel finanskonti. 
3. I hurtigfanen **Priser inkl. mva** velger du hvilke linjetyper i ordrer du vil oppdatere salgsprisene for. Salgspriser på linjer av typen vare og ressurs vil alltid bli oppdatert.

### <a name="to-set-up-product-posting-group-conversion"></a>Slik definerer du omregning av varebokføringsgruppe:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Oppsett for endring av mva-sats**, og velg deretter den relaterte koblingen.  
2. På siden **Oppsett for endring av mva-sats** velger du handlingen **Mva-bokføringsgruppekonv.** eller **Gen. varebokføringsgruppekonv.**  
3. Angi gjeldende bokføringsgruppe i feltet **Fra-kode**.  
4. Angi den nye bokføringsgruppen i feltet **Til-kode**.  

### <a name="to-perform-vat-rate-change-conversion"></a>Utføre konverteringer av mva-sats

Du bruker endringsverktøyet for mva-sats til å administrere endringer i standardsatsen for mva. Du utfører omregninger av mva og generelle bokføringsgrupper for å endre mva-satser og opprettholde en nøyaktig mva-rapportering. Avhengig av oppsettet gjøres følgende endringer:  

* Mva-bokføringsgrupper og generelle bokføringsgrupper konverteres.  
* Endringene er implementert i finanskontoer, kunder, leverandører, åpne dokumenter, kladdelinjer osv.  

> [!IMPORTANT]  
> Før du foretar endringen av mva-satsen, kan du teste konverteringen. Hvis du vil gjøre dette, følger du fremgangsmåten nedenfor, men må du fjerne merket for **Utfør konvertering** og **Verktøy for endring av mva-sats ferdig**. Under testkonvertering fjernes feltet **Konvertert** i tabellen **Mva-sats – endringsloggpost** og feltet **Konvertert dato** i tabellen **Mva-sats – endringsloggpost** er tom. Når konverteringen er fullført, velger du **Mva-sats – endringsloggposter** for å vise resultatene av testkonverteringen. Kontroller hver post før du utfører konvertering. Kontroller særlig transaksjoner som bruker en gammel mva-sats.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Endring av mva-sats** og velg deretter koblingen **Oppsett for endring av mva-sats**.  
2. Kontroller at du allerede har definert omregningen av mva-varebokføringsgruppen eller omregningen av varebokføringsgruppen.  
3. Merk av for **Utfør konvertering**.  

    > [!IMPORTANT]  
    >  Fjern merket for **Verktøy for endring av mva-sats ferdig**. Avmerkingsboksen velges automatisk når konverteringen for mva-satsendring er fullført.  

4. Velg handlingen **Komnverter**.  
5. Når konverteringen er fullført, velger du **Mva-sats – endringsloggposter** for å vise resultatene av konverteringen.  

> [!IMPORTANT]  
> Etter konverteringen er feltet **Konvertert** i tabellen **Loggpost for mva-satsendring** valgt og feltet **Konvertert dato** i tabellen **Loggpost for mva-satsendring** viser konverteringsdatoen.  

## <a name="see-also"></a>Se også

[Definere merverdiavgift (mva)](finance-setup-vat.md)  
[Definere urealisert merverdiavgift](finance-setup-unrealized-vat.md)  
[Rapportere mva til skattemyndighetene](finance-how-report-vat.md)  
[Arbeide med mva på kjøp og salg](finance-work-with-vat.md)  
[Lokal funksjonalitet i Business Central](about-localization.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]