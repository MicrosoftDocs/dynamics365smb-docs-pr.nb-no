---
title: Innføring i Contoso Coffee-produksjon
description: Oversikt over scenarioer for hvordan Contoso Coffee-demo data kan hjelpe deg å lære hvordan du bruker produksjonsfunksjonene i Business Central.
ms.date: 04/01/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '4765,'
author: brentholtorf
ms.author: bholtorf
---

# Innføring i Contoso Coffee-produksjon

Contoso Coffee er et fiktivt selskap som produserer forbrukerkaffemaskiner og kommersielle kaffemaskiner. **Contoso Coffee**-appene for Business Central legger til demonstrasjonsdata som du kan bruke til å lære hvordan du bruker produksjonsfunksjonene i Business Central.  

Appen har fire produkter som er optimalisert for ulike scenarioer:

- **SP-SCM1009 Airpot**  

  Dette produktet er en stykkliste med en delmontering, **Ruting**. Bruk dette til å demonstrere standard produksjonsflyt. Den er definert med alternative rutinger som du kan bruke til å demonstrere ulike scenarioer som involverer underleverandører. Lagermetoden er *Standard*.  

- **SP-SCM1011 Airpot Duo**  

  Dette produktet krever varesporing og har en komponent som også krever varesporing. Lagermetoden er *Spesifikk*.  

- **SP-SCM1004 Autodrip**  

  Dette produktet er en stykkliste med en delmontering, **Ruting**. Vi anbefaler den for å demonstrere de forskjellige trekkmetodene, både for komponenter og operasjoner. Lagermetoden er *Standard*.

- **SP-SCM1006 AutoDripLite**

  Dette produktet har tre varianter og tre stykklister som kan knyttes til lagerføringsenheter. Produktet bruker fantomstykklistekonseptet. Lagermetoden er *Standard*.

Produksjonsaktivitetene for alle scenarioene bruker *HOVED*-lokasjonen.  

> [!IMPORTANT]
> Før du kjører noen av scenarioene for Contoso Coffee, må du bokføre eventuelle varekladdelinjer med åpningssaldoer. Hvis du vil ha flere krav, kan du se [Konfigurer Contoso Coffee-data](#set-up-contoso-coffee-manufacturing-data).

## Konfigurer data for Contoso Coffee-produksjon

[!INCLUDE [contoso-coffee-app-install](../../includes/contoso-coffee-app-install.md)]

|Felt  |Description  |
|---------|---------|
|**Produksjonslokasjon** |Angir lageret som du vil bruke for produksjonsoperasjoner. Standarden er *HOVED*, men du kan endre den etter behov.|


Når du er klar, velger du **Opprett demonstrasjonsdata**-handling. Det tar noen minutter å legge til dataene i den underliggende databasen, men da er du klar til å kjøre de ulike scenarioene.  

## Scenarier

Demodata for Contoso Coffee-produksjon støtter nå følgende scenarioer for test og opplæring:

1. [Opprett en ny produksjonsstykkliste og stykklisteversjon](create-new-production-bom-version.md)  
2. [Opprett en ny rute](create-new-routing.md)  
3. [Opprett en fast planlagt produksjonsordre og endre den](create-firm-planned-production-order-change.md)  
4. [Kombiner automatisk og manuell trekking](combine-automatic-manual-flushing.md)  
5. [Bruk ordreplanlegging til å opprette og reservere forsyning](order-planning-create-reserve-supply.md)  
6. [Definer og behandle en underleveranseoperasjon](set-up-process-subcontracting-operation.md)  
7. [Definer ny kapasitet](set-up-new-capacity.md)  
8. [Forutse behov for varevarianter med ulike stykklister tildelt](variants.md)  

Les trinnene for hvert scenario i den relevante artikkelen.  

> [!IMPORTANT]
> Disse gjennomgangene krever at brukeropplevelsen er satt til *Premium* på siden **Firmainformasjon**.

## Se også

[Produksjon](../../production-manage-manufacturing.md)  
[Produksjonsrapporter og analyser i Business Central](../../production-reports.md)  
