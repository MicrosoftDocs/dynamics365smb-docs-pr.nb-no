---
title: Brukertilgangsflyt for Microsoft 365-lisenser
description: Få en oversikt over hva som skjer når en bruker får tilgang til Business Central-data ved å bruke Microsoft 365-lisensen for første gang.
author: mikebc
ms.author: mikebc
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---
# Brukertilgangsflyt for Microsoft 365-lisenser

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Denne artikkelen beskriver hva som skjer når en bruker får tilgang til Business Central-data ved å bruke Microsoft 365-lisensen for første gang. Ved å forstå denne flyten kan administratoren planlegge tilnærmingen sin og konfigurere at Business Central skal samsvare med forretningsbehovene.

1. Først godkjennes brukerens identitet 
2. Business Central bekrefter at alle [minimumskravene](admin-access-with-m365-license.md#minimum-requirements) er oppfylt.
3. Business Central bekrefter at denne brukeren ikke har en bedre lisens, for eksempel en Business Central-lisens eller en administrativ rolle, for eksempel en delegert administratorrolle. 
4. Business Central bekrefter om brukeren har tilgang til data som tilhører et miljø som har aktivert tilgang med Microsoft 365-lisenser. 
5. Brukerposten klargjøres i Business Central, tildeler brukergruppen, profilen og tillatelsessettene som er definert på siden for Microsoft 365-lisenskonfigurasjon. Som standard er Teams-brukergruppen tildel, ansattprofilen er tildelt og bare påloggingstillatelsessettet er tildelt. Andre standard innstillinger for brukerinnstillinger brukes også, akkurat som lisensierte Business Central-brukere. 
6. Den fullstendige Business Central-sikkerhetsmodellen brukes til å avgjøre om brukeren skal ha tilgang til posten, siden, i det angitte firmaet og i angitt miljø. 

Hvis alle trinnene er vellykket, kan brukeren nå vise disse Business Central-dataene i Teams. Business Central-tjenesten sikrer automatisk skrivebeskyttet tilgang og forenkler brukergrensesnittet. 

Brukerkontoen er nå registrert i Business Central og kan behandles på samme måte som enhver Business Central-bruker.

> [!NOTE]
> Trinnene kan variere, avhengig av eventuell tilleggssikkerhetskonfigurasjon du har angitt i Microsoft 365 eller Business Central.

## Se også

[Business Central-tilgang med Microsoft 365-lisenser](admin-access-with-m365-license.md#minimum-requirements)  
[Konfigurer tilgang med Microsoft 365-lisenser](admin-access-with-m365-license-setup.md)  