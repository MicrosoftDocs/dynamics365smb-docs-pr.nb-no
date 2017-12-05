---
title: "Designdetaljer – Interne lagerflyter | Microsoft-dokumentasjon"
description: "Flyten av varer mellom hyller på en selskapslokasjon dreier seg i hovedsak om å plukke komponenter og plassere sluttvarer for montering eller produksjonsordrer og adhocflyttinger, for eksempel etterfylling av hyller, uten en relasjon til kildedokumenter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 957c8889d943ed412af7555271897b52c0759969
ms.contentlocale: nb-no
ms.lasthandoff: 11/10/2017

---
# <a name="design-details-internal-warehouse-flows"></a>Designdetaljer: Interne lagerflyter
Flyten av varer mellom hyller på en selskapslokasjon dreier seg i hovedsak om å plukke komponenter og plassere sluttvarer for montering eller produksjonsordrer og adhocflyttinger, for eksempel etterfylling av hyller, uten en relasjon til kildedokumenter. Omfanget av og karakteren til aktivitetene som er involvert, varierer mellom grunnleggende og avanserte lagerstyring.  

 Enkelte interne flyter overlapper inngående eller utgående flyter. Noe av denne overlappingen vises som trinn 4 og 5 i de grafiske diagrammene for henholdsvis avanserte inngående og utgående flyter. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Inngående lagerflyt](design-details-outbound-warehouse-flow.md).  

## <a name="internal-flows-in-basic-warehousing"></a>Interne flyter i Grunnleggende lagerstyring  
 I grunnleggende lageroppsett vil flyten av varer mellom hyller i selskapet være sentrert rundt plukk av komponenter og plassering av sluttvarer for produksjons- og monteringsordrer og adhocflyttinger, for eksempel etterfylling av hyller, uten relasjon til kildedokumenter.  

### <a name="flows-to-and-from-production"></a>Flyter til og fra produksjon  
 Hovedintegrasjonen mellom produksjonsordrer og grunnleggende lageraktiviteter representeres av muligheten til å plukke produksjonskomponenter i vinduet **Lagerplukk** eller **Lagerflytting**.  

> [!NOTE]  
>  I vinduet **Lagerplukk** bokføres komponentforbruket sammen med plukkbokføringen. Ved hjelp av vinduet **Lagerflytting**, blir bare hyllejusteringer registrert, og det utføres ingen finansbokføringer for varen.  

 I tillegg til komponenthåndtering representeres integreringen av muligheten til å plassere produserte varer med vinduet **Lagerplassering**.  

 Feltene **Til-Hyllekode for produksjon**, **Fra-Hyllekode for produksjon** og **Åpen prod.hyllekode** på lokasjonskortet eller kortene for produksjonsressurs/arbeidssenter definerer standardflyter til og fra produksjonsområder.  

 Hvis du vil ha mer informasjon om hvordan komponentforbruk er trekkes fra hyller til produksjon eller åpne produksjonshyller, kan du se avsnittet Trekke produksjonskomponenter i lageret i dette emnet.  

### <a name="flows-to-and-from-assembly"></a>Flyter til og fra montering  
 Hovedintegrasjonen mellom monteringsordrer og grunnleggende lageraktiviteter representeres av muligheten til å flytte en monteringskomponent til monteringsområdet.  

 Det finnes ingen bestemt lagerfunksjonalitet for å plassere monteringsvarer, men du kan angi en standard plasseringshylle for hyllekoden i monteringsordrehodet. Bokføring av monteringsordre Funksjoner da som bokføring av en plassering. Lageraktiviteten som flytter monteringsvarer til lageret, kan håndteres i vinduet **Intern flytting** uten noen relasjon til monteringsordren.  

 Følgende monteringsflyter finnes.  

|Flyt|Beskrivelse|  
|----------|---------------------------------------|  
|Monter til lager|Komponentene trengs i en monteringsordre der avgangen lagres på lageret.<br /><br /> Denne lagerflyten håndteres i vinduet **Lagerflytting**. Én hentelinje angir hvor komponentene skal hentes fra. Én plasseringslinje angir hvor komponentene skal plasseres.|  
|Monter til ordre|Komponentene trengs i en monteringsordre som er knyttet til en ordre som leveres når den solgte varen er montert.|  

