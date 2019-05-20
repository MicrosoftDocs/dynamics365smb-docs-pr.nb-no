---
title: Datoberegning for salg | Microsoft-dokumentasjon
description: Programmet beregner automatisk datoen du må bestille en vare på for å ha den på lager på en bestemt dato. Dette er datoen da du kan forvente at varer som ble bestilt på en bestemt dato, vil være tilgjengelig for plukking.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a620b7ed9d06cdd8adf7b12bea2b55aecea32bcc
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251132"
---
# <a name="date-calculation-for-sales"></a>Beregne dato for salg
[!INCLUDE[d365fin](includes/d365fin_md.md)] beregner automatisk hvilken dato en vare på en ordrelinje tidligst kan leveres på.

Hvis en kunde har bedt om en bestemt leveringsdato, beregnes datoen varene må være tilgjengelige for plukking, for at leveringsdatoen skal kunne innfris.

Hvis kunden ikke ber om en bestemt leveringsdato, beregnes datoen varene kan leveres på, fra og med den datoen varene er tilgjengelige for plukking.

## <a name="calculating-a-requested-delivery-date"></a>Beregne en ønsket leveringsdato
Hvis du angir en ønsket leveringsdato på ordren, brukes denne datoen som utgangspunkt for følgende beregninger.

- ønsket leveringsdato - leveringstid = planlagt forsendelsesdato
- planlagt forsendelsesdato - utgående lagerhåndteringstid = forsendelsesdato

Hvis varene er tilgjengelige for plukking på forsendelsesdatoen, kan salgsprosessen fortsette.

Hvis ikke varene er tilgjengelige for plukking på forsendelsesdatoen, vises en advarsel om at det er tomt på lager.

## <a name="calculating-the-earliest-possible-delivery-date"></a>Beregne den tidligste mulige leveringsdatoen
Hvis du ikke angir en ønsket leveringsdato på ordrelinjen, eller hvis ønsket leveringsdato ikke kan innfris, beregnes datoen som varene tidligst er tilgjengelige på. Denne datoen angis deretter i feltet Forsendelsesdato på linjen, og datoen du planlegger å sende og levere varene til kunden på beregnes også ved hjelp av følgende formler.

- forsendelsesdato + utgående lagerhåndteringstid = forsendelsesdato
- planlagt forsendelsesdato + leveringstid = planlagt leveringsdato


## <a name="see-also"></a>Se også  
 [Beregne dato for kjøp](purchasing-date-calculation-for-purchases.md)   
 [Beregne ordrebekreftelsesdatoer](sales-how-to-calculate-order-promising-dates.md)  
 [Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
