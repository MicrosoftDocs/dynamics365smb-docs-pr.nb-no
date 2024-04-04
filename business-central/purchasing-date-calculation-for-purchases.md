---
title: Beregn datoer for kjøp
description: Denne artikkelen beskriver hvordan du kan beregne datoer for kjøp.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'purchase order, purchase, date, receipt, delivery, lead time'
ms.search.forms: null
ms.date: 10/28/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="calculate-dates-for-purchases"></a>Beregn datoer for kjøp

Hvis du vil ha varer på lager til en bestemt dato, kan [!INCLUDE[prod_short](includes/prod_short.md)] automatisk beregne datoen du må bestille dem på. 

Resultatet er datoen da du kan plukke varene du bestilte.  

Hvis du angir en ønsket mottaksdato på en bestillingslinje, er den beregnede ordredatoen datoen når du må legge inn bestillingen. Datoen da varene er tilgjengelige for plukking, vises i feltet **Forventet mottaksdato**.  

Hvis du ikke angir en ønsket mottaksdato, er datoen du forventer å motta varene på, basert på bestillingsdatoen på linjen. 

Mottaksdatoen er også datoen varene vil være tilgjengelige for plukking.  

> [!TIP]
> Som standard er mange av datofeltene som denne artikkelen nevner, skjult på bestillingslinjer. Hvis et felt ikke er tilgjengelig, kan du legge det til ved å tilpasse siden. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).

## <a name="calculating-with-a-requested-receipt-date"></a>Beregne med en ønsket mottaksdato

Hvis det finnes en ønsket mottaksdato på bestillingslinjen, brukes denne datoen som grunnlag for følgende beregninger:  

- ønsket mottaksdato - beregning av leveringstid = bestillingsdato  
- ønsket mottaksdato + inngående lagerhåndteringstid + sikkerhetsleveringstid = forventet mottaksdato  

Hvis du angir en ønsket mottaksdato på en bestillingslinje, tildeles denne datoen til nye linjer når du oppretter dem. Du kan endre eller fjerne datoen på linjene.  

> [!NOTE]
> Hvis prosessen er basert på beregning bakover, for eksempel hvis du bruker ønsket mottaksdato til å hente den planlagte ordredatoen, anbefaler vi at du bruker datoformler som har faste varigheter, for eksempel "5D" i fem dager eller "1U" for én uke. Datoformler uten faste varigheter, for eksempel GU for gjeldende uke eller GM for gjeldende måned, kan resultere i feil datoberegninger. Hvis du vil ha mer informasjon om datoformler, kan du se [Arbeid med datoer og klokkeslett i kalenderen](ui-enter-date-ranges.md).

## <a name="calculating-without-a-requested-receipt-date"></a>Beregne uten en ønsket mottaksdato

Hvis du angir en bestillingslinje uten en ønsket mottaksdato, viser feltet **Ordredato** på linjen datoen i feltet **Ordredato** i bestillingshodet. Denne datoen er enten den angitte datoen eller arbeidsdatoen. Datoer beregnes deretter for bestillingslinjen, med utgangspunkt i bestillingsdatoen, slik:  

- bestillingsdato + beregning av leveringstid = planlagt mottaksdato  
- planlagt mottaksdato + inngående lagerhåndteringstid + sikkerhetsleveringstid = forventet mottaksdato  

Hvis du endrer bestillingsdatoen på linjen, beregner [!INCLUDE[prod_short](includes/prod_short.md)] de andre datoene på nytt.  

## <a name="default-values-for-lead-time-calculation"></a>Standardverdier for beregning av leveringstid

[!INCLUDE[prod_short](includes/prod_short.md)] bruker datoformelen i feltet **Beregning av leveringstid** på bestillingslinjen for å beregne ordren og de forventede mottaksdatoene.  

Du kan angi datoformelen manuelt på linjer. Hvis ikke bruker [!INCLUDE[prod_short](includes/prod_short.md)] formlene som er definert på følgende sider i denne prioritetsrekkefølgen:

1. Vare/leverandør-katalog
2. Varekort
3. Lagerføringsenhetskort
4. Leverandørkort

## <a name="see-also"></a>Se også

[Beregne dato for salg](sales-date-calculation-for-sales.md)  
[Beregn ordrebekreftelsesdatoer](sales-how-to-calculate-order-promising-dates.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