> [!NOTE]  
>  Hvis varer monteres til ordre, vil lagerplukk for den tilknyttede ordren deretter utløse en lagerflytting for alle involverte monteringskomponenter, ikke bare for den solgte varen som når du leverer varer på lager.  

 Feltene **Til-Hyllekode for montering**, **Fra-Hyllekode for montering** og **Hyllek. lev. fra m. til ordre** på lokasjonskortet definerer standardflyter til og fra monteringsområder.  

> [!NOTE]  
>  Feltet **Hyllek. lev. fra m. til ordre** fungerer som fra-hylle for montering i monter-til-ordre-scenarier.  

### <a name="ad-hoc-movements"></a>Adhocflyttinger  
 I grunnleggende lagerstyring blir flytting av varer fra hylle til hylle uten relasjon til kildedokumenter, utført i vinduet **Intern flytting**, som fungerer sammen med vinduet **Lagerflytting**.  

 En metode for flytting av varer ad hoc mellom hyller, er å bokføre positive poster i feltet **Ny hyllekode** i vinduet **Vareoverf.kladd**.  

## <a name="internal-flows-in-advanced-warehousing"></a>Interne flyter i Avansert lagerstyring  
 I avanserte lageroppsett er flyten av varer mellom hyller i selskapet sentrert rundt plukk av komponenter og plassering av sluttvarer for produksjonsordrer og plukk av komponenter for monteringsordrer. I tillegg oppstår interne flyter som ad hoc-flyttinger, for eksempel etterfylling av hyller, uten relasjon til kildedokumenter.  

### <a name="flows-to-and-from-production"></a>Flyter til og fra produksjon  
 Hovedintegrasjonen mellom produksjonsordrer og avanserte lageraktiviteter representeres av muligheten til å plukke produksjonskomponenter i **Plukk**-vinduet og **Plukkforslag**-vinduet og muligheten til å plassere produserte varer i **Intern plassering**-vinduet.  

 Et annet integreringspunkt i produksjonen finnes i vinduet **Lagerflytting** og i vinduet Flytteforslag, der du kan plassere komponenter og ta produserte varer for frigitte produksjonsordrer.  

 Feltene **Til-Hyllekode for produksjon**, **Fra-Hyllekode for produksjon** og **Åpen prod.hyllekode** på lokasjonskortet eller kortene for produksjonsressurs/arbeidssenter definerer standardflyter til og fra produksjonsområder.  

 Hvis du vil ha mer informasjon om hvordan komponentforbruk er trekkes fra hyller til produksjon eller åpne produksjonshyller, kan du se avsnittet Trekke produksjonskomponenter i lageret i dette emnet.  

### <a name="flows-to-and-from-assembly"></a>Flyter til og fra montering  
 Hovedintegrasjonen mellom monteringsordrer og avanserte lageraktiviteter representeres av muligheten til å plukke monteringskomponenter i både **Plukk**-vinduet og **Plukkforslag**-vinduet. Denne funksjonaliteten fungerer nøyaktig slik som plukking av komponenter for produksjonsordrer.  

 Det finnes ingen bestemt lagerfunksjonalitet for å plassere monteringsvarer, men du kan angi en standard plasseringshylle for hyllekoden i monteringsordrehodet. Bokføring av monteringsordre Funksjoner da som bokføring av en plassering. Lageraktiviteten som flytter monteringsvarer til lageret, kan håndteres i vinduet **Flytteforslag** eller vinduet **Intern plassering** uten noen relasjon til monteringsordren.  

> [!NOTE]  
>  Hvis varer monteres til ordre, vil lagerlevering for den tilknyttede ordren deretter utløse lagerplukk for alle involverte monteringskomponenter, ikke bare for den solgte varen som når du leverer varer på lager.  

 Feltene **Til-Hyllekode for montering** og **Fra-Hyllekode for montering** på lokasjonskortet definerer standardflyter til og fra monteringsområder.  

