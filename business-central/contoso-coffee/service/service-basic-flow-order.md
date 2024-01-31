---
title: Gjennomgang av serviceordrer for servicevarer
description: Denne artikkelen veileder deg gjennom flere kjerneprosesser som involverer serviceordrer og varer.
author: andreipa
ms.author: andreipa
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Gjennomgang av serviceordrer for servicevarer

Denne gjennomgangen viser flere kjerneprosesser:

- Opprette en ad hoc-serviceordre og registrere reparasjon av varen
- Gi et utlånsobjekt til kunden for en reparasjonstid
- Bokføre og fakturere serviceordren
    
## Opprett en serviceordre

### Scenario  

Charles, servicelederen, oppretter en serviceordre for et reparasjonsscenario og låner ut et utlånsobjekt til kunden for reparasjonstidspunktet.

### Trinn

1. Opprett serviceordren manuelt for varen som krever reparasjon.
   1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **serviceordrer**
   2. Velg handlingen **Ny**.
   3. Skriv inn **10000** i kundenummeret. felt
   4. Velg **REPARASJON** i feltet **Serviceordretype**.
   5. Velg **S-100** som **varenr.** på linjene.
2. Valgfritt
   1. Velg Linjehandlingen **Feilsøking** for å sjekke mulige løsninger.
   2. Velg linjehandlingen **Forhold ml. feil-/løsningskoder**
   3. Velg *STØY* som **Symptomkode**
   4. Velg *5-2 Høy ulyd under brygging* som **Feilkode**, og lukk siden. Feilkode, løsningskoder oppdateres på linjer.
3. Lån ut en erstatning mens varen repareres
   1. På linjene velger du **UTLÅN1** som Utlånsobj.nr.. Bekreft utstedelsen av utlånsobjektet ved å velge **Ja** for å låne ut utlånsobjektet. 
   2. Velg funksjonshandlingen **Hent standard servicekoder**, velg standardkode som er knyttet til servicegruppen, og velg **OK**.
   
### Resultater

- Det opprettes en serviceordre for varen
- Serviceordrens servicedokumentlogg viser utlånsobjektaktivitetene.
- Utlånsobjektet har en post som gjenspeiler utlånet.
   

## Registrer utførte arbeid, merk utlåner som returnert.

### Scenario  

Serviceteknikeren markerer utlån som returnert, registrerer utført arbeid.

### Trinn

1. Finn serviceoppgaven og registrer tid 
   1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Serviceoppgaver**, og velg deretter den relaterte koblingen.
   2. Finn serviceordren du vil angi tid for.
   3. Velg handlingen **Arbeidsordre**.
   4. Angi følgende informasjon

    |Type|Nr.|Antall|
    |----|---|--------|  
    |Element|SER102|2|

   4. Velg *FERDIG* i feltet **Reparasjonsstatuskode**
    
2. Merk utlånsobjekt som returnert
   1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Utlånsobjekter** og velg den relaterte koblingen.
   2. Finn utlånsobjektet som skal merkes som returnert.
   3. Velg handlingen **Motta** 
   4. Bekreft retur av utlånsobjektet ved å velge **Ja** for å returnere utlånsobjektet.
      
### Resultater

- Serviceordrens **servicedokumentlogg** viser utlånsobjektaktivitetene.
- Utlånsobjektet har en post som gjenspeiler mottaket.


### Scenario  

Charles, servicelederen, bokfører den ferdige serviceordren.

1. Finn serviceordren 
   1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Serviceordrer**, og velg deretter den relaterte koblingen.
   2. Finn serviceordren du vil bokføre.

2. På serviceordren bokfører du fakturaen
   1. Velg handlingen **Bokfør** for å fullføre serviceordren, velg handlingen **Lever og fakturer**, og velg deretter knappen **OK**.
   2. Bekreft åpningen av den bokførte fakturaen ved å velge **Ja**. 
### Resultater

- **Bokført servicefaktura** opprettes.
- **Serviceposter** som er tilknyttet varen og ressursen, opprettes

## Se også
[Gjennomgang av servicekontrakter for servicevarer](service-contract-flow.md)  
[Tjeneste](../../service-service.md)
