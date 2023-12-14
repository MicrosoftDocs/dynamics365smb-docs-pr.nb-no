---
title: Endre årlig beløp på servicekontrakter eller kontrakttilbud
description: Du kan endre beløpet som vil bli fakturert årlig for servicekontrakten eller servicekontrakttilbud.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---
# Endre årlig beløp på servicekontrakter eller kontrakttilbud
Du kan endre årlig beløp i servicekontrakten eller kontrakttilbudet for å rette beløpet som skal faktureres hvert år.  

## Slik endrer du årlig beløp på servicekontrakten eller kontrakttilbudet  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Servicekontrakter** eller **Servicekontrakttilbud**, og velg deretter den relaterte koblingen.  
2. Velg kontrakten eller kontrakttilbudet.  
3. Velg handlingen **Åpne kontakt** for å åpne kontrakten eller kontrakttilbudet for redigering.  
4. Merk av for **Tillat beløp som ikke er i balanse** hvis du vil endre årlig beløp og fordele differansen i årlig beløp manuelt på kontraktlinjene. Hvis ikke, fjerner du merket for å fordele differansen i årlig beløp automatisk på kontraktlinjene når du har endret årlig beløp.  
5. Endre innholdet i feltet **Årlig beløp**. Du kan ikke undertegne, det vil si konvertere til servicekontrakt, hvis du arbeider på et kontrakttilbud, eller låse servicekontrakten hvis den har et negativt årlig beløp. Hvis du setter årlig beløp til null, må innholdet i feltet **Fakturaperiode** være **Ingen** enten ved undertegning eller låsing av servicekontrakten.  
6. Avhengig av om det er merket av for feltet **Tillat beløp som ikke er i balanse**, skal du bruke manuell eller automatisk fordeling av årlig beløpsdifferanse. Kontraktlinjene blir oppdatert slik at verdien i feltet **Beregnet årlig beløp** blir lik det nye årlige beløpet.  

## Distribuere forskjeller mellom nye og beregnede årlige beløp
Hvis du endrer årlig beløp på en servicekontrakt eller kontrakttilbud, må du kanskje fordele differansen mellom det nye og det beregnede årlige beløpet, på kontraktlinjene. Det finnes tre måter å fordele beløp:

* Jevn distribusjon  
* Distribusjon basert på linjebeløp  
* Distribusjon basert på fortjeneste

### Jevn distribusjon
Hvis du endrer årlig beløp på servicekontrakten eller kontrakttilbudet, vil du kanskje fordele differansen mellom det nye og det beregnede beløpet på kontraktlinjene. Jevn fordeling er én av de automatiske fordelingsmetodene som kan bidra til lik fordeling av differansen mellom nytt og beregnet årlig beløp, på linjebeløpene på kontraktlinjene. Følgende oversikt over fordelingsbehandlingen beskriver hovedtanken bak denne metoden:  

1. Differansen mellom feltverdiene i det nye **Årlig beløp** og **Beregnet årlig beløp** divideres med antall kontraktlinjer i servicekontrakten eller kontrakttilbudet.  
2. Feltet **Linjebeløp** oppdateres ved å legge til resultatet av forrige operasjon.  
3. Innholdet i feltene **Linjerabattbeløp**, **Linjerabatt-%** og **Bruttofortjeneste** oppdateres i henhold til den nye verdien i feltet **Linjebeløp**, på følgende måte:   
    * Linjerabattbeløp = Linjeverdi - Linjebeløp.  
    * Linjerabatt-% = Linjerabattbeløp / Linjeverdi * 100.  
    * Bruttofortjeneste = Linjebeløp - Linjekostnad.  

 Trinnene gjentas for hver kontraktlinje.  

#### Eksempel  
Det er ikke merket av for **Tillat beløp som ikke er i balanse** i servicekontrakten som har tre kontraktlinjer med slik informasjon.  

|Vare|Linjekostnad|Linjeverdi|Linjerabatt-%|Linjerabattbeløp|Linjebeløp|Bruttofortjeneste|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Vare 1|30,00|40,00|0,00|0,00|40,00|10,00|  
|Vare 2|40,00|50,00|10,00|5,00|45,00|5,00|  
|Vare 3|50,00|70,00|10,00|7,00|63,00|13,00|  

Verdien i feltet **Årlig beløp** er lik den i feltet **Beregnet årlig beløp**, som alltid er lik summen av linjebeløpene. I dette tilfellet er det lik følgende: 40 + 45 + 63 = 148.  

