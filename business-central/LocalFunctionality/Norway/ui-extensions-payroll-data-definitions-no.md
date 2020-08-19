---
title: Lønnsdatadefinisjoner (NO) | Microsoft-dokumentasjon
description: Denne utvidelsen gjør det enkelt å utveksle data med lønnstjenesteleverandøren i Norge.
author: edupont04
manager: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: b16edb8a5c2e5422fc072b80242ad5d0b174af35
ms.sourcegitcommit: 007b331b6974983ee614db0406f00777da359ecb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/10/2020
ms.locfileid: "3676993"
---
# <a name="the-payroll-data-definitions-no-extension"></a>Utvidelsen Lønnsdatadefinisjoner (NO)

Hvis bedriften din bruker Huldt & Lillevik Lønn - Visma-lønnstjenesteleverandørene i Norge kan utvidelsen **Lønnsdatadefinisjoner (NO)** hjelpe deg med å registrere lønnstransaksjoner fra disse leverandørene raskt og nøyaktig. Utvidelsen inneholder datautvekslingsdefinisjoner som lar deg lese inn lønnstransaksjoner i filer som leverandørene sender til deg. Hvis du vil ha mer informasjon om datautvekslingsdefinisjoner, kan du se [Definere datautvekslingsdefinisjoner](../../across-how-to-set-up-data-exchange-definitions.md).   

## <a name="getting-started"></a>Komme i gang

Det første trinnet er å tilordne typer lønnstransaksjoner til finanskontiene som du ønsker å bokføre dem til, i [!INCLUDE[prodshort](../../includes/prodshort.md)]. Du kan for eksempel bokføre pensjonsbidrag til en konto med navnet Pensjon, og skatt betalt på bidragene til en konto med navnet Pensjonsskatt. Dette skjer utenfor [!INCLUDE[prodshort](../../includes/prodshort.md)]. Du kan for eksempel bruke et Excel-regneark for å visualisere tilordningen. Arbeid med lønnstjenesteleverandøren for å være sikker på at filen de eksporterer, inneholder tilordningen. Vanligvis kan du finne informasjon om hvordan du konfigurerer eksportfiler på leverandørens nettsted.  

Når du har installert utvidelsen, er neste trinn å angi formatet for lønnsdatafilen fra lønnstjenesteleverandøren. Hvis du vil gjøre dette, kan du gå til **Finansoppsett**-siden og velge leverandøren i feltet **Importformat for lønnstransaksjon**.  

## <a name="to-import-a-payroll-file"></a>Slik importerer du en lønnsfil

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](../../media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finanskladder**, og velg deretter den relaterte koblingen.   
2.  Velg kladden som skal brukes, og bruk deretter handlingen **Importer lønnsfil** til å importere datafilen fra lønnstjenesteleverandøren.  

## <a name="see-also"></a>Se også
[Funksjonalitet som er spesifikk for norske brukere](norway-local-functionality.md)   
