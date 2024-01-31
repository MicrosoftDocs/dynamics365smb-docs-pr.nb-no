---
title: Serviceprisstyring
description: 'Med serviceprisstyring kan du definere serviceprisgrupper, servicepriser, serviceprisjustering og mer.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Serviceprisstyring
Med funksjonen for serviceprisstyring kan du bruke best pris på serviceordrer, definere tilpassede serviceprisavtaler for kunder, øke de ansattes effektivitet og fremskynde faktureringsprosessen.  
  
Med serviceprisstyring kan du definere forskjellige serviceprisgrupper, slik at du kan ta hensyn til servicevaren eller servicevaregruppen, i tillegg til feiltypen som berører serviceoppgaven. Du kan definere disse gruppene for en begrenset tidsperiode, eller for en bestemt kunde eller valuta. Du kan bruke prisberegningsstrukturer som maler for å tildele en bestemt pris til en bestemt serviceoppgave.  
  
Dette gjør det for eksempel mulig å tildele bestemte varer som er inkludert i serviceprisen, samt typen arbeid som er inkludert. Dette gjør det også mulig å bruke forskjellige merverdiavgifts- og rabattsatser for forskjellige serviceprisgrupper. For å sikre at riktige priser blir brukt, kan du tildele faste, minste og høyeste pris, avhengig av avtalene du har med kundene.  
  
Før prisen på en servicevare i en serviceordre justeres, får du oversikt over hvordan resultatet av prisjusteringen blir. Du kan godta dette resultatet, eller du kan foreta flere endringer hvis du ønsker et annet resultat. Hele justeringen utføres linje for linje, noe som betyr at det ikke opprettes noen ekstra linjer.  
  
Og til sist kan du bruke standardrapporter og statistikk for serviceprisgrupper til å holde oversikt over lønnsomheten for hver serviceprisgruppe.  
  
## Serviceprisjusteringsgrupper  
Du kan bruke serviceprisjusteringsgrupper til å definere de forskjellige typene av prisjusteringer for servicelinjer. Du kan for eksempel definere en serviceprisjusteringsgruppe som justerer prisene for reservedeler, en som justerer prisene på arbeid, en som justerer prisene for kostnader og så videre. Du kan også definere om serviceprisjusteringen skal gjelde bare for én bestemt vare eller ressurs, eller for alle varer eller ressurser.  
  
Prisjusteringsfunksjonen kan ikke brukes på servicevarer som under følgende betingelser:

* Varen tilhører servicekontrakter. Du kan bare justere serviceprisene for varer som er del av en serviceordre. 
* Hvis servicevaren har en garanti. 
* Hvis servicelinjen er bokført som faktura, enten helt eller delvis.  
  
Når du bruker funksjonen for serviceprisjustering, erstattes alle rabatter i ordren med verdier fra serviceprisjusteringen.  
  
## Serviceprisgrupper  
Du kan definere serviceprisgrupper for å opprette grupper med servicevarer som skal ha samme spesielle serviceprissetting. Når du har definert serviceprisgrupper, kan du tilordne dem til servicevarer på servicevarelinjer. Du kan dessuten tilordne serviceprisgrupper til servicevaregrupper.  
  
Før du kan tildele en serviceprisgruppe til en servicevare, må du bestemme for hvilket feilområde, hvilken valuta eller serviceprisjusteringsgruppe serviceprisgruppen skal gjelde. Du må bestemme hvilket beløp prisjusteringen skal justere til, og om dette beløpet skal være inkludert merverdiavgift og rabatter. Du må dessuten bestemme om denne justeringen skal gjelde et fast beløp, eller bare skal gjelde ved bestemte forhold.  
  
Når du tildeler en serviceprisgruppe til en servicevare, vil all spesiell serviceprissetting som du definerer i denne gruppen, gjelde for denne servicevaren.  
  
## Serviceprissetting  
Du definerer de faktiske typene serviceprissetting (prisjusteringstype og pris) for en kombinasjon av serviceprisgrupper og kundeprisgrupper. Du velger en prisjusteringsgruppe for hver enkelt type serviceprissetting. Du angir dessuten prisjusteringstypen (fast, maksimal eller ingen) og den faktiske prisen.  
  
Du kan for eksempel definere typer med serviceprissetting for en serviceprisgruppe for radio. For kunder uten en prisgruppe kan du fastsette å bruke serviceprissetting med maksimalpris på arbeid, som er prisjusteringsgruppen for arbeid. For kunder med en bestemt prisgruppe kan du beslutte å bruke serviceprissetting med en fast pris på arbeid, den samme prisjusteringsgruppen for arbeid.  

#### [Nåværende opplevelse](#tab/current-experience)
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Servicevarer**, og velg deretter den relaterte koblingen.  
2. Velg servicevaren, utvid hurtigfanen **Priser og salg**, og velg handlingen **Ressurs**, **Vare** eller **Finanskonto**.
3. Fyll ut feltene etter behov på sidene **Ressurspriser for prosjekt**, **Varepriser for prosjekt** og **Finanskontopriser for prosjekt**.

  
## Serviceprisjustering  
Med serviceprisjustering kan du justere prisen på en vare, ressurs, finanskonto eller kostnad på en serviceordre.  
  
Når du har angitt en vare på servicevarelinjen, angir du alle opplysninger om kostnadene for denne varen på servicelinjene. Når du kjører funksjonen Juster servicepris, kan du forhåndsvise prisjusteringene. Du kan gjøre endringer hvis du må. Når du godkjenner endringene, beregnes justeringene før de overføres til servicelinjene. Deretter bokfører du serviceordren.  
  
Avhengig av prisjusteringstype beregnes det samlede beløpet for justeringene.  
  
Tabellen nedenfor beskriver beregningene.  
  
|Alternativ | Beskrivelse |  
|----------------------------------|---------------------------------------|  
|**Fast pris**|Dette betyr at du forlanger en fast pris for servicevaren, ressursen, finanskontoen eller kostnaden, uavhengig av faktiske kostnader eller normale priser. Valg av dette alternativet betyr at serviceprisjusteringen vil gi det eksakte beløpet som er angitt i serviceprisgruppen.|  
|**Maksimum**|Dette betyr at du setter en øvre grense på prisen til kunden, uavhengig av faktiske kostnader eller normale priser. Valg av dette alternativet betyr at serviceprisjusteringen bare utføres hvis den samlede prisen overstiger beløpet som er angitt i serviceprisgruppen.|  
|**Minimum**|Dette betyr at du setter en nedre grense på prisen til kunden, uavhengig av faktiske kostnader eller normale priser. Valg av dette alternativet betyr at serviceprisjusteringen bare utføres hvis den samlede prisen er lavere enn beløpet som er angitt i serviceprisgruppen.|  
  
## Se også  
[Definere priser og ekstra kostnader for servicer](service-how-setup-service-costs-pricing.md)  
[Konfigurere servicehåndtering](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]