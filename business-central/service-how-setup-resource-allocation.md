---
title: Definere ressurstildeling | Microsoft-dokumentasjon
description: Finn ut hvordan systemet kan sørge for at du tilordner en person som ikke har de nødvendige kompetansen til å yte service.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'resource, skill, service, zones'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Definere ressurstildeling
For å sikre at en serviceoppgave utføres tilfredsstillende, er det viktig å finne en ressurs som er kvalifisert for å gjøre arbeidet. Du kan definere [!INCLUDE[prod_short](includes/prod_short.md)], slik at det er enkelt å tildele en person som har riktig kompetansen for prosjektet. I [!INCLUDE[prod_short](includes/prod_short.md)] kaller vi dette _ressurstildeling_. Du kan tildele ressurser basert på kompetanse, tilgjengelighet eller om de er i samme servicesone som kunden. 

Hvis du vil bruke ressurstildeling, må du definere:  
  
* Kompetansene som kreves for å reparere og vedlikeholde servicevarer. Du tilordner disse til servicevarer og ressurser.  
* Geografiske områder, som kalles soner, som du definerer for markedet. Det kan for eksempel være øst, vest, midten og så videre. Du tilordner disse til kunder og ressurser.  
* Om du vil vise ressurskompetanse og soner, og om det skal vises en advarsel hvis noen velger en ukvalifisert ressurs eller en ressurs som ikke er i kundesonen.  

## Definere kompetanser
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kompetanse** og velger den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Du tilordner disse til servicevarer og ressurser.
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Servicevarer** eller **Ressurser** og velg den relaterte koblingen.  
2. Åpne kortet for servicevaren eller ressursen, og velg deretter ett av følgende:  
  
    * For servicevarer velger du **Ressurskompetanse**.  
    * For ressurser velger du **Kompetanse**.  

## Definere soner
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Soner**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Tilordne soner til kunder og ressurser 
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kunder** eller **Ressurser** og velg den relaterte koblingen.  
2. Åpne kortet for servicevaren eller ressursen, og velg deretter ett av følgende:  
  
    * For kunder velger du en sone i feltet **Servicesonekode**.  
    * For ressurser velger du handlingen **Servicesoner**.  

## Angi hva som skal vises når en ressurs er valgt
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Serviceoppsett**, og velg deretter den relaterte koblingen. 
2. I feltet **Alt. for ressurskompetanse** velger du ett av alternativene som er beskrevet i tabellen nedenfor.  
  
    |**Alternativ**|**Beskrivelse**|  
    |------------|-------------|  
    |Vis kode | Viser bare koden.|  
    |Vis advarsel | Viser informasjonen og en advarsel hvis du velger en ressurs som ikke er kvalifisert.|  
    |Ikke i bruk | Viser ikke denne informasjonen.|  

## Oppdatere ressurskapasitet  
Du må kanskje endre kapasiteten for ressurser.  
  
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Ressurskapasitet** og velg den relaterte koblingen.  
2. Velg ressursen, og velg deretter handlingen **Angi kapasitet**.  
3. Utfør endringen, og velge deretter **Oppdater kapasitet**.  

## Oppdatere kompetanse for varer, servicevarer eller servicevaregrupper
Hvis du vil endre kompetansekodene som er tilordnet til varer, for eksempel fra **PC** til **PCS**, kan du gjøre dette for en vare, servicevare eller for alle varer i en servicevaregruppe.  
  
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** eller **Servicevare** eller **Servicevaregruppe**, og velg deretter relatert kobling.  
2. Velg enheten som skal oppdateres, og velg deretter handlingen **Ressurskompetanse**.  
3. På linjen med koden som skal endres, velger du den relevante kompetansekoden i **Kompetansekode**-feltet.  
4.  Hvis varen har tilordnede servicevarer, åpnes det en dialogboks med følgende to alternativer:  
  
    * Endre kompetansekodene til den valgte verdien: Velg dette alternativet hvis du vil erstatte den gamle kompetansekoden med den nye for alle relaterte servicevarer.  
    * Slett kompetansekodene eller oppdater relasjonen: Velg dette alternativet hvis du vil endre kompetansekoden bare for denne varen. Kompetansekoden for relaterte servicevarer tilordnes på nytt, dvs. at **Tilordnet fra**-feltet blir oppdatert.  
  
## Se også
[Tildele ressurser](service-how-to-allocate-resources.md)  
[Konfigurere arbeidstimer og servicetimer](service-how-setup-work-service-hours.md)  
[Konfigurere feilrapportering](service-how-setup-fault-reporting.md)  
[Definere koder for standardservicer](service-how-setup-service-coding.md)  
 



[!INCLUDE[footer-include](includes/footer-banner.md)]