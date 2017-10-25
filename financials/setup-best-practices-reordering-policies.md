---
title: "Anbefalte fremgangsmåter for oppsett – gjenbestillingsprinsipper | Microsoft-dokumentasjon"
description: "**Gjenbestillingsprinsipp**-feltet på varekortene tilbyr fire forskjellige planleggingsmetoder som bestemmer hvordan individuelle planleggingsparameter samhandler."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0041dcd1e1c7b4eda2d000c8c387bc8b751d4212
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="setup-best-practices-reordering-policies"></a>Anbefalte fremgangsmåter for oppsett: Gjenbestillingsprinsipper
**Gjenbestillingsprinsipp**-feltet på varekortene tilbyr fire forskjellige planleggingsmetoder som bestemmer hvordan individuelle planleggingsparameter samhandler.  

Varens ABC-klassifisering er et det beste grunnlaget for valg av gjenbestillingsprinsipp. Når du bruker ABC-klassifisering for lagerstyring og forsyningsplanlegging, administreres varer i henhold til tre forskjellige klasser avhengig av verdi og volum i forhold til den totale beholdningen. Verdi- og volumdistribusjonen av de tre klassene vises i tabellen nedenfor.

|Klasse|Prosent av totalt lagervolum|Prosent av total lagerverdi|
|-----|-----------------------------|----------------------------|
|A|10–20|50–70|
|B|20|20|
|L|60–70|10–30|

ABC-klassifisering sier at du kan spare både krefter og penger ved å ha mindre streng kontroll på lav verdi-volumvarer enn på høy verdi-volumvarer. Illustrasjonen nedenfor viser hvilket gjenbestillingsprinsipp i [!INCLUDE[d365fin](includes/d365fin_md.md)] som passer best for henholdsvis A-, B- og C-varer.

![ABC-klassifisering](media/abc_classification.png "abc_classification")

Tabellen nedenfor inneholder anbefalte fremgangsmåter for å velge mellom de fire prinsippene.  

|Oppsettsalternativ|Anbefalt fremgangsmåte|Merknad|  
|------------------|-------------------|-------------|  
|**Bestilling**|Bruk dette for A-varer.<br /><br /> Bruk dette for produser-til-ordre-varer.<br /><br /> I produksjon bruker du dette for varer på øverste nivå og dyre komponenter og halvfabrikater.<br /><br /> Bruk dette for varer som er kjøpt som direkte leveringer og spesialbestillinger.<br /><br /> Ikke bruk hvis du ikke godtar automatisk reservering.|Varer, for eksempel skinnsofaer i en møbelbutikk, er varer med høy verdi og lav og uregelmessig ordrehastighet, der beholdningen er uakseptabel, eller der de nødvendige attributtene varierer. Best gjenbestillingsprinsippet er derfor ett som planlegger hver eneste forespørsel individuelt.|  
|**Parti for parti**|Bruk dette for B-varer.<br /><br /> I produksjon bruker du dette for komponenter som forekommer i flere stykklister. Dette sikrer at bestillinger for den samme leverandøren kombineres, slik at det kan fremforhandles bedre priser.<br /><br /> Bruk dette hvis du ikke er sikker på hvilket gjenbestillingsprinsipp du skal velge.|B-varer, for eksempel spisestoler, har en vanlig og relativt høy ordrehastighet, men også høye føringskostnader. Det beste gjenbestillingsprinsippet for B-varer er derfor ett som er økonomisk og bunter sammen behov i gjenbestillingssyklusen.<br /><br /> 80 prosent av varene kan bruke denne policyen.<br /><br /> Kan brukes uten planleggingsparametre.|  
|**Fast gjenbest.ant.**|Bruk dette for C-varer.<br /><br /> Kombiner med parametere for gjenbestillingspunkt.<br /><br /> I produksjon bruker du dette for komponenter på laveste nivå.<br /><br /> Ikke bruk hvis varen ofte er reservert.|C-varer, for eksempel tekopper, er varer med lav verdi med høy og vanlig ordrehastighet. Det beste gjenbestillingsprinsippet for C-varer er derfor ett som garanterer kontinuerlig tilgjengelighet ved alltid å være over et gjenbestillingspunkt.<br /><br /> Hvis brukeren reserverer et antall for et behov i fjern fremtid, forstyrres planleggingsgrunnlaget. Selv om prosjekterte lagernivået er akseptabelt når det gjelder gjenbestillingspunktet, er antallene kanskje ikke tilgjengelige på grunn av reservasjonen.|  
|**Maks.ant.**|Bruk dette for C-varer med høy lagerføringskost eller lagringsbegrensninger.<br /><br /> Kombiner med én eller flere ordremodifikatorer (minimum/maksimum ordreantall eller bestillingsfaktor).|C-varer, for eksempel tekopper, er varer med lav verdi med høy og vanlig ordrehastighet. Det beste gjenbestillingsprinsippet for C-varer er derfor ett som garanterer kontinuerlig tilgjengelighet ved alltid å være over et gjenbestillingspunkt, men under en maksimumsbeholdning.<br /><br /> Hvis du vil endre den foreslåtte ordren, vil du kanskje at ordreantallet skal reduseres til et angitt maksimumsordreantall, økes til et angitt minimumsordreantall eller rundes av oppover for å dekke en angitt bestillingsfaktor. **Obs!** Hvis dette brukes med et gjenbestillingspunkt, holdes beholdningen mellom gjenbestillingspunktet og maksimumsantallet.|  

## <a name="see-also"></a>Se også  
 [Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging](setup-best-practices-supply-planning.md)   
 [Designdetaljer: Gjenbestillingsprinsipper](design-details-reordering-policies.md)   
 [Designdetaljer: Ordre](design-details-order.md)   
 [Designdetaljer: Parti for parti](design-details-lot-for-lot.md)   
 [Designdetaljer: Fast gjenbest.ant.](design-details-fixed-reorder-qty.md)   
 [Designdetaljer: Maks.ant.](design-details-maximum-qty.md)   
 [Konfigurere komplekse moduler ved å bruke anbefalte fremgangsmåter](set-up-complex-application-areas-using-best-practices.md)  
 [Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

