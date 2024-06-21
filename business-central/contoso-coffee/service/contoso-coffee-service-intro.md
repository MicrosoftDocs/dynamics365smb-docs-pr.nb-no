---
title: Innføring i Contoso Coffee-servicebehandling
description: Denne artikkelen gir deg en innføring i demonstrasjonsdataene for Consoso Coffee for servicebehandling.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 11/27/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="introduction-to-contoso-coffee-service-management"></a>Innføring i Contoso Coffee-servicebehandling

Contoso Coffee er et fiktivt selskap som produserer forbrukerkaffemaskiner og kommersielle kaffemaskiner. **Contoso Coffee**-appene for Business Central legger til demonstrasjonsdata som du kan bruke til å lære hvordan du bruker servicebehandlingsfunksjonene i Business Central.

Denne appen inneholder flere elementer som brukes til hovedgjennomgangene:

- Ressurser med tilordnede ferdigheter
- Varer som er konfigurert til å opprette servicevarer
- Utlånsobjekter

> [!IMPORTANT]
> Før du kjører noen av scenarioene for Contoso Coffee, må du bokføre eventuelle varekladdelinjer med åpningssaldoer. Hvis du vil ha flere krav, kan du se [Konfigurer Contoso Coffee-data](#set-up-contoso-coffee-service-management-data).
>
> 
## <a name="set-up-contoso-coffee-service-management-data"></a>Konfigurer data for Contoso Coffee-servicebehandling

[!INCLUDE [contoso-coffee-app-install](../../includes/contoso-coffee-app-install.md)]

Når de relevante appene er installert, går du til siden [Demoverktøy for Contoso](https://businesscentral.dynamics.com/?page=5194)-siden i [!INCLUDE [prod_short](../../includes/prod_short.md)] , velger *Service-modul*-linjen og bruker **Konfigurer** til å klargjøre modulene. Tabellen nedenfor beskriver innstillingene:  

|Felt  |Description  |
|---------|---------|
|**Kundenr.**  |Kunden som skal brukes i scenarioer i salgsoperasjoner.|
|**Leverandørnr.**  |Leverandøren som skal brukes i alle scenarioer i innkjøpsoperasjoner.|
|**Vare 1 nr.**  |Varen som skal brukes for reparasjon og vedlikehold-scenarioene.|
|**Servicevarenr. 1**  |Elementet av typen service for å bruke reparasjonsscenario.|
|**Servicevarenr. 2**  |Elementet av typen service for å bruke reparasjonsscenario.|
|**Ressursnr. 1**  |Ressursen som skal brukes for kontraktscenarioene.|
|**Ressursnr. 2**  |Ressursen som skal brukes for ødelagt/reparer-scenarioene.|
|**Tjenesteplassering** |Angir lageret som du vil bruke for serviceoperasjoner. Standarden er *HOVED*, men du kan endre den etter behov.|

Når du er klar, velger du **Opprett demonstrasjonsdata**-handling. Det tar noen minutter å legge til dataene i den underliggende databasen, men da er du klar til å kjøre de ulike scenarioene.  

## <a name="scenarios"></a>Scenarier

Demodata for Contoso Coffee støtter nå følgende servicescenarioer for test og opplæring:

1. Opprette serviceordre for ad hoc-reparasjonsforespørsler, plassere og motta utlånsobjekter, registrere tid og fakturere kunder med [gjennomgang av serviceordrer for servicevarer](service-basic-flow-order.md)
2. Opprette servicekontrakter, generere serviceordrer, fakturere kontraktgebyrer og tildele ressurser med [gjennomgang av servicekontrakter for servicevarer](service-contract-flow.md)

Les trinnene for hvert scenario i den relevante artikkelen.  

> [!IMPORTANT]
> Disse servicegjennomgangene krever at brukeropplevelsen er satt til **Premium** på siden **Firmainformasjon**.


## <a name="see-also"></a>Se også

[Tjeneste](../../service-service.md)
