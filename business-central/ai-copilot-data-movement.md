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
ms.search.form: 7775
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


## Neste trinn

Du velger (eller velger bort) å tillate dataflytting på tvers av geografiske områder fra siden [Copilot og KI-funksjoner](https://businesscentral.dynamics.com/?page=7775). Hvis du vil ha mer informasjon, kan du gå til [Tillat dataflytting på tvers av geografiske områder](enable-ai.md#allow-data-movement-across-geographies).