Hvis du endrer **Årlig beløp** til 139, beregner beløpet som skal legges til hver feltverdi i **Linjebeløp**. Dette beløpet beregnes ved å trekke **Beregnet årlig beløp** fra den nye verdien i feltet **Årlig beløp** og dividere resultatet med antall kontraktlinjer i servicekontrakten. I dette tilfellet vil det være lik følgende: (139 - 148) / 3 = -3. Deretter legges det sist beregnede tallet til i hver verdi i **Linjebeløp**-feltet, og verdiene i feltene **Linjerabatt-%**, **Linjerabattbeløp**, og **Fortjeneste** oppdateres ved hjelp av formlene i fremgangsmåten som beskrives ovenfor.  

Til slutt viser kontraktlinjene disse dataene.  

|Vare|Linjekostnad|Linjeverdi|Linjerabatt-%|Linjerabattbeløp|Linjebeløp|Bruttofortjeneste|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Vare 1|30,00|40,00|7,50|3,00|37,00|7,00|  
|Vare 2|40,00|50,00|16.00|8.00|42.00|2.00|  
|Vare 3|50.00|70.00|14.29|10.00|60.00|10.00|  

### Distribusjon basert på linjebeløp
Hvis du endrer årlig beløp på servicekontrakten eller kontrakttilbudet, vil du kanskje fordele differansen mellom det nye og det beregnede beløpet på kontraktlinjene. Fordeling basert på linjebeløp er en automatiske metode som kan hjelpe deg å fordele differansen mellom nytt og beregnet årlig beløp, på linjebeløpene på kontraktlinjene. Denne fordelingen utføres proporsjonalt med linjebeløpsandelen i det beregnede årlige beløpet. Følgende oversikt over fordelingsbehandlingen for hver kontraktlinje, beskriver hovedtanken bak denne metoden:  

1. Prosentfordeling etter linjebeløp beregnes slik: Innholdet i feltet **Linjebeløp** divideres med summen av feltverdiene i **Beregnet årlig beløp** på alle kontraktlinjer.  
2. Feltverdien i **Linjebeløp** oppdateres ved addisjon av differansen mellom det nye årlige beløpet og det beregnede årlige beløpet. Deretter multipliseres det med prosentfordelingen for linjebeløp.  
3. Innholdet i feltene **Linjerabattbeløp**, **Linjerabatt-%** og **Bruttofortjeneste** oppdateres i henhold til den nye verdien i feltet **Linjerabattbeløp**, på følgende måte:  

    * Linjerabattbeløp = Linjeverdi - Linjebeløp  
    * Linjerabatt-% = Linjerabattbeløp / Linjeverdi * 100.  
    * Fortjeneste = Linjebeløp - Linjekostnad  

Trinnene gjentas for hver kontraktlinje.  

#### Eksempel  
Det er ikke merket av for **Tillat beløp som ikke er i balanse** i servicekontrakten som har tre kontraktlinjer med slik informasjon.  

|Vare|Linjekostnad|Linjeverdi|Linjerabatt-%|Linjerabattbeløp|Linjebeløp|Bruttofortjeneste|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Vare 1|15,00|17,00|3,00|0,51|25,00|1,49|  
|Vare 2|20,00|23,00|Ingen|0,00|55,10|3,00|  
|Vare 3|24,00|27,00|3,00|0,81|112,70|2,19|  

Verdien i feltet **Årlig beløp** er lik den i feltet **Beregnet årlig beløp**, som alltid er lik summen av linjebeløpene. I dette tilfellet er det lik følgende: 16,49 + 23,00 + 26,19 = 65,68.  

Hvis du endrer **Årlig beløp** til 60, beregnes prosentfordelingen av bruttofortjenesten for hver kontraktlinje:  

* Vare 1 – 5 / (5 + 5,1 +12,7) = 0,2193 %  
* Vare 2 – 5,1 / (5 + 5,1 + 12,7) = 0,2237  
* Vare 3 – 12.7 / (5 + 5,1 +12,7) = 0,557 %  

Verdien i feltet **Linjebeløp** oppdateres på hver kontraktlinje ved bruk av følgende formel: Linjebeløp = Linjebeløp + differansen mellom nytt og beregnet årlig beløp * Prosentfordeling. Deretter oppdateres feltverdiene i **Linjerabattbeløp**, **Linjerabatt-%** og **Bruttofortjeneste** ved bruk av formelen som er beskrevet i fremgangsmåten ovenfor.  

