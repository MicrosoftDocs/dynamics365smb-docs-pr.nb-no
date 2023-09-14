---
title: Designdetaljer – Bokføring av forventet kost
description: 'Forventede kostnader representerer for eksempel overslaget for kjøpspris for en vare du registrerer, før du faktisk mottar fakturaen for varen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 07/20/2021
ms.author: bholtorf
---
# Designdetaljer: Bokføre forventet kost
Forventede kostnader representerer for eksempel overslaget for kjøpspris for en vare du registrerer, før du faktisk mottar fakturaen for varen.  

 Du kan bokføre forventet kost på lager og i finans. Når du bokfører et antall som bare er mottatt eller levert, men ikke fakturert, opprettes deretter en verdipost den forventede kostnaden. Denne forventede kostnaden påvirker lagerverdien, men bokføres ikke i finans med mindre du konfigurerer systemet slik at dette gjøres.  

> [!NOTE]  
>  Forventede kostnader behandles bare for varetransaksjoner. Forventede kostnader er ikke for immaterielle transaksjonstyper, for eksempel kapasitet og varegebyr.  

 Hvis bare antallsdelen av en lagerøkning er bokført, vil ikke lagerverdien i Finans endres med mindre du har merket av for **Bokf. av forventet kost i Finans** på siden **Lageroppsett**. I slike tilfeller bokføres forventet kost på midlertidige konti på mottakstidspunktet. Når mottaket er ferdigfakturert, balanseres de midlertidige kontiene, og de faktiske kostnadene bokføres til lagerkontoen.  

 For å støtte avstemming og sporing viser den fakturerte verdiposten det forventede kostbeløpet som er bokført på motkonti og midlertidige konti.  

## Forutsetninger for bokføring av forventede kostnader

Du må gjøre følgende for å gjøre det mulig å bokføre forventede kostnader:
1. På siden **Lageroppsett** velger du avmerkingsboksen **Automatisk kostbokføring** og **Bokf. av forventet kost i finans**.
2. Definer midlertidige konti som skal brukes i forbindelse med bokføringsprosessen for forventet kostnad.  

  På siden **Lagerbokføringsoppsett** bekrefter du **lagerkontoen** og feltene **Lagerkonto (midlertidig)** for **Lokasjonskode og koden for lagerbokføringsgruppe** for varen som skal kjøpes. Hvis du vil ha mer informasjon om disse kontiene, kan du se [Designdetaljer: Konti i finans](design-details-accounts-in-the-general-ledger.md).
3. På siden **Generelt bokføringsoppsett** kontrollerer du feltet **Forv. lagerjust.kto. (midl.)** for feltet **Bokføringsgruppe – firma** og **Bokføringsgruppe – vare** du vil bruke.
4. Når du oppretter en bestilling, er standardverdien feltet **Leverandørs fakturanr.** er obligatorisk. Du må deaktivere denne funksjonen på siden **Kjøpsoppsett** ved å fjerne merket for feltet **Obligatorisk nr. for eksternt dokument**.

## Eksempel  

> [!NOTE]  
> Kontonumrene som brukes i dette eksemplet, er bare til referanse og vil være forskjellige i systemet. Definer dem som angitt i forutsetningene ovenfor.

Du bokfører en bestilling som mottatt. Forventet kostnad er LV 95,00.  

 **Verdiposter**  

|Bokføringsdato|Posttype|Kostbeløp (forventet)|Forventet kost bokført i Finans|Forventet kostnad|Varepostnr.|Løpenr.|  
|------------------|----------------|------------------------------|----------------------------------|-------------------|---------------------------|---------------|  
|01.01.20|Kjøpspris/prod.kost|95,00|95,00|Ja|1|1|  

 **Relasjonsposter i tabellen Finans – varepostrelasjon**  

|Finansløpenr.|Verdiløpenummer|Finansjournalnr.|  
|--------------------|---------------------|-----------------------|  
|1|1|1|  
|2|1|1|  

 **Finansposter**  

|Bokføringsdato|Finanskonto|Kontonummer (En-US-demo)|Beløp|Løpenr.|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01.01.20|Forventet lagerjusteringskonto (midlertidig)|5530|-95,00|2|  
|01.01.20|Lagerkonto (midlertidig)|2131|95,00|1|  

 Senere bokfører du bestillingen som fakturert. Fakturert kost er LV 100,00.  

 **Verdiposter**  

|Bokføringsdato|Kostbeløp (faktisk)|Kostbeløp (forventet)|Bokført kost|Forventet kostnad|Varepostnr.|Løpenr.|  
|------------------|----------------------------|------------------------------|-------------------------|-------------------|---------------------------|---------------|  
|15.01.20|100,00|-95,00|100,00|Nei|1|2|  

 **Relasjonsposter i tabellen Finans – varepostrelasjon**  

|Finansløpenr.|Verdiløpenummer|Finansjournalnr.|  
|--------------------|---------------------|-----------------------|  
|3|2|2|  
|4|2|2|  
|5|2|2|  
|6|2|2|  

 **Finansposter**  

|Bokføringsdato|Finanskonto|Kontonr. (bare eksempler!)|Beløp|Løpenr.|  
|------------------|------------------|---------------------------------|------------|---------------|  
|15.01.20|Forventet lagerjusteringskonto (midlertidig)|5530|95,00|4|  
|15.01.20|Lagerkonto (midlertidig)|2131|-95,00|3|  
|15.01.20|Konto utl. kj.pris/prod.kost|7291|-100|6|  
|15.01.20|Lagerkonto|2130|100|5|  

## Se også
 [Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)   
 [Designdetaljer: Kostjustering](design-details-cost-adjustment.md)   
 [Designdetaljer: Avstemming med konti i Finans](design-details-reconciliation-with-the-general-ledger.md)   
 [Designdetaljer: Lagerbokføring](design-details-inventory-posting.md)   
 [Designdetaljer: Avvik](design-details-variance.md)  
 [Administrere lagerkostnader](finance-manage-inventory-costs.md)  
 [Finans](finance.md)  
 [Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
