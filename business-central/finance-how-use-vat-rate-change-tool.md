---
title: Bruk verktøyet for endring av mva-sats | Microsoft-dokumenter
description: Bruke verktøyet for endring av mva-sats
author: andregu
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 01/06/2020
ms.author: andregu
ms.openlocfilehash: 0fe23bb6b1d4ce6fbf73a1978a66f6d47b8e78fe
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/28/2020
ms.locfileid: "2992235"
---
# <a name="use-the-vat-rate-change-tool"></a>Bruke verktøyet for endring av mva-sats

## <a name="understanding-the-vat-rate-conversion-process"></a>Forstå konvertering av mva-satsendring  
Verktøyet for endring av mva-sats utfører mva-satskonverteringer for hoveddata, kladder og ordrer på forskjellige måter. Valgte hoveddata og kladder blir oppdatert med den nye varebokføringsgruppen eller mva-varebokføringsgruppen. Hvis en ordre er fullstendig eller delvis levert, beholder de leverte varene gjeldende varebokføringsgruppe eller mva-varebokføringsgruppe. En ny ordrelinje blir opprettet for usendte varer og oppdatert for å justere gjeldende og nye mva- eller varebokføringsgrupper. I tillegg oppdateres varegebyrtilordninger, reservasjoner og varesporingsinformasjon i henhold til dette.  

Det er et par ting verktøyet ikke konverterer:

* Ordrer eller bestillinger og fakturaer der leveringer er bokført. Disse dokumentene bokføres med den gjeldende mva-satsen.  
* Dokumenter som har bokførte forskuddsfakturaer. Du har for eksempel foretatt eller mottatt forskuddsbetaling på fakturaer som ikke ble fullført før du brukte verktøyet for endring av mva-sats. I dette tilfellet blir det en forskjell mellom mva. som er forfalt og mva. som er betalt i forskuddsbetalingene, når fakturaen er fullført. Verktøyet for endring av mva-sats vil hoppe over disse dokumentene, og du må oppdatere dem manuelt.  
* Direkte leveringer eller spesialordrer.  
* Ordrer eller bestillinger med lagerintegrasjon hvis de er delvis levert eller mottatt.  
* Servicekontrakter.  

### <a name="to-prepare-vat-rate-change-conversions"></a>Klargjøre konverteringer av mva-satsendring  
Før du konfigurerer verktøyet for mva-satsendring, må du gjøre følgende forberedelser.

* Hvis du har transaksjoner som bruker forskjellige satser, må du dele dem inn i ulike grupper ved å opprette nye finanskonti for hver sats, eller ved å bruke datafiltre til å gruppere transaksjoner i henhold til sats.  
* Hvis du oppretter nye finanskonti, må du opprette nye generelle bokføringsgrupper.  
* Hvis du vil redusere antall dokumenter som konverteres, må du bokføre så mange dokumenter som mulig og redusere ikke-bokførte dokumenter til et minimum.  
* Sikkerhetskopiere data.

### <a name="to-set-up-the-vat-rate-change-tool"></a>Slik konfigurerer du verktøyet for endring av mva-sats:  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Oppsett for endring av mva-sats**, og velg deretter den relaterte koblingen.  
2. På hurtigfanene **Hoveddata**, **Kladder** og **dokumenter** velger du en bokføringsgruppeverdi fra alternativlisten over nødvendige felt. For hver gruppe kan du velge om du vil konvertere mva-bokføringsgrupper for varer eller varebokføringsgrupper, eller konvertere begge verdier hvis de er tilgjengelige i hoveddataelementet. For enkelte områder kan du også angi et filter for å konvertere bare et delsett med verdier, for eksempel finanskonti. 

### <a name="to-set-up-product-posting-group-conversion"></a>Slik definerer du omregning av varebokføringsgruppe:  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Oppsett for endring av mva-sats**, og velg deretter den relaterte koblingen.  
2. På siden **Oppsett for endring av mva-sats** velger du handlingen **Mva-bokføringsgruppekonv.** eller **Gen. varebokføringsgruppekonv.**  
3. Angi gjeldende bokføringsgruppe i feltet **Fra-kode**.  
4. Angi den nye bokføringsgruppen i feltet **Til-kode**.  

### <a name="to-perform-vat-rate-change-conversion"></a>Utføre konverteringer av mva-sats  
Du bruker endringsverktøyet for mva-sats til å administrere endringer i standardsatsen for mva. Du utfører omregninger av mva og generelle bokføringsgrupper for å endre mva-satser og opprettholde en nøyaktig mva-rapportering. Avhengig av oppsettet gjøres følgende endringer:  

* Mva-bokføringsgrupper og generelle bokføringsgrupper konverteres.  
* Endringene er implementert i finanskontoer, kunder, leverandører, åpne dokumenter, kladdelinjer osv.  

> [!IMPORTANT]  
>  Før du foretar endringen av mva-satsen, kan du teste konverteringen. Hvis du vil gjøre dette, følger du fremgangsmåten nedenfor, men må du fjerne merket for **Utfør konvertering** og **Verktøy for endring av mva-sats ferdig**. Under testkonvertering fjernes feltet **Konvertert** i tabellen **Mva-sats – endringsloggpost** og feltet **Konvertert dato** i tabellen **Mva-sats – endringsloggpost** er tom. Når konverteringen er fullført, velger du **Mva-sats – endringsloggposter** for å vise resultatene av testkonverteringen. Kontroller hver post før du utfører konvertering. Kontroller særlig transaksjoner som bruker en gammel mva-sats.     

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Endring av mva-sats**, og velg koblingen **Oppsett for endring av mva-sats**.  
2. Kontroller at du allerede har definert omregningen av mva-varebokføringsgruppen eller omregningen av varebokføringsgruppen.  
3. Merk av for **Utfør konvertering**.  

    > [!IMPORTANT]  
    >  Fjern merket for **Verktøy for endring av mva-sats ferdig**. Avmerkingsboksen velges automatisk når konverteringen for mva-satsendring er fullført.  

4. Velg handlingen **Komnverter**.  
5. Når konverteringen er fullført, velger du **Mva-sats – endringsloggposter** for å vise resultatene av konverteringen.  

> [!IMPORTANT]  
>  Etter konverteringen er feltet **Konvertert** i tabellen **Loggpost for mva-satsendring** valgt og feltet **Konvertert dato** i tabellen **Loggpost for mva-satsendring** viser konverteringsdatoen.  
## <a name="see-also"></a>Se også  
[Definere merverdiavgift (mva)](finance-setup-vat.md)  
[Definere urealisert merverdiavgift](finance-setup-unrealized-vat.md)      
[Rapportere mva til skattemyndighetene](finance-how-report-vat.md)  
[Arbeide med mva på kjøp og salg](finance-work-with-vat.md)  
[Lokal funksjonalitet i Business Central](about-localization.md)
