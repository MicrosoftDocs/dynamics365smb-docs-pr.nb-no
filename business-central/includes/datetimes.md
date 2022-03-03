---
author: edupont04
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 44cd8156e66be7736da4f1c51f507715d7842478
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8147417"
---
Når du angir dato og klokkeslett, som er en dato og klokkeslett kombinert i ett felt, må du angi et mellomrom mellom datoen og klokkeslettet. Datodelen kan bare inneholde mellomrom i form av det offisielle datoskilletegnet i regioninnstillingene. Klokkeslettet kan inneholde mellomrom rundt AM/PM-indikatoren i relevante regionale innstillinger.

<!--It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.-->

Tabellen nedenfor viser forskjellige måter som du kan angi datoer og klokkeslett på, og hvordan de tolkes.  

|Angivelse|Tolkning|
|---------------|------------------------|
|08-01-2022 05:48:12 PM|08\-01\-2022 05:48:12 PM|
|131222 132455|13-12-22 13:24:55|
|1-12-22 10|01-12-22 10:00:00|
|1.12.22 5|01-12-22 05:00:00|
|1.12.22|01-12-22 00:00:00|
|11 12|11.nneværende måned.inneværende år 12.00.00|
|1112 12|11.12.inneværende år 12.00.00|
|d eller i dag|dagens dato 00:00:00|
|d klokkeslett|dagens dato og klokkeslett|
|d 10.30|dagens dato 10:30:00|
|d 3.3.3|dagens dato 03.03.03|
|a eller arbeidsdag|arbeidsdatoen 00.00.00|
|m eller mandag|mandag i inneværende uke 00.00.00|
|ti eller tirsdag|tirsdag i inneværende uke 00:00:00|
|o eller onsdag|onsdag i inneværende uke 00.00.00|
|to eller torsdag|torsdag i inneværende uke 00.00.00|
|f eller fredag|fredag i inneværende uke 00.00.00|
|l eller lørdag|lørdag i inneværende uke 00.00.00|
|s eller søndag|søndag i inneværende uke 00.00.00|
|ti 10.30|tirsdag i inneværende uke 10:30:00|
|ti 3.3.3|tirsdag i inneværende uke 03.03.03|
|t23 t|Tirsdag i uke 23 i arbeidsdatoåret, gjeldende klokkeslett|
|t23|Tirsdag i uke 23 i arbeidsdatoåret|
|t 23|I dag 23:00:00|
|t-1|Tirsdag i uke 1 i arbeidsdatoåret|