Til slutt viser kontraktlinjene disse dataene.  

|Vare|Linjekostnad|Linjeverdi|Linjerabatt-%|Linjerabattbeløp|Linjebeløp|Bruttofortjeneste|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Vare 1|15,00|17,00|11,41|1,94|15,06|0,06|  
|Vare 2|20,00|23,00|8.65|1.99|21.01|1.01|  
|Vare 3|24.00|27.00|11.37|3.07|23.93|-0,07|  

### Distribusjon basert på fortjeneste
Hvis du endrer årlig beløp på servicekontrakten eller kontrakttilbudet, vil du kanskje fordele differansen mellom det nye og det beregnede beløpet på kontraktlinjene. Fordeling basert på bruttofortjeneste er en av de automatiske metodene som hjelper deg å fordele differansen mellom nytt og beregnet årlig beløp, på linjebeløpene på kontraktlinjene. Denne fordelingen blir utført proporsjonalt med linjenes andel av totalkontraktens eller kontrakttilbudets bruttofortjeneste. Følgende oversikt over fordelingsbehandlingen for hver kontraktlinje, beskriver hovedtanken bak denne metoden:  

1. Prosentfordelingen av bruttofortjenesten beregnes slik: innholdet i feltet **Bruttofortjeneste** divideres med summen av feltverdiene i **Bruttofortjeneste**, på alle kontraktlinjer.  
2. Feltverdien i **Linjebeløp** oppdateres ved addisjon av differansen mellom det nye årlige beløpet og det beregnede årlige beløpet. Deretter multipliseres det med prosentfordelingen for bruttofortjeneste.  
3. Innholdet i feltene Linjerabattbeløp, Linjerabatt-% og Bruttofortjeneste oppdateres i henhold til den nye verdien i feltet **Linjebeløp**, på følgende måte:  

    * Linjerabattbeløp = Linjeverdi - Linjebeløp  
    * Linjerabatt-% = Linjerabattbeløp / Linjeverdi * 100.  
    * Fortjeneste = Linjebeløp - Linjekostnad  

#### Eksempel  
Det er ikke merket av for **Tillat beløp som ikke er i balanse** i servicekontrakten som har tre kontraktlinjer med slik informasjon.  

|Vare|Linjekostnad|Linjeverdi|Linjerabatt-%|Linjerabattbeløp|Linjebeløp|Bruttofortjeneste|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Vare 1|20,00|25,00|0,00|0,00|25,00|5,00|  
|Vare 2|50,00|58,00|5,00|2,90|55,10|5,10|  
|Vare 3|100,00|115,00|2,00|2,30|112,70|12,70|  

Verdien i feltet **Årlig beløp** er lik den i feltet **Beregnet årlig beløp**, som alltid er lik summen av linjebeløpene. I dette tilfellet er det lik følgende: 25,00 + 55,10 + 112,70 = 192,80.  

 Hvis du endrer **Årlig beløp** til 180, beregnes prosentfordelingen av bruttofortjenesten for hver kontraktlinje:  

* Vare 1 – 5 / (5 + 5,1 +1 2,7) = 0,2193 %  
* Vare 2 – 5,1 / (5 + 5,1 + 12,7) = 0,2237  
* Vare 3 – 12.7 / (5 + 5,1 +12,7) = 0,557 %  

Verdien i feltet **Linjebeløp** oppdateres på hver kontraktlinje ved bruk av følgende formel: Linjebeløp = Linjebeløp + differansen mellom nytt og beregnet årlig beløp * Prosentfordeling. Deretter oppdateres feltverdiene i **Linjerabattbeløp**, **Linjerabatt-%** og **Bruttofortjeneste** ved bruk av formelen i trinn 3 i fremgangsmåten som er beskrevet ovenfor.  

Til slutt viser kontraktlinjene disse dataene.  

|Vare|Linjekostnad|Linjeverdi|Linjerabatt-%|Linjerabattbeløp|Linjebeløp|Bruttofortjeneste|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Vare 1|20,00|25,00|11,24|2,81|22,19|2,19|  
|Vare 2|50,00|58,00|9.93|5.76|52.24|2.24|  
|Vare 3|100.00|115.00|8.20|9.43|105.57|5.57|  

## Se også  
[Opprette servicekontrakter og servicekontrakttilbud](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Konfigurere servicehåndtering](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]