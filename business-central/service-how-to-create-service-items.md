---
title: Opprette servicevarer
description: 'Les om ulike måter du kan opprette servicevarer på i Business Central, for eksempel i en serviceordre eller når du leverer varer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: null
ms.date: 03/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Opprett servicevarer

I [!INCLUDE[prod_short](includes/prod_short.md)] refererer betegnelsen "servicevare" til utstyr eller varer som trenger service. Når du oppretter en serviceordre, kan du angi varene som trenger service. I ordren kan du knytte en servicevare til en vare på lageret eller i en servicevaregruppe.

Når du mottar en vare som trenger service, kan du registrere den som en servicevare. Det er flere måter å gjøre dette på. Du kan for eksempel oppretter en servicevare på siden **Servicevarer** eller som en del av en annen prosess, for eksempel når du arbeider med en serviceordre.

## Slik oppretter du en servicevare

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Servicevarer**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Slik oppretter du servicevarer i en serviceordre

Når du mottar varer for service som du registrere som servicevarer, kan du opprette dem som servicevarer på sidene **Serviceordre** eller **Servicetilbud**.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Serviceordrer**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Velg handlingen **Opprett servicevare**.  

    Et tall blir tilordnet til servicevaren, og et servicevarekort opprettes. Feltet **Servicevarenr.** fylles ut med nummeret på den nye servicevaren.

## Slik oppretter du en servicevare når du leverer varer

Når du leverer varer ved å bokføre ordrer eller salgsfakturaer, registreres de leverte varene automatisk som servicevarer hvis følgende betingelse gjelder: Varene må tilhøre en servicevaregruppe med en avmerking i **Opprett servicevare**-boksen. Hvis varene har serienumre registrert på siden Varesporingslinjer, kopieres denne informasjonen automatisk til **Serienr**-feltet på servicevarekortet når du oppretter servicevarer.  

Følgende fremgangsmåte viser hvordan du oppretter servicevarer når du leverer varer i ordrer.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.  
2. Åpne den aktuelle ordren.  
3. Velg handlingen **Bokfør** eller **Bokfør og skriv ut**.  
4. Velg handlingen **Lever** eller **Lever og fakturer**.  
5. Servicevarene opprettes automatisk for varene i ordren, forutsatt at disse tilhører en servicevaregruppe du har definert for å opprette servicevarer. Hvis du har registrert bestemte serienumre på siden **Varesporingslinjer**, tilordnes de til disse servicevarene.  

> [!NOTE]  
> Hvis en vare er en stykkliste og du har utvidet stykklisten, behandles de utvidede stykklistevarene på samme måte som vanlige varer. Servicevarer opprettes basert på betingelsen for servicevaregrupper og eventuelt betingelsen for serienumre. Hvis det opprettes en servicevare for en utvidet stykklistevare som består av andre stykklistekomponenter, opprettes dessuten disse varene som servicevarekomponenter for den utvidede stykklisteservicevaren.  
>
> Hvis en vare er en stykklistevare og du ikke har utvidet stykklisten, opprettes det en servicevare for den basert på betingelsen for servicevaregruppen og eventuelt betingelsen for serienumre.  

## Slik setter du inn et startgebyr for en servicevare

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Serviceoppgaver**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Arbeidsordre**.
3. Velger servicelinjen, og velg deretter handlingen **Handlinger**, **Funksjoner** og deretter **Sett inn startgebyr**.  

    En servicelinje av typen **Kostnad** settes inn med startgebyret. Startgebyret gjelder for den valgte servicevaren.

## Blokker varer, varevarianter eller bestemte servicevarer

Du kan forhindre at varer, varevarianter eller servicevarer brukes i servicetransaksjoner, for eksempel servicekontrakter, serviceordrer og servicefakturaer. Dette kan være nyttig hvis du vil begrense tilgjengeligheten av enkelte varer eller servicevarer til serviceformål, for eksempel på grunn av avviklet støtte, begrenset lager eller kontraktsmessige avtaler.

Hvis du vil blokkere en vare eller en varevariant fra å bli brukt i servicetransaksjoner, aktiverer du veksleknappen **Tjeneste sperret** på siden **Varekort**, **Varevarianter** og **Varevariantkort**. Du kan også angi dette feltet på **Varemal**-siden, og det vil bli kopiert til varene som er opprettet fra den malen.

Når en vare eller en varevariant er serviceblokkert, er den ikke tilgjengelig for valg på følgende sider:

- Servicelinje (unntatt servicekreditnotaer, der du ser et varsel om at varen eller varianten er sperret, men tillatt for denne dokumenttypen)
- Servicevare
- Servicekontraktlinje
- Standard servicefakturalinje

Hvis du manuelt angir et varenummer eller en variant som er blokkert, får du en feilmelding som sier "Feltet inneholder en verdi som ikke finnes i den relaterte tabellen".

Hvis du i tillegg har servicekontrakter, servicekontrakttilbud eller serviceordrer som inkluderer blokkerte servicevarer eller varevarianter, kan du ikke bruke følgende handlinger:

- **Lås** eller **Lag kontrakt** på siden **Servicekontrakttilbud**.
- **Lås kontrakt**, **Signer kontrakt**, **Opprett kontraktserviceordrer** eller **Opprett kontraktfakturaer** på siden **Servicekontrakt**.
- **Lag ordre** på siden **Servicetilbud**.
- **Frigi til levering** eller **Bokfør** på siden **Serviceordre**.
- **Bokfør** på siden **Servicefaktura**.

### Blokker en servicevare

Hvis du vil blokkere en servicevare fra å bli brukt i servicetransaksjoner, går du til siden **Servicevarekort** og velger ett av følgende alternativer i **Sperret**-feltet:

- **Servicekontrakt**: Blokker servicevaren fra å bli brukt i servicekontrakter og servicekontrakttilbud, men ikke i serviceordrer eller andre servicedokumenter.
- **Alle**: Blokker servicevaren fra å bli brukt i servicetransaksjoner, inkludert servicekontrakter, serviceordrer og andre servicedokumenter.

Når en servicevare er sperret, kan du ikke velge den på følgende sider:

- Servicekontraktlinje (hvis sperret for servicekontrakt eller alle)
- Servicevarelinje (unntatt servicekreditnotaer, hvis sperret for alle)

Hvis du manuelt angir et servicevarenummer for en blokkert servicevare, får du en feilmelding som sier "Feltet inneholder en verdi som ikke finnes i den relaterte tabellen".

Hvis du i tillegg har servicekontrakter, servicekontrakttilbud eller serviceordrer som inkluderer blokkerte servicevarer, kan du ikke bruke følgende handlinger:

- **Lås** og **Lag kontrakt** på siden **Servicekontrakttilbud** (hvis blokkert for servicekontrakt, eller alle).
- **Lås kontrakt**, **Signer kontrakt** eller **Skift kunde** på siden **Servicekontrakt** (hvis blokkert for servicekontrakt, eller alle).
- **Lag ordre** på **Servicetilbud** (hvis blokkert for alle).
- **Frigi til levering** eller **Bokfør** på **Serviceordre** (hvis blokkert for alle). Hvis serviceordredokumenter inneholder flere servicevarer, og noen er sperret og andre ikke, kan du frigi og bokføre ikke-blokkerte linjer. Vurder om du skal aktivere veksleknappen **Én servicevarelinje/ordre** på siden **Serviceoppsett**).
- **Bokfør** på siden **Servicefaktura** (hvis blokkert for alle).

Du kan også vise de blokkerte servicevarene ved å bruke et filter på følgende rapporter:

- Servicevarer (rapport 5935)
- Servicevarer – utgått garanti (rapport 5937)
- Servicefortjeneste (servicevarer) (rapport 5938)

### Dataoppgradering

Denne funksjonen krever ikke ekstra konfigurering. Hvis du imidlertid oppgraderer [!INCLUDE [prod_short](includes/prod_short.md)], må du være oppmerksom på følgende:

- Hvis du har varer, varevarianter eller varemaler der bryteren **Sperret salg** er aktivert, aktiveres også feltet **Tjeneste sperret** for disse postene under oppgraderingen. Dette sikrer at den eksisterende logikken for sperret salg også gjelder for servicetransaksjoner.
- Data oppgraderes bare hvis du har minst én servicevare i firmaet, noe som betyr at du bruker serviceadministrasjonsfunksjonaliteten og trenger dataoppgraderingen. Hvis du ikke har servicevarer, hoppes dataoppgraderingen over, og veksleknappen **Tjeneste sperret** er deaktivert som standard for alle varer, varevarianter og varemaler.

## Se også

[Konfigurer servicevarer og servicevarekomponenter](service-how-setup-service-items.md)  
[Konfigurere servicehåndtering](service-setup-service.md)  
[Servicebehandling](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
