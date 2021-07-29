---
title: Kunderapporter og -analyse
description: Se hvilke rapporter og analyser som er tilgjengelige i standardversjonen av Business Central, slik at du kan holde oversikt over kunder.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 07/13/2021
ms.author: edupont
ms.openlocfilehash: 76de1625ee71b666b01d6b2fef1efe5605d9a418
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543360"
---
# <a name="accounts-receivable-reports-and-analytics-in-business-central"></a>Kunderapporter og analyser av aktiva i Business Central

For å hjelpe deg med å administrere kunder i [!INCLUDE [prod_short](includes/prod_short.md)] er standardrapporter og analyse innebygd. Det flytter seg utenfor tradisjonelle rapporteringsbegrensninger for å hjelpe deg med å utforme forskjellige typer rapporter effektivt.  

## <a name="reports"></a>Rapporter

Tabellen nedenfor beskriver noen av nøkkelrapportene i kunderapportering.

| Rapport | Objekt-ID | Beskrivelse |
|--|--|--|
| **Aldersfordelt saldoliste – kunder** | 120 | Viser beløpet som gjenstår med kunder inndelt i tidsintervaller for tiden som er forfalt. Rapporten viser også hvilken del av kundens saldoen som ikke forfaller, og som kan vises med eller uten dokumentdetaljer for hver kunde. Denne rapporten er hovedrapporten for avstemming av kundeposter til finans. Hvis du antar at du ikke har lov til å bokføre på kontoene som brukes i konto for kundebokføringsgrupper, er denne rapporten en spesifikasjon av beløpene du finner i finans. |
| **Kundeutskrift** | 1316 | Genererer en kontoutskrift for et angitt tidsintervall. Den sendes vanligvis til kundene for å gi dem en oversikt over utestående beløp, og også som purring for å betale eventuelle forfalte beløp. Du kan velge å vise de forfalte beløpene i en separat del. Du kan inkludere et aldersfordeling som ligner på den som brukes i **Aldersfordelt saldoliste – kunder**. Når det gjelder aldersfordelingen, angir du vanligvis *30D*, som betyr 30 dager, for eksempel 30, 60, 90 og 90+ dager forfalt, fra sluttdatoen eller *1M+CM*, som vil være den gjeldende måneden i et eget intervall, og så månedlige intervaller for de foregående månedene. **Obs!** i kundeoversikten har denne rapporten også en egen handling, **Planlagte utdrag**. Dette alternativet filtrerer ikke kunden du har valgt. Det er samme rapport, men brukes når du vil sende utdrag til alle/flere kunder. |
| **Kunde – saldo per dato** | 121 | Viser de åpne kundepostene frem til sluttdatoen. Denne rapporten viser lignende innhold som kundeutdraget, men uten indikasjon på at posten er forfalt. **Obs!** Datofilteret vil bli brukt på de detaljerte kundepostene. Dette betyr at hvis du har betalinger senere enn sluttdatoen som er utlignet mot fakturaer innen datointervallet, vises fakturaene i rapporten ettersom sluttdatoen ikke er blitt lukket. |
| **Kunde – saldoliste** | 129 | Viser bevegelsen for kunder for perioden som er angitt i datofilteret, i tillegg til bevegelsesår for regnskapsåret som tilsvarer den valgte perioden. Rapporten grupperes etter bokføringsgrupper for kunde og gir en annen visning av kundeposten enn rapporten **Aldersfordelt saldoliste – kunde**. **Obs!** Hvis du ikke har definert noen regnskapsperioder, vil ikke systemet vite hvilket regnskapsår som skal brukes, og enten vise år til dato fra det siste regnskapsåret som er definert, eller bare velge perioden, som kanskje ikke kommer fra begynnelsen av et år.|
| **Kunde – finanskontoutdrag** | 104 | Viser alle kundepostene i det angitte datofilteret. Denne rapporten brukes vanligvis til å kontrollere at alle poster for en bestemt kunde er beregnet på eller andre interne sjekker i kundeposter. |
| **Kunde – kvittering** | 211 | Oppretter en kvittering for hver kundepost av typen **Betaling**. Hvis betalingen er utlignet mot fakturaer, blir fakturaene angitt. Hvis ikke vil den bare angi betalingsbeløpet som ikke-utlignet. Denne rapporten brukes til å sende til kunder som ønsker dokumentasjon for betalingskvittering.|
| **Avstem kunde- og leverandørkonti** | 33 |Viser finanspostene som er et resultat av bokføring av kunde- og leverandørposter per finanskonto og bokføringsgrupper. Denne rapporten brukes til å avstemme saldoene på kunde- og leverandørposter til finanssaldoer. |
| **Kunde – enkel forfallsoversikt**| 109 |Dette er en eldre versjon av en aldersfordelt rapport for kunder. Vi anbefaler at du bruker rapporten **Aldersfordelt saldoliste – kunde** i stedet. |
| **Salgsstatistikk** |112  |[!INCLUDE [reports-sales-statistics](includes/reports-sales-statistics.md)]<br>Denne rapporten kan også brukes i kunder etter hvert som det er enklere å foreta et raskt oppslag av bokførte betalinger, rabatter og salg for en gitt kunde.|
|**Kundeoversikt**|101| Viser diverse grunnleggende informasjon om kunder, for eksempel kundebokføringsgruppe, rabattgruppe, rentenota- og betalingsinformasjon, selger, kundens standardvaluta og kredittgrense i lokal valuta (NOK) og kundens gjeldende saldo (i NOK). Rapporten kan for eksempel brukes til å vedlikeholde opplysningene i tabellen Kunde.|

## <a name="see-also"></a>Se også

[Analysere årsregnskap i Microsoft Excel](finance-analyze-excel.md)  
[Arbeide med dimensjoner](finance-dimensions.md)  
[Administrer aktiva](fa-manage.md)  
[Oversikt over lokal funksjonalitet](about-localization.md)  
[Regnskapsføreropplevelser i [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
