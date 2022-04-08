---
title: 'Feilsøking: Få tilgang til kamera og plassering'
description: Denne artikkelen beskriver hvordan du feilsøker tilgang til kamera- og plasseringsinformasjon i Business Central.
author: blrobl
ms.author: t-blrobl
ms.date: 04/01/2021
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: conceptual
ms.openlocfilehash: 5c5693b05d8590e569e0fb1b80993e35550c5ed5
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2022
ms.locfileid: "8518812"
---
# <a name="troubleshooting-accessing-camera-and-location"></a>Feilsøking: Få tilgang til kamera og plassering

Du kan oppleve problemer når du prøver å få til gang til kamera- og plasseringsinformasjon for en enhet fra [!INCLUDE[prod_short](includes/prod_short.md)]. Nedenfor finner du mulige årsaker til disse problemene og hvordan du omgår dem.

## <a name="device-must-have-camera-and-location-capabilities"></a>Enheten må ha kamera- og plasseringsegenskaper

For å få tilgang til kameraet eller en brukers plassering fra en enheten må enheten henholdsvis ha et fysisk kamera eller muligheten til å hente plasseringsinformasjon.

Hvis enheten har kamera- og plasseringsegenskaper, men du fremdeles har problemer, kan det hende at enkelte driver trenger oppdatering eller ny installasjon. Selv om du er usikker, anbefaler vi alltid at du oppdaterer enheten operativsystem, drivere og nettleser til den nyeste versjonen for den beste opplevelsen.

## <a name="access-permissions-not-enabled"></a>Tilgangstillatelser ikke aktivert

Du må aktivere generell tilgang til kamera og plassering fra enhetens personverninnstillinger og uttrykkelig tillate at [!INCLUDE[prod_short](includes/prod_short.md)] får tilgang til dem. For å se eller endre tillatelser for en enhet som kjører i Windows, går du for eksempel til **Innstillinger**, velger **Personvern** og **Apptillatelser**. 

For mobile enheter må du gi kamera- og plasseringstilgangstillatelser til [!INCLUDE[prod_short](includes/prod_short.md)]-mobilappen. For å gjøre det for en iOS-enhet går du til **Innstillinger**, velger **Personvern** og **Kamera** eller **Plassering**. For å gjøre det for Android-enheter går du til **Innstillinger**, velger **Apper og varsler**, **Avansert**, **Tillatelsesbehandling** og **Kamera** eller **Plassering**.

Hvis du bruker [!INCLUDE[prod_short](includes/prod_short.md)] i en nettleser, må du i tillegg gi [!INCLUDE[prod_short](includes/prod_short.md)]-nettstedet tillatelse til å få tilgang til kamera- eller plasseringsinformasjon. For å se eller endre et nettsteds tillatelser i Microsoft Edge-nettleseren går du til **Innstillinger**, **Nettstedstillatelser** og **Kamera** eller **Plassering**. Vær oppmerksom på at dette kan være annerledes for andre nettlesere.

Som standard vil enheten eller nettleseren vise en forespørsel om tilgang til disse egenskapene når brukeren aktiverer dem for første gang.

> [!NOTE]  
> Enkelte eldre nettlesere gir ikke tilgang til kamera og plassering. Kamera er for eksempel ikke tilgjengelig i Internet Explorer eller den gamle Microsoft Edge.

## <a name="web-client-connection-not-secure"></a>Nettklienttilkobling ikke sikker

Kamera- og plasseringsegenskaper er bare tilgjengelig når du har tilgang til nettklienten via SSL-sikrede HTTP-tilkobling ved å bruke URI-skjemaet `https://`. 

Det eneste unntaket er å koble til `http://localhost`, som brukes til formål for utvikling og testing.


## <a name="work-with-virtualization-technologies"></a>Arbeid med visualiseringsteknologier

Når du kobler til [!INCLUDE[prod_short](includes/prod_short.md)] via Eksternt skrivebord eller en annen virtualisering, kan det hende tilgang til kamera og plassering ikke er tilgjengelig. I dette tilfellet bruker du det fysiske systemet i stedet.

## <a name="antivirus-software"></a>Antivirusprogramvare
Enkelte antivirusprogramvarer blokkerer tilgang til kamera og plassering som standard. Husk å sjekke innstillingene for antivirusprogramvaren.

## <a name="see-also"></a>Se også
[Implementere kameraet i AL](/dynamics365/business-central/dev-itpro/developer/devenv-implement-camera-al)  
[Implementere plasseringen i AL](/dynamics365/business-central/dev-itpro/developer/devenv-implement-location-al)


[!INCLUDE[footer-include](includes/footer-banner.md)]