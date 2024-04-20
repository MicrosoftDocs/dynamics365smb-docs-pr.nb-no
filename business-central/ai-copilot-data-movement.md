---
title: Copilot-dataflytting på tvers av geografiske områder
description: 'Finn ut hvordan data som brukes i kopilotfunksjoner i Dynamics 365 Business Central, flyttes på tvers av geografiske områder der Azure OpenAI-tjenesten ikke er tilgjengelig som standard.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.date: 04/16/2024
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
---

# Copilot-dataflytting på tvers av geografiske områder 

Copilot er tilgjengelig i alle støttede [land/områder i Business Central](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations). Copilot bruker imidlertid Microsoft Azure OpenAI-tjenesten, som for øyeblikket bare er tilgjengelig for Business Central i enkelte geografiske områder. Dette betyr at hvis miljøet befinner seg et annet sted, må data fra Copilot og generative KI-funksjoner overføres utenfor ditt geografiske område og kan behandles og lagres utenfor samsvarsgrensen. Data inkluderer KI-meldingene og forretningsdataene dine som brukes av eller genereres av Copilot. I dette tilfellet må du velge å tillate dataflytting til en Azure OpenAI-tjeneste i en annen geografi. <!--For a list of geographies, refer to the [Azure OpenAI Service geographies](#azure-openai-service-geographies) section that follows.-->

> [!IMPORTANT]
> Hvis miljøet ditt befinner seg i samme Azure-område som Azure OpenAI-tjenesten, kobles det automatisk til Azure OpenAI-tjenesten, det finnes ikke noe alternativ.

> [!NOTE]
> Individuelle Copilot- og generative KI-funksjoner er kanskje ikke tilgjengelige i alle miljøland/-områder i Business Central. Rådfør deg med utgiveren av hver funksjon for å finne ut mer om tilgjengelighet.
> 
> Copilot- og generative KI-funksjoner fra ikke-Microsoft-utgivere, for eksempel de som kommer fra tilpassinger eller AppSource-apper du installerer, definerer hver sine egne spesifikke Azure OpenAI-tjenesteområder. Rådfør deg med utgiveren av utvidelsen for å finne ut hvilke regionale Azure-tjenester som brukes av utvidelsen. 

### Azure OpenAI-tjeneste-geografier

Tabellen nedenfor viser Azure OpenAI-tjenestens geografiske område som brukes av Copilot, basert på Azure-området i et Business Central-miljø. Denne informasjonen er viktig når du skal avgjøre om du skal velge dataflytting på tvers av geografiske områder. Du kan identifisere Azure-området for miljøet i Business Central-administrasjonssenteret (se [Administrer miljøer i administrasjonssenteret](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)).

| Azure-område for miljø| Azure OpenAI-tjenestegeografi|Administratorhandling kreves for å få tilgang til Copilot| 
| - | - | - |
|Asia (øst, sørøst) |USA|Ja|
|Australia (sør-øst)| Australia |Nei |
|Brasil (sør) |USA|Ja|
|Canada (sentralt, øst)|USA|Ja|
|Europa (vest, nord)| Sverige eller Sveits |Nei\*|
|Frankrike (sentralt, sør)| Sverige eller Sveits |Ja|
|Tyskland (nord, vest-sentralt)| Sverige eller Sveits |Ja|
|India (sentralt, sør)|India|Nei|
|Japan (øst, vest)|USA|Ja|
|Korea (sentralt, sør)|USA|Ja|
|Norge (øst, vest)|Sverige eller Sveits |Ja|
|Sør-Afrika (nord, vest)|USA|Ja|
|Sveits (nord, vest) |Sverige eller Sveits |Ja|
|De forente arabiske emirater (nord, vest)|USA|Ja|
|Storbritannia (sør, vest)|Storbritannia|Nei|
|USA (sentral, øst, nord-sentral, sør-sentral, vest) |USA|Nei|

\* For miljøer i Azure-områder i Vest-Europa og Nord-Europa aktiverer Business Central automatisk dataflytting på tvers av geografiske områder, men administratorer kan velge det bort når som helst.

> [!NOTE]
> Når en Azure OpenAI-tjeneste blir tilgjengelig i Business Central-geografien, går miljøet automatisk over til å bruke Azure OpenAI-tjenesten, og det er ikke nødvendig eller mulig å melde seg på.
<!--

BC geos base on https://dynamics.microsoft.com/en-us/availability-reports/georeport/
case "AUSTRALIAEAST":
            case "AUSTRALIASOUTHEAST":
                return new CapiRegion("au", 2);
            case "BRAZILSOUTH":
                return new CapiRegion("br", 2);
            case "CANADACENTRAL":
            case "CANADAEAST":
                return new CapiRegion("ca", 2);
            case "CENTRALINDIA":
            case "SOUTHINDIA":
                return new CapiRegion("in", 1);
            case "EASTASIA":
                return new CapiRegion("as", 2);
            case "EASTUS":
            case "EASTUS2":
            case "SOUTHCENTRALUS":
            case "CENTRALUS":
            case "NORTHCENTRALUS":
            case "WESTUS":
            case "US":
                return new CapiRegion("us", 9, HasGpt4InGeo: true, HasTurboInGeo: true);
            case "FRANCECENTRAL":
            case "FRANCESOUTH":
                return new CapiRegion("fr", 1);
            case "GERMANYNORTH":
            case "GERMANYWESTCENTRAL":
                return new CapiRegion("de", 1);
            case "JAPANEAST":
            case "JAPANWEST":
                return new CapiRegion("jp", 1);
            case "KOREACENTRAL":
            case "KOREASOUTH":
                return new CapiRegion("kr", 1);
            case "NORWAYEAST":
            case "NORWAYWEST":
                return new CapiRegion("no", 1);
            case "SOUTHAFRICANORTH":
            case "SOUTHWESTAFRICA":
                return new CapiRegion("za", 1);
            case "SOUTHEASTASIA":
                return new CapiRegion("sg", 1);
            case "SWITZERLANDNORTH":
            case "SWITZERLANDWEST":
                return new CapiRegion("ch", 1, HasTurboInGeo: true);
            case "UKSOUTH":
            case "UKWEST":
                return new CapiRegion("uk", 2);
            case "NORTHEUROPE":
            case "WESTEUROPE":
                return new CapiRegion("eu", 10);
            case "UAENORTH":
            case "UAECENTRAL":
                return new CapiRegion("ae", 1);

-->

## Neste trinn

Du velger (eller velger bort) å tillate dataflytting på tvers av geografiske områder fra siden [Copilot og KI-funksjoner](https://businesscentral.dynamics.com/?page=7775). Hvis du vil ha mer informasjon, kan du gå til [Tillat dataflytting på tvers av geografiske områder](enable-ai.md#allow-data-movement-across-geographies).
