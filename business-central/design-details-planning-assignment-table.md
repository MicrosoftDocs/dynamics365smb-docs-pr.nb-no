---
title: Designdetaljer – Tabell for planleggingstilordning | Microsoft-dokumentasjon
description: Dette emnet gir innsikt i hva som skjer når du endrer hvordan du planlegger for en vare.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c98e89340ac85f48a4341ac9c9b714c1135db683
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5390827"
---
# <a name="design-details-planning-assignment-table"></a>Designdetaljer: Tabell for planleggingstilordning
Det må planlegges for alle varer, men det er ingen grunn til å beregne en plan for en vare med mindre det er en endring i mønsteret for behov eller forsyning siden planen sist ble beregnet.  

Hvis brukeren har angitt en ny ordre eller endret en eksisterende, er det grunn til å beregne planen på nytt. Andre årsaker inkluderer en endring i prognosen eller ønsket sikkerhetslagerantall. Endring av en stykkliste ved å legge til eller fjerne en komponent, vil mest sannsynlig indikerer en endring, men bare for komponentvaren.  

For flere lokasjoner foregår tildelingen på nivået for en vare per lokasjonskombinasjon. Hvis det for eksempel er opprettet en ordre på bare én lokasjon, vil programmet tilordne varen på denne spesifikke lokasjonen for planlegging.  

Grunnen til å velge varer for planlegging har å gjøre med systemytelsen. Hvis det ikke har oppstått endringer i en vares behov-/ forsyningsmønster, foreslår vil ikke planleggingssystemet foreslå handlinger som skal utføres. Uten planleggingstilordningen måtte systemet ha utført beregningene for alle varer for å finne ut hva det skal planlegge for, og dette hadde tappet systemressursene.  

Tabellen **Planleggingstilordning** overvåker behovs- og forsyningshendelser og tilordner de riktige varene for planlegging. Følgende hendelser overvåkes:  

* En ny ordre, prognose, komponent, bestilling, produksjonsordre, monteringsordre eller overføringsordre.  
* Endring av vare, antall, lokasjon, variant eller dato på en ordre, prognose, komponent, bestilling, produksjonsordre, monteringsordre eller overføringsordre.  
* Annullering av en ordre, prognose, komponent, bestilling, produksjonsordre, monteringsordre eller overføringsordre.  
* Forbruk av varer som ikke er planlagt.  
* Avgang av varer som ikke er planlagt.  
* Ikke planlagte endringer på lageret.  

For disse direkteforskyvningene for forsyning/behov vedlikeholder ordresporings- og handlingsmeldingssystemet tabellen Planleggingstilordning, og angir en planleggingsårsak som en handlingsmelding.  

Følgende endringer i hoveddata kan også føre til en ubalanse i planleggingen:  

* Endring av status til Sertifisert i produksjonsstykklistehodet (for alle varer som bruker hodet).  
* Slettet linje (underordnet vare).  
* Endring av status til Sertifisert i rutehodet (for alle varer som bruker rutingen).  
* Endringer i følgende varekortfelt.  
* Sikkerhetslagerantall eller Sikkerhetsleveringstid.  
* Beregning av leveringstid.  
* Gjenbestillingspunkt.  
* Produksjonsstykklistenummer (og alle underordnede for gammel stykklistereferanse).  
* Rutenr.  
* Gjenbestillingsprinsipp.  

I slike tilfeller vil en ny funksjon, Behandle planleggingstilordning, opprettholde tabellen og angir planleggingsårsaken som Bevegelse.  

Følgende endringer fører ikke til en planleggingstilordning:  

* Kalendere  
* Andre planleggingsparametre på varekortet:  

Følgende begrensninger gjelder ved beregning av MPS eller MRP:  

* MPS: Planleggingssystemet kontrollerer at varen har en behovsprognose eller en ordre. Hvis ikke, inkluderes ikke varen i planen.  
* MRP: Hvis planleggingssystemet oppdager at varen etterfylles av en MPS-planleggingslinje eller MPS-forsyningsordre, blir varen utelatt fra planleggingen. Eventuelle behov fra aktuelle komponenter er imidlertid inkludert .  

## <a name="see-also"></a>Se også  
[Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md)   
[Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md)   
[Designdetaljer: Overføringer i planlegging](design-details-transfers-in-planning.md)   
[Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]