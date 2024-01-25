---
title: Arbeidsflyter i Dynamics 365 Business Central
description: Bruk innebygde funksjoner i arbeidsflyten til å definere godkjenningsarbeidsflyter til å supplere automatiserte arbeidsflyter basert på Power Automate. Du kan konfigurere trinn for å tildele oppgaver til forskjellige personer som en del av de ulike forretningsprosessoppgavene.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 10/10/2022
ms.custom: bap-template
---
# Arbeidsflyter i Dynamics 365 Business Central

Du kan definere og bruke arbeidsflyter til å koble forretningsprosessoppgaver som utføres av forskjellige brukere. Systemoppgaver, for eksempel automatisk bokføring, kan tas med som trinn i arbeidsflytprosesser. Systemoppgaver kan innledes eller etterfølges av brukeroppgaver. Å be om og gi godkjenning til å opprette nye oppføringer er typiske arbeidsflyttrinn.

Standardversjonen av [!INCLUDE [prod_short](includes/prod_short.md)] støtter disse typene arbeidsflyter:
  
* Power Automate-flyter

  * Automatiserte flytprosesser som utløses av hendelser (som oppførings- eller dokumentoppretting, -endring eller -sletting) i [!INCLUDE[prod_short](includes/prod_short.md)]. Også inkludert er godkjenningsflytprosesser som opprettes i Power Automate, som kan utløses når det bes om godkjenning i [!INCLUDE[prod_short](includes/prod_short.md)].
  * Direkteflytprosesser som manuelt utløses fra **Automatiser**-handlingsmenyen på lister, kort og dokumentsider.

    Opprett og manuelt utløs en Power Automate-flyt i en [!INCLUDE[prod_short](includes/prod_short.md)]-post, for eksempel en kunde, vare eller ordre, med alternativer for å manipulere informasjon både internt og eksternt (ved hjelp av integrerte verktøy).

* Godkjenningsarbeidsflyt basert på innebygde arbeidsflytmaler

  På siden **Arbeidsflytmaler** kan du se alle tilgjengelige arbeidsflyter. Prøveversjonen av [!INCLUDE[prod_short](includes/prod_short.md)] omfatter mange forhåndskonfigurerte arbeidsflyter representert av arbeidsflytmaler som du kan kopiere for å opprette nye. Når du åpner en mal fra siden **Arbeidsflytmaler** og arbeidsflytnavnet starter med *MS-*, ble malen lagt til av Microsoft.

## Power Automate-flyter

Med [!INCLUDE [prod_short](includes/prod_short.md)] online kan du registrere deg for Power Automate for å bygge kraftige automatiserte arbeidsflyter. Du kan kjøre arbeidsflytene fra [!INCLUDE [prod_short](includes/prod_short.md)]. Flytene kan koble til interne og eksterne datakilder og verktøy, uten å kodekunnskap.

|**Hvis du vil** |**Se**|
|-------|-------|
|Kom i gang med Power Automate, opprett flyter og kjør direkteflyter|[Bruk Power Automate-flyter i [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md)|
|Finn ut mer om hvordan du oppretter, redigerer og behandler flytprosesser|[Konfigurer automatiserte flytprosesser](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) og [Konfigurer direkteflytprosesser](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)|
|Konfigurer Power Automate-integrering med [!INCLUDE[prod_short](includes/prod_short.md)] for brukere som administrator|[Konfigurer Power Automate-integrering](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup)|

## Arbeidsflyter for godkjenning

Opprett en arbeidsflyt for godkjenning ved å definere hva arbeidsflyten skal starte, og hva som skjer etterpå, på denne måten:

* En arbeidsflythendelse som er moderert av hendelsesbetingelser.
* et arbeidsflytsvar som er moderert av svaralternativer

For å definere arbeidsflyttrinn må du fylle ut felter på arbeidsflytlinjer ved å bruke hendelsen og svar som representerer scenarioer som støttes.

Eksempler på hendelser for arbeidsflyt for godkjenning omfatter blant annet oppretting av ordrer eller bestillinger / tilbud / fakturaer, prisendringer, leverandør- eller kundeendringer med mer.

[!INCLUDE[workflow](includes/workflow.md)]

| **Hvis du vil** | **Se** |
|--|--|
| Definer brukere for arbeidsflyt for godkjenning, angi hvordan brukere skal varsles, og opprett nye arbeidsflyter. (For å opprette nye arbeidsflyter for scenarier som ikke støttes, kan du implementere nødvendige arbeidsflytelementer ved å tilpasse programkoden.) | [Konfigurer godkjenningsarbeidsflyter](across-set-up-workflows.md) |
| Aktiver arbeidsflyter for godkjenning, handle på arbeidsflytvarsler, inkludert å be om og godkjenne et flyttrinn. Arkiver og slett arbeidsflyter. | [Bruk arbeidsflyter for godkjenning](across-use-workflows.md) |

<!--
| Integrate company data with Power Automate workflows, using both internal and external sources and events to create and automate tasks or workflows. | [Use Power Automate Flows in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md) |-->

## Se også

[Salg](sales-manage-sales.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Administrere prosjekter](projects-manage-projects.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Feilsøk automatiserte arbeidsflyter for [!INCLUDE[prod_short](includes/prod_short.md)]](across-flow-troubleshoot.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
