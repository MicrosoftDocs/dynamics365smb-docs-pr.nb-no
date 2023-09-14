---
title: Sette opp markedsføringskampanjer i Business Central| Microsoft-dokumentasjon
description: Beskriver hvordan du kan sette opp og kjøre markedsføringskampanjer i Business Central for å identifisere og trekke til deg prospekter og beholde kunder.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'marketing, campaign, promo, prospect'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Administrere markedsføringskampanjer
Ved å ha en solid markedsføringsplan kan du identifisere, trekke til deg og beholde kunder. En markedsføringsplan består av forskjellige kampanjer og andre samhandlinger i forbindelse med salgs- og markedsføringsaktiviteter. Når du planlegger en kampanje, må du bestemme deg for hvilke kontakter du skal rette deg mot, hvilken type kampanje du vil kjøre (for eksempel salgsmesse eller direktereklame), og hvilke selgere som skal utføre hver oppgave.

Hver kampanje består av forskjellige aktiviteter eller oppgaver. Du kan kombinere flere oppgaver, for eksempel oppgaver som representerer et trinn, i aktiviteter. Aktivitetsoppgaver er knyttet til hverandre ved hjelp av en datoformel. Enkeltoppgaver kan bare tilordnes til selgere. Aktiviteter kan tilordnes til salgsmuligheter, selgere, grupper av selgere og kontakter. Hvis du vil ha mer informasjon, kan du se [Definere salgssykluser for salgsmuligheter og syklusfaser](marketing-how-setup-opportunity-sales-cycles-stages.md).

## Definere enkeltkampanjer
Før du kan opprette en kampanje, må du definere *statuskoder for kampanjen*. Ved hjelp av disse kodene kan du kontrollere kampanjen ved å tilordne en status til den. Når du arbeider deg gjennom fasene i en kampanje, kan du se på hvilket trinn en kampanje befinner seg, og hvilket trinn som følger. Du definererer koder for kampanjestatus på siden **Kampanjestatus**.

Du kan opprette et kampanjekort for hver kampanje du vil følge. Du kan også vise disse kampanjekortene for å vise generell informasjon om kampanjene.
Du kan slette kampanjeposter hvis for eksempel posten registrerer en handling som er kansellert. Du kan bare slette kansellerte kampanjeposter.

### Velge målgruppen
Når du har opprettet en kampanje, kan du begynne å opprette segmenter som angir målgruppen til kampanjen. Hvis du vil ha mer informasjon, kan du se [Håndtere segmenter](marketing-segments.md).

### Registrere rabattprosenter
Når du har definert kampanjen, bestemt hvilke segmenter du vil kampanjen skal dekke, og angitt startdatoen og sluttdatoen, registrerer du rabattprosenten som kunden vil få for de individuelle varene, på linjene på siden **Salgslinjerabatter**. Du kan også registrere salgsprisene for de individuelle varene på linjene på **Salgspriser**-siden. Du kan få tilgang til begge sidene fra kampanjekortet.

 Når du har definert salgsprisene/linjerabattene og segmentene på kampanjekortet, må du aktivere dem slik at kampanjeprisene/-rabattene gjenspeiles på linjene.

> [!NOTE]  
>   For å kunne aktivere salgsprisene/linjerabattene, må du angi om hele segmentet eller bare noen kontakter er mål for kampanjen. Hvis salgsprisene/linjerabattene dekker alle kontaktene i segmentet, merker du av for **Kampanjemål**-feltet på hurtigfanen **Kampanje** på **Segment**-kortet.

Hvis salgsprisene/linjerabattene ikke skal tilbys alle kontaktene i segmentet, kan du fjerne merket for **Kampanjemål**-feltet for de relavante kontaktene. Hvis du ikke ser dette feltet, kan du legge det til i visningen. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).

## Utføre kampanjer
Mens en kampanje kjører, registreres all samhandling med kontaktene eller segmentet, slik at du kan få statistikk og annen informasjon om kostnader og hvor vellykket kampanjen er.

Kampanjer utføres av selgere, og du må opprette aktiviteter for å representere hver oppgave og tilordne dem til de relevante selgerne. Hvis du vil ha mer informasjon, kan du se [Definere salgssykluser for salgsmuligheter og syklusfaser](marketing-how-setup-opportunity-sales-cycles-stages.md).

## Se også
[Administrere kontakter](marketing-contacts.md)  
[Håndtere segmenter](marketing-segments.md)  
[Håndtere salgsmuligheter](marketing-manage-sales-opportunities.md)  
[Arbeid med Business Central](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]