---
title: Om kostregnskap
description: Kostregnskap kan hjelpe deg med å forstå kostnadene ved å drive et selskap. Informasjon i kostregnskap er utformet for å analysere ulike problemer.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '1101, 1103, 1105, 1108, 1111, 1112, 1124, 1123'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Om kostregnskap

Kostregnskap kan hjelpe deg med å forstå kostnadene ved å drive et selskap. Informasjon i kostregnskap er utformet for å analysere:  

- Hvile kostnadstyper som inntreffer for bedriften din.  
- Hvor kostnadene oppstår.
- Hvem som har ansvaret for kostnadene.

I kostnadsregnskap fordeler du faktiske og budsjetterte kostnader for operasjoner, avdelinger, produkter og prosjekter for å analysere lønnsomhet for firmaet ditt.  

## Arbeidsflyt i kostregnskap

Kostregnskap har følgende hovedkomponenter:  

- Kosttyper, kostsentre og kostobjekter  
- Kostposter og kostkladder  
- Kostfordelinger  
- Kostbudsjetter
- Kostrapportering  

Følgende diagram viser arbeidsflyten i kostregnskap.  

![Oversikt over kostregnskap.](media/costaccountingoverview.png "CostAccountingOverview")  

## Kosttyper, kostsentre og kostobjekter

Du definerer kosttyper, kostsentre og kostobjekter for å analysere hva kostnadene er, hvor kostnadene kommer fra og hvem som skal bære kostnadene.  

Først definerer du et diagram med kosttyper med en struktur og funksjonalitet som ligner på finanskontoplanen. Du kan opprette ditt eget diagram med kosttyper eller gjøre dette ved å overføre resultatregnskapskontoene for finans.  

Kostsentre er avdelinger og lønnsomhetssentre som er ansvarlig for kostnader og inntekter. Ofte er flere kostsentre definert i kostregnskap enn i noen av dimensjonene som er definert i finans. I finans brukes vanligvis bare kostsentre på første nivå for direkte kostnader og innledende kostnader. I kostregnskap opprettes flere kostsentre for ekstra fordelingsnivåer.  

Kostobjekter er et selskaps produkter, produktgrupper eller tjenester. Disse objektene er de ferdige varene som bærer kostnadene.  

Du kan koble kostsentre til avdelinger og kostobjekter til prosjekter i selskapet. Du kan imidlertid koble kostsentre og kostobjekter til dimensjoner gjennom finans og supplere informasjonen med delsummer og titler.  

## Kostposter og kostkladder

Driftskostnadene kan overføres fra finans. Du kan automatisk overføre kostpostene fra finans til kostposter for hver bokføring. Du kan også bruke en kjørsel til å overføre finanspostene til kostposter basert på daglig eller månedlig sammendragsbokføring.  

I kostkladder kan du bokføre kost og aktiviteter som ikke kommer fra finans eller ikke genereres av fordelinger. Du kan for eksempel bokføre rene driftskostnader, interne gebyrer, fordelinger og korreksjonsposter mellom kosttyper, kostsentre og kostobjekter enkeltvis eller på en gjentaksbasis.  

## Kostfordelinger

Fordelingder flytter kostnader og inntekter mellom kosttyper, kostsentre og kostobjekter. Indirekte kostnader blir først bokført til kostsentre og senere belastet kostobjekter. Dette kan for eksempel gjøres i salgsavdelingen som selger flere produkter samtidig. Avdelingens indirekte kostnader, for eksempel lønn, forsyninger og reiseutgifter, tilordnes i utgangspunktet til salgskostsenteret. Kostnadene fordeles deretter mellom de ulike produktene (kostobjekter) som selges, sammen med materialene som kjøpes inn (direkte kost).

Fordelingsbasen og nøyaktigheten av fordelingsdefinisjonen har en innflytelse på resultatene for kostnadsfordelinger. Fordelingsdefinisjonen fordeler kostnader først fra såkalte pre-kostsentre til hovedkostsentre og deretter fra kostsentre til kostobjekter.  

Hver fordeling består av en fordelingskilde og ett eller flere fordelingsmål. Du kan fordele faktiske verdier eller budsjetterte verdier ved å bruke statisk fordeling basert på en bestemt verdi. Det kan for eksempel være kvadratmeter eller et fastsatt fordelingsforhold på 5:2:4. Du kan også fordele faktiske verdier eller budsjetterte verdier ved å bruke metoden for dynamisk fordeling med ni forhåndsdefinerte fordelingsgrunnlag og tolv dynamiske datointervaller.  

## Kostbudsjetter

På lignende måte som på budsjettering i finans kan du opprette budsjetter for å planlegge kostnader i en bestemt periode (for eksempel et regnskapsår), som kan brukes på et kostsenter (selskapets avdeling), eller på et kostobjekt (produkt eller en service). Du kan opprette så mange kostbudsjetter som du vil. Du kan deretter kopiere kostbudsjettet til finansbudsjettet, og omvendt. Og du kan overføre budsjetterte kostnader som faktiske kostnader.

## Kostrapportering

De fleste rapporter og statistikker er basert på bokførte kostposter. Du kan angi sorteringen av resultatene og bruke filtre for å definere hvilke data som skal vises. Du kan opprette rapporter for analyse av kostdistribusjon. I tillegg kan du bruke standard finansrapporter til å definere hvordan rapportene for diagrammet med kosttyper skal vises.  

## Se også

[Gjør rede for kostnader](finance-manage-cost-accounting.md)  
[Finans](finance.md)  
[Terminologi i kostnadsregnskap](finance-terminology-in-cost-accounting.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
