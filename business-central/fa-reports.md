---
title: Rapporter og analyse av aktiva
description: Se hvilke rapporter og analyser som er tilgjengelige i standardversjonen av Business Central, slik at du kan holde oversikt over aktivaene.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 07/13/2021
ms.author: edupont
ms.openlocfilehash: c28e62a2de51323e0a7dcd2f4b5ea26d5896d718
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543359"
---
# <a name="fixed-assets-reports-and-analytics-in-business-central"></a>Rapporter og analyser av aktiva i Business Central

For å hjelpe deg med å administrere aktiva i [!INCLUDE [prod_short](includes/prod_short.md)] er standardrapporter og analyse innebygd. Det flytter seg utenfor tradisjonelle rapporteringsbegrensninger for å hjelpe deg med å utforme forskjellige typer rapporter effektivt.  

## <a name="reports"></a>Rapporter

Tabellen nedenfor beskriver noen av nøkkelrapportene i aktivarapportering.

| Rapport | Objekt-ID | Beskrivelse |
|--|--|--|
| **Aktivaoversikt** | 5601 | Viser oversikten over aktiva og tilhørende oppsettsopplysninger for et gitt avskrivningstablå. |
| **Aktiva – anskaffelsesoversikt** | 5608 | Viser alle aktiva som er anskaffet innenfor et gitt datointervall. Du kan også ta med aktiva som er opprettet, men ennå ikke anskaffet. |
| **Detaljer for aktivum** | 5604 | Viser aktivapostene for aktiva. |
| **Analyse av aktivum** | 5600 | Analyserapporten der du kan angi to datokolonner og tre datakolonner som skal vises i rapporten. Hvis du for eksempel vil generere en rapport som skal brukes til avstemming med finans, legger du til kolonner for anskaffelseskostnad ved sluttdato, avskrivninger for sluttdato og bokført verdi ved sluttdato. En kontrollrapport kan ha anskaffelser/bevegelse, nedskrivning/bevegelse, og oppskrivning/bevegelse, slik at alle endringer i aktiva kan kontrolleres om nødvendig. Hvis du velger **Budsjettrapport**-feltet og angir en sluttdato senere, beregner rapporten fremtidig avskrivning og kan gi estimater for fremtidige avskrivnings- og bokverdier hvis du valgte disse feltene som rapportkolonner. |
| **Forventet verdi for aktivum** | 5607 | Viser de forventede avskrivningsbeløpene og den bokførte verdien for en fremtidig periode for aktiva. Rapporten er nyttig når du for eksempel bruker ulike avskrivningsmetoder for aktiva og du vil estimere neste års avskrivning. Bruk rapporten til å opprette budsjettbeløpene for avskrivning ved å velge et budsjett og feltet **Kopier til finansbudsjett**. |
| **Aktiva – bokført verdi 01** | 5605 | Viser detaljert informasjon om anskaffelseskost, avskrivingsverdi og bokført verdi både for individuelle aktiva og grupper av disse. For hver av disse beløpstypene blir beløpene beregnet i begynnelsen og slutten av en gitt periode, samt for selve perioden. Hvis du velger feltet **Budsjettrapport**, vil rapporten beregne den forventede avskrivningen for perioden. Angi en *gruppetype* hvis du vil at rapporten skal gruppere aktiva og skrive ut gruppetotaler. Hvis du for eksempel har opprettet seks aktivaklasser, kan du velge alternativet *Aktivaklasse* for å få gruppetotaler utskrevet for hver av de seks klassekodene.|
| **Aktiva – bokført verdi 02** | 5606 |Viser en oversikt over aktivatablåverdien ved endringer i anskaffelse, avskrivning og oppskrivning innenfor perioden, med en ytterligere analyse etter tillegg og avhending i perioden. Bruk denne rapporten til å beskrive endringene i aktiva for en gitt periode når mange forskjellige endringer forekommer på tvers av aktiva. Hvis du velger feltet **Budsjettrapport**, vil rapporten beregne den forventede avskrivningen for perioden. Angi en *gruppetype* hvis du vil at rapporten skal gruppere aktiva og skrive ut gruppetotaler. Hvis du for eksempel har opprettet seks aktivaklasser, kan du velge alternativet *Aktivaklasse* for å få gruppetotaler utskrevet for hver av de seks klassekodene. |
| **Finansanalyse for aktivum**| 5610 |Viser en analyse av dine aktiva med ulike typer data for individuelle aktiva og/eller grupper av disse. På hurtigfanen Aktiva kan du definere filtre hvis du vil at rapporten bare skal ta med enkelte aktiva. På hurtigfanen Alternativer skreddersyr du rapporten slik at den dekker dine behov. Rapporten ligner på **rapporten for aktivaanalyse**, men spesifikt for å avstemme finans og spesifikt for validering av salgsposter. Rapporten forutsetter at du kjenner finanskontiene som er angitt i bokføringsoppsettet. |
| **Aktivajournal** |5603  |Viser bokførte aktivaposter, sortert og inndelt etter journalnummer. Du kan angi hvilken journals poster som skal vises, ved å definere filter. Det er viktig å definere filter, ellers kan rapporten komme til å vise en enorm mengde informasjon. |

## <a name="see-also"></a>Se også

[Analysere årsregnskap i Microsoft Excel](finance-analyze-excel.md)  
[Arbeide med dimensjoner](finance-dimensions.md)  
[Administrer aktiva](fa-manage.md)  
[Oversikt over lokal funksjonalitet](about-localization.md)  
[Regnskapsføreropplevelser i [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
