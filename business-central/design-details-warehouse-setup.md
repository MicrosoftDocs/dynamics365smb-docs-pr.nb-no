---
title: Designdetaljer – Lageroppsett
description: Lagerfunksjonaliteten inneholder forskjellige typer kompleksitet, som stort sett defineres av oppsettet for hyllen på lokasjonskort.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: 9014836d228ee5bd01a74129fa0ba2aa0dd8dcea
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8142344"
---
# <a name="design-details-warehouse-setup"></a>Designdetaljer: Lageroppsett

Lagerfunksjonaliteten i [!INCLUDE[prod_short](includes/prod_short.md)] inneholder ulike kompleksitetsnivåer, som definert av lisenstillatelser i granulene som tilbys. Kompleksitetsnivået i en lagerløsning er hovedsakelig definert av hylleoppsettet på lokasjonskort, som i sin tur er lisenskontrollert, slik at tilgang til hylleoppsettsfeltene defineres av lisensen. I tillegg styrer programobjektene i lisensen hvilke brukergrensesnittdokument som skal brukes for de støttede lageraktivitetene.  
<!--
The following warehouse-related granules exist:  

- Basic Inventory (4010)  
- Bin (4170)  
- Put Away (4180)  
- Warehouse Receipt (4190)  
- Pick (4200)  
- Warehouse Shipment (4210)  
- Warehouse Management Systems (4620)  
- Internal Picks and Put-aways (4630)  
- Automated Data Capture System (4640)
- Bin Setup (4660)  

