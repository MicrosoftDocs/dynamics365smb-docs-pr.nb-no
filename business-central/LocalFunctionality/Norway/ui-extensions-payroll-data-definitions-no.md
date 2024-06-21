---
title: 'Lønnsdatadefinisjoner [NO]'
description: Utvidelsen Lønnsdatadefinisjoner gjør det enkelt å utveksle data med lønnstjenesteleverandøren i Norge.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Utvidelsen Lønnsdatadefinisjoner i den norske versjonen

Hvis bedriften din bruker Huldt & Lillevik Lønn - Visma-lønnstjenesteleverandørene i Norge kan utvidelsen **Lønnsdatadefinisjoner (NO)** hjelpe deg med å registrere lønnstransaksjoner fra disse leverandørene raskt og nøyaktig. Utvidelsen inneholder datautvekslingsdefinisjoner som lar deg lese inn lønnstransaksjoner i filer som leverandørene sender til deg. Hvis du vil ha mer informasjon om datautvekslingsdefinisjoner, kan du se [Definere datautvekslingsdefinisjoner](../../across-how-to-set-up-data-exchange-definitions.md).   

## Komme i gang

Det første trinnet er å tilordne typer lønnstransaksjoner til finanskontiene som du ønsker å bokføre dem til, i [!INCLUDE[prod_short](../../includes/prod_short.md)]. Du kan for eksempel bokføre pensjonsbidrag til en konto med navnet Pensjon, og skatt betalt på bidragene til en konto med navnet Pensjonsskatt. Dette skjer utenfor [!INCLUDE[prod_short](../../includes/prod_short.md)]. Du kan for eksempel bruke et Excel-regneark for å visualisere tilordningen. Arbeid med lønnstjenesteleverandøren for å være sikker på at filen de eksporterer, inneholder tilordningen. Vanligvis kan du finne informasjon om hvordan du konfigurerer eksportfiler på leverandørens nettsted.  

Når du har installert utvidelsen, er neste trinn å angi formatet for lønnsdatafilen fra lønnstjenesteleverandøren. Hvis du vil gjøre dette, kan du gå til **Finansoppsett**-siden og velge leverandøren i feltet **Importformat for lønnstransaksjon**.  

## Slik importerer du en lønnsfil

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finanskladder**, og velg deretter den relaterte koblingen.   
2.  Velg kladden som skal brukes, og bruk deretter handlingen **Importer lønnsfil** til å importere datafilen fra lønnstjenesteleverandøren.  

## Se også
[Funksjonalitet som er spesifikk for norske brukere](norway-local-functionality.md)   


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
