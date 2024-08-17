---
title: Business Central-tilgang med Microsoft 365-lisenser
description: 'Finn ut hvordan brukerne kan få tilgang til Business Central-data, for eksempel i Microsoft Teams-nettpratvinduer og -kanaler, med bare en Microsoft 365-lisens, men ingen Business Central-lisens.'
author: mikebc
ms.author: mikebc
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: overview
ms.date: 06/06/2024
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---

# Business Central-tilgang med Microsoft 365-lisenser

[!INCLUDE[prod_short](includes/prod_short.md)]-brukere tildeles en Dynamics 365 Business Central-lisens som gjør at de kan vise, endre og handle med forretningsdata fra et hvilket som helst brukergrensesnitt. For alle andre ansatte på tvers av organisasjonen som bare trenger å vise data av og til, gir Business Central tilgang gjennom Microsoft 365.  

Når en organisasjon har både et Dynamics 365 Business Central- og Microsoft 365-abonnement, kan de konfigurere miljøer til å gi tilgang med Microsoft 365-lisenser og deretter velge nøyaktig hvilke tabeller og andre objekter denne kategorien av brukeren skal ha tilgang til. Når de er konfigurert, kan ansatte som har en Microsoft 365-lisens, men ingen [!INCLUDE [prod_short](includes/prod_short.md)]-lisens, vise [!INCLUDE [prod_short](includes/prod_short.md)]-oppføringer som deles med dem i Microsoft Teams-nettprat og -kanaler.

## Hvorfor aktivere tilgang med Microsoft 365-lisenser  

- Få tilgang til hoveddata som hver enkelt ansatt i organisasjonen skal ha tilgang til.

- Gi avdelinger som ikke kan kjøre på [!INCLUDE [prod_short](includes/prod_short.md)], muligheten til selvbetjening ved å få tilgang til nøkkeldataene som trengs for å utføre oppgavene sine, noe som eliminerer behovet for kontinuerlig å be om data fra andre.

- Øk samarbeidseffektiviteten slik at oppgaver og prosjekter som går over flere avdelinger, fullføres i tide, ved å eliminere friksjonen som vanligvis er knyttet til nektet tilgang på grunn av lisensiering.

- Øk teamytelsen slik at brukere kan foreta datadrevne beslutninger som er inkluderende for alle i gruppen, selv om de ikke arbeider i [!INCLUDE [prod_short](includes/prod_short.md)].

- Oppfyll lisensbudsjettmål ved å tildele lisenser som progressivt samsvarer med de ansattes behov, med Microsoft 365-lisenser for skrivebeskyttet tilgang, Dynamics 365 Business Central Team Member-lisenser for begrenset skrivetilgang og Dynamics 365 Business Central Essentials eller Premium for full skrivetilgang.

- Forbedre datasikkerheten ved å redusere behovet for å lime inn skjermsnutter av forretningsdata utenfor datastyringsgrenser.

## Bruk rettigheter

Når en person får tilgang til [!INCLUDE [prod_short](includes/prod_short.md)] med en Microsoft 365-lisens, gir denne lisensen brukeren tillatelse til å lese (men ikke skrive) [!INCLUDE [prod_short](includes/prod_short.md)]-data med et forenklet brukergrensesnitt i Microsoft Teams. Denne delen forklarer disse bruksrettighetene og begrensningene som hjelper deg med å planlegge hvordan du konfigurerer og får mest mulig ut av denne funksjonen. Hvis du vil ha mer informasjon om denne lisenstypen sammenlignet med andre [!INCLUDE [prod_short](includes/prod_short.md)]-lisenser, kan du se [Lisensieringsveiledning for Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).
 
### Klienttilgang

Brukere har rett til å få tilgang til [!INCLUDE [prod_short](includes/prod_short.md)]-data i Microsoft Teams. I tabellen nedenfor finner du en oversikt over de ulike tilgangsmåtene for [!INCLUDE [prod_short](includes/prod_short.md)]-tjenesten som er tillatt med denne lisensen.

