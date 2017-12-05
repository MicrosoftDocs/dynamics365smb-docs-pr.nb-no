---
title: Servicestatistikk | Microsoft-dokumentasjon
description: "Få en rask oversikt over innholdet i servicedokumenter, som ordrer, tilbud, fakturaer eller kreditnotaer, detaljene i bestemte servicelinjer og servicevarene."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: e4cc14212f30c7b42aaf9d08c848488ab65444f6
ms.contentlocale: nb-no
ms.lasthandoff: 11/10/2017

---

# <a name="viewing-service-statistics"></a>Vise servicestatistikk
Financials kan levere litt statistikk som du kan bruke til å analysere servicedokumenter og bestemme hvor godt du administrerer serviceprosessene. Du kan analysere servicekontrakter, varer, tilbud, ordrer, fakturaer og kreditnotaer ved å velge handlingen **Statistikk**. For servicevarer og kontrakter kan du også bruke vinduet **Servicevare - Trendscape** eller **Kontrakt - Trendscape** for å vise en oversikt over bokførte serviceposter for en bestemt servicevare.   

## <a name="viewing-statistics-for-service-orders"></a>Vise statistikk for serviceordrer
Funksjonen for serviceordrestatistikk gir deg en rask oversikt over innholdet i hele serviceordren, detaljene i bestemte servicelinjer, informasjon i tilknytning til fakturering, levering og forbruk samt kundens saldo.  

Statistiske data vises for en serviceordre i vinduet **Serviceordrestatistikk** for den aktuelle ordren. Du kan åpne det relevante statistikkvinduet fra en serviceordre. I vinduet **Serviceordrer** velger du **Statistikk**. Hurtigfanene i dette vinduet gir informasjon om antall, beløp, mva, kost, bruttofortjeneste og kundens kredittgrense. Beløpene i vinduet er i samme valuta som i serviceordren, hvis ikke annet er angitt.  

### <a name="view-totals-for-a-service-order"></a>Vise totaler for en serviceordre  
Du kan vise totalbeløp i servicelinjene, med og uten mva, mva-andel, kost og fortjeneste i servicelinjene. Vinduet viser også vareopplysninger, for eksempel vekt, volum og antall kolli.  

### <a name="view-shipping-information"></a>Vise leveringsopplysninger  
Du kan se informasjon om varer, ressurser eller kost som skal leveres. Som informasjonsgrunnlag brukes verdiene som er angitt i feltet **Levere (antall)** i hver av servicelinjene i ordren.  

### <a name="view-order-details"></a>Vise ordredetaljer  
Du kan vise informasjon om varer, ressurstimer og kost som skal faktureres og forbrukes. Tabellen nedenfor beskriver denne informasjonen.  

|Kolonne | Beskrivelse|  
|------------|---------------------------------------|  
|**Fakturering**|Viser beløp som skal bokføres som fakturert, fra serviceordren.|  
|**Forbruk**|Viser antall og kost for varer eller ressurser som skal bokføres som forbrukt.|  
|**I alt**|Viser totalbeløpene i serviceordren som blir resultatet når fakturerings- og forbruksbeløpene legges sammen.|  

### <a name="analyze-service-order-lines"></a>Analysere serviceordrelinjer  
Du kan analysere informasjon etter hvilke typer servicelinjer som inngår i serviceordren. Beløpene vises separat for:  

* Varer  
* Ressurser  
* Kostnader og finanskontoer  

### <a name="view-customer-information"></a>Vise kundeopplysninger  
Se saldoen på kundens konto samt den maksimale kreditten som kan tilstås kunden du har opprettet servicedokumentet for.

## <a name="viewing-service-item-statistics"></a>Vise servicevarestatistikk
I vinduet **Servicevarestatistikk** vises oppdatert informasjon om sen servicevare basert på følgende serviceposttyper:  

* Ressurser  
* Varer  
* Servicekostnad  
* Servicekontrakter  
* Sum  

For hver posttype kan du vise fakturert beløp, forbruk (beløp), kostbeløp, antall, fakturert og forbrukt antall, bruttofortjenestebeløp og bruttofortjenesteprosent. Bruttofortjenesteprosenten beregnes i henhold til følgende formel:  

* (Fakturert beløp - Bruk (Kostnader)) x 100 / Fakturert beløp  

## <a name="using-trendscapes"></a>Bruke Trendscapes
For servicevarer og servicekontrakter inneholder vinduet **Servicevare - Trendscape** eller **Servicekontrakt - Trendscape** en rulleoversikt over serviceposter i en periode for en bestemt servicevare eller kontrakt. Hvis du vil vise trendscape, åpner du servicevaren eller servicekontrakten, velger handlingen **Statistikk** og deretter **Trendscape**.

