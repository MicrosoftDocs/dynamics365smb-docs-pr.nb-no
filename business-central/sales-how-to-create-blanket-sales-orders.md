---
title: Arbeide med rammeordrer eller rammebestillinger
description: Bruk rammeordrer når en kunde har forpliktet seg til å kjøpe store antall som skal leveres i flere mindre leveringer over en bestemt tidsperiode. Det samme gjelder kjøp.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '507, 509, 6620, 6622, 6623, 9303, 9310'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Arbeide med rammeordrer eller rammebestillinger

En rammeordre utgjør rammene for en langsiktig avtale mellom deg og kunden. På samme måte bruker du rammebestillinger til å håndtere langsiktige avtaler mellom deg og leverandøren.

En rammeordre opprettes som regel når en kunde har forpliktet seg til å kjøpe store antall som skal leveres i flere mindre leveringer over en bestemt tidsperiode. Rammeordrer dekker ofte bare én vare med forhåndsbestemte leveringsdatoer. Hovedgrunnen til å bruke en rammeordre i stedet for en salgsordre er at antallene som angis på en rammeordre ikke påvirker tilgjengeligheten for varene.

På rammeordren kan hver enkelt levering settes opp som en ordrelinje som deretter kan konverteres til en salgsordre på leveringstidspunktet.

Et eksempel på et tilfelle hvor en rammeordre kan brukes er når en kunde ringer og bestiller 1000 enheter av en vare, og de vil at det skal leveres 250 enheter per uke over den neste måneden.

> [!NOTE]
> Rammebestillinger fungerer på lignende måte som rammeordrer. Denne dokumentasjonen dekker bare rammeordrer.

## Slik oppretter du en rammeordre

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Rammeordrer**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. La **Ordredato**-feltet stå tomt. Når egne ordrer opprettes fra rammeordren, settes ordredatoen for salgsordren til faktisk arbeidsdato.
5. På hurtigfanen **Linjer** oppretter du egne linjer for hver levering. Hvis kunden for eksempel vil ha 1 000 enheter fordelt jevnt på fire uker, angir du fire linjer på 250 enheter hver.  

## Slik oppretter du en ordre fra en rammeordre  

1. Hvis du vil opprette en ordre fra noen av linjene i rammeordren, fjerner du antallet i **Levere (antall)**-feltet på alle linjene som du ikke vil levere på dette tidspunktet.  
2. Når du er klar til å opprette bestillinger, velger du handlingen **Lag ordre** og velger deretter **Ja**. Det vises en melding om at rammebestillingen er tilordnet et bestillingsnummer. Vær oppmerksom på at rammebestillingen ikke slettes.  
3. Velg **OK**.  
4. Hvis du vil se resultatene av de foregående trinnene, velger du **Linje**-handlingen velger handlingen **Ikke-bokførte linjer** og deretter handlingen **Ordrer**.  
5. På siden **Salgslinjer** velger du ønsket ordre, velger **Linje**-handlingen og deretter **Vis dokument**.  

Følgende gjelder for ordrer når de har blitt opprettet fra rammeordrer:  

- Når rammeordren konverteres til en ordre, inneholder ordren alle linjene fra rammeordren. Linjene der antallet i **Levere (antall)**-feltet ble slettet, vises, men med tomme **Antall**-felt. Du kan velge å la linjene stå, redigere dem eller slette dem.  
- Det er viktig å huske at antallet på ordrelinjen ikke må overstige antallet på den tilordnede rammeordrelinjen. Ellers vil det ikke være mulig å bokføre ordren.  
- Når ordren er bokført som levert og/eller fakturert, oppdateres **Levert (antall)**- og **Fakturert (antall)**-feltene på den tilknyttede rammebestillingen.  
- Rammeordrenummeret og linjenummeret registreres som egenskaper for salgslinjene ved oppretting fra en rammeordre.  
- Når ordrer ikke er opprettet direkte fra rammeordren, men er relatert til den, kan en kobling mellom en ordre og en rammeordre opprettes ved at rammeordrenummeret i **Rammeordrenr**-feltet på ordrelinjen.  
- Når ordren er opprettet for det totale antallet på en rammebestillingslinje, kan ingen andre ordrer opprettes for den samme linjen. Brukere kan ikke angi et antall i feltet **Levere (antall)**. Hvis det imidlertid er behov for å angi flere antall i en rammebestilling, kan verdien i **Antall**-feltet økes, og flere bestillinger kan da opprettes.  
- Den fakturerte rammeordren blir i systemet til den slettes, enten ved å slette individuelle rammeordrer, eller ved å bruke kjørselen **Slett fakturerte rammeordrer**.  
- Hvis en kunde også er registrert som kontakt i modulen Markedsføring, og hvis du har angitt en kode for samhandlingsmal for rammeordre på siden **Markedsføringsoppsett**, registreres en samhandling i tabellen Samhandlingspost når du velger **Skriv ut** for å skrive ut rammeordren.

