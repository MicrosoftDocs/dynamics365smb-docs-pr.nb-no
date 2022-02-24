---
title: Datoberegning for kjøp | Microsoft-dokumentasjon
description: Programmet beregner automatisk datoen du må bestille en vare på for å ha den på lager på en bestemt dato. Dette er datoen da du kan forvente at varer som ble bestilt på en bestemt dato, vil være tilgjengelig for plukking.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 7b39bcd593489e40d218cf29a3d288dd128cce04
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192774"
---
# <a name="date-calculation-for-purchases"></a>Beregne dato for kjøp
[!INCLUDE[d365fin](includes/d365fin_md.md)] beregner automatisk datoen du må bestille en vare på for å ha den på lager på en bestemt dato. Dette er datoen da du kan forvente at varer som ble bestilt på en bestemt dato, vil være tilgjengelig for plukking.  

Hvis du angir en ønsket mottaksdato på et bestillingshode, er den beregnede bestillingsdatoen datoen bestillingen må foretas for at du skal kunne motta varene på ønsket dato. Deretter beregnes datoen da varene er tilgjengelige for plukking, og denne angis i feltet **Forventet mottaksdato**.  

Hvis du ikke angir en ønsket mottaksdato, brukes bestillingsdatoen på linjen som utgangspunkt for beregning av datoen du kan forvente å motta varene på, samt datoen som varene er tilgjengelige for plukking på.  

## <a name="calculating-with-a-requested-receipt-date"></a>Beregne med en ønsket mottaksdato  
Hvis det finnes en ønsket mottaksdato på bestillingslinjen, brukes denne datoen som utgangspunkt for følgende beregninger.  

- ønsket mottaksdato - beregning av leveringstid = bestillingsdato  
- ønsket mottaksdato + inngående lagerhåndteringstid + sikkerhetsleveringstid = forventet mottaksdato  

Hvis du angir en ønsket mottaksdato i bestillingshodet, kopieres denne datoen til tilsvarende felt på alle linjene. Du kan endre denne datoen på hvilken som helst av linjene, eller du kan fjerne datoen fra linjen.  

> [!Note]
> Hvis prosessen er basert på beregning bakover, for eksempel hvis du bruker ønsket mottaksdato til å hente den planlagte ordredatoen, anbefaler vi at du bruker datoformler som har faste varigheter, for eksempel "5D" i fem dager eller "1U" for én uke. Datoformler uten faste varigheter, for eksempel "GU" for gjeldende uke eller GM for gjeldende måned, kan resultere i feil datoberegninger. Hvis du vil ha mer informasjon om datoformler, kan du se [Arbeide med datoer og klokkeslett i kalenderen](ui-enter-date-ranges.md).

## <a name="calculating-without-a-requested-delivery-date"></a>Beregne uten en ønsket leveringsdato  
Hvis du angir en bestillingslinje uten en ønsket leveringsdato, fylles feltet **Ordredato** på linjen ut med datoen i feltet **Ordredato** i bestillingshodet. Dette er enten den angitte datoen eller arbeidsdatoen. Følgende datoer beregnes deretter for bestillingslinjen, med utgangspunkt i bestillingsdatoen.  

- bestillingsdato + beregning av leveringstid = planlagt mottaksdato  
- planlagt mottaksdato + inngående lagerhåndteringstid + sikkerhetsleveringstid = forventet mottaksdato  

Hvis du endrer bestillingsdatoen på linjen, som når varene ikke er tilgjengelige hos leverandøren før på en senere dato, beregner de aktuelle datoene på linjen automatisk på nytt.  

Hvis du endrer bestillingsdatoen i hodet, så kopieres denne datoen til feltet **Ordredato** på alle linjene, og alle de aktuelle datofeltene beregnes deretter på nytt.  

## <a name="see-also"></a>Se også  
 [Beregne dato for salg](sales-date-calculation-for-sales.md)   
 [Beregne ordrebekreftelsesdatoer](sales-how-to-calculate-order-promising-dates.md)  
 [Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