### <a name="ad-hoc-movements"></a>Adhocflyttinger  
 I avansert lagerstyring blir flytting av varer fra hylle til hylle uten relasjon til kildedokumenter, behandlet i vinduet **Flytteforslag** og registrert i vinduet Lagerflytting.  

## <a name="flushing-production-components-in-the-warehouse"></a>Trekke produksjonskomponenter i lageret  
 Hvis det er angitt på varekortet, vil komponenter som er plukket med lagerplukk, bli bokført som forbrukte av produksjonsordren når lagerplukket registreres. Ved hjelp av trekkmetodene **Plukk + Fremover** og **Plukk + Bakover**, utløser plukkregistreringen den relaterte forbruksbokføringen henholdsvis når den første operasjonen starter, eller når den siste operasjonen er fullført.  

 Tenk deg følgende scenario basert på [!INCLUDE[d365fin](includes/d365fin_md.md)]-demonstrasjonsdatabasen, HVIT lokasjon.  

 Det finnes en produksjonsordre for 15 STK av varen LS-100. Noen av varene i komponentoversikten må trekkes manuelt i en forbrukskladd, og andre varer i oversikten kan plukkes og trekkes automatisk ved hjelp av trekkmetoden **Plukk + Bakover**.  

> [!NOTE]  
>  **Plukk + fremover** fungerer bare hvis den andre operasjonen for produksjonsrutelinjen bruker en rutekoblingskode. Hvis en planlagt produksjonsordre frigis, starter lagertrekk fremover for komponenter som **Plukk + Fremover** er angitt for. Trekking kan imidlertid ikke finne sted før plukk av komponentene er registrert, noe som igjen bare kan finne sted når ordren frigis.  

 Fremgangsmåten nedenfor beskriver hva ulike brukere gjør, og det relaterte svaret:  

1.  Verkstedlederen frigir produksjonsordren. Varer med trekkmetoden **Fremover** og ingen rutekoblingskode, trekkes fra den åpne produksjonshylle.  
2.  Verkstedlederen velger knappen **Opprett lagerplukk** på produksjonsordren. Et lagerplukkdokumentet opprettet plukking for varer med trekkmetodene **Manuell**, **Plukk + Bakover** og **Plukk + Fremover**. Disse varene plasseres i hyllen til produksjon.  
3.  Lagerlederen tilordner plukkingene til en lagermedarbeider.  
4.  Lagermedarbeideren plukker varene fra aktuelle hyller og plasserer dem i hyllen til produksjon eller i hyllen som er angitt i plukkingen, som kan være en arbeidssenterhylle eller produksjonsressurshylle.  
5.  Lagermedarbeideren registrerer plukkingen. Antallet trekkes fra plukkhyllene og legges til forbrukshyllen. **Plukket ant.**-feltet oppdateres i komponentoversikten for alle plukkede varer.  

    > [!NOTE]  
    >  Bare antallet som plukkes kan brukes.  

6.  Maskinoperatøren gir produksjonssjefen beskjed om at sluttvarene er ferdige.  
7.  Verkstedlederen bruker forbrukskladden eller produksjonskladden til å bokføre forbruk av komponentvarer som bruker enten trekkmetoden **Manuell** eller trekkmetoden **Fremover** eller **Plukk + Fremover** sammen med rutekoblingskoder.  
8.  Produksjonssjefen bokfører avgangen til produksjonsordren og endrer statusen til **Ferdig**. Antallet komponentvarer som bruker trekkmetoden **Bakover**, trekkes fra den åpne produksjonshyllen, og antallet komponentvarer som bruker trekkmetoden **Plukk + Bakover**, trekkes fra hyllen til produksjon.  

 Illustrasjonen nedenfor viser når **Hyllekode**-feltet i komponentoversikten fylles i henhold til lokasjonsoppsettet eller oppsettet for produksjonsressurs/arbeidssenter.  

 ![Flytskjema for hylle](media/binflow.png "BinFlow")  

## <a name="see-also"></a>Se også  
 [Designdetaljer: Lagerstyring](design-details-warehouse-management.md)

