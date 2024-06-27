---
title: Anbefalte fremgangsmåter for oppsett – gjenbestillingsprinsipper | Microsoft Docs
description: Gjenbestillingsprinsipp-feltet på varekortene tilbyr fire forskjellige planleggingsmetoder som bestemmer hvordan individuelle planleggingsparameter samhandler.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# Anbefalte fremgangsmåter for oppsett: Gjenbestillingsprinsipper

**Gjenbestillingsprinsipp**-feltet på varekortene inneholder planleggingsmetoder som bestemmer hvordan individuelle planleggingsparameter samhandler.  

Varens ABC-klassifisering er et det beste grunnlaget for valg av gjenbestillingsprinsipp. Når du bruker ABC-klassifisering, håndterer du varer i henhold til tre klasser. Hvilken klasse du bruker, avhenger av varens verdi og volum i forhold til den totale beholdningen. Verdi- og volumdistribusjonen av de tre klassene vises i tabellen nedenfor.

|Klasse|Prosent av totalt lagervolum|Prosent av total lagerverdi|
|-----|-----------------------------|----------------------------|
|A|10–20|50–70|
|B|20|20|
|L|60–70|10–30|

ABC-klassifisering sier at du kan spare både krefter og penger ved å ha mindre streng kontroll på lav verdi-volumvarer enn på høy verdi-volumvarer. Illustrasjonen nedenfor viser hvilket gjenbestillingsprinsipp i [!INCLUDE[prod_short](includes/prod_short.md)] som passer best for henholdsvis A-, B- og C-varer.

![ABC-klassifisering.](media/abc_classification.png "abc_classification")

Tabellen nedenfor inneholder anbefalte fremgangsmåter for å velge mellom de fire prinsippene.  

|Oppsettsalternativ|Anbefalt fremgangsmåte|Merknad|  
|------------------|-------------------|-------------|  
|**Bestilling**|Bruk dette for A-varer.<br /><br /> Bruk dette for produser-til-ordre-varer.<br /><br /> I produksjon bruker du dette for varer på øverste nivå og dyre komponenter og halvfabrikater.<br /><br /> Bruk dette for varer som er kjøpt som direkte leveringer og spesialbestillinger.<br /><br /> Ikke bruk dette hvis du ikke godtar automatisk reservering.|Varer, for eksempel skinnsofaer i en møbelbutikk, er varer med høy verdi og lav og uregelmessig ordrehastighet, der beholdningen er uakseptabel, eller der de nødvendige attributtene varierer. Best gjenbestillingsprinsippet er derfor ett som planlegger hver eneste forespørsel individuelt.|  
|**Parti for parti**|Bruk dette for B-varer.<br /><br /> I produksjon bruker du dette for komponenter som forekommer i flere stykklister. Denne policyen sikrer at bestillinger for den samme leverandøren kombineres, slik at det kan fremforhandles bedre priser.<br /><br /> Bruk dette hvis du ikke er sikker på hvilket gjenbestillingsprinsipp du skal velge.|B-varer, for eksempel spisestoler, har en vanlig og relativt høy ordrehastighet, men også høye føringskostnader. Det beste gjenbestillingsprinsippet for B-varer er derfor ett som er økonomisk og bunter sammen behov i gjenbestillingssyklusen.<br /><br /> 80 prosent av varene kan bruke denne policyen.<br /><br /> Kan brukes uten planleggingsparametre.|  
|**Fast gjenbest.ant.**|Bruk dette for C-varer.<br /><br /> Kombiner med parametere for gjenbestillingspunkt.<br /><br /> I produksjon bruker du dette for komponenter på laveste nivå.<br /><br /> Ikke bruk dette hvis varen ofte er reservert.|C-varer, for eksempel tekopper, er varer med lav verdi med høy og vanlig ordrehastighet. Det beste gjenbestillingsprinsippet for C-varer er derfor ett som garanterer kontinuerlig tilgjengelighet ved alltid å være over et gjenbestillingspunkt.<br /><br /> Hvis brukeren reserverer et antall for et behov i fjern fremtid, forstyrres planleggingsgrunnlaget. Selv om prosjekterte lagernivået er akseptabelt når det gjelder gjenbestillingspunktet, er antallene kanskje ikke tilgjengelige på grunn av reservasjonen.|  
|**Maks.ant. **|Bruk dette for C-varer med høy lagerføringskost eller lagringsbegrensninger.<br /><br /> Kombiner med én eller flere ordremodifikatorer (minimum/maksimum ordreantall eller bestillingsfaktor).|C-varer, for eksempel tekopper, er varer med lav verdi med høy og vanlig ordrehastighet. Det beste gjenbestillingsprinsippet for C-varer er derfor ett som garanterer kontinuerlig tilgjengelighet ved alltid å være over et gjenbestillingspunkt, men under en maksimumsbeholdning.<br /><br /> Hvis du vil endre den foreslåtte ordren, vil du kanskje at ordreantallet skal reduseres til et angitt maksimumsordreantall, økes til et angitt minimumsordreantall eller rundes av oppover for å dekke en angitt bestillingsfaktor. **Obs!** Hvis dette brukes med et gjenbestillingspunkt, holdes beholdningen mellom gjenbestillingspunktet og maksimumsantallet.|  

## Se også

 [Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging](setup-best-practices-supply-planning.md)  
 [Utformingsdetaljer: Håndter gjenbestillingsprinsipper](design-details-handling-reordering-policies.md)  
 [Konfigurere komplekse moduler ved å bruke anbefalte fremgangsmåter](set-up-complex-application-areas-using-best-practices.md)  
 [Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
