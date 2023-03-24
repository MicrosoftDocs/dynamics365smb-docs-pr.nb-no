---
title: Anbefalte fremgangsmåter for oppsett – Planleggingsparametere
description: Dette emnet beskriver de beste fremgangsmåtene for å definere valgte planleggingsparameterfelter med hurtigfanen Planlegging på varekortet.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: edupont
---
# Anbefalte fremgangsmåter for oppsett: Planleggingsparametere

Hurtigfanen **Planlegging** på varekortet er kjernen i et selskaps forsyningskjede. Det er svært viktig for kostnadseffektiv lagerkontroll og god kundeservice å angi riktige planleggingsparametre.  

 Tabellen nedenfor inneholder anbefalte fremgangsmåter for hvordan du konfigurerer valgte planleggingsparameterfelt. Hvis du vil ha mer informasjon om et felt, velger du koblingen i kolonnen **Oppsettfelt**.  

|Oppsettfelt|Anbefalt fremgangsmåte|Merknad|  
|-----------------|-------------------|-------------|  
|Gjenbestillingsprinsipp||Hvis du vil ha mer informasjon, kan du se [Anbefalte fremgangsmåter for oppsett: Gjenbestillingsprinsipper](setup-best-practices-reordering-policies.md).|  
|Reserver|Velg **Aldri** når varen planlegges ved hjelp av et gjenbestillingspunkt.<br /><br /> Velg **Aldri** i produksjon, slik at planleggingssystemet kan dekke alle behov.<br /><br /> Velg **Valgfritt** for varene det kan hende du vil reservere for kunder med topp prioritet.<br /><br /> Velg **Alltid** for unike varer (varer av typen ikke-standard), for eksempel varer av typen diverse som er inngående for bestemte behov.|Reservasjoner motvirker vanligvis formålet med planlegging, som er å få behov og forsyning i balanse. Varer som er definert for planlegging skal derfor vanligvis ikke reserveres.<br /><br /> Hvis brukeren reserverer et lagerantall for fremtidig behov, forstyrres planleggingsgrunnlaget, og det kan hende at gjenbestillingspunktet ikke virker som det skal. Selv om prosjekterte lagernivået er akseptabelt når det gjelder gjenbestillingspunktet, er antallene kanskje ikke tilgjengelige på grunn av reservasjonen.|  
|Avdempingsperiode|Angi i forhold til leverandørens fleksibilitet.<br /><br /> Ved hjelp av en kortere periode kan du redusere arbeidskapitalen ved å unngå mye lager, men det kan også forårsake at flere handlinger må planlegges på nytt.|Hvis leverandøren godtar endringer i siste øyeblikk i ordrer, bruker du en kortere periode, men vær forberedt på flere handlinger med ny planlegging. Hvis leverandøren krever fast planlegging, forlenger du perioden så mye som mulig.<br /><br /> Hvis du vil ha informasjon om **Avdempingsperiode**-feltet, kan du se [Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md).|  
|Ta med lagerbeholdning|Velg alltid dette når du bruker gjenbestillingsprinsippet Parti for parti.|Ingen valg bare i spesielle situasjoner, for eksempel når varer på lager er ikke er salgbare.|  
|Sikkerhetsleveringstid|Velg mellom 1D og 6D.<br /><br /> Angi en sikkerhetsleveringstid på minst én dag for å kontrollere at forsyninger er tilgjengelige dagen før de trengs.<br /><br /> Hvis du bruker en ny leverandør, definerer du en lengre tid til du blir kjent med leveringsprestasjonen deres.<br /><br /> I produksjon definerer du lengre sikkerhetsleveringstider for kritiske komponenter.|Forsyning som planlegges av systemet for å unngå tomt lager, ankommer på samme dag som lageret blir tomt. Dette kan være flere timer for sent hvis behovet for eksempel er nødvendig om morgenen, og forsyningen ankommer om ettermiddagen. **Obs!** Feltet **Sikkerhetsleveringstid** bruker hovedkalenderen. 14D er derfor ikke nødvendigvis to uker.|  
|Sikkerhetslagerantall|Bruk dette for varer med store svingninger i etterspørsel.<br /><br /> I produksjon bruker du dette for kritiske komponenter.<br /><br /> Bruk dette for varer som er underlagt serviceavtaler.|Hvis feltet **Gjenbestillingspunkt** er ikke fylt ut, fungerer sikkerhetslagerantallet også som et gjenbestillingspunkt.|  
|Akkumuleringsperiode for parti|Hvis du ønsker bare noen få store bestillinger og godtar å ha varene på lager, angir du en lang akkumuleringsperiode for parti.<br /><br /> Hvis du ønsker flere små bestillinger og minimal beholdning, angir du en kort akkumuleringsperiode for parti.|Akkumuleringsperioden for parti er vanligvis den lengste perioden som du vil ha varen på lager.|  
|Gjenbestillingspunkt|Baser gjenbestillingspunktet på varens behovsprofil.|Hvis historiske data viser at gjennomsnittsbehovet for varen er 100 enheter i løpet av en leveringstid på sju dager, må du angi minst 100 for gjenbestillingspunktet.<br /><br /> Dette betyr at når lagernivået faller til under 100 enheter, vil planleggingssystemet foreslå å etterfylle fordi forsyningen av varen tar sju dager, og det må være nok til å dekke etterspørselen innenfor disse sju dager.|  
|Tidsperiode|La stå tomt, noe som betyr at lagernivået er kontrolleres hver dag.|Kontroll av lagernivået hver dag sikrer optimal planlegging av gjenbestillingspunkt. **Obs!** En tidsperiode på 1U betyr at lagernivået kan være under gjenbestillingspunktet i én uke før en forsyningsordre blir foreslått.|  
|Avrundingspresisjon|Angi 0,00001 i dyr produksjon.|Store avrundingsantall for vrak eller materialforbruk kan beløpe seg til svært store lagerkostnader. Det kan derfor være relevant å angi den minste avrundingspresisjonen for å minimere denne potensielle kostnaden.|  

> [!NOTE]  
> Gode fremgangsmåter for planleggingsparameter på varekort gjelder også for de samme feltene på LFE-kort.  
>
> Hvis selskaper planlegger for behov på ulike lokasjoner, anbefales det sterkt at de definerer lagerføringsenheter for hver lokasjon, og at alt behov opprettes ved hjelp av en verdi i **Lokasjonskode**-feltet. Finn ut mer under [Utformingsdetaljer: Planlegg med eller uten lokasjoner](production-planning-with-without-locations.md).  

## Se også  
[Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging](setup-best-practices-supply-planning.md)  
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)  
[Konfigurere komplekse moduler ved å bruke anbefalte fremgangsmåter](set-up-complex-application-areas-using-best-practices.md)  
[Utformingsdetaljer: Planlegg med eller uten lokasjoner](production-planning-with-without-locations.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