|Klient som bruker Business Central-tjenesten |Tilgang|
|-|-|
|Business Central-app for Microsoft Teams|![Ja](media/check.png)|
|Business Central-nettklient |![Nei](media/x-icon.png ) |
|Business Central-mobilapper|![Nei](media/x-icon.png )|
|Business Central-API-er|![Nei](media/x-icon.png )|
|Business Central-integreringer med andre Office-programmer|![Nei](media/x-icon.png )|
|Business Central innebygd i andre programmer |![Nei](media/x-icon.png )|

### Datatilgang

Brukerne har rett til å lese tabelldata, men de kan ikke endre, opprette eller slette poster. [!INCLUDE [prod_short](includes/prod_short.md)]-plattformen forhindrer automatisk skriving til noen datatabeller.  

### Bruk av objekter

Tilgang til Microsoft 365-lisenser begrenser ikke hvilke Business Central-objekter eller -objektområder det er tilgang til. Brukere har rett til å få tilgang til Microsoft-grunnprogrammet og alle utvidelser, for eksempel tilpasninger og tilleggsprogrammer.

## Forenklet brukergrensesnitt

Brukere har rett til et redusert sett med funksjoner og funksjoner som leveres av [!INCLUDE [prod_short](includes/prod_short.md)] i Microsoft Teams. Tabellene nedenfor angir nevneverdige funksjoner. Dette er ikke en fullstendig liste og kan endres.

