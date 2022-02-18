---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ae96e5a3fc1cc7f4b17e5ef208650248cbe0b3c2
ms.sourcegitcommit: 2c972dfc94d27245eaa99efcf638d030dedafb22
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/09/2022
ms.locfileid: "8104267"
---
Tabellen nedenfor beskriver noen av nøkkelrapportene i kjøpsrapportering.

|Rapport |Objekt-ID|Beskrivelse  |
|---------|---------|---------|
|**Kjøpsstatistikk**|312|[!INCLUDE [reports-purchase-statistics](reports-purchase-statistics.md)]|
|**Leverandør – ti på topp-liste**|311|Viser informasjon om kjøp fra leverandører for en bestemt periode. Du kan bestemme antall leverandører som skal inngå i rapporten.<br>Leverandørene sorteres etter beløp, og du bestemmer om de skal sorteres etter kjøpsbeløp eller saldo. Rapporten gir et raskt overblikk over hvilke leverandører du har mest utestående hos, eller handler mest hos.|
|**Leverandørvarekatalog** eller **Vare-/leverandørkatalog**|320 eller 720|Viser en liste over leverandører for valgte varer eller varer for utvalgte leverandører. For hver kombinasjon av vare og leverandør vises opplysninger om direkte enhetskost, leveringstid og leverandørers varenummer.<br>I USA, Canada og Mexico er ikke denne rapporten tilgjengelig. Bruk i stedet rapporten **Vare-/leverandørkatalog** (10164).|
|**Leverandør/vare-kjøp**|313|Viser en oversikt over vareposter for hver leverandør i en bestemt periode. Rapporten inneholder opplysninger om fakturert antall, beløp og eventuelle rabatter. Den kan for eksempel brukes til å analysere varekjøp for et selskap, og til å vise om det er en forbindelse mellom rabatter og varekjøp.|
|**Lagerkost og prisliste**|716|Viser en oversikt over prisinformasjon om de valgte varene eller lagerføringsenhetene: direkte enhetskost, siste direkte kostnad, salgspris, fortjenesteprosent og fortjeneste.|
|**Lager – tilgjengelighetsoversikt**|707|Hvis du vil ha en oversikt over bestemte varer/lagerføringsenheter og deres tilgjengelighet. Denne rapporten viser samlede verdier som bruttokrav, tidsplanlagte og planlagte mottak, lageret og så videre. |
|**Vare/leverandør-statistikk**|714|Viser en oversikt over leverandører som firmaet har kjøpt varer fra i en bestemt periode. Den viser opplysninger om fakturert antall, beløp og rabatt. Rapporten kan brukes til analyse av firmaets varekjøp.|
|**Varer i bestillinger**|709|Viser en oversikt over varer i bestilling fra leverandører. Den viser også opplysninger om mottaksdato og eventuell restordre i antall og beløp. Rapporten kan for eksempel brukes til å gi et overblikk over når du kan forvente å få levert varer, og om det skal utstedes en påminnelse om restordre|
|**Reserv. tilgjengelig for kjøp**|409|Viser tilgjengeligheten av varer for levering på kjøpsbilag, for eksempel ordrereturer. Du bestemmer om rapporten skal angi status for hvert bilag eller for hver bestillingslinje. <br>Når du skriver ut rapporten, kan du også oppdatere antallet som er tilgjengelig for levering i feltet **Motta (antall)** på bestillingslinjene. På kjøpskreditnota og negative bestillingslinjer inneholder feltet **Motta (antall)** antallet som skal leveres. Deretter kan du bruke rapporten til å bestemme hvilke bilag som skal leveres. **Obs**! Denne rapporten er ikke tilgjengelig for avanserte lagerfunksjoner.|
<!--|**Leverandør – forfalte poster**|11006| DACH-spesifikk: en rapport som kan brukes av teamlederen for den kjøpte avdelingen som skal ordne regnskapet. Her får du en oversikt over de ubetalte leverandørfakturaene, inkludert forfallsdatoer, valuta og beløp. Grunnlaget er de åpne leverandørpostene.| -->

