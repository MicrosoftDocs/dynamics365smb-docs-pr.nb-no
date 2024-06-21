---
title: Innføring i Contoso Coffee
description: Oversikt over scenarioer for hvordan Contoso Coffee-demo data kan hjelpe deg å lære hvordan du bruker lagerfunksjonene i Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: 4764
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
---

# Innføring i Contoso Coffee-lager

Contoso Coffee er et fiktivt selskap som produserer forbrukerkaffemaskiner og kommersielle kaffemaskiner. **Contoso Coffee**-appene for Business Central legger til demonstrasjonsdata som du kan bruke til å lære hvordan du bruker lagerfunksjonene i Business Central. Du kan konfigurere lagerfunksjoner på ulike måter, se [Oversikt over forskjellige konfigurasjonsalternativer](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

Appen har tre lokasjoner som er optimalisert for ulike scenarioer:

- **SØLV**  

  Denne lokasjonen er konfigurert for bruk av hyller. Den kan lett konfigureres til å støtte grunnleggende eller avanserte. 

- **GULT**  

  Denne lokasjonen bruker avansert lageroppsett, men bruker ikke hyller. Den kan konfigureres på nytt for å støtte grunnleggende oppsett.

- **KR.SAND**  

  Denne lokasjonen bruker avansert lageroppsett med lagerstyring, som gir mer avanserte regler for hvordan varer flytter seg gjennom lageret.

## Konfigurer Contoso Coffee-lagerdata

[!INCLUDE [contoso-coffee-app-install](../../includes/contoso-coffee-app-install.md)]

Når de relevante appene er installert, går du til siden [Demoverktøy for Contoso](https://businesscentral.dynamics.com/?page=5194)-siden i [!INCLUDE [prod_short](../../includes/prod_short.md)] , velger *Lagermoduloppsett*-linjen og bruker **Konfigurer** til å klargjøre modulene. Tabellene nedenfor beskriver innstillingene:  

|Felt  |Description  |
|---------|---------|
|**Lokasjonshylle**  |Lokasjonen som skal brukes for scenarioer for grunnleggende lokasjon.|
|**Lokasjon avansert**  |Lokasjonen som skal brukes for scenarioer for enkel logistikk.|
|**Lagerstyring for lokasjon**  |Lokasjonen som skal brukes for scenarioer for avansert logistikk.|
|**Lokasjon i transitt**  |Lokasjonen som skal brukes for i transitt-lokasjonen i overføringsscenarioer.|
|**Kundenr.**  |Kunden som skal brukes i grunnleggende og enkle scenarioer i salgsoperasjoner.|
|**Leverandørnr.**  |Leverandøren som skal brukes i alle scenarioer i innkjøpsoperasjoner.|
|**Vare 1 nr.**  |Hovedvaren som skal brukes for alle scenarioene.|
|**Vare 2 nr.**  |Tilleggsvaren som skal brukes for alle scenarioene.|
|**Vare 3 nr.**  |Varen med sporing.|

Når du er klar, velger du **Opprett demonstrasjonsdata**-handling. Det tar noen minutter å legge til dataene i den underliggende databasen, men da er du klar til å kjøre de ulike scenarioene.  

> [!IMPORTANT]
> Hvis du kjører scenarioene, kan det være lurt å kontrollere at brukeren er lagt til for bestemte lokasjoner. Hvis du vil ha mer informasjon, kan du se [Definere lageransatte](../../warehouse-how-to-set-up-warehouse-employees.md).

## Scenarier

Demodata for Contoso Coffee-lager støtter nå følgende scenarioer for test og opplæring:

1.  [Gjennomgang av inngående og utgående flyt i grunnleggende lageroppsett](warehouse-basic-flow-putaway-pick.md)
2.  [Gjennomgang av inngående og utgående flyt i blandede lageroppsett](warehouse-mixed-flow-receive-pick-ship.md)
3.  [Gjennomgang av inngående og utgående flyt i avansert lageroppsett med lagerstyring](warehouse-directed-flow.md)

Les trinnene for hvert scenario i den relevante artikkelen.  

## Se også

[Definer lagerbeholdning](../../inventory-setup-inventory.md) 
[Slik definerer du lokasjoner](../../inventory-how-setup-locations.md) 
[Lagerstyring](../../warehouse-manage-warehouse.md) 
[Utformingsdetaljer](../../design-details-warehouse-overview.md) 