For more information about each granule, see [[!INCLUDE[prod_short](includes/prod_short.md)] Price Sheets](https://go.microsoft.com/fwlink/?LinkId=238341) (requires PartnerSource account). -->

Tabellen nedenfor viser hvilke granuler som kreves for å kunne definere ulike kompleksitetsnivåer for lager, hvilke grensesnittdokumenter som støtter hvert nivå, og hvilke lokasjonskoder som gjenspeiler disse nivåene i [!INCLUDE[prod_short](includes/prod_short.md)]-demonstrasjonsdatabasen.  

[!INCLUDE [locations-cronus](includes/locations-cronus.md)]

|Kompleksitetsnivå|Beskrivelse|Grensesnittdokument|Eksempel lokasjon|Minimum granulenkrav|  
|----------------|-----------|-----------|---------------|---------------------------|  
|1|Ingen dedikert lageraktivitet.<br /><br /> Mottaks-/leveringsbokføring fra ordrer.|Bestilling|BLÅ|Grunnleggende lagerbeholdning|  
|2|Ingen dedikert lageraktivitet.<br /><br /> Mottaks-/leveringsbokføring fra ordrer.<br /><br /> Hyllekode kreves.|Ordre, med hyllekode|SØLV|Grunnleggende lagerbeholdning / hylle|  
|3 <br /><br /> **Merk**: Selv om innstillingene kalles **Plukk nødv.** og **Plassering nødv.**, kan du bokføre mottak og leveringer direkte fra kildedokumenter for firma på lokasjoner der du velger disse avmerkingsboksene.|Grunnleggende lageraktiviteten, ordre for ordre.<br /><br /> Mottaks-/leveringsbokføring fra lagerplasserings-/plukkdokumenter. <br /><br /> Hyllekode kreves.|Lagerplassering / Lagerflytting / Lagerplukk med hyllekode|(SØLV + Plassering nødv. eller Plassering nødv.)|Grunnleggende lagerbeholdning / hylle / plassering / plukk|  
|4|Avansert lageraktivitet, for flere ordrer.<br /><br /> Konsoliderte mottaks-/leveringspostering basert på lagerplassering/plukkregistreringer.|Lagermottak/Plassering/Plukk/Lagerlevering/Plukkforslag|GRØNN|Grunnleggende lagerbeholdning / lagermottak / plassering / plukk / lagerlevering|  
|5|Avansert lageraktivitet, for flere ordrer.<br /><br /> Konsoliderte mottaks-/leveringspostering basert på lagerplassering/plukkregistreringer.<br /><br /> Hyllekode kreves.|Lagermottak/Plassering/Plukk/Lagerlevering/Plukkforslag/Plasseringsforslag, med hyllekode|(GRØNN + Hylle obligatorisk)|Grunnleggende lagerbeholdning / hylle / lagermottak / plassering / plukk / lagerlevering|  
|6 <br /><br /> **Obs**! Dette nivået kalles «LA», siden det krever den mest avanserte granulen, Lagerstyringssystem.|Avansert lageraktivitet, for flere ordrer<br /><br /> Konsoliderte mottaks-/leveringspostering basert på lagerplassering/plukkregistreringer<br /><br /> Hyllekode kreves.<br /><br /> Sone-/klassekode er valgfri.<br /><br /> Lagermedarbeidere følger arbeidsflyten<br /><br /> Planlegg etterfylling av hylle<br /><br /> Hylleprioritering<br /><br /> Hylleoppsett etter kapasitet<br /><br /> Plasseringsoptimalisering  <!-- Hand-held device integration -->|Lagermottak/Plassering/Plukk/Lagerlevering/Lagerflytting/Plukkforslag/Plasseringsforslag/Intern. Plukk/Intern plassering, med hylle/klasse/sone-kode<br /><br /> Ulike forslag for hyllehåndtering<br /><br /> ADFS-skjermer|KR.SAND|Grunnleggende lagerbeholdning / hylle / plassering / lagermottak / plukk / lagerlevering / lagerstyringssystemer / interne plukk og plasseringer / hylleoppsett /<!-- Automated Data Capture System/ -->Hylleoppsett|  

Hvis du vil se eksempler på hvordan grensesnittdokumentene brukes for hvert kompleksitetsnivå for lageret, kan du se [Designdetaljer: Inngående lagerflyt](design-details-inbound-warehouse-flow.md).  

## <a name="bin-and-bin-content"></a>Hylle og hylleinnhold

En hylle er en lagringsenhet som er utformet for å inneholde atskilte deler. Dette er den minste beholderenheten i [!INCLUDE[prod_short](includes/prod_short.md)]. Vareantall i hyller kalles hylleinnhold. Et oppslag fra **Vare**-feltet eller **Hyllekode**-feltet på en hvilken som helst lagerrelatert dokumentlinjen viser beregnet tilgjengeligheten for varen på hyllen.  

Et hylleinnhold kan gis egenskapen for Fast, Dedikert eller Standard for å angi hvordan hylleinnholdet kan brukes. Hyller med ingen av disse egenskapene kalles flytende hyller.  

En fast hylle kan inneholde elementer som er tilordnet til den aktuelle hyllekoden. Egenskapen for fast hylle sikrer at hylleinnholdet ikke forsvinner selv om hylleinnholdet tømmes for et øyeblikk, og hyllen velges dermed på nytt så snart den er etterfylt.  

En dedikert hylle inneholder hylleinnhold som bare kan plukkes for dedikert ressurs, for eksempel en produksjonsressurs som bruker den aktuelle hyllen. Annet ikke-plukkinnhold, for eksempel antall utgående på en leveringsbokføring, kan fortsatt brukes fra en dedikert hylle. Bare hylleinnhold som **Opprett plukk**-algoritmen tar hensyn til er beskyttet i en dedikert hylle.  

Egenskapen for standardhylle brukes av systemet til å foreslå hyller for lageraktiviteter. Egenskapen for standardhylle brukes ikke på LA-lokasjoner. På steder der det kreves hyller, brukes egenskapen i inngående flyter til å angi hvor varer skal plasseres. I utgående flyter brukes egenskapen til å angi hvor varer skal plukkes fra.  

> [!NOTE]  
>  Hvis utgående varer er plassert i flere hyller, blir varer først plukket fra ikke-standard hyllene for å tømme dette hylleinnholdet, og deretter blir resten av varene plukket fra standardhyllen.  

Det kan bare finnes én standardhylle per vare per lokasjon.  

## <a name="bin-type"></a>Hylletype

I LA-installasjoner kan du begrense lageraktiviteter som er tillatt for en hylle, ved å tilordne en hylletype til den. Følgende hylletyper finnes:  

|Hylletype|Beskrivelse|  
|------------------|---------------------------------------|  
|MOTTA|Varer som er bokført som mottatt, men som ennå ikke er plassert.|  
|LEVERE|Varer som er plukket for lagerleveringslinjer, men som ennå ikke er bokført som levert.|  
|PUT AWAY|Vanligvis varer som skal lagres i store enheter, men som du ikke vil opprette tilgang til for plukking. I og med at disse hyllene ikke brukes til plukking, verken for produksjonsordrer eller følgesedler, kan bruk av en hylle av typen Plassere være begrenset, men hylletypen kan være nyttig hvis du har kjøpt et stort antall varer. Hyller av denne typen bør alltid ha en lav hylleprioritering, slik at, når mottatte varer plasseres, andre PUTPICK-hyller med høyere prioritering som er fast knyttet til varen, plasseres først. Hvis du bruker denne hylletypen, må du regelmessig etterfylle hyllene slik at varene som er lagret i disse hyllene, også blir tilgjengelige i hyller av typen PUTPICK eller PICK.|  
|PICK|Varer som bare skal brukes til plukk. Etterfylling av disse hyllene kan bare gjøres med flytting, ikke med plassering.|  
|PUTPICK|Varer i hyller som er foreslått både for plasserings- og plukkfunksjoner. Hyller av denne typen har forskjellige hylleprioriteringer. Du kan sette opp masselagringshyllene som denne typen hylle med lave hylleprioriteringer sammenlignet med dine vanlige plukkhyller eller hyller i forhåndsplukkingsområder.|  
|KK|Denne hyllen brukes til lagerjusteringer hvis du angir denne hyllen på lokasjonskortet i feltet **Hyllekode for justering**. Du kan også sette opp hyller av denne typen for defekte varer og varer som blir kontrollert. Du kan flytte varer til denne typen hylle hvis du vil gjøre dem utilgjengelig for den vanlige vareflyten. **Obs!**  I motsetning til alle andre hylletyper er det ikke merket av for noen av varehåndteringsalternativene for **KK**-hylletypen som standard. Dette angir at alt innhold du plasserer i en KK-hylle er utelukket fra vareflyter.|  

For alle hylletyper, unntatt PLUKK, PLASSPLUKK og PLASSERING, tillates ingen annen aktivitet for hyllen enn det som er angitt av hylletypen. En hylle av typen **Motta** kan for eksempel bare brukes til å motta varer til eller plukke varene fra.  

> [!NOTE]  
> Bare flytting kan utføres til hyller av typen MOTTAK og KK. Likeledes er det bare flyttinger som kan gjøres fra hyller av typen LEVERING og KK.  

## <a name="bin-ranking"></a>Hylleprioritering

I avanserte lagerstyring kan du automatisere og optimalisere hvordan varer samles på plassering og plukkforslag ved rangering av hyllene, slik at varene blir foreslått plukket eller plassert i henhold til rangeringskriterier for å brukelagerplassen optimalt.  

Plasseringsprosesser er optimalisert i henhold til hylleprioriteringen ved å foreslå høyt prioriterte hyller før lavt prioriterte hyller. Plukkprosessen er også optimalisert ved først å foreslå varer fra hylleinnhold med høy hylleprioritering. Etterfylling av hyller foreslås også fra lavere til høyere prioriterte hyller.  

Hylleprioriteringen sammen med informasjonen om hylleinnhold er de grunnleggende egenskapene som lar brukere spor varer på lageret.  

## <a name="bin-setup"></a>Hylleoppsett  
I avansert lagerstyring kan hyller konfigureres med kapasitetsverdier, for eksempel antall, det totale kubikkinnholdet og vekt, for å styre hvilke og hvordan varer lagres på hyllen.  

På hvert enkelt varekort kan du tilordne en enhet for varen, for eksempel deler, paller, liter, gram eller bokser. Du kan også ha en lagerenhet for en vare og angi større enheter som er basert på den. Du kan for eksempel angi at pall er lik 16 enheter, der det siste er en lagerenhet.  

Hvis du vil angi et maksimalt antall for en bestemt vare som skal lagres i en enkelthylle, og varen har flere enn én enhet, må du angi det maksimale antallet for hver enhet som finnes på varekortet. Hvis en vare er konfigurert til å håndteres i stykker og paller, må feltet **Maks. ant.** på siden **Hylleinnhold** for denne varen også være i stykker og paller. Hvis ikke, blir ikke det tillatte antallet for hyllen beregnet på riktig måte.  

Før du angir begrensninger for kapasitet for hylleinnhold på en hylle, må du først kontrollere at varens enhet og dimensjoner er angitt på varekortet.  

> [!NOTE]  
> Det er bare mulig å arbeide med flere enheter i LA-installasjoner. I alle andre konfigurasjoner kan hylleinnhold bare være i lagerenheten. Antallet konverteres til grunnenhet for alle transaksjoner med enhet større enn varens grunnenhet.  

## <a name="zone"></a>Sone

I avanserte lagerstyring kan hyller grupperes i soner for å styre hvordan arbeidsflyten er i lageraktiviteter.  

En sone kan være en mottakssone eller en lagringssone, og hver sone kan bestå av én eller flere hyller.  

De fleste egenskapene som er tilordnet en sone tilordnes som standard til hyllen som er opprettet fra denne sonen.  

## <a name="class"></a>Klasse  
I avanserte lagerstyring kan du tilordne lagerklassekoder til varer, hyller og sonene for å styre hvor forskjellige vareklasser blir lagret, for eksempel frosne varer. Du kan dele opp en sone i flere lagerklasser. Varer i mottakssonen kan for eksempel lagres som frosset, farlige eller en annen klasse.  

Når du arbeider med lagerklasser og en standard mottaks-/leveringshylle, må du fylle ut de aktuelle hyllene på lagermottaks- og lagerfølgeseddellinjene manuelt.  

I inngående flyter utheves lagerklassekoden bare på innkommende linjer der vareklassekoden ikke samsvarer med standard mottakshylle. Hvis riktige standardhyller ikke tilordnes, kan ikke antallet mottas.  

## <a name="location"></a>Lokasjon

En lokasjon er en fysisk struktur eller et sted der beholdning mottas, lagres og leveres, potensielt organisert i hyller. En lokasjon kan være et lager, en servicebil, et utstillingslokale, et anlegg eller et område på et anlegg.  

## <a name="first-expired-first-out"></a>FEFO (First Expired First Out)

Hvis du merker av for **Plukk i henhold til FEFO** for hurtigfanen **Hylleprinsipp** på lokasjonskortet, blir varesporede varer plukket i henhold til utløpsdatoen. Varene med de tidligste utløpsdatoene plukkes først.  

Lageraktiviteter i alle plukke- og flyttedokumenter sorteres i henhold til FEFO, med mindre de aktuelle varene allerede har fått tilordnet serie-/partinumre. Hvis bare en del av antallet på linjen allerede er tilordnet vare-/partinumre, brukes FEFO til å sortere det gjenstående antallet som skal plukkes.  

Når det plukkes etter FEFO, samles tilgjengelige varer som utløper først, i en midlertidig varesporingsliste basert på utløpsdato. Hvis to varer har samme utløpsdato, blir varen med lavest parti- eller serienummer valgt først. Hvis parti- eller serienumrene er like, blir varen som ble registrert først, valgt først. Standardkriterier for å velge varer i plukkhyller, for eksempel Hylleprioritering eller Anbrekk, brukes på denne midlertidige FEFO-varesporingslisten.  

## <a name="put-away-template"></a>Plasseringsmal

Plasseringsmalen kan tilordnes til en vare og en lokasjon. Plasseringsmalen angir et sett med prioriterte regler som må følges ved opprettelse av plasseringer. En plasseringsmal kan for eksempel kreve at varen plasseres i en hyllen med hylleinnhold som samsvarer med enheten, og hvis det ikke finnes en lignende hylle med nok kapasitet, må varen plasseres i en tom hylle.  

## <a name="see-also"></a>Se også

[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)   
[Designdetaljer: Tilgjengelighet i lageret](design-details-availability-in-the-warehouse.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]