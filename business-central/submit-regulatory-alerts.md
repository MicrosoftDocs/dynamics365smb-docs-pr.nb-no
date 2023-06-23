---
title: Sende forskriftsmessige varsler
description: 'Hvis du vet om ny lovgivning som krever funksjonsstøtte i Business Central, kan du følge denne veiledningen for å sende et forskriftsmessig varsel til produktteamet.'
author: sorenfriisalexandersen
ms.topic: conceptual
ms.reviewer: edupont
ms.search.keywords: null
ms.date: 06/25/2021
ms.author: soalex
---
# Sende varsler om lands-/regionsspesifikke forskriftsmessige funksjoner

Vi anbefaler at du bruker Microsoft Dynamics Lifecycle Services (LCS) til å sende lovmessige varsler gjennom tjenesten Forskriftsmessig Dynamics-varselsending.  

## Sende forskriftsmessig varsel i LCS

1. Gå til [https://lcs.dynamics.com](https://lcs.dynamics.com) og logg på  

    Du vil se prosjektene du har tilgang til.

2. Velg prosjektet **Forskriftsmessige varsler – globalt**

    Dette åpner prosjektet og viser en rekke ting relatert til dette prosjektet

3. Velg **Varseltjeneste** på høyre side i delen **Flere verktøy**

    Det vises en oversikt over varsler med overskriften **Forskriftsmessig Dynamics-varselsending**

4. Du kan legge til et nytt varsel ved å klikke på plusstegnet **(+)** på toppen av listen

    Her får du en firetrinns veiledning for hvordan du oppretter varselet. Veiledningen har følgende trinn:
    - Søke etter eksisterende elementer

        Søk etter informasjon du synes er relevant for varselet du vil opprette. Hvis du ikke finner noen relevante søkeresultater, kan du velge knappen **Send forskriftsmessig varsel** nederst på siden for å gå videre med varselinnsendingen.
    - Knytte til forretningsprosesser

        Denne delen er ikke er relevant for Dynamics 365 Business Central. Velg **Hopp over** for å gå til neste trinn.
    - Beskriv varselet

        Angi informasjon om varselet i de gjeldende feltene. Nødvendige felt angis med en rød stjerne (\*) i veiledningen.

        |Felt        |Description                               |
        |-------------|------------------------------------------|
        |Tittel  | Angi en beskrivende tittel for å identifisere det berørte området. For eksempel angi *Endringer i fakturadokumentet per 1. juli 2019*. |
        |Description  | Angi en kort oversikt av loven. Beskrivelsen må fokusere på problemer som er relevante for ERP-aktiviteter, slik at brukere kan forstå kravene på høyt nivå uten å måtte lese lovgivningen først.|
        |Land  | Angi landet eller regionen lovgivningen gjelder for.|
        |Bransje| Angi bransje hvis behovet bare gjelder for bestemte bransjer. Velg for eksempel **Offentlig sektor**, **Detaljhandel**, eller **Produksjon**.|
        |Funksjonsreferanse  | Dette er relevant for Dynamics 365 Business Central, men du kan angi en funksjonsreferanse hvis du kjenner den. Listen over funksjoner for det bestemte landet finner du i [Lokaliseringsportal](/dynamics/s-e/) på området CustomerSource. |
        |Dato for håndhevelse av lov  | Angi datoen når berørte kunder må begynne å overholde loven.|
        |Offentlig kunngjøringsdato  | Angi datoen myndighetene skal kunngjøre endringen.|
        |Siste registreringsdato  | Velg fristen for den første sendingen av den nye eller endrede rapporten.|
        |Koble til lovgivningen  | Angi én eller flere koblinger til den publiserte loven, tolkningsretningslinjer, implementeringsretningslinjer eller annen nyttig dokumentasjon som hjelper brukere med å forstå eller implementere kravet.|
        |Selskapsnavn  | Fylle ut firmanavnet for personen som sender varselet.|
        |Kontaktnavn  | Fyll ut navnet på personen som sender varselet. |
        |E-postadresse for kontakt  | E-postadressen til personen som sender varselet.|
        |Forretningsprosess  | Forretningsprosesser som du valgte gjennom veiviseren for **varselinnsendingen**|
        |Kommentarer  | Angi flere opplysninger som kan hjelpe brukerne med å forstå eller implementere kravet. Klikk **Send** for å lagre kommentaren. Flere merknader kan legges til og bør sendes separat. Merknader lagres i rekkefølgen de blir lagt til i. |
        |Jeg vil se ...  | Klikk på knappen **Last opp**, og bla deretter for å velge en fil som skal legges til som et vedlegg. Når du har valgt filen, lastes den opp og vises som en tilknyttet fil. Du kan legge til opptil tre filer som har en størrelsen på 5 MB. For å slette filer som er tilknyttet, klikk på **Fjern** under navnet på filen. Vedlegg må være offentlig tilgjengelige materialer. De kan ikke være proprietære eller kundespesifikke/partnerspesifikk.|

        Klikk **Send** for å lagre og sende varselet.

        Hvis du ikke har alle de nødvendige opplysningene, eller hvis du ennå ikke er klar til å sende varselet, kan du lagre et delvis fullført varsel.

    - Bekreftelse på innsending

      Når du har sendt varselet, får du en bekreftelse på at varselet er sendt til Microsoft.

## Se også

[Lokal funksjonalitet i [!INCLUDE[prod_long](includes/prod_long.md)]](about-localization.md)  
[Endre språk og nasjonal innstilling](about-locale-language.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Velkommen til Business Central](welcome.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]