## Slik viser du statusen for en rammeordre

Du kan vise statusen for en rammeordre på siden **Rammeordrestatistikk**. Dette kan være relevant når du begynner å fakturere ordren som opprettes fra rammeordren.  

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Rammeordrer**, og velg deretter den relaterte koblingen.  
2.  Velg en rammeordre, og velg deretter **Statistikk**-handlingen.  
3.  På siden **Rammeordrestatistikk** i hurtigfanen **Generelt** vises informasjonsoversikt over hele bestillingen basert på det totale antallet i **Antall**-feltene på rammebestillingslinjene.  

- På hurtigfanen **Fakturering** vises en informasjonsoversikt basert på det totale antallet i **Fakturer (antall)**-feltene på salgsrammebestillingslinjene.  
- På hurtigfanen **Levering** vises en informasjonsoversikt basert på det totale antallet i **Motta (antall)**-feltene på salgsrammebestillingslinjene.  
- På hurtigfanen **Forskudd** vises en informasjonsoversikt over eventuelle forhåndsbetalte beløp.  
- På hurtigfanen **Leverandør** vises bestemte grunnleggende opplysninger om leverandøren.

## Vise ikke-bokførte og bokførte rammeordrelinjer

Koblingen mellom rammeordren og den opprinnelige salgsordren, og eventuelle andre salgsdokumenter, beholdes etter bokføring som en liste over bokførte og ikke-bokførte salgsordrefakturalinjer.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Rammeordrer**, og velg deretter den relaterte koblingen.
2. Åpne rammeordren du vil vise.
3. Hvis du vil vise ikke-bokførte poster, velger du den aktuelle linjen, velger **Linje**-handlingen og deretter **Ikke-bokførte linjer**. Velg ett av følgende alternativene.  

|Alternativ|Beskrivelse|
|--|--|
|**Bestillinger**|Angir åpne ordrer knyttet til den valgte linjen.|
|**Fakturaer**|Angir åpne fakturaer som har blitt knyttet til den valgte linjen. Åpne fakturaer knyttes vanligvis til en rammeordre ved at rammeordrenummeret angis på salgsfakturalinjen.|
|**Ordreretur**|Angir åpne ordrereturer som har blitt knyttet til den valgte linjen.|
|**Kreditnotaer**|Angir åpne kreditnotaer som har blitt knyttet til den valgte linjen.|

4. Hvis du vil vise bokførte poster, velger du den aktuelle linjen, velger **Linje**-handlingen og deretter **Bokførte linjer**-handlingen. Velg ett av følgende alternativene.  

|Alternativ|Beskrivelse|
|---|----|
|**Følgesedler**|Bokførte følgesedler knyttet til den valgte linjen.|
|**Fakturaer**|Bokførte fakturaer knyttet til den valgte linjen.|
|**Retursedler**|Åpne retursedler som har blitt knyttet til den valgte linjen.|
|**Kreditnotaer**|Bokførte kreditnotaer som har blitt knyttet til den valgte linjen.|

5. På siden **Salgslinjer** velger du handlingen **Vis dokument** for å vise posten.

## Se relatert [Microsoft-opplæring](/training/modules/create-sales-documents-dynamics-365-business-central/)

## Se også

[Salg](sales-manage-sales.md)  
[Opprette rammemonteringsordrer](assembly-how-to-create-blanket-assembly-orders.md)  
[Sette opp salg](sales-setup-sales.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
