---
title: Opprette rammeordrer | Microsoft-dokumentasjon
description: "Bruk rammeordrer når en kunde har forpliktet seg til å kjøpe store antall som skal leveres i flere mindre leveringer over en bestemt tidsperiode."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 75e170f10927844ca37a001812e78e062e88c451
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-blanket-sales-orders"></a>Arbeide med rammeordrer
En rammeordre utgjør rammene for en langsiktig avtale mellom deg og kunden.

En rammeordre opprettes som regel når en kunde har forpliktet seg til å kjøpe store antall som skal leveres i flere mindre leveringer over en bestemt tidsperiode. Rammeordrer dekker ofte bare én vare med forhåndsbestemte leveringsdatoer. Hovedgrunnen til å bruke en rammeordre i stedet for en salgsordre er at antallene som angis på en rammeordre ikke påvirker tilgjengeligheten for varene.

På rammeordren kan hver enkelt levering settes opp som en ordrelinje som deretter kan konverteres til en salgsordre på leveringstidspunktet.

Et eksempel på et tilfelle hvor en rammeordre kan brukes er når en kunde ringer og bestiller 1000 enheter av en vare, og de vil at det skal leveres 250 enheter per uke over den neste måneden.

> [!NOTE]
> Rammebestillinger fungerer på lignende måte som rammeordrer. Denne dokumentasjonen dekker ikke rammebestillinger.

## <a name="to-create-a-blanket-sales-order"></a>Slik oppretter du en rammeordre  
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Rammeordrer**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  La **Ordredato**-feltet stå tomt. Når egne ordrer opprettes fra rammeordren, settes ordredatoen for salgsordren til faktisk arbeidsdato.
5. På hurtigfanen **Linjer** oppretter du egne linjer for hver levering. Hvis kunden for eksempel vil ha 1&#160;000 enheter fordelt jevnt på fire uker, angir du fire linjer på 250 enheter hver.   

## <a name="to-create-a-sales-order-from-a-blanket-sales-order"></a>Slik oppretter du en ordre fra en rammeordre  

1.  Hvis du vil opprette en ordre fra noen av linjene i rammemonteringsordren, fjerner du antallet i **Levere (antall)**-feltet på alle linjene som du IKKE vil levere på dette tidspunktet.  
2.  Når du er klar til å opprette bestillinger, velger du handlingen **Lag ordre** og velger deretter **Ja**. Det vises en melding om at rammebestillingen er tilordnet et bestillingsnummer. Vær oppmerksom på at rammebestillingen ikke slettes.  
3.  Velg **OK**.  
4.  Hvis du vil se resultatene av de foregående trinnene, velger du **Linje**-handlingen velger handlingen **Ikke-bokførte linjer** og deretter handlingen **Ordrer**.  
5.  I vinduet **Salgslinjer** velger du ønsket ordre, velger **Linje**-handlingen og deretter **Vis dokument**.  

Følgende gjelder for ordrer når de har blitt opprettet fra rammeordrer:  

- Når rammeordren konverteres til en ordre, inneholder ordren alle linjene fra rammeordren. Linjene der antallet i **Levere (antall)**-feltet ble slettet, vises, men med tomme **Antall**-felt. Du kan velge å la linjene stå, redigere dem eller slette dem.  
- Det er viktig å huske at antallet på ordrelinjen ikke må overstige antallet på den tilordnede rammeordrelinjen. Ellers vil det ikke være mulig å bokføre ordren.  
- Når ordren er bokført som levert og/eller fakturert, oppdateres **Levert (antall)**- og **Fakturert (antall)**-feltene på den tilknyttede rammebestillingen.  
- Rammeordrenummeret og linjenummeret registreres som egenskaper for salgslinjene ved oppretting fra en rammeordre.  
- Når ordrer ikke er opprettet direkte fra rammeordren, men er relatert til den, kan en kobling mellom en ordre og en rammeordre opprettes ved at rammeordrenummeret i **Rammeordrenr**-feltet på ordrelinjen.  
- Når ordren er opprettet for det totale antallet på en rammebestillingslinje, kan ingen andre ordrer opprettes for den samme linjen. Brukere kan ikke angi et antall i feltet **Levere (antall)**. Hvis det imidlertid er behov for å angi flere antall i en rammebestilling, kan verdien i **Antall**-feltet økes, og flere bestillinger kan da opprettes.  
- Den fakturerte rammeordren blir i systemet til den slettes, enten ved å slette individuelle rammeordrer, eller ved å bruke kjørselen **Slett fakturerte rammeordrer**.  
- Hvis en kunde også er registrert som kontakt i modulen Markedsføring, og hvis du har angitt en kode for samhandlingsmal for rammeordre i vinduet **Markedsføringsoppsett**, registreres en samhandling i tabellen Samhandlingspost når du velger **Skriv ut** for å skrive ut rammeordren.

## <a name="to-view-the-status-of-a-blanket-purchase-order"></a>Slik viser du statusen for rammebestillinger  
Du kan vise statusen for en rammeordre i vinduet **Bestillingsstatistikk**. Dette kan være relevant når du begynner å fakturere ordren som opprettes fra rammebestillingen.  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Rammeordrer**, og velg deretter den relaterte koblingen.  
2.  Velg en rammebestilling, og velg deretter **Statistikk**-handlingen.  
3.  På hurtigfanen **Generelt** i **Bestillingsstatistikk**-vinduet vises en informasjonsoversikt over hele bestillingen, basert på det totale antallet i **Antall**-feltene på bestillingslinjene.  

    - På hurtigfanen **Fakturering** vises en informasjonsoversikt basert på det totale antallet i **Fakturer (antall)**-feltene på rammebestillingslinjene.  
    - På hurtigfanen **Levering** vises en informasjonsoversikt basert på det totale antallet i **Motta (antall)**-feltene på rammebestillingslinjene.  
    - På hurtigfanen **Forskudd** vises en informasjonsoversikt over eventuelle forhåndsbetalte beløp.  
    - På hurtigfanen **Leverandør** vises bestemte grunnleggende opplysninger om leverandøren.    

## <a name="to-view-unposted-and-posted-blanket-sales-order-lines"></a>Vise ikke-bokførte og bokførte rammeordrelinjer   
Koblingen mellom rammeordren og den opprinnelige salgsordren, og eventuelle andre salgsdokumenter, beholdes etter bokføring som en liste over bokførte og ikke-bokførte salgsordrefakturalinjer.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Rammeordrer**, og velg deretter den relaterte koblingen.
2. Åpne rammeordren du vil vise.
3. Hvis du vil vise ikke-bokførte poster, velger du den aktuelle linjen, velger **Linje**-handlingen og deretter **Ikke-bokførte linjer**. Velg ett av følgende alternativene.  

    <table>
    <tr>
    <th>Alternativ</th>
    <th>Beskrivelse</th>
    </tr>
    <tr>
    <td>**Bestillinger**</td>
    <td>Angir åpne ordrer knyttet til den valgte linjen.</td>
    </tr>
    <tr>
    <td>**Fakturaer**</td>
    <td>Angir åpne fakturaer som har blitt knyttet til den valgte linjen. Åpne fakturaer knyttes vanligvis til en rammeordre ved at rammeordrenummeret angis på salgsfakturalinjen.</td>
    </tr>
    <tr>
    <td>**Ordreretur**</td>
    <td>Angir åpne ordrereturer som har blitt knyttet til den valgte linjen.</td>
    </tr>
    <tr>
    <td>**Kreditnotaer**</td>
    <td>Angir åpne kreditnotaer som har blitt knyttet til den valgte linjen.</td>
    </tr>
    </table>
4.Hvis du vil vise bokførte poster, velger du den aktuelle linjen, velger **Linje**-handlingen og deretter **Bokførte linjer**. Velg ett av følgende alternativene.  

    <table>
    <tr>
    <th>Alternativ</th>
    <th>Beskrivelse</th>
    </tr>
    <tr>
    <td>**Følgesedler**</td>
    <td>Bokførte følgesedler knyttet til den valgte linjen.</td>
    </tr>
    <tr>
    <td>**Fakturaer**</td>
    <td>Bokførte fakturaer knyttet til den valgte linjen.</td>
    </tr>
    <tr>
    <td>**Retursedler**</td>
    <td>Åpne retursedler som har blitt knyttet til den valgte linjen.</td>
    </tr>
    <tr>
    <td>**Kreditnotaer**</td>
    <td>Bokførte kreditnotaer som har blitt knyttet til den valgte linjen.</td>
    </tr>
    </table>
5.I **Salgslinjer**-vinduet velger du handlingen **Vis dokument** for å vise posten.

## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)  
[Sette opp salg](sales-setup-sales.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

