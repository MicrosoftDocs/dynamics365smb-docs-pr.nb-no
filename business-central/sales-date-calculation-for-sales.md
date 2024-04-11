---
title: Beregn leveringsdato for salg
description: Programmet beregner automatisk datoen du må bestille en vare på for å ha den på lager på en bestemt dato og tilgjengelig for plukking.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 03/06/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Beregn leveringsdato for salg

[!INCLUDE[prod_short](includes/prod_short.md)] beregner automatisk hvilken dato en vare på en ordrelinje tidligst kan leveres på.

* Hvis en kunde har bedt om en bestemt leveringsdato, beregnes datoen varene må være tilgjengelige for plukking, for at leveringsdatoen skal kunne innfris.
* Hvis en kunde ikke ber om en bestemt leveringsdato, beregnes datoen som varene kan leveres. Beregningen begynner fra den datoen varene er tilgjengelige for plukking.

## Beregn en ønsket leveringsdato

Hvis du angir en ønsket leveringsdato på ordren, blir denne datoen som utgangspunkt for følgende beregninger.

- *ønsket leveringsdato - leveringstid = planlagt forsendelsesdato*
- *planlagt forsendelsesdato - utgående lagerhåndteringstid = forsendelsesdato*

Hvis varene er tilgjengelige for plukking på forsendelsesdatoen, kan salgsprosessen fortsette. Hvis ikke, vises en advarsel om tomt lager.

> [!NOTE]
> Hvis prosessen er basert på beregning bakover, for eksempel hvis du bruker ønsket leveringsdato til å hente den planlagte forsendelsesdatoen, anbefaler vi at du bruker datoformler med faste varigheter, for eksempel "5D" i fem dager eller "1U" for én uke. Datoformler uten faste varigheter, for eksempel GU for gjeldende uke eller GM for gjeldende måned, kan resultere i feil datoberegninger. Finn ut mer om datoformler under [Arbeid med datoer og klokkeslett i kalenderen](ui-enter-date-ranges.md).

## Beregne den tidligste mulige leveringsdatoen

Hvis du ikke angir en ønsket leveringsdato på ordrelinjen, eller hvis ønsket leveringsdato ikke kan innfris, beregnes datoen som varene tidligst er tilgjengelige på. Denne datoen angis deretter i feltet **Forsendelsesdato** på linjen, og datoen du planlegger å sende og levere varene til kunden på beregnes også ved hjelp av følgende formler.

- *forsendelsesdato + utgående lagerhåndteringstid = forsendelsesdato*
- *planlagt forsendelsesdato + leveringstid = planlagt leveringsdato*

## Se også

[Beregn dato for kjøp](purchasing-date-calculation-for-purchases.md)  
[Beregn ordrebekreftelsesdatoer](sales-how-to-calculate-order-promising-dates.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
