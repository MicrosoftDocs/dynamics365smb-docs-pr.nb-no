---
title: Definere foretrukne metoder for å sende salgsdokumenter | Microsoft-dokumentasjon
description: 'Beskriver hvordan du konfigurerer kundens foretrukne sendemetode for salgsdokumenter, for eksempel e-post, PDF-fil, elektronisk dokument og så videre.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'email, PDF, electronic document'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Definere en profil for dokumentsending
Du kan definere hver kunde med en foretrukket metode for sending av salgsdokumenter, slik at du ikke trenger å velge et alternativ for sending hver gang du velger handlingen **Bokfør og send**.

På siden **Profiler for dokumentsending** definerer du ulike sendingsprofiler som du kan velge fra feltet **Profil for dokumentsending** på et kundekort. Du kan merke av for **Standard** for å angi at profilen for dokumentsending er standardprofilen for alle kunder, bortsett fra kunder der feltet **Profil for dokumentsending** er fylt ut med en annen sendingsprofil.

Når du velger handlingen **Bokfør og send** i et salgsdokument, viser dialogboksen **Bokfør og send bekreftelse** sendingsprofilen som brukes, enten den som er satt opp for kunden, eller standarden for alle kunder. I dialogboksen kan du endre sendingsprofilen for salgsdokumentet. Hvis du vil ha mer informasjon, kan du se [Fakturere salg](sales-how-invoice-sales.md).
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHH?rel=0]

## Slik definerer du en profil for dokumentsending:
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Profiler for dokumentsending**, og velg deretter den relaterte koblingen.
2. På siden **Profiler for dokumentsending** velger du handlingen **Ny**.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Slik angir du en sendingsprofil på et kundekort:
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.
2. Åpne kortet til kunden som du vil definere en sendingsprofil for.
3. Velg en profil i feltet i feltet **Profiler for dokumentsending**, som du har satt opp som beskrevet i forrige fremgangsmåte.

## Se også
[Sette opp salg](sales-setup-sales.md)  
[Salg](sales-manage-sales.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]