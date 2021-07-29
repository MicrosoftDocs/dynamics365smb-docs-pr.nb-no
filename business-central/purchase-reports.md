---
title: Kjøpsrapporter og analyser
description: Se hvilke kjøpsrapporter og analyser som er tilgjengelige i standardversjonen av Business Central, slik at du kan holde oversikt over virksomheten.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 3f818e556b2ebe3f50189b0057f1302a5598d904
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543173"
---
# <a name="purchase-reports-and-analytics-in-business-central"></a>Kjøpsrapporter og analyser i Business Central

Kjøpsrapportering i [!INCLUDE [prod_short](includes/prod_short.md)] gjør det mulig for innkjøps- og forretningsfolk å få innsikt og statistikk om gjeldende og tidligere kjøpsaktiviteter.  

## <a name="reports"></a>Rapporter

Tabellen nedenfor beskriver noen av nøkkelrapportene i kjøpsrapportering.

|Rapport |Objekt-ID|Beskrivelse  |
|---------|---------|---------|
|**Kjøpsstatistikk**|312|[!INCLUDE [reports-purchase-statistics](includes/reports-purchase-statistics.md)]|
|**Leverandør – ti på topp-liste**|311|Viser informasjon om kjøp fra leverandører for en bestemt periode. Du kan bestemme antall leverandører som skal inngå i rapporten.<br>Leverandørene sorteres etter beløp, og du bestemmer om de skal sorteres etter kjøpsbeløp eller saldo. Rapporten gir et raskt overblikk over hvilke leverandører du har mest utestående hos, eller handler mest hos.|
|**Leverandørvarekatalog** eller **Vare-/leverandørkatalog**|320 eller 720|Viser en liste over leverandører for valgte varer eller varer for utvalgte leverandører. For hver kombinasjon av vare og leverandør vises opplysninger om direkte enhetskost, leveringstid og leverandørers varenummer.<br>I USA, Canada og Mexico er ikke denne rapporten tilgjengelig. Bruk i stedet rapporten **Vare-/leverandørkatalog** (10164).|
|**Leverandør/vare-kjøp**|313|Viser en oversikt over vareposter for hver leverandør i en bestemt periode. Rapporten inneholder opplysninger om fakturert antall, beløp og eventuelle rabatter. Den kan for eksempel brukes til å analysere varekjøp for et selskap, og til å vise om det er en forbindelse mellom rabatter og varekjøp.|
|**Lagerkost og prisliste**|716|Viser en oversikt over prisinformasjon om de valgte varene eller lagerføringsenhetene: direkte enhetskost, siste direkte kostnad, salgspris, fortjenesteprosent og fortjeneste.|
|**Lager – tilgjengelighetsoversikt**|707|Hvis du vil ha en oversikt over bestemte varer/lagerføringsenheter og deres tilgjengelighet. Denne rapporten viser samlede verdier som bruttokrav, tidsplanlagte og planlagte mottak, lageret og så videre. |
|**Vare/leverandør-statistikk**|714|Viser en oversikt over leverandører som firmaet har kjøpt varer fra i en bestemt periode. Den viser opplysninger om fakturert antall, beløp og rabatt. Rapporten kan brukes til analyse av firmaets varekjøp.|
|**Varer i bestillinger**|709|Viser en oversikt over varer i bestilling fra leverandører. Den viser også opplysninger om mottaksdato og eventuell restordre i antall og beløp. Rapporten kan for eksempel brukes til å gi et overblikk over når du kan forvente å få levert varer, og om det skal utstedes en påminnelse om restordre|
|**Reserv. tilgjengelig for kjøp**|409|Viser tilgjengeligheten av varer for levering på kjøpsbilag, for eksempel ordrereturer. Du bestemmer om rapporten skal angi status for hvert bilag eller for hver bestillingslinje. <br>Når du skriver ut rapporten, kan du også oppdatere antallet som er tilgjengelig for levering i feltet **Motta (antall)** på bestillingslinjene. På kjøpskreditnota og negative bestillingslinjer inneholder feltet **Motta (antall)** antallet som skal leveres. Deretter kan du bruke rapporten til å bestemme hvilke bilag som skal leveres. **Obs**! Denne rapporten er ikke tilgjengelig for avanserte lagerfunksjoner.|
<!--|**Leverandør – forfalte poster**|11006| DACH-spesifikk: en rapport som kan brukes av teamlederen for den kjøpte avdelingen som skal ordne regnskapet. Her får du en oversikt over de ubetalte leverandørfakturaene, inkludert forfallsdatoer, valuta og beløp. Grunnlaget er de åpne leverandørpostene.| -->




## <a name="tasks"></a>Oppgaver

Følgende artikler beskriver noen av de viktige oppgavene for å analysere tilstanden i virksomheten din:

* [Opprette analyserapporter](bi-how-create-analysis-views-reports.md)  
* [Vis tilgjengeligheten av varer](inventory-how-availability-overview.md)  


## <a name="see-also"></a>Se også

[Definere kjøp](purchasing-setup-purchasing.md)  
[Innkjøp](purchasing-manage-purchasing.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
