---
author: edupont04
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c2f5f4c264150802920169139c90c0456f9a27c4
ms.sourcegitcommit: cdb57f14960f58b1d36a1b373fbf35dfed5fad9e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/23/2022
ms.locfileid: "8334853"
---
Tabellen nedenfor beskriver noen av nøkkelrapportene i leverandørrapportering.

| Rapport | Beskrivelse | ID | 
|--|--|--|
| [Aldersfordelt saldoliste – leverandør](https://businesscentral.dynamics.com?report=322) |Viser forfalte saldoer for leverandører i forfalte intervaller. De forfalte beløpene kan vises etter forfallsdato, bokføringsdato eller bilagsdato etter behov. Du kan velge å vise beløpene i lokal valuta (LV) og skrive ut detaljer for de forfalte dokumentene. Tidsintervallene kan ha overskrifter med datoer eller med antall forfalte datoer i forhold til den angitte aldersfordelingen.<br>Denne rapporten er hovedrapporten for avstemming av leverandørposter til finans. Hvis du antar at du ikke har lov til å bokføre på kontoene som brukes i konto for leverandørbokføringsgrupper, er denne rapporten en spesifikasjon av beløpene du finner i finans.| 322|
| [Leverandør – saldo per dato](https://businesscentral.dynamics.com?report=321) | Viser leverandørsaldoen etter sluttdato for angitt datointervall. Du kan velge å vise leverandørsaldoen i lokal valuta (LV). Merk av for **Ta med ikke-utlignede poster** hvis du vil vise poster som har blitt lukket av sluttdatoen, men som er ikke-utlignet (åpnet) på et senere tidspunkt. Merk av for **Vis poster med nullsaldo** for å vise leverandører med en saldo på null ved sluttdatoen i datofilteret. Datofilteret gjelder den detaljerte leverandørposten for postene i rapporten. Hvis du har betalinger senere enn sluttdatoen som er utlignet mot fakturaer innen datointervallet, vises fakturaene i rapporten ettersom sluttdatoen ikke er blitt lukket. | 321 |
| [Leverandør – råbalanse](https://businesscentral.dynamics.com?report=329) | Viser bevegelsen for leverandører for perioden som er angitt i datofilteret, i tillegg til bevegelsesår for regnskapsåret som tilsvarer den valgte perioden. Rapporten grupperes etter bokføringsgrupper for leverandør og gir en annen visning av leverandørposten enn rapporten **Aldersfordelt saldoliste – leverandør**. **Obs!** Hvis du ikke har definert noen regnskapsperioder, vil ikke systemet vite hvilket regnskapsår som skal brukes, og enten vise år til dato fra det siste regnskapsåret som er definert, eller bare velge perioden, som kanskje ikke kommer fra begynnelsen av et år.|329 | 
| [Leverandør – finanskontoutdrag](https://businesscentral.dynamics.com?report=304) | Viser alle leverandørpostene i det angitte datofilteret. Rapporten viser leverandørens startsaldoer i forhold til datofilteret. | 304 | 
| [Kjøpsstatistikk](https://businesscentral.dynamics.com?report=312) |[!INCLUDE [reports-purchase-statistics](reports-purchase-statistics.md)]<br>Denne rapporten kan også brukes i leverandører etter hvert som det er enklere å foreta et raskt oppslag av bokførte betalinger, rabatter og andre transaksjoner for en gitt leverandør.| 312 |
| [Leverandør – forfallsoversikt](https://businesscentral.dynamics.com?report=305)| Eldre rapport for aldersfordelt saldoliste – leverandør. Vi anbefaler at du bruker rapporten **Aldersfordelt saldoliste – leverandør** i stedet. Du kan velge periodelengde og en dato som skal brukes som angitt *forfalte per*-dato.|305| 
| [Avvent. utbetalinger](https://businesscentral.dynamics.com?report=319)| Viser leverandørposter der **Avvent**-feltet ikke er tomt.| 319 |
| [Forhåndsutbetalingskladd for leverandør](https://businesscentral.dynamics.com?report=317)|Viser betalingskladden med informasjon om kontantrabatt og betalingstoleranse. Rapporten kan brukes til å kontrollere betalinger før du oppretter betalingsfiler og bokfører kladden. **Obs!** Rapporten vil vise kontantrabatter på feil måte når det er brukt flere kreditnotaer i en utligning. I dette tilfellet vises kontantrabatten for resten av kreditnotaene som et ikke-utlignet beløp.| 317 |
| [Leverandør – liste](https://businesscentral.dynamics.com?report=301)|Viser diverse grunnleggende opplysninger om leverandører, for eksempel leverandørbokføringsgruppe, rabatt- og betalingsinformasjon, prioritetsnivå og leverandørens standardvaluta og leverandørens saldo (i LV). Rapporten kan for eksempel brukes til ajourføring av opplysningene i tabellen Leverandør.|301|