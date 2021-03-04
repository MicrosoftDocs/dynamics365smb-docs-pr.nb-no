---
title: Datoberegning for salg | Microsoft-dokumentasjon
description: Programmet beregner automatisk datoen du må bestille en vare på for å ha den på lager på en bestemt dato. Dette er datoen da du kan forvente at varer som ble bestilt på en bestemt dato, vil være tilgjengelig for plukking.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 26782d211d205bb5414c5bd423ccf240f70f197e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748471"
---
# <a name="date-calculation-for-sales"></a>Beregne dato for salg
[!INCLUDE[prod_short](includes/prod_short.md)] beregner automatisk hvilken dato en vare på en ordrelinje tidligst kan leveres på.

Hvis en kunde har bedt om en bestemt leveringsdato, beregnes datoen varene må være tilgjengelige for plukking, for at leveringsdatoen skal kunne innfris.

Hvis kunden ikke ber om en bestemt leveringsdato, beregnes datoen varene kan leveres på, fra og med den datoen varene er tilgjengelige for plukking.

## <a name="calculating-a-requested-delivery-date"></a>Beregne en ønsket leveringsdato
Hvis du angir en ønsket leveringsdato på ordren, blir denne datoen som utgangspunkt for følgende beregninger.

- ønsket leveringsdato - leveringstid = planlagt forsendelsesdato
- planlagt forsendelsesdato - utgående lagerhåndteringstid = forsendelsesdato

Hvis varene er tilgjengelige for plukking på forsendelsesdatoen, kan salgsprosessen fortsette. Hvis ikke, vises en advarsel om tomt lager.

> [!Note]
> Hvis prosessen er basert på beregning bakover, for eksempel hvis du bruker ønsket leveringsdato til å hente den planlagte forsendelsesdatoen, anbefaler vi at du bruker datoformler som har faste varigheter, for eksempel "5D" i fem dager eller "1U" for én uke. Datoformler uten faste varigheter, for eksempel "GU" for gjeldende uke eller GM for gjeldende måned, kan resultere i feil datoberegninger. Hvis du vil ha mer informasjon om datoformler, kan du se [Arbeide med datoer og klokkeslett i kalenderen](ui-enter-date-ranges.md).

## <a name="calculating-the-earliest-possible-delivery-date"></a>Beregne den tidligste mulige leveringsdatoen
Hvis du ikke angir en ønsket leveringsdato på ordrelinjen, eller hvis ønsket leveringsdato ikke kan innfris, beregnes datoen som varene tidligst er tilgjengelige på. Denne datoen angis deretter i feltet Forsendelsesdato på linjen, og datoen du planlegger å sende og levere varene til kunden på beregnes også ved hjelp av følgende formler.

- forsendelsesdato + utgående lagerhåndteringstid = forsendelsesdato
- planlagt forsendelsesdato + leveringstid = planlagt leveringsdato


## <a name="see-also"></a>Se også  
 [Beregne dato for kjøp](purchasing-date-calculation-for-purchases.md)   
 [Beregne ordrebekreftelsesdatoer](sales-how-to-calculate-order-promising-dates.md)  
 [Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]