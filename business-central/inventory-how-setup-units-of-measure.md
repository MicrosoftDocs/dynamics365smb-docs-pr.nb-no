---
title: Definere vareenheter | Microsoft-dokumentasjon
description: Du kan definere flere enheter for en vare slik at du kan tilordne enheter til varen for følgende formål.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: UOM
ms.date: 10/16/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Definere enheter

Som en del av å definere [!INCLUDE [prod_short](includes/prod_short.md)] kan du definere generelle enheter på **Enheter**-siden. Når du deretter registrerer nye varer, angir du lagerenheten på **varekortet**. Du kan også legge til enheter senere.  

Du kan definere flere enheter for en vare slik at du kan tilordne enheter til varen for følgende formål:

- Tilordne en lagerenhet på varekortet for varen for å definere hvordan den lagres på lageret, og for å bruke den som grunnlaget for konvertering for alternative enheter.
- Tilordne alternative enheter til kjøps-, produksjons- eller salgsdokumenter for å angi hvor mange enheter av lagerenheter du håndterer samtidig i disse prosessene. Du kan for eksempel kjøpe varen på paller, og bare bruke enkeltdeler i produksjonen.

Hvis en vare lagerføres i én enhet, men produseres i en annen, opprettes en produksjonsordre som bruker en produksjonsbunkeenhet til å beregne riktig antall komponenter mens kjørselen **Forny produksjonsordre** kjøres. Ett eksempel på beregning med produksjonsbunkeenhet er når en produsert vare lagerføres i stykker, men produseres i tonn. Hvis du vil ha mer informasjon, kan du se [Arbeide med produksjonsbunkeenhet](production-how-to-use-the-manufacturing-batch-unit-of-measure.md).  

Et annet verktøy som gjør det enklere å arbeide med flere enheter for varer, er muligheten til å angi en avrundingspresisjon for lagerenheter. Ved å angi en avrundingspresisjon får du veiledning om hva noen skal angi for en gitt forretningsprosess, og bidrar til å redusere avrundingsproblemer. Når du bruker alternative enheter, bidrar verdien i feltet **Antall per enhet** til å beregne antallet i lagerenheten, noe som kan føre til avrundingsproblemer. La oss for eksempel anta at du mottar en boks som inneholder seks varer. Når boksen ankommer til lageret, oppdager du at én av de seks varene mangler. Du bestemmer deg for ikke å bokføre mottaket av én boks, men i stedet endre antallet mottatt til fem av seks stykker. Det vil føre til mottak av 4,99998 stykker, i stedet for fem. På siden **Enheter** kan du angi en verdi som konverterer antallet til et tall som er enklere å forstå, i feltet **Avrundingspresisjon for antall**. Hvis du fortsetter med eksemplet, setter vi inn **1** i feltet for å runde opp til fem stykker.

## Slik definerer du enheter

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Enheter** og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**. Det settes inn en ny, tom linje.  
3. Fyll ut feltene. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
4. Hvis du vet at organisasjonen vil selge varer med denne enhetskoden til kunder i andre land/områder, kan du legge til oversettelser.  
    1. Velg koden du vil definere oversettelser for, og velg deretter handlingen **Oversettelser**.
    2. I **Språkkode**-feltet velger du rullegardinpilen for å vise en oversikt over tilgjengelige språkkoder. Velg språkkoden du vil opprette en oversettelse for, og klikk deretter OK-knappen for å kopiere koden til feltet.
    3. Angi den teksten i feltet **Beskrivelse**.
5. Gjenta de forrige trinnene for eventuelle tilleggsenheter du vil legge til.  

Når du registrerer en ny vare, kan du velge lagerenheten fra oversikten over enheter som du nå har definert. Du kan også definere flere enheter for en vare.  