Funksjoner i [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Teams:

|Funksjon  |Tilgjengelig|
|-|-|
|Vis [!INCLUDE [prod_short](includes/prod_short.md)]-kort|![Ja](media/check.png)|
|Vis kortdetaljer |![Ja](media/check.png) |
|Fest kortdetaljer som en fane |![Ja](media/check.png)|
|Vis [!INCLUDE [prod_short](includes/prod_short.md)]-faner|![Ja](media/check.png)|
|Legg til en [!INCLUDE [prod_short](includes/prod_short.md)]-fane|![Nei_](media/x-icon.png )|
|Søk etter forretningskontakter |![Nei](media/x-icon.png )|
|Lim inn og del en koblingsforhånds visning som et kort|![Nei](media/x-icon.png )|

Funksjoner for [!INCLUDE [prod_short](includes/prod_short.md)]-klienten som er innebygd i Teams:

|Funksjon |Tilgjengelig|Eksempelfunksjoner|
|-|-|-|
|Systemhandlinger for datamanipulering |![Nei](media/x-icon.png )|Rediger, opprett, slett|
|Grunnleggende funksjoner i lister|![Ja](media/check.png)|Søk, sorter, endre oppsett|
|Avanserte funksjoner i lister|![Nei](media/x-icon.png )|Filterrute, visninger|
|Drill ned fra listen til kort |![Ja](media/check.png)||
|Få tilgang til data fra relaterte tabeller|![Nei](media/x-icon.png )|Faktaboksrute, feltneddrilling, kikking, slå opp |
|Handlinger|![Nei](media/x-icon.png )|Handlingsrad, handlingsmenyer, sidevarslingshandlinger|
|Snarveier på hele systemet|![Nei](media/x-icon.png )|Mine innstillinger, rolleutforsker, Fortell meg-søk  |
|Kopier|![Ja](media/check.png)|Kopier rader, kopier feltverdier, kopier kobling til side|
|Grensesnittilpasning|![Nei](media/x-icon.png )|Tilpass| 
|Innebygd tilpasning|![Ja](media/check.png)|Endre størrelse på kolonne, Vis/skjul, Vis mer |
|Datadeling |![Nei](media/x-icon.png )|Åpne eller rediger i Excel, Del til Teams|
|Innebygd brukerhjelp|![Ja](media/check.png) |Verktøytips, koblinger til dokumentasjon|
|Avansert brukerhjelp |![Nei](media/x-icon.png )|Side- og feltopplæringstips, hjelperute|

## Minstekrav

Denne delen beskriver minimumskravene som må oppfylles for organisasjonen for å muliggjøre tilgang med Microsoft 365-lisenser og for individuelle Microsoft Teams-brukere å få tilgang til [!INCLUDE [prod_short](includes/prod_short.md)]-data uten en [!INCLUDE [prod_short](includes/prod_short.md)]-lisens.

### Krav for å gi tilgang

- [!INCLUDE [prod_short](includes/prod_short.md)] online (SaaS).

- Miljøer må være av plattformversjon 21.1 eller nyere.

### Krav for individuelle brukere som skal ha tilgang til data i Teams

- Data må åpnes ved hjelp av [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Teams. Brukere må ha [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Teams installert og må bruke en av de støttede Teams-klientene. Hvis du vil se en liste over Teams-klienter som støttes av [!INCLUDE [prod_short](includes/prod_short.md)], kan du se [Minimumskrav for bruk av Business Central](product-requirements.md#teams).

- Brukere må være interne for organisasjonen, noe som betyr at en brukeridentitet kommer fra samme hjemmeleietaker der [!INCLUDE [prod_short](includes/prod_short.md)] distribueres og der tilgang er aktivert. Eksterne identiteter støttes ikke. [!INCLUDE [prod_short](includes/prod_short.md)] forhindrer automatisk tilgang til gjester.

- Brukere må tildeles en Microsoft 365-lisens fra en av de følgende planene.
  
  |Støttet plan|Produkt-ID |
  |-|-|
  |Microsoft 365 Business Basic|3b555118-da6a-4418-894f-7df1e2096870|
  |Microsoft 365 Business Standard|f245ecc8-75af-4f8e-b61f-27d8114de5f3|
  |Microsoft 365 Business Premium |cbdc14ab-d96c-4c30-b9f4-6ada7cdc1d46|
  |Microsoft 365 E3 |05e9a617-0261-4cee-bb44-138d3ef5d965 |
  |Microsoft 365 E5|06ebc4ee-1bb5-47dd-8120-11324bc54e06|
  |Microsoft 365 F1|50f60901-3181-4b75-8a2c-4c8e4c1d5a72|
  |Microsoft 365 F3|66b55226-6b4f-492c-910c-a3b7a3c9d993|
  |Office 365 E1|18181a46-0d4e-45cd-891e-60aabd171b4e|
  |Office 365 E2 |6634e0ce-1a9f-428c-a498-f84ec7b8aa2e|
  |Office 365 E3|6fd2c87f-b296-42f0-b197-1e91e994b900|
  |Office 365 E5|c7df2760-2c81-4ef7-b578-5b5392b571df|
  |Office 365 F2|131fd665-5752-4995-a628-bcba5c889745|
  |Office 365 F3|4b585984-651b-448a-9e53-3b10f069cf7f|
  |Microsoft Teams Essentials (Microsoft Entra-identitet) |3ab6abff-666f-4424-bfb7-f0bc274ec7bc|
  
  De fleste tilbud basert på disse planene støttes også. Hvis du for eksempel abonnerer på Microsoft 365 Business Premium (ansattpris for ideelle organisasjoner), er det et bestemt tilbud for veldedige organisasjoner basert på Microsoft 365 Business Premium-planen og som derfor støttes.

  > [!NOTE]
  > Finner du ikke planen din i listen? Microsoft er hele tiden ute etter tilbakemelding om hvordan vi kan forbedre tjenesten og utvide tilbudet slik at flere kunder kan utnytte denne funksjonen. Del forslaget ditt om hvilke planer vi bør støtte senere, på [https://aka.ms/bcIdeas](https://aka.ms/bcIdeas).

- Brukere må tildeles en Microsoft 365-lisens som har Microsoft Teams-appen aktivert i listen over apper for denne lisensen.

  |Støttede apper|Tjenesteplan-ID|
  |-|-|
  |Microsoft Teams|57ff2da0-773e-42df-b2af-ffb7a2317929 |

- Organisasjonen må ha minst én annen bruker som er tildelt en Dynamics 365 Business Central-lisens.

## Neste trinn

- Få en forståelse av brukertilgangsflyten for å hjelpe deg med å planlegge din tilnærming og konfigurasjon av Business Central som passer til forretningsbehovene. Se [Brukertilgangsflyt](admin-access-with-m365-license-flow.md).
- Konfigurer miljøet og brukerne for tilgang med Microsoft 365-lisenser. Se [Konfigurer tilgang med Microsoft 365-lisenser ](admin-access-with-m365-license-setup.md).
- For feilsøkingstips, se [Feilsøking i Business Central](/troubleshoot/dynamics-365/business-central/welcome-business-central).

## Se også

[Business Central og Microsoft Teams-integrering](across-teams-overview.md)  

