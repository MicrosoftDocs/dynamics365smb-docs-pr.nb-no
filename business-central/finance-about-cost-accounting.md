---
title: Om kostregnskap
description: Kostregnskap kan hjelpe deg med å forstå kostnadene ved å drive et selskap. Informasjon i kostregnskap er utformet for å analysere ulike problemer.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '1101, 1103, 1105, 1108, 1111, 1112, 1124, 1123'
ms.date: 08/23/2022
ms.author: edupont
---
# <a name="about-cost-accounting" />Om kostregnskap

Kostregnskap kan hjelpe deg med å forstå kostnadene ved å drive et selskap. Informasjon i kostregnskap er utformet for å analysere:  

- Typen kostnader som inntreffer når du driver virksomhet  
- Hvor kostnadene oppstår
- Hvem som har ansvaret for kostnadene  

I kostnadsregnskap fordeler du faktiske og budsjetterte kostnader for operasjoner, avdelinger, produkter og prosjekter for å analysere lønnsomhet for firmaet ditt.  

## <a name="workflow-in-cost-accounting" />Arbeidsflyt i kostregnskap

Kostregnskap har følgende hovedkomponenter:  

- Kosttyper, kostsentre og kostobjekter  
- Kostposter og kostkladder  
- Kostfordelinger  
- Kostbudsjetter
- Kostrapportering  

Følgende diagram viser arbeidsflyten i kostregnskap.  

![Oversikt over kostregnskap.](media/costaccountingoverview.png "CostAccountingOverview")  

## <a name="cost-types-cost-centers-and-cost-objects" />Kosttyper, kostsentre og kostobjekter

Du definerer kosttyper, kostsentre og kostobjekter for å analysere hva kostnadene er, hvor kostnadene kommer fra og hvem som skal bære kostnadene.  

Først definerer du et diagram med kosttyper med en struktur og funksjonalitet som ligner på finanskontoplanen. Du kan opprette ditt eget diagram med kosttyper eller gjøre dette ved å overføre resultatregnskapskontoene for finans.  

Kostsentre er avdelinger og lønnsomhetssentre som er ansvarlig for kostnader og inntekter. Ofte er flere kostsentre definert i kostregnskap enn i noen av dimensjonene som er definert i finans. I finans brukes vanligvis bare kostsentre på første nivå for direkte kostnader og innledende kostnader. I kostregnskap opprettes ytterligere kostsentre for ytterligere fordelingsnivåer.  

Kostobjekter er et selskaps produkter, produktgrupper eller tjenester. Dette er de ferdige varene for et selskap som bærer kostnadene.  

Du kan koble kostsentre til avdelinger og kostobjekter til prosjekter i selskapet. Du kan imidlertid koble kostsentre og kostobjekter til dimensjoner gjennom finans og supplere informasjonen med delsummer og titler.  

## <a name="cost-entries-and-cost-journals" />Kostposter og kostkladder

Driftskostnadene kan overføres fra finans. Du kan automatisk overføre kostpostene fra finans til kostposter for hver bokføring. Du kan også bruke en kjørsel til å overføre finanspostene til kostposter basert på daglig eller månedlig sammendragsbokføring.  

I kostkladder kan du bokføre kost og aktiviteter som ikke kommer fra finans eller ikke genereres av fordelinger. Du kan for eksempel bokføre rene driftskostnader, interne gebyrer, fordelinger og korreksjonsposter mellom kosttyper, kostsentre og kostobjekter enkeltvis eller på en gjentaksbasis.  

## <a name="cost-allocations" />Kostfordelinger

Fordelingder flytter kostnader og inntekter mellom kosttyper, kostsentre og kostobjekter. Indirekte kostnader blir først bokført til kostsentre og senere belastet kostobjekter. Dette kan for eksempel gjøres i salgsavdelingen som selger flere produkter samtidig. Avdelingens administrasjonskostnader, for eksempel lønn, forsyninger og reiseutgifter, tilordnes først til kostsenteret, som deretter fordeles mellom de ulike produktene (kostobjekter) som er solgt, sammen med materialet som ble kjøpt (direkte kostnad) for bruk i dem.

Fordelingsbasen som brukes, og nøyaktigheten av fordelingsdefinisjonen har en innflytelse på resultatene for kostnadsfordelinger. Fordelingsdefinisjonen brukes til å fordele kostnader først fra såkalte pre-kostsentre til hovedkostsentre og deretter fra kostsentre til kostobjekter.  

Hver fordeling består av en fordelingskilde og ett eller flere fordelingsmål. Du kan fordele faktiske verdier eller budsjetterte verdier ved å bruke metoden for statisk fordeling som er basert på en definitiv verdi, for eksempel kvadratmeterantall, eller et fastsatt fordelingsforhold på 5:2:4. Du kan også fordele faktiske verdier eller budsjetterte verdier ved å bruke metoden for dynamisk fordeling med ni forhåndsdefinerte fordelingsgrunnlag og tolv dynamiske datointervaller.  

## <a name="cost-budgets" />Kostbudsjetter

På lignende måte som på budsjettering i finans kan du opprette budsjetter for å planlegge kostnader i en bestemt periode (for eksempel et regnskapsår), som kan brukes på et kostsenter (selskapets avdeling), eller på et kostobjekt (produkt eller en service). Du kan opprette så mange kostbudsjetter som du vil. Du kan deretter kopiere kostbudsjettet til finansbudsjettet, og omvendt. Og du kan overføre budsjetterte kostnader som faktiske kostnader.

## <a name="cost-reporting" />Kostrapportering

De fleste rapporter og statistikker er basert på bokførte kostposter. Du kan angi sorteringen av resultatene og bruke filtre for å definere hvilke data som skal vises. Du kan opprette rapporter for analyse av kostdistribusjon. I tillegg kan du bruke standard finansrapporter til å definere hvordan rapportene for diagrammet med kosttyper skal vises.  

## <a name="see-related-microsoft-trainingtrainingpathsuse-cost-accounting-dynamics--business-central" />Se relatert [Microsoft-opplæring](/training/paths/use-cost-accounting-dynamics-365-business-central/)

## <a name="see-also" />Se også

[Gjøre rede for kostnader](finance-manage-cost-accounting.md)  
[Finans](finance.md)  
[Terminologi i kostregnskap](finance-terminology-in-cost-accounting.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