## Slik definerer du flere vareenheter

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.
2. Åpne varekortet som du vil definere alternative enheter for.
3. Velg handlingen **Enheter**. Siden **Vareenheter** åpnes.
4. Hvis feltet **Lagerenhet** på varekortet er fylt ut, er denne enheten allerede konfigurert.
5. Velg handlingen **Ny**. Det settes inn en ny, tom linje.
6. I feltet **Kode** angir du navnet på enheten. Du kan også velge feltet for å velge fra enhetskodene som finnes i databasen.
7. I feltet **Antall per enhet** angir du hvor mange enheter av lagerenheten den nye enheten inneholder.
8. I **Høyde**-, **Bredde**-, **Lengde**- og **Vekt**-feltene kan du også angi eksakte opplysninger om vareenheten, slik at [!INCLUDE [prod_short](includes/prod_short.md)] kan beregne hvor mange av hver vareenhet som kan plasseres på en bestemt hylle. **Kubikkinnhold**-feltet beregnes automatisk basert på **høyde**, **bredde** og **lengde**.

    Hvis noen av disse feltene inneholder en annen verdi enn 0, brukes dette målet i alle prosesser som omfatter plassering av varer på en hylle: plasseringer, flyttinger, mottak, leveringer, plukkinger og justeringer. [!INCLUDE [prod_short](includes/prod_short.md)] kontrollerer summen av hver fysiske enhet til varene som plasseres og de varene som allerede finnes på hyllen, opp mot maksimal størrelse eller andre mål som får plass på en hylle i henhold til det hyllekapasitetsprinsippet som du valgte på lokasjonskortet for varen. Du må med andre ord bruke samme enhet for hver dimensjon på tvers av alle vareenheter – bruk for eksempel kilo eller pund for vekt, men være konsekvent.
9. Gjenta trinn 5 til 7 for å definere alle alternative enheter som du vil bruke i ulike prosesser for denne varen.

    I **Lagerenhet**-feltet nederst i vinduet, kan du vise eller endre varens lagerenhet. Du kan også endre lagerenheten i **Lagerenhet**-feltet på varekortet. På **Enheter**-siden må lagerenheter ha verdien **1** i feltet **Antall per enhet**.

Du kan nå bruke de alternative enhetene på kjøps-, produksjons- og salgsdokumenter. Hvis du vil ha mer informasjon, kan du se [Angi en standardenhetskode for kjøpstransaksjoner](#to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions).  

## Slik definerer du enhetsoversettelser

Når du selger varer til kunder i utlandet, kan du angi enheten på kundens språk. Dette kan du gjøre ved å angi oversettelser for enheter.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Enheter** og velg deretter den relaterte koblingen.
2. Velg koden du vil definere oversettelser for, og velg deretter handlingen **Oversettelser**.
3. I **Språkkode**-feltet velger du rullegardinpilen for å vise en oversikt over tilgjengelige språkkoder. Velg språkkoden du vil opprette en oversettelse for, og klikk deretter OK-knappen for å kopiere koden til feltet.
4. Angi den teksten i feltet **Beskrivelse**.
5. Gjenta trinn 2 til 4 for enhetskodene og språkene du vil angi oversettelser for.

## Angi en standardenhetskode for kjøpstransaksjoner

Hvis du vanligvis kjøper eller selger i andre enheter enn lagerenhetene, kan du angi en separat enhet for innkjøp og salg. Hvis du vil gjøre dette, må du definere enheter på siden **Vareenheter**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.
2. Åpne det aktuelle varekortet du vil angi en standardkode for salgs- eller kjøpsenhet for.
3. For salg åpner du siden **Vareenheter** i feltet **Salgsenhet** på hurtigfanen **Fakturering**.
4. For kjøp åpner du siden **Vareenheter** under **Kjøpsenhet** på hurtigfanen **Etterfylling**.
5. Velg koden du vil definere som standardenhet for salg eller kjøp, og velg deretter **OK**-knappen.

## Se også

[Arbeide med produksjonsbunkeenhet](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)  
[Registrer nye varer](inventory-how-register-new-items.md)  
[Håndtere lager](inventory-manage-inventory.md)  
[Håndtere kjøp](purchasing-manage-purchasing.md)  
[Håndtere salg](sales-manage-sales.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
