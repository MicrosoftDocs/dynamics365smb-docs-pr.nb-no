---
title: Gjennomgang av servicekontrakter for servicevarer
description: Denne artikkelen veileder deg gjennom ulike scenarier som involverer servicevarer og kontrakter.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 11/08/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Gjennomgang av servicekontrakter for servicevarer

Denne gjennomgangen viser flere kjerneprosesser:

- Opprettelse av servicevarer gjennom salg
- Opprette og fakturere for en servicekontrakt
- Opprette en serviceordre for en servicekontrakt
- Tilordne en ressurs basert på kompetanse og sone
- Fullføre tidsregistreringen for serviceordren
- Bokføre og fakturere kontraktserviceordren

## Opprett servicevarer

### Scenario  

Susan, ordrebehandleren, bokfører en ordre og selger en vare som er konfigurert til å generere en servicevare.  

### Trinn

1. Kontroller at **Servicevaregruppe** er valgt for **Vare** .
   
    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.  
    2. Velg elementet *S-100* og åpne det.
    3. Kontroller verdien i feltet **Servicevaregruppe**.
       
2. Bokfør **Salgsordre** for å opprette servicevaren for kunden.  

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.  
    2. Velg ordren for kunde 10000. Det eksterne ordrenr. er *SVC-1*.
    3. Velg **Bokfør**-handlingen for å sende varen til kunden.

### Resultater

- Det opprettes en servicevare for kunde 10000

##  Fakturer en servicekontrakt

### Scenario

Charles, servicelederen, oppretter deretter en servicekontrakt som skal faktureres for regelmessige vedlikeholdsbesøk.

3. Opprette **Servicekontrakt** for den nye servicevaren
    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Servicekontrakter**, og velg deretter den relaterte koblingen.
    2. Velg handlingen **Ny**.  
    3. I bekreftelsesdialogboksen velger du **Ja** for å opprette kontrakt ved hjelp av mal. 
    4. Velg *Ikke-for.bet. kontr. – månedlig*.
    5. På hurtigfanen Service, i **Serviceordretype**, angir du **VEDLIKH**.
    6. På linjene skriver du inn følgende informasjon:

    |Servicevarenr.|Linjeverdi|  
    |----------------|----------|  
    |SV000001|6000|

    7. Velg **Signer kontrakt**-handlingen, og bekreft signeringen.
    8. Velg **Ja** for å bekrefte opprettelsen av en servicefaktura. Du mottar en bekreftelsesmelding med servicefakturanummeret.

3. Bokfør servicefakturaen
   1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Servicefakturaer**, og velg deretter den relaterte koblingen.
   2. Finn servicefakturaen, og velg **Bokfør**-handlingen.

### Resultater

- En signert servicekontrakt opprettes med vareposter
- En bokført servicefaktura opprettes

## Opprett en serviceordre for en servicekontrakt og tildel ressurser

### Scenario  

Charles, servicelederen, oppretter serviceordrene for vanlige vedlikeholdsordrer under servicekontrakten og ser deretter gjennom servicefordelingen for å tilordne dem.

### Trinn

1. Kjør serviceordrene som skal oppfylle forpliktelsene i aktive servicekontrakter.
   1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Opprett kontraktserviceordrer**, og velg deretter den relaterte koblingen.
   2. Angi start- og sluttdato for måneden i feltene Startdato og Sluttdato på hurtigfanen Alternativer
   3. Velg **OK** for å bekrefte opprettelsen av en serviceordrer. Du mottar en bekreftelsesmelding med antallet opprettede serviceordrer.

2. Gå gjennom ordrene som venter på oppdrag via Servicefordelingen
   1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Servicefordeling** og velg den relaterte koblingen.
   2. Servicefordeling viser alle åpne serviceordrer sammen med **Ant. tildelinger** for å vise om serviceordrene er tildelt til en ressurs.
   3. Velg handlingen **Vis dokumenter** for å åpne en serviceordre.  Du ser at faktaboksen Servicevarelinjer viser hvilke ressurser som er kompetente til å arbeide med denne varen.

3. Tilordne en ressurs til serviceordren
   1. Fra serviceordren velger du linjehandlingen **Ressurstildelinger**
   2. Skriv inn følgende informasjon for tilkoblingen fra ressurstildeling

    |Servicevarenr.|Ressursnr.|Tildelingsdato|Tildelte timer|
    |----------------|------------|---------------|---------------|  
    |SV000001|RESOURCE1|d|1|

    3. Tildelingen endres til statusen Aktiv.
    4. Oppdatering av servicefordeling viser **Ant. tildelinger** endret fra 0 til 1 for serviceordren.

### Resultater

- Serviceordrer opprettes for servicekontraktene
- Serviceordrene tildeles til en ressurs for å fullføre arbeidet

## Fullfør tidsregistreringen for serviceordren og bokføre serviceordren

### Scenario  

Serviceteknikeren registrerer tiden direkte mot serviceordren og merker deretter ordren som ferdig.

> [!NOTE]
> Tidsoppføring for serviceordrer kan angis via timelister. For mer informasjon, se [lenke til timeliste hvis denne merknaden gir mening].

### Trinn

1. Finn serviceordren, og angi klokkeslettet i servicelinjen
   1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Serviceordrer**, og velg deretter den relaterte koblingen.
   2. Finn serviceordren du vil angi tid for.
   3. Velg linjehandlingen **Servicelinje**.
   4. Angi følgende informasjon

    |Type|Nr.|Antall|Antall til forbruk|
    |----|---|--------|--------|   
    |Ressurs|RESOURCE1|2|2|

2. På serviceordren bokfører du forbruket
   1. Velg handlingen **Bokfør** for å fullføre serviceordren, velg handlingen **Lever og forbruk**, og velg deretter knappen **OK**.

### Resultater

- Serviceposter opprettes knyttet til servicevaren, servicekontrakten og ressursen

## Se også

[Innføring i demodata for Contoso Coffee](../../contoso-coffee/contoso-coffee-intro.md)  
[Om produksjonsordrer](../../production-about-production-orders.md)