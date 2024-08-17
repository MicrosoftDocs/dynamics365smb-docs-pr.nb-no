---
title: Forstå kontoplanen
description: 'Beskriver kontoplanen, hvordan du definerer den og hvordan du bruker den.'
author: kennienp
ms.topic: conceptual
ms.search.keywords: 'analysis, history, track'
ms.search.form: '18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158'
ms.date: 08/06/2024
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
---

# Forstå kontoplanen

En kontoplan fungerer som en omfattende katalog over finanskontoer og tilhørende referansenumre. En kontoplan består vanligvis av to hovedkontokategorier:

- Balansekontoer: Disse kontoene sporer selskapets objekter, gjeld og nettoverdi.
- Resultatregnskapskontoer: Disse kontoene registrerer inntekter fra ulike kilder og sporer også utgifter.

Balansekontoer er videre kategorisert i tre grupper:

1. Objektkontoer: Disse kontoene sporer alle verdifulle ressurser som eies av selskapet ditt.
1. Ansvarskontoer: De registrerer selskapets gjeld.
1. Egenkapitalkontoer: Representere restverdien i virksomheten etter fradrag av gjeld fra eiendeler.

Inntektskontoer er delt inn i to grupper:

1. Inntektskontoer: Disse kontoene registrerer selskapets inntekter fra forskjellige kilder.
1. Utgiftskontoer: Disse kontoene registrerer alle selskapets utgifter.

Bruk kontoplanen til å registrere transaksjoner i organisasjonens finans. Hver konto har vanligvis en identifikator (kontonummer) og en beskrivende tittel eller overskrift, og de er systematisk kodet basert på kontotypen.

[!INCLUDE[prod_short](includes/prod_short.md)] inneholder en standard kontoplan som er klar til å støtte forretningsvirksomheten din.

Sammensetningen av selskapets kontoplan er en strategisk beslutning som tas av ledelsen (eller av landsspesifikk regulering). Det varierer basert på selskapets bransje, forretningsmodell og økonomiske struktur. Avhengig av bransjen kan du for eksempel ha spesifikke objektkontoer som er tilpasset selskapets unike drift og behov:

* En detaljhandelsvirksomhet kan legge vekt på lager og kundefordringer.
* Et teknologiselskap kan fokusere på immaterielle objekter som patenter og programvare.
* Et produksjonsanlegg sporer aktiva og forsyninger.

## Siden Kontoplan

Kontoplanen viser alle finanskontoer. Fra kontoplanen kan du gjøre ting som:  

* Vise rapporter som viser finansposter og saldoer.  
* Lukke resultatregnskapet.  
* Åpne finanskontokortet for å legge til eller endre innstillinger.  
* Vise en liste over bokføringsgrupper for kontoen.
* Vise separate debet- og kreditsaldoer for én konto.

Du kan legge til, endre eller slette finanskontoer. For å unngå avvik kan du imidlertid ikke slette en finanskonto hvis dataene fra den er brukt i kontoplanen. Du kan også blokkere uttilsiktet sletting av kontoer i sensitive perioder. Hvis du vil finne ut mer om hvordan du beskytter kontoer mot sletting, kan du gå til [Slett kontoer](finance-setup-chart-accounts.md#delete-accounts).  

## Kodehierarkiet i finanskontoer

Selskaper oppretter vanligvis en hierarkisk struktur i finanskontokoder for å gjenspeile hvor de hører hjemme i kontoplanen. I noen implementeringer angir for eksempel finanskontokoder som begynner med **1**, objektkontoer, mens finanskontokoder som begynner med 3, angir egenkapitalkontoer. I noen områder er det lokale forskrifter for bruk av en standard kontoplan. Hvis du vil hjelpe brukerne med å forstå dette hierarkiet uten å måtte kjenne til den interne kodestrukturen, kan du definere overskrifter og delsummer i kontoplanen som kapsler inn disse interne strukturene.

## Utform kontoplanen

Hver linje i kontoplanen er en finanskonto av en av disse typene:

* Bokføring (kladder kan bokføre linjer til disse kontoene)
* Overskrift (definerer en overskrift i kontoplanen)
* Sum (definerer en formel for en delsum i kontoplanen)
* Fra-sum (definerer en begynnende overskrift for en delsum i kontoplanen). Alle etterfølgende linjer til en Til-sum-linje er rykket inn)
* Til-sum (definerer en sluttoverskrift for en delsum og formelen for den i kontoplanen. Alle etterfølgende linjer etter denne Til-sum-linjen er rykket ut)

En minimalistisk kontoplan kan bestå av bare linjer med bokføringskontoer. Du bruker de fire andre typene til å definere hvordan kontoplanen også viser et regnskap med overskrifter og delsummer. Sammentellingskontoer brukes ofte i finansrapportering.

> [!TIP]
> Hvis du bruker andre kontotyper enn **Bokføring** i kontoplanen, kan du definere forskjellige visninger for å vise de rå bokføringskontoene uten kontotypene for rapporteringstype for sammentelling og overskrifter. Eksempel: Vis bare bokføringskontoer og Skjul blokkerte kontoer.

## Bruk dimensjoner til å forenkle kontoplanen

Dimensjoner er attributter og verdier som kategoriserer poster slik at du kan spore og analysere dem på dokumenter, for eksempel ordrer. Dimensjoner kan for eksempel angi hvilket prosjekt eller hvilken avdeling en post kommer fra. I stedet for å opprette separate finanskonti for hver avdeling og hvert prosjekt, kan du for eksempel bruke dimensjoner som grunnlag for analyse og unngå å måtte opprette en komplisert kontoplan.

Hvis du vil ha mer informasjon om dimensjoner, kan du gå til [Arbeide med dimensjoner](finance-dimensions.md).

## Få en rask oversikt over økonomien din

**Kontoplan**-siden viser konti i en hierarkisk liste som gir rask tilgang til viktig informasjon for hver konto. Listen er imidlertid statisk, og hvis du har mange kontoer, må du kanskje rulle for å vise ulike kontoer. Hvis du bare vil ha en rask oversikt over det grunnleggende, for eksempel bevegelser og saldoer, er siden **Kontoplanoversikt** et nyttig alternativ. Kolonneoppsettet på siden er det samme som siden **Kontoplaner** (men med færre kolonner), slik at den er enklere å forstå. Du kan vise eller skjule de hierarkiske nivåene. For at det skal bli enkelt å bytte mellom sidene er siden **Kontoplanoversikt** tilgjengelig fra **Kontoplan**-siden.

## Tilgang til å opprette og redigere kontoplanen

I en liten organisasjon, for eksempel CRONUS-demoselskapet, kan de fleste brukere redigere kontoplanen, unntatt brukere med en gruppemedlemslisens. Større organisasjoner bruker vanligvis roller og tillatelser til å begrense redigering av kontoplanene. Hvis du er administrator eller har rollen som Forretningssjef eller Regnskapsfører, kan du kontrollere brukertillatelsene for å gi de riktige personene tilgang til relevante tabeller. Hvis du vil ha mer informasjon, kan du gå til [Få en oversikt over en brukers tillatelser](ui-define-granular-permissions.md#get-an-overview-of-a-users-permissions).  


<!-- ## Standard chart of accounts in different regions
Uncomment when we have more examples added to our localization documentation

Some regions have defined standards for the chart of accounts structure you should use in your company. 

Here are some examples of such standards that have been implemented in localized versions of [!INCLUDE[prod_short](includes/prod_short.md)]:

* [Standard chart of accounts in Denmark](localfunctionality/denmark/how-to-set-up-standard-coa.md)
-->

## Anbefalte fremgangsmåter for kontoplan

Her er noen anbefalte fremgangsmåter du kan vurdere når du utvikler og vedlikeholder kontoplanene:

* Lag selskapets kontoplan for å støtte behovene for finansrapportering, slik at ledelsen kan ta strategiske beslutninger.
* Vurder å starte enkelt med færre finanskontoer. Du kan alltid legge til mer detaljerte kontoer om nødvendig.
* Definer overskrifter og delsummer i kontoplanen som summerer de interne strukturene i finanskontoer.
* Bruk dimensjoner til å forenkle kontoplanen. Ikke ha spesifikke finanskontoer for hvert produkt eller hver avdeling.
* Legg til nye finanskontoer etter hvert som de kommer inn, men fjern kontoer fra kontoplanen bare i perioden slutten av finansperioden.

## Se også

[Definere eller endre kontoplanen](finance-setup-chart-accounts.md)    
[Forstå finans](finance-general-ledger.md)  
[Finansiell analyse](bi.md)    
[Oversikt over finans](finance.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
