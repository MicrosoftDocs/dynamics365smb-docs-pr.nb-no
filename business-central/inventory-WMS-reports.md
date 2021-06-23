---
title: Lager og lagerrapporter og analyse
description: Se hvilke beholdnings- og lagerrapporter og analyser som er tilgjengelige i standardversjonen av Business Central, slik at du kan holde oversikt over virksomheten.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 8a4418699f28acd3ede80616ba69c56f50781e43
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216383"
---
# <a name="inventory-and-warehouse-reports-and-analytics-in-business-central"></a>Lager og lagerrapporter og analyse i Business Central

Beholdnings- og lagerrapportering i [!INCLUDE [prod_short](includes/prod_short.md)] gjør det mulig for lager- og forretningsfolk å få innsikt og statistikk om gjeldende og tidligere beholdnings- og lageraktiviteter.  

## <a name="reports"></a>Rapporter

Tabellen nedenfor beskriver noen av nøkkelrapportene i beholdnings- og lagerrapportering.

|Rapport |Objekt-ID|Beskrivelse  |
|---------|---------|---------|
|**Lager – tilgjengelighetsoversikt**|707|Hvis du vil ha en oversikt over bestemte varer/lagerføringsenheter og deres tilgjengelighet. Denne rapporten viser samlede verdier som bruttokrav, tidsplanlagte og planlagte mottak, lageret og så videre. |
|**Lagerverdisetting**|1001|Viser lagerverdi for bestemte varer på lager. Rapporten viser også opplysninger om verdien av økninger og reduksjoner i lagerbeholdningen over tid.|
|**Vareholdbarhet – mengde**|5809|Viser en oversikt over antallet valgte varer på lageret med vareholdbarhetsdatoer som er i en bestemt periode. Listen inneholder antallet enheter av den valgte varen som utløper i en gitt tidsperiode. For hver vare du angir når du definerer rapporten, viser utskriften antallet enheter som utløper i løpet av hver av tre like lange perioder, og samlet lagerantall av den valgte varen.<br>Du kan angi hva som skal inkluderes i rapporten, ved å definere filtre. Hvis du ikke definerer filtre, tar rapporten med alle postene. Antallet i rapporten gjenspeiler bare antallet av varen som holdbarhetsdatoer er definert for.|
|**Varealder – antall** eller **Varealder – verdi**|5807 eller 5808|Viser en oversikt over alderen på utvalgte varer i beholdningen. Oversikten viser hvor mange enheter eller verdier som ble lagt til eller fjernet fra lageret, og når dette ble gjort. Det blir lagt til eller fjernet varer fra lager ved kjøp, salg og opp- og nedjusteringer.|
|**Lagerkost og prisliste**|716|Viser en oversikt over prisinformasjon om de valgte varene eller lagerføringsenhetene: direkte enhetskost, siste direkte kostnad, salgspris, fortjenesteprosent og fortjeneste. |
|**Lagerhylle – oversikt**|7319|Viser en oversikt over lagerhyller, oppsettet og antall varer i hyllene. Denne rapporten kan brukes for alle lokasjoner som har «hylle» som obligatorisk-felt. |
|**Lagerleveringsstatus**|7313|Viser en oversikt over åpne kildedokumenter med leverte varer eller varer klare til levering per lokasjon. Denne rapporten kan brukes for alle lokasjoner der **Nødvendige leveringer** er aktivert. **Lagerleveringsstatus** viser lokasjoner, hyllekoder, dokumentstatus, antall.|
|**Lagerplukkliste**|813|Viser en oversikt over ordrer der en vare er inkludert. Følgende informasjon vises for hver vare: ordrelinje med kundenavn, variantkode, lokasjonskode, hyllekode, leveringsdato, mengde som skal leveres og enhet. Mengden som skal leveres legges sammen for hver vare. Rapporten kan for eksempel brukes når det skal hentes varer fra lageret.<br>Obs! Denne funksjonen er ikke tilgjengelig for avanserte lagerfunksjoner.|
|**Lagerjusteringshylle**|7320|Denne spesialrapporten er bare beregnet for et avansert lager og viser de gjenstående antallene som fortsatt er lagret i selve justeringshyllen. Vanligvis vil denne bestemte hyllen være tom. Den eneste årsaken når denne hyllen skal fylles, er resultatet av fysisk opptellingsprosess, eller om antall varer er blitt fjernet eller lagt til i lageret|


## <a name="tasks"></a>Oppgaver

Følgende artikler beskriver noen av de viktige oppgavene for å analysere tilstanden i virksomheten din:

* [Opprette analyserapporter](bi-how-create-analysis-views-reports.md)  
* [Vis tilgjengeligheten av varer](inventory-how-availability-overview.md)


## <a name="see-also"></a>Se også

[Definere lager](inventory-setup-inventory.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)  
[Lagerstyring](warehouse-manage-warehouse.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
