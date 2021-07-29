---
title: Leverandørrapporter og -analyse
description: Se hvilke rapporter og analyser som er tilgjengelige i standardversjonen av Business Central, slik at du kan holde oversikt over leverandører.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 07/13/2021
ms.author: edupont
ms.openlocfilehash: 774fd24bc15cb4cefb56991289d9c72c0909a319
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543361"
---
# <a name="accounts-payable-reports-and-analytics-in-business-central"></a>Leverandørrapporter og analyser av aktiva i Business Central

For å hjelpe deg med å administrere leverandører i [!INCLUDE [prod_short](includes/prod_short.md)] er standardrapporter og analyse innebygd. Det flytter seg utenfor tradisjonelle rapporteringsbegrensninger for å hjelpe deg med å utforme forskjellige typer rapporter effektivt.  

## <a name="reports"></a>Rapporter

Tabellen nedenfor beskriver noen av nøkkelrapportene i leverandørrapportering.

| Rapport | Objekt-ID | Beskrivelse |
|--|--|--|
| **Aldersfordelt saldoliste – leverandør** | 322|Viser forfalte saldoer for leverandører i forfalte intervaller. De forfalte beløpene kan vises etter forfallsdato, bokføringsdato eller bilagsdato etter behov. Du kan velge å vise beløpene i lokal valuta (NOK) og skrive ut detaljer for de forfalte dokumentene. Tidsintervallene kan ha overskrifter med datoer eller med antall forfalte datoer i forhold til den angitte aldersfordelingen.<br>Denne rapporten er hovedrapporten for avstemming av leverandørposter til finans. Hvis du antar at du ikke har lov til å bokføre på kontoene som brukes i konto for leverandørbokføringsgrupper, er denne rapporten en spesifikasjon av beløpene du finner i finans.|
| **Leverandør – saldo per dato** | 321 | Viser leverandørsaldoen etter sluttdato for angitt datointervall. Du kan velge å vise leverandørsaldoen i lokal valuta (NOK). Merk av for **Ta med ikke-utlignede poster** hvis du vil vise poster som har blitt lukket av sluttdatoen, men som er ikke-utlignet (åpnet) på et senere tidspunkt. Merk av for **Vis poster med nullsaldo** for å vise leverandører med en saldo på null ved sluttdatoen i datofilteret. Datofilteret gjelder den detaljerte leverandørposten for postene i rapporten. Hvis du har betalinger senere enn sluttdatoen som er utlignet mot fakturaer innen datointervallet, vises fakturaene i rapporten ettersom sluttdatoen ikke er blitt lukket. |
| **Leverandør – råbalanse** | 329 | Viser bevegelsen for leverandører for perioden som er angitt i datofilteret, i tillegg til bevegelsesår for regnskapsåret som tilsvarer den valgte perioden. Rapporten grupperes etter bokføringsgrupper for leverandør og gir en annen visning av leverandørposten enn rapporten **Aldersfordelt saldoliste – leverandør**. **Obs!** Hvis du ikke har definert noen regnskapsperioder, vil ikke systemet vite hvilket regnskapsår som skal brukes, og enten vise år til dato fra det siste regnskapsåret som er definert, eller bare velge perioden, som kanskje ikke kommer fra begynnelsen av et år.|
| **Leverandør – finanskontoutdrag** | 304 | Viser alle leverandørpostene i det angitte datofilteret. Rapporten viser leverandørens startsaldoer i forhold til datofilteret. |
| **Kjøpsstatistikk** |312 |[!INCLUDE [reports-purchase-statistics](includes/reports-purchase-statistics.md)]<br>Denne rapporten kan også brukes i leverandører etter hvert som det er enklere å foreta et raskt oppslag av bokførte betalinger, rabatter og andre transaksjoner for en gitt leverandør.|
|**Leverandør – forfallsoversikt**|305| Eldre rapport for aldersfordelt saldoliste – leverandør. Vi anbefaler at du bruker rapporten **Aldersfordelt saldoliste – leverandør** i stedet. Du kan velge periodelengde og en dato som skal brukes som angitt *forfalte per*-dato.|
|**Avvent. utbetalinger**|319|Viser leverandørposter der **Avvent**-feltet ikke er tomt.|
|**Forhåndsutbetalingskladd for leverandør**|317|Viser betalingskladden med informasjon om kontantrabatt og betalingstoleranse. Rapporten kan brukes til å kontrollere betalinger før du oppretter betalingsfiler og bokfører kladden. **Obs!** Rapporten vil vise kontantrabatter på feil måte når det er brukt flere kreditnotaer i en utligning. I dette tilfellet vises kontantrabatten for resten av kreditnotaene som et ikke-utlignet beløp.|
|**Leverandør – liste**|301|Viser diverse grunnleggende opplysninger om leverandører, for eksempel leverandørbokføringsgruppe, rabatt- og betalingsinformasjon, prioritetsnivå og leverandørens standardvaluta og leverandørens saldo (i NOK). Rapporten kan for eksempel brukes til ajourføring av opplysningene i tabellen Leverandør.|

## <a name="see-also"></a>Se også

[Analysere årsregnskap i Microsoft Excel](finance-analyze-excel.md)  
[Arbeide med dimensjoner](finance-dimensions.md)  
[Administrer aktiva](fa-manage.md)  
[Oversikt over lokal funksjonalitet](about-localization.md)  
[Regnskapsføreropplevelser i [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