Når du ruller i listen, beregnes beløpene i lokal valuta i henhold til det angitte tidsintervallet. Beløpene beregnes alle beløp fra serviceposter, det vil si poster som opprettes når du bokfører serviceordrer eller servicefakturaer.

Du kan filtrere listen ved å angi servicevarer som skal tas med.  

> [!Tip]  
>  Hvis du har valgt tidsintervallet **Dag** og du vil rulle over en lang periode, kan du gjøre dette raskere ved å skifte til et større intervall, for eksempel **Kvartal**. Når du har funnet perioden du vil ha, kan du gå tilbake til det opprinnelige intervallet for å vise mer detaljerte opplysninger om intervallene.   

## <a name="viewing-gains-and-losses-on-contracts"></a>Vise agio og disagio for kontrakter  
En kontraktresultatpost genereres når et kontrakttilbud konverteres til en servicekontrakt, når kontraktlinjer legges til eller fjernes fra en servicekontrakt, eller når en kontrakt avbrytes. Du kan vise agio og disagio for kontrakter på siden nedenfor.  

|Side | Beskrivelse|  
|----------------|---------------------------------------|  
|**Kontraktresultat (kontrakter)**|Slik viser du kontraktresultat etter servicekontrakt.|  
|**Kontraktresultat (grupper)**|Slik viser du kontraktresultat etter servicekontraktgruppe.|  
|**Kontraktresultat (kunder)**|Slik viser du kontraktresultat etter kunde.|  
|**Kontraktresultat (årsaker)**|Slik viser du kontraktresultat etter årsakskode.|  
|**Kontraktresultat (ansv.sent)**|Slik viser du kontraktresultat etter ansvarssenter.|  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), skriver inn navnet på siden som skal vises, og velger deretter den relaterte koblingen.  
2. Fyll ut filtervilkårene du vil bruke. Velg for eksempel en verdi for **Filter for årsaksspor** i vinduet **Kontraktresultat (årsaker)**.  
3. Velg handlingen **Vis matrise**.

## <a name="viewing-statistics-for-posted-service-documents"></a>Vise servicestatistikk for bokførte dokumenter
Ved hjelp av funksjonen for servicestatistikk kan du få en statistisk oversikt over innholdet i bokførte servicedokumenter, for eksempel en bokført følgeseddel, bokført faktura og bokført kreditnota.  

Den statistiske informasjonen vises i statistikkvinduet for det tilhørende bokførte servicedokumentet. Du kan åpne det relevante statistikkvinduet fra dokumenter for bokførte servicefølgesedler, bokførte servicefakturaer eller bokførte servicekreditnotaer. Velg **Statistikk** under **Prosess** i fanebladet **Hjem** for hver av disse dokumenttypene. Velg for eksempel **Statistikk** under **Prosess** i fanebladet **Hjem** i vinduet **Bokførte servicefakturaer**.  

### <a name="posted-service-shipment-statistics"></a>Statistikk for bokført servicefølgeseddel  
Vinduet **Statistikk for servicefølgesedler** gir en oversikt over en bokført servicefølgeseddel. Dette omfatter informasjon om det fysiske innholdet i leveringen, for eksempel antall leverte varer, ressurstimer eller -kost samt vekt og volum for de leverte varene.  

### <a name="posted-service-invoice-statistics"></a>Statistikk for bokført servicefaktura  
Du kan vise et statistisk sammendrag av en bokført servicefaktura i vinduet **Statistikk for servicefaktura**. Du kan vise totalene for den bokførte servicefakturaen. Dataene omfatter totalbeløp i servicelinjene (med og uten mva) som er bokført som fakturert, mva-andel, kost og fortjeneste i den bokførte fakturaen. Vinduet viser også informasjon om følgende:  

* Varene i servicefakturalinjene, for eksempel vekt, volum og antall kolli.  
* Saldoen på kundens konto samt den maksimale kreditten som kan du gi kunden.  

### <a name="posted-service-credit-memo-statistics"></a>Statistikk for bokført salgskreditnota (service)  
Du kan bruke vinduet **Statistikk for salgskreditnota (service)** til å få en statistisk oversikt over linjene i en bokført salgskreditnota (service). Oversikten kan omfatte følgende:

* Totalbeløpene i den bokførte kreditnotaen, vises som antall, beløp, mva, kost og fortjeneste. Det er også informasjon om varene i servicelinjene i den bokførte kreditnotaen, for eksempel antall, vekt og volum.  
* Generell informasjon om kunden, for eksempel kundens kredittgrense og kontosaldo.  

## <a name="see-also"></a>Se også  
[Opprette serviceordrer](service-how-to-create-service-orders.md)   
[Opprette servicevarer](service-how-to-create-service-items.md)   
[Planlegge service](service-plan-service.md)  

