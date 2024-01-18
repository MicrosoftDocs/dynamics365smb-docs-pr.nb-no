---
title: Innføring i demodata for Contoso Coffee
description: Oversikt over scenarioer for hvordan Contoso Coffee-demo data kan hjelpe deg å lære hvordan du bruker funksjonene i Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.date: 09/20/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '5194,'
ms.custom: bap-template
---

# <a name="introduction-to-contoso-coffee-demo-data"></a>Innføring i demodata for Contoso Coffee

Contoso Coffee er et fiktivt selskap som produserer forbrukerkaffemaskiner og kommersielle kaffemaskiner. **Contoso Coffee**-appene for [!INCLUDE [prod_short](../includes/prod_short.md)] legger til demonstrasjonsdata som du kan bruke til å lære hvordan du bruker funksjonene i [!INCLUDE [prod_short](../includes/prod_short.md)].  

## <a name="set-up-contoso-coffee-data"></a>Konfigurer Contoso Coffee-data

[!INCLUDE [contoso-coffee-app-install](../includes/contoso-coffee-app-install.md)]

Når appene er installert, går du til siden **Demoverktøy for Contoso**, og bruker handlingen **Konfigurer** til å klargjøre følgende moduler. Du kan velge å installere alle tilgjengelige data, som inkluderer oppsetts- og produksjonsdata, eller bare oppsettsdata.

 - **Fellesmodulen** for å klargjøre generelle innstillinger som [!INCLUDE [prod_short](../includes/prod_short.md)] krever. For eksempel ting som nummerserier. 

Tabellen nedenfor beskriver innstillingene:  

|Felt  |Description  |
|---------|---------|
|**Startår** |Angir det første året du vil bruke for Contoso Coffee-demondataene. Året er enten et kalenderår eller et regnskapsår, avhengig av firmaoppsettet.|
|**Lands-/regionkode**|Angir en land/region for innenlandske kunder og leverandører.|
|**Selskapstype**    |Angir om det aktuelle selskapet må rapportere mva. eller salgsmva. |
|**Prisfaktor**     |Angir en faktor for å konvertere en pris fra USD/EUR til den lokale valutaen. *1* betyr at prisen er det samme beløpet i hvilken som helst valuta. Et høyere nummer brukes til å hente prisen i lokal valuta. |
|**Avrundingspresisjon**  |Angir avrundingspresisjonen du vil opprette demodataene med.|

 - [Produksjonsmodulen](manufacturing/contoso-coffee-manufacturing-intro.md) for å klargjøree for [produksjonsscenarioer](manufacturing/contoso-coffee-manufacturing-intro.md#scenarios).
 - [Lagermodul](warehousing/contoso-coffee-warehousing-intro.md) for å klargjøre for [lagerscenarioer](warehousing/contoso-coffee-warehousing-intro.md#scenarios).
 - [Servicemodul](service/contoso-coffee-service-intro.md) for å klargjøre for [Servicescenarioer](service/contoso-coffee-service-intro.md#scenarios).

Når du har konfigurert modulene du vil prøve, velger du handlingen **Generer** for å opprette demonstrasjonsdata for dem.

## <a name="see-also"></a>Se også

[Produksjon](../production-manage-manufacturing.md)  
[Lagerstyring](../warehouse-manage-warehouse.md)  
[Tjeneste](../service-service.md)
<!-- [Projects and Jobs](../projects-manage-projects.md) -->

