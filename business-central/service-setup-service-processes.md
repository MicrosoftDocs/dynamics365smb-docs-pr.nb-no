---
title: Definere prosesser for servicehåndtering
description: Lær hvordan du konfigurerer prosesser som sørger for at kundene dine er tilfreds med servicen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'service, number sequences, setup, warnings, fee, contracts, warranties'
ms.date: 02/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Konfigurere prosesser for servicehåndtering

Her er noen eksempler på innstillinger du kan bruke i servicehåndteringsprosessene:  
  
* Noen generelle innstillinger for ulike prosesser, for eksempel advarsler, beregningsmåte for neste service for servicevarer, startgebyret for å vurdere, feilrapporteringsnivået som skal brukes og så videre.  
* Typen informasjon som teknikere må angi i servicedokumenter. Du kan for eksempel kreve at de skal angi ordretype, start- og/eller sluttdato for arbeidet og typen arbeid som er utført.  
* Noen standardinnstillinger for responstider og garantier. Dette omfatter standard responstid for å starte servicen, garantirabattprosenter for deler og arbeid og hvor lenge garantier er gyldige.  
* Innstillinger for kontrakter, for eksempel maksimalt antall dager du kan bruke for kontraktserviceordrer, om det skal brukes årsakskoder når en kontrakt avbrytes, standardtekster for beskrivelser og kontraktverdier.  
* Nummerserier for servicerelaterte dokumenter og varer.  

## Slik angir du generelle og obligatoriske innstillinger

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Serviceoppsett**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Definer bokføringspolicyer for servicefakturaer for brukere

Selskaper har ofte unike prosesser for fakturaer og leveringer. Prosesser kan for eksempel variere fra én person som bokfører alt i en serviceordre, til flere ansatte, som hver for seg arbeider med sine egne sider.

Du kan bruke bokføringspolicyer til å begrense brukere fra å bokføre servicefakturaer, eller kreve at de bokfører fakturaer sammen med den tilknyttede servicefølgeseddelen. For å definere en bokføringspolicy går du til siden **Brukeroppsett**, feltet **Bokføringspolicy for servicefaktura**, og velger et av følgende alternativer:

* **Tillatt** (standard): Behold gjeldende virkemåte, der du kan velge bokføringsalternativene, for eksempel **Lever**, **Fakturer** og **Lever og fakturer**.
* **Forbudt**: Hindre folk i å bokføre servicefakturaer. [!INCLUDE [prod_short](includes/prod_short.md)] viser en bekreftelsesdialogboks som bare inneholder alternativet **Lever**.
* **Obligatorisk**: La brukere bokføre fakturaer sammen med servicefølgesedler. [!INCLUDE [prod_short](includes/prod_short.md)] viser en bekreftelsesdialogboks som bare inneholder alternativet **Lever og fakturer**.

Denne innstillingen påvirker følgende dokumenter:

* Serviceordrer
* Lagerleveringer
* Servicefakturaer
* Servicekreditnotaer

Tabellen nedenfor beskriver innvirkningene på de ulike dokumentene.

|Dokument  |Tillat<br>Viser en rekke alternativer   |Forbudt<br>Bekreftelsesdialogboks  |Obligatorisk<br>Bekreftelsesdialogboks  |
|---------|---------|---------|---------|
|Serviceordre     | * Lever<br>* Fakturer<br>* Lever og fakturer<br>* Lever og forbruk         |* Lever<br>* Lever og forbruk  |Vil du bokføre leveringen og fakturaen?         |
|Lagerlevering     |* Lever<br>* Lever og fakturer         |Vil du bokføre leveringen?         | Vil du bokføre leveringen og fakturaen?        |
|Servicefaktura     | Vil du bokføre fakturaen?         | Feil: Du kan ikke bokføre.       |Vil du bokføre fakturaen?         |
|Service - kreditnota     | Vil du bokføre kreditnotaen?         | Feil: Du kan ikke bokføre.        |Vil du bokføre kreditnotaen?         |

> [!NOTE]
> Når du bokfører servicefakturaer og kreditnotaer, har du ingen bokføringsalternativer. Dokumentene bokfører alltid fysiske og økonomiske transaksjoner sammen. Du kan ikke delvis bokføre servicefakturaer og kreditnotaer.

## Se også  

[Konfigurer feilrapportering](service-how-setup-fault-reporting.md)  
[Konfigurer ressurstildeling](service-how-setup-resource-allocation.md)  
[Definere koder for standardservicer](service-how-setup-service-coding.md)  
[Definere ekstra kostnader for servicer](service-how-setup-service-costs-pricing.md)  
[Definere feilsøking](service-how-setup-troubleshooting.md)  
[Servicebehandling](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